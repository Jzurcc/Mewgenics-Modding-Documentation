# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Characters & Bosses

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `variant_of` | [`Enum/String`](./Enums.md#enum-variant_of) | `BirdSmall, BirdBase, Cherub` |  |
| `scale` | [`Enum/String`](./Enums.md#enum-scale) | `.5` |  |

</details>

---

### Context: `properties`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `faction` | [`Enum/String`](./Enums.md#enum-faction) | `enemies, birds, none` |  |
| `health` | Number | `7, 16, 2` |  |
| `tag` | [`Array`](./Arrays.md#array-tag) | `rat, animal, [ cat blob ]` | Specific entity tag required. |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `boss, object, cat` | Classification/category type. |
| `movement` | Number | `4, 5, 3` |  |
| `corpse_health` | [`Enum/String`](./Enums.md#enum-corpse_health) | `indestructible, 0, 3` |  |
| `inherit_faction` | Boolean | `false, true` |  |
| `dispersed_bonus_turns` | Number | `2, 0, 3` |  |
| `base_mana_regen` | Number | `3, 0, 999` |  |
| `size` | [`Enum/String`](./Enums.md#enum-size) | `gemini, 2x2, 3x3` |  |
| `shield` | Number | `100, 50, 65` |  |
| `move_block` | [`Enum/String`](./Enums.md#enum-move_block) | `everything_even_when_dead, nothing` |  |
| `kill_required` | Boolean | `false, true` |  |
| `can_be_backstabbed` | Boolean | `false` |  |
| `initiative` | Number | `-100, -999, 999` |  |
| `takes_turns` | Boolean | `false, true` |  |
| `mana_regen` | Number | `999` |  |
| `mana` | Number | `100` | Base maximum mana pool. |
| `flying` | Boolean | `true` |  |
| `banned_elite_buffs` | [`Array`](./Arrays.md#array-banned_elite_buffs) | `[ Twin ], [ Mad ], [ Protected ]` |  |
| `hidden_tag` | [`Enum/String`](./Enums.md#enum-hidden_tag) | `the_coven, [ bird bonusbird ], angeljunk` |  |
| `weak_threshold` | Number | `1, 0, 5` |  |
| `knockback_immune` | Boolean | `true` |  |
| `can_be_champion` | Boolean | `false, true` |  |
| `lock_orientation` | [`Array`](./Arrays.md#array-lock_orientation) | `[ -1 0 ], [ 0, -1 ], [ -1, 0 ]` |  |
| `ai_scale` | [`Enum/String`](./Enums.md#enum-ai_scale) | `.5, .25, .01` |  |
| `layer` | [`Enum/String`](./Enums.md#enum-layer) | `pickups, gas, all` |  |
| `auto_run_priority` | [`Enum/String`](./Enums.md#enum-auto_run_priority) | `stationary, support, default` |  |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Rock ], [ Earth ], [ Dust ]` |  |
| `inanimate` | Boolean | `true` |  |
| `disperse_main_turns` | Boolean | `false, true` |  |
| `hidden_tags` | [`Enum/String`](./Enums.md#enum-hidden_tags) | `terminator_mini, [ terminator_mini dc_cat ]` |  |
| `tags` | [`Array`](./Arrays.md#array-tags) | `[ cat robot ]` |  |
| `evenly_dispersed_bonus_turns` | Number | `2, 1, 3` |  |
| `exclude_from_hallucinate` | Boolean | `true` |  |
| `round_end_bonus_turns` | Number | `1` |  |
| `can_be_overkilled` | Boolean | `false, true` |  |
| `can_collect_coins` | Boolean | `false, true` |  |
| `deathpoof_size` | Number | `1` |  |
| `dispersed_bonus_turns_consider_initiative` | Boolean | `false` |  |
| `held_coins` | [`Array`](./Arrays.md#array-held_coins) | `[ 5 10 ], 0, 5` |  |
| `initial_health` | Number | `4, 10, 14` |  |
| `can_eat_food` | Boolean | `false, true` |  |
| `can_grant_extra_turns` | Boolean | `false` |  |
| `tall` | Boolean | `true` |  |
| `dispersed_bonus_turns_before_cats` | Boolean | `false, true` |  |
| `divine_shield` | Number | `2, 1, 3` |  |
| `is_player_cat` | Boolean | `false, true` |  |
| `boss_minions_runaway` | Boolean | `false` |  |
| `mana_matters` | Boolean | `false, true` |  |
| `access_to_player_inventory` | Boolean | `false, true` |  |
| `act_points` | Number | `2, 0, 4` |  |
| `takes_main_turn` | Boolean | `false` |  |
| `visually_spiky` | Boolean | `true` |  |
| `allow_passive_spelltransforming` | Boolean | `true` |  |
| `base_crit_chance` | Number | `0` |  |
| `last_turn_is_main_turn` | Boolean | `true` |  |
| `round_start_bonus_turns` | Number | `1` |  |
| `view_bleeding_characters_as_enemies` | Boolean | `true` |  |
| `aoe_pierce_mode` | [`Enum/String`](./Enums.md#enum-aoe_pierce_mode) | `block` |  |
| `base_initiative` | Number | `0, -1` |  |
| `base_movement` | Number | `4` |  |
| `catdata_ignore_skills` | Boolean | `true` |  |
| `disallow_items` | [`Enum/String`](./Enums.md#enum-disallow_items) | `Nuke, all` |  |
| `always_triggers_traps` | Boolean | `true` |  |
| `base_health` | Number | `0` |  |
| `base_health_regen` | Number | `0` |  |
| `base_initial_mana` | Number | `0` |  |
| `base_mana` | Number | `0` |  |
| `blocking` | Boolean | `false` |  |
| `can_be_elite` | Boolean | `false` |  |
| `can_run` | Boolean | `false` |  |
| `champion` | Boolean | `true` |  |
| `force_not_familiar` | Boolean | `true` |  |
| `hint_no_corpse` | Boolean | `true` |  |
| `must_start_facing_camera` | Boolean | `false` |  |
| `tile_desire_cost` | Number | `200, 100` |  |
| `uncapturable` | Boolean | `false, true` |  |
| `aggro_target_is_enemy` | Boolean | `true` |  |
| `allow_flying_effect` | Boolean | `true` |  |
| `allow_offmap_corpse` | Boolean | `true` |  |
| `allow_replacebrain` | Boolean | `false` |  |
| `always_face_forward` | Boolean | `true` |  |
| `capture_as_cat` | Boolean | `true` |  |
| `elite` | Boolean | `true` |  |
| `first_turn_is_main_turn` | Boolean | `true` |  |
| `ignore_mouseover` | Boolean | `true` |  |
| `ignore_tiles` | Boolean | `true` |  |
| `inanimate_can_receive_specific_statuses` | [`Array`](./Arrays.md#array-inanimate_can_receive_specific_statuses) | `[ Burn ]` |  |
| `mouseover_priority` | Number | `10` |  |
| `move_points` | Number | `2` |  |
| `pickup_type` | Number | `1` |  |
| `scale` | Number | `1.3` |  |
| `speculative_inanimate` | Boolean | `false` |  |
| `static` | Boolean | `true` |  |
| `two_fronts` | Boolean | `true` |  |
| `two_fronts_switch` | Boolean | `true` |  |
| `view_bugs_as_enemies` | Boolean | `true` |  |

</details>

---

### Context: `stats`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `strength` | Number | `8, 5, 4` |  |
| `constitution` | Number | `8, 9, 5` |  |
| `dexterity` | Number | `8, 9, 5` |  |
| `charisma` | Number | `8, 9, 5` |  |
| `intelligence` | Number | `10, 9, 5` |  |
| `speed` | Number | `7, 2, 5` | Base speed/initiative stat. |
| `luck` | Number | `8, 5, 3` |  |

</details>

---

### Context: `graphics`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `name` | String | `"ENEMY_MEDBIRD_NAME", "ENEMY_BIRD_NAME", "ENEMY_LITTLEBIRD_NAME"` | Localization key for the character's name. |
| `movieclip` | [`Enum/String`](./Enums.md#enum-movieclip) | `BirdMed, BirdSmall, BirdLarge` |  |
| `tooltip` | String | `"ENEMY_RADICALRAT_DESC", "ENEMY_BIRD_DESC", "ENEMY_CHERUB_FINALBOSS_DESC"` |  |
| `shadow_size` | Number | `2, .5, 3` |  |
| `scale` | [`Enum/String`](./Enums.md#enum-scale) | `.9, .5, .8` |  |
| `uifloaters_offset` | Number | `2.5, 2, 1.5` |  |
| `custom_cat_data` | [`Enum/String`](./Enums.md#enum-custom_cat_data) | `Kitten, Mangy, TomTom` |  |
| `water_mask` | [`Enum/String`](./Enums.md#enum-water_mask) | `square, medium, medmed` |  |
| `spawnin_animation` | String | `"digUp", digUp, "howl"` |  |
| `alt_animations` | [`Array`](./Arrays.md#array-alt_animations) | `[ [ idle girlyIdle ], [ [ idle twitchyIdle ], [ [ idle cuteIdle ]` |  |
| `piece_alt_frame` | Number | `7, 5, 3` |  |
| `shadow` | [`Enum/String`](./Enums.md#enum-shadow) | `MedSlimeShadow, TormentorShadow, none` |  |
| `move_speed_sync_frames` | Number | `7, 22.5, 40` |  |
| `no_splatter` | Boolean | `true` |  |
| `projectile_spawn_offset` | [`Array`](./Arrays.md#array-projectile_spawn_offset) | `[ 0 1.5 ], [ 0 1 ], [ .25 1 ]` |  |
| `tint` | [`Array`](./Arrays.md#array-tint) | `[ .7 1 .7 1 ], [ 0 0 0 1 ], green` |  |
| `move_speed_multiplier` | [`Enum/String`](./Enums.md#enum-move_speed_multiplier) | `.5, .66, 1.75` |  |
| `dont_sink` | Boolean | `true` |  |
| `art_flip` | Number | `-1` |  |
| `depth_offset` | [`Enum/String`](./Enums.md#enum-depth_offset) | `-.1, 5, .01` |  |
| `walk` | [`Enum/String`](./Enums.md#enum-walk) | `raptorWalk, stompwalk, zombieWalk` |  |
| `dead` | [`Enum/String`](./Enums.md#enum-dead) | `skeletonDead, empty` |  |
| `dying` | [`Enum/String`](./Enums.md#enum-dying) | `dead, dyingDisassembled` |  |
| `four_way_animations` | Boolean | `true` |  |
| `hit` | [`Enum/String`](./Enums.md#enum-hit) | `hitDisassembled, skeletonCorpseHit` |  |
| `stunned` | [`Enum/String`](./Enums.md#enum-stunned) | `dead, idleDisassembled` |  |
| `weak` | [`Enum/String`](./Enums.md#enum-weak) | `dead, idleDisassembled` |  |
| `deadhit` | [`Enum/String`](./Enums.md#enum-deadhit) | `skeletonCorpseHit` |  |
| `show_infinity_damage_warning` | Boolean | `true` |  |
| `always_huge_mask` | Boolean | `true` |  |
| `default_attack_animation` | [`Enum/String`](./Enums.md#enum-default_attack_animation) | `bite1, attack2` |  |
| `desc` | [`Enum/String`](./Enums.md#enum-desc) | `ENEMY_FATWOMAN_DESC, "OBJECT_DECOY_DESC"` | Localization key for the character's desc. |
| `shade_occluded_objects` | Boolean | `true` |  |
| `dodge` | [`Enum/String`](./Enums.md#enum-dodge) | `liquidmetaldodge` |  |
| `no_horizontal_flip` | Boolean | `true` |  |
| `non_blocking_animations` | [`Array`](./Arrays.md#array-non_blocking_animations) | `[ "hit" , "critical" ]` |  |
| `override_portrait` | [`Enum/String`](./Enums.md#enum-override_portrait) | `Cherub` |  |
| `randomize_starting_frame` | Boolean | `false` |  |
| `status_display_count_max` | Number | `5` |  |

</details>

---

### Context: `ai`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `brain` | [`Enum/String`](./Enums.md#enum-brain) | `PatternBrain, PlayerBrain, GenericBrain` |  |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `extra_careless, simple, default` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance_always_move, chaotic_runaway, bird` |  |
| `end_turn_on_formswitch` | Boolean | `false, true` |  |
| `auto_orient` | Boolean | `false` |  |
| `reset_pattern_on_formswitch` | Boolean | `false, true` |  |
| `stun_advances_pattern` | Boolean | `false, true` |  |
| `fallback_advances_pattern` | Boolean | `false, true` |  |
| `consider_spells` | Boolean | `false` |  |
| `animate_choice` | Boolean | `false, true` |  |
| `clamp_pattern` | Boolean | `true` |  |
| `randomize_pattern_start` | Boolean | `true` |  |
| `random_orient` | Boolean | `true` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `JohnnyBlast` |  |
| `dice_abilities` | [`Array`](./Arrays.md#array-dice_abilities) | `[ D6Fizzle D6Confused D6Poop D6Laser D6Quake D6Storm D6Wr...` |  |
| `never_hit_ally_corpses` | Boolean | `true` |  |
| `post_absorb_move_weights` | [`Enum/String`](./Enums.md#enum-post_absorb_move_weights) | `minimum_move` |  |
| `reset_pattern_on_round_begin` | Boolean | `true` |  |
| `roll_ability` | [`Enum/String`](./Enums.md#enum-roll_ability) | `RollDice` |  |

</details>

---

### Context: `abilities`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicMelee, None, DustMelee` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `DustMove, DefaultMove, None` |  |
| `spells` | [`Array`](./Arrays.md#array-spells) | `[ BirdFly ], [ TrampleDash MoveOne ], [ SpawnBomb BombRatTurtle RockToss_BomberRat ]` |  |
| `can_get_bonus` | Boolean | `true` |  |

</details>

---

### Context: `passives`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SpawnOnDeath` | [`Block`](./Characters_and_Bosses.md#context-spawnondeath) | `{ ... }, BiggestFood, FrankPinky` | Event Trigger: Spawns a specific entity when killed. |
| `Trample` | Number | `6, 5, 3` | Applies or references the 'Trample' effect/state. |
| `Robot` | [`Block`](./Items_and_Equipment.md#context-robot) | `{ ... }, 1` | Character Form: Behavior and stats for the 'Robot' state. |
| `Brace` | Number | `10, 1, 4` | Applies or references the 'Brace' effect/state. |
| `CounterAttack` | [`Enum/String`](./Enums.md#enum-counterattack) | `YeticatSnowball_Counter, BungaSwipe, attack` | Reaction: Executes a counter-attack ability when hit. |
| `DeathRattle` | [`Block`](./Characters_and_Bosses.md#context-deathrattle) | `{ ... }, BoomerCatExplode, MoonHead_KillHands` | Event Trigger: Executes logic or abilities exactly when the character dies. |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Creep, Fire, Ice` | Applies or references the 'ElementImmune' effect/state. |
| `ImmediateAbilityReaction` | [`Enum/String`](./Enums.md#enum-immediateabilityreaction) | `NubsGoop, ChubsGoop, BumbleButt` | Reaction: Executes an ability instantly, interrupting the current sequence. |
| `Undead` | Number | `1` | Applies or references the 'Undead' effect/state. |
| `AddStatusToBasicAttack` | [`Block`](./Characters_and_Bosses.md#context-addstatustobasicattack) | `{ ... }` | Modifier: Injects a status effect payload into the character's basic attacks. |
| `AbilityReaction` | [`Block`](./Characters_and_Bosses.md#context-abilityreaction) | `{ ... }, TC_DashReaction, attack` | AI Trigger: Executes an ability in reaction to a specific event (e.g., taking damage). |
| `StatusImmunity` | [`Enum/String`](./Enums.md#enum-statusimmunity) | `Webbed, Poison, [ Poison, Bleed ]` | Applies or references the 'StatusImmunity' effect/state. |
| `Buddy` | [`Enum/String`](./Enums.md#enum-buddy) | `Nubs, Ornstein, Smough` | Character Form / AI State: Behavior and stats for the 'Buddy' familiar state. |
| `AddMovement` | Number | `-2, 2, 1` | Applies or references the 'AddMovement' effect/state. |
| `Thorns` | Number | `2, 5, 3` | Applies or references the 'Thorns' effect/state. |
| `TransformOnDeath` | [`Enum/String`](./Enums.md#enum-transformondeath) | `RatKing, SimonFlopper, Carcus` | Applies or references the 'TransformOnDeath' effect/state. |
| `NoHealthOnlyShield` | Number | `1` | Applies or references the 'NoHealthOnlyShield' effect/state. |
| `WaterWalk` | Number | `1` | Applies or references the 'WaterWalk' effect/state. |
| `CoinPickup` | Number | `2, 1, 3` | Applies or references the 'CoinPickup' effect/state. |
| `LimitDamage` | Number | `1` | Applies or references the 'LimitDamage' effect/state. |
| `MoveWhenDamaged` | [`Block`](./Characters_and_Bosses.md#context-movewhendamaged) | `{ ... }, move, TKNG_Hop` | AI Movement: Forces a reposition when taking damage. |
| `StripStatuses` | Number | `1` | Applies or references the 'StripStatuses' effect/state. |
| `LimitHeal` | Number | `1, 0` | Applies or references the 'LimitHeal' effect/state. |
| `ReflectProjectiles` | [`Block`](./Characters_and_Bosses.md#context-reflectprojectiles) | `{ ... }, 100%, 1` | Passive: Reflects incoming projectiles back at the attacker. |
| `BackstabImmunity` | Number | `1` | Applies or references the 'BackstabImmunity' effect/state. |
| `FadeInsteadOfDie` | Number | `1` | Applies or references the 'FadeInsteadOfDie' effect/state. |
| `Plant` | Number | `1` | Applies or references the 'Plant' effect/state. |
| `RandomizeAIWeightsEachTurn` | [`Array`](./Arrays.md#array-randomizeaiweightseachturn) | `[ { decision_weights default move_weights keep_distance }..., [ { decision_weights blind move_weights chubs_and_nubs_bl..., [ { decision_weights default move_weights stay_close } { ...` | Applies or references the 'RandomizeAIWeightsEachTurn' effect/state. |
| `SmallRockBehavior` | [`Block`](./Characters_and_Bosses.md#context-smallrockbehavior) | `{ ... }, 0, 5` | AI Logic: Movement/interaction profile for small rocks. |
| `AbilityWhenBuddyDies` | [`Enum/String`](./Enums.md#enum-abilitywhenbuddydies) | `GirlDinoCry, ChubsRage, Guillotina2Rage` | Applies or references the 'AbilityWhenBuddyDies' effect/state. |
| `TransformInXTurns` | [`Block`](./Characters_and_Bosses.md#context-transforminxturns) | `{ ... }` | Logic: Forces a form change after X turns. |
| `AddDamage` | Number | `2, 1, 4` | Applies or references the 'AddDamage' effect/state. |
| `Divide4OnDeath` | [`Enum/String`](./Enums.md#enum-divide4ondeath) | `BiggestFood, MedSlime, Clot` | Applies or references the 'Divide4OnDeath' effect/state. |
| `HealthGain` | Number | `8, 1, 5` | Applies or references the 'HealthGain' effect/state. |
| `InnateElement` | [`Enum/String`](./Enums.md#enum-innateelement) | `Water, Fire` | Applies or references the 'InnateElement' effect/state. |
| `KaijuKnockbackImmune` | Number | `1` | Applies or references the 'KaijuKnockbackImmune' effect/state. |
| `MoveTowardsDamageSource` | [`Block`](./Characters_and_Bosses.md#context-movetowardsdamagesource) | `{ ... }, MoveOne` | AI Movement: Closes distance on the last source of damage. |
| `OverrideMaxHealth` | Number | `1, 25` | Applies or references the 'OverrideMaxHealth' effect/state. |
| `TagGreed` | [`Enum/String`](./Enums.md#enum-taggreed) | `pickup, bishop_hat, food` | Applies or references the 'TagGreed' effect/state. |
| `YOffset` | [`Enum/String`](./Enums.md#enum-yoffset) | `.35, -.18` | Applies or references the 'YOffset' effect/state. |
| `Angel` | Number | `1` | Applies or references the 'Angel' effect/state. |
| `DebuffImmunity` | Number | `1` | Applies or references the 'DebuffImmunity' effect/state. |
| `KineticSpikes` | Number | `1, 5` | Applies or references the 'KineticSpikes' effect/state. |
| `MinimumKnockbackFromAllDamage` | Number | `1` | Applies or references the 'MinimumKnockbackFromAllDamage' effect/state. |
| `MoveTowardsKillers` | [`Block`](./Characters_and_Bosses.md#context-movetowardskillers) | `{ ... }, ReaperRevenge` | AI Movement: Seeks out entities that have recently killed an ally. |
| `StartOffMap` | Number | `1` | Applies or references the 'StartOffMap' effect/state. |
| `TransformOnDeathImmediately` | [`Block`](./Characters_and_Bosses.md#context-transformondeathimmediately) | `{ ... }, NoHead` | Logic: Bypasses death sequence to instantly assume a new form. |
| `AbilityAfterEnemyCastSpell_Stackable` | [`Enum/String`](./Enums.md#enum-abilityafterenemycastspell_stackable) | `ThornUpX, ThornUp` | Applies or references the 'AbilityAfterEnemyCastSpell_Stackable' effect/state. |
| `AddMaxHealth` | Number | `5` | Applies or references the 'AddMaxHealth' effect/state. |
| `AddMeleeKnockback` | Number | `2, 1, 10` | Applies or references the 'AddMeleeKnockback' effect/state. |
| `Ammo` | Number | `6, 1, 3` | Applies or references the 'Ammo' effect/state. |
| `BackstabAllDirections` | Number | `1` | Applies or references the 'BackstabAllDirections' effect/state. |
| `Bird` | [`Enum/String`](./Enums.md#enum-bird) | `CookedChickenLeg` | Applies or references the 'Bird' effect/state. |
| `ChangeTileOnPop` | [`Enum/String`](./Enums.md#enum-changetileonpop) | `GlitchTile, OilTile, CreepTile` | Applies or references the 'ChangeTileOnPop' effect/state. |
| `CountAsCorpse` | Number | `1` | Applies or references the 'CountAsCorpse' effect/state. |
| `DisplayDangerAOE` | [`Enum/String`](./Enums.md#enum-displaydangeraoe) | `TheChild_Wrath, MoonHead_Blow, attack` | Applies or references the 'DisplayDangerAOE' effect/state. |
| `GroundFlopper` | [`Enum/String`](./Enums.md#enum-groundflopper) | `MoveOne, DefaultMove` | Applies or references the 'GroundFlopper' effect/state. |
| `IgnoreTiles` | Number | `1` | Applies or references the 'IgnoreTiles' effect/state. |
| `LoopingSoundWhileAlive` | [`Enum/String`](./Enums.md#enum-loopingsoundwhilealive) | `Twister_loop, BigUFO_ambient_looping, Bomb_FuseLoop` | Applies or references the 'LoopingSoundWhileAlive' effect/state. |
| `PrioritizeFarAwayTargets` | Number | `10, 1` | Applies or references the 'PrioritizeFarAwayTargets' effect/state. |
| `SharkySmellsBlood` | Number | `1` | Applies or references the 'SharkySmellsBlood' effect/state. |
| `StunImmunity` | [`Block`](./Characters_and_Bosses.md#context-stunimmunity) | `{ ... }, 1` | Passive: Prevents Stun from being applied. |
| `WeremanTransformationReceiver` | [`Enum/String`](./Enums.md#enum-weremantransformationreceiver) | `CaveWomanDropTransform, CaveManTransform` | Applies or references the 'WeremanTransformationReceiver' effect/state. |
| `AddHiddenTag` | [`Enum/String`](./Enums.md#enum-addhiddentag) | `unlit_candle, grown_hitler_clone, hitler_clone_fetus` | Applies or references the 'AddHiddenTag' effect/state. |
| `AddInitiative` | Number | `-10, -9999, 999999` | Applies or references the 'AddInitiative' effect/state. |
| `AddTag` | [`Enum/String`](./Enums.md#enum-addtag) | `tumor, fetus, cat` | Applies or references the 'AddTag' effect/state. |
| `AggroTargetIsCurrentTurn` | Number | `1` | Applies or references the 'AggroTargetIsCurrentTurn' effect/state. |
| `BaseStatMultiply` | [`Enum/String`](./Enums.md#enum-basestatmultiply) | `.666, .5, .25` | Applies or references the 'BaseStatMultiply' effect/state. |
| `BonusTurnPattern` | [`Array`](./Arrays.md#array-bonusturnpattern) | `[ { dispersed_bonus_turns 2 round_end_bonus_turns 1 } { r..., [ { evenly_dispersed_bonus_turns 0 round_end_bonus_turns ..., [ { evenly_dispersed_bonus_turns 1 round_end_bonus_turns ...` | Applies or references the 'BonusTurnPattern' effect/state. |
| `CanMutateTo` | [`Array`](./Arrays.md#array-canmutateto) | `[ TumorousMaggot, ChargeyMaggot, SwappyMaggot ], Hyde, [ Lumpy, Leaper ]` | Applies or references the 'CanMutateTo' effect/state. |
| `DigestDeadBodies` | [`Enum/String`](./Enums.md#enum-digestdeadbodies) | `MoonHead_Digest, Digest, LennyCatDies` | Applies or references the 'DigestDeadBodies' effect/state. |
| `FaceShield` | Number | `0` | Applies or references the 'FaceShield' effect/state. |
| `InjuryImmunity` | Number | `1` | Applies or references the 'InjuryImmunity' effect/state. |
| `MimicSpawnerAttacks` | Number | `1, -1` | Applies or references the 'MimicSpawnerAttacks' effect/state. |
| `MinimumKnockbackFromPhysicalAttacks` | Number | `1` | Applies or references the 'MinimumKnockbackFromPhysicalAttacks' effect/state. |
| `MutateViaAbility` | [`Enum/String`](./Enums.md#enum-mutateviaability) | `BBTransformMutant` | Applies or references the 'MutateViaAbility' effect/state. |
| `PrioritizeHitDifferentTargets` | Number | `1` | Applies or references the 'PrioritizeHitDifferentTargets' effect/state. |
| `RunInXTurns` | Number | `2, 1, 3` | Applies or references the 'RunInXTurns' effect/state. |
| `SharePickupsWithSpawner` | Number | `0, 1` | Applies or references the 'SharePickupsWithSpawner' effect/state. |
| `SpawnThingOnDeath` | [`Enum/String`](./Enums.md#enum-spawnthingondeath) | `Boulder, Food, Gamete` | Applies or references the 'SpawnThingOnDeath' effect/state. |
| `SpeedUp` | Number | `6, 2` | Applies or references the 'SpeedUp' effect/state. |
| `SupportFormChangeInsteadOfRun` | [`Block`](./Characters_and_Bosses.md#context-supportformchangeinsteadofrun) | `{ ... }, Attacker` | AI Logic: Forces a support unit to transform rather than flee. |
| `TileTrail_Ahead` | [`Enum/String`](./Enums.md#enum-tiletrail_ahead) | `WaterTile, FireTile, OilTile` | Applies or references the 'TileTrail_Ahead' effect/state. |
| `WeaponsDontLoseDurability` | Number | `1` | Applies or references the 'WeaponsDontLoseDurability' effect/state. |
| `AddCorpseHealth` | Number | `-999` | Applies or references the 'AddCorpseHealth' effect/state. |
| `AggroTargetIsBuddy` | Number | `1` | Applies or references the 'AggroTargetIsBuddy' effect/state. |
| `AllDamageImmune_IncludingSpeculative` | Number | `1` | Applies or references the 'AllDamageImmune_IncludingSpeculative' effect/state. |
| `AlphaTurns` | Number | `1` | Applies or references the 'AlphaTurns' effect/state. |
| `AlwaysHitDifferentTargets` | Number | `1` | Applies or references the 'AlwaysHitDifferentTargets' effect/state. |
| `BuffImmunity` | Number | `1` | Applies or references the 'BuffImmunity' effect/state. |
| `CanShield` | Number | `1` | Applies or references the 'CanShield' effect/state. |
| `ChanceToDisableActionsIfNotCharmed` | Number | `75%` | Applies or references the 'ChanceToDisableActionsIfNotCharmed' effect/state. |
| `ChangeTileOnDeath` | [`Enum/String`](./Enums.md#enum-changetileondeath) | `WaterTile` | Applies or references the 'ChangeTileOnDeath' effect/state. |
| `DemonicGlyphFrames` | Number | `1` | Applies or references the 'DemonicGlyphFrames' effect/state. |
| `DiesToElement` | [`Block`](./Characters_and_Bosses.md#context-diestoelement) | `{ ... }, Wind` | Vulnerability: Character dies instantly if hit by this element. |
| `DissuadeInstakills` | Number | `1` | Applies or references the 'DissuadeInstakills' effect/state. |
| `DodgeChance_Status` | Number | `66, 100` | Applies or references the 'DodgeChance_Status' effect/state. |
| `ExpireOnSpawnerTurnEnd` | Number | `1` | Applies or references the 'ExpireOnSpawnerTurnEnd' effect/state. |
| `ExtraDispersedTurns` | Number | `1` | Applies or references the 'ExtraDispersedTurns' effect/state. |
| `FaceLastDamage` | [`Block`](./Characters_and_Bosses.md#context-facelastdamage) | `{ ... }, 1` | Reaction: Forces the character to face towards the last damage source. |
| `FinalBossShield` | [`Enum/String`](./Enums.md#enum-finalbossshield) | `DestroyerShieldBash, None` | Applies or references the 'FinalBossShield' effect/state. |
| `Flying` | Number | `1` | Applies or references the 'Flying' effect/state. |
| `GoopWalk` | Number | `1` | Applies or references the 'GoopWalk' effect/state. |
| `HealthRegenUp` | Number | `2, 4` | Applies or references the 'HealthRegenUp' effect/state. |
| `ImmobilePassive` | Number | `1` | Applies or references the 'ImmobilePassive' effect/state. |
| `KaijuWinCon` | [`Enum/String`](./Enums.md#enum-kaijuwincon) | `zaratana, pyrophina` | Applies or references the 'KaijuWinCon' effect/state. |
| `MagicDamageImmune` | Number | `1` | Applies or references the 'MagicDamageImmune' effect/state. |
| `MamaCatAnimations` | Number | `1` | Applies or references the 'MamaCatAnimations' effect/state. |
| `MiniVolcanoReaction` | [`Enum/String`](./Enums.md#enum-minivolcanoreaction) | `MiniVolcano_Spurt, ThrobShot_Reaction` | Applies or references the 'MiniVolcanoReaction' effect/state. |
| `PermanentMadness` | Number | `1` | Applies or references the 'PermanentMadness' effect/state. |
| `PrioritizeAggroTarget` | Number | `1` | Applies or references the 'PrioritizeAggroTarget' effect/state. |
| `PrioritizePlayerCats` | Number | `1` | Applies or references the 'PrioritizePlayerCats' effect/state. |
| `PrioritizeWeakestEnemy` | Number | `1` | Applies or references the 'PrioritizeWeakestEnemy' effect/state. |
| `SafeDoomed` | Number | `1` | Applies or references the 'SafeDoomed' effect/state. |
| `SpawnCreepOnHit` | Number | `1` | Applies or references the 'SpawnCreepOnHit' effect/state. |
| `SurviveAt1HP` | Number | `1` | Applies or references the 'SurviveAt1HP' effect/state. |
| `TileTrail` | [`Enum/String`](./Enums.md#enum-tiletrail) | `ShadowTile, CreepTile` | Applies or references the 'TileTrail' effect/state. |
| `TransformWhenBuddyDies` | [`Enum/String`](./Enums.md#enum-transformwhenbuddydies) | `UltraOrnstein, UltraSmough` | Applies or references the 'TransformWhenBuddyDies' effect/state. |
| `UnlockOrientation` | Number | `1` | Applies or references the 'UnlockOrientation' effect/state. |
| `UseAbility` | [`Enum/String`](./Enums.md#enum-useability) | `TormentorRuneAbsorb, MegaGuppy_SummonTheChild` | Logic: Forces execution of an ability. |
| `AbilityOnBattleStart_UseAI` | [`Enum/String`](./Enums.md#enum-abilityonbattlestart_useai) | `TheCreator_SpawnCloneTeam` | Applies or references the 'AbilityOnBattleStart_UseAI' effect/state. |
| `AddElementsToBasicAttack` | [`Enum/String`](./Enums.md#enum-addelementstobasicattack) | `Fire` | Applies or references the 'AddElementsToBasicAttack' effect/state. |
| `AdvancedTint` | [`Array`](./Arrays.md#array-advancedtint) | `[ .6, .6, .6, 1 .5, .5, .5, 0 ]` | Applies or references the 'AdvancedTint' effect/state. |
| `AggroTargetIsLastEnemyThatDealtDamage` | Number | `1` | Applies or references the 'AggroTargetIsLastEnemyThatDealtDamage' effect/state. |
| `AggroTargetIsLowestHealthEnemyTillItDies` | Number | `1` | Applies or references the 'AggroTargetIsLowestHealthEnemyTillItDies' effect/state. |
| `AggroTargetIsLowestMaxHealthCat` | Number | `1` | Applies or references the 'AggroTargetIsLowestMaxHealthCat' effect/state. |
| `AlienBeastDangerZones` | [`Array`](./Arrays.md#array-alienbeastdangerzones) | `[ AlienBeastScream AlienBeastEat AlienBeastPuke AlienBeas...` | Applies or references the 'AlienBeastDangerZones' effect/state. |
| `AlienBeastEyeStalks` | Number | `3` | Applies or references the 'AlienBeastEyeStalks' effect/state. |
| `AllSpellsCostActPoints` | Number | `1` | Applies or references the 'AllSpellsCostActPoints' effect/state. |
| `AllStatsUp` | Number | `2` | Applies or references the 'AllStatsUp' effect/state. |
| `AvoidDamagingCharmedEnemies` | Number | `1` | Applies or references the 'AvoidDamagingCharmedEnemies' effect/state. |
| `AwardCoinsOnDeath` | Number | `10` | Applies or references the 'AwardCoinsOnDeath' effect/state. |
| `BasicAIDangerZone` | Number | `2` | Applies or references the 'BasicAIDangerZone' effect/state. |
| `BlackHolePassive` | Number | `1` | Applies or references the 'BlackHolePassive' effect/state. |
| `BloatEyePassive2` | [`Enum/String`](./Enums.md#enum-bloateyepassive2) | `BloatEyeMovement2` | Applies or references the 'BloatEyePassive2' effect/state. |
| `BlockAllDamage` | Number | `1` | Applies or references the 'BlockAllDamage' effect/state. |
| `BombBehavior` | Number | `1` | Applies or references the 'BombBehavior' effect/state. |
| `Burn` | Number | `3` | Applies or references the 'Burn' effect/state. |
| `CCImmunity` | Number | `1` | Applies or references the 'CCImmunity' effect/state. |
| `CapReceivedDamage` | Number | `1` | Applies or references the 'CapReceivedDamage' effect/state. |
| `ConjureBonusAbility` | [`Enum/String`](./Enums.md#enum-conjurebonusability) | `random` | Adds a temporary bonus ability to the character's hand/deck. |
| `CounterAttackAfterEnemyCastSpell` | [`Enum/String`](./Enums.md#enum-counterattackafterenemycastspell) | `Telekinesis` | Applies or references the 'CounterAttackAfterEnemyCastSpell' effect/state. |
| `CrowAttackLink` | Number | `1` | Applies or references the 'CrowAttackLink' effect/state. |
| `DamageFromBehindOnly` | Number | `1` | Applies or references the 'DamageFromBehindOnly' effect/state. |
| `DemonicGlyphStealer` | Number | `1` | Applies or references the 'DemonicGlyphStealer' effect/state. |
| `DicerArt` | [`Array`](./Arrays.md#array-dicerart) | `[ 59 52 65 50 54 63 64 ]` | Applies or references the 'DicerArt' effect/state. |
| `DieWhenOnlyGolemsLeft` | Number | `1` | Applies or references the 'DieWhenOnlyGolemsLeft' effect/state. |
| `DieWhenSpawnerDies` | Number | `1` | Applies or references the 'DieWhenSpawnerDies' effect/state. |
| `DisableSpells` | Number | `1` | Applies or references the 'DisableSpells' effect/state. |
| `Disguised` | Number | `1` | Applies or references the 'Disguised' effect/state. |
| `DisguisedTrapper` | [`Enum/String`](./Enums.md#enum-disguisedtrapper) | `FearMelee` | Applies or references the 'DisguisedTrapper' effect/state. |
| `DisplayBuddyCatOnSpawn` | Number | `3` | Applies or references the 'DisplayBuddyCatOnSpawn' effect/state. |
| `DivineShield` | Number | `2` | Applies or references the 'DivineShield' effect/state. |
| `DivineShieldPickup` | Number | `1` | Applies or references the 'DivineShieldPickup' effect/state. |
| `DodgeChance` | Number | `50%` | Applies or references the 'DodgeChance' effect/state. |
| `DodgeChanceWithBlindSpot` | Number | `25%` | Applies or references the 'DodgeChanceWithBlindSpot' effect/state. |
| `DustCloudBehavior` | Number | `1` | Applies or references the 'DustCloudBehavior' effect/state. |
| `Dybbuk1HPTracker` | Number | `1` | Applies or references the 'Dybbuk1HPTracker' effect/state. |
| `ElectricArcs` | Number | `1` | Applies or references the 'ElectricArcs' effect/state. |
| `ElementWeakness` | [`Enum/String`](./Enums.md#enum-elementweakness) | `Fire` | Applies or references the 'ElementWeakness' effect/state. |
| `EnrageOnDamage` | Number | `1` | Applies or references the 'EnrageOnDamage' effect/state. |
| `EraseSpawnCoins` | Number | `1` | Applies or references the 'EraseSpawnCoins' effect/state. |
| `EventBounterHunterPassive` | Number | `1` | Applies or references the 'EventBounterHunterPassive' effect/state. |
| `ExtraMovePoints` | Number | `1` | Applies or references the 'ExtraMovePoints' effect/state. |
| `ExtraTurnsPerTaggedUnit` | [`Enum/String`](./Enums.md#enum-extraturnspertaggedunit) | `sprout` | Applies or references the 'ExtraTurnsPerTaggedUnit' effect/state. |
| `FlingObjectsOnTop` | Number | `8` | Applies or references the 'FlingObjectsOnTop' effect/state. |
| `FlushmasterCelebration` | [`Enum/String`](./Enums.md#enum-flushmastercelebration) | `celebrate` | Applies or references the 'FlushmasterCelebration' effect/state. |
| `ForceDodgeEverything` | Number | `1` | Applies or references the 'ForceDodgeEverything' effect/state. |
| `FormChangeWhenBuddyDies` | [`Enum/String`](./Enums.md#enum-formchangewhenbuddydies) | `Rage` | Applies or references the 'FormChangeWhenBuddyDies' effect/state. |
| `FreePathfindElement` | [`Enum/String`](./Enums.md#enum-freepathfindelement) | `Water` | Applies or references the 'FreePathfindElement' effect/state. |
| `FullBlockEverything` | Number | `1` | Applies or references the 'FullBlockEverything' effect/state. |
| `FullBlockEverythingTo0Damage` | Number | `1` | Applies or references the 'FullBlockEverythingTo0Damage' effect/state. |
| `GasCanBehavior` | Number | `1` | Applies or references the 'GasCanBehavior' effect/state. |
| `GasCloudBehavior2` | Number | `2` | Applies or references the 'GasCloudBehavior2' effect/state. |
| `GeminiTwin` | Number | `1` | Applies or references the 'GeminiTwin' effect/state. |
| `GlobalManaDrainAura` | Number | `-1` | Applies or references the 'GlobalManaDrainAura' effect/state. |
| `GoopImmunity` | Number | `1` | Applies or references the 'GoopImmunity' effect/state. |
| `GuillotinaDeathHead` | Number | `1` | Applies or references the 'GuillotinaDeathHead' effect/state. |
| `HarpoonTrapPassive` | [`Enum/String`](./Enums.md#enum-harpoontrappassive) | `HarpoonTrapPull` | Applies or references the 'HarpoonTrapPassive' effect/state. |
| `HiddenDoomed` | Number | `2` | Applies or references the 'HiddenDoomed' effect/state. |
| `IceBlockBehavior` | Number | `1` | Applies or references the 'IceBlockBehavior' effect/state. |
| `IllusionTint` | Number | `1` | Applies or references the 'IllusionTint' effect/state. |
| `InheritSpawnerStats` | Number | `1` | Applies or references the 'InheritSpawnerStats' effect/state. |
| `InsertIntoBackgroundPlaceholder` | Number | `1` | Applies or references the 'InsertIntoBackgroundPlaceholder' effect/state. |
| `JohnnyWasher` | [`Enum/String`](./Enums.md#enum-johnnywasher) | `BBTransformZealot` | Applies or references the 'JohnnyWasher' effect/state. |
| `KnockbackImmunity` | Number | `1` | Applies or references the 'KnockbackImmunity' effect/state. |
| `LegacySpawnSavedCatIfExists` | [`Enum/String`](./Enums.md#enum-legacyspawnsavedcatifexists) | `Legacy_Marshmallow_StolenCatID` | Applies or references the 'LegacySpawnSavedCatIfExists' effect/state. |
| `LockOrientationFaceTile` | [`Array`](./Arrays.md#array-lockorientationfacetile) | `[ 0 0 ]` | Applies or references the 'LockOrientationFaceTile' effect/state. |
| `ManglerMonsterPassive` | [`Enum/String`](./Enums.md#enum-manglermonsterpassive) | `ManglerMonsterDashAttack` | Applies or references the 'ManglerMonsterPassive' effect/state. |
| `MissChance` | Number | `20` | Applies or references the 'MissChance' effect/state. |
| `MoonHeadCrackedVisual` | [`Enum/String`](./Enums.md#enum-moonheadcrackedvisual) | `Cracked` | Applies or references the 'MoonHeadCrackedVisual' effect/state. |
| `MulticatHeads` | Number | `0` | Applies or references the 'MulticatHeads' effect/state. |
| `MutateAfterXTurns` | Number | `3` | Applies or references the 'MutateAfterXTurns' effect/state. |
| `MuteDemonicGlyphDisplay` | Number | `1` | Applies or references the 'MuteDemonicGlyphDisplay' effect/state. |
| `OrthogonalAIDangerZone` | Number | `10` | Applies or references the 'OrthogonalAIDangerZone' effect/state. |
| `PackHunting` | Number | `1` | Applies or references the 'PackHunting' effect/state. |
| `Phasing` | Number | `1` | Applies or references the 'Phasing' effect/state. |
| `PoisonThorns` | Number | `3` | Applies or references the 'PoisonThorns' effect/state. |
| `ReturnBoundItemOnBattleEnd` | Number | `1` | Applies or references the 'ReturnBoundItemOnBattleEnd' effect/state. |
| `RunWhenKittensDead` | Number | `1` | Applies or references the 'RunWhenKittensDead' effect/state. |
| `SetSpellCosts` | Number | `0` | Applies or references the 'SetSpellCosts' effect/state. |
| `SpawnCreepOnHitKnockback` | Number | `1` | Applies or references the 'SpawnCreepOnHitKnockback' effect/state. |
| `SpawnerCatDataReference` | Number | `1` | Applies or references the 'SpawnerCatDataReference' effect/state. |
| `SpreadWater` | Number | `1` | Applies or references the 'SpreadWater' effect/state. |
| `SproutsGrantMovement` | Number | `1` | Applies or references the 'SproutsGrantMovement' effect/state. |
| `StartDead` | Number | `100%` | Applies or references the 'StartDead' effect/state. |
| `StrengthUp` | Number | `2` | Applies or references the 'StrengthUp' effect/state. |
| `TVBotDisableAttack` | Number | `1` | Applies or references the 'TVBotDisableAttack' effect/state. |
| `TVBotDisableMove` | Number | `1` | Applies or references the 'TVBotDisableMove' effect/state. |
| `TVBotDisableSpells` | Number | `1` | Applies or references the 'TVBotDisableSpells' effect/state. |
| `TakeWeaponFromSpawner` | Number | `1` | Applies or references the 'TakeWeaponFromSpawner' effect/state. |
| `Tall` | Number | `1` | Applies or references the 'Tall' effect/state. |
| `TallTumorManaBurn` | [`Enum/String`](./Enums.md#enum-talltumormanaburn) | `TT_ManaBurn` | Applies or references the 'TallTumorManaBurn' effect/state. |
| `Terminator2Chase` | [`Enum/String`](./Enums.md#enum-terminator2chase) | `move` | Applies or references the 'Terminator2Chase' effect/state. |
| `TileElementDamageImmunity` | [`Enum/String`](./Enums.md#enum-tileelementdamageimmunity) | `Ice` | Applies or references the 'TileElementDamageImmunity' effect/state. |
| `TireBehavior` | Number | `1` | Applies or references the 'TireBehavior' effect/state. |
| `TormentorHeal` | Number | `1` | Applies or references the 'TormentorHeal' effect/state. |
| `TowerDefenseReflex` | [`Enum/String`](./Enums.md#enum-towerdefensereflex) | `attack` | Applies or references the 'TowerDefenseReflex' effect/state. |
| `TrackAmountKilledByPlayer` | [`Enum/String`](./Enums.md#enum-trackamountkilledbyplayer) | `BonusBirdsKilled` | Applies or references the 'TrackAmountKilledByPlayer' effect/state. |
| `TutorialBossRiggedFight` | Number | `16` | Applies or references the 'TutorialBossRiggedFight' effect/state. |
| `UncappedHP` | Number | `1` | Applies or references the 'UncappedHP' effect/state. |
| `UpTireBehavior` | Number | `5` | Applies or references the 'UpTireBehavior' effect/state. |
| `UseAbilityWhenShieldDepleted` | [`Enum/String`](./Enums.md#enum-useabilitywhenshielddepleted) | `T3Pebbles_PrimeBoulderDrop` | Applies or references the 'UseAbilityWhenShieldDepleted' effect/state. |
| `Wall` | Number | `1` | Applies or references the 'Wall' effect/state. |
| `WhitelistPickupType` | [`Enum/String`](./Enums.md#enum-whitelistpickuptype) | `food` | Applies or references the 'WhitelistPickupType' effect/state. |
| `WideBackstab` | Number | `1` | Applies or references the 'WideBackstab' effect/state. |
| `WispDodge` | Number | `1` | Applies or references the 'WispDodge' effect/state. |
| `ZeroKnockbackDamage` | Number | `1` | Applies or references the 'ZeroKnockbackDamage' effect/state. |

</details>

---

### Context: `pattern`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `do` | [`Enum/String`](./Enums.md#enum-do) | `**SimonFlopper_WiggleChance, **SimonFlopper_WiggleGuaranteed, **SimonFlopper_WiggleFake` |  |
| `do_priority` | [`Array`](./Arrays.md#array-do_priority) | `[ *RockToss_BomberRat, RockToss_BomberRat ], [ BumblefootEatCorpse, BumblefootEatCat, BumblefootBoneSh..., [ *QueenWeb, attack, QueenMinis ]` |  |
| `do_all` | [`Array`](./Arrays.md#array-do_all) | `[ CovenFamine CovenRise3 ], [ CovenPestilence CovenRise2 ], [ CovenWar CovenRise4 ]` |  |
| `move_then_do` | [`Enum/String`](./Enums.md#enum-move_then_do) | `attack, NubsJump, SimonFlopper_SpawnMinion` |  |
| `do_random` | [`Array`](./Arrays.md#array-do_random) | `[ ScaryHaunt ScaryFear ], [ Escape attack DybbukReanimate ], [ Escape attack DybbukReanimate DybbukWisps ]` |  |
| `do_strict` | [`Array`](./Arrays.md#array-do_strict) | `[ MCFlamethrower ], [ MCStorm ], [ MCBlizzard ]` |  |
| `do_nothing` | [`Array`](./Arrays.md#array-do_nothing) | `[ ]` |  |
| `move_then_do_priority` | [`Array`](./Arrays.md#array-move_then_do_priority) | `[ BBPickupCrown, *attack, *BBToss ], [ BBPickupCrown, *BBToss, *attack ], [ DrinkUp attack ]` |  |
| `move_then_do_random` | [`Array`](./Arrays.md#array-move_then_do_random) | `[ CerberubsJumpBlind CerberubsJumpNormal ], [ ClotEvolve ClotFailEvolve ], [ ClotEvolveCatCopy ClotFailEvolve ]` |  |
| `do_all_shuffle` | [`Array`](./Arrays.md#array-do_all_shuffle) | `[ attack DybbukWisps DybbukRePossess ], [ YetiSlam YetiSlam YetiSlam YetiBite YetiBite YetiBite Y...` |  |
| `do_best` | [`Array`](./Arrays.md#array-do_best) | `[ JohnnyPush JohnnyPull ]` |  |
| `do_best_multiple` | [`Array`](./Arrays.md#array-do_best_multiple) | `[ attack spell0 spell1 spell2 spell3 spell4 weapon trinket ]` |  |
| `do_priority_alternating` | [`Array`](./Arrays.md#array-do_priority_alternating) | `[ *BadBone, *GoodBone, BadBone_copy, GoodBone_copy, BadBo...` |  |
| `move_then_do_all` | [`Array`](./Arrays.md#array-move_then_do_all) | `[ LennyShove, LennyGrabDead, LennyGrab ]` |  |

</details>

---

### Context: `FormChangeWhileHasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Counterspell, Consuming, Grappling` | ID of the status effect to apply or check. |
| `form_hasnot` | [`Enum/String`](./Enums.md#enum-form_hasnot) | `Big, Small, Default` |  |
| `form_has` | [`Enum/String`](./Enums.md#enum-form_has) | `HasCat, HasRock, Full` |  |

</details>

---

### Context: `FormChanger`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `initial_form` | [`Enum/String`](./Enums.md#enum-initial_form) | `Up, Flop, Default` |  |
| `Butcher` | Block | `{ ... }` | Applies or references the 'Butcher' effect/state. |
| `Colorless` | Block | `{ ... }` | Applies or references the 'Colorless' effect/state. |
| `Druid` | Block | `{ ... }` | Applies or references the 'Druid' effect/state. |
| `Fighter` | Block | `{ ... }` | Applies or references the 'Fighter' effect/state. |
| `Hunter` | Block | `{ ... }` | Applies or references the 'Hunter' effect/state. |
| `Mage` | Block | `{ ... }` | Applies or references the 'Mage' effect/state. |
| `Medic` | Block | `{ ... }` | Applies or references the 'Medic' effect/state. |
| `Monk` | Block | `{ ... }` | Applies or references the 'Monk' effect/state. |
| `Necromancer` | Block | `{ ... }` | Applies or references the 'Necromancer' effect/state. |
| `NoDeathRattle` | Block | `{ ... }` | Applies or references the 'NoDeathRattle' effect/state. |
| `Psychic` | Block | `{ ... }` | Applies or references the 'Psychic' effect/state. |
| `Tank` | Block | `{ ... }` | Applies or references the 'Tank' effect/state. |
| `Thief` | Block | `{ ... }` | Applies or references the 'Thief' effect/state. |
| `Tinkerer` | Block | `{ ... }` | Applies or references the 'Tinkerer' effect/state. |
| `Unmounted` | Block | `{ ... }` | Applies or references the 'Unmounted' effect/state. |
| `sync_brain_patterns` | Boolean | `true` |  |

</details>

---

### Context: `alt_spawn_pool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Antidote` | [`Enum/String`](./Enums.md#enum-antidote) | `.5, 1` | Applies or references the 'Antidote' effect/state. |
| `Blessing` | [`Enum/String`](./Enums.md#enum-blessing) | `.5, 1` | Applies or references the 'Blessing' effect/state. |
| `BigCatnip` | Number | `6, 10, 1` | Applies or references the 'BigCatnip' effect/state. |
| `BigScrap` | Number | `6, 4.5, 1` | Applies or references the 'BigScrap' effect/state. |
| `BiggestFood` | Number | `6, 1, 15` | Applies or references the 'BiggestFood' effect/state. |
| `Coin` | Number | `1, 70` | Applies or references the 'Coin' effect/state. |
| `BigFood` | Number | `20, 5` | Applies or references the 'BigFood' effect/state. |
| `Coin10` | Number | `1, .1` | Applies or references the 'Coin10' effect/state. |
| `Coin3` | Number | `1` | Applies or references the 'Coin3' effect/state. |
| `Coin4` | Number | `1` | Applies or references the 'Coin4' effect/state. |
| `MedCatnip` | Number | `20, 5` | Applies or references the 'MedCatnip' effect/state. |
| `MedScrap` | Number | `20, 5` | Applies or references the 'MedScrap' effect/state. |
| `RandomArmorPickup` | Number | `4.5, 40` | Applies or references the 'RandomArmorPickup' effect/state. |
| `RandomCatnipPickup` | Number | `10, 30` | Applies or references the 'RandomCatnipPickup' effect/state. |
| `RandomFoodPickup` | Number | `40, 15` | Applies or references the 'RandomFoodPickup' effect/state. |
| `Bear` | Number | `1` | Applies or references the 'Bear' effect/state. |
| `BlackBird` | Number | `3000` | Applies or references the 'BlackBird' effect/state. |
| `Catepillar` | Number | `10` | Applies or references the 'Catepillar' effect/state. |
| `Catnip` | Number | `20` | Applies or references the 'Catnip' effect/state. |
| `CharmedDip` | Number | `1` | Applies or references the 'CharmedDip' effect/state. |
| `CharmedFloater` | Number | `1` | Applies or references the 'CharmedFloater' effect/state. |
| `CharmedPile` | Number | `1` | Applies or references the 'CharmedPile' effect/state. |
| `Cherub` | Number | `1` | Applies or references the 'Cherub' effect/state. |
| `Chicken` | Number | `3000` | Applies or references the 'Chicken' effect/state. |
| `Coin2` | Number | `1` | Applies or references the 'Coin2' effect/state. |
| `Dove` | Number | `1000` | Applies or references the 'Dove' effect/state. |
| `Eagle` | Number | `300` | Applies or references the 'Eagle' effect/state. |
| `Food` | Number | `20` | Applies or references the 'Food' effect/state. |
| `Harpy` | Number | `1` | Applies or references the 'Harpy' effect/state. |
| `HummingBird` | Number | `300` | Applies or references the 'HummingBird' effect/state. |
| `LargeBirdPool` | Number | `1` | Applies or references the 'LargeBirdPool' effect/state. |
| `MedBirdPool` | Number | `1` | Applies or references the 'MedBirdPool' effect/state. |
| `Mutant` | Number | `1` | Character Form: Behavior and stats for the 'Mutant' state. |
| `Pigeon` | Number | `3000` | Applies or references the 'Pigeon' effect/state. |
| `RandomBiggerArmorPickup` | Number | `4.5` | Applies or references the 'RandomBiggerArmorPickup' effect/state. |
| `RandomBiggerCatnipPickup` | Number | `10` | Applies or references the 'RandomBiggerCatnipPickup' effect/state. |
| `RandomBiggerFoodPickup` | Number | `15` | Applies or references the 'RandomBiggerFoodPickup' effect/state. |
| `Raven` | Number | `300` | Applies or references the 'Raven' effect/state. |
| `Scrap` | Number | `20` | Applies or references the 'Scrap' effect/state. |
| `Seagull` | Number | `1000` | Applies or references the 'Seagull' effect/state. |
| `SmallBirdPool` | Number | `1` | Applies or references the 'SmallBirdPool' effect/state. |
| `Snake` | Number | `10` | Applies or references the 'Snake' effect/state. |
| `Squirrel` | Number | `10` | Applies or references the 'Squirrel' effect/state. |
| `Toad` | Number | `10` | Applies or references the 'Toad' effect/state. |
| `Turkey` | Number | `1000` | Applies or references the 'Turkey' effect/state. |
| `Turtle` | Number | `10` | Applies or references the 'Turtle' effect/state. |

</details>

---

### Context: `sound`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `alt_sounds` | [`Array`](./Arrays.md#array-alt_sounds) | `[ [ SE_BirdSmall_DyingCall SE_BirdDying_Hummingbird ], [ [ SE_BirdSmall_DyingCall SE_BirdDying_Blackbird ], [ [ SE_BirdSmall_DyingCall SE_BirdDying_Dove ]` |  |
| `SE_Cat_StompLegMove` | [`Enum/String`](./Enums.md#enum-se_cat_stomplegmove) | `SE_Terminator1_WalkLeg, SE_Terminator2_WalkLeg` | Applies or references the 'SE_Cat_StompLegMove' effect/state. |
| `SE_CatSwishThrow` | [`Enum/String`](./Enums.md#enum-se_catswishthrow) | `SE_ThrowGrenade` | Applies or references the 'SE_CatSwishThrow' effect/state. |
| `SE_Cat_ShadowStepIn` | [`Enum/String`](./Enums.md#enum-se_cat_shadowstepin) | `SE_Terminator_ShadowStepIn` | Applies or references the 'SE_Cat_ShadowStepIn' effect/state. |
| `SE_Cat_ShadowStepOut` | [`Enum/String`](./Enums.md#enum-se_cat_shadowstepout) | `SE_Terminator_ShadowStepOut` | Applies or references the 'SE_Cat_ShadowStepOut' effect/state. |
| `SE_Cat_WeaponLower` | [`Enum/String`](./Enums.md#enum-se_cat_weaponlower) | `SE_Terminator_WeaponLower` | Applies or references the 'SE_Cat_WeaponLower' effect/state. |
| `SE_Cat_WeaponRaise` | [`Enum/String`](./Enums.md#enum-se_cat_weaponraise) | `SE_Terminator_WeaponRaise` | Applies or references the 'SE_Cat_WeaponRaise' effect/state. |
| `SE_Cat_bearHug` | [`Enum/String`](./Enums.md#enum-se_cat_bearhug) | `SE_Terminator_bearHug` | Applies or references the 'SE_Cat_bearHug' effect/state. |
| `SE_Cat_equipWeapon` | [`Enum/String`](./Enums.md#enum-se_cat_equipweapon) | `SE_TerminatorSwapWeapon` | Applies or references the 'SE_Cat_equipWeapon' effect/state. |
| `SE_PetRock_Dash` | [`Enum/String`](./Enums.md#enum-se_petrock_dash) | `SE_PetBoulder_Dash` | Applies or references the 'SE_PetRock_Dash' effect/state. |
| `animation_prefix` | [`Enum/String`](./Enums.md#enum-animation_prefix) | `RattleSnake` |  |

</details>

---

### Context: `turns`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `takes_turns` | Boolean | `false, true` |  |
| `dispersed_bonus_turns` | Number | `1, 2, 0` |  |
| `takes_main_turn` | Boolean | `false, true` |  |
| `evenly_dispersed_bonus_turns` | Number | `2, 1` |  |
| `round_end_bonus_turns` | Number | `1` |  |
| `wait_till_next_round_to_update_turns` | Boolean | `true` |  |
| `round_start_bonus_turns` | Number | `1` |  |

</details>

---

### Context: `HealthPickup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `frame_range` | [`Array`](./Arrays.md#array-frame_range) | `[ 5 5 ], [ 3 4 ], [ 1 2 ]` |  |
| `stacks` | Number | `7, 10, 4` | Number of stacks or intensity to apply. |
| `stored_food_value` | Number | `2, 1, 3` |  |
| `anything_eats` | Boolean | `true` |  |
| `force_frame` | Number | `12` |  |

</details>

---

### Context: `CatPartsTransform`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `palette` | [`Enum/String`](./Enums.md#enum-palette) | `Mage, Fighter, Hunter` |  |
| `arm1` | Number | `1045, 1044, 1043` | Sprite variant ID for the front arm. |
| `arm2` | Number | `1045, 1044, 1043` |  |
| `body` | Number | `1024, 1013, 1012` | Sprite variant ID for the body. |
| `ear1` | Number | `1013, 1028, 1029` | Sprite variant ID for the front ear. |
| `head` | Number | `1019, 1027, 1020` | Sprite variant ID for the head. |
| `leg1` | Number | `1045, 1044, 1043` | Sprite variant ID for the front leg. |
| `leg2` | Number | `1045, 1044, 1043` |  |
| `tail` | Number | `1034, 1036, 1035` | Sprite variant ID for the tail. |
| `texture` | Number | `29, 60, 19` |  |
| `eye1` | Number | `1057, 1013` |  |
| `eye2` | Number | `1057, 1013` |  |
| `ear2` | Number | `1013` |  |

</details>

---

### Context: `equipment`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `face` | [`Enum/String`](./Enums.md#enum-face) | `AtomicMark, WesternHat, MetalPlate` |  |
| `head` | [`Enum/String`](./Enums.md#enum-head) | `Banana, LoansharksFedora, CoinBag` |  |
| `neck` | [`Enum/String`](./Enums.md#enum-neck) | `MageCollar, Poncho, Slime` |  |
| `weapon` | [`Enum/String`](./Enums.md#enum-weapon) | `ButcherHook, GunslingerPistol, AstroTaser` | Weapon item constraint. |

</details>

---

### Context: `mainturn_pattern`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `do` | [`Enum/String`](./Enums.md#enum-do) | `**BombRatTurtle, **TrampleDash, HealSelf` |  |
| `do_all` | [`Array`](./Arrays.md#array-do_all) | `[ *AlienBeastScream *AlienBeastEat *AlienBeastPuke *Alien..., [ *MarshmallowZealot, CloseConvert, attack ], [ attack DustTeleport ]` |  |
| `do_priority` | [`Array`](./Arrays.md#array-do_priority) | `[ ChumShot_Damage, ChumShot_Maggot ], [ attack Simon_Shot ], [ *HitlerHeil attack move ]` |  |
| `do_strict` | [`Array`](./Arrays.md#array-do_strict) | `[ BasicMelee, RageUp ], [ *WizSpellShield, WizBlizzard ]` |  |
| `move_then_do` | [`Enum/String`](./Enums.md#enum-move_then_do) | `RockSong, attack` |  |

</details>

---

### Context: `CharacterLightSource`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `color` | [`Array`](./Arrays.md#array-color) | `[ .7, .8, .9 ], [ .3, .7, 1 ], [ .8, .9, 1 ]` |  |
| `size` | Number | `2, 1.5, 4` |  |
| `glow` | [`Array`](./Arrays.md#array-glow) | `[ 1, 1, 1, .5 ], [ .7, .8, .9, .5 ], [ .3, .7, 1, .5 ]` |  |

</details>

---

### Context: `bonusturn_pattern`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `do` | [`Enum/String`](./Enums.md#enum-do) | `move, *SpawnBomb, DustDash` |  |
| `do_priority` | [`Array`](./Arrays.md#array-do_priority) | `[ TormentorBite TormentorSpawn attack ], [ TormentorSpawn TormentorBite attack ], [ G3GrabHead move *G3GrabHead ]` |  |
| `do_strict` | [`Array`](./Arrays.md#array-do_strict) | `[ WizStorm ], [ WizFlamethrower ], [ ]` |  |
| `do_all` | [`Array`](./Arrays.md#array-do_all) | `[ attack AlienBeastOpenEyes ], [ TrembloSuck *TrembloEat TrembloEat ], [ CloseConvert, attack ]` |  |
| `move_then_do` | [`Enum/String`](./Enums.md#enum-move_then_do) | `RatKingSpawn` |  |

</details>

---

### Context: `AbilityHealthThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `DybbukPossess, FormShrinkFour, FormShrinkThree` | The specific ability ID to cast. |
| `threshold` | [`Enum/String`](./Enums.md#enum-threshold) | `4*champion_multiplier, 3*champion_multiplier, 1` |  |
| `even_if_stunned` | Boolean | `true` |  |
| `immediate` | Boolean | `true` |  |
| `use_ai` | Boolean | `true` |  |
| `also_use_if_buddy_is_dead` | Boolean | `true` |  |
| `threshold_min` | [`Enum/String`](./Enums.md#enum-threshold_min) | `X` |  |

</details>

---

### Context: `BossRewards`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `common` | [`Enum/String`](./Enums.md#enum-common) | `RatBomb, ChubsCollar, Blubber` |  |
| `rare` | [`Enum/String`](./Enums.md#enum-rare) | `SpiderBaby, RadGlasses, BorisBrain` |  |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `TinySpider, Rat, Maggot` |  |
| `good` | Boolean | `false, true` |  |
| `spawn_on_death_hit` | Boolean | `false` |  |
| `chance` | Number | `50%, .25, 33%` | Probability (0.0 to 1.0) of executing this action. |
| `coins` | Number | `1` |  |
| `auto_cast` | [`Enum/String`](./Enums.md#enum-auto_cast) | `Dash_Enemy` |  |
| `consider_all_layers` | Boolean | `true` |  |
| `melee_ability_only` | Boolean | `true` |  |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0, 5` | The base damage properties of an attack. |
| `knockback` | Number | `4, 2, 3` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `status, none` | Classification/category type. |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Fire ]` |  |
| `cant_miss` | Boolean | `true` |  |

</details>

---

### Context: `FormChangeOnElementInfluence`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `water, very_hot, wind` | Specific element type required or applied. |
| `form` | [`Enum/String`](./Enums.md#enum-form) | `hot, default, Unlit` |  |
| `exclude` | [`Enum/String`](./Enums.md#enum-exclude) | `water, fire` |  |
| `particle` | [`Enum/String`](./Enums.md#enum-particle) | `FireExtinguish` |  |
| `sfx` | [`Enum/String`](./Enums.md#enum-sfx) | `FireExtinguish` |  |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `2, 1` | Applies or references the 'Bleed' effect/state. |
| `Burn` | Number | `2, 1, 4` | Applies or references the 'Burn' effect/state. |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `RemoteLeech` | Number | `1` | Applies or references the 'RemoteLeech' effect/state. |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |
| `DamageUp` | Number | `-1` | Applies or references the 'DamageUp' effect/state. |
| `Knockback` | Number | `3` | Applies or references the 'Knockback' effect/state. |
| `Leech` | Number | `2` | Applies or references the 'Leech' effect/state. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `Possessed` | Number | `1` | Applies or references the 'Possessed' effect/state. |
| `RandomStatUp` | Number | `-1` | Applies or references the 'RandomStatUp' effect/state. |
| `RemoteFlatLeech` | Number | `1` | Applies or references the 'RemoteFlatLeech' effect/state. |
| `Rot` | Number | `1` | Applies or references the 'Rot' effect/state. |
| `Slow` | Number | `1` | Applies or references the 'Slow' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `Weakness` | Number | `1` | Applies or references the 'Weakness' effect/state. |

</details>

---

### Context: `ImmediateAbilityReaction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `ButtWeb, AlienBeastGoop, ButtWeb_AlreadyEnraged` | The specific ability ID to cast. |
| `ability_damage_only` | Boolean | `true` |  |
| `backstabs_only` | Boolean | `true` |  |
| `damage_threshold` | Number | `10` |  |
| `even_if_blocked` | Boolean | `true` |  |
| `even_if_stunned` | Boolean | `true` |  |
| `health_threshold` | Number | `50, 70` |  |
| `buddy_damage_only` | Boolean | `true` |  |
| `target_furthest_valid` | Boolean | `true` |  |

</details>

---

### Context: `AbilityReaction`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MoonHandDash, attack, ButtFlip` | The specific ability ID to cast. |
| `ability_damage_only` | Boolean | `true` |  |
| `backstabs_only` | Boolean | `true` |  |
| `only_when_not_your_turn` | Boolean | `true` |  |
| `cancel_knockback` | Boolean | `true` |  |
| `enemies_only` | Boolean | `true` |  |
| `even_on_0_damage` | Boolean | `true` |  |
| `even_on_0_damage_if_knockback` | Boolean | `true` |  |
| `match_knockback_direction` | Boolean | `true` |  |
| `ranged_only` | Boolean | `true` |  |
| `verify_target` | Boolean | `true` |  |

</details>

---

### Context: `PassiveGroup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FormChange` | [`Enum/String`](./Enums.md#enum-formchange) | `Mage, Fighter, Hunter` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `ReplaceBasicAttack` | [`Enum/String`](./Enums.md#enum-replacebasicattack) | `BasicMelee, BasicRanged, BasicMagicShortRanged` | Applies or references the 'ReplaceBasicAttack' effect/state. |
| `SelfStatusCarefulness` | Number | `1` | Applies or references the 'SelfStatusCarefulness' effect/state. |
| `StatusCarefulness` | Number | `1` | Applies or references the 'StatusCarefulness' effect/state. |
| `ExtraBasicAttacks` | Number | `1` | Applies or references the 'ExtraBasicAttacks' effect/state. |

</details>

---

### Context: `Consumed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `do_not_pop_corpse` | Boolean | `true` |  |
| `drop_on_death` | [`Enum/String`](./Enums.md#enum-drop_on_death) | `deferred` |  |
| `force_contact` | Boolean | `true` | If true, enforces physical overlap. |
| `instant` | Boolean | `true` |  |
| `mount_mode` | [`Enum/String`](./Enums.md#enum-mount_mode) | `auto` | If true, treats the consumption as riding/mounting instead of eating. |
| `struggle_ability` | [`Enum/String`](./Enums.md#enum-struggle_ability) | `Thrash` | Ability triggered by the consumed entity while inside the consumer. |
| `use_placeholder` | Boolean | `true` |  |

</details>

---

### Context: `DeathRattle`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MoonHandDrop_Deathrattle, UFO_SpelunkyDeath, JarHeadDeath` | The specific ability ID to cast. |
| `is_dying_animation` | Boolean | `true` |  |
| `pop_corpse` | Boolean | `false` |  |
| `cancel_knockback` | Boolean | `true` |  |
| `immediate` | Boolean | `true` |  |
| `must_target_killer` | Boolean | `true` |  |
| `target_killer` | Boolean | `true` |  |

</details>

---

### Context: `TransformInXTurns`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Array`](./Arrays.md#array-object) | `SkeletonCatRevived, TallSkeletonCatRevived, [ Squirrel Crow Snake Turtle Toad Catepillar ]` |  |
| `stacks` | Number | `2, 1, 3` | Number of stacks or intensity to apply. |
| `initiative` | [`Enum/String`](./Enums.md#enum-initiative) | `keep_turns_end_turn` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `hatch` |  |
| `turns` | [`Array`](./Arrays.md#array-turns) | `[ 1 4 ]` | Turn counter tracking. |

</details>

---

### Context: `fallback`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `do` | [`Enum/String`](./Enums.md#enum-do) | `RockToss_ColorlessCat_AsCloseAsPossible, JohnnyBlast, attack` |  |
| `do_priority` | [`Array`](./Arrays.md#array-do_priority) | `[ *attack RunFar ], [ attack TrembloEat ], [ attack, Magnetize, YeetTowardsBuddy ]` |  |
| `do_all` | [`Array`](./Arrays.md#array-do_all) | `[ move, *CoreFreakFury ]` |  |
| `do_best` | [`Array`](./Arrays.md#array-do_best) | `[ Magnetize, attack, GuillotinaTossCollide, YeetTowardsBu...` |  |
| `do_nothing` | [`Array`](./Arrays.md#array-do_nothing) | `[ ]` |  |
| `do_random` | [`Array`](./Arrays.md#array-do_random) | `[ CHSpawn CHCry ]` |  |
| `move_then_do` | [`Enum/String`](./Enums.md#enum-move_then_do) | `CerberubsCalm` |  |

</details>

---

### Context: `CaveFamilyEnrage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `CaveCatEnrageTwo, CaveCatEnrageOne` | The specific ability ID to cast. |
| `count` | Number | `0, 1` | The numerical quantity. |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `cavefamily` | Specific entity tag required. |

</details>

---

### Context: `TransformOnElementInfluence`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Holy, Fire` | Specific element type required or applied. |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CookedFood, CookedBiggestFood, CookedBigFood` |  |

</details>

---

### Context: `ChanceToSpitOnDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `TinaSpit, PteroEscape, MoonHandDrop` | The specific ability ID to cast. |
| `flat_chance` | Number | `50%, 100%` |  |
| `chance_per_damage` | Number | `0%, 2%` |  |
| `backstabs_only` | Boolean | `true` |  |
| `even_on_0_damage_if_knockback` | Boolean | `true` |  |

</details>

---

### Context: `MovementReaction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MoonHandGrab, MoonHead_EatCat, weapon` | The specific ability ID to cast. |
| `enemies_only` | Boolean | `false, true` |  |
| `objects_too` | Boolean | `true` |  |
| `on_self_move_too` | Boolean | `true` |  |
| `blind_spot` | Boolean | `true` |  |
| `forward_only` | Boolean | `true` |  |
| `self_move_exclude_self_abilities` | Boolean | `true` |  |

</details>

---

### Context: `DeathRattleRevive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `AZ_LoseHead, HitlerPulp1, HitlerPulp2` | The specific ability ID to cast. |
| `even_if_stunned` | Boolean | `true` |  |

</details>

---

### Context: `FormChangeOffMap`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `form_offmap` | [`Enum/String`](./Enums.md#enum-form_offmap) | `Start_Ceiling, Default_Ceiling, Insane_Ceiling` |  |
| `form_onmap` | [`Enum/String`](./Enums.md#enum-form_onmap) | `Insane_Ground, Default, Default_Ground` |  |

</details>

---

### Context: `SecurityBotProtect`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `SZBShoot, CBShoot_ZodiacStyle, attack` | The specific ability ID to cast. |
| `enemies_only` | Boolean | `true` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None, SBotAngryMove` |  |
| `tag_restriction` | [`Enum/String`](./Enums.md#enum-tag_restriction) | `dinofamily, dc_cat` |  |
| `not_on_kill` | Boolean | `true` |  |

</details>

---

### Context: `ally_rewards`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `blackbird_pool, chapter, dove_pool` | Generates an item drop from the specified loot pool. |

</details>

---

### Context: `StatusCollector`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `StrengthUp` | Number | `1` | Applies or references the 'StrengthUp' effect/state. |
| `Poison` | Number | `2` | Applies or references the 'Poison' effect/state. |
| `Slow` | Number | `2` | Applies or references the 'Slow' effect/state. |

</details>

---

### Context: `round_end_bonusturn_pattern`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `do_all` | [`Array`](./Arrays.md#array-do_all) | `[ MoonHead_CallForHelp MoonHead_RefreshBrace ], [ MoonHead_ChewCat MoonHead_CallForHelp MoonHead_RefreshB..., [ *QueenHippoUppercut QueenHippoAttack move QueenHippoTire ]` |  |
| `do` | [`Enum/String`](./Enums.md#enum-do) | `RallyMaggots, CutterCut, SuckMF` |  |
| `do_one` | [`Array`](./Arrays.md#array-do_one) | `[ **ZaratanaVSWeatherRoar **ZaratanaVSRoar ], [ **PyrophinaVSWeatherRoar **PyrophinaVSRoar ]` |  |
| `do_random` | [`Array`](./Arrays.md#array-do_random) | `[ TKNG_Spread TKNG_Kneel TKNG_Roulette TKNG_GoAway ], [ SimonSays_Scatter, SimonSays_ComeHere, SimonSays_GoAway ]` |  |
| `do_nothing` | [`Array`](./Arrays.md#array-do_nothing) | `[ ]` |  |
| `do_priority` | [`Array`](./Arrays.md#array-do_priority) | `[ NCReanimate NCGravecrawlFAR ]` |  |

</details>

---

### Context: `effects`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | `2, 5` | Applies or references the 'Burn' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `Thorns` | Number | `1` | Applies or references the 'Thorns' effect/state. |
| `BlackHoleSuck` | Number | `1` | Applies or references the 'BlackHoleSuck' effect/state. |
| `Confusion` | Number | `1` | Applies or references the 'Confusion' effect/state. |
| `ConstitutionUp` | Number | `-1` | Applies or references the 'ConstitutionUp' effect/state. |
| `Vaporize` | Number | `20` | Applies or references the 'Vaporize' effect/state. |

</details>

---

### Context: `FormChangeWhilePrimingAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `not_priming` | [`Enum/String`](./Enums.md#enum-not_priming) | `DualSword, SwordAndShield, NotPriming` |  |
| `priming` | [`Enum/String`](./Enums.md#enum-priming) | `Priming, SwordAndShield_Primed, DualSword_Primed` |  |

</details>

---

### Context: `MoveTowardsDamageSource`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `check_in_form` | [`Enum/String`](./Enums.md#enum-check_in_form) | `Boris, Default` |  |
| `move_ability` | [`Enum/String`](./Enums.md#enum-move_ability) | `MoveOne, MD_WalkOne` |  |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `can_move_zero` | Boolean | `true` |  |
| `check_has_status` | [`Enum/String`](./Enums.md#enum-check_has_status) | `FinalBossHitCountdownBoris` |  |
| `do_not_move_on_top` | Boolean | `true` |  |
| `face_towards_after` | Boolean | `true` |  |
| `ignore_tagged_sources` | [`Enum/String`](./Enums.md#enum-ignore_tagged_sources) | `megadino` |  |
| `move_far` | Boolean | `false` |  |
| `move_short` | Boolean | `true` |  |

</details>

---

### Context: `HasCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `PteroPeck, MoonHandSqueeze, MoonHead_ChewCat` |  |
| `animation_suffix` | String | `"Grabbing", "Cat"` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |
| `partial_animation_suffix` | String | `"Swallowed"` |  |

</details>

---

### Context: `MoveClose`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_close, stay_close_always_move, stay_close_avoid_allies` |  |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `attack, Spin_Enemy` |  |

</details>

---

### Context: `FormChangeHealthThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `form_above` | [`Enum/String`](./Enums.md#enum-form_above) | `Full, Standing, Default` |  |
| `form_below` | [`Enum/String`](./Enums.md#enum-form_below) | `Damaged, Standing2, DesireMech` |  |
| `threshold` | [`Enum/String`](./Enums.md#enum-threshold) | `X-4, 50, 25` |  |
| `count_shield` | Boolean | `true` |  |

</details>

---

### Context: `SmallRockBehavior`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `9, 5` | The base damage properties of an attack. |
| `knockback` | Number | `2, 1, 5` |  |
| `chain` | Boolean | `true` |  |

</details>

---

### Context: `Trapper`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `YA_Laser, HellHandGrab, BloatSideLaser` | The specific ability ID to cast. |
| `cancel_movement` | Boolean | `false` |  |
| `pathfinding_avoidance` | Number | `250` |  |
| `range` | Number | `10` | Distance or area of effect in tiles. |

</details>

---

### Context: `ReplaceBrain`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `brain` | [`Enum/String`](./Enums.md#enum-brain) | `PatternBrain` |  |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `default` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance, stay_close` |  |

</details>

---

### Context: `BungaEntrance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `BecomeTheDestroyer, BungaEntrance` | The specific ability ID to cast. |
| `even_if_stunned` | Boolean | `true` |  |
| `health_threshold` | Number | `150, -1` |  |
| `warrior_tag` | [`Enum/String`](./Enums.md#enum-warrior_tag) | `bungawarrior, finalboss_clonecat` |  |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `displace` | Boolean | `true` |  |
| `distance` | Number | `3` | The distance in tiles to knock the target away. |
| `self_damage` | Boolean | `false` | Recoil or self-inflicted damage/effects applied to the caster. |
| `stacks` | Number | `5` | Number of stacks or intensity to apply. |

</details>

---

### Context: `MoveAway`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MoveTwoCantrip, DoubleDistanceMove, ExtraMove` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_far, blind_move_far, keep_distance_always_move` |  |

</details>

---

### Context: `MoveWhenDamaged`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `weights` | [`Enum/String`](./Enums.md#enum-weights) | `stay_far_always_move, chaotic, stay_near_allies_always_move` |  |
| `move_ability` | [`Enum/String`](./Enums.md#enum-move_ability) | `WaterTrailMove` |  |

</details>

---

### Context: `Rage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | String | `"Rage"` |  |
| `animation_suffix` | String | `"Rage"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `ChubsSpinRage` |  |
| `move_speed_multiplier` | Number | `2` |  |

</details>

---

### Context: `TransformOnDeathImmediately`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `first_turn` | [`Enum/String`](./Enums.md#enum-first_turn) | `keep_turns` |  |
| `obj` | [`Enum/String`](./Enums.md#enum-obj) | `TallSkeletonCatCorpse, SkeletonCatCorpse, SkeletonShamblerCorpse` |  |

</details>

---

### Context: `hot`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Hot"` |  |
| `name` | String | `"OBJECT_HOTPETROCK_NAME", "OBJECT_HOTROCK_NAME", "OBJECT_HOTBOULDER_NAME"` | Localization key for the character's name. |

</details>

---

### Context: `Buddy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | `false` |  |
| `obj` | [`Enum/String`](./Enums.md#enum-obj) | `PyrophinaVS, Dice, ZaratanaVS` |  |
| `reclaim_if_lost` | Boolean | `true` |  |

</details>

---

### Context: `FinalBossPupils`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `look_at_offset` | [`Array`](./Arrays.md#array-look_at_offset) | `[ 0 2.5 0 ]` |  |
| `radius` | Number | `13` | Distance or area of effect in tiles. |
| `reset_center_because_no_target_halflife` | [`Enum/String`](./Enums.md#enum-reset_center_because_no_target_halflife) | `.1` |  |
| `reset_center_because_of_animation_halflife` | [`Enum/String`](./Enums.md#enum-reset_center_because_of_animation_halflife) | `.05` |  |
| `teleport_tracking_halflife` | [`Enum/String`](./Enums.md#enum-teleport_tracking_halflife) | `.01` |  |
| `tracking_acquisition_halflife` | [`Enum/String`](./Enums.md#enum-tracking_acquisition_halflife) | `.1` |  |
| `virtual_head_position` | [`Array`](./Arrays.md#array-virtual_head_position) | `[ 11 2 11 ]` |  |

</details>

---

### Context: `ReflectProjectiles`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `self_damage` | Number | `2` | Recoil or self-inflicted damage/effects applied to the caster. |

</details>

---

### Context: `2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicMelee_2Hits, BoneWormShotMed` |  |
| `partial_animation_suffix` | Number | `2` |  |
| `animation_suffix` | Number | `2` |  |
| `uifloaters_offset` | Number | `2.2` |  |

</details>

---

### Context: `3`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicMelee_3Hits, BoneWormShotTall` |  |
| `partial_animation_suffix` | Number | `3` |  |
| `animation_suffix` | Number | `3` |  |
| `uifloaters_offset` | Number | `3` |  |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MoveTwo` | The specific ability ID to cast. |
| `range` | Number | `2, 4` | Distance or area of effect in tiles. |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `food` | Specific entity tag required. |

</details>

---

### Context: `ArmorPickup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `frame_range` | [`Array`](./Arrays.md#array-frame_range) | `[ 3 5 ], [ 6 6 ], [ 1 2 ]` |  |
| `stacks` | Number | `6, 2, 4` | Number of stacks or intensity to apply. |

</details>

---

### Context: `CaveMan`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"CaveMan"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `CaveMan3HitCombo` |  |
| `name` | String | `"ENEMY_CAVEMANMAN_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_CAVEMANMAN_DESC"` |  |

</details>

---

### Context: `CaveManSpear`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"SpearCaveMan"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `CaveManThrowSpear` |  |
| `name` | String | `"ENEMY_SPEARCAVEMAN_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_SPEARCAVEMAN_DESC"` |  |

</details>

---

### Context: `ManaPickup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `frame_range` | [`Array`](./Arrays.md#array-frame_range) | `[ 3 5 ], [ 6 6 ], [ 1 2 ]` |  |
| `stacks` | Number | `6, 2, 4` | Number of stacks or intensity to apply. |

</details>

---

### Context: `MoveForThrow`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `PyrophinaVSCatThrow, PyrophinaSoloCatThrow` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `util_minmove` |  |

</details>

---

### Context: `MoveTowardsKillers`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `character_filter` | [`Array`](./Arrays.md#array-character_filter) | `[ SpiderCat, TallSpiderCat ]` |  |
| `move_ability` | [`Enum/String`](./Enums.md#enum-move_ability) | `SpiderReturn` |  |

</details>

---

### Context: `SpawnOnDeath`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `faction` | [`Enum/String`](./Enums.md#enum-faction) | `enemies, allies` |  |
| `obj` | [`Array`](./Arrays.md#array-obj) | `RiftKitten, [ Kitten Kitten TomTom TomTom Mangy Mangy CatCaller CatCa..., [ Spookie Spookie Scary Coin2 Coin3 Coin4 ]` |  |

</details>

---

### Context: `SpearRun`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `CaveManSpearRun` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `CaveManPickupSpear` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `util_minmove` |  |

</details>

---

### Context: `SpewerAltGraphics`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Fire` | Number | `1` | Character Form: Behavior and stats for the 'Fire' state. |
| `FireFull` | Number | `1` | Character Form: Behavior and stats for the 'FireFull' state. |
| `Normal` | Number | `0` | Character Form: Behavior and stats for the 'Normal' state. |
| `NormalFull` | Number | `0` | Character Form: Behavior and stats for the 'NormalFull' state. |
| `Tar` | Number | `2` | Character Form: Behavior and stats for the 'Tar' state. |
| `TarFull` | Number | `2` | Character Form: Behavior and stats for the 'TarFull' state. |

</details>

---

### Context: `StatusEachTurnBeginIfHasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `2` | Applies or references the 'AllStatsUp' effect/state. |
| `DamageUp` | Number | `2` | Applies or references the 'DamageUp' effect/state. |
| `HealthGain` | Number | `8` | Applies or references the 'HealthGain' effect/state. |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `pulse3` |  |
| `consume` | Boolean | `true` |  |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Counterspell` | ID of the status effect to apply or check. |

</details>

---

### Context: `TVBotScreen`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Die` | Number | `6` | Character Form / Logic: Forces the character to die. |
| `Dumb` | Number | `3` | AI Profile: A simplified, less optimal decision-making profile. |
| `Fuck` | Number | `5` | Applies or references the 'Fuck' effect/state. |
| `Obey` | Number | `1` | AI State: Enforced compliance logic (e.g., when Charmed). |
| `Shit` | Number | `4` | Applies or references the 'Shit' effect/state. |
| `Stop` | Number | `2` | AI Movement: Forces the character to cease movement. |

</details>

---

### Context: `Turtled`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Turtle` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |

</details>

---

### Context: `BattlefieldUniqueRandomPassive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Number | `1` | Applies or references the 'DemonicGlyph_Bite' effect/state. |
| `DemonicGlyph_Bounce` | Number | `1` | Applies or references the 'DemonicGlyph_Bounce' effect/state. |
| `DemonicGlyph_Fire` | Number | `1` | Applies or references the 'DemonicGlyph_Fire' effect/state. |
| `DemonicGlyph_Movement` | Number | `1` | Applies or references the 'DemonicGlyph_Movement' effect/state. |
| `DemonicGlyph_Summon` | Number | `1` | Applies or references the 'DemonicGlyph_Summon' effect/state. |

</details>

---

### Context: `Bishop`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Bishop"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BBXLightning` |  |
| `name` | String | `"ENEMY_CULTISTBISHOP_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_CULTISTBISHOP_DESC"` |  |
| `uifloaters_offset` | Number | `2.5` |  |

</details>

---

### Context: `BungaCheers`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ally_damage` | [`Enum/String`](./Enums.md#enum-ally_damage) | `littleboo` |  |
| `ally_dead` | [`Enum/String`](./Enums.md#enum-ally_dead) | `bigboo` |  |
| `enemy_damage` | [`Enum/String`](./Enums.md#enum-enemy_damage) | `littlecheer` |  |
| `enemy_dead` | [`Enum/String`](./Enums.md#enum-enemy_dead) | `bigcheer` |  |
| `warrior_tag` | [`Enum/String`](./Enums.md#enum-warrior_tag) | `bungawarrior` |  |

</details>

---

### Context: `FinalBossHitCountdownBoris`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Block`](./Characters_and_Bosses.md#context-forceuseability) | `{ ... }, TheChild_TransformExplosive` | Logic: Forces the execution of a specific ability. |
| `icon` | Number | `802` |  |
| `icon_ready` | Number | `803` |  |
| `stacks` | Number | `7` | Number of stacks or intensity to apply. |

</details>

---

### Context: `FinalBossHitCountdownExplosive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Block`](./Characters_and_Bosses.md#context-forceuseability) | `{ ... }, TheChild_TransformHoly` | Logic: Forces the execution of a specific ability. |
| `icon` | Number | `800` |  |
| `icon_ready` | Number | `801` |  |
| `stacks` | Number | `7` | Number of stacks or intensity to apply. |

</details>

---

### Context: `Grown`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Grown` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `HitlerCloneSwipes` |  |
| `name` | String | `"ENEMY_HITLERCLONE_NAME"` | Localization key for the character's name. |
| `uifloaters_offset` | Number | `1.5` |  |
| `weak_threshold` | Number | `15` |  |

</details>

---

### Context: `MonkCatReactionAbilities`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `attack` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `move` |  |
| `spell` | [`Enum/String`](./Enums.md#enum-spell) | `MCHadouken` |  |
| `trinket` | [`Enum/String`](./Enums.md#enum-trinket) | `MCHadouken` |  |
| `weapon` | [`Enum/String`](./Enums.md#enum-weapon) | `attack` | Weapon item constraint. |

</details>

---

### Context: `Mutant`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Mutant"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BBMutantSwipe` |  |
| `move_speed_multiplier` | [`Enum/String`](./Enums.md#enum-move_speed_multiplier) | `.5` |  |
| `name` | String | `"ENEMY_CULTISTMUTANT_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_CULTISTMUTANT_DESC"` |  |

</details>

---

### Context: `PassiveWhileHasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `DemonicGlyph_Summon, DemonicGlyph_Fire, DemonicGlyph_Bite` | ID of the status effect to apply or check. |

</details>

---

### Context: `Pulp2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `2` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |
| `tooltip` | [`Enum/String`](./Enums.md#enum-tooltip) | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `uifloaters_offset` | Number | `1` |  |

</details>

---

### Context: `Pulp3`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `3` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |
| `tooltip` | [`Enum/String`](./Enums.md#enum-tooltip) | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `uifloaters_offset` | Number | `1` |  |

</details>

---

### Context: `Pulp4`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `4` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |
| `tooltip` | [`Enum/String`](./Enums.md#enum-tooltip) | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `uifloaters_offset` | Number | `1` |  |

</details>

---

### Context: `Pulp5`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `5` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |
| `tooltip` | [`Enum/String`](./Enums.md#enum-tooltip) | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `uifloaters_offset` | Number | `1` |  |

</details>

---

### Context: `Pulp6`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `6` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |
| `tooltip` | [`Enum/String`](./Enums.md#enum-tooltip) | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `uifloaters_offset` | Number | `1` |  |

</details>

---

### Context: `Pulp7`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `7` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |
| `tooltip` | [`Enum/String`](./Enums.md#enum-tooltip) | `ENEMY_TERMINATOR3_HITLERHEAD_DESC` |  |
| `uifloaters_offset` | Number | `1` |  |

</details>

---

### Context: `SlotMachineRollPool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SlotResult_Jackpot_Coins` | Number | `1` | Applies or references the 'SlotResult_Jackpot_Coins' effect/state. |
| `SlotResult_Explode` | Number | `1` | Applies or references the 'SlotResult_Explode' effect/state. |
| `SlotResult_Nothing` | Number | `7` | Applies or references the 'SlotResult_Nothing' effect/state. |
| `SlotResult_RandomPickup` | Number | `11` | Applies or references the 'SlotResult_RandomPickup' effect/state. |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `UseAbility_NonStack` | [`Enum/String`](./Enums.md#enum-useability_nonstack) | `BBTransformZealot, GenericRage` | Applies or references the 'UseAbility_NonStack' effect/state. |
| `HealthGain` | Number | `5` | Applies or references the 'HealthGain' effect/state. |

</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ExtraBasicAttacks_Status` | Number | `1` | Applies or references the 'ExtraBasicAttacks_Status' effect/state. |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |
| `HealthRegenUp` | Number | `1` | Applies or references the 'HealthRegenUp' effect/state. |
| `TakeExtraTurn` | Number | `1` | Applies or references the 'TakeExtraTurn' effect/state. |

</details>

---

### Context: `eat_damage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | `true` |  |
| `damage` | Number | `0` | The base damage properties of an attack. |
| `makes_contact` | Boolean | `true` |  |
| `piercing` | Boolean | `true` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `melee` | Classification/category type. |

</details>

---

### Context: `AbilityOnRoundEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `DestroyerRaise` | The specific ability ID to cast. |
| `force_display_name` | Boolean | `true` |  |

</details>

---

### Context: `BaitAura`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `range` | Number | `3` | Distance or area of effect in tiles. |

</details>

---

### Context: `Cat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `formchange` | [`Enum/String`](./Enums.md#enum-formchange) | `BigHoldingCat, SmallHoldingCat` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `spawnHoldingCat` |  |

</details>

---

### Context: `CaveBaby`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"CaveBaby"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `CaveBabyMelee` |  |
| `name` | String | `"ENEMY_CAVEBABY_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_CAVEBABY_DESC"` |  |

</details>

---

### Context: `CaveWoman`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"CaveWoman"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `CaveWomanKick` |  |
| `name` | String | `"ENEMY_CAVEMANWOMAN_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_CAVEMANWOMAN_DESC"` |  |

</details>

---

### Context: `CaveWomanHasCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"CatCaveWoman"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `CaveWomanCatSlap` |  |
| `name` | String | `"ENEMY_CAVEMANWOMAN2_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_CAVEMANWOMAN2_DESC"` |  |

</details>

---

### Context: `CherubimReaction`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Leave` | [`Enum/String`](./Enums.md#enum-leave) | `LELeave, CherubimLeave` | Applies or references the 'Leave' effect/state. |
| `Return` | [`Enum/String`](./Enums.md#enum-return) | `CherubimReturn, LEReturn` | Applies or references the 'Return' effect/state. |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `chapter` | Generates an item drop from the specified loot pool. |
| `odds` | Number | `5%, 33%` | The probability (0.0 to 1.0) of triggering the 'good roll' success state. |

</details>

---

### Context: `Cultist`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Cultist"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicMelee` |  |
| `name` | String | `"ENEMY_CULTISTLACKEY_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_CULTISTLACKEY_DESC"` |  |

</details>

---

### Context: `DashRandomly`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `ShamblerDash` | The specific ability ID to cast. |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `blind` |  |

</details>

---

### Context: `Down`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Down"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `ButtFart` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `TeleportFlipUp` |  |

</details>

---

### Context: `DualSword`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"2"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `DestroyerAttack2` |  |
| `move_speed_multiplier` | Number | `1.5` |  |
| `tooltip` | String | `"ENEMY_DESTROYER2_DESC"` |  |

</details>

---

### Context: `DualSword_Primed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Holy2"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `DestroyerAttack2` |  |
| `move_speed_multiplier` | Number | `1.5` |  |
| `tooltip` | String | `"ENEMY_DESTROYER2_DESC"` |  |

</details>

---

### Context: `Escape`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `DybbukEscape` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance_always_move` |  |

</details>

---

### Context: `ForceUseAbility`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`FinalBossHitCountdownBoris`](./Characters_and_Bosses.md#context-finalbosshitcountdownboris), [`FinalBossHitCountdownExplosive`](./Characters_and_Bosses.md#context-finalbosshitcountdownexplosive)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `TheChild_Wrath, TheChild_Pulse` | The specific ability ID to cast. |
| `show_name` | Boolean | `true` |  |

</details>

---

### Context: `FormChangeDuringWeatherElement`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Water` | Specific element type required or applied. |
| `form` | [`Enum/String`](./Enums.md#enum-form) | `Rain` |  |

</details>

---

### Context: `Full`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Full"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `KirbySpit` |  |

</details>

---

### Context: `MegaDinoDropController`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `head_drop` | [`Enum/String`](./Enums.md#enum-head_drop) | `MD_HeadDrop` |  |
| `leg_leave` | [`Enum/String`](./Enums.md#enum-leg_leave) | `MD_LegLeave` |  |
| `leg_return` | [`Enum/String`](./Enums.md#enum-leg_return) | `MD_LegReturn` |  |
| `stable_legs` | Number | `3` |  |

</details>

---

### Context: `MotherTumorPassive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `considered_forms` | [`Array`](./Arrays.md#array-considered_forms) | `[ Big BigHolding BigHoldingCat ]` |  |
| `grow_ability` | [`Enum/String`](./Enums.md#enum-grow_ability) | `MotherTumorGrow` |  |
| `pass_ani` | [`Enum/String`](./Enums.md#enum-pass_ani) | `pass` |  |
| `receive_ani` | [`Enum/String`](./Enums.md#enum-receive_ani) | `receive` |  |

</details>

---

### Context: `MoveCenter`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_near_map_center` |  |

</details>

---

### Context: `NonCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `formchange` | [`Enum/String`](./Enums.md#enum-formchange) | `BigHolding, SmallHolding` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `spawnHolding` |  |

</details>

---

### Context: `ProtectTargetedAllies`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `SwapPositions_TankCat` | The specific ability ID to cast. |
| `target_filter` | [`Enum/String`](./Enums.md#enum-target_filter) | `any, Kitten` |  |

</details>

---

### Context: `RemoveStatusStacks`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | `10, 1` | The number of stacks to remove. |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Brace, DodgeChance_Status` | The specific status effect ID to remove. |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `HealthGain` | Number | `4` | Applies or references the 'HealthGain' effect/state. |
| `SpeedUp` | Number | `2` | Applies or references the 'SpeedUp' effect/state. |

</details>

---

### Context: `StatusGroup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FindItemFromPool` | [`Enum/String`](./Enums.md#enum-finditemfrompool) | `mutant_pool, parasites` | Generates an item drop from the specified loot pool. |

</details>

---

### Context: `TinkererBasicAttackSwitching`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `craft_ability` | [`Enum/String`](./Enums.md#enum-craft_ability) | `TinkererCraft` |  |
| `throw_ability` | [`Enum/String`](./Enums.md#enum-throw_ability) | `TinkererThrow` |  |

</details>

---

### Context: `TransformOnElementInfluencex`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Holy` | Specific element type required or applied. |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Bait, PurifiedPoisonFood` |  |

</details>

---

### Context: `Washer`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicMelee` |  |
| `name` | String | `"ENEMY_CULTISTWASHER_NAME"` | Localization key for the character's name. |
| `partial_animation_suffix` | String | `"Cultist"` |  |
| `tooltip` | String | `"ENEMY_CULTISTWASHER_DESC"` |  |

</details>

---

### Context: `WereMan`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"WereMan"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `WereManFurySwipes` |  |
| `name` | String | `"ENEMY_WEREMAN_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_WEREMAN_DESC"` |  |

</details>

---

### Context: `Zealot`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Zealot"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BBStabby` |  |
| `name` | String | `"ENEMY_CULTISTZEALOT_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_CULTISTZEALOT_DESC"` |  |

</details>

---

### Context: `ZealotBomb`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"BombZealot"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BBExplode` |  |
| `name` | String | `"ENEMY_BOMBZEALOT_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"ENEMY_BOMBZEALOT_DESC"` |  |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `TVBotDie` | Number | `1` | Applies or references the 'TVBotDie' effect/state. |
| `TVBotDumb` | Number | `1` | Applies or references the 'TVBotDumb' effect/state. |
| `TVBotObey` | Number | `1` | Applies or references the 'TVBotObey' effect/state. |
| `TVBotStop` | Number | `1` | Applies or references the 'TVBotStop' effect/state. |

</details>

---

### Context: `1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `1` |  |
| `partial_animation_suffix` | Number | `1` |  |
| `uifloaters_offset` | Number | `1.4` |  |

</details>

---

### Context: `4`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | `4` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicMelee_4Hits` |  |
| `partial_animation_suffix` | Number | `4` |  |

</details>

---

### Context: `AllStatsAura`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `aura_requires_tag` | [`Enum/String`](./Enums.md#enum-aura_requires_tag) | `humanoid` |  |
| `range` | [`Enum/String`](./Enums.md#enum-range) | `global` | Distance or area of effect in tiles. |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `Big`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Big, "Big"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `GameteSpawn` |  |

</details>

---

### Context: `BlackHole`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"BlackHole"` |  |
| `name` | String | `"OBJECT_BLACKHOLE_NAME"` | Localization key for the character's name. |
| `tooltip` | String | `"OBJECT_BLACKHOLE_DESC"` |  |

</details>

---

### Context: `ChaosBossFormChangeGuide`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `active_pieces` | [`Array`](./Arrays.md#array-active_pieces) | `[ Johnny Throb Flush ]` |  |
| `passive_pieces` | [`Array`](./Arrays.md#array-passive_pieces) | `[ Host Nettle Bubs ]` |  |
| `passives_health_threshold` | Number | `50%` |  |

</details>

---

### Context: `ChaosHeadDropIn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `ChaosSpawnIn` | The specific ability ID to cast. |
| `new_music` | [`Enum/String`](./Enums.md#enum-new_music) | `chaos_boss_part2` |  |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `riftheadguardian` | Specific entity tag required. |

</details>

---

### Context: `Default`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `LennyShove` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `LennyTrampleMove` |  |
| `partial_animation_suffix` | String | `""` |  |

</details>

---

### Context: `Explody`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Expl` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `ToxExplode` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |

</details>

---

### Context: `FaceAwayLastDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean | `true` |  |
| `override_hit_animation` | Boolean | `true` |  |
| `use_turn_animations` | Boolean | `true` |  |

</details>

---

### Context: `FinalBossBeamQueue`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `queue` | [`Enum/String`](./Enums.md#enum-queue) | `TheChild_TargetBeam` |  |
| `release` | [`Enum/String`](./Enums.md#enum-release) | `TheChild_ReleaseBeams` |  |
| `transform` | [`Enum/String`](./Enums.md#enum-transform) | `TheChild_TransformBoris` |  |

</details>

---

### Context: `FinalBossHitCountdownHoly`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `icon` | Number | `804` |  |
| `icon_ready` | Number | `805` |  |
| `stacks` | Number | `7` | Number of stacks or intensity to apply. |

</details>

---

### Context: `HitlerExecute`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `HitlerShoot` | The specific ability ID to cast. |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `grown_hitler_clone` | Specific entity tag required. |
| `threshold` | Number | `15` |  |

</details>

---

### Context: `HumanDead`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `DH` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `HCSpin` |  |
| `tooltip` | String | `"ENEMY_HUMANCAT2_DESC"` |  |

</details>

---

### Context: `InfiniteRebirth`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `health` | Number | `25%` |  |
| `immediate` | Boolean | `true` |  |
| `playercat_health` | Number | `25%` |  |

</details>

---

### Context: `Lifted`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Lift"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |

</details>

---

### Context: `MoveAwayWhenEnemyAdjacent`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `move_ability` | [`Enum/String`](./Enums.md#enum-move_ability) | `YA_Jetpack` |  |
| `once_per_turn` | Boolean | `true` |  |
| `weights` | [`Enum/String`](./Enums.md#enum-weights) | `stay_far_always_move` |  |

</details>

---

### Context: `MoveForBarrage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `ZaratanaVSBombardment` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_far` |  |

</details>

---

### Context: `MoveForDash`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `attack` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance` |  |

</details>

---

### Context: `MoveForGrass`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `StegoGrassStomp` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `StegoEatGrass` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `minimum_move` |  |

</details>

---

### Context: `MoveForPounce`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `attack` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance` |  |

</details>

---

### Context: `MoveForSpin`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `PyrophinaVSRun` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `PyrophinaVSSpinThrow` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_close` |  |

</details>

---

### Context: `MoveOneForPuke`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `AlienBeastMoveOne` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `AlienBeastPuke` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance` |  |

</details>

---

### Context: `MoveToHead`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `G3RunToHead` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `G3GrabHead` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `minimum_move` |  |

</details>

---

### Context: `MoveTowards`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `attack` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_close` |  |

</details>

---

### Context: `Normal`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `TinaBasicBigMeleeA, SpewerLobbed_Normal` |  |
| `animation_suffix` | String | `"Up"` |  |

</details>

---

### Context: `Nuke`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Nuke` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `None` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `None` |  |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `0` | The base damage properties of an attack. |
| `knockback` | Number | `5` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `status` | Classification/category type. |

</details>

---

### Context: `Sitting`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Chair` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `DoNothing` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `DoNothing` |  |

</details>

---

### Context: `SquirrelForm`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicMelee` |  |
| `tooltip` | [`Enum/String`](./Enums.md#enum-tooltip) | `ENEMY_DRAVENSQUIRRELFORM_DESC` |  |

</details>

---

### Context: `StacyMutant_Health`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddMaxHealth` | Number | `25` | Applies or references the 'AddMaxHealth' effect/state. |
| `AddSpeed` | Number | `-3` | Applies or references the 'AddSpeed' effect/state. |
| `SizeScale` | Number | `1.2` | Applies or references the 'SizeScale' effect/state. |

</details>

---

### Context: `StacyMutant_Ice`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddMovement` | Number | `-1` | Applies or references the 'AddMovement' effect/state. |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Ice` | Applies or references the 'ElementImmune' effect/state. |
| `ReplaceBasicAttack` | [`Enum/String`](./Enums.md#enum-replacebasicattack) | `SM_IceBreath` | Applies or references the 'ReplaceBasicAttack' effect/state. |

</details>

---

### Context: `StacyMutant_Speed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddDamage` | Number | `-1` | Applies or references the 'AddDamage' effect/state. |
| `AddSpeed` | Number | `6` | Applies or references the 'AddSpeed' effect/state. |
| `SizeScale` | [`Enum/String`](./Enums.md#enum-sizescale) | `.8` | Applies or references the 'SizeScale' effect/state. |

</details>

---

### Context: `SuckMF`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `TormentorSuck` | The specific ability ID to cast. |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `careless` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance` |  |

</details>

---

### Context: `SupportFormChangeInsteadOfRun`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `SBotAnger, TVChangeDie` | The specific ability ID to cast. |
| `wait_till_turn` | Boolean | `true` |  |

</details>

---

### Context: `T3HitlerSpawningPhase`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `T3JoinFight` | Flag |  | Applies or references the 'T3JoinFight' effect/state. |
| `T3Spawn_Colorless` | Flag |  | Applies or references the 'T3Spawn_Colorless' effect/state. |
| `spell_use_groups` | [`Array`](./Arrays.md#array-spell_use_groups) | `[ [ T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T...` |  |

</details>

---

### Context: `TransformOnStatusThreshold`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Moth` |  |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `AllStatsUp` | ID of the status effect to apply or check. |
| `threshold` | Number | `5` |  |

</details>

---

### Context: `TwisterFling`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `5` | The base damage properties of an attack. |
| `max_dist` | Number | `5` |  |
| `min_dist` | Number | `3` |  |

</details>

---

### Context: `Unflip`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `TeleportFlipUp` | The specific ability ID to cast. |
| `move_for_ability` | [`Enum/String`](./Enums.md#enum-move_for_ability) | `Spin_Enemy` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_close_always_move` |  |

</details>

---

### Context: `Up`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Up"` |  |
| `tooltip` | String | `"OBJECT_TIREUP_DESC"` |  |

</details>

---

### Context: `ai_if_spawned_as_enemy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `brain` | [`Enum/String`](./Enums.md#enum-brain) | `PatternBrain` |  |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `default` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `keep_distance` |  |

</details>

---

### Context: `dispersed_bonusturn_pattern`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `do` | [`Enum/String`](./Enums.md#enum-do) | `Simon_Trash, attack, Simon_Tentacle` |  |

</details>

---

### Context: `other_form_change_abilities`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Boris` | [`Enum/String`](./Enums.md#enum-boris) | `MegaGuppy_TransformBoris` | Character Form / AI State: Behavior and stats for the 'Boris' state. |
| `Explosive` | [`Enum/String`](./Enums.md#enum-explosive) | `MegaGuppy_TransformExplosive` | Character Form: Behavior and stats for the 'Explosive' state. |
| `Holy` | [`Enum/String`](./Enums.md#enum-holy) | `MegaGuppy_TransformHoly` | Character Form: Behavior and stats for the 'Holy' state. |

</details>

---

### Context: `statuses`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |

</details>

---

### Context: `5`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BasicMelee_5Hits` |  |
| `partial_animation_suffix` | Number | `5` |  |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Fury` | Number | `75` | Applies or references the 'Fury' effect/state. |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `ZombieTombstone` | The ID of the ability to autocast. |
| `even_if_stunned` | Boolean | `true` | If true, bypasses stun and hard-CC restrictions to cast anyway. |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `BackflipDodge` | The specific dodge ability to trigger (e.g., DestroyerDodge). |
| `stacks` | Number | `1` | Number of stacks or intensity to apply. |

</details>

---

### Context: `Boris`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"2"` |  |

</details>

---

### Context: `CerberubsAggroTargetBehavior`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `alert_form` | [`Enum/String`](./Enums.md#enum-alert_form) | `Alert` |  |
| `default_form` | [`Enum/String`](./Enums.md#enum-default_form) | `Normal` |  |

</details>

---

### Context: `CerberubsJumpBlind`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `CerberubsJump` | The specific ability ID to cast. |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `nubs_fakeblind` |  |

</details>

---

### Context: `CerberubsJumpNormal`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `CerberubsJump` | The specific ability ID to cast. |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `default` |  |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `DybbukBackflipDodge` | The specific ability ID to cast. |
| `chance` | Number | `100%` | Probability (0.0 to 1.0) of executing this action. |

</details>

---

### Context: `ChanceToFormChangeOnAbilityDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `15%` | Probability (0.0 to 1.0) of executing this action. |
| `form` | [`Enum/String`](./Enums.md#enum-form) | `Flop2` |  |

</details>

---

### Context: `ChaosBossPieces`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `active_pieces` | [`Array`](./Arrays.md#array-active_pieces) | `[ Johnny Throb Flush ]` |  |
| `passive_pieces` | [`Array`](./Arrays.md#array-passive_pieces) | `[ Host Nettle Bubs ]` |  |

</details>

---

### Context: `Charging`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `MoonHead_Blow` |  |
| `partial_animation_suffix` | String | `"Charging"` |  |

</details>

---

### Context: `CloseConvert`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MarshmallowConvert` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_close` |  |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `odds` | Number | `0.5` | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. |

</details>

---

### Context: `CounterAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `StegoTailSwipe` | The specific ability ID to cast. |
| `without_orienting` | Boolean | `true` |  |

</details>

---

### Context: `DelayedAutoRevive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `health` | Number | `50%` |  |
| `rounds` | Number | `1` |  |

</details>

---

### Context: `DiceBehavior`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `dice_size` | Number | `6` |  |
| `knockback_damage` | Number | `5` |  |

</details>

---

### Context: `DiesToElement`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Fire` | Specific element type required or applied. |
| `instant` | Boolean | `true` |  |

</details>

---

### Context: `DybbukPossessionFallback`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `exit_ability` | [`Enum/String`](./Enums.md#enum-exit_ability) | `DybbukReturn` |  |
| `form` | [`Enum/String`](./Enums.md#enum-form) | `Possessing` |  |

</details>

---

### Context: `Empty`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `""` |  |

</details>

---

### Context: `Explosive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"3"` |  |

</details>

---

### Context: `FightPhase`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `T3Shoot` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `FloatMove` |  |

</details>

---

### Context: `FinalBossBecomeTheChild`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `GlobalSpawnCharacter` | [`Enum/String`](./Enums.md#enum-globalspawncharacter) | `MegaGuppy` | Applies or references the 'GlobalSpawnCharacter' effect/state. |
| `PlayBackground` | Number | `1` | Applies or references the 'PlayBackground' effect/state. |

</details>

---

### Context: `FinalBossShieldHealth`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `break_ability` | [`Enum/String`](./Enums.md#enum-break_ability) | `DestroyerBreakShield` |  |
| `state_health` | [`Array`](./Arrays.md#array-state_health) | `[ 0 35 35 35 35 0 ]` |  |

</details>

---

### Context: `FireFull`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Full` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `SpewerSpit` |  |

</details>

---

### Context: `FoodMove`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `CaveBabyFoodMove` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_close_move_if_possible` |  |

</details>

---

### Context: `ForceTrample`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `BirthwortTrample` | The specific ability ID to cast. |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `always_cast_careless` |  |

</details>

---

### Context: `GainDisorderFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | [`Enum/String`](./Enums.md#enum-chance) | `.1` | Probability (0.0 to 1.0) of executing this action. |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `diseases` |  |

</details>

---

### Context: `HPAltStates`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `clipname` | [`Enum/String`](./Enums.md#enum-clipname) | `poopmain` |  |
| `thresholds` | [`Array`](./Arrays.md#array-thresholds) | `[ [ 1 0 ]` |  |

</details>

---

### Context: `HalfDead`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"2"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `RatKingDash` |  |

</details>

---

### Context: `HasDeadCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"CatDead"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `LennyCatSlap` |  |

</details>

---

### Context: `HasRock`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"rock"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `AmoebaRockBash` |  |

</details>

---

### Context: `HealNeighborsEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | `true` |  |
| `stacks` | Number | `3` | Number of stacks or intensity to apply. |

</details>

---

### Context: `Holy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"1"` |  |

</details>

---

### Context: `InitialPhase`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `T3Shoot` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `FloatMove` |  |

</details>

---

### Context: `JohnnyNeedsWashing`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `form_unwashed` | [`Enum/String`](./Enums.md#enum-form_unwashed) | `Unwashed` |  |
| `form_washed` | [`Enum/String`](./Enums.md#enum-form_washed) | `Washed` |  |

</details>

---

### Context: `LeapClose`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `GKLeap` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `towards_aggro` |  |

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

### Context: `ModularPickup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Cleanse` | Number | `0` | Applies or references the 'Cleanse' effect/state. |
| `sound_event` | [`Enum/String`](./Enums.md#enum-sound_event) | `EatAntidote` |  |

</details>

---

### Context: `Mount`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `eject_ability` | [`Enum/String`](./Enums.md#enum-eject_ability) | `MechSuitEject` |  |
| `enter_ability` | [`Enum/String`](./Enums.md#enum-enter_ability) | `EnterMech` |  |

</details>

---

### Context: `MoveSpaced`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `move` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `terminator_keep_distance_always_move` |  |

</details>

---

### Context: `MultiSpawnOnDeath`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count` | [`Array`](./Arrays.md#array-count) | `[ 0, 2 ]` | The numerical quantity. |
| `obj` | [`Enum/String`](./Enums.md#enum-obj) | `Maggot` |  |

</details>

---

### Context: `NCGravecrawlFAR`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `NCGravecrawl` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_far` |  |

</details>

---

### Context: `NormalFull`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Full` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `SpewerSpit` |  |

</details>

---

### Context: `Open`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Open` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `GSOpenAttack` |  |

</details>

---

### Context: `PassiveWhileNotHasStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `ExistUntilIdleUpkeep, DemonicGlyph_Movement` | ID of the status effect to apply or check. |

</details>

---

### Context: `Primed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `GA_Telekinesis_Big` |  |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `primed` |  |

</details>

---

### Context: `ReturnA`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `HangerBotReturn` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_close` |  |

</details>

---

### Context: `RunFar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `PyrophinaVSRun` | The specific ability ID to cast. |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `run_far` |  |

</details>

---

### Context: `RunWhenLastPlayerCatIsCharmed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean | `true` |  |
| `legacy_savekey` | [`Enum/String`](./Enums.md#enum-legacy_savekey) | `Legacy_Marshmallow_StolenCatID` |  |

</details>

---

### Context: `ScalingAttackAnimation`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `default` | [`Enum/String`](./Enums.md#enum-default) | `bite1` | Baseline configuration. |
| `thresholds` | [`Array`](./Arrays.md#array-thresholds) | `[ [ 5, bite2 ]` |  |

</details>

---

### Context: `SkipFirstRounds`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pop_chance` | Number | `50%` |  |
| `stacks` | Number | `2` | Number of stacks or intensity to apply. |

</details>

---

### Context: `Small`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `""` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `GameteInflate` |  |

</details>

---

### Context: `StacyMutant_Damage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddDamage` | Number | `2` | Applies or references the 'AddDamage' effect/state. |
| `AddMaxHealth` | Number | `-25` | Applies or references the 'AddMaxHealth' effect/state. |

</details>

---

### Context: `StacyMutant_Fire`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Fire` | Applies or references the 'ElementImmune' effect/state. |
| `ReplaceBasicAttack` | [`Enum/String`](./Enums.md#enum-replacebasicattack) | `SM_Lavashot` | Applies or references the 'ReplaceBasicAttack' effect/state. |

</details>

---

### Context: `StacyMutant_Lightning`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Electric` | Applies or references the 'ElementImmune' effect/state. |
| `ReplaceBasicAttack` | [`Enum/String`](./Enums.md#enum-replacebasicattack) | `SM_LightningDash` | Applies or references the 'ReplaceBasicAttack' effect/state. |

</details>

---

### Context: `Standing`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BungaSmash` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `DefaultMove` |  |

</details>

---

### Context: `Standing2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `BungaSmash` |  |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `BungaJumpMove` |  |

</details>

---

### Context: `StatusAfterXTurns`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `CancerExplode` | Logic: Forces the execution of a specific ability. |
| `stacks` | Number | `3` | Number of stacks or intensity to apply. |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RemoveAmbientLightEffects` | Number | `4` | Applies or references the 'RemoveAmbientLightEffects' effect/state. |
| `RemoveGlobalModifiers` | [`Array`](./Arrays.md#array-removeglobalmodifiers) | `[ BloodRain ]` | Applies or references the 'RemoveGlobalModifiers' effect/state. |

</details>

---

### Context: `StatusOnSpawnIn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Number | `1` | Applies or references the 'CaptureFamiliar' effect/state. |
| `SetHealth` | Number | `50%` | Applies or references the 'SetHealth' effect/state. |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ConstitutionUp` | Number | `-1` | Applies or references the 'ConstitutionUp' effect/state. |
| `StrengthUp` | Number | `-1` | Applies or references the 'StrengthUp' effect/state. |

</details>

---

### Context: `SupportDieInsteadOfRun`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `alt_dead_ani` | [`Enum/String`](./Enums.md#enum-alt_dead_ani) | `off` |  |
| `alt_dying_ani` | [`Enum/String`](./Enums.md#enum-alt_dying_ani) | `shutdown` |  |

</details>

---

### Context: `SwimmingFormChange`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `form_in` | [`Enum/String`](./Enums.md#enum-form_in) | `Water` |  |
| `form_out` | [`Enum/String`](./Enums.md#enum-form_out) | `Out` |  |

</details>

---

### Context: `SwitchMusic`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `new_layer` | [`Enum/String`](./Enums.md#enum-new_layer) | `event` | The specific audio layer to transition to (e.g., map, battle). |
| `new_song` | [`Enum/String`](./Enums.md#enum-new_song) | `same` | The ID of the new music track. |

</details>

---

### Context: `SwordAndShield_Primed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Holy"` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `DestroyerAttack` |  |

</details>

---

### Context: `TF_TargetAllies`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `TwistingFlames` | The specific ability ID to cast. |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `util_target_allies` |  |

</details>

---

### Context: `TF_TargetEnemies`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `TwistingFlames` | The specific ability ID to cast. |
| `decision_weights` | [`Enum/String`](./Enums.md#enum-decision_weights) | `util_target_enemies` |  |

</details>

---

### Context: `TarFull`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Full` |  |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `SpewerSpit` |  |

</details>

---

### Context: `Terminator2Run`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `move_ability` | [`Enum/String`](./Enums.md#enum-move_ability) | `T2GoopRun` |  |
| `move_weights` | [`Enum/String`](./Enums.md#enum-move_weights) | `stay_far_always_move` |  |

</details>

---

### Context: `TerminatorChase`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `T1ChokeReaction` | The specific ability ID to cast. |
| `move` | [`Enum/String`](./Enums.md#enum-move) | `MoveOne` |  |

</details>

---

### Context: `TerminatorSkin`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `groups` | [`Array`](./Arrays.md#array-groups) | `[ { stacks 48 ParticleBurst Gibs_terminatorskin CatPartsT...` |  |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Brace` | ID of the status effect to apply or check. |

</details>

---

### Context: `UnlimitedDeathRattleRevive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `MD_Lift` | The specific ability ID to cast. |
| `even_if_stunned` | Boolean | `true` |  |

</details>

---

### Context: `UseAbility`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `Destroyer2HolyAttack` | The ID of the ability to trigger. |
| `respect_prime` | Boolean | `true` | If true, respects the ability's prime/cooldown state. |

</details>

---

### Context: `UseAbilityWhenOutOfStatus`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `QueenHippoHeartAttack` | The specific ability ID to cast. |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `Brace` | ID of the status effect to apply or check. |

</details>

---

### Context: `alternate_energized_effect`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `FormChange` | [`Enum/String`](./Enums.md#enum-formchange) | `GuaranteedJackpot` | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| `SpellDamageUp` | Number | `1` | Applies or references the 'SpellDamageUp' effect/state. |

</details>

---

### Context: `passive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `DoNothing` |  |

</details>

---

### Context: `statuses_on_enter_form`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `UseAbility` | [`Enum/String`](./Enums.md#enum-useability) | `KirbySpit` | Logic: Forces execution of an ability. |

</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Leech` | Number | `2` | Applies or references the 'Leech' effect/state. |

</details>

---

### Context: `AddStatusToTrampleDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |

</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | `1` | Applies or references the 'Bleed' effect/state. |

</details>

---

### Context: `AggroTargetIsGovernedByHitEffect`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | `false` |  |

</details>

---

### Context: `Alert`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Alert` |  |

</details>

---

### Context: `Angry`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | String | `"Angry"` |  |

</details>

---

### Context: `BellyFull`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | String | `"Belly"` |  |

</details>

---

### Context: `BigHolding`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"BigHolding"` |  |

</details>

---

### Context: `BigHoldingCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"BigHoldingCat"` |  |

</details>

---

### Context: `Bomb`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Button` |  |

</details>

---

### Context: `Conditional_HasKnockback`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RemoveKnockback` | Number | `1` | Applies or references the 'RemoveKnockback' effect/state. |

</details>

---

### Context: `Conditional_IsPhysicalAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RemoveKnockback` | Number | `1` | Applies or references the 'RemoveKnockback' effect/state. |

</details>

---

### Context: `CreateGlobalModifiers`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `BloodRain` | Number | `1` | Applies or references the 'BloodRain' effect/state. |

</details>

---

### Context: `DiesToPiercingAndSpikes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `deferred` | Boolean | `true` |  |

</details>

---

### Context: `DodgeWhenTargeted`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ability` | [`Enum/String`](./Enums.md#enum-ability) | `ShadowstepDodge` | The specific ability ID to cast. |

</details>

---

### Context: `Drunker`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Drunk` |  |

</details>

---

### Context: `FaceLastDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean | `true` |  |

</details>

---

### Context: `FinalBossSyncAnimations`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `other_character` | [`Enum/String`](./Enums.md#enum-other_character) | `MegaGuppy` |  |

</details>

---

### Context: `Fire`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `SpewerLobbed_Lava` |  |

</details>

---

### Context: `Flop`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Down"` |  |

</details>

---

### Context: `Flop2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Down"` |  |

</details>

---

### Context: `FlushHost`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Host` |  |

</details>

---

### Context: `Grappling`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Grapple` |  |

</details>

---

### Context: `Guarding`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | String | `"Guarding"` |  |

</details>

---

### Context: `Headless`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Headless"` |  |

</details>

---

### Context: `Hint_CrackedVisuals`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Cracked"` |  |

</details>

---

### Context: `Hint_CrackedVisuals2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"ChargingCracked"` |  |

</details>

---

### Context: `Hint_CrackedVisuals3`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"SwallowedCracked"` |  |

</details>

---

### Context: `Holding`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | String | `"Holding"` |  |

</details>

---

### Context: `Insane_Ceiling`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Insane"` |  |

</details>

---

### Context: `Insane_Ground`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Insane"` |  |

</details>

---

### Context: `JohnnyHost`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Host` |  |

</details>

---

### Context: `Joystick`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Joystick"` |  |

</details>

---

### Context: `Lit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Lit` |  |

</details>

---

### Context: `MotherGrowController`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tumor_object` | [`Enum/String`](./Enums.md#enum-tumor_object) | `MotherTumor` |  |

</details>

---

### Context: `Mounted`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Cat"` |  |

</details>

---

### Context: `MouthFull`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | String | `"MouthFull"` |  |

</details>

---

### Context: `MoveAfterAnyAttemptedAttack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `weights` | [`Enum/String`](./Enums.md#enum-weights) | `bat_chaos_runaway` |  |

</details>

---

### Context: `MoveAwayFromDamageSource`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `move_ability` | [`Enum/String`](./Enums.md#enum-move_ability) | `BirdFly` |  |

</details>

---

### Context: `NoEyes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"0"` |  |

</details>

---

### Context: `NoStick`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `ManglerJab` |  |

</details>

---

### Context: `Nothing`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `spawn` |  |

</details>

---

### Context: `Off`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `Off` |  |

</details>

---

### Context: `OneEye`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"1"` |  |

</details>

---

### Context: `OpenCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | [`Enum/String`](./Enums.md#enum-animation_suffix) | `OpenCat` |  |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Fire` | Specific element type required or applied. |

</details>

---

### Context: `Possessing`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Possessing"` |  |

</details>

---

### Context: `SharePickups`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `include_coins` | Boolean | `true` |  |

</details>

---

### Context: `SmallHolding`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"Holding"` |  |

</details>

---

### Context: `SmallHoldingCat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String | `"HoldingCat"` |  |

</details>

---

### Context: `StacyMutant_Brace`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | `3` | Applies or references the 'Brace' effect/state. |

</details>

---

### Context: `StacyMutant_Counter`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `CounterAttack` | [`Enum/String`](./Enums.md#enum-counterattack) | `SM_BleedCounter` | Reaction: Executes a counter-attack ability when hit. |

</details>

---

### Context: `StacyMutant_DoubleHead`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ExtraDispersedTurns` | Number | `1` | Applies or references the 'ExtraDispersedTurns' effect/state. |

</details>

---

### Context: `StacyMutant_Holy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `DivineShield` | Number | `7` | Applies or references the 'DivineShield' effect/state. |

</details>

---

### Context: `StacyMutant_Mirror`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ReflectProjectiles` | Number | `100%` | Passive: Reflects incoming projectiles back at the attacker. |

</details>

---

### Context: `StacyMutant_Thorns`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Thorns` | Number | `3` | Applies or references the 'Thorns' effect/state. |

</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | `1` | Fires a randomized number of magic missiles. |

</details>

---

### Context: `StatusEachTurnEndIfEnabledAtStartOfTurn`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ForceUseAbility` | [`Enum/String`](./Enums.md#enum-forceuseability) | `T2UnClone` | Logic: Forces the execution of a specific ability. |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `SpeedUp_WithoutInitiative` | Number | `1` | Applies or references the 'SpeedUp_WithoutInitiative' effect/state. |

</details>

---

### Context: `StatusOnEnemyConfused`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `ImmediateUseAbility` | [`Enum/String`](./Enums.md#enum-immediateuseability) | `FuzzerReact` | Applies or references the 'ImmediateUseAbility' effect/state. |

</details>

---

### Context: `StatusOverlappingCharactersAndDie`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Poison` | Number | `1` | Applies or references the 'Poison' effect/state. |

</details>

---

### Context: `StatusWhenStatusCompletelyRemoved`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `status` | [`Enum/String`](./Enums.md#enum-status) | `BackflipWhenTargeted` | ID of the status effect to apply or check. |

</details>

---

### Context: `StunImmunity`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean | `false` |  |

</details>

---

### Context: `SwordAndShield`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `DestroyerAttack` |  |

</details>

---

### Context: `SyncFormsWithBuddy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `no_buddy` | [`Enum/String`](./Enums.md#enum-no_buddy) | `Rage` |  |

</details>

---

### Context: `Tar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `attack` | [`Enum/String`](./Enums.md#enum-attack) | `SpewerLobbed_Tar` |  |

</details>

---

### Context: `ThrobHost`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Host` |  |

</details>

---

### Context: `Unlit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Unlit` |  |

</details>

---

### Context: `Unwashed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | [`Enum/String`](./Enums.md#enum-partial_animation_suffix) | `Unwashed` |  |

</details>

---

### Context: `Water`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | String | `"Water"` |  |

</details>

---

### Context: `additional_statuses`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `PermanentMadness` | Number | `1` | Applies or references the 'PermanentMadness' effect/state. |

</details>

---

### Context: `exit_animations`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Default` | [`Enum/String`](./Enums.md#enum-default) | `release` | Character Form: The baseline default behavior state. |

</details>

---

### Context: `round_start_bonusturn_pattern`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `do_priority` | [`Array`](./Arrays.md#array-do_priority) | `[ MutateAOE SpawnMaggots ]` |  |

</details>

---

### Context: `0`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `AddStatusToReceivedDamage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `AdventureTokenPassivePool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `AllAlive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Attacker`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `BirdRewards`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Bully`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Close`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Damaged`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Default_Ceiling`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Default_Ground`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `DesireMech`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Die`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Dumb`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Else`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Flush`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `FlushBubs`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `FlushNettle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `GuaranteedJackpot`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Johnny`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `JohnnyBubs`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `JohnnyNettle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `LastHit`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `MotherTumorSpawnInCapture`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `NeutronStar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `NotPriming`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Obey`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `OffMap`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `OffScreen`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `OneAlive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Out`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `PassiveWhenDead`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Priming`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Rain`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `RandomPassivePool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Robot`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `SpawningPhase`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Start_Ceiling`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Stop`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `TempPassiveUntilSettled`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Throb`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ThrobBubs`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ThrobNettle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Transformed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `TwoAlive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `TwoEyes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `Washed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `active`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `damage_instance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `default`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `virtual_abilities`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

