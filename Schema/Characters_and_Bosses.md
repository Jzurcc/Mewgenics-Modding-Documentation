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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2985 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 2609 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 2344 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1910 ||
| [`variant_of`](./Enums.md#enum-variant_of) | Enum | Indicates this ability is a variant of another named ability, inheriting its properties. | 1195 ||
| [`properties`](#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 600 ||
| [`stats`](#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 461 ||
| [`abilities`](#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 460 ||
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 459 ||
| [`sound`](#object-sound) | Object | A container object defining audio configurations, including alternate sound lists. | 62 ||
| [`distance_to_ally`](./Enums.md) | Number | The preferred distance (in tiles) to maintain from allies; negative values or 0 disable the preference. | 55 | 2 |
| [`distance_to_character`](./Enums.md) | Integer | The preferred distance (in tiles) to maintain from any character; negative values or 0 disable the preference. | 55 | 0 |
| [`distance_to_enemy`](./Enums.md) | Number | The preferred distance (in tiles) to maintain from enemies; negative values or 0 disable the preference. | 55 | 0 |
| [`face_closest_enemy`](./Enums.md) | Integer | If nonzero, the character will face the closest enemy. | 55 | 0 |
| [`preferred_distance`](./Enums.md) | Enum / Integer | The ideal distance to maintain from a target, expressed either as an absolute tile count or relative to movement (e.g., `mov+2`) or reach (`mov+reach`). | 55 | reach |
| [`total_distance_moved`](./Enums.md) | Number | The total distance the character has moved, used in movement weight calculations. | 55 | 0 |
| [`equipment`](#object-equipment) | Object | A container object defining the character's equipped items (head, face, neck, weapon, etc.). | 44 ||
| [`accurate_knockback`](./Enums.md) | Boolean | If true, knockback from attacks is applied accurately (e.g., straight line); if false, knockback may be erratic. | 32 | false |
| [`buff_ally`](./Enums.md) | Integer | The number of buffs applied to ally units. | 32 | 0 |
| [`buff_enemy`](./Enums.md) | Integer | The number of buffs applied to enemy units. Negative values may apply debuffs. | 32 | 0 |
| [`buff_self`](./Enums.md) | Integer | The number of buffs applied to the unit itself. Negative values may apply debuffs. | 32 | 0 |
| [`consider_overkill`](./Enums.md) | Boolean | If true, the AI considers overkill damage when evaluating actions. | 32 | false |
| [`consider_secondary_damage`](./Enums.md) | Boolean | If true, the AI considers secondary damage (e.g., splash) when evaluating actions. | 32 | false |
| [`consider_total_damage`](./Enums.md) | Boolean | If true, the AI considers total damage output (including secondary) when evaluating actions. | 32 | false |
| [`damage_ally`](./Enums.md) | Number | A multiplier for damage dealt to ally units. Negative values reduce damage. | 32 | 0 |
| [`damage_ally_corpse`](./Enums.md) | Integer | The amount of damage dealt to ally corpses. | 32 | 0 |
| [`damage_enemy`](./Enums.md) | Integer | The amount of damage dealt to enemy units. | 32 | 0 |
| [`damage_enemy_corpse`](./Enums.md) | Number | A multiplier for damage dealt to enemy corpses. | 32 | 0 |
| [`damage_self`](./Enums.md) | Number | A multiplier for damage dealt to the unit itself. | 32 | 2 |
| [`debuff_ally`](./Enums.md) | Number | A multiplier for debuffs applied to ally units. | 32 | 0 |
| [`debuff_enemy`](./Enums.md) | Integer | The number of debuffs applied to enemy units. | 32 | 0 |
| [`debuff_self`](./Enums.md) | Number | A multiplier for debuffs applied to the unit itself. | 32 | 2 |
| [`heal_ally`](./Enums.md) | Integer | The amount of health restored to ally units. | 32 | 0 |
| [`heal_enemy`](./Enums.md) | Integer | The amount of health restored to enemy units. Negative values deal damage. | 32 | 0 |
| [`heal_self`](./Enums.md) | Integer | The amount of health restored to the unit itself. Negative values deal damage. | 32 | 0 |
| [`kill_ally`](./Enums.md) | Integer | The chance (percentage) to instantly kill an ally unit. | 32 | 0 |
| [`kill_enemy`](./Enums.md) | Number | The chance (percentage or probability) to instantly kill an enemy unit. | 32 | 0 |
| [`negative_weight_scale`](./Enums.md) | Number | A multiplier applied to the weight of negative (penalty) decisions in AI calculations. | 32 | .99 |
| [`revive_ally_corpse`](./Enums.md) | Integer | The chance (percentage) to revive an ally corpse. | 32 | 0 |
| [`revive_enemy_corpse`](./Enums.md) | Integer | The chance (percentage) to revive an enemy corpse. Negative values may cause destruction. | 32 | 0 |
| [`spawn_object`](./Enums.md) | Integer | If non-zero, enables spawning of an object. The value may specify the number of objects. | 32 | 0 |
| [`spawn_object_distance_to_ally`](./Enums.md) | Number | The distance offset from ally units for spawned objects. Negative values move closer. | 32 | .0001 |
| [`spawn_object_distance_to_enemy`](./Enums.md) | Number | The distance offset from enemy units for spawned objects. | 32 | 0 |
| [`spend_mana_scale`](./Enums.md) | Number | A multiplier applied to mana cost when making decisions. | 32 | .99 |
| [`alt_spawn_pool`](#object-alt_spawn_pool) | Object | An alternative spawn pool defining possible objects to spawn with their weights. | 18 ||
| [`brain`](./Enums.md#enum-brain) | Enum | Specifies the AI brain type used for decision-making logic. | 5 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 5 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 5 ||
| [`scale`](./Enums.md#enum-scale) | Number | The scale multiplier applied to the unit's visual size. | 5 ||
| [`flat_cast_bonus`](./Enums.md) | Integer | A flat bonus added to the AI's cast chance evaluation. | 5 | 99999 |
| [`randomness`](./Enums.md) | Integer | The amount of randomness added to AI decision-making to avoid predictability. | 5 | 50 |
| [`cap_distance_to_ally`](./Enums.md) | Integer | The maximum distance the AI will maintain from ally units. | 4 | 2 |
| [`pattern`](#object-pattern) | Object | Defines a sequence of actions the AI will execute in order, with optional priority or all-in-one. | 3 ||
| [`consider_aoe`](./Enums.md) | Boolean | If true, the AI considers area-of-effect damage when evaluating actions. | 3 | false |
| [`danger_avoidance`](./Enums.md) | Number | A weight multiplier for the AI's tendency to avoid dangerous positions. | 3 | 20 |
| [`distance_to_aggro_target`](./Enums.md) | Integer | The preferred distance the AI tries to maintain from its aggro target. Negative values indicate behind. | 3 | -1 |
| [`distance_to_corpse`](./Enums.md) | Number | The preferred distance the AI tries to maintain from corpses. Negative values indicate moving towards. | 3 | 0 |
| [`simple`](./Enums.md) | Boolean | If true, the AI uses simplified decision-making logic. | 3 | true |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 ||
| `end_turn_on_formswitch` | Boolean | If true, the unit's turn ends immediately after switching forms. | 2 ||
| [`cap_distance_to_enemy`](./Enums.md) | Integer | The maximum distance the AI will maintain from enemy units. | 2 | 2 |
| [`distance_to_water`](./Enums.md) | Number | The preferred distance the AI tries to maintain from water tiles. Negative values indicate moving towards. | 2 | -1 |
| [`face_aggro_target`](./Enums.md) | Integer | A weight multiplier for the AI's tendency to face its aggro target. | 2 | 10 |
| [`spawn_object_preferred_distance`](./Enums.md) | Integer | The preferred distance from the unit at which objects are spawned. | 2 | 5 |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`ai_if_spawned_as_enemy`](#object-ai_if_spawned_as_enemy) | Object | Overrides the unit's AI settings when it is spawned as an enemy rather than an ally. | 1 ||
| `consider_spells` | Boolean | If true, the AI considers using spells in its decision-making. | 1 ||
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 ||
| [`cap_distance_to_character`](./Enums.md) | Integer | The maximum distance the AI will maintain from any character (ally or enemy). | 1 | 2 |
| [`cap_total_distance_moved`](./Enums.md) | Integer | The maximum number of tiles a unit can move before its movement is capped. | 1 | 1 |
| [`consider_aggro_target_enemy`](./Enums.md) | Boolean | If true, the AI considers the aggro target when determining movement or attack behavior. | 1 | true |
| [`count_nomove_in_eval`](./Enums.md) | Boolean | If true, the evaluation of a move includes the option of not moving. | 1 | false |
| [`distance_to_center`](./Enums.md) | Integer | The distance in tiles from the current position to the map center for AI evaluation. | 1 | -1 |
| [`exclude_characters_tagged`](./Enums.md) | Enum | Specifies a tag; characters with this tag are excluded from AI behavior targeting. | 1 | siren |
| [`face_camera`](./Enums.md) | Integer | If true, the spawned unit always faces the camera. | 1 | 1000 |
| [`lava`](./Enums.md) | Integer | A weight or priority value for preferring lava tiles in AI movement decisions. | 1 | 5 |
| [`tall_grass`](./Enums.md) | Integer | A weight or priority value for preferring tall grass tiles in AI movement decisions. | 1 | 5 |

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
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 517 ||
| [`movieclip`](./Enums.md#enum-movieclip) | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. | 461 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 409 ||
| `shadow_size` | Number | A multiplier for the size of the object's shadow relative to its default. | 151 ||
| [`scale`](./Enums.md#enum-scale) | Number | The scale multiplier applied to the unit's visual size. | 149 ||
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 149 ||
| [`custom_cat_data`](./Enums.md#enum-custom_cat_data) | Enum | Specifies a dataset or customization profile for cat graphics or behavior. | 127 ||
| [`water_mask`](./Enums.md#enum-water_mask) | Enum | Specifies the shape or size of the water reflection mask applied to the object. | 83 ||
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array | An array of alternative animation state replacements, each as [state, animation_name]. | 47 ||
| [`spawnin_animation`](./Strings.md#string-spawnin_animation) | Enum | Specifies the animation played when the unit spawns in. | 37 ||
| `piece_alt_frame` | Integer | The frame index from the graphical piece sheet to use as an alternative display frame. | 27 ||
| [`shadow`](./Enums.md#enum-shadow) | Enum | Specifies the visual shadow asset or type applied to the object. | 23 ||
| `move_speed_sync_frames` | Number | The number of animation frames used to synchronize the movement speed of the unit. | 20 ||
| `no_splatter` | Boolean | If true, prevents the blood splatter visual effect from appearing when the object spawns or is popped. | 17 ||
| [`projectile_spawn_offset`](./Arrays.md#array-projectile_spawn_offset) | Array | A pair of coordinates [x, y] defining the offset from the unit's origin where projectiles spawn. | 17 ||
| [`tint`](./Arrays.md#array-tint) | Array / Enum | A color tint applied to the object, either as an RGBA array [r, g, b, a] or a named color keyword. | 17 ||
| [`move_speed_multiplier`](./Enums.md#enum-move_speed_multiplier) | Number | A multiplier for the unit's base movement speed. | 16 ||
| `dont_sink` | Boolean | If true, the object does not sink into or clip with terrain or water surfaces. | 14 ||
| `art_flip` | Integer | Controls the horizontal flip of the art; -1 flips, 1 is normal. | 7 ||
| [`depth_offset`](./Enums.md#enum-depth_offset) | Number | An offset to the object's drawing depth, affecting its rendering order relative to other objects. | 6 ||
| `four_way_animations` | Boolean | If true, the unit uses separate animations for four facing directions. | 4 ||
| `show_infinity_damage_warning` | Boolean | If true, the game displays a warning when the unit has infinite damage potential. | 3 ||
| `always_huge_mask` | Boolean | If true, the unit always uses a large collision or visibility mask regardless of its actual size. | 2 ||
| [`default_attack_animation`](./Enums.md#enum-default_attack_animation) | Enum | Specifies the name of the default attack animation to use when no specific one is defined. | 2 ||
| [`desc`](./Strings.md#string-desc) | Enum | Specifies the localized description string for the item or ability. | 2 ||
| `shade_occluded_objects` | Boolean | If true, the object is drawn with a shade when occluded by other objects. | 2 ||
| `no_horizontal_flip` | Boolean | If true, the object's art is never flipped horizontally. | 1 ||
| [`override_portrait`](./Enums.md#enum-override_portrait) | Enum | Specifies a different portrait asset name to use instead of the default. | 1 ||
| `randomize_starting_frame` | Boolean | If true, the animation starts at a random frame instead of the first frame. | 1 ||
| `status_display_count_max` | Integer | The maximum number of status effect icons displayed on the unit's HUD. | 1 ||
| [`non_blocking_animations`](./Arrays.md#array-non_blocking_animations) | Array | A list of animation names that do not block gameplay or chain into new actions. | 1 ||

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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 2344 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 1787 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2039 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Contains status effects to add to the basic attack. | 133 ||
| [`FormChanger`](#object-formchanger) | Object | Defines the unit's form-changing data, including multiple form definitions and their sub-properties. | 106 ||
| [`Brace`](./Enums.md) | Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 94 | 99 |
| [`Trample`](./Enums.md) | Integer | The amount of bonus damage dealt when moving through an enemy. | 88 | 3 |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 65 | 2 |
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object | Defines the damage and effects applied back to a melee attacker upon being hit. | 59 ||
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 52 | 2 |
| [`StatusEachTurnEnd`](Cat_Mutations.md#object-statuseachturnend) | Object | Specifies status effects applied to the unit at the end of each of its turns. | 49 ||
| [`Robot`](#object-robot) | Integer / Object | If an integer 1, the unit is robotic and affected by electric/energized effects. If an object, contains further robot-specific properties. | 47 | 1 |
| [`ElementImmune`](./Enums.md) | Enum | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 39 | Ice |
| [`DeathRattle`](#object-deathrattle) | Enum / Object | Specifies an ability or effect triggered when the unit dies, optionally with a pop_corpse flag. | 35 | BBExplode |
| [`FormChangeWhileHasStatus`](#object-formchangewhilehasstatus) | Object | Defines a form change condition that activates while the unit has a specific status effect. | 35 ||
| [`CounterAttack`](Cat_Mutations.md#object-counterattack) | Array / Enum / Object | Specifies the ability used when the unit counterattacks after being hit. | 34 | [GSScream] |
| [`StatusImmunity`](./Enums.md) | Array / Enum | A list of status effect names the unit is immune to. | 34 | [Burn] |
| [`StatusOnKill`](Cat_Mutations.md#object-statusonkill) | Object | Specifies status effects or actions triggered when the unit kills an enemy. | 29 ||
| [`StatusOnTookDamage`](Cat_Mutations.md#object-statusontookdamage) | Object | Specifies status effects or actions triggered when the unit takes damage. | 29 ||
| [`SpawnThingOnDamage`](Cat_Mutations.md#object-spawnthingondamage) | Object | Specifies an object that spawns on the tile when the unit takes damage. | 28 ||
| [`ImmediateAbilityReaction`](#object-immediateabilityreaction) | Array / Enum / Object | Specifies an ability or list of abilities used immediately in reaction to a triggering event. | 26 | [ManglerFumbleEven] |
| [`Undead`](./Enums.md) | Integer | If set, flags the unit as undead (e.g., 1) with associated mechanics. | 25 | 1 |
| [`AbilityReaction`](#object-abilityreaction) | Enum / Object | Specifies the ability used as a reaction when the unit is targeted by an ability. | 23 | MoonWormCurl |
| [`SpawnOnDeath`](#object-spawnondeath) | Enum / Object | Specifies an object and its faction to spawn when the unit dies. | 21 | BiggestFood |
| [`AddMovement`](./Enums.md) | Integer | The amount of bonus movement points added to the unit's base movement. | 20 | 2 |
| [`BossRewards`](#object-bossrewards) | Object | Defines the common and rare item rewards dropped by a boss on defeat. | 20 ||
| [`BirdRewards`](#object-birdrewards) | Object | Defines the rewards and statuses applied when a bird allies with the unit. | 18 ||
| [`Buddy`](#object-buddy) | Enum / Object | Specifies a buddy unit that accompanies or is spawned alongside the unit, with optional reclaim and targeting properties. | 17 | Guillotina3Head |
| [`CharacterLightSource`](#object-characterlightsource) | Object | Defines a dynamic light source attached to the unit, including color, glow, and size. | 16 ||
| [`HealthPickup`](#object-healthpickup) | Object | Defines properties for a health pickup object, such as healing amount and visual frame range. | 16 ||
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 15 | 5 |
| [`RevengeDamage`](Abilities_and_Spells.md#object-revengedamage) | Object | An object defining the damage and effects that trigger when the unit is attacked. | 15 ||
| [`AddCorpseHealth`](./Enums.md) | Integer | The amount of bonus health the unit's corpse has before it can be resurrected. | 14 | -999 |
| [`AllStatsUp`](./Enums.md) | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 14 | 2 |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance the unit has to dodge incoming attacks. | 14 | 50 |
| [`InnateElement`](./Enums.md) | Enum | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 14 | Water |
| [`WaterWalk`](./Enums.md) | Integer | If greater than 0, allows the unit to traverse water tiles as if they were ground. | 14 | 1 |
| [`DeathRattleRevive`](#object-deathrattlerevive) | Enum / Object | Specifies an ability or effect that revives the unit upon death, with options for stunning behavior. | 13 | HCHumanDie |
| [`TransformOnDeath`](./Enums.md) | Array / Enum | Specifies the unit or list of units to transform into upon death. | 13 | [Hive] |
| [`AbilityHealthThreshold`](#object-abilityhealththreshold) | Object | Defines an ability and conditions for its activation when the unit's health reaches a threshold. | 12 ||
| [`NoHealthOnlyShield`](./Enums.md) | Integer | If set (e.g., 1), the unit has no health and only a shield for damage absorption. | 12 | 1 |
| [`ReflectProjectiles`](#object-reflectprojectiles) | Integer / Object | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 12 | 100 |
| [`SpawnThingOnDeath`](./Enums.md) | Enum | Specifies the name of an object to spawn upon death. | 12 | Boulder |
| [`MoveWhenDamaged`](Cat_Mutations.md#object-movewhendamaged) | Enum / Object | Defines movement behavior when the unit takes damage, such as weights and move ability. | 11 | move |
| [`CoinPickup`](./Enums.md) | Integer | The amount of coins awarded when this pickup is collected. | 10 | 4 |
| [`LimitDamage`](./Enums.md) | Integer | The maximum amount of damage the unit can take from a single hit. | 10 | 1 |
| [`MoveTowardsDamageSource`](#object-movetowardsdamagesource) | Enum / Object | Determines the movement behavior when moving towards the unit that dealt damage to it. | 10 | MoveOne |
| [`StripStatuses`](./Enums.md) | Integer | If 1, removes all status effects from the unit at the beginning of its turn. | 10 | 1 |
| [`AddTag`](./Enums.md) | Enum | Specifies a gameplay tag (e.g., 'rock', 'plant') to add to the unit, used for interaction checks. | 9 | fetus |
| [`BackstabImmunity`](./Enums.md) | Integer | If greater than 0, prevents the unit from taking extra damage from backstabs. | 9 | 1 |
| [`Flying`](./Enums.md) | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 9 | 1 |
| [`LimitHeal`](./Enums.md) | Integer | If 1, prevents the unit from being healed. | 9 | 0 |
| [`MissChance`](./Enums.md) | Integer | The flat percentage chance that the unit's attacks will miss. | 9 | 20 |
| [`MovementReaction`](#object-movementreaction) | Object | Specifies an ability to cast when a unit moves within range, with options for targeting and conditions. | 9 ||
| [`PoisonThorns`](./Enums.md) | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 9 | 3 |
| [`SmallRockBehavior`](#object-smallrockbehavior) | Integer / Object | Defines the damage, knockback, and chain properties of small rocks spawned from this unit when destroyed. | 9 | 0 |
| [`StatusCollector`](#object-statuscollector) | Object | Specifies the status effects and their stack counts that the unit collects to trigger transformations. | 9 ||
| [`TransformOnElementInfluence`](#object-transformonelementinfluence) | Object | Defines the element that triggers a transformation and the object to transform into. | 9 ||
| [`FadeInsteadOfDie`](./Enums.md) | Integer | If non-zero, the unit fades out instead of dying. | 8 | 1 |
| [`FormChangeOffMap`](#object-formchangeoffmap) | Object | Specifies the unit's form when off the map and when on the map. | 8 ||
| [`FormChangeOnElementInfluence`](#object-formchangeonelementinfluence) | Object | Defines the element that triggers a form change, optional visual effects, and the target form. | 8 ||
| [`PermanentMadness`](./Enums.md) | Integer | The number of permanent madness stacks applied. | 8 | 1 |
| [`Plant`](./Enums.md) | Integer | If set to 1, marks the unit as a Plant type, granting associated immunities and interactions. | 8 | 1 |
| [`RandomizeAIWeightsEachTurn`](./Enums.md) | Array | The range of random weights applied to AI actions each turn. | 8 | [chubs_and_nubs_blind] |
| [`StatusOnDie`](Cat_Mutations.md#object-statusondie) | Object | Specifies status effects or actions triggered when the unit dies. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 |
| [`AbilityWhenBuddyDies`](./Enums.md) | Enum | Specifies the ability to cast when a nearby allied unit dies. | 7 | Guillotina2Rage |
| [`AddElementsToBasicAttack`](./Enums.md) | Enum | Specifies an elemental damage type that is added to the unit's basic attacks. | 7 | Fire |
| [`AddInitiative`](./Enums.md) | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 7 | 999999 |
| [`AlphaTurns`](./Enums.md) | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 7 | 1 |
| [`ChanceToSpitOnDamage`](#object-chancetospitondamage) | Object | Configures the chance to use a spit ability when taking damage, including base chance and per-damage bonus. | 7 ||
| [`DebuffImmunity`](./Enums.md) | Integer | If 1, the unit is immune to debuffs. | 7 | 1 |
| [`MinimumKnockbackFromAllDamage`](./Enums.md) | Integer | The minimum knockback distance the unit will suffer from any damage source. | 7 | 1 |
| [`OverrideMaxHealth`](./Enums.md) | Integer | Replaces the unit's maximum health with this value. | 7 | 25 |
| [`SecurityBotProtect`](#object-securitybotprotect) | Object | Specifies the ability and movement used by a security bot to protect allies. | 7 ||
| [`SetSpellCosts`](./Enums.md) | Integer | Overrides the cost of all spells to this value. | 7 | 0 |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 7 | 2 |
| [`StatusOnEndMove`](Cat_Mutations.md#object-statusonendmove) | Object | Specifies status effects or actions triggered when the unit finishes moving. | 7 ||
| [`TransformInXTurns`](#object-transforminxturns) | Object | Defines a delayed transformation after a set number of turns, with optional target object and initiative handling. | 7 ||
| [`AddDamage`](./Enums.md) | Integer | The amount of damage added to all attacks. Negative values reduce damage. | 6 | 2 |
| [`CaveFamilyEnrage`](#object-cavefamilyenrage) | Object | Specifies the ability used when the number of family members with a given tag falls below a threshold. | 6 ||
| [`DelayedAutoRevive`](#object-delayedautorevive) | Object | Configures an automatic revival after a delay, with specified rounds and health percentage. | 6 ||
| [`Divide4OnDeath`](./Enums.md) | Enum | The object that spawns in four instances upon this unit's death. | 6 | MedSlime |
| [`DodgeChance_Status`](./Enums.md) | Integer | The flat percentage increase to dodge chance applied as a status effect. | 6 | 66 |
| [`FormChangeWhilePrimingAbility`](#object-formchangewhileprimingability) | Object | Defines the form changes when a specific ability is being primed and when it is not. | 6 ||
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 6 | 5 |
| [`IgnoreTiles`](./Enums.md) | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 6 | 1 |
| [`KaijuKnockbackImmune`](./Enums.md) | Integer | If 1, the unit is immune to knockback from kaiju sources. | 6 | 1 |
| [`StatusOnTookDamageFromAbility`](Cat_Mutations.md#object-statusontookdamagefromability) | Object | Specifies status effects triggered when the unit takes damage specifically from an ability (not environmental). | 6 ||
| [`StunImmunity`](#object-stunimmunity) | Integer / Object | If 1, the unit is immune to stun. The optional object configures whether to cleanse stun on apply. | 6 | 1 |
| [`TagGreed`](./Enums.md) | Enum | The tag of items that this unit will move towards to collect. | 6 | bishop_hat |
| [`TileTrail`](./Enums.md) | Enum | Specifies the type of tile left behind as the unit moves. | 6 | ShadowTile |
| [`YOffset`](./Enums.md) | Number | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 6 | -.18 |
| [`AddHiddenTag`](./Enums.md) | Enum | A hidden tag applied to the unit for internal logic and triggers. | 5 | hitler_clone_fetus |
| [`Angel`](./Enums.md) | Integer | If 1, the unit is an angel type, which may affect behavior like reviving. | 5 | 1 |
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Enum / Object | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 5 | SpiderReturn |
| [`Burn`](./Enums.md) | Integer | The amount of Burn applied, either as a fixed number or a formula string. | 5 | 2 |
| [`FaceShield`](./Enums.md) | Integer | If 1, the unit has a face shield that protects it from certain attacks or effects. | 5 | 0 |
| [`InjuryImmunity`](./Enums.md) | Integer | The number of turns the unit is immune to injuries. | 5 | 1 |
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit cannot be knocked back. | 5 | 1 |
| [`MoveTowardsKillers`](#object-movetowardskillers) | Enum / Object | Determines the movement behavior when moving towards units that have killed an ally. | 5 | ReaperRevenge |
| [`SharkySmellsBlood`](./Enums.md) | Integer | If 1, the unit is attracted to damaged units and may prioritize them. | 5 | 1 |
| [`StartOffMap`](./Enums.md) | Integer | If 1, the unit begins the encounter off the map. | 5 | 1 |
| [`TransformOnDeathImmediately`](#object-transformondeathimmediately) | Enum / Object | The object to transform into immediately upon death, with optional turn handling. | 5 | NoHead |
| [`AbilityAfterEnemyCastSpell_Stackable`](./Enums.md) | Enum | The ability to cast after an enemy spell, which can stack in effect. | 4 | ThornUp |
| [`AddMaxHealth`](./Enums.md) | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 4 | -25 |
| [`AddMeleeKnockback`](./Enums.md) | Integer | The amount of additional knockback dealt by melee attacks. | 4 | 2 |
| [`AddStatusToWeapons`](#object-addstatustoweapons) | Object | Specifies status effects to add to the unit's weapon attacks, with their stack counts. | 4 ||
| [`AddTemporaryEffectsToBasicAttack`](Cat_Mutations.md#object-addtemporaryeffectstobasicattack) | Object | A container object that lists temporary status effects applied to the unit's basic attack. | 4 ||
| [`Ammo`](./Enums.md) | Integer | The amount of ammo to add or remove (negative values subtract). | 4 | 3 |
| [`BackstabAllDirections`](./Enums.md) | Integer | If 1, the unit deals backstab damage from all directions. | 4 | 1 |
| [`BaitAura`](#object-baitaura) | Object | The range of the bait aura that draws enemies towards the unit. | 4 ||
| [`Bird`](./Enums.md) | Enum | The object dropped by this bird unit upon death. | 4 | CookedChickenLeg |
| [`BuffImmunity`](./Enums.md) | Integer | If 1, the unit is immune to buffs. An optional object can list buffs to exclude from immunity. | 4 | 1 |
| [`ChanceToBackflip`](Cat_Mutations.md#object-chancetobackflip) | Object | An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit. | 4 ||
| [`ChangeTileOnPop`](./Enums.md) | Enum | The type of tile that appears when this unit is destroyed. | 4 | OilTile |
| [`CountAsCorpse`](./Enums.md) | Integer | If 1, the unit counts as a corpse for interactions like raising or necromancy. | 4 | 1 |
| [`DisplayDangerAOE`](./Enums.md) | Enum | The ability whose area of effect is displayed to warn players. | 4 | TheChild_Wrath |
| [`ExtraDispersedTurns`](./Enums.md) | Integer | The number of additional or fewer turns in the dispersed turn order. | 4 | 1 |
| [`GroundFlopper`](./Enums.md) | Enum | The movement ability used when this unit is on the ground. | 4 | DefaultMove |
| [`LoopingSoundWhileAlive`](./Enums.md) | Enum | The looping sound effect played while the unit is alive. | 4 | Bomb_FuseLoop |
| [`PassiveWhenAffectedByElement`](Cat_Mutations.md#object-passivewhenaffectedbyelement) | Object | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 4 ||
| [`PassiveWhenDead`](#object-passivewhendead) | Object | Passive effects that remain active while the unit is dead. | 4 ||
| [`PrioritizeFarAwayTargets`](./Enums.md) | Integer | The weight for AI to prioritize targets based on distance; higher values favor farther targets. | 4 | 10 |
| [`StatusOnGainCoins`](#object-statusongaincoins) | Object | Specifies status effects applied when this unit gains coins. | 4 ||
| [`Trapper`](#object-trapper) | Object | Specifies a trap-placing ability and its targeting parameters. | 4 ||
| [`WeremanTransformationReceiver`](./Enums.md) | Enum | Determines which transformation animation or effect is applied when this unit is turned by a were-creature. | 4 | CaveWomanDropTransform |
| [`ArmorPickup`](#object-armorpickup) | Object | The amount of armor stacks and the frame range for the pickup animation. | 3 ||
| [`AbilityWhenTaggedCharacterMovesNear`](Cat_Mutations.md#object-abilitywhentaggedcharactermovesnear) | Object | An object containing `ability`, `tag`, and `range` that triggers the specified ability when a character with the given tag moves within range. | 3 ||
| [`AddStatusToSpells`](#object-addstatustospells) | Object | Specifies status effects added to all spell attacks used by this unit. | 3 ||
| [`AggroTargetIsCurrentTurn`](./Enums.md) | Integer | If set to 1, the unit's aggro target is the unit currently taking its turn. | 3 | 1 |
| [`BaseStatMultiply`](./Enums.md) | Number | A multiplier applied to the unit's base stats. | 3 | .5 |
| [`BonusTurnPattern`](./Enums.md) | Array | An array defining the pattern of bonus turns granted to this unit. | 3 | [0] |
| [`CanMutateTo`](./Enums.md) | Array / Enum | Specifies the mutation forms this unit can transform into, either a single form or an array of possible forms. | 3 | [Leaper] |
| [`DigestDeadBodies`](./Enums.md) | Enum | Specifies the ability or animation used when digesting a dead body. | 3 | MoonHead_Digest |
| [`ExtraMovePoints`](./Enums.md) | Integer | The number of additional movement points granted to this unit. | 3 | 1 |
| [`FormChangeHealthThreshold`](#object-formchangehealththreshold) | Object | Specifies health thresholds that trigger form changes, with form_below for health at or below and form_above for health above. | 3 ||
| [`ManaPickup`](#object-manapickup) | Object | The amount of mana stacks and the frame range for the pickup animation. | 3 ||
| [`MimicSpawnerAttacks`](./Enums.md) | Integer | If positive, the number of attacks mimicked; if -1, mimics all attacks from spawner. | 3 | -1 |
| [`MinimumKnockbackFromPhysicalAttacks`](./Enums.md) | Integer | The minimum knockback distance applied when hit by a physical attack. | 3 | 1 |
| [`MutateViaAbility`](./Enums.md) | Enum | Specifies the ability that triggers a mutation form change. | 3 | BBTransformMutant |
| [`PrioritizeHitDifferentTargets`](./Enums.md) | Integer | If set to 1, the unit's AI prioritizes hitting different targets rather than focusing one. | 3 | 1 |
| [`ProtectTargetedAllies`](#object-protecttargetedallies) | Object | Specifies the ability used to protect targeted allies, including an optional target filter. | 3 ||
| [`RandomPassivePool`](#object-randompassivepool) | Object | A pool of random passives from which one is chosen for this unit. | 3 ||
| [`RunInXTurns`](./Enums.md) | Integer | The number of turns after which this unit will flee the battle. | 3 | 2 |
| [`SharePickupsWithSpawner`](./Enums.md) | Integer | If set to 1, pickups collected by this unit are also given to its spawner. | 3 | 0 |
| [`SpawnCreepOnHit`](./Enums.md) | Integer | If set to 1, spawns creep on the tile when this unit takes damage. | 3 | 1 |
| [`StrengthUp`](./Enums.md) | Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 3 | 2 |
| [`SupportFormChangeInsteadOfRun`](#object-supportformchangeinsteadofrun) | Enum / Object | Specifies a form change to trigger instead of fleeing, either as a passive object with ability details or a direct form name. | 3 | Attacker |
| [`TileTrail_Ahead`](./Enums.md) | Enum | Specifies the type of tile to place one tile ahead of the unit's movement. | 3 | WaterTile |
| [`WeaponsDontLoseDurability`](./Enums.md) | Integer | If set to 1, weapons equipped by this unit do not lose durability. | 3 | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 ||
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 ||
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 ||
| [`AbilityOnRoundEnd`](#object-abilityonroundend) | Object | Specifies an ability that is automatically executed at the end of each round. | 2 ||
| [`AggroTargetIsBuddy`](./Enums.md) | Integer | If set to 1, the unit's aggro target is its buddy (linked partner). | 2 | 1 |
| [`AllDamageImmune_IncludingSpeculative`](./Enums.md) | Integer | If set to 1, this unit is immune to all damage, including speculative damage. | 2 | 1 |
| [`AlwaysHitDifferentTargets`](./Enums.md) | Integer | If set to 1, attacks always target different units, never the same target twice. | 2 | 1 |
| [`BungaEntrance`](#object-bungaentrance) | Object | Specifies the entrance animation, ability, and conditions for this unit's dramatic battle entrance. | 2 ||
| [`CCImmunity`](./Enums.md) | Integer | If set to 1, this unit is immune to crowd control effects. | 2 | 1 |
| [`CanShield`](./Enums.md) | Integer | If set to 1, this unit can generate shields. | 2 | 1 |
| [`ChanceToDisableActionsIfNotCharmed`](./Enums.md) | Integer | The percentage chance to disable actions of enemies that are not charmed. | 2 | 75 |
| [`ChangeTileOnDeath`](./Enums.md) | Enum | Specifies the tile type that replaces the current tile when this unit dies. | 2 | WaterTile |
| [`CherubimReaction`](#object-cherubimreaction) | Object | Specifies the abilities used when this unit leaves or returns to the battlefield. | 2 ||
| [`CreateGlobalModifiers`](Abilities_and_Spells.md#object-createglobalmodifiers) | Object | Defines global gameplay modifiers to activate. | 2 ||
| [`DemonicGlyphFrames`](./Enums.md) | Integer | The number of animation frames for the demonic glyph effect. | 2 | 1 |
| [`DiesToElement`](#object-diestoelement) | Enum / Object | Specifies the element that instantly kills this unit, optionally with an instant flag. | 2 | Wind |
| [`DissuadeInstakills`](./Enums.md) | Integer | If set to 1, this unit cannot be instantly killed. | 2 | 1 |
| [`ExpireOnSpawnerTurnEnd`](./Enums.md) | Integer | If set to 1, this unit is removed from battle at the end of its spawner's turn. | 2 | 1 |
| [`FaceLastDamage`](#object-facelastdamage) | Integer / Object | If set to 1, the unit turns to face the direction of the last damage received; an object can specify animation settings. | 2 | 1 |
| [`FinalBossShield`](./Enums.md) | Enum | Specifies the shield ability used by a final boss, or None for no shield. | 2 | None |
| [`FormChangeDuringWeatherElement`](#object-formchangeduringweatherelement) | Object | Specifies a form change that triggers when the weather matches a given element. | 2 ||
| [`FreePathfindElement`](./Enums.md) | Enum | Specifies a terrain element (e.g., Water, Grass) that the unit can pathfind through without penalty. | 2 | Water |
| [`GoopWalk`](./Enums.md) | Integer | If set to 1, this unit can move through goop tiles without being slowed or damaged. | 2 | 1 |
| [`ImmobilePassive`](./Enums.md) | Integer | If set to 1, this unit cannot move from its starting position. | 2 | 1 |
| [`InfiniteRebirth`](#object-infiniterebirth) | Object | Specifies the health and effects for unlimited rebirth upon death. | 2 ||
| [`KaijuWinCon`](./Enums.md) | Enum | Determines which kaiju victory condition is active for this unit. | 2 | zaratana |
| [`MagicDamageImmune`](./Enums.md) | Integer | If set to 1, this unit is immune to magic damage. | 2 | 1 |
| [`MamaCatAnimations`](./Enums.md) | Integer | If set to 1, enables special mama cat animations. | 2 | 1 |
| [`MiniVolcanoReaction`](./Enums.md) | Enum | Specifies the ability triggered when a mini volcano erupts near this unit. | 2 | ThrobShot_Reaction |
| [`MotherTumorSpawnInCapture`](#object-mothertumorspawnincapture) | Object | Specifies the form changes and statuses applied when the mother tumor spawns after capturing a cat or non-cat. | 2 ||
| [`MoveAwayFromDamageSource`](#object-moveawayfromdamagesource) | Object | Specifies the move ability used to flee from the source of damage, or an object with `move_ability`. | 2 ||
| [`PassiveWhileHasStatus`](Cat_Mutations.md#object-passivewhilehasstatus) | Object | An object containing `status` and `passives` that grants the listed passives while the unit has the specified status. | 2 ||
| [`PassiveWhileNotHasStatus`](#object-passivewhilenothasstatus) | Object | Specifies a set of passives that are active only when this unit does not have the given status. | 2 ||
| [`PrioritizeAggroTarget`](./Enums.md) | Integer | A priority weight for targeting the current aggro target. | 2 | 1 |
| [`PrioritizePlayerCats`](./Enums.md) | Integer | A priority weight for targeting player-controlled cats. | 2 | 1 |
| [`PrioritizeWeakestEnemy`](./Enums.md) | Integer | A priority weight for targeting the weakest enemy unit. | 2 | 1 |
| [`SafeDoomed`](./Enums.md) | Integer | The number of SafeDoomed stacks applied, or 'level' to scale with character level. | 2 | 1 |
| [`SharePickups`](#object-sharepickups) | Object | If 1 or an object with include_coins, makes the unit share pickups with nearby allies. | 2 ||
| [`SlotMachineRollPool`](#object-slotmachinerollpool) | Object | Defines the weighted pool of possible slot machine roll results. | 2 ||
| [`StatusAfterXTurns`](#object-statusafterxturns) | Object | Applies a status effect or forces an ability usage after a set number of turns. | 2 ||
| [`StatusOnSpawnIn`](#object-statusonspawnin) | Object | Applies statuses or actions upon the unit spawning into the battlefield. | 2 ||
| [`SurviveAt1HP`](./Enums.md) | Integer | If 1, the unit survives a fatal hit with 1 HP instead of dying. | 2 | 1 |
| [`TowerDefenseReflex`](./Enums.md) | Enum | Specifies the ability or attack used when the unit counterattacks in tower defense reflex mode. | 2 | attack |
| [`TransformOnElementInfluencex`](#object-transformonelementinfluencex) | Object | Transforms into a specified object when influenced by a given element. | 2 ||
| [`TransformWhenBuddyDies`](./Enums.md) | Enum | Specifies the form the unit transforms into when its buddy dies. | 2 | UltraOrnstein |
| [`UncappedHP`](./Enums.md) | Integer | If 1, the unit's maximum HP is not capped by standard limits. | 2 | 1 |
| [`UnlockOrientation`](./Enums.md) | Integer | If 1, allows the unit to freely rotate or face any direction regardless of movement. | 2 | 1 |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | The name of the ability the target is forced to use. | 2 | KirbySpit |
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 ||
| [`AbilityOnBattleStart_UseAI`](./Enums.md) | Enum | Specifies the ability the unit will use at the start of battle via AI resolution. | 1 | TheCreator_SpawnCloneTeam |
| [`AddStatusToReceivedDamage`](#object-addstatustoreceiveddamage) | Object | Applies a status effect to the attacker when the unit takes damage. | 1 ||
| [`AdvancedTint`](./Enums.md) | Array | An RGBA color array for advanced sprite tinting. | 1 | [0] |
| [`AdventureTokenPassivePool`](#object-adventuretokenpassivepool) | Object | A pool of passive definitions granted to the unit when picked up as an adventure token. | 1 ||
| [`AggroTargetIsGovernedByHitEffect`](#object-aggrotargetisgovernedbyhiteffect) | Object | If set, the aggro target is determined by the unit's hit effect, with a sub-key for enemies_only. | 1 ||
| [`AggroTargetIsLastEnemyThatDealtDamage`](./Enums.md) | Integer | If 1, the unit's aggro target is the last enemy that damaged it. | 1 | 1 |
| [`AggroTargetIsLowestHealthEnemyTillItDies`](./Enums.md) | Integer | If 1, the unit focuses the lowest health enemy until that enemy dies. | 1 | 1 |
| [`AggroTargetIsLowestMaxHealthCat`](./Enums.md) | Integer | If 1, the unit targets the cat ally with the lowest maximum health. | 1 | 1 |
| [`AlienBeastDangerZones`](./Enums.md) | Array | An array of ability names that mark dangerous zones for the Alien Beast fight. | 1 | [AlienBeastPuke] |
| [`AlienBeastEyeStalks`](./Enums.md) | Integer | The number of eye stalk segments on the Alien Beast. | 1 | 3 |
| [`AllSpellsCostActPoints`](./Enums.md) | Integer | If 1, all spells require action points instead of mana or other resources. | 1 | 1 |
| [`AllStatsAura`](#object-allstatsaura) | Object | An aura that grants bonus stacks of all stats to allies within range. | 1 ||
| [`AvoidDamagingCharmedEnemies`](./Enums.md) | Integer | If 1, the unit avoids dealing damage to charmed enemies. | 1 | 1 |
| [`AwardCoinsOnDeath`](./Enums.md) | Integer | The amount of coins awarded to the killer when this unit dies. | 1 | 10 |
| [`BasicAIDangerZone`](./Enums.md) | Integer | The radius of the danger zone used by the basic AI for area denial. | 1 | 2 |
| [`BattlefieldUniqueRandomPassive`](#object-battlefielduniquerandompassive) | Object | A pool of unique random passives that can be applied to each battlefield instance. | 1 ||
| [`BlackHolePassive`](./Enums.md) | Integer | If 1, the unit has black hole passive mechanics. | 1 | 1 |
| [`BloatEyePassive2`](./Enums.md) | Enum | Specifies the movement ability for the Bloat Eye enemy. | 1 | BloatEyeMovement2 |
| [`BlockAllDamage`](./Enums.md) | Integer | If 1, the unit blocks all incoming damage. | 1 | 1 |
| [`BombBehavior`](./Enums.md) | Integer | If 1, the unit explodes after a set duration or on death. | 1 | 1 |
| [`BungaCheers`](#object-bungacheers) | Object | Defines cheer particle effects and sounds triggered by ally or enemy actions. | 1 ||
| [`CapReceivedDamage`](./Enums.md) | Integer | If 1, the unit caps incoming damage to a maximum per hit. | 1 | 1 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 ||
| [`CerberubsAggroTargetBehavior`](#object-cerberubsaggrotargetbehavior) | Object | Defines the default and alert forms used by Cerberubs when changing aggro behavior. | 1 ||
| [`ChanceToFormChangeOnAbilityDamage`](#object-chancetoformchangeonabilitydamage) | Object | A chance to transform into a different form when damaged by an ability. | 1 ||
| [`ChaosBossFormChangeGuide`](#object-chaosbossformchangeguide) | Object | Defines active and passive piece sets and a health threshold for the Chaos boss's form change pattern. | 1 ||
| [`ChaosBossPieces`](#object-chaosbosspieces) | Object | Defines the list of active and passive piece tags for the Chaos boss fight. | 1 ||
| [`ChaosHeadDropIn`](#object-chaosheaddropin) | Object | Defines the tag, spawn ability, and music for the Chaos head's drop-in sequence. | 1 ||
| [`ConjureBonusAbility`](./Enums.md) | Enum | Specifies the name of the bonus ability to conjure. | 1 | random |
| [`CounterAttackAfterEnemyCastSpell`](./Enums.md) | Enum | Specifies the ability the unit uses to counterattack after an enemy casts a spell. | 1 | Telekinesis |
| [`CrowAttackLink`](./Enums.md) | Integer | If 1, allows this unit's attacks to chain or link to nearby enemies like a crow. | 1 | 1 |
| [`DamageFromBehindOnly`](./Enums.md) | Integer | If 1, the unit can only be damaged when attacked from behind. | 1 | 1 |
| [`DemonicGlyphStealer`](./Enums.md) | Integer | If 1, the unit can steal demonic glyphs from other units. | 1 | 1 |
| [`DiceBehavior`](#object-dicebehavior) | Object | Defines the dice size and knockback damage for the Dice enemy. | 1 ||
| [`DicerArt`](./Enums.md) | Array | An array of art offset values for the Dicer enemy. | 1 | [50] |
| [`DieWhenOnlyGolemsLeft`](./Enums.md) | Integer | If 1, the unit dies when only golem-type allies remain on the field. | 1 | 1 |
| [`DieWhenSpawnerDies`](./Enums.md) | Integer | If 1, the unit dies when its spawner unit dies. | 1 | 1 |
| [`DiesToPiercingAndSpikes`](#object-diestopiercingandspikes) | Object | Makes the unit take lethal damage from piercing attacks and spike terrain. | 1 ||
| [`DisableSpells`](./Enums.md) | Integer | If 1, the unit cannot cast spells. | 1 | 1 |
| [`Disguised`](./Enums.md) | Integer | If true, the unit is disguised, appearing as a different faction or model. | 1 | 1 |
| [`DisguisedTrapper`](./Enums.md) | Enum | Specifies the passive used when disguised as a trapper, e.g. FearMelee. | 1 | FearMelee |
| [`DisplayBuddyCatOnSpawn`](./Enums.md) | Integer | The number of buddy cat objects to display when the unit spawns. | 1 | 3 |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | 2 |
| [`DivineShieldPickup`](./Enums.md) | Integer | The number of divine shield charges granted on pickup. | 1 | 1 |
| [`DodgeChanceWithBlindSpot`](./Enums.md) | Integer | The percentage chance to dodge attacks while a blind spot condition is active. | 1 | 25 |
| [`DodgeWhenTargeted`](#object-dodgewhentargeted) | Object | An object defining the ability and effects triggered when the unit is targeted for an attack. | 1 ||
| [`DustCloudBehavior`](./Enums.md) | Integer | An integer flag that controls the behavior mode of a dust cloud entity. | 1 | 1 |
| [`Dybbuk1HPTracker`](./Enums.md) | Integer | A flag indicating the unit tracks that it has 1 HP remaining for Dybbuk possession mechanics. | 1 | 1 |
| [`DybbukPossessionFallback`](#object-dybbukpossessionfallback) | Object | An object specifying the fallback form and exit ability used when possession fails. | 1 ||
| [`ElectricArcs`](./Enums.md) | Integer | The number of electric arcs emitted by this unit. | 1 | 1 |
| [`ElementWeakness`](./Enums.md) | Enum | Determines which element the unit is weak to, e.g. Fire. | 1 | Fire |
| [`EnrageOnDamage`](./Enums.md) | Integer | If set to 1, the unit gains enrage stacks when taking damage. | 1 | 1 |
| [`EraseSpawnCoins`](./Enums.md) | Integer | If set to 1, the unit erases spawn coins from the map on spawn. | 1 | 1 |
| [`EventBounterHunterPassive`](./Enums.md) | Integer | A flag enabling the event bounty hunter passive behavior. | 1 | 1 |
| [`ExtraTurnsPerTaggedUnit`](./Enums.md) | Enum | Specifies the tag of units that grant extra turns when present. | 1 | sprout |
| [`FaceAwayLastDamage`](#object-faceawaylastdamage) | Object | An object defining animation overrides for the last damage event when the unit faces away. | 1 ||
| [`FinalBossBeamQueue`](#object-finalbossbeamqueue) | Object | An object defining the queue of beam ability actions for the final boss form. | 1 ||
| [`FinalBossBecomeTheChild`](#object-finalbossbecomethechild) | Object | An object defining the transformation and environment changes when the boss becomes TheChild. | 1 ||
| [`FinalBossHitCountdownBoris`](#object-finalbosshitcountdownboris) | Object | An object defining the countdown status effect properties for the Boris phase, including stacks, icons, and forced abilities. | 1 ||
| [`FinalBossHitCountdownExplosive`](#object-finalbosshitcountdownexplosive) | Object | An object defining the countdown status effect properties for the Explosive phase, including stacks, icons, and forced abilities. | 1 ||
| [`FinalBossHitCountdownHoly`](#object-finalbosshitcountdownholy) | Object | An object defining the countdown status effect properties for the Holy phase, including stacks and icons. | 1 ||
| [`FinalBossPupils`](#object-finalbosspupils) | Object | An object configuring the visual tracking of the final boss's pupils, including radius, head position, and teleport tracking. | 1 ||
| [`FinalBossShieldHealth`](#object-finalbossshieldhealth) | Object | An object defining the shield health thresholds per visual state for the final boss. | 1 ||
| [`FinalBossSyncAnimations`](#object-finalbosssyncanimations) | Object | An object defining animation synchronization with another character, including form change abilities. | 1 ||
| [`FlingObjectsOnTop`](./Enums.md) | Integer | The number of objects to fling on top of this unit. | 1 | 8 |
| [`FlushmasterCelebration`](./Enums.md) | Enum | Specifies the celebration animation or effect name used by the Flushmaster. | 1 | celebrate |
| [`ForceDodgeEverything`](./Enums.md) | Integer | If set to 1, the unit will always dodge all incoming attacks. | 1 | 1 |
| [`FormChangeWhenBuddyDies`](./Enums.md) | Enum | Specifies the form name the unit changes into when its buddy dies. | 1 | Rage |
| [`FullBlockEverything`](./Enums.md) | Integer | If set to 1, the unit fully blocks all incoming damage. | 1 | 1 |
| [`FullBlockEverythingTo0Damage`](./Enums.md) | Integer | If set to 1, the unit reduces all incoming damage to 0. | 1 | 1 |
| [`GasCanBehavior`](./Enums.md) | Integer | An integer flag that controls the behavior mode of a gas can entity. | 1 | 1 |
| [`GasCloudBehavior2`](./Enums.md) | Integer | An integer flag that controls a secondary behavior mode of a gas cloud entity. | 1 | 2 |
| [`GeminiTwin`](./Enums.md) | Integer | If set to 1, this unit is the twin in a Gemini pair. | 1 | 1 |
| [`GlobalManaDrainAura`](./Enums.md) | Integer | The amount of mana drained per turn from all units in range. | 1 | -1 |
| [`GoopImmunity`](./Enums.md) | Integer | If set to 1, the unit is immune to goop status effects. | 1 | 1 |
| [`GuillotinaDeathHead`](./Enums.md) | Integer | If set to 1, the unit spawns a head object upon death via guillotine. | 1 | 1 |
| [`HPAltStates`](#object-hpaltstates) | Object | An object defining alternate visual frames based on current HP thresholds. | 1 ||
| [`HarpoonTrapPassive`](./Enums.md) | Enum | Specifies the ability name used when the harpoon trap is triggered. | 1 | HarpoonTrapPull |
| [`HealNeighborsEachTurn`](#object-healneighborseachturn) | Object | An object defining the amount and target filtering for healing adjacent units each turn. | 1 ||
| [`HiddenDoomed`](./Enums.md) | Integer | The number of stacks of a hidden doomed status effect applied to the unit. | 1 | 2 |
| [`HitlerExecute`](#object-hitlerexecute) | Object | An object defining the tag, ability, and health threshold for executing a clone. | 1 ||
| [`IceBlockBehavior`](./Enums.md) | Integer | An integer flag that controls the behavior mode of an ice block entity. | 1 | 1 |
| [`IllusionTint`](./Enums.md) | Integer | If non-zero, applies an illusionary tint to the unit's sprite. | 1 | 1 |
| [`InheritSpawnerStats`](./Enums.md) | Integer | If set to 1, the unit inherits the stats of its spawner. | 1 | 1 |
| [`InsertIntoBackgroundPlaceholder`](./Enums.md) | Integer | If set to 1, the unit is inserted into a background placeholder slot. | 1 | 1 |
| [`JohnnyNeedsWashing`](#object-johnnyneedswashing) | Object | An object specifying the form names for washed and unwashed states. | 1 ||
| [`JohnnyWasher`](./Enums.md) | Enum | Specifies the ability name used by the washer form to clean Johnny. | 1 | BBTransformZealot |
| [`LegacySpawnSavedCatIfExists`](./Enums.md) | Enum | Specifies the legacy saved cat ID to spawn if it exists in the save data. | 1 | Legacy_Marshmallow_StolenCatID |
| [`LockOrientationFaceTile`](./Enums.md) | Array | A tile coordinate [x y] that the unit's orientation is locked to face. | 1 | [0] |
| [`ManglerMonsterPassive`](./Enums.md) | Enum | Specifies the ability name used for the Mangler monster's dash attack. | 1 | ManglerMonsterDashAttack |
| [`MegaDinoDropController`](#object-megadinodropcontroller) | Object | An object defining the abilities and stable leg count for the Mega Dino's leg drop sequence. | 1 ||
| [`ModularPickup`](#object-modularpickup) | Object | An object defining the effects and sounds triggered when the unit is picked up. | 1 ||
| [`MonkCatReactionAbilities`](#object-monkcatreactionabilities) | Object | A set of mappings from action types (move, attack, spell, trinket) to the corresponding ability IDs the MonkCat will use for reactions. | 1 ||
| [`MoonHeadCrackedVisual`](./Enums.md) | Enum | Specifies the visual state for the character's cracked head appearance. | 1 | Cracked |
| [`MotherGrowController`](#object-mothergrowcontroller) | Object | Controls the growth of tumors on The Mother, including the tumor object, damage type, damage amount, and whether it pierces defense when eating damage. | 1 ||
| [`MotherTumorPassive`](#object-mothertumorpassive) | Object | Defines the passive behavior for a MotherTumor, including the forms considered for pass/receive, the pass and receive animations, and the grow ability. | 1 ||
| [`Mount`](#object-mount) | Object | Defines the entering and ejecting abilities for a mountable unit, along with its death rattle ability. | 1 ||
| [`MoveAfterAnyAttemptedAttack`](#object-moveafteranyattemptedattack) | Object | Defines the movement behavior (weights and abilities) used after any attempted attack. | 1 ||
| [`MoveAwayWhenEnemyAdjacent`](#object-moveawaywhenenemyadjacent) | Object | Defines the movement behavior (move_ability, weights, and whether it triggers once per turn) when an enemy is adjacent. | 1 ||
| [`MultiSpawnOnDeath`](#object-multispawnondeath) | Object | Specifies the object to spawn and the range of number of objects to spawn on death. | 1 ||
| [`MulticatHeads`](./Enums.md) | Integer | The number of additional heads the Multicat has. | 1 | 0 |
| [`MutateAfterXTurns`](./Enums.md) | Integer | The number of turns after which the character automatically mutates (or transforms). | 1 | 3 |
| [`MuteDemonicGlyphDisplay`](./Enums.md) | Integer | If set to 1, suppresses the display of demonic glyphs on the character. | 1 | 1 |
| [`OrthogonalAIDangerZone`](./Enums.md) | Integer | The range (in tiles) for the AI's orthogonal danger zone detection. | 1 | 10 |
| [`PackHunting`](./Enums.md) | Integer | If set to 1, enables pack hunting behavior for the character. | 1 | 1 |
| [`Phasing`](./Enums.md) | Integer | If set to 1, allows the character to phase through solid objects or obstacles. | 1 | 1 |
| [`ReturnBoundItemOnBattleEnd`](./Enums.md) | Integer | If set to 1, items bound to this character are returned to their owner at the end of battle. | 1 | 1 |
| [`RunWhenKittensDead`](./Enums.md) | Integer | If set to 1, causes the character to attempt to flee when all associated kittens are dead. | 1 | 1 |
| [`RunWhenLastPlayerCatIsCharmed`](#object-runwhenlastplayercatischarmed) | Object | Defines the behavior (including mid-turn decision allowance and legacy save key) for fleeing when the last player cat is charmed. | 1 ||
| [`ScalingAttackAnimation`](#object-scalingattackanimation) | Object | Maps attack animations to damage thresholds; when the unit's attack stat reaches a threshold, the corresponding animation overrides the default. | 1 ||
| [`SkipFirstRounds`](#object-skipfirstrounds) | Object | Determines the number of initial rounds to skip and the chance per round of 'popping' (becoming active). | 1 ||
| [`SpawnCreepOnHitKnockback`](./Enums.md) | Integer | If set to 1, spawns creep on the tile where a hit knocks back an enemy. | 1 | 1 |
| [`SpawnerCatDataReference`](./Enums.md) | Integer | A reference ID pointing to the spawner cat's data, used by minions to link back to their spawner. | 1 | 1 |
| [`SpewerAltGraphics`](#object-speweraltgraphics) | Object | Maps different Spewer liquid types (Normal, Fire, Tar) to their corresponding alternate graphic indices. | 1 ||
| [`SpreadWater`](./Enums.md) | Integer | If set to 1, causes the character to spread water onto adjacent tiles. | 1 | 1 |
| [`SproutsGrantMovement`](./Enums.md) | Integer | If set to 1, sprouts on the character grant additional movement (aliases to MovementUp). | 1 | 1 |
| [`StartDead`](./Enums.md) | Integer | The percentage chance that the character starts the battle already dead. | 1 | 100 |
| [`StatusEachTurnBeginIfHasStatus`](#object-statuseachturnbeginifhasstatus) | Object | Defines a status effect to apply (and optionally consume) at the start of each turn if the character already has a specific status, with a specified animation. | 1 ||
| [`StatusEachTurnEndIfEnabledAtStartOfTurn`](#object-statuseachturnendifenabledatstartofturn) | Object | Defines an ability to force-use at the end of each turn if the character was in the specified form at the start of the turn. | 1 ||
| [`StatusOnEnemyConfused`](#object-statusonenemyconfused) | Object | Defines an ability to immediately use when an enemy becomes confused. | 1 ||
| [`StatusOverlappingCharactersAndDie`](#object-statusoverlappingcharactersanddie) | Object | Defines a status effect applied to overlapping characters, after which the character dies. | 1 ||
| [`StatusWhenStatusCompletelyRemoved`](#object-statuswhenstatuscompletelyremoved) | Object | Defines a status to apply and an ability to use when a specific status is completely removed from the character. | 1 ||
| [`SupportDieInsteadOfRun`](#object-supportdieinsteadofrun) | Object | Configures alternative dying and dead animations for support units that die instead of fleeing. | 1 ||
| [`SwimmingFormChange`](#object-swimmingformchange) | Object | Defines the form names to switch to when in water and when exiting water. | 1 ||
| [`SyncFormsWithBuddy`](#object-syncformswithbuddy) | Object | Specifies the form to revert to if the character has no buddy, ensuring form synchronization. | 1 ||
| [`T3HitlerSpawningPhase`](#object-t3hitlerspawningphase) | Object | Defines weighted groups of spawn abilities used during the T3Hitler boss's spawning phase. | 1 ||
| [`TVBotDisableAttack`](./Enums.md) | Integer | If set to 1, disables the TVBot's ability to attack. | 1 | 1 |
| [`TVBotDisableMove`](./Enums.md) | Integer | If set to 1, disables the TVBot's ability to move. | 1 | 1 |
| [`TVBotDisableSpells`](./Enums.md) | Integer | If set to 1, disables the TVBot's ability to use spells. | 1 | 1 |
| [`TVBotScreen`](#object-tvbotscreen) | Object | Maps TVBot screen channel names to their corresponding form indices. | 1 ||
| [`TakeWeaponFromSpawner`](./Enums.md) | Integer | If set to 1, the minion inherits the weapon from its spawner. | 1 | 1 |
| [`Tall`](./Enums.md) | Integer | If set to 1, the character occupies a taller hitbox or sprite space. | 1 | 1 |
| [`TallTumorManaBurn`](./Enums.md) | Enum | Specifies the mana burn ability used by the TallTumor. | 1 | TT_ManaBurn |
| [`Terminator2Chase`](./Enums.md) | Enum | Specifies the movement ability used by Terminator2 when chasing the target. | 1 | move |
| [`Terminator2Run`](#object-terminator2run) | Object | Defines the movement ability and movement weights used by Terminator2 when running away. | 1 ||
| [`TerminatorChase`](#object-terminatorchase) | Object | Defines the movement ability and reaction ability used by Terminator1 when chasing a target, plus whether it prioritizes player cats. | 1 ||
| [`TerminatorSkin`](#object-terminatorskin) | Object | Defines the status effect and groups of stacks applied by the Terminator's skin passive. | 1 ||
| [`TileElementDamageImmunity`](./Enums.md) | Enum | Determines which tile element type the character is immune to damage from. | 1 | Ice |
| [`TinkererBasicAttackSwitching`](Cat_Classes.md#object-tinkererbasicattackswitching) | Object | Defines the abilities used for the Tinkerer's basic attack switching mechanic. | 1 ||
| [`TireBehavior`](./Enums.md) | Integer | If set to 1, activates special tire-related behavior for the character. | 1 | 1 |
| [`TormentorHeal`](./Enums.md) | Integer | If set to 1, the Tormentor can heal itself. | 1 | 1 |
| [`TrackAmountKilledByPlayer`](./Enums.md) | Enum | Specifies the name of the counter used to track how many of this type the player has killed. | 1 | BonusBirdsKilled |
| [`TransformOnStatusThreshold`](#object-transformonstatusthreshold) | Object | Defines the status effect, the stack threshold at which to transform, and the object to transform into. | 1 ||
| [`TutorialBossRiggedFight`](./Enums.md) | Integer | The turn count at which the tutorial boss fight becomes rigged. | 1 | 16 |
| [`TwisterFling`](#object-twisterfling) | Object | Defines the minimum distance, maximum distance, and damage for the TwisterFling ability. | 1 ||
| [`UnlimitedDeathRattleRevive`](#object-unlimiteddeathrattlerevive) | Object | Configures an unlimited revive effect, including the ability to use and whether it works even when stunned. | 1 ||
| [`UpTireBehavior`](./Enums.md) | Integer | The behavior type integer for the Tire's upward form. | 1 | 5 |
| [`UseAbilityWhenOutOfStatus`](#object-useabilitywhenoutofstatus) | Object | Defines an ability to execute when the unit no longer has a specified status. | 1 ||
| [`UseAbilityWhenShieldDepleted`](./Enums.md) | Enum | The ability to use when the unit's shield is fully depleted. | 1 | T3Pebbles_PrimeBoulderDrop |
| [`Wall`](./Enums.md) | Integer | If 1, the unit is treated as an impassable wall. | 1 | 1 |
| [`WhitelistPickupType`](./Enums.md) | Enum | Specifies the type of pickup that this unit is allowed to collect. | 1 | food |
| [`WideBackstab`](./Enums.md) | Integer | The additional width for backstab attacks, in tiles. | 1 | 1 |
| [`WispDodge`](./Enums.md) | Integer | If 1, the unit gains the Wisp's dodge ability. | 1 | 1 |
| [`ZeroKnockbackDamage`](./Enums.md) | Integer | If 1, the unit takes no damage from knockback effects. | 1 | 1 |

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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 538 ||
| [`faction`](./Enums.md#enum-faction) | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 505 ||
| `health` | Integer | The maximum hit points of the unit. | 427 ||
| [`tag`](./Arrays.md#array-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 399 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 280 ||
| `movement` | Integer | The movement range of the unit in tiles per turn. | 277 ||
| [`corpse_health`](./Enums.md#enum-corpse_health) | Variable | The health of the unit's corpse after death; 'indestructible' means it cannot be destroyed. | 195 ||
| `inherit_faction` | Boolean | If true, the unit inherits the faction of its spawner or parent. | 115 ||
| `dispersed_bonus_turns` | Integer | The number of bonus turns granted to this unit when its turn order is dispersed. | 104 ||
| `base_mana_regen` | Integer | The base amount of mana regenerated per turn. | 90 ||
| [`size`](./Enums.md#enum-size) | Enum / Number | The scale factor (size multiplier) of the spawned unit. | 80 ||
| `shield` | Enum / Integer | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 74 ||
| [`move_block`](./Enums.md#enum-move_block) | Enum | Determines which movement directions are blocked. | 73 ||
| `kill_required` | Boolean | If true, the unit must be killed to complete the objective. | 69 ||
| `can_be_backstabbed` | Boolean | If true, the unit can be backstabbed. | 68 ||
| `initiative` | Enum / Integer | The unit's turn order priority; can be an integer modifier or 'keep_turns_end_turn' to force end of turn after acting. | 61 ||
| `takes_turns` | Boolean | If true, the unit participates in the turn order. | 61 ||
| `mana_regen` | Integer | The amount of mana regenerated per turn, overriding base_mana_regen if set. | 51 ||
| `mana` | Enum / Integer | The amount of mana required to cast, as a formula or stat. | 50 ||
| `flying` | Boolean | If true, the unit can fly over obstacles and is immune to ground effects. | 47 ||
| [`banned_elite_buffs`](./Arrays.md#array-banned_elite_buffs) | Array | A list of elite buff types that cannot be applied to this unit. | 45 ||
| [`hidden_tag`](./Arrays.md#array-hidden_tag) | Array / Enum | A tag used for internal categorization, not shown to the player. | 38 ||
| `weak_threshold` | Integer | The health threshold below which the unit is considered weakened. | 32 ||
| `knockback_immune` | Boolean | If true, the unit cannot be knocked back. | 25 ||
| `can_be_champion` | Boolean | If true, the unit can spawn as a champion variant. | 20 ||
| [`lock_orientation`](./Arrays.md#array-lock_orientation) | Array | Forces the unit's facing direction to a fixed vector. | 19 ||
| [`ai_scale`](./Enums.md#enum-ai_scale) | Number | A multiplier for the unit's AI decision-making weight. | 18 ||
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Specifies the layer on which the ability's effect operates (e.g., characters, tiles, gas). | 17 ||
| [`auto_run_priority`](./Enums.md#enum-auto_run_priority) | Enum | Determines the unit's auto-run behavior priority. | 16 ||
| `inanimate` | Boolean | If true, the unit is treated as an inanimate object. | 16 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 16 ||
| `disperse_main_turns` | Boolean | If true, the unit's main turns are dispersed across the turn order. | 15 ||
| [`hidden_tags`](./Arrays.md#array-hidden_tags) | Array / Enum | A list of hidden tags for internal grouping and behavior. | 14 ||
| [`tags`](./Arrays.md#array-tags) | Array / Enum | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 14 ||
| `evenly_dispersed_bonus_turns` | Integer | The number of bonus turns spread evenly across the turn order for this unit. | 13 ||
| `exclude_from_hallucinate` | Boolean | If true, the unit is not included in hallucination effects. | 13 ||
| `round_end_bonus_turns` | Integer | The number of bonus turns granted at the end of each round. | 13 ||
| `can_be_overkilled` | Boolean | If true, the unit can be overkilled. | 12 ||
| `can_collect_coins` | Boolean | If true, the unit can pick up coins. | 10 ||
| `deathpoof_size` | Integer | The size scale of the death poof effect when the unit dies. | 10 ||
| `dispersed_bonus_turns_consider_initiative` | Boolean | If true, dispersed bonus turns take the unit's initiative into account. | 10 ||
| `initial_health` | Integer | The starting health of the unit when spawned. | 10 ||
| [`held_coins`](./Arrays.md#array-held_coins) | Array / Integer | The number of coins the unit holds; can be a range [min max]. | 10 ||
| `can_eat_food` | Boolean | If true, the unit can consume food items. | 9 ||
| `can_grant_extra_turns` | Boolean | If true, the unit can grant extra turns to allies. | 8 ||
| `tall` | Boolean | If true, the unit occupies two vertical tiles. | 8 ||
| `dispersed_bonus_turns_before_cats` | Boolean | If true, the unit's dispersed bonus turns occur before the cat's turn order. | 7 ||
| `divine_shield` | Integer | The number of stacks of the Divine Shield status this mutation provides. | 7 ||
| `is_player_cat` | Boolean | If true, the unit is considered a player-controlled cat. | 7 ||
| `boss_minions_runaway` | Boolean | If true, the boss's minions will flee when the boss is defeated. | 6 ||
| `mana_matters` | Boolean | If true, the unit's mana is used for ability costs and mana regeneration. | 6 ||
| `access_to_player_inventory` | Boolean | If true, the unit can access and use items from the player's inventory. | 5 ||
| `act_points` | Integer | The number of action points required to use the ability. | 5 ||
| `takes_main_turn` | Boolean | If true, the unit consumes the main turn phase of the round. | 5 ||
| `visually_spiky` | Boolean | If true, the unit's sprite appears visually spiky for aesthetic purposes. | 5 ||
| `allow_passive_spelltransforming` | Boolean | If true, the unit can be transformed into spells via passive effects. | 4 ||
| `base_crit_chance` | Integer | The base critical hit chance for the unit. | 4 ||
| `last_turn_is_main_turn` | Boolean | If true, the unit's final turn in a round is treated as a main turn. | 4 ||
| `round_start_bonus_turns` | Integer | The number of extra turns the unit gains at the start of each round. | 4 ||
| `view_bleeding_characters_as_enemies` | Boolean | If true, the unit treats any bleeding character as an enemy. | 4 ||
| [`aoe_pierce_mode`](./Enums.md#enum-aoe_pierce_mode) | Enum | Specifies the area-of-effect piercing behavior for projectiles. | 3 ||
| `base_initiative` | Integer | The unit's base initiative, used for turn order determination. | 3 ||
| `base_movement` | Integer | The unit's base movement range in tiles. | 3 ||
| `catdata_ignore_skills` | Boolean | If true, the unit ignores its cat data skills. | 3 ||
| [`disallow_items`](./Enums.md#enum-disallow_items) | Enum | Determines which items the unit is prohibited from using. | 3 ||
| `always_triggers_traps` | Boolean | If true, the unit always activates traps upon stepping on them. | 2 ||
| `base_health` | Integer | The unit's base maximum health. | 2 ||
| `base_health_regen` | Integer | The amount of health the unit regenerates per turn. | 2 ||
| `base_initial_mana` | Integer | The amount of mana the unit starts with at the beginning of a mission. | 2 ||
| `base_mana` | Integer | The unit's base maximum mana. | 2 ||
| `blocking` | Boolean | If true, the unit blocks movement and line-of-sight. | 2 ||
| `can_be_elite` | Boolean | If true, the unit can spawn as an elite variant. | 2 ||
| `can_run` | Boolean | If true, the unit can use the run command to flee from battle. | 2 ||
| `champion` | Boolean | If true, the unit is a champion variant with boosted stats. | 2 ||
| `force_not_familiar` | Boolean | If true, the unit cannot be used as a familiar. | 2 ||
| `hint_no_corpse` | Boolean | If true, the unit does not leave a corpse when defeated. | 2 ||
| `must_start_facing_camera` | Boolean | If true, the unit must be placed facing the camera at the start of a mission. | 2 ||
| `tile_desire_cost` | Integer | The cost modifier for the unit's desire to move onto a tile. | 2 ||
| `uncapturable` | Boolean | If true, the unit cannot be captured. | 2 ||
| `aggro_target_is_enemy` | Boolean | If true, the unit's aggression target is considered an enemy. | 1 ||
| `allow_flying_effect` | Boolean | If true, the unit can be affected by flying mechanics. | 1 ||
| `allow_offmap_corpse` | Boolean | If true, the unit can leave a corpse if defeated off the map. | 1 ||
| `allow_replacebrain` | Boolean | If true, the unit can have its brain replaced via certain abilities. | 1 ||
| `always_face_forward` | Boolean | If true, the unit always faces forward regardless of direction. | 1 ||
| `capture_as_cat` | Boolean | If true, the unit is captured as a cat rather than an object. | 1 ||
| `elite` | Boolean | If true, the unit is an elite variant with enhanced abilities. | 1 ||
| `first_turn_is_main_turn` | Boolean | If true, the unit's first turn in a round is treated as a main turn. | 1 ||
| `ignore_mouseover` | Boolean | If true, the unit cannot be hovered over or selected via mouse. | 1 ||
| `ignore_tiles` | Boolean | If true, the unit ignores tile-based collision and placement rules. | 1 ||
| `mouseover_priority` | Integer | The priority for mouseover targeting among multiple units. | 1 ||
| `move_points` | Integer | The number of move points required to use the ability. | 1 ||
| `pickup_type` | Integer | Specifies the type identifier for pickup items. | 1 ||
| `scale` | Number | The scale multiplier applied to the unit's visual size. | 1 ||
| `speculative_inanimate` | Boolean | If true, the unit is treated as an inanimate object for gameplay purposes. | 1 ||
| `static` | Boolean | If true, the unit cannot move and is anchored in place. | 1 ||
| `two_fronts` | Boolean | If true, the unit has a second front side for orientation. | 1 ||
| `two_fronts_switch` | Boolean | If true, the unit can switch between its two front sides. | 1 ||
| `view_bugs_as_enemies` | Boolean | If true, the unit treats bug-type characters as enemies. | 1 ||
| [`inanimate_can_receive_specific_statuses`](./Arrays.md#array-inanimate_can_receive_specific_statuses) | Array | A list of statuses that an inanimate unit can receive. | 1 ||

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
| [`brain`](./Enums.md#enum-brain) | Enum | Specifies the AI brain type used for decision-making logic. | 573 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 493 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 490 ||
| [`pattern`](#object-pattern) | Object | Defines a sequence of actions the AI will execute in order, with optional priority or all-in-one. | 289 ||
| [`mainturn_pattern`](#object-mainturn_pattern) | Object | Specifies the AI behavior pattern used during main turns. | 44 ||
| `end_turn_on_formswitch` | Boolean | If true, the unit's turn ends immediately after switching forms. | 39 ||
| [`virtual_abilities`](#object-virtual_abilities) | Object | Defines virtual abilities and their movement weights for AI decision-making. | 35 ||
| `auto_orient` | Boolean | If true, the unit automatically faces the nearest target. | 31 ||
| `reset_pattern_on_formswitch` | Boolean | If true, the AI pattern resets when the unit switches forms. | 31 ||
| `stun_advances_pattern` | Boolean | If true, the AI advances to the next step in its pattern when stunned. | 30 ||
| `fallback_advances_pattern` | Boolean | If true, using the fallback action advances the AI's pattern index. | 28 ||
| [`bonusturn_pattern`](#object-bonusturn_pattern) | Object | The action sequence the AI follows during a bonus turn. | 27 ||
| [`fallback`](#object-fallback) | Object | The action sequence the AI uses when its main pattern cannot execute. | 23 ||
| [`round_end_bonusturn_pattern`](#object-round_end_bonusturn_pattern) | Object | The action sequence the AI executes at the end of the round as a bonus turn. | 12 ||
| `consider_spells` | Boolean | If true, the AI considers using spells in its decision-making. | 11 ||
| `animate_choice` | Boolean | If true, the AI animates its decision-making process (e.g., thinking indicator). | 8 ||
| `clamp_pattern` | Boolean | If true, the AI's pattern index is clamped to the last valid entry rather than resetting or overflowing. | 5 ||
| `randomize_pattern_start` | Boolean | If true, the AI starts its pattern from a random index at the beginning of combat. | 3 ||
| [`dispersed_bonusturn_pattern`](#object-dispersed_bonusturn_pattern) | Object | The action sequence used when bonus turns are evenly distributed among multiple units. | 2 ||
| `random_orient` | Boolean | If true, the AI randomizes its facing direction on spawn. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| `never_hit_ally_corpses` | Boolean | If true, the AI avoids targeting or damaging ally corpses. | 1 ||
| [`post_absorb_move_weights`](./Enums.md#enum-post_absorb_move_weights) | Enum | Specifies the movement weight set used after the AI absorbs a target. | 1 ||
| `reset_pattern_on_round_begin` | Boolean | If true, the AI's pattern index resets to the start at the beginning of each round. | 1 ||
| [`roll_ability`](./Enums.md#enum-roll_ability) | Enum | Specifies the ability name used for the AI's dice-rolling mechanic. | 1 ||
| [`round_start_bonusturn_pattern`](#object-round_start_bonusturn_pattern) | Object | The action sequence the AI executes at the start of the round as a bonus turn. | 1 ||
| [`dice_abilities`](./Arrays.md#array-dice_abilities) | Array | The list of ability names from which the AI randomly selects when rolling dice. | 1 ||

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
| `strength` | Integer | The base strength stat, used for physical damage calculations. | 386 ||
| `constitution` | Integer | The base constitution stat, used for health and damage mitigation. | 380 ||
| `dexterity` | Integer | The base dexterity stat, used for accuracy and evasion. | 380 ||
| `charisma` | Integer | The base charisma stat, used for social or mind-affecting abilities. | 379 ||
| `intelligence` | Integer | The base intelligence stat, used for spell power and mana. | 379 ||
| `speed` | Array / Number | The speed of the projectile or move, can be a value or a range. | 379 ||
| `luck` | Integer | The base luck stat, used for critical hits and random beneficial effects. | 160 ||

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
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 438 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 433 ||
| [`spells`](./Arrays.md#array-spells) | Array | The list of spell ability IDs the unit possesses. | 381 ||
| `can_get_bonus` | Boolean | If true, the unit can gain bonus turns from abilities or effects. | 30 ||

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
| [`do`](./Enums.md#enum-do) | Enum | The single, specific ability the AI executes. | 101 ||
| [`do_all`](./Arrays.md#array-do_all) | Array | The list of abilities the AI executes in sequence during its turn. | 91 ||
| [`do_priority`](./Arrays.md#array-do_priority) | Array | The list of abilities the AI executes, evaluating them in order of highest priority. | 82 ||
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum | The specific ability the AI executes after moving. | 11 ||
| [`do_random`](./Arrays.md#array-do_random) | Array | The list of abilities from which the AI randomly selects one to execute. | 9 ||
| [`do_strict`](./Arrays.md#array-do_strict) | Array | The list of abilities the AI executes in strict sequence, without any alternative. | 4 ||
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array | The list of actions (typically empty) the AI takes when it does nothing. | 3 ||
| [`move_then_do_random`](./Arrays.md#array-move_then_do_random) | Array | The list of abilities from which the AI randomly selects one to execute after moving. | 3 ||
| [`move_then_do_priority`](./Arrays.md#array-move_then_do_priority) | Array | The list of abilities the AI executes after moving, in priority order. | 2 ||
| [`do_all_shuffle`](./Arrays.md#array-do_all_shuffle) | Array | The list of abilities the AI shuffles and then executes in the resulting random order. | 2 ||
| [`do_best`](./Arrays.md#array-do_best) | Array | The list of abilities the AI evaluates to pick the one with the highest immediate benefit. | 1 ||
| [`do_best_multiple`](./Arrays.md#array-do_best_multiple) | Array | The list of abilities the AI evaluates to pick multiple beneficial ones to execute. | 1 ||
| [`do_priority_alternating`](./Arrays.md#array-do_priority_alternating) | Array | The list of abilities the AI executes in a priority order that alternates each turn. | 1 ||
| [`move_then_do_all`](./Arrays.md#array-move_then_do_all) | Array | The list of abilities the AI executes in sequence after moving. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 10 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 10 ||
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 5 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||

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
| [`initial_form`](./Enums.md#enum-initial_form) | Enum / Integer | Specifies the starting form name for a unit with FormChanger. | 56 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 56 ||
| [`Default`](#object-default) | Enum / Object | The default form configuration for a unit, containing its standard stats and abilities. | 37 ||
| [`Normal`](#object-normal) | Integer / Object | The normal form configuration, used as a baseline state for shape-shifting units. | 11 ||
| [`Rage`](#object-rage) | Object | The rage form configuration, applied when the unit enters an enraged state. | 10 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 ||
| [`HasCat`](#object-hascat) | Object | The form configuration applied when the unit is holding or has swallowed a cat. | 5 ||
| [`default`](#object-default) | Enum / Object | The default configuration or value used when no specific override is provided. | 4 ||
| [`hot`](#object-hot) | Object | The form configuration applied when the unit is in a hot state, granting fire element. | 4 ||
| [`OffMap`](#object-offmap) | Object | The form configuration applied when the unit is off the battlefield map. | 4 ||
| [`AllAlive`](#object-allalive) | Object | The form configuration applied when all family members are alive. | 3 ||
| [`Down`](#object-down) | Object | The form configuration applied when the unit is in a knocked-down or prone state. | 3 ||
| [`Full`](#object-full) | Object | The form configuration applied when the unit is in a full state. | 3 ||
| [`OneAlive`](#object-onealive) | Object | The form configuration applied when only one family member remains alive. | 3 ||
| [`TwoAlive`](#object-twoalive) | Object | A form that activates when two specific units are alive, granting the contained passives and abilities. | 3 ||
| [`Up`](#object-up) | Object | Defines the 'Up' form, including its animation, AI behavior, and passives such as UpTireBehavior. | 3 ||
| [`active`](#object-active) | Object | Defines the active form, containing passives and abilities that are active while in this form. | 2 ||
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 ||
| [`Big`](#object-big) | Object | Defines the 'Big' form, including its animation, attack, passives, and positional data. | 2 ||
| [`Boris`](#object-boris) | Enum / Object | Specifies the 'Boris' form within FormChanger, with its own animation suffix and passives. | 2 ||
| [`CaveMan`](#object-caveman) | Object | Defines the 'CaveMan' form of a CavePerson enemy, including its animation, attack, and passives. | 2 ||
| [`CaveManSpear`](#object-cavemanspear) | Object | Defines the 'CaveManSpear' form of a CavePerson enemy, with a spear attack and corresponding animation. | 2 ||
| [`Empty`](#object-empty) | Object | Defines the 'Empty' form, typically indicating a state with no content (e.g., empty stomach). | 2 ||
| [`Explosive`](#object-explosive) | Enum / Object | Specifies the 'Explosive' form within FormChanger, with its own animation suffix and passives. | 2 ||
| [`Holding`](#object-holding) | Object | Defines the 'Holding' form, used when the unit is holding an object, with associated movement and form change behaviors. | 2 ||
| [`Holy`](#object-holy) | Enum / Object | Specifies the 'Holy' form within FormChanger, with its own animation suffix and passives. | 2 ||
| [`NotPriming`](#object-notpriming) | Object | Defines the 'NotPriming' form, which allows the unit to take main turns and grants bonus turns. | 2 ||
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 ||
| [`passive`](#object-passive) | Object | Defines the passive form, where the unit does nothing (uses DoNothing attack) and is inactive. | 2 ||
| [`Priming`](#object-priming) | Object | Defines the 'Priming' form, where the unit does not take main turns but gains bonus turns at round end. | 2 ||
| [`Rain`](#object-rain) | Object | Defines the rain weather effect with associated particle, sound, and rendering settings. | 2 ||
| [`Small`](#object-small) | Object | Defines the 'Small' form, typically used for smaller size variants, with its own attack and animation. | 2 ||
| [`SquirrelForm`](#object-squirrelform) | Object | Defines the 'SquirrelForm', a transformation used by units like DeathMetal, granting melee attack and speed bonuses. | 2 ||
| [`Turtled`](#object-turtled) | Object | Defines the 'Turtled' form, a defensive state where the unit cannot attack or move. | 2 ||
| [`Alert`](#object-alert) | Object | Defines the 'Alert' form, an alerted state with a pattern brain AI. | 1 ||
| [`Angry`](#object-angry) | Object | Defines the 'Angry' form, an enraged state with its own AI. | 1 ||
| [`Attacker`](#object-attacker) | Object | Defines the 'Attacker' form, focusing on offensive actions like attacking and charging. | 1 ||
| [`BellyFull`](#object-bellyfull) | Object | Defines the 'BellyFull' form, used when the unit has the Consuming status, with appropriate animation. | 1 ||
| [`BigHolding`](#object-bigholding) | Object | Defines the 'BigHolding' form, a larger variant while holding an object, triggered by the Consuming status. | 1 ||
| [`BigHoldingCat`](#object-bigholdingcat) | Object | Defines the 'BigHoldingCat' form, a cat-sized variant of the holding form while Consuming. | 1 ||
| [`Bishop`](#object-bishop) | Object | Defines the 'Bishop' form for Cultist enemies, with its own attack (BBXLightning) and animation. | 1 ||
| [`BlackHole`](#object-blackhole) | Object | Defines the 'BlackHole' form, a variant of NeutronStar with its own animation and name. | 1 ||
| [`Bomb`](#object-bomb) | Object | Defines the 'Bomb' form, an explosive state that triggers an ability on death. | 1 ||
| [`Bully`](#object-bully) | Object | Defines the 'Bully' form, which allows the unit to take turns and enables its passives. | 1 ||
| [`Butcher`](Engine_LogicKeys.md#object-butcher) | Object | Specifies the 'Butcher' form within FormChanger, used for boss dialogue. | 1 ||
| [`CaveBaby`](#object-cavebaby) | Object | Defines the 'CaveBaby' form of a CavePerson enemy, with reduced health and baby attack. | 1 ||
| [`CaveWoman`](#object-cavewoman) | Object | Defines the 'CaveWoman' form of a CavePerson enemy, with kick attack and higher health. | 1 ||
| [`CaveWomanHasCat`](#object-cavewomanhascat) | Object | Defines the 'CaveWomanHasCat' form, a variant of CaveWoman that attacks with a cat slap. | 1 ||
| [`Charging`](#object-charging) | Object | Defines the 'Charging' form, a wind-up state for a powerful attack. | 1 ||
| [`Close`](#object-close) | Object | Defines the 'Close' form, which triggers GSOpen ability upon reaction. | 1 ||
| [`Colorless`](Engine_LogicKeys.md#object-colorless) | Object | Specifies the 'Colorless' form within FormChanger, used for boss dialogue. | 1 ||
| [`Cultist`](#object-cultist) | Object | Defines the 'Cultist' form, a basic melee form with its own name and tooltip. | 1 ||
| [`Damaged`](#object-damaged) | Object | Defines the 'Damaged' form, an injured state with a specific AI pattern to drink and attack. | 1 ||
| [`Default_Ceiling`](#object-default_ceiling) | Object | Defines the 'Default_Ceiling' form for SpiderQueen, with AI pattern to spawn spiders. | 1 ||
| [`Default_Ground`](#object-default_ground) | Object | Defines the 'Default_Ground' form for SpiderQueen, with AI pattern to web and attack. | 1 ||
| [`DesireMech`](#object-desiremech) | Object | Defines the 'DesireMech' form, a mech suit form with its own AI pattern. | 1 ||
| [`Die`](#object-die) | Integer / Object | If set, kills the target immediately. | 1 ||
| [`Druid`](Engine_LogicKeys.md#object-druid) | Object | Specifies the 'Druid' form within FormChanger, used for boss dialogue. | 1 ||
| [`Drunker`](#object-drunker) | Object | Defines the 'Drunker' form, a drunken state with altered animation. | 1 ||
| [`DualSword`](#object-dualsword) | Object | Defines the 'DualSword' form of TheDestroyer, increasing move speed and using a dual sword attack. | 1 ||
| [`DualSword_Primed`](#object-dualsword_primed) | Object | Defines the 'DualSword_Primed' form, a powered-up dual sword state with holy animation. | 1 ||
| [`Dumb`](#object-dumb) | Integer / Object | Defines the 'Dumb' form, which can be either a numeric value or an object with passives that disable spells and turn off TV. | 1 ||
| [`Explody`](#object-explody) | Object | Defines the 'Explody' form, an explosive state that uses ToxExplode attack and cannot move. | 1 ||
| [`Fighter`](Engine_LogicKeys.md#object-fighter) | Object | Specifies the 'Fighter' form within FormChanger, used for boss dialogue. | 1 ||
| [`FightPhase`](#object-fightphase) | Object | Defines the 'FightPhase' form, a combat form with float move and shoot attack, taking turns. | 1 ||
| [`Fire`](#object-fire) | Integer / Object | Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack. | 1 ||
| [`FireFull`](#object-firefull) | Integer / Object | Defines the 'FireFull' form, a fully charged fire state with its own animation and visual combo. | 1 ||
| [`Flop`](#object-flop) | Object | Defines the initial flopped down state, using animation suffix 'Down' and a pattern AI that requires 4 wiggles to exit. | 1 ||
| [`Flop2`](#object-flop2) | Object | Defines a subsequent flopped down state triggered on hit, with variable wiggles (2-6) to recover. | 1 ||
| [`Flush`](#object-flush) | Object | Defines a form that executes a sequence of actions (FlushX, side switch, form switch) and has a spell with a localized name. | 1 ||
| [`FlushBubs`](#object-flushbubs) | Object | Defines a form granting an immediate ability reaction for Cerberubs shotgun. | 1 ||
| [`FlushHost`](#object-flushhost) | Object | Defines a host form with a partial animation suffix and a reflect projectiles passive that deals 2 self-damage. | 1 ||
| [`FlushNettle`](#object-flushnettle) | Object | Defines a form that gains thorns and kinetic spikes after an enemy casts a spell. | 1 ||
| [`Grappling`](#object-grappling) | Object | Defines a grappling form with a specific animation suffix and exit animations. | 1 ||
| [`Grown`](#object-grown) | Object | Defines the grown form with a custom attack, name, UI floater offset, and a health weak threshold. | 1 ||
| [`GuaranteedJackpot`](#object-guaranteedjackpot) | Object | Defines a form that guarantees a jackpot coin result from slot machine rolls. | 1 ||
| [`Guarding`](#object-guarding) | Object | Defines a guarding form with a high brace passive. | 1 ||
| [`HalfDead`](#object-halfdead) | Object | Defines the half-dead form with reduced movement and a dash attack. | 1 ||
| [`HasDeadCat`](#object-hasdeadcat) | Object | Defines a form when Lenny's cat is dead, with a slap attack and conditional form change while the status is active. | 1 ||
| [`HasRock`](#object-hasrock) | Object | Defines a form where the unit has a rock, with a bash attack. | 1 ||
| [`Headless`](#object-headless) | Object | Defines a headless form with increased movement. | 1 ||
| [`Hint_CrackedVisuals`](#object-hint_crackedvisuals) | Object | Defines a visual state with cracked animation suffix. | 1 ||
| [`Hint_CrackedVisuals2`](#object-hint_crackedvisuals2) | Object | Defines a visual state with charging cracked animation. | 1 ||
| [`Hint_CrackedVisuals3`](#object-hint_crackedvisuals3) | Object | Defines a visual state with swallowed cracked animation. | 1 ||
| [`HumanDead`](#object-humandead) | Object | Defines a form when the human half is dead, with a spin attack and custom tooltip. | 1 ||
| [`Hunter`](Engine_LogicKeys.md#object-hunter) | Object | Defines a list of quotes for the Hunter class (vs boss, embark, return early). | 1 ||
| [`InitialPhase`](#object-initialphase) | Object | Defines the initial phase form with a float move, shoot attack, and the ability to take turns. | 1 ||
| [`Insane_Ceiling`](#object-insane_ceiling) | Object | Defines the insane ceiling form with pattern AI and animation suffix. | 1 ||
| [`Insane_Ground`](#object-insane_ground) | Object | Defines the insane ground form with pattern AI and animation suffix. | 1 ||
| [`Johnny`](#object-johnny) | Object | Defines a form that executes a mega blast, side switch, and form switch in sequence. | 1 ||
| [`JohnnyBubs`](#object-johnnybubs) | Object | Defines a form granting an immediate ability reaction for Cerberubs shotgun. | 1 ||
| [`JohnnyHost`](#object-johnnyhost) | Object | Defines a host form with a partial animation suffix and a reflect projectiles passive that deals 2 self-damage. | 1 ||
| [`JohnnyNettle`](#object-johnnynettle) | Object | Defines a form that gains thorns and kinetic spikes after an enemy casts a spell. | 1 ||
| [`Joystick`](#object-joystick) | Object | Defines a form with joystick animation and an immediate ability reaction (fumble even/odd). | 1 ||
| [`LastHit`](#object-lasthit) | Object | Defines a form that grants 2 dispersed bonus turns after the last hit. | 1 ||
| [`Lifted`](#object-lifted) | Object | Defines a lifted form with no attack or movement options. | 1 ||
| [`Lit`](#object-lit) | Object | Defines a lit form that changes when wind element influence is applied. | 1 ||
| [`Mage`](Engine_LogicKeys.md#object-mage) | Object | Defines a list of quotes for the Mage class. | 1 ||
| [`Medic`](Engine_LogicKeys.md#object-medic) | Object | Defines a list of quotes for the Medic class. | 1 ||
| [`Monk`](Engine_LogicKeys.md#object-monk) | Object | Defines a list of quotes for the Monk class. | 1 ||
| [`Mounted`](#object-mounted) | Object | Defines a mounted form with 'Cat' animation suffix. | 1 ||
| [`MouthFull`](#object-mouthfull) | Object | Defines a form with mouth full animation that changes while the Consuming status is active. | 1 ||
| [`Mutant`](#object-mutant) | Integer / Object | As an object, defines the mutant form with reduced move speed and custom name. As an integer, defines spawn weight. | 1 ||
| [`Necromancer`](Engine_LogicKeys.md#object-necromancer) | Object | Defines a list of quotes for the Necromancer class. | 1 ||
| [`NeutronStar`](#object-neutronstar) | Object | Defines the neutron star form with custom graphics and a random pattern AI (rumble or explode). | 1 ||
| [`NoDeathRattle`](./Engine_LogicKeys.md#valid-property-keys) | Object | Defines a form that suppresses death rattle and triggers a heart attack when a buddy dies. | 1 ||
| [`NoEyes`](#object-noeyes) | Object | Defines a form with no eyes animation. | 1 ||
| [`NormalFull`](#object-normalfull) | Integer / Object | As an object, defines the normal full form with a spit attack and conditional form change. As an integer, specifies alt graphics index. | 1 ||
| [`NoStick`](#object-nostick) | Object | Defines a form without a stick, using a jab attack with pattern AI. | 1 ||
| [`Nuke`](#object-nuke) | Object | Defines a nuke form with no attack or movement options. | 1 ||
| [`Obey`](#object-obey) | Integer / Object | As an object, defines an obey form that disables attacks and reacts with TV off. As an integer, defines a value (e.g., weight or count). | 1 ||
| [`Off`](#object-off) | Object | Defines an off form with a 'Off' animation suffix. | 1 ||
| [`OffScreen`](#object-offscreen) | Object | Defines an off-screen form that does not take turns and drops in chaos heads. | 1 ||
| [`OneEye`](#object-oneeye) | Object | Defines a form with one eye that triggers an ability at 40% health threshold. | 1 ||
| [`Open`](#object-open) | Object | Defines an open form with increased movement and a specific attack. | 1 ||
| [`OpenCat`](#object-opencat) | Object | Defines an open cat form that changes when the Consuming status is active. | 1 ||
| [`Out`](#object-out) | Object | Defines a form that is 'out' with a ground flopper movement passive. | 1 ||
| [`Possessing`](#object-possessing) | Object | Form state when the unit is possessing another entity. | 1 ||
| [`Primed`](#object-primed) | Object | Form state representing the unit being primed, with specific attack and AI behavior. | 1 ||
| [`Psychic`](Engine_LogicKeys.md#object-psychic) | Object | Form identifier for the Psychic boss type, used for dialogue references. | 1 ||
| [`Pulp2`](#object-pulp2) | Object | Form state for the second stage of pulping, with no attacks or movement. | 1 ||
| [`Pulp3`](#object-pulp3) | Object | Form state for the third stage of pulping, with no attacks or movement. | 1 ||
| [`Pulp4`](#object-pulp4) | Object | Form state for the fourth stage of pulping, with no attacks or movement. | 1 ||
| [`Pulp5`](#object-pulp5) | Object | Form state for the fifth stage of pulping, with no attacks or movement. | 1 ||
| [`Pulp6`](#object-pulp6) | Object | Form state for the sixth stage of pulping, with no attacks or movement. | 1 ||
| [`Pulp7`](#object-pulp7) | Object | Form state for the seventh stage of pulping, with no attacks or movement. | 1 ||
| [`Sitting`](#object-sitting) | Object | Form state where the unit is sitting, with no movement or attack. | 1 ||
| [`SmallHolding`](#object-smallholding) | Object | Form state when the unit is holding a small object, triggering a form change while consuming. | 1 ||
| [`SmallHoldingCat`](#object-smallholdingcat) | Object | Form state when the unit is holding a cat, triggering a form change while consuming. | 1 ||
| [`SpawningPhase`](#object-spawningphase) | Object | Form state for the spawning phase, where the unit is immobile and cannot take turns. | 1 ||
| [`Standing`](#object-standing) | Object | Form state where the unit is standing, with default movement and attack. | 1 ||
| [`Standing2`](#object-standing2) | Object | Form state where the unit is standing with a jumping movement ability. | 1 ||
| [`Start_Ceiling`](#object-start_ceiling) | Object | Form state for starting on the ceiling, with a form change trigger when entering the map. | 1 ||
| [`Stop`](#object-stop) | Integer / Object | If an integer, the number of turns the unit is stopped. If an object, the form configuration for the stopped state. | 1 ||
| [`SwordAndShield`](#object-swordandshield) | Object | Form state with sword and shield, using the DestroyerAttack ability. | 1 ||
| [`SwordAndShield_Primed`](#object-swordandshield_primed) | Object | Primed form state of SwordAndShield with holy animation and no final boss shield. | 1 ||
| `sync_brain_patterns` | Boolean | If true, synchronizes brain patterns across form changes. | 1 ||
| [`Tank`](Engine_LogicKeys.md#object-tank) | Object | Form identifier for the Tank boss type, used for dialogue references. | 1 ||
| [`Tar`](#object-tar) | Integer / Object | If an integer, the number of tar stacks. If an object, the form state for the tar-covered unit. | 1 ||
| [`TarFull`](#object-tarfull) | Integer / Object | If an integer, the number of full tar stacks. If an object, the form state for the fully tar-covered unit. | 1 ||
| [`Thief`](Engine_LogicKeys.md#object-thief) | Object | Form identifier for the Thief boss type. | 1 ||
| [`Throb`](#object-throb) | Object | Form state for the Chaos unit's throb behavior, with a spread pattern. | 1 ||
| [`ThrobBubs`](#object-throbbubs) | Object | Form state for Chaos unit throb that reacts with a shotgun attack. | 1 ||
| [`ThrobHost`](#object-throbhost) | Object | Form state for Chaos unit acting as host, reflecting projectiles. | 1 ||
| [`ThrobNettle`](#object-throbnettle) | Object | Form state for Chaos unit with thorns and kinetic spikes that stack after enemy spells. | 1 ||
| [`Tinkerer`](Engine_LogicKeys.md#object-tinkerer) | Object | Form identifier for the Tinkerer boss type. | 1 ||
| [`Transformed`](#object-transformed) | Object | Form state after transformation, ending the turn on form switch. | 1 ||
| [`TwoEyes`](#object-twoeyes) | Object | Form state with two eyes, triggering ability at a health threshold. | 1 ||
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 ||
| [`Unlit`](#object-unlit) | Object | Form state for an unlit candle, muting demonic glyph display. | 1 ||
| [`Unmounted`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Form state when the unit is unmounted from its mech suit, with no additional properties. | 1 ||
| [`Unwashed`](#object-unwashed) | Object | Form state for the unwashed version of Johnny, with its own AI pattern. | 1 ||
| [`Washed`](#object-washed) | Object | Form state for the washed version of Johnny, with a blast attack. | 1 ||
| [`Washer`](#object-washer) | Object | Form state for the washer variant of a cultist, with basic melee attack. | 1 ||
| [`Water`](#object-water) | Object | Form state for water element, applying a puddle or movement bonus. | 1 ||
| [`WereMan`](#object-wereman) | Object | Form state for the were-man transformation, with fury swipe attack and sabertooth faction. | 1 ||
| [`Zealot`](#object-zealot) | Object | Form state for the zealot variant of a cultist, with a stabbing attack. | 1 ||
| [`ZealotBomb`](#object-zealotbomb) | Object | Form state for the bomb zealot variant, with an explosion attack. | 1 ||

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
| [`faction`](./Enums.md#enum-faction) | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 4 ||
| [`obj`](./Arrays.md#array-obj) | Array / Enum | Specifies one or more object names to bounce towards the target. | 4 ||
| [`additional_statuses`](#object-additional_statuses) | Object | Additional status effects applied to the spawned unit on death. | 1 ||

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
| [`alt_sounds`](./Arrays.md#array-alt_sounds) | Array | Array of alternate sound pairs for specific audio events. | 61 ||
| [`animation_prefix`](./Enums.md#enum-animation_prefix) | Enum | Prefix used for the unit's animation sounds. | 1 ||

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
| [`alternate_energized_effect`](#object-alternate_energized_effect) | Object | Effects applied when the robot becomes energized, such as form changes or stat boosts. | 2 ||

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
| `takes_turns` | Boolean | If true, the unit participates in the turn order. | 23 ||
| `dispersed_bonus_turns` | Integer | The number of bonus turns granted to this unit when its turn order is dispersed. | 18 ||
| `takes_main_turn` | Boolean | If true, the unit consumes the main turn phase of the round. | 10 ||
| `evenly_dispersed_bonus_turns` | Integer | The number of bonus turns spread evenly across the turn order for this unit. | 7 ||
| `round_end_bonus_turns` | Integer | The number of bonus turns granted at the end of each round. | 5 ||
| `wait_till_next_round_to_update_turns` | Boolean | If true, delays turn count updates until the next round. | 4 ||
| `round_start_bonus_turns` | Integer | The number of extra turns the unit gains at the start of each round. | 1 ||

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
| [`face`](./Enums.md#enum-face) | Enum | The face equipment item assigned to the unit. | 16 ||
| [`head`](./Enums.md#enum-head) | Enum / Number | The catalog ID for the cat's head part. | 14 ||
| [`neck`](./Enums.md#enum-neck) | Enum | The neck equipment item assigned to the unit. | 10 ||
| [`weapon`](./Enums.md#enum-weapon) | Enum | The name of the weapon item the unit starts with. | 7 ||

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
| [`do`](./Enums.md#enum-do) | Enum | The single, specific ability the AI executes. | 23 ||
| [`do_all`](./Arrays.md#array-do_all) | Array | The list of abilities the AI executes in sequence during its turn. | 9 ||
| [`do_priority`](./Arrays.md#array-do_priority) | Array | The list of abilities the AI executes, evaluating them in order of highest priority. | 8 ||
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum | The specific ability the AI executes after moving. | 2 ||
| [`do_strict`](./Arrays.md#array-do_strict) | Array | The list of abilities the AI executes in strict sequence, without any alternative. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 28 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 24 ||
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 10 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||

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
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 35 ||
| [`form_hasnot`](./Enums.md#enum-form_hasnot) | Enum | Specifies a form that the unit must not be in for the status-triggered form change to occur. | 30 ||
| [`form_has`](./Enums.md#enum-form_has) | Enum | Specifies a form that the unit must be in for the status-triggered form change to occur. | 25 ||

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
| `TVBotDie` | Integer | Keyword tooltip definition for the TVBot's death behavior, with name, tooltip, and icon. | 1 ||
| `TVBotDumb` | Integer | Defines the keyword tooltip for the TVBotDumb status or ability. | 1 ||
| `TVBotObey` | Integer | Defines the keyword tooltip for the TVBotObey status or ability. | 1 ||
| `TVBotStop` | Integer | Defines the keyword tooltip for the TVBotStop status or ability. | 1 ||

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
| [`MoveAway`](#object-moveaway) | Object | Defines an AI virtual ability that moves the unit away from its current target using the specified ability and move weights. | 4 ||
| [`MoveClose`](#object-moveclose) | Object | Defines an AI virtual ability that moves the unit close to its target using the specified ability and move weights. | 4 ||
| [`DashRandomly`](#object-dashrandomly) | Object | Defines an AI virtual ability that causes the unit to dash in a random direction using the specified ability and decision weights. | 2 ||
| [`Escape`](#object-escape) | Object | Defines an AI virtual ability that causes the unit to escape using the specified ability and move weights. | 2 ||
| [`MoveCenter`](#object-movecenter) | Object | Defines an AI virtual ability that moves the unit toward the center of the map using the specified ability and move weights. | 2 ||
| [`MoveForThrow`](#object-moveforthrow) | Object | Defines an AI virtual ability that moves the unit into position for a throw ability. | 2 ||
| [`SpearRun`](#object-spearrun) | Object | Defines an AI virtual ability that moves the unit to run with a spear and pick it up. | 2 ||
| [`CerberubsJumpBlind`](#object-cerberubsjumpblind) | Object | Defines an AI virtual ability that makes Cerberubs jump with blind decision weights. | 1 ||
| [`CerberubsJumpNormal`](#object-cerberubsjumpnormal) | Object | Defines an AI virtual ability that makes Cerberubs jump with default decision weights. | 1 ||
| [`CloseConvert`](#object-closeconvert) | Object | Defines an AI virtual ability that moves close and uses the MarshmallowConvert ability. | 1 ||
| [`FoodMove`](#object-foodmove) | Object | Defines an AI virtual ability that moves the unit toward food using the CaveBabyFoodMove ability. | 1 ||
| [`ForceTrample`](#object-forcetrample) | Object | Defines an AI virtual ability that forces the unit to trample carelessly using the BirthwortTrample ability. | 1 ||
| [`LeapClose`](#object-leapclose) | Object | Defines an AI virtual ability that makes the unit leap toward its aggro target. | 1 ||
| [`MoveForBarrage`](#object-moveforbarrage) | Object | Defines an AI virtual ability that moves the unit to a position suitable for a barrage ability. | 1 ||
| [`MoveForDash`](#object-movefordash) | Object | Defines an AI virtual ability that moves the unit into position for a dash attack. | 1 ||
| [`MoveForGrass`](#object-moveforgrass) | Object | Defines an AI virtual ability that moves the unit to stomp and eat grass. | 1 ||
| [`MoveForPounce`](#object-moveforpounce) | Object | Defines an AI virtual ability that moves the unit into position for a pounce attack. | 1 ||
| [`MoveForSpin`](#object-moveforspin) | Object | Defines an AI virtual ability that moves the unit to set up a spin throw. | 1 ||
| [`MoveOneForPuke`](#object-moveoneforpuke) | Object | Defines an AI virtual ability that moves the unit one step for a puke ability. | 1 ||
| [`MoveSpaced`](#object-movespaced) | Object | Defines an AI virtual ability that moves the unit while maintaining a specific distance. | 1 ||
| [`MoveToHead`](#object-movetohead) | Object | Defines an AI virtual ability that moves the unit to the head of a target to grab it. | 1 ||
| [`MoveTowards`](#object-movetowards) | Object | Defines an AI virtual ability that moves the unit toward its target. | 1 ||
| [`NCGravecrawlFAR`](#object-ncgravecrawlfar) | Object | Defines an AI virtual ability that makes a NecroCat gravecrawl while staying far from enemies. | 1 ||
| [`ReturnA`](#object-returna) | Object | Defines an AI virtual ability that makes a HangerBot return to a close position. | 1 ||
| [`RunFar`](#object-runfar) | Object | Defines an AI virtual ability that makes the unit run far away. | 1 ||
| [`SuckMF`](#object-suckmf) | Object | Defines an AI virtual ability that makes a Tormentor suck enemies carelessly while keeping distance. | 1 ||
| [`TF_TargetAllies`](#object-tf_targetallies) | Object | Defines an AI virtual ability that casts Twisting Flames targeting allies. | 1 ||
| [`TF_TargetEnemies`](#object-tf_targetenemies) | Object | Defines an AI virtual ability that casts Twisting Flames targeting enemies. | 1 ||
| [`Unflip`](#object-unflip) | Object | Defines an AI virtual ability that teleports the unit to flip up and spin an enemy. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 205 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 56 |
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 30 | 2 |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 29 | 2 |
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is pushed away from the source on hit. | 24 | 3 |
| [`Burn`](./Enums.md) | Integer | The amount of Burn applied, either as a fixed number or a formula string. | 16 | 2 |
| [`Fear`](./Enums.md) | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 13 | 1 |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 12 | 1 |
| [`Slow`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 10 | 2 |
| [`Stun`](./Enums.md) | Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 8 | 1 |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 7 | 1 |
| [`Weakness`](./Enums.md) | Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 7 | 1 |
| [`Leech`](./Enums.md) | Integer | The amount of health leeched from the target (heals the attacker). | 5 | 2 |
| [`Rot`](./Enums.md) | Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 5 | 1 |
| [`Madness`](./Enums.md) | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 3 | 1 |
| [`RemoteLeech`](./Enums.md) | Integer | The amount of remote leech applied to the target on basic attack. | 2 | 1 |
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | 2 |
| [`GainDisorderFromPool`](#object-gaindisorderfrompool) | Object | Specifies a pool of disorders from which one is randomly gained on basic attack, with an optional chance. | 1 ||
| [`Possessed`](./Enums.md) | Integer | The number of possession stacks applied, or a template with name and tooltips. | 1 | 1 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | -1 |
| [`RemoteFlatLeech`](./Enums.md) | Integer | The flat amount of remote leech applied to the target on basic attack. | 1 | 1 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 13 ||
| `pop_corpse` | Boolean | If true, the corpse is destroyed instead of left behind on death. | 11 ||
| `is_dying_animation` | Boolean | If true, the unit plays its dying animation before the death rattle effect. | 7 ||
| `cancel_knockback` | Boolean | If true, knockback from the triggering event is negated. | 1 ||
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 1 ||
| `must_target_killer` | Boolean | If true, the death rattle effect must target the unit that killed it. | 1 ||
| `target_killer` | Boolean | If true, the death rattle effect targets the killer. | 1 ||

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
| [`do`](./Enums.md#enum-do) | Enum | The single, specific ability the AI executes. | 15 ||
| [`do_priority`](./Arrays.md#array-do_priority) | Array | The list of abilities the AI executes, evaluating them in order of highest priority. | 4 ||
| [`do_all`](./Arrays.md#array-do_all) | Array | The list of abilities the AI executes in sequence during its turn. | 4 ||
| [`do_strict`](./Arrays.md#array-do_strict) | Array | The list of abilities the AI executes in strict sequence, without any alternative. | 3 ||
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum | The specific ability the AI executes after moving. | 1 ||

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
| [`palette`](./Enums.md#enum-palette) | Enum / Integer | Specifies the color palette index for the ability's visuals. | 17 ||
| `ear1` | Integer | The catalog ID for the cat's first ear part. | 13 ||
| `tail` | Integer | The catalog ID for the cat's tail part. | 13 ||
| `arm2` | Number | The catalog ID for the cat's second arm part. | 11 ||
| `arm1` | Number | The catalog ID for the cat's first arm part. | 10 ||
| `ear2` | Integer | The catalog ID for the cat's second ear part. | 10 ||
| `leg1` | Integer | The catalog ID for the cat's first leg part. | 8 ||
| `leg2` | Integer | The catalog ID for the cat's second leg part. | 8 ||
| `head` | Enum / Number | The catalog ID for the cat's head part. | 6 ||
| `texture` | Integer | The catalog ID for the cat's texture. | 6 ||
| `body` | Number | The catalog ID for the cat's body part. | 5 ||
| `eye1` | Integer | The catalog ID for the cat's first eye part. | 3 ||
| `eye2` | Integer | The catalog ID for the cat's second eye part. | 3 ||

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
| [`do`](./Enums.md#enum-do) | Enum | The single, specific ability the AI executes. | 12 ||
| [`do_priority`](./Arrays.md#array-do_priority) | Array | The list of abilities the AI executes, evaluating them in order of highest priority. | 6 ||
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum | The specific ability the AI executes after moving. | 1 ||
| [`do_all`](./Arrays.md#array-do_all) | Array | The list of abilities the AI executes in sequence during its turn. | 1 ||
| [`do_best`](./Arrays.md#array-do_best) | Array | The list of abilities the AI evaluates to pick the one with the highest immediate benefit. | 1 ||
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array | The list of actions (typically empty) the AI takes when it does nothing. | 1 ||
| [`do_random`](./Arrays.md#array-do_random) | Array | The list of abilities from which the AI randomly selects one to execute. | 1 ||

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
| [`common`](./Engine_EventKeys.md#valid-property-keys) | `String` | Defines the common reward block for a boss encounter. | 20 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 20 ||
| [`rare`](./Engine_EventKeys.md#valid-property-keys) | `String` | Defines the rare reward block for a boss encounter. | 16 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 10 ||
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 7 ||
| `backstabs_only` | Boolean | If true, the reaction only triggers on backstab damage. | 3 ||
| `only_when_not_your_turn` | Boolean | If true, the reaction only triggers when it is not the unit's turn. | 3 ||
| `cancel_knockback` | Boolean | If true, knockback from the triggering event is negated. | 1 ||
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 1 ||
| `even_on_0_damage` | Boolean | If true, the reaction triggers even when the damage dealt is zero. | 1 ||
| `even_on_0_damage_if_knockback` | Boolean | If true, the reaction triggers on zero damage if knockback occurs. | 1 ||
| `match_knockback_direction` | Boolean | If true, the reaction's knockback direction matches the triggering knockback direction. | 1 ||
| `ranged_only` | Boolean | If true, the reaction only triggers on ranged attacks. | 1 ||
| `verify_target` | Boolean | If true, the reaction verifies that the target is valid before triggering. | 1 ||

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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 70 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 47 ||
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 24 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 22 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 10 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 10 ||
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target regardless of accuracy or evasion. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 18 ||
| [`FindItemFromPool`](./Enums.md) | Enum | Specifies the loot pool from which to find an item, with an optional chance. | 16 | eagle_pool |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 2 ||
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`Antidote`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Float | The multiplier for the number of antidote pickups spawned. | 5 ||
| `Blessing` | Float | The multiplier for the number of blessing pickups spawned. | 5 ||
| [`BigCatnip`](Engine_LogicKeys.md#object-bigcatnip) | Integer / Object | The number of big catnip pickups spawned. | 4 ||
| [`BiggestFood`](Engine_LogicKeys.md#object-biggestfood) | Integer / Object | The number of biggest food pickups spawned. | 4 ||
| [`BigScrap`](Engine_LogicKeys.md#object-bigscrap) | Number / Object | The amount of big scrap pickups spawned. | 4 ||
| [`Coin`](Engine_LogicKeys.md#object-coin) | Integer / Object | The number of coin pickups spawned. | 4 ||
| [`BigFood`](Engine_LogicKeys.md#object-bigfood) | Integer / Object | The number of big food pickups spawned. | 2 ||
| `Coin10` | Float | The multiplier for the number of Coin10 pickups spawned. | 2 ||
| [`Coin3`](Engine_LogicKeys.md#object-coin3) | Integer / Object | The number of Coin3 pickups spawned. | 2 ||
| [`Coin4`](Engine_LogicKeys.md#object-coin4) | Integer / Object | The number of Coin4 pickups spawned. | 2 ||
| [`MedCatnip`](Engine_LogicKeys.md#object-medcatnip) | Integer / Object | The number of medium catnip pickups spawned. | 2 ||
| [`MedScrap`](Engine_LogicKeys.md#object-medscrap) | Integer / Object | The number of medium scrap pickups spawned. | 2 ||
| [`RandomArmorPickup`](Engine_LogicKeys.md#object-randomarmorpickup) | Number / Object | The amount of random armor pickups spawned. | 2 ||
| [`RandomCatnipPickup`](Engine_LogicKeys.md#object-randomcatnippickup) | Integer / Object | The number of random catnip pickups spawned. | 2 ||
| [`RandomFoodPickup`](Engine_LogicKeys.md#object-randomfoodpickup) | Integer / Object | The number of random food pickups spawned. | 2 ||
| [`Bear`](Engine_LogicKeys.md#object-bear) | Integer / Object | The number of bear familiars spawned. | 1 ||
| [`BlackBird`](Engine_LogicKeys.md#object-blackbird) | Integer / Object | The number of black birds spawned. | 1 ||
| [`Catepillar`](Engine_LogicKeys.md#object-catepillar) | Integer / Object | The number of caterpillar familiars spawned. | 1 ||
| [`Catnip`](Engine_LogicKeys.md#object-catnip) | Integer / Object | The number of catnip pickups spawned. | 1 ||
| [`CharmedDip`](Engine_LogicKeys.md#object-charmeddip) | Integer / Object | The number of charmed dip pickups spawned. | 1 ||
| [`CharmedFloater`](Engine_LogicKeys.md#object-charmedfloater) | Integer / Object | The number of charmed floater pickups spawned. | 1 ||
| [`CharmedPile`](Engine_LogicKeys.md#object-charmedpile) | Integer / Object | The number of charmed pile pickups spawned. | 1 ||
| [`Cherub`](Engine_LogicKeys.md#object-cherub) | Integer / Object | The number of cherubs spawned. | 1 ||
| [`Chicken`](Engine_LogicKeys.md#object-chicken) | Integer / Object | The number of chicken pickups spawned. | 1 ||
| [`Coin2`](Engine_LogicKeys.md#object-coin2) | Integer / Object | The number of Coin2 pickups spawned. | 1 ||
| [`Dove`](Engine_LogicKeys.md#object-dove) | Integer / Object | The number of doves spawned. | 1 ||
| [`Eagle`](Engine_LogicKeys.md#object-eagle) | Integer / Object | The number of eagles spawned. | 1 ||
| [`Food`](Engine_LogicKeys.md#object-food) | Integer / Object | The number of food pickups spawned. | 1 ||
| [`Harpy`](Engine_LogicKeys.md#object-harpy) | Integer / Object | The number of harpies spawned. | 1 ||
| [`HummingBird`](Engine_LogicKeys.md#object-hummingbird) | Integer / Object | The number of hummingbirds spawned. | 1 ||
| [`LargeBirdPool`](Engine_LogicKeys.md#object-largebirdpool) | Integer / Object | The weight for spawning from the large bird pool. | 1 ||
| [`MedBirdPool`](Engine_LogicKeys.md#object-medbirdpool) | Integer / Object | The weight for spawning from the medium bird pool. | 1 ||
| [`Mutant`](#object-mutant) | Integer / Object | As an object, defines the mutant form with reduced move speed and custom name. As an integer, defines spawn weight. | 1 ||
| [`Pigeon`](Engine_LogicKeys.md#object-pigeon) | Integer / Object | The number of pigeons spawned. | 1 ||
| [`RandomBiggerArmorPickup`](Engine_LogicKeys.md#object-randombiggerarmorpickup) | Number / Object | The amount of bigger random armor pickups spawned. | 1 ||
| [`RandomBiggerCatnipPickup`](Engine_LogicKeys.md#object-randombiggercatnippickup) | Integer / Object | The number of bigger random catnip pickups spawned. | 1 ||
| [`RandomBiggerFoodPickup`](Engine_LogicKeys.md#object-randombiggerfoodpickup) | Integer / Object | The number of bigger random food pickups spawned. | 1 ||
| [`Raven`](Engine_LogicKeys.md#object-raven) | Integer / Object | The number of ravens spawned. | 1 ||
| [`Scrap`](Engine_LogicKeys.md#object-scrap) | Integer / Object | The number of scrap pickups spawned. | 1 ||
| [`Seagull`](Engine_LogicKeys.md#object-seagull) | Integer / Object | The number of seagulls spawned. | 1 ||
| [`SmallBirdPool`](Engine_LogicKeys.md#object-smallbirdpool) | Integer / Object | The weight for spawning from the small bird pool. | 1 ||
| [`Snake`](Engine_LogicKeys.md#object-snake) | Integer / Object | The number of snake familiars spawned. | 1 ||
| [`Squirrel`](Engine_LogicKeys.md#object-squirrel) | Integer / Object | The number of squirrel familiars spawned. | 1 ||
| [`Toad`](Engine_LogicKeys.md#object-toad) | Integer / Object | The number of toad familiars spawned. | 1 ||
| [`Turkey`](Engine_LogicKeys.md#object-turkey) | Integer / Object | The number of turkeys spawned. | 1 ||
| [`Turtle`](Engine_LogicKeys.md#object-turtle) | Integer / Object | The number of turtle familiars spawned. | 1 ||

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
| [`ally_rewards`](#object-ally_rewards) | Object | Defines the rewards granted to the ally when the BirdRewards passive triggers. | 18 ||
| [`statuses`](#object-statuses) | Object | Defines the status effects applied when the parent trigger event occurs. | 5 ||

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
| `size` | Enum / Number | The scale factor (size multiplier) of the spawned unit. | 16 ||
| [`color`](./Arrays.md#array-color) | Array | The RGB color of the light source. | 16 ||
| [`glow`](./Arrays.md#array-glow) | Array | The RGBA glow color of the light source. | 8 ||

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 15 ||
| `stored_food_value` | Integer | The amount of food value stored in this pickup. | 15 ||
| [`frame_range`](./Arrays.md#array-frame_range) | Array | Specifies the minimum and maximum animation frame for the health pickup. | 15 ||
| `anything_eats` | Boolean | If true, any unit can consume this health pickup. | 4 ||
| `force_frame` | Integer | Forces the health pickup to use a specific animation frame. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 12 ||
| [`AllStatsUp`](./Enums.md) | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | 2 |
| [`Consumed`](Abilities_and_Spells.md#object-consumed) | Object | An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`. | 4 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1695 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 750 ||
| [`Stun`](./Enums.md) | Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 98 | 1 |
| [`Burn`](./Enums.md) | Integer | The amount of Burn applied, either as a fixed number or a formula string. | 85 | 2 |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 37 | 1 |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 22 | -1 |
| `Vaporize` | `Number` | Removes the target from play, preventing its corpse from being interacted with. | 21 ||
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 12 | 2 |
| `BlackHoleSuck` | `Number` | The strength of the black hole's pull effect. | 1 ||

</details>

---

### Object: `ImmediateAbilityReaction`


**Definition:** No definition provided.  
**Total Count:** 13


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 13 ||
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 6 ||
| `backstabs_only` | Boolean | If true, the reaction only triggers on backstab damage. | 2 ||
| `damage_threshold` | Integer | The amount of damage that must be dealt to trigger the ability reaction. | 2 ||
| `even_if_blocked` | Boolean | If true, the reaction triggers even if the damage is blocked. | 2 ||
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 2 ||
| `health_threshold` | Integer | The health value at or below which the reaction triggers. -1 disables this check. | 2 ||
| `buddy_damage_only` | Boolean | If true, only damage dealt by the unit's buddy triggers the reaction. | 1 ||
| `target_furthest_valid` | Boolean | If true, the reaction targets the furthest valid enemy. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 13 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 12 ||
| [`threshold`](./Enums.md) | Enum / Integer | The health threshold value, either as a formula using X (max health) or a fixed integer. | 12 | 200 |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 7 ||
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 6 ||
| `use_ai` | Boolean | If true, the ability uses AI targeting logic when triggered at the threshold. | 2 ||
| `also_use_if_buddy_is_dead` | Boolean | If true, the ability is also triggered when the unit's buddy is dead. | 1 ||
| [`threshold_min`](./Math_Equations.md) | Equation | The minimum health threshold formula (e.g., X) for the ability to trigger. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 14 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 13 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 12 ||
| [`FormChange`](./Enums.md) | Enum | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 12 | Druid |
| [`ReplaceBasicAttack`](./Enums.md) | Enum | Specifies the ability ID that replaces the unit's basic attack. | 11 | BasicStraightShot |
| [`SelfStatusCarefulness`](./Enums.md) | Integer | The carefulness level when applying statuses to self, used to control stacking. | 2 | 1 |
| [`StatusCarefulness`](./Enums.md) | Integer | The carefulness level when applying statuses, used to control stacking behavior. | 2 | 1 |
| [`ExtraBasicAttacks`](./Enums.md) | Integer | The number of additional basic attacks the unit can perform per turn. | 1 | 1 |
| [`TinkererBasicAttackSwitching`](Cat_Classes.md#object-tinkererbasicattackswitching) | Object | Defines the abilities used for the Tinkerer's basic attack switching mechanic. | 1 ||

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
| [`do_all`](./Arrays.md#array-do_all) | Array | The list of abilities the AI executes in sequence during its turn. | 6 ||
| [`do`](./Enums.md#enum-do) | Enum | The single, specific ability the AI executes. | 3 ||
| [`do_one`](./Arrays.md#array-do_one) | Array | Specifies the ability references for a single bonus turn pattern at round end. | 2 ||
| [`do_random`](./Arrays.md#array-do_random) | Array | The list of abilities from which the AI randomly selects one to execute. | 2 ||
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array | The list of actions (typically empty) the AI takes when it does nothing. | 1 ||
| [`do_priority`](./Arrays.md#array-do_priority) | Array | The list of abilities the AI executes, evaluating them in order of highest priority. | 1 ||

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
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 38 ||
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 20 ||
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A probability (decimal or percentage) for a form change or other effect to occur. | 12 ||
| `spawn_on_death_hit` | Boolean | If true, spawning only occurs when the damage is lethal. | 10 ||
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 2 ||
| `consider_all_layers` | Boolean | If true, considers all map layers when determining the spawn location. | 2 ||
| [`auto_cast`](./Enums.md#enum-auto_cast) | Enum | Specifies the ability to automatically cast on the spawned unit. | 1 ||
| `melee_ability_only` | Boolean | If true, spawning only occurs in response to melee damage. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 8 ||
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 8 ||

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
| [`weights`](./Enums.md#enum-weights) | Array / Enum | Specifies the weight array or named preset for the crazy eye background AI. | 9 ||
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 10 ||
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 8 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 6 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 6 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 4 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| `move_speed_multiplier` | Number | A multiplier for the unit's base movement speed. | 1 ||

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
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 9 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 9 ||
| [`exclude`](./Enums.md#enum-exclude) | Enum | Specifies an element or effect that does not trigger the form change. | 5 ||
| [`particle`](./Enums.md#enum-particle) | Enum | Specifies the particle effect displayed. | 5 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 5 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 ||
| [`StrengthUp`](./Enums.md) | Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 7 | 2 |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 4 | 2 |
| [`Slow`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 ||
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 8 ||
| [`initiative`](./Enums.md#enum-initiative) | Enum / Integer | The unit's turn order priority; can be an integer modifier or 'keep_turns_end_turn' to force end of turn after acting. | 4 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||

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
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 9 ||
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 9 ||

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
| [`form_offmap`](./Enums.md#enum-form_offmap) | Enum | Specifies the form name to use when the unit is off the map. | 8 ||
| [`form_onmap`](./Enums.md#enum-form_onmap) | Enum | Specifies the form name to use when the unit returns to the map. | 8 ||

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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 4 ||
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 4 ||
| `chain` | Boolean | Specifies the ability to chain into and execute. | 2 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 7 ||
| `flat_chance` | Integer | The base percentage chance to spit when taking damage. | 5 ||
| `chance_per_damage` | Integer | The additional percentage chance to spit per point of damage taken. | 3 ||
| `backstabs_only` | Boolean | If true, the reaction only triggers on backstab damage. | 1 ||
| `even_on_0_damage_if_knockback` | Boolean | If true, the reaction triggers on zero damage if knockback occurs. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 11 ||
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 7 ||
| `on_self_move_too` | Boolean | If true, the reaction triggers when the unit themselves move. | 3 ||
| `objects_too` | Boolean | If true, the reaction triggers on movement of objects as well. | 2 ||
| `blind_spot` | Boolean | If true, the reaction triggers only on movement from a blind spot. | 1 ||
| `forward_only` | Boolean | If true, the reaction triggers only on forward movement relative to the unit. | 1 ||
| `self_move_exclude_self_abilities` | Boolean | If true, movement caused by the unit's own abilities does not trigger the reaction. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 6 ||
| `count` | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 6 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 6 ||

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
| [`priming`](./Enums.md#enum-priming) | Enum | Specifies the form name to use while the unit is priming an ability. | 6 ||
| [`not_priming`](./Enums.md#enum-not_priming) | Enum | Specifies the form name to use when the unit is not priming an ability. | 6 ||

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
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 5 ||
| `move_far` | Boolean | If true, the unit moves the maximum distance towards the damage source. | 4 ||
| [`check_in_form`](./Enums.md#enum-check_in_form) | Enum | Specifies the form the unit must be in to trigger movement. | 2 ||
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| `can_move_zero` | Boolean | If true, the unit can move even if the distance to the damage source is zero. | 1 ||
| [`check_has_status`](./Enums.md#enum-check_has_status) | Enum | Specifies a status effect the unit must have for the movement to trigger. | 1 ||
| `do_not_move_on_top` | Boolean | If true, the unit stops before reaching the damage source's tile. | 1 ||
| `face_towards_after` | Boolean | If true, the unit rotates to face the damage source after moving. | 1 ||
| [`ignore_tagged_sources`](./Enums.md#enum-ignore_tagged_sources) | Enum | Specifies a unit tag to ignore as a damage source for movement. | 1 ||
| `move_short` | Boolean | If true, the unit moves a shorter distance towards the damage source. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 7 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 5 ||
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 3 ||
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum | Specifies a tag that the target unit must have for the team cast to trigger. | 3 ||
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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 5 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 5 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 4 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 4 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||

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
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 3 ||
| [`character_filter`](./Arrays.md#array-character_filter) | Array | Specifies which characters to consider as killers when moving towards them. | 3 ||

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
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 6 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 6 ||

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
| [`first_turn`](./Enums.md#enum-first_turn) | Enum | Determines when the spawned unit takes its first turn relative to the spawn event. | 4 ||
| [`obj`](./Enums.md#enum-obj) | Array / Enum | Specifies one or more object names to bounce towards the target. | 4 ||

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
| `range` | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 4 ||

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
| [`animation_suffix`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Specifies an animation suffix for the current form, used to load different sprites. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 22 ||
| [`struggle_ability`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of the ability the consumed unit uses to attempt escape. | 17 ||
| `force_contact` | `Boolean` | If true, the consumed unit is forced into contact with the consumer. | 15 ||
| `instant` | `Boolean` | If true, the consumption happens immediately without a timer. | 12 ||
| [`mount_mode`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the mounting mode; values include 'auto' or 'true'. | 12 ||
| `do_not_pop_corpse` | `Boolean` | If true, the consumed unit's corpse is not popped upon consumption. | 11 ||
| [`drop_on_death`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Determines if and how the consumed unit is dropped on death; values include 'true', 'false', or 'deferred'. | 11 ||
| `use_placeholder` | Boolean | If true, renders the ability using a temporary placeholder animation instead of the final art. | 3 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 ||
| `show_name` | Boolean | If true, displays the ability name when force used. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 4 ||
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 4 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 4 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 4 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 3 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 3 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||

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
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 55 ||
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 5 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 5 |
| [`AllStatsUp`](./Enums.md) | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | 2 |
| [`Conditional_BadRoll`](Abilities_and_Spells.md#object-conditional_badroll) | Object | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 1 ||
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | 2 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 34 ||
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 5 | 5 |
| [`UseAbility_NonStack`](./Enums.md) | Enum | Specifies an ability to use on kill that does not stack with itself. | 3 | BBTransformZealot |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [`ExtraBasicAttacks_Status`](./Enums.md) | Integer | The number of additional basic attacks the unit can perform each turn. | 2 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | 2 |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | 2 |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the source. | 1 | 1 |

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
| `cleanse_on_apply` | Boolean | If true, removes any existing stun effect when this immunity is applied. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 ||
| `cancel_movement` | Boolean | If true, the trapper cancels the trapped unit's movement. | 2 ||
| `pathfinding_avoidance` | Integer | The weight that makes other units avoid traversing this tile during pathfinding. | 2 ||
| `range` | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 2 ||

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 ||
| [`frame_range`](./Arrays.md#array-frame_range) | Array | Specifies the minimum and maximum animation frame for the health pickup. | 3 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

</details>

---

### Object: `Buddy`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 3 ||
| [`obj`](./Enums.md#enum-obj) | Array / Enum | Specifies one or more object names to bounce towards the target. | 3 ||
| `reclaim_if_lost` | Boolean | If true, the buddy can be reclaimed after being lost. | 1 ||

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
| [`formchange`](./Enums.md#enum-formchange) | Enum | Specifies the form to change into. | 3 ||
| [`statuses`](#object-statuses) | Object | Defines the status effects applied when the parent trigger event occurs. | 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 ||
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 3 ||
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`form_above`](./Enums.md#enum-form_above) | Enum | The form to change to when health is above the threshold. | 3 ||
| [`form_below`](./Enums.md#enum-form_below) | Enum | The form to change to when health is below the threshold. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`threshold`](./Enums.md) | Enum / Integer | The health threshold value, either as a formula using X (max health) or a fixed integer. | 3 | 200 |
| `count_shield` | Boolean | If true, shields count towards the health threshold calculation. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 ||
| [`statuses_on_enter_form`](#object-statuses_on_enter_form) | Object | Statuses or abilities applied when entering this form. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 ||

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 ||
| [`frame_range`](./Arrays.md#array-frame_range) | Array | Specifies the minimum and maximum animation frame for the health pickup. | 3 ||

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
| [`formchange`](./Enums.md#enum-formchange) | Enum | Specifies the form to change into. | 3 ||
| [`statuses`](#object-statuses) | Object | Defines the status effects applied when the parent trigger event occurs. | 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||

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
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 3 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`PassiveGroup`](#object-passivegroup) | Object | A group of passive abilities that can be randomly assigned. | 2 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Contains status effects to add to the basic attack. | 1 ||
| [`TransformInXTurns`](#object-transforminxturns) | Object | Defines a delayed transformation after a set number of turns, with optional target object and initiative handling. | 1 ||

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
| [`brain`](./Enums.md#enum-brain) | Enum | Specifies the AI brain type used for decision-making logic. | 4 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 4 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 4 ||
| [`pattern`](#object-pattern) | Object | Defines a sequence of actions the AI will execute in order, with optional priority or all-in-one. | 3 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 ||
| `wait_till_turn` | Boolean | If true, the form change will not occur until the unit's next turn. | 1 ||

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
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 3 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 3 ||
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 ||
| `force_display_name` | Boolean | If true, forces the display name to show for the ability. | 2 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 ||
| `range` | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 5 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 5 ||

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
| `Fury` | Integer | The amount of Fury (bonus damage or charges) gained. | 4 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`FormChange`](./Enums.md) | Enum | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 1 | Druid |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 9 ||
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 6 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 ||
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 2 ||
| `health_threshold` | Integer | The health value at or below which the reaction triggers. -1 disables this check. | 2 ||
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum | Specifies the tag used to identify allied warriors for this ability. | 2 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 ||
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`Leave`](Engine_LogicKeys.md#object-leave) | Enum / Object | Specifies the ability used when this unit leaves the field. | 2 ||
| [`Return`](Engine_LogicKeys.md#object-return) | Enum / Object | Specifies the ability used when this unit returns to the field. | 2 ||

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
| `odds` | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 37 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 37 | |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 28 ||
| [`FindItemFromPool`](./Enums.md) | Enum | Specifies the loot pool from which to find an item, with an optional chance. | 5 | eagle_pool |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 2 ||

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
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 1 ||
| `instant` | `Boolean` | If true, the consumption happens immediately without a timer. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 ||

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
| [`do`](./Enums.md#enum-do) | Enum | The single, specific ability the AI executes. | 2 ||

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 ||

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| `use_turn_animations` | Boolean | If true, uses turn-based animations for the face change. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||

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
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 2 ||
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 2 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||

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
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 24 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 22 ||
| `displace` | Boolean | If true, the knockback also displaces the target to a different tile. | 2 ||
| [`self_damage`](./Enums.md) | Boolean / Integer | Defines damage or effects applied to the caster when using the ability. | 2 | 2 |
| [{Damaging Keys}](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 2 |

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
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||

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
| [`Cat`](#object-cat) | Object | Defines the behavior and form change for captured cat units. | 2 ||
| [`NonCat`](#object-noncat) | Object | Defines the behavior and form change for captured non-cat units. | 2 ||
| [`Nothing`](#object-nothing) | Object | Defines the behavior when nothing is captured, typically just an animation. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 2 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move_speed_multiplier`](./Enums.md#enum-move_speed_multiplier) | Number | A multiplier for the unit's base movement speed. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 ||

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
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 ||
| [`target_filter`](./Enums.md#enum-target_filter) | Enum | Specifies which targets the protection applies to, based on their unit type or tag. | 2 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 ||

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 4 ||

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
| [`SlotResult_Jackpot_Coins`](Engine_LogicKeys.md#object-slotresult_jackpot_coins) | Integer / Object | The result of a jackpot roll that spawns coins, or the weight of that result in the pool. | 2 ||
| [`SlotResult_Explode`](Engine_LogicKeys.md#object-slotresult_explode) | Integer / Object | The result of an explosion roll, or the weight of that result. | 1 ||
| [`SlotResult_Nothing`](Engine_LogicKeys.md#object-slotresult_nothing) | Integer / Object | The result of a nothing roll, or the weight of that result. | 1 ||
| [`SlotResult_RandomPickup`](Engine_LogicKeys.md#object-slotresult_randompickup) | Integer / Object | The result of a random pickup roll, or the weight of that result. | 1 ||

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 2 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 ||
| [`FindItemFromPool`](./Enums.md) | Enum | Specifies the loot pool from which to find an item, with an optional chance. | 2 | eagle_pool |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 38 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 14 |
| [`StrengthUp`](./Enums.md) | Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 4 | 2 |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 3 | -1 |
| [`RemoveStatusStacks`](Abilities_and_Spells.md#object-removestatusstacks) | Object | An object specifying a status name and the number of stacks to remove from the target. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 ||
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object | Defines the damage and effects applied back to a melee attacker upon being hit. | 2 ||

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
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum | The ability used for the craft action in the Tinkerer's basic attack switching. | 3 ||
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum | The ability used for the throw action in the Tinkerer's basic attack switching. | 3 ||

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
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 2 ||
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 2 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 2 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 2 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 2 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`PermanentMadness`](./Enums.md) | Integer | The number of permanent madness stacks applied. | 1 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 ||
| [`Bleed`](./Enums.md) | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 3 | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`StacyMutant_Brace`](#object-stacymutant_brace) | Object | A passive group granting the Brace ability and cosmetic changes. | 1 ||
| [`StacyMutant_Counter`](#object-stacymutant_counter) | Object | A passive group granting a counter attack and a bleed effect on basic attacks. | 1 ||
| [`StacyMutant_Damage`](#object-stacymutant_damage) | Object | A passive group increasing damage and decreasing max health with cosmetic changes. | 1 ||
| [`StacyMutant_DoubleHead`](#object-stacymutant_doublehead) | Object | A passive group granting an extra dispersed turn and cosmetic changes. | 1 ||
| [`StacyMutant_Fire`](#object-stacymutant_fire) | Object | A passive group granting fire immunity and a lava shot basic attack. | 1 ||
| [`StacyMutant_Health`](#object-stacymutant_health) | Object | A passive group increasing max health, reducing speed, and scaling size. | 1 ||
| [`StacyMutant_Holy`](#object-stacymutant_holy) | Object | A passive group granting a divine shield and cosmetic changes. | 1 ||
| [`StacyMutant_Ice`](#object-stacymutant_ice) | Object | A passive group granting ice immunity and an ice breath basic attack. | 1 ||
| [`StacyMutant_Lightning`](#object-stacymutant_lightning) | Object | A passive group granting electric immunity and a lightning dash basic attack. | 1 ||
| [`StacyMutant_Mirror`](#object-stacymutant_mirror) | Object | A passive group granting projectile reflection and random magic missile each turn. | 1 ||
| [`StacyMutant_Speed`](#object-stacymutant_speed) | Object | A passive group increasing speed, reducing damage, and scaling size. | 1 ||
| [`StacyMutant_Thorns`](#object-stacymutant_thorns) | Object | A passive group granting thorns damage and cosmetic changes. | 1 ||

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
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 1 ||

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
| [`brain`](./Enums.md#enum-brain) | Enum | Specifies the AI brain type used for decision-making logic. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||
| [`pattern`](#object-pattern) | Object | Defines a sequence of actions the AI will execute in order, with optional priority or all-in-one. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`aura_requires_tag`](./Enums.md#enum-aura_requires_tag) | Enum | Specifies the tag that units must have to be affected by this aura. | 1 ||
| [`range`](./Enums.md#enum-range) | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 7 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 7 ||

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
| `DemonicGlyph_Bite` | Integer | The weight for the demonic glyph of bite, or its configuration. | 1 ||
| `DemonicGlyph_Bounce` | Integer | The weight for the demonic glyph of bounce, or its configuration. | 1 ||
| `DemonicGlyph_Fire` | Integer | The weight for the demonic glyph of fire, or its configuration. | 1 ||
| `DemonicGlyph_Movement` | Integer | The weight for the demonic glyph of movement, or its configuration. | 1 ||
| `DemonicGlyph_Summon` | Integer | The weight for the demonic glyph of summon, or its configuration. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ally_damage`](./Enums.md#enum-ally_damage) | Enum | Specifies the cheer effect when an ally takes damage. | 1 ||
| [`ally_dead`](./Enums.md#enum-ally_dead) | Enum | Specifies the cheer effect when an ally dies. | 1 ||
| [`enemy_damage`](./Enums.md#enum-enemy_damage) | Enum | Specifies the cheer effect when an enemy takes damage. | 1 ||
| [`enemy_dead`](./Enums.md#enum-enemy_dead) | Enum | Specifies the cheer effect when an enemy dies. | 1 ||
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum | Specifies the tag used to identify allied warriors for this ability. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`alert_form`](./Enums.md#enum-alert_form) | Enum | Specifies the form to use when the unit is alerted. | 1 ||
| [`default_form`](./Enums.md#enum-default_form) | Enum | Specifies the default form before aggro. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 6 ||
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 6 ||

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
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 1 ||

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
| `passives_health_threshold` | Integer | The health percentage threshold at which the boss's passive abilities change. | 1 ||
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array | An array of piece names that are considered actively part of the current form. | 1 ||
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array | An array of piece names that are considered passively part of the current form. | 1 ||

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
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array | An array of piece names that are considered actively part of the current form. | 1 ||
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array | An array of piece names that are considered passively part of the current form. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`new_music`](./Enums.md#enum-new_music) | Enum | Specifies the music track to play during the boss's head drop-in animation. | 1 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| `odds` | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 |
| [`Madness`](./Enums.md) | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | 1 |

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
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 ||
| `RemoveKnockback` | `Number` | The number of knockback stacks removed from the received damage. | 1 ||
| [`TempPassiveUntilSettled`](#object-temppassiveuntilsettled) | Object | An object containing a temporary passive that is applied until the character's position is settled. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 ||

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
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 ||
| `RemoveKnockback` | `Number` | The number of knockback stacks removed from the received damage. | 1 ||
| [`TempPassiveUntilSettled`](#object-temppassiveuntilsettled) | Object | An object containing a temporary passive that is applied until the character's position is settled. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 ||

</details>

---

### Object: `CounterAttack`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 ||
| `without_orienting` | Boolean | If true, the counter-attack does not rotate the character to face the attacker. | 1 ||

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
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | Inherits game-wide rule modifiers. You can utilize any key from the Engine Global Modifier Keys list here to alter overarching game mechanics (e.g., changing gravity or stamina costs). | 5 ||
| `BloodRain` | `Number` | If non-zero, enables the blood rain visual effect. | 3 ||
| [`LowerAmbientLight`](Abilities_and_Spells.md#object-lowerambientlight) | Object | If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly. | 3 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 |

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 |

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
| `health` | Integer | The maximum hit points of the unit. | 6 ||
| `rounds` | Integer | The number of rounds after which the auto-revive triggers. | 6 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||

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
| `dice_size` | Integer | The number of sides on the die. | 1 ||
| `knockback_damage` | Integer | The amount of damage dealt by the knockback. | 1 ||

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
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Associates keyword tooltips with the ability, often used for status effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 |

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
| `deferred` | Boolean | If true, the destruction is deferred until the character is settled. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||

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
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| `move_speed_multiplier` | Number | A multiplier for the unit's base movement speed. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| `move_speed_multiplier` | Number | A multiplier for the unit's base movement speed. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Associates keyword tooltips with the ability, often used for status effects. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum | Determines the ability used when the Dybbuk possession ends. | 1 ||
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 1 ||

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
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target regardless of accuracy or evasion. | 1 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 1 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 1 ||
| `makes_contact` | `Boolean` | If true, the damage instance is considered a contact hit, triggering contact-based passives on both the attacker and target. | 1 ||
| `piercing` | `Boolean` | If true, the damage instance ignores armor or damage reduction effects on the target. | 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 1 ||

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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 23 ||
| [`Conditional_HasKnockback`](#object-conditional_hasknockback) | Object | An object containing actions that execute if the incoming damage has knockback. | 1 ||
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 ||

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
| [`Default`](#object-default) | Enum / Object | The default form configuration for a unit, containing its standard stats and abilities. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 1 ||
| `override_hit_animation` | Boolean | If true, the character's hit animation is overridden by the face-away animation. | 1 ||
| `use_turn_animations` | Boolean | If true, uses turn-based animations for the face change. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`queue`](./Enums.md#enum-queue) | Enum | Specifies the ability queued to fire the boss's beam. | 1 ||
| [`release`](./Enums.md#enum-release) | Enum | Specifies the ability queued to release the boss's stored beams. | 1 ||
| [`transform`](./Enums.md#enum-transform) | Enum | Specifies the ability queued to transform the boss into its next form. | 1 ||

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
| [`GlobalSpawnCharacter`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Specifies the name of a character to spawn globally. | 1 ||
| `PlayBackground` | `Number` | Specifies the background index to play. | 1 ||
| [`SwitchMusic`](Abilities_and_Spells.md#object-switchmusic) | Object | Defines a new song or layer for the background music. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| `icon` | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 1 ||
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`ForceUseAbility`](#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 1 | CancerExplode |

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
| `icon` | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 1 ||
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`ForceUseAbility`](#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 1 | CancerExplode |

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
| `icon` | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 1 ||
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

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
| `radius` | Array / Integer | The range in tiles of the distortion ring effect; an array [min, max] specifies a random radius within that range. | 1 ||
| [`reset_center_because_no_target_halflife`](./Enums.md#enum-reset_center_because_no_target_halflife) | Number | The half-life for the pupil position to reset to center when no target is available. | 1 ||
| [`reset_center_because_of_animation_halflife`](./Enums.md#enum-reset_center_because_of_animation_halflife) | Number | The half-life for the pupil position to reset to center during an animation. | 1 ||
| [`teleport_tracking_halflife`](./Enums.md#enum-teleport_tracking_halflife) | Number | The half-life for the pupil tracking to reacquire a target after a teleport. | 1 ||
| [`tracking_acquisition_halflife`](./Enums.md#enum-tracking_acquisition_halflife) | Number | The half-life for the pupil tracking to smoothly acquire a new target. | 1 ||
| [`look_at_offset`](./Arrays.md#array-look_at_offset) | Array | A 3D vector offset from the head position that the pupils should look at. | 1 ||
| [`virtual_head_position`](./Arrays.md#array-virtual_head_position) | Array | A 3D vector representing the virtual position of the head for pupil tracking. | 1 ||

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
| [`state_health`](./Arrays.md#array-state_health) | Array | An array of health thresholds defining state transitions. | 1 ||

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
| [`other_character`](./Enums.md#enum-other_character) | Enum | Specifies the name of the other boss character whose animations are synced. | 1 ||
| [`other_form_change_abilities`](#object-other_form_change_abilities) | Object | An object mapping form names to the other character's form change abilities. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 1 ||

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
| [`chance`](./Enums.md#enum-chance) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||
| [`pool`](./Enums.md#enum-pool) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 1 ||

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
| [`exit_animations`](#object-exit_animations) | Object | An object mapping exit conditions to their corresponding animation names. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 1 ||
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 ||
| `weak_threshold` | Integer | The health threshold below which the unit is considered weakened. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`threshold`](./Enums.md) | Enum / Integer | The health threshold value, either as a formula using X (max health) or a fixed integer. | 1 | 200 |

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
| [`clipname`](./Enums.md#enum-clipname) | Enum | Specifies the animation clip name to use for the alt state. | 1 ||
| [`thresholds`](./Arrays.md#array-thresholds) | Array | An array of health percentage thresholds that trigger an alt state. | 1 ||

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
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||

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
| `health` | Integer | The maximum hit points of the unit. | 3 ||
| `playercat_health` | Integer | The percentage of maximum health the player cat must have to trigger the rebirth. | 3 ||
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`form_unwashed`](./Enums.md#enum-form_unwashed) | Enum | Specifies the form name for the unwashed state. | 1 ||
| [`form_washed`](./Enums.md#enum-form_washed) | Enum | Specifies the form name for the washed state. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| `speed` | Array / Number | The speed of the projectile or move, can be a value or a range. | 3 ||
| [`amount`](./Arrays.md#array-amount) | Array | For ambient light, the target brightness value (as a float or percentage array for RGB). | 3 ||

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
| [`head_drop`](./Enums.md#enum-head_drop) | Enum | Specifies the ability triggered when the head drops down. | 1 ||
| [`leg_leave`](./Enums.md#enum-leg_leave) | Enum | Specifies the ability triggered when the legs leave the body. | 1 ||
| [`leg_return`](./Enums.md#enum-leg_return) | Enum | Specifies the ability triggered when the legs return to the body. | 1 ||
| `stable_legs` | Integer | The number of legs that must be stable for the head to drop. | 1 ||

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
| [`sound_event`](./Enums.md#enum-sound_event) | Enum | Specifies the sound event to play when the pickup is used. | 1 ||
| [`Cleanse`](./Enums.md) | Integer | The number of stacks of negative status effects removed from the target. | 1 | 0 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`spell`](./Enums.md#enum-spell) | Enum | Specifies the spell ability to use as a reaction. | 1 ||
| [`trinket`](./Enums.md#enum-trinket) | Enum | The name of the trinket item the unit starts with. | 1 ||
| [`weapon`](./Enums.md#enum-weapon) | Enum | The name of the weapon item the unit starts with. | 1 ||

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
| [`eat_damage`](#object-eat_damage) | Object | An object defining the damage properties of the eat attack. | 1 ||
| [`tumor_object`](./Enums.md#enum-tumor_object) | Enum | Specifies the name of the tumor object to spawn. | 1 ||

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
| [`Cat`](#object-cat) | Object | Defines the behavior and form change for captured cat units. | 1 ||
| [`grow_ability`](./Enums.md#enum-grow_ability) | Enum | Specifies the ability used by the tumor to grow. | 1 ||
| [`NonCat`](#object-noncat) | Object | Defines the behavior and form change for captured non-cat units. | 1 ||
| [`pass_ani`](./Enums.md#enum-pass_ani) | Enum | Specifies the animation played when passing something to the tumor. | 1 ||
| [`receive_ani`](./Enums.md#enum-receive_ani) | Enum | Specifies the animation played when receiving something from the tumor. | 1 ||
| [`considered_forms`](./Arrays.md#array-considered_forms) | Array | An array of form names the tumor considers for interaction. | 1 ||

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
| [`eject_ability`](./Enums.md#enum-eject_ability) | Enum | Specifies the ability used to eject the mounted character. | 1 ||
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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`weights`](./Enums.md#enum-weights) | Array / Enum | Specifies the weight array or named preset for the crazy eye background AI. | 1 ||

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
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 1 ||

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
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 1 ||
| `once_per_turn` | Boolean | If true, the movement away can only trigger once per turn. | 1 ||
| [`weights`](./Enums.md#enum-weights) | Array / Enum | Specifies the weight array or named preset for the crazy eye background AI. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| [`obj`](./Enums.md#enum-obj) | Array / Enum | Specifies one or more object names to bounce towards the target. | 1 ||
| [`count`](./Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||

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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||

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
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Associates keyword tooltips with the ability, often used for status effects. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||

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
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 |

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`Boris`](#object-boris) | Enum / Object | Specifies the 'Boris' form within FormChanger, with its own animation suffix and passives. | 1 ||
| [`Explosive`](#object-explosive) | Enum / Object | Specifies the 'Explosive' form within FormChanger, with its own animation suffix and passives. | 1 ||
| [`Holy`](#object-holy) | Enum / Object | Specifies the 'Holy' form within FormChanger, with its own animation suffix and passives. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 18 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 18 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 18 ||

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| `animation_suffix` | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 33 ||
| [`StatusGroup`](Abilities_and_Spells.md#object-statusgroup) | Object | A container grouping multiple status effects to be applied simultaneously. | 3 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 8 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 5 ||
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 3 ||

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
| [`do_priority`](./Arrays.md#array-do_priority) | Array | The list of abilities the AI executes, evaluating them in order of highest priority. | 1 ||

</details>

---


<details>
<summary><b>AddStatusToReceivedDamage</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>AddStatusToSpells</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>AddStatusToTrampleDamage</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>PassiveWhenDead</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>StatusOnEnemyConfused</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

<details>
<summary><b>StatusOnSpawnIn</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 ||

</details>

### Object: `RunFar`


**Definition:** AI Movement: Maximize distance from targets.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| `allow_decision_mid_turn` | Boolean | If true, allows the decision to run to occur mid-turn instead of at the end. | 1 ||
| [`legacy_savekey`](./Enums.md#enum-legacy_savekey) | Enum | Specifies the save key used to persist a legacy stolen cat ID. | 1 ||

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
| [`default`](#object-default) | Enum / Object | The default configuration or value used when no specific override is provided. | 1 ||
| [`thresholds`](./Arrays.md#array-thresholds) | Array | An array of health percentage thresholds that trigger an alt state. | 1 ||

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
| `include_coins` | Boolean | If true, coins are included in the shared pickup pool. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| `pop_chance` | Integer | The percentage chance that the first round is skipped. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`Fire`](#object-fire) | Integer / Object | Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack. | 1 ||
| [`FireFull`](#object-firefull) | Integer / Object | Defines the 'FireFull' form, a fully charged fire state with its own animation and visual combo. | 1 ||
| [`Normal`](#object-normal) | Integer / Object | The normal form configuration, used as a baseline state for shape-shifting units. | 1 ||
| [`NormalFull`](#object-normalfull) | Integer / Object | As an object, defines the normal full form with a spit attack and conditional form change. As an integer, specifies alt graphics index. | 1 ||
| [`Tar`](#object-tar) | Integer / Object | If an integer, the number of tar stacks. If an object, the form state for the tar-covered unit. | 1 ||
| [`TarFull`](#object-tarfull) | Integer / Object | If an integer, the number of full tar stacks. If an object, the form state for the fully tar-covered unit. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`Brace`](./Enums.md) | Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | 99 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Contains status effects to add to the basic attack. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 ||
| [`CounterAttack`](Cat_Mutations.md#object-counterattack) | Array / Enum / Object | Specifies the ability used when the unit counterattacks after being hit. | 1 | [GSScream] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`AddDamage`](./Enums.md) | Integer | The amount of damage added to all attacks. Negative values reduce damage. | 1 | 2 |
| [`AddMaxHealth`](./Enums.md) | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 1 | -25 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 ||
| [`ExtraDispersedTurns`](./Enums.md) | Integer | The number of additional or fewer turns in the dispersed turn order. | 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 ||
| [`ElementImmune`](./Enums.md) | Enum | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 1 | Ice |
| [`ReplaceBasicAttack`](./Enums.md) | Enum | Specifies the ability ID that replaces the unit's basic attack. | 1 | BasicStraightShot |
| [`ReplaceBrain`](#object-replacebrain) | Object | Defines a replacement AI brain and behavior pattern for the mutant. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`AddMaxHealth`](./Enums.md) | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 1 | -25 |
| [`AddSpeed`](./Enums.md) | Integer | The amount of speed added (or subtracted) to the unit. | 1 | 6 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 ||
| [`SizeScale`](./Enums.md) | Number | The multiplier applied to the unit's visual and hitbox size. | 1 | .8 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 ||
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`AddMovement`](./Enums.md) | Integer | The amount of bonus movement points added to the unit's base movement. | 1 | 2 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 ||
| [`ElementImmune`](./Enums.md) | Enum | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 1 | Ice |
| [`ReplaceBasicAttack`](./Enums.md) | Enum | Specifies the ability ID that replaces the unit's basic attack. | 1 | BasicStraightShot |
| [`ReplaceBrain`](#object-replacebrain) | Object | Defines a replacement AI brain and behavior pattern for the mutant. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 ||
| [`ElementImmune`](./Enums.md) | Enum | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 1 | Ice |
| [`ReplaceBasicAttack`](./Enums.md) | Enum | Specifies the ability ID that replaces the unit's basic attack. | 1 | BasicStraightShot |
| [`ReplaceBrain`](#object-replacebrain) | Object | Defines a replacement AI brain and behavior pattern for the mutant. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 ||
| [`ReflectProjectiles`](#object-reflectprojectiles) | Integer / Object | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 1 | 100 |
| [`StatusEachTurnEndForEachTurn`](#object-statuseachturnendforeachturn) | Object | Statuses applied at the end of each turn, with the number of turns as nested values. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`AddDamage`](./Enums.md) | Integer | The amount of damage added to all attacks. Negative values reduce damage. | 1 | 2 |
| [`AddSpeed`](./Enums.md) | Integer | The amount of speed added (or subtracted) to the unit. | 1 | 6 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 ||
| [`SizeScale`](./Enums.md) | Number | The multiplier applied to the unit's visual and hitbox size. | 1 | .8 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 ||
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 ||
| [`ForceUseAbility`](#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 2 | CancerExplode |

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
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 ||
| `consume` | Boolean | If true, the status is consumed after triggering. | 1 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`AllStatsUp`](./Enums.md) | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | 2 |
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | 2 |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 1 | 5 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 ||
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 3 | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`ForceUseAbility`](#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 1 | CancerExplode |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 ||
| [`RemoveAmbientLightEffects`](./Enums.md) | Integer | The fade-out duration in seconds for ambient light effects. | 1 | 4 |
| [`RemoveGlobalModifiers`](./Enums.md) | Array | List of global modifier names to remove upon death. | 1 | [BloodRain] |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 ||
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Object | The number of backflip charges, or an object defining its ability. | 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | 2 |

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
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | The name of the ability the target is forced to use. | 1 | KirbySpit |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

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
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Associates keyword tooltips with the ability, often used for status effects. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| [`alt_dead_ani`](./Enums.md#enum-alt_dead_ani) | Enum | Specifies the alternative death animation to use when the support unit dies instead of running. | 1 ||
| [`alt_dying_ani`](./Enums.md#enum-alt_dying_ani) | Enum | Specifies the alternative dying animation to use. | 1 ||

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
| [`form_in`](./Enums.md#enum-form_in) | Enum | Determines the form to change into when entering water. | 1 ||
| [`form_out`](./Enums.md#enum-form_out) | Enum | Determines the form to change into when leaving water. | 1 ||

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
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | Specifies the music layer to switch to (e.g., 'event', 'battle', 'map'). | 7 ||
| [`new_song`](./Enums.md#enum-new_song) | Enum | Specifies the song to switch to; 'same' keeps the current song playing on the new layer. | 6 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`no_buddy`](./Enums.md#enum-no_buddy) | Enum | Specifies an alternative form to use when there is no buddy. | 1 ||

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
| [`spell_use_groups`](./Arrays.md#array-spell_use_groups) | Array | List of spell use groups that the spawning phase can use. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 1 ||

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
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 ||
| [`groups`](./Arrays.md#array-groups) | Array | Groups of actors that this skin applies to. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 |

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
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 1 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`threshold`](./Enums.md) | Enum / Integer | The health threshold value, either as a formula using X (max health) or a fixed integer. | 1 | 200 |

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
| `Die` | `Number` | If set, kills the target immediately. | 1 ||
| [`Dumb`](#object-dumb) | Integer / Object | Defines the 'Dumb' form, which can be either a numeric value or an object with passives that disable spells and turn off TV. | 1 ||
| `Fuck` | Integer | The number of times the TV bot screen displays the 'Fuck' message. | 1 ||
| [`Obey`](#object-obey) | Integer / Object | As an object, defines an obey form that disables attacks and reacts with TV off. As an integer, defines a value (e.g., weight or count). | 1 ||
| `Shit` | Integer | The number of times the TV bot screen displays the 'Shit' message. | 1 ||
| [`Stop`](#object-stop) | Integer / Object | If an integer, the number of turns the unit is stopped. If an object, the form configuration for the stopped state. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 ||

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
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 1 ||
| `max_dist` | Integer | The maximum distance in tiles the target can be displaced by the knockback effect. | 1 ||
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | Specifies the ability that the unit needs to move close to use. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 1 ||

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
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 ||
| `respect_prime` | Boolean | If true, the ability will only be used if the unit is primed for it. | 2 ||

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
| [`ai`](#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 ||
| [`name`](./Strings.md#string-name) | Enum | Specifies the localized name string for the entity, item, or ability. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum | The localization string key used for the tooltip displayed on hover. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||

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
