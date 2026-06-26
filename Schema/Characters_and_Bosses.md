# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Characters & Bosses

> **Associated Files:** `data/characters/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 600

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2985 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Visual parameters and animation bindings. | 2609 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage logic on contact. | 2344 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1910 ||
| [`variant_of`](./Enums.md#enum-variant_of) | Enum | Specifies the base character that this entry is a variant of. | 1195 ||
| [`properties`](#object-properties) | Object | General engine properties. | 600 ||
| [`stats`](#object-stats) | Object | Core character metrics (Health, Strength, etc.). | 461 ||
| [`abilities`](#object-abilities) | Object | Lists the ability IDs the character possesses. | 460 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 459 ||
| [`sound`](#object-sound) | Object | Audio bindings. | 62 ||
| [`distance_to_ally`](./Enums.md) | Number | Weight for the AI to consider distance to allies when making decisions. | 55 | 2 |
| [`distance_to_character`](./Enums.md) | Integer | Weight for the AI to consider distance to any character (ally or enemy). | 55 | 0 |
| [`distance_to_enemy`](./Enums.md) | Number | Weight for the AI to consider distance to enemies. | 55 | 0 |
| [`face_closest_enemy`](./Enums.md) | Integer | If non-zero, the AI will prioritize facing the closest enemy. | 55 | 0 |
| [`preferred_distance`](./Enums.md) | Enum / Integer | Specifies the preferred distance from the target; can be a number or keywords like 'reach'. | 55 | reach |
| [`total_distance_moved`](./Enums.md) | Number | Weight for the AI to consider the total distance moved by the unit. | 55 | 0 |
| [`equipment`](#object-equipment) | Object | List of item IDs the character spawns equipped with. | 44 ||
| [`accurate_knockback`](./Enums.md) | Boolean | If false, the AI will not account for accurate knockback calculations. | 32 | false |
| [`buff_ally`](./Enums.md) | Integer | Weight for the AI to prioritize buffing allies. | 32 | 0 |
| [`buff_enemy`](./Enums.md) | Integer | Weight for the AI to consider buffing enemies (negative values discourage). | 32 | 0 |
| [`buff_self`](./Enums.md) | Integer | Weight for the AI to prioritize buffing self. | 32 | 0 |
| [`consider_overkill`](./Enums.md) | Boolean | If true, the AI will factor in overkill damage when evaluating attacks. | 32 | false |
| [`consider_secondary_damage`](./Enums.md) | Boolean | If true, the AI will consider secondary damage effects. | 32 | false |
| [`consider_total_damage`](./Enums.md) | Boolean | If true, the AI will consider the total damage output of an action. | 32 | false |
| [`damage_ally`](./Enums.md) | Number | Weight for the AI to consider damaging allies (negative values discourage). | 32 | 0 |
| [`damage_ally_corpse`](./Enums.md) | Integer | Weight for the AI to consider damaging ally corpses. | 32 | 0 |
| [`damage_enemy`](./Enums.md) | Integer | Weight for the AI to prioritize damaging enemies. | 32 | 0 |
| [`damage_enemy_corpse`](./Enums.md) | Number | Weight for the AI to consider damaging enemy corpses. | 32 | 0 |
| [`damage_self`](./Enums.md) | Number | Weight for the AI to consider self-damage (negative values discourage). | 32 | 2 |
| [`debuff_ally`](./Enums.md) | Number | Weight for the AI to consider debuffing allies. | 32 | 0 |
| [`debuff_enemy`](./Enums.md) | Integer | Weight for the AI to prioritize debuffing enemies. | 32 | 0 |
| [`debuff_self`](./Enums.md) | Number | Weight for the AI to consider self-debuff. | 32 | 2 |
| [`heal_ally`](./Enums.md) | Integer | Weight for the AI to prioritize healing allies. | 32 | 0 |
| [`heal_enemy`](./Enums.md) | Integer | Weight for the AI to consider healing enemies. | 32 | 0 |
| [`heal_self`](./Enums.md) | Integer | Weight for the AI to prioritize self-healing. | 32 | 0 |
| [`kill_ally`](./Enums.md) | Integer | Weight for the AI to consider killing allies (negative avoids). | 32 | 0 |
| [`kill_enemy`](./Enums.md) | Number | Weight for the AI to prioritize killing enemies. | 32 | 0 |
| [`negative_weight_scale`](./Enums.md) | Number | Multiplier applied to negative decision weights to adjust their influence. | 32 | .99 |
| [`revive_ally_corpse`](./Enums.md) | Integer | Weight for the AI to prioritize reviving ally corpses. | 32 | 0 |
| [`revive_enemy_corpse`](./Enums.md) | Integer | Weight for the AI to consider reviving enemy corpses. | 32 | 0 |
| [`spawn_object`](./Enums.md) | Integer | Weight for the AI to consider spawning objects. | 32 | 0 |
| [`spawn_object_distance_to_ally`](./Enums.md) | Number | Weight for the AI to consider distance to allies when spawning objects. | 32 | .0001 |
| [`spawn_object_distance_to_enemy`](./Enums.md) | Number | Weight for the AI to consider distance to enemies when spawning objects. | 32 | 0 |
| [`spend_mana_scale`](./Enums.md) | Number | Multiplier applied to mana spending decisions to adjust AI's resource management. | 32 | .99 |
| [`alt_spawn_pool`](#object-alt_spawn_pool) | Object | Alternative pools to draw minions from. | 18 ||
| [`brain`](./Enums.md#enum-brain) | Enum | Specifies the AI brain type (e.g., NoBrain, PlayerBrain, GenericBrain). | 5 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 5 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 5 ||
| [`scale`](./Enums.md#enum-scale) | Number | A multiplier for the unit's overall scale, affecting size and related properties. | 5 ||
| [`flat_cast_bonus`](./Enums.md) | Integer | A flat bonus added to the unit's casting ability, overriding normal cast probability. | 5 | 99999 |
| [`randomness`](./Enums.md) | Integer | The amount of randomness added to the AI's movement decisions, with higher values causing more erratic behavior. | 5 | 50 |
| [`cap_distance_to_ally`](./Enums.md) | Integer | The maximum distance in tiles the AI will maintain from an ally unit. | 4 | 2 |
| [`pattern`](#object-pattern) | Object | AI sequence logic. | 3 ||
| [`consider_aoe`](./Enums.md) | Boolean | If true, the AI will consider area-of-effect attacks when evaluating moves. | 3 | false |
| [`danger_avoidance`](./Enums.md) | Number | A multiplier influencing how strongly the AI avoids dangerous tiles or situations. | 3 | 20 |
| [`distance_to_aggro_target`](./Enums.md) | Integer | The preferred distance in tiles the AI tries to maintain from its aggro target. Negative values indicate closeness. | 3 | -1 |
| [`distance_to_corpse`](./Enums.md) | Number | The preferred distance in tiles the AI tries to maintain from corpses. Negative values indicate attraction. | 3 | 0 |
| [`simple`](./Enums.md) | Boolean | If true, the AI uses a simplified decision-making process, ignoring complex evaluations. | 3 | true |
| `partial_animation_suffix` | Enum / Integer | Examples: `3, 2, 1` | 2 ||
| `end_turn_on_formswitch` | Boolean | If true, the unit's turn ends immediately after switching forms. | 2 ||
| [`cap_distance_to_enemy`](./Enums.md) | Integer | The maximum distance in tiles the AI will attempt to maintain from enemies. | 2 | 2 |
| [`distance_to_water`](./Enums.md) | Number | The preferred distance in tiles the AI tries to maintain from water tiles. Negative values indicate attraction. | 2 | -1 |
| [`face_aggro_target`](./Enums.md) | Integer | The priority weight for the AI to face its aggro target. Higher values increase likelihood. | 2 | 10 |
| [`spawn_object_preferred_distance`](./Enums.md) | Integer | The preferred distance in tiles at which the AI will spawn objects. | 2 | 5 |
| `animation_suffix` | Enum / Integer | Examples: `3, 4, 2` | 1 ||
| [`ai_if_spawned_as_enemy`](#object-ai_if_spawned_as_enemy) | Object | AI logic override used only if the character is spawned as an enemy. | 1 ||
| `consider_spells` | Boolean | If true, the AI will consider using spells when evaluating actions. | 1 ||
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 1 ||
| [`cap_distance_to_character`](./Enums.md) | Integer | The maximum distance in tiles the AI will maintain from a specific character. | 1 | 2 |
| [`cap_total_distance_moved`](./Enums.md) | Integer | The maximum total distance in tiles the AI is allowed to move per turn. | 1 | 1 |
| [`consider_aggro_target_enemy`](./Enums.md) | Boolean | If true, the AI considers the aggro target's enemies when making decisions. | 1 | true |
| [`count_nomove_in_eval`](./Enums.md) | Boolean | If false, the AI does not count moves that result in no movement during evaluation. | 1 | false |
| [`distance_to_center`](./Enums.md) | Integer | The preferred distance in tiles the AI tries to maintain from the center of the map. Negative values indicate attraction. | 1 | -1 |
| [`exclude_characters_tagged`](./Enums.md) | Enum | Specifies a tag that excludes certain characters from AI movement considerations. | 1 | siren |
| [`face_camera`](./Enums.md) | Integer | If true, the spawned entity's sprite always rotates to face the camera, useful for billboard effects or UI elements. | 1 | 1000 |
| [`lava`](./Enums.md) | Integer | A weight value influencing the AI's preference for moving onto lava tiles. Higher values increase preference. | 1 | 5 |
| [`tall_grass`](./Enums.md) | Integer | A weight value influencing the AI's preference for moving onto tall grass tiles. Higher values increase preference. | 1 | 5 |

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
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 517 ||
| [`movieclip`](./Enums.md#enum-movieclip) | Array / Enum | Specifies the movieclip asset used for the room's visual representation, such as 'SmallUFO' or 'Worm'. | 461 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 409 ||
| `shadow_size` | Number | A multiplier for the size of the unit's shadow. Values above 1 increase shadow size. | 151 ||
| [`scale`](./Enums.md#enum-scale) | Number | A multiplier for the unit's overall scale, affecting size and related properties. | 149 ||
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 149 ||
| [`custom_cat_data`](./Enums.md#enum-custom_cat_data) | Enum | Specifies a custom visual data identifier for cat characters, such as 'Grey' or 'TankCat'. | 127 ||
| [`water_mask`](./Enums.md#enum-water_mask) | Enum | Specifies the size or shape of the water mask applied to the unit's graphics, such as 'medium' or 'big'. | 83 ||
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array | Alternative animation sets for a cat class, defined as pairs of animation states and their replacements. | 47 ||
| [`spawnin_animation`](./Strings.md#string-spawnin_animation) | Enum | Specifies the animation played when the entity spawns, such as 'digUp', 'grow', or 'summonspawnin', controlling its visual entry. | 37 ||
| `piece_alt_frame` | Integer | The frame index used for an alternate piece of the unit's animation. | 27 ||
| [`shadow`](./Enums.md#enum-shadow) | Enum | Specifies the shadow type asset used for the unit, such as 'None' or 'BigSlimeShadow'. | 23 ||
| `move_speed_sync_frames` | Number | The number of frames over which the unit's movement animation syncs, controlling animation speed. | 20 ||
| `no_splatter` | Boolean | If true, prevents blood splatter visual effect when the object pops and spawns. | 17 ||
| [`projectile_spawn_offset`](./Arrays.md#array-projectile_spawn_offset) | Array | An [x, y] offset in tiles for where projectiles spawn relative to the unit's position. | 17 ||
| [`tint`](./Arrays.md#array-tint) | Array / Enum | Specifies a color tint applied to the unit's graphics, either as a named color or an RGBA array [r g b a]. | 17 ||
| [`move_speed_multiplier`](./Enums.md#enum-move_speed_multiplier) | Number | A multiplier for the unit's movement animation speed. Values above 1 increase speed. | 16 ||
| `dont_sink` | Boolean | If true, the unit does not visually sink into water tiles. | 14 ||
| `art_flip` | Integer | Specifies the horizontal flip direction for the unit's art. -1 flips the art horizontally. | 7 ||
| [`depth_offset`](./Enums.md#enum-depth_offset) | Number | An offset to the unit's visual depth sorting layer, affecting draw order on the map. | 6 ||
| `four_way_animations` | Boolean | If true, the unit has separate animations for the four cardinal directions. | 4 ||
| `show_infinity_damage_warning` | Boolean | If true, displays a warning when the unit has infinite damage. | 3 ||
| `always_huge_mask` | Boolean | If true, always renders the unit's portrait mask as huge. | 2 ||
| [`default_attack_animation`](./Enums.md#enum-default_attack_animation) | Enum | Specifies the default attack animation name for the unit. | 2 ||
| [`desc`](./Strings.md#string-desc) | Enum | Localization key for the character's desc. | 2 ||
| `shade_occluded_objects` | Boolean | If true, shades objects that are occluded by this unit. | 2 ||
| `no_horizontal_flip` | Boolean | If true, prevents the unit's sprite from flipping horizontally when facing left. | 1 ||
| [`override_portrait`](./Enums.md#enum-override_portrait) | Enum | Specifies an alternate portrait to use for the unit. | 1 ||
| `randomize_starting_frame` | Boolean | If true, randomizes the starting animation frame of the unit. | 1 ||
| `status_display_count_max` | Integer | The maximum number of status effect icons displayed at once. | 1 ||
| [`non_blocking_animations`](./Arrays.md#array-non_blocking_animations) | Array | List of animation names that do not block other animations from playing simultaneously. | 1 ||

</details>

---

### Object: `damage_instance`


**Definition:** Object defining the combat math and status effects applied upon successful hit.  
**Total Count:** 2346


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2344 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging impact triggers. | 1787 ||

</details>

---

### Object: `passives`


**Definition:** Object listing intrinsic passive modifiers.  
**Total Count:** 733


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Alert`](./Characters_and_Bosses.md#object-alert), [`AllAlive`](./Characters_and_Bosses.md#object-allalive), [`BellyFull`](./Characters_and_Bosses.md#object-bellyfull), [`Big`](./Characters_and_Bosses.md#object-big), [`BigHolding`](./Characters_and_Bosses.md#object-bigholding), [`BigHoldingCat`](./Characters_and_Bosses.md#object-bigholdingcat), [`Bishop`](./Characters_and_Bosses.md#object-bishop), [`BlackHole`](./Characters_and_Bosses.md#object-blackhole), [`Bomb`](./Characters_and_Bosses.md#object-bomb), [`Boris`](./Characters_and_Bosses.md#object-boris), [`Bully`](./Characters_and_Bosses.md#object-bully), [`CaveBaby`](./Characters_and_Bosses.md#object-cavebaby), [`CaveMan`](./Characters_and_Bosses.md#object-caveman), [`CaveManSpear`](./Characters_and_Bosses.md#object-cavemanspear), [`CaveWoman`](./Characters_and_Bosses.md#object-cavewoman), [`CaveWomanHasCat`](./Characters_and_Bosses.md#object-cavewomanhascat), [`Charging`](./Characters_and_Bosses.md#object-charging), [`Close`](./Characters_and_Bosses.md#object-close), [`Cultist`](./Characters_and_Bosses.md#object-cultist), [`Default`](./Characters_and_Bosses.md#object-default), and 97 more...

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2039 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | An object defining status effects to apply on basic attacks, with optional conditions. | 133 ||
| [`FormChanger`](#object-formchanger) | Object | Defines form-changing behavior, containing sub-forms with their own passives, abilities, and AI. | 106 ||
| [`Brace`](./Enums.md) | Integer | The amount of flat damage reduction applied to the source. | 94 | 99 |
| [`Trample`](./Enums.md) | Integer | The number of tiles this character can move through enemies, dealing damage or applying effects equal to the value. | 88 | 3 |
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 65 | 2 |
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object | A damage instance object that triggers when the unit is hit by melee attacks while this passive is active. | 59 ||
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 52 | 2 |
| [`StatusEachTurnEnd`](Cat_Mutations.md#object-statuseachturnend) | Object | Status effects that are applied to the unit at the end of each turn. | 49 ||
| [`Robot`](#object-robot) | Integer / Object | Marks the unit as a robot. An integer enables the passive; an object can specify alternate energized effects or allow self-energize. | 47 | 1 |
| [`ElementImmune`](./Enums.md) | Enum | Specifies an element (e.g., Fire, Ice) the unit is immune to. | 39 | Ice |
| [`DeathRattle`](#object-deathrattle) | Enum / Object | Defines an ability or explosion that triggers upon the unit's death. | 35 | BBExplode |
| [`FormChangeWhileHasStatus`](#object-formchangewhilehasstatus) | Object | Forces a form change when the unit has or lacks a specific status effect. | 35 ||
| [`CounterAttack`](Cat_Mutations.md#object-counterattack) | Array / Enum / Object | Specifies the ability name used for counterattacking when hit. | 34 | [GSScream] |
| [`StatusImmunity`](./Enums.md) | Array / Enum | List of status effects the unit is immune to. | 34 | [Burn] |
| [`StatusOnKill`](Cat_Mutations.md#object-statusonkill) | Object | Status effects applied to the unit whenever it kills an enemy. | 29 ||
| [`StatusOnTookDamage`](Cat_Mutations.md#object-statusontookdamage) | Object | Status effects applied to the unit whenever it takes damage. | 29 ||
| [`SpawnThingOnDamage`](Cat_Mutations.md#object-spawnthingondamage) | Object | Object specifying an entity to spawn when the unit takes damage, with optional conditions. | 28 ||
| [`ImmediateAbilityReaction`](#object-immediateabilityreaction) | Array / Enum / Object | Triggers an ability immediately in response to an event, optionally with conditions like even if stunned. | 26 | [ManglerFumbleEven] |
| [`Undead`](./Enums.md) | Integer | Marks the unit as undead. Higher values may indicate undead type or tier. | 25 | 1 |
| [`AbilityReaction`](#object-abilityreaction) | Enum / Object | Specifies an ability to trigger as a reaction when certain conditions are met. | 23 | MoonWormCurl |
| [`SpawnOnDeath`](#object-spawnondeath) | Enum / Object | Specifies the entity to spawn upon the unit's death. | 21 | BiggestFood |
| [`AddMovement`](./Enums.md) | Integer | The number of extra movement tiles the unit gains per turn. | 20 | 2 |
| [`BossRewards`](#object-bossrewards) | Object | Defines the loot table (common/rare items) dropped by a boss. | 20 ||
| [`BirdRewards`](#object-birdrewards) | Object | Defines rewards given by bird allies, including item pools and conditional odds. | 18 ||
| [`Buddy`](#object-buddy) | Enum / Object | Specifies the character template of the unit's buddy (paired ally). | 17 | Guillotina3Head |
| [`CharacterLightSource`](#object-characterlightsource) | Object | Defines a dynamic light source emitted by the unit, with color, glow, and size. | 16 ||
| [`HealthPickup`](#object-healthpickup) | Object | Defines health pickup behavior: number of stacks, frame range, stored food value, and whether anything can eat it. | 16 ||
| [`KineticSpikes`](./Enums.md) | Integer | The number of Kinetic Spikes stacks applied, which deal damage back to attackers when the unit is hit. | 15 | 5 |
| [`RevengeDamage`](Abilities_and_Spells.md#object-revengedamage) | Object | An object specifying the effects (e.g., Marked, Charmed, Petrify) applied to the attacker when the unit takes damage. | 15 ||
| [`AddCorpseHealth`](./Enums.md) | Integer | The amount of additional health a corpse has when the unit dies. | 14 | -999 |
| [`AllStatsUp`](./Enums.md) | Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 14 | 2 |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance to dodge incoming attacks. | 14 | 50 |
| [`InnateElement`](./Enums.md) | Enum | Specifies the unit's innate elemental type (Fire, Ice, Electric, etc.). | 14 | Water |
| [`WaterWalk`](./Enums.md) | Integer | If set to 1, allows the unit to move over water tiles as if they were normal terrain. | 14 | 1 |
| [`DeathRattleRevive`](#object-deathrattlerevive) | Enum / Object | Defines an ability or effect that triggers when the unit would die but revives instead. | 13 | HCHumanDie |
| [`TransformOnDeath`](./Enums.md) | Array / Enum | Specifies the character template to transform into upon death. | 13 | [Hive] |
| [`AbilityHealthThreshold`](#object-abilityhealththreshold) | Object | Triggers an ability when the unit's health drops below a specified threshold. | 12 ||
| [`NoHealthOnlyShield`](./Enums.md) | Integer | Marks the unit as having no health bar, only a shield. | 12 | 1 |
| [`ReflectProjectiles`](#object-reflectprojectiles) | Integer / Object | The percentage chance to reflect projectiles back at the attacker. | 12 | 100 |
| [`SpawnThingOnDeath`](./Enums.md) | Enum | Specifies a specific entity to spawn upon death, distinct from standard spawns. | 12 | Boulder |
| [`MoveWhenDamaged`](Cat_Mutations.md#object-movewhendamaged) | Enum / Object | Defines movement behavior triggered when the unit takes damage, including the ability to use and movement weights. | 11 | move |
| [`CoinPickup`](./Enums.md) | Integer | The amount of currency provided by this pickup. | 10 | 4 |
| [`LimitDamage`](./Enums.md) | Integer | The maximum damage the unit can take per hit (limiter). | 10 | 1 |
| [`MoveTowardsDamageSource`](#object-movetowardsdamagesource) | Enum / Object | Causes the unit to move towards the source of damage, using a specified move ability. | 10 | MoveOne |
| [`StripStatuses`](./Enums.md) | Integer | Removes all status effects from the unit when activated (value likely toggle). | 10 | 1 |
| [`AddTag`](./Enums.md) | Enum | Specifies a unit tag (e.g., fetus, plant, bug) to add to the unit. | 9 | fetus |
| [`BackstabImmunity`](./Enums.md) | Integer | If set to 1, the unit is immune to backstab damage. | 9 | 1 |
| [`Flying`](./Enums.md) | Integer | The number of stacks of the Flying status effect applied to the unit. | 9 | 1 |
| [`LimitHeal`](./Enums.md) | Integer | The maximum amount of health the unit can heal per instance. | 9 | 0 |
| [`MissChance`](./Enums.md) | Integer | The percentage chance that the unit's attacks will miss. | 9 | 20 |
| [`MovementReaction`](#object-movementreaction) | Object | Triggers an ability when an entity moves near the unit. | 9 ||
| [`PoisonThorns`](./Enums.md) | Integer | Applies Poison stacks to any unit that attacks this unit in melee. | 9 | 3 |
| [`SmallRockBehavior`](#object-smallrockbehavior) | Integer / Object | Defines the damage, knockback, and chain properties of small rocks spawned by asteroid enemies. | 9 | 0 |
| [`StatusCollector`](#object-statuscollector) | Object | A container of status effects applied to the unit upon pickup or activation. | 9 ||
| [`TransformOnElementInfluence`](#object-transformonelementinfluence) | Object | Transforms the unit into another object when influenced by a specific element (e.g., Fire cooks food). | 9 ||
| [`FadeInsteadOfDie`](./Enums.md) | Integer | The number of stacks of FadeInsteadOfDie, causing the unit to fade out and despawn instead of dying when reaching zero health. | 8 | 1 |
| [`FormChangeOffMap`](#object-formchangeoffmap) | Object | Switches between off-map and on-map forms when the unit moves between areas. | 8 ||
| [`FormChangeOnElementInfluence`](#object-formchangeonelementinfluence) | Object | Changes the unit's form when influenced by an element, with optional exclusion and effects. | 8 ||
| [`PermanentMadness`](./Enums.md) | Integer | If set to 1, the Madness status is permanent and will never expire; can use an alias for the status. | 8 | 1 |
| [`Plant`](./Enums.md) | Integer | The number of stacks of the Plant status effect applied to the unit. | 8 | 1 |
| [`RandomizeAIWeightsEachTurn`](./Enums.md) | Array | List of AI weight sets that are randomly assigned each turn for behavior variation. | 8 | [chubs_and_nubs_blind] |
| [`StatusOnDie`](Cat_Mutations.md#object-statusondie) | Object | Defines statuses or effects that are applied when the unit dies. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |
| [`AbilityWhenBuddyDies`](./Enums.md) | Enum | Specifies the ability triggered when the unit's buddy dies. | 7 | Guillotina2Rage |
| [`AddElementsToBasicAttack`](./Enums.md) | Enum | Specifies the elemental damage type added to the unit's basic attack. | 7 | Fire |
| [`AddInitiative`](./Enums.md) | Integer | The amount to add to the unit's initiative score, affecting turn order. | 7 | 999999 |
| [`AlphaTurns`](./Enums.md) | Integer | The number of additional alpha turns the unit receives at the start of combat. | 7 | 1 |
| [`ChanceToSpitOnDamage`](#object-chancetospitondamage) | Object | Gives a chance (flat or per-damage) to use a spit ability when damaged. | 7 ||
| [`DebuffImmunity`](./Enums.md) | Integer | Grants immunity to debuffs (value likely toggle or tier). | 7 | 1 |
| [`MinimumKnockbackFromAllDamage`](./Enums.md) | Integer | Enforces a minimum knockback distance from all incoming damage. | 7 | 1 |
| [`OverrideMaxHealth`](./Enums.md) | Integer | Overrides the unit's maximum health to a specific value. | 7 | 25 |
| [`SecurityBotProtect`](#object-securitybotprotect) | Object | Defends a tagged ally by using an ability or move when threatened. | 7 ||
| [`SetSpellCosts`](./Enums.md) | Integer | Overrides all spell costs to a fixed value. | 7 | 0 |
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 7 | 2 |
| [`StatusOnEndMove`](Cat_Mutations.md#object-statusonendmove) | Object | Defines statuses or effects applied when the unit finishes moving. | 7 ||
| [`TransformInXTurns`](#object-transforminxturns) | Object | Transforms the unit into another object after a set number of turns (stacks). | 7 ||
| [`AddDamage`](./Enums.md) | Integer | Adds a flat amount to the unit's damage output (can be negative). | 6 | 2 |
| [`CaveFamilyEnrage`](#object-cavefamilyenrage) | Object | Triggers an enrage ability for cave family members when few allies remain alive. | 6 ||
| [`DelayedAutoRevive`](#object-delayedautorevive) | Object | Automatically revives the unit after a specified number of rounds with a given health percentage. | 6 ||
| [`Divide4OnDeath`](./Enums.md) | Enum | Specifies the unit or object spawned when this unit dies via the Divide4 mechanic. | 6 | MedSlime |
| [`DodgeChance_Status`](./Enums.md) | Integer | The percentage of dodge chance granted by this status effect. | 6 | 66 |
| [`FormChangeWhilePrimingAbility`](#object-formchangewhileprimingability) | Object | Determines the form changes applied when the unit is or is not priming an ability. | 6 ||
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 6 | 5 |
| [`IgnoreTiles`](./Enums.md) | Integer | If set to 1, the unit ignores tile effects while moving. | 6 | 1 |
| [`KaijuKnockbackImmune`](./Enums.md) | Integer | The intensity of immunity to knockback from Kaiju-size characters; 1 full immunity. | 6 | 1 |
| [`StatusOnTookDamageFromAbility`](Cat_Mutations.md#object-statusontookdamagefromability) | Object | Defines statuses applied when the unit takes damage from an ability. | 6 ||
| [`StunImmunity`](#object-stunimmunity) | Integer / Object | If 1, the unit is immune to stun. As an object, can specify advanced behavior such as cleanse on apply. | 6 | 1 |
| [`TagGreed`](./Enums.md) | Enum | Specifies the item tag that the unit is attracted to or collects greedily. | 6 | bishop_hat |
| [`TileTrail`](./Enums.md) | Enum | Specifies the tile type (e.g., CreepTile, WaterTile) left behind as the character moves. | 6 | ShadowTile |
| [`YOffset`](./Enums.md) | Number | A vertical offset multiplier used to adjust the unit's visual position on the tile. | 6 | -.18 |
| [`AddHiddenTag`](./Enums.md) | Enum | Adds a hidden tag to the unit for internal logic or quest tracking. | 5 | hitler_clone_fetus |
| [`Angel`](./Enums.md) | Integer | If set to 1, grants angelic properties, such as revival or holy damage. | 5 | 1 |
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Enum / Object | An object defining an ability that is automatically cast each round, with optional force display or ignore stun. | 5 | SpiderReturn |
| [`Burn`](./Enums.md) | Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 5 | 2 |
| [`FaceShield`](./Enums.md) | Integer | A boolean flag (1 or 0) indicating whether the unit has a face shield that blocks specific effects. | 5 | 0 |
| [`InjuryImmunity`](./Enums.md) | Integer | The number of stacks of InjuryImmunity, granting immunity to receiving injuries (permanent wounds) for that many instances. | 5 | 1 |
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit is immune to knockback effects. | 5 | 1 |
| [`MoveTowardsKillers`](#object-movetowardskillers) | Enum / Object | Causes the unit to move towards its killers, using the specified ability and optional character filter. | 5 | ReaperRevenge |
| [`SharkySmellsBlood`](./Enums.md) | Integer | If set to 1, enables blood-sensing behavior, often targeting wounded enemies. | 5 | 1 |
| [`StartOffMap`](./Enums.md) | Integer | If set to 1, the unit begins the encounter off the map. | 5 | 1 |
| [`TransformOnDeathImmediately`](#object-transformondeathimmediately) | Enum / Object | Determines the unit or object this unit transforms into immediately upon death. | 5 | NoHead |
| [`AbilityAfterEnemyCastSpell_Stackable`](./Enums.md) | Enum | Specifies the ability triggered after an enemy casts a spell; this effect can stack. | 4 | ThornUp |
| [`AddMaxHealth`](./Enums.md) | Integer | The amount to add to the unit's maximum health. Negative values reduce max health. | 4 | -25 |
| [`AddMeleeKnockback`](./Enums.md) | Integer | The amount of knockback added to the unit's melee attacks. | 4 | 2 |
| [`AddStatusToWeapons`](#object-addstatustoweapons) | Object | A dictionary of status effects to apply to the unit's weapon attacks. | 4 ||
| [`AddTemporaryEffectsToBasicAttack`](Cat_Mutations.md#object-addtemporaryeffectstobasicattack) | Object | Adds temporary statuses or effects to the unit's basic attack for the current turn. | 4 ||
| [`Ammo`](./Enums.md) | Integer | The change in ammunition count; positive values add ammo, negative values consume ammo. | 4 | 3 |
| [`BackstabAllDirections`](./Enums.md) | Integer | If set to 1, the unit can backstab enemies from any direction. | 4 | 1 |
| [`BaitAura`](#object-baitaura) | Object | An aura that draws enemy aggro; 'range' specifies the radius in tiles. | 4 ||
| [`Bird`](./Enums.md) | Enum | Specifies the bird type associated with this unit, used for bird-related mechanics. | 4 | CookedChickenLeg |
| [`BuffImmunity`](./Enums.md) | Integer | If set to 1, the unit is immune to buffs. As an object, can exclude specific buffs. | 4 | 1 |
| [`ChanceToBackflip`](Cat_Mutations.md#object-chancetobackflip) | Object | Defines the chance and ability used for the unit to backflip and dodge an incoming attack. | 4 ||
| [`ChangeTileOnPop`](./Enums.md) | Enum | The tile type that appears when this unit is destroyed (popped). | 4 | OilTile |
| [`CountAsCorpse`](./Enums.md) | Integer | If set to 1, the unit is considered a corpse for relevant effects. | 4 | 1 |
| [`DisplayDangerAOE`](./Enums.md) | Enum | The ability name whose area of effect is displayed to the player as a danger zone. | 4 | TheChild_Wrath |
| [`ExtraDispersedTurns`](./Enums.md) | Integer | Additional turns granted, distributed across the turn order. | 4 | 1 |
| [`GroundFlopper`](./Enums.md) | Enum | Specifies the ability used for movement while flopping on the ground. | 4 | DefaultMove |
| [`LoopingSoundWhileAlive`](./Enums.md) | Enum | The name of a looping sound effect played while the unit is alive. | 4 | Bomb_FuseLoop |
| [`PassiveWhenAffectedByElement`](Cat_Mutations.md#object-passivewhenaffectedbyelement) | Object | Grants additional passive effects when the unit is under the effects of a specified element. | 4 ||
| [`PassiveWhenDead`](#object-passivewhendead) | Object | A set of passive effects that remain active after the unit's death. | 4 ||
| [`PrioritizeFarAwayTargets`](./Enums.md) | Integer | Weight for AI to prioritize targeting units farther away. | 4 | 10 |
| [`StatusOnGainCoins`](#object-statusongaincoins) | Object | A dictionary of status effects applied when the unit collects coins. | 4 ||
| [`Trapper`](#object-trapper) | Object | Configures a trap ability that the unit places, including range and AI avoidance. | 4 ||
| [`WeremanTransformationReceiver`](./Enums.md) | Enum | The transformation name applied when the unit is affected by a were-man curse. | 4 | CaveWomanDropTransform |
| [`ArmorPickup`](#object-armorpickup) | Object | Pickup Logic: Defines what happens when an armor item is collected. | 3 ||
| [`AbilityWhenTaggedCharacterMovesNear`](Cat_Mutations.md#object-abilitywhentaggedcharactermovesnear) | Object | Triggers a specified ability when a character with a specific tag moves within range. | 3 ||
| [`AddStatusToSpells`](#object-addstatustospells) | Object | A dictionary of status effects to apply to the unit's spell attacks. | 3 ||
| [`AggroTargetIsCurrentTurn`](./Enums.md) | Integer | If set to 1, the unit's AI prioritizes targeting the unit currently taking their turn. | 3 | 1 |
| [`BaseStatMultiply`](./Enums.md) | Number | A multiplier applied to the unit's base stats. | 3 | .5 |
| [`BonusTurnPattern`](./Enums.md) | Array | An array defining the turn order pattern for awarding bonus turns. | 3 | [0] |
| [`CanMutateTo`](./Enums.md) | Array / Enum | List of units this unit can mutate into. | 3 | [Leaper] |
| [`DigestDeadBodies`](./Enums.md) | Enum | Specifies the ability that allows this unit to consume dead bodies. | 3 | MoonHead_Digest |
| [`ExtraMovePoints`](./Enums.md) | Integer | Additional movement points granted each turn. | 3 | 1 |
| [`FormChangeHealthThreshold`](#object-formchangehealththreshold) | Object | Configuration for changing the unit's appearance based on current health relative to a threshold. | 3 ||
| [`ManaPickup`](#object-manapickup) | Object | Configures a mana pickup spawned by this unit, with number of stacks and frame animation range. | 3 ||
| [`MimicSpawnerAttacks`](./Enums.md) | Integer | Number of times the unit mimics its spawner's attacks. Negative values may disable. | 3 | -1 |
| [`MinimumKnockbackFromPhysicalAttacks`](./Enums.md) | Integer | The minimum knockback distance inflicted by physical attacks on this unit. | 3 | 1 |
| [`MutateViaAbility`](./Enums.md) | Enum | Specifies the ability that triggers a mutation in this unit. | 3 | BBTransformMutant |
| [`PrioritizeHitDifferentTargets`](./Enums.md) | Integer | If set to 1, the unit's AI prefers to attack different targets when possible. | 3 | 1 |
| [`ProtectTargetedAllies`](#object-protecttargetedallies) | Object | Configures protection behavior for allies being targeted, using a specified ability or action. | 3 ||
| [`RandomPassivePool`](#object-randompassivepool) | Object | A pool of passive groups from which a random set is applied. | 3 ||
| [`RunInXTurns`](./Enums.md) | Integer | Number of turns after which the unit will run away. | 3 | 2 |
| [`SharePickupsWithSpawner`](./Enums.md) | Integer | If set to 1, pickups collected are also given to the unit's spawner. | 3 | 0 |
| [`SpawnCreepOnHit`](./Enums.md) | Integer | If set to 1, the unit spawns creep tiles when it is hit. | 3 | 1 |
| [`StrengthUp`](./Enums.md) | Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 3 | 2 |
| [`SupportFormChangeInsteadOfRun`](#object-supportformchangeinsteadofrun) | Enum / Object | Determines a form change that occurs when support is triggered, instead of fleeing. | 3 | Attacker |
| [`TileTrail_Ahead`](./Enums.md) | Enum | Specifies the tile type placed on the tile ahead of the character's movement direction. | 3 | WaterTile |
| [`WeaponsDontLoseDurability`](./Enums.md) | Integer | If true, weapons do not lose durability when used. | 3 | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 ||
| [`ai`](#object-ai) | Object | Examples: `{ ... }` | 2 ||
| `partial_animation_suffix` | Enum / Integer | Examples: `4, 2` | 2 ||
| [`AbilityOnRoundEnd`](#object-abilityonroundend) | Object | Defines an ability that is executed at the end of each round. | 2 ||
| [`AggroTargetIsBuddy`](./Enums.md) | Integer | If true, the unit's aggro target is its buddy (friendly ally). | 2 | 1 |
| [`AllDamageImmune_IncludingSpeculative`](./Enums.md) | Integer | If true, the unit is immune to all damage, including speculative/undetermined damage sources. | 2 | 1 |
| [`AlwaysHitDifferentTargets`](./Enums.md) | Integer | If true, each attack must hit a different target than the previous one. | 2 | 1 |
| [`BungaEntrance`](#object-bungaentrance) | Object | Defines a special entrance behavior, including warrior tag, ability, health threshold, and whether it triggers even if stunned. | 2 ||
| [`CCImmunity`](./Enums.md) | Integer | If true, the unit is immune to crowd control effects. | 2 | 1 |
| [`CanShield`](./Enums.md) | Integer | If true, the unit can use a shield to block attacks. | 2 | 1 |
| [`ChanceToDisableActionsIfNotCharmed`](./Enums.md) | Integer | The percentage chance that the unit will disable actions of enemies that are not charmed. | 2 | 75 |
| [`ChangeTileOnDeath`](./Enums.md) | Enum | Specifies the type of tile that appears on the unit's death. | 2 | WaterTile |
| [`CherubimReaction`](#object-cherubimreaction) | Object | Defines leave and return abilities for a cherubim-like behavior. | 2 ||
| [`CreateGlobalModifiers`](Abilities_and_Spells.md#object-createglobalmodifiers) | Object | An object containing global modifier effects to apply after the time delay. | 2 ||
| [`DemonicGlyphFrames`](./Enums.md) | Integer | The number of frames for a demonic glyph effect. | 2 | 1 |
| [`DiesToElement`](#object-diestoelement) | Enum / Object | Specifies the element that kills the unit instantly, optionally with an 'instant' flag. | 2 | Wind |
| [`DissuadeInstakills`](./Enums.md) | Integer | If true, the unit discourages or prevents instant kills. | 2 | 1 |
| [`ExpireOnSpawnerTurnEnd`](./Enums.md) | Integer | If true, the unit expires (is removed) at the end of the spawner's turn. | 2 | 1 |
| [`FaceLastDamage`](#object-facelastdamage) | Integer / Object | When set, the unit faces the direction of the last damage taken, optionally with turn animations. | 2 | 1 |
| [`FinalBossShield`](./Enums.md) | Enum | Specifies the shield ability used by a final boss form. | 2 | None |
| [`FormChangeDuringWeatherElement`](#object-formchangeduringweatherelement) | Object | Defines a form change that occurs when a specific weather element is present. | 2 ||
| [`FreePathfindElement`](./Enums.md) | Enum | Specifies a terrain element that the unit can pathfind through without penalty. | 2 | Water |
| [`GoopWalk`](./Enums.md) | Integer | If true, the unit can walk on goop tiles without penalty. | 2 | 1 |
| [`ImmobilePassive`](./Enums.md) | Integer | If true, the unit is immobile and cannot move. | 2 | 1 |
| [`InfiniteRebirth`](#object-infiniterebirth) | Object | Defines the parameters for infinite rebirth, including health percentage, player cat health, and whether immediate. | 2 ||
| [`KaijuWinCon`](./Enums.md) | Enum | Specifies the win condition name for a kaiju encounter (e.g., 'zaratana' or 'pyrophina'). | 2 | zaratana |
| [`MagicDamageImmune`](./Enums.md) | Integer | If true, the unit is immune to magic damage. | 2 | 1 |
| [`MamaCatAnimations`](./Enums.md) | Integer | If true, the unit uses mama cat specific animations. | 2 | 1 |
| [`MiniVolcanoReaction`](./Enums.md) | Enum | Specifies the ability/effect triggered when a mini volcano event occurs. | 2 | ThrobShot_Reaction |
| [`MotherTumorSpawnInCapture`](#object-mothertumorspawnincapture) | Object | Defines the spawn behavior and form changes when Mother Tumor captures a unit. | 2 ||
| [`MoveAwayFromDamageSource`](#object-moveawayfromdamagesource) | Object | Specifies the ability used by the unit to move away from the source of damage. | 2 ||
| [`PassiveWhileHasStatus`](Cat_Mutations.md#object-passivewhilehasstatus) | Object | Grants additional passive effects while the unit is afflicted with a specified status. | 2 ||
| [`PassiveWhileNotHasStatus`](#object-passivewhilenothasstatus) | Object | Defines a set of passives that are only active while the unit does not have a specific status. | 2 ||
| [`PrioritizeAggroTarget`](./Enums.md) | Integer | If true, the unit will prioritize its aggro target over other enemies. | 2 | 1 |
| [`PrioritizePlayerCats`](./Enums.md) | Integer | If true, the unit prioritizes player cats as targets. | 2 | 1 |
| [`PrioritizeWeakestEnemy`](./Enums.md) | Integer | If true, the unit prioritizes the weakest enemy. | 2 | 1 |
| [`SafeDoomed`](./Enums.md) | Integer | The number of turns until the target is instantly killed when this counter reaches zero, but unlike standard Doomed, it does not inflict injuries upon death. | 2 | 1 |
| [`SharePickups`](#object-sharepickups) | Object | If set, the unit shares pickups with allies, optionally including coins. | 2 ||
| [`SlotMachineRollPool`](#object-slotmachinerollpool) | Object | Defines the weighted pool of results for a slot machine ability. | 2 ||
| [`StatusAfterXTurns`](#object-statusafterxturns) | Object | Defines a status effect that is applied after a certain number of turns, with optional forced ability use. | 2 ||
| [`StatusOnSpawnIn`](#object-statusonspawnin) | Object | Defines statuses applied to the unit when it spawns into the battle. | 2 ||
| [`SurviveAt1HP`](./Enums.md) | Integer | If true, the unit survives lethal damage at 1 HP. | 2 | 1 |
| [`TowerDefenseReflex`](./Enums.md) | Enum | Specifies the reflex ability (e.g., 'attack') used in tower defense mode. | 2 | attack |
| [`TransformOnElementInfluencex`](#object-transformonelementinfluencex) | Object | Defines a transformation that occurs when the unit is influenced by a specific element. | 2 ||
| [`TransformWhenBuddyDies`](./Enums.md) | Enum | Specifies the form or object the unit transforms into when its buddy dies. | 2 | UltraOrnstein |
| [`UncappedHP`](./Enums.md) | Integer | If true, the unit's HP is not capped and can exceed normal limits. | 2 | 1 |
| [`UnlockOrientation`](./Enums.md) | Integer | If true, the unit's orientation is unlocked and can face any direction. | 2 | 1 |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | Specifies the ability name the unit will use at the end of each round. | 2 | KirbySpit |
| `animation_suffix` | Enum / Integer | Examples: `1` | 1 ||
| `uifloaters_offset` | Number | Examples: `2.2` | 1 ||
| [`AbilityOnBattleStart_UseAI`](./Enums.md) | Enum | Specifies an ability that is used at battle start via AI. | 1 | TheCreator_SpawnCloneTeam |
| [`AddStatusToReceivedDamage`](#object-addstatustoreceiveddamage) | Object | Defines a status effect applied to the attacker when the unit receives damage, possibly conditional. | 1 ||
| [`AdvancedTint`](./Enums.md) | Array | An array of color values for an advanced tint effect on the unit. | 1 | [0] |
| [`AdventureTokenPassivePool`](#object-adventuretokenpassivepool) | Object | Defines a pool of passives that can be granted through adventure tokens. | 1 ||
| [`AggroTargetIsGovernedByHitEffect`](#object-aggrotargetisgovernedbyhiteffect) | Object | Defines whether aggro target is determined by hit effects, with optional 'enemies_only' flag. | 1 ||
| [`AggroTargetIsLastEnemyThatDealtDamage`](./Enums.md) | Integer | If true, the unit's aggro target is the last enemy that dealt damage to it. | 1 | 1 |
| [`AggroTargetIsLowestHealthEnemyTillItDies`](./Enums.md) | Integer | If true, the unit's aggro target is the lowest health enemy until that enemy dies. | 1 | 1 |
| [`AggroTargetIsLowestMaxHealthCat`](./Enums.md) | Integer | If true, the unit's aggro target is the cat with the lowest max health. | 1 | 1 |
| [`AlienBeastDangerZones`](./Enums.md) | Array | An array of ability names that define danger zones for the Alien Beast. | 1 | [AlienBeastPuke] |
| [`AlienBeastEyeStalks`](./Enums.md) | Integer | The number of eye stalk projectiles fired in a spread pattern. | 1 | 3 |
| [`AllSpellsCostActPoints`](./Enums.md) | Integer | The number of action points required to cast any spell. | 1 | 1 |
| [`AllStatsAura`](#object-allstatsaura) | Object | An aura that modifies all stats of units with a specific tag within range. | 1 ||
| [`AvoidDamagingCharmedEnemies`](./Enums.md) | Integer | If set to 1, the unit will not deal damage to charmed enemies. | 1 | 1 |
| [`AwardCoinsOnDeath`](./Enums.md) | Integer | The number of coins awarded to the player when this unit dies. | 1 | 10 |
| [`BasicAIDangerZone`](./Enums.md) | Integer | The radius in tiles around the unit considered dangerous for basic AI movement. | 1 | 2 |
| [`BattlefieldUniqueRandomPassive`](#object-battlefielduniquerandompassive) | Object | A set of passives that are randomly assigned to one unit per battlefield. | 1 ||
| [`BlackHolePassive`](./Enums.md) | Integer | If set to 1, enables the black hole form behavior (attracts and damages nearby units). | 1 | 1 |
| [`BloatEyePassive2`](./Enums.md) | Enum | Specifies the name of the secondary movement ability for the Bloat Eye form. | 1 | BloatEyeMovement2 |
| [`BlockAllDamage`](./Enums.md) | Integer | If set to 1, the unit blocks all incoming damage. | 1 | 1 |
| [`BombBehavior`](./Enums.md) | Integer | If set to 1, enables bomb behavior (detonates after a delay or on contact). | 1 | 1 |
| [`BungaCheers`](#object-bungacheers) | Object | A set of cheer and boo reactions based on ally/enemy damage and death triggers. | 1 ||
| [`CapReceivedDamage`](./Enums.md) | Integer | The maximum amount of damage the unit can receive per hit. | 1 | 1 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Specifies which cat body part IDs to transform into upon applying the effect. | 1 ||
| [`CerberubsAggroTargetBehavior`](#object-cerberubsaggrotargetbehavior) | Object | Defines the form names for default and alert aggro states of Cerberubs heads. | 1 ||
| [`ChanceToFormChangeOnAbilityDamage`](#object-chancetoformchangeonabilitydamage) | Object | Defines a percentage chance and target form when the unit takes ability damage. | 1 ||
| [`ChaosBossFormChangeGuide`](#object-chaosbossformchangeguide) | Object | Defines the sequence and health thresholds for Chaos boss form changes between active and passive piece groups. | 1 ||
| [`ChaosBossPieces`](#object-chaosbosspieces) | Object | Defines the lists of active and passive piece character names that compose the Chaos boss. | 1 ||
| [`ChaosHeadDropIn`](#object-chaosheaddropin) | Object | Defines the spawn tag, ability, and music change for a Chaos head dropping in from off-screen. | 1 ||
| [`ConjureBonusAbility`](./Enums.md) | Enum | Specifies the bonus ability that the unit gains, either by class or by specific ability name. | 1 | random |
| [`CounterAttackAfterEnemyCastSpell`](./Enums.md) | Enum | Specifies the ability name the unit uses to counter-attack after an enemy casts a spell. | 1 | Telekinesis |
| [`CrowAttackLink`](./Enums.md) | Integer | If set to 1, the crow's attack is linked to another unit's position. | 1 | 1 |
| [`DamageFromBehindOnly`](./Enums.md) | Integer | If set to 1, the unit can only deal damage from behind a target. | 1 | 1 |
| [`DemonicGlyphStealer`](./Enums.md) | Integer | If set to 1, the unit can steal demonic glyphs from other units. | 1 | 1 |
| [`DiceBehavior`](#object-dicebehavior) | Object | Defines the dice size and knockback damage for the dice roll ability. | 1 ||
| [`DicerArt`](./Enums.md) | Array | An array of ability IDs that the Dicer unit can randomly use. | 1 | [50] |
| [`DieWhenOnlyGolemsLeft`](./Enums.md) | Integer | If set to 1, the unit dies when only golem-type allies remain on the battlefield. | 1 | 1 |
| [`DieWhenSpawnerDies`](./Enums.md) | Integer | If set to 1, the unit dies immediately when its spawner is killed. | 1 | 1 |
| [`DiesToPiercingAndSpikes`](#object-diestopiercingandspikes) | Object | An object with a deferred flag; if true, the unit is killed by piercing damage or spike tiles. | 1 ||
| [`DisableSpells`](./Enums.md) | Integer | If set to 1, the unit cannot cast any spells. | 1 | 1 |
| [`Disguised`](./Enums.md) | Integer | If set to 1, the unit appears as a different unit type until revealed. | 1 | 1 |
| [`DisguisedTrapper`](./Enums.md) | Enum | Specifies the ability name triggered when the disguised unit is revealed. | 1 | FearMelee |
| [`DisplayBuddyCatOnSpawn`](./Enums.md) | Integer | The number of buddy cat units displayed as attached to this unit on spawn. | 1 | 3 |
| [`DivineShield`](./Enums.md) | Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 2 |
| [`DivineShieldPickup`](./Enums.md) | Integer | If set to 1, the unit can pick up divine shield charges from the environment. | 1 | 1 |
| [`DodgeChanceWithBlindSpot`](./Enums.md) | Integer | The percentage chance to dodge attacks when the attacker is in the unit's blind spot. | 1 | 25 |
| [`DodgeWhenTargeted`](#object-dodgewhentargeted) | Object | Defines the dodge ability and tile trail used when the unit is targeted by an attack. | 1 ||
| [`DustCloudBehavior`](./Enums.md) | Integer | If set to 1, enables the dust cloud behavior (obscures vision on movement). | 1 | 1 |
| [`Dybbuk1HPTracker`](./Enums.md) | Integer | If set to 1, tracks that the Dybbuk unit has exactly 1 HP remaining. | 1 | 1 |
| [`DybbukPossessionFallback`](#object-dybbukpossessionfallback) | Object | Defines the form and exit ability when the Dybbuk fails to possess a target. | 1 ||
| [`ElectricArcs`](./Enums.md) | Integer | If set to 1, the unit emits electric arcs that hit nearby enemies. | 1 | 1 |
| [`ElementWeakness`](./Enums.md) | Enum | Specifies the damage element (e.g. Fire) the unit is weak against. | 1 | Fire |
| [`EnrageOnDamage`](./Enums.md) | Integer | If set to 1, the unit gains enrage buffs when taking damage. | 1 | 1 |
| [`EraseSpawnCoins`](./Enums.md) | Integer | If set to 1, the unit prevents coins from being spawned on death. | 1 | 1 |
| [`EventBounterHunterPassive`](./Enums.md) | Integer | If set to 1, enables the event bounty hunter passive (awards extra rewards for killing event units). | 1 | 1 |
| [`ExtraTurnsPerTaggedUnit`](./Enums.md) | Enum | Specifies the tag name of units that grant the unit extra turns. | 1 | sprout |
| [`FaceAwayLastDamage`](#object-faceawaylastdamage) | Object | An object controlling animations and forcing the unit to face away from the last damage source. | 1 ||
| [`FinalBossBeamQueue`](#object-finalbossbeamqueue) | Object | Defines the queue, release, and transform abilities for the final boss beam attack sequence. | 1 ||
| [`FinalBossBecomeTheChild`](#object-finalbossbecomethechild) | Object | Defines the spawn and transformation sequence for the final boss becoming TheChild form. | 1 ||
| [`FinalBossHitCountdownBoris`](#object-finalbosshitcountdownboris) | Object | An object defining the stacks, icons, and forced ability for the Boris-form hit countdown mechanic. | 1 ||
| [`FinalBossHitCountdownExplosive`](#object-finalbosshitcountdownexplosive) | Object | An object defining the stacks, icons, and forced ability for the Explosive-form hit countdown mechanic. | 1 ||
| [`FinalBossHitCountdownHoly`](#object-finalbosshitcountdownholy) | Object | An object defining the stacks, icons, and forced ability for the Holy-form hit countdown mechanic. | 1 ||
| [`FinalBossPupils`](#object-finalbosspupils) | Object | An object defining the visual pupil tracking parameters for a final boss, including radius, virtual head position, look offset, and teleport tracking halflife. | 1 ||
| [`FinalBossShieldHealth`](#object-finalbossshieldhealth) | Object | An object containing an array of shield health values for each visual state (clean, scuffed, cracked1, cracked2, etc.). | 1 ||
| [`FinalBossSyncAnimations`](#object-finalbosssyncanimations) | Object | An object linking a boss's animations to another character's form change abilities for synchronized visual transitions. | 1 ||
| [`FlingObjectsOnTop`](./Enums.md) | Integer | The number of objects flung upward from this entity when triggered. | 1 | 8 |
| [`FlushmasterCelebration`](./Enums.md) | Enum | Specifies the celebration animation or state for the Flushmaster unit. | 1 | celebrate |
| [`ForceDodgeEverything`](./Enums.md) | Integer | If 1, the unit will automatically dodge all incoming attacks regardless of hit chance. | 1 | 1 |
| [`FormChangeWhenBuddyDies`](./Enums.md) | Enum | Determines which form the unit changes into when its buddy or ally dies. | 1 | Rage |
| [`FullBlockEverything`](./Enums.md) | Integer | If 1, the unit will block all incoming attacks, reducing damage to zero. | 1 | 1 |
| [`FullBlockEverythingTo0Damage`](./Enums.md) | Integer | If 1, the unit blocks all incoming attacks and reduces damage to zero (variant of FullBlockEverything). | 1 | 1 |
| [`GasCanBehavior`](./Enums.md) | Integer | If 1, enables the gas can behavior where the unit explodes or releases gas when destroyed. | 1 | 1 |
| [`GasCloudBehavior2`](./Enums.md) | Integer | If set to 2, enables a secondary behavior for gas clouds, likely periodic damage or spread. | 1 | 2 |
| [`GeminiTwin`](./Enums.md) | Integer | If 1, marks this unit as one of the Gemini twin cats, linking their behavior. | 1 | 1 |
| [`GlobalManaDrainAura`](./Enums.md) | Integer | The radius of an aura that drains mana from all units on the battlefield; negative value indicates a specific mode. | 1 | -1 |
| [`GoopImmunity`](./Enums.md) | Integer | If 1, the unit is immune to goop status effects. | 1 | 1 |
| [`GuillotinaDeathHead`](./Enums.md) | Integer | If 1, spawns a death head (like the Guillotina boss's head) upon dying. | 1 | 1 |
| [`HPAltStates`](#object-hpaltstates) | Object | An object defining alternative visual states based on current HP thresholds, with a clipname and frame indices. | 1 ||
| [`HarpoonTrapPassive`](./Enums.md) | Enum | Specifies the type of harpoon trap behavior, such as pulling in enemies. | 1 | HarpoonTrapPull |
| [`HealNeighborsEachTurn`](#object-healneighborseachturn) | Object | An object defining the amount of healing applied to neighboring allies each turn, with a stack count and ally-only flag. | 1 ||
| [`HiddenDoomed`](./Enums.md) | Integer | The number of turns before the unit becomes doomed while hidden. | 1 | 2 |
| [`HitlerExecute`](#object-hitlerexecute) | Object | An object defining the execution parameters for the Hitler boss, including the clone tag, ability used, and HP threshold. | 1 ||
| [`IceBlockBehavior`](./Enums.md) | Integer | If 1, enables ice block behavior where the unit freezes and blocks movement. | 1 | 1 |
| [`IllusionTint`](./Enums.md) | Integer | The number of stacks of IllusionTint, applying a visual tint to the unit to mark it as an illusion or summoned copy. | 1 | 1 |
| [`InheritSpawnerStats`](./Enums.md) | Integer | If 1, the spawned unit inherits the stats and passives of its spawner. | 1 | 1 |
| [`InsertIntoBackgroundPlaceholder`](./Enums.md) | Integer | If 1, the unit is inserted into a background placeholder for layered rendering. | 1 | 1 |
| [`JohnnyNeedsWashing`](#object-johnnyneedswashing) | Object | An object defining the two visual forms for Johnny, washed and unwashed. | 1 ||
| [`JohnnyWasher`](./Enums.md) | Enum | Specifies the ability used to wash Johnny, transforming him to his washed form. | 1 | BBTransformZealot |
| [`LegacySpawnSavedCatIfExists`](./Enums.md) | Enum | Specifies the legacy save key used to spawn a previously stolen cat if it exists in the save data. | 1 | Legacy_Marshmallow_StolenCatID |
| [`LockOrientationFaceTile`](./Enums.md) | Array | The tile coordinate that the unit's orientation is locked to face, preventing rotation. | 1 | [0] |
| [`ManglerMonsterPassive`](./Enums.md) | Enum | Specifies the ability used by the Mangler Monster when executing its dash attack. | 1 | ManglerMonsterDashAttack |
| [`MegaDinoDropController`](#object-megadinodropcontroller) | Object | An object controlling the leg and head drop phases of the Mega Dino boss, including abilities and stable leg count. | 1 ||
| [`ModularPickup`](#object-modularpickup) | Object | An object defining the effects and sound when a unit picks up a modular item, such as cleansing statuses. | 1 ||
| [`MonkCatReactionAbilities`](#object-monkcatreactionabilities) | Object | An object mapping action types (move, attack, spell, trinket) to specific abilities used by the Monk Cat for reactions. | 1 ||
| [`MoonHeadCrackedVisual`](./Enums.md) | Enum | Specifies the visual state (e.g., 'Cracked') for the Moon Head when damaged. | 1 | Cracked |
| [`MotherGrowController`](#object-mothergrowcontroller) | Object | An object controlling the growth of the Mother boss by consuming tumors, with damage specifications. | 1 ||
| [`MotherTumorPassive`](#object-mothertumorpassive) | Object | An object defining the behavior of Mother Tumor units, including form restrictions, animation, and growth ability. | 1 ||
| [`Mount`](#object-mount) | Object | An object defining the abilities used to enter and eject from a mount, and the death rattle explosion. | 1 ||
| [`MoveAfterAnyAttemptedAttack`](#object-moveafteranyattemptedattack) | Object | An object defining the movement behavior after any attack attempt, using a weighted decision tree. | 1 ||
| [`MoveAwayWhenEnemyAdjacent`](#object-moveawaywhenenemyadjacent) | Object | An object defining the behavior to move away when an enemy is adjacent, specifying the move ability and frequency. | 1 ||
| [`MultiSpawnOnDeath`](#object-multispawnondeath) | Object | An object defining multiple units spawned upon death, with the object type and count range. | 1 ||
| [`MulticatHeads`](./Enums.md) | Integer | The number of additional heads on a Multicat unit, affecting attacks and appearance. | 1 | 0 |
| [`MutateAfterXTurns`](./Enums.md) | Integer | The number of turns after which the unit mutates into a different form. | 1 | 3 |
| [`MuteDemonicGlyphDisplay`](./Enums.md) | Integer | If 1, suppresses the visual display of demonic glyphs on the unit. | 1 | 1 |
| [`OrthogonalAIDangerZone`](./Enums.md) | Integer | The range in tiles for an orthogonal AI danger zone, affecting movement decisions. | 1 | 10 |
| [`PackHunting`](./Enums.md) | Integer | If 1, the unit will coordinate attacks with nearby allies of the same type. | 1 | 1 |
| [`Phasing`](./Enums.md) | Integer | If 1, the unit can phase through obstacles and walls. | 1 | 1 |
| [`ReturnBoundItemOnBattleEnd`](./Enums.md) | Integer | If 1, any bound item (like a phantom mask) is returned to the unit after battle ends. | 1 | 1 |
| [`RunWhenKittensDead`](./Enums.md) | Integer | If 1, the unit will flee or retreat when all kittens (player cats) are dead. | 1 | 1 |
| [`RunWhenLastPlayerCatIsCharmed`](#object-runwhenlastplayercatischarmed) | Object | An object defining the behavior to retreat when the last player cat is charmed, with mid-turn decision allowance and save key. | 1 ||
| [`ScalingAttackAnimation`](#object-scalingattackanimation) | Object | An object defining attack animations that scale based on damage or stat thresholds, with default and threshold-based animations. | 1 ||
| [`SkipFirstRounds`](#object-skipfirstrounds) | Object | An object defining how many initial rounds the unit is hidden and the chance to pop out each round. | 1 ||
| [`SpawnCreepOnHitKnockback`](./Enums.md) | Integer | If 1, the unit spawns creep terrain when hitting an enemy with knockback. | 1 | 1 |
| [`SpawnerCatDataReference`](./Enums.md) | Integer | The character ID of the cat to spawn as a familiar or copy. | 1 | 1 |
| [`SpewerAltGraphics`](#object-speweraltgraphics) | Object | Maps elemental types to alternate sprite sets for the Spewer's visual appearance. | 1 ||
| [`SpreadWater`](./Enums.md) | Integer | The number of tiles of water spread when the unit moves or is destroyed. | 1 | 1 |
| [`SproutsGrantMovement`](./Enums.md) | Integer | The amount of bonus movement granted when collecting sprouts. | 1 | 1 |
| [`StartDead`](./Enums.md) | Integer | The probability (as a percentage) that the unit begins the encounter dead. | 1 | 100 |
| [`StatusEachTurnBeginIfHasStatus`](#object-statuseachturnbeginifhasstatus) | Object | Defines a status effect applied at the start of each turn if the unit already has a specific status, optionally consuming it. | 1 ||
| [`StatusEachTurnEndIfEnabledAtStartOfTurn`](#object-statuseachturnendifenabledatstartofturn) | Object | Triggers a passive effect at the end of each turn if the unit's form was enabled at the start of that turn. | 1 ||
| [`StatusOnEnemyConfused`](#object-statusonenemyconfused) | Object | Defines a status effect or ability triggered when an enemy becomes confused. | 1 ||
| [`StatusOverlappingCharactersAndDie`](#object-statusoverlappingcharactersanddie) | Object | Defines a status effect applied to any unit that overlaps this unit's tile, then destroys this unit. | 1 ||
| [`StatusWhenStatusCompletelyRemoved`](#object-statuswhenstatuscompletelyremoved) | Object | Defines an effect or ability triggered when a tracked status effect is completely removed from the unit. | 1 ||
| [`SupportDieInsteadOfRun`](#object-supportdieinsteadofrun) | Object | Causes a support-type unit to play alternate death animations instead of fleeing when its health is depleted. | 1 ||
| [`SwimmingFormChange`](#object-swimmingformchange) | Object | Defines the character forms used when entering and leaving water tiles. | 1 ||
| [`SyncFormsWithBuddy`](#object-syncformswithbuddy) | Object | Causes this unit to share its form changes with a linked buddy, applying a fallback form if no buddy exists. | 1 ||
| [`T3HitlerSpawningPhase`](#object-t3hitlerspawningphase) | Object | Defines the weighted list of spawn abilities used during the T3Hitler boss's spawning phase. | 1 ||
| [`TVBotDisableAttack`](./Enums.md) | Integer | If set to 1, disables the TVBot's ability to attack. | 1 | 1 |
| [`TVBotDisableMove`](./Enums.md) | Integer | If set to 1, disables the TVBot's ability to move. | 1 | 1 |
| [`TVBotDisableSpells`](./Enums.md) | Integer | If set to 1, disables the TVBot's ability to use spells. | 1 | 1 |
| [`TVBotScreen`](#object-tvbotscreen) | Object | Maps TV bot form names to their integer channel IDs, controlling which behavior mode is active. | 1 ||
| [`TakeWeaponFromSpawner`](./Enums.md) | Integer | If set to 1, the unit copies the weapon of the character that spawned it. | 1 | 1 |
| [`Tall`](./Enums.md) | Integer | If set to 1, the unit occupies two vertical tiles and is immune to low-hitting attacks. | 1 | 1 |
| [`TallTumorManaBurn`](./Enums.md) | Enum | Specifies the mana burn type for the TallTumor's special attack. | 1 | TT_ManaBurn |
| [`Terminator2Chase`](./Enums.md) | Enum | Specifies the movement type used by the T2 Terminator when chasing its target. | 1 | move |
| [`Terminator2Run`](#object-terminator2run) | Object | Defines the movement ability and weight-based pathfinding logic for the T2 Terminator's run form. | 1 ||
| [`TerminatorChase`](#object-terminatorchase) | Object | Defines the movement ability and reaction ability used by the T1 Terminator when chasing its target. | 1 ||
| [`TerminatorSkin`](#object-terminatorskin) | Object | Defines a damage-absorbing skin with a status and a segmented health pool (groups). | 1 ||
| [`TileElementDamageImmunity`](./Enums.md) | Enum | Determines which tile element type the unit is immune to damage from (e.g., Ice, Fire). | 1 | Ice |
| [`TinkererBasicAttackSwitching`](Cat_Classes.md#object-tinkererbasicattackswitching) | Object | Object containing craft_ability and throw_ability names, enabling the Tinkerer to switch between crafting and throwing basic attacks. | 1 ||
| [`TireBehavior`](./Enums.md) | Integer | Enables the tire's rolling behavior, causing it to move in a set direction each turn. | 1 | 1 |
| [`TormentorHeal`](./Enums.md) | Integer | If set to 1, the Tormentor heals for a percentage of damage dealt. | 1 | 1 |
| [`TrackAmountKilledByPlayer`](./Enums.md) | Enum | Specifies the stat tracker key that records how many of this unit type the player has killed. | 1 | BonusBirdsKilled |
| [`TransformOnStatusThreshold`](#object-transformonstatusthreshold) | Object | Defines a transformation to a new object when a specific status effect reaches a given stack threshold. | 1 ||
| [`TutorialBossRiggedFight`](./Enums.md) | Integer | Overrides the health of the tutorial boss to a specific value for scripted encounters. | 1 | 16 |
| [`TwisterFling`](#object-twisterfling) | Object | Defines the minimum and maximum distance and damage dealt when the Twister flings a held unit. | 1 ||
| [`UnlimitedDeathRattleRevive`](#object-unlimiteddeathrattlerevive) | Object | Defines an ability triggered when the unit would die, allowing an unlimited number of revives even if stunned. | 1 ||
| [`UpTireBehavior`](./Enums.md) | Integer | The number of tiles the tire rolls upward each turn. | 1 | 5 |
| [`UseAbilityWhenOutOfStatus`](#object-useabilitywhenoutofstatus) | Object | Triggers a specified ability when the unit runs out of a tracked status effect. | 1 ||
| [`UseAbilityWhenShieldDepleted`](./Enums.md) | Enum | Specifies the ability triggered when the unit's shield is fully depleted. | 1 | T3Pebbles_PrimeBoulderDrop |
| [`Wall`](./Enums.md) | Integer | If set to 1, the unit is an immovable wall that blocks movement and projectiles. | 1 | 1 |
| [`WhitelistPickupType`](./Enums.md) | Enum | Restricts the unit's pickups to only items of the specified type. | 1 | food |
| [`WideBackstab`](./Enums.md) | Integer | If set to 1, the unit can backstab enemies from a wider angle, including diagonals. | 1 | 1 |
| [`WispDodge`](./Enums.md) | Integer | If set to 1, the wisp unit has a chance to dodge attacks entirely. | 1 | 1 |
| [`ZeroKnockbackDamage`](./Enums.md) | Integer | If set to 1, knockback collisions deal no damage to this unit. | 1 | 1 |

</details>

---

### Object: `properties`


**Definition:** General engine properties.  
**Total Count:** 600


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 538 ||
| [`faction`](./Enums.md#enum-faction) | Enum | Determines which faction the spawned entity belongs to, controlling its team allegiance and targeting behavior. | 505 ||
| `health` | Integer | The unit's base health, specified as an absolute integer or a percentage modifier. | 427 ||
| [`tag`](./Arrays.md#array-tag) | Array / Enum | Specific entity tag required. | 399 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 280 ||
| `movement` | Integer | The number of tiles the unit can move per turn. | 277 ||
| [`corpse_health`](./Enums.md#enum-corpse_health) | Variable | The number of hits the unit's corpse can take before being destroyed, or 'indestructible'. | 195 ||
| `inherit_faction` | Boolean | If true, the unit inherits the faction of the character that spawned it. | 115 ||
| `dispersed_bonus_turns` | Integer | The number of extra turns granted to the unit when it spawns from a dispersed group. | 104 ||
| `base_mana_regen` | Integer | The amount of mana the unit regenerates at the start of each turn. | 90 ||
| [`size`](./Enums.md#enum-size) | Enum / Number | A scale multiplier for the spawned entity's visual size, specified as a single value or a randomized range [min, max]; 'gemini' uses a special sizing mode. | 80 ||
| `shield` | Enum / Integer | The unit's shield value, specified as an integer or a formula. | 74 ||
| [`move_block`](./Enums.md#enum-move_block) | Enum | Specifies which entities or conditions block this unit's movement. | 73 ||
| `kill_required` | Boolean | If true, this unit must be killed for the encounter to end. | 69 ||
| `can_be_backstabbed` | Boolean | If true, the unit can be hit with backstab bonuses from behind. | 68 ||
| `initiative` | Enum / Integer | Determines the unit's turn order position; lower values act earlier. | 61 ||
| `takes_turns` | Boolean | If true, the unit actively takes turns in the turn order. | 61 ||
| `mana_regen` | Integer | The amount of mana the unit regenerates per turn. | 51 ||
| `mana` | Enum / Integer | Base maximum mana pool. | 50 ||
| `flying` | Boolean | If true, the unit is treated as flying and ignores grounded movement restrictions. | 47 ||
| [`banned_elite_buffs`](./Arrays.md#array-banned_elite_buffs) | Array | Array of elite buff names that cannot be applied to this unit. | 45 ||
| [`hidden_tag`](./Arrays.md#array-hidden_tag) | Array / Enum | Specifies a hidden tag for internal logic or grouping, not displayed in game. | 38 ||
| `weak_threshold` | Integer | The health threshold below which the unit is considered 'weak' for mechanics. | 32 ||
| `knockback_immune` | Boolean | If true, the unit cannot be knocked back by any effect. | 25 ||
| `can_be_champion` | Boolean | If true, this unit can be upgraded to a champion variant. | 20 ||
| [`lock_orientation`](./Arrays.md#array-lock_orientation) | Array | Specifies a fixed facing direction for the unit as an [x, y] offset. | 19 ||
| [`ai_scale`](./Enums.md#enum-ai_scale) | Number | A multiplier for the unit's AI decision-making weight or priority. | 18 ||
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Determines which visual or gameplay layer (e.g. "tiles", "pickups", "characters") the editor object belongs to. | 17 ||
| [`auto_run_priority`](./Enums.md#enum-auto_run_priority) | Enum | Determines the automatic movement priority for the unit's AI (e.g., 'stationary', 'support'). | 16 ||
| `inanimate` | Boolean | If true, the unit is considered an inanimate object (e.g., a wall or block). | 16 ||
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 16 ||
| `disperse_main_turns` | Boolean | If true, the unit's main turns are spread out evenly across the turn order instead of clumped. | 15 ||
| [`hidden_tags`](./Arrays.md#array-hidden_tags) | Array / Enum | Array of additional hidden tags for internal categorization or logic. | 14 ||
| [`tags`](./Arrays.md#array-tags) | Array / Enum | Array of gameplay-relevant tags for item or unit categorization (e.g., 'consumable', 'cat'). | 14 ||
| `evenly_dispersed_bonus_turns` | Integer | The number of extra turns this unit gets, evenly inserted into the turn queue. | 13 ||
| `exclude_from_hallucinate` | Boolean | If true, this unit cannot be generated by hallucination effects. | 13 ||
| `round_end_bonus_turns` | Integer | The number of extra turns this unit gets at the end of the round. | 13 ||
| `can_be_overkilled` | Boolean | If true, this unit can be dealt damage beyond its remaining health, triggering overkill mechanics. | 12 ||
| `can_collect_coins` | Boolean | If true, this unit can pick up dropped coins on the map. | 10 ||
| `deathpoof_size` | Integer | The size of the visual poof effect played when this unit dies. | 10 ||
| `dispersed_bonus_turns_consider_initiative` | Boolean | If true, the unit's extra bonus turns are placed considering its initiative value. | 10 ||
| `initial_health` | Integer | The starting health of the unit before any modifiers. | 10 ||
| [`held_coins`](./Arrays.md#array-held_coins) | Array / Integer | If an array [min max], specifies a range of coins held; if an integer, a fixed amount. | 10 ||
| `can_eat_food` | Boolean | If true, the unit can consume food items from the inventory or ground. | 9 ||
| `can_grant_extra_turns` | Boolean | If true, the unit can grant extra turns to other units via abilities. | 8 ||
| `tall` | Boolean | If true, the unit occupies multiple vertical tiles (2x1 or 2x2). | 8 ||
| `dispersed_bonus_turns_before_cats` | Boolean | If true, the unit's extra bonus turns are placed before any player cat turns. | 7 ||
| `divine_shield` | Integer | The number of charges of divine shield that block incoming damage fully. | 7 ||
| `is_player_cat` | Boolean | If true, this unit is considered a player-controlled cat for game mechanics. | 7 ||
| `boss_minions_runaway` | Boolean | If true, minions spawned by this boss will flee when the boss is defeated. | 6 ||
| `mana_matters` | Boolean | If true, this unit uses mana and interacts with mana-related mechanics. | 6 ||
| `access_to_player_inventory` | Boolean | If true, the unit can access and use items from the player's shared inventory. | 5 ||
| `act_points` | Integer | The number of action points required or provided to use an ability or skill. | 5 ||
| `takes_main_turn` | Boolean | If true, this entity uses a full main turn action in the turn order. | 5 ||
| `visually_spiky` | Boolean | If true, the unit displays spiky visual effects on its sprite. | 5 ||
| `allow_passive_spelltransforming` | Boolean | If true, passive abilities can trigger spell transformation for this unit. | 4 ||
| `base_crit_chance` | Integer | The base critical hit chance percentage for the unit. | 4 ||
| `last_turn_is_main_turn` | Boolean | If true, the final turn in a multi-turn sequence counts as a main turn. | 4 ||
| `round_start_bonus_turns` | Integer | The number of extra turns this unit gets at the start of the round. | 4 ||
| `view_bleeding_characters_as_enemies` | Boolean | If true, the unit treats any bleeding character as an enemy target. | 4 ||
| [`aoe_pierce_mode`](./Enums.md#enum-aoe_pierce_mode) | Enum | Specifies how area-of-effect attacks handle obstacle collision (e.g., 'block'). | 3 ||
| `base_initiative` | Integer | The unmodified initiative value for the unit, used before any modifiers. | 3 ||
| `base_movement` | Integer | The unmodified movement range in tiles for the unit. | 3 ||
| `catdata_ignore_skills` | Boolean | If true, the unit's saved cat data will not include skill modifications. | 3 ||
| [`disallow_items`](./Enums.md#enum-disallow_items) | Enum | Specifies items that cannot be used by this unit ('all' or specific item name). | 3 ||
| `always_triggers_traps` | Boolean | If true, the unit will trigger any traps it steps on regardless of other conditions. | 2 ||
| `base_health` | Integer | The unmodified health total of the unit, used before any modifiers. | 2 ||
| `base_health_regen` | Integer | The amount of health regenerated per turn. | 2 ||
| `base_initial_mana` | Integer | The amount of mana a unit starts with at the beginning of a battle. | 2 ||
| `base_mana` | Integer | The maximum mana capacity of a unit. | 2 ||
| `blocking` | Boolean | If true, the animation or ability prevents other actions from occurring until it finishes. | 2 ||
| `can_be_elite` | Boolean | If true, this unit type can spawn as an elite variant. | 2 ||
| `can_run` | Boolean | If true, the unit is capable of fleeing from battle. | 2 ||
| `champion` | Boolean | If true, this unit is a champion variant with enhanced stats or abilities. | 2 ||
| `force_not_familiar` | Boolean | If true, this unit is prevented from being treated as a familiar. | 2 ||
| `hint_no_corpse` | Boolean | If true, hints will not display a corpse icon for this unit. | 2 ||
| `must_start_facing_camera` | Boolean | If true, this unit must begin the battle facing the camera. | 2 ||
| `tile_desire_cost` | Integer | The amount of desire cost consumed when moving onto a tile. | 2 ||
| `uncapturable` | Boolean | If true, this unit cannot be captured by the player. | 2 ||
| `aggro_target_is_enemy` | Boolean | If true, this unit's aggression target is always an enemy. | 1 ||
| `allow_flying_effect` | Boolean | If true, this unit can receive the flying status effect. | 1 ||
| `allow_offmap_corpse` | Boolean | If true, this unit can leave a corpse even when killed off the map edge. | 1 ||
| `allow_replacebrain` | Boolean | If true, this unit can have its brain replaced via the replace brain mechanic. | 1 ||
| `always_face_forward` | Boolean | If true, this unit's sprite always faces forward regardless of direction. | 1 ||
| `capture_as_cat` | Boolean | If true, this unit is captured as a cat instead of the default capture method. | 1 ||
| `elite` | Boolean | If true, this unit is an elite variant with enhanced stats or abilities. | 1 ||
| `first_turn_is_main_turn` | Boolean | If true, this unit's first turn is treated as a main turn instead of a bonus turn. | 1 ||
| `ignore_mouseover` | Boolean | If true, this unit does not highlight or respond to mouse hover. | 1 ||
| `ignore_tiles` | Boolean | If true, this unit ignores tile-based movement restrictions. | 1 ||
| `mouseover_priority` | Integer | The priority value for mouseover selection, higher values take precedence. | 1 ||
| `move_points` | Integer | The number of movement tiles this unit can traverse per action. | 1 ||
| `pickup_type` | Integer | Specifies the pickup behavior category (e.g., 1 for coins). | 1 ||
| `scale` | Number | A multiplier for the unit's overall scale, affecting size and related properties. | 1 ||
| `speculative_inanimate` | Boolean | If true, this object is tentatively treated as inanimate for targeting purposes. | 1 ||
| `static` | Boolean | If true, this object does not move or animate based on game state. | 1 ||
| `two_fronts` | Boolean | If true, this unit can attack from both its front and back sides. | 1 ||
| `two_fronts_switch` | Boolean | If true, this unit can switch which side is considered its front. | 1 ||
| `view_bugs_as_enemies` | Boolean | If true, this unit treats bug-type units as enemies. | 1 ||
| [`inanimate_can_receive_specific_statuses`](./Arrays.md#array-inanimate_can_receive_specific_statuses) | Array | A list of status effect names that even inanimate objects can receive. | 1 ||

</details>

---

### Object: `ai`


**Definition:** Core block defining the AI behavior logic and weights.  
**Total Count:** 583


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Alert`](./Characters_and_Bosses.md#object-alert), [`Angry`](./Characters_and_Bosses.md#object-angry), [`Attacker`](./Characters_and_Bosses.md#object-attacker), [`BellyFull`](./Characters_and_Bosses.md#object-bellyfull), [`Bishop`](./Characters_and_Bosses.md#object-bishop), [`BlackHole`](./Characters_and_Bosses.md#object-blackhole), [`Bully`](./Characters_and_Bosses.md#object-bully), [`CaveBaby`](./Characters_and_Bosses.md#object-cavebaby), [`CaveMan`](./Characters_and_Bosses.md#object-caveman), [`CaveManSpear`](./Characters_and_Bosses.md#object-cavemanspear), [`CaveWoman`](./Characters_and_Bosses.md#object-cavewoman), [`CaveWomanHasCat`](./Characters_and_Bosses.md#object-cavewomanhascat), [`Charging`](./Characters_and_Bosses.md#object-charging), [`Cultist`](./Characters_and_Bosses.md#object-cultist), [`Damaged`](./Characters_and_Bosses.md#object-damaged), [`Default`](./Characters_and_Bosses.md#object-default), [`Default_Ceiling`](./Characters_and_Bosses.md#object-default_ceiling), [`Default_Ground`](./Characters_and_Bosses.md#object-default_ground), [`DesireMech`](./Characters_and_Bosses.md#object-desiremech), [`Down`](./Characters_and_Bosses.md#object-down), and 64 more...

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum | Specifies the AI brain type (e.g., NoBrain, PlayerBrain, GenericBrain). | 573 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 493 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 490 ||
| [`pattern`](#object-pattern) | Object | AI sequence logic. | 289 ||
| [`mainturn_pattern`](#object-mainturn_pattern) | Object | AI Logic: Determines standard ability usage during the main turn. | 44 ||
| `end_turn_on_formswitch` | Boolean | If true, the unit's turn ends immediately after switching forms. | 39 ||
| [`virtual_abilities`](#object-virtual_abilities) | Object | Abilities that are evaluated but not directly castable by the player. | 35 ||
| `auto_orient` | Boolean | If true, the AI automatically rotates the unit to face its target. | 31 ||
| `reset_pattern_on_formswitch` | Boolean | If true, the AI pattern index resets to 0 when the unit changes form. | 31 ||
| `stun_advances_pattern` | Boolean | If true, being stunned advances the AI pattern index. | 30 ||
| `fallback_advances_pattern` | Boolean | If true, using a fallback AI command advances the pattern index. | 28 ||
| [`bonusturn_pattern`](#object-bonusturn_pattern) | Object | AI Logic: Determines ability usage during bonus turns. | 27 ||
| [`fallback`](#object-fallback) | Object | Logic executed if primary options fail. | 23 ||
| [`round_end_bonusturn_pattern`](#object-round_end_bonusturn_pattern) | Object | AI Logic: Ability usage pattern during round-end bonus turns. | 12 ||
| `consider_spells` | Boolean | If true, the AI will consider using spells when evaluating actions. | 11 ||
| `animate_choice` | Boolean | If true, the AI plays an animation before executing its chosen ability. | 8 ||
| `clamp_pattern` | Boolean | If true, the AI pattern index is clamped to the pattern list length, preventing overflow. | 5 ||
| `randomize_pattern_start` | Boolean | If true, the AI starts at a random index in its pattern on initial spawn. | 3 ||
| [`dispersed_bonusturn_pattern`](#object-dispersed_bonusturn_pattern) | Object | AI Logic: Alternative bonus turn ability pattern. | 2 ||
| `random_orient` | Boolean | If true, the AI randomly orients the unit upon spawn. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| `never_hit_ally_corpses` | Boolean | If true, the AI avoids targeting or damaging ally corpses. | 1 ||
| [`post_absorb_move_weights`](./Enums.md#enum-post_absorb_move_weights) | Enum | Specifies the movement weighting behavior after absorbing a unit (e.g., minimum_move). | 1 ||
| `reset_pattern_on_round_begin` | Boolean | If true, the AI pattern resets at the start of each round. | 1 ||
| [`roll_ability`](./Enums.md#enum-roll_ability) | Enum | Specifies the ability name used for a dice roll mechanic (e.g., RollDice). | 1 ||
| [`round_start_bonusturn_pattern`](#object-round_start_bonusturn_pattern) | Object | AI Logic: Ability usage pattern during round-start bonus turns. | 1 ||
| [`dice_abilities`](./Arrays.md#array-dice_abilities) | Array | A list of ability names associated with the faces of a dice roll. | 1 ||

</details>

---

### Object: `stats`


**Definition:** Core character metrics (Health, Strength, etc.).  
**Total Count:** 497


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `strength` | Integer | The base strength stat governing physical damage dealt. | 386 ||
| `constitution` | Integer | The base constitution stat governing physical damage defense. | 380 ||
| `dexterity` | Integer | The base dexterity stat governing accuracy and evasion. | 380 ||
| `charisma` | Integer | The base charisma stat governing social or status effect interactions. | 379 ||
| `intelligence` | Integer | The base intelligence stat governing magical or mental abilities. | 379 ||
| `speed` | Array / Number | Base speed/initiative stat. | 379 ||
| `luck` | Integer | The base luck stat governing random event outcomes and critical chances. | 160 ||

</details>

---

### Object: `abilities`


**Definition:** Lists the ability IDs the character possesses.  
**Total Count:** 460


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 438 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 433 ||
| [`spells`](./Arrays.md#array-spells) | Array | The number of spells the unit has access to. | 381 ||
| `can_get_bonus` | Boolean | If true, the unit can perform a bonus action. | 30 ||

</details>

---

### Object: `pattern`


**Definition:** AI sequence logic.  
**Total Count:** 296


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root), [`ReplaceBrain`](./Characters_and_Bosses.md#object-replacebrain), [`ai`](./Characters_and_Bosses.md#object-ai), [`ai_if_spawned_as_enemy`](./Characters_and_Bosses.md#object-ai_if_spawned_as_enemy)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum | Specifies a single action the unit performs in this pattern step. | 101 ||
| [`do_all`](./Arrays.md#array-do_all) | Array | A list of actions the unit performs in sequence. | 91 ||
| [`do_priority`](./Arrays.md#array-do_priority) | Array | A list of actions executed in order of priority, stopping when one succeeds. | 82 ||
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum | The unit moves before performing this single action. | 11 ||
| [`do_random`](./Arrays.md#array-do_random) | Array | A list of actions from which one is chosen at random. | 9 ||
| [`do_strict`](./Arrays.md#array-do_strict) | Array | A list of actions executed in strict sequence. | 4 ||
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array | A list of actions that cause the unit to skip its turn. | 3 ||
| [`move_then_do_random`](./Arrays.md#array-move_then_do_random) | Array | The unit moves, then randomly performs one action from the list. | 3 ||
| [`move_then_do_priority`](./Arrays.md#array-move_then_do_priority) | Array | The unit moves, then executes the first successful action from the prioritized list. | 2 ||
| [`do_all_shuffle`](./Arrays.md#array-do_all_shuffle) | Array | A list of actions shuffled randomly, then executed in that order. | 2 ||
| [`do_best`](./Arrays.md#array-do_best) | Array | A list of actions evaluated for optimal outcome; the best one is chosen. | 1 ||
| [`do_best_multiple`](./Arrays.md#array-do_best_multiple) | Array | A list of actions evaluated for optimal outcome; the best possible combination is chosen. | 1 ||
| [`do_priority_alternating`](./Arrays.md#array-do_priority_alternating) | Array | A list of actions executed in priority order, alternating between entries on successive uses. | 1 ||
| [`move_then_do_all`](./Arrays.md#array-move_then_do_all) | Array | The unit moves, then executes all actions in the list in sequence. | 1 ||

</details>

---

### Object: `Normal`


**Definition:** Character Form: Behavior and stats for the \'Normal\' state.  
**Total Count:** 231


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 10 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 5 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||

</details>

---

### Object: `Angry`


**Definition:** Character Form / AI State: Behavior and stats for the \'Angry\' state.  
**Total Count:** 221


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||

</details>

---

### Object: `FormChanger`


**Definition:** AI Role: Designates the character as one that frequently shifts forms.  
**Total Count:** 106


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`initial_form`](./Enums.md#enum-initial_form) | Enum / Integer | Specifies which form the unit starts in. | 56 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 56 ||
| [`Default`](#object-default) | Enum / Object | Character Form: The baseline default behavior state. | 37 ||
| [`Normal`](#object-normal) | Integer / Object | Character Form: Behavior and stats for the \'Normal\' state. | 11 ||
| [`Rage`](#object-rage) | Object | Character Form: Behavior and stats for the \'Rage\' state. | 10 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 ||
| [`HasCat`](#object-hascat) | Object | Character Form: Behavior and stats for the \'HasCat\' state. | 5 ||
| [`default`](#object-default) | Enum / Object | Baseline configuration. | 4 ||
| [`hot`](#object-hot) | Object | Visual effect indicator. | 4 ||
| [`OffMap`](#object-offmap) | Object | Character Form: Behavior and stats for the 'OffMap' state. | 4 ||
| [`AllAlive`](#object-allalive) | Object | Encounter State: Logic executed when all specific entities are currently alive. | 3 ||
| [`Down`](#object-down) | Object | Character Form: Behavior and stats for the \'Down\' state. | 3 ||
| [`Full`](#object-full) | Object | Character Form: Behavior and stats for the \'Full\' state. | 3 ||
| [`OneAlive`](#object-onealive) | Object | Encounter State: Logic executed when exactly one target is alive. | 3 ||
| [`TwoAlive`](#object-twoalive) | Object | Encounter State: Logic executed when exactly two targets are alive. | 3 ||
| [`Up`](#object-up) | Object | Character Form: Behavior and stats for the \'Up\' state. | 3 ||
| [`active`](#object-active) | Object | Defines actively executed abilities. | 2 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 ||
| [`Big`](#object-big) | Object | Character Form / AI State: Behavior and stats for the \'Big\' state. | 2 ||
| [`Boris`](#object-boris) | Enum / Object | Character Form / AI State: Behavior and stats for the \'Boris\' state. | 2 ||
| [`CaveMan`](#object-caveman) | Object | Character Form: Behavior and stats for the \'CaveMan\' state. | 2 ||
| [`CaveManSpear`](#object-cavemanspear) | Object | Character Form: Behavior and stats for the \'CaveManSpear\' state. | 2 ||
| [`Empty`](#object-empty) | Object | Character Form: Behavior and stats for the \'Empty\' state. | 2 ||
| [`Explosive`](#object-explosive) | Enum / Object | Character Form: Behavior and stats for the \'Explosive\' state. | 2 ||
| [`Holding`](#object-holding) | Object | Character Form: Behavior and stats for the \'Holding\' state. | 2 ||
| [`Holy`](#object-holy) | Enum / Object | Character Form: Behavior and stats for the \'Holy\' state. | 2 ||
| [`NotPriming`](#object-notpriming) | Object | Character Form: Behavior and stats when not charging an ability. | 2 ||
| `partial_animation_suffix` | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 2 ||
| [`passive`](#object-passive) | Object | Intrinsic passive modifier. | 2 ||
| [`Priming`](#object-priming) | Object | Character Form: Behavior and stats when charging an ability. | 2 ||
| [`Rain`](#object-rain) | Object | Character Form: Behavior and stats for the 'Rain' state. | 2 ||
| [`Small`](#object-small) | Object | Character Form: Behavior and stats for the \'Small\' state. | 2 ||
| [`SquirrelForm`](#object-squirrelform) | Object | Character Form: Behavior and stats for the 'SquirrelForm' state. | 2 ||
| [`Turtled`](#object-turtled) | Object | Character Form: Behavior and stats for the 'Turtled' state. | 2 ||
| [`Alert`](#object-alert) | Object | AI State: The behavior profile used when the character is alerted to enemies. | 1 ||
| [`Angry`](#object-angry) | Object | Character Form / AI State: Behavior and stats for the \'Angry\' state. | 1 ||
| [`Attacker`](#object-attacker) | Object | AI Role: Designates the character as an attacker rather than support. | 1 ||
| [`BellyFull`](#object-bellyfull) | Object | Character Form / AI State: Behavior and stats for the \'BellyFull\' state. | 1 ||
| [`BigHolding`](#object-bigholding) | Object | Character Form / AI State: Behavior and stats for the \'BigHolding\' state. | 1 ||
| [`BigHoldingCat`](#object-bigholdingcat) | Object | Character Form / AI State: Behavior and stats for the \'BigHoldingCat\' state. | 1 ||
| [`Bishop`](#object-bishop) | Object | Character Form / AI State: Behavior and stats for the \'Bishop\' state. | 1 ||
| [`BlackHole`](#object-blackhole) | Object | Character Form / AI State: Behavior and stats for the \'BlackHole\' state. | 1 ||
| [`Bomb`](#object-bomb) | Object | Character Form / AI State: Behavior and stats for the 'Bomb' state. | 1 ||
| [`Bully`](#object-bully) | Object | Character Form / AI State: Behavior and stats for the 'Bully' state. | 1 ||
| [`Butcher`](Engine_LogicKeys.md#object-butcher) | Object | Applies or references the 'Butcher' effect/state. | 1 ||
| [`CaveBaby`](#object-cavebaby) | Object | Character Form: Behavior and stats for the \'CaveBaby\' state. | 1 ||
| [`CaveWoman`](#object-cavewoman) | Object | Character Form: Behavior and stats for the \'CaveWoman\' state. | 1 ||
| [`CaveWomanHasCat`](#object-cavewomanhascat) | Object | Character Form: Behavior and stats for the \'CaveWomanHasCat\' state. | 1 ||
| [`Charging`](#object-charging) | Object | Character Form / AI State: Behavior when charging an attack. | 1 ||
| [`Close`](#object-close) | Object | AI Movement logic: Maneuvers into close/melee range. | 1 ||
| [`Colorless`](Engine_LogicKeys.md#object-colorless) | Object | Applies or references the 'Colorless' effect/state. | 1 ||
| [`Cultist`](#object-cultist) | Object | Character Form: Behavior and stats for the \'Cultist\' state. | 1 ||
| [`Damaged`](#object-damaged) | Object | Character Form / AI State: Behavior when health is critically low. | 1 ||
| [`Default_Ceiling`](#object-default_ceiling) | Object | Character Form: The baseline behavior state while attached to the ceiling. | 1 ||
| [`Default_Ground`](#object-default_ground) | Object | Character Form: The baseline behavior state while on the ground. | 1 ||
| [`DesireMech`](#object-desiremech) | Object | Character Form: Behavior and stats for the 'DesireMech' state. | 1 ||
| [`Die`](#object-die) | Integer / Object | Character Form / Logic: Forces the character to die. | 1 ||
| [`Druid`](Engine_LogicKeys.md#object-druid) | Object | Applies or references the 'Druid' effect/state. | 1 ||
| [`Drunker`](#object-drunker) | Object | Character Form: Behavior and stats for the 'Drunker' state. | 1 ||
| [`DualSword`](#object-dualsword) | Object | Character Form: Behavior and stats for the \'DualSword\' state. | 1 ||
| [`DualSword_Primed`](#object-dualsword_primed) | Object | Character Form: Behavior and stats for the \'DualSword_Primed\' state. | 1 ||
| [`Dumb`](#object-dumb) | Integer / Object | AI Profile: A simplified, less optimal decision-making profile. | 1 ||
| [`Explody`](#object-explody) | Object | Character Form: Behavior and stats for the 'Explody' state. | 1 ||
| [`Fighter`](Engine_LogicKeys.md#object-fighter) | Object | Applies or references the 'Fighter' effect/state. | 1 ||
| [`FightPhase`](#object-fightphase) | Object | Boss Logic: Main combat phase. | 1 ||
| [`Fire`](#object-fire) | Integer / Object | Character Form: Behavior and stats for the 'Fire' state. | 1 ||
| [`FireFull`](#object-firefull) | Integer / Object | Character Form: Behavior and stats for the 'FireFull' state. | 1 ||
| [`Flop`](#object-flop) | Object | Character Form: Behavior and stats for the \'Flop\' state. | 1 ||
| [`Flop2`](#object-flop2) | Object | Character Form: Behavior and stats for the \'Flop2\' state. | 1 ||
| [`Flush`](#object-flush) | Object | Character Form: Behavior and stats for the 'Flush' state. | 1 ||
| [`FlushBubs`](#object-flushbubs) | Object | Character Form: Behavior and stats for the 'FlushBubs' state. | 1 ||
| [`FlushHost`](#object-flushhost) | Object | Character Form: Behavior and stats for the 'FlushHost' state. | 1 ||
| [`FlushNettle`](#object-flushnettle) | Object | Character Form: Behavior and stats for the 'FlushNettle' state. | 1 ||
| [`Grappling`](#object-grappling) | Object | Character Form / AI State: Behavior while grappling an opponent. | 1 ||
| [`Grown`](#object-grown) | Object | Character Form: Behavior and stats for the \'Grown\' state. | 1 ||
| [`GuaranteedJackpot`](#object-guaranteedjackpot) | Object | Loot Logic: Guarantees a high-tier drop. | 1 ||
| [`Guarding`](#object-guarding) | Object | Character Form / AI State: Defensive behavior state. | 1 ||
| [`HalfDead`](#object-halfdead) | Object | Character Form: Behavior and stats for the \'HalfDead\' state. | 1 ||
| [`HasDeadCat`](#object-hasdeadcat) | Object | Character Form: Behavior and stats for the \'HasDeadCat\' state. | 1 ||
| [`HasRock`](#object-hasrock) | Object | Character Form: Behavior and stats for the \'HasRock\' state. | 1 ||
| [`Headless`](#object-headless) | Object | Character Form: Behavior and stats for the \'Headless\' state. | 1 ||
| [`Hint_CrackedVisuals`](#object-hint_crackedvisuals) | Object | Visual: Overlay effects for cracked/damaged terrain or objects. | 1 ||
| [`Hint_CrackedVisuals2`](#object-hint_crackedvisuals2) | Object | Visual: Secondary cracked visual overlay. | 1 ||
| [`Hint_CrackedVisuals3`](#object-hint_crackedvisuals3) | Object | Visual: Tertiary cracked visual overlay. | 1 ||
| [`HumanDead`](#object-humandead) | Object | Character Form: Behavior and stats for the \'HumanDead\' state. | 1 ||
| [`Hunter`](Engine_LogicKeys.md#object-hunter) | Object | Applies or references the 'Hunter' effect/state. | 1 ||
| [`InitialPhase`](#object-initialphase) | Object | Boss Logic: The starting phase of an encounter. | 1 ||
| [`Insane_Ceiling`](#object-insane_ceiling) | Object | Character Form: Insane behavior state while attached to the ceiling. | 1 ||
| [`Insane_Ground`](#object-insane_ground) | Object | Character Form: Insane behavior state while on the ground. | 1 ||
| [`Johnny`](#object-johnny) | Object | Character Form: Behavior and stats for the 'Johnny' state. | 1 ||
| [`JohnnyBubs`](#object-johnnybubs) | Object | Character Form: Behavior and stats for the 'JohnnyBubs' state. | 1 ||
| [`JohnnyHost`](#object-johnnyhost) | Object | Character Form: Behavior and stats for the 'JohnnyHost' state. | 1 ||
| [`JohnnyNettle`](#object-johnnynettle) | Object | Character Form: Behavior and stats for the 'JohnnyNettle' state. | 1 ||
| [`Joystick`](#object-joystick) | Object | Character Form: Behavior and stats for the \'Joystick\' state. | 1 ||
| [`LastHit`](#object-lasthit) | Object | Logic: Executes logic on the final hit of a multi-hit attack. | 1 ||
| [`Lifted`](#object-lifted) | Object | Character Form: Behavior and stats for the \'Lifted\' state. | 1 ||
| [`Lit`](#object-lit) | Object | Character Form: Behavior and stats for the 'Lit' state. | 1 ||
| [`Mage`](Engine_LogicKeys.md#object-mage) | Object | Applies or references the 'Mage' effect/state. | 1 ||
| [`Medic`](Engine_LogicKeys.md#object-medic) | Object | Applies or references the 'Medic' effect/state. | 1 ||
| [`Monk`](Engine_LogicKeys.md#object-monk) | Object | Applies or references the 'Monk' effect/state. | 1 ||
| [`Mounted`](#object-mounted) | Object | Character Form: Behavior and stats for the \'Mounted\' state. | 1 ||
| [`MouthFull`](#object-mouthfull) | Object | Character Form: Behavior and stats for the \'MouthFull\' state. | 1 ||
| [`Mutant`](#object-mutant) | Integer / Object | Character Form: Behavior and stats for the \'Mutant\' state. | 1 ||
| [`Necromancer`](Engine_LogicKeys.md#object-necromancer) | Object | Applies or references the 'Necromancer' effect/state. | 1 ||
| [`NeutronStar`](#object-neutronstar) | Object | Character Form: Behavior and stats for the 'NeutronStar' state. | 1 ||
| [`NoDeathRattle`](./Engine_LogicKeys.md#valid-property-keys) | Object | Applies or references the 'NoDeathRattle' effect/state. | 1 ||
| [`NoEyes`](#object-noeyes) | Object | Character Form: Behavior and stats for the \'NoEyes\' state. | 1 ||
| [`NormalFull`](#object-normalfull) | Integer / Object | Character Form: Behavior and stats for the 'NormalFull' state. | 1 ||
| [`NoStick`](#object-nostick) | Object | Character Form: Behavior and stats for the 'NoStick' state. | 1 ||
| [`Nuke`](#object-nuke) | Object | Character Form: Behavior and stats for the 'Nuke' state. | 1 ||
| [`Obey`](#object-obey) | Integer / Object | AI State: Enforced compliance logic (e.g., when Charmed). | 1 ||
| [`Off`](#object-off) | Object | Character Form: Behavior and stats for the 'Off' state. | 1 ||
| [`OffScreen`](#object-offscreen) | Object | Character Form: Behavior and stats for the 'OffScreen' state. | 1 ||
| [`OneEye`](#object-oneeye) | Object | Character Form: Behavior and stats for the \'OneEye\' state. | 1 ||
| [`Open`](#object-open) | Object | Character Form: Behavior and stats for the 'Open' state. | 1 ||
| [`OpenCat`](#object-opencat) | Object | Character Form: Behavior and stats for the 'OpenCat' state. | 1 ||
| [`Out`](#object-out) | Object | Character Form: Behavior and stats for the 'Out' state. | 1 ||
| [`Possessing`](#object-possessing) | Object | Character Form: Behavior and stats for the \'Possessing\' state. | 1 ||
| [`Primed`](#object-primed) | Object | Character Form: Behavior and stats for the 'Primed' state. | 1 ||
| [`Psychic`](Engine_LogicKeys.md#object-psychic) | Object | Applies or references the 'Psychic' effect/state. | 1 ||
| [`Pulp2`](#object-pulp2) | Object | Character Form: Behavior and stats for the 'Pulp2' state. | 1 ||
| [`Pulp3`](#object-pulp3) | Object | Character Form: Behavior and stats for the 'Pulp3' state. | 1 ||
| [`Pulp4`](#object-pulp4) | Object | Character Form: Behavior and stats for the 'Pulp4' state. | 1 ||
| [`Pulp5`](#object-pulp5) | Object | Character Form: Behavior and stats for the 'Pulp5' state. | 1 ||
| [`Pulp6`](#object-pulp6) | Object | Character Form: Behavior and stats for the 'Pulp6' state. | 1 ||
| [`Pulp7`](#object-pulp7) | Object | Character Form: Behavior and stats for the 'Pulp7' state. | 1 ||
| [`Sitting`](#object-sitting) | Object | Character Form: Behavior and stats for the 'Sitting' state. | 1 ||
| [`SmallHolding`](#object-smallholding) | Object | Character Form: Behavior and stats for the \'SmallHolding\' state. | 1 ||
| [`SmallHoldingCat`](#object-smallholdingcat) | Object | Character Form: Behavior and stats for the \'SmallHoldingCat\' state. | 1 ||
| [`SpawningPhase`](#object-spawningphase) | Object | Boss Logic: Phase focused on summoning minions. | 1 ||
| [`Standing`](#object-standing) | Object | Character Form: Behavior and stats for the 'Standing' state. | 1 ||
| [`Standing2`](#object-standing2) | Object | Character Form: Behavior and stats for the 'Standing2' state. | 1 ||
| [`Start_Ceiling`](#object-start_ceiling) | Object | Character Form: Behavior and stats for the 'Start_Ceiling' state. | 1 ||
| [`Stop`](#object-stop) | Integer / Object | AI Movement: Forces the character to cease movement. | 1 ||
| [`SwordAndShield`](#object-swordandshield) | Object | Character Form: Behavior and stats for the 'SwordAndShield' state. | 1 ||
| [`SwordAndShield_Primed`](#object-swordandshield_primed) | Object | Character Form: Behavior and stats for the \'SwordAndShield_Primed\' state. | 1 ||
| `sync_brain_patterns` | Boolean | If true, the unit's AI patterns are synchronized across all its forms. | 1 ||
| [`Tank`](Engine_LogicKeys.md#object-tank) | Object | Applies or references the 'Tank' effect/state. | 1 ||
| [`Tar`](#object-tar) | Integer / Object | Character Form: Behavior and stats for the 'Tar' state. | 1 ||
| [`TarFull`](#object-tarfull) | Integer / Object | Character Form: Behavior and stats for the 'TarFull' state. | 1 ||
| [`Thief`](Engine_LogicKeys.md#object-thief) | Object | Applies or references the 'Thief' effect/state. | 1 ||
| [`Throb`](#object-throb) | Object | Character Form: Behavior and stats for the 'Throb' state. | 1 ||
| [`ThrobBubs`](#object-throbbubs) | Object | Character Form: Behavior and stats for the 'ThrobBubs' state. | 1 ||
| [`ThrobHost`](#object-throbhost) | Object | Character Form: Behavior and stats for the 'ThrobHost' state. | 1 ||
| [`ThrobNettle`](#object-throbnettle) | Object | Character Form: Behavior and stats for the 'ThrobNettle' state. | 1 ||
| [`Tinkerer`](Engine_LogicKeys.md#object-tinkerer) | Object | Applies or references the 'Tinkerer' effect/state. | 1 ||
| [`Transformed`](#object-transformed) | Object | Character Form: Behavior and stats for the 'Transformed' state. | 1 ||
| [`TwoEyes`](#object-twoeyes) | Object | Character Form: Behavior and stats for the 'TwoEyes' state. | 1 ||
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 1 ||
| [`Unlit`](#object-unlit) | Object | Character Form: Behavior and stats for the 'Unlit' state. | 1 ||
| [`Unmounted`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Applies or references the 'Unmounted' effect/state. | 1 ||
| [`Unwashed`](#object-unwashed) | Object | Character Form: Behavior and stats for the 'Unwashed' state. | 1 ||
| [`Washed`](#object-washed) | Object | Character Form: Behavior and stats for the 'Washed' state. | 1 ||
| [`Washer`](#object-washer) | Object | Character Form: Behavior and stats for the \'Washer\' state. | 1 ||
| [`Water`](#object-water) | Object | Character Form: Behavior and stats for the \'Water\' state. | 1 ||
| [`WereMan`](#object-wereman) | Object | Character Form: Behavior and stats for the \'WereMan\' state. | 1 ||
| [`Zealot`](#object-zealot) | Object | Character Form: Behavior and stats for the \'Zealot\' state. | 1 ||
| [`ZealotBomb`](#object-zealotbomb) | Object | Character Form: Behavior and stats for the \'ZealotBomb\' state. | 1 ||

</details>

---

### Object: `SpawnOnDeath`


**Definition:** No definition provided.  
**Total Count:** 79


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum | Determines which faction the spawned entity belongs to, controlling its team allegiance and targeting behavior. | 4 ||
| [`obj`](./Arrays.md#array-obj) | Array / Enum | The object(s) spawned when this passive triggers. | 4 ||
| [`additional_statuses`](#object-additional_statuses) | Object | Generic statuses added to the character. | 1 ||

</details>

---

### Object: `sound`


**Definition:** Audio bindings.  
**Total Count:** 62


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_sounds`](./Arrays.md#array-alt_sounds) | Array | A list of alternative sound sets, each set is a list of sound clips that override the default sounds. | 61 ||
| [`animation_prefix`](./Enums.md#enum-animation_prefix) | Enum | Specifies the prefix added to sound names for this unit's sounds. | 1 ||

</details>

---

### Object: `Robot`


**Definition:** No definition provided.  
**Total Count:** 46


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alternate_energized_effect`](#object-alternate_energized_effect) | Object | Overrides default energized visuals. | 2 ||

</details>

---

### Object: `turns`


**Definition:** Turn counter tracking.  
**Total Count:** 45


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Bishop`](./Characters_and_Bosses.md#object-bishop), [`Bully`](./Characters_and_Bosses.md#object-bully), [`Default`](./Characters_and_Bosses.md#object-default), [`Default_Ceiling`](./Characters_and_Bosses.md#object-default_ceiling), [`Default_Ground`](./Characters_and_Bosses.md#object-default_ground), [`FightPhase`](./Characters_and_Bosses.md#object-fightphase), [`Holding`](./Characters_and_Bosses.md#object-holding), [`InitialPhase`](./Characters_and_Bosses.md#object-initialphase), [`Insane_Ceiling`](./Characters_and_Bosses.md#object-insane_ceiling), [`Insane_Ground`](./Characters_and_Bosses.md#object-insane_ground), [`LastHit`](./Characters_and_Bosses.md#object-lasthit), [`Lifted`](./Characters_and_Bosses.md#object-lifted), [`Mutant`](./Characters_and_Bosses.md#object-mutant), [`Normal`](./Characters_and_Bosses.md#object-normal), [`NotPriming`](./Characters_and_Bosses.md#object-notpriming), [`Nuke`](./Characters_and_Bosses.md#object-nuke), [`OffMap`](./Characters_and_Bosses.md#object-offmap), [`OffScreen`](./Characters_and_Bosses.md#object-offscreen), [`OneAlive`](./Characters_and_Bosses.md#object-onealive), [`Possessing`](./Characters_and_Bosses.md#object-possessing), and 13 more...

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `takes_turns` | Boolean | If true, the unit actively takes turns in the turn order. | 23 ||
| `dispersed_bonus_turns` | Integer | The number of extra turns granted to the unit when it spawns from a dispersed group. | 18 ||
| `takes_main_turn` | Boolean | If true, this entity uses a full main turn action in the turn order. | 10 ||
| `evenly_dispersed_bonus_turns` | Integer | The number of extra turns this unit gets, evenly inserted into the turn queue. | 7 ||
| `round_end_bonus_turns` | Integer | The number of extra turns this unit gets at the end of the round. | 5 ||
| `wait_till_next_round_to_update_turns` | Boolean | If true, the unit's turn count is updated at the start of the next round instead of immediately. | 4 ||
| `round_start_bonus_turns` | Integer | The number of extra turns this unit gets at the start of the round. | 1 ||

</details>

---

### Object: `equipment`


**Definition:** List of item IDs the character spawns equipped with.  
**Total Count:** 44


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`face`](./Enums.md#enum-face) | Enum | Specifies the equipment item placed in the face slot. | 16 ||
| [`head`](./Enums.md#enum-head) | Enum / Number | The visual ID (integer) of the head part applied to the cat. | 14 ||
| [`neck`](./Enums.md#enum-neck) | Enum | Specifies the equipment item placed in the neck slot. | 10 ||
| [`weapon`](./Enums.md#enum-weapon) | Enum | Weapon item constraint. | 7 ||

</details>

---

### Object: `mainturn_pattern`


**Definition:** AI Logic: Determines standard ability usage during the main turn.  
**Total Count:** 44


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum | Specifies a single action the unit performs in this pattern step. | 23 ||
| [`do_all`](./Arrays.md#array-do_all) | Array | A list of actions the unit performs in sequence. | 9 ||
| [`do_priority`](./Arrays.md#array-do_priority) | Array | A list of actions executed in order of priority, stopping when one succeeds. | 8 ||
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum | The unit moves before performing this single action. | 2 ||
| [`do_strict`](./Arrays.md#array-do_strict) | Array | A list of actions executed in strict sequence. | 2 ||

</details>

---

### Object: `Default`


**Definition:** Character Form: The baseline default behavior state.  
**Total Count:** 38


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 28 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 24 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 10 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||

</details>

---

### Object: `FormChangeWhileHasStatus`


**Definition:** Logic: Changes form automatically while possessing a specific status.  
**Total Count:** 35


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 35 ||
| [`form_hasnot`](./Enums.md#enum-form_hasnot) | Enum | Specifies a form the unit must NOT currently be in for this passive to trigger. | 30 ||
| [`form_has`](./Enums.md#enum-form_has) | Enum | Specifies the form the unit must currently be in for this passive to trigger. | 25 ||

</details>

---

### Object: `keyword_tooltips`


**Definition:** Forces specific UI tooltips to appear when hovering over the ability.  
**Total Count:** 35


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Die`](./Characters_and_Bosses.md#object-die), [`Dumb`](./Characters_and_Bosses.md#object-dumb), [`Obey`](./Characters_and_Bosses.md#object-obey), [`Stop`](./Characters_and_Bosses.md#object-stop)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TVBotDie` | Integer | Applies or references the 'TVBotDie' effect/state. | 1 ||
| `TVBotDumb` | Integer | Applies or references the 'TVBotDumb' effect/state. | 1 ||
| `TVBotObey` | Integer | Applies or references the 'TVBotObey' effect/state. | 1 ||
| `TVBotStop` | Integer | Applies or references the 'TVBotStop' effect/state. | 1 ||

</details>

---

### Object: `virtual_abilities`


**Definition:** Abilities that are evaluated but not directly castable by the player.  
**Total Count:** 35


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`MoveAway`](#object-moveaway) | Object | AI Movement: Moves away from the target. | 4 ||
| [`MoveClose`](#object-moveclose) | Object | AI Movement: Moves into melee range. | 4 ||
| [`DashRandomly`](#object-dashrandomly) | Object | AI Movement: Dashes to a random valid tile. | 2 ||
| [`Escape`](#object-escape) | Object | AI Movement: Logic for fleeing or escaping the map. | 2 ||
| [`MoveCenter`](#object-movecenter) | Object | AI Movement: Moves toward the center of the map. | 2 ||
| [`MoveForThrow`](#object-moveforthrow) | Object | AI Movement: Repositions to gain line of sight for throwing. | 2 ||
| [`SpearRun`](#object-spearrun) | Object | AI Movement: Specific movement logic for Spear enemies. | 2 ||
| [`CerberubsJumpBlind`](#object-cerberubsjumpblind) | Object | AI Logic: Blind jump attack pattern for Cerberubs. | 1 ||
| [`CerberubsJumpNormal`](#object-cerberubsjumpnormal) | Object | AI Logic: Normal jump attack pattern for Cerberubs. | 1 ||
| [`CloseConvert`](#object-closeconvert) | Object | AI State: Logic for converting adjacent units. | 1 ||
| [`FoodMove`](#object-foodmove) | Object | AI Movement: Logic for seeking out food items. | 1 ||
| [`ForceTrample`](#object-forcetrample) | Object | Logic: Forces movement to act as a trample attack. | 1 ||
| [`LeapClose`](#object-leapclose) | Object | AI Movement: Executes a jumping maneuver to close distance. | 1 ||
| [`MoveForBarrage`](#object-moveforbarrage) | Object | AI Movement: Repositions to optimize a barrage attack. | 1 ||
| [`MoveForDash`](#object-movefordash) | Object | AI Movement: Repositions to set up a dash attack line. | 1 ||
| [`MoveForGrass`](#object-moveforgrass) | Object | AI Movement: Moves toward grass tiles. | 1 ||
| [`MoveForPounce`](#object-moveforpounce) | Object | AI Movement: Repositions to optimize a pounce trajectory. | 1 ||
| [`MoveForSpin`](#object-moveforspin) | Object | AI Movement: Repositions into a cluster of enemies for a spin attack. | 1 ||
| [`MoveOneForPuke`](#object-moveoneforpuke) | Object | AI Movement: Specific positioning logic for puke attacks. | 1 ||
| [`MoveSpaced`](#object-movespaced) | Object | AI Movement: Moves to maintain a specific distance from targets. | 1 ||
| [`MoveToHead`](#object-movetohead) | Object | AI Movement: Navigates toward the 'head' or primary target. | 1 ||
| [`MoveTowards`](#object-movetowards) | Object | AI Movement: Moves toward the nearest target. | 1 ||
| [`NCGravecrawlFAR`](#object-ncgravecrawlfar) | Object | AI Movement: Specific grapple/crawl logic. | 1 ||
| [`ReturnA`](#object-returna) | Object | Boss Logic: Specific phase return trigger. | 1 ||
| [`RunFar`](#object-runfar) | Object | AI Movement: Maximize distance from targets. | 1 ||
| [`SuckMF`](#object-suckmf) | Object | Character Form: Behavior and stats for the 'SuckMF' state. | 1 ||
| [`TF_TargetAllies`](#object-tf_targetallies) | Object | AI Targeting: Prioritizes allies. | 1 ||
| [`TF_TargetEnemies`](#object-tf_targetenemies) | Object | AI Targeting: Prioritizes enemies. | 1 ||
| [`Unflip`](#object-unflip) | Object | Logic: Reverses a flipped state. | 1 ||

</details>

---

### Object: `AddStatusToBasicAttack`


**Definition:** Injects a status effect payload that applies whenever the character performs a basic attack.  
**Total Count:** 32


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#object-randompassivepool), [`StacyMutant_Counter`](./Characters_and_Bosses.md#object-stacymutant_counter), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 205 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 56 |
| [`Bleed`](./Enums.md) | Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 30 | 2 |
| [`Poison`](./Enums.md) | Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 29 | 2 |
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is knocked back. | 24 | 3 |
| [`Burn`](./Enums.md) | Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 16 | 2 |
| [`Fear`](./Enums.md) | Integer | The number of Fear stacks applied, which reduces the target's accuracy and may cause it to flee; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 13 | 1 |
| [`Bruise`](./Enums.md) | Integer | The number of Bruise stacks applied, or an array with duration and chance. | 12 | 1 |
| [`Slow`](./Enums.md) | Integer | The number of turns of Slow applied, or an array with duration and chance. | 10 | 2 |
| [`Stun`](./Enums.md) | Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 8 | 1 |
| [`Confusion`](./Enums.md) | Integer | The number of turns of Confusion applied, or an array with duration and chance. | 7 | 1 |
| [`Weakness`](./Enums.md) | Integer | The number of Weakness stacks applied, which increases damage taken by the target; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 7 | 1 |
| [`Leech`](./Enums.md) | Integer | The amount of health stolen per hit as a percentage of damage dealt. | 5 | 2 |
| [`Rot`](./Enums.md) | Integer | The number of stacks of Rot, causing damage over time and potentially spawning a fly on death; can be an array `[stacks, probability]`. | 5 | 1 |
| [`Madness`](./Enums.md) | Integer | Specifies the number of Madness stacks applied, which cause the target to act randomly or attack allies; can be an integer, array `[stacks, probability]`, or a keyword alias. | 3 | 1 |
| [`RemoteLeech`](./Enums.md) | Integer | The amount of health the unit leeches from a distant target. | 2 | 1 |
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 1 | 2 |
| [`GainDisorderFromPool`](#object-gaindisorderfrompool) | Object | Specifies a pool of disorders or a custom chance to gain a disorder when the condition is met. | 1 ||
| [`Possessed`](./Enums.md) | Integer | The number of stacks of the Possessed status effect applied, which causes the unit to be controlled by an external force. | 1 | 1 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase (or decrease if negative) applied to a random stat. | 1 | -1 |
| [`RemoteFlatLeech`](./Enums.md) | Integer | The flat amount of health the unit leeches from a distant target. | 1 | 1 |

</details>

---

### Object: `DeathRattle`


**Definition:** No definition provided.  
**Total Count:** 29


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 13 ||
| `pop_corpse` | Boolean | If true, the unit's corpse is removed when this passive triggers. | 11 ||
| `is_dying_animation` | Boolean | If true, the unit plays its dying animation when this passive triggers. | 7 ||
| `cancel_knockback` | Boolean | If true, knockback effects are negated when this reaction triggers. | 1 ||
| `immediate` | Boolean | If true, the forced attack executes immediately without waiting. | 1 ||
| `must_target_killer` | Boolean | If true, the reaction must target the unit that killed it. | 1 ||
| `target_killer` | Boolean | If true, the reaction targets the unit that killed it. | 1 ||

</details>

---

### Object: `bonusturn_pattern`


**Definition:** AI Logic: Determines ability usage during bonus turns.  
**Total Count:** 27


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum | Specifies a single action the unit performs in this pattern step. | 15 ||
| [`do_priority`](./Arrays.md#array-do_priority) | Array | A list of actions executed in order of priority, stopping when one succeeds. | 4 ||
| [`do_all`](./Arrays.md#array-do_all) | Array | A list of actions the unit performs in sequence. | 4 ||
| [`do_strict`](./Arrays.md#array-do_strict) | Array | A list of actions executed in strict sequence. | 3 ||
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum | The unit moves before performing this single action. | 1 ||

</details>

---

### Object: `CatPartsTransform`


**Definition:** Transforms specific body parts into different visual variants.  
**Total Count:** 25


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveGroup`](./Characters_and_Bosses.md#object-passivegroup), [`StacyMutant_Brace`](./Characters_and_Bosses.md#object-stacymutant_brace), [`StacyMutant_Counter`](./Characters_and_Bosses.md#object-stacymutant_counter), [`StacyMutant_Damage`](./Characters_and_Bosses.md#object-stacymutant_damage), [`StacyMutant_DoubleHead`](./Characters_and_Bosses.md#object-stacymutant_doublehead), [`StacyMutant_Fire`](./Characters_and_Bosses.md#object-stacymutant_fire), [`StacyMutant_Health`](./Characters_and_Bosses.md#object-stacymutant_health), [`StacyMutant_Holy`](./Characters_and_Bosses.md#object-stacymutant_holy), [`StacyMutant_Ice`](./Characters_and_Bosses.md#object-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#object-stacymutant_lightning), [`StacyMutant_Mirror`](./Characters_and_Bosses.md#object-stacymutant_mirror), [`StacyMutant_Speed`](./Characters_and_Bosses.md#object-stacymutant_speed), [`StacyMutant_Thorns`](./Characters_and_Bosses.md#object-stacymutant_thorns), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`palette`](./Enums.md#enum-palette) | Enum / Integer | Index or list of palette indices used for coloring the entity or its variations. | 17 ||
| `ear1` | Integer | Sprite variant ID for the front ear. | 13 ||
| `tail` | Integer | Sprite variant ID for the tail. | 13 ||
| `arm2` | Number | The visual ID (integer/number) of the second arm part applied to the cat. | 11 ||
| `arm1` | Number | Sprite variant ID for the front arm. | 10 ||
| `ear2` | Integer | The visual ID (integer) of the second ear part applied to the cat. | 10 ||
| `leg1` | Integer | Sprite variant ID for the front leg. | 8 ||
| `leg2` | Integer | The visual ID (integer) of the second leg part applied to the cat. | 8 ||
| `head` | Enum / Number | Sprite variant ID for the head. | 6 ||
| `texture` | Integer | The visual ID (integer) of the texture applied to the cat. | 6 ||
| `body` | Number | Sprite variant ID for the body. | 5 ||
| `eye1` | Integer | The visual ID (integer) of the first eye part applied to the cat. | 3 ||
| `eye2` | Integer | The visual ID (integer) of the second eye part applied to the cat. | 3 ||

</details>

---

### Object: `fallback`


**Definition:** Logic executed if primary options fail.  
**Total Count:** 23


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum | Specifies a single action the unit performs in this pattern step. | 12 ||
| [`do_priority`](./Arrays.md#array-do_priority) | Array | A list of actions executed in order of priority, stopping when one succeeds. | 6 ||
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum | The unit moves before performing this single action. | 1 ||
| [`do_all`](./Arrays.md#array-do_all) | Array | A list of actions the unit performs in sequence. | 1 ||
| [`do_best`](./Arrays.md#array-do_best) | Array | A list of actions evaluated for optimal outcome; the best one is chosen. | 1 ||
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array | A list of actions that cause the unit to skip its turn. | 1 ||
| [`do_random`](./Arrays.md#array-do_random) | Array | A list of actions from which one is chosen at random. | 1 ||

</details>

---

### Object: `BossRewards`


**Definition:** Loot logic: Rewards dropped upon defeating a boss.  
**Total Count:** 20


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`common`](./Engine_EventKeys.md#valid-property-keys) | `String` | Specifies the common reward table or specific reward given. | 20 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 20 ||
| [`rare`](./Engine_EventKeys.md#valid-property-keys) | `String` | Specifies the rare reward table or specific reward given. | 16 ||

</details>

---

### Object: `AbilityReaction`


**Definition:** No definition provided.  
**Total Count:** 19


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 10 ||
| `ability_damage_only` | Boolean | If true, this reaction only triggers from damage caused by abilities. | 7 ||
| `backstabs_only` | Boolean | If true, this reaction only triggers when the unit is backstabbed. | 3 ||
| `only_when_not_your_turn` | Boolean | If true, this reaction only triggers when it is not the unit's turn. | 3 ||
| `cancel_knockback` | Boolean | If true, knockback effects are negated when this reaction triggers. | 1 ||
| `enemies_only` | Boolean | If true, this effect only targets enemies. | 1 ||
| `even_on_0_damage` | Boolean | If true, this reaction triggers even when no damage is dealt. | 1 ||
| `even_on_0_damage_if_knockback` | Boolean | If true, this reaction triggers on zero-damage hits if knockback occurred. | 1 ||
| `match_knockback_direction` | Boolean | If true, the reaction's knockback direction matches the triggering knockback's direction. | 1 ||
| `ranged_only` | Boolean | If true, this reaction only triggers from ranged attacks. | 1 ||
| `verify_target` | Boolean | If true, the game checks the target is valid before executing the reaction. | 1 ||

</details>

---

### Object: `MeleeRevengeDamage`


**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 19


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#object-temppassiveuntilsettled), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 70 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging impact triggers. | 47 ||
| `knockback` | Enum / Integer | The number of tiles to push the target away from the attacker; can be negative to pull the target closer, or 'str' to scale with the attacker's strength stat. | 24 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 22 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 10 ||
| [`elements`](./Arrays.md#array-elements) | Array | A list of elemental types applied to the damage instance, such as Heat or Fire, used for weaknesses, resistances, and visual effects. | 10 ||
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target, bypassing accuracy and evasion checks. | 1 ||

</details>

---

### Object: `ally_rewards`


**Definition:** Loot logic triggered if an ally dies.  
**Total Count:** 18


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BirdRewards`](./Characters_and_Bosses.md#object-birdrewards)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 18 ||
| [`FindItemFromPool`](./Enums.md) | Enum | Determines the item pool name from which a random item is granted to the source. | 16 | eagle_pool |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Defines a random roll with odds; if successful, the specified effects are applied. | 2 ||
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | An object listing possible status effects to randomly pick from and apply. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `alt_spawn_pool`


**Definition:** Alternative pools to draw minions from.  
**Total Count:** 18


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Antidote`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Float | Applies or references the 'Antidote' effect/state. | 5 ||
| `Blessing` | Float | Applies or references the 'Blessing' effect/state. | 5 ||
| [`BigCatnip`](Engine_LogicKeys.md#object-bigcatnip) | Integer / Object | Applies or references the 'BigCatnip' effect/state. | 4 ||
| [`BiggestFood`](Engine_LogicKeys.md#object-biggestfood) | Integer / Object | Applies or references the 'BiggestFood' effect/state. | 4 ||
| [`BigScrap`](Engine_LogicKeys.md#object-bigscrap) | Number / Object | Applies or references the 'BigScrap' effect/state. | 4 ||
| [`Coin`](Engine_LogicKeys.md#object-coin) | Integer / Object | Applies or references the 'Coin' effect/state. | 4 ||
| [`BigFood`](Engine_LogicKeys.md#object-bigfood) | Integer / Object | Applies or references the 'BigFood' effect/state. | 2 ||
| `Coin10` | Float | Applies or references the 'Coin10' effect/state. | 2 ||
| [`Coin3`](Engine_LogicKeys.md#object-coin3) | Integer / Object | Applies or references the 'Coin3' effect/state. | 2 ||
| [`Coin4`](Engine_LogicKeys.md#object-coin4) | Integer / Object | Applies or references the 'Coin4' effect/state. | 2 ||
| [`MedCatnip`](Engine_LogicKeys.md#object-medcatnip) | Integer / Object | Applies or references the 'MedCatnip' effect/state. | 2 ||
| [`MedScrap`](Engine_LogicKeys.md#object-medscrap) | Integer / Object | Applies or references the 'MedScrap' effect/state. | 2 ||
| [`RandomArmorPickup`](Engine_LogicKeys.md#object-randomarmorpickup) | Number / Object | Applies or references the 'RandomArmorPickup' effect/state. | 2 ||
| [`RandomCatnipPickup`](Engine_LogicKeys.md#object-randomcatnippickup) | Integer / Object | Applies or references the 'RandomCatnipPickup' effect/state. | 2 ||
| [`RandomFoodPickup`](Engine_LogicKeys.md#object-randomfoodpickup) | Integer / Object | Applies or references the 'RandomFoodPickup' effect/state. | 2 ||
| [`Bear`](Engine_LogicKeys.md#object-bear) | Integer / Object | Applies or references the 'Bear' effect/state. | 1 ||
| [`BlackBird`](Engine_LogicKeys.md#object-blackbird) | Integer / Object | Applies or references the 'BlackBird' effect/state. | 1 ||
| [`Catepillar`](Engine_LogicKeys.md#object-catepillar) | Integer / Object | Applies or references the 'Catepillar' effect/state. | 1 ||
| [`Catnip`](Engine_LogicKeys.md#object-catnip) | Integer / Object | Applies or references the 'Catnip' effect/state. | 1 ||
| [`CharmedDip`](Engine_LogicKeys.md#object-charmeddip) | Integer / Object | Applies or references the 'CharmedDip' effect/state. | 1 ||
| [`CharmedFloater`](Engine_LogicKeys.md#object-charmedfloater) | Integer / Object | Applies or references the 'CharmedFloater' effect/state. | 1 ||
| [`CharmedPile`](Engine_LogicKeys.md#object-charmedpile) | Integer / Object | Applies or references the 'CharmedPile' effect/state. | 1 ||
| [`Cherub`](Engine_LogicKeys.md#object-cherub) | Integer / Object | Applies or references the 'Cherub' effect/state. | 1 ||
| [`Chicken`](Engine_LogicKeys.md#object-chicken) | Integer / Object | Applies or references the 'Chicken' effect/state. | 1 ||
| [`Coin2`](Engine_LogicKeys.md#object-coin2) | Integer / Object | Applies or references the 'Coin2' effect/state. | 1 ||
| [`Dove`](Engine_LogicKeys.md#object-dove) | Integer / Object | Applies or references the 'Dove' effect/state. | 1 ||
| [`Eagle`](Engine_LogicKeys.md#object-eagle) | Integer / Object | Applies or references the 'Eagle' effect/state. | 1 ||
| [`Food`](Engine_LogicKeys.md#object-food) | Integer / Object | Applies or references the 'Food' effect/state. | 1 ||
| [`Harpy`](Engine_LogicKeys.md#object-harpy) | Integer / Object | Applies or references the 'Harpy' effect/state. | 1 ||
| [`HummingBird`](Engine_LogicKeys.md#object-hummingbird) | Integer / Object | Applies or references the 'HummingBird' effect/state. | 1 ||
| [`LargeBirdPool`](Engine_LogicKeys.md#object-largebirdpool) | Integer / Object | Applies or references the 'LargeBirdPool' effect/state. | 1 ||
| [`MedBirdPool`](Engine_LogicKeys.md#object-medbirdpool) | Integer / Object | Applies or references the 'MedBirdPool' effect/state. | 1 ||
| [`Mutant`](#object-mutant) | Integer / Object | Character Form: Behavior and stats for the 'Mutant' state. | 1 ||
| [`Pigeon`](Engine_LogicKeys.md#object-pigeon) | Integer / Object | Applies or references the 'Pigeon' effect/state. | 1 ||
| [`RandomBiggerArmorPickup`](Engine_LogicKeys.md#object-randombiggerarmorpickup) | Number / Object | Applies or references the 'RandomBiggerArmorPickup' effect/state. | 1 ||
| [`RandomBiggerCatnipPickup`](Engine_LogicKeys.md#object-randombiggercatnippickup) | Integer / Object | Applies or references the 'RandomBiggerCatnipPickup' effect/state. | 1 ||
| [`RandomBiggerFoodPickup`](Engine_LogicKeys.md#object-randombiggerfoodpickup) | Integer / Object | Applies or references the 'RandomBiggerFoodPickup' effect/state. | 1 ||
| [`Raven`](Engine_LogicKeys.md#object-raven) | Integer / Object | Applies or references the 'Raven' effect/state. | 1 ||
| [`Scrap`](Engine_LogicKeys.md#object-scrap) | Integer / Object | Applies or references the 'Scrap' effect/state. | 1 ||
| [`Seagull`](Engine_LogicKeys.md#object-seagull) | Integer / Object | Applies or references the 'Seagull' effect/state. | 1 ||
| [`SmallBirdPool`](Engine_LogicKeys.md#object-smallbirdpool) | Integer / Object | Applies or references the 'SmallBirdPool' effect/state. | 1 ||
| [`Snake`](Engine_LogicKeys.md#object-snake) | Integer / Object | Applies or references the 'Snake' effect/state. | 1 ||
| [`Squirrel`](Engine_LogicKeys.md#object-squirrel) | Integer / Object | Applies or references the 'Squirrel' effect/state. | 1 ||
| [`Toad`](Engine_LogicKeys.md#object-toad) | Integer / Object | Applies or references the 'Toad' effect/state. | 1 ||
| [`Turkey`](Engine_LogicKeys.md#object-turkey) | Integer / Object | Applies or references the 'Turkey' effect/state. | 1 ||
| [`Turtle`](Engine_LogicKeys.md#object-turtle) | Integer / Object | Applies or references the 'Turtle' effect/state. | 1 ||

</details>

---

### Object: `BirdRewards`


**Definition:** Loot logic: Rewards dropped by bird-type enemies.  
**Total Count:** 18


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ally_rewards`](#object-ally_rewards) | Object | Loot logic triggered if an ally dies. | 18 ||
| [`statuses`](#object-statuses) | Object | Status effects possessed by the character. | 5 ||

</details>

---

### Object: `CharacterLightSource`


**Definition:** Visual: Attaches a dynamic lighting source to the character.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `size` | Enum / Number | A scale multiplier for the spawned entity's visual size, specified as a single value or a randomized range [min, max]; 'gemini' uses a special sizing mode. | 16 ||
| [`color`](./Arrays.md#array-color) | Array | An RGB color array or named color used for this visual effect. | 16 ||
| [`glow`](./Arrays.md#array-glow) | Array | Specifies the RGBA color values for the character's glow effect. | 8 ||

</details>

---

### Object: `HealthPickup`


**Definition:** Pickup Logic: Defines what happens when a health item is collected.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 15 ||
| `stored_food_value` | Integer | The amount of food value this pickup provides when consumed. | 15 ||
| [`frame_range`](./Arrays.md#array-frame_range) | Array | Specifies the animation frame range (start and end) for the pickup's sprite. | 15 ||
| `anything_eats` | Boolean | If true, any unit can consume this pickup, not just those with specific dietary restrictions. | 4 ||
| `force_frame` | Integer | Forces the pickup to display a specific animation frame. | 1 ||

</details>

---

### Object: `statuses`


**Definition:** Status effects possessed by the character.  
**Total Count:** 14


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BirdRewards`](./Characters_and_Bosses.md#object-birdrewards), [`Cat`](./Characters_and_Bosses.md#object-cat), [`NonCat`](./Characters_and_Bosses.md#object-noncat)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 ||
| [`AllStatsUp`](./Enums.md) | Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 4 | 2 |
| [`Consumed`](Abilities_and_Spells.md#object-consumed) | Object | An object defining behavior when a buddy is consumed, including instant kill or status application. | 4 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `default`


**Definition:** Character Form: The baseline default behavior state.  
**Total Count:** 13


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `effects`
### Object: `effects`

**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 13


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Characters_and_Bosses.md#object-meleerevengedamage), [`damage_instance`](./Characters_and_Bosses.md#object-damage_instance), [`eat_damage`](./Characters_and_Bosses.md#object-eat_damage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1695 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 750 ||
| [`Stun`](./Enums.md) | Integer | The number of Stun stacks applied, which prevents the target from taking actions; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 98 | 1 |
| [`Burn`](./Enums.md) | Integer | The number of Burn stacks applied, which deals fire damage over time; can be an integer, a variable X, or an array `[stacks, probability]` to specify chance of application. | 85 | 2 |
| [`Confusion`](./Enums.md) | Integer | The number of turns of Confusion applied, or an array with duration and chance. | 37 | 1 |
| [`ConstitutionUp`](./Enums.md) | Integer | The amount of Constitution (HP) increase, or an array with duration and chance. | 22 | -1 |
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 21 ||
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 12 | 2 |
| `BlackHoleSuck` | `Number` | Applies or references the 'BlackHoleSuck' effect/state. | 1 ||

</details>

---

### Object: `ImmediateAbilityReaction`


**Definition:** No definition provided.  
**Total Count:** 13


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 13 ||
| `ability_damage_only` | Boolean | If true, this reaction only triggers from damage caused by abilities. | 6 ||
| `backstabs_only` | Boolean | If true, this reaction only triggers when the unit is backstabbed. | 2 ||
| `damage_threshold` | Integer | The amount of damage taken that triggers this immediate ability reaction. | 2 ||
| `even_if_blocked` | Boolean | If true, the reaction triggers even if the damage was blocked. | 2 ||
| `even_if_stunned` | Boolean | If true, the reaction triggers even if the unit is stunned. | 2 ||
| `health_threshold` | Integer | The health threshold (absolute HP value) that triggers the reaction. Use -1 for no threshold. | 2 ||
| `buddy_damage_only` | Boolean | If true, the reaction only triggers from damage dealt by the unit's buddy. | 1 ||
| `target_furthest_valid` | Boolean | If true, the reaction targets the furthest valid target instead of the closest. | 1 ||

</details>

---

### Object: `AbilityHealthThreshold`


**Definition:** AI Trigger: Executes an ability when health drops below a specific threshold.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 13 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 ||
| [`threshold`](./Enums.md) | Enum / Integer | The health threshold value (absolute or equation) at which this ability becomes available. | 12 | 200 |
| `even_if_stunned` | Boolean | If true, the reaction triggers even if the unit is stunned. | 7 ||
| `immediate` | Boolean | If true, the forced attack executes immediately without waiting. | 6 ||
| `use_ai` | Boolean | If true, the AI decides whether to use the ability when the threshold is met. | 2 ||
| `also_use_if_buddy_is_dead` | Boolean | If true, the ability can still be used at threshold if the unit's buddy is dead. | 1 ||
| [`threshold_min`](./Math_Equations.md) | Equation | Specifies the minimum health threshold (as an equation) for the ability to be available. | 1 ||

</details>

---

### Object: `PassiveGroup`


**Definition:** Passive: A collection of passives grouped together for easier management.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#object-randompassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 13 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Specifies which cat body part IDs to transform into upon applying the effect. | 12 ||
| [`FormChange`](./Enums.md) | Enum | Specifies the target form name or an object with form parameters and optional side effects (e.g., faction change, healing). | 12 | Druid |
| [`ReplaceBasicAttack`](./Enums.md) | Enum | Specifies the name of the ability that replaces the unit's basic attack. | 11 | BasicStraightShot |
| [`SelfStatusCarefulness`](./Enums.md) | Integer | The weight value for carefulness when applying status effects to self from this passive group. | 2 | 1 |
| [`StatusCarefulness`](./Enums.md) | Integer | The weight value for carefulness when applying status effects to others from this passive group. | 2 | 1 |
| [`ExtraBasicAttacks`](./Enums.md) | Integer | The number of additional basic attacks the unit can perform each turn. | 1 | 1 |
| [`TinkererBasicAttackSwitching`](Cat_Classes.md#object-tinkererbasicattackswitching) | Object | Object containing craft_ability and throw_ability names, enabling the Tinkerer to switch between crafting and throwing basic attacks. | 1 ||

</details>

---

### Object: `round_end_bonusturn_pattern`


**Definition:** AI Logic: Ability usage pattern during round-end bonus turns.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_all`](./Arrays.md#array-do_all) | Array | A list of actions the unit performs in sequence. | 6 ||
| [`do`](./Enums.md#enum-do) | Enum | Specifies a single action the unit performs in this pattern step. | 3 ||
| [`do_one`](./Arrays.md#array-do_one) | Array | Specifies an array of ability references that will be used for one round-end bonus turn pattern. | 2 ||
| [`do_random`](./Arrays.md#array-do_random) | Array | A list of actions from which one is chosen at random. | 2 ||
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array | A list of actions that cause the unit to skip its turn. | 1 ||
| [`do_priority`](./Arrays.md#array-do_priority) | Array | A list of actions executed in order of priority, stopping when one succeeds. | 1 ||

</details>

---

### Object: `SpawnThingOnDamage`


**Definition:** Applies or references the 'SpawnThingOnDamage' effect/state.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 38 ||
| `good` | Boolean | The outcome block triggered on successful condition when spawning something on damage. | 20 ||
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Probability (0.0 to 1.0) of executing this action. | 12 ||
| `spawn_on_death_hit` | Boolean | If true, the spawn occurs specifically when the damaging hit kills the target. | 10 ||
| `coins` | Integer | The amount of coins (or a random range [min max]) awarded when the spawn trigger occurs. | 2 ||
| `consider_all_layers` | Boolean | If true, considers all map layers when determining spawn location. | 2 ||
| [`auto_cast`](./Enums.md#enum-auto_cast) | Enum | Specifies the ability to automatically cast when the spawn trigger occurs. | 1 ||
| `melee_ability_only` | Boolean | If true, the trigger only activates from melee ability damage. | 1 ||

</details>

---

### Object: `DeathRattleRevive`


**Definition:** No definition provided.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 8 ||
| `even_if_stunned` | Boolean | If true, the reaction triggers even if the unit is stunned. | 8 ||

</details>

---

### Object: `MoveWhenDamaged`


**Definition:** No definition provided.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Array / Enum | An array of three weighting values or a named preset for Crazy Eye background behavior weights. | 9 ||
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the ability used to move when damaged. | 2 ||

</details>

---

### Object: `Rage`


**Definition:** Character Form: Behavior and stats for the \'Rage\' state.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 8 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 6 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 6 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 4 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| `move_speed_multiplier` | Number | A multiplier for the unit's movement animation speed. Values above 1 increase speed. | 1 ||

</details>

---

### Object: `FormChangeOnElementInfluence`


**Definition:** Logic: Changes form when affected by an element.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the form name (e.g., "Big", "Small", "Angry") the unit transforms into. | 9 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 9 ||
| [`exclude`](./Enums.md#enum-exclude) | Enum | Specifies an element type that is excluded from triggering the form change. | 5 ||
| [`particle`](./Enums.md#enum-particle) | Enum | Specifies the particle effect to play on form change. | 5 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Specifies the sound effect to play on form change. | 5 ||

</details>

---

### Object: `ReflectProjectiles`


**Definition:** No definition provided.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusCollector`


**Definition:** Passive: Gains benefits based on the number of statuses applied to them.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 ||
| [`StrengthUp`](./Enums.md) | Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 7 | 2 |
| [`Poison`](./Enums.md) | Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 4 | 2 |
| [`Slow`](./Enums.md) | Integer | The number of turns of Slow applied, or an array with duration and chance. | 4 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `TransformInXTurns`


**Definition:** Logic: Forces a form change after X turns.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#object-randompassivepool), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 8 ||
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 8 ||
| [`initiative`](./Enums.md#enum-initiative) | Enum / Integer | Determines the unit's turn order position; lower values act earlier. | 4 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation clip to use for the ability’s meta representation. | 2 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||

</details>

---

### Object: `TransformOnElementInfluence`


**Definition:** Logic: Changes form when affected by elements.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 9 ||
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 9 ||

</details>

---

### Object: `FormChangeOffMap`


**Definition:** Logic: Changes form when pushed off the map.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_offmap`](./Enums.md#enum-form_offmap) | Enum | Specifies the form to use when the unit is off the map. | 8 ||
| [`form_onmap`](./Enums.md#enum-form_onmap) | Enum | Specifies the form to use when the unit is on the map. | 8 ||

</details>

---

### Object: `SmallRockBehavior`


**Definition:** No definition provided.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 4 ||
| `knockback` | Enum / Integer | The number of tiles to push the target away from the attacker; can be negative to pull the target closer, or 'str' to scale with the attacker's strength stat. | 4 ||
| `chain` | Boolean | Specifies the chain effect type (e.g., 'splashM') or 'true' to enable chaining. | 2 ||

</details>

---

### Object: `ChanceToSpitOnDamage`


**Definition:** Reaction: Probability to use a spit counter-attack when damaged.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 7 ||
| `flat_chance` | Integer | The flat percentage chance to spit when damaged. | 5 ||
| `chance_per_damage` | Integer | The percentage chance to spit per point of damage taken. | 3 ||
| `backstabs_only` | Boolean | If true, this reaction only triggers when the unit is backstabbed. | 1 ||
| `even_on_0_damage_if_knockback` | Boolean | If true, this reaction triggers on zero-damage hits if knockback occurred. | 1 ||

</details>

---

### Object: `MovementReaction`


**Definition:** Reaction: Triggers an effect or ability when forced to move.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 11 ||
| `enemies_only` | Boolean | If true, this effect only targets enemies. | 7 ||
| `on_self_move_too` | Boolean | If true, the movement reaction also triggers when the unit moves itself. | 3 ||
| `objects_too` | Boolean | If true, the movement reaction also considers objects moving. | 2 ||
| `blind_spot` | Boolean | If true, the movement reaction only triggers from positions not in the unit's line of sight. | 1 ||
| `forward_only` | Boolean | If true, the movement reaction only triggers when movement occurs in the unit's forward direction. | 1 ||
| `self_move_exclude_self_abilities` | Boolean | If true, the movement reaction excludes movement caused by the unit's own abilities. | 1 ||

</details>

---

### Object: `CaveFamilyEnrage`


**Definition:** AI Trigger: Enrage logic triggered when a cave family member is killed.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 6 ||
| `count` | Array / Integer | The numerical quantity. | 6 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specific entity tag required. | 6 ||

</details>

---

### Object: `FormChangeWhilePrimingAbility`


**Definition:** Logic: Changes form while preparing/priming a specific ability.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`priming`](./Enums.md#enum-priming) | Enum | Specifies the form to switch to when the unit is priming an ability. | 6 ||
| [`not_priming`](./Enums.md#enum-not_priming) | Enum | Specifies the form to switch to when the unit is not priming an ability. | 6 ||

</details>

---

### Object: `MoveTowardsDamageSource`


**Definition:** No definition provided.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the ability used to move when damaged. | 5 ||
| `move_far` | Boolean | If true, the unit moves as far as possible towards the damage source. | 4 ||
| [`check_in_form`](./Enums.md#enum-check_in_form) | Enum | Specifies the form that the unit must be in for this movement to trigger. | 2 ||
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| `can_move_zero` | Boolean | If true, the unit can move even if the distance to the damage source is zero. | 1 ||
| [`check_has_status`](./Enums.md#enum-check_has_status) | Enum | Specifies a status effect that the unit must have for this movement to trigger. | 1 ||
| `do_not_move_on_top` | Boolean | If true, the unit will not move onto the same tile as the damage source. | 1 ||
| `face_towards_after` | Boolean | If true, the unit faces the damage source after moving. | 1 ||
| [`ignore_tagged_sources`](./Enums.md#enum-ignore_tagged_sources) | Enum | Specifies a tag that, if present on the damage source, causes the movement to be ignored. | 1 ||
| `move_short` | Boolean | If true, the unit moves a short distance towards the damage source. | 1 ||

</details>

---

### Object: `SecurityBotProtect`


**Definition:** AI Logic: Guarding behavior for Security Bot units.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 7 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 5 ||
| `enemies_only` | Boolean | If true, this effect only targets enemies. | 3 ||
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum | Specifies a tag that restricts which units receive protection from this passive. | 3 ||
| `not_on_kill` | Boolean | If true, the protection does not trigger when the protected unit is killed. | 2 ||

</details>

---

### Object: `HasCat`


**Definition:** Character Form: Behavior and stats for the \'HasCat\' state.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 5 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 5 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 4 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 4 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||

</details>

---

### Object: `MoveTowardsKillers`


**Definition:** No definition provided.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the ability used to move when damaged. | 3 ||
| [`character_filter`](./Arrays.md#array-character_filter) | Array | Specifies the list of character types that the unit will move towards. | 3 ||

</details>

---

### Object: `PassiveWhileHasStatus`


**Definition:** Passive: Activates only while the character has the specified status.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 6 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 6 ||

</details>

---

### Object: `TransformOnDeathImmediately`


**Definition:** No definition provided.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum | Determines when the spawned entity takes its first action, such as 'initiative' (immediately), 'next_turn' (after current unit), 'end_of_round', or 'next_round'. | 4 ||
| [`obj`](./Enums.md#enum-obj) | Array / Enum | The object(s) spawned when this passive triggers. | 4 ||

</details>

---

### Object: `BaitAura`


**Definition:** Passive: Projects an aura that attracts specific enemy types (e.g., flies/maggots).  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `range` | Enum / Integer | Distance or area of effect in tiles. | 4 ||

</details>

---

### Object: `Big`


**Definition:** Character Form / AI State: Behavior and stats for the \'Big\' state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A string or number appended to the base animation name to identify the specific animation variant. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Consumed`


**Definition:** State object triggered when this object or entity is eaten/consumed by another character.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`statuses`](./Characters_and_Bosses.md#object-statuses)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 22 ||
| [`struggle_ability`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Ability triggered by the consumed entity while inside the consumer. | 17 ||
| `force_contact` | `Boolean` | If true, enforces physical overlap. | 15 ||
| `instant` | `Boolean` | If true, the consumption (e.g., grabbing, eating) happens instantly without animation delay. | 12 ||
| [`mount_mode`](./Engine_LogicKeys.md#valid-property-keys) | `String` | If true, treats the consumption as riding/mounting instead of eating. | 12 ||
| `do_not_pop_corpse` | `Boolean` | If true, the consumed unit's corpse is not spawned or popped into the world. | 11 ||
| [`drop_on_death`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies whether and how the consumed unit is dropped upon death. "deferred" delays the drop, "true" forces it, "false" prevents it. | 11 ||
| `use_placeholder` | Boolean | If true, a placeholder graphic is used instead of the intended animation. | 3 ||

</details>

---

### Object: `ForceUseAbility`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossHitCountdownBoris`](./Characters_and_Bosses.md#object-finalbosshitcountdownboris), [`FinalBossHitCountdownExplosive`](./Characters_and_Bosses.md#object-finalbosshitcountdownexplosive)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 5 ||
| `show_name` | Boolean | If true, the ability's name is displayed when it is forced. | 2 ||

</details>

---

### Object: `Holy`


**Definition:** Character Form: Behavior and stats for the \'Holy\' state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `hot`


**Definition:** Visual effect indicator.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 4 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 4 ||

</details>

---

### Object: `MoveAway`


**Definition:** AI Movement: Moves away from the target.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 4 ||

</details>

---

### Object: `MoveClose`


**Definition:** AI Movement: Moves into melee range.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 4 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Determines which animation or movement ability is used to close distance. | 3 ||

</details>

---

### Object: `OffMap`


**Definition:** Character Form: Behavior and stats for the 'OffMap' state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 3 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||

</details>

---

### Object: `passive`


**Definition:** Intrinsic passive modifier.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 ||

</details>

---

### Object: `StatusEachTurnEnd`


**Definition:** Applies or references the 'StatusEachTurnEnd' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 55 ||
| [`SpeedUp`](./Enums.md) | Integer | Specifies the number of Speed stacks applied, where each stack modifies the unit's turn order and dodge chance. | 5 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |
| [`AllStatsUp`](./Enums.md) | Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | 2 |
| [`Conditional_BadRoll`](Abilities_and_Spells.md#object-conditional_badroll) | Object | Defines a conditional effect that triggers on a bad roll with a given probability, optionally with an else clause. | 1 ||
| [`DivineShield`](./Enums.md) | Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 2 |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 1 | 5 |

</details>

---

### Object: `StatusOnKill`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 34 ||
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 5 | 5 |
| [`UseAbility_NonStack`](./Enums.md) | Enum | Specifies the ability to use on kill, but it will not stack with itself. | 3 | BBTransformZealot |

</details>

---

### Object: `StatusOnTookDamageFromAbility`


**Definition:** Event Trigger: Applies statuses when taking damage from an ability.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`ExtraBasicAttacks_Status`](./Enums.md) | Integer | The number of extra basic attacks the unit can perform each turn. Stacks for additional attacks. | 2 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`Bleed`](./Enums.md) | Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 2 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of health regeneration (HealthRegen) granted by this damage instance. | 1 | 2 |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the unit. | 1 | 1 |

</details>

---

### Object: `StunImmunity`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean | If true, applying StunImmunity removes existing stun effects. | 1 ||

</details>

---

### Object: `Trapper`


**Definition:** Character Form: Behavior and stats for the 'Trapper' state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 ||
| `cancel_movement` | Boolean | If true, the Trapper cancels the unit's movement when triggered. | 2 ||
| `pathfinding_avoidance` | Integer | The amount of pathfinding avoidance cost assigned to the trap tile. | 2 ||
| `range` | Enum / Integer | Distance or area of effect in tiles. | 2 ||

</details>

---

### Object: `AllAlive`


**Definition:** Encounter State: Logic executed when all specific entities are currently alive.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `ArmorPickup`


**Definition:** Pickup Logic: Defines what happens when an armor item is collected.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 3 ||
| [`frame_range`](./Arrays.md#array-frame_range) | Array | Specifies the animation frame range (start and end) for the pickup's sprite. | 3 ||

</details>

---

### Object: `Bomb`


**Definition:** Character Form / AI State: Behavior and stats for the 'Bomb' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Buddy`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the Buddy effect only targets allies. | 3 ||
| [`obj`](./Enums.md#enum-obj) | Array / Enum | The object(s) spawned when this passive triggers. | 3 ||
| `reclaim_if_lost` | Boolean | If true, the Buddy will attempt to be reclaimed if it becomes lost. | 1 ||

</details>

---

### Object: `Cat`


**Definition:** Character Form: Base form for standard cats.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#object-mothertumorpassive), [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#object-mothertumorspawnincapture)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum | Specifies the formchange name to apply when the cat is captured or present. | 3 ||
| [`statuses`](#object-statuses) | Object | Status effects possessed by the character. | 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation clip to use for the ability’s meta representation. | 1 ||

</details>

---

### Object: `CaveMan`


**Definition:** Character Form: Behavior and stats for the \'CaveMan\' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||

</details>

---

### Object: `Down`


**Definition:** Character Form: Behavior and stats for the \'Down\' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 3 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||

</details>

---

### Object: `Fire`


**Definition:** Character Form: Behavior and stats for the 'Fire' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `FormChangeHealthThreshold`


**Definition:** Logic: Changes form when health crosses a threshold.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_above`](./Enums.md#enum-form_above) | Enum | Specifies the form to change into when health is above the threshold. | 3 ||
| [`form_below`](./Enums.md#enum-form_below) | Enum | Specifies the form to change into when health is below the threshold. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`threshold`](./Enums.md) | Enum / Integer | The health threshold value (absolute or equation) at which this ability becomes available. | 3 | 200 |
| `count_shield` | Boolean | If true, shields are counted as health when evaluating the health threshold for form changes. | 1 ||

</details>

---

### Object: `Full`


**Definition:** Character Form: Behavior and stats for the \'Full\' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 ||
| [`statuses_on_enter_form`](#object-statuses_on_enter_form) | Object | Status effects instantly applied upon transitioning into this form. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 ||

</details>

---

### Object: `ManaPickup`


**Definition:** Pickup Logic: Defines what happens when a mana item is collected.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 3 ||
| [`frame_range`](./Arrays.md#array-frame_range) | Array | Specifies the animation frame range (start and end) for the pickup's sprite. | 3 ||

</details>

---

### Object: `NonCat`


**Definition:** Character Form: Behavior and stats for the 'NonCat' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#object-mothertumorpassive), [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#object-mothertumorspawnincapture)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum | Specifies the formchange name to apply when the cat is captured or present. | 3 ||
| [`statuses`](#object-statuses) | Object | Status effects possessed by the character. | 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation clip to use for the ability’s meta representation. | 1 ||

</details>

---

### Object: `OneAlive`


**Definition:** Encounter State: Logic executed when exactly one target is alive.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 3 ||

</details>

---

### Object: `RandomPassivePool`


**Definition:** Logic: Grants a random passive from the specified pool upon spawning.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`PassiveGroup`](#object-passivegroup) | Object | Defines a grouping of passives that can be randomly selected from the passive pool. | 2 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | An object defining status effects to apply on basic attacks, with optional conditions. | 1 ||
| [`TransformInXTurns`](#object-transforminxturns) | Object | Transforms the unit into another object after a set number of turns (stacks). | 1 ||

</details>

---

### Object: `ReplaceBrain`


**Definition:** Applies the 'ReplaceBrain' effect.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StacyMutant_Fire`](./Characters_and_Bosses.md#object-stacymutant_fire), [`StacyMutant_Ice`](./Characters_and_Bosses.md#object-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#object-stacymutant_lightning)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum | Specifies the AI brain type (e.g., NoBrain, PlayerBrain, GenericBrain). | 4 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 4 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 4 ||
| [`pattern`](#object-pattern) | Object | AI sequence logic. | 3 ||

</details>

---

### Object: `SquirrelForm`


**Definition:** Character Form: Behavior and stats for the 'SquirrelForm' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||

</details>

---

### Object: `SupportFormChangeInsteadOfRun`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| `wait_till_turn` | Boolean | If true, the support form change waits until the unit's turn instead of happening immediately. | 1 ||

</details>

---

### Object: `TwoAlive`


**Definition:** Encounter State: Logic executed when exactly two targets are alive.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 3 ||

</details>

---

### Object: `Up`


**Definition:** Character Form: Behavior and stats for the \'Up\' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 3 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||

</details>

---

### Object: `Water`


**Definition:** Character Form: Behavior and stats for the \'Water\' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `AbilityOnRoundEnd`


**Definition:** AI Trigger: Executes an ability at the end of the combat round.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| `force_display_name` | Boolean | If true, forces the display of the ability name even if it would otherwise be hidden. | 2 ||

</details>

---

### Object: `AbilityWhenTaggedCharacterMovesNear`


**Definition:** AI Trigger: Executes an ability when a character with a specific tag moves adjacent.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 5 ||
| `range` | Enum / Integer | Distance or area of effect in tiles. | 5 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specific entity tag required. | 5 ||

</details>

---

### Object: `active`


**Definition:** Defines actively executed abilities.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddTemporaryEffectsToBasicAttack`


**Definition:** Applies the 'AddTemporaryEffectsToBasicAttack' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fury` | Integer | Applies or references the 'Fury' effect/state. | 4 ||

</details>

---

### Object: `alternate_energized_effect`


**Definition:** Overrides default energized visuals.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Robot`](./Characters_and_Bosses.md#object-robot)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`FormChange`](./Enums.md) | Enum | Specifies the target form name or an object with form parameters and optional side effects (e.g., faction change, healing). | 1 | Druid |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp, increasing spell damage dealt by the unit. | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `AutocastEachRound`


**Definition:** Forces the character to automatically cast a specific ability at the start of each combat round.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 9 ||
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 6 ||

</details>

---

### Object: `Bishop`


**Definition:** Character Form / AI State: Behavior and stats for the \'Bishop\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `BlackHole`


**Definition:** Character Form / AI State: Behavior and stats for the \'BlackHole\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Boris`


**Definition:** Character Form / AI State: Behavior and stats for the \'Boris\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `BungaEntrance`


**Definition:** Animation/AI State: Bunga entering the arena.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| `even_if_stunned` | Boolean | If true, the reaction triggers even if the unit is stunned. | 2 ||
| `health_threshold` | Integer | The health threshold (absolute HP value) that triggers the reaction. Use -1 for no threshold. | 2 ||
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum | Specifies the tag used to identify summoned warriors for the Bunga entrance sequence. | 2 ||

</details>

---

### Object: `CaveBaby`


**Definition:** Character Form: Behavior and stats for the \'CaveBaby\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `CaveManSpear`


**Definition:** Character Form: Behavior and stats for the \'CaveManSpear\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||

</details>

---

### Object: `CaveWoman`


**Definition:** Character Form: Behavior and stats for the \'CaveWoman\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `CherubimReaction`


**Definition:** Reaction: Custom reaction triggers for Cherubim enemies.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Leave`](Engine_LogicKeys.md#object-leave) | Enum / Object | Applies or references the 'Leave' effect/state. | 2 ||
| [`Return`](Engine_LogicKeys.md#object-return) | Enum / Object | Applies or references the 'Return' effect/state. | 2 ||

</details>

---

### Object: `Conditional_GoodRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ally_rewards`](./Characters_and_Bosses.md#object-ally_rewards)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 37 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 37 | |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 28 ||
| [`FindItemFromPool`](./Enums.md) | Enum | Determines the item pool name from which a random item is granted to the source. | 5 | eagle_pool |

</details>

---

### Object: `Cultist`


**Definition:** Character Form: Behavior and stats for the \'Cultist\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `DashRandomly`


**Definition:** AI Movement: Dashes to a random valid tile.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 2 ||

</details>

---

### Object: `DiesToElement`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 1 ||
| `instant` | `Boolean` | If true, the consumption (e.g., grabbing, eating) happens instantly without animation delay. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

---

### Object: `dispersed_bonusturn_pattern`


**Definition:** AI Logic: Alternative bonus turn ability pattern.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum | Specifies a single action the unit performs in this pattern step. | 2 ||

</details>

---

### Object: `Empty`


**Definition:** Character Form: Behavior and stats for the \'Empty\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 ||

</details>

---

### Object: `Escape`


**Definition:** AI Movement: Logic for fleeing or escaping the map.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 ||

</details>

---

### Object: `Explosive`


**Definition:** Character Form: Behavior and stats for the \'Explosive\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `FaceLastDamage`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean | If true, uses the unit's turn animations for the face-last-damage effect. | 1 ||

</details>

---

### Object: `FireFull`


**Definition:** Character Form: Behavior and stats for the 'FireFull' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Flush`


**Definition:** Character Form: Behavior and stats for the 'Flush' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||

</details>

---

### Object: `FormChangeDuringWeatherElement`


**Definition:** Logic: Changes form automatically during specific weather conditions.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 2 ||
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the form name (e.g., "Big", "Small", "Angry") the unit transforms into. | 2 ||

</details>

---

### Object: `Holding`


**Definition:** Character Form: Behavior and stats for the \'Holding\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Johnny`


**Definition:** Character Form: Behavior and stats for the 'Johnny' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||

</details>

---

### Object: `KnockUpAndAway`


**Definition:** Displaces the target vertically and horizontally away from the source.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#object-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#object-conditional_isphysicalattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The distance in tiles to knock the target away. | 24 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 22 ||
| `displace` | Boolean | If true, the unit is displaced (teleported) by the knock up and away. | 2 ||
| [`self_damage`](./Enums.md) | Boolean / Integer | A damage instance object that applies damage and effects to the source unit itself. | 2 | 2 |
| [{Damaging Keys}](./Engine_DamagingKeys.md#valid-property-keys) | Object | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Object: `LastHit`


**Definition:** Logic: Executes logic on the final hit of a multi-hit attack.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||

</details>

---

### Object: `MotherTumorSpawnInCapture`


**Definition:** Boss Logic: Logic for capturing entities inside the Mother's tumors upon spawning.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](#object-cat) | Object | Character Form: Base form for standard cats. | 2 ||
| [`NonCat`](#object-noncat) | Object | Character Form: Behavior and stats for the 'NonCat' state. | 2 ||
| [`Nothing`](#object-nothing) | Object | Character Form: Behavior and stats for the 'Nothing' state. | 1 ||

</details>

---

### Object: `MoveCenter`


**Definition:** AI Movement: Moves toward the center of the map.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 ||

</details>

---

### Object: `MoveForThrow`


**Definition:** AI Movement: Repositions to gain line of sight for throwing.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Determines which animation or movement ability is used to close distance. | 2 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 ||

</details>

---

### Object: `Mutant`


**Definition:** Character Form: Behavior and stats for the \'Mutant\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move_speed_multiplier`](./Enums.md#enum-move_speed_multiplier) | Number | A multiplier for the unit's movement animation speed. Values above 1 increase speed. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `NeutronStar`


**Definition:** Character Form: Behavior and stats for the 'NeutronStar' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `NotPriming`


**Definition:** Character Form: Behavior and stats when not charging an ability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `Nuke`


**Definition:** Character Form: Behavior and stats for the 'Nuke' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `PassiveWhileNotHasStatus`


**Definition:** Passive: Activates only while the character does NOT have the specified status.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 ||

</details>

---

### Object: `Priming`


**Definition:** Character Form: Behavior and stats when charging an ability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 ||

</details>

---

### Object: `ProtectTargetedAllies`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| [`target_filter`](./Enums.md#enum-target_filter) | Enum | Specifies the target filter for the protect ability (e.g., 'any' or a specific unit type). | 2 ||

</details>

---

### Object: `Rain`


**Definition:** Character Form: Behavior and stats for the 'Rain' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||

</details>

---

### Object: `RemoveStatusStacks`


**Definition:** Removes a specific number of stacks of a status effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Characters_and_Bosses.md#object-statusonendmove), [`StatusOnTookDamage`](./Characters_and_Bosses.md#object-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | The number of stacks to remove. | 4 ||
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 4 ||

</details>

---

### Object: `SlotMachineRollPool`


**Definition:** Logic: Defines the possible outcomes for slot machine enemies.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SlotResult_Jackpot_Coins`](Engine_LogicKeys.md#object-slotresult_jackpot_coins) | Integer / Object | Applies or references the 'SlotResult_Jackpot_Coins' effect/state. | 2 ||
| [`SlotResult_Explode`](Engine_LogicKeys.md#object-slotresult_explode) | Integer / Object | Applies or references the 'SlotResult_Explode' effect/state. | 1 ||
| [`SlotResult_Nothing`](Engine_LogicKeys.md#object-slotresult_nothing) | Integer / Object | Applies or references the 'SlotResult_Nothing' effect/state. | 1 ||
| [`SlotResult_RandomPickup`](Engine_LogicKeys.md#object-slotresult_randompickup) | Integer / Object | Applies or references the 'SlotResult_RandomPickup' effect/state. | 1 ||

</details>

---

### Object: `Small`


**Definition:** Character Form: Behavior and stats for the \'Small\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||

</details>

---

### Object: `SpearRun`


**Definition:** AI Movement: Specific movement logic for Spear enemies.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Determines which animation or movement ability is used to close distance. | 2 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 2 ||

</details>

---

### Object: `statuses_on_enter_form`


**Definition:** Status effects instantly applied upon transitioning into this form.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Full`](./Characters_and_Bosses.md#object-full)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusGroup`


**Definition:** Groups multiple status effects together for batch application.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Characters_and_Bosses.md#object-randomstatusfrompool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [`FindItemFromPool`](./Enums.md) | Enum | Determines the item pool name from which a random item is granted to the source. | 2 | eagle_pool |

</details>

---

### Object: `StatusOnSpawnIn`


**Definition:** Event Trigger: Applies statuses immediately when spawned.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnTookDamage`


**Definition:** Event Trigger: Applies nested statuses when took damage.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 38 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 14 |
| [`StrengthUp`](./Enums.md) | Integer | Specifies the number of Strength stacks applied, where positive values increase melee damage and negative values decrease it. | 4 | 2 |
| [`ConstitutionUp`](./Enums.md) | Integer | The amount of Constitution (HP) increase, or an array with duration and chance. | 3 | -1 |
| [`RemoveStatusStacks`](Abilities_and_Spells.md#object-removestatusstacks) | Object | Defines a status and number of stacks to remove from the target when status is applied on taking damage. | 1 ||

</details>

---

### Object: `TempPassiveUntilSettled`


**Definition:** Passive: Active only until the physics engine stops moving the character.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#object-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#object-conditional_isphysicalattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object | A damage instance object that triggers when the unit is hit by melee attacks while this passive is active. | 2 ||

</details>

---

### Object: `TinkererBasicAttackSwitching`


**Definition:** Logic: Allows Tinkerer to swap basic attacks.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveGroup`](./Characters_and_Bosses.md#object-passivegroup), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum | Specifies the ability used for crafting in the Tinkerer's basic attack switching. | 3 ||
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum | Specifies the ability used for throwing in the Tinkerer's basic attack switching. | 3 ||

</details>

---

### Object: `TransformOnElementInfluencex`


**Definition:** Logic: Variant element influence transformation.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 2 ||
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 2 ||

</details>

---

### Object: `Turtled`


**Definition:** Character Form: Behavior and stats for the 'Turtled' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 2 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 2 ||

</details>

---

### Object: `WereMan`


**Definition:** Character Form: Behavior and stats for the \'WereMan\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Zealot`


**Definition:** Character Form: Behavior and stats for the \'Zealot\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `additional_statuses`


**Definition:** Generic statuses added to the character.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnOnDeath`](./Characters_and_Bosses.md#object-spawnondeath)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`PermanentMadness`](./Enums.md) | Integer | If set to 1, the Madness status is permanent and will never expire; can use an alias for the status. | 1 | 1 |

</details>

---

### Object: `AddStatusToReceivedDamage`


**Definition:** Modifier: Applies a status effect whenever the character takes damage.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToSpells`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToTrampleDamage`


**Definition:** Applies the 'AddStatusToTrampleDamage' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Characters_and_Bosses.md#object-passivewhendead)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToWeapons`


**Definition:** Applies the 'AddStatusToWeapons' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`Bleed`](./Enums.md) | Integer | The number of Bleed stacks applied, which deals bleeding damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 3 | 2 |

</details>

---

### Object: `AdventureTokenPassivePool`


**Definition:** Map/Metaprogression: Pool of passive modifiers applied by adventure tokens.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`StacyMutant_Brace`](#object-stacymutant_brace) | Object | Defines the Brace passive and associated cat part transformations for the StacyMutant adventure token. | 1 ||
| [`StacyMutant_Counter`](#object-stacymutant_counter) | Object | Defines the CounterAttack passive and associated cat part transformations for the StacyMutant adventure token. | 1 ||
| [`StacyMutant_Damage`](#object-stacymutant_damage) | Object | Defines the damage bonus, max health penalty, and cat part transformations for the StacyMutant adventure token. | 1 ||
| [`StacyMutant_DoubleHead`](#object-stacymutant_doublehead) | Object | Defines the extra turns and cat part transformations for the StacyMutant adventure token. | 1 ||
| [`StacyMutant_Fire`](#object-stacymutant_fire) | Object | Defines the fire immunity, basic attack replacement, and cat part transformations for the StacyMutant adventure token. | 1 ||
| [`StacyMutant_Health`](#object-stacymutant_health) | Object | Defines the max health bonus, speed penalty, size scale, and cat part transformations for the StacyMutant adventure token. | 1 ||
| [`StacyMutant_Holy`](#object-stacymutant_holy) | Object | Defines the DivineShield and cat part transformations for the StacyMutant adventure token. | 1 ||
| [`StacyMutant_Ice`](#object-stacymutant_ice) | Object | Defines the ice immunity, basic attack replacement, movement penalty, and cat part transformations for the StacyMutant adventure token. | 1 ||
| [`StacyMutant_Lightning`](#object-stacymutant_lightning) | Object | Defines the lightning immunity, basic attack replacement, and cat part transformations for the StacyMutant adventure token. | 1 ||
| [`StacyMutant_Mirror`](#object-stacymutant_mirror) | Object | Defines the projectile reflection and automatic magic missile for the StacyMutant adventure token. | 1 ||
| [`StacyMutant_Speed`](#object-stacymutant_speed) | Object | Defines the damage penalty, speed bonus, size scale, and cat part transformations for the StacyMutant adventure token. | 1 ||
| [`StacyMutant_Thorns`](#object-stacymutant_thorns) | Object | Defines the Thorns passive and cat part transformations for the StacyMutant adventure token. | 1 ||

</details>

---

### Object: `AggroTargetIsGovernedByHitEffect`


**Definition:** AI Logic: Forces the character's aggro to follow specific hit effects rather than default proximity.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | If true, this effect only targets enemies. | 1 ||

</details>

---

### Object: `ai_if_spawned_as_enemy`


**Definition:** AI logic override used only if the character is spawned as an enemy.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum | Specifies the AI brain type (e.g., NoBrain, PlayerBrain, GenericBrain). | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||
| [`pattern`](#object-pattern) | Object | AI sequence logic. | 1 ||

</details>

---

### Object: `Alert`


**Definition:** AI State: The behavior profile used when the character is alerted to enemies.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `AllStatsAura`


**Definition:** Passive: Projects an aura that modifies all primary stats of nearby characters.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aura_requires_tag`](./Enums.md#enum-aura_requires_tag) | Enum | Specifies the tag required for units to be affected by the all-stats aura. | 1 ||
| [`range`](./Enums.md#enum-range) | Enum / Integer | Distance or area of effect in tiles. | 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||

</details>

---

### Object: `Attacker`


**Definition:** AI Role: Designates the character as an attacker rather than support.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||

</details>

---

### Object: `BackflipWhenTargeted`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnGainCoins`](./Characters_and_Bosses.md#object-statusongaincoins)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific dodge ability to trigger (e.g., DestroyerDodge). | 7 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 7 ||

</details>

---

### Object: `BattlefieldUniqueRandomPassive`


**Definition:** Map Rule: Grants a unique random passive modifier to the battlefield.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Integer | Applies or references the 'DemonicGlyph_Bite' effect/state. | 1 ||
| `DemonicGlyph_Bounce` | Integer | Applies or references the 'DemonicGlyph_Bounce' effect/state. | 1 ||
| `DemonicGlyph_Fire` | Integer | Applies or references the 'DemonicGlyph_Fire' effect/state. | 1 ||
| `DemonicGlyph_Movement` | Integer | Applies or references the 'DemonicGlyph_Movement' effect/state. | 1 ||
| `DemonicGlyph_Summon` | Integer | Applies or references the 'DemonicGlyph_Summon' effect/state. | 1 ||

</details>

---

### Object: `BellyFull`


**Definition:** Character Form / AI State: Behavior and stats for the \'BellyFull\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `BigHolding`


**Definition:** Character Form / AI State: Behavior and stats for the \'BigHolding\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `BigHoldingCat`


**Definition:** Character Form / AI State: Behavior and stats for the \'BigHoldingCat\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Bully`


**Definition:** Character Form / AI State: Behavior and stats for the 'Bully' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `BungaCheers`


**Definition:** Animation/AI State: Bunga cheering animation logic.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ally_damage`](./Enums.md#enum-ally_damage) | Enum | Specifies the cheering animation to play when an ally takes damage. | 1 ||
| [`ally_dead`](./Enums.md#enum-ally_dead) | Enum | Specifies the cheering animation to play when an ally dies. | 1 ||
| [`enemy_damage`](./Enums.md#enum-enemy_damage) | Enum | Specifies the cheering animation to play when an enemy takes damage. | 1 ||
| [`enemy_dead`](./Enums.md#enum-enemy_dead) | Enum | Specifies the cheering animation to play when an enemy dies. | 1 ||
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum | Specifies the tag used to identify summoned warriors for the Bunga entrance sequence. | 1 ||

</details>

---

### Object: `CaveWomanHasCat`


**Definition:** Character Form: Behavior and stats for the \'CaveWomanHasCat\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `CerberubsAggroTargetBehavior`


**Definition:** AI Logic: Custom aggro targeting rules for Cerberubs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alert_form`](./Enums.md#enum-alert_form) | Enum | Specifies the form to switch to when the Cerberubs unit is alerted. | 1 ||
| [`default_form`](./Enums.md#enum-default_form) | Enum | Specifies the default form for the Cerberubs unit. | 1 ||

</details>

---

### Object: `CerberubsJumpBlind`


**Definition:** AI Logic: Blind jump attack pattern for Cerberubs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 1 ||

</details>

---

### Object: `CerberubsJumpNormal`


**Definition:** AI Logic: Normal jump attack pattern for Cerberubs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 1 ||

</details>

---

### Object: `ChanceToBackflip`


**Definition:** Applies or references the 'ChanceToBackflip' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 6 ||
| `chance` | Number | Probability (0.0 to 1.0) of executing this action. | 6 ||

</details>

---

### Object: `ChanceToFormChangeOnAbilityDamage`


**Definition:** Reaction: Probability to change forms when taking ability damage.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0) of executing this action. | 1 ||
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the form name (e.g., "Big", "Small", "Angry") the unit transforms into. | 1 ||

</details>

---

### Object: `ChaosBossFormChangeGuide`


**Definition:** Boss Logic: Maps the form transition phases for the Chaos Boss.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives_health_threshold` | Integer | The health percentage threshold at which the Chaos boss's passive pieces activate. | 1 ||
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array | The list of active boss piece names that are used in the Chaos boss fight. | 1 ||
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array | The list of passive boss piece names that are used in the Chaos boss fight. | 1 ||

</details>

---

### Object: `ChaosBossPieces`


**Definition:** Boss Logic: Defines the separate destructible pieces of the Chaos Boss.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array | The list of active boss piece names that are used in the Chaos boss fight. | 1 ||
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array | The list of passive boss piece names that are used in the Chaos boss fight. | 1 ||

</details>

---

### Object: `ChaosHeadDropIn`


**Definition:** Boss Logic: Drop-in attack/animation for the Chaos Head.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`new_music`](./Enums.md#enum-new_music) | Enum | Specifies the music track to play when the Chaos head drops in. | 1 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specific entity tag required. | 1 ||

</details>

---

### Object: `Charging`


**Definition:** Character Form / AI State: Behavior when charging an attack.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Close`


**Definition:** AI Movement logic: Maneuvers into close/melee range.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `CloseConvert`


**Definition:** AI State: Logic for converting adjacent units.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `Conditional_BadRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized bad outcome probability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Characters_and_Bosses.md#object-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |
| [`Madness`](./Enums.md) | Integer | Specifies the number of Madness stacks applied, which cause the target to act randomly or attack allies; can be an integer, array `[stacks, probability]`, or a keyword alias. | 1 | 1 |

</details>

---

### Object: `Conditional_HasKnockback`


**Definition:** Conditional: Executes logic if the triggering attack deals knockback.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Characters_and_Bosses.md#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Logic: Applies vertical and horizontal displacement. | 1 ||
| `RemoveKnockback` | `Number` | Applies or references the 'RemoveKnockback' effect/state. | 1 ||
| [`TempPassiveUntilSettled`](#object-temppassiveuntilsettled) | Object | Passive: Active only until the physics engine stops moving the character. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

---

### Object: `Conditional_IsPhysicalAttack`


**Definition:** Conditional: Executes logic if the triggering attack is physical.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#object-addstatustoreceiveddamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Logic: Applies vertical and horizontal displacement. | 1 ||
| `RemoveKnockback` | `Number` | Applies or references the 'RemoveKnockback' effect/state. | 1 ||
| [`TempPassiveUntilSettled`](#object-temppassiveuntilsettled) | Object | Passive: Active only until the physics engine stops moving the character. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

---

### Object: `CounterAttack`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 5 ||
| `without_orienting` | Boolean | If true, the counterattack is performed without reorienting the unit. | 1 ||

</details>

---

### Object: `CreateGlobalModifiers`


**Definition:** Generates global map or encounter rules/modifiers.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| `BloodRain` | `Number` | Applies or references the 'BloodRain' effect/state. | 3 ||
| [`LowerAmbientLight`](Abilities_and_Spells.md#object-lowerambientlight) | Object | Visual: Dims the map lighting. | 3 ||

</details>

---

### Object: `Damaged`


**Definition:** Character Form / AI State: Behavior when health is critically low.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||

</details>

---

### Object: `Default_Ceiling`


**Definition:** Character Form: The baseline behavior state while attached to the ceiling.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `Default_Ground`


**Definition:** Character Form: The baseline behavior state while on the ground.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `DelayedAutoRevive`


**Definition:** Applies or references the 'DelayedAutoRevive' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer | The unit's base health, specified as an absolute integer or a percentage modifier. | 6 ||
| `rounds` | Integer | The number of rounds the unit must wait before reviving. | 6 ||

</details>

---

### Object: `DesireMech`


**Definition:** Character Form: Behavior and stats for the 'DesireMech' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||

</details>

---

### Object: `DiceBehavior`


**Definition:** AI Logic: Custom behavior for Dice enemies.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dice_size` | Integer | The number of sides on the die used by the dice behavior. | 1 ||
| `knockback_damage` | Integer | The amount of damage dealt to the target upon knockback. | 1 ||

</details>

---

### Object: `Die`


**Definition:** Character Form / Logic: Forces the character to die.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `DiesToPiercingAndSpikes`


**Definition:** Vulnerability: Character dies instantly if hit by piercing attacks or spikes.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `deferred` | Boolean | If true, the death is deferred until the end of the current action. | 1 ||

</details>

---

### Object: `DodgeWhenTargeted`


**Definition:** Reaction: Executes a dodge maneuver when targeted.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||

</details>

---

### Object: `Drunker`


**Definition:** Character Form: Behavior and stats for the 'Drunker' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||

</details>

---

### Object: `DualSword`


**Definition:** Character Form: Behavior and stats for the \'DualSword\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| `move_speed_multiplier` | Number | A multiplier for the unit's movement animation speed. Values above 1 increase speed. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `DualSword_Primed`


**Definition:** Character Form: Behavior and stats for the \'DualSword_Primed\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| `move_speed_multiplier` | Number | A multiplier for the unit's movement animation speed. Values above 1 increase speed. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Dumb`


**Definition:** AI Profile: A simplified, less optimal decision-making profile.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `DybbukPossessionFallback`


**Definition:** Logic: Fallback state when a Dybbuk possession fails.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum | Specifies the ability used to exit the possession state. | 1 ||
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the form name (e.g., "Big", "Small", "Angry") the unit transforms into. | 1 ||

</details>

---

### Object: `eat_damage`


**Definition:** Damage dealt when this entity consumes another.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherGrowController`](./Characters_and_Bosses.md#object-mothergrowcontroller)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target, bypassing accuracy and evasion checks. | 1 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 1 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging impact triggers. | 1 ||
| `makes_contact` | `Boolean` | If true, the damage instance is considered a contact hit, which can trigger contact-based statuses like Thorns or BleedThorns. | 1 ||
| `piercing` | `Boolean` | If true, the damage instance ignores armor and damage reduction effects. | 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

---

### Object: `Else`


**Definition:** Fallback object that executes if the preceding `Conditional_` block evaluated to false.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#object-addstatustoreceiveddamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 23 ||
| [`Conditional_HasKnockback`](#object-conditional_hasknockback) | Object | Conditional: Executes logic if the triggering attack deals knockback. | 1 ||
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Logic: Applies vertical and horizontal displacement. | 1 ||

</details>

---

### Object: `exit_animations`


**Definition:** Animations played when leaving a form/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Grappling`](./Characters_and_Bosses.md#object-grappling)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Default`](#object-default) | Enum / Object | Character Form: The baseline default behavior state. | 1 ||

</details>

---

### Object: `Explody`


**Definition:** Character Form: Behavior and stats for the 'Explody' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `FaceAwayLastDamage`


**Definition:** Reaction: Forces the character to face away from the last damage source.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean | If true, this reaction only triggers from damage caused by abilities. | 1 ||
| `override_hit_animation` | Boolean | If true, overrides the default hit animation with a custom one. | 1 ||
| `use_turn_animations` | Boolean | If true, uses the unit's turn animations for the face-last-damage effect. | 1 ||

</details>

---

### Object: `FightPhase`


**Definition:** Boss Logic: Main combat phase.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `FinalBossBeamQueue`


**Definition:** Boss Logic: Attack queue for the final boss beam.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`queue`](./Enums.md#enum-queue) | Enum | Specifies the ability or animation to queue for the beam attack. | 1 ||
| [`release`](./Enums.md#enum-release) | Enum | Specifies the ability or animation to release the queued beams. | 1 ||
| [`transform`](./Enums.md#enum-transform) | Enum | Specifies the ability or animation to transform the boss into another form. | 1 ||

</details>

---

### Object: `FinalBossBecomeTheChild`


**Definition:** Boss Logic: Phase transition for the final boss.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`GlobalSpawnCharacter`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'GlobalSpawnCharacter' effect/state. | 1 ||
| `PlayBackground` | `Number` | Applies or references the 'PlayBackground' effect/state. | 1 ||
| [`SwitchMusic`](Abilities_and_Spells.md#object-switchmusic) | Object | Event Trigger: Changes background music track. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `FinalBossHitCountdownBoris`


**Definition:** Boss Logic: Countdown trigger for Boris.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon` | Integer | The ID of the icon displayed on the countdown overlay. | 1 ||
| `icon_ready` | Integer | The ID of the icon displayed when the countdown is ready. | 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`ForceUseAbility`](#object-forceuseability) | Enum / Object | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 1 | CancerExplode |

</details>

---

### Object: `FinalBossHitCountdownExplosive`


**Definition:** Boss Logic: Countdown trigger for explosives.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon` | Integer | The ID of the icon displayed on the countdown overlay. | 1 ||
| `icon_ready` | Integer | The ID of the icon displayed when the countdown is ready. | 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`ForceUseAbility`](#object-forceuseability) | Enum / Object | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 1 | CancerExplode |

</details>

---

### Object: `FinalBossHitCountdownHoly`


**Definition:** Boss Logic: Countdown trigger for holy attacks.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon` | Integer | The ID of the icon displayed on the countdown overlay. | 1 ||
| `icon_ready` | Integer | The ID of the icon displayed when the countdown is ready. | 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||

</details>

---

### Object: `FinalBossPupils`


**Definition:** Boss Logic: Pupil state management.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `radius` | Array / Integer | Distance or area of effect in tiles. | 1 ||
| [`reset_center_because_no_target_halflife`](./Enums.md#enum-reset_center_because_no_target_halflife) | Number | The halflife in seconds for resetting pupil center when no target exists. | 1 ||
| [`reset_center_because_of_animation_halflife`](./Enums.md#enum-reset_center_because_of_animation_halflife) | Number | The halflife in seconds for resetting pupil center due to animation interruption. | 1 ||
| [`teleport_tracking_halflife`](./Enums.md#enum-teleport_tracking_halflife) | Number | The halflife in seconds for updating pupil tracking after a teleport. | 1 ||
| [`tracking_acquisition_halflife`](./Enums.md#enum-tracking_acquisition_halflife) | Number | The halflife in seconds for acquiring a new tracking target. | 1 ||
| [`look_at_offset`](./Arrays.md#array-look_at_offset) | Array | A 3D vector offset for the look-at target position. | 1 ||
| [`virtual_head_position`](./Arrays.md#array-virtual_head_position) | Array | A 3D vector defining the virtual head position used for pupil calculations. | 1 ||

</details>

---

### Object: `FinalBossShieldHealth`


**Definition:** Boss Logic: Shield health management.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`break_ability`](./Enums.md#enum-break_ability) | Enum | Specifies the ability used to break the shield. | 1 ||
| [`state_health`](./Arrays.md#array-state_health) | Array | An array of health thresholds corresponding to different shield states. | 1 ||

</details>

---

### Object: `FinalBossSyncAnimations`


**Definition:** Boss Logic: Synchronizes multi-part boss animations.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`other_character`](./Enums.md#enum-other_character) | Enum | Specifies the other character to synchronize animations with. | 1 ||
| [`other_form_change_abilities`](#object-other_form_change_abilities) | Object | Lists secondary abilities used to change forms. | 1 ||

</details>

---

### Object: `Flop`


**Definition:** Character Form: Behavior and stats for the \'Flop\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Flop2`


**Definition:** Character Form: Behavior and stats for the \'Flop2\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `FlushBubs`


**Definition:** Character Form: Behavior and stats for the 'FlushBubs' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `FlushHost`


**Definition:** Character Form: Behavior and stats for the 'FlushHost' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `FlushNettle`


**Definition:** Character Form: Behavior and stats for the 'FlushNettle' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `FoodMove`


**Definition:** AI Movement: Logic for seeking out food items.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `ForceTrample`


**Definition:** Logic: Forces movement to act as a trample attack.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 1 ||

</details>

---

### Object: `GainDisorderFromPool`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Characters_and_Bosses.md#object-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Number | Probability (0.0 to 1.0) of executing this action. | 1 ||
| [`pool`](./Enums.md#enum-pool) | Array / Enum | Specifies the loot pool, ability pool, or item category from which an item or effect is selected; can be a specific pool name, table index, or inline array. | 1 ||

</details>

---

### Object: `Grappling`


**Definition:** Character Form / AI State: Behavior while grappling an opponent.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit_animations`](#object-exit_animations) | Object | Animations played when leaving a form/state. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||

</details>

---

### Object: `Grown`


**Definition:** Character Form: Behavior and stats for the \'Grown\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 1 ||
| `weak_threshold` | Integer | The health threshold below which the unit is considered 'weak' for mechanics. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `GuaranteedJackpot`


**Definition:** Loot Logic: Guarantees a high-tier drop.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `Guarding`


**Definition:** Character Form / AI State: Defensive behavior state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `HalfDead`


**Definition:** Character Form: Behavior and stats for the \'HalfDead\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `HasDeadCat`


**Definition:** Character Form: Behavior and stats for the \'HasDeadCat\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `HasRock`


**Definition:** Character Form: Behavior and stats for the \'HasRock\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||

</details>

---

### Object: `Headless`


**Definition:** Character Form: Behavior and stats for the \'Headless\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `HealNeighborsEachTurn`


**Definition:** Passive: Restores health to adjacent allies at the start of the turn.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the Buddy effect only targets allies. | 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||

</details>

---

### Object: `Hint_CrackedVisuals`


**Definition:** Visual: Overlay effects for cracked/damaged terrain or objects.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||

</details>

---

### Object: `Hint_CrackedVisuals2`


**Definition:** Visual: Secondary cracked visual overlay.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||

</details>

---

### Object: `Hint_CrackedVisuals3`


**Definition:** Visual: Tertiary cracked visual overlay.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||

</details>

---

### Object: `HitlerExecute`


**Definition:** Boss Logic: Specific execution or ultimate attack state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specific entity tag required. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`threshold`](./Enums.md) | Enum / Integer | The health threshold value (absolute or equation) at which this ability becomes available. | 1 | 200 |

</details>

---

### Object: `HPAltStates`


**Definition:** Visual: Alternative sprite states based on current health.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`clipname`](./Enums.md#enum-clipname) | Enum | Specifies the animation clip name for the alternate state. | 1 ||
| [`thresholds`](./Arrays.md#array-thresholds) | Array | An array of health percentage thresholds that trigger state changes. | 1 ||

</details>

---

### Object: `HumanDead`


**Definition:** Character Form: Behavior and stats for the \'HumanDead\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||

</details>

---

### Object: `InfiniteRebirth`


**Definition:** Applies the 'InfiniteRebirth' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer | The unit's base health, specified as an absolute integer or a percentage modifier. | 3 ||
| `playercat_health` | Integer | The percentage of maximum health the player cat must have to trigger rebirth. | 3 ||
| `immediate` | Boolean | If true, the forced attack executes immediately without waiting. | 1 ||

</details>

---

### Object: `InitialPhase`


**Definition:** Boss Logic: The starting phase of an encounter.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Insane_Ceiling`


**Definition:** Character Form: Insane behavior state while attached to the ceiling.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Insane_Ground`


**Definition:** Character Form: Insane behavior state while on the ground.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `JohnnyBubs`


**Definition:** Character Form: Behavior and stats for the 'JohnnyBubs' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `JohnnyHost`


**Definition:** Character Form: Behavior and stats for the 'JohnnyHost' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `JohnnyNeedsWashing`


**Definition:** Character Form: Behavior and stats for the 'JohnnyNeedsWashing' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_unwashed`](./Enums.md#enum-form_unwashed) | Enum | Specifies the form when the character is unwashed. | 1 ||
| [`form_washed`](./Enums.md#enum-form_washed) | Enum | Specifies the form when the character is washed. | 1 ||

</details>

---

### Object: `JohnnyNettle`


**Definition:** Character Form: Behavior and stats for the 'JohnnyNettle' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Joystick`


**Definition:** Character Form: Behavior and stats for the \'Joystick\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `LeapClose`


**Definition:** AI Movement: Executes a jumping maneuver to close distance.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `Lifted`


**Definition:** Character Form: Behavior and stats for the \'Lifted\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Lit`


**Definition:** Character Form: Behavior and stats for the 'Lit' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `LowerAmbientLight`


**Definition:** A visual effect that dims the map's lighting.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CreateGlobalModifiers`](./Characters_and_Bosses.md#object-createglobalmodifiers)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `speed` | Array / Number | The transition speed. | 3 ||
| [`amount`](./Arrays.md#array-amount) | Array | The target opacity/dimness level. | 3 ||

</details>

---

### Object: `MegaDinoDropController`


**Definition:** Boss Logic: Manages loot drops for the Mega Dino.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`head_drop`](./Enums.md#enum-head_drop) | Enum | Specifies the ability or animation for the head dropping. | 1 ||
| [`leg_leave`](./Enums.md#enum-leg_leave) | Enum | Specifies the ability or animation for legs leaving the body. | 1 ||
| [`leg_return`](./Enums.md#enum-leg_return) | Enum | Specifies the ability or animation for legs returning to the body. | 1 ||
| `stable_legs` | Integer | The number of legs required to remain stable before the head drops. | 1 ||

</details>

---

### Object: `ModularPickup`


**Definition:** Pickup Logic: Defines what happens when a modular item is collected.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`sound_event`](./Enums.md#enum-sound_event) | Enum | Specifies the sound event played on pickup. | 1 ||
| [`Cleanse`](./Enums.md) | Integer | If set to 1, removes all status effects from the target; if 0, no cleanse. | 1 | 0 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `MonkCatReactionAbilities`


**Definition:** Reaction: Specific counter-attack or dodge abilities used by the Monk class.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`spell`](./Enums.md#enum-spell) | Enum | Specifies the spell ability granted by this reaction. | 1 ||
| [`trinket`](./Enums.md#enum-trinket) | Enum | Specifies the trinket item associated with this ability. | 1 ||
| [`weapon`](./Enums.md#enum-weapon) | Enum | Weapon item constraint. | 1 ||

</details>

---

### Object: `MotherGrowController`


**Definition:** Boss Logic: Manages the growth phases of the Mother boss.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eat_damage`](#object-eat_damage) | Object | Damage dealt when this entity consumes another. | 1 ||
| [`tumor_object`](./Enums.md#enum-tumor_object) | Enum | Specifies the parent tumor object that controls growth. | 1 ||

</details>

---

### Object: `MotherTumorPassive`


**Definition:** Boss Logic: Passive effects applied to the Mother's tumors.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](#object-cat) | Object | Character Form: Base form for standard cats. | 1 ||
| [`grow_ability`](./Enums.md#enum-grow_ability) | Enum | Specifies the ability used to grow the tumor. | 1 ||
| [`NonCat`](#object-noncat) | Object | Character Form: Behavior and stats for the 'NonCat' state. | 1 ||
| [`pass_ani`](./Enums.md#enum-pass_ani) | Enum | Specifies the animation played when passing the tumor. | 1 ||
| [`receive_ani`](./Enums.md#enum-receive_ani) | Enum | Specifies the animation played when receiving the tumor. | 1 ||
| [`considered_forms`](./Arrays.md#array-considered_forms) | Array | An array of form names considered for growth decisions. | 1 ||

</details>

---

### Object: `Mount`


**Definition:** Character Form: Behavior and stats for the 'Mount' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eject_ability`](./Enums.md#enum-eject_ability) | Enum | Specifies the ability used to eject the rider from the mount. | 1 ||
| [`enter_ability`](./Enums.md#enum-enter_ability) | Enum | Specifies the ability used to enter the mount. | 1 ||

</details>

---

### Object: `Mounted`


**Definition:** Character Form: Behavior and stats for the \'Mounted\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||

</details>

---

### Object: `MouthFull`


**Definition:** Character Form: Behavior and stats for the \'MouthFull\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `MoveAfterAnyAttemptedAttack`


**Definition:** AI Movement: Forces a move action immediately after attacking, even if it missed.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Array / Enum | An array of three weighting values or a named preset for Crazy Eye background behavior weights. | 1 ||

</details>

---

### Object: `MoveAwayFromDamageSource`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the ability used to move when damaged. | 1 ||

</details>

---

### Object: `MoveAwayWhenEnemyAdjacent`


**Definition:** AI Movement: Moves away if an enemy enters an adjacent tile.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the ability used to move when damaged. | 1 ||
| `once_per_turn` | Boolean | If true, this movement reaction can only trigger once per turn. | 1 ||
| [`weights`](./Enums.md#enum-weights) | Array / Enum | An array of three weighting values or a named preset for Crazy Eye background behavior weights. | 1 ||

</details>

---

### Object: `MoveForBarrage`


**Definition:** AI Movement: Repositions to optimize a barrage attack.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Determines which animation or movement ability is used to close distance. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `MoveForDash`


**Definition:** AI Movement: Repositions to set up a dash attack line.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Determines which animation or movement ability is used to close distance. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `MoveForGrass`


**Definition:** AI Movement: Moves toward grass tiles.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Determines which animation or movement ability is used to close distance. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `MoveForPounce`


**Definition:** AI Movement: Repositions to optimize a pounce trajectory.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Determines which animation or movement ability is used to close distance. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `MoveForSpin`


**Definition:** AI Movement: Repositions into a cluster of enemies for a spin attack.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Determines which animation or movement ability is used to close distance. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `MoveOneForPuke`


**Definition:** AI Movement: Specific positioning logic for puke attacks.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Determines which animation or movement ability is used to close distance. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `MoveSpaced`


**Definition:** AI Movement: Moves to maintain a specific distance from targets.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `MoveToHead`


**Definition:** AI Movement: Navigates toward the 'head' or primary target.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Determines which animation or movement ability is used to close distance. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `MoveTowards`


**Definition:** AI Movement: Moves toward the nearest target.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Determines which animation or movement ability is used to close distance. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `MultiSpawnOnDeath`


**Definition:** Event Trigger: Spawns multiple entities upon death.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`obj`](./Enums.md#enum-obj) | Array / Enum | The object(s) spawned when this passive triggers. | 1 ||
| [`count`](./Arrays.md#array-count) | Array / Integer | The numerical quantity. | 1 ||

</details>

---

### Object: `NCGravecrawlFAR`


**Definition:** AI Movement: Specific grapple/crawl logic.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `NoEyes`


**Definition:** Character Form: Behavior and stats for the \'NoEyes\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||

</details>

---

### Object: `NormalFull`


**Definition:** Character Form: Behavior and stats for the 'NormalFull' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `NoStick`


**Definition:** Character Form: Behavior and stats for the 'NoStick' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||

</details>

---

### Object: `Nothing`


**Definition:** Character Form: Behavior and stats for the 'Nothing' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#object-mothertumorspawnincapture)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation clip to use for the ability’s meta representation. | 1 ||

</details>

---

### Object: `Obey`


**Definition:** AI State: Enforced compliance logic (e.g., when Charmed).  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Off`


**Definition:** Character Form: Behavior and stats for the 'Off' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||

</details>

---

### Object: `OffScreen`


**Definition:** Character Form: Behavior and stats for the 'OffScreen' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `OneEye`


**Definition:** Character Form: Behavior and stats for the \'OneEye\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Open`


**Definition:** Character Form: Behavior and stats for the 'Open' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `OpenCat`


**Definition:** Character Form: Behavior and stats for the 'OpenCat' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `other_form_change_abilities`


**Definition:** Lists secondary abilities used to change forms.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossSyncAnimations`](./Characters_and_Bosses.md#object-finalbosssyncanimations)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Boris`](#object-boris) | Enum / Object | Character Form / AI State: Behavior and stats for the 'Boris' state. | 1 ||
| [`Explosive`](#object-explosive) | Enum / Object | Character Form: Behavior and stats for the 'Explosive' state. | 1 ||
| [`Holy`](#object-holy) | Enum / Object | Character Form: Behavior and stats for the 'Holy' state. | 1 ||

</details>

---

### Object: `Out`


**Definition:** Character Form: Behavior and stats for the 'Out' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `PassiveWhenAffectedByElement`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 18 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 18 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 18 ||

</details>

---

### Object: `PassiveWhenDead`


**Definition:** State Trigger: Grants passives when this condition is met.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `Possessing`


**Definition:** Character Form: Behavior and stats for the \'Possessing\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Primed`


**Definition:** Character Form: Behavior and stats for the 'Primed' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Pulp2`


**Definition:** Character Form: Behavior and stats for the 'Pulp2' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Pulp3`


**Definition:** Character Form: Behavior and stats for the 'Pulp3' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Pulp4`


**Definition:** Character Form: Behavior and stats for the 'Pulp4' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Pulp5`


**Definition:** Character Form: Behavior and stats for the 'Pulp5' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Pulp6`


**Definition:** Character Form: Behavior and stats for the 'Pulp6' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Pulp7`


**Definition:** Character Form: Behavior and stats for the 'Pulp7' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| `uifloaters_offset` | Number | The vertical offset in pixels for UI floaters displayed above the unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `RandomStatusFromPool`


**Definition:** Selects and applies a random status effect from the provided nested object.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ally_rewards`](./Characters_and_Bosses.md#object-ally_rewards)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 33 ||
| [`StatusGroup`](Abilities_and_Spells.md#object-statusgroup) | Object | A collection of status effects applied together as a group, each with its own stack count. | 3 ||

</details>

---

### Object: `ReturnA`


**Definition:** Boss Logic: Specific phase return trigger.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `RevengeDamage`


**Definition:** Reaction trigger: Deals damage to the attacker when hit.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 8 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 5 ||
| `knockback` | Enum / Integer | The number of tiles to push the target away from the attacker; can be negative to pull the target closer, or 'str' to scale with the attacker's strength stat. | 3 ||

</details>

---

### Object: `round_start_bonusturn_pattern`


**Definition:** AI Logic: Ability usage pattern during round-start bonus turns.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_priority`](./Arrays.md#array-do_priority) | Array | A list of actions executed in order of priority, stopping when one succeeds. | 1 ||

</details>

---


<details>
<summary><b>AddStatusToReceivedDamage</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>AddStatusToSpells</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>AddStatusToTrampleDamage</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>PassiveWhenDead</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>StatusOnEnemyConfused</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>StatusOnSpawnIn</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

### Object: `RunFar`


**Definition:** AI Movement: Maximize distance from targets.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `RunWhenLastPlayerCatIsCharmed`


**Definition:** AI Logic: Flee logic when the player team is entirely crowd-controlled.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean | If true, allows this passive to make decisions during the middle of a turn. | 1 ||
| [`legacy_savekey`](./Enums.md#enum-legacy_savekey) | Enum | Specifies the legacy save key for recovering stolen cats. | 1 ||

</details>

---

### Object: `ScalingAttackAnimation`


**Definition:** Visual: Animation scales based on damage output.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`default`](#object-default) | Enum / Object | Baseline configuration. | 1 ||
| [`thresholds`](./Arrays.md#array-thresholds) | Array | An array of health percentage thresholds that trigger state changes. | 1 ||

</details>

---

### Object: `SharePickups`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_coins` | Boolean | If true, includes coins in shared pickups. | 1 ||

</details>

---

### Object: `Sitting`


**Definition:** Character Form: Behavior and stats for the 'Sitting' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `SkipFirstRounds`


**Definition:** AI Logic: Passes turn for the first X rounds of combat.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pop_chance` | Integer | The percentage chance that the first round skip will trigger. | 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||

</details>

---

### Object: `SmallHolding`


**Definition:** Character Form: Behavior and stats for the \'SmallHolding\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `SmallHoldingCat`


**Definition:** Character Form: Behavior and stats for the \'SmallHoldingCat\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `SpawningPhase`


**Definition:** Boss Logic: Phase focused on summoning minions.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `SpewerAltGraphics`


**Definition:** Visual: Alternative graphics for Spewer enemies.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Fire`](#object-fire) | Integer / Object | Character Form: Behavior and stats for the 'Fire' state. | 1 ||
| [`FireFull`](#object-firefull) | Integer / Object | Character Form: Behavior and stats for the 'FireFull' state. | 1 ||
| [`Normal`](#object-normal) | Integer / Object | Character Form: Behavior and stats for the 'Normal' state. | 1 ||
| [`NormalFull`](#object-normalfull) | Integer / Object | Character Form: Behavior and stats for the 'NormalFull' state. | 1 ||
| [`Tar`](#object-tar) | Integer / Object | Character Form: Behavior and stats for the 'Tar' state. | 1 ||
| [`TarFull`](#object-tarfull) | Integer / Object | Character Form: Behavior and stats for the 'TarFull' state. | 1 ||

</details>

---

### Object: `StacyMutant_Brace`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Brace' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Brace`](./Enums.md) | Integer | The amount of flat damage reduction applied to the source. | 1 | 99 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Specifies which cat body part IDs to transform into upon applying the effect. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Counter`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Counter' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | An object defining status effects to apply on basic attacks, with optional conditions. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Specifies which cat body part IDs to transform into upon applying the effect. | 1 ||
| [`CounterAttack`](Cat_Mutations.md#object-counterattack) | Array / Enum / Object | Specifies the ability name used for counterattacking when hit. | 1 | [GSScream] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Damage`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Damage' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`AddDamage`](./Enums.md) | Integer | Adds a flat amount to the unit's damage output (can be negative). | 1 | 2 |
| [`AddMaxHealth`](./Enums.md) | Integer | The amount to add to the unit's maximum health. Negative values reduce max health. | 1 | -25 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Specifies which cat body part IDs to transform into upon applying the effect. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_DoubleHead`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_DoubleHead' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Specifies which cat body part IDs to transform into upon applying the effect. | 1 ||
| [`ExtraDispersedTurns`](./Enums.md) | Integer | Additional turns granted, distributed across the turn order. | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Fire`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Fire' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Specifies which cat body part IDs to transform into upon applying the effect. | 1 ||
| [`ElementImmune`](./Enums.md) | Enum | Specifies an element (e.g., Fire, Ice) the unit is immune to. | 1 | Ice |
| [`ReplaceBasicAttack`](./Enums.md) | Enum | Specifies the name of the ability that replaces the unit's basic attack. | 1 | BasicStraightShot |
| [`ReplaceBrain`](#object-replacebrain) | Object | Specifies a brain override object to replace the default AI. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Health`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Health' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`AddMaxHealth`](./Enums.md) | Integer | The amount to add to the unit's maximum health. Negative values reduce max health. | 1 | -25 |
| [`AddSpeed`](./Enums.md) | Integer | The amount of speed added (or subtracted) to the unit. | 1 | 6 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Specifies which cat body part IDs to transform into upon applying the effect. | 1 ||
| [`SizeScale`](./Enums.md) | Number | A multiplier for the unit's visual size. Values above 1 increase size, values below 1 decrease size. | 1 | .8 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Holy`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Holy' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Specifies which cat body part IDs to transform into upon applying the effect. | 1 ||
| [`DivineShield`](./Enums.md) | Integer | The number of charges of Divine Shield applied, which blocks the next instances of damage entirely; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Ice`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Ice' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`AddMovement`](./Enums.md) | Integer | The number of extra movement tiles the unit gains per turn. | 1 | 2 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Specifies which cat body part IDs to transform into upon applying the effect. | 1 ||
| [`ElementImmune`](./Enums.md) | Enum | Specifies an element (e.g., Fire, Ice) the unit is immune to. | 1 | Ice |
| [`ReplaceBasicAttack`](./Enums.md) | Enum | Specifies the name of the ability that replaces the unit's basic attack. | 1 | BasicStraightShot |
| [`ReplaceBrain`](#object-replacebrain) | Object | Specifies a brain override object to replace the default AI. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Lightning`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Lightning' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Specifies which cat body part IDs to transform into upon applying the effect. | 1 ||
| [`ElementImmune`](./Enums.md) | Enum | Specifies an element (e.g., Fire, Ice) the unit is immune to. | 1 | Ice |
| [`ReplaceBasicAttack`](./Enums.md) | Enum | Specifies the name of the ability that replaces the unit's basic attack. | 1 | BasicStraightShot |
| [`ReplaceBrain`](#object-replacebrain) | Object | Specifies a brain override object to replace the default AI. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Mirror`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Mirror' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Specifies which cat body part IDs to transform into upon applying the effect. | 1 ||
| [`ReflectProjectiles`](#object-reflectprojectiles) | Integer / Object | The percentage chance to reflect projectiles back at the attacker. | 1 | 100 |
| [`StatusEachTurnEndForEachTurn`](#object-statuseachturnendforeachturn) | Object | Specifies an object defining status effects applied at end of each turn for each turn. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Speed`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Speed' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`AddDamage`](./Enums.md) | Integer | Adds a flat amount to the unit's damage output (can be negative). | 1 | 2 |
| [`AddSpeed`](./Enums.md) | Integer | The amount of speed added (or subtracted) to the unit. | 1 | 6 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Specifies which cat body part IDs to transform into upon applying the effect. | 1 ||
| [`SizeScale`](./Enums.md) | Number | A multiplier for the unit's visual size. Values above 1 increase size, values below 1 decrease size. | 1 | .8 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Thorns`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Thorns' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Specifies which cat body part IDs to transform into upon applying the effect. | 1 ||
| [`Thorns`](./Enums.md) | Integer | The number of Thorns stacks applied, which deals damage back to melee attackers. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `Standing`


**Definition:** Character Form: Behavior and stats for the 'Standing' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Standing2`


**Definition:** Character Form: Behavior and stats for the 'Standing2' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Start_Ceiling`


**Definition:** Character Form: Behavior and stats for the 'Start_Ceiling' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `StatusAfterXTurns`


**Definition:** Event Trigger: Applies a status effect after X turns have passed.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`ForceUseAbility`](#object-forceuseability) | Enum / Object | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 2 | CancerExplode |

</details>

---

### Object: `StatusEachTurnBeginIfHasStatus`


**Definition:** Event Trigger: Applies a status at the start of the turn if a prerequisite status is met.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation clip to use for the ability’s meta representation. | 1 ||
| `consume` | Boolean | If true, the status is consumed upon applying the effect. | 1 ||
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`AllStatsUp`](./Enums.md) | Integer | The amount (or array with duration and chance) of all stats increased (or decreased). | 1 | 2 |
| [`DamageUp`](./Enums.md) | Integer | The amount of damage increase, or a string formula for dynamic calculation. | 1 | 2 |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 1 | 5 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `StatusEachTurnEndForEachTurn`


**Definition:** Event Trigger: Applies nested statuses to each turn end for each turn.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StacyMutant_Mirror`](./Characters_and_Bosses.md#object-stacymutant_mirror)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, each dealing independent damage; can also be an object with custom tooltip data. | 3 | 1 |

</details>

---

### Object: `StatusEachTurnEndIfEnabledAtStartOfTurn`


**Definition:** Event Trigger: Applies a status at the end of the turn if an enabling condition was met at the start.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`ForceUseAbility`](#object-forceuseability) | Enum / Object | Determines which ability the target is forced to cast immediately, ignoring normal costs and cooldowns. | 1 | CancerExplode |

</details>

---

### Object: `StatusOnDie`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 ||
| [`RemoveAmbientLightEffects`](./Enums.md) | Integer | The duration or amount of ambient light effect removal applied over time. | 1 | 4 |
| [`RemoveGlobalModifiers`](./Enums.md) | Array | An array of global modifier names to remove on death. | 1 | [BloodRain] |

</details>

---

### Object: `StatusOnEndMove`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnEnemyConfused`


**Definition:** Event Trigger: Applies statuses when an enemy becomes confused.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnGainCoins`


**Definition:** Event Trigger: Applies nested statuses when gain coins.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Object | The number of stacks of BackflipWhenTargeted or an object defining the dodge ability; causes the unit to perform a backflip dodge when targeted. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StatusOverlappingCharactersAndDie`


**Definition:** Event Trigger: Applies statuses to overlapping entities, then destroys self.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Poison`](./Enums.md) | Integer | The number of Poison stacks applied, which deals poison damage over time; an array `[stacks, probability]` can be used to specify the number of stacks and the chance of application. | 1 | 2 |

</details>

---

### Object: `StatusWhenStatusCompletelyRemoved`


**Definition:** Event Trigger: Applies statuses when a tracked status effect is fully cleansed.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | Specifies the ability name the unit will use at the end of each round. | 1 | KirbySpit |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `Stop`


**Definition:** AI Movement: Forces the character to cease movement.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `SuckMF`


**Definition:** Character Form: Behavior and stats for the 'SuckMF' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `SupportDieInsteadOfRun`


**Definition:** AI Logic: Forces a support unit to die rather than flee.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_dead_ani`](./Enums.md#enum-alt_dead_ani) | Enum | Specifies an alternative animation clip used when dead instead of default run. | 1 ||
| [`alt_dying_ani`](./Enums.md#enum-alt_dying_ani) | Enum | Specifies an alternative animation clip used when dying instead of default run. | 1 ||

</details>

---

### Object: `SwimmingFormChange`


**Definition:** Logic: Automates form change when entering/exiting water.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_in`](./Enums.md#enum-form_in) | Enum | Specifies the form used when entering water. | 1 ||
| [`form_out`](./Enums.md#enum-form_out) | Enum | Specifies the form used when exiting water. | 1 ||

</details>

---

### Object: `SwitchMusic`


**Definition:** Changes the background music track or layer during combat.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossBecomeTheChild`](./Characters_and_Bosses.md#object-finalbossbecomethechild)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | The specific audio layer to transition to (e.g., map, battle). | 7 ||
| [`new_song`](./Enums.md#enum-new_song) | Enum | The ID of the new music track. | 6 ||

</details>

---

### Object: `SwordAndShield`


**Definition:** Character Form: Behavior and stats for the 'SwordAndShield' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `SwordAndShield_Primed`


**Definition:** Character Form: Behavior and stats for the \'SwordAndShield_Primed\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `SyncFormsWithBuddy`


**Definition:** Logic: Forces this character's form to match their familiar/buddy.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`no_buddy`](./Enums.md#enum-no_buddy) | Enum | Specifies the named form (e.g., Rage) used when syncing forms without a buddy. | 1 ||

</details>

---

### Object: `T3HitlerSpawningPhase`


**Definition:** Boss Logic: Minion spawn phase for the T3 Hitler boss.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spell_use_groups`](./Arrays.md#array-spell_use_groups) | Array | An array defining the groups of spells available during the spawning phase. | 1 ||

</details>

---

### Object: `Tar`


**Definition:** Character Form: Behavior and stats for the 'Tar' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `TarFull`


**Definition:** Character Form: Behavior and stats for the 'TarFull' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Terminator2Run`


**Definition:** AI Movement: Specific run logic for Terminator2.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the ability used to move when damaged. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `TerminatorChase`


**Definition:** AI Movement: Specific chase logic for Terminator.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Determines which movement ability the unit uses. | 1 ||

</details>

---

### Object: `TerminatorSkin`


**Definition:** Visual: Skin definition for Terminator.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 ||
| [`groups`](./Arrays.md#array-groups) | Array | Determines which skin groups are applied to the unit. | 1 ||

</details>

---

### Object: `TF_TargetAllies`


**Definition:** AI Targeting: Prioritizes allies.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 1 ||

</details>

---

### Object: `TF_TargetEnemies`


**Definition:** AI Targeting: Prioritizes enemies.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the preset decision weight set (e.g., careless, zombie) for the AI. | 1 ||

</details>

---

### Object: `Throb`


**Definition:** Character Form: Behavior and stats for the 'Throb' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||

</details>

---

### Object: `ThrobBubs`


**Definition:** Character Form: Behavior and stats for the 'ThrobBubs' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `ThrobHost`


**Definition:** Character Form: Behavior and stats for the 'ThrobHost' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `ThrobNettle`


**Definition:** Character Form: Behavior and stats for the 'ThrobNettle' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Transformed`


**Definition:** Character Form: Behavior and stats for the 'Transformed' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `TransformOnStatusThreshold`


**Definition:** Logic: Changes form when a status effect reaches a certain stack count.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the template identifier of the entity to spawn, referencing a predefined character or object in the game data. | 1 ||
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`threshold`](./Enums.md) | Enum / Integer | The health threshold value (absolute or equation) at which this ability becomes available. | 1 | 200 |

</details>

---

### Object: `TVBotScreen`


**Definition:** Visual: TV Bot screen state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Die` | `Number` | Character Form / Logic: Forces the character to die. | 1 ||
| [`Dumb`](#object-dumb) | Integer / Object | AI Profile: A simplified, less optimal decision-making profile. | 1 ||
| `Fuck` | Integer | Applies or references the 'Fuck' effect/state. | 1 ||
| [`Obey`](#object-obey) | Integer / Object | AI State: Enforced compliance logic (e.g., when Charmed). | 1 ||
| `Shit` | Integer | Applies or references the 'Shit' effect/state. | 1 ||
| [`Stop`](#object-stop) | Integer / Object | AI Movement: Forces the character to cease movement. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `TwisterFling`


**Definition:** Logic: Fling behavior for tornado attacks.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 1 ||
| `max_dist` | Integer | The maximum distance (in tiles) the target can be flung. | 1 ||
| `min_dist` | Integer | The minimum distance (in tiles) the target must be flung. | 1 ||

</details>

---

### Object: `TwoEyes`


**Definition:** Character Form: Behavior and stats for the 'TwoEyes' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `Unflip`


**Definition:** Logic: Reverses a flipped state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Determines which animation or movement ability is used to close distance. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Specifies the movement behavior pattern used by the AI, such as 'semi_blind' or 'prefer_tall_grass_always_move'. | 1 ||

</details>

---

### Object: `UnlimitedDeathRattleRevive`


**Definition:** Logic: Endless resurrection on death.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| `even_if_stunned` | Boolean | If true, the reaction triggers even if the unit is stunned. | 1 ||

</details>

---

### Object: `Unlit`


**Definition:** Character Form: Behavior and stats for the 'Unlit' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Unwashed`


**Definition:** Character Form: Behavior and stats for the 'Unwashed' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||

</details>

---

### Object: `UseAbility`


**Definition:** Forces the character or target to instantly use a specified ability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusWhenStatusCompletelyRemoved`](./Characters_and_Bosses.md#object-statuswhenstatuscompletelyremoved)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger. | 2 ||
| `respect_prime` | Boolean | If true, respects the ability's prime/cooldown state. | 2 ||

</details>

---

### Object: `UseAbilityWhenOutOfStatus`


**Definition:** Logic: Casts a specific ability the moment a status effect expires.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 ||

</details>

---

### Object: `Washed`


**Definition:** Character Form: Behavior and stats for the 'Washed' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `Washer`


**Definition:** Character Form: Behavior and stats for the \'Washer\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | A string or number appended to a partial animation name to identify the variant. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---

### Object: `ZealotBomb`


**Definition:** Character Form: Behavior and stats for the \'ZealotBomb\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | A string or number appended to the base animation name to identify the specific animation variant. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the name of the ability used as the basic attack for this unit. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | Specifies the localization key for the tooltip displayed when hovering over the character or object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Defines passive abilities granted when the parent condition is active. | 1 ||

</details>

---


---

## Auto-Discovered Objects


### Object: `BoneWormShotSmall`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>
