# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see AUDIT_GAPS.md. For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Characters & Bosses

> **Associated Files:** `data/characters/`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 600

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1571 | passives<br>class<br>	ag |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 2609 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 2344 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1910 | `{ . . . }` |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. | 1195 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 600 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 461 | `{ . . . }` |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 460 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 459 | `{ . . . }` |
| [`sound`](./Miscellaneous.md#object-sound) | Object  | A container object defining audio configurations, including alternate sound lists. | 62 | `{ . . . }` |
| `distance_to_ally` | Float | The preferred distance (in tiles) to maintain from allies; negative values or 0 disable the preference. | 55 | `-.1`<br>`-1`<br>`0` |
| `distance_to_character` | Integer | The preferred distance (in tiles) to maintain from any character; negative values or 0 disable the preference. | 55 | `-1`<br>`0`<br>`1` |
| `distance_to_enemy` | Float | The preferred distance (in tiles) to maintain from enemies; negative values or 0 disable the preference. | 55 | `-.01`<br>`-.5`<br>`-1` |
| `face_closest_enemy` | Integer | If nonzero, the character will face the closest enemy. | 55 | `0`<br>`1` |
| [`preferred_distance`](./Enums.md#enum-preferred_distance) | Enum / Integer  | The ideal distance to maintain from a target, expressed either as an absolute tile count or relative to movement (e.g., `mov+2`) or reach (`mov+reach`). | 55 | `0`<br>`1`<br>`2` |
| `total_distance_moved` | Float | The total distance the character has moved, used in movement weight calculations. | 55 | `-0.001`<br>`-0.01`<br>`-1` |
| [`equipment`](./Miscellaneous.md#object-equipment) | Object  | A container object defining the character's equipped items (head, face, neck, weapon, etc.). | 44 | `{ . . . }` |
| `accurate_knockback` | Boolean | If true, knockback from attacks is applied accurately (e.g., straight line); if false, knockback may be erratic. | 32 | `false` |
| `buff_ally` | Integer | The number of buffs applied to ally units. | 32 | `0`<br>`1`<br>`10` |
| `buff_enemy` | Integer | The number of buffs applied to enemy units. Negative values may apply debuffs. | 32 | `-1`<br>`-100`<br>`0` |
| `buff_self` | Integer | The number of buffs applied to the unit itself. Negative values may apply debuffs. | 32 | `-1`<br>`0` |
| `consider_overkill` | Boolean | If true, the AI considers overkill damage when evaluating actions. | 32 | `false`<br>`true` |
| `consider_secondary_damage` | Boolean | If true, the AI considers secondary damage (e.g., splash) when evaluating actions. | 32 | `false`<br>`true` |
| `consider_total_damage` | Boolean | If true, the AI considers total damage output (including secondary) when evaluating actions. | 32 | `false`<br>`true` |
| `damage_ally` | Float | A multiplier for damage dealt to ally units. Negative values reduce damage. | 32 | `-1`<br>`-100`<br>`.5` |
| `damage_ally_corpse` | Integer | The amount of damage dealt to ally corpses. | 32 | `0`<br>`1`<br>`100` |
| `damage_enemy` | Integer | The amount of damage dealt to enemy units. | 32 | `0`<br>`1`<br>`100` |
| `damage_enemy_corpse` | Float | A multiplier for damage dealt to enemy corpses. | 32 | `.1`<br>`0`<br>`0.1` |
| `damage_self` | Float | A multiplier for damage dealt to the unit itself. | 32 | `-0.1`<br>`-1`<br>`-1.1` |
| `debuff_ally` | Float | A multiplier for debuffs applied to ally units. | 32 | `-1`<br>`-100`<br>`.5` |
| `debuff_enemy` | Integer | The number of debuffs applied to enemy units. | 32 | `0`<br>`1`<br>`100` |
| `debuff_self` | Float | A multiplier for debuffs applied to the unit itself. | 32 | `-0.1`<br>`-1`<br>`-1.1` |
| `heal_ally` | Integer | The amount of health restored to ally units. | 32 | `0`<br>`1`<br>`10` |
| `heal_enemy` | Integer | The amount of health restored to enemy units. Negative values deal damage. | 32 | `-1`<br>`-100`<br>`0` |
| `heal_self` | Integer | The amount of health restored to the unit itself. Negative values deal damage. | 32 | `-1`<br>`-100`<br>`0` |
| `kill_ally` | Integer | The chance (percentage) to instantly kill an ally unit. | 32 | `0`<br>`40` |
| `kill_enemy` | Float | The chance (percentage or probability) to instantly kill an enemy unit. | 32 | `.2`<br>`0`<br>`100` |
| `negative_weight_scale` | Float | A multiplier applied to the weight of negative (penalty) decisions in AI calculations. | 32 | `.99` |
| `revive_ally_corpse` | Integer | The chance (percentage) to revive an ally corpse. | 32 | `0`<br>`1`<br>`10` |
| `revive_enemy_corpse` | Integer | The chance (percentage) to revive an enemy corpse. Negative values may cause destruction. | 32 | `-1`<br>`-100`<br>`0` |
| `spawn_object` | Integer | If non-zero, enables spawning of an object. The value may specify the number of objects. | 32 | `0`<br>`1` |
| `spawn_object_distance_to_ally` | Float | The distance offset from ally units for spawned objects. Negative values move closer. | 32 | `-.0001`<br>`-.01`<br>`.0001` |
| `spawn_object_distance_to_enemy` | Float | The distance offset from enemy units for spawned objects. | 32 | `-.01`<br>`0`<br>`1` |
| `spend_mana_scale` | Float | A multiplier applied to mana cost when making decisions. | 32 | `.99` |
| [`alt_spawn_pool`](./Miscellaneous.md#object-alt_spawn_pool) | Object  | An alternative spawn pool defining possible objects to spawn with their weights. | 18 | `{ . . . }` |
| [`brain`](./Enums.md#enum-brain) | Enum | Specifies the AI brain type used for decision-making logic. | 5 | `DicerBrain`<br>`GenericBrain`<br>`MountBrain` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 5 | `always_cast`<br>`always_cast_careless`<br>`angry` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 5 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| `scale` | Float | The scale multiplier applied to the unit's visual size. | 5 | `.5`<br>`.6`<br>`.7` |
| `flat_cast_bonus` | Integer | A flat bonus added to the AI's cast chance evaluation. | 5 | `99999` |
| `randomness` | Integer | The amount of randomness added to AI decision-making to avoid predictability. | 5 | `4`<br>`50`<br>`6` |
| `cap_distance_to_ally` | Integer | The maximum distance the AI will maintain from ally units. | 4 | `2`<br>`4`<br>`7` |
| [`pattern`](./Miscellaneous.md#object-pattern) | Object  | Defines a sequence of actions the AI will execute in order, with optional priority or all-in-one. | 3 | `{ . . . }` |
| `consider_aoe` | Boolean | If true, the AI considers area-of-effect damage when evaluating actions. | 3 | `false`<br>`true` |
| `danger_avoidance` | Float | A weight multiplier for the AI's tendency to avoid dangerous positions. | 3 | `.1`<br>`1000`<br>`20` |
| `distance_to_aggro_target` | Integer | The preferred distance the AI tries to maintain from its aggro target. Negative values indicate behind. | 3 | `-1`<br>`-10` |
| `distance_to_corpse` | Float | The preferred distance the AI tries to maintain from corpses. Negative values indicate moving towards. | 3 | `-.1`<br>`-100`<br>`0` |
| `simple` | Boolean | If true, the AI uses simplified decision-making logic. | 3 | `true` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| `end_turn_on_formswitch` | Boolean | If true, the unit's turn ends immediately after switching forms. | 2 | `false`<br>`true` |
| `cap_distance_to_enemy` | Integer | The maximum distance the AI will maintain from enemy units. | 2 | `2`<br>`5` |
| `distance_to_water` | Float | The preferred distance the AI tries to maintain from water tiles. Negative values indicate moving towards. | 2 | `-.0001`<br>`-1` |
| `face_aggro_target` | Integer | A weight multiplier for the AI's tendency to face its aggro target. | 2 | `1`<br>`10` |
| `spawn_object_preferred_distance` | Integer | The preferred distance from the unit at which objects are spawned. | 2 | `4`<br>`5` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`ai_if_spawned_as_enemy`](./Miscellaneous.md#object-ai_if_spawned_as_enemy) | Object  | Overrides the unit's AI settings when it is spawned as an enemy rather than an ally. | 1 | `{ . . . }` |
| `consider_spells` | Boolean | If true, the AI considers using spells in its decision-making. | 1 | `false` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| `cap_distance_to_character` | Integer | The maximum distance the AI will maintain from any character (ally or enemy). | 1 | `2` |
| `cap_total_distance_moved` | Integer | The maximum number of tiles a unit can move before its movement is capped. | 1 | `1` |
| `consider_aggro_target_enemy` | Boolean | If true, the AI considers the aggro target when determining movement or attack behavior. | 1 | `true` |
| `count_nomove_in_eval` | Boolean | If true, the evaluation of a move includes the option of not moving. | 1 | `false` |
| `distance_to_center` | Integer | The distance in tiles from the current position to the map center for AI evaluation. | 1 | `-1` |
| [`exclude_characters_tagged`](./Enums.md#enum-exclude_characters_tagged) | Enum  | Specifies a tag; characters with this tag are excluded from AI behavior targeting. | 1 | `siren` |
| `face_camera` | Integer | If true, the spawned unit always faces the camera. | 1 | `1000`<br>`true` |
| `lava` | Integer | A weight or priority value for preferring lava tiles in AI movement decisions. | 1 | `5` |
| `tall_grass` | Integer | A weight or priority value for preferring tall grass tiles in AI movement decisions. | 1 | `5` |

</details>


---


### Object: `graphics`


**Definition:** An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects.
**Total Count:** 2609

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 517 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 461 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 409 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `shadow_size` | Float | A multiplier for the size of the object's shadow relative to its default. | 151 | `.20`<br>`.25`<br>`.4` |
| `scale` | Float | The scale multiplier applied to the unit's visual size. | 149 | `.5`<br>`.6`<br>`.7` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 149 | `.5`<br>`1`<br>`1.3` |
| [`custom_cat_data`](./Enums.md#enum-custom_cat_data) | Enum | Specifies a dataset or customization profile for cat graphics or behavior. | 127 | `AlbinoTomTom`<br>`AngelicCat`<br>`Ankylosaurus` |
| [`water_mask`](./Enums.md#enum-water_mask) | Enum | Specifies the shape or size of the water reflection mask applied to the object. | 83 | `big`<br>`medium`<br>`medmed` |
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array | An array of alternative animation state replacements, each as [state, animation_name]. | 47 | `[`<br>`[[idle girlyIdle]]` |
| [`spawnin_animation`](./Enums.md#enum-spawnin_animation) | Enum  | Specifies the animation played when the unit spawns in. | 37 | `"digUp"`<br>`"howl"`<br>`beamin` |
| `piece_alt_frame` | Integer | The frame index from the graphical piece sheet to use as an alternative display frame. | 27 | `1`<br>`11`<br>`13` |
| [`shadow`](./Enums.md#enum-shadow) | Enum | Specifies the visual shadow asset or type applied to the object. | 23 | `BigSlimeShadow`<br>`MedSlimeShadow`<br>`None` |
| `move_speed_sync_frames` | Float | The number of animation frames used to synchronize the movement speed of the unit. | 20 | `22`<br>`22.5`<br>`28` |
| `no_splatter` | Boolean | If true, prevents the blood splatter visual effect from appearing when the object spawns or is popped. | 17 | `false`<br>`true` |
| [`projectile_spawn_offset`](./Arrays.md#array-projectile_spawn_offset) | Array | A pair of coordinates [x, y] defining the offset from the unit's origin where projectiles spawn. | 17 | `[-1 .5]`<br>`[.1 1.5]`<br>`[.25 1.5]` |
| [`tint`](./Arrays.md#array-tint) | Array / Enum | A color tint applied to the object, either as an RGBA array [r, g, b, a] or a named color keyword. | 17 | `[.7 1 .7 1]`<br>`[.7, .4, .4, 1]`<br>`[0 0 0 1]` |
| `move_speed_multiplier` | Float | A multiplier for the unit's base movement speed. | 16 | `.5`<br>`.66`<br>`.75` |
| `dont_sink` | Boolean | If true, the object does not sink into or clip with terrain or water surfaces. | 14 | `true` |
| `art_flip` | Integer | Controls the horizontal flip of the art; -1 flips, 1 is normal. | 7 | `-1` |
| `depth_offset` | Float | An offset to the object's drawing depth, affecting its rendering order relative to other objects. | 6 | `-.1`<br>`.01`<br>`.015` |
| `four_way_animations` | Boolean | If true, the unit uses separate animations for four facing directions. | 4 | `true` |
| `show_infinity_damage_warning` | Boolean | If true, the game displays a warning when the unit has infinite damage potential. | 3 | `true` |
| `always_huge_mask` | Boolean | If true, the unit always uses a large collision or visibility mask regardless of its actual size. | 2 | `true` |
| [`default_attack_animation`](./Enums.md#enum-default_attack_animation) | Enum | Specifies the name of the default attack animation to use when no specific one is defined. | 2 | `attack2`<br>`bite1` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 2 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `shade_occluded_objects` | Boolean | If true, the object is drawn with a shade when occluded by other objects. | 2 | `true` |
| `no_horizontal_flip` | Boolean | If true, the object's art is never flipped horizontally. | 1 | `true` |
| [`override_portrait`](./Enums.md#enum-override_portrait) | Enum | Specifies a different portrait asset name to use instead of the default. | 1 | `Cherub` |
| `randomize_starting_frame` | Boolean | If true, the animation starts at a random frame instead of the first frame. | 1 | `false` |
| `status_display_count_max` | Integer | The maximum number of status effect icons displayed on the unit's HUD. | 1 | `5` |
| [`non_blocking_animations`](./Arrays.md#array-non_blocking_animations) | Array | A list of animation names that do not block gameplay or chain into new actions. | 1 | `["hit", "critical"]` |

</details>


---


### Object: `damage_instance`


**Definition:** Defines damage properties, effects, and healing for the ability's direct damage.
**Total Count:** 2346

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1731 | `damage_instance`<br>`spell`<br>`false` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1787 | `{ . . . }` |
`damage_instance`<br>`spell`<br>`self_damage`

</details>


---


### Object: `passives`


**Definition:** A container object listing passive effects granted to the unit.
**Total Count:** 733

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Alert`](./Characters_and_Bosses.md#object-alert), [`AllAlive`](./Characters_and_Bosses.md#object-allalive), [`BellyFull`](./Characters_and_Bosses.md#object-bellyfull), [`Big`](./Characters_and_Bosses.md#object-big), [`BigHolding`](./Characters_and_Bosses.md#object-bigholding), [`BigHoldingCat`](./Characters_and_Bosses.md#object-bigholdingcat), [`Bishop`](./Characters_and_Bosses.md#object-bishop), [`BlackHole`](./Characters_and_Bosses.md#object-blackhole), [`Bomb`](./Characters_and_Bosses.md#object-bomb), [`Boris`](./Characters_and_Bosses.md#object-boris), [`Bully`](./Characters_and_Bosses.md#object-bully), [`CaveBaby`](./Characters_and_Bosses.md#object-cavebaby), [`CaveMan`](./Characters_and_Bosses.md#object-caveman), [`CaveManSpear`](./Characters_and_Bosses.md#object-cavemanspear), [`CaveWoman`](./Characters_and_Bosses.md#object-cavewoman), [`CaveWomanHasCat`](./Characters_and_Bosses.md#object-cavewomanhascat), [`Charging`](./Characters_and_Bosses.md#object-charging), [`Close`](./Characters_and_Bosses.md#object-close), [`Cultist`](./Characters_and_Bosses.md#object-cultist), [`Default`](./Characters_and_Bosses.md#object-default), and 97 more...

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2628 | passives<br>class<br>	ag |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 133 | `{ . . . }` |
| [`FormChanger`](./Passives_and_Statuses.md#object-formchanger) | Object  | Defines the unit's form-changing data, including multiple form definitions and their sub-properties. | 106 | `{ . . . }` |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 94 | `1`<br>`10`<br>`2` |
| `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 88 | `1`<br>`3`<br>`4` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 65 | `1`<br>`2`<br>`3` |
| [`MeleeRevengeDamage`](./Passives_and_Statuses.md#object-meleerevengedamage) | Object  | Defines the damage and effects applied back to a melee attacker upon being hit. | 59 | `{ . . . }` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 52 | `1`<br>`2`<br>`3` |
| [`StatusEachTurnEnd`](./Passives_and_Statuses.md#object-statuseachturnend) | Object  | Specifies status effects applied to the unit at the end of each of its turns. | 49 | `{ . . . }` |
| [`Robot`](./Passives_and_Statuses.md#object-robot) | Integer / Object  | If an integer 1, the unit is robotic and affected by electric/energized effects. If an object, contains further robot-specific properties. | 47 | `{ . . . }`<br>`1` |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 39 | `Creep`<br>`Electric`<br>`Fire` |
| [`DeathRattle`](./Passives_and_Statuses.md#object-deathrattle) | Enum / Object  | Specifies an ability or effect triggered when the unit dies, optionally with a pop_corpse flag. | 35 | `{ . . . }`<br>`BBExplode`<br>`BloatyExplodey`<br>`BombFlyExplode` |
| [`FormChangeWhileHasStatus`](./Passives_and_Statuses.md#object-formchangewhilehasstatus) | Object  | Defines a form change condition that activates while the unit has a specific status effect. | 35 | `{ . . . }` |
| [`CounterAttack`](./Passives_and_Statuses.md#object-counterattack) | Array / Enum / Object  | Specifies the ability used when the unit counterattacks after being hit. | 34 | `{ . . . }`<br>`BungaSwipe`<br>`CloakerHex`<br>`CollectiveCounter` |
| [`StatusImmunity`](./Arrays.md#array-statusimmunity) | Array / Enum  | A list of status effect names the unit is immune to. | 34 | `Burn`<br>`Poison`<br>`Tarred` |
| [`StatusOnKill`](./Passives_and_Statuses.md#object-statusonkill) | Object  | Specifies status effects or actions triggered when the unit kills an enemy. | 29 | `{ . . . }` |
| [`StatusOnTookDamage`](./Passives_and_Statuses.md#object-statusontookdamage) | Object  | Specifies status effects or actions triggered when the unit takes damage. | 29 | `{ . . . }` |
| [`SpawnThingOnDamage`](./Passives_and_Statuses.md#object-spawnthingondamage) | Object  | Specifies an object that spawns on the tile when the unit takes damage. | 28 | `{ . . . }` |
| [`ImmediateAbilityReaction`](./Passives_and_Statuses.md#object-immediateabilityreaction) | Array / Enum / Object  | Specifies an ability or list of abilities used immediately in reaction to a triggering event. | 26 | `{ . . . }`<br>`BirthwortReactionShot`<br>`BumbleButt`<br>`CatGoop` |
| `Undead` | Integer | If set, flags the unit as undead (e.g., 1) with associated mechanics. | 25 | `1` |
| [`AbilityReaction`](./Passives_and_Statuses.md#object-abilityreaction) | Enum / Object  | Specifies the ability used as a reaction when the unit is targeted by an ability. | 23 | `{ . . . }`<br>`AnkyloSpin`<br>`GSOpen`<br>`Gassy_AssBlast` |
| [`SpawnOnDeath`](./Passives_and_Statuses.md#object-spawnondeath) | Enum / Object  | Specifies an object and its faction to spawn when the unit dies. | 21 | `{ . . . }`<br>`Antidote`<br>`BiggestFood`<br>`FrankPinky` |
| `AddMovement` | Integer | The amount of bonus movement points added to the unit's base movement. | 20 | `-1`<br>`-2`<br>`1` |
| [`BossRewards`](./Passives_and_Statuses.md#object-bossrewards) | Object  | Defines the common and rare item rewards dropped by a boss on defeat. | 20 | `{ . . . }` |
| [`BirdRewards`](./Passives_and_Statuses.md#object-birdrewards) | Object  | Defines the rewards and statuses applied when a bird allies with the unit. | 18 | `{ . . . }` |
| [`Buddy`](./Passives_and_Statuses.md#object-buddy) | Enum / Object  | Specifies a buddy unit that accompanies or is spawned alongside the unit, with optional reclaim and targeting properties. | 17 | `{ . . . }`<br>`BoyDino`<br>`CaveCatDad`<br>`Chubs` |
| [`CharacterLightSource`](./Passives_and_Statuses.md#object-characterlightsource) | Object  | Defines a dynamic light source attached to the unit, including color, glow, and size. | 16 | `{ . . . }` |
| [`HealthPickup`](./Passives_and_Statuses.md#object-healthpickup) | Object  | Defines properties for a health pickup object, such as healing amount and visual frame range. | 16 | `{ . . . }` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 15 | `1`<br>`2`<br>`3` |
| [`RevengeDamage`](./Passives_and_Statuses.md#object-revengedamage) | Object  | An object defining the damage and effects that trigger when the unit is attacked. | 15 | `{ . . . }` |
| `AddCorpseHealth` | Integer | The amount of bonus health the unit's corpse has before it can be resurrected. | 14 | `-999`<br>`-999999`<br>`100` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 14 | `-1`<br>`-2`<br>`1` |
| `DodgeChance` | Integer | The percentage chance the unit has to dodge incoming attacks. | 14 | `10%`<br>`15%`<br>`2%` |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum  | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 14 | `Earth`<br>`Electric`<br>`Fire` |
| `WaterWalk` | Integer | If greater than 0, allows the unit to traverse water tiles as if they were ground. | 14 | `1` |
| [`DeathRattleRevive`](./Passives_and_Statuses.md#object-deathrattlerevive) | Enum / Object  | Specifies an ability or effect that revives the unit upon death, with options for stunning behavior. | 13 | `{ . . . }`<br>`DoNothing`<br>`HCHumanDie`<br>`ToxPuff` |
| [`TransformOnDeath`](./Arrays.md#array-transformondeath) | Array / Enum  | Specifies the unit or list of units to transform into upon death. | 13 | `BishopHat`<br>`CanCreeperOut`<br>`Carcus` |
| [`AbilityHealthThreshold`](./Passives_and_Statuses.md#object-abilityhealththreshold) | Object  | Defines an ability and conditions for its activation when the unit's health reaches a threshold. | 12 | `{ . . . }` |
| `NoHealthOnlyShield` | Integer | If set (e.g., 1), the unit has no health and only a shield for damage absorption. | 12 | `1` |
| [`ReflectProjectiles`](./Passives_and_Statuses.md#object-reflectprojectiles) | Integer / Object  | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 12 | `{ . . . }`<br>`1`<br>`10%`<br>`100%` |
| [`SpawnThingOnDeath`](./Enums.md#enum-spawnthingondeath) | Enum  | Specifies the name of an object to spawn upon death. | 12 | `Boulder`<br>`CharmedDemonKitten`<br>`CharmedFlySwarm` |
| [`MoveWhenDamaged`](./Passives_and_Statuses.md#object-movewhendamaged) | Enum / Object  | Defines movement behavior when the unit takes damage, such as weights and move ability. | 11 | `{ . . . }`<br>`TKNG_Hop`<br>`move` |
| `CoinPickup` | Integer | The amount of coins awarded when this pickup is collected. | 10 | `1`<br>`10`<br>`2` |
| `LimitDamage` | Integer | The maximum amount of damage the unit can take from a single hit. | 10 | `1` |
| [`MoveTowardsDamageSource`](./Passives_and_Statuses.md#object-movetowardsdamagesource) | Enum / Object  | Determines the movement behavior when moving towards the unit that dealt damage to it. | 10 | `{ . . . }`<br>`MoveOne` |
| `StripStatuses` | Integer | If 1, removes all status effects from the unit at the beginning of its turn. | 10 | `1` |
| [`AddTag`](./Enums.md#enum-addtag) | Enum  | Specifies a gameplay tag (e.g., 'rock', 'plant') to add to the unit, used for interaction checks. | 9 | `bug`<br>`cat`<br>`fetus` |
| `BackstabImmunity` | Integer | If greater than 0, prevents the unit from taking extra damage from backstabs. | 9 | `1` |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 9 | `1` |
| `LimitHeal` | Integer | If 1, prevents the unit from being healed. | 9 | `0`<br>`1` |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 9 | `10`<br>`15`<br>`20` |
| [`MovementReaction`](./Passives_and_Statuses.md#object-movementreaction) | Object  | Specifies an ability to cast when a unit moves within range, with options for targeting and conditions. | 9 | `{ . . . }` |
| `PoisonThorns` | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 9 | `1`<br>`2`<br>`3` |
| [`SmallRockBehavior`](./Passives_and_Statuses.md#object-smallrockbehavior) | Integer / Object  | Defines the damage, knockback, and chain properties of small rocks spawned from this unit when destroyed. | 9 | `{ . . . }`<br>`0`<br>`5` |
| [`StatusCollector`](./Passives_and_Statuses.md#object-statuscollector) | Object  | Specifies the status effects and their stack counts that the unit collects to trigger transformations. | 9 | `{ . . . }` |
| [`TransformOnElementInfluence`](./Passives_and_Statuses.md#object-transformonelementinfluence) | Object  | Defines the element that triggers a transformation and the object to transform into. | 9 | `{ . . . }` |
| `FadeInsteadOfDie` | Integer | If non-zero, the unit fades out instead of dying. | 8 | `1` |
| [`FormChangeOffMap`](./Passives_and_Statuses.md#object-formchangeoffmap) | Object  | Specifies the unit's form when off the map and when on the map. | 8 | `{ . . . }` |
| [`FormChangeOnElementInfluence`](./Passives_and_Statuses.md#object-formchangeonelementinfluence) | Object  | Defines the element that triggers a form change, optional visual effects, and the target form. | 8 | `{ . . . }` |
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. | 8 | `1` |
| `Plant` | Integer | If set to 1, marks the unit as a Plant type, granting associated immunities and interactions. | 8 | `1` |
| [`RandomizeAIWeightsEachTurn`](./Arrays.md#array-randomizeaiweightseachturn) | Array  | The range of random weights applied to AI actions each turn. | 8 | `[` |
| [`StatusOnDie`](./Passives_and_Statuses.md#object-statusondie) | Object  | Specifies status effects or actions triggered when the unit dies. | 8 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 | `Default`<br>`FormChange`<br>`Druid` | `AbilityWhenBuddyDies` | Enum | Specifies the ability to cast when a nearby allied unit dies. | 174 | Default<br>FormChange<br>Druid |
| [`AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack) | Enum  | Specifies an elemental damage type that is added to the unit's basic attacks. | 7 | `Electric`<br>`Fire`<br>`Gravity` |
| `AddInitiative` | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 7 | `-10`<br>`-100`<br>`-20` |
| `AlphaTurns` | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 7 | `-1`<br>`1` |
| [`ChanceToSpitOnDamage`](./Passives_and_Statuses.md#object-chancetospitondamage) | Object  | Configures the chance to use a spit ability when taking damage, including base chance and per-damage bonus. | 7 | `{ . . . }` |
| `DebuffImmunity` | Integer | If 1, the unit is immune to debuffs. | 7 | `1` |
| `MinimumKnockbackFromAllDamage` | Integer | The minimum knockback distance the unit will suffer from any damage source. | 7 | `1` |
| `OverrideMaxHealth` | Integer | Replaces the unit's maximum health with this value. | 7 | `1`<br>`25` |
| [`SecurityBotProtect`](./Passives_and_Statuses.md#object-securitybotprotect) | Object  | Specifies the ability and movement used by a security bot to protect allies. | 7 | `{ . . . }` |
| `SetSpellCosts` | Integer | Overrides the cost of all spells to this value. | 7 | `0`<br>`1`<br>`3` |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 7 | `-1`<br>`-2`<br>`-4` |
| [`StatusOnEndMove`](./Passives_and_Statuses.md#object-statusonendmove) | Object  | Specifies status effects or actions triggered when the unit finishes moving. | 7 | `{ . . . }` |
| [`TransformInXTurns`](./Passives_and_Statuses.md#object-transforminxturns) | Object  | Defines a delayed transformation after a set number of turns, with optional target object and initiative handling. | 7 | `{ . . . }` |
| `AddDamage` | Integer | The amount of damage added to all attacks. Negative values reduce damage. | 6 | `-1`<br>`1`<br>`2` |
| [`CaveFamilyEnrage`](./Passives_and_Statuses.md#object-cavefamilyenrage) | Object  | Specifies the ability used when the number of family members with a given tag falls below a threshold. | 6 | `{ . . . }` |
| [`DelayedAutoRevive`](./Passives_and_Statuses.md#object-delayedautorevive) | Object  | Configures an automatic revival after a delay, with specified rounds and health percentage. | 6 | `{ . . . }` |
| [`Divide4OnDeath`](./Enums.md#enum-divide4ondeath) | Enum  | The object that spawns in four instances upon this unit's death. | 6 | `BiggestFood`<br>`Clot`<br>`MedSlime` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 6 | `1`<br>`10`<br>`100` |
| [`FormChangeWhilePrimingAbility`](./Passives_and_Statuses.md#object-formchangewhileprimingability) | Object  | Defines the form changes when a specific ability is being primed and when it is not. | 6 | `{ . . . }` |
| `HealthGain` | Integer | The amount of health restored to the source. | 6 | `1`<br>`10`<br>`2` |
| `IgnoreTiles` | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 6 | `1` |
| `KaijuKnockbackImmune` | Integer | If 1, the unit is immune to knockback from kaiju sources. | 6 | `1` |
| [`StatusOnTookDamageFromAbility`](./Passives_and_Statuses.md#object-statusontookdamagefromability) | Object  | Specifies status effects triggered when the unit takes damage specifically from an ability (not environmental). | 6 | `{ . . . }` |
| [`StunImmunity`](./Passives_and_Statuses.md#object-stunimmunity) | Integer / Object  | If 1, the unit is immune to stun. The optional object configures whether to cleanse stun on apply. | 6 | `{ . . . }`<br>`1` |
| [`TagGreed`](./Enums.md#enum-taggreed) | Enum  | The tag of items that this unit will move towards to collect. | 6 | `bishop_hat`<br>`food`<br>`pickup` |
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum  | Specifies the type of tile left behind as the unit moves. | 6 | `BrambleTile`<br>`CreepTile`<br>`FireTile` |
| `YOffset` | Float | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 6 | `-.18`<br>`.25`<br>`.35` |
| [`AddHiddenTag`](./Enums.md#enum-addhiddentag) | Enum  | A hidden tag applied to the unit for internal logic and triggers. | 5 | `bowling_ball`<br>`grown_hitler_clone`<br>`hitler_clone_fetus` |
| `Angel` | Integer | If 1, the unit is an angel type, which may affect behavior like reviving. | 5 | `1` |
| [`AutocastEachRound`](./Passives_and_Statuses.md#object-autocasteachround) | Enum / Object  | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 5 | `{ . . . }`<br>`SpiderReturn` |
| `Burn` | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 5 | `1`<br>`10`<br>`2` |
| `FaceShield` | Integer | If 1, the unit has a face shield that protects it from certain attacks or effects. | 5 | `0`<br>`1` |
| `InjuryImmunity` | Integer | The number of turns the unit is immune to injuries. | 5 | `1` |
| `KnockbackImmunity` | Integer | If set to 1, the unit cannot be knocked back. | 5 | `1` |
| [`MoveTowardsKillers`](./Passives_and_Statuses.md#object-movetowardskillers) | Enum / Object  | Determines the movement behavior when moving towards units that have killed an ally. | 5 | `{ . . . }`<br>`ReaperRevenge` |
| `SharkySmellsBlood` | Integer | If 1, the unit is attracted to damaged units and may prioritize them. | 5 | `1` |
| `StartOffMap` | Integer | If 1, the unit begins the encounter off the map. | 5 | `1` |
| [`TransformOnDeathImmediately`](./Passives_and_Statuses.md#object-transformondeathimmediately) | Enum / Object  | The object to transform into immediately upon death, with optional turn handling. | 5 | `{ . . . }`<br>`NoHead` |
| [`AbilityAfterEnemyCastSpell_Stackable`](./Enums.md#enum-abilityafterenemycastspell_stackable) | Enum  | The ability to cast after an enemy spell, which can stack in effect. | 4 | `ThornUp`<br>`ThornUpX` |
| `AddMaxHealth` | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 4 | `-25`<br>`10`<br>`2` |
| `AddMeleeKnockback` | Integer | The amount of additional knockback dealt by melee attacks. | 4 | `1`<br>`10`<br>`2` |
| [`AddStatusToWeapons`](./Passives_and_Statuses.md#object-addstatustoweapons) | Object  | Specifies status effects to add to the unit's weapon attacks, with their stack counts. | 4 | `{ . . . }` |
| [`AddTemporaryEffectsToBasicAttack`](./Passives_and_Statuses.md#object-addtemporaryeffectstobasicattack) | Object  | A container object that lists temporary status effects applied to the unit's basic attack. | 4 | `{ . . . }` |
| `Ammo` | Integer | The amount of ammo to add or remove (negative values subtract). | 4 | `-1`<br>`-99999`<br>`1` |
| `BackstabAllDirections` | Integer | If 1, the unit deals backstab damage from all directions. | 4 | `1` |
| [`BaitAura`](./Passives_and_Statuses.md#object-baitaura) | Object  | The range of the bait aura that draws enemies towards the unit. | 4 | `{ . . . }` |
| [`Bird`](./Enums.md#enum-bird) | Enum  | The object dropped by this bird unit upon death. | 4 | `CookedChickenLeg` |
| `BuffImmunity` | Integer | If 1, the unit is immune to buffs. An optional object can list buffs to exclude from immunity. | 4 | `1` |
| [`ChanceToBackflip`](./Passives_and_Statuses.md#object-chancetobackflip) | Object  | An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit. | 4 | `{ . . . }` |
| [`ChangeTileOnPop`](./Enums.md#enum-changetileonpop) | Enum  | The type of tile that appears when this unit is destroyed. | 4 | `CreepTile`<br>`GlitchTile`<br>`OilTile` |
| `CountAsCorpse` | Integer | If 1, the unit counts as a corpse for interactions like raising or necromancy. | 4 | `1` |
| [`DisplayDangerAOE`](./Enums.md#enum-displaydangeraoe) | Enum  | The ability whose area of effect is displayed to warn players. | 4 | `GrenadeExplode`<br>`MoonHead_Blow`<br>`TheChild_Wrath` |
| `ExtraDispersedTurns` | Integer | The number of additional or fewer turns in the dispersed turn order. | 4 | `-1`<br>`1` |
| [`GroundFlopper`](./Enums.md#enum-groundflopper) | Enum  | The movement ability used when this unit is on the ground. | 4 | `DefaultMove`<br>`MoveOne` |
| [`LoopingSoundWhileAlive`](./Enums.md#enum-loopingsoundwhilealive) | Enum  | The looping sound effect played while the unit is alive. | 4 | `BigUFO_ambient_looping`<br>`Bomb_FuseLoop`<br>`Twister_loop` |
| [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#object-passivewhenaffectedbyelement) | Object  | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 4 | `{ . . . }` |
| [`PassiveWhenDead`](./Passives_and_Statuses.md#object-passivewhendead) | Object  | Passive effects that remain active while the unit is dead. | 4 | `{ . . . }` |
| `PrioritizeFarAwayTargets` | Integer | The weight for AI to prioritize targets based on distance; higher values favor farther targets. | 4 | `1`<br>`10` |
| [`StatusOnGainCoins`](./Passives_and_Statuses.md#object-statusongaincoins) | Object  | Specifies status effects applied when this unit gains coins. | 4 | `{ . . . }` |
| [`Trapper`](./Passives_and_Statuses.md#object-trapper) | Object  | Specifies a trap-placing ability and its targeting parameters. | 4 | `{ . . . }` |
| [`WeremanTransformationReceiver`](./Enums.md#enum-weremantransformationreceiver) | Enum  | Determines which transformation animation or effect is applied when this unit is turned by a were-creature. | 4 | `CaveManTransform`<br>`CaveWomanDropTransform` |
| [`ArmorPickup`](./Passives_and_Statuses.md#object-armorpickup) | Object  | The amount of armor stacks and the frame range for the pickup animation. | 3 | `{ . . . }` |
| [`AbilityWhenTaggedCharacterMovesNear`](./Passives_and_Statuses.md#object-abilitywhentaggedcharactermovesnear) | Object  | An object containing `ability`, `tag`, and `range` that triggers the specified ability when a character with the given tag moves within range. | 3 | `{ . . . }` |
| [`AddStatusToSpells`](./Passives_and_Statuses.md#object-addstatustospells) | Object  | Specifies status effects added to all spell attacks used by this unit. | 3 | `{ . . . }` |
| `AggroTargetIsCurrentTurn` | Integer | If set to 1, the unit's aggro target is the unit currently taking its turn. | 3 | `1` |
| `BaseStatMultiply` | Float | A multiplier applied to the unit's base stats. | 3 | `.25`<br>`.5`<br>`.666` |
| [`BonusTurnPattern`](./Arrays.md#array-bonusturnpattern) | Array  | An array defining the pattern of bonus turns granted to this unit. | 3 | `[` |
| [`CanMutateTo`](./Arrays.md#array-canmutateto) | Array / Enum  | Specifies the mutation forms this unit can transform into, either a single form or an array of possible forms. | 3 | `Hyde`<br>`[Lumpy, Leaper]`<br>`[TumorousMaggot, ChargeyMaggot, SwappyMaggot]` |
| [`DigestDeadBodies`](./Enums.md#enum-digestdeadbodies) | Enum  | Specifies the ability or animation used when digesting a dead body. | 3 | `Digest`<br>`LennyCatDies`<br>`MoonHead_Digest` |
| `ExtraMovePoints` | Integer | The number of additional movement points granted to this unit. | 3 | `1` |
| [`FormChangeHealthThreshold`](./Passives_and_Statuses.md#object-formchangehealththreshold) | Object  | Specifies health thresholds that trigger form changes, with form_below for health at or below and form_above for health above. | 3 | `{ . . . }` |
| [`ManaPickup`](./Passives_and_Statuses.md#object-manapickup) | Object  | The amount of mana stacks and the frame range for the pickup animation. | 3 | `{ . . . }` |
| `MimicSpawnerAttacks` | Integer | If positive, the number of attacks mimicked; if -1, mimics all attacks from spawner. | 3 | `-1`<br>`1` |
| `MinimumKnockbackFromPhysicalAttacks` | Integer | The minimum knockback distance applied when hit by a physical attack. | 3 | `1` |
| [`MutateViaAbility`](./Enums.md#enum-mutateviaability) | Enum  | Specifies the ability that triggers a mutation form change. | 3 | `BBTransformMutant` |
| `PrioritizeHitDifferentTargets` | Integer | If set to 1, the unit's AI prioritizes hitting different targets rather than focusing one. | 3 | `1` |
| [`ProtectTargetedAllies`](./Passives_and_Statuses.md#object-protecttargetedallies) | Object  | Specifies the ability used to protect targeted allies, including an optional target filter. | 3 | `{ . . . }` |
| [`RandomPassivePool`](./Passives_and_Statuses.md#object-randompassivepool) | Object  | A pool of random passives from which one is chosen for this unit. | 3 | `{ . . . }` |
| `RunInXTurns` | Integer | The number of turns after which this unit will flee the battle. | 3 | `1`<br>`2`<br>`3` |
| `SharePickupsWithSpawner` | Integer | If set to 1, pickups collected by this unit are also given to its spawner. | 3 | `0`<br>`1` |
| `SpawnCreepOnHit` | Integer | If set to 1, spawns creep on the tile when this unit takes damage. | 3 | `1` |
| `StrengthUp` | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 3 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`SupportFormChangeInsteadOfRun`](./Passives_and_Statuses.md#object-supportformchangeinsteadofrun) | Enum / Object  | Specifies a form change to trigger instead of fleeing, either as a passive object with ability details or a direct form name. | 3 | `{ . . . }`<br>`Attacker` |
| [`TileTrail_Ahead`](./Enums.md#enum-tiletrail_ahead) | Enum  | Specifies the type of tile to place one tile ahead of the unit's movement. | 3 | `FireTile`<br>`FlowerTile`<br>`OilTile` |
| `WeaponsDontLoseDurability` | Integer | If set to 1, weapons equipped by this unit do not lose durability. | 3 | `0`<br>`1` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`AbilityOnRoundEnd`](./Passives_and_Statuses.md#object-abilityonroundend) | Object  | Specifies an ability that is automatically executed at the end of each round. | 2 | `{ . . . }` |
| `AggroTargetIsBuddy` | Integer | If set to 1, the unit's aggro target is its buddy (linked partner). | 2 | `1` |
| `AllDamageImmune_IncludingSpeculative` | Integer | If set to 1, this unit is immune to all damage, including speculative damage. | 2 | `1` |
| `AlwaysHitDifferentTargets` | Integer | If set to 1, attacks always target different units, never the same target twice. | 2 | `1` |
| [`BungaEntrance`](./Passives_and_Statuses.md#object-bungaentrance) | Object  | Specifies the entrance animation, ability, and conditions for this unit's dramatic battle entrance. | 2 | `{ . . . }` |
| `CCImmunity` | Integer | If set to 1, this unit is immune to crowd control effects. | 2 | `1` |
| `CanShield` | Integer | If set to 1, this unit can generate shields. | 2 | `1` |
| `ChanceToDisableActionsIfNotCharmed` | Integer | The percentage chance to disable actions of enemies that are not charmed. | 2 | `75%` |
| [`ChangeTileOnDeath`](./Enums.md#enum-changetileondeath) | Enum  | Specifies the tile type that replaces the current tile when this unit dies. | 2 | `WaterTile` |
| [`CherubimReaction`](./Passives_and_Statuses.md#object-cherubimreaction) | Object  | Specifies the abilities used when this unit leaves or returns to the battlefield. | 2 | `{ . . . }` |
| [`CreateGlobalModifiers`](./Passives_and_Statuses.md#object-createglobalmodifiers) | Object  | Defines global gameplay modifiers to activate. | 2 | `{ . . . }` |
| `DemonicGlyphFrames` | Integer | The number of animation frames for the demonic glyph effect. | 2 | `1` |
| [`DiesToElement`](./Passives_and_Statuses.md#object-diestoelement) | Enum / Object  | Specifies the element that instantly kills this unit, optionally with an instant flag. | 2 | `{ . . . }`<br>`Wind` |
| `DissuadeInstakills` | Integer | If set to 1, this unit cannot be instantly killed. | 2 | `1` |
| `ExpireOnSpawnerTurnEnd` | Integer | If set to 1, this unit is removed from battle at the end of its spawner's turn. | 2 | `1` |
| [`FaceLastDamage`](./Passives_and_Statuses.md#object-facelastdamage) | Integer / Object  | If set to 1, the unit turns to face the direction of the last damage received; an object can specify animation settings. | 2 | `{ . . . }`<br>`1` |
| [`FinalBossShield`](./Enums.md#enum-finalbossshield) | Enum  | Specifies the shield ability used by a final boss, or None for no shield. | 2 | `DestroyerShieldBash`<br>`None` |
| [`FormChangeDuringWeatherElement`](./Passives_and_Statuses.md#object-formchangeduringweatherelement) | Object  | Specifies a form change that triggers when the weather matches a given element. | 2 | `{ . . . }` |
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum  | Specifies a terrain element (e.g., Water, Grass) that the unit can pathfind through without penalty. | 2 | `Grass`<br>`Water` |
| `GoopWalk` | Integer | If set to 1, this unit can move through goop tiles without being slowed or damaged. | 2 | `1` |
| `ImmobilePassive` | Integer | If set to 1, this unit cannot move from its starting position. | 2 | `1` |
| [`InfiniteRebirth`](./Passives_and_Statuses.md#object-infiniterebirth) | Object  | Specifies the health and effects for unlimited rebirth upon death. | 2 | `{ . . . }` |
| [`KaijuWinCon`](./Enums.md#enum-kaijuwincon) | Enum  | Determines which kaiju victory condition is active for this unit. | 2 | `pyrophina`<br>`zaratana` |
| `MagicDamageImmune` | Integer | If set to 1, this unit is immune to magic damage. | 2 | `1` |
| `MamaCatAnimations` | Integer | If set to 1, enables special mama cat animations. | 2 | `1` |
| [`MiniVolcanoReaction`](./Enums.md#enum-minivolcanoreaction) | Enum  | Specifies the ability triggered when a mini volcano erupts near this unit. | 2 | `MiniVolcano_Spurt`<br>`ThrobShot_Reaction` |
| [`MotherTumorSpawnInCapture`](./Passives_and_Statuses.md#object-mothertumorspawnincapture) | Object  | Specifies the form changes and statuses applied when the mother tumor spawns after capturing a cat or non-cat. | 2 | `{ . . . }` |
| [`MoveAwayFromDamageSource`](./Passives_and_Statuses.md#object-moveawayfromdamagesource) | Object  | Specifies the move ability used to flee from the source of damage, or an object with `move_ability`. | 2 | `{ . . . }` |
| [`PassiveWhileHasStatus`](./Miscellaneous.md#object-passivewhilehasstatus) | Object  | An object containing `status` and `passives` that grants the listed passives while the unit has the specified status. | 2 | `{ . . . }` |
| [`PassiveWhileNotHasStatus`](./Passives_and_Statuses.md#object-passivewhilenothasstatus) | Object  | Specifies a set of passives that are active only when this unit does not have the given status. | 2 | `{ . . . }` |
| `PrioritizeAggroTarget` | Integer | A priority weight for targeting the current aggro target. | 2 | `1` |
| `PrioritizePlayerCats` | Integer | A priority weight for targeting player-controlled cats. | 2 | `1` |
| `PrioritizeWeakestEnemy` | Integer | A priority weight for targeting the weakest enemy unit. | 2 | `1` |
| `SafeDoomed` | Integer | The number of SafeDoomed stacks applied, or 'level' to scale with character level. | 2 | `1`<br>`2`<br>`level` |
| [`SharePickups`](./Passives_and_Statuses.md#object-sharepickups) | Object  | If 1 or an object with include_coins, makes the unit share pickups with nearby allies. | 2 | `{ . . . }` |
| [`SlotMachineRollPool`](./Passives_and_Statuses.md#object-slotmachinerollpool) | Object  | Defines the weighted pool of possible slot machine roll results. | 2 | `{ . . . }` |
| [`StatusAfterXTurns`](./Passives_and_Statuses.md#object-statusafterxturns) | Object  | Applies a status effect or forces an ability usage after a set number of turns. | 2 | `{ . . . }` |
| [`StatusOnSpawnIn`](./Passives_and_Statuses.md#object-statusonspawnin) | Object  | Applies statuses or actions upon the unit spawning into the battlefield. | 2 | `{ . . . }` |
| `SurviveAt1HP` | Integer | If 1, the unit survives a fatal hit with 1 HP instead of dying. | 2 | `1` |
| [`TowerDefenseReflex`](./Enums.md#enum-towerdefensereflex) | Enum  | Specifies the ability or attack used when the unit counterattacks in tower defense reflex mode. | 2 | `BasicRanged_1DMG`<br>`attack` |
| [`TransformOnElementInfluencex`](./Passives_and_Statuses.md#object-transformonelementinfluencex) | Object  | Transforms into a specified object when influenced by a given element. | 2 | `{ . . . }` |
| [`TransformWhenBuddyDies`](./Enums.md#enum-transformwhenbuddydies) | Enum  | Specifies the form the unit transforms into when its buddy dies. | 2 | `UltraOrnstein`<br>`UltraSmough` |
| `UncappedHP` | Integer | If 1, the unit's maximum HP is not capped by standard limits. | 2 | `1` |
| `UnlockOrientation` | Integer | If 1, allows the unit to freely rotate or face any direction regardless of movement. | 2 | `1` |
| [`UseAbility`](./Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. | 2 | `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`AbilityOnBattleStart_UseAI`](./Enums.md#enum-abilityonbattlestart_useai) | Enum  | Specifies the ability the unit will use at the start of battle via AI resolution. | 1 | `TheCreator_SpawnCloneTeam` |
| [`AddStatusToReceivedDamage`](./Passives_and_Statuses.md#object-addstatustoreceiveddamage) | Object  | Applies a status effect to the attacker when the unit takes damage. | 1 | `{ . . . }` |
| [`AdvancedTint`](./Arrays.md#array-advancedtint) | Array  | An RGBA color array for advanced sprite tinting. | 1 | `[` |
| [`AdventureTokenPassivePool`](./Miscellaneous.md#object-adventuretokenpassivepool) | Object  | A pool of passive definitions granted to the unit when picked up as an adventure token. | 1 | `{ . . . }` |
| [`AggroTargetIsGovernedByHitEffect`](./Passives_and_Statuses.md#object-aggrotargetisgovernedbyhiteffect) | Object  | If set, the aggro target is determined by the unit's hit effect, with a sub-key for enemies_only. | 1 | `{ . . . }` |
| `AggroTargetIsLastEnemyThatDealtDamage` | Integer | If 1, the unit's aggro target is the last enemy that damaged it. | 1 | `1` |
| `AggroTargetIsLowestHealthEnemyTillItDies` | Integer | If 1, the unit focuses the lowest health enemy until that enemy dies. | 1 | `1` |
| `AggroTargetIsLowestMaxHealthCat` | Integer | If 1, the unit targets the cat ally with the lowest maximum health. | 1 | `1` |
| [`AlienBeastDangerZones`](./Arrays.md#array-alienbeastdangerzones) | Array  | An array of ability names that mark dangerous zones for the Alien Beast fight. | 1 | [AlienBeastPuke] |
| `AlienBeastEyeStalks` | Integer | The number of eye stalk segments on the Alien Beast. | 1 | `3` |
| `AllSpellsCostActPoints` | Integer | If 1, all spells require action points instead of mana or other resources. | 1 | `1` |
| [`AllStatsAura`](./Passives_and_Statuses.md#object-allstatsaura) | Object  | An aura that grants bonus stacks of all stats to allies within range. | 1 | `{ . . . }` |
| `AvoidDamagingCharmedEnemies` | Integer | If 1, the unit avoids dealing damage to charmed enemies. | 1 | `1` |
| `AwardCoinsOnDeath` | Integer | The amount of coins awarded to the killer when this unit dies. | 1 | `10` |
| `BasicAIDangerZone` | Integer | The radius of the danger zone used by the basic AI for area denial. | 1 | `2` |
| [`BattlefieldUniqueRandomPassive`](./Passives_and_Statuses.md#object-battlefielduniquerandompassive) | Object  | A pool of unique random passives that can be applied to each battlefield instance. | 1 | `{ . . . }` |
| `BlackHolePassive` | Integer | If 1, the unit has black hole passive mechanics. | 1 | `1` |
| [`BloatEyePassive2`](./Enums.md#enum-bloateyepassive2) | Enum  | Specifies the movement ability for the Bloat Eye enemy. | 1 | `BloatEyeMovement2` |
| `BlockAllDamage` | Integer | If 1, the unit blocks all incoming damage. | 1 | `1` |
| `BombBehavior` | Integer | If 1, the unit explodes after a set duration or on death. | 1 | `1` |
| [`BungaCheers`](./Passives_and_Statuses.md#object-bungacheers) | Object  | Defines cheer particle effects and sounds triggered by ally or enemy actions. | 1 | `{ . . . }` |
| `CapReceivedDamage` | Integer | If 1, the unit caps incoming damage to a maximum per hit. | 1 | `1` |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| [`CerberubsAggroTargetBehavior`](./Passives_and_Statuses.md#object-cerberubsaggrotargetbehavior) | Object  | Defines the default and alert forms used by Cerberubs when changing aggro behavior. | 1 | `{ . . . }` |
| [`ChanceToFormChangeOnAbilityDamage`](./Passives_and_Statuses.md#object-chancetoformchangeonabilitydamage) | Object  | A chance to transform into a different form when damaged by an ability. | 1 | `{ . . . }` |
| [`ChaosBossFormChangeGuide`](./Passives_and_Statuses.md#object-chaosbossformchangeguide) | Object  | Defines active and passive piece sets and a health threshold for the Chaos boss's form change pattern. | 1 | `{ . . . }` |
| [`ChaosBossPieces`](./Passives_and_Statuses.md#object-chaosbosspieces) | Object  | Defines the list of active and passive piece tags for the Chaos boss fight. | 1 | `{ . . . }` |
| [`ChaosHeadDropIn`](./Passives_and_Statuses.md#object-chaosheaddropin) | Object  | Defines the tag, spawn ability, and music for the Chaos head's drop-in sequence. | 1 | `{ . . . }` |
| [`ConjureBonusAbility`](./Enums.md#enum-conjurebonusability) | Enum  | Specifies the name of the bonus ability to conjure. | 1 | `Class`<br>`Colorless`<br>`Mage` |
| [`CounterAttackAfterEnemyCastSpell`](./Enums.md#enum-counterattackafterenemycastspell) | Enum  | Specifies the ability the unit uses to counterattack after an enemy casts a spell. | 1 | `Telekinesis` |
| `CrowAttackLink` | Integer | If 1, allows this unit's attacks to chain or link to nearby enemies like a crow. | 1 | `1` |
| `DamageFromBehindOnly` | Integer | If 1, the unit can only be damaged when attacked from behind. | 1 | `1` |
| `DemonicGlyphStealer` | Integer | If 1, the unit can steal demonic glyphs from other units. | 1 | `1` |
| [`DiceBehavior`](./Passives_and_Statuses.md#object-dicebehavior) | Object  | Defines the dice size and knockback damage for the Dice enemy. | 1 | `{ . . . }` |
| [`DicerArt`](./Arrays.md#array-dicerart) | Array  | An array of art offset values for the Dicer enemy. | 1 | `[59 52 65 50 54 63 64]` |
| `DieWhenOnlyGolemsLeft` | Integer | If 1, the unit dies when only golem-type allies remain on the field. | 1 | `1` |
| `DieWhenSpawnerDies` | Integer | If 1, the unit dies when its spawner unit dies. | 1 | `1` |
| [`DiesToPiercingAndSpikes`](./Passives_and_Statuses.md#object-diestopiercingandspikes) | Object  | Makes the unit take lethal damage from piercing attacks and spike terrain. | 1 | `{ . . . }` |
| `DisableSpells` | Integer | If 1, the unit cannot cast spells. | 1 | `1` |
| `Disguised` | Integer | If true, the unit is disguised, appearing as a different faction or model. | 1 | `1` |
| [`DisguisedTrapper`](./Enums.md#enum-disguisedtrapper) | Enum  | Specifies the passive used when disguised as a trapper, e.g. FearMelee. | 1 | `FearMelee` |
| `DisplayBuddyCatOnSpawn` | Integer | The number of buddy cat objects to display when the unit spawns. | 1 | `3` |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| `DivineShieldPickup` | Integer | The number of divine shield charges granted on pickup. | 1 | `1` |
| `DodgeChanceWithBlindSpot` | Integer | The percentage chance to dodge attacks while a blind spot condition is active. | 1 | `25%` |
| [`DodgeWhenTargeted`](./Passives_and_Statuses.md#object-dodgewhentargeted) | Object  | An object defining the ability and effects triggered when the unit is targeted for an attack. | 1 | `{ . . . }` |
| `DustCloudBehavior` | Integer | An integer flag that controls the behavior mode of a dust cloud entity. | 1 | `1` |
| `Dybbuk1HPTracker` | Integer | A flag indicating the unit tracks that it has 1 HP remaining for Dybbuk possession mechanics. | 1 | `1` |
| [`DybbukPossessionFallback`](./Passives_and_Statuses.md#object-dybbukpossessionfallback) | Object  | An object specifying the fallback form and exit ability used when possession fails. | 1 | `{ . . . }` |
| `ElectricArcs` | Integer | The number of electric arcs emitted by this unit. | 1 | `1` |
| [`ElementWeakness`](./Enums.md#enum-elementweakness) | Enum  | Determines which element the unit is weak to, e.g. Fire. | 1 | `Fire` |
| `EnrageOnDamage` | Integer | If set to 1, the unit gains enrage stacks when taking damage. | 1 | `1` |
| `EraseSpawnCoins` | Integer | If set to 1, the unit erases spawn coins from the map on spawn. | 1 | `1` |
| `EventBounterHunterPassive` | Integer | A flag enabling the event bounty hunter passive behavior. | 1 | `1` |
| [`ExtraTurnsPerTaggedUnit`](./Enums.md#enum-extraturnspertaggedunit) | Enum  | Specifies the tag of units that grant extra turns when present. | 1 | `sprout` |
| [`FaceAwayLastDamage`](./Passives_and_Statuses.md#object-faceawaylastdamage) | Object  | An object defining animation overrides for the last damage event when the unit faces away. | 1 | `{ . . . }` |
| [`FinalBossBeamQueue`](./Passives_and_Statuses.md#object-finalbossbeamqueue) | Object  | An object defining the queue of beam ability actions for the final boss form. | 1 | `{ . . . }` |
| [`FinalBossBecomeTheChild`](./Passives_and_Statuses.md#object-finalbossbecomethechild) | Object  | An object defining the transformation and environment changes when the boss becomes TheChild. | 1 | `{ . . . }` |
| [`FinalBossHitCountdownBoris`](./Passives_and_Statuses.md#object-finalbosshitcountdownboris) | Object  | An object defining the countdown status effect properties for the Boris phase, including stacks, icons, and forced abilities. | 1 | `{ . . . }` |
| [`FinalBossHitCountdownExplosive`](./Passives_and_Statuses.md#object-finalbosshitcountdownexplosive) | Object  | An object defining the countdown status effect properties for the Explosive phase, including stacks, icons, and forced abilities. | 1 | `{ . . . }` |
| [`FinalBossHitCountdownHoly`](./Passives_and_Statuses.md#object-finalbosshitcountdownholy) | Object  | An object defining the countdown status effect properties for the Holy phase, including stacks and icons. | 1 | `{ . . . }` |
| [`FinalBossPupils`](./Passives_and_Statuses.md#object-finalbosspupils) | Object  | An object configuring the visual tracking of the final boss's pupils, including radius, head position, and teleport tracking. | 1 | `{ . . . }` |
| [`FinalBossShieldHealth`](./Passives_and_Statuses.md#object-finalbossshieldhealth) | Object  | An object defining the shield health thresholds per visual state for the final boss. | 1 | `{ . . . }` |
| [`FinalBossSyncAnimations`](./Passives_and_Statuses.md#object-finalbosssyncanimations) | Object  | An object defining animation synchronization with another character, including form change abilities. | 1 | `{ . . . }` |
| `FlingObjectsOnTop` | Integer | The number of objects to fling on top of this unit. | 1 | `8` |
| [`FlushmasterCelebration`](./Enums.md#enum-flushmastercelebration) | Enum  | Specifies the celebration animation or effect name used by the Flushmaster. | 1 | `celebrate` |
| `ForceDodgeEverything` | Integer | If set to 1, the unit will always dodge all incoming attacks. | 1 | `1` |
| [`FormChangeWhenBuddyDies`](./Enums.md#enum-formchangewhenbuddydies) | Enum  | Specifies the form name the unit changes into when its buddy dies. | 1 | `Rage` |
| `FullBlockEverything` | Integer | If set to 1, the unit fully blocks all incoming damage. | 1 | `1` |
| `FullBlockEverythingTo0Damage` | Integer | If set to 1, the unit reduces all incoming damage to 0. | 1 | `1` |
| `GasCanBehavior` | Integer | An integer flag that controls the behavior mode of a gas can entity. | 1 | `1` |
| `GasCloudBehavior2` | Integer | An integer flag that controls a secondary behavior mode of a gas cloud entity. | 1 | `2` |
| `GeminiTwin` | Integer | If set to 1, this unit is the twin in a Gemini pair. | 1 | `1` |
| `GlobalManaDrainAura` | Integer | The amount of mana drained per turn from all units in range. | 1 | `-1` |
| `GoopImmunity` | Integer | If set to 1, the unit is immune to goop status effects. | 1 | `1` |
| `GuillotinaDeathHead` | Integer | If set to 1, the unit spawns a head object upon death via guillotine. | 1 | `1` |
| [`HPAltStates`](./Passives_and_Statuses.md#object-hpaltstates) | Object  | An object defining alternate visual frames based on current HP thresholds. | 1 | `{ . . . }` |
| [`HarpoonTrapPassive`](./Enums.md#enum-harpoontrappassive) | Enum  | Specifies the ability name used when the harpoon trap is triggered. | 1 | `HarpoonTrapPull` |
| [`HealNeighborsEachTurn`](./Passives_and_Statuses.md#object-healneighborseachturn) | Object  | An object defining the amount and target filtering for healing adjacent units each turn. | 1 | `{ . . . }` |
| `HiddenDoomed` | Integer | The number of stacks of a hidden doomed status effect applied to the unit. | 1 | `2` |
| [`HitlerExecute`](./Passives_and_Statuses.md#object-hitlerexecute) | Object  | An object defining the tag, ability, and health threshold for executing a clone. | 1 | `{ . . . }` |
| `IceBlockBehavior` | Integer | An integer flag that controls the behavior mode of an ice block entity. | 1 | `1` |
| `IllusionTint` | Integer | If non-zero, applies an illusionary tint to the unit's sprite. | 1 | `1` |
| `InheritSpawnerStats` | Integer | If set to 1, the unit inherits the stats of its spawner. | 1 | `1` |
| `InsertIntoBackgroundPlaceholder` | Integer | If set to 1, the unit is inserted into a background placeholder slot. | 1 | `1` |
| [`JohnnyNeedsWashing`](./Passives_and_Statuses.md#object-johnnyneedswashing) | Object  | An object specifying the form names for washed and unwashed states. | 1 | `{ . . . }` |
| [`JohnnyWasher`](./Enums.md#enum-johnnywasher) | Enum  | Specifies the ability name used by the washer form to clean Johnny. | 1 | `BBTransformZealot` |
| [`LegacySpawnSavedCatIfExists`](./Enums.md#enum-legacyspawnsavedcatifexists) | Enum  | Specifies the legacy saved cat ID to spawn if it exists in the save data. | 1 | `Legacy_Marshmallow_StolenCatID` |
| [`LockOrientationFaceTile`](./Arrays.md#array-lockorientationfacetile) | Array  | A tile coordinate [x y] that the unit's orientation is locked to face. | 1 | `[0 0]` |
| [`ManglerMonsterPassive`](./Enums.md#enum-manglermonsterpassive) | Enum  | Specifies the ability name used for the Mangler monster's dash attack. | 1 | `ManglerMonsterDashAttack` |
| [`MegaDinoDropController`](./Passives_and_Statuses.md#object-megadinodropcontroller) | Object  | An object defining the abilities and stable leg count for the Mega Dino's leg drop sequence. | 1 | `{ . . . }` |
| [`ModularPickup`](./Passives_and_Statuses.md#object-modularpickup) | Object  | An object defining the effects and sounds triggered when the unit is picked up. | 1 | `{ . . . }` |
| [`MonkCatReactionAbilities`](./Passives_and_Statuses.md#object-monkcatreactionabilities) | Object  | A set of mappings from action types (move, attack, spell, trinket) to the corresponding ability IDs the MonkCat will use for reactions. | 1 | `{ . . . }` |
| [`MoonHeadCrackedVisual`](./Enums.md#enum-moonheadcrackedvisual) | Enum  | Specifies the visual state for the character's cracked head appearance. | 1 | `Cracked` |
| [`MotherGrowController`](./Passives_and_Statuses.md#object-mothergrowcontroller) | Object  | Controls the growth of tumors on The Mother, including the tumor object, damage type, damage amount, and whether it pierces defense when eating damage. | 1 | `{ . . . }` |
| [`MotherTumorPassive`](./Passives_and_Statuses.md#object-mothertumorpassive) | Object  | Defines the passive behavior for a MotherTumor, including the forms considered for pass/receive, the pass and receive animations, and the grow ability. | 1 | `{ . . . }` |
| [`Mount`](./Passives_and_Statuses.md#object-mount) | Object  | Defines the entering and ejecting abilities for a mountable unit, along with its death rattle ability. | 1 | `{ . . . }` |
| [`MoveAfterAnyAttemptedAttack`](./Passives_and_Statuses.md#object-moveafteranyattemptedattack) | Object  | Defines the movement behavior (weights and abilities) used after any attempted attack. | 1 | `{ . . . }` |
| [`MoveAwayWhenEnemyAdjacent`](./Passives_and_Statuses.md#object-moveawaywhenenemyadjacent) | Object  | Defines the movement behavior (move_ability, weights, and whether it triggers once per turn) when an enemy is adjacent. | 1 | `{ . . . }` |
| [`MultiSpawnOnDeath`](./Passives_and_Statuses.md#object-multispawnondeath) | Object  | Specifies the object to spawn and the range of number of objects to spawn on death. | 1 | `{ . . . }` |
| `MulticatHeads` | Integer | The number of additional heads the Multicat has. | 1 | `0` |
| `MutateAfterXTurns` | Integer | The number of turns after which the character automatically mutates (or transforms). | 1 | `3` |
| `MuteDemonicGlyphDisplay` | Integer | If set to 1, suppresses the display of demonic glyphs on the character. | 1 | `1` |
| `OrthogonalAIDangerZone` | Integer | The range (in tiles) for the AI's orthogonal danger zone detection. | 1 | `10` |
| `PackHunting` | Integer | If set to 1, enables pack hunting behavior for the character. | 1 | `1` |
| `Phasing` | Integer | If set to 1, allows the character to phase through solid objects or obstacles. | 1 | `1` |
| `ReturnBoundItemOnBattleEnd` | Integer | If set to 1, items bound to this character are returned to their owner at the end of battle. | 1 | `1` |
| `RunWhenKittensDead` | Integer | If set to 1, causes the character to attempt to flee when all associated kittens are dead. | 1 | `1` |
| [`RunWhenLastPlayerCatIsCharmed`](./Passives_and_Statuses.md#object-runwhenlastplayercatischarmed) | Object  | Defines the behavior (including mid-turn decision allowance and legacy save key) for fleeing when the last player cat is charmed. | 1 | `{ . . . }` |
| [`ScalingAttackAnimation`](./Passives_and_Statuses.md#object-scalingattackanimation) | Object  | Maps attack animations to damage thresholds; when the unit's attack stat reaches a threshold, the corresponding animation overrides the default. | 1 | `{ . . . }` |
| [`SkipFirstRounds`](./Passives_and_Statuses.md#object-skipfirstrounds) | Object  | Determines the number of initial rounds to skip and the chance per round of 'popping' (becoming active). | 1 | `{ . . . }` |
| `SpawnCreepOnHitKnockback` | Integer | If set to 1, spawns creep on the tile where a hit knocks back an enemy. | 1 | `1` |
| `SpawnerCatDataReference` | Integer | A reference ID pointing to the spawner cat's data, used by minions to link back to their spawner. | 1 | `1` |
| [`SpewerAltGraphics`](./Passives_and_Statuses.md#object-speweraltgraphics) | Object  | Maps different Spewer liquid types (Normal, Fire, Tar) to their corresponding alternate graphic indices. | 1 | `{ . . . }` |
| `SpreadWater` | Integer | If set to 1, causes the character to spread water onto adjacent tiles. | 1 | `1` |
| `SproutsGrantMovement` | Integer | If set to 1, sprouts on the character grant additional movement (aliases to MovementUp). | 1 | `1` |
| `StartDead` | Integer | The percentage chance that the character starts the battle already dead. | 1 | `100%` |
| [`StatusEachTurnBeginIfHasStatus`](./Passives_and_Statuses.md#object-statuseachturnbeginifhasstatus) | Object  | Defines a status effect to apply (and optionally consume) at the start of each turn if the character already has a specific status, with a specified animation. | 1 | `{ . . . }` |
| [`StatusEachTurnEndIfEnabledAtStartOfTurn`](./Passives_and_Statuses.md#object-statuseachturnendifenabledatstartofturn) | Object  | Defines an ability to force-use at the end of each turn if the character was in the specified form at the start of the turn. | 1 | `{ . . . }` |
| [`StatusOnEnemyConfused`](./Passives_and_Statuses.md#object-statusonenemyconfused) | Object  | Defines an ability to immediately use when an enemy becomes confused. | 1 | `{ . . . }` |
| [`StatusOverlappingCharactersAndDie`](./Passives_and_Statuses.md#object-statusoverlappingcharactersanddie) | Object  | Defines a status effect applied to overlapping characters, after which the character dies. | 1 | `{ . . . }` |
| [`StatusWhenStatusCompletelyRemoved`](./Passives_and_Statuses.md#object-statuswhenstatuscompletelyremoved) | Object  | Defines a status to apply and an ability to use when a specific status is completely removed from the character. | 1 | `{ . . . }` |
| [`SupportDieInsteadOfRun`](./Passives_and_Statuses.md#object-supportdieinsteadofrun) | Object  | Configures alternative dying and dead animations for support units that die instead of fleeing. | 1 | `{ . . . }` |
| [`SwimmingFormChange`](./Passives_and_Statuses.md#object-swimmingformchange) | Object  | Defines the form names to switch to when in water and when exiting water. | 1 | `{ . . . }` |
| [`SyncFormsWithBuddy`](./Passives_and_Statuses.md#object-syncformswithbuddy) | Object  | Specifies the form to revert to if the character has no buddy, ensuring form synchronization. | 1 | `{ . . . }` |
| [`T3HitlerSpawningPhase`](./Passives_and_Statuses.md#object-t3hitlerspawningphase) | Object  | Defines weighted groups of spawn abilities used during the T3Hitler boss's spawning phase. | 1 | `{ . . . }` |
| `TVBotDisableAttack` | Integer | If set to 1, disables the TVBot's ability to attack. | 1 | `1` |
| `TVBotDisableMove` | Integer | If set to 1, disables the TVBot's ability to move. | 1 | `1` |
| `TVBotDisableSpells` | Integer | If set to 1, disables the TVBot's ability to use spells. | 1 | `1` |
| [`TVBotScreen`](./Passives_and_Statuses.md#object-tvbotscreen) | Object  | Maps TVBot screen channel names to their corresponding form indices. | 1 | `{ . . . }` |
| `TakeWeaponFromSpawner` | Integer | If set to 1, the minion inherits the weapon from its spawner. | 1 | `1` |
| `Tall` | Integer | If set to 1, the character occupies a taller hitbox or sprite space. | 1 | `1` |
| [`TallTumorManaBurn`](./Enums.md#enum-talltumormanaburn) | Enum  | Specifies the mana burn ability used by the TallTumor. | 1 | `TT_ManaBurn` |
| [`Terminator2Chase`](./Enums.md#enum-terminator2chase) | Enum  | Specifies the movement ability used by Terminator2 when chasing the target. | 1 | `move` |
| [`Terminator2Run`](./Passives_and_Statuses.md#object-terminator2run) | Object  | Defines the movement ability and movement weights used by Terminator2 when running away. | 1 | `{ . . . }` |
| [`TerminatorChase`](./Passives_and_Statuses.md#object-terminatorchase) | Object  | Defines the movement ability and reaction ability used by Terminator1 when chasing a target, plus whether it prioritizes player cats. | 1 | `{ . . . }` |
| [`TerminatorSkin`](./Passives_and_Statuses.md#object-terminatorskin) | Object  | Defines the status effect and groups of stacks applied by the Terminator's skin passive. | 1 | `{ . . . }` |
| [`TileElementDamageImmunity`](./Enums.md#enum-tileelementdamageimmunity) | Enum  | Determines which tile element type the character is immune to damage from. | 1 | `Ice` |
| [`TinkererBasicAttackSwitching`](./Passives_and_Statuses.md#object-tinkererbasicattackswitching) | Object  | Defines the abilities used for the Tinkerer's basic attack switching mechanic. | 1 | `{ . . . }` |
| `TireBehavior` | Integer | If set to 1, activates special tire-related behavior for the character. | 1 | `1` |
| `TormentorHeal` | Integer | If set to 1, the Tormentor can heal itself. | 1 | `1` |
| [`TrackAmountKilledByPlayer`](./Enums.md#enum-trackamountkilledbyplayer) | Enum  | Specifies the name of the counter used to track how many of this type the player has killed. | 1 | `BonusBirdsKilled` |
| [`TransformOnStatusThreshold`](./Passives_and_Statuses.md#object-transformonstatusthreshold) | Object  | Defines the status effect, the stack threshold at which to transform, and the object to transform into. | 1 | `{ . . . }` |
| `TutorialBossRiggedFight` | Integer | The turn count at which the tutorial boss fight becomes rigged. | 1 | `16` |
| [`TwisterFling`](./Passives_and_Statuses.md#object-twisterfling) | Object  | Defines the minimum distance, maximum distance, and damage for the TwisterFling ability. | 1 | `{ . . . }` |
| [`UnlimitedDeathRattleRevive`](./Passives_and_Statuses.md#object-unlimiteddeathrattlerevive) | Object  | Configures an unlimited revive effect, including the ability to use and whether it works even when stunned. | 1 | `{ . . . }` |
| `UpTireBehavior` | Integer | The behavior type integer for the Tire's upward form. | 1 | `5` |
| [`UseAbilityWhenOutOfStatus`](./Passives_and_Statuses.md#object-useabilitywhenoutofstatus) | Object  | Defines an ability to execute when the unit no longer has a specified status. | 1 | `{ . . . }` |
| [`UseAbilityWhenShieldDepleted`](./Enums.md#enum-useabilitywhenshielddepleted) | Enum  | The ability to use when the unit's shield is fully depleted. | 1 | `T3Pebbles_PrimeBoulderDrop` |
| `Wall` | Integer | If 1, the unit is treated as an impassable wall. | 1 | `1` |
| [`WhitelistPickupType`](./Enums.md#enum-whitelistpickuptype) | Enum  | Specifies the type of pickup that this unit is allowed to collect. | 1 | `food` |
| `WideBackstab` | Integer | The additional width for backstab attacks, in tiles. | 1 | `1` |
| `WispDodge` | Integer | If 1, the unit gains the Wisp's dodge ability. | 1 | `1` |
| `ZeroKnockbackDamage` | Integer | If 1, the unit takes no damage from knockback effects. | 1 | `1` |

</details>


---


### Object: `properties`


**Definition:** A container object defining a character's base attributes, tags, faction, health, movement, and other core properties.
**Total Count:** 600

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 534 | `damage_instance`<br>`spell`<br>`false` |
| [`faction`](./Enums.md#enum-faction) | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 505 | `allies`<br>`auto`<br>`birds` |
| `health` | Integer | The maximum hit points of the unit. | 427 | `0`<br>`1`<br>`10` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 399 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 280 | `[attack move spell]`<br>`attack`<br>`battle` |`damage_instance`<br>`spell`<br>`self_damage`
| `movement` | Integer | The movement range of the unit in tiles per turn. | 277 | `0`<br>`1`<br>`2` |
| `corpse_health` | Integer | The health of the unit's corpse after death; 'indestructible' means it cannot be destroyed. | 195 | `0`<br>`1`<br>`3` |
| `inherit_faction` | Boolean | If true, the unit inherits the faction of its spawner or parent. | 115 | `false`<br>`true` |
| `dispersed_bonus_turns` | Integer | The number of bonus turns granted to this unit when its turn order is dispersed. | 104 | `0`<br>`1`<br>`2` |
| `base_mana_regen` | Integer | The base amount of mana regenerated per turn. | 90 | `0`<br>`3`<br>`999` |
| [`size`](./Enums.md#enum-size) | Enum / Float | The scale factor (size multiplier) of the spawned unit. | 80 | `.2`<br>`.5`<br>`1` |
| [`shield`](./Enums.md#enum-shield) | Enum / Integer  | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 74 | `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |
| [`move_block`](./Enums.md#enum-move_block) | Enum | Determines which movement directions are blocked. | 73 | `everything_even_when_dead`<br>`nothing` |
| `kill_required` | Boolean | If true, the unit must be killed to complete the objective. | 69 | `false`<br>`true` |
| `can_be_backstabbed` | Boolean | If true, the unit can be backstabbed. | 68 | `false` |
| [`initiative`](./Enums.md#enum-initiative) | Enum / Integer  | The unit's turn order priority; can be an integer modifier or 'keep_turns_end_turn' to force end of turn after acting. | 61 | `-10`<br>`-100`<br>`-20` |
| `takes_turns` | Boolean | If true, the unit participates in the turn order. | 61 | `false`<br>`true` |
| `mana_regen` | Integer | The amount of mana regenerated per turn, overriding base_mana_regen if set. | 51 | `999` |
| `mana` | Equation | The amount of mana required to cast, as a formula or stat. | 50 | `"4-clamp(floor(X/7), 0, 1)"`<br>`"max(4-X, 0)"`<br>`"max(7-2*X,0)"` |
| `flying` | Boolean | If true, the unit can fly over obstacles and is immune to ground effects. | 47 | `true` |
| [`banned_elite_buffs`](./Arrays.md#array-banned_elite_buffs) | Array | A list of elite buff types that cannot be applied to this unit. | 45 | `[Depressing]`<br>`[Mad Twin]`<br>`[Mad]` |
| [`hidden_tag`](./Arrays.md#array-hidden_tag) | Array / Enum | A tag used for internal categorization, not shown to the player. | 38 | `[bird bonusbird]`<br>`[megadino megadinoleg]`<br>`[moonhand moonboss]` |
| `weak_threshold` | Integer | The health threshold below which the unit is considered weakened. | 32 | `0`<br>`1`<br>`15` |
| `knockback_immune` | Boolean | If true, the unit cannot be knocked back. | 25 | `true` |
| `can_be_champion` | Boolean | If true, the unit can spawn as a champion variant. | 20 | `false`<br>`true` |
| [`lock_orientation`](./Arrays.md#array-lock_orientation) | Array | Forces the unit's facing direction to a fixed vector. | 19 | `[-1 0]`<br>`[-1, 0]`<br>`[0 -1]` |
| `ai_scale` | Float | A multiplier for the unit's AI decision-making weight. | 18 | `.01`<br>`.25`<br>`.5` |
| `layer` | `String` | Specifies the layer on which the ability's effect operates (e.g., characters, tiles, gas). | 17 | `2`<br>`all`<br>`characters` |
| [`auto_run_priority`](./Enums.md#enum-auto_run_priority) | Enum | Determines the unit's auto-run behavior priority. | 16 | `default`<br>`stationary`<br>`support` |
| `inanimate` | Boolean | If true, the unit is treated as an inanimate object. | 16 | `true` |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 16 | `[`<br>`[Heat Fire]` |
| `disperse_main_turns` | Boolean | If true, the unit's main turns are dispersed across the turn order. | 15 | `false`<br>`true` |
| [`hidden_tags`](./Arrays.md#array-hidden_tags) | Array / Enum | A list of hidden tags for internal grouping and behavior. | 14 | `[terminator_mini dc_cat]`<br>`terminator_mini` |
| [`tags`](./Arrays.md#array-tags) | Array / Enum | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 14 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| `evenly_dispersed_bonus_turns` | Integer | The number of bonus turns spread evenly across the turn order for this unit. | 13 | `1`<br>`2`<br>`3` |
| `initiative_adjustment` | Integer | Adjusts the unit's base initiative. | 1 | `5` |
| `exclude_from_hallucinate` | Boolean | If true, the unit is not included in hallucination effects. | 13 | `true` |
| `round_end_bonus_turns` | Integer | The number of bonus turns granted at the end of each round. | 13 | `1` |
| `can_be_overkilled` | Boolean | If true, the unit can be overkilled. | 12 | `false`<br>`true` |
| `can_collect_coins` | Boolean | If true, the unit can pick up coins. | 10 | `false`<br>`true` |
| `deathpoof_size` | Integer | The size scale of the death poof effect when the unit dies. | 10 | `1` |
| `dispersed_bonus_turns_consider_initiative` | Boolean | If true, dispersed bonus turns take the unit's initiative into account. | 10 | `false` |
| `initial_health` | Integer | The starting health of the unit when spawned. | 10 | `1`<br>`10`<br>`14` |
| [`held_coins`](./Arrays.md#array-held_coins) | Array / Integer | The number of coins the unit holds; can be a range [min max]. | 10 | `0`<br>`5`<br>`[0 1]` |
| `can_eat_food` | Boolean | If true, the unit can consume food items. | 9 | `false`<br>`true` |
| `can_grant_extra_turns` | Boolean | If true, the unit can grant extra turns to allies. | 8 | `false` |
| `tall` | Boolean | If true, the unit occupies two vertical tiles. | 8 | `true` |
| `dispersed_bonus_turns_before_cats` | Boolean | If true, the unit's dispersed bonus turns occur before the cat's turn order. | 7 | `false`<br>`true` |
| `divine_shield` | Integer | The number of stacks of the Divine Shield status this mutation provides. | 7 | `0`<br>`1`<br>`2` |
| `is_player_cat` | Boolean | If true, the unit is considered a player-controlled cat. | 7 | `false`<br>`true` |
| `boss_minions_runaway` | Boolean | If true, the boss's minions will flee when the boss is defeated. | 6 | `false` |
| `mana_matters` | Boolean | If true, the unit's mana is used for ability costs and mana regeneration. | 6 | `false`<br>`true`<br>`true*/` |
| `access_to_player_inventory` | Boolean | If true, the unit can access and use items from the player's inventory. | 5 | `false`<br>`true` |
| `act_points` | Integer | The number of action points required to use the ability. | 5 | `0`<br>`1`<br>`2` |
| `takes_main_turn` | Boolean | If true, the unit consumes the main turn phase of the round. | 5 | `false`<br>`true` |
| `visually_spiky` | Boolean | If true, the unit's sprite appears visually spiky for aesthetic purposes. | 5 | `true` |
| `allow_passive_spelltransforming` | Boolean | If true, the unit can be transformed into spells via passive effects. | 4 | `true` |
| `base_crit_chance` | Integer | The base critical hit chance for the unit. | 4 | `-999`<br>`0` |
| `last_turn_is_main_turn` | Boolean | If true, the unit's final turn in a round is treated as a main turn. | 4 | `true` |
| `round_start_bonus_turns` | Integer | The number of extra turns the unit gains at the start of each round. | 4 | `1` |
| `view_bleeding_characters_as_enemies` | Boolean | If true, the unit treats any bleeding character as an enemy. | 4 | `true` |
| [`aoe_pierce_mode`](./Enums.md#enum-aoe_pierce_mode) | Enum | Specifies the area-of-effect piercing behavior for projectiles. | 3 | `block` |
| `base_initiative` | Integer | The unit's base initiative, used for turn order determination. | 3 | `-1`<br>`0` |
| `base_movement` | Integer | The unit's base movement range in tiles. | 3 | `4` |
| `catdata_ignore_skills` | Boolean | If true, the unit ignores its cat data skills. | 3 | `true` |
| [`disallow_items`](./Enums.md#enum-disallow_items) | Enum | Determines which items the unit is prohibited from using. | 3 | `Nuke`<br>`all` |
| `always_triggers_traps` | Boolean | If true, the unit always activates traps upon stepping on them. | 2 | `true` |
| `base_health` | Integer | The unit's base maximum health. | 2 | `0` |
| `base_health_regen` | Integer | The amount of health the unit regenerates per turn. | 2 | `0` |
| `base_initial_mana` | Integer | The amount of mana the unit starts with at the beginning of a mission. | 2 | `0` |
| `base_mana` | Integer | The unit's base maximum mana. | 2 | `0` |
| `blocking` | Boolean | If true, the unit blocks movement and line-of-sight. | 2 | `false`<br>`idlenoani` |
| `can_be_elite` | Boolean | If true, the unit can spawn as an elite variant. | 2 | `false` |
| `can_run` | Boolean | If true, the unit can use the run command to flee from battle. | 2 | `false` |
| `champion` | Boolean | If true, the unit is a champion variant with boosted stats. | 2 | `true` |
| `force_not_familiar` | Boolean | If true, the unit cannot be used as a familiar. | 2 | `true` |
| `hint_no_corpse` | Boolean | If true, the unit does not leave a corpse when defeated. | 2 | `true` |
| `must_start_facing_camera` | Boolean | If true, the unit must be placed facing the camera at the start of a mission. | 2 | `false` |
| `tile_desire_cost` | Integer | The cost modifier for the unit's desire to move onto a tile. | 2 | `100`<br>`200` |
| `uncapturable` | Boolean | If true, the unit cannot be captured. | 2 | `false`<br>`true` |
| `aggro_target_is_enemy` | Boolean | If true, the unit's aggression target is considered an enemy. | 1 | `true` |
| `allow_flying_effect` | Boolean | If true, the unit can be affected by flying mechanics. | 1 | `true` |
| `allow_offmap_corpse` | Boolean | If true, the unit can leave a corpse if defeated off the map. | 1 | `true` |
| `allow_replacebrain` | Boolean | If true, the unit can have its brain replaced via certain abilities. | 1 | `false` |
| `always_face_forward` | Boolean | If true, the unit always faces forward regardless of direction. | 1 | `true` |
| `capture_as_cat` | Boolean | If true, the unit is captured as a cat rather than an object. | 1 | `true` |
| `elite` | Boolean | If true, the unit is an elite variant with enhanced abilities. | 1 | `true` |
| `first_turn_is_main_turn` | Boolean | If true, the unit's first turn in a round is treated as a main turn. | 1 | `true` |
| `ignore_mouseover` | Boolean | If true, the unit cannot be hovered over or selected via mouse. | 1 | `true` |
| `ignore_tiles` | Boolean | If true, the unit ignores tile-based collision and placement rules. | 1 | `true` |
| `mouseover_priority` | Integer | The priority for mouseover targeting among multiple units. | 1 | `10` |
| `move_points` | Integer | The number of move points required to use the ability. | 1 | `0`<br>`1`<br>`2` |
| `pickup_type` | Integer | Specifies the type identifier for pickup items. | 1 | `1` |
| `scale` | Float | The scale multiplier applied to the unit's visual size. | 1 | `.5`<br>`.6`<br>`.7` |
| `speculative_inanimate` | Boolean | If true, the unit is treated as an inanimate object for gameplay purposes. | 1 | `false` |
| `static` | Boolean | If true, the unit cannot move and is anchored in place. | 1 | `true` |
| `two_fronts` | Boolean | If true, the unit has a second front side for orientation. | 1 | `true` |
| `two_fronts_switch` | Boolean | If true, the unit can switch between its two front sides. | 1 | `true` |
| `view_bugs_as_enemies` | Boolean | If true, the unit treats bug-type characters as enemies. | 1 | `true` |
| [`inanimate_can_receive_specific_statuses`](./Arrays.md#array-inanimate_can_receive_specific_statuses) | Array | A list of statuses that an inanimate unit can receive. | 1 | `[Burn]` |

</details>


---


### Object: `ai`


**Definition:** A container object defining the character's artificial intelligence brain and decision weights.
**Total Count:** 583

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Alert`](./Characters_and_Bosses.md#object-alert), [`Angry`](./Characters_and_Bosses.md#object-angry), [`Attacker`](./Characters_and_Bosses.md#object-attacker), [`BellyFull`](./Characters_and_Bosses.md#object-bellyfull), [`Bishop`](./Characters_and_Bosses.md#object-bishop), [`BlackHole`](./Characters_and_Bosses.md#object-blackhole), [`Bully`](./Characters_and_Bosses.md#object-bully), [`CaveBaby`](./Characters_and_Bosses.md#object-cavebaby), [`CaveMan`](./Characters_and_Bosses.md#object-caveman), [`CaveManSpear`](./Characters_and_Bosses.md#object-cavemanspear), [`CaveWoman`](./Characters_and_Bosses.md#object-cavewoman), [`CaveWomanHasCat`](./Characters_and_Bosses.md#object-cavewomanhascat), [`Charging`](./Characters_and_Bosses.md#object-charging), [`Cultist`](./Characters_and_Bosses.md#object-cultist), [`Damaged`](./Characters_and_Bosses.md#object-damaged), [`Default`](./Characters_and_Bosses.md#object-default), [`Default_Ceiling`](./Characters_and_Bosses.md#object-default_ceiling), [`Default_Ground`](./Characters_and_Bosses.md#object-default_ground), [`DesireMech`](./Characters_and_Bosses.md#object-desiremech), [`Down`](./Characters_and_Bosses.md#object-down), and 64 more...

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum | Specifies the AI brain type used for decision-making logic. | 573 | `DicerBrain`<br>`GenericBrain`<br>`MountBrain` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 493 | `always_cast`<br>`always_cast_careless`<br>`angry` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 490 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`pattern`](./Miscellaneous.md#object-pattern) | Object  | Defines a sequence of actions the AI will execute in order, with optional priority or all-in-one. | 289 | `{ . . . }` |
| [`mainturn_pattern`](./Miscellaneous.md#object-mainturn_pattern) | Object  | Specifies the AI behavior pattern used during main turns. | 44 | `{ . . . }` |
| `end_turn_on_formswitch` | Boolean | If true, the unit's turn ends immediately after switching forms. | 39 | `false`<br>`true` |
| [`virtual_abilities`](./Miscellaneous.md#object-virtual_abilities) | Object  | Defines virtual abilities and their movement weights for AI decision-making. | 35 | `{ . . . }` |
| `auto_orient` | Boolean | If true, the unit automatically faces the nearest target. | 31 | `false` |
| `reset_pattern_on_formswitch` | Boolean | If true, the AI pattern resets when the unit switches forms. | 31 | `false`<br>`true` |
| `stun_advances_pattern` | Boolean | If true, the AI advances to the next step in its pattern when stunned. | 30 | `false`<br>`true` |
| `fallback_advances_pattern` | Boolean | If true, using the fallback action advances the AI's pattern index. | 28 | `false`<br>`true` |
| [`bonusturn_pattern`](./Miscellaneous.md#object-bonusturn_pattern) | Object  | The action sequence the AI follows during a bonus turn. | 27 | `{ . . . }` |
| [`fallback`](./Miscellaneous.md#object-fallback) | Object  | The action sequence the AI uses when its main pattern cannot execute. | 23 | `{ . . . }` |
| [`round_end_bonusturn_pattern`](./Miscellaneous.md#object-round_end_bonusturn_pattern) | Object  | The action sequence the AI executes at the end of the round as a bonus turn. | 12 | `{ . . . }` |
| `consider_spells` | Boolean | If true, the AI considers using spells in its decision-making. | 11 | `false` |
| `animate_choice` | Boolean | If true, the AI animates its decision-making process (e.g., thinking indicator). | 8 | `false`<br>`true` |
| `clamp_pattern` | Boolean | If true, the AI's pattern index is clamped to the last valid entry rather than resetting or overflowing. | 5 | `true` |
| `randomize_pattern_start` | Boolean | If true, the AI starts its pattern from a random index at the beginning of combat. | 3 | `true` |
| [`dispersed_bonusturn_pattern`](./Miscellaneous.md#object-dispersed_bonusturn_pattern) | Object  | The action sequence used when bonus turns are evenly distributed among multiple units. | 2 | `{ . . . }` |
| `random_orient` | Boolean | If true, the AI randomizes its facing direction on spawn. | 2 | `true` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| `never_hit_ally_corpses` | Boolean | If true, the AI avoids targeting or damaging ally corpses. | 1 | `true` |
| [`post_absorb_move_weights`](./Enums.md#enum-post_absorb_move_weights) | Enum | Specifies the movement weight set used after the AI absorbs a target. | 1 | `minimum_move` |
| `reset_pattern_on_round_begin` | Boolean | If true, the AI's pattern index resets to the start at the beginning of each round. | 1 | `true` |
| [`roll_ability`](./Enums.md#enum-roll_ability) | Enum | Specifies the ability name used for the AI's dice-rolling mechanic. | 1 | `RollDice` |
| [`round_start_bonusturn_pattern`](./Miscellaneous.md#object-round_start_bonusturn_pattern) | Object  | The action sequence the AI executes at the start of the round as a bonus turn. | 1 | `{ . . . }` |
| [`dice_abilities`](./Arrays.md#array-dice_abilities) | Array | The list of ability names from which the AI randomly selects when rolling dice. | 1 ||

</details>


---


### Object: `stats`


**Definition:** A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.).
**Total Count:** 497

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `strength` | Integer | The base strength stat, used for physical damage calculations. | 386 | `1`<br>`10`<br>`15` |
| `constitution` | Integer | The base constitution stat, used for health and damage mitigation. | 380 | `1`<br>`10`<br>`2` |
| `dexterity` | Integer | The base dexterity stat, used for accuracy and evasion. | 380 | `1`<br>`2`<br>`3` |
| `charisma` | Integer | The base charisma stat, used for social or mind-affecting abilities. | 379 | `1`<br>`2`<br>`3` |
| `intelligence` | Integer | The base intelligence stat, used for spell power and mana. | 379 | `0`<br>`1`<br>`10` |
| [`speed`](./Arrays.md#array-speed) | Array / Float  | The speed of the projectile or move, can be a value or a range. | 379 | `-30`<br>`-4`<br>`.5` |
| `luck` | Integer | The base luck stat, used for critical hits and random beneficial effects. | 160 | `1`<br>`10`<br>`3` |

</details>


---


### Object: `abilities`


**Definition:** A container object defining a character's move, attack, and spell abilities.
**Total Count:** 460

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 438 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 433 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`spells`](./Arrays.md#array-spells) | Array | The list of spell ability IDs the unit possesses. | 381 | `1`<br>`2`<br>`5` |
| `can_get_bonus` | Boolean | If true, the unit can gain bonus turns from abilities or effects. | 30 | `true` |

</details>


---


### Object: `pattern`


**Definition:** Defines a sequence of actions the AI will execute in order, with optional priority or all-in-one.
**Total Count:** 296

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root), [`ReplaceBrain`](./Characters_and_Bosses.md#object-replacebrain), [`ai`](./Characters_and_Bosses.md#object-ai), [`ai_if_spawned_as_enemy`](./Characters_and_Bosses.md#object-ai_if_spawned_as_enemy)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum | The single, specific ability the AI executes. | 101 | `**BombRatTurtle`<br>`**G3Shake`<br>`**RockySlam` |
| [`do_all`](./Arrays.md#array-do_all) | Array | The list of abilities the AI executes in sequence during its turn. | 91 | `[*BungaEatCat attack BungaRoar move]`<br>`[*ButtFart, Unflip]`<br>`[*DCBirthSquirrel attack DCBirthSquirrel]` |
| [`do_priority`](./Arrays.md#array-do_priority) | Array | The list of abilities the AI executes, evaluating them in order of highest priority. | 82 | `[ attack]`<br>`[**DestroyerThrowShield DestroyerHolyAttack]`<br>`[**DestroyerThrowShield attack]` |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum | The specific ability the AI executes after moving. | 11 | `CHuskCatShade`<br>`CerberubsBarrage`<br>`CerberubsCalm` |
| [`do_random`](./Arrays.md#array-do_random) | Array | The list of abilities from which the AI randomly selects one to execute. | 9 | `[**TVChangeObey **TVChangeStop **TVChangeDumb]`<br>`[AZ_BreakNeck AZ_BreakLeg AZ_BreakArm]`<br>`[CHSpawn CHCry]` |
| [`do_strict`](./Arrays.md#array-do_strict) | Array | The list of abilities the AI executes in strict sequence, without any alternative. | 4 | `[*CanCreeperSlide, MoveCenter]`<br>`[*CraterCreeperSlide, MoveCenter]`<br>`[*WizSpellShield, WizBlizzard]` |
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array | The list of actions (typically empty) the AI takes when it does nothing. | 3 | `[]` |
| [`move_then_do_random`](./Arrays.md#array-move_then_do_random) | Array | The list of abilities from which the AI randomly selects one to execute after moving. | 3 | `[CerberubsJumpBlind CerberubsJumpNormal]`<br>`[ClotEvolve ClotFailEvolve]`<br>`[ClotEvolveCatCopy ClotFailEvolve]` |
| [`move_then_do_priority`](./Arrays.md#array-move_then_do_priority) | Array | The list of abilities the AI executes after moving, in priority order. | 2 | `[BBPickupCrown, *BBToss, *attack]`<br>`[BBPickupCrown, *attack, *BBToss]`<br>`[DrinkUp attack]` |
| [`do_all_shuffle`](./Arrays.md#array-do_all_shuffle) | Array | The list of abilities the AI shuffles and then executes in the resulting random order. | 2 | `[YetiSlam YetiSlam YetiSlam`<br>`[attack DybbukWisps DybbukRePossess]` |
| [`do_best`](./Arrays.md#array-do_best) | Array | The list of abilities the AI evaluates to pick the one with the highest immediate benefit. | 1 | `[JohnnyPush JohnnyPull]` |
| [`do_best_multiple`](./Arrays.md#array-do_best_multiple) | Array | The list of abilities the AI evaluates to pick multiple beneficial ones to execute. | 1 ||
| [`do_priority_alternating`](./Arrays.md#array-do_priority_alternating) | Array | The list of abilities the AI executes in a priority order that alternates each turn. | 1 ||
| [`move_then_do_all`](./Arrays.md#array-move_then_do_all) | Array | The list of abilities the AI executes in sequence after moving. | 1 | `[LennyShove, LennyGrabDead, LennyGrab]` |

</details>


---


### Object: `Normal`


**Definition:** The normal form configuration, used as a baseline state for shape-shifting units.
**Total Count:** 231

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 10 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 5 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


---


### Object: `Angry`


**Definition:** Defines the 'Angry' form, an enraged state with its own AI.
**Total Count:** 221

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer  | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


---


### Object: `FormChanger`


**Definition:** Defines the unit's form-changing data, including multiple form definitions and their sub-properties.
**Total Count:** 106

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`initial_form`](./Enums.md#enum-initial_form) | Enum / Integer | Specifies the starting form name for a unit with FormChanger. | 56 | `0`<br>`1`<br>`5` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 2 | Default<br>FormChange<br>Druid |
| [`Default`](./Miscellaneous.md#object-default) | Enum / Object  | The default form configuration for a unit, containing its standard stats and abilities. | 37 | `{ . . . }`<br>`release` |
| [`Normal`](./Miscellaneous.md#object-normal) | Integer / Object  | The normal form configuration, used as a baseline state for shape-shifting units. | 11 | `{ . . . }`<br>`0` |
| [`Rage`](./Miscellaneous.md#object-rage) | Object  | The rage form configuration, applied when the unit enters an enraged state. | 10 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 120 | passives<br>class<br>	ag |
| [`HasCat`](./Miscellaneous.md#object-hascat) | Object  | The form configuration applied when the unit is holding or has swallowed a cat. | 5 | `{ . . . }` |
| [`default`](./Miscellaneous.md#object-default) | Enum / Object  | The default configuration or value used when no specific override is provided. | 4 | `{ . . . }`<br>`bite1` |
| [`hot`](./Miscellaneous.md#object-hot) | Object  | The form configuration applied when the unit is in a hot state, granting fire element. | 4 | `{ . . . }` |
| [`OffMap`](./Miscellaneous.md#object-offmap) | Object  | The form configuration applied when the unit is off the battlefield map. | 4 | `{ . . . }` |
| [`AllAlive`](./Miscellaneous.md#object-allalive) | Object  | The form configuration applied when all family members are alive. | 3 | `{ . . . }` |
| [`Down`](./Miscellaneous.md#object-down) | Object  | The form configuration applied when the unit is in a knocked-down or prone state. | 3 | `{ . . . }` |
| [`Full`](./Miscellaneous.md#object-full) | Object  | The form configuration applied when the unit is in a full state. | 3 | `{ . . . }` |
| [`OneAlive`](./Miscellaneous.md#object-onealive) | Object  | The form configuration applied when only one family member remains alive. | 3 | `{ . . . }` |
| [`TwoAlive`](./Miscellaneous.md#object-twoalive) | Object  | A form that activates when two specific units are alive, granting the contained passives and abilities. | 3 | `{ . . . }` |
| [`Up`](./Miscellaneous.md#object-up) | Object  | Defines the 'Up' form, including its animation, AI behavior, and passives such as UpTireBehavior. | 3 | `{ . . . }` |
| [`active`](./Miscellaneous.md#object-active) | Object  | Defines the active form, containing passives and abilities that are active while in this form. | 2 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`Big`](./Miscellaneous.md#object-big) | Object  | Defines the 'Big' form, including its animation, attack, passives, and positional data. | 2 | `{ . . . }` |
| [`Boris`](./Miscellaneous.md#object-boris) | Enum / Object  | Specifies the 'Boris' form within FormChanger, with its own animation suffix and passives. | 2 | `{ . . . }`<br>`MegaGuppy_TransformBoris` |
| [`CaveMan`](./Miscellaneous.md#object-caveman) | Object  | Defines the 'CaveMan' form of a CavePerson enemy, including its animation, attack, and passives. | 2 | `{ . . . }` |
| [`CaveManSpear`](./Miscellaneous.md#object-cavemanspear) | Object  | Defines the 'CaveManSpear' form of a CavePerson enemy, with a spear attack and corresponding animation. | 2 | `{ . . . }` |
| [`Empty`](./Miscellaneous.md#object-empty) | Object  | Defines the 'Empty' form, typically indicating a state with no content (e.g., empty stomach). | 2 | `{ . . . }` |
| [`Explosive`](./Miscellaneous.md#object-explosive) | Enum / Object  | Specifies the 'Explosive' form within FormChanger, with its own animation suffix and passives. | 2 | `{ . . . }`<br>`MegaGuppy_TransformExplosive` |
| [`Holding`](./Miscellaneous.md#object-holding) | Object  | Defines the 'Holding' form, used when the unit is holding an object, with associated movement and form change behaviors. | 2 | `{ . . . }` |
| [`Holy`](./Passives_and_Statuses.md#object-holy) | Enum / Object  | Specifies the 'Holy' form within FormChanger, with its own animation suffix and passives. | 2 | `{ . . . }`<br>`MegaGuppy_TransformHoly` |
| [`NotPriming`](./Miscellaneous.md#object-notpriming) | Object  | Defines the 'NotPriming' form, which allows the unit to take main turns and grants bonus turns. | 2 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passive`](./Miscellaneous.md#object-passive) | Object  | Defines the passive form, where the unit does nothing (uses DoNothing attack) and is inactive. | 2 | `{ . . . }` |
| [`Priming`](./Miscellaneous.md#object-priming) | Object  | Defines the 'Priming' form, where the unit does not take main turns but gains bonus turns at round end. | 2 | `{ . . . }` |
| [`Rain`](./Miscellaneous.md#object-rain) | Object  | Defines the rain weather effect with associated particle, sound, and rendering settings. | 2 | `{ . . . }` |
| [`Small`](./Miscellaneous.md#object-small) | Object  | Defines the 'Small' form, typically used for smaller size variants, with its own attack and animation. | 2 | `{ . . . }` |
| [`SquirrelForm`](./Miscellaneous.md#object-squirrelform) | Object  | Defines the 'SquirrelForm', a transformation used by units like DeathMetal, granting melee attack and speed bonuses. | 2 | `{ . . . }` |
| [`Turtled`](./Miscellaneous.md#object-turtled) | Object  | Defines the 'Turtled' form, a defensive state where the unit cannot attack or move. | 2 | `{ . . . }` |
| [`Alert`](./Miscellaneous.md#object-alert) | Object  | Defines the 'Alert' form, an alerted state with a pattern brain AI. | 1 | `{ . . . }` |
| [`Angry`](./Miscellaneous.md#object-angry) | Object  | Defines the 'Angry' form, an enraged state with its own AI. | 1 | `{ . . . }` |
| [`Attacker`](./Miscellaneous.md#object-attacker) | Object  | Defines the 'Attacker' form, focusing on offensive actions like attacking and charging. | 1 | `{ . . . }` |
| [`BellyFull`](./Miscellaneous.md#object-bellyfull) | Object  | Defines the 'BellyFull' form, used when the unit has the Consuming status, with appropriate animation. | 1 | `{ . . . }` |
| [`BigHolding`](./Miscellaneous.md#object-bigholding) | Object  | Defines the 'BigHolding' form, a larger variant while holding an object, triggered by the Consuming status. | 1 | `{ . . . }` |
| [`BigHoldingCat`](./Miscellaneous.md#object-bigholdingcat) | Object  | Defines the 'BigHoldingCat' form, a cat-sized variant of the holding form while Consuming. | 1 | `{ . . . }` |
| [`Bishop`](./Miscellaneous.md#object-bishop) | Object  | Defines the 'Bishop' form for Cultist enemies, with its own attack (BBXLightning) and animation. | 1 | `{ . . . }` |
| [`BlackHole`](./Miscellaneous.md#object-blackhole) | Object  | Defines the 'BlackHole' form, a variant of NeutronStar with its own animation and name. | 1 | `{ . . . }` |
| [`Bomb`](./Miscellaneous.md#object-bomb) | Object  | Defines the 'Bomb' form, an explosive state that triggers an ability on death. | 1 | `{ . . . }` |
| [`Bully`](./Miscellaneous.md#object-bully) | Object  | Defines the 'Bully' form, which allows the unit to take turns and enables its passives. | 1 | `{ . . . }` |
| [`Butcher`](./Engine_LogicKeys.md#object-butcher) | Object  | Specifies the 'Butcher' form within FormChanger, used for boss dialogue. | 1 | `{ . . . }` |
| [`CaveBaby`](./Miscellaneous.md#object-cavebaby) | Object  | Defines the 'CaveBaby' form of a CavePerson enemy, with reduced health and baby attack. | 1 | `{ . . . }` |
| [`CaveWoman`](./Miscellaneous.md#object-cavewoman) | Object  | Defines the 'CaveWoman' form of a CavePerson enemy, with kick attack and higher health. | 1 | `{ . . . }` |
| [`CaveWomanHasCat`](./Miscellaneous.md#object-cavewomanhascat) | Object  | Defines the 'CaveWomanHasCat' form, a variant of CaveWoman that attacks with a cat slap. | 1 | `{ . . . }` |
| [`Charging`](./Miscellaneous.md#object-charging) | Object  | Defines the 'Charging' form, a wind-up state for a powerful attack. | 1 | `{ . . . }` |
| [`Close`](./Miscellaneous.md#object-close) | Object  | Defines the 'Close' form, which triggers GSOpen ability upon reaction. | 1 | `{ . . . }` |
| [`Colorless`](./Engine_LogicKeys.md#object-colorless) | Object  | Specifies the 'Colorless' form within FormChanger, used for boss dialogue. | 1 | `{ . . . }` |
| [`Cultist`](./Miscellaneous.md#object-cultist) | Object  | Defines the 'Cultist' form, a basic melee form with its own name and tooltip. | 1 | `{ . . . }` |
| [`Damaged`](./Miscellaneous.md#object-damaged) | Object  | Defines the 'Damaged' form, an injured state with a specific AI pattern to drink and attack. | 1 | `{ . . . }` |
| [`Default_Ceiling`](./Miscellaneous.md#object-default_ceiling) | Object  | Defines the 'Default_Ceiling' form for SpiderQueen, with AI pattern to spawn spiders. | 1 | `{ . . . }` |
| [`Default_Ground`](./Miscellaneous.md#object-default_ground) | Object  | Defines the 'Default_Ground' form for SpiderQueen, with AI pattern to web and attack. | 1 | `{ . . . }` |
| [`DesireMech`](./Miscellaneous.md#object-desiremech) | Object  | Defines the 'DesireMech' form, a mech suit form with its own AI pattern. | 1 | `{ . . . }` |
| [`Die`](./Miscellaneous.md#object-die) | Integer / Object  | If set, kills the target immediately. | 1 | `{ . . . }`<br>`1`<br>`6` |
| [`Druid`](./Engine_LogicKeys.md#object-druid) | Object  | Specifies the 'Druid' form within FormChanger, used for boss dialogue. | 1 | `{ . . . }` |
| [`Drunker`](./Miscellaneous.md#object-drunker) | Object  | Defines the 'Drunker' form, a drunken state with altered animation. | 1 | `{ . . . }` |
| [`DualSword`](./Miscellaneous.md#object-dualsword) | Object  | Defines the 'DualSword' form of TheDestroyer, increasing move speed and using a dual sword attack. | 1 | `{ . . . }` |
| [`DualSword_Primed`](./Miscellaneous.md#object-dualsword_primed) | Object  | Defines the 'DualSword_Primed' form, a powered-up dual sword state with holy animation. | 1 | `{ . . . }` |
| [`Dumb`](./Miscellaneous.md#object-dumb) | Integer / Object  | Defines the 'Dumb' form, which can be either a numeric value or an object with passives that disable spells and turn off TV. | 1 | `{ . . . }`<br>`3` |
| [`Explody`](./Miscellaneous.md#object-explody) | Object  | Defines the 'Explody' form, an explosive state that uses ToxExplode attack and cannot move. | 1 | `{ . . . }` |
| [`Fighter`](./Engine_LogicKeys.md#object-fighter) | Object  | Specifies the 'Fighter' form within FormChanger, used for boss dialogue. | 1 | `{ . . . }` |
| [`FightPhase`](./Miscellaneous.md#object-fightphase) | Object  | Defines the 'FightPhase' form, a combat form with float move and shoot attack, taking turns. | 1 | `{ . . . }` |
| [`Fire`](./Passives_and_Statuses.md#object-fire) | Integer / Object  | Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack. | 1 | `{ . . . }`<br>`1` |
| [`FireFull`](./Miscellaneous.md#object-firefull) | Integer / Object  | Defines the 'FireFull' form, a fully charged fire state with its own animation and visual combo. | 1 | `{ . . . }`<br>`1` |
| [`Flop`](./Miscellaneous.md#object-flop) | Object  | Defines the initial flopped down state, using animation suffix 'Down' and a pattern AI that requires 4 wiggles to exit. | 1 | `{ . . . }` |
| [`Flop2`](./Miscellaneous.md#object-flop2) | Object  | Defines a subsequent flopped down state triggered on hit, with variable wiggles (2-6) to recover. | 1 | `{ . . . }` |
| [`Flush`](./Miscellaneous.md#object-flush) | Object  | Defines a form that executes a sequence of actions (FlushX, side switch, form switch) and has a spell with a localized name. | 1 | `{ . . . }` |
| [`FlushBubs`](./Miscellaneous.md#object-flushbubs) | Object  | Defines a form granting an immediate ability reaction for Cerberubs shotgun. | 1 | `{ . . . }` |
| [`FlushHost`](./Miscellaneous.md#object-flushhost) | Object  | Defines a host form with a partial animation suffix and a reflect projectiles passive that deals 2 self-damage. | 1 | `{ . . . }` |
| [`FlushNettle`](./Miscellaneous.md#object-flushnettle) | Object  | Defines a form that gains thorns and kinetic spikes after an enemy casts a spell. | 1 | `{ . . . }` |
| [`Grappling`](./Miscellaneous.md#object-grappling) | Object  | Defines a grappling form with a specific animation suffix and exit animations. | 1 | `{ . . . }` |
| [`Grown`](./Miscellaneous.md#object-grown) | Object  | Defines the grown form with a custom attack, name, UI floater offset, and a health weak threshold. | 1 | `{ . . . }` |
| [`GuaranteedJackpot`](./Miscellaneous.md#object-guaranteedjackpot) | Object  | Defines a form that guarantees a jackpot coin result from slot machine rolls. | 1 | `{ . . . }` |
| [`Guarding`](./Miscellaneous.md#object-guarding) | Object  | Defines a guarding form with a high brace passive. | 1 | `{ . . . }` |
| [`HalfDead`](./Miscellaneous.md#object-halfdead) | Object  | Defines the half-dead form with reduced movement and a dash attack. | 1 | `{ . . . }` |
| [`HasDeadCat`](./Miscellaneous.md#object-hasdeadcat) | Object  | Defines a form when Lenny's cat is dead, with a slap attack and conditional form change while the status is active. | 1 | `{ . . . }` |
| [`HasRock`](./Miscellaneous.md#object-hasrock) | Object  | Defines a form where the unit has a rock, with a bash attack. | 1 | `{ . . . }` |
| [`Headless`](./Miscellaneous.md#object-headless) | Object  | Defines a headless form with increased movement. | 1 | `{ . . . }` |
| [`Hint_CrackedVisuals`](./Miscellaneous.md#object-hint_crackedvisuals) | Object  | Defines a visual state with cracked animation suffix. | 1 | `{ . . . }` |
| [`Hint_CrackedVisuals2`](./Miscellaneous.md#object-hint_crackedvisuals2) | Object  | Defines a visual state with charging cracked animation. | 1 | `{ . . . }` |
| [`Hint_CrackedVisuals3`](./Miscellaneous.md#object-hint_crackedvisuals3) | Object  | Defines a visual state with swallowed cracked animation. | 1 | `{ . . . }` |
| [`HumanDead`](./Miscellaneous.md#object-humandead) | Object  | Defines a form when the human half is dead, with a spin attack and custom tooltip. | 1 | `{ . . . }` |
| [`Hunter`](./Engine_LogicKeys.md#object-hunter) | Object  | Defines a list of quotes for the Hunter class (vs boss, embark, return early). | 1 | `{ . . . }` |
| [`InitialPhase`](./Miscellaneous.md#object-initialphase) | Object  | Defines the initial phase form with a float move, shoot attack, and the ability to take turns. | 1 | `{ . . . }` |
| [`Insane_Ceiling`](./Miscellaneous.md#object-insane_ceiling) | Object  | Defines the insane ceiling form with pattern AI and animation suffix. | 1 | `{ . . . }` |
| [`Insane_Ground`](./Miscellaneous.md#object-insane_ground) | Object  | Defines the insane ground form with pattern AI and animation suffix. | 1 | `{ . . . }` |
| [`Johnny`](./Miscellaneous.md#object-johnny) | Object  | Defines a form that executes a mega blast, side switch, and form switch in sequence. | 1 | `{ . . . }` |
| [`JohnnyBubs`](./Miscellaneous.md#object-johnnybubs) | Object  | Defines a form granting an immediate ability reaction for Cerberubs shotgun. | 1 | `{ . . . }` |
| [`JohnnyHost`](./Miscellaneous.md#object-johnnyhost) | Object  | Defines a host form with a partial animation suffix and a reflect projectiles passive that deals 2 self-damage. | 1 | `{ . . . }` |
| [`JohnnyNettle`](./Miscellaneous.md#object-johnnynettle) | Object  | Defines a form that gains thorns and kinetic spikes after an enemy casts a spell. | 1 | `{ . . . }` |
| [`Joystick`](./Miscellaneous.md#object-joystick) | Object  | Defines a form with joystick animation and an immediate ability reaction (fumble even/odd). | 1 | `{ . . . }` |
| [`LastHit`](./Miscellaneous.md#object-lasthit) | Object  | Defines a form that grants 2 dispersed bonus turns after the last hit. | 1 | `{ . . . }` |
| [`Lifted`](./Miscellaneous.md#object-lifted) | Object  | Defines a lifted form with no attack or movement options. | 1 | `{ . . . }` |
| [`Lit`](./Miscellaneous.md#object-lit) | Object  | Defines a lit form that changes when wind element influence is applied. | 1 | `{ . . . }` |
| [`Mage`](./Engine_LogicKeys.md#object-mage) | Object  | Defines a list of quotes for the Mage class. | 1 | `{ . . . }` |
| [`Medic`](./Engine_LogicKeys.md#object-medic) | Object  | Defines a list of quotes for the Medic class. | 1 | `{ . . . }` |
| [`Monk`](./Engine_LogicKeys.md#object-monk) | Object  | Defines a list of quotes for the Monk class. | 1 | `{ . . . }` |
| [`Mounted`](./Miscellaneous.md#object-mounted) | Object  | Defines a mounted form with 'Cat' animation suffix. | 1 | `{ . . . }` |
| [`MouthFull`](./Miscellaneous.md#object-mouthfull) | Object  | Defines a form with mouth full animation that changes while the Consuming status is active. | 1 | `{ . . . }` |
| [`Mutant`](./Miscellaneous.md#object-mutant) | Integer / Object  | As an object, defines the mutant form with reduced move speed and custom name. As an integer, defines spawn weight. | 1 | `{ . . . }`<br>`1` |
| [`Necromancer`](./Engine_LogicKeys.md#object-necromancer) | Object  | Defines a list of quotes for the Necromancer class. | 1 | `{ . . . }` |
| [`NeutronStar`](./Miscellaneous.md#object-neutronstar) | Object  | Defines the neutron star form with custom graphics and a random pattern AI (rumble or explode). | 1 | `{ . . . }` |
| `NoDeathRattle` | Object | Defines a form that suppresses death rattle and triggers a heart attack when a buddy dies. | 1 | `{ . . . }` |
| [`NoEyes`](./Miscellaneous.md#object-noeyes) | Object  | Defines a form with no eyes animation. | 1 | `{ . . . }` |
| [`NormalFull`](./Miscellaneous.md#object-normalfull) | Integer / Object  | As an object, defines the normal full form with a spit attack and conditional form change. As an integer, specifies alt graphics index. | 1 | `{ . . . }`<br>`0` |
| [`NoStick`](./Miscellaneous.md#object-nostick) | Object  | Defines a form without a stick, using a jab attack with pattern AI. | 1 | `{ . . . }` |
| [`Nuke`](./Miscellaneous.md#object-nuke) | Object  | Defines a nuke form with no attack or movement options. | 1 | `{ . . . }` |
| [`Obey`](./Miscellaneous.md#object-obey) | Integer / Object  | As an object, defines an obey form that disables attacks and reacts with TV off. As an integer, defines a value (e.g., weight or count). | 1 | `{ . . . }`<br>`1` |
| [`Off`](./Miscellaneous.md#object-off) | Object  | Defines an off form with a 'Off' animation suffix. | 1 | `{ . . . }` |
| [`OffScreen`](./Miscellaneous.md#object-offscreen) | Object  | Defines an off-screen form that does not take turns and drops in chaos heads. | 1 | `{ . . . }` |
| [`OneEye`](./Miscellaneous.md#object-oneeye) | Object  | Defines a form with one eye that triggers an ability at 40% health threshold. | 1 | `{ . . . }` |
| [`Open`](./Miscellaneous.md#object-open) | Object  | Defines an open form with increased movement and a specific attack. | 1 | `{ . . . }` |
| [`OpenCat`](./Miscellaneous.md#object-opencat) | Object  | Defines an open cat form that changes when the Consuming status is active. | 1 | `{ . . . }` |
| [`Out`](./Miscellaneous.md#object-out) | Object  | Defines a form that is 'out' with a ground flopper movement passive. | 1 | `{ . . . }` |
| [`Possessing`](./Miscellaneous.md#object-possessing) | Object  | Form state when the unit is possessing another entity. | 1 | `{ . . . }` |
| [`Primed`](./Miscellaneous.md#object-primed) | Object  | Form state representing the unit being primed, with specific attack and AI behavior. | 1 | `{ . . . }` |
| [`Psychic`](./Engine_LogicKeys.md#object-psychic) | Object  | Form identifier for the Psychic boss type, used for dialogue references. | 1 | `{ . . . }` |
| [`Pulp2`](./Miscellaneous.md#object-pulp2) | Object  | Form state for the second stage of pulping, with no attacks or movement. | 1 | `{ . . . }` |
| [`Pulp3`](./Miscellaneous.md#object-pulp3) | Object  | Form state for the third stage of pulping, with no attacks or movement. | 1 | `{ . . . }` |
| [`Pulp4`](./Miscellaneous.md#object-pulp4) | Object  | Form state for the fourth stage of pulping, with no attacks or movement. | 1 | `{ . . . }` |
| [`Pulp5`](./Miscellaneous.md#object-pulp5) | Object  | Form state for the fifth stage of pulping, with no attacks or movement. | 1 | `{ . . . }` |
| [`Pulp6`](./Miscellaneous.md#object-pulp6) | Object  | Form state for the sixth stage of pulping, with no attacks or movement. | 1 | `{ . . . }` |
| [`Pulp7`](./Miscellaneous.md#object-pulp7) | Object  | Form state for the seventh stage of pulping, with no attacks or movement. | 1 | `{ . . . }` |
| [`Sitting`](./Miscellaneous.md#object-sitting) | Object  | Form state where the unit is sitting, with no movement or attack. | 1 | `{ . . . }` |
| [`SmallHolding`](./Miscellaneous.md#object-smallholding) | Object  | Form state when the unit is holding a small object, triggering a form change while consuming. | 1 | `{ . . . }` |
| [`SmallHoldingCat`](./Miscellaneous.md#object-smallholdingcat) | Object  | Form state when the unit is holding a cat, triggering a form change while consuming. | 1 | `{ . . . }` |
| [`SpawningPhase`](./Miscellaneous.md#object-spawningphase) | Object  | Form state for the spawning phase, where the unit is immobile and cannot take turns. | 1 | `{ . . . }` |
| [`Standing`](./Miscellaneous.md#object-standing) | Object  | Form state where the unit is standing, with default movement and attack. | 1 | `{ . . . }` |
| [`Standing2`](./Miscellaneous.md#object-standing2) | Object  | Form state where the unit is standing with a jumping movement ability. | 1 | `{ . . . }` |
| [`Start_Ceiling`](./Miscellaneous.md#object-start_ceiling) | Object  | Form state for starting on the ceiling, with a form change trigger when entering the map. | 1 | `{ . . . }` |
| [`Stop`](./Miscellaneous.md#object-stop) | Integer / Object  | If an integer, the number of turns the unit is stopped. If an object, the form configuration for the stopped state. | 1 | `{ . . . }`<br>`2` |
| [`SwordAndShield`](./Miscellaneous.md#object-swordandshield) | Object  | Form state with sword and shield, using the DestroyerAttack ability. | 1 | `{ . . . }` |
| [`SwordAndShield_Primed`](./Miscellaneous.md#object-swordandshield_primed) | Object  | Primed form state of SwordAndShield with holy animation and no final boss shield. | 1 | `{ . . . }` |
| `sync_brain_patterns` | Boolean | If true, synchronizes brain patterns across form changes. | 1 | `true` |
| [`Tank`](./Engine_LogicKeys.md#object-tank) | Object  | Form identifier for the Tank boss type, used for dialogue references. | 1 | `{ . . . }` |
| [`Tar`](./Miscellaneous.md#object-tar) | Integer / Object  | If an integer, the number of tar stacks. If an object, the form state for the tar-covered unit. | 1 | `{ . . . }`<br>`2` |
| [`TarFull`](./Miscellaneous.md#object-tarfull) | Integer / Object  | If an integer, the number of full tar stacks. If an object, the form state for the fully tar-covered unit. | 1 | `{ . . . }`<br>`2` |
| [`Thief`](./Engine_LogicKeys.md#object-thief) | Object  | Form identifier for the Thief boss type. | 1 | `{ . . . }` |
| [`Throb`](./Miscellaneous.md#object-throb) | Object  | Form state for the Chaos unit's throb behavior, with a spread pattern. | 1 | `{ . . . }` |
| [`ThrobBubs`](./Miscellaneous.md#object-throbbubs) | Object  | Form state for Chaos unit throb that reacts with a shotgun attack. | 1 | `{ . . . }` |
| [`ThrobHost`](./Miscellaneous.md#object-throbhost) | Object  | Form state for Chaos unit acting as host, reflecting projectiles. | 1 | `{ . . . }` |
| [`ThrobNettle`](./Miscellaneous.md#object-throbnettle) | Object  | Form state for Chaos unit with thorns and kinetic spikes that stack after enemy spells. | 1 | `{ . . . }` |
| [`Tinkerer`](./Engine_LogicKeys.md#object-tinkerer) | Object  | Form identifier for the Tinkerer boss type. | 1 | `{ . . . }` |
| [`Transformed`](./Miscellaneous.md#object-transformed) | Object  | Form state after transformation, ending the turn on form switch. | 1 | `{ . . . }` |
| [`TwoEyes`](./Miscellaneous.md#object-twoeyes) | Object  | Form state with two eyes, triggering ability at a health threshold. | 1 | `{ . . . }` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`Unlit`](./Miscellaneous.md#object-unlit) | Object  | Form state for an unlit candle, muting demonic glyph display. | 1 | `{ . . . }` |
| `Unmounted` | Object | Form state when the unit is unmounted from its mech suit, with no additional properties. | 1 | `{ . . . }` |
| [`Unwashed`](./Miscellaneous.md#object-unwashed) | Object  | Form state for the unwashed version of Johnny, with its own AI pattern. | 1 | `{ . . . }` |
| [`Washed`](./Miscellaneous.md#object-washed) | Object  | Form state for the washed version of Johnny, with a blast attack. | 1 | `{ . . . }` |
| [`Washer`](./Miscellaneous.md#object-washer) | Object  | Form state for the washer variant of a cultist, with basic melee attack. | 1 | `{ . . . }` |
| [`Water`](./Passives_and_Statuses.md#object-water) | Object  | Form state for water element, applying a puddle or movement bonus. | 1 | `{ . . . }` |
| [`WereMan`](./Miscellaneous.md#object-wereman) | Object  | Form state for the were-man transformation, with fury swipe attack and sabertooth faction. | 1 | `{ . . . }` |
| [`Zealot`](./Miscellaneous.md#object-zealot) | Object  | Form state for the zealot variant of a cultist, with a stabbing attack. | 1 | `{ . . . }` |
| [`ZealotBomb`](./Miscellaneous.md#object-zealotbomb) | Object  | Form state for the bomb zealot variant, with an explosion attack. | 1 | `{ . . . }` |

</details>


---


### Object: `SpawnOnDeath`


**Definition:** Specifies an object and its faction to spawn when the unit dies.
**Total Count:** 79

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 4 | `allies`<br>`auto`<br>`birds` |
| [`obj`](./Arrays.md#array-obj) | Array / Enum | Specifies one or more object names to bounce towards the target. | 4 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |
| [`additional_statuses`](./Miscellaneous.md#object-additional_statuses) | Object  | Additional status effects applied to the spawned unit on death. | 1 | `{ . . . }` |

</details>


---


### Object: `sound`


**Definition:** A container object defining audio configurations, including alternate sound lists.
**Total Count:** 62

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_sounds`](./Arrays.md#array-alt_sounds) | Array | Array of alternate sound pairs for specific audio events. | 61 | `[`<br>`[[DamageBlocked DamageBlocked_CanCreeper]]`<br>`[[HitGround Bomb_Land]]` |
| [`animation_prefix`](./Enums.md#enum-animation_prefix) | Enum | Prefix used for the unit's animation sounds. | 1 | `RattleSnake` |

</details>


---


### Object: `Robot`


**Definition:** If an integer 1, the unit is robotic and affected by electric/energized effects. If an object, contains further robot-specific properties.
**Total Count:** 46

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alternate_energized_effect`](./Miscellaneous.md#object-alternate_energized_effect) | Object  | Effects applied when the robot becomes energized, such as form changes or stat boosts. | 2 | `{ . . . }` |

</details>


---


### Object: `turns`


**Definition:** Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`.
**Total Count:** 45

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Bishop`](./Characters_and_Bosses.md#object-bishop), [`Bully`](./Characters_and_Bosses.md#object-bully), [`Default`](./Characters_and_Bosses.md#object-default), [`Default_Ceiling`](./Characters_and_Bosses.md#object-default_ceiling), [`Default_Ground`](./Characters_and_Bosses.md#object-default_ground), [`FightPhase`](./Characters_and_Bosses.md#object-fightphase), [`Holding`](./Characters_and_Bosses.md#object-holding), [`InitialPhase`](./Characters_and_Bosses.md#object-initialphase), [`Insane_Ceiling`](./Characters_and_Bosses.md#object-insane_ceiling), [`Insane_Ground`](./Characters_and_Bosses.md#object-insane_ground), [`LastHit`](./Characters_and_Bosses.md#object-lasthit), [`Lifted`](./Characters_and_Bosses.md#object-lifted), [`Mutant`](./Characters_and_Bosses.md#object-mutant), [`Normal`](./Characters_and_Bosses.md#object-normal), [`NotPriming`](./Characters_and_Bosses.md#object-notpriming), [`Nuke`](./Characters_and_Bosses.md#object-nuke), [`OffMap`](./Characters_and_Bosses.md#object-offmap), [`OffScreen`](./Characters_and_Bosses.md#object-offscreen), [`OneAlive`](./Characters_and_Bosses.md#object-onealive), [`Possessing`](./Characters_and_Bosses.md#object-possessing), and 13 more...

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `takes_turns` | Boolean | If true, the unit participates in the turn order. | 23 | `false`<br>`true` |
| `dispersed_bonus_turns` | Integer | The number of bonus turns granted to this unit when its turn order is dispersed. | 18 | `0`<br>`1`<br>`2` |
| `takes_main_turn` | Boolean | If true, the unit consumes the main turn phase of the round. | 10 | `false`<br>`true` |
| `evenly_dispersed_bonus_turns` | Integer | The number of bonus turns spread evenly across the turn order for this unit. | 7 | `1`<br>`2`<br>`3` |
| `round_end_bonus_turns` | Integer | The number of bonus turns granted at the end of each round. | 5 | `1` |
| `wait_till_next_round_to_update_turns` | Boolean | If true, delays turn count updates until the next round. | 4 | `true` |
| `round_start_bonus_turns` | Integer | The number of extra turns the unit gains at the start of each round. | 1 | `1` |

</details>


---


### Object: `equipment`


**Definition:** A container object defining the character's equipped items (head, face, neck, weapon, etc.).
**Total Count:** 44

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`face`](./Enums.md#enum-face) | Enum | The face equipment item assigned to the unit. | 16 | `1004`<br>`1019`<br>`AtomicMark` |
| [`head`](./Enums.md#enum-head) | Enum / Float | The catalog ID for the cat's head part. | 14 | `-1`<br>`1`<br>`1.3` |
| [`neck`](./Enums.md#enum-neck) | Enum | The neck equipment item assigned to the unit. | 10 | `AngelicAura`<br>`AngelicAura_Terminator`<br>`DruidNeck` |
| [`weapon`](./Enums.md#enum-weapon) | Enum | The name of the weapon item the unit starts with. | 7 | `AstroTaser`<br>`ButcherHook`<br>`CaveCatClub` |

</details>


---


### Object: `mainturn_pattern`


**Definition:** Specifies the AI behavior pattern used during main turns.
**Total Count:** 44

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum | The single, specific ability the AI executes. | 23 | `**BombRatTurtle`<br>`**G3Shake`<br>`**RockySlam` |
| [`do_all`](./Arrays.md#array-do_all) | Array | The list of abilities the AI executes in sequence during its turn. | 9 | `[*BungaEatCat attack BungaRoar move]`<br>`[*ButtFart, Unflip]`<br>`[*DCBirthSquirrel attack DCBirthSquirrel]` |
| [`do_priority`](./Arrays.md#array-do_priority) | Array | The list of abilities the AI executes, evaluating them in order of highest priority. | 8 | `[ attack]`<br>`[**DestroyerThrowShield DestroyerHolyAttack]`<br>`[**DestroyerThrowShield attack]` |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum | The specific ability the AI executes after moving. | 2 | `CHuskCatShade`<br>`CerberubsBarrage`<br>`CerberubsCalm` |
| [`do_strict`](./Arrays.md#array-do_strict) | Array | The list of abilities the AI executes in strict sequence, without any alternative. | 2 | `[*CanCreeperSlide, MoveCenter]`<br>`[*CraterCreeperSlide, MoveCenter]`<br>`[*WizSpellShield, WizBlizzard]` |

</details>


---


### Object: `Default`


**Definition:** The default form configuration for a unit, containing its standard stats and abilities.
**Total Count:** 38

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 9 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 24 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 10 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer  | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


---


### Object: `FormChangeWhileHasStatus`


**Definition:** Defines a form change condition that activates while the unit has a specific status effect.
**Total Count:** 35

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 35 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`form_hasnot`](./Enums.md#enum-form_hasnot) | Enum | Specifies a form that the unit must not be in for the status-triggered form change to occur. | 30 | `Big`<br>`CaveWoman`<br>`Close` |
| [`form_has`](./Enums.md#enum-form_has) | Enum | Specifies a form that the unit must be in for the status-triggered form change to occur. | 25 | `BellyFull`<br>`CaveWomanHasCat`<br>`FireFull` |

</details>


---


### Object: `keyword_tooltips`


**Definition:** Associates keyword tooltips with the ability, often used for status effects.
**Total Count:** 35

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Die`](./Characters_and_Bosses.md#object-die), [`Dumb`](./Characters_and_Bosses.md#object-dumb), [`Obey`](./Characters_and_Bosses.md#object-obey), [`Stop`](./Characters_and_Bosses.md#object-stop)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TVBotDie` | Integer | Keyword tooltip definition for the TVBot's death behavior, with name, tooltip, and icon. | 1 ||
| `TVBotDumb` | Integer | Defines the keyword tooltip for the TVBotDumb status or ability. | 1 ||
| `TVBotObey` | Integer | Defines the keyword tooltip for the TVBotObey status or ability. | 1 ||
| `TVBotStop` | Integer | Defines the keyword tooltip for the TVBotStop status or ability. | 1 ||

</details>


---


### Object: `virtual_abilities`


**Definition:** Defines virtual abilities and their movement weights for AI decision-making.
**Total Count:** 35

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`MoveAway`](./Miscellaneous.md#object-moveaway) | Object  | Defines an AI virtual ability that moves the unit away from its current target using the specified ability and move weights. | 4 | `{ . . . }` |
| [`MoveClose`](./Miscellaneous.md#object-moveclose) | Object  | Defines an AI virtual ability that moves the unit close to its target using the specified ability and move weights. | 4 | `{ . . . }` |
| [`DashRandomly`](./Miscellaneous.md#object-dashrandomly) | Object  | Defines an AI virtual ability that causes the unit to dash in a random direction using the specified ability and decision weights. | 2 | `{ . . . }` |
| [`Escape`](./Miscellaneous.md#object-escape) | Object  | Defines an AI virtual ability that causes the unit to escape using the specified ability and move weights. | 2 | `{ . . . }` |
| [`MoveCenter`](./Miscellaneous.md#object-movecenter) | Object  | Defines an AI virtual ability that moves the unit toward the center of the map using the specified ability and move weights. | 2 | `{ . . . }` |
| [`MoveForThrow`](./Miscellaneous.md#object-moveforthrow) | Object  | Defines an AI virtual ability that moves the unit into position for a throw ability. | 2 | `{ . . . }` |
| [`SpearRun`](./Miscellaneous.md#object-spearrun) | Object  | Defines an AI virtual ability that moves the unit to run with a spear and pick it up. | 2 | `{ . . . }` |
| [`CerberubsJumpBlind`](./Miscellaneous.md#object-cerberubsjumpblind) | Object  | Defines an AI virtual ability that makes Cerberubs jump with blind decision weights. | 1 | `{ . . . }` |
| [`CerberubsJumpNormal`](./Miscellaneous.md#object-cerberubsjumpnormal) | Object  | Defines an AI virtual ability that makes Cerberubs jump with default decision weights. | 1 | `{ . . . }` |
| [`CloseConvert`](./Miscellaneous.md#object-closeconvert) | Object  | Defines an AI virtual ability that moves close and uses the MarshmallowConvert ability. | 1 | `{ . . . }` |
| [`FoodMove`](./Miscellaneous.md#object-foodmove) | Object  | Defines an AI virtual ability that moves the unit toward food using the CaveBabyFoodMove ability. | 1 | `{ . . . }` |
| [`ForceTrample`](./Miscellaneous.md#object-forcetrample) | Object  | Defines an AI virtual ability that forces the unit to trample carelessly using the BirthwortTrample ability. | 1 | `{ . . . }` |
| [`LeapClose`](./Miscellaneous.md#object-leapclose) | Object  | Defines an AI virtual ability that makes the unit leap toward its aggro target. | 1 | `{ . . . }` |
| [`MoveForBarrage`](./Miscellaneous.md#object-moveforbarrage) | Object  | Defines an AI virtual ability that moves the unit to a position suitable for a barrage ability. | 1 | `{ . . . }` |
| [`MoveForDash`](./Miscellaneous.md#object-movefordash) | Object  | Defines an AI virtual ability that moves the unit into position for a dash attack. | 1 | `{ . . . }` |
| [`MoveForGrass`](./Miscellaneous.md#object-moveforgrass) | Object  | Defines an AI virtual ability that moves the unit to stomp and eat grass. | 1 | `{ . . . }` |
| [`MoveForPounce`](./Miscellaneous.md#object-moveforpounce) | Object  | Defines an AI virtual ability that moves the unit into position for a pounce attack. | 1 | `{ . . . }` |
| [`MoveForSpin`](./Miscellaneous.md#object-moveforspin) | Object  | Defines an AI virtual ability that moves the unit to set up a spin throw. | 1 | `{ . . . }` |
| [`MoveOneForPuke`](./Miscellaneous.md#object-moveoneforpuke) | Object  | Defines an AI virtual ability that moves the unit one step for a puke ability. | 1 | `{ . . . }` |
| [`MoveSpaced`](./Miscellaneous.md#object-movespaced) | Object  | Defines an AI virtual ability that moves the unit while maintaining a specific distance. | 1 | `{ . . . }` |
| [`MoveToHead`](./Miscellaneous.md#object-movetohead) | Object  | Defines an AI virtual ability that moves the unit to the head of a target to grab it. | 1 | `{ . . . }` |
| [`MoveTowards`](./Miscellaneous.md#object-movetowards) | Object  | Defines an AI virtual ability that moves the unit toward its target. | 1 | `{ . . . }` |
| [`NCGravecrawlFAR`](./Miscellaneous.md#object-ncgravecrawlfar) | Object  | Defines an AI virtual ability that makes a NecroCat gravecrawl while staying far from enemies. | 1 | `{ . . . }` |
| [`ReturnA`](./Miscellaneous.md#object-returna) | Object  | Defines an AI virtual ability that makes a HangerBot return to a close position. | 1 | `{ . . . }` |
| [`RunFar`](./Miscellaneous.md#object-runfar) | Object  | Defines an AI virtual ability that makes the unit run far away. | 1 | `{ . . . }` |
| [`SuckMF`](./Miscellaneous.md#object-suckmf) | Object  | Defines an AI virtual ability that makes a Tormentor suck enemies carelessly while keeping distance. | 1 | `{ . . . }` |
| [`TF_TargetAllies`](./Miscellaneous.md#object-tf_targetallies) | Object  | Defines an AI virtual ability that casts Twisting Flames targeting allies. | 1 | `{ . . . }` |
| [`TF_TargetEnemies`](./Miscellaneous.md#object-tf_targetenemies) | Object  | Defines an AI virtual ability that casts Twisting Flames targeting enemies. | 1 | `{ . . . }` |
| [`Unflip`](./Miscellaneous.md#object-unflip) | Object  | Defines an AI virtual ability that teleports the unit to flip up and spin an enemy. | 1 | `{ . . . }` |

</details>


---


### Object: `AddStatusToBasicAttack`


**Definition:** Contains status effects to add to the basic attack.
**Total Count:** 32

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#object-randompassivepool), [`StacyMutant_Counter`](./Characters_and_Bosses.md#object-stacymutant_counter), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 121 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 56 | `Default`<br>`FormChange`<br>`Druid` | `Bleed` | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 45 | Default<br>FormChange<br>Druid |
| `Poison` | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 29 | `1`<br>`10`<br>`2` |
| `Knockback` | Equation | The number of tiles the target is pushed away from the source on hit. | 24 | `1`<br>`10`<br>`2` |
| `Burn` | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 16 | `1`<br>`10`<br>`2` |
| `Fear` | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 13 | `1`<br>`10`<br>`2` |
| `Bruise` | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 12 | `1`<br>`2`<br>`3` |
| `Slow` | Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 10 | `-1`<br>`1`<br>`2` |
| `Stun` | Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`2`<br>`3` |
| `Confusion` | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 7 | `1`<br>`10`<br>`2` |
| `Weakness` | Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 7 | `1`<br>`2`<br>`3` |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 5 | `1`<br>`2` |
| `Rot` | Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 5 | `-999999`<br>`1`<br>`2` |
| `Madness` | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 3 | `1`<br>`2`<br>`3` |
| `RemoteLeech` | Integer | The amount of remote leech applied to the target on basic attack. | 2 | `1` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`GainDisorderFromPool`](./Miscellaneous.md#object-gaindisorderfrompool) | Object  | Specifies a pool of disorders from which one is randomly gained on basic attack, with an optional chance. | 1 | `{ . . . }` |
| `Possessed` | Integer | The number of possession stacks applied, or a template with name and tooltips. | 1 | `1` |
| `RandomStatUp` | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `RemoteFlatLeech` | Integer | The flat amount of remote leech applied to the target on basic attack. | 1 | `1` |

</details>


---


### Object: `DeathRattle`


**Definition:** Specifies an ability or effect triggered when the unit dies, optionally with a pop_corpse flag.
**Total Count:** 29

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 13 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `pop_corpse` | Boolean | If true, the corpse is destroyed instead of left behind on death. | 11 | `false` |
| `is_dying_animation` | Boolean | If true, the unit plays its dying animation before the death rattle effect. | 7 | `true` |
| `cancel_knockback` | Boolean | If true, knockback from the triggering event is negated. | 1 | `true` |
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 1 | `false`<br>`true` |
| `must_target_killer` | Boolean | If true, the death rattle effect must target the unit that killed it. | 1 | `true` |
| `target_killer` | Boolean | If true, the death rattle effect targets the killer. | 1 | `true` |

</details>


---


### Object: `bonusturn_pattern`


**Definition:** The action sequence the AI follows during a bonus turn.
**Total Count:** 27

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum | The single, specific ability the AI executes. | 15 | `**BombRatTurtle`<br>`**G3Shake`<br>`**RockySlam` |
| [`do_priority`](./Arrays.md#array-do_priority) | Array | The list of abilities the AI executes, evaluating them in order of highest priority. | 4 | `[ attack]`<br>`[**DestroyerThrowShield DestroyerHolyAttack]`<br>`[**DestroyerThrowShield attack]` |
| [`do_all`](./Arrays.md#array-do_all) | Array | The list of abilities the AI executes in sequence during its turn. | 4 | `[*BungaEatCat attack BungaRoar move]`<br>`[*ButtFart, Unflip]`<br>`[*DCBirthSquirrel attack DCBirthSquirrel]` |
| [`do_strict`](./Arrays.md#array-do_strict) | Array | The list of abilities the AI executes in strict sequence, without any alternative. | 3 | `[*CanCreeperSlide, MoveCenter]`<br>`[*CraterCreeperSlide, MoveCenter]`<br>`[*WizSpellShield, WizBlizzard]` |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum | The specific ability the AI executes after moving. | 1 | `CHuskCatShade`<br>`CerberubsBarrage`<br>`CerberubsCalm` |

</details>


---


### Object: `CatPartsTransform`


**Definition:** Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs.
**Total Count:** 25

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveGroup`](./Characters_and_Bosses.md#object-passivegroup), [`StacyMutant_Brace`](./Characters_and_Bosses.md#object-stacymutant_brace), [`StacyMutant_Counter`](./Characters_and_Bosses.md#object-stacymutant_counter), [`StacyMutant_Damage`](./Characters_and_Bosses.md#object-stacymutant_damage), [`StacyMutant_DoubleHead`](./Characters_and_Bosses.md#object-stacymutant_doublehead), [`StacyMutant_Fire`](./Characters_and_Bosses.md#object-stacymutant_fire), [`StacyMutant_Health`](./Characters_and_Bosses.md#object-stacymutant_health), [`StacyMutant_Holy`](./Characters_and_Bosses.md#object-stacymutant_holy), [`StacyMutant_Ice`](./Characters_and_Bosses.md#object-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#object-stacymutant_lightning), [`StacyMutant_Mirror`](./Characters_and_Bosses.md#object-stacymutant_mirror), [`StacyMutant_Speed`](./Characters_and_Bosses.md#object-stacymutant_speed), [`StacyMutant_Thorns`](./Characters_and_Bosses.md#object-stacymutant_thorns), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`palette`](./Enums.md#enum-palette) | Enum / Integer | Specifies the color palette index for the ability's visuals. | 17 | `-1`<br>`0`<br>`1` |
| `ear1` | Integer | The catalog ID for the cat's first ear part. | 13 | `-2`<br>`1005`<br>`1013` |
| `tail` | Integer | The catalog ID for the cat's tail part. | 13 | `-1`<br>`1000`<br>`1001` |
| `arm2` | Number | The catalog ID for the cat's second arm part. | 11 | `-1`<br>`-2`<br>`1` |
| `arm1` | Number | The catalog ID for the cat's first arm part. | 10 | `-1`<br>`-2`<br>`1` |
| `ear2` | Integer | The catalog ID for the cat's second ear part. | 10 | `1005`<br>`1013`<br>`1036` |
| `leg1` | Integer | The catalog ID for the cat's first leg part. | 8 | `-1`<br>`-2`<br>`1` |
| `leg2` | Integer | The catalog ID for the cat's second leg part. | 8 | `-1`<br>`1`<br>`10` |
| [`head`](./Enums.md#enum-head) | Enum / Float  | The catalog ID for the cat's head part. | 6 | `-1`<br>`1`<br>`1.3` |
| `texture` | Integer | The catalog ID for the cat's texture. | 6 | `-1`<br>`1`<br>`1000` |
| `body` | Float | The catalog ID for the cat's body part. | 5 | `-1`<br>`1`<br>`1.1` |
| `eye1` | Integer | The catalog ID for the cat's first eye part. | 3 | `-1`<br>`-2`<br>`1013` |
| `eye2` | Integer | The catalog ID for the cat's second eye part. | 3 | `-1`<br>`1013`<br>`1057` |

</details>


---


### Object: `fallback`


**Definition:** The action sequence the AI uses when its main pattern cannot execute.
**Total Count:** 23

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum | The single, specific ability the AI executes. | 12 | `**BombRatTurtle`<br>`**G3Shake`<br>`**RockySlam` |
| [`do_priority`](./Arrays.md#array-do_priority) | Array | The list of abilities the AI executes, evaluating them in order of highest priority. | 6 | `[ attack]`<br>`[**DestroyerThrowShield DestroyerHolyAttack]`<br>`[**DestroyerThrowShield attack]` |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum | The specific ability the AI executes after moving. | 1 | `CHuskCatShade`<br>`CerberubsBarrage`<br>`CerberubsCalm` |
| [`do_all`](./Arrays.md#array-do_all) | Array | The list of abilities the AI executes in sequence during its turn. | 1 | `[*BungaEatCat attack BungaRoar move]`<br>`[*ButtFart, Unflip]`<br>`[*DCBirthSquirrel attack DCBirthSquirrel]` |
| [`do_best`](./Arrays.md#array-do_best) | Array | The list of abilities the AI evaluates to pick the one with the highest immediate benefit. | 1 | `[JohnnyPush JohnnyPull]` |
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array | The list of actions (typically empty) the AI takes when it does nothing. | 1 | `[]` |
| [`do_random`](./Arrays.md#array-do_random) | Array | The list of abilities from which the AI randomly selects one to execute. | 1 | `[**TVChangeObey **TVChangeStop **TVChangeDumb]`<br>`[AZ_BreakNeck AZ_BreakLeg AZ_BreakArm]`<br>`[CHSpawn CHCry]` |

</details>


---


### Object: `BossRewards`


**Definition:** Defines the common and rare item rewards dropped by a boss on defeat.
**Total Count:** 20

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `common` | `String` | Defines the common reward block for a boss encounter. | 20 | `100`<br>`14`<br>`5` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 20 | `common`<br>`rare`<br>`cha` |
| `rare` | `String` | Defines the rare reward block for a boss encounter. | 16 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `AbilityReaction`


**Definition:** Specifies the ability used as a reaction when the unit is targeted by an ability.
**Total Count:** 19

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 10 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 7 | `true` |
| `backstabs_only` | Boolean | If true, the reaction only triggers on backstab damage. | 3 | `true` |
| `only_when_not_your_turn` | Boolean | If true, the reaction only triggers when it is not the unit's turn. | 3 | `true` |
| `cancel_knockback` | Boolean | If true, knockback from the triggering event is negated. | 1 | `true` |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 1 | `false`<br>`true` |
| `even_on_0_damage` | Boolean | If true, the reaction triggers even when the damage dealt is zero. | 1 | `true` |
| `even_on_0_damage_if_knockback` | Boolean | If true, the reaction triggers on zero damage if knockback occurs. | 1 | `true` |
| `match_knockback_direction` | Boolean | If true, the reaction's knockback direction matches the triggering knockback direction. | 1 | `true` |
| `ranged_only` | Boolean | If true, the reaction only triggers on ranged attacks. | 1 | `true` |
| `verify_target` | Boolean | If true, the reaction verifies that the target is valid before triggering. | 1 | `true` |

</details>


---


### Object: `MeleeRevengeDamage`


**Definition:** Defines the damage and effects applied back to a melee attacker upon being hit.
**Total Count:** 19

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#object-temppassiveuntilsettled), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 36 | `damage_instance`<br>`spell`<br>`false` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 47 | `{ . . . }` |
| [`knockback`](./Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 24 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 22 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 10 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 10 | `[`<br>`[Heat Fire]` |
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target regardless of accuracy or evasion. | 1 | `true` |

</details>


---


### Object: `ally_rewards`


**Definition:** Defines the rewards granted to the ally when the BirdRewards passive triggers.
**Total Count:** 18

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BirdRewards`](./Characters_and_Bosses.md#object-birdrewards)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 18 | passives<br>class<br>	ag |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 16 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 2 | `{ . . . }` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |`damage_instance`<br>`spell`<br>`self_damage`

</details>


---


### Object: `alt_spawn_pool`


**Definition:** An alternative spawn pool defining possible objects to spawn with their weights.
**Total Count:** 18

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Antidote` | Float | The multiplier for the number of antidote pickups spawned. | 5 | `.5`<br>`1` |
| `Blessing` | Float | The multiplier for the number of blessing pickups spawned. | 5 | `.5`<br>`1` |
| [`BigCatnip`](./Engine_LogicKeys.md#object-bigcatnip) | Integer / Object  | The number of big catnip pickups spawned. | 4 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`BiggestFood`](./Engine_LogicKeys.md#object-biggestfood) | Integer / Object  | The number of biggest food pickups spawned. | 4 | `{ . . . }`<br>`1`<br>`15`<br>`4` |
| [`BigScrap`](./Engine_LogicKeys.md#object-bigscrap) | Float / Object  | The amount of big scrap pickups spawned. | 4 | `{ . . . }`<br>`1`<br>`2`<br>`4.5` |
| [`Coin`](./Engine_LogicKeys.md#object-coin) | Integer / Object  | The number of coin pickups spawned. | 4 | `{ . . . }`<br>`1`<br>`70` |
| [`BigFood`](./Engine_LogicKeys.md#object-bigfood) | Integer / Object  | The number of big food pickups spawned. | 2 | `{ . . . }`<br>`20`<br>`5` |
| `Coin10` | Float | The multiplier for the number of Coin10 pickups spawned. | 2 | `.1`<br>`1` |
| [`Coin3`](./Engine_LogicKeys.md#object-coin3) | Integer / Object  | The number of Coin3 pickups spawned. | 2 | `{ . . . }`<br>`1` |
| [`Coin4`](./Engine_LogicKeys.md#object-coin4) | Integer / Object  | The number of Coin4 pickups spawned. | 2 | `{ . . . }`<br>`1` |
| [`MedCatnip`](./Engine_LogicKeys.md#object-medcatnip) | Integer / Object  | The number of medium catnip pickups spawned. | 2 | `{ . . . }`<br>`20`<br>`5` |
| [`MedScrap`](./Engine_LogicKeys.md#object-medscrap) | Integer / Object  | The number of medium scrap pickups spawned. | 2 | `{ . . . }`<br>`20`<br>`5` |
| [`RandomArmorPickup`](./Engine_LogicKeys.md#object-randomarmorpickup) | Float / Object  | The amount of random armor pickups spawned. | 2 | `{ . . . }`<br>`4.5`<br>`40` |
| [`RandomCatnipPickup`](./Engine_LogicKeys.md#object-randomcatnippickup) | Integer / Object  | The number of random catnip pickups spawned. | 2 | `{ . . . }`<br>`10`<br>`30` |
| [`RandomFoodPickup`](./Engine_LogicKeys.md#object-randomfoodpickup) | Integer / Object  | The number of random food pickups spawned. | 2 | `{ . . . }`<br>`15`<br>`40` |
| [`Bear`](./Engine_LogicKeys.md#object-bear) | Integer / Object  | The number of bear familiars spawned. | 1 | `{ . . . }`<br>`1` |
| [`BlackBird`](./Engine_LogicKeys.md#object-blackbird) | Integer / Object  | The number of black birds spawned. | 1 | `{ . . . }`<br>`3000` |
| [`Catepillar`](./Engine_LogicKeys.md#object-catepillar) | Integer / Object  | The number of caterpillar familiars spawned. | 1 | `{ . . . }`<br>`10` |
| [`Catnip`](./Engine_LogicKeys.md#object-catnip) | Integer / Object  | The number of catnip pickups spawned. | 1 | `{ . . . }`<br>`20`<br>`3` |
| [`CharmedDip`](./Engine_LogicKeys.md#object-charmeddip) | Integer / Object  | The number of charmed dip pickups spawned. | 1 | `{ . . . }`<br>`1` |
| [`CharmedFloater`](./Engine_LogicKeys.md#object-charmedfloater) | Integer / Object  | The number of charmed floater pickups spawned. | 1 | `{ . . . }`<br>`1` |
| [`CharmedPile`](./Engine_LogicKeys.md#object-charmedpile) | Integer / Object  | The number of charmed pile pickups spawned. | 1 | `{ . . . }`<br>`1` |
| [`Cherub`](./Engine_LogicKeys.md#object-cherub) | Integer / Object  | The number of cherubs spawned. | 1 | `{ . . . }`<br>`1` |
| [`Chicken`](./Engine_LogicKeys.md#object-chicken) | Integer / Object  | The number of chicken pickups spawned. | 1 | `{ . . . }`<br>`.01`<br>`.1`<br>`2` |
| [`Coin2`](./Engine_LogicKeys.md#object-coin2) | Integer / Object  | The number of Coin2 pickups spawned. | 1 | `{ . . . }`<br>`1` |
| [`Dove`](./Engine_LogicKeys.md#object-dove) | Integer / Object  | The number of doves spawned. | 1 | `{ . . . }`<br>`1000` |
| [`Eagle`](./Engine_LogicKeys.md#object-eagle) | Integer / Object  | The number of eagles spawned. | 1 | `{ . . . }`<br>`300` |
| [`Food`](./Shops.md#object-food) | Integer / Object  | The number of food pickups spawned. | 1 | `{ . . . }`<br>`20` |
| [`Harpy`](./Engine_LogicKeys.md#object-harpy) | Integer / Object  | The number of harpies spawned. | 1 | `{ . . . }`<br>`1` |
| [`HummingBird`](./Engine_LogicKeys.md#object-hummingbird) | Integer / Object  | The number of hummingbirds spawned. | 1 | `{ . . . }`<br>`300` |
| [`LargeBirdPool`](./Engine_LogicKeys.md#object-largebirdpool) | Integer / Object  | The weight for spawning from the large bird pool. | 1 | `{ . . . }`<br>`1` |
| [`MedBirdPool`](./Engine_LogicKeys.md#object-medbirdpool) | Integer / Object  | The weight for spawning from the medium bird pool. | 1 | `{ . . . }`<br>`1` |
| [`Mutant`](./Miscellaneous.md#object-mutant) | Integer / Object  | As an object, defines the mutant form with reduced move speed and custom name. As an integer, defines spawn weight. | 1 | `{ . . . }`<br>`1` |
| [`Pigeon`](./Engine_LogicKeys.md#object-pigeon) | Integer / Object  | The number of pigeons spawned. | 1 | `{ . . . }`<br>`3000` |
| [`RandomBiggerArmorPickup`](./Engine_LogicKeys.md#object-randombiggerarmorpickup) | Float / Object  | The amount of bigger random armor pickups spawned. | 1 | `{ . . . }`<br>`4.5` |
| [`RandomBiggerCatnipPickup`](./Engine_LogicKeys.md#object-randombiggercatnippickup) | Integer / Object  | The number of bigger random catnip pickups spawned. | 1 | `{ . . . }`<br>`10` |
| [`RandomBiggerFoodPickup`](./Engine_LogicKeys.md#object-randombiggerfoodpickup) | Integer / Object  | The number of bigger random food pickups spawned. | 1 | `{ . . . }`<br>`15` |
| [`Raven`](./Engine_LogicKeys.md#object-raven) | Integer / Object  | The number of ravens spawned. | 1 | `{ . . . }`<br>`300` |
| [`Scrap`](./Engine_LogicKeys.md#object-scrap) | Integer / Object  | The number of scrap pickups spawned. | 1 | `{ . . . }`<br>`20` |
| [`Seagull`](./Engine_LogicKeys.md#object-seagull) | Integer / Object  | The number of seagulls spawned. | 1 | `{ . . . }`<br>`1000` |
| [`SmallBirdPool`](./Engine_LogicKeys.md#object-smallbirdpool) | Integer / Object  | The weight for spawning from the small bird pool. | 1 | `{ . . . }`<br>`1` |
| [`Snake`](./Engine_LogicKeys.md#object-snake) | Integer / Object  | The number of snake familiars spawned. | 1 | `{ . . . }`<br>`10` |
| [`Squirrel`](./Engine_LogicKeys.md#object-squirrel) | Integer / Object  | The number of squirrel familiars spawned. | 1 | `{ . . . }`<br>`10` |
| [`Toad`](./Engine_LogicKeys.md#object-toad) | Integer / Object  | The number of toad familiars spawned. | 1 | `{ . . . }`<br>`10` |
| [`Turkey`](./Engine_LogicKeys.md#object-turkey) | Integer / Object  | The number of turkeys spawned. | 1 | `{ . . . }`<br>`1000`<br>`2` |
| [`Turtle`](./Engine_LogicKeys.md#object-turtle) | Integer / Object  | The number of turtle familiars spawned. | 1 | `{ . . . }`<br>`10` |

</details>


---


### Object: `BirdRewards`


**Definition:** Defines the rewards and statuses applied when a bird allies with the unit.
**Total Count:** 18

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ally_rewards`](./Miscellaneous.md#object-ally_rewards) | Object  | Defines the rewards granted to the ally when the BirdRewards passive triggers. | 18 | `{ . . . }` |
| [`statuses`](./Passives_and_Statuses.md#object-statuses) | Object  | Defines the status effects applied when the parent trigger event occurs. | 5 | `{ . . . }` |

</details>


---


### Object: `CharacterLightSource`


**Definition:** Defines a dynamic light source attached to the unit, including color, glow, and size.
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`size`](./Enums.md#enum-size) | Enum / Float  | The scale factor (size multiplier) of the spawned unit. | 16 | `.2`<br>`.5`<br>`1` |
| [`color`](./Arrays.md#array-color) | Array | The RGB color of the light source. | 16 | `[.27 .47 .18]`<br>`[.3, .7, 1]`<br>`[.32 .10 .10]` |
| [`glow`](./Arrays.md#array-glow) | Array | The RGBA glow color of the light source. | 8 | `[.3, .7, 1, .5]`<br>`[.7, .3, 1, .5]`<br>`[.7, .8, .9, .5]` |

</details>


---


### Object: `HealthPickup`


**Definition:** Defines properties for a health pickup object, such as healing amount and visual frame range.
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 15 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `stored_food_value` | Integer | The amount of food value stored in this pickup. | 15 | `0`<br>`1`<br>`2` |
| [`frame_range`](./Arrays.md#array-frame_range) | Array | Specifies the minimum and maximum animation frame for the health pickup. | 15 | `[1 2]`<br>`[11 12]`<br>`[13 13]` |
| `anything_eats` | Boolean | If true, any unit can consume this health pickup. | 4 | `true` |
| `force_frame` | Integer | Forces the health pickup to use a specific animation frame. | 1 | `12` |

</details>


---


### Object: `statuses`


**Definition:** Defines the status effects applied when the parent trigger event occurs.
**Total Count:** 14

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BirdRewards`](./Characters_and_Bosses.md#object-birdrewards), [`Cat`](./Characters_and_Bosses.md#object-cat), [`NonCat`](./Characters_and_Bosses.md#object-noncat)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>	ag |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | `-1`<br>`-2`<br>`1` |
| [`Consumed`](./Passives_and_Statuses.md#object-consumed) | Object  | An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`. | 4 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `default`


**Definition:** The default configuration or value used when no specific override is provided.
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `effects`


**Definition:** Applies a list of status effects or visual effects to targets.
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Characters_and_Bosses.md#object-meleerevengedamage), [`damage_instance`](./Characters_and_Bosses.md#object-damage_instance), [`eat_damage`](./Characters_and_Bosses.md#object-eat_damage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1085 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 624 | Default<br>FormChange<br>Druid |
| `Stun` | Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 98 | `1`<br>`2`<br>`3` |
| `Burn` | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 85 | `1`<br>`10`<br>`2` |
| `Confusion` | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 37 | `1`<br>`10`<br>`2` |
| `ConstitutionUp` | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 22 | `-1`<br>`-2`<br>`1` |
| `Vaporize` | `Number` | Removes the target from play, preventing its corpse from being interacted with. | 21 | `1`<br>`20` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 12 | `1`<br>`2`<br>`3` |
| `BlackHoleSuck` | `Number` | The strength of the black hole's pull effect. | 1 | `1` |

</details>


---


### Object: `ImmediateAbilityReaction`


**Definition:** Specifies an ability or list of abilities used immediately in reaction to a triggering event.
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 13 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 6 | `true` |
| `backstabs_only` | Boolean | If true, the reaction only triggers on backstab damage. | 2 | `true` |
| `damage_threshold` | Integer | The amount of damage that must be dealt to trigger the ability reaction. | 2 | `10` |
| `even_if_blocked` | Boolean | If true, the reaction triggers even if the damage is blocked. | 2 | `true` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 2 | `true` |
| `health_threshold` | Integer | The health value at or below which the reaction triggers. -1 disables this check. | 2 | `-1`<br>`150`<br>`50` |
| `buddy_damage_only` | Boolean | If true, only damage dealt by the unit's buddy triggers the reaction. | 1 | `true` |
| `target_furthest_valid` | Boolean | If true, the reaction targets the furthest valid enemy. | 1 | `true` |

</details>


---


### Object: `AbilityHealthThreshold`


**Definition:** Defines an ability and conditions for its activation when the unit's health reaches a threshold.
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 13 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 12 | passives<br>class<br>	ag |
| [`threshold`](./Enums.md#enum-threshold) | Enum / Integer  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 12 | `"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 7 | `true` |
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 6 | `false`<br>`true` |
| `use_ai` | Boolean | If true, the ability uses AI targeting logic when triggered at the threshold. | 2 | `true` |
| `also_use_if_buddy_is_dead` | Boolean | If true, the ability is also triggered when the unit's buddy is dead. | 1 | `true` |
| `threshold_min` | Equation | The minimum health threshold formula (e.g., X) for the ability to trigger. | 1 | `X` |

</details>


---


### Object: `PassiveGroup`


**Definition:** A group of passive abilities that can be randomly assigned.
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#object-randompassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 14 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 13 | `Default`<br>`FormChange`<br>`Druid` | [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 13 | Default<br>FormChange<br>Druid |
| [`FormChange`](./Enums.md#enum-formchange) | Enum  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 12 | `Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum  | Specifies the ability ID that replaces the unit's basic attack. | 11 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| `SelfStatusCarefulness` | Integer | The carefulness level when applying statuses to self, used to control stacking. | 2 | `1` |
| `StatusCarefulness` | Integer | The carefulness level when applying statuses, used to control stacking behavior. | 2 | `1` |
| `ExtraBasicAttacks` | Integer | The number of additional basic attacks the unit can perform per turn. | 1 | `1`<br>`2` |
| [`TinkererBasicAttackSwitching`](./Passives_and_Statuses.md#object-tinkererbasicattackswitching) | Object  | Defines the abilities used for the Tinkerer's basic attack switching mechanic. | 1 | `{ . . . }` |

</details>


---


### Object: `round_end_bonusturn_pattern`


**Definition:** The action sequence the AI executes at the end of the round as a bonus turn.
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_all`](./Arrays.md#array-do_all) | Array | The list of abilities the AI executes in sequence during its turn. | 6 | `[*BungaEatCat attack BungaRoar move]`<br>`[*ButtFart, Unflip]`<br>`[*DCBirthSquirrel attack DCBirthSquirrel]` |
| [`do`](./Enums.md#enum-do) | Enum | The single, specific ability the AI executes. | 3 | `**BombRatTurtle`<br>`**G3Shake`<br>`**RockySlam` |
| [`do_one`](./Arrays.md#array-do_one) | Array | Specifies the ability references for a single bonus turn pattern at round end. | 2 | `[**PyrophinaVSWeatherRoar **PyrophinaVSRoar]`<br>`[**ZaratanaVSWeatherRoar **ZaratanaVSRoar]` |
| [`do_random`](./Arrays.md#array-do_random) | Array | The list of abilities from which the AI randomly selects one to execute. | 2 | `[**TVChangeObey **TVChangeStop **TVChangeDumb]`<br>`[AZ_BreakNeck AZ_BreakLeg AZ_BreakArm]`<br>`[CHSpawn CHCry]` |
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array | The list of actions (typically empty) the AI takes when it does nothing. | 1 | `[]` |
| [`do_priority`](./Arrays.md#array-do_priority) | Array | The list of abilities the AI executes, evaluating them in order of highest priority. | 1 | `[ attack]`<br>`[**DestroyerThrowShield DestroyerHolyAttack]`<br>`[**DestroyerThrowShield attack]` |

</details>


---


### Object: `SpawnThingOnDamage`


**Definition:** Specifies an object that spawns on the tile when the unit takes damage.
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 38 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 20 | `false`<br>`true` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 12 | `.02`<br>`.1`<br>`.15` |
| `spawn_on_death_hit` | Boolean | If true, spawning only occurs when the damage is lethal. | 10 | `false` |
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 2 | `1`<br>`2`<br>`25` |
| `consider_all_layers` | Boolean | If true, considers all map layers when determining the spawn location. | 2 | `true` |
| [`auto_cast`](./Enums.md#enum-auto_cast) | Enum | Specifies the ability to automatically cast on the spawned unit. | 1 | `Dash_Enemy` |
| `melee_ability_only` | Boolean | If true, spawning only occurs in response to melee damage. | 1 | `true` |

</details>


---


### Object: `DeathRattleRevive`


**Definition:** Specifies an ability or effect that revives the unit upon death, with options for stunning behavior.
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 8 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 8 | `true` |

</details>


---


### Object: `MoveWhenDamaged`


**Definition:** Defines movement behavior when the unit takes damage, such as weights and move ability.
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Arrays.md#array-weights) | Array / Enum  | Specifies the weight array or named preset for the crazy eye background AI. | 9 | `[0 0 1]`<br>`[0 1 0]`<br>`[1 0 0]` |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 2 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |

</details>


---


### Object: `Rage`


**Definition:** The rage form configuration, applied when the unit enters an enraged state.
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 9 | passives<br>class<br>	ag |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 8 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 6 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 6 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer  | Specifies an animation suffix for partial form changes. | 4 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| `move_speed_multiplier` | Float | A multiplier for the unit's base movement speed. | 1 | `.5`<br>`.66`<br>`.75` |

</details>


---


### Object: `FormChangeOnElementInfluence`


**Definition:** Defines the element that triggers a form change, optional visual effects, and the target form.
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 9 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 9 | `Electric`<br>`Fire`<br>`Gravity` |
| [`exclude`](./Enums.md#enum-exclude) | Enum | Specifies an element or effect that does not trigger the form change. | 5 | `SpellDamageUp`<br>`fire`<br>`water` |
| [`particle`](./Enums.md#enum-particle) | Enum | Specifies the particle effect displayed. | 5 | `ArrowFromAbove`<br>`BigMagicMissileBlast`<br>`Bolt` |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 5 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |

</details>


---


### Object: `ReflectProjectiles`


**Definition:** The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage.
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusCollector`


**Definition:** Specifies the status effects and their stack counts that the unit collects to trigger transformations.
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| `StrengthUp` | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 7 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `Poison` | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 4 | `1`<br>`10`<br>`2` |
| `Slow` | Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `-1`<br>`1`<br>`2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `TransformInXTurns`


**Definition:** Defines a delayed transformation after a set number of turns, with optional target object and initiative handling.
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#object-randompassivepool), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 8 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `initiative` | Integer | The unit's turn order priority; can be an integer modifier or 'keep_turns_end_turn' to force end of turn after acting. | 4 | `-10`<br>`-100`<br>`-20` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


---


### Object: `TransformOnElementInfluence`


**Definition:** Defines the element that triggers a transformation and the object to transform into.
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 9 | `Electric`<br>`Fire`<br>`Gravity` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 9 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

</details>


---


### Object: `FormChangeOffMap`


**Definition:** Specifies the unit's form when off the map and when on the map.
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_offmap`](./Enums.md#enum-form_offmap) | Enum | Specifies the form name to use when the unit is off the map. | 8 | `Default_Ceiling`<br>`Insane_Ceiling`<br>`OffMap` |
| [`form_onmap`](./Enums.md#enum-form_onmap) | Enum | Specifies the form name to use when the unit returns to the map. | 8 | `Default`<br>`Default_Ground`<br>`FightPhase` |

</details>


---


### Object: `SmallRockBehavior`


**Definition:** Defines the damage, knockback, and chain properties of small rocks spawned from this unit when destroyed.
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 4 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`knockback`](./Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 4 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| `chain` | Boolean | Specifies the ability to chain into and execute. | 2 | `AcidSplash`<br>`CaveSplash`<br>`FireFullSmall` |

</details>


---


### Object: `ChanceToSpitOnDamage`


**Definition:** Configures the chance to use a spit ability when taking damage, including base chance and per-damage bonus.
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 7 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `flat_chance` | Integer | The base percentage chance to spit when taking damage. | 5 | `100%`<br>`50%` |
| `chance_per_damage` | Integer | The additional percentage chance to spit per point of damage taken. | 3 | `0%`<br>`2%` |
| `backstabs_only` | Boolean | If true, the reaction only triggers on backstab damage. | 1 | `true` |
| `even_on_0_damage_if_knockback` | Boolean | If true, the reaction triggers on zero damage if knockback occurs. | 1 | `true` |

</details>


---


### Object: `MovementReaction`


**Definition:** Specifies an ability to cast when a unit moves within range, with options for targeting and conditions.
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 11 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 7 | `false`<br>`true` |
| `on_self_move_too` | Boolean | If true, the reaction triggers when the unit themselves move. | 3 | `true` |
| `objects_too` | Boolean | If true, the reaction triggers on movement of objects as well. | 2 | `true` |
| `blind_spot` | Boolean | If true, the reaction triggers only on movement from a blind spot. | 1 | `true` |
| `forward_only` | Boolean | If true, the reaction triggers only on forward movement relative to the unit. | 1 | `true` |
| `self_move_exclude_self_abilities` | Boolean | If true, movement caused by the unit's own abilities does not trigger the reaction. | 1 | `true` |

</details>


---


### Object: `CaveFamilyEnrage`


**Definition:** Specifies the ability used when the number of family members with a given tag falls below a threshold.
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 6 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 6 | `0`<br>`1`<br>`10` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 6 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |

</details>


---


### Object: `FormChangeWhilePrimingAbility`


**Definition:** Defines the form changes when a specific ability is being primed and when it is not.
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`priming`](./Enums.md#enum-priming) | Enum | Specifies the form name to use while the unit is priming an ability. | 6 | `DualSword_Primed`<br>`Priming`<br>`SwordAndShield_Primed` |
| [`not_priming`](./Enums.md#enum-not_priming) | Enum | Specifies the form name to use when the unit is not priming an ability. | 6 | `DualSword`<br>`NotPriming`<br>`SwordAndShield` |

</details>


---


### Object: `MoveTowardsDamageSource`


**Definition:** Determines the movement behavior when moving towards the unit that dealt damage to it.
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 5 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |
| `move_far` | Boolean | If true, the unit moves the maximum distance towards the damage source. | 4 | `false` |
| [`check_in_form`](./Enums.md#enum-check_in_form) | Enum | Specifies the form the unit must be in to trigger movement. | 2 | `Boris`<br>`Default` |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `can_move_zero` | Boolean | If true, the unit can move even if the distance to the damage source is zero. | 1 | `true` |
| [`check_has_status`](./Enums.md#enum-check_has_status) | Enum | Specifies a status effect the unit must have for the movement to trigger. | 1 | `FinalBossHitCountdownBoris` |
| `do_not_move_on_top` | Boolean | If true, the unit stops before reaching the damage source's tile. | 1 | `true` |
| `face_towards_after` | Boolean | If true, the unit rotates to face the damage source after moving. | 1 | `true` |
| [`ignore_tagged_sources`](./Enums.md#enum-ignore_tagged_sources) | Enum | Specifies a unit tag to ignore as a damage source for movement. | 1 | `megadino` |
| `move_short` | Boolean | If true, the unit moves a shorter distance towards the damage source. | 1 | `true` |

</details>


---


### Object: `SecurityBotProtect`


**Definition:** Specifies the ability and movement used by a security bot to protect allies.
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 7 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 5 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 3 | `false`<br>`true` |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum | Specifies a tag that the target unit must have for the team cast to trigger. | 3 | `collective`<br>`dc_cat`<br>`dinofamily` |
| `not_on_kill` | Boolean | If true, the protection does not trigger when the protected unit is killed. | 2 | `true` |

</details>


---


### Object: `HasCat`


**Definition:** The form configuration applied when the unit is holding or has swallowed a cat.
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 5 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 5 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>	ag |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 4 | `{ . . . }` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer  | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


---


### Object: `MoveTowardsKillers`


**Definition:** Determines the movement behavior when moving towards units that have killed an ally.
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 3 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |
| [`character_filter`](./Arrays.md#array-character_filter) | Array | Specifies which characters to consider as killers when moving towards them. | 3 | `[SpiderCat, TallSpiderCat]` |

</details>


---


### Object: `PassiveWhileHasStatus`


**Definition:** An object containing `status` and `passives` that grants the listed passives while the unit has the specified status.
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 6 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 10 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 6 | `{ . . . }` |

</details>


---


### Object: `TransformOnDeathImmediately`


**Definition:** The object to transform into immediately upon death, with optional turn handling.
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum | Determines when the spawned unit takes its first turn relative to the spawn event. | 4 | `end_of_round`<br>`initiative`<br>`keep_turns` |
| [`obj`](./Arrays.md#array-obj) | Array / Enum  | Specifies one or more object names to bounce towards the target. | 4 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |

</details>


---


### Object: `BaitAura`


**Definition:** The range of the bait aura that draws enemies towards the unit.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 4 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `Big`


**Definition:** Defines the 'Big' form, including its animation, attack, passives, and positional data.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Consumed`


**Definition:** An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`statuses`](./Characters_and_Bosses.md#object-statuses)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 23 | Default<br>FormChange<br>Druid |
| `struggle_ability` | `String` | Specifies the name of the ability the consumed unit uses to attempt escape. | 17 | `CHuskStruggle`<br>`CaveWomanEscape`<br>`LennyStruggle` |
| `force_contact` | `Boolean` | If true, the consumed unit is forced into contact with the consumer. | 15 | `true` |
| `instant` | `Boolean` | If true, the consumption happens immediately without a timer. | 12 | `true` |
| `mount_mode` | `String` | Specifies the mounting mode; values include 'auto' or 'true'. | 12 | `auto`<br>`true` |
| `do_not_pop_corpse` | `Boolean` | If true, the consumed unit's corpse is not popped upon consumption. | 11 | `true` |
| `drop_on_death` | `String` | Determines if and how the consumed unit is dropped on death; values include 'true', 'false', or 'deferred'. | 11 | `deferred`<br>`false`<br>`true` |
| `use_placeholder` | Boolean | If true, renders the ability using a temporary placeholder animation instead of the final art. | 3 | `true` |

</details>


---


### Object: `ForceUseAbility`


**Definition:** The name of the ability the source is forced to use, optionally with a chance.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossHitCountdownBoris`](./Characters_and_Bosses.md#object-finalbosshitcountdownboris), [`FinalBossHitCountdownExplosive`](./Characters_and_Bosses.md#object-finalbosshitcountdownexplosive)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `show_name` | Boolean | If true, displays the ability name when force used. | 2 | `true` |

</details>


---


### Object: `Holy`


**Definition:** Specifies the 'Holy' form within FormChanger, with its own animation suffix and passives.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `hot`


**Definition:** The form configuration applied when the unit is in a hot state, granting fire element.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 4 | `""`<br>`"0"`<br>`"1"` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 4 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 8 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 4 | `{ . . . }` |

</details>


---


### Object: `MoveAway`


**Definition:** Defines an AI virtual ability that moves the unit away from its current target using the specified ability and move weights.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 4 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `MoveClose`


**Definition:** Defines an AI virtual ability that moves the unit close to its target using the specified ability and move weights.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 4 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 3 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |

</details>


---


### Object: `OffMap`


**Definition:** The form configuration applied when the unit is off the battlefield map.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 3 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


---


### Object: `passive`


**Definition:** Defines the passive form, where the unit does nothing (uses DoNothing attack) and is inactive.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |

</details>


---


### Object: `StatusEachTurnEnd`


**Definition:** Specifies status effects applied to the unit at the end of each of its turns.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 42 | passives<br>class<br>	ag |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 5 | `-1`<br>`-2`<br>`-4` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 5 | `Default`<br>`FormChange`<br>`Druid` | `AllStatsUp` | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 7 | Default<br>FormChange<br>Druid |
| [`Conditional_BadRoll`](./Passives_and_Statuses.md#object-conditional_badroll) | Object  | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 1 | `{ . . . }` |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusOnKill`


**Definition:** Specifies status effects or actions triggered when the unit kills an enemy.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 20 | passives<br>class<br>	ag |
| `HealthGain` | Integer | The amount of health restored to the source. | 5 | `1`<br>`10`<br>`2` |
| [`UseAbility_NonStack`](./Enums.md#enum-useability_nonstack) | Enum  | Specifies an ability to use on kill that does not stack with itself. | 3 | `BBTransformZealot`<br>`GenericRage` |

</details>


---


### Object: `StatusOnTookDamageFromAbility`


**Definition:** Specifies status effects triggered when the unit takes damage specifically from an ability (not environmental).
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>	ag |
| `ExtraBasicAttacks_Status` | Integer | The number of additional basic attacks the unit can perform each turn. | 2 | `1` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | `Bleed` | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 2 | Default<br>FormChange<br>Druid |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |
| `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 1 | `1` |

</details>


---


### Object: `StunImmunity`


**Definition:** If 1, the unit is immune to stun. The optional object configures whether to cleanse stun on apply.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean | If true, removes any existing stun effect when this immunity is applied. | 1 | `false` |

</details>


---


### Object: `Trapper`


**Definition:** Specifies a trap-placing ability and its targeting parameters.
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `cancel_movement` | Boolean | If true, the trapper cancels the trapped unit's movement. | 2 | `false` |
| `pathfinding_avoidance` | Integer | The weight that makes other units avoid traversing this tile during pathfinding. | 2 | `250` |
| [`range`](./Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `AllAlive`


**Definition:** The form configuration applied when all family members are alive.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `ArmorPickup`


**Definition:** The amount of armor stacks and the frame range for the pickup animation.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`frame_range`](./Arrays.md#array-frame_range) | Array | Specifies the minimum and maximum animation frame for the health pickup. | 3 | `[1 2]`<br>`[11 12]`<br>`[13 13]` |

</details>


---


### Object: `Bomb`


**Definition:** Defines the 'Bomb' form, an explosive state that triggers an ability on death.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Buddy`


**Definition:** Specifies a buddy unit that accompanies or is spawned alongside the unit, with optional reclaim and targeting properties.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 3 | `false`<br>`true` |
| [`obj`](./Arrays.md#array-obj) | Array / Enum  | Specifies one or more object names to bounce towards the target. | 3 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |
| `reclaim_if_lost` | Boolean | If true, the buddy can be reclaimed after being lost. | 1 | `true` |

</details>


---


### Object: `Cat`


**Definition:** Defines the behavior and form change for captured cat units.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#object-mothertumorpassive), [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#object-mothertumorspawnincapture)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum | Specifies the form to change into. | 3 | `BigHolding`<br>`BigHoldingCat`<br>`SmallHolding` |
| [`statuses`](./Passives_and_Statuses.md#object-statuses) | Object  | Defines the status effects applied when the parent trigger event occurs. | 2 | `{ . . . }` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `CaveMan`


**Definition:** Defines the 'CaveMan' form of a CavePerson enemy, including its animation, attack, and passives.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


---


### Object: `Down`


**Definition:** The form configuration applied when the unit is in a knocked-down or prone state.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 3 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |

</details>


---


### Object: `Fire`


**Definition:** Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `FormChangeHealthThreshold`


**Definition:** Specifies health thresholds that trigger form changes, with form_below for health at or below and form_above for health above.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_above`](./Enums.md#enum-form_above) | Enum | The form to change to when health is above the threshold. | 3 | `Default`<br>`Full`<br>`Standing` |
| [`form_below`](./Enums.md#enum-form_below) | Enum | The form to change to when health is below the threshold. | 3 | `Damaged`<br>`DesireMech`<br>`Standing2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |
| [`threshold`](./Enums.md#enum-threshold) | Enum / Integer  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 3 | `"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| `count_shield` | Boolean | If true, shields count towards the health threshold calculation. | 1 | `true` |

</details>


---


### Object: `Full`


**Definition:** The form configuration applied when the unit is in a full state.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`statuses_on_enter_form`](./Miscellaneous.md#object-statuses_on_enter_form) | Object  | Statuses or abilities applied when entering this form. | 2 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


---


### Object: `ManaPickup`


**Definition:** The amount of mana stacks and the frame range for the pickup animation.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`frame_range`](./Arrays.md#array-frame_range) | Array | Specifies the minimum and maximum animation frame for the health pickup. | 3 | `[1 2]`<br>`[11 12]`<br>`[13 13]` |

</details>


---


### Object: `NonCat`


**Definition:** Defines the behavior and form change for captured non-cat units.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#object-mothertumorpassive), [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#object-mothertumorspawnincapture)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum | Specifies the form to change into. | 3 | `BigHolding`<br>`BigHoldingCat`<br>`SmallHolding` |
| [`statuses`](./Passives_and_Statuses.md#object-statuses) | Object  | Defines the status effects applied when the parent trigger event occurs. | 2 | `{ . . . }` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `OneAlive`


**Definition:** The form configuration applied when only one family member remains alive.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 3 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 3 | `{ . . . }` |

</details>


---


### Object: `RandomPassivePool`


**Definition:** A pool of random passives from which one is chosen for this unit.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 22 | passives<br>class<br>	ag |
| [`PassiveGroup`](./Passives_and_Statuses.md#object-passivegroup) | Object  | A group of passive abilities that can be randomly assigned. | 2 | `{ . . . }` |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 1 | `{ . . . }` |
| [`TransformInXTurns`](./Passives_and_Statuses.md#object-transforminxturns) | Object  | Defines a delayed transformation after a set number of turns, with optional target object and initiative handling. | 1 | `{ . . . }` |

</details>


---


### Object: `ReplaceBrain`


**Definition:** Defines a replacement AI brain and behavior pattern for the mutant.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StacyMutant_Fire`](./Characters_and_Bosses.md#object-stacymutant_fire), [`StacyMutant_Ice`](./Characters_and_Bosses.md#object-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#object-stacymutant_lightning)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum | Specifies the AI brain type used for decision-making logic. | 4 | `DicerBrain`<br>`GenericBrain`<br>`MountBrain` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 4 | `always_cast`<br>`always_cast_careless`<br>`angry` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 4 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`pattern`](./Miscellaneous.md#object-pattern) | Object  | Defines a sequence of actions the AI will execute in order, with optional priority or all-in-one. | 3 | `{ . . . }` |

</details>


---


### Object: `SquirrelForm`


**Definition:** Defines the 'SquirrelForm', a transformation used by units like DeathMetal, granting melee attack and speed bonuses.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


---


### Object: `SupportFormChangeInsteadOfRun`


**Definition:** Specifies a form change to trigger instead of fleeing, either as a passive object with ability details or a direct form name.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `wait_till_turn` | Boolean | If true, the form change will not occur until the unit's next turn. | 1 | `true` |

</details>


---


### Object: `TwoAlive`


**Definition:** A form that activates when two specific units are alive, granting the contained passives and abilities.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 3 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 3 | `{ . . . }` |

</details>


---


### Object: `Up`


**Definition:** Defines the 'Up' form, including its animation, AI behavior, and passives such as UpTireBehavior.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 3 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


---


### Object: `Water`


**Definition:** Form state for water element, applying a puddle or movement bonus.
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer  | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `AbilityOnRoundEnd`


**Definition:** Specifies an ability that is automatically executed at the end of each round.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `force_display_name` | Boolean | If true, forces the display name to show for the ability. | 2 | `true` |

</details>


---


### Object: `AbilityWhenTaggedCharacterMovesNear`


**Definition:** An object containing `ability`, `tag`, and `range` that triggers the specified ability when a character with the given tag moves within range.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`range`](./Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 5 | `1`<br>`10`<br>`2` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 5 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |

</details>


---


### Object: `active`


**Definition:** Defines the active form, containing passives and abilities that are active while in this form.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AddTemporaryEffectsToBasicAttack`


**Definition:** A container object that lists temporary status effects applied to the unit's basic attack.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fury` | Integer | The amount of Fury (bonus damage or charges) gained. | 4 | `10`<br>`55`<br>`75` |

</details>


---


### Object: `alternate_energized_effect`


**Definition:** Effects applied when the robot becomes energized, such as form changes or stat boosts.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Robot`](./Characters_and_Bosses.md#object-robot)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`FormChange`](./Enums.md#enum-formchange) | Enum  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 1 | `Big`<br>`BigHolding`<br>`BigHoldingCat` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 1 | `1`<br>`3` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `AutocastEachRound`


**Definition:** Contains an ability name and optional 'even_if_stunned' flag to autocast each round.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 9 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 6 | `true` |

</details>


---


### Object: `Bishop`


**Definition:** Defines the 'Bishop' form for Cultist enemies, with its own attack (BBXLightning) and animation.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `BlackHole`


**Definition:** Defines the 'BlackHole' form, a variant of NeutronStar with its own animation and name.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Boris`


**Definition:** Specifies the 'Boris' form within FormChanger, with its own animation suffix and passives.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `BungaEntrance`


**Definition:** Specifies the entrance animation, ability, and conditions for this unit's dramatic battle entrance.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 2 | `true` |
| `health_threshold` | Integer | The health value at or below which the reaction triggers. -1 disables this check. | 2 | `-1`<br>`150`<br>`50` |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum | Specifies the tag used to identify allied warriors for this ability. | 2 | `bungawarrior`<br>`finalboss_clonecat` |

</details>


---


### Object: `CaveBaby`


**Definition:** Defines the 'CaveBaby' form of a CavePerson enemy, with reduced health and baby attack.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `CaveManSpear`


**Definition:** Defines the 'CaveManSpear' form of a CavePerson enemy, with a spear attack and corresponding animation.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


---


### Object: `CaveWoman`


**Definition:** Defines the 'CaveWoman' form of a CavePerson enemy, with kick attack and higher health.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `CherubimReaction`


**Definition:** Specifies the abilities used when this unit leaves or returns to the battlefield.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Leave`](./Engine_LogicKeys.md#object-leave) | Enum / Object  | Specifies the ability used when this unit leaves the field. | 2 | `{ . . . }`<br>`CherubimLeave`<br>`LELeave` |
| [`Return`](./Engine_LogicKeys.md#object-return) | Enum / Object  | Specifies the ability used when this unit returns to the field. | 2 | `{ . . . }`<br>`CherubimReturn`<br>`LEReturn` |

</details>


---


### Object: `Conditional_GoodRoll`


**Definition:** Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ally_rewards`](./Characters_and_Bosses.md#object-ally_rewards)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 37 | `.1`<br>`.16666666`<br>`.3` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 37 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 15 | passives<br>class<br>	ag |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 5 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |

</details>


---


### Object: `Cultist`


**Definition:** Defines the 'Cultist' form, a basic melee form with its own name and tooltip.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `DashRandomly`


**Definition:** Defines an AI virtual ability that causes the unit to dash in a random direction using the specified ability and decision weights.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 2 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


---


### Object: `DiesToElement`


**Definition:** Specifies the element that instantly kills this unit, optionally with an instant flag.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 1 | `Electric`<br>`Fire`<br>`Gravity` |
| `instant` | `Boolean` | If true, the consumption happens immediately without a timer. | 1 | `true` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `dispersed_bonusturn_pattern`


**Definition:** The action sequence used when bonus turns are evenly distributed among multiple units.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum | The single, specific ability the AI executes. | 2 | `**BombRatTurtle`<br>`**G3Shake`<br>`**RockySlam` |

</details>


---


### Object: `Empty`


**Definition:** Defines the 'Empty' form, typically indicating a state with no content (e.g., empty stomach).
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |

</details>


---


### Object: `Escape`


**Definition:** Defines an AI virtual ability that causes the unit to escape using the specified ability and move weights.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `Explosive`


**Definition:** Specifies the 'Explosive' form within FormChanger, with its own animation suffix and passives.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `FaceLastDamage`


**Definition:** If set to 1, the unit turns to face the direction of the last damage received; an object can specify animation settings.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean | If true, uses turn-based animations for the face change. | 1 | `true` |

</details>


---


### Object: `FireFull`


**Definition:** Defines the 'FireFull' form, a fully charged fire state with its own animation and visual combo.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Flush`


**Definition:** Defines a form that executes a sequence of actions (FlushX, side switch, form switch) and has a spell with a localized name.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


---


### Object: `FormChangeDuringWeatherElement`


**Definition:** Specifies a form change that triggers when the weather matches a given element.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 2 | `Electric`<br>`Fire`<br>`Gravity` |
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 2 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |

</details>


---


### Object: `Holding`


**Definition:** Defines the 'Holding' form, used when the unit is holding an object, with associated movement and form change behaviors.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer  | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Johnny`


**Definition:** Defines a form that executes a mega blast, side switch, and form switch in sequence.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


---


### Object: `KnockUpAndAway`


**Definition:** Contains parameters for launching the target upward and away from the source, including stacks and distance.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#object-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#object-conditional_isphysicalattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 24 | `-3`<br>`10`<br>`2` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 22 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `displace` | Boolean | If true, the knockback also displaces the target to a different tile. | 2 | `true` |
| `self_damage` | Boolean / Integer | Defines damage or effects applied to the caster when using the ability. | 2 | `1`<br>`10`<br>`100%` |
| [{Damaging Keys}](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 2 | `damage_instance`<br>`spell`<br>`false` |

</details>


---


### Object: `LastHit`


**Definition:** Defines a form that grants 2 dispersed bonus turns after the last hit.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


---


### Object: `MotherTumorSpawnInCapture`


**Definition:** Specifies the form changes and statuses applied when the mother tumor spawns after capturing a cat or non-cat.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](./Miscellaneous.md#object-cat) | Object  | Defines the behavior and form change for captured cat units. | 2 | `{ . . . }` |
| [`NonCat`](./Miscellaneous.md#object-noncat) | Object  | Defines the behavior and form change for captured non-cat units. | 2 | `{ . . . }` |
| [`Nothing`](./Miscellaneous.md#object-nothing) | Object  | Defines the behavior when nothing is captured, typically just an animation. | 1 | `{ . . . }` |

</details>


---


### Object: `MoveCenter`


**Definition:** Defines an AI virtual ability that moves the unit toward the center of the map using the specified ability and move weights.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `MoveForThrow`


**Definition:** Defines an AI virtual ability that moves the unit into position for a throw ability.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 2 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `Mutant`


**Definition:** As an object, defines the mutant form with reduced move speed and custom name. As an integer, defines spawn weight.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| `move_speed_multiplier` | Float | A multiplier for the unit's base movement speed. | 1 | `.5`<br>`.66`<br>`.75` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `NeutronStar`


**Definition:** Defines the neutron star form with custom graphics and a random pattern AI (rumble or explode).
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>`damage_instance`<br>`spell`<br>`self_damage`

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `NotPriming`


**Definition:** Defines the 'NotPriming' form, which allows the unit to take main turns and grants bonus turns.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag`

</details>


---


### Object: `Nuke`


**Definition:** Defines a nuke form with no attack or movement options.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `PassiveWhileNotHasStatus`


**Definition:** Specifies a set of passives that are active only when this unit does not have the given status.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 2 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


---


### Object: `Priming`


**Definition:** Defines the 'Priming' form, where the unit does not take main turns but gains bonus turns at round end.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


---


### Object: `ProtectTargetedAllies`


**Definition:** Specifies the ability used to protect targeted allies, including an optional target filter.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`target_filter`](./Enums.md#enum-target_filter) | Enum | Specifies which targets the protection applies to, based on their unit type or tag. | 2 | `Kitten`<br>`any` |

</details>


---


### Object: `Rain`


**Definition:** Defines the rain weather effect with associated particle, sound, and rendering settings.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |

</details>


---


### Object: `RemoveStatusStacks`


**Definition:** An object specifying a status name and the number of stacks to remove from the target.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Characters_and_Bosses.md#object-statusonendmove), [`StatusOnTookDamage`](./Characters_and_Bosses.md#object-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | passives<br>class<br>	ag |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 4 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |

</details>


---


### Object: `SlotMachineRollPool`


**Definition:** Defines the weighted pool of possible slot machine roll results.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SlotResult_Jackpot_Coins`](./Engine_LogicKeys.md#object-slotresult_jackpot_coins) | Integer / Object  | The result of a jackpot roll that spawns coins, or the weight of that result in the pool. | 2 | `{ . . . }`<br>`1` |
| [`SlotResult_Explode`](./Engine_LogicKeys.md#object-slotresult_explode) | Integer / Object  | The result of an explosion roll, or the weight of that result. | 1 | `{ . . . }`<br>`1` |
| [`SlotResult_Nothing`](./Engine_LogicKeys.md#object-slotresult_nothing) | Integer / Object  | The result of a nothing roll, or the weight of that result. | 1 | `{ . . . }`<br>`7` |
| [`SlotResult_RandomPickup`](./Engine_LogicKeys.md#object-slotresult_randompickup) | Integer / Object  | The result of a random pickup roll, or the weight of that result. | 1 | `{ . . . }`<br>`11` |

</details>


---


### Object: `Small`


**Definition:** Defines the 'Small' form, typically used for smaller size variants, with its own attack and animation.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |

</details>


---


### Object: `SpearRun`


**Definition:** Defines an AI virtual ability that moves the unit to run with a spear and pick it up.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 2 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `statuses_on_enter_form`


**Definition:** Statuses or abilities applied when entering this form.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Full`](./Characters_and_Bosses.md#object-full)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusGroup`


**Definition:** A container grouping multiple status effects to be applied simultaneously.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Characters_and_Bosses.md#object-randomstatusfrompool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>	ag |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 2 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |

</details>


---


### Object: `StatusOnSpawnIn`


**Definition:** Applies statuses or actions upon the unit spawning into the battlefield.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusOnTookDamage`


**Definition:** Specifies status effects or actions triggered when the unit takes damage.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 30 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 14 | `Default`<br>`FormChange`<br>`Druid` | `StrengthUp` | Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 13 | Default<br>FormChange<br>Druid |
| `ConstitutionUp` | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 3 | `-1`<br>`-2`<br>`1` |
| [`RemoveStatusStacks`](./Miscellaneous.md#object-removestatusstacks) | Object  | An object specifying a status name and the number of stacks to remove from the target. | 1 | `{ . . . }` |

</details>


---


### Object: `TempPassiveUntilSettled`


**Definition:** An object containing a temporary passive that is applied until the character's position is settled.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#object-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#object-conditional_isphysicalattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`MeleeRevengeDamage`](./Passives_and_Statuses.md#object-meleerevengedamage) | Object  | Defines the damage and effects applied back to a melee attacker upon being hit. | 2 | `{ . . . }` |

</details>


---


### Object: `TinkererBasicAttackSwitching`


**Definition:** Defines the abilities used for the Tinkerer's basic attack switching mechanic.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveGroup`](./Characters_and_Bosses.md#object-passivegroup), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum | The ability used for the craft action in the Tinkerer's basic attack switching. | 3 | `TinkererCraft` |
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum | The ability used for the throw action in the Tinkerer's basic attack switching. | 3 | `TinkererThrow` |

</details>


---


### Object: `TransformOnElementInfluencex`


**Definition:** Transforms into a specified object when influenced by a given element.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 2 | `Electric`<br>`Fire`<br>`Gravity` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

</details>


---


### Object: `Turtled`


**Definition:** Defines the 'Turtled' form, a defensive state where the unit cannot attack or move.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 2 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 2 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |

</details>


---


### Object: `WereMan`


**Definition:** Form state for the were-man transformation, with fury swipe attack and sabertooth faction.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Zealot`


**Definition:** Form state for the zealot variant of a cultist, with a stabbing attack.
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>	ag |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `additional_statuses`


**Definition:** Additional status effects applied to the spawned unit on death.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnOnDeath`](./Characters_and_Bosses.md#object-spawnondeath)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. | 1 | `1` |

</details>


---


### Object: `AddStatusToReceivedDamage`


**Definition:** Applies a status effect to the attacker when the unit takes damage.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AddStatusToSpells`


**Definition:** Specifies status effects added to all spell attacks used by this unit.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AddStatusToTrampleDamage`


**Definition:** An object whose nested keys define statuses applied to trample damage.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Characters_and_Bosses.md#object-passivewhendead)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AddStatusToWeapons`


**Definition:** Specifies status effects to add to the unit's weapon attacks, with their stack counts.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| `Bleed` | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 3 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `AdventureTokenPassivePool`


**Definition:** A pool of passive definitions granted to the unit when picked up as an adventure token.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 12 | passives<br>class<br>	ag |
| [`StacyMutant_Brace`](./Miscellaneous.md#object-stacymutant_brace) | Object  | A passive group granting the Brace ability and cosmetic changes. | 1 | `{ . . . }` |
| [`StacyMutant_Counter`](./Miscellaneous.md#object-stacymutant_counter) | Object  | A passive group granting a counter attack and a bleed effect on basic attacks. | 1 | `{ . . . }` |
| [`StacyMutant_Damage`](./Miscellaneous.md#object-stacymutant_damage) | Object  | A passive group increasing damage and decreasing max health with cosmetic changes. | 1 | `{ . . . }` |
| [`StacyMutant_DoubleHead`](./Miscellaneous.md#object-stacymutant_doublehead) | Object  | A passive group granting an extra dispersed turn and cosmetic changes. | 1 | `{ . . . }` |
| [`StacyMutant_Fire`](./Miscellaneous.md#object-stacymutant_fire) | Object  | A passive group granting fire immunity and a lava shot basic attack. | 1 | `{ . . . }` |
| [`StacyMutant_Health`](./Miscellaneous.md#object-stacymutant_health) | Object  | A passive group increasing max health, reducing speed, and scaling size. | 1 | `{ . . . }` |
| [`StacyMutant_Holy`](./Miscellaneous.md#object-stacymutant_holy) | Object  | A passive group granting a divine shield and cosmetic changes. | 1 | `{ . . . }` |
| [`StacyMutant_Ice`](./Miscellaneous.md#object-stacymutant_ice) | Object  | A passive group granting ice immunity and an ice breath basic attack. | 1 | `{ . . . }` |
| [`StacyMutant_Lightning`](./Miscellaneous.md#object-stacymutant_lightning) | Object  | A passive group granting electric immunity and a lightning dash basic attack. | 1 | `{ . . . }` |
| [`StacyMutant_Mirror`](./Miscellaneous.md#object-stacymutant_mirror) | Object  | A passive group granting projectile reflection and random magic missile each turn. | 1 | `{ . . . }` |
| [`StacyMutant_Speed`](./Miscellaneous.md#object-stacymutant_speed) | Object  | A passive group increasing speed, reducing damage, and scaling size. | 1 | `{ . . . }` |
| [`StacyMutant_Thorns`](./Miscellaneous.md#object-stacymutant_thorns) | Object  | A passive group granting thorns damage and cosmetic changes. | 1 | `{ . . . }` |

</details>


---


### Object: `AggroTargetIsGovernedByHitEffect`


**Definition:** If set, the aggro target is determined by the unit's hit effect, with a sub-key for enemies_only.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 1 | `false`<br>`true` |

</details>


---


### Object: `ai_if_spawned_as_enemy`


**Definition:** Overrides the unit's AI settings when it is spawned as an enemy rather than an ally.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum | Specifies the AI brain type used for decision-making logic. | 1 | `DicerBrain`<br>`GenericBrain`<br>`MountBrain` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 1 | `always_cast`<br>`always_cast_careless`<br>`angry` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`pattern`](./Miscellaneous.md#object-pattern) | Object  | Defines a sequence of actions the AI will execute in order, with optional priority or all-in-one. | 1 | `{ . . . }` |

</details>


---


### Object: `Alert`


**Definition:** Defines the 'Alert' form, an alerted state with a pattern brain AI.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `AllStatsAura`


**Definition:** An aura that grants bonus stacks of all stats to allies within range.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aura_requires_tag`](./Enums.md#enum-aura_requires_tag) | Enum | Specifies the tag that units must have to be affected by this aura. | 1 | `humanoid` |
| [`range`](./Enums.md#enum-range) | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 1 | `1`<br>`10`<br>`2` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `Attacker`


**Definition:** Defines the 'Attacker' form, focusing on offensive actions like attacking and charging.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


---


### Object: `BackflipWhenTargeted`


**Definition:** The number of backflip charges, or an object defining its ability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnGainCoins`](./Characters_and_Bosses.md#object-statusongaincoins)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 7 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 7 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `BattlefieldUniqueRandomPassive`


**Definition:** A pool of unique random passives that can be applied to each battlefield instance.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Integer | The weight for the demonic glyph of bite, or its configuration. | 1 | `1` |
| `DemonicGlyph_Bounce` | Integer | The weight for the demonic glyph of bounce, or its configuration. | 1 | `1` |
| `DemonicGlyph_Fire` | Integer | The weight for the demonic glyph of fire, or its configuration. | 1 | `1` |
| `DemonicGlyph_Movement` | Integer | The weight for the demonic glyph of movement, or its configuration. | 1 | `1` |
| `DemonicGlyph_Summon` | Integer | The weight for the demonic glyph of summon, or its configuration. | 1 | `1` |

</details>


---


### Object: `BellyFull`


**Definition:** Defines the 'BellyFull' form, used when the unit has the Consuming status, with appropriate animation.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer  | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `BigHolding`


**Definition:** Defines the 'BigHolding' form, a larger variant while holding an object, triggered by the Consuming status.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `BigHoldingCat`


**Definition:** Defines the 'BigHoldingCat' form, a cat-sized variant of the holding form while Consuming.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Bully`


**Definition:** Defines the 'Bully' form, which allows the unit to take turns and enables its passives.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `BungaCheers`


**Definition:** Defines cheer particle effects and sounds triggered by ally or enemy actions.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ally_damage`](./Enums.md#enum-ally_damage) | Enum | Specifies the cheer effect when an ally takes damage. | 1 | `littleboo` |
| [`ally_dead`](./Enums.md#enum-ally_dead) | Enum | Specifies the cheer effect when an ally dies. | 1 | `bigboo` |
| [`enemy_damage`](./Enums.md#enum-enemy_damage) | Enum | Specifies the cheer effect when an enemy takes damage. | 1 | `littlecheer` |
| [`enemy_dead`](./Enums.md#enum-enemy_dead) | Enum | Specifies the cheer effect when an enemy dies. | 1 | `bigcheer` |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum | Specifies the tag used to identify allied warriors for this ability. | 1 | `bungawarrior`<br>`finalboss_clonecat` |

</details>


---


### Object: `CaveWomanHasCat`


**Definition:** Defines the 'CaveWomanHasCat' form, a variant of CaveWoman that attacks with a cat slap.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `CerberubsAggroTargetBehavior`


**Definition:** Defines the default and alert forms used by Cerberubs when changing aggro behavior.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alert_form`](./Enums.md#enum-alert_form) | Enum | Specifies the form to use when the unit is alerted. | 1 | `Alert` |
| [`default_form`](./Enums.md#enum-default_form) | Enum | Specifies the default form before aggro. | 1 | `Normal` |

</details>


---


### Object: `CerberubsJumpBlind`


**Definition:** Defines an AI virtual ability that makes Cerberubs jump with blind decision weights.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 1 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


---


### Object: `CerberubsJumpNormal`


**Definition:** Defines an AI virtual ability that makes Cerberubs jump with default decision weights.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 1 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


---


### Object: `ChanceToBackflip`


**Definition:** An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 6 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 6 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `ChanceToFormChangeOnAbilityDamage`


**Definition:** A chance to transform into a different form when damaged by an ability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 1 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |

</details>


---


### Object: `ChaosBossFormChangeGuide`


**Definition:** Defines active and passive piece sets and a health threshold for the Chaos boss's form change pattern.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives_health_threshold` | Integer | The health percentage threshold at which the boss's passive abilities change. | 1 | `50%` |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array | An array of piece names that are considered actively part of the current form. | 1 | `[Johnny Throb Flush]` |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array | An array of piece names that are considered passively part of the current form. | 1 | `[Host Nettle Bubs]` |

</details>


---


### Object: `ChaosBossPieces`


**Definition:** Defines the list of active and passive piece tags for the Chaos boss fight.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array | An array of piece names that are considered actively part of the current form. | 1 | `[Johnny Throb Flush]` |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array | An array of piece names that are considered passively part of the current form. | 1 | `[Host Nettle Bubs]` |

</details>


---


### Object: `ChaosHeadDropIn`


**Definition:** Defines the tag, spawn ability, and music for the Chaos head's drop-in sequence.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`new_music`](./Enums.md#enum-new_music) | Enum | Specifies the music track to play during the boss's head drop-in animation. | 1 | `chaos_boss_part2` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |

</details>


---


### Object: `Charging`


**Definition:** Defines the 'Charging' form, a wind-up state for a powerful attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer  | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Close`


**Definition:** Defines the 'Close' form, which triggers GSOpen ability upon reaction.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `CloseConvert`


**Definition:** Defines an AI virtual ability that moves close and uses the MarshmallowConvert ability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `Conditional_BadRoll`


**Definition:** An object containing an `odds` value and effects that are applied when a random roll succeeds.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Characters_and_Bosses.md#object-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 8 | `.1`<br>`.16666666`<br>`.3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>	ag |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 | `Default`<br>`FormChange`<br>`Druid` | `Madness` | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 8 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_HasKnockback`


**Definition:** An object containing actions that execute if the incoming damage has knockback.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Characters_and_Bosses.md#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](./Miscellaneous.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 | `{ . . . }` |
| `RemoveKnockback` | `Number` | The number of knockback stacks removed from the received damage. | 1 | `1` |
| [`TempPassiveUntilSettled`](./Miscellaneous.md#object-temppassiveuntilsettled) | Object  | An object containing a temporary passive that is applied until the character's position is settled. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_IsPhysicalAttack`


**Definition:** A conditional block that executes its child actions only if the triggering event is a physical attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#object-addstatustoreceiveddamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](./Miscellaneous.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 | `{ . . . }` |
| `RemoveKnockback` | `Number` | The number of knockback stacks removed from the received damage. | 1 | `1` |
| [`TempPassiveUntilSettled`](./Miscellaneous.md#object-temppassiveuntilsettled) | Object  | An object containing a temporary passive that is applied until the character's position is settled. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `CounterAttack`


**Definition:** Specifies the ability used when the unit counterattacks after being hit.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `without_orienting` | Boolean | If true, the counter-attack does not rotate the character to face the attacker. | 1 | `true` |

</details>


---


### Object: `CreateGlobalModifiers`


**Definition:** Defines global gameplay modifiers to activate.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Variable | If true, activates a global modifier effect on the house environment. | 5 | `CreateGlobalModifiers`<br>`BloodRain`<br>`NextPlayerCatTakesExtraTurn` |
| `BloodRain` | `Number` | If non-zero, enables the blood rain visual effect. | 3 | `1` |
| [`LowerAmbientLight`](./Miscellaneous.md#object-lowerambientlight) | Object  | If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly. | 3 | `{ . . . }` |

</details>


---


### Object: `Damaged`


**Definition:** Defines the 'Damaged' form, an injured state with a specific AI pattern to drink and attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


---


### Object: `Default_Ceiling`


**Definition:** Defines the 'Default_Ceiling' form for SpiderQueen, with AI pattern to spawn spiders.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag`

</details>


---


### Object: `Default_Ground`


**Definition:** Defines the 'Default_Ground' form for SpiderQueen, with AI pattern to web and attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag`

</details>


---


### Object: `DelayedAutoRevive`


**Definition:** Configures an automatic revival after a delay, with specified rounds and health percentage.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer | The maximum hit points of the unit. | 6 | `0`<br>`1`<br>`10` |
| `rounds` | Integer | The number of rounds after which the auto-revive triggers. | 6 | `1`<br>`2` |

</details>


---


### Object: `DesireMech`


**Definition:** Defines the 'DesireMech' form, a mech suit form with its own AI pattern.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


---


### Object: `DiceBehavior`


**Definition:** Defines the dice size and knockback damage for the Dice enemy.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dice_size` | Integer | The number of sides on the die. | 1 | `6` |
| `knockback_damage` | Integer | The amount of damage dealt by the knockback. | 1 | `5` |

</details>


---


### Object: `Die`


**Definition:** If set, kills the target immediately.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag`

</details>


---


### Object: `DiesToPiercingAndSpikes`


**Definition:** Makes the unit take lethal damage from piercing attacks and spike terrain.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `deferred` | Boolean | If true, the destruction is deferred until the character is settled. | 1 | `true` |

</details>


---


### Object: `DodgeWhenTargeted`


**Definition:** An object defining the ability and effects triggered when the unit is targeted for an attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |

</details>


---


### Object: `Drunker`


**Definition:** Defines the 'Drunker' form, a drunken state with altered animation.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


---


### Object: `DualSword`


**Definition:** Defines the 'DualSword' form of TheDestroyer, increasing move speed and using a dual sword attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| `move_speed_multiplier` | Float | A multiplier for the unit's base movement speed. | 1 | `.5`<br>`.66`<br>`.75` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `DualSword_Primed`


**Definition:** Defines the 'DualSword_Primed' form, a powered-up dual sword state with holy animation.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| `move_speed_multiplier` | Float | A multiplier for the unit's base movement speed. | 1 | `.5`<br>`.66`<br>`.75` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Dumb`


**Definition:** Defines the 'Dumb' form, which can be either a numeric value or an object with passives that disable spells and turn off TV.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `DybbukPossessionFallback`


**Definition:** An object specifying the fallback form and exit ability used when possession fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum | Determines the ability used when the Dybbuk possession ends. | 1 | `DybbukReturn` |
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 1 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |

</details>


---


### Object: `eat_damage`


**Definition:** An object defining the damage properties of the eat attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherGrowController`](./Characters_and_Bosses.md#object-mothergrowcontroller)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target regardless of accuracy or evasion. | 1 | `true` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| `makes_contact` | `Boolean` | If true, the damage instance is considered a contact hit, triggering contact-based passives on both the attacker and target. | 1 | `false`<br>`true` |
| `piercing` | `Boolean` | If true, the damage instance ignores armor or damage reduction effects on the target. | 1 | `true` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1 | `damage_instance`<br>`spell`<br>`false` |

</details>


---


### Object: `Else`


**Definition:** Contains the fallback effects to apply when a preceding conditional check fails.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#object-addstatustoreceiveddamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 14 | Default<br>FormChange<br>Druid |
| [`Conditional_HasKnockback`](./Characters_and_Bosses.md#object-conditional_hasknockback) | Object  | An object containing actions that execute if the incoming damage has knockback. | 1 | `{ . . . }` |
| [`KnockUpAndAway`](./Miscellaneous.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 | `{ . . . }` |

</details>


---


### Object: `exit_animations`


**Definition:** An object mapping exit conditions to their corresponding animation names.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Grappling`](./Characters_and_Bosses.md#object-grappling)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Default`](./Miscellaneous.md#object-default) | Enum / Object  | The default form configuration for a unit, containing its standard stats and abilities. | 1 | `{ . . . }`<br>`release` |

</details>


---


### Object: `Explody`


**Definition:** Defines the 'Explody' form, an explosive state that uses ToxExplode attack and cannot move.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `FaceAwayLastDamage`


**Definition:** An object defining animation overrides for the last damage event when the unit faces away.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 1 | `true` |
| `override_hit_animation` | Boolean | If true, the character's hit animation is overridden by the face-away animation. | 1 | `true` |
| `use_turn_animations` | Boolean | If true, uses turn-based animations for the face change. | 1 | `true` |

</details>


---


### Object: `FightPhase`


**Definition:** Defines the 'FightPhase' form, a combat form with float move and shoot attack, taking turns.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `FinalBossBeamQueue`


**Definition:** An object defining the queue of beam ability actions for the final boss form.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`queue`](./Enums.md#enum-queue) | Enum | Specifies the ability queued to fire the boss's beam. | 1 | `TheChild_TargetBeam` |
| [`release`](./Enums.md#enum-release) | Enum | Specifies the ability queued to release the boss's stored beams. | 1 | `TheChild_ReleaseBeams` |
| [`transform`](./Enums.md#enum-transform) | Enum | Specifies the ability queued to transform the boss into its next form. | 1 | `TheChild_TransformBoris` |

</details>


---


### Object: `FinalBossBecomeTheChild`


**Definition:** An object defining the transformation and environment changes when the boss becomes TheChild.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GlobalSpawnCharacter` | `String` | Specifies the name of a character to spawn globally. | 1 | `MegaGuppy` |
| `PlayBackground` | `Number` | Specifies the background index to play. | 1 | `0`<br>`1` |
| [`SwitchMusic`](./Miscellaneous.md#object-switchmusic) | Object  | Defines a new song or layer for the background music. | 1 | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `FinalBossHitCountdownBoris`


**Definition:** An object defining the countdown status effect properties for the Boris phase, including stacks, icons, and forced abilities.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon` | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 1 | `800`<br>`802`<br>`804` |
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 1 | `801`<br>`803`<br>`805` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |

</details>


---


### Object: `FinalBossHitCountdownExplosive`


**Definition:** An object defining the countdown status effect properties for the Explosive phase, including stacks, icons, and forced abilities.
**Total Count:** 1

`damage_instance`<br>`spell`<br>`self_damage`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon` | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 1 | `800`<br>`802`<br>`804` |
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 1 | `801`<br>`803`<br>`805` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |

</details>


---


### Object: `FinalBossHitCountdownHoly`


**Definition:** An object defining the countdown status effect properties for the Holy phase, including stacks and icons.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon` | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 1 | `800`<br>`802`<br>`804` |
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 1 | `801`<br>`803`<br>`805` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `FinalBossPupils`


**Definition:** An object configuring the visual tracking of the final boss's pupils, including radius, head position, and teleport tracking.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`radius`](./Arrays.md#array-radius) | Array / Integer  | The range in tiles of the distortion ring effect; an array [min, max] specifies a random radius within that range. | 1 | `0`<br>`1`<br>`13` |
| `reset_center_because_no_target_halflife` | Float | The half-life for the pupil position to reset to center when no target is available. | 1 | `.1` |
| `reset_center_because_of_animation_halflife` | Float | The half-life for the pupil position to reset to center during an animation. | 1 | `.05` |
| `teleport_tracking_halflife` | Float | The half-life for the pupil tracking to reacquire a target after a teleport. | 1 | `.01` |
| `tracking_acquisition_halflife` | Float | The half-life for the pupil tracking to smoothly acquire a new target. | 1 | `.1` |
| [`look_at_offset`](./Arrays.md#array-look_at_offset) | Array | A 3D vector offset from the head position that the pupils should look at. | 1 | `[0 2.5 0]` |
| [`virtual_head_position`](./Arrays.md#array-virtual_head_position) | Array | A 3D vector representing the virtual position of the head for pupil tracking. | 1 | `[11 2 11]` |

</details>


---


### Object: `FinalBossShieldHealth`


**Definition:** An object defining the shield health thresholds per visual state for the final boss.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`break_ability`](./Enums.md#enum-break_ability) | Enum | Specifies the ability used to break the shield. | 1 | `DestroyerBreakShield` |
| [`state_health`](./Arrays.md#array-state_health) | Array | An array of health thresholds defining state transitions. | 1 | `[` |

</details>


---


### Object: `FinalBossSyncAnimations`


**Definition:** An object defining animation synchronization with another character, including form change abilities.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`other_character`](./Enums.md#enum-other_character) | Enum | Specifies the name of the other boss character whose animations are synced. | 1 | `MegaGuppy` |
| [`other_form_change_abilities`](./Miscellaneous.md#object-other_form_change_abilities) | Object  | An object mapping form names to the other character's form change abilities. | 1 | `{ . . . }` |

</details>


---


### Object: `Flop`


**Definition:** Defines the initial flopped down state, using animation suffix 'Down' and a pattern AI that requires 4 wiggles to exit.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Flop2`


**Definition:** Defines a subsequent flopped down state triggered on hit, with variable wiggles (2-6) to recover.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `FlushBubs`


**Definition:** Defines a form granting an immediate ability reaction for Cerberubs shotgun.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `FlushHost`


**Definition:** Defines a host form with a partial animation suffix and a reflect projectiles passive that deals 2 self-damage.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `FlushNettle`


**Definition:** Defines a form that gains thorns and kinetic spikes after an enemy casts a spell.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `FoodMove`


**Definition:** Defines an AI virtual ability that moves the unit toward food using the CaveBabyFoodMove ability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `ForceTrample`


**Definition:** Defines an AI virtual ability that forces the unit to trample carelessly using the BirthwortTrample ability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 1 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


---


### Object: `GainDisorderFromPool`


**Definition:** Specifies a pool of disorders from which one is randomly gained on basic attack, with an optional chance.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Characters_and_Bosses.md#object-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 1 | `2`<br>`3`<br>`4` |

</details>


---


### Object: `Grappling`


**Definition:** Defines a grappling form with a specific animation suffix and exit animations.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit_animations`](./Miscellaneous.md#object-exit_animations) | Object  | An object mapping exit conditions to their corresponding animation names. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


---


### Object: `Grown`


**Definition:** Defines the grown form with a custom attack, name, UI floater offset, and a health weak threshold.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| `weak_threshold` | Integer | The health threshold below which the unit is considered weakened. | 1 | `0`<br>`1`<br>`15` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `GuaranteedJackpot`


**Definition:** Defines a form that guarantees a jackpot coin result from slot machine rolls.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `Guarding`


**Definition:** Defines a guarding form with a high brace passive.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer  | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `HalfDead`


**Definition:** Defines the half-dead form with reduced movement and a dash attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `HasDeadCat`


**Definition:** Defines a form when Lenny's cat is dead, with a slap attack and conditional form change while the status is active.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `HasRock`


**Definition:** Defines a form where the unit has a rock, with a bash attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |

</details>


---


### Object: `Headless`


**Definition:** Defines a headless form with increased movement.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `HealNeighborsEachTurn`


**Definition:** An object defining the amount and target filtering for healing adjacent units each turn.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 1 | `false`<br>`true` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `Hint_CrackedVisuals`


**Definition:** Defines a visual state with cracked animation suffix.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


---


### Object: `Hint_CrackedVisuals2`


**Definition:** Defines a visual state with charging cracked animation.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


---


### Object: `Hint_CrackedVisuals3`


**Definition:** Defines a visual state with swallowed cracked animation.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


---


### Object: `HitlerExecute`


**Definition:** An object defining the tag, ability, and health threshold for executing a clone.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`threshold`](./Enums.md#enum-threshold) | Enum / Integer  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 1 | `"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |

</details>


---


### Object: `HPAltStates`


**Definition:** An object defining alternate visual frames based on current HP thresholds.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`clipname`](./Enums.md#enum-clipname) | Enum | Specifies the animation clip name to use for the alt state. | 1 | `poopmain` |
| [`thresholds`](./Arrays.md#array-thresholds) | Array | An array of health percentage thresholds that trigger an alt state. | 1 | `[` |

</details>


---


### Object: `HumanDead`


**Definition:** Defines a form when the human half is dead, with a spin attack and custom tooltip.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |

</details>


---


### Object: `InfiniteRebirth`


**Definition:** Specifies the health and effects for unlimited rebirth upon death.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer | The maximum hit points of the unit. | 3 | `0`<br>`1`<br>`10` |
| `playercat_health` | Integer | The percentage of maximum health the player cat must have to trigger the rebirth. | 3 | `100%`<br>`25%` |
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 1 | `false`<br>`true` |

</details>


---


### Object: `InitialPhase`


**Definition:** Defines the initial phase form with a float move, shoot attack, and the ability to take turns.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Insane_Ceiling`


**Definition:** Defines the insane ceiling form with pattern AI and animation suffix.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Insane_Ground`


**Definition:** Defines the insane ground form with pattern AI and animation suffix.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `JohnnyBubs`


**Definition:** Defines a form granting an immediate ability reaction for Cerberubs shotgun.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `JohnnyHost`


**Definition:** Defines a host form with a partial animation suffix and a reflect projectiles passive that deals 2 self-damage.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `JohnnyNeedsWashing`


**Definition:** An object specifying the form names for washed and unwashed states.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_unwashed`](./Enums.md#enum-form_unwashed) | Enum | Specifies the form name for the unwashed state. | 1 | `Unwashed` |
| [`form_washed`](./Enums.md#enum-form_washed) | Enum | Specifies the form name for the washed state. | 1 | `Washed` |

</details>


---


### Object: `JohnnyNettle`


**Definition:** Defines a form that gains thorns and kinetic spikes after an enemy casts a spell.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Joystick`


**Definition:** Defines a form with joystick animation and an immediate ability reaction (fumble even/odd).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `LeapClose`


**Definition:** Defines an AI virtual ability that makes the unit leap toward its aggro target.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `Lifted`


**Definition:** Defines a lifted form with no attack or movement options.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Lit`


**Definition:** Defines a lit form that changes when wind element influence is applied.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `LowerAmbientLight`


**Definition:** If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CreateGlobalModifiers`](./Characters_and_Bosses.md#object-createglobalmodifiers)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`speed`](./Arrays.md#array-speed) | Array / Float  | The speed of the projectile or move, can be a value or a range. | 3 | `-30`<br>`-4`<br>`.5` |
| [`amount`](./Arrays.md#array-amount) | Array | For ambient light, the target brightness value (as a float or percentage array for RGB). | 3 | `.1`<br>`.25`<br>`.35` |

</details>


---


### Object: `MegaDinoDropController`


**Definition:** An object defining the abilities and stable leg count for the Mega Dino's leg drop sequence.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`head_drop`](./Enums.md#enum-head_drop) | Enum | Specifies the ability triggered when the head drops down. | 1 | `MD_HeadDrop` |
| [`leg_leave`](./Enums.md#enum-leg_leave) | Enum | Specifies the ability triggered when the legs leave the body. | 1 | `MD_LegLeave` |
| [`leg_return`](./Enums.md#enum-leg_return) | Enum | Specifies the ability triggered when the legs return to the body. | 1 | `MD_LegReturn` |
| `stable_legs` | Integer | The number of legs that must be stable for the head to drop. | 1 | `3` |

</details>


---


### Object: `ModularPickup`


**Definition:** An object defining the effects and sounds triggered when the unit is picked up.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`sound_event`](./Enums.md#enum-sound_event) | Enum | Specifies the sound event to play when the pickup is used. | 1 | `EatAntidote` |
| `Cleanse` | Integer | The number of stacks of negative status effects removed from the target. | 1 | `0`<br>`1` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` | [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | 0 | Default<br>FormChange<br>Druid | `Key`<br>`Default`<br>`FormChange`

</details>


---


### Object: `MonkCatReactionAbilities`


**Definition:** A set of mappings from action types (move, attack, spell, trinket) to the corresponding ability IDs the MonkCat will use for reactions.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`spell`](./Enums.md#enum-spell) | Enum | Specifies the spell ability to use as a reaction. | 1 | `MCHadouken` |
| [`trinket`](./Enums.md#enum-trinket) | Enum | The name of the trinket item the unit starts with. | 1 | `MCHadouken`<br>`MonkStyleChanger` |
| [`weapon`](./Enums.md#enum-weapon) | Enum | The name of the weapon item the unit starts with. | 1 | `AstroTaser`<br>`ButcherHook`<br>`CaveCatClub` |

</details>


---


### Object: `MotherGrowController`


**Definition:** Controls the growth of tumors on The Mother, including the tumor object, damage type, damage amount, and whether it pierces defense when eating damage.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eat_damage`](./Miscellaneous.md#object-eat_damage) | Object  | An object defining the damage properties of the eat attack. | 1 | `{ . . . }` |
| [`tumor_object`](./Enums.md#enum-tumor_object) | Enum | Specifies the name of the tumor object to spawn. | 1 | `MotherTumor` |

</details>


---


### Object: `MotherTumorPassive`


**Definition:** Defines the passive behavior for a MotherTumor, including the forms considered for pass/receive, the pass and receive animations, and the grow ability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](./Miscellaneous.md#object-cat) | Object  | Defines the behavior and form change for captured cat units. | 1 | `{ . . . }` |
| [`grow_ability`](./Enums.md#enum-grow_ability) | Enum | Specifies the ability used by the tumor to grow. | 1 | `MotherTumorGrow` |
| [`NonCat`](./Miscellaneous.md#object-noncat) | Object  | Defines the behavior and form change for captured non-cat units. | 1 | `{ . . . }` |
| [`pass_ani`](./Enums.md#enum-pass_ani) | Enum | Specifies the animation played when passing something to the tumor. | 1 | `pass` |
| [`receive_ani`](./Enums.md#enum-receive_ani) | Enum | Specifies the animation played when receiving something from the tumor. | 1 | `receive` |
| [`considered_forms`](./Arrays.md#array-considered_forms) | Array | An array of form names the tumor considers for interaction. | 1 | `[Big BigHolding BigHoldingCat]` |

</details>


---


### Object: `Mount`


**Definition:** Defines the entering and ejecting abilities for a mountable unit, along with its death rattle ability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eject_ability`](./Enums.md#enum-eject_ability) | Enum | Specifies the ability used to eject the mounted character. | 1 | `MechSuitEject` |
| [`enter_ability`](./Enums.md#enum-enter_ability) | Enum | Specifies the ability used to enter the mount. | 1 | `EnterMech` |

</details>


---


### Object: `Mounted`


**Definition:** Defines a mounted form with 'Cat' animation suffix.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


---


### Object: `MouthFull`


**Definition:** Defines a form with mouth full animation that changes while the Consuming status is active.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer  | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `MoveAfterAnyAttemptedAttack`


**Definition:** Defines the movement behavior (weights and abilities) used after any attempted attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Arrays.md#array-weights) | Array / Enum  | Specifies the weight array or named preset for the crazy eye background AI. | 1 | `[0 0 1]`<br>`[0 1 0]`<br>`[1 0 0]` |

</details>


---


### Object: `MoveAwayFromDamageSource`


**Definition:** Specifies the move ability used to flee from the source of damage, or an object with `move_ability`.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 1 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |

</details>


---


### Object: `MoveAwayWhenEnemyAdjacent`


**Definition:** Defines the movement behavior (move_ability, weights, and whether it triggers once per turn) when an enemy is adjacent.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 1 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |
| `once_per_turn` | Boolean | If true, the movement away can only trigger once per turn. | 1 | `true` |
| [`weights`](./Arrays.md#array-weights) | Array / Enum  | Specifies the weight array or named preset for the crazy eye background AI. | 1 | `[0 0 1]`<br>`[0 1 0]`<br>`[1 0 0]` |

</details>


---


### Object: `MoveForBarrage`


**Definition:** Defines an AI virtual ability that moves the unit to a position suitable for a barrage ability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `MoveForDash`


**Definition:** Defines an AI virtual ability that moves the unit into position for a dash attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `MoveForGrass`


**Definition:** Defines an AI virtual ability that moves the unit to stomp and eat grass.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `MoveForPounce`


**Definition:** Defines an AI virtual ability that moves the unit into position for a pounce attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `MoveForSpin`


**Definition:** Defines an AI virtual ability that moves the unit to set up a spin throw.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `MoveOneForPuke`


**Definition:** Defines an AI virtual ability that moves the unit one step for a puke ability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `MoveSpaced`


**Definition:** Defines an AI virtual ability that moves the unit while maintaining a specific distance.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `MoveToHead`


**Definition:** Defines an AI virtual ability that moves the unit to the head of a target to grab it.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `MoveTowards`


**Definition:** Defines an AI virtual ability that moves the unit toward its target.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `MultiSpawnOnDeath`


**Definition:** Specifies the object to spawn and the range of number of objects to spawn on death.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`obj`](./Arrays.md#array-obj) | Array / Enum  | Specifies one or more object names to bounce towards the target. | 1 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |
| [`count`](./Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `NCGravecrawlFAR`


**Definition:** Defines an AI virtual ability that makes a NecroCat gravecrawl while staying far from enemies.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `NoEyes`


**Definition:** Defines a form with no eyes animation.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


---


### Object: `NormalFull`


**Definition:** As an object, defines the normal full form with a spit attack and conditional form change. As an integer, specifies alt graphics index.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `NoStick`


**Definition:** Defines a form without a stick, using a jab attack with pattern AI.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |

</details>


---


### Object: `Nothing`


**Definition:** Defines the behavior when nothing is captured, typically just an animation.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#object-mothertumorspawnincapture)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `Obey`


**Definition:** As an object, defines an obey form that disables attacks and reacts with TV off. As an integer, defines a value (e.g., weight or count).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Off`


**Definition:** Defines an off form with a 'Off' animation suffix.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |

</details>


---


### Object: `OffScreen`


**Definition:** Defines an off-screen form that does not take turns and drops in chaos heads.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag`

</details>


---


### Object: `OneEye`


**Definition:** Defines a form with one eye that triggers an ability at 40% health threshold.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Open`


**Definition:** Defines an open form with increased movement and a specific attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `OpenCat`


**Definition:** Defines an open cat form that changes when the Consuming status is active.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `other_form_change_abilities`


**Definition:** An object mapping form names to the other character's form change abilities.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossSyncAnimations`](./Characters_and_Bosses.md#object-finalbosssyncanimations)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Boris`](./Miscellaneous.md#object-boris) | Enum / Object  | Specifies the 'Boris' form within FormChanger, with its own animation suffix and passives. | 1 | `{ . . . }`<br>`MegaGuppy_TransformBoris` |
| [`Explosive`](./Miscellaneous.md#object-explosive) | Enum / Object  | Specifies the 'Explosive' form within FormChanger, with its own animation suffix and passives. | 1 | `{ . . . }`<br>`MegaGuppy_TransformExplosive` |
| [`Holy`](./Passives_and_Statuses.md#object-holy) | Enum / Object  | Specifies the 'Holy' form within FormChanger, with its own animation suffix and passives. | 1 | `{ . . . }`<br>`MegaGuppy_TransformHoly` |

</details>


---


### Object: `Out`


**Definition:** Defines a form that is 'out' with a ground flopper movement passive.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `PassiveWhenAffectedByElement`


**Definition:** An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 18 | `Electric`<br>`Fire`<br>`Gravity` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 30 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 18 | `{ . . . }` |

</details>


---


### Object: `PassiveWhenDead`


**Definition:** Passive effects that remain active while the unit is dead.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `Possessing`


**Definition:** Form state when the unit is possessing another entity.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Primed`


**Definition:** Form state representing the unit being primed, with specific attack and AI behavior.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Pulp2`


**Definition:** Form state for the second stage of pulping, with no attacks or movement.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Pulp3`


**Definition:** Form state for the third stage of pulping, with no attacks or movement.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Pulp4`


**Definition:** Form state for the fourth stage of pulping, with no attacks or movement.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Pulp5`


**Definition:** Form state for the fifth stage of pulping, with no attacks or movement.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Pulp6`


**Definition:** Form state for the sixth stage of pulping, with no attacks or movement.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Pulp7`


**Definition:** Form state for the seventh stage of pulping, with no attacks or movement.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer   | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `uifloaters_offset` | Float | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 | `.5`<br>`1`<br>`1.3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `RandomStatusFromPool`


**Definition:** A collection of status effects; one is randomly chosen and applied to the target.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ally_rewards`](./Characters_and_Bosses.md#object-ally_rewards)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 31 | passives<br>class<br>	ag |
| [`StatusGroup`](./Passives_and_Statuses.md#object-statusgroup) | Object  | A container grouping multiple status effects to be applied simultaneously. | 3 | `{ . . . }` |

</details>


---


### Object: `ReturnA`


**Definition:** Defines an AI virtual ability that makes a HangerBot return to a close position.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `RevengeDamage`


**Definition:** An object defining the damage and effects that trigger when the unit is attacked.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 8 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 5 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`knockback`](./Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 3 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |

</details>


---


### Object: `round_start_bonusturn_pattern`


**Definition:** The action sequence the AI executes at the start of the round as a bonus turn.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_priority`](./Arrays.md#array-do_priority) | Array | The list of abilities the AI executes, evaluating them in order of highest priority. | 1 | `[ attack]`<br>`[**DestroyerThrowShield DestroyerHolyAttack]`<br>`[**DestroyerThrowShield attack]` |

</details>


---


<details>
<summary><b>AddStatusToReceivedDamage</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>AddStatusToSpells</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>AddStatusToTrampleDamage</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>PassiveWhenDead</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 8 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>StatusOnEnemyConfused</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>	ag |

</details>
<details>
<summary><b>StatusOnSpawnIn</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>	ag |

</details>


### Object: `RunFar`


**Definition:** Defines an AI virtual ability that makes the unit run far away.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `RunWhenLastPlayerCatIsCharmed`


**Definition:** Defines the behavior (including mid-turn decision allowance and legacy save key) for fleeing when the last player cat is charmed.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean | If true, allows the decision to run to occur mid-turn instead of at the end. | 1 | `true` |
| [`legacy_savekey`](./Enums.md#enum-legacy_savekey) | Enum | Specifies the save key used to persist a legacy stolen cat ID. | 1 | `Legacy_Marshmallow_StolenCatID` |

</details>


---


### Object: `ScalingAttackAnimation`


**Definition:** Maps attack animations to damage thresholds; when the unit's attack stat reaches a threshold, the corresponding animation overrides the default.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`default`](./Miscellaneous.md#object-default) | Enum / Object  | The default configuration or value used when no specific override is provided. | 1 | `{ . . . }`<br>`bite1` |
| [`thresholds`](./Arrays.md#array-thresholds) | Array | An array of health percentage thresholds that trigger an alt state. | 1 | `[` |

</details>


---


### Object: `SharePickups`


**Definition:** If 1 or an object with include_coins, makes the unit share pickups with nearby allies.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_coins` | Boolean | If true, coins are included in the shared pickup pool. | 1 | `true` |

</details>


---


### Object: `Sitting`


**Definition:** Form state where the unit is sitting, with no movement or attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `SkipFirstRounds`


**Definition:** Determines the number of initial rounds to skip and the chance per round of 'popping' (becoming active).
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pop_chance` | Integer | The percentage chance that the first round is skipped. | 1 | `50%` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `SmallHolding`


**Definition:** Form state when the unit is holding a small object, triggering a form change while consuming.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `SmallHoldingCat`


**Definition:** Form state when the unit is holding a cat, triggering a form change while consuming.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `SpawningPhase`


**Definition:** Form state for the spawning phase, where the unit is immobile and cannot take turns.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `SpewerAltGraphics`


**Definition:** Maps different Spewer liquid types (Normal, Fire, Tar) to their corresponding alternate graphic indices.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Fire`](./Passives_and_Statuses.md#object-fire) | Integer / Object  | Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack. | 1 | `{ . . . }`<br>`1` |
| [`FireFull`](./Miscellaneous.md#object-firefull) | Integer / Object  | Defines the 'FireFull' form, a fully charged fire state with its own animation and visual combo. | 1 | `{ . . . }`<br>`1` |
| [`Normal`](./Miscellaneous.md#object-normal) | Integer / Object  | The normal form configuration, used as a baseline state for shape-shifting units. | 1 | `{ . . . }`<br>`0` |
| [`NormalFull`](./Miscellaneous.md#object-normalfull) | Integer / Object  | As an object, defines the normal full form with a spit attack and conditional form change. As an integer, specifies alt graphics index. | 1 | `{ . . . }`<br>`0` |
| [`Tar`](./Miscellaneous.md#object-tar) | Integer / Object  | If an integer, the number of tar stacks. If an object, the form state for the tar-covered unit. | 1 | `{ . . . }`<br>`2` |
| [`TarFull`](./Miscellaneous.md#object-tarfull) | Integer / Object  | If an integer, the number of full tar stacks. If an object, the form state for the fully tar-covered unit. | 1 | `{ . . . }`<br>`2` |

</details>


---


### Object: `StacyMutant_Brace`


**Definition:** A passive group granting the Brace ability and cosmetic changes.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | `1`<br>`10`<br>`2` |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StacyMutant_Counter`


**Definition:** A passive group granting a counter attack and a bleed effect on basic attacks.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 1 | `{ . . . }` |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| [`CounterAttack`](./Passives_and_Statuses.md#object-counterattack) | Array / Enum / Object  | Specifies the ability used when the unit counterattacks after being hit. | 1 | `{ . . . }`<br>`BungaSwipe`<br>`CloakerHex`<br>`CollectiveCounter` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StacyMutant_Damage`


**Definition:** A passive group increasing damage and decreasing max health with cosmetic changes.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| `AddDamage` | Integer | The amount of damage added to all attacks. Negative values reduce damage. | 1 | `-1`<br>`1`<br>`2` |
| `AddMaxHealth` | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 1 | `-25`<br>`10`<br>`2` |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StacyMutant_DoubleHead`


**Definition:** A passive group granting an extra dispersed turn and cosmetic changes.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| `ExtraDispersedTurns` | Integer | The number of additional or fewer turns in the dispersed turn order. | 1 | `-1`<br>`1` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StacyMutant_Fire`


**Definition:** A passive group granting fire immunity and a lava shot basic attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 1 | `Creep`<br>`Electric`<br>`Fire` |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum  | Specifies the ability ID that replaces the unit's basic attack. | 1 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`ReplaceBrain`](./Passives_and_Statuses.md#object-replacebrain) | Object  | Defines a replacement AI brain and behavior pattern for the mutant. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StacyMutant_Health`


**Definition:** A passive group increasing max health, reducing speed, and scaling size.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| `AddMaxHealth` | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 1 | `-25`<br>`10`<br>`2` |
| `AddSpeed` | Integer | The amount of speed added (or subtracted) to the unit. | 1 | `-3`<br>`4`<br>`6` |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| `SizeScale` | Float | The multiplier applied to the unit's visual and hitbox size. | 1 | `.4`<br>`.6`<br>`.7` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StacyMutant_Holy`


**Definition:** A passive group granting a divine shield and cosmetic changes.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StacyMutant_Ice`


**Definition:** A passive group granting ice immunity and an ice breath basic attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| `AddMovement` | Integer | The amount of bonus movement points added to the unit's base movement. | 1 | `-1`<br>`-2`<br>`1` |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 1 | `Creep`<br>`Electric`<br>`Fire` |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum  | Specifies the ability ID that replaces the unit's basic attack. | 1 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`ReplaceBrain`](./Passives_and_Statuses.md#object-replacebrain) | Object  | Defines a replacement AI brain and behavior pattern for the mutant. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StacyMutant_Lightning`


**Definition:** A passive group granting electric immunity and a lightning dash basic attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 1 | `Creep`<br>`Electric`<br>`Fire` |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum  | Specifies the ability ID that replaces the unit's basic attack. | 1 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`ReplaceBrain`](./Passives_and_Statuses.md#object-replacebrain) | Object  | Defines a replacement AI brain and behavior pattern for the mutant. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StacyMutant_Mirror`


**Definition:** A passive group granting projectile reflection and random magic missile each turn.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| [`ReflectProjectiles`](./Passives_and_Statuses.md#object-reflectprojectiles) | Integer / Object  | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 1 | `{ . . . }`<br>`1`<br>`10%`<br>`100%` |
| [`StatusEachTurnEndForEachTurn`](./Passives_and_Statuses.md#object-statuseachturnendforeachturn) | Object  | Statuses applied at the end of each turn, with the number of turns as nested values. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StacyMutant_Speed`


**Definition:** A passive group increasing speed, reducing damage, and scaling size.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| `AddDamage` | Integer | The amount of damage added to all attacks. Negative values reduce damage. | 1 | `-1`<br>`1`<br>`2` |
| `AddSpeed` | Integer | The amount of speed added (or subtracted) to the unit. | 1 | `-3`<br>`4`<br>`6` |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| `SizeScale` | Float | The multiplier applied to the unit's visual and hitbox size. | 1 | `.4`<br>`.6`<br>`.7` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StacyMutant_Thorns`


**Definition:** A passive group granting thorns damage and cosmetic changes.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `Standing`


**Definition:** Form state where the unit is standing, with default movement and attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Standing2`


**Definition:** Form state where the unit is standing with a jumping movement ability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Start_Ceiling`


**Definition:** Form state for starting on the ceiling, with a form change trigger when entering the map.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `StatusAfterXTurns`


**Definition:** Applies a status effect or forces an ability usage after a set number of turns.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 2 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |

</details>


---


### Object: `StatusEachTurnBeginIfHasStatus`


**Definition:** Defines a status effect to apply (and optionally consume) at the start of each turn if the character already has a specific status, with a specified animation.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `consume` | Boolean | If true, the status is consumed after triggering. | 1 | `true` |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusEachTurnEndForEachTurn`


**Definition:** Statuses applied at the end of each turn, with the number of turns as nested values.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StacyMutant_Mirror`](./Characters_and_Bosses.md#object-stacymutant_mirror)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| `RandomMagicMissile` | Integer | The number of random magic missiles fired, or an object defining its properties. | 3 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusEachTurnEndIfEnabledAtStartOfTurn`


**Definition:** Defines an ability to force-use at the end of each turn if the character was in the specified form at the start of the turn.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |

</details>


---


### Object: `StatusOnDie`


**Definition:** Specifies status effects or actions triggered when the unit dies.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>	ag |
| `RemoveAmbientLightEffects` | Integer | The fade-out duration in seconds for ambient light effects. | 1 | `.5`<br>`4` |
| [`RemoveGlobalModifiers`](./Arrays.md#array-removeglobalmodifiers) | Array  | List of global modifier names to remove upon death. | 1 | `[BloodRain]` |

</details>


---


### Object: `StatusOnEndMove`


**Definition:** Specifies status effects or actions triggered when the unit finishes moving.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusOnEnemyConfused`


**Definition:** Defines an ability to immediately use when an enemy becomes confused.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusOnGainCoins`


**Definition:** Specifies status effects applied when this unit gains coins.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>	ag |
| [`BackflipWhenTargeted`](./Passives_and_Statuses.md#object-backflipwhentargeted) | Object  | The number of backflip charges, or an object defining its ability. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOverlappingCharactersAndDie`


**Definition:** Defines a status effect applied to overlapping characters, after which the character dies.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| `Poison` | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusWhenStatusCompletelyRemoved`


**Definition:** Defines a status to apply and an ability to use when a specific status is completely removed from the character.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`UseAbility`](./Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. | 1 | `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `Stop`


**Definition:** If an integer, the number of turns the unit is stopped. If an object, the form configuration for the stopped state.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `SuckMF`


**Definition:** Defines an AI virtual ability that makes a Tormentor suck enemies carelessly while keeping distance.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 1 | `always_cast`<br>`always_cast_careless`<br>`angry` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `SupportDieInsteadOfRun`


**Definition:** Configures alternative dying and dead animations for support units that die instead of fleeing.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_dead_ani`](./Enums.md#enum-alt_dead_ani) | Enum | Specifies the alternative death animation to use when the support unit dies instead of running. | 1 | `off` |
| [`alt_dying_ani`](./Enums.md#enum-alt_dying_ani) | Enum | Specifies the alternative dying animation to use. | 1 | `shutdown` |

</details>


---


### Object: `SwimmingFormChange`


**Definition:** Defines the form names to switch to when in water and when exiting water.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_in`](./Enums.md#enum-form_in) | Enum | Determines the form to change into when entering water. | 1 | `Water` |
| [`form_out`](./Enums.md#enum-form_out) | Enum | Determines the form to change into when leaving water. | 1 | `Out` |

</details>


---


### Object: `SwitchMusic`


**Definition:** Defines a new song or layer for the background music.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossBecomeTheChild`](./Characters_and_Bosses.md#object-finalbossbecomethechild)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | Specifies the music layer to switch to (e.g., 'event', 'battle', 'map'). | 7 | `battle`<br>`event`<br>`map` |
| [`new_song`](./Enums.md#enum-new_song) | Enum | Specifies the song to switch to; 'same' keeps the current song playing on the new layer. | 6 | `same` |

</details>


---


### Object: `SwordAndShield`


**Definition:** Form state with sword and shield, using the DestroyerAttack ability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `SwordAndShield_Primed`


**Definition:** Primed form state of SwordAndShield with holy animation and no final boss shield.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `SyncFormsWithBuddy`


**Definition:** Specifies the form to revert to if the character has no buddy, ensuring form synchronization.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`no_buddy`](./Enums.md#enum-no_buddy) | Enum | Specifies an alternative form to use when there is no buddy. | 1 | `Rage` |

</details>


---


### Object: `T3HitlerSpawningPhase`


**Definition:** Defines weighted groups of spawn abilities used during the T3Hitler boss's spawning phase.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spell_use_groups`](./Arrays.md#array-spell_use_groups) | Array | List of spell use groups that the spawning phase can use. | 1 | `[` |

</details>


---


### Object: `Tar`


**Definition:** If an integer, the number of tar stacks. If an object, the form state for the tar-covered unit.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `TarFull`


**Definition:** If an integer, the number of full tar stacks. If an object, the form state for the fully tar-covered unit.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Terminator2Run`


**Definition:** Defines the movement ability and movement weights used by Terminator2 when running away.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 1 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `TerminatorChase`


**Definition:** Defines the movement ability and reaction ability used by Terminator1 when chasing a target, plus whether it prioritizes player cats.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |

</details>


---


### Object: `TerminatorSkin`


**Definition:** Defines the status effect and groups of stacks applied by the Terminator's skin passive.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`groups`](./Arrays.md#array-groups) | Array | Groups of actors that this skin applies to. | 1 | `[` |

</details>


---


### Object: `TF_TargetAllies`


**Definition:** Defines an AI virtual ability that casts Twisting Flames targeting allies.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 1 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


---


### Object: `TF_TargetEnemies`


**Definition:** Defines an AI virtual ability that casts Twisting Flames targeting enemies.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 1 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


---


### Object: `Throb`


**Definition:** Form state for the Chaos unit's throb behavior, with a spread pattern.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |

</details>


---


### Object: `ThrobBubs`


**Definition:** Form state for Chaos unit throb that reacts with a shotgun attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `ThrobHost`


**Definition:** Form state for Chaos unit acting as host, reflecting projectiles.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `ThrobNettle`


**Definition:** Form state for Chaos unit with thorns and kinetic spikes that stack after enemy spells.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Transformed`


**Definition:** Form state after transformation, ending the turn on form switch.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag`

</details>


---


### Object: `TransformOnStatusThreshold`


**Definition:** Defines the status effect, the stack threshold at which to transform, and the object to transform into.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`threshold`](./Enums.md#enum-threshold) | Enum / Integer  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 1 | `"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |

</details>


---


### Object: `TVBotScreen`


**Definition:** Maps TVBot screen channel names to their corresponding form indices.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Die` | `Number` | If set, kills the target immediately. | 1 | `1`<br>`6` |
| [`Dumb`](./Miscellaneous.md#object-dumb) | Integer / Object  | Defines the 'Dumb' form, which can be either a numeric value or an object with passives that disable spells and turn off TV. | 1 | `{ . . . }`<br>`3` |
| `Fuck` | Integer | The number of times the TV bot screen displays the 'Fuck' message. | 1 | `5` |
| [`Obey`](./Miscellaneous.md#object-obey) | Integer / Object  | As an object, defines an obey form that disables attacks and reacts with TV off. As an integer, defines a value (e.g., weight or count). | 1 | `{ . . . }`<br>`1` |
| `Shit` | Integer | The number of times the TV bot screen displays the 'Shit' message. | 1 | `4` |
| [`Stop`](./Miscellaneous.md#object-stop) | Integer / Object  | If an integer, the number of turns the unit is stopped. If an object, the form configuration for the stopped state. | 1 | `{ . . . }`<br>`2` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `TwisterFling`


**Definition:** Defines the minimum distance, maximum distance, and damage for the TwisterFling ability.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `max_dist` | Integer | The maximum distance in tiles the target can be displaced by the knockback effect. | 1 | `2`<br>`20`<br>`3` |
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 1 | `2`<br>`3`<br>`4` |

</details>


---


### Object: `TwoEyes`


**Definition:** Form state with two eyes, triggering ability at a health threshold.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `Unflip`


**Definition:** Defines an AI virtual ability that teleports the unit to flip up and spin an enemy.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 | `AlienBeastPuke`<br>`CaveManPickupSpear`<br>`G3GrabHead` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `UnlimitedDeathRattleRevive`


**Definition:** Configures an unlimited revive effect, including the ability to use and whether it works even when stunned.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 1 | `true` |

</details>


---


### Object: `Unlit`


**Definition:** Form state for an unlit candle, muting demonic glyph display.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Unwashed`


**Definition:** Form state for the unwashed version of Johnny, with its own AI pattern.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |

</details>


---


### Object: `UseAbility`


**Definition:** The name of the ability the target is forced to use.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusWhenStatusCompletelyRemoved`](./Characters_and_Bosses.md#object-statuswhenstatuscompletelyremoved)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `respect_prime` | Boolean | If true, the ability will only be used if the unit is primed for it. | 2 | `true` |

</details>


---


### Object: `UseAbilityWhenOutOfStatus`


**Definition:** Defines an ability to execute when the unit no longer has a specified status.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |

</details>


---


### Object: `Washed`


**Definition:** Form state for the washed version of Johnny, with a blast attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `Washer`


**Definition:** Form state for the washer variant of a cultist, with basic melee attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer  | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

</details>


---


### Object: `ZealotBomb`


**Definition:** Form state for the bomb zealot variant, with an explosion attack.
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer  | Specifies an animation suffix for the current form, used to load different sprites. | 1 | `""`<br>`"0"`<br>`"1"` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>	ag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |

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