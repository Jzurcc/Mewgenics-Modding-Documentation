# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Characters & Bosses

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/600) |
| :--- | :--- | :--- | :--- |
| [`properties`](./Characters_and_Bosses.md#context-properties) | Block | General engine properties. | 600 |
| [`graphics`](./Characters_and_Bosses.md#context-graphics) | Block | Visual parameters and animation bindings. | 558 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 544 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 460 |
| [`abilities`](./Characters_and_Bosses.md#context-abilities) | Block | Lists the ability IDs the character possesses. | 458 |
| [`stats`](./Characters_and_Bosses.md#context-stats) | Block | Core character metrics (Health, Strength, etc.). | 388 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum/String |  | 240 |
| [`sound`](./Characters_and_Bosses.md#context-sound) | Block | Audio bindings. | 62 |
| [`equipment`](./Characters_and_Bosses.md#context-equipment) | Block | List of item IDs the character spawns equipped with. | 44 |
| [`alt_spawn_pool`](./Characters_and_Bosses.md#context-alt_spawn_pool) | Block | Alternative pools to draw minions from. | 18 |
| [`ai_if_spawned_as_enemy`](./Characters_and_Bosses.md#context-ai_if_spawned_as_enemy) | Block | AI logic override used only if the character is spawned as an enemy. | 1 |
| [`damage_instance`](./Characters_and_Bosses.md#context-damage_instance) | Block | Defines damage logic on contact. | 1 |
| [`scale`](./Enums.md#enum-scale) | Enum/String |  | 1 |

</details>

---

### Context: `ai`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`0`](./Characters_and_Bosses.md#context-0), [`1`](./Characters_and_Bosses.md#context-1), [`2`](./Characters_and_Bosses.md#context-2), [`3`](./Characters_and_Bosses.md#context-3), [`4`](./Characters_and_Bosses.md#context-4), [`Alert`](./Characters_and_Bosses.md#context-alert), [`Angry`](./Characters_and_Bosses.md#context-angry), [`Attacker`](./Characters_and_Bosses.md#context-attacker), [`BellyFull`](./Characters_and_Bosses.md#context-bellyfull), [`Bishop`](./Characters_and_Bosses.md#context-bishop), [`BlackHole`](./Characters_and_Bosses.md#context-blackhole), [`Bully`](./Characters_and_Bosses.md#context-bully), [`CaveBaby`](./Characters_and_Bosses.md#context-cavebaby), [`CaveMan`](./Characters_and_Bosses.md#context-caveman), [`CaveManSpear`](./Characters_and_Bosses.md#context-cavemanspear), [`CaveWoman`](./Characters_and_Bosses.md#context-cavewoman), [`CaveWomanHasCat`](./Characters_and_Bosses.md#context-cavewomanhascat), [`Charging`](./Characters_and_Bosses.md#context-charging), [`Cultist`](./Characters_and_Bosses.md#context-cultist), [`Damaged`](./Characters_and_Bosses.md#context-damaged), [`Default`](./Characters_and_Bosses.md#context-default), [`Default_Ceiling`](./Characters_and_Bosses.md#context-default_ceiling), [`Default_Ground`](./Characters_and_Bosses.md#context-default_ground), [`DesireMech`](./Characters_and_Bosses.md#context-desiremech), [`Down`](./Characters_and_Bosses.md#context-down), [`DualSword`](./Characters_and_Bosses.md#context-dualsword), [`DualSword_Primed`](./Characters_and_Bosses.md#context-dualsword_primed), [`Explody`](./Characters_and_Bosses.md#context-explody), [`FightPhase`](./Characters_and_Bosses.md#context-fightphase), [`Fire`](./Characters_and_Bosses.md#context-fire), [`FireFull`](./Characters_and_Bosses.md#context-firefull), [`Flop`](./Characters_and_Bosses.md#context-flop), [`Flop2`](./Characters_and_Bosses.md#context-flop2), [`Flush`](./Characters_and_Bosses.md#context-flush), [`FlushBubs`](./Characters_and_Bosses.md#context-flushbubs), [`FlushHost`](./Characters_and_Bosses.md#context-flushhost), [`FlushNettle`](./Characters_and_Bosses.md#context-flushnettle), [`Full`](./Characters_and_Bosses.md#context-full), [`Grown`](./Characters_and_Bosses.md#context-grown), [`Guarding`](./Characters_and_Bosses.md#context-guarding), [`HalfDead`](./Characters_and_Bosses.md#context-halfdead), [`HasCat`](./Characters_and_Bosses.md#context-hascat), [`HasDeadCat`](./Characters_and_Bosses.md#context-hasdeadcat), [`HasRock`](./Characters_and_Bosses.md#context-hasrock), [`Headless`](./Characters_and_Bosses.md#context-headless), [`Holding`](./Characters_and_Bosses.md#context-holding), [`InitialPhase`](./Characters_and_Bosses.md#context-initialphase), [`Insane_Ceiling`](./Characters_and_Bosses.md#context-insane_ceiling), [`Insane_Ground`](./Characters_and_Bosses.md#context-insane_ground), [`Johnny`](./Characters_and_Bosses.md#context-johnny), [`JohnnyBubs`](./Characters_and_Bosses.md#context-johnnybubs), [`JohnnyHost`](./Characters_and_Bosses.md#context-johnnyhost), [`JohnnyNettle`](./Characters_and_Bosses.md#context-johnnynettle), [`MouthFull`](./Characters_and_Bosses.md#context-mouthfull), [`Mutant`](./Characters_and_Bosses.md#context-mutant), [`NeutronStar`](./Characters_and_Bosses.md#context-neutronstar), [`NoStick`](./Characters_and_Bosses.md#context-nostick), [`Normal`](./Characters_and_Bosses.md#context-normal), [`NormalFull`](./Characters_and_Bosses.md#context-normalfull), [`Nuke`](./Characters_and_Bosses.md#context-nuke), [`OffMap`](./Characters_and_Bosses.md#context-offmap), [`Open`](./Characters_and_Bosses.md#context-open), [`Primed`](./Characters_and_Bosses.md#context-primed), [`ROOT`](./Characters_and_Bosses.md#context-root), [`Rage`](./Characters_and_Bosses.md#context-rage), [`Rain`](./Characters_and_Bosses.md#context-rain), [`Sitting`](./Characters_and_Bosses.md#context-sitting), [`SquirrelForm`](./Characters_and_Bosses.md#context-squirrelform), [`Standing`](./Characters_and_Bosses.md#context-standing), [`Standing2`](./Characters_and_Bosses.md#context-standing2), [`SwordAndShield`](./Characters_and_Bosses.md#context-swordandshield), [`SwordAndShield_Primed`](./Characters_and_Bosses.md#context-swordandshield_primed), [`Tar`](./Characters_and_Bosses.md#context-tar), [`TarFull`](./Characters_and_Bosses.md#context-tarfull), [`Throb`](./Characters_and_Bosses.md#context-throb), [`ThrobBubs`](./Characters_and_Bosses.md#context-throbbubs), [`ThrobHost`](./Characters_and_Bosses.md#context-throbhost), [`ThrobNettle`](./Characters_and_Bosses.md#context-throbnettle), [`Transformed`](./Characters_and_Bosses.md#context-transformed), [`Turtled`](./Characters_and_Bosses.md#context-turtled), [`Unwashed`](./Characters_and_Bosses.md#context-unwashed), [`Up`](./Characters_and_Bosses.md#context-up), [`Washed`](./Characters_and_Bosses.md#context-washed), [`Washer`](./Characters_and_Bosses.md#context-washer), [`WereMan`](./Characters_and_Bosses.md#context-wereman), [`Zealot`](./Characters_and_Bosses.md#context-zealot), [`ZealotBomb`](./Characters_and_Bosses.md#context-zealotbomb)

| Property Key | Type | Definition | Count (X/578) |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum/String |  | 578 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum/String |  | 498 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 495 |
| [`pattern`](./Characters_and_Bosses.md#context-pattern) | Block | AI sequence logic. | 292 |
| [`mainturn_pattern`](./Characters_and_Bosses.md#context-mainturn_pattern) | Block | AI Logic: Determines standard ability usage during the main turn. | 44 |
| `end_turn_on_formswitch` | Boolean |  | 41 |
| [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities) | Block | Abilities that are evaluated but not directly castable by the player. | 35 |
| `auto_orient` | Boolean |  | 31 |
| `reset_pattern_on_formswitch` | Boolean |  | 31 |
| `stun_advances_pattern` | Boolean |  | 30 |
| `fallback_advances_pattern` | Boolean |  | 28 |
| [`bonusturn_pattern`](./Characters_and_Bosses.md#context-bonusturn_pattern) | Block | AI Logic: Determines ability usage during bonus turns. | 27 |
| [`fallback`](./Characters_and_Bosses.md#context-fallback) | Block | Logic executed if primary options fail. | 23 |
| `consider_spells` | Boolean |  | 12 |
| [`round_end_bonusturn_pattern`](./Characters_and_Bosses.md#context-round_end_bonusturn_pattern) | Block | AI Logic: Ability usage pattern during round-end bonus turns. | 12 |
| `animate_choice` | Boolean |  | 8 |
| `clamp_pattern` | Boolean |  | 5 |
| `randomize_pattern_start` | Boolean |  | 3 |
| [`dispersed_bonusturn_pattern`](./Characters_and_Bosses.md#context-dispersed_bonusturn_pattern) | Block | AI Logic: Alternative bonus turn ability pattern. | 2 |
| `random_orient` | Boolean |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`dice_abilities`](./Arrays.md#array-dice_abilities) | Array |  | 1 |
| `never_hit_ally_corpses` | Boolean |  | 1 |
| [`post_absorb_move_weights`](./Enums.md#enum-post_absorb_move_weights) | Enum/String |  | 1 |
| `reset_pattern_on_round_begin` | Boolean |  | 1 |
| [`roll_ability`](./Enums.md#enum-roll_ability) | Enum/String |  | 1 |
| [`round_start_bonusturn_pattern`](./Characters_and_Bosses.md#context-round_start_bonusturn_pattern) | Block | AI Logic: Ability usage pattern during round-start bonus turns. | 1 |

</details>

---

### Context: `graphics`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count (X/517) |
| :--- | :--- | :--- | :--- |
| `name` | String | Localization key for the character's name. | 517 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum/String |  | 461 |
| `tooltip` | String |  | 409 |
| [`shadow_size`](./Enums.md#enum-shadow_size) | Enum/String |  | 151 |
| [`scale`](./Enums.md#enum-scale) | Enum/String |  | 149 |
| `uifloaters_offset` | Number |  | 149 |
| [`custom_cat_data`](./Enums.md#enum-custom_cat_data) | Enum/String |  | 127 |
| [`water_mask`](./Enums.md#enum-water_mask) | Enum/String |  | 83 |
| [`spawnin_animation`](./Enums.md#enum-spawnin_animation) | Enum/String |  | 37 |
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array |  | 33 |
| `piece_alt_frame` | Number |  | 27 |
| [`shadow`](./Enums.md#enum-shadow) | Enum/String |  | 23 |
| `move_speed_sync_frames` | Number |  | 20 |
| `no_splatter` | Boolean |  | 17 |
| [`projectile_spawn_offset`](./Arrays.md#array-projectile_spawn_offset) | Array |  | 17 |
| [`tint`](./Arrays.md#array-tint) | Array |  | 17 |
| [`move_speed_multiplier`](./Enums.md#enum-move_speed_multiplier) | Enum/String |  | 16 |
| `dont_sink` | Boolean |  | 14 |
| `art_flip` | Number |  | 7 |
| [`depth_offset`](./Enums.md#enum-depth_offset) | Enum/String |  | 6 |
| [`walk`](./Enums.md#enum-walk) | Enum/String |  | 5 |
| [`dead`](./Enums.md#enum-dead) | Enum/String |  | 4 |
| [`dying`](./Enums.md#enum-dying) | Enum/String |  | 4 |
| `four_way_animations` | Boolean |  | 4 |
| [`hit`](./Enums.md#enum-hit) | Enum/String |  | 4 |
| [`stunned`](./Enums.md#enum-stunned) | Enum/String |  | 4 |
| [`weak`](./Enums.md#enum-weak) | Enum/String |  | 4 |
| [`deadhit`](./Enums.md#enum-deadhit) | Enum/String |  | 3 |
| `show_infinity_damage_warning` | Boolean |  | 3 |
| `always_huge_mask` | Boolean |  | 2 |
| [`default_attack_animation`](./Enums.md#enum-default_attack_animation) | Enum/String |  | 2 |
| [`desc`](./Enums.md#enum-desc) | Enum/String | Localization key for the character's desc. | 2 |
| `shade_occluded_objects` | Boolean |  | 2 |
| [`dodge`](./Enums.md#enum-dodge) | Enum/String |  | 1 |
| `no_horizontal_flip` | Boolean |  | 1 |
| [`non_blocking_animations`](./Arrays.md#array-non_blocking_animations) | Array |  | 1 |
| [`override_portrait`](./Enums.md#enum-override_portrait) | Enum/String |  | 1 |
| `randomize_starting_frame` | Boolean |  | 1 |
| `status_display_count_max` | Number |  | 1 |

</details>

---

### Context: `properties`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count (X/505) |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum/String |  | 505 |
| `health` | Number |  | 427 |
| [`tag`](./Arrays.md#array-tag) | Array | Specific entity tag required. | 399 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification/category type. | 280 |
| `movement` | Number |  | 278 |
| [`corpse_health`](./Enums.md#enum-corpse_health) | Enum/String |  | 195 |
| `inherit_faction` | Boolean |  | 115 |
| `dispersed_bonus_turns` | Number |  | 104 |
| `base_mana_regen` | Number |  | 90 |
| [`size`](./Enums.md#enum-size) | Enum/String |  | 80 |
| `shield` | Number |  | 74 |
| [`move_block`](./Enums.md#enum-move_block) | Enum/String |  | 73 |
| `kill_required` | Boolean |  | 69 |
| `can_be_backstabbed` | Boolean |  | 68 |
| `initiative` | Number |  | 61 |
| `takes_turns` | Boolean |  | 61 |
| `mana_regen` | Number |  | 51 |
| `mana` | Number | Base maximum mana pool. | 50 |
| `flying` | Boolean |  | 47 |
| [`banned_elite_buffs`](./Arrays.md#array-banned_elite_buffs) | Array |  | 45 |
| [`hidden_tag`](./Enums.md#enum-hidden_tag) | Enum/String |  | 38 |
| `weak_threshold` | Number |  | 32 |
| `knockback_immune` | Boolean |  | 25 |
| `can_be_champion` | Boolean |  | 20 |
| [`lock_orientation`](./Arrays.md#array-lock_orientation) | Array |  | 19 |
| [`ai_scale`](./Enums.md#enum-ai_scale) | Enum/String |  | 18 |
| [`layer`](./Enums.md#enum-layer) | Enum/String |  | 17 |
| [`auto_run_priority`](./Enums.md#enum-auto_run_priority) | Enum/String |  | 16 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 16 |
| `inanimate` | Boolean |  | 16 |
| `disperse_main_turns` | Boolean |  | 15 |
| [`hidden_tags`](./Enums.md#enum-hidden_tags) | Enum/String |  | 14 |
| [`tags`](./Arrays.md#array-tags) | Array |  | 14 |
| `evenly_dispersed_bonus_turns` | Number |  | 13 |
| `exclude_from_hallucinate` | Boolean |  | 13 |
| `round_end_bonus_turns` | Number |  | 13 |
| `can_be_overkilled` | Boolean |  | 12 |
| `can_collect_coins` | Boolean |  | 10 |
| `deathpoof_size` | Number |  | 10 |
| `dispersed_bonus_turns_consider_initiative` | Boolean |  | 10 |
| [`held_coins`](./Arrays.md#array-held_coins) | Array |  | 10 |
| `initial_health` | Number |  | 10 |
| `can_eat_food` | Boolean |  | 9 |
| `can_grant_extra_turns` | Boolean |  | 8 |
| `tall` | Boolean |  | 8 |
| `dispersed_bonus_turns_before_cats` | Boolean |  | 7 |
| `divine_shield` | Number |  | 7 |
| `is_player_cat` | Boolean |  | 7 |
| `boss_minions_runaway` | Boolean |  | 6 |
| `mana_matters` | Boolean |  | 6 |
| `access_to_player_inventory` | Boolean |  | 5 |
| `act_points` | Number |  | 5 |
| `takes_main_turn` | Boolean |  | 5 |
| `visually_spiky` | Boolean |  | 5 |
| `allow_passive_spelltransforming` | Boolean |  | 4 |
| `base_crit_chance` | Number |  | 4 |
| `last_turn_is_main_turn` | Boolean |  | 4 |
| `round_start_bonus_turns` | Number |  | 4 |
| `view_bleeding_characters_as_enemies` | Boolean |  | 4 |
| [`aoe_pierce_mode`](./Enums.md#enum-aoe_pierce_mode) | Enum/String |  | 3 |
| `base_initiative` | Number |  | 3 |
| `base_movement` | Number |  | 3 |
| `catdata_ignore_skills` | Boolean |  | 3 |
| [`disallow_items`](./Enums.md#enum-disallow_items) | Enum/String |  | 3 |
| `always_triggers_traps` | Boolean |  | 2 |
| `base_health` | Number |  | 2 |
| `base_health_regen` | Number |  | 2 |
| `base_initial_mana` | Number |  | 2 |
| `base_mana` | Number |  | 2 |
| `blocking` | Boolean |  | 2 |
| `can_be_elite` | Boolean |  | 2 |
| `can_run` | Boolean |  | 2 |
| `champion` | Boolean |  | 2 |
| `force_not_familiar` | Boolean |  | 2 |
| `hint_no_corpse` | Boolean |  | 2 |
| `must_start_facing_camera` | Boolean |  | 2 |
| `tile_desire_cost` | Number |  | 2 |
| `uncapturable` | Boolean |  | 2 |
| `aggro_target_is_enemy` | Boolean |  | 1 |
| `allow_flying_effect` | Boolean |  | 1 |
| `allow_offmap_corpse` | Boolean |  | 1 |
| `allow_replacebrain` | Boolean |  | 1 |
| `always_face_forward` | Boolean |  | 1 |
| `capture_as_cat` | Boolean |  | 1 |
| `elite` | Boolean |  | 1 |
| `first_turn_is_main_turn` | Boolean |  | 1 |
| `ignore_mouseover` | Boolean |  | 1 |
| `ignore_tiles` | Boolean |  | 1 |
| [`inanimate_can_receive_specific_statuses`](./Arrays.md#array-inanimate_can_receive_specific_statuses) | Array |  | 1 |
| `mouseover_priority` | Number |  | 1 |
| `move_points` | Number |  | 1 |
| `pickup_type` | Number |  | 1 |
| `scale` | Number |  | 1 |
| `speculative_inanimate` | Boolean |  | 1 |
| `static` | Boolean |  | 1 |
| `two_fronts` | Boolean |  | 1 |
| `two_fronts_switch` | Boolean |  | 1 |
| `view_bugs_as_enemies` | Boolean |  | 1 |

</details>

---

### Context: `abilities`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count (X/436) |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 436 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 433 |
| [`spells`](./Arrays.md#array-spells) | Array |  | 381 |
| `can_get_bonus` | Boolean |  | 30 |

</details>

---

### Context: `stats`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count (X/386) |
| :--- | :--- | :--- | :--- |
| `strength` | Number |  | 386 |
| `constitution` | Number |  | 380 |
| `dexterity` | Number |  | 380 |
| `charisma` | Number |  | 379 |
| `intelligence` | Number |  | 379 |
| `speed` | Number | Base speed/initiative stat. | 379 |
| `luck` | Number |  | 160 |

</details>

---

### Context: `pattern`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ReplaceBrain`](./Characters_and_Bosses.md#context-replacebrain), [`ai`](./Characters_and_Bosses.md#context-ai), [`ai_if_spawned_as_enemy`](./Characters_and_Bosses.md#context-ai_if_spawned_as_enemy)

| Property Key | Type | Definition | Count (X/128) |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum/String |  | 128 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 106 |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 101 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum/String |  | 11 |
| [`do_random`](./Arrays.md#array-do_random) | Array |  | 10 |
| [`do_strict`](./Arrays.md#array-do_strict) | Array |  | 6 |
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array |  | 3 |
| [`move_then_do_priority`](./Arrays.md#array-move_then_do_priority) | Array |  | 3 |
| [`move_then_do_random`](./Arrays.md#array-move_then_do_random) | Array |  | 3 |
| [`do_all_shuffle`](./Arrays.md#array-do_all_shuffle) | Array |  | 2 |
| [`do_best`](./Arrays.md#array-do_best) | Array |  | 1 |
| [`do_best_multiple`](./Arrays.md#array-do_best_multiple) | Array |  | 1 |
| [`do_priority_alternating`](./Arrays.md#array-do_priority_alternating) | Array |  | 1 |
| [`move_then_do_all`](./Arrays.md#array-move_then_do_all) | Array |  | 1 |

</details>

---

### Context: `passives`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Characters_and_Bosses.md#context-1), [`2`](./Characters_and_Bosses.md#context-2), [`3`](./Characters_and_Bosses.md#context-3), [`4`](./Characters_and_Bosses.md#context-4), [`5`](./Characters_and_Bosses.md#context-5), [`Alert`](./Characters_and_Bosses.md#context-alert), [`AllAlive`](./Characters_and_Bosses.md#context-allalive), [`BellyFull`](./Characters_and_Bosses.md#context-bellyfull), [`Big`](./Characters_and_Bosses.md#context-big), [`BigHolding`](./Characters_and_Bosses.md#context-bigholding), [`BigHoldingCat`](./Characters_and_Bosses.md#context-bigholdingcat), [`Bishop`](./Characters_and_Bosses.md#context-bishop), [`BlackHole`](./Characters_and_Bosses.md#context-blackhole), [`Bomb`](./Characters_and_Bosses.md#context-bomb), [`Boris`](./Characters_and_Bosses.md#context-boris), [`Bully`](./Characters_and_Bosses.md#context-bully), [`CaveBaby`](./Characters_and_Bosses.md#context-cavebaby), [`CaveMan`](./Characters_and_Bosses.md#context-caveman), [`CaveManSpear`](./Characters_and_Bosses.md#context-cavemanspear), [`CaveWoman`](./Characters_and_Bosses.md#context-cavewoman), [`CaveWomanHasCat`](./Characters_and_Bosses.md#context-cavewomanhascat), [`Charging`](./Characters_and_Bosses.md#context-charging), [`Close`](./Characters_and_Bosses.md#context-close), [`Cultist`](./Characters_and_Bosses.md#context-cultist), [`Default`](./Characters_and_Bosses.md#context-default), [`Default_Ceiling`](./Characters_and_Bosses.md#context-default_ceiling), [`Default_Ground`](./Characters_and_Bosses.md#context-default_ground), [`Die`](./Characters_and_Bosses.md#context-die), [`Down`](./Characters_and_Bosses.md#context-down), [`DualSword`](./Characters_and_Bosses.md#context-dualsword), [`DualSword_Primed`](./Characters_and_Bosses.md#context-dualsword_primed), [`Dumb`](./Characters_and_Bosses.md#context-dumb), [`Explody`](./Characters_and_Bosses.md#context-explody), [`Explosive`](./Characters_and_Bosses.md#context-explosive), [`FightPhase`](./Characters_and_Bosses.md#context-fightphase), [`Fire`](./Characters_and_Bosses.md#context-fire), [`FireFull`](./Characters_and_Bosses.md#context-firefull), [`Flop`](./Characters_and_Bosses.md#context-flop), [`Flop2`](./Characters_and_Bosses.md#context-flop2), [`FlushBubs`](./Characters_and_Bosses.md#context-flushbubs), [`FlushHost`](./Characters_and_Bosses.md#context-flushhost), [`FlushNettle`](./Characters_and_Bosses.md#context-flushnettle), [`Full`](./Characters_and_Bosses.md#context-full), [`Grown`](./Characters_and_Bosses.md#context-grown), [`GuaranteedJackpot`](./Characters_and_Bosses.md#context-guaranteedjackpot), [`Guarding`](./Characters_and_Bosses.md#context-guarding), [`HalfDead`](./Characters_and_Bosses.md#context-halfdead), [`HasCat`](./Characters_and_Bosses.md#context-hascat), [`HasDeadCat`](./Characters_and_Bosses.md#context-hasdeadcat), [`Headless`](./Characters_and_Bosses.md#context-headless), [`Holding`](./Characters_and_Bosses.md#context-holding), [`Holy`](./Characters_and_Bosses.md#context-holy), [`InitialPhase`](./Characters_and_Bosses.md#context-initialphase), [`Insane_Ceiling`](./Characters_and_Bosses.md#context-insane_ceiling), [`Insane_Ground`](./Characters_and_Bosses.md#context-insane_ground), [`JohnnyBubs`](./Characters_and_Bosses.md#context-johnnybubs), [`JohnnyHost`](./Characters_and_Bosses.md#context-johnnyhost), [`JohnnyNettle`](./Characters_and_Bosses.md#context-johnnynettle), [`Joystick`](./Characters_and_Bosses.md#context-joystick), [`Lifted`](./Characters_and_Bosses.md#context-lifted), [`Lit`](./Characters_and_Bosses.md#context-lit), [`MouthFull`](./Characters_and_Bosses.md#context-mouthfull), [`Mutant`](./Characters_and_Bosses.md#context-mutant), [`NeutronStar`](./Characters_and_Bosses.md#context-neutronstar), [`Normal`](./Characters_and_Bosses.md#context-normal), [`NormalFull`](./Characters_and_Bosses.md#context-normalfull), [`NotPriming`](./Characters_and_Bosses.md#context-notpriming), [`Nuke`](./Characters_and_Bosses.md#context-nuke), [`Obey`](./Characters_and_Bosses.md#context-obey), [`OffScreen`](./Characters_and_Bosses.md#context-offscreen), [`OneAlive`](./Characters_and_Bosses.md#context-onealive), [`OneEye`](./Characters_and_Bosses.md#context-oneeye), [`Open`](./Characters_and_Bosses.md#context-open), [`OpenCat`](./Characters_and_Bosses.md#context-opencat), [`Out`](./Characters_and_Bosses.md#context-out), [`PassiveWhenAffectedByElement`](./Characters_and_Bosses.md#context-passivewhenaffectedbyelement), [`PassiveWhileHasStatus`](./Characters_and_Bosses.md#context-passivewhilehasstatus), [`PassiveWhileNotHasStatus`](./Characters_and_Bosses.md#context-passivewhilenothasstatus), [`Possessing`](./Characters_and_Bosses.md#context-possessing), [`Primed`](./Characters_and_Bosses.md#context-primed), [`Priming`](./Characters_and_Bosses.md#context-priming), [`Pulp2`](./Characters_and_Bosses.md#context-pulp2), [`Pulp3`](./Characters_and_Bosses.md#context-pulp3), [`Pulp4`](./Characters_and_Bosses.md#context-pulp4), [`Pulp5`](./Characters_and_Bosses.md#context-pulp5), [`Pulp6`](./Characters_and_Bosses.md#context-pulp6), [`Pulp7`](./Characters_and_Bosses.md#context-pulp7), [`ROOT`](./Characters_and_Bosses.md#context-root), [`Rage`](./Characters_and_Bosses.md#context-rage), [`Sitting`](./Characters_and_Bosses.md#context-sitting), [`SmallHolding`](./Characters_and_Bosses.md#context-smallholding), [`SmallHoldingCat`](./Characters_and_Bosses.md#context-smallholdingcat), [`SpawningPhase`](./Characters_and_Bosses.md#context-spawningphase), [`SquirrelForm`](./Characters_and_Bosses.md#context-squirrelform), [`Standing`](./Characters_and_Bosses.md#context-standing), [`Standing2`](./Characters_and_Bosses.md#context-standing2), [`Start_Ceiling`](./Characters_and_Bosses.md#context-start_ceiling), [`Stop`](./Characters_and_Bosses.md#context-stop), [`SwordAndShield`](./Characters_and_Bosses.md#context-swordandshield), [`SwordAndShield_Primed`](./Characters_and_Bosses.md#context-swordandshield_primed), [`Tar`](./Characters_and_Bosses.md#context-tar), [`TarFull`](./Characters_and_Bosses.md#context-tarfull), [`ThrobBubs`](./Characters_and_Bosses.md#context-throbbubs), [`ThrobHost`](./Characters_and_Bosses.md#context-throbhost), [`ThrobNettle`](./Characters_and_Bosses.md#context-throbnettle), [`Transformed`](./Characters_and_Bosses.md#context-transformed), [`Turtled`](./Characters_and_Bosses.md#context-turtled), [`TwoAlive`](./Characters_and_Bosses.md#context-twoalive), [`TwoEyes`](./Characters_and_Bosses.md#context-twoeyes), [`Unlit`](./Characters_and_Bosses.md#context-unlit), [`Up`](./Characters_and_Bosses.md#context-up), [`Washed`](./Characters_and_Bosses.md#context-washed), [`Washer`](./Characters_and_Bosses.md#context-washer), [`Water`](./Characters_and_Bosses.md#context-water), [`WereMan`](./Characters_and_Bosses.md#context-wereman), [`Zealot`](./Characters_and_Bosses.md#context-zealot), [`ZealotBomb`](./Characters_and_Bosses.md#context-zealotbomb), [`active`](./Characters_and_Bosses.md#context-active), [`default`](./Characters_and_Bosses.md#context-default), [`hot`](./Characters_and_Bosses.md#context-hot)

| Property Key | Type | Definition | Count (X/106) |
| :--- | :--- | :--- | :--- |
| [`FormChanger`](./Characters_and_Bosses.md#context-formchanger) | Block | AI Role: Designates the character as one that frequently shifts forms. | 106 |
| [`SpawnOnDeath`](./Enums.md#enum-spawnondeath) | Enum/String | Event Trigger: Spawns a specific entity when killed. | 79 |
| `Trample` | Number | Applies or references the 'Trample' effect/state. | 76 |
| `Robot` | Number | Character Form: Behavior and stats for the 'Robot' state. | 46 |
| `Brace` | Number | Applies or references the 'Brace' effect/state. | 38 |
| [`FormChangeWhileHasStatus`](./Characters_and_Bosses.md#context-formchangewhilehasstatus) | Block | Logic: Changes form automatically while possessing a specific status. | 35 |
| [`CounterAttack`](./Enums.md#enum-counterattack) | Enum/String | Reaction: Executes a counter-attack ability when hit. | 30 |
| [`DeathRattle`](./Enums.md#enum-deathrattle) | Enum/String | Event Trigger: Executes logic or abilities exactly when the character dies. | 29 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum/String | Applies or references the 'ElementImmune' effect/state. | 27 |
| [`ImmediateAbilityReaction`](./Enums.md#enum-immediateabilityreaction) | Enum/String | Reaction: Executes an ability instantly, interrupting the current sequence. | 26 |
| `Undead` | Number | Applies or references the 'Undead' effect/state. | 24 |
| [`AddStatusToBasicAttack`](./Characters_and_Bosses.md#context-addstatustobasicattack) | Block | Modifier: Injects a status effect payload into the character's basic attacks. | 21 |
| [`BossRewards`](./Characters_and_Bosses.md#context-bossrewards) | Block | Loot logic: Rewards dropped upon defeating a boss. | 20 |
| [`AbilityReaction`](./Enums.md#enum-abilityreaction) | Enum/String | AI Trigger: Executes an ability in reaction to a specific event (e.g., taking damage). | 19 |
| [`StatusImmunity`](./Enums.md#enum-statusimmunity) | Enum/String | Applies or references the 'StatusImmunity' effect/state. | 19 |
| [`BirdRewards`](./Characters_and_Bosses.md#context-birdrewards) | Block | Loot logic: Rewards dropped by bird-type enemies. | 18 |
| [`Buddy`](./Enums.md#enum-buddy) | Enum/String | Character Form / AI State: Behavior and stats for the 'Buddy' familiar state. | 17 |
| [`MeleeRevengeDamage`](./Characters_and_Bosses.md#context-meleerevengedamage) | Block | Reaction: Deals damage or status effects to an attacker upon receiving melee damage. | 17 |
| `AddMovement` | Number | Applies or references the 'AddMovement' effect/state. | 16 |
| [`CharacterLightSource`](./Characters_and_Bosses.md#context-characterlightsource) | Block | Visual: Attaches a dynamic lighting source to the character. | 16 |
| [`HealthPickup`](./Characters_and_Bosses.md#context-healthpickup) | Block | Pickup Logic: Defines what happens when a health item is collected. | 16 |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. | 14 |
| [`TransformOnDeath`](./Enums.md#enum-transformondeath) | Enum/String | Applies or references the 'TransformOnDeath' effect/state. | 13 |
| [`AbilityHealthThreshold`](./Characters_and_Bosses.md#context-abilityhealththreshold) | Block | AI Trigger: Executes an ability when health drops below a specific threshold. | 12 |
| `NoHealthOnlyShield` | Number | Applies or references the 'NoHealthOnlyShield' effect/state. | 12 |
| [`SpawnThingOnDamage`](./Characters_and_Bosses.md#context-spawnthingondamage) | Block | Event Trigger: Spawns an entity when taking damage. | 12 |
| `WaterWalk` | Number | Applies or references the 'WaterWalk' effect/state. | 12 |
| `CoinPickup` | Number | Applies or references the 'CoinPickup' effect/state. | 10 |
| [`DeathRattleRevive`](./Characters_and_Bosses.md#context-deathrattlerevive) | Block | Event Trigger: Revives the character immediately upon death. | 10 |
| `LimitDamage` | Number | Applies or references the 'LimitDamage' effect/state. | 10 |
| [`MoveWhenDamaged`](./Enums.md#enum-movewhendamaged) | Enum/String | AI Movement: Forces a reposition when taking damage. | 10 |
| `StripStatuses` | Number | Applies or references the 'StripStatuses' effect/state. | 10 |
| [`FormChangeOnElementInfluence`](./Characters_and_Bosses.md#context-formchangeonelementinfluence) | Block | Logic: Changes form when affected by an element. | 9 |
| `LimitHeal` | Number | Applies or references the 'LimitHeal' effect/state. | 9 |
| `ReflectProjectiles` | Number | Passive: Reflects incoming projectiles back at the attacker. | 9 |
| [`StatusCollector`](./Characters_and_Bosses.md#context-statuscollector) | Block | Passive: Gains benefits based on the number of statuses applied to them. | 9 |
| [`TransformOnElementInfluence`](./Characters_and_Bosses.md#context-transformonelementinfluence) | Block | Logic: Changes form when affected by elements. | 9 |
| `BackstabImmunity` | Number | Applies or references the 'BackstabImmunity' effect/state. | 8 |
| `FadeInsteadOfDie` | Number | Applies or references the 'FadeInsteadOfDie' effect/state. | 8 |
| [`FormChangeOffMap`](./Characters_and_Bosses.md#context-formchangeoffmap) | Block | Logic: Changes form when pushed off the map. | 8 |
| `Plant` | Number | Applies or references the 'Plant' effect/state. | 8 |
| [`RandomizeAIWeightsEachTurn`](./Arrays.md#array-randomizeaiweightseachturn) | Array | Applies or references the 'RandomizeAIWeightsEachTurn' effect/state. | 8 |
| `SmallRockBehavior` | Number | AI Logic: Movement/interaction profile for small rocks. | 8 |
| [`AbilityWhenBuddyDies`](./Enums.md#enum-abilitywhenbuddydies) | Enum/String | Applies or references the 'AbilityWhenBuddyDies' effect/state. | 7 |
| [`ChanceToSpitOnDamage`](./Characters_and_Bosses.md#context-chancetospitondamage) | Block | Reaction: Probability to use a spit counter-attack when damaged. | 7 |
| [`MovementReaction`](./Characters_and_Bosses.md#context-movementreaction) | Block | Reaction: Triggers an effect or ability when forced to move. | 7 |
| [`TransformInXTurns`](./Characters_and_Bosses.md#context-transforminxturns) | Block | Logic: Forces a form change after X turns. | 7 |
| `AddDamage` | Number | Applies or references the 'AddDamage' effect/state. | 6 |
| [`CaveFamilyEnrage`](./Characters_and_Bosses.md#context-cavefamilyenrage) | Block | AI Trigger: Enrage logic triggered when a cave family member is killed. | 6 |
| [`Divide4OnDeath`](./Enums.md#enum-divide4ondeath) | Enum/String | Applies or references the 'Divide4OnDeath' effect/state. | 6 |
| [`FormChangeWhilePrimingAbility`](./Characters_and_Bosses.md#context-formchangewhileprimingability) | Block | Logic: Changes form while preparing/priming a specific ability. | 6 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 6 |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum/String | Applies or references the 'InnateElement' effect/state. | 6 |
| `KaijuKnockbackImmune` | Number | Applies or references the 'KaijuKnockbackImmune' effect/state. | 6 |
| [`MoveTowardsDamageSource`](./Characters_and_Bosses.md#context-movetowardsdamagesource) | Block | AI Movement: Closes distance on the last source of damage. | 6 |
| `OverrideMaxHealth` | Number | Applies or references the 'OverrideMaxHealth' effect/state. | 6 |
| [`SecurityBotProtect`](./Characters_and_Bosses.md#context-securitybotprotect) | Block | AI Logic: Guarding behavior for Security Bot units. | 6 |
| [`TagGreed`](./Enums.md#enum-taggreed) | Enum/String | Applies or references the 'TagGreed' effect/state. | 6 |
| [`YOffset`](./Enums.md#enum-yoffset) | Enum/String | Applies or references the 'YOffset' effect/state. | 6 |
| `Angel` | Number | Applies or references the 'Angel' effect/state. | 5 |
| `DebuffImmunity` | Number | Applies or references the 'DebuffImmunity' effect/state. | 5 |
| `KineticSpikes` | Number | Applies or references the 'KineticSpikes' effect/state. | 5 |
| `MinimumKnockbackFromAllDamage` | Number | Applies or references the 'MinimumKnockbackFromAllDamage' effect/state. | 5 |
| [`MoveTowardsKillers`](./Enums.md#enum-movetowardskillers) | Enum/String | AI Movement: Seeks out entities that have recently killed an ally. | 5 |
| [`PassiveWhileHasStatus`](./Characters_and_Bosses.md#context-passivewhilehasstatus) | Block | Passive: Activates only while the character has the specified status. | 5 |
| `StartOffMap` | Number | Applies or references the 'StartOffMap' effect/state. | 5 |
| [`TransformOnDeathImmediately`](./Enums.md#enum-transformondeathimmediately) | Enum/String | Logic: Bypasses death sequence to instantly assume a new form. | 5 |
| [`AbilityAfterEnemyCastSpell_Stackable`](./Enums.md#enum-abilityafterenemycastspell_stackable) | Enum/String | Applies or references the 'AbilityAfterEnemyCastSpell_Stackable' effect/state. | 4 |
| `AddMaxHealth` | Number | Applies or references the 'AddMaxHealth' effect/state. | 4 |
| `AddMeleeKnockback` | Number | Applies or references the 'AddMeleeKnockback' effect/state. | 4 |
| `Ammo` | Number | Applies or references the 'Ammo' effect/state. | 4 |
| `BackstabAllDirections` | Number | Applies or references the 'BackstabAllDirections' effect/state. | 4 |
| [`BaitAura`](./Characters_and_Bosses.md#context-baitaura) | Block | Passive: Projects an aura that attracts specific enemy types (e.g., flies/maggots). | 4 |
| [`Bird`](./Enums.md#enum-bird) | Enum/String | Applies or references the 'Bird' effect/state. | 4 |
| [`ChangeTileOnPop`](./Enums.md#enum-changetileonpop) | Enum/String | Applies or references the 'ChangeTileOnPop' effect/state. | 4 |
| `CountAsCorpse` | Number | Applies or references the 'CountAsCorpse' effect/state. | 4 |
| [`DisplayDangerAOE`](./Enums.md#enum-displaydangeraoe) | Enum/String | Applies or references the 'DisplayDangerAOE' effect/state. | 4 |
| [`GroundFlopper`](./Enums.md#enum-groundflopper) | Enum/String | Applies or references the 'GroundFlopper' effect/state. | 4 |
| `IgnoreTiles` | Number | Applies or references the 'IgnoreTiles' effect/state. | 4 |
| [`LoopingSoundWhileAlive`](./Enums.md#enum-loopingsoundwhilealive) | Enum/String | Applies or references the 'LoopingSoundWhileAlive' effect/state. | 4 |
| `PrioritizeFarAwayTargets` | Number | Applies or references the 'PrioritizeFarAwayTargets' effect/state. | 4 |
| `SharkySmellsBlood` | Number | Applies or references the 'SharkySmellsBlood' effect/state. | 4 |
| [`StatusEachTurnEnd`](./Characters_and_Bosses.md#context-statuseachturnend) | Block | Event Trigger: Applies a status at the end of every turn. | 4 |
| [`StatusOnKill`](./Characters_and_Bosses.md#context-statusonkill) | Block | Event Trigger: Applies statuses when the character kills an enemy. | 4 |
| [`StatusOnTookDamageFromAbility`](./Characters_and_Bosses.md#context-statusontookdamagefromability) | Block | Event Trigger: Applies statuses when taking damage from an ability. | 4 |
| `StunImmunity` | Number | Passive: Prevents Stun from being applied. | 4 |
| [`Trapper`](./Characters_and_Bosses.md#context-trapper) | Block | Character Form: Behavior and stats for the 'Trapper' state. | 4 |
| [`WeremanTransformationReceiver`](./Enums.md#enum-weremantransformationreceiver) | Enum/String | Applies or references the 'WeremanTransformationReceiver' effect/state. | 4 |
| [`AddHiddenTag`](./Enums.md#enum-addhiddentag) | Enum/String | Applies or references the 'AddHiddenTag' effect/state. | 3 |
| `AddInitiative` | Number | Applies or references the 'AddInitiative' effect/state. | 3 |
| [`AddTag`](./Enums.md#enum-addtag) | Enum/String | Applies or references the 'AddTag' effect/state. | 3 |
| `AggroTargetIsCurrentTurn` | Number | Applies or references the 'AggroTargetIsCurrentTurn' effect/state. | 3 |
| [`ArmorPickup`](./Characters_and_Bosses.md#context-armorpickup) | Block | Pickup Logic: Defines what happens when an armor item is collected. | 3 |
| [`BaseStatMultiply`](./Enums.md#enum-basestatmultiply) | Enum/String | Applies or references the 'BaseStatMultiply' effect/state. | 3 |
| [`BonusTurnPattern`](./Arrays.md#array-bonusturnpattern) | Array | Applies or references the 'BonusTurnPattern' effect/state. | 3 |
| [`CanMutateTo`](./Arrays.md#array-canmutateto) | Array | Applies or references the 'CanMutateTo' effect/state. | 3 |
| [`DigestDeadBodies`](./Enums.md#enum-digestdeadbodies) | Enum/String | Applies or references the 'DigestDeadBodies' effect/state. | 3 |
| `FaceShield` | Number | Applies or references the 'FaceShield' effect/state. | 3 |
| [`FormChangeHealthThreshold`](./Characters_and_Bosses.md#context-formchangehealththreshold) | Block | Logic: Changes form when health crosses a threshold. | 3 |
| `InjuryImmunity` | Number | Applies or references the 'InjuryImmunity' effect/state. | 3 |
| [`ManaPickup`](./Characters_and_Bosses.md#context-manapickup) | Block | Pickup Logic: Defines what happens when a mana item is collected. | 3 |
| `MimicSpawnerAttacks` | Number | Applies or references the 'MimicSpawnerAttacks' effect/state. | 3 |
| `MinimumKnockbackFromPhysicalAttacks` | Number | Applies or references the 'MinimumKnockbackFromPhysicalAttacks' effect/state. | 3 |
| [`MutateViaAbility`](./Enums.md#enum-mutateviaability) | Enum/String | Applies or references the 'MutateViaAbility' effect/state. | 3 |
| `PrioritizeHitDifferentTargets` | Number | Applies or references the 'PrioritizeHitDifferentTargets' effect/state. | 3 |
| [`RandomPassivePool`](./Characters_and_Bosses.md#context-randompassivepool) | Block | Logic: Grants a random passive from the specified pool upon spawning. | 3 |
| `RunInXTurns` | Number | Applies or references the 'RunInXTurns' effect/state. | 3 |
| `SharePickupsWithSpawner` | Number | Applies or references the 'SharePickupsWithSpawner' effect/state. | 3 |
| [`SpawnThingOnDeath`](./Enums.md#enum-spawnthingondeath) | Enum/String | Applies or references the 'SpawnThingOnDeath' effect/state. | 3 |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 3 |
| [`SupportFormChangeInsteadOfRun`](./Enums.md#enum-supportformchangeinsteadofrun) | Enum/String | AI Logic: Forces a support unit to transform rather than flee. | 3 |
| [`TileTrail_Ahead`](./Enums.md#enum-tiletrail_ahead) | Enum/String | Applies or references the 'TileTrail_Ahead' effect/state. | 3 |
| `WeaponsDontLoseDurability` | Number | Applies or references the 'WeaponsDontLoseDurability' effect/state. | 3 |
| [`AbilityOnRoundEnd`](./Characters_and_Bosses.md#context-abilityonroundend) | Block | AI Trigger: Executes an ability at the end of the combat round. | 2 |
| [`AbilityWhenTaggedCharacterMovesNear`](./Characters_and_Bosses.md#context-abilitywhentaggedcharactermovesnear) | Block | AI Trigger: Executes an ability when a character with a specific tag moves adjacent. | 2 |
| `AddCorpseHealth` | Number | Applies or references the 'AddCorpseHealth' effect/state. | 2 |
| [`AddTemporaryEffectsToBasicAttack`](./Characters_and_Bosses.md#context-addtemporaryeffectstobasicattack) | Block | Modifier: Adds temporary statuses to the character's basic attacks. | 2 |
| `AggroTargetIsBuddy` | Number | Applies or references the 'AggroTargetIsBuddy' effect/state. | 2 |
| `AllDamageImmune_IncludingSpeculative` | Number | Applies or references the 'AllDamageImmune_IncludingSpeculative' effect/state. | 2 |
| `AlphaTurns` | Number | Applies or references the 'AlphaTurns' effect/state. | 2 |
| `AlwaysHitDifferentTargets` | Number | Applies or references the 'AlwaysHitDifferentTargets' effect/state. | 2 |
| [`AutocastEachRound`](./Characters_and_Bosses.md#context-autocasteachround) | Block | AI Trigger: Forces the character to cast a specific ability at the start of each round. | 2 |
| `BuffImmunity` | Number | Applies or references the 'BuffImmunity' effect/state. | 2 |
| [`BungaEntrance`](./Characters_and_Bosses.md#context-bungaentrance) | Block | Animation/AI State: Bunga entering the arena. | 2 |
| `CanShield` | Number | Applies or references the 'CanShield' effect/state. | 2 |
| `ChanceToDisableActionsIfNotCharmed` | Number | Applies or references the 'ChanceToDisableActionsIfNotCharmed' effect/state. | 2 |
| [`ChangeTileOnDeath`](./Enums.md#enum-changetileondeath) | Enum/String | Applies or references the 'ChangeTileOnDeath' effect/state. | 2 |
| [`CherubimReaction`](./Characters_and_Bosses.md#context-cherubimreaction) | Block | Reaction: Custom reaction triggers for Cherubim enemies. | 2 |
| `DemonicGlyphFrames` | Number | Applies or references the 'DemonicGlyphFrames' effect/state. | 2 |
| [`DiesToElement`](./Enums.md#enum-diestoelement) | Enum/String | Vulnerability: Character dies instantly if hit by this element. | 2 |
| `DissuadeInstakills` | Number | Applies or references the 'DissuadeInstakills' effect/state. | 2 |
| `DodgeChance_Status` | Number | Applies or references the 'DodgeChance_Status' effect/state. | 2 |
| `ExpireOnSpawnerTurnEnd` | Number | Applies or references the 'ExpireOnSpawnerTurnEnd' effect/state. | 2 |
| `ExtraDispersedTurns` | Number | Applies or references the 'ExtraDispersedTurns' effect/state. | 2 |
| `FaceLastDamage` | Number | Reaction: Forces the character to face towards the last damage source. | 2 |
| [`FinalBossShield`](./Enums.md#enum-finalbossshield) | Enum/String | Applies or references the 'FinalBossShield' effect/state. | 2 |
| `Flying` | Number | Applies or references the 'Flying' effect/state. | 2 |
| [`FormChangeDuringWeatherElement`](./Characters_and_Bosses.md#context-formchangeduringweatherelement) | Block | Logic: Changes form automatically during specific weather conditions. | 2 |
| `GoopWalk` | Number | Applies or references the 'GoopWalk' effect/state. | 2 |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. | 2 |
| `ImmobilePassive` | Number | Applies or references the 'ImmobilePassive' effect/state. | 2 |
| [`KaijuWinCon`](./Enums.md#enum-kaijuwincon) | Enum/String | Applies or references the 'KaijuWinCon' effect/state. | 2 |
| `MagicDamageImmune` | Number | Applies or references the 'MagicDamageImmune' effect/state. | 2 |
| `MamaCatAnimations` | Number | Applies or references the 'MamaCatAnimations' effect/state. | 2 |
| [`MiniVolcanoReaction`](./Enums.md#enum-minivolcanoreaction) | Enum/String | Applies or references the 'MiniVolcanoReaction' effect/state. | 2 |
| [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#context-mothertumorspawnincapture) | Block | Boss Logic: Logic for capturing entities inside the Mother's tumors upon spawning. | 2 |
| [`PassiveWhileNotHasStatus`](./Characters_and_Bosses.md#context-passivewhilenothasstatus) | Block | Passive: Activates only while the character does NOT have the specified status. | 2 |
| `PermanentMadness` | Number | Applies or references the 'PermanentMadness' effect/state. | 2 |
| `PrioritizeAggroTarget` | Number | Applies or references the 'PrioritizeAggroTarget' effect/state. | 2 |
| `PrioritizePlayerCats` | Number | Applies or references the 'PrioritizePlayerCats' effect/state. | 2 |
| `PrioritizeWeakestEnemy` | Number | Applies or references the 'PrioritizeWeakestEnemy' effect/state. | 2 |
| [`ProtectTargetedAllies`](./Characters_and_Bosses.md#context-protecttargetedallies) | Block | AI Logic: Navigates to intercept attacks directed at allies. | 2 |
| `SafeDoomed` | Number | Applies or references the 'SafeDoomed' effect/state. | 2 |
| [`SlotMachineRollPool`](./Characters_and_Bosses.md#context-slotmachinerollpool) | Block | Logic: Defines the possible outcomes for slot machine enemies. | 2 |
| `SpawnCreepOnHit` | Number | Applies or references the 'SpawnCreepOnHit' effect/state. | 2 |
| [`StatusOnSpawnIn`](./Characters_and_Bosses.md#context-statusonspawnin) | Block | Event Trigger: Applies statuses immediately when spawned. | 2 |
| [`StatusOnTookDamage`](./Characters_and_Bosses.md#context-statusontookdamage) | Block | Event Trigger: Applies statuses when the character takes damage. | 2 |
| `SurviveAt1HP` | Number | Applies or references the 'SurviveAt1HP' effect/state. | 2 |
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum/String | Applies or references the 'TileTrail' effect/state. | 2 |
| [`TransformOnElementInfluencex`](./Characters_and_Bosses.md#context-transformonelementinfluencex) | Block | Logic: Variant element influence transformation. | 2 |
| [`TransformWhenBuddyDies`](./Enums.md#enum-transformwhenbuddydies) | Enum/String | Applies or references the 'TransformWhenBuddyDies' effect/state. | 2 |
| `UnlockOrientation` | Number | Applies or references the 'UnlockOrientation' effect/state. | 2 |
| [`UseAbility`](./Enums.md#enum-useability) | Enum/String | Logic: Forces execution of an ability. | 2 |
| [`AbilityOnBattleStart_UseAI`](./Enums.md#enum-abilityonbattlestart_useai) | Enum/String | Applies or references the 'AbilityOnBattleStart_UseAI' effect/state. | 1 |
| [`AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack) | Enum/String | Applies or references the 'AddElementsToBasicAttack' effect/state. | 1 |
| [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#context-addstatustoreceiveddamage) | Block | Modifier: Applies a status effect whenever the character takes damage. | 1 |
| [`AddStatusToSpells`](./Characters_and_Bosses.md#context-addstatustospells) | Block | Modifier: Injects a status effect payload into all spells cast by the character. | 1 |
| [`AddStatusToWeapons`](./Characters_and_Bosses.md#context-addstatustoweapons) | Block | Modifier: Injects a status effect into attacks made with weapons. | 1 |
| [`AdvancedTint`](./Arrays.md#array-advancedtint) | Array | Applies or references the 'AdvancedTint' effect/state. | 1 |
| [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool) | Block | Map/Metaprogression: Pool of passive modifiers applied by adventure tokens. | 1 |
| [`AggroTargetIsGovernedByHitEffect`](./Characters_and_Bosses.md#context-aggrotargetisgovernedbyhiteffect) | Block | AI Logic: Forces the character's aggro to follow specific hit effects rather than default proximity. | 1 |
| `AggroTargetIsLastEnemyThatDealtDamage` | Number | Applies or references the 'AggroTargetIsLastEnemyThatDealtDamage' effect/state. | 1 |
| `AggroTargetIsLowestHealthEnemyTillItDies` | Number | Applies or references the 'AggroTargetIsLowestHealthEnemyTillItDies' effect/state. | 1 |
| `AggroTargetIsLowestMaxHealthCat` | Number | Applies or references the 'AggroTargetIsLowestMaxHealthCat' effect/state. | 1 |
| [`AlienBeastDangerZones`](./Arrays.md#array-alienbeastdangerzones) | Array | Applies or references the 'AlienBeastDangerZones' effect/state. | 1 |
| `AlienBeastEyeStalks` | Number | Applies or references the 'AlienBeastEyeStalks' effect/state. | 1 |
| `AllSpellsCostActPoints` | Number | Applies or references the 'AllSpellsCostActPoints' effect/state. | 1 |
| [`AllStatsAura`](./Characters_and_Bosses.md#context-allstatsaura) | Block | Passive: Projects an aura that modifies all primary stats of nearby characters. | 1 |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 1 |
| `AvoidDamagingCharmedEnemies` | Number | Applies or references the 'AvoidDamagingCharmedEnemies' effect/state. | 1 |
| `AwardCoinsOnDeath` | Number | Applies or references the 'AwardCoinsOnDeath' effect/state. | 1 |
| `BasicAIDangerZone` | Number | Applies or references the 'BasicAIDangerZone' effect/state. | 1 |
| [`BattlefieldUniqueRandomPassive`](./Characters_and_Bosses.md#context-battlefielduniquerandompassive) | Block | Map Rule: Grants a unique random passive modifier to the battlefield. | 1 |
| `BlackHolePassive` | Number | Applies or references the 'BlackHolePassive' effect/state. | 1 |
| [`BloatEyePassive2`](./Enums.md#enum-bloateyepassive2) | Enum/String | Applies or references the 'BloatEyePassive2' effect/state. | 1 |
| `BlockAllDamage` | Number | Applies or references the 'BlockAllDamage' effect/state. | 1 |
| `BombBehavior` | Number | Applies or references the 'BombBehavior' effect/state. | 1 |
| [`BungaCheers`](./Characters_and_Bosses.md#context-bungacheers) | Block | Animation/AI State: Bunga cheering animation logic. | 1 |
| `Burn` | Number | Applies or references the 'Burn' effect/state. | 1 |
| `CCImmunity` | Number | Applies or references the 'CCImmunity' effect/state. | 1 |
| `CapReceivedDamage` | Number | Applies or references the 'CapReceivedDamage' effect/state. | 1 |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| [`CerberubsAggroTargetBehavior`](./Characters_and_Bosses.md#context-cerberubsaggrotargetbehavior) | Block | AI Logic: Custom aggro targeting rules for Cerberubs. | 1 |
| [`ChanceToBackflip`](./Characters_and_Bosses.md#context-chancetobackflip) | Block | Reaction: Probability to execute a backflip dodge. | 1 |
| [`ChanceToFormChangeOnAbilityDamage`](./Characters_and_Bosses.md#context-chancetoformchangeonabilitydamage) | Block | Reaction: Probability to change forms when taking ability damage. | 1 |
| [`ChaosBossFormChangeGuide`](./Characters_and_Bosses.md#context-chaosbossformchangeguide) | Block | Boss Logic: Maps the form transition phases for the Chaos Boss. | 1 |
| [`ChaosBossPieces`](./Characters_and_Bosses.md#context-chaosbosspieces) | Block | Boss Logic: Defines the separate destructible pieces of the Chaos Boss. | 1 |
| [`ChaosHeadDropIn`](./Characters_and_Bosses.md#context-chaosheaddropin) | Block | Boss Logic: Drop-in attack/animation for the Chaos Head. | 1 |
| [`ConjureBonusAbility`](./Enums.md#enum-conjurebonusability) | Enum/String | Adds a temporary bonus ability to the character's hand/deck. | 1 |
| [`CounterAttackAfterEnemyCastSpell`](./Enums.md#enum-counterattackafterenemycastspell) | Enum/String | Applies or references the 'CounterAttackAfterEnemyCastSpell' effect/state. | 1 |
| [`CreateGlobalModifiers`](./Characters_and_Bosses.md#context-createglobalmodifiers) | Block | Encounter Rule: Generates map-wide modifiers. | 1 |
| `CrowAttackLink` | Number | Applies or references the 'CrowAttackLink' effect/state. | 1 |
| `DamageFromBehindOnly` | Number | Applies or references the 'DamageFromBehindOnly' effect/state. | 1 |
| [`DelayedAutoRevive`](./Characters_and_Bosses.md#context-delayedautorevive) | Block | Logic: Character revives automatically after a set delay. | 1 |
| `DemonicGlyphStealer` | Number | Applies or references the 'DemonicGlyphStealer' effect/state. | 1 |
| [`DiceBehavior`](./Characters_and_Bosses.md#context-dicebehavior) | Block | AI Logic: Custom behavior for Dice enemies. | 1 |
| [`DicerArt`](./Arrays.md#array-dicerart) | Array | Applies or references the 'DicerArt' effect/state. | 1 |
| `DieWhenOnlyGolemsLeft` | Number | Applies or references the 'DieWhenOnlyGolemsLeft' effect/state. | 1 |
| `DieWhenSpawnerDies` | Number | Applies or references the 'DieWhenSpawnerDies' effect/state. | 1 |
| [`DiesToPiercingAndSpikes`](./Characters_and_Bosses.md#context-diestopiercingandspikes) | Block | Vulnerability: Character dies instantly if hit by piercing attacks or spikes. | 1 |
| `DisableSpells` | Number | Applies or references the 'DisableSpells' effect/state. | 1 |
| `Disguised` | Number | Applies or references the 'Disguised' effect/state. | 1 |
| [`DisguisedTrapper`](./Enums.md#enum-disguisedtrapper) | Enum/String | Applies or references the 'DisguisedTrapper' effect/state. | 1 |
| `DisplayBuddyCatOnSpawn` | Number | Applies or references the 'DisplayBuddyCatOnSpawn' effect/state. | 1 |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. | 1 |
| `DivineShieldPickup` | Number | Applies or references the 'DivineShieldPickup' effect/state. | 1 |
| `DodgeChance` | Number | Applies or references the 'DodgeChance' effect/state. | 1 |
| `DodgeChanceWithBlindSpot` | Number | Applies or references the 'DodgeChanceWithBlindSpot' effect/state. | 1 |
| [`DodgeWhenTargeted`](./Characters_and_Bosses.md#context-dodgewhentargeted) | Block | Reaction: Executes a dodge maneuver when targeted. | 1 |
| `DustCloudBehavior` | Number | Applies or references the 'DustCloudBehavior' effect/state. | 1 |
| `Dybbuk1HPTracker` | Number | Applies or references the 'Dybbuk1HPTracker' effect/state. | 1 |
| [`DybbukPossessionFallback`](./Characters_and_Bosses.md#context-dybbukpossessionfallback) | Block | Logic: Fallback state when a Dybbuk possession fails. | 1 |
| `ElectricArcs` | Number | Applies or references the 'ElectricArcs' effect/state. | 1 |
| [`ElementWeakness`](./Enums.md#enum-elementweakness) | Enum/String | Applies or references the 'ElementWeakness' effect/state. | 1 |
| `EnrageOnDamage` | Number | Applies or references the 'EnrageOnDamage' effect/state. | 1 |
| `EraseSpawnCoins` | Number | Applies or references the 'EraseSpawnCoins' effect/state. | 1 |
| `EventBounterHunterPassive` | Number | Applies or references the 'EventBounterHunterPassive' effect/state. | 1 |
| `ExtraMovePoints` | Number | Applies or references the 'ExtraMovePoints' effect/state. | 1 |
| [`ExtraTurnsPerTaggedUnit`](./Enums.md#enum-extraturnspertaggedunit) | Enum/String | Applies or references the 'ExtraTurnsPerTaggedUnit' effect/state. | 1 |
| [`FaceAwayLastDamage`](./Characters_and_Bosses.md#context-faceawaylastdamage) | Block | Reaction: Forces the character to face away from the last damage source. | 1 |
| [`FinalBossBeamQueue`](./Characters_and_Bosses.md#context-finalbossbeamqueue) | Block | Boss Logic: Attack queue for the final boss beam. | 1 |
| [`FinalBossBecomeTheChild`](./Characters_and_Bosses.md#context-finalbossbecomethechild) | Block | Boss Logic: Phase transition for the final boss. | 1 |
| [`FinalBossHitCountdownBoris`](./Characters_and_Bosses.md#context-finalbosshitcountdownboris) | Block | Boss Logic: Countdown trigger for Boris. | 1 |
| [`FinalBossHitCountdownExplosive`](./Characters_and_Bosses.md#context-finalbosshitcountdownexplosive) | Block | Boss Logic: Countdown trigger for explosives. | 1 |
| [`FinalBossHitCountdownHoly`](./Characters_and_Bosses.md#context-finalbosshitcountdownholy) | Block | Boss Logic: Countdown trigger for holy attacks. | 1 |
| [`FinalBossPupils`](./Characters_and_Bosses.md#context-finalbosspupils) | Block | Boss Logic: Pupil state management. | 1 |
| [`FinalBossShieldHealth`](./Characters_and_Bosses.md#context-finalbossshieldhealth) | Block | Boss Logic: Shield health management. | 1 |
| [`FinalBossSyncAnimations`](./Characters_and_Bosses.md#context-finalbosssyncanimations) | Block | Boss Logic: Synchronizes multi-part boss animations. | 1 |
| `FlingObjectsOnTop` | Number | Applies or references the 'FlingObjectsOnTop' effect/state. | 1 |
| [`FlushmasterCelebration`](./Enums.md#enum-flushmastercelebration) | Enum/String | Applies or references the 'FlushmasterCelebration' effect/state. | 1 |
| `ForceDodgeEverything` | Number | Applies or references the 'ForceDodgeEverything' effect/state. | 1 |
| [`FormChangeWhenBuddyDies`](./Enums.md#enum-formchangewhenbuddydies) | Enum/String | Applies or references the 'FormChangeWhenBuddyDies' effect/state. | 1 |
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum/String | Applies or references the 'FreePathfindElement' effect/state. | 1 |
| `FullBlockEverything` | Number | Applies or references the 'FullBlockEverything' effect/state. | 1 |
| `FullBlockEverythingTo0Damage` | Number | Applies or references the 'FullBlockEverythingTo0Damage' effect/state. | 1 |
| `GasCanBehavior` | Number | Applies or references the 'GasCanBehavior' effect/state. | 1 |
| `GasCloudBehavior2` | Number | Applies or references the 'GasCloudBehavior2' effect/state. | 1 |
| `GeminiTwin` | Number | Applies or references the 'GeminiTwin' effect/state. | 1 |
| `GlobalManaDrainAura` | Number | Applies or references the 'GlobalManaDrainAura' effect/state. | 1 |
| `GoopImmunity` | Number | Applies or references the 'GoopImmunity' effect/state. | 1 |
| `GuillotinaDeathHead` | Number | Applies or references the 'GuillotinaDeathHead' effect/state. | 1 |
| [`HPAltStates`](./Characters_and_Bosses.md#context-hpaltstates) | Block | Visual: Alternative sprite states based on current health. | 1 |
| [`HarpoonTrapPassive`](./Enums.md#enum-harpoontrappassive) | Enum/String | Applies or references the 'HarpoonTrapPassive' effect/state. | 1 |
| [`HealNeighborsEachTurn`](./Characters_and_Bosses.md#context-healneighborseachturn) | Block | Passive: Restores health to adjacent allies at the start of the turn. | 1 |
| `HiddenDoomed` | Number | Applies or references the 'HiddenDoomed' effect/state. | 1 |
| [`HitlerExecute`](./Characters_and_Bosses.md#context-hitlerexecute) | Block | Boss Logic: Specific execution or ultimate attack state. | 1 |
| `IceBlockBehavior` | Number | Applies or references the 'IceBlockBehavior' effect/state. | 1 |
| `IllusionTint` | Number | Applies or references the 'IllusionTint' effect/state. | 1 |
| [`InfiniteRebirth`](./Characters_and_Bosses.md#context-infiniterebirth) | Block | Logic: Allows the character to revive endlessly. | 1 |
| `InheritSpawnerStats` | Number | Applies or references the 'InheritSpawnerStats' effect/state. | 1 |
| `InsertIntoBackgroundPlaceholder` | Number | Applies or references the 'InsertIntoBackgroundPlaceholder' effect/state. | 1 |
| [`JohnnyNeedsWashing`](./Characters_and_Bosses.md#context-johnnyneedswashing) | Block | Character Form: Behavior and stats for the 'JohnnyNeedsWashing' state. | 1 |
| [`JohnnyWasher`](./Enums.md#enum-johnnywasher) | Enum/String | Applies or references the 'JohnnyWasher' effect/state. | 1 |
| `KnockbackImmunity` | Number | Applies or references the 'KnockbackImmunity' effect/state. | 1 |
| [`LegacySpawnSavedCatIfExists`](./Enums.md#enum-legacyspawnsavedcatifexists) | Enum/String | Applies or references the 'LegacySpawnSavedCatIfExists' effect/state. | 1 |
| [`LockOrientationFaceTile`](./Arrays.md#array-lockorientationfacetile) | Array | Applies or references the 'LockOrientationFaceTile' effect/state. | 1 |
| [`ManglerMonsterPassive`](./Enums.md#enum-manglermonsterpassive) | Enum/String | Applies or references the 'ManglerMonsterPassive' effect/state. | 1 |
| [`MegaDinoDropController`](./Characters_and_Bosses.md#context-megadinodropcontroller) | Block | Boss Logic: Manages loot drops for the Mega Dino. | 1 |
| `MissChance` | Number | Applies or references the 'MissChance' effect/state. | 1 |
| [`ModularPickup`](./Characters_and_Bosses.md#context-modularpickup) | Block | Pickup Logic: Defines what happens when a modular item is collected. | 1 |
| [`MonkCatReactionAbilities`](./Characters_and_Bosses.md#context-monkcatreactionabilities) | Block | Reaction: Specific counter-attack or dodge abilities used by the Monk class. | 1 |
| [`MoonHeadCrackedVisual`](./Enums.md#enum-moonheadcrackedvisual) | Enum/String | Applies or references the 'MoonHeadCrackedVisual' effect/state. | 1 |
| [`MotherGrowController`](./Characters_and_Bosses.md#context-mothergrowcontroller) | Block | Boss Logic: Manages the growth phases of the Mother boss. | 1 |
| [`MotherTumorPassive`](./Characters_and_Bosses.md#context-mothertumorpassive) | Block | Boss Logic: Passive effects applied to the Mother's tumors. | 1 |
| [`Mount`](./Characters_and_Bosses.md#context-mount) | Block | Character Form: Behavior and stats for the 'Mount' state. | 1 |
| [`MoveAfterAnyAttemptedAttack`](./Characters_and_Bosses.md#context-moveafteranyattemptedattack) | Block | AI Movement: Forces a move action immediately after attacking, even if it missed. | 1 |
| [`MoveAwayFromDamageSource`](./Characters_and_Bosses.md#context-moveawayfromdamagesource) | Block | AI Movement: Moves away from the source of recent damage. | 1 |
| [`MoveAwayWhenEnemyAdjacent`](./Characters_and_Bosses.md#context-moveawaywhenenemyadjacent) | Block | AI Movement: Moves away if an enemy enters an adjacent tile. | 1 |
| [`MultiSpawnOnDeath`](./Characters_and_Bosses.md#context-multispawnondeath) | Block | Event Trigger: Spawns multiple entities upon death. | 1 |
| `MulticatHeads` | Number | Applies or references the 'MulticatHeads' effect/state. | 1 |
| `MutateAfterXTurns` | Number | Applies or references the 'MutateAfterXTurns' effect/state. | 1 |
| `MuteDemonicGlyphDisplay` | Number | Applies or references the 'MuteDemonicGlyphDisplay' effect/state. | 1 |
| `OrthogonalAIDangerZone` | Number | Applies or references the 'OrthogonalAIDangerZone' effect/state. | 1 |
| `PackHunting` | Number | Applies or references the 'PackHunting' effect/state. | 1 |
| [`PassiveWhenAffectedByElement`](./Characters_and_Bosses.md#context-passivewhenaffectedbyelement) | Block | Passive: Activates only when afflicted by the specified element. | 1 |
| [`PassiveWhenDead`](./Characters_and_Bosses.md#context-passivewhendead) | Block | Passive: Activates only while the character is dead (e.g., corpse effects). | 1 |
| `Phasing` | Number | Applies or references the 'Phasing' effect/state. | 1 |
| `PoisonThorns` | Number | Applies or references the 'PoisonThorns' effect/state. | 1 |
| `ReturnBoundItemOnBattleEnd` | Number | Applies or references the 'ReturnBoundItemOnBattleEnd' effect/state. | 1 |
| [`RevengeDamage`](./Characters_and_Bosses.md#context-revengedamage) | Block | Reaction: Deals damage when taking damage. | 1 |
| `RunWhenKittensDead` | Number | Applies or references the 'RunWhenKittensDead' effect/state. | 1 |
| [`RunWhenLastPlayerCatIsCharmed`](./Characters_and_Bosses.md#context-runwhenlastplayercatischarmed) | Block | AI Logic: Flee logic when the player team is entirely crowd-controlled. | 1 |
| [`ScalingAttackAnimation`](./Characters_and_Bosses.md#context-scalingattackanimation) | Block | Visual: Animation scales based on damage output. | 1 |
| `SetSpellCosts` | Number | Applies or references the 'SetSpellCosts' effect/state. | 1 |
| [`SharePickups`](./Characters_and_Bosses.md#context-sharepickups) | Block | Passive: Item pickups collected by this unit are shared with others. | 1 |
| [`SkipFirstRounds`](./Characters_and_Bosses.md#context-skipfirstrounds) | Block | AI Logic: Passes turn for the first X rounds of combat. | 1 |
| `SpawnCreepOnHitKnockback` | Number | Applies or references the 'SpawnCreepOnHitKnockback' effect/state. | 1 |
| `SpawnerCatDataReference` | Number | Applies or references the 'SpawnerCatDataReference' effect/state. | 1 |
| [`SpewerAltGraphics`](./Characters_and_Bosses.md#context-speweraltgraphics) | Block | Visual: Alternative graphics for Spewer enemies. | 1 |
| `SpreadWater` | Number | Applies or references the 'SpreadWater' effect/state. | 1 |
| `SproutsGrantMovement` | Number | Applies or references the 'SproutsGrantMovement' effect/state. | 1 |
| `StartDead` | Number | Applies or references the 'StartDead' effect/state. | 1 |
| [`StatusAfterXTurns`](./Characters_and_Bosses.md#context-statusafterxturns) | Block | Event Trigger: Applies a status effect after X turns have passed. | 1 |
| [`StatusEachTurnBeginIfHasStatus`](./Characters_and_Bosses.md#context-statuseachturnbeginifhasstatus) | Block | Event Trigger: Applies a status at the start of the turn if a prerequisite status is met. | 1 |
| [`StatusEachTurnEndIfEnabledAtStartOfTurn`](./Characters_and_Bosses.md#context-statuseachturnendifenabledatstartofturn) | Block | Event Trigger: Applies a status at the end of the turn if an enabling condition was met at the start. | 1 |
| [`StatusOnDie`](./Characters_and_Bosses.md#context-statusondie) | Block | Event Trigger: Applies statuses when the character dies. | 1 |
| [`StatusOnEndMove`](./Characters_and_Bosses.md#context-statusonendmove) | Block | Event Trigger: Applies statuses when the character finishes moving. | 1 |
| [`StatusOnEnemyConfused`](./Characters_and_Bosses.md#context-statusonenemyconfused) | Block | Event Trigger: Applies statuses when an enemy becomes confused. | 1 |
| [`StatusOnGainCoins`](./Characters_and_Bosses.md#context-statusongaincoins) | Block | Event Trigger: Applies statuses when coins are collected. | 1 |
| [`StatusOverlappingCharactersAndDie`](./Characters_and_Bosses.md#context-statusoverlappingcharactersanddie) | Block | Event Trigger: Applies statuses to overlapping entities, then destroys self. | 1 |
| [`StatusWhenStatusCompletelyRemoved`](./Characters_and_Bosses.md#context-statuswhenstatuscompletelyremoved) | Block | Event Trigger: Applies statuses when a tracked status effect is fully cleansed. | 1 |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. | 1 |
| [`SupportDieInsteadOfRun`](./Characters_and_Bosses.md#context-supportdieinsteadofrun) | Block | AI Logic: Forces a support unit to die rather than flee. | 1 |
| [`SwimmingFormChange`](./Characters_and_Bosses.md#context-swimmingformchange) | Block | Logic: Automates form change when entering/exiting water. | 1 |
| [`SyncFormsWithBuddy`](./Characters_and_Bosses.md#context-syncformswithbuddy) | Block | Logic: Forces this character's form to match their familiar/buddy. | 1 |
| [`T3HitlerSpawningPhase`](./Characters_and_Bosses.md#context-t3hitlerspawningphase) | Block | Boss Logic: Minion spawn phase for the T3 Hitler boss. | 1 |
| `TVBotDisableAttack` | Number | Applies or references the 'TVBotDisableAttack' effect/state. | 1 |
| `TVBotDisableMove` | Number | Applies or references the 'TVBotDisableMove' effect/state. | 1 |
| `TVBotDisableSpells` | Number | Applies or references the 'TVBotDisableSpells' effect/state. | 1 |
| [`TVBotScreen`](./Characters_and_Bosses.md#context-tvbotscreen) | Block | Visual: TV Bot screen state. | 1 |
| `TakeWeaponFromSpawner` | Number | Applies or references the 'TakeWeaponFromSpawner' effect/state. | 1 |
| `Tall` | Number | Applies or references the 'Tall' effect/state. | 1 |
| [`TallTumorManaBurn`](./Enums.md#enum-talltumormanaburn) | Enum/String | Applies or references the 'TallTumorManaBurn' effect/state. | 1 |
| [`Terminator2Chase`](./Enums.md#enum-terminator2chase) | Enum/String | Applies or references the 'Terminator2Chase' effect/state. | 1 |
| [`Terminator2Run`](./Characters_and_Bosses.md#context-terminator2run) | Block | AI Movement: Specific run logic for Terminator2. | 1 |
| [`TerminatorChase`](./Characters_and_Bosses.md#context-terminatorchase) | Block | AI Movement: Specific chase logic for Terminator. | 1 |
| [`TerminatorSkin`](./Characters_and_Bosses.md#context-terminatorskin) | Block | Visual: Skin definition for Terminator. | 1 |
| [`TileElementDamageImmunity`](./Enums.md#enum-tileelementdamageimmunity) | Enum/String | Applies or references the 'TileElementDamageImmunity' effect/state. | 1 |
| [`TinkererBasicAttackSwitching`](./Characters_and_Bosses.md#context-tinkererbasicattackswitching) | Block | Logic: Allows Tinkerer to swap basic attacks. | 1 |
| `TireBehavior` | Number | Applies or references the 'TireBehavior' effect/state. | 1 |
| `TormentorHeal` | Number | Applies or references the 'TormentorHeal' effect/state. | 1 |
| [`TowerDefenseReflex`](./Enums.md#enum-towerdefensereflex) | Enum/String | Applies or references the 'TowerDefenseReflex' effect/state. | 1 |
| [`TrackAmountKilledByPlayer`](./Enums.md#enum-trackamountkilledbyplayer) | Enum/String | Applies or references the 'TrackAmountKilledByPlayer' effect/state. | 1 |
| [`TransformOnStatusThreshold`](./Characters_and_Bosses.md#context-transformonstatusthreshold) | Block | Logic: Changes form when a status effect reaches a certain stack count. | 1 |
| `TutorialBossRiggedFight` | Number | Applies or references the 'TutorialBossRiggedFight' effect/state. | 1 |
| [`TwisterFling`](./Characters_and_Bosses.md#context-twisterfling) | Block | Logic: Fling behavior for tornado attacks. | 1 |
| `UncappedHP` | Number | Applies or references the 'UncappedHP' effect/state. | 1 |
| [`UnlimitedDeathRattleRevive`](./Characters_and_Bosses.md#context-unlimiteddeathrattlerevive) | Block | Logic: Endless resurrection on death. | 1 |
| `UpTireBehavior` | Number | Applies or references the 'UpTireBehavior' effect/state. | 1 |
| [`UseAbilityWhenOutOfStatus`](./Characters_and_Bosses.md#context-useabilitywhenoutofstatus) | Block | Logic: Casts a specific ability the moment a status effect expires. | 1 |
| [`UseAbilityWhenShieldDepleted`](./Enums.md#enum-useabilitywhenshielddepleted) | Enum/String | Applies or references the 'UseAbilityWhenShieldDepleted' effect/state. | 1 |
| `Wall` | Number | Applies or references the 'Wall' effect/state. | 1 |
| [`WhitelistPickupType`](./Enums.md#enum-whitelistpickuptype) | Enum/String | Applies or references the 'WhitelistPickupType' effect/state. | 1 |
| `WideBackstab` | Number | Applies or references the 'WideBackstab' effect/state. | 1 |
| `WispDodge` | Number | Applies or references the 'WispDodge' effect/state. | 1 |
| `ZeroKnockbackDamage` | Number | Applies or references the 'ZeroKnockbackDamage' effect/state. | 1 |

</details>

---

### Context: `sound`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count (X/61) |
| :--- | :--- | :--- | :--- |
| [`alt_sounds`](./Arrays.md#array-alt_sounds) | Array |  | 61 |
| [`SE_Cat_StompLegMove`](./Enums.md#enum-se_cat_stomplegmove) | Enum/String | Applies or references the 'SE_Cat_StompLegMove' effect/state. | 2 |
| [`SE_CatSwishThrow`](./Enums.md#enum-se_catswishthrow) | Enum/String | Applies or references the 'SE_CatSwishThrow' effect/state. | 1 |
| [`SE_Cat_ShadowStepIn`](./Enums.md#enum-se_cat_shadowstepin) | Enum/String | Applies or references the 'SE_Cat_ShadowStepIn' effect/state. | 1 |
| [`SE_Cat_ShadowStepOut`](./Enums.md#enum-se_cat_shadowstepout) | Enum/String | Applies or references the 'SE_Cat_ShadowStepOut' effect/state. | 1 |
| [`SE_Cat_WeaponLower`](./Enums.md#enum-se_cat_weaponlower) | Enum/String | Applies or references the 'SE_Cat_WeaponLower' effect/state. | 1 |
| [`SE_Cat_WeaponRaise`](./Enums.md#enum-se_cat_weaponraise) | Enum/String | Applies or references the 'SE_Cat_WeaponRaise' effect/state. | 1 |
| [`SE_Cat_bearHug`](./Enums.md#enum-se_cat_bearhug) | Enum/String | Applies or references the 'SE_Cat_bearHug' effect/state. | 1 |
| [`SE_Cat_equipWeapon`](./Enums.md#enum-se_cat_equipweapon) | Enum/String | Applies or references the 'SE_Cat_equipWeapon' effect/state. | 1 |
| [`SE_PetRock_Dash`](./Enums.md#enum-se_petrock_dash) | Enum/String | Applies or references the 'SE_PetRock_Dash' effect/state. | 1 |
| [`animation_prefix`](./Enums.md#enum-animation_prefix) | Enum/String |  | 1 |

</details>

---

### Context: `FormChanger`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/59) |
| :--- | :--- | :--- | :--- |
| [`initial_form`](./Enums.md#enum-initial_form) | Enum/String |  | 59 |
| [`Default`](./Characters_and_Bosses.md#context-default) | Block | Character Form: The baseline default behavior state. | 37 |
| [`Normal`](./Characters_and_Bosses.md#context-normal) | Block | Character Form: Behavior and stats for the 'Normal' state. | 11 |
| [`Rage`](./Characters_and_Bosses.md#context-rage) | Block | Character Form: Behavior and stats for the 'Rage' state. | 10 |
| [`HasCat`](./Characters_and_Bosses.md#context-hascat) | Block | Character Form: Behavior and stats for the 'HasCat' state. | 5 |
| [`OffMap`](./Characters_and_Bosses.md#context-offmap) | Block | Character Form: Behavior and stats for the 'OffMap' state. | 4 |
| [`default`](./Characters_and_Bosses.md#context-default) | Block | Baseline configuration. | 4 |
| [`hot`](./Characters_and_Bosses.md#context-hot) | Block | Visual effect indicator. | 4 |
| [`AllAlive`](./Characters_and_Bosses.md#context-allalive) | Block | Encounter State: Logic executed when all specific entities are currently alive. | 3 |
| [`Down`](./Characters_and_Bosses.md#context-down) | Block | Character Form: Behavior and stats for the 'Down' state. | 3 |
| [`Full`](./Characters_and_Bosses.md#context-full) | Block | Character Form: Behavior and stats for the 'Full' state. | 3 |
| [`OneAlive`](./Characters_and_Bosses.md#context-onealive) | Block | Encounter State: Logic executed when exactly one target is alive. | 3 |
| [`TwoAlive`](./Characters_and_Bosses.md#context-twoalive) | Block | Encounter State: Logic executed when exactly two targets are alive. | 3 |
| [`Up`](./Characters_and_Bosses.md#context-up) | Block | Character Form: Behavior and stats for the 'Up' state. | 3 |
| [`Big`](./Characters_and_Bosses.md#context-big) | Block | Character Form / AI State: Behavior and stats for the 'Big' state. | 2 |
| [`Boris`](./Characters_and_Bosses.md#context-boris) | Block | Character Form / AI State: Behavior and stats for the 'Boris' state. | 2 |
| [`CaveMan`](./Characters_and_Bosses.md#context-caveman) | Block | Character Form: Behavior and stats for the 'CaveMan' state. | 2 |
| [`CaveManSpear`](./Characters_and_Bosses.md#context-cavemanspear) | Block | Character Form: Behavior and stats for the 'CaveManSpear' state. | 2 |
| [`Empty`](./Characters_and_Bosses.md#context-empty) | Block | Character Form: Behavior and stats for the 'Empty' state. | 2 |
| [`Explosive`](./Characters_and_Bosses.md#context-explosive) | Block | Character Form: Behavior and stats for the 'Explosive' state. | 2 |
| [`Holding`](./Characters_and_Bosses.md#context-holding) | Block | Character Form: Behavior and stats for the 'Holding' state. | 2 |
| [`Holy`](./Characters_and_Bosses.md#context-holy) | Block | Character Form: Behavior and stats for the 'Holy' state. | 2 |
| [`NotPriming`](./Characters_and_Bosses.md#context-notpriming) | Block | Character Form: Behavior and stats when not charging an ability. | 2 |
| [`Priming`](./Characters_and_Bosses.md#context-priming) | Block | Character Form: Behavior and stats when charging an ability. | 2 |
| [`Rain`](./Characters_and_Bosses.md#context-rain) | Block | Character Form: Behavior and stats for the 'Rain' state. | 2 |
| [`Small`](./Characters_and_Bosses.md#context-small) | Block | Character Form: Behavior and stats for the 'Small' state. | 2 |
| [`SquirrelForm`](./Characters_and_Bosses.md#context-squirrelform) | Block | Character Form: Behavior and stats for the 'SquirrelForm' state. | 2 |
| [`Turtled`](./Characters_and_Bosses.md#context-turtled) | Block | Character Form: Behavior and stats for the 'Turtled' state. | 2 |
| [`active`](./Characters_and_Bosses.md#context-active) | Block | Defines actively executed abilities. | 2 |
| [`passive`](./Characters_and_Bosses.md#context-passive) | Block | Intrinsic passive modifier. | 2 |
| [`Alert`](./Characters_and_Bosses.md#context-alert) | Block | AI State: The behavior profile used when the character is alerted to enemies. | 1 |
| [`Angry`](./Characters_and_Bosses.md#context-angry) | Block | Character Form / AI State: Behavior and stats for the 'Angry' state. | 1 |
| [`Attacker`](./Characters_and_Bosses.md#context-attacker) | Block | AI Role: Designates the character as an attacker rather than support. | 1 |
| [`BellyFull`](./Characters_and_Bosses.md#context-bellyfull) | Block | Character Form / AI State: Behavior and stats for the 'BellyFull' state. | 1 |
| [`BigHolding`](./Characters_and_Bosses.md#context-bigholding) | Block | Character Form / AI State: Behavior and stats for the 'BigHolding' state. | 1 |
| [`BigHoldingCat`](./Characters_and_Bosses.md#context-bigholdingcat) | Block | Character Form / AI State: Behavior and stats for the 'BigHoldingCat' state. | 1 |
| [`Bishop`](./Characters_and_Bosses.md#context-bishop) | Block | Character Form / AI State: Behavior and stats for the 'Bishop' state. | 1 |
| [`BlackHole`](./Characters_and_Bosses.md#context-blackhole) | Block | Character Form / AI State: Behavior and stats for the 'BlackHole' state. | 1 |
| [`Bomb`](./Characters_and_Bosses.md#context-bomb) | Block | Character Form / AI State: Behavior and stats for the 'Bomb' state. | 1 |
| [`Bully`](./Characters_and_Bosses.md#context-bully) | Block | Character Form / AI State: Behavior and stats for the 'Bully' state. | 1 |
| `Butcher` | Block | Applies or references the 'Butcher' effect/state. | 1 |
| [`CaveBaby`](./Characters_and_Bosses.md#context-cavebaby) | Block | Character Form: Behavior and stats for the 'CaveBaby' state. | 1 |
| [`CaveWoman`](./Characters_and_Bosses.md#context-cavewoman) | Block | Character Form: Behavior and stats for the 'CaveWoman' state. | 1 |
| [`CaveWomanHasCat`](./Characters_and_Bosses.md#context-cavewomanhascat) | Block | Character Form: Behavior and stats for the 'CaveWomanHasCat' state. | 1 |
| [`Charging`](./Characters_and_Bosses.md#context-charging) | Block | Character Form / AI State: Behavior when charging an attack. | 1 |
| [`Close`](./Characters_and_Bosses.md#context-close) | Block | AI Movement logic: Maneuvers into close/melee range. | 1 |
| `Colorless` | Block | Applies or references the 'Colorless' effect/state. | 1 |
| [`Cultist`](./Characters_and_Bosses.md#context-cultist) | Block | Character Form: Behavior and stats for the 'Cultist' state. | 1 |
| [`Damaged`](./Characters_and_Bosses.md#context-damaged) | Block | Character Form / AI State: Behavior when health is critically low. | 1 |
| [`Default_Ceiling`](./Characters_and_Bosses.md#context-default_ceiling) | Block | Character Form: The baseline behavior state while attached to the ceiling. | 1 |
| [`Default_Ground`](./Characters_and_Bosses.md#context-default_ground) | Block | Character Form: The baseline behavior state while on the ground. | 1 |
| [`DesireMech`](./Characters_and_Bosses.md#context-desiremech) | Block | Character Form: Behavior and stats for the 'DesireMech' state. | 1 |
| [`Die`](./Characters_and_Bosses.md#context-die) | Block | Character Form / Logic: Forces the character to die. | 1 |
| `Druid` | Block | Applies or references the 'Druid' effect/state. | 1 |
| [`Drunker`](./Characters_and_Bosses.md#context-drunker) | Block | Character Form: Behavior and stats for the 'Drunker' state. | 1 |
| [`DualSword`](./Characters_and_Bosses.md#context-dualsword) | Block | Character Form: Behavior and stats for the 'DualSword' state. | 1 |
| [`DualSword_Primed`](./Characters_and_Bosses.md#context-dualsword_primed) | Block | Character Form: Behavior and stats for the 'DualSword_Primed' state. | 1 |
| [`Dumb`](./Characters_and_Bosses.md#context-dumb) | Block | AI Profile: A simplified, less optimal decision-making profile. | 1 |
| [`Explody`](./Characters_and_Bosses.md#context-explody) | Block | Character Form: Behavior and stats for the 'Explody' state. | 1 |
| [`FightPhase`](./Characters_and_Bosses.md#context-fightphase) | Block | Boss Logic: Main combat phase. | 1 |
| `Fighter` | Block | Applies or references the 'Fighter' effect/state. | 1 |
| [`Fire`](./Characters_and_Bosses.md#context-fire) | Block | Character Form: Behavior and stats for the 'Fire' state. | 1 |
| [`FireFull`](./Characters_and_Bosses.md#context-firefull) | Block | Character Form: Behavior and stats for the 'FireFull' state. | 1 |
| [`Flop`](./Characters_and_Bosses.md#context-flop) | Block | Character Form: Behavior and stats for the 'Flop' state. | 1 |
| [`Flop2`](./Characters_and_Bosses.md#context-flop2) | Block | Character Form: Behavior and stats for the 'Flop2' state. | 1 |
| [`Flush`](./Characters_and_Bosses.md#context-flush) | Block | Character Form: Behavior and stats for the 'Flush' state. | 1 |
| [`FlushBubs`](./Characters_and_Bosses.md#context-flushbubs) | Block | Character Form: Behavior and stats for the 'FlushBubs' state. | 1 |
| [`FlushHost`](./Characters_and_Bosses.md#context-flushhost) | Block | Character Form: Behavior and stats for the 'FlushHost' state. | 1 |
| [`FlushNettle`](./Characters_and_Bosses.md#context-flushnettle) | Block | Character Form: Behavior and stats for the 'FlushNettle' state. | 1 |
| [`Grappling`](./Characters_and_Bosses.md#context-grappling) | Block | Character Form / AI State: Behavior while grappling an opponent. | 1 |
| [`Grown`](./Characters_and_Bosses.md#context-grown) | Block | Character Form: Behavior and stats for the 'Grown' state. | 1 |
| [`GuaranteedJackpot`](./Characters_and_Bosses.md#context-guaranteedjackpot) | Block | Loot Logic: Guarantees a high-tier drop. | 1 |
| [`Guarding`](./Characters_and_Bosses.md#context-guarding) | Block | Character Form / AI State: Defensive behavior state. | 1 |
| [`HalfDead`](./Characters_and_Bosses.md#context-halfdead) | Block | Character Form: Behavior and stats for the 'HalfDead' state. | 1 |
| [`HasDeadCat`](./Characters_and_Bosses.md#context-hasdeadcat) | Block | Character Form: Behavior and stats for the 'HasDeadCat' state. | 1 |
| [`HasRock`](./Characters_and_Bosses.md#context-hasrock) | Block | Character Form: Behavior and stats for the 'HasRock' state. | 1 |
| [`Headless`](./Characters_and_Bosses.md#context-headless) | Block | Character Form: Behavior and stats for the 'Headless' state. | 1 |
| [`Hint_CrackedVisuals`](./Characters_and_Bosses.md#context-hint_crackedvisuals) | Block | Visual: Overlay effects for cracked/damaged terrain or objects. | 1 |
| [`Hint_CrackedVisuals2`](./Characters_and_Bosses.md#context-hint_crackedvisuals2) | Block | Visual: Secondary cracked visual overlay. | 1 |
| [`Hint_CrackedVisuals3`](./Characters_and_Bosses.md#context-hint_crackedvisuals3) | Block | Visual: Tertiary cracked visual overlay. | 1 |
| [`HumanDead`](./Characters_and_Bosses.md#context-humandead) | Block | Character Form: Behavior and stats for the 'HumanDead' state. | 1 |
| `Hunter` | Block | Applies or references the 'Hunter' effect/state. | 1 |
| [`InitialPhase`](./Characters_and_Bosses.md#context-initialphase) | Block | Boss Logic: The starting phase of an encounter. | 1 |
| [`Insane_Ceiling`](./Characters_and_Bosses.md#context-insane_ceiling) | Block | Character Form: Insane behavior state while attached to the ceiling. | 1 |
| [`Insane_Ground`](./Characters_and_Bosses.md#context-insane_ground) | Block | Character Form: Insane behavior state while on the ground. | 1 |
| [`Johnny`](./Characters_and_Bosses.md#context-johnny) | Block | Character Form: Behavior and stats for the 'Johnny' state. | 1 |
| [`JohnnyBubs`](./Characters_and_Bosses.md#context-johnnybubs) | Block | Character Form: Behavior and stats for the 'JohnnyBubs' state. | 1 |
| [`JohnnyHost`](./Characters_and_Bosses.md#context-johnnyhost) | Block | Character Form: Behavior and stats for the 'JohnnyHost' state. | 1 |
| [`JohnnyNettle`](./Characters_and_Bosses.md#context-johnnynettle) | Block | Character Form: Behavior and stats for the 'JohnnyNettle' state. | 1 |
| [`Joystick`](./Characters_and_Bosses.md#context-joystick) | Block | Character Form: Behavior and stats for the 'Joystick' state. | 1 |
| [`LastHit`](./Characters_and_Bosses.md#context-lasthit) | Block | Logic: Executes logic on the final hit of a multi-hit attack. | 1 |
| [`Lifted`](./Characters_and_Bosses.md#context-lifted) | Block | Character Form: Behavior and stats for the 'Lifted' state. | 1 |
| [`Lit`](./Characters_and_Bosses.md#context-lit) | Block | Character Form: Behavior and stats for the 'Lit' state. | 1 |
| `Mage` | Block | Applies or references the 'Mage' effect/state. | 1 |
| `Medic` | Block | Applies or references the 'Medic' effect/state. | 1 |
| `Monk` | Block | Applies or references the 'Monk' effect/state. | 1 |
| [`Mounted`](./Characters_and_Bosses.md#context-mounted) | Block | Character Form: Behavior and stats for the 'Mounted' state. | 1 |
| [`MouthFull`](./Characters_and_Bosses.md#context-mouthfull) | Block | Character Form: Behavior and stats for the 'MouthFull' state. | 1 |
| [`Mutant`](./Characters_and_Bosses.md#context-mutant) | Block | Character Form: Behavior and stats for the 'Mutant' state. | 1 |
| `Necromancer` | Block | Applies or references the 'Necromancer' effect/state. | 1 |
| [`NeutronStar`](./Characters_and_Bosses.md#context-neutronstar) | Block | Character Form: Behavior and stats for the 'NeutronStar' state. | 1 |
| `NoDeathRattle` | Block | Applies or references the 'NoDeathRattle' effect/state. | 1 |
| [`NoEyes`](./Characters_and_Bosses.md#context-noeyes) | Block | Character Form: Behavior and stats for the 'NoEyes' state. | 1 |
| [`NoStick`](./Characters_and_Bosses.md#context-nostick) | Block | Character Form: Behavior and stats for the 'NoStick' state. | 1 |
| [`NormalFull`](./Characters_and_Bosses.md#context-normalfull) | Block | Character Form: Behavior and stats for the 'NormalFull' state. | 1 |
| [`Nuke`](./Characters_and_Bosses.md#context-nuke) | Block | Character Form: Behavior and stats for the 'Nuke' state. | 1 |
| [`Obey`](./Characters_and_Bosses.md#context-obey) | Block | AI State: Enforced compliance logic (e.g., when Charmed). | 1 |
| [`Off`](./Characters_and_Bosses.md#context-off) | Block | Character Form: Behavior and stats for the 'Off' state. | 1 |
| [`OffScreen`](./Characters_and_Bosses.md#context-offscreen) | Block | Character Form: Behavior and stats for the 'OffScreen' state. | 1 |
| [`OneEye`](./Characters_and_Bosses.md#context-oneeye) | Block | Character Form: Behavior and stats for the 'OneEye' state. | 1 |
| [`Open`](./Characters_and_Bosses.md#context-open) | Block | Character Form: Behavior and stats for the 'Open' state. | 1 |
| [`OpenCat`](./Characters_and_Bosses.md#context-opencat) | Block | Character Form: Behavior and stats for the 'OpenCat' state. | 1 |
| [`Out`](./Characters_and_Bosses.md#context-out) | Block | Character Form: Behavior and stats for the 'Out' state. | 1 |
| [`Possessing`](./Characters_and_Bosses.md#context-possessing) | Block | Character Form: Behavior and stats for the 'Possessing' state. | 1 |
| [`Primed`](./Characters_and_Bosses.md#context-primed) | Block | Character Form: Behavior and stats for the 'Primed' state. | 1 |
| `Psychic` | Block | Applies or references the 'Psychic' effect/state. | 1 |
| [`Pulp2`](./Characters_and_Bosses.md#context-pulp2) | Block | Character Form: Behavior and stats for the 'Pulp2' state. | 1 |
| [`Pulp3`](./Characters_and_Bosses.md#context-pulp3) | Block | Character Form: Behavior and stats for the 'Pulp3' state. | 1 |
| [`Pulp4`](./Characters_and_Bosses.md#context-pulp4) | Block | Character Form: Behavior and stats for the 'Pulp4' state. | 1 |
| [`Pulp5`](./Characters_and_Bosses.md#context-pulp5) | Block | Character Form: Behavior and stats for the 'Pulp5' state. | 1 |
| [`Pulp6`](./Characters_and_Bosses.md#context-pulp6) | Block | Character Form: Behavior and stats for the 'Pulp6' state. | 1 |
| [`Pulp7`](./Characters_and_Bosses.md#context-pulp7) | Block | Character Form: Behavior and stats for the 'Pulp7' state. | 1 |
| [`Sitting`](./Characters_and_Bosses.md#context-sitting) | Block | Character Form: Behavior and stats for the 'Sitting' state. | 1 |
| [`SmallHolding`](./Characters_and_Bosses.md#context-smallholding) | Block | Character Form: Behavior and stats for the 'SmallHolding' state. | 1 |
| [`SmallHoldingCat`](./Characters_and_Bosses.md#context-smallholdingcat) | Block | Character Form: Behavior and stats for the 'SmallHoldingCat' state. | 1 |
| [`SpawningPhase`](./Characters_and_Bosses.md#context-spawningphase) | Block | Boss Logic: Phase focused on summoning minions. | 1 |
| [`Standing`](./Characters_and_Bosses.md#context-standing) | Block | Character Form: Behavior and stats for the 'Standing' state. | 1 |
| [`Standing2`](./Characters_and_Bosses.md#context-standing2) | Block | Character Form: Behavior and stats for the 'Standing2' state. | 1 |
| [`Start_Ceiling`](./Characters_and_Bosses.md#context-start_ceiling) | Block | Character Form: Behavior and stats for the 'Start_Ceiling' state. | 1 |
| [`Stop`](./Characters_and_Bosses.md#context-stop) | Block | AI Movement: Forces the character to cease movement. | 1 |
| [`SwordAndShield`](./Characters_and_Bosses.md#context-swordandshield) | Block | Character Form: Behavior and stats for the 'SwordAndShield' state. | 1 |
| [`SwordAndShield_Primed`](./Characters_and_Bosses.md#context-swordandshield_primed) | Block | Character Form: Behavior and stats for the 'SwordAndShield_Primed' state. | 1 |
| `Tank` | Block | Applies or references the 'Tank' effect/state. | 1 |
| [`Tar`](./Characters_and_Bosses.md#context-tar) | Block | Character Form: Behavior and stats for the 'Tar' state. | 1 |
| [`TarFull`](./Characters_and_Bosses.md#context-tarfull) | Block | Character Form: Behavior and stats for the 'TarFull' state. | 1 |
| `Thief` | Block | Applies or references the 'Thief' effect/state. | 1 |
| [`Throb`](./Characters_and_Bosses.md#context-throb) | Block | Character Form: Behavior and stats for the 'Throb' state. | 1 |
| [`ThrobBubs`](./Characters_and_Bosses.md#context-throbbubs) | Block | Character Form: Behavior and stats for the 'ThrobBubs' state. | 1 |
| [`ThrobHost`](./Characters_and_Bosses.md#context-throbhost) | Block | Character Form: Behavior and stats for the 'ThrobHost' state. | 1 |
| [`ThrobNettle`](./Characters_and_Bosses.md#context-throbnettle) | Block | Character Form: Behavior and stats for the 'ThrobNettle' state. | 1 |
| `Tinkerer` | Block | Applies or references the 'Tinkerer' effect/state. | 1 |
| [`Transformed`](./Characters_and_Bosses.md#context-transformed) | Block | Character Form: Behavior and stats for the 'Transformed' state. | 1 |
| [`TwoEyes`](./Characters_and_Bosses.md#context-twoeyes) | Block | Character Form: Behavior and stats for the 'TwoEyes' state. | 1 |
| [`Unlit`](./Characters_and_Bosses.md#context-unlit) | Block | Character Form: Behavior and stats for the 'Unlit' state. | 1 |
| `Unmounted` | Block | Applies or references the 'Unmounted' effect/state. | 1 |
| [`Unwashed`](./Characters_and_Bosses.md#context-unwashed) | Block | Character Form: Behavior and stats for the 'Unwashed' state. | 1 |
| [`Washed`](./Characters_and_Bosses.md#context-washed) | Block | Character Form: Behavior and stats for the 'Washed' state. | 1 |
| [`Washer`](./Characters_and_Bosses.md#context-washer) | Block | Character Form: Behavior and stats for the 'Washer' state. | 1 |
| [`Water`](./Characters_and_Bosses.md#context-water) | Block | Character Form: Behavior and stats for the 'Water' state. | 1 |
| [`WereMan`](./Characters_and_Bosses.md#context-wereman) | Block | Character Form: Behavior and stats for the 'WereMan' state. | 1 |
| [`Zealot`](./Characters_and_Bosses.md#context-zealot) | Block | Character Form: Behavior and stats for the 'Zealot' state. | 1 |
| [`ZealotBomb`](./Characters_and_Bosses.md#context-zealotbomb) | Block | Character Form: Behavior and stats for the 'ZealotBomb' state. | 1 |
| `sync_brain_patterns` | Boolean |  | 1 |

</details>

---

### Context: `FormChangeWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/35) |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum/String | ID of the status effect to apply or check. | 35 |
| [`form_hasnot`](./Enums.md#enum-form_hasnot) | Enum/String |  | 30 |
| [`form_has`](./Enums.md#enum-form_has) | Enum/String |  | 25 |

</details>

---

### Context: `Default`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/24) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 24 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 10 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| `partial_animation_suffix` | String |  | 1 |

</details>

---

### Context: `mainturn_pattern`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count (X/23) |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum/String |  | 23 |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 9 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 8 |
| [`do_strict`](./Arrays.md#array-do_strict) | Array |  | 2 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum/String |  | 2 |

</details>

---

### Context: `turns`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Bishop`](./Characters_and_Bosses.md#context-bishop), [`Bully`](./Characters_and_Bosses.md#context-bully), [`Default`](./Characters_and_Bosses.md#context-default), [`Default_Ceiling`](./Characters_and_Bosses.md#context-default_ceiling), [`Default_Ground`](./Characters_and_Bosses.md#context-default_ground), [`FightPhase`](./Characters_and_Bosses.md#context-fightphase), [`Holding`](./Characters_and_Bosses.md#context-holding), [`InitialPhase`](./Characters_and_Bosses.md#context-initialphase), [`Insane_Ceiling`](./Characters_and_Bosses.md#context-insane_ceiling), [`Insane_Ground`](./Characters_and_Bosses.md#context-insane_ground), [`LastHit`](./Characters_and_Bosses.md#context-lasthit), [`Lifted`](./Characters_and_Bosses.md#context-lifted), [`Mutant`](./Characters_and_Bosses.md#context-mutant), [`Normal`](./Characters_and_Bosses.md#context-normal), [`NotPriming`](./Characters_and_Bosses.md#context-notpriming), [`Nuke`](./Characters_and_Bosses.md#context-nuke), [`OffMap`](./Characters_and_Bosses.md#context-offmap), [`OffScreen`](./Characters_and_Bosses.md#context-offscreen), [`OneAlive`](./Characters_and_Bosses.md#context-onealive), [`Possessing`](./Characters_and_Bosses.md#context-possessing), [`Priming`](./Characters_and_Bosses.md#context-priming), [`Pulp2`](./Characters_and_Bosses.md#context-pulp2), [`Pulp3`](./Characters_and_Bosses.md#context-pulp3), [`Pulp4`](./Characters_and_Bosses.md#context-pulp4), [`Pulp5`](./Characters_and_Bosses.md#context-pulp5), [`Pulp6`](./Characters_and_Bosses.md#context-pulp6), [`Pulp7`](./Characters_and_Bosses.md#context-pulp7), [`Rage`](./Characters_and_Bosses.md#context-rage), [`Sitting`](./Characters_and_Bosses.md#context-sitting), [`SpawningPhase`](./Characters_and_Bosses.md#context-spawningphase), [`Standing`](./Characters_and_Bosses.md#context-standing), [`Standing2`](./Characters_and_Bosses.md#context-standing2), [`TwoAlive`](./Characters_and_Bosses.md#context-twoalive)

| Property Key | Type | Definition | Count (X/23) |
| :--- | :--- | :--- | :--- |
| `takes_turns` | Boolean |  | 23 |
| `dispersed_bonus_turns` | Number |  | 18 |
| `takes_main_turn` | Boolean |  | 10 |
| `evenly_dispersed_bonus_turns` | Number |  | 7 |
| `round_end_bonus_turns` | Number |  | 5 |
| `wait_till_next_round_to_update_turns` | Boolean |  | 4 |
| `round_start_bonus_turns` | Number |  | 1 |

</details>

---

### Context: `BossRewards`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/20) |
| :--- | :--- | :--- | :--- |
| [`common`](./Enums.md#enum-common) | Enum/String |  | 20 |
| [`rare`](./Enums.md#enum-rare) | Enum/String |  | 16 |

</details>

---

### Context: `bonusturn_pattern`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count (X/19) |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum/String |  | 19 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 11 |
| [`do_strict`](./Arrays.md#array-do_strict) | Array |  | 5 |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 4 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum/String |  | 1 |

</details>

---

### Context: `BirdRewards`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/18) |
| :--- | :--- | :--- | :--- |
| [`ally_rewards`](./Characters_and_Bosses.md#context-ally_rewards) | Block | Loot logic triggered if an ally dies. | 18 |
| [`statuses`](./Characters_and_Bosses.md#context-statuses) | Block | Status effects possessed by the character. | 5 |

</details>

---

### Context: `CatPartsTransform`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveGroup`](./Characters_and_Bosses.md#context-passivegroup), [`StacyMutant_Brace`](./Characters_and_Bosses.md#context-stacymutant_brace), [`StacyMutant_Counter`](./Characters_and_Bosses.md#context-stacymutant_counter), [`StacyMutant_Damage`](./Characters_and_Bosses.md#context-stacymutant_damage), [`StacyMutant_DoubleHead`](./Characters_and_Bosses.md#context-stacymutant_doublehead), [`StacyMutant_Fire`](./Characters_and_Bosses.md#context-stacymutant_fire), [`StacyMutant_Health`](./Characters_and_Bosses.md#context-stacymutant_health), [`StacyMutant_Holy`](./Characters_and_Bosses.md#context-stacymutant_holy), [`StacyMutant_Ice`](./Characters_and_Bosses.md#context-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#context-stacymutant_lightning), [`StacyMutant_Mirror`](./Characters_and_Bosses.md#context-stacymutant_mirror), [`StacyMutant_Speed`](./Characters_and_Bosses.md#context-stacymutant_speed), [`StacyMutant_Thorns`](./Characters_and_Bosses.md#context-stacymutant_thorns), [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/16) |
| :--- | :--- | :--- | :--- |
| [`palette`](./Enums.md#enum-palette) | Enum/String |  | 16 |
| `arm1` | Number | Sprite variant ID for the front arm. | 3 |
| `arm2` | Number |  | 3 |
| `body` | Number | Sprite variant ID for the body. | 3 |
| `ear1` | Number | Sprite variant ID for the front ear. | 3 |
| `head` | Number | Sprite variant ID for the head. | 3 |
| `leg1` | Number | Sprite variant ID for the front leg. | 3 |
| `leg2` | Number |  | 3 |
| `tail` | Number | Sprite variant ID for the tail. | 3 |
| `texture` | Number |  | 3 |
| `eye1` | Number |  | 2 |
| `eye2` | Number |  | 2 |
| `ear2` | Number |  | 1 |

</details>

---

### Context: `CharacterLightSource`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/16) |
| :--- | :--- | :--- | :--- |
| [`color`](./Arrays.md#array-color) | Array |  | 16 |
| `size` | Number |  | 16 |
| [`glow`](./Arrays.md#array-glow) | Array |  | 8 |

</details>

---

### Context: `ally_rewards`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BirdRewards`](./Characters_and_Bosses.md#context-birdrewards)

| Property Key | Type | Definition | Count (X/16) |
| :--- | :--- | :--- | :--- |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum/String | Generates an item drop from the specified loot pool. | 16 |
| [`Conditional_GoodRoll`](./Characters_and_Bosses.md#context-conditional_goodroll) | Block | Conditional: Executes logic on a good RNG roll. | 2 |
| [`RandomStatusFromPool`](./Characters_and_Bosses.md#context-randomstatusfrompool) | Block | Logic: Applies a random status from the pool. | 1 |

</details>

---

### Context: `equipment`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count (X/16) |
| :--- | :--- | :--- | :--- |
| [`face`](./Enums.md#enum-face) | Enum/String |  | 16 |
| [`head`](./Enums.md#enum-head) | Enum/String |  | 14 |
| [`neck`](./Enums.md#enum-neck) | Enum/String |  | 10 |
| [`weapon`](./Enums.md#enum-weapon) | Enum/String | Weapon item constraint. | 7 |

</details>

---

### Context: `HealthPickup`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/15) |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array |  | 15 |
| `stacks` | Number | Number of stacks or intensity to apply. | 15 |
| `stored_food_value` | Number |  | 15 |
| `anything_eats` | Boolean |  | 4 |
| `force_frame` | Number |  | 1 |

</details>

---

### Context: `ImmediateAbilityReaction`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/13) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 13 |
| `ability_damage_only` | Boolean |  | 6 |
| `backstabs_only` | Boolean |  | 2 |
| `damage_threshold` | Number |  | 2 |
| `even_if_blocked` | Boolean |  | 2 |
| `even_if_stunned` | Boolean |  | 2 |
| `health_threshold` | Number |  | 2 |
| `buddy_damage_only` | Boolean |  | 1 |
| `target_furthest_valid` | Boolean |  | 1 |

</details>

---

### Context: `AbilityHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 12 |
| [`threshold`](./Enums.md#enum-threshold) | Enum/String |  | 11 |
| `even_if_stunned` | Boolean |  | 6 |
| `immediate` | Boolean |  | 5 |
| `use_ai` | Boolean |  | 2 |
| `also_use_if_buddy_is_dead` | Boolean |  | 1 |
| [`threshold_min`](./Enums.md#enum-threshold_min) | Enum/String |  | 1 |

</details>

---

### Context: `PassiveGroup`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#context-randompassivepool)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 12 |
| [`FormChange`](./Enums.md#enum-formchange) | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 12 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum/String | Applies or references the 'ReplaceBasicAttack' effect/state. | 11 |
| `SelfStatusCarefulness` | Number | Applies or references the 'SelfStatusCarefulness' effect/state. | 2 |
| `StatusCarefulness` | Number | Applies or references the 'StatusCarefulness' effect/state. | 2 |
| `ExtraBasicAttacks` | Number | Applies or references the 'ExtraBasicAttacks' effect/state. | 1 |
| [`TinkererBasicAttackSwitching`](./Characters_and_Bosses.md#context-tinkererbasicattackswitching) | Block | Logic: Allows Tinkerer to swap basic attacks. | 1 |

</details>

---

### Context: `RandomPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| [`PassiveGroup`](./Characters_and_Bosses.md#context-passivegroup) | Block | Passive: A collection of passives grouped together for easier management. | 12 |
| [`AddStatusToBasicAttack`](./Characters_and_Bosses.md#context-addstatustobasicattack) | Block | Modifier: Injects a status effect payload into the character's basic attacks. | 10 |
| [`TransformInXTurns`](./Characters_and_Bosses.md#context-transforminxturns) | Block | Logic: Forces a form change after X turns. | 2 |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 12 |
| `good` | Boolean |  | 8 |
| `spawn_on_death_hit` | Boolean |  | 6 |
| `chance` | Number | Probability (0.0 to 1.0) of executing this action. | 4 |
| `coins` | Number |  | 2 |
| [`auto_cast`](./Enums.md#enum-auto_cast) | Enum/String |  | 1 |
| `consider_all_layers` | Boolean |  | 1 |
| `melee_ability_only` | Boolean |  | 1 |

</details>

---

### Context: `fallback`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum/String |  | 12 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 6 |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 1 |
| [`do_best`](./Arrays.md#array-do_best) | Array |  | 1 |
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array |  | 1 |
| [`do_random`](./Arrays.md#array-do_random) | Array |  | 1 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum/String |  | 1 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#context-temppassiveuntilsettled), [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/11) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 11 |
| [`effects`](./Characters_and_Bosses.md#context-effects) | Block | Non-damaging impact triggers. | 11 |
| `knockback` | Number |  | 9 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification/category type. | 8 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 5 |
| `cant_miss` | Boolean |  | 1 |

</details>

---

### Context: `Normal`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/10) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 10 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 5 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 2 |
| `animation_suffix` | String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `AbilityReaction`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 9 |
| `ability_damage_only` | Boolean |  | 6 |
| `backstabs_only` | Boolean |  | 3 |
| `only_when_not_your_turn` | Boolean |  | 3 |
| `cancel_knockback` | Boolean |  | 1 |
| `enemies_only` | Boolean |  | 1 |
| `even_on_0_damage` | Boolean |  | 1 |
| `even_on_0_damage_if_knockback` | Boolean |  | 1 |
| `match_knockback_direction` | Boolean |  | 1 |
| `ranged_only` | Boolean |  | 1 |
| `verify_target` | Boolean |  | 1 |

</details>

---

### Context: `FormChangeOnElementInfluence`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String | Specific element type required or applied. | 9 |
| [`form`](./Enums.md#enum-form) | Enum/String |  | 9 |
| [`exclude`](./Enums.md#enum-exclude) | Enum/String |  | 5 |
| [`particle`](./Enums.md#enum-particle) | Enum/String |  | 5 |
| [`sfx`](./Enums.md#enum-sfx) | Enum/String |  | 5 |

</details>

---

### Context: `TransformOnElementInfluence`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/9) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String | Specific element type required or applied. | 9 |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 9 |

</details>

---

### Context: `DeathRattle`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/8) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 8 |
| `is_dying_animation` | Boolean |  | 7 |
| `pop_corpse` | Boolean |  | 6 |
| `cancel_knockback` | Boolean |  | 1 |
| `immediate` | Boolean |  | 1 |
| `must_target_killer` | Boolean |  | 1 |
| `target_killer` | Boolean |  | 1 |

</details>

---

### Context: `DeathRattleRevive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/8) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 8 |
| `even_if_stunned` | Boolean |  | 8 |

</details>

---

### Context: `FormChangeOffMap`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/8) |
| :--- | :--- | :--- | :--- |
| [`form_offmap`](./Enums.md#enum-form_offmap) | Enum/String |  | 8 |
| [`form_onmap`](./Enums.md#enum-form_onmap) | Enum/String |  | 8 |

</details>

---

### Context: `Rage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/8) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 8 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 6 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 6 |
| `partial_animation_suffix` | String |  | 4 |
| `animation_suffix` | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `move_speed_multiplier` | Number |  | 1 |

</details>

---

### Context: `TransformInXTurns`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#context-randompassivepool), [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/8) |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array |  | 8 |
| `stacks` | Number | Number of stacks or intensity to apply. | 8 |
| [`initiative`](./Enums.md#enum-initiative) | Enum/String |  | 4 |
| [`animation`](./Enums.md#enum-animation) | Enum/String |  | 2 |
| [`turns`](./Arrays.md#array-turns) | Array | Turn counter tracking. | 1 |

</details>

---

### Context: `ChanceToSpitOnDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 7 |
| `flat_chance` | Number |  | 5 |
| `chance_per_damage` | Number |  | 3 |
| `backstabs_only` | Boolean |  | 1 |
| `even_on_0_damage_if_knockback` | Boolean |  | 1 |

</details>

---

### Context: `MoveWhenDamaged`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum/String |  | 7 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum/String |  | 1 |

</details>

---

### Context: `MovementReaction`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 7 |
| `enemies_only` | Boolean |  | 3 |
| `objects_too` | Boolean |  | 2 |
| `on_self_move_too` | Boolean |  | 2 |
| `blind_spot` | Boolean |  | 1 |
| `forward_only` | Boolean |  | 1 |
| `self_move_exclude_self_abilities` | Boolean |  | 1 |

</details>

---

### Context: `ReflectProjectiles`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| `self_damage` | Number | Recoil or self-inflicted damage/effects applied to the caster. | 7 |

</details>

---

### Context: `StatusCollector`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/7) |
| :--- | :--- | :--- | :--- |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. | 7 |
| `Poison` | Number | Applies or references the 'Poison' effect/state. | 4 |
| `Slow` | Number | Applies or references the 'Slow' effect/state. | 4 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#context-randompassivepool), [`StacyMutant_Counter`](./Characters_and_Bosses.md#context-stacymutant_counter), [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. | 6 |
| `Burn` | Number | Applies or references the 'Burn' effect/state. | 4 |
| `Poison` | Number | Applies or references the 'Poison' effect/state. | 4 |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 2 |
| `Fear` | Number | Applies or references the 'Fear' effect/state. | 2 |
| `RemoteLeech` | Number | Applies or references the 'RemoteLeech' effect/state. | 2 |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. | 1 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 1 |
| [`GainDisorderFromPool`](./Characters_and_Bosses.md#context-gaindisorderfrompool) | Block | Logic: Applies a negative mutation/disorder from a specific pool. | 1 |
| `Knockback` | Number | Applies or references the 'Knockback' effect/state. | 1 |
| `Leech` | Number | Applies or references the 'Leech' effect/state. | 1 |
| `Madness` | Number | Applies the Madness debuff/status effect. | 1 |
| `Possessed` | Number | Applies or references the 'Possessed' effect/state. | 1 |
| `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. | 1 |
| `RemoteFlatLeech` | Number | Applies or references the 'RemoteFlatLeech' effect/state. | 1 |
| `Rot` | Number | Applies or references the 'Rot' effect/state. | 1 |
| `Slow` | Number | Applies or references the 'Slow' effect/state. | 1 |
| `Stun` | Number | Applies or references the 'Stun' effect/state. | 1 |
| `Weakness` | Number | Applies or references the 'Weakness' effect/state. | 1 |

</details>

---

### Context: `CaveFamilyEnrage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 6 |
| `count` | Number | The numerical quantity. | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum/String | Specific entity tag required. | 6 |

</details>

---

### Context: `FormChangeWhilePrimingAbility`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| [`not_priming`](./Enums.md#enum-not_priming) | Enum/String |  | 6 |
| [`priming`](./Enums.md#enum-priming) | Enum/String |  | 6 |

</details>

---

### Context: `round_end_bonusturn_pattern`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 6 |
| [`do`](./Enums.md#enum-do) | Enum/String |  | 3 |
| [`do_one`](./Arrays.md#array-do_one) | Array |  | 2 |
| [`do_random`](./Arrays.md#array-do_random) | Array |  | 2 |
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array |  | 1 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 1 |

</details>

---

### Context: `HasCat`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 5 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 5 |
| `animation_suffix` | String |  | 4 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 4 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| `partial_animation_suffix` | String |  | 1 |

</details>

---

### Context: `PassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 5 |
| [`status`](./Enums.md#enum-status) | Enum/String | ID of the status effect to apply or check. | 5 |

</details>

---

### Context: `SecurityBotProtect`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 5 |
| `enemies_only` | Boolean |  | 3 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 3 |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum/String |  | 3 |
| `not_on_kill` | Boolean |  | 2 |

</details>

---

### Context: `alt_spawn_pool`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| [`Antidote`](./Enums.md#enum-antidote) | Enum/String | Applies or references the 'Antidote' effect/state. | 5 |
| [`Blessing`](./Enums.md#enum-blessing) | Enum/String | Applies or references the 'Blessing' effect/state. | 5 |
| `BigCatnip` | Number | Applies or references the 'BigCatnip' effect/state. | 4 |
| `BigScrap` | Number | Applies or references the 'BigScrap' effect/state. | 4 |
| `BiggestFood` | Number | Applies or references the 'BiggestFood' effect/state. | 4 |
| `Coin` | Number | Applies or references the 'Coin' effect/state. | 4 |
| `BigFood` | Number | Applies or references the 'BigFood' effect/state. | 2 |
| `Coin10` | Number | Applies or references the 'Coin10' effect/state. | 2 |
| `Coin3` | Number | Applies or references the 'Coin3' effect/state. | 2 |
| `Coin4` | Number | Applies or references the 'Coin4' effect/state. | 2 |
| `MedCatnip` | Number | Applies or references the 'MedCatnip' effect/state. | 2 |
| `MedScrap` | Number | Applies or references the 'MedScrap' effect/state. | 2 |
| `RandomArmorPickup` | Number | Applies or references the 'RandomArmorPickup' effect/state. | 2 |
| `RandomCatnipPickup` | Number | Applies or references the 'RandomCatnipPickup' effect/state. | 2 |
| `RandomFoodPickup` | Number | Applies or references the 'RandomFoodPickup' effect/state. | 2 |
| `Bear` | Number | Applies or references the 'Bear' effect/state. | 1 |
| `BlackBird` | Number | Applies or references the 'BlackBird' effect/state. | 1 |
| `Catepillar` | Number | Applies or references the 'Catepillar' effect/state. | 1 |
| `Catnip` | Number | Applies or references the 'Catnip' effect/state. | 1 |
| `CharmedDip` | Number | Applies or references the 'CharmedDip' effect/state. | 1 |
| `CharmedFloater` | Number | Applies or references the 'CharmedFloater' effect/state. | 1 |
| `CharmedPile` | Number | Applies or references the 'CharmedPile' effect/state. | 1 |
| `Cherub` | Number | Applies or references the 'Cherub' effect/state. | 1 |
| `Chicken` | Number | Applies or references the 'Chicken' effect/state. | 1 |
| `Coin2` | Number | Applies or references the 'Coin2' effect/state. | 1 |
| `Dove` | Number | Applies or references the 'Dove' effect/state. | 1 |
| `Eagle` | Number | Applies or references the 'Eagle' effect/state. | 1 |
| `Food` | Number | Applies or references the 'Food' effect/state. | 1 |
| `Harpy` | Number | Applies or references the 'Harpy' effect/state. | 1 |
| `HummingBird` | Number | Applies or references the 'HummingBird' effect/state. | 1 |
| `LargeBirdPool` | Number | Applies or references the 'LargeBirdPool' effect/state. | 1 |
| `MedBirdPool` | Number | Applies or references the 'MedBirdPool' effect/state. | 1 |
| `Mutant` | Number | Character Form: Behavior and stats for the 'Mutant' state. | 1 |
| `Pigeon` | Number | Applies or references the 'Pigeon' effect/state. | 1 |
| `RandomBiggerArmorPickup` | Number | Applies or references the 'RandomBiggerArmorPickup' effect/state. | 1 |
| `RandomBiggerCatnipPickup` | Number | Applies or references the 'RandomBiggerCatnipPickup' effect/state. | 1 |
| `RandomBiggerFoodPickup` | Number | Applies or references the 'RandomBiggerFoodPickup' effect/state. | 1 |
| `Raven` | Number | Applies or references the 'Raven' effect/state. | 1 |
| `Scrap` | Number | Applies or references the 'Scrap' effect/state. | 1 |
| `Seagull` | Number | Applies or references the 'Seagull' effect/state. | 1 |
| `SmallBirdPool` | Number | Applies or references the 'SmallBirdPool' effect/state. | 1 |
| `Snake` | Number | Applies or references the 'Snake' effect/state. | 1 |
| `Squirrel` | Number | Applies or references the 'Squirrel' effect/state. | 1 |
| `Toad` | Number | Applies or references the 'Toad' effect/state. | 1 |
| `Turkey` | Number | Applies or references the 'Turkey' effect/state. | 1 |
| `Turtle` | Number | Applies or references the 'Turtle' effect/state. | 1 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Characters_and_Bosses.md#context-meleerevengedamage), [`damage_instance`](./Characters_and_Bosses.md#context-damage_instance), [`eat_damage`](./Characters_and_Bosses.md#context-eat_damage)

| Property Key | Type | Definition | Count (X/5) |
| :--- | :--- | :--- | :--- |
| `Burn` | Number | Applies or references the 'Burn' effect/state. | 5 |
| `Stun` | Number | Applies or references the 'Stun' effect/state. | 2 |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. | 2 |
| `BlackHoleSuck` | Number | Applies or references the 'BlackHoleSuck' effect/state. | 1 |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. | 1 |
| `ConstitutionUp` | Number | Applies or references the 'ConstitutionUp' effect/state. | 1 |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. | 1 |

</details>

---

### Context: `BaitAura`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `range` | Number | Distance or area of effect in tiles. | 4 |

</details>

---

### Context: `Consumed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`statuses`](./Characters_and_Bosses.md#context-statuses)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `do_not_pop_corpse` | Boolean |  | 4 |
| [`drop_on_death`](./Enums.md#enum-drop_on_death) | Enum/String |  | 4 |
| `force_contact` | Boolean | If true, enforces physical overlap. | 4 |
| `instant` | Boolean |  | 4 |
| [`mount_mode`](./Enums.md#enum-mount_mode) | Enum/String | If true, treats the consumption as riding/mounting instead of eating. | 4 |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum/String | Ability triggered by the consumed entity while inside the consumer. | 4 |
| `use_placeholder` | Boolean |  | 2 |

</details>

---

### Context: `MoveAway`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 4 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 4 |

</details>

---

### Context: `MoveClose`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 4 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 4 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum/String |  | 3 |

</details>

---

### Context: `SmallRockBehavior`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 4 |
| `knockback` | Number |  | 4 |
| `chain` | Boolean |  | 2 |

</details>

---

### Context: `StatusGroup`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Characters_and_Bosses.md#context-randomstatusfrompool)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum/String | Generates an item drop from the specified loot pool. | 4 |

</details>

---

### Context: `TransformOnDeathImmediately`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum/String |  | 4 |
| [`obj`](./Enums.md#enum-obj) | Enum/String |  | 4 |

</details>

---

### Context: `Trapper`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 4 |
| `cancel_movement` | Boolean |  | 2 |
| `pathfinding_avoidance` | Number |  | 2 |
| `range` | Number | Distance or area of effect in tiles. | 2 |

</details>

---

### Context: `hot`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 4 |
| `name` | String | Localization key for the character's name. | 4 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 4 |

</details>

---

### Context: `statuses`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BirdRewards`](./Characters_and_Bosses.md#context-birdrewards), [`Cat`](./Characters_and_Bosses.md#context-cat), [`NonCat`](./Characters_and_Bosses.md#context-noncat)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`Consumed`](./Characters_and_Bosses.md#context-consumed) | Block | State triggered when the entity is eaten/consumed. | 4 |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 3 |

</details>

---

### Context: `virtual_abilities`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`MoveAway`](./Characters_and_Bosses.md#context-moveaway) | Block | AI Movement: Moves away from the target. | 4 |
| [`MoveClose`](./Characters_and_Bosses.md#context-moveclose) | Block | AI Movement: Moves into melee range. | 4 |
| [`DashRandomly`](./Characters_and_Bosses.md#context-dashrandomly) | Block | AI Movement: Dashes to a random valid tile. | 2 |
| [`Escape`](./Characters_and_Bosses.md#context-escape) | Block | AI Movement: Logic for fleeing or escaping the map. | 2 |
| [`MoveCenter`](./Characters_and_Bosses.md#context-movecenter) | Block | AI Movement: Moves toward the center of the map. | 2 |
| [`MoveForThrow`](./Characters_and_Bosses.md#context-moveforthrow) | Block | AI Movement: Repositions to gain line of sight for throwing. | 2 |
| [`SpearRun`](./Characters_and_Bosses.md#context-spearrun) | Block | AI Movement: Specific movement logic for Spear enemies. | 2 |
| [`CerberubsJumpBlind`](./Characters_and_Bosses.md#context-cerberubsjumpblind) | Block | AI Logic: Blind jump attack pattern for Cerberubs. | 1 |
| [`CerberubsJumpNormal`](./Characters_and_Bosses.md#context-cerberubsjumpnormal) | Block | AI Logic: Normal jump attack pattern for Cerberubs. | 1 |
| [`CloseConvert`](./Characters_and_Bosses.md#context-closeconvert) | Block | AI State: Logic for converting adjacent units. | 1 |
| [`FoodMove`](./Characters_and_Bosses.md#context-foodmove) | Block | AI Movement: Logic for seeking out food items. | 1 |
| [`ForceTrample`](./Characters_and_Bosses.md#context-forcetrample) | Block | Logic: Forces movement to act as a trample attack. | 1 |
| [`LeapClose`](./Characters_and_Bosses.md#context-leapclose) | Block | AI Movement: Executes a jumping maneuver to close distance. | 1 |
| [`MoveForBarrage`](./Characters_and_Bosses.md#context-moveforbarrage) | Block | AI Movement: Repositions to optimize a barrage attack. | 1 |
| [`MoveForDash`](./Characters_and_Bosses.md#context-movefordash) | Block | AI Movement: Repositions to set up a dash attack line. | 1 |
| [`MoveForGrass`](./Characters_and_Bosses.md#context-moveforgrass) | Block | AI Movement: Moves toward grass tiles. | 1 |
| [`MoveForPounce`](./Characters_and_Bosses.md#context-moveforpounce) | Block | AI Movement: Repositions to optimize a pounce trajectory. | 1 |
| [`MoveForSpin`](./Characters_and_Bosses.md#context-moveforspin) | Block | AI Movement: Repositions into a cluster of enemies for a spin attack. | 1 |
| [`MoveOneForPuke`](./Characters_and_Bosses.md#context-moveoneforpuke) | Block | AI Movement: Specific positioning logic for puke attacks. | 1 |
| [`MoveSpaced`](./Characters_and_Bosses.md#context-movespaced) | Block | AI Movement: Moves to maintain a specific distance from targets. | 1 |
| [`MoveToHead`](./Characters_and_Bosses.md#context-movetohead) | Block | AI Movement: Navigates toward the 'head' or primary target. | 1 |
| [`MoveTowards`](./Characters_and_Bosses.md#context-movetowards) | Block | AI Movement: Moves toward the nearest target. | 1 |
| [`NCGravecrawlFAR`](./Characters_and_Bosses.md#context-ncgravecrawlfar) | Block | AI Movement: Specific grapple/crawl logic. | 1 |
| [`ReturnA`](./Characters_and_Bosses.md#context-returna) | Block | Boss Logic: Specific phase return trigger. | 1 |
| [`RunFar`](./Characters_and_Bosses.md#context-runfar) | Block | AI Movement: Maximize distance from targets. | 1 |
| [`SuckMF`](./Characters_and_Bosses.md#context-suckmf) | Block | Character Form: Behavior and stats for the 'SuckMF' state. | 1 |
| [`TF_TargetAllies`](./Characters_and_Bosses.md#context-tf_targetallies) | Block | AI Targeting: Prioritizes allies. | 1 |
| [`TF_TargetEnemies`](./Characters_and_Bosses.md#context-tf_targetenemies) | Block | AI Targeting: Prioritizes enemies. | 1 |
| [`Unflip`](./Characters_and_Bosses.md#context-unflip) | Block | Logic: Reverses a flipped state. | 1 |

</details>

---

### Context: `AllAlive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |

</details>

---

### Context: `ArmorPickup`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array |  | 3 |
| `stacks` | Number | Number of stacks or intensity to apply. | 3 |

</details>

---

### Context: `Buddy`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 3 |
| [`obj`](./Enums.md#enum-obj) | Enum/String |  | 3 |
| `reclaim_if_lost` | Boolean |  | 1 |

</details>

---

### Context: `Cat`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#context-mothertumorpassive), [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#context-mothertumorspawnincapture)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum/String |  | 3 |
| [`statuses`](./Characters_and_Bosses.md#context-statuses) | Block | Status effects possessed by the character. | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum/String |  | 1 |

</details>

---

### Context: `Down`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| `animation_suffix` | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |

</details>

---

### Context: `FormChangeHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`form_above`](./Enums.md#enum-form_above) | Enum/String |  | 3 |
| [`form_below`](./Enums.md#enum-form_below) | Enum/String |  | 3 |
| `threshold` | Number |  | 3 |
| `count_shield` | Boolean |  | 1 |

</details>

---

### Context: `ManaPickup`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array |  | 3 |
| `stacks` | Number | Number of stacks or intensity to apply. | 3 |

</details>

---

### Context: `MoveTowardsKillers`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`character_filter`](./Arrays.md#array-character_filter) | Array |  | 3 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum/String |  | 3 |

</details>

---

### Context: `NonCat`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#context-mothertumorpassive), [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#context-mothertumorspawnincapture)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum/String |  | 3 |
| [`statuses`](./Characters_and_Bosses.md#context-statuses) | Block | Status effects possessed by the character. | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum/String |  | 1 |

</details>

---

### Context: `OffMap`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 3 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `OneAlive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 3 |

</details>

---

### Context: `ReplaceBrain`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StacyMutant_Fire`](./Characters_and_Bosses.md#context-stacymutant_fire), [`StacyMutant_Ice`](./Characters_and_Bosses.md#context-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#context-stacymutant_lightning)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum/String |  | 3 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum/String |  | 3 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 3 |
| [`pattern`](./Characters_and_Bosses.md#context-pattern) | Block | AI sequence logic. | 3 |

</details>

---

### Context: `SpawnOnDeath`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum/String |  | 3 |
| [`obj`](./Arrays.md#array-obj) | Array |  | 3 |
| [`additional_statuses`](./Characters_and_Bosses.md#context-additional_statuses) | Block | Generic statuses added to the character. | 1 |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`UseAbility_NonStack`](./Enums.md#enum-useability_nonstack) | Enum/String | Applies or references the 'UseAbility_NonStack' effect/state. | 3 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 2 |

</details>

---

### Context: `TwoAlive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 3 |

</details>

---

### Context: `Up`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| `animation_suffix` | String |  | 2 |
| `tooltip` | String |  | 1 |

</details>

---

### Context: `default`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |

</details>

---

### Context: `dispersed_bonusturn_pattern`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum/String |  | 3 |

</details>

---

### Context: `1`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| `animation_suffix` | Number |  | 1 |
| `partial_animation_suffix` | Number |  | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `2`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 2 |
| `partial_animation_suffix` | Number |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| `animation_suffix` | Number |  | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `3`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 2 |
| `partial_animation_suffix` | Number |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| `animation_suffix` | Number |  | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `AbilityOnRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 2 |
| `force_display_name` | Boolean |  | 2 |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 2 |
| `range` | Number | Distance or area of effect in tiles. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum/String | Specific entity tag required. | 2 |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Fury` | Number | Applies or references the 'Fury' effect/state. | 2 |

</details>

---

### Context: `Big`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum/String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Boris`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `BungaEntrance`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 2 |
| `even_if_stunned` | Boolean |  | 2 |
| `health_threshold` | Number |  | 2 |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum/String |  | 2 |

</details>

---

### Context: `CaveMan`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| `animation_suffix` | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| `name` | String | Localization key for the character's name. | 1 |
| `tooltip` | String |  | 1 |

</details>

---

### Context: `CaveManSpear`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| `animation_suffix` | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| `name` | String | Localization key for the character's name. | 1 |
| `tooltip` | String |  | 1 |

</details>

---

### Context: `CherubimReaction`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Leave`](./Enums.md#enum-leave) | Enum/String | Applies or references the 'Leave' effect/state. | 2 |
| [`Return`](./Enums.md#enum-return) | Enum/String | Applies or references the 'Return' effect/state. | 2 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ally_rewards`](./Characters_and_Bosses.md#context-ally_rewards)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum/String | Generates an item drop from the specified loot pool. | 2 |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 2 |

</details>

---

### Context: `DashRandomly`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 2 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum/String |  | 2 |

</details>

---

### Context: `Empty`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 2 |

</details>

---

### Context: `Escape`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 2 |

</details>

---

### Context: `Explosive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `FinalBossHitCountdownBoris`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Logic: Forces the execution of a specific ability. | 2 |
| `icon` | Number |  | 1 |
| `icon_ready` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `FinalBossHitCountdownExplosive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Logic: Forces the execution of a specific ability. | 2 |
| `icon` | Number |  | 1 |
| `icon_ready` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `ForceUseAbility`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 2 |
| `show_name` | Boolean |  | 2 |

</details>

---

### Context: `FormChangeDuringWeatherElement`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String | Specific element type required or applied. | 2 |
| [`form`](./Enums.md#enum-form) | Enum/String |  | 2 |

</details>

---

### Context: `Full`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| `animation_suffix` | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| [`statuses_on_enter_form`](./Characters_and_Bosses.md#context-statuses_on_enter_form) | Block | Status effects instantly applied upon transitioning into this form. | 2 |

</details>

---

### Context: `Holy`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#context-conditional_isphysicalattack)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `displace` | Boolean |  | 2 |
| `distance` | Number | The distance in tiles to knock the target away. | 2 |
| `self_damage` | Boolean | Recoil or self-inflicted damage/effects applied to the caster. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `MotherTumorSpawnInCapture`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`Cat`](./Characters_and_Bosses.md#context-cat) | Block | Character Form: Base form for standard cats. | 2 |
| [`NonCat`](./Characters_and_Bosses.md#context-noncat) | Block | Character Form: Behavior and stats for the 'NonCat' state. | 2 |
| [`Nothing`](./Characters_and_Bosses.md#context-nothing) | Block | Character Form: Behavior and stats for the 'Nothing' state. | 1 |

</details>

---

### Context: `MoveCenter`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 2 |

</details>

---

### Context: `MoveForThrow`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum/String |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 2 |

</details>

---

### Context: `MoveTowardsDamageSource`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`check_in_form`](./Enums.md#enum-check_in_form) | Enum/String |  | 2 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum/String |  | 2 |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| `can_move_zero` | Boolean |  | 1 |
| [`check_has_status`](./Enums.md#enum-check_has_status) | Enum/String |  | 1 |
| `do_not_move_on_top` | Boolean |  | 1 |
| `face_towards_after` | Boolean |  | 1 |
| [`ignore_tagged_sources`](./Enums.md#enum-ignore_tagged_sources) | Enum/String |  | 1 |
| `move_far` | Boolean |  | 1 |
| `move_short` | Boolean |  | 1 |

</details>

---

### Context: `NotPriming`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `PassiveWhileNotHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| [`status`](./Enums.md#enum-status) | Enum/String | ID of the status effect to apply or check. | 2 |

</details>

---

### Context: `Priming`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 2 |

</details>

---

### Context: `ProtectTargetedAllies`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 2 |
| [`target_filter`](./Enums.md#enum-target_filter) | Enum/String |  | 2 |

</details>

---

### Context: `Rain`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ally_rewards`](./Characters_and_Bosses.md#context-ally_rewards)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`StatusGroup`](./Characters_and_Bosses.md#context-statusgroup) | Block | Logic: Groups statuses for batch application. | 2 |

</details>

---

### Context: `RemoveStatusStacks`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Characters_and_Bosses.md#context-statusonendmove), [`StatusOnTookDamage`](./Characters_and_Bosses.md#context-statusontookdamage)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks to remove. | 2 |
| [`status`](./Enums.md#enum-status) | Enum/String | The specific status effect ID to remove. | 2 |

</details>

---

### Context: `Robot`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`alternate_energized_effect`](./Characters_and_Bosses.md#context-alternate_energized_effect) | Block | Overrides default energized visuals. | 2 |

</details>

---

### Context: `SlotMachineRollPool`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `SlotResult_Jackpot_Coins` | Number | Applies or references the 'SlotResult_Jackpot_Coins' effect/state. | 2 |
| `SlotResult_Explode` | Number | Applies or references the 'SlotResult_Explode' effect/state. | 1 |
| `SlotResult_Nothing` | Number | Applies or references the 'SlotResult_Nothing' effect/state. | 1 |
| `SlotResult_RandomPickup` | Number | Applies or references the 'SlotResult_RandomPickup' effect/state. | 1 |

</details>

---

### Context: `SpearRun`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum/String |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 2 |

</details>

---

### Context: `SquirrelForm`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum/String |  | 1 |

</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `ExtraBasicAttacks_Status` | Number | Applies or references the 'ExtraBasicAttacks_Status' effect/state. | 2 |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. | 1 |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. | 1 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 1 |

</details>

---

### Context: `SupportFormChangeInsteadOfRun`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 2 |
| `wait_till_turn` | Boolean |  | 1 |

</details>

---

### Context: `TempPassiveUntilSettled`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#context-conditional_isphysicalattack)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`MeleeRevengeDamage`](./Characters_and_Bosses.md#context-meleerevengedamage) | Block | Reaction: Deals damage or status effects to an attacker upon receiving melee damage. | 2 |

</details>

---

### Context: `TinkererBasicAttackSwitching`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveGroup`](./Characters_and_Bosses.md#context-passivegroup), [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum/String |  | 2 |
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum/String |  | 2 |

</details>

---

### Context: `TransformOnElementInfluencex`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String | Specific element type required or applied. | 2 |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 2 |

</details>

---

### Context: `Turtled`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum/String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |

</details>

---

### Context: `active`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |

</details>

---

### Context: `passive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 2 |

</details>

---

### Context: `statuses_on_enter_form`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Full`](./Characters_and_Bosses.md#context-full)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`UseAbility`](./Enums.md#enum-useability) | Enum/String | Logic: Forces execution of an ability. | 2 |

</details>

---

### Context: `0`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `4`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `partial_animation_suffix` | Number |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `5`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `partial_animation_suffix` | Number |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `AddStatusToReceivedDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#context-conditional_isphysicalattack) | Block | Conditional: Executes logic if the triggering attack is physical. | 1 |
| [`Else`](./Characters_and_Bosses.md#context-else) | Block | Fallback logic block for conditionals. | 1 |

</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Leech` | Number | Applies or references the 'Leech' effect/state. | 1 |

</details>

---

### Context: `AddStatusToTrampleDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Characters_and_Bosses.md#context-passivewhendead)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 1 |

</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. | 1 |

</details>

---

### Context: `AdventureTokenPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`StacyMutant_Brace`](./Characters_and_Bosses.md#context-stacymutant_brace) | Block | Character Form: Behavior and stats for the 'StacyMutant_Brace' state. | 1 |
| [`StacyMutant_Counter`](./Characters_and_Bosses.md#context-stacymutant_counter) | Block | Character Form: Behavior and stats for the 'StacyMutant_Counter' state. | 1 |
| [`StacyMutant_Damage`](./Characters_and_Bosses.md#context-stacymutant_damage) | Block | Character Form: Behavior and stats for the 'StacyMutant_Damage' state. | 1 |
| [`StacyMutant_DoubleHead`](./Characters_and_Bosses.md#context-stacymutant_doublehead) | Block | Character Form: Behavior and stats for the 'StacyMutant_DoubleHead' state. | 1 |
| [`StacyMutant_Fire`](./Characters_and_Bosses.md#context-stacymutant_fire) | Block | Character Form: Behavior and stats for the 'StacyMutant_Fire' state. | 1 |
| [`StacyMutant_Health`](./Characters_and_Bosses.md#context-stacymutant_health) | Block | Character Form: Behavior and stats for the 'StacyMutant_Health' state. | 1 |
| [`StacyMutant_Holy`](./Characters_and_Bosses.md#context-stacymutant_holy) | Block | Character Form: Behavior and stats for the 'StacyMutant_Holy' state. | 1 |
| [`StacyMutant_Ice`](./Characters_and_Bosses.md#context-stacymutant_ice) | Block | Character Form: Behavior and stats for the 'StacyMutant_Ice' state. | 1 |
| [`StacyMutant_Lightning`](./Characters_and_Bosses.md#context-stacymutant_lightning) | Block | Character Form: Behavior and stats for the 'StacyMutant_Lightning' state. | 1 |
| [`StacyMutant_Mirror`](./Characters_and_Bosses.md#context-stacymutant_mirror) | Block | Character Form: Behavior and stats for the 'StacyMutant_Mirror' state. | 1 |
| [`StacyMutant_Speed`](./Characters_and_Bosses.md#context-stacymutant_speed) | Block | Character Form: Behavior and stats for the 'StacyMutant_Speed' state. | 1 |
| [`StacyMutant_Thorns`](./Characters_and_Bosses.md#context-stacymutant_thorns) | Block | Character Form: Behavior and stats for the 'StacyMutant_Thorns' state. | 1 |

</details>

---

### Context: `AggroTargetIsGovernedByHitEffect`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean |  | 1 |

</details>

---

### Context: `Alert`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `AllStatsAura`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`aura_requires_tag`](./Enums.md#enum-aura_requires_tag) | Enum/String |  | 1 |
| [`range`](./Enums.md#enum-range) | Enum/String | Distance or area of effect in tiles. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `Angry`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `partial_animation_suffix` | String |  | 1 |

</details>

---

### Context: `Attacker`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to autocast. | 1 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 1 |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnGainCoins`](./Characters_and_Bosses.md#context-statusongaincoins)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific dodge ability to trigger (e.g., DestroyerDodge). | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `BattlefieldUniqueRandomPassive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Number | Applies or references the 'DemonicGlyph_Bite' effect/state. | 1 |
| `DemonicGlyph_Bounce` | Number | Applies or references the 'DemonicGlyph_Bounce' effect/state. | 1 |
| `DemonicGlyph_Fire` | Number | Applies or references the 'DemonicGlyph_Fire' effect/state. | 1 |
| `DemonicGlyph_Movement` | Number | Applies or references the 'DemonicGlyph_Movement' effect/state. | 1 |
| `DemonicGlyph_Summon` | Number | Applies or references the 'DemonicGlyph_Summon' effect/state. | 1 |

</details>

---

### Context: `BellyFull`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `partial_animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `BigHolding`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `BigHoldingCat`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Bishop`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `name` | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| `tooltip` | String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `BlackHole`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| `name` | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| `tooltip` | String |  | 1 |

</details>

---

### Context: `Bomb`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Bully`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `BungaCheers`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ally_damage`](./Enums.md#enum-ally_damage) | Enum/String |  | 1 |
| [`ally_dead`](./Enums.md#enum-ally_dead) | Enum/String |  | 1 |
| [`enemy_damage`](./Enums.md#enum-enemy_damage) | Enum/String |  | 1 |
| [`enemy_dead`](./Enums.md#enum-enemy_dead) | Enum/String |  | 1 |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum/String |  | 1 |

</details>

---

### Context: `CaveBaby`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `name` | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| `tooltip` | String |  | 1 |

</details>

---

### Context: `CaveWoman`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `name` | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| `tooltip` | String |  | 1 |

</details>

---

### Context: `CaveWomanHasCat`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `name` | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| `tooltip` | String |  | 1 |

</details>

---

### Context: `CerberubsAggroTargetBehavior`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`alert_form`](./Enums.md#enum-alert_form) | Enum/String |  | 1 |
| [`default_form`](./Enums.md#enum-default_form) | Enum/String |  | 1 |

</details>

---

### Context: `CerberubsJumpBlind`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum/String |  | 1 |

</details>

---

### Context: `CerberubsJumpNormal`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum/String |  | 1 |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| `chance` | Number | Probability (0.0 to 1.0) of executing this action. | 1 |

</details>

---

### Context: `ChanceToFormChangeOnAbilityDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0) of executing this action. | 1 |
| [`form`](./Enums.md#enum-form) | Enum/String |  | 1 |

</details>

---

### Context: `ChaosBossFormChangeGuide`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array |  | 1 |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array |  | 1 |
| `passives_health_threshold` | Number |  | 1 |

</details>

---

### Context: `ChaosBossPieces`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array |  | 1 |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array |  | 1 |

</details>

---

### Context: `ChaosHeadDropIn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`new_music`](./Enums.md#enum-new_music) | Enum/String |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String | Specific entity tag required. | 1 |

</details>

---

### Context: `Charging`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `partial_animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Close`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `CloseConvert`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Characters_and_Bosses.md#context-statuseachturnend)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Madness` | Number | Applies the Madness debuff/status effect. | 1 |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 1 |

</details>

---

### Context: `Conditional_HasKnockback`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Characters_and_Bosses.md#context-else)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](./Characters_and_Bosses.md#context-knockupandaway) | Block | Logic: Applies vertical and horizontal displacement. | 1 |
| `RemoveKnockback` | Number | Applies or references the 'RemoveKnockback' effect/state. | 1 |
| [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#context-temppassiveuntilsettled) | Block | Passive: Active only until the physics engine stops moving the character. | 1 |

</details>

---

### Context: `Conditional_IsPhysicalAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#context-addstatustoreceiveddamage)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](./Characters_and_Bosses.md#context-knockupandaway) | Block | Logic: Applies vertical and horizontal displacement. | 1 |
| `RemoveKnockback` | Number | Applies or references the 'RemoveKnockback' effect/state. | 1 |
| [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#context-temppassiveuntilsettled) | Block | Passive: Active only until the physics engine stops moving the character. | 1 |

</details>

---

### Context: `CounterAttack`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| `without_orienting` | Boolean |  | 1 |

</details>

---

### Context: `CreateGlobalModifiers`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `BloodRain` | Number | Applies or references the 'BloodRain' effect/state. | 1 |
| [`LowerAmbientLight`](./Characters_and_Bosses.md#context-lowerambientlight) | Block | Visual: Dims the map lighting. | 1 |

</details>

---

### Context: `Cultist`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `name` | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| `tooltip` | String |  | 1 |

</details>

---

### Context: `Damaged`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `Default_Ceiling`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Default_Ground`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `DelayedAutoRevive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 1 |
| `rounds` | Number |  | 1 |

</details>

---

### Context: `DesireMech`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `DiceBehavior`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `dice_size` | Number |  | 1 |
| `knockback_damage` | Number |  | 1 |

</details>

---

### Context: `Die`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `DiesToElement`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String | Specific element type required or applied. | 1 |
| `instant` | Boolean |  | 1 |

</details>

---

### Context: `DiesToPiercingAndSpikes`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `deferred` | Boolean |  | 1 |

</details>

---

### Context: `DodgeWhenTargeted`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |

</details>

---

### Context: `Drunker`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum/String |  | 1 |

</details>

---

### Context: `DualSword`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `move_speed_multiplier` | Number |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| `tooltip` | String |  | 1 |

</details>

---

### Context: `DualSword_Primed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `move_speed_multiplier` | Number |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| `tooltip` | String |  | 1 |

</details>

---

### Context: `Dumb`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `DybbukPossessionFallback`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum/String |  | 1 |
| [`form`](./Enums.md#enum-form) | Enum/String |  | 1 |

</details>

---

### Context: `Else`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#context-addstatustoreceiveddamage)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Conditional_HasKnockback`](./Characters_and_Bosses.md#context-conditional_hasknockback) | Block | Conditional: Executes logic if the triggering attack deals knockback. | 1 |

</details>

---

### Context: `Explody`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum/String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `FaceAwayLastDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean |  | 1 |
| `override_hit_animation` | Boolean |  | 1 |
| `use_turn_animations` | Boolean |  | 1 |

</details>

---

### Context: `FaceLastDamage`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean |  | 1 |

</details>

---

### Context: `FightPhase`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `FinalBossBeamQueue`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`queue`](./Enums.md#enum-queue) | Enum/String |  | 1 |
| [`release`](./Enums.md#enum-release) | Enum/String |  | 1 |
| [`transform`](./Enums.md#enum-transform) | Enum/String |  | 1 |

</details>

---

### Context: `FinalBossBecomeTheChild`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum/String | Applies or references the 'GlobalSpawnCharacter' effect/state. | 1 |
| `PlayBackground` | Number | Applies or references the 'PlayBackground' effect/state. | 1 |
| [`SwitchMusic`](./Characters_and_Bosses.md#context-switchmusic) | Block | Event Trigger: Changes background music track. | 1 |

</details>

---

### Context: `FinalBossHitCountdownHoly`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `icon` | Number |  | 1 |
| `icon_ready` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `FinalBossPupils`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`look_at_offset`](./Arrays.md#array-look_at_offset) | Array |  | 1 |
| `radius` | Number | Distance or area of effect in tiles. | 1 |
| [`reset_center_because_no_target_halflife`](./Enums.md#enum-reset_center_because_no_target_halflife) | Enum/String |  | 1 |
| [`reset_center_because_of_animation_halflife`](./Enums.md#enum-reset_center_because_of_animation_halflife) | Enum/String |  | 1 |
| [`teleport_tracking_halflife`](./Enums.md#enum-teleport_tracking_halflife) | Enum/String |  | 1 |
| [`tracking_acquisition_halflife`](./Enums.md#enum-tracking_acquisition_halflife) | Enum/String |  | 1 |
| [`virtual_head_position`](./Arrays.md#array-virtual_head_position) | Array |  | 1 |

</details>

---

### Context: `FinalBossShieldHealth`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`break_ability`](./Enums.md#enum-break_ability) | Enum/String |  | 1 |
| [`state_health`](./Arrays.md#array-state_health) | Array |  | 1 |

</details>

---

### Context: `FinalBossSyncAnimations`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`other_character`](./Enums.md#enum-other_character) | Enum/String |  | 1 |
| [`other_form_change_abilities`](./Characters_and_Bosses.md#context-other_form_change_abilities) | Block | Lists secondary abilities used to change forms. | 1 |

</details>

---

### Context: `Fire`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `FireFull`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum/String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Flop`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Flop2`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Flush`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `FlushBubs`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `FlushHost`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `FlushNettle`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `FoodMove`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `ForceTrample`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum/String |  | 1 |

</details>

---

### Context: `GainDisorderFromPool`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Characters_and_Bosses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum/String | Probability (0.0 to 1.0) of executing this action. | 1 |
| [`pool`](./Enums.md#enum-pool) | Enum/String |  | 1 |

</details>

---

### Context: `Grappling`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`exit_animations`](./Characters_and_Bosses.md#context-exit_animations) | Block | Animations played when leaving a form/state. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum/String |  | 1 |

</details>

---

### Context: `Grown`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum/String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `name` | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| `uifloaters_offset` | Number |  | 1 |
| `weak_threshold` | Number |  | 1 |

</details>

---

### Context: `GuaranteedJackpot`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Guarding`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `partial_animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `HPAltStates`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`clipname`](./Enums.md#enum-clipname) | Enum/String |  | 1 |
| [`thresholds`](./Arrays.md#array-thresholds) | Array |  | 1 |

</details>

---

### Context: `HalfDead`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `HasDeadCat`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `HasRock`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |

</details>

---

### Context: `Headless`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `HealNeighborsEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `Hint_CrackedVisuals`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 1 |

</details>

---

### Context: `Hint_CrackedVisuals2`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 1 |

</details>

---

### Context: `Hint_CrackedVisuals3`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 1 |

</details>

---

### Context: `HitlerExecute`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum/String | Specific entity tag required. | 1 |
| `threshold` | Number |  | 1 |

</details>

---

### Context: `Holding`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `partial_animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `HumanDead`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum/String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `tooltip` | String |  | 1 |

</details>

---

### Context: `InfiniteRebirth`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 1 |
| `immediate` | Boolean |  | 1 |
| `playercat_health` | Number |  | 1 |

</details>

---

### Context: `InitialPhase`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Insane_Ceiling`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Insane_Ground`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Johnny`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `JohnnyBubs`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `JohnnyHost`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `JohnnyNeedsWashing`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`form_unwashed`](./Enums.md#enum-form_unwashed) | Enum/String |  | 1 |
| [`form_washed`](./Enums.md#enum-form_washed) | Enum/String |  | 1 |

</details>

---

### Context: `JohnnyNettle`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Joystick`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `LastHit`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `LeapClose`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `Lifted`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Lit`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `LowerAmbientLight`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CreateGlobalModifiers`](./Characters_and_Bosses.md#context-createglobalmodifiers)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`amount`](./Arrays.md#array-amount) | Array | The target opacity/dimness level. | 1 |
| `speed` | Number | The transition speed. | 1 |

</details>

---

### Context: `MegaDinoDropController`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`head_drop`](./Enums.md#enum-head_drop) | Enum/String |  | 1 |
| [`leg_leave`](./Enums.md#enum-leg_leave) | Enum/String |  | 1 |
| [`leg_return`](./Enums.md#enum-leg_return) | Enum/String |  | 1 |
| `stable_legs` | Number |  | 1 |

</details>

---

### Context: `ModularPickup`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 1 |
| [`sound_event`](./Enums.md#enum-sound_event) | Enum/String |  | 1 |

</details>

---

### Context: `MonkCatReactionAbilities`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| [`spell`](./Enums.md#enum-spell) | Enum/String |  | 1 |
| [`trinket`](./Enums.md#enum-trinket) | Enum/String |  | 1 |
| [`weapon`](./Enums.md#enum-weapon) | Enum/String | Weapon item constraint. | 1 |

</details>

---

### Context: `MotherGrowController`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`eat_damage`](./Characters_and_Bosses.md#context-eat_damage) | Block | Damage dealt when this entity consumes another. | 1 |
| [`tumor_object`](./Enums.md#enum-tumor_object) | Enum/String |  | 1 |

</details>

---

### Context: `MotherTumorPassive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Cat`](./Characters_and_Bosses.md#context-cat) | Block | Character Form: Base form for standard cats. | 1 |
| [`NonCat`](./Characters_and_Bosses.md#context-noncat) | Block | Character Form: Behavior and stats for the 'NonCat' state. | 1 |
| [`considered_forms`](./Arrays.md#array-considered_forms) | Array |  | 1 |
| [`grow_ability`](./Enums.md#enum-grow_ability) | Enum/String |  | 1 |
| [`pass_ani`](./Enums.md#enum-pass_ani) | Enum/String |  | 1 |
| [`receive_ani`](./Enums.md#enum-receive_ani) | Enum/String |  | 1 |

</details>

---

### Context: `Mount`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`eject_ability`](./Enums.md#enum-eject_ability) | Enum/String |  | 1 |
| [`enter_ability`](./Enums.md#enum-enter_ability) | Enum/String |  | 1 |

</details>

---

### Context: `Mounted`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 1 |

</details>

---

### Context: `MouthFull`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `partial_animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `MoveAfterAnyAttemptedAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum/String |  | 1 |

</details>

---

### Context: `MoveAwayFromDamageSource`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum/String |  | 1 |

</details>

---

### Context: `MoveAwayWhenEnemyAdjacent`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum/String |  | 1 |
| `once_per_turn` | Boolean |  | 1 |
| [`weights`](./Enums.md#enum-weights) | Enum/String |  | 1 |

</details>

---

### Context: `MoveForBarrage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum/String |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `MoveForDash`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum/String |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `MoveForGrass`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum/String |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `MoveForPounce`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum/String |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `MoveForSpin`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum/String |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `MoveOneForPuke`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum/String |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `MoveSpaced`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `MoveToHead`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum/String |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `MoveTowards`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum/String |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `MultiSpawnOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array | The numerical quantity. | 1 |
| [`obj`](./Enums.md#enum-obj) | Enum/String |  | 1 |

</details>

---

### Context: `Mutant`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move_speed_multiplier`](./Enums.md#enum-move_speed_multiplier) | Enum/String |  | 1 |
| `name` | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| `tooltip` | String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `NCGravecrawlFAR`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `NeutronStar`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `NoEyes`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 1 |

</details>

---

### Context: `NoStick`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |

</details>

---

### Context: `NormalFull`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum/String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Nothing`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#context-mothertumorspawnincapture)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum/String |  | 1 |

</details>

---

### Context: `Nuke`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum/String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Obey`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Off`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum/String |  | 1 |

</details>

---

### Context: `OffScreen`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `OneEye`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Open`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum/String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `OpenCat`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Out`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum/String | Specific element type required or applied. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `PassiveWhenDead`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`AddStatusToTrampleDamage`](./Characters_and_Bosses.md#context-addstatustotrampledamage) | Block | Modifier: Injects a status effect into the character's trample damage. | 1 |

</details>

---

### Context: `Possessing`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Primed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Pulp2`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum/String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `Pulp3`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum/String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `Pulp4`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum/String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `Pulp5`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum/String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `Pulp6`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum/String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `Pulp7`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum/String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `ReturnA`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| `knockback` | Number |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification/category type. | 1 |

</details>

---

### Context: `RunFar`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `RunWhenLastPlayerCatIsCharmed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean |  | 1 |
| [`legacy_savekey`](./Enums.md#enum-legacy_savekey) | Enum/String |  | 1 |

</details>

---

### Context: `ScalingAttackAnimation`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`default`](./Enums.md#enum-default) | Enum/String | Baseline configuration. | 1 |
| [`thresholds`](./Arrays.md#array-thresholds) | Array |  | 1 |

</details>

---

### Context: `SharePickups`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `include_coins` | Boolean |  | 1 |

</details>

---

### Context: `Sitting`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum/String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `SkipFirstRounds`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `pop_chance` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `Small`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |

</details>

---

### Context: `SmallHolding`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `SmallHoldingCat`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `SpawningPhase`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `SpewerAltGraphics`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Fire` | Number | Character Form: Behavior and stats for the 'Fire' state. | 1 |
| `FireFull` | Number | Character Form: Behavior and stats for the 'FireFull' state. | 1 |
| `Normal` | Number | Character Form: Behavior and stats for the 'Normal' state. | 1 |
| `NormalFull` | Number | Character Form: Behavior and stats for the 'NormalFull' state. | 1 |
| `Tar` | Number | Character Form: Behavior and stats for the 'Tar' state. | 1 |
| `TarFull` | Number | Character Form: Behavior and stats for the 'TarFull' state. | 1 |

</details>

---

### Context: `StacyMutant_Brace`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | Applies or references the 'Brace' effect/state. | 1 |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |

</details>

---

### Context: `StacyMutant_Counter`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Characters_and_Bosses.md#context-addstatustobasicattack) | Block | Modifier: Injects a status effect payload into the character's basic attacks. | 1 |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| [`CounterAttack`](./Enums.md#enum-counterattack) | Enum/String | Reaction: Executes a counter-attack ability when hit. | 1 |

</details>

---

### Context: `StacyMutant_Damage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AddDamage` | Number | Applies or references the 'AddDamage' effect/state. | 1 |
| `AddMaxHealth` | Number | Applies or references the 'AddMaxHealth' effect/state. | 1 |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |

</details>

---

### Context: `StacyMutant_DoubleHead`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| `ExtraDispersedTurns` | Number | Applies or references the 'ExtraDispersedTurns' effect/state. | 1 |

</details>

---

### Context: `StacyMutant_Fire`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum/String | Applies or references the 'ElementImmune' effect/state. | 1 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum/String | Applies or references the 'ReplaceBasicAttack' effect/state. | 1 |
| [`ReplaceBrain`](./Characters_and_Bosses.md#context-replacebrain) | Block | AI Logic: Completely overrides the character's AI profile with a new one. | 1 |

</details>

---

### Context: `StacyMutant_Health`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AddMaxHealth` | Number | Applies or references the 'AddMaxHealth' effect/state. | 1 |
| `AddSpeed` | Number | Applies or references the 'AddSpeed' effect/state. | 1 |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| `SizeScale` | Number | Applies or references the 'SizeScale' effect/state. | 1 |

</details>

---

### Context: `StacyMutant_Holy`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. | 1 |

</details>

---

### Context: `StacyMutant_Ice`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AddMovement` | Number | Applies or references the 'AddMovement' effect/state. | 1 |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum/String | Applies or references the 'ElementImmune' effect/state. | 1 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum/String | Applies or references the 'ReplaceBasicAttack' effect/state. | 1 |
| [`ReplaceBrain`](./Characters_and_Bosses.md#context-replacebrain) | Block | AI Logic: Completely overrides the character's AI profile with a new one. | 1 |

</details>

---

### Context: `StacyMutant_Lightning`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum/String | Applies or references the 'ElementImmune' effect/state. | 1 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum/String | Applies or references the 'ReplaceBasicAttack' effect/state. | 1 |
| [`ReplaceBrain`](./Characters_and_Bosses.md#context-replacebrain) | Block | AI Logic: Completely overrides the character's AI profile with a new one. | 1 |

</details>

---

### Context: `StacyMutant_Mirror`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| `ReflectProjectiles` | Number | Passive: Reflects incoming projectiles back at the attacker. | 1 |
| [`StatusEachTurnEndForEachTurn`](./Characters_and_Bosses.md#context-statuseachturnendforeachturn) | Block | Event Trigger: Applies a scaling status at the end of every turn based on turn count. | 1 |

</details>

---

### Context: `StacyMutant_Speed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AddDamage` | Number | Applies or references the 'AddDamage' effect/state. | 1 |
| `AddSpeed` | Number | Applies or references the 'AddSpeed' effect/state. | 1 |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| [`SizeScale`](./Enums.md#enum-sizescale) | Enum/String | Applies or references the 'SizeScale' effect/state. | 1 |

</details>

---

### Context: `StacyMutant_Thorns`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. | 1 |

</details>

---

### Context: `Standing`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Standing2`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Start_Ceiling`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `StatusAfterXTurns`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Logic: Forces the execution of a specific ability. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `StatusEachTurnBeginIfHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 1 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 1 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 1 |
| [`animation`](./Enums.md#enum-animation) | Enum/String |  | 1 |
| `consume` | Boolean |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum/String | ID of the status effect to apply or check. | 1 |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 1 |
| [`Conditional_BadRoll`](./Characters_and_Bosses.md#context-conditional_badroll) | Block | Conditional: Executes logic on a bad RNG roll. | 1 |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. | 1 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 1 |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 1 |

</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StacyMutant_Mirror`](./Characters_and_Bosses.md#context-stacymutant_mirror)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. | 1 |

</details>

---

### Context: `StatusEachTurnEndIfEnabledAtStartOfTurn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum/String | Logic: Forces the execution of a specific ability. | 1 |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `RemoveAmbientLightEffects` | Number | Applies or references the 'RemoveAmbientLightEffects' effect/state. | 1 |
| [`RemoveGlobalModifiers`](./Arrays.md#array-removeglobalmodifiers) | Array | Applies or references the 'RemoveGlobalModifiers' effect/state. | 1 |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`RemoveStatusStacks`](./Characters_and_Bosses.md#context-removestatusstacks) | Block | Logic: Removes stacks of a specific status effect. | 1 |
| `SpeedUp_WithoutInitiative` | Number | Applies or references the 'SpeedUp_WithoutInitiative' effect/state. | 1 |

</details>

---

### Context: `StatusOnEnemyConfused`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum/String | Applies or references the 'ImmediateUseAbility' effect/state. | 1 |

</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`BackflipWhenTargeted`](./Characters_and_Bosses.md#context-backflipwhentargeted) | Block | Reaction: Character executes a backflip dodge when targeted by an attack. | 1 |

</details>

---

### Context: `StatusOnSpawnIn`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 1 |
| `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. | 1 |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `ConstitutionUp` | Number | Applies or references the 'ConstitutionUp' effect/state. | 1 |
| [`RemoveStatusStacks`](./Characters_and_Bosses.md#context-removestatusstacks) | Block | Logic: Removes stacks of a specific status effect. | 1 |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. | 1 |

</details>

---

### Context: `StatusOverlappingCharactersAndDie`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Poison` | Number | Applies or references the 'Poison' effect/state. | 1 |

</details>

---

### Context: `StatusWhenStatusCompletelyRemoved`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`UseAbility`](./Characters_and_Bosses.md#context-useability) | Block | Logic: Forces execution of an ability. | 1 |
| [`status`](./Enums.md#enum-status) | Enum/String | ID of the status effect to apply or check. | 1 |

</details>

---

### Context: `Stop`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `StunImmunity`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean |  | 1 |

</details>

---

### Context: `SuckMF`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum/String |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `SupportDieInsteadOfRun`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`alt_dead_ani`](./Enums.md#enum-alt_dead_ani) | Enum/String |  | 1 |
| [`alt_dying_ani`](./Enums.md#enum-alt_dying_ani) | Enum/String |  | 1 |

</details>

---

### Context: `SwimmingFormChange`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`form_in`](./Enums.md#enum-form_in) | Enum/String |  | 1 |
| [`form_out`](./Enums.md#enum-form_out) | Enum/String |  | 1 |

</details>

---

### Context: `SwitchMusic`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossBecomeTheChild`](./Characters_and_Bosses.md#context-finalbossbecomethechild)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum/String | The specific audio layer to transition to (e.g., map, battle). | 1 |
| [`new_song`](./Enums.md#enum-new_song) | Enum/String | The ID of the new music track. | 1 |

</details>

---

### Context: `SwordAndShield`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `SwordAndShield_Primed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `SyncFormsWithBuddy`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`no_buddy`](./Enums.md#enum-no_buddy) | Enum/String |  | 1 |

</details>

---

### Context: `T3HitlerSpawningPhase`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `T3JoinFight` | Flag | Applies or references the 'T3JoinFight' effect/state. | 1 |
| `T3Spawn_Colorless` | Flag | Applies or references the 'T3Spawn_Colorless' effect/state. | 1 |
| [`spell_use_groups`](./Arrays.md#array-spell_use_groups) | Array |  | 1 |

</details>

---

### Context: `TF_TargetAllies`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum/String |  | 1 |

</details>

---

### Context: `TF_TargetEnemies`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum/String |  | 1 |

</details>

---

### Context: `TVBotScreen`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Die` | Number | Character Form / Logic: Forces the character to die. | 1 |
| `Dumb` | Number | AI Profile: A simplified, less optimal decision-making profile. | 1 |
| `Fuck` | Number | Applies or references the 'Fuck' effect/state. | 1 |
| `Obey` | Number | AI State: Enforced compliance logic (e.g., when Charmed). | 1 |
| `Shit` | Number | Applies or references the 'Shit' effect/state. | 1 |
| `Stop` | Number | AI Movement: Forces the character to cease movement. | 1 |

</details>

---

### Context: `Tar`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `TarFull`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum/String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Terminator2Run`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum/String |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `TerminatorChase`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move`](./Enums.md#enum-move) | Enum/String |  | 1 |

</details>

---

### Context: `TerminatorSkin`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`groups`](./Arrays.md#array-groups) | Array |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum/String | ID of the status effect to apply or check. | 1 |

</details>

---

### Context: `Throb`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `ThrobBubs`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `ThrobHost`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `ThrobNettle`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `TransformOnStatusThreshold`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum/String | ID of the status effect to apply or check. | 1 |
| `threshold` | Number |  | 1 |

</details>

---

### Context: `Transformed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `TwisterFling`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| `max_dist` | Number |  | 1 |
| `min_dist` | Number |  | 1 |

</details>

---

### Context: `TwoEyes`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Unflip`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum/String |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |

</details>

---

### Context: `UnlimitedDeathRattleRevive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| `even_if_stunned` | Boolean |  | 1 |

</details>

---

### Context: `Unlit`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum/String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Unwashed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum/String |  | 1 |

</details>

---

### Context: `UseAbility`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusWhenStatusCompletelyRemoved`](./Characters_and_Bosses.md#context-statuswhenstatuscompletelyremoved)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The ID of the ability to trigger. | 1 |
| `respect_prime` | Boolean | If true, respects the ability's prime/cooldown state. | 1 |

</details>

---

### Context: `UseAbilityWhenOutOfStatus`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum/String | The specific ability ID to cast. | 1 |
| [`status`](./Enums.md#enum-status) | Enum/String | ID of the status effect to apply or check. | 1 |

</details>

---

### Context: `Washed`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Washer`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `name` | String | Localization key for the character's name. | 1 |
| `partial_animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| `tooltip` | String |  | 1 |

</details>

---

### Context: `Water`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `partial_animation_suffix` | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `WereMan`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `name` | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| `tooltip` | String |  | 1 |

</details>

---

### Context: `Zealot`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `name` | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| `tooltip` | String |  | 1 |

</details>

---

### Context: `ZealotBomb`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum/String |  | 1 |
| `name` | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| `tooltip` | String |  | 1 |

</details>

---

### Context: `additional_statuses`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnOnDeath`](./Characters_and_Bosses.md#context-spawnondeath)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `PermanentMadness` | Number | Applies or references the 'PermanentMadness' effect/state. | 1 |

</details>

---

### Context: `ai_if_spawned_as_enemy`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum/String |  | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum/String |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum/String |  | 1 |
| [`pattern`](./Characters_and_Bosses.md#context-pattern) | Block | AI sequence logic. | 1 |

</details>

---

### Context: `alternate_energized_effect`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Robot`](./Characters_and_Bosses.md#context-robot)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`FormChange`](./Enums.md#enum-formchange) | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 1 |
| `SpellDamageUp` | Number | Applies or references the 'SpellDamageUp' effect/state. | 1 |

</details>

---

### Context: `damage_instance`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`effects`](./Characters_and_Bosses.md#context-effects) | Block | Non-damaging impact triggers. | 1 |

</details>

---

### Context: `eat_damage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherGrowController`](./Characters_and_Bosses.md#context-mothergrowcontroller)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean |  | 1 |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Characters_and_Bosses.md#context-effects) | Block | Non-damaging impact triggers. | 1 |
| `makes_contact` | Boolean |  | 1 |
| `piercing` | Boolean |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum/String | Classification/category type. | 1 |

</details>

---

### Context: `exit_animations`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Grappling`](./Characters_and_Bosses.md#context-grappling)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Default`](./Enums.md#enum-default) | Enum/String | Character Form: The baseline default behavior state. | 1 |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Die`](./Characters_and_Bosses.md#context-die), [`Dumb`](./Characters_and_Bosses.md#context-dumb), [`Obey`](./Characters_and_Bosses.md#context-obey), [`Stop`](./Characters_and_Bosses.md#context-stop)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `TVBotDie` | Number | Applies or references the 'TVBotDie' effect/state. | 1 |
| `TVBotDumb` | Number | Applies or references the 'TVBotDumb' effect/state. | 1 |
| `TVBotObey` | Number | Applies or references the 'TVBotObey' effect/state. | 1 |
| `TVBotStop` | Number | Applies or references the 'TVBotStop' effect/state. | 1 |

</details>

---

### Context: `other_form_change_abilities`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossSyncAnimations`](./Characters_and_Bosses.md#context-finalbosssyncanimations)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`Boris`](./Enums.md#enum-boris) | Enum/String | Character Form / AI State: Behavior and stats for the 'Boris' state. | 1 |
| [`Explosive`](./Enums.md#enum-explosive) | Enum/String | Character Form: Behavior and stats for the 'Explosive' state. | 1 |
| [`Holy`](./Enums.md#enum-holy) | Enum/String | Character Form: Behavior and stats for the 'Holy' state. | 1 |

</details>

---

### Context: `round_start_bonusturn_pattern`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 1 |

</details>

---

