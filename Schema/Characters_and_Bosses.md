# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Characters & Bosses

> **Associated Files:** `data/characters/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 600

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1549 |
| [`properties`](./Characters_and_Bosses.md#object-properties) | Object | General engine properties. | 600 |
| [`graphics`](./Characters_and_Bosses.md#object-graphics) | Object | Visual parameters and animation bindings. | 558 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 464 |
| [`abilities`](./Characters_and_Bosses.md#object-abilities) | Object | Lists the ability IDs the character possesses. | 458 |
| [`stats`](./Characters_and_Bosses.md#object-stats) | Object | Core character metrics (Health, Strength, etc.). | 388 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum |  | 240 |
| [`sound`](./Characters_and_Bosses.md#object-sound) | Object | Audio bindings. | 62 |
| [`equipment`](./Characters_and_Bosses.md#object-equipment) | Object | List of item IDs the character spawns equipped with. | 44 |
| [`alt_spawn_pool`](./Characters_and_Bosses.md#object-alt_spawn_pool) | Object | Alternative pools to draw minions from. | 18 |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 5 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 5 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 5 |
| `animation_suffix` | Number | Examples: `3, 4, 2` | 3 |
| `initial_form` | Number | Examples: `1, 5, 0` | 3 |
| `partial_animation_suffix` | Number | Examples: `3, 2, 1` | 3 |
| [`pattern`](./Characters_and_Bosses.md#object-pattern) | Object | AI sequence logic. | 3 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| `end_turn_on_formswitch` | Boolean |  | 2 |
| [`ai_if_spawned_as_enemy`](./Characters_and_Bosses.md#object-ai_if_spawned_as_enemy) | Object | AI logic override used only if the character is spawned as an enemy. | 1 |
| `consider_spells` | Boolean |  | 1 |
| [`damage_instance`](./Characters_and_Bosses.md#object-damage_instance) | Object | Defines damage logic on contact. | 1 |
| [`scale`](./Enums.md#enum-scale) | Enum |  | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Object: `passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 733

> **Referenced by:** [`Alert`](./Characters_and_Bosses.md#object-alert), [`AllAlive`](./Characters_and_Bosses.md#object-allalive), [`BellyFull`](./Characters_and_Bosses.md#object-bellyfull), [`Big`](./Characters_and_Bosses.md#object-big), [`BigHolding`](./Characters_and_Bosses.md#object-bigholding), [`BigHoldingCat`](./Characters_and_Bosses.md#object-bigholdingcat), [`Bishop`](./Characters_and_Bosses.md#object-bishop), [`BlackHole`](./Characters_and_Bosses.md#object-blackhole), [`Bomb`](./Characters_and_Bosses.md#object-bomb), [`Boris`](./Characters_and_Bosses.md#object-boris), [`Bully`](./Characters_and_Bosses.md#object-bully), [`CaveBaby`](./Characters_and_Bosses.md#object-cavebaby), [`CaveMan`](./Characters_and_Bosses.md#object-caveman), [`CaveManSpear`](./Characters_and_Bosses.md#object-cavemanspear), [`CaveWoman`](./Characters_and_Bosses.md#object-cavewoman), [`CaveWomanHasCat`](./Characters_and_Bosses.md#object-cavewomanhascat), [`Charging`](./Characters_and_Bosses.md#object-charging), [`Close`](./Characters_and_Bosses.md#object-close), [`Cultist`](./Characters_and_Bosses.md#object-cultist), [`Default`](./Characters_and_Bosses.md#object-default), and 97 more...

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2609 |
| [`ArmorPickup`](./Characters_and_Bosses.md#object-armorpickup) | Object | Pickup Logic: Defines what happens when an armor item is collected. | 3 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Examples: `{ ... }` | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| `partial_animation_suffix` | Number | Examples: `4, 2` | 2 |
| `animation_suffix` | Number | Examples: `1` | 1 |
| `uifloaters_offset` | Number | Examples: `2.2` | 1 |

</details>

---

### Object: `properties`

**Definition:** General engine properties.
**Total Count:** 600



<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 539 |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 505 |
| `health` | Number |  | 427 |
| [`tag`](./Arrays.md#array-tag) | Array | Specific entity tag required. | 399 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 280 |
| `movement` | Number |  | 278 |
| [`corpse_health`](./Enums.md#enum-corpse_health) | Mixed |  | 195 |
| `inherit_faction` | Boolean |  | 115 |
| `dispersed_bonus_turns` | Number |  | 104 |
| `base_mana_regen` | Number |  | 90 |
| [`size`](./Enums.md#enum-size) | Enum |  | 80 |
| `shield` | Number |  | 74 |
| [`move_block`](./Enums.md#enum-move_block) | Enum |  | 73 |
| `kill_required` | Boolean |  | 69 |
| `can_be_backstabbed` | Boolean |  | 68 |
| `initiative` | Number |  | 61 |
| `takes_turns` | Boolean |  | 61 |
| `mana_regen` | Number |  | 51 |
| `mana` | Number | Base maximum mana pool. | 50 |
| `flying` | Boolean |  | 47 |
| [`banned_elite_buffs`](./Arrays.md#array-banned_elite_buffs) | Array |  | 45 |
| [`hidden_tag`](./Arrays.md#array-hidden_tag) | Array |  | 38 |
| `weak_threshold` | Number |  | 32 |
| `knockback_immune` | Boolean |  | 25 |
| `can_be_champion` | Boolean |  | 20 |
| [`lock_orientation`](./Arrays.md#array-lock_orientation) | Array |  | 19 |
| [`ai_scale`](./Enums.md#enum-ai_scale) | Enum |  | 18 |
| [`auto_run_priority`](./Enums.md#enum-auto_run_priority) | Enum |  | 16 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 16 |
| `inanimate` | Boolean |  | 16 |
| `disperse_main_turns` | Boolean |  | 15 |
| [`hidden_tags`](./Arrays.md#array-hidden_tags) | Array |  | 14 |
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
| [`aoe_pierce_mode`](./Enums.md#enum-aoe_pierce_mode) | Enum |  | 3 |
| `base_initiative` | Number |  | 3 |
| `base_movement` | Number |  | 3 |
| `catdata_ignore_skills` | Boolean |  | 3 |
| [`disallow_items`](./Enums.md#enum-disallow_items) | Enum |  | 3 |
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
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | `Enum/String` |  | 0 |

</details>

---

### Object: `ai`


**Definition:** Core block defining the AI behavior logic and weights.
**Total Count:** 583


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`Alert`](./Characters_and_Bosses.md#object-alert), [`Angry`](./Characters_and_Bosses.md#object-angry), [`Attacker`](./Characters_and_Bosses.md#object-attacker), [`BellyFull`](./Characters_and_Bosses.md#object-bellyfull), [`Bishop`](./Characters_and_Bosses.md#object-bishop), [`BlackHole`](./Characters_and_Bosses.md#object-blackhole), [`Bully`](./Characters_and_Bosses.md#object-bully), [`CaveBaby`](./Characters_and_Bosses.md#object-cavebaby), [`CaveMan`](./Characters_and_Bosses.md#object-caveman), [`CaveManSpear`](./Characters_and_Bosses.md#object-cavemanspear), [`CaveWoman`](./Characters_and_Bosses.md#object-cavewoman), [`CaveWomanHasCat`](./Characters_and_Bosses.md#object-cavewomanhascat), [`Charging`](./Characters_and_Bosses.md#object-charging), [`Cultist`](./Characters_and_Bosses.md#object-cultist), [`Damaged`](./Characters_and_Bosses.md#object-damaged), [`Default`](./Characters_and_Bosses.md#object-default), [`Default_Ceiling`](./Characters_and_Bosses.md#object-default_ceiling), [`Default_Ground`](./Characters_and_Bosses.md#object-default_ground), [`DesireMech`](./Characters_and_Bosses.md#object-desiremech), [`Down`](./Characters_and_Bosses.md#object-down), and 64 more...

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 573 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 493 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 490 |
| [`pattern`](./Characters_and_Bosses.md#object-pattern) | Object | AI sequence logic. | 289 |
| [`mainturn_pattern`](./Characters_and_Bosses.md#object-mainturn_pattern) | Object | AI Logic: Determines standard ability usage during the main turn. | 44 |
| `end_turn_on_formswitch` | Boolean |  | 39 |
| [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities) | Object | Abilities that are evaluated but not directly castable by the player. | 35 |
| `auto_orient` | Boolean |  | 31 |
| `reset_pattern_on_formswitch` | Boolean |  | 31 |
| `stun_advances_pattern` | Boolean |  | 30 |
| `fallback_advances_pattern` | Boolean |  | 28 |
| [`bonusturn_pattern`](./Characters_and_Bosses.md#object-bonusturn_pattern) | Object | AI Logic: Determines ability usage during bonus turns. | 27 |
| [`fallback`](./Characters_and_Bosses.md#object-fallback) | Object | Logic executed if primary options fail. | 23 |
| [`round_end_bonusturn_pattern`](./Characters_and_Bosses.md#object-round_end_bonusturn_pattern) | Object | AI Logic: Ability usage pattern during round-end bonus turns. | 12 |
| `consider_spells` | Boolean |  | 11 |
| `animate_choice` | Boolean |  | 8 |
| `clamp_pattern` | Boolean |  | 5 |
| `randomize_pattern_start` | Boolean |  | 3 |
| [`dispersed_bonusturn_pattern`](./Characters_and_Bosses.md#object-dispersed_bonusturn_pattern) | Object | AI Logic: Alternative bonus turn ability pattern. | 2 |
| `random_orient` | Boolean |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`dice_abilities`](./Arrays.md#array-dice_abilities) | Array |  | 1 |
| [`post_absorb_move_weights`](./Enums.md#enum-post_absorb_move_weights) | Enum |  | 1 |
| [`roll_ability`](./Enums.md#enum-roll_ability) | Enum |  | 1 |
| [`round_start_bonusturn_pattern`](./Characters_and_Bosses.md#object-round_start_bonusturn_pattern) | Object | AI Logic: Ability usage pattern during round-start bonus turns. | 1 |
| `never_hit_ally_corpses` | Boolean |  | 1 |
| `reset_pattern_on_round_begin` | Boolean |  | 1 |

</details>

---

### Object: `graphics`


**Definition:** Visual parameters and animation bindings.


<details>
<summary><b>Expand</b></summary>

**Total Count:** 558

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 517 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  | 461 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 409 |
| `shadow_size` | Number |  | 151 |
| [`scale`](./Enums.md#enum-scale) | Enum |  | 149 |
| `uifloaters_offset` | Number |  | 149 |
| [`custom_cat_data`](./Enums.md#enum-custom_cat_data) | Enum |  | 127 |
| [`water_mask`](./Enums.md#enum-water_mask) | Enum |  | 83 |
| [`spawnin_animation`](./Strings.md#string-spawnin_animation) | String |  | 37 |
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array |  | 33 |
| `piece_alt_frame` | Number |  | 27 |
| [`shadow`](./Enums.md#enum-shadow) | Enum |  | 23 |
| `move_speed_sync_frames` | Number |  | 20 |
| `no_splatter` | Boolean |  | 17 |
| [`projectile_spawn_offset`](./Arrays.md#array-projectile_spawn_offset) | Array |  | 17 |
| [`tint`](./Arrays.md#array-tint) | Array |  | 17 |
| [`move_speed_multiplier`](./Enums.md#enum-move_speed_multiplier) | Enum |  | 16 |
| `dont_sink` | Boolean |  | 14 |
| `art_flip` | Number |  | 7 |
| [`depth_offset`](./Enums.md#enum-depth_offset) | Enum |  | 6 |
| [`walk`](./Enums.md#enum-walk) | Enum |  | 5 |
| [`dead`](./Enums.md#enum-dead) | Enum |  | 4 |
| [`dying`](./Enums.md#enum-dying) | Enum |  | 4 |
| `four_way_animations` | Boolean |  | 4 |
| [`hit`](./Enums.md#enum-hit) | Enum |  | 4 |
| [`stunned`](./Enums.md#enum-stunned) | Enum |  | 4 |
| [`weak`](./Enums.md#enum-weak) | Enum |  | 4 |
| [`deadhit`](./Enums.md#enum-deadhit) | Enum |  | 3 |
| `show_infinity_damage_warning` | Boolean |  | 3 |
| `always_huge_mask` | Boolean |  | 2 |
| [`default_attack_animation`](./Enums.md#enum-default_attack_animation) | Enum |  | 2 |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the character's desc. | 2 |
| `shade_occluded_objects` | Boolean |  | 2 |
| [`dodge`](./Enums.md#enum-dodge) | Enum |  | 1 |
| `no_horizontal_flip` | Boolean |  | 1 |
| [`non_blocking_animations`](./Arrays.md#array-non_blocking_animations) | Array |  | 1 |
| [`override_portrait`](./Enums.md#enum-override_portrait) | Enum |  | 1 |
| `randomize_starting_frame` | Boolean |  | 1 |
| `status_display_count_max` | Number |  | 1 |

</details>

---

### Object: `abilities`


**Definition:** Lists the ability IDs the character possesses.
**Total Count:** 458


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 436 |
| [`move`](./Enums.md#enum-move) | Enum |  | 433 |
| [`spells`](./Arrays.md#array-spells) | Array |  | 381 |
| `can_get_bonus` | Boolean |  | 30 |
| `BoneWormShotSmall` | Flag |  | 1 |

</details>

---

### Object: `stats`


**Definition:** Core character metrics (Health, Strength, etc.).
**Total Count:** 388


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count |
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

### Object: `pattern`


**Definition:** AI sequence logic.
**Total Count:** 296


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root), [`ReplaceBrain`](./Characters_and_Bosses.md#object-replacebrain), [`ai`](./Characters_and_Bosses.md#object-ai), [`ai_if_spawned_as_enemy`](./Characters_and_Bosses.md#object-ai_if_spawned_as_enemy)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum |  | 128 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 106 |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 101 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum |  | 11 |
| [`do_random`](./Arrays.md#array-do_random) | Array |  | 10 |
| [`do_strict`](./Arrays.md#array-do_strict) | Array |  | 6 |
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array |  | 3 |
| [`move_then_do_priority`](./Arrays.md#array-move_then_do_priority) | Array |  | 3 |
| [`move_then_do_random`](./Arrays.md#array-move_then_do_random) | Array |  | 3 |
| [`do_all_shuffle`](./Arrays.md#array-do_all_shuffle) | Array |  | 2 |
| [`do_best_multiple`](./Arrays.md#array-do_best_multiple) | Array |  | 1 |
| [`do_best`](./Arrays.md#array-do_best) | Array |  | 1 |
| [`do_priority_alternating`](./Arrays.md#array-do_priority_alternating) | Array |  | 1 |
| [`move_then_do_all`](./Arrays.md#array-move_then_do_all) | Array |  | 1 |

</details>

---

### Object: `FormChanger`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 106

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 120 |
| [`initial_form`](./Enums.md#enum-initial_form) | Enum |  | 56 |
| [`Default`](./Characters_and_Bosses.md#object-default) | Object | Character Form: The baseline default behavior state. | 37 |
| [`Normal`](./Characters_and_Bosses.md#object-normal) | Object | Character Form: Behavior and stats for the \'Normal\' state. | 11 |
| [`Rage`](./Characters_and_Bosses.md#object-rage) | Object | Character Form: Behavior and stats for the \'Rage\' state. | 10 |
| [`HasCat`](./Characters_and_Bosses.md#object-hascat) | Object | Character Form: Behavior and stats for the \'HasCat\' state. | 5 |
| [`default`](./Characters_and_Bosses.md#object-default) | Object | Baseline configuration. | 4 |
| [`hot`](./Characters_and_Bosses.md#object-hot) | Object | Visual effect indicator. | 4 |
| [`OffMap`](./Characters_and_Bosses.md#object-offmap) | Object | Character Form: Behavior and stats for the 'OffMap' state. | 4 |
| [`AllAlive`](./Characters_and_Bosses.md#object-allalive) | Object | Encounter State: Logic executed when all specific entities are currently alive. | 3 |
| [`Down`](./Characters_and_Bosses.md#object-down) | Object | Character Form: Behavior and stats for the \'Down\' state. | 3 |
| [`Full`](./Characters_and_Bosses.md#object-full) | Object | Character Form: Behavior and stats for the \'Full\' state. | 3 |
| [`OneAlive`](./Characters_and_Bosses.md#object-onealive) | Object | Encounter State: Logic executed when exactly one target is alive. | 3 |
| [`TwoAlive`](./Characters_and_Bosses.md#object-twoalive) | Object | Encounter State: Logic executed when exactly two targets are alive. | 3 |
| [`Up`](./Characters_and_Bosses.md#object-up) | Object | Character Form: Behavior and stats for the \'Up\' state. | 3 |
| [`active`](./Characters_and_Bosses.md#object-active) | Object | Defines actively executed abilities. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`Big`](./Characters_and_Bosses.md#object-big) | Object | Character Form / AI State: Behavior and stats for the \'Big\' state. | 2 |
| [`Boris`](./Characters_and_Bosses.md#object-boris) | Object | Character Form / AI State: Behavior and stats for the \'Boris\' state. | 2 |
| [`CaveMan`](./Characters_and_Bosses.md#object-caveman) | Object | Character Form: Behavior and stats for the \'CaveMan\' state. | 2 |
| [`CaveManSpear`](./Characters_and_Bosses.md#object-cavemanspear) | Object | Character Form: Behavior and stats for the \'CaveManSpear\' state. | 2 |
| [`Empty`](./Characters_and_Bosses.md#object-empty) | Object | Character Form: Behavior and stats for the \'Empty\' state. | 2 |
| [`Explosive`](./Characters_and_Bosses.md#object-explosive) | Object | Character Form: Behavior and stats for the \'Explosive\' state. | 2 |
| [`Holding`](./Characters_and_Bosses.md#object-holding) | Object | Character Form: Behavior and stats for the \'Holding\' state. | 2 |
| [`Holy`](./Characters_and_Bosses.md#object-holy) | Object | Character Form: Behavior and stats for the \'Holy\' state. | 2 |
| [`NotPriming`](./Characters_and_Bosses.md#object-notpriming) | Object | Character Form: Behavior and stats when not charging an ability. | 2 |
| `partial_animation_suffix` | Number |  | 2 |
| [`passive`](./Characters_and_Bosses.md#object-passive) | Object | Intrinsic passive modifier. | 2 |
| [`Priming`](./Characters_and_Bosses.md#object-priming) | Object | Character Form: Behavior and stats when charging an ability. | 2 |
| [`Small`](./Characters_and_Bosses.md#object-small) | Object | Character Form: Behavior and stats for the \'Small\' state. | 2 |
| [`SquirrelForm`](./Characters_and_Bosses.md#object-squirrelform) | Object | Character Form: Behavior and stats for the 'SquirrelForm' state. | 2 |
| [`Turtled`](./Characters_and_Bosses.md#object-turtled) | Object | Character Form: Behavior and stats for the 'Turtled' state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`Alert`](./Characters_and_Bosses.md#object-alert) | Object | AI State: The behavior profile used when the character is alerted to enemies. | 1 |
| [`Angry`](./Characters_and_Bosses.md#object-angry) | Object | Character Form / AI State: Behavior and stats for the \'Angry\' state. | 1 |
| [`Attacker`](./Characters_and_Bosses.md#object-attacker) | Object | AI Role: Designates the character as an attacker rather than support. | 1 |
| [`BellyFull`](./Characters_and_Bosses.md#object-bellyfull) | Object | Character Form / AI State: Behavior and stats for the \'BellyFull\' state. | 1 |
| [`BigHolding`](./Characters_and_Bosses.md#object-bigholding) | Object | Character Form / AI State: Behavior and stats for the \'BigHolding\' state. | 1 |
| [`BigHoldingCat`](./Characters_and_Bosses.md#object-bigholdingcat) | Object | Character Form / AI State: Behavior and stats for the \'BigHoldingCat\' state. | 1 |
| [`Bishop`](./Characters_and_Bosses.md#object-bishop) | Object | Character Form / AI State: Behavior and stats for the \'Bishop\' state. | 1 |
| [`BlackHole`](./Characters_and_Bosses.md#object-blackhole) | Object | Character Form / AI State: Behavior and stats for the \'BlackHole\' state. | 1 |
| [`Bomb`](./Characters_and_Bosses.md#object-bomb) | Object | Character Form / AI State: Behavior and stats for the 'Bomb' state. | 1 |
| [`Bully`](./Characters_and_Bosses.md#object-bully) | Object | Character Form / AI State: Behavior and stats for the 'Bully' state. | 1 |
| [`Butcher`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Applies or references the 'Butcher' effect/state. | 1 |
| [`CaveBaby`](./Characters_and_Bosses.md#object-cavebaby) | Object | Character Form: Behavior and stats for the \'CaveBaby\' state. | 1 |
| [`CaveWoman`](./Characters_and_Bosses.md#object-cavewoman) | Object | Character Form: Behavior and stats for the \'CaveWoman\' state. | 1 |
| [`CaveWomanHasCat`](./Characters_and_Bosses.md#object-cavewomanhascat) | Object | Character Form: Behavior and stats for the \'CaveWomanHasCat\' state. | 1 |
| [`Charging`](./Characters_and_Bosses.md#object-charging) | Object | Character Form / AI State: Behavior when charging an attack. | 1 |
| [`Close`](./Characters_and_Bosses.md#object-close) | Object | AI Movement logic: Maneuvers into close/melee range. | 1 |
| [`Colorless`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | Applies or references the 'Colorless' effect/state. | 1 |
| [`Cultist`](./Characters_and_Bosses.md#object-cultist) | Object | Character Form: Behavior and stats for the \'Cultist\' state. | 1 |
| [`Damaged`](./Characters_and_Bosses.md#object-damaged) | Object | Character Form / AI State: Behavior when health is critically low. | 1 |
| [`Default_Ceiling`](./Characters_and_Bosses.md#object-default_ceiling) | Object | Character Form: The baseline behavior state while attached to the ceiling. | 1 |
| [`Default_Ground`](./Characters_and_Bosses.md#object-default_ground) | Object | Character Form: The baseline behavior state while on the ground. | 1 |
| [`DesireMech`](./Characters_and_Bosses.md#object-desiremech) | Object | Character Form: Behavior and stats for the 'DesireMech' state. | 1 |
| [`Druid`](./Engine_LogicKeys.md#valid-property-keys) | Object | Applies or references the 'Druid' effect/state. | 1 |
| [`Drunker`](./Characters_and_Bosses.md#object-drunker) | Object | Character Form: Behavior and stats for the 'Drunker' state. | 1 |
| [`DualSword`](./Characters_and_Bosses.md#object-dualsword) | Object | Character Form: Behavior and stats for the \'DualSword\' state. | 1 |
| [`DualSword_Primed`](./Characters_and_Bosses.md#object-dualsword_primed) | Object | Character Form: Behavior and stats for the \'DualSword_Primed\' state. | 1 |
| [`Dumb`](./Characters_and_Bosses.md#object-dumb) | Object | AI Profile: A simplified, less optimal decision-making profile. | 1 |
| [`Explody`](./Characters_and_Bosses.md#object-explody) | Object | Character Form: Behavior and stats for the 'Explody' state. | 1 |
| [`Fighter`](./Engine_LogicKeys.md#valid-property-keys) | Object | Applies or references the 'Fighter' effect/state. | 1 |
| [`FightPhase`](./Characters_and_Bosses.md#object-fightphase) | Object | Boss Logic: Main combat phase. | 1 |
| [`Fire`](./Characters_and_Bosses.md#object-fire) | Object | Character Form: Behavior and stats for the 'Fire' state. | 1 |
| [`FireFull`](./Characters_and_Bosses.md#object-firefull) | Object | Character Form: Behavior and stats for the 'FireFull' state. | 1 |
| [`Flop`](./Characters_and_Bosses.md#object-flop) | Object | Character Form: Behavior and stats for the \'Flop\' state. | 1 |
| [`Flop2`](./Characters_and_Bosses.md#object-flop2) | Object | Character Form: Behavior and stats for the \'Flop2\' state. | 1 |
| [`Flush`](./Characters_and_Bosses.md#object-flush) | Object | Character Form: Behavior and stats for the 'Flush' state. | 1 |
| [`FlushBubs`](./Characters_and_Bosses.md#object-flushbubs) | Object | Character Form: Behavior and stats for the 'FlushBubs' state. | 1 |
| [`FlushHost`](./Characters_and_Bosses.md#object-flushhost) | Object | Character Form: Behavior and stats for the 'FlushHost' state. | 1 |
| [`FlushNettle`](./Characters_and_Bosses.md#object-flushnettle) | Object | Character Form: Behavior and stats for the 'FlushNettle' state. | 1 |
| [`Grappling`](./Characters_and_Bosses.md#object-grappling) | Object | Character Form / AI State: Behavior while grappling an opponent. | 1 |
| [`Grown`](./Characters_and_Bosses.md#object-grown) | Object | Character Form: Behavior and stats for the \'Grown\' state. | 1 |
| [`GuaranteedJackpot`](./Characters_and_Bosses.md#object-guaranteedjackpot) | Object | Loot Logic: Guarantees a high-tier drop. | 1 |
| [`Guarding`](./Characters_and_Bosses.md#object-guarding) | Object | Character Form / AI State: Defensive behavior state. | 1 |
| [`HalfDead`](./Characters_and_Bosses.md#object-halfdead) | Object | Character Form: Behavior and stats for the \'HalfDead\' state. | 1 |
| [`HasDeadCat`](./Characters_and_Bosses.md#object-hasdeadcat) | Object | Character Form: Behavior and stats for the \'HasDeadCat\' state. | 1 |
| [`HasRock`](./Characters_and_Bosses.md#object-hasrock) | Object | Character Form: Behavior and stats for the \'HasRock\' state. | 1 |
| [`Headless`](./Characters_and_Bosses.md#object-headless) | Object | Character Form: Behavior and stats for the \'Headless\' state. | 1 |
| [`Hint_CrackedVisuals`](./Characters_and_Bosses.md#object-hint_crackedvisuals) | Object | Visual: Overlay effects for cracked/damaged terrain or objects. | 1 |
| [`Hint_CrackedVisuals2`](./Characters_and_Bosses.md#object-hint_crackedvisuals2) | Object | Visual: Secondary cracked visual overlay. | 1 |
| [`Hint_CrackedVisuals3`](./Characters_and_Bosses.md#object-hint_crackedvisuals3) | Object | Visual: Tertiary cracked visual overlay. | 1 |
| [`HumanDead`](./Characters_and_Bosses.md#object-humandead) | Object | Character Form: Behavior and stats for the \'HumanDead\' state. | 1 |
| [`Hunter`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | Applies or references the 'Hunter' effect/state. | 1 |
| [`InitialPhase`](./Characters_and_Bosses.md#object-initialphase) | Object | Boss Logic: The starting phase of an encounter. | 1 |
| [`Insane_Ceiling`](./Characters_and_Bosses.md#object-insane_ceiling) | Object | Character Form: Insane behavior state while attached to the ceiling. | 1 |
| [`Insane_Ground`](./Characters_and_Bosses.md#object-insane_ground) | Object | Character Form: Insane behavior state while on the ground. | 1 |
| [`Johnny`](./Characters_and_Bosses.md#object-johnny) | Object | Character Form: Behavior and stats for the 'Johnny' state. | 1 |
| [`JohnnyBubs`](./Characters_and_Bosses.md#object-johnnybubs) | Object | Character Form: Behavior and stats for the 'JohnnyBubs' state. | 1 |
| [`JohnnyHost`](./Characters_and_Bosses.md#object-johnnyhost) | Object | Character Form: Behavior and stats for the 'JohnnyHost' state. | 1 |
| [`JohnnyNettle`](./Characters_and_Bosses.md#object-johnnynettle) | Object | Character Form: Behavior and stats for the 'JohnnyNettle' state. | 1 |
| [`Joystick`](./Characters_and_Bosses.md#object-joystick) | Object | Character Form: Behavior and stats for the \'Joystick\' state. | 1 |
| [`LastHit`](./Characters_and_Bosses.md#object-lasthit) | Object | Logic: Executes logic on the final hit of a multi-hit attack. | 1 |
| [`Lifted`](./Characters_and_Bosses.md#object-lifted) | Object | Character Form: Behavior and stats for the \'Lifted\' state. | 1 |
| [`Lit`](./Characters_and_Bosses.md#object-lit) | Object | Character Form: Behavior and stats for the 'Lit' state. | 1 |
| [`Mage`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Applies or references the 'Mage' effect/state. | 1 |
| [`Medic`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | Applies or references the 'Medic' effect/state. | 1 |
| [`Monk`](./Engine_LogicKeys.md#valid-property-keys) | Object | Applies or references the 'Monk' effect/state. | 1 |
| [`Mounted`](./Characters_and_Bosses.md#object-mounted) | Object | Character Form: Behavior and stats for the \'Mounted\' state. | 1 |
| [`MouthFull`](./Characters_and_Bosses.md#object-mouthfull) | Object | Character Form: Behavior and stats for the \'MouthFull\' state. | 1 |
| [`Mutant`](./Characters_and_Bosses.md#object-mutant) | Object | Character Form: Behavior and stats for the \'Mutant\' state. | 1 |
| [`Necromancer`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Applies or references the 'Necromancer' effect/state. | 1 |
| [`NeutronStar`](./Characters_and_Bosses.md#object-neutronstar) | Object | Character Form: Behavior and stats for the 'NeutronStar' state. | 1 |
| [`NoDeathRattle`](./Engine_LogicKeys.md#valid-property-keys) | Object | Applies or references the 'NoDeathRattle' effect/state. | 1 |
| [`NoEyes`](./Characters_and_Bosses.md#object-noeyes) | Object | Character Form: Behavior and stats for the \'NoEyes\' state. | 1 |
| [`NormalFull`](./Characters_and_Bosses.md#object-normalfull) | Object | Character Form: Behavior and stats for the 'NormalFull' state. | 1 |
| [`NoStick`](./Characters_and_Bosses.md#object-nostick) | Object | Character Form: Behavior and stats for the 'NoStick' state. | 1 |
| [`Nuke`](./Characters_and_Bosses.md#object-nuke) | Object | Character Form: Behavior and stats for the 'Nuke' state. | 1 |
| [`Obey`](./Characters_and_Bosses.md#object-obey) | Object | AI State: Enforced compliance logic (e.g., when Charmed). | 1 |
| [`Off`](./Characters_and_Bosses.md#object-off) | Object | Character Form: Behavior and stats for the 'Off' state. | 1 |
| [`OffScreen`](./Characters_and_Bosses.md#object-offscreen) | Object | Character Form: Behavior and stats for the 'OffScreen' state. | 1 |
| [`OneEye`](./Characters_and_Bosses.md#object-oneeye) | Object | Character Form: Behavior and stats for the \'OneEye\' state. | 1 |
| [`Open`](./Characters_and_Bosses.md#object-open) | Object | Character Form: Behavior and stats for the 'Open' state. | 1 |
| [`OpenCat`](./Characters_and_Bosses.md#object-opencat) | Object | Character Form: Behavior and stats for the 'OpenCat' state. | 1 |
| [`Out`](./Characters_and_Bosses.md#object-out) | Object | Character Form: Behavior and stats for the 'Out' state. | 1 |
| [`Possessing`](./Characters_and_Bosses.md#object-possessing) | Object | Character Form: Behavior and stats for the \'Possessing\' state. | 1 |
| [`Primed`](./Characters_and_Bosses.md#object-primed) | Object | Character Form: Behavior and stats for the 'Primed' state. | 1 |
| [`Psychic`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Applies or references the 'Psychic' effect/state. | 1 |
| [`Pulp2`](./Characters_and_Bosses.md#object-pulp2) | Object | Character Form: Behavior and stats for the 'Pulp2' state. | 1 |
| [`Pulp3`](./Characters_and_Bosses.md#object-pulp3) | Object | Character Form: Behavior and stats for the 'Pulp3' state. | 1 |
| [`Pulp4`](./Characters_and_Bosses.md#object-pulp4) | Object | Character Form: Behavior and stats for the 'Pulp4' state. | 1 |
| [`Pulp5`](./Characters_and_Bosses.md#object-pulp5) | Object | Character Form: Behavior and stats for the 'Pulp5' state. | 1 |
| [`Pulp6`](./Characters_and_Bosses.md#object-pulp6) | Object | Character Form: Behavior and stats for the 'Pulp6' state. | 1 |
| [`Pulp7`](./Characters_and_Bosses.md#object-pulp7) | Object | Character Form: Behavior and stats for the 'Pulp7' state. | 1 |
| [`Sitting`](./Characters_and_Bosses.md#object-sitting) | Object | Character Form: Behavior and stats for the 'Sitting' state. | 1 |
| [`SmallHolding`](./Characters_and_Bosses.md#object-smallholding) | Object | Character Form: Behavior and stats for the \'SmallHolding\' state. | 1 |
| [`SmallHoldingCat`](./Characters_and_Bosses.md#object-smallholdingcat) | Object | Character Form: Behavior and stats for the \'SmallHoldingCat\' state. | 1 |
| [`SpawningPhase`](./Characters_and_Bosses.md#object-spawningphase) | Object | Boss Logic: Phase focused on summoning minions. | 1 |
| [`Standing`](./Characters_and_Bosses.md#object-standing) | Object | Character Form: Behavior and stats for the 'Standing' state. | 1 |
| [`Standing2`](./Characters_and_Bosses.md#object-standing2) | Object | Character Form: Behavior and stats for the 'Standing2' state. | 1 |
| [`Start_Ceiling`](./Characters_and_Bosses.md#object-start_ceiling) | Object | Character Form: Behavior and stats for the 'Start_Ceiling' state. | 1 |
| [`Stop`](./Characters_and_Bosses.md#object-stop) | Object | AI Movement: Forces the character to cease movement. | 1 |
| [`SwordAndShield`](./Characters_and_Bosses.md#object-swordandshield) | Object | Character Form: Behavior and stats for the 'SwordAndShield' state. | 1 |
| [`SwordAndShield_Primed`](./Characters_and_Bosses.md#object-swordandshield_primed) | Object | Character Form: Behavior and stats for the \'SwordAndShield_Primed\' state. | 1 |
| `sync_brain_patterns` | Boolean |  | 1 |
| [`Tank`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Applies or references the 'Tank' effect/state. | 1 |
| [`Tar`](./Characters_and_Bosses.md#object-tar) | Object | Character Form: Behavior and stats for the 'Tar' state. | 1 |
| [`TarFull`](./Characters_and_Bosses.md#object-tarfull) | Object | Character Form: Behavior and stats for the 'TarFull' state. | 1 |
| [`Thief`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Applies or references the 'Thief' effect/state. | 1 |
| [`Throb`](./Characters_and_Bosses.md#object-throb) | Object | Character Form: Behavior and stats for the 'Throb' state. | 1 |
| [`ThrobBubs`](./Characters_and_Bosses.md#object-throbbubs) | Object | Character Form: Behavior and stats for the 'ThrobBubs' state. | 1 |
| [`ThrobHost`](./Characters_and_Bosses.md#object-throbhost) | Object | Character Form: Behavior and stats for the 'ThrobHost' state. | 1 |
| [`ThrobNettle`](./Characters_and_Bosses.md#object-throbnettle) | Object | Character Form: Behavior and stats for the 'ThrobNettle' state. | 1 |
| [`Tinkerer`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | Applies or references the 'Tinkerer' effect/state. | 1 |
| [`Transformed`](./Characters_and_Bosses.md#object-transformed) | Object | Character Form: Behavior and stats for the 'Transformed' state. | 1 |
| [`TwoEyes`](./Characters_and_Bosses.md#object-twoeyes) | Object | Character Form: Behavior and stats for the 'TwoEyes' state. | 1 |
| `uifloaters_offset` | Number |  | 1 |
| [`Unlit`](./Characters_and_Bosses.md#object-unlit) | Object | Character Form: Behavior and stats for the 'Unlit' state. | 1 |
| [`Unmounted`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Applies or references the 'Unmounted' effect/state. | 1 |
| [`Unwashed`](./Characters_and_Bosses.md#object-unwashed) | Object | Character Form: Behavior and stats for the 'Unwashed' state. | 1 |
| [`Washed`](./Characters_and_Bosses.md#object-washed) | Object | Character Form: Behavior and stats for the 'Washed' state. | 1 |
| [`Washer`](./Characters_and_Bosses.md#object-washer) | Object | Character Form: Behavior and stats for the \'Washer\' state. | 1 |
| [`Water`](./Characters_and_Bosses.md#object-water) | Object | Character Form: Behavior and stats for the \'Water\' state. | 1 |
| [`WereMan`](./Characters_and_Bosses.md#object-wereman) | Object | Character Form: Behavior and stats for the \'WereMan\' state. | 1 |
| [`Zealot`](./Characters_and_Bosses.md#object-zealot) | Object | Character Form: Behavior and stats for the \'Zealot\' state. | 1 |
| [`ZealotBomb`](./Characters_and_Bosses.md#object-zealotbomb) | Object | Character Form: Behavior and stats for the \'ZealotBomb\' state. | 1 |
| [`Die`](./Characters_and_Bosses.md#object-die) | Object | Character Form / Logic: Forces the character to die. | 0 |
| [`Rain`](./Characters_and_Bosses.md#object-rain) | Object | Character Form: Behavior and stats for the 'Rain' state. | 0 |

</details>

---

### Object: `SpawnOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 79

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 3 |
| [`obj`](./Arrays.md#array-obj) | Array |  | 3 |
| [`additional_statuses`](./Characters_and_Bosses.md#object-additional_statuses) | Object | Generic statuses added to the character. | 1 |

</details>

---

### Object: `sound`


**Definition:** Audio bindings.
**Total Count:** 62


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alt_sounds`](./Arrays.md#array-alt_sounds) | Array |  | 61 |
| [`animation_prefix`](./Enums.md#enum-animation_prefix) | Enum |  | 1 |

</details>

---

### Object: `Robot`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 46

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alternate_energized_effect`](./Characters_and_Bosses.md#object-alternate_energized_effect) | Object | Overrides default energized visuals. | 2 |

</details>

---

### Object: `turns`


**Definition:** Turn counter tracking.
**Total Count:** 45


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`Bishop`](./Characters_and_Bosses.md#object-bishop), [`Bully`](./Characters_and_Bosses.md#object-bully), [`Default`](./Characters_and_Bosses.md#object-default), [`Default_Ceiling`](./Characters_and_Bosses.md#object-default_ceiling), [`Default_Ground`](./Characters_and_Bosses.md#object-default_ground), [`FightPhase`](./Characters_and_Bosses.md#object-fightphase), [`Holding`](./Characters_and_Bosses.md#object-holding), [`InitialPhase`](./Characters_and_Bosses.md#object-initialphase), [`Insane_Ceiling`](./Characters_and_Bosses.md#object-insane_ceiling), [`Insane_Ground`](./Characters_and_Bosses.md#object-insane_ground), [`LastHit`](./Characters_and_Bosses.md#object-lasthit), [`Lifted`](./Characters_and_Bosses.md#object-lifted), [`Mutant`](./Characters_and_Bosses.md#object-mutant), [`Normal`](./Characters_and_Bosses.md#object-normal), [`NotPriming`](./Characters_and_Bosses.md#object-notpriming), [`Nuke`](./Characters_and_Bosses.md#object-nuke), [`OffMap`](./Characters_and_Bosses.md#object-offmap), [`OffScreen`](./Characters_and_Bosses.md#object-offscreen), [`OneAlive`](./Characters_and_Bosses.md#object-onealive), [`Possessing`](./Characters_and_Bosses.md#object-possessing), and 13 more...

| Key | Type | Definition | Count |
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

### Object: `equipment`


**Definition:** List of item IDs the character spawns equipped with.
**Total Count:** 44


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`face`](./Enums.md#enum-face) | Enum |  | 16 |
| [`head`](./Enums.md#enum-head) | Enum |  | 14 |
| [`neck`](./Enums.md#enum-neck) | Enum |  | 10 |
| [`weapon`](./Enums.md#enum-weapon) | Enum | Weapon item constraint. | 7 |

</details>

---

### Object: `mainturn_pattern`


**Definition:** AI Logic: Determines standard ability usage during the main turn.
**Total Count:** 44


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum |  | 23 |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 9 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 8 |
| [`do_strict`](./Arrays.md#array-do_strict) | Array |  | 2 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum |  | 2 |

</details>

---

### Object: `Default`


**Definition:** Baseline configuration.
**Total Count:** 37


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 10 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |

</details>

---

### Object: `FormChangeWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 35 |
| [`form_hasnot`](./Enums.md#enum-form_hasnot) | Enum |  | 30 |
| [`form_has`](./Enums.md#enum-form_has) | Enum |  | 25 |

</details>

---

### Object: `virtual_abilities`


**Definition:** Abilities that are evaluated but not directly castable by the player.
**Total Count:** 35


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`MoveAway`](./Characters_and_Bosses.md#object-moveaway) | Object | AI Movement: Moves away from the target. | 4 |
| [`MoveClose`](./Characters_and_Bosses.md#object-moveclose) | Object | AI Movement: Moves into melee range. | 4 |
| [`DashRandomly`](./Characters_and_Bosses.md#object-dashrandomly) | Object | AI Movement: Dashes to a random valid tile. | 2 |
| [`Escape`](./Characters_and_Bosses.md#object-escape) | Object | AI Movement: Logic for fleeing or escaping the map. | 2 |
| [`MoveCenter`](./Characters_and_Bosses.md#object-movecenter) | Object | AI Movement: Moves toward the center of the map. | 2 |
| [`MoveForThrow`](./Characters_and_Bosses.md#object-moveforthrow) | Object | AI Movement: Repositions to gain line of sight for throwing. | 2 |
| [`SpearRun`](./Characters_and_Bosses.md#object-spearrun) | Object | AI Movement: Specific movement logic for Spear enemies. | 2 |
| [`CerberubsJumpBlind`](./Characters_and_Bosses.md#object-cerberubsjumpblind) | Object | AI Logic: Blind jump attack pattern for Cerberubs. | 1 |
| [`CerberubsJumpNormal`](./Characters_and_Bosses.md#object-cerberubsjumpnormal) | Object | AI Logic: Normal jump attack pattern for Cerberubs. | 1 |
| [`CloseConvert`](./Characters_and_Bosses.md#object-closeconvert) | Object | AI State: Logic for converting adjacent units. | 1 |
| [`FoodMove`](./Characters_and_Bosses.md#object-foodmove) | Object | AI Movement: Logic for seeking out food items. | 1 |
| [`ForceTrample`](./Characters_and_Bosses.md#object-forcetrample) | Object | Logic: Forces movement to act as a trample attack. | 1 |
| [`LeapClose`](./Characters_and_Bosses.md#object-leapclose) | Object | AI Movement: Executes a jumping maneuver to close distance. | 1 |
| [`MoveForBarrage`](./Characters_and_Bosses.md#object-moveforbarrage) | Object | AI Movement: Repositions to optimize a barrage attack. | 1 |
| [`MoveForDash`](./Characters_and_Bosses.md#object-movefordash) | Object | AI Movement: Repositions to set up a dash attack line. | 1 |
| [`MoveForGrass`](./Characters_and_Bosses.md#object-moveforgrass) | Object | AI Movement: Moves toward grass tiles. | 1 |
| [`MoveForPounce`](./Characters_and_Bosses.md#object-moveforpounce) | Object | AI Movement: Repositions to optimize a pounce trajectory. | 1 |
| [`MoveForSpin`](./Characters_and_Bosses.md#object-moveforspin) | Object | AI Movement: Repositions into a cluster of enemies for a spin attack. | 1 |
| [`MoveOneForPuke`](./Characters_and_Bosses.md#object-moveoneforpuke) | Object | AI Movement: Specific positioning logic for puke attacks. | 1 |
| [`MoveSpaced`](./Characters_and_Bosses.md#object-movespaced) | Object | AI Movement: Moves to maintain a specific distance from targets. | 1 |
| [`MoveToHead`](./Characters_and_Bosses.md#object-movetohead) | Object | AI Movement: Navigates toward the 'head' or primary target. | 1 |
| [`MoveTowards`](./Characters_and_Bosses.md#object-movetowards) | Object | AI Movement: Moves toward the nearest target. | 1 |
| [`NCGravecrawlFAR`](./Characters_and_Bosses.md#object-ncgravecrawlfar) | Object | AI Movement: Specific grapple/crawl logic. | 1 |
| [`ReturnA`](./Characters_and_Bosses.md#object-returna) | Object | Boss Logic: Specific phase return trigger. | 1 |
| [`RunFar`](./Characters_and_Bosses.md#object-runfar) | Object | AI Movement: Maximize distance from targets. | 1 |
| [`SuckMF`](./Characters_and_Bosses.md#object-suckmf) | Object | Character Form: Behavior and stats for the 'SuckMF' state. | 1 |
| [`TF_TargetAllies`](./Characters_and_Bosses.md#object-tf_targetallies) | Object | AI Targeting: Prioritizes allies. | 1 |
| [`TF_TargetEnemies`](./Characters_and_Bosses.md#object-tf_targetenemies) | Object | AI Targeting: Prioritizes enemies. | 1 |
| [`Unflip`](./Characters_and_Bosses.md#object-unflip) | Object | Logic: Reverses a flipped state. | 1 |

</details>

---

### Object: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 32

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#object-randompassivepool), [`StacyMutant_Counter`](./Characters_and_Bosses.md#object-stacymutant_counter), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 119 |

</details>

---

### Object: `DeathRattle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 29

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 8 |
| `is_dying_animation` | Boolean |  | 7 |
| `pop_corpse` | Boolean |  | 6 |
| `cancel_knockback` | Boolean |  | 1 |
| `immediate` | Boolean |  | 1 |
| `must_target_killer` | Boolean |  | 1 |
| `target_killer` | Boolean |  | 1 |

</details>

---

### Object: `bonusturn_pattern`


**Definition:** AI Logic: Determines ability usage during bonus turns.
**Total Count:** 27


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum |  | 19 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 11 |
| [`do_strict`](./Arrays.md#array-do_strict) | Array |  | 5 |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 4 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum |  | 1 |

</details>

---

### Object: `CatPartsTransform`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 25

> **Referenced by:** [`PassiveGroup`](./Characters_and_Bosses.md#object-passivegroup), [`StacyMutant_Brace`](./Characters_and_Bosses.md#object-stacymutant_brace), [`StacyMutant_Counter`](./Characters_and_Bosses.md#object-stacymutant_counter), [`StacyMutant_Damage`](./Characters_and_Bosses.md#object-stacymutant_damage), [`StacyMutant_DoubleHead`](./Characters_and_Bosses.md#object-stacymutant_doublehead), [`StacyMutant_Fire`](./Characters_and_Bosses.md#object-stacymutant_fire), [`StacyMutant_Health`](./Characters_and_Bosses.md#object-stacymutant_health), [`StacyMutant_Holy`](./Characters_and_Bosses.md#object-stacymutant_holy), [`StacyMutant_Ice`](./Characters_and_Bosses.md#object-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#object-stacymutant_lightning), [`StacyMutant_Mirror`](./Characters_and_Bosses.md#object-stacymutant_mirror), [`StacyMutant_Speed`](./Characters_and_Bosses.md#object-stacymutant_speed), [`StacyMutant_Thorns`](./Characters_and_Bosses.md#object-stacymutant_thorns), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`palette`](./Enums.md#enum-palette) | Enum |  | 16 |
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

### Object: `fallback`


**Definition:** Logic executed if primary options fail.
**Total Count:** 23


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum |  | 12 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 6 |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 1 |
| [`do_best`](./Arrays.md#array-do_best) | Array |  | 1 |
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array |  | 1 |
| [`do_random`](./Arrays.md#array-do_random) | Array |  | 1 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum |  | 1 |

</details>

---

### Object: `BossRewards`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 20 |
| [`common`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| [`rare`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 0 |

</details>

---

### Object: `AbilityReaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 19

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 9 |
| `ability_damage_only` | Boolean |  | 6 |
| `backstabs_only` | Boolean |  | 3 |
| `only_when_not_your_turn` | Boolean |  | 3 |
| `cancel_knockback` | Boolean |  | 1 |
| `enemies_only` | Boolean |  | 1 |
| `even_on_0_damage_if_knockback` | Boolean |  | 1 |
| `even_on_0_damage` | Boolean |  | 1 |
| `match_knockback_direction` | Boolean |  | 1 |
| `ranged_only` | Boolean |  | 1 |
| `verify_target` | Boolean |  | 1 |

</details>

---

### Object: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 19

> **Referenced by:** [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#object-temppassiveuntilsettled), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 36 |
| `damage` | Number | The base damage properties of an attack. | 11 |
| `knockback` | Number |  | 9 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 8 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 5 |
  | [`AddDamageToElementDamage`](#adddamagetoelementdamage) | Object | Applies or references the 'AddDamageToElementDamage' effect/state. | 0 |
  | [`AddStatusToElementDamage`](#addstatustoelementdamage) | Object | Applies the 'AddStatusToElementDamage' effect. | 0 |
  | [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. | 0 |
  | [`StatusImmunity`](./Enums.md#enum-statusimmunity) | Enum | Applies or references the 'StatusImmunity' effect/state. | 0 |
| `cant_miss` | `Boolean` |  | 0 |
| [`effects`](./Characters_and_Bosses.md#object-effects) | Object | Non-damaging impact triggers. | 0 |

</details>

---

### Object: `BirdRewards`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ally_rewards`](./Characters_and_Bosses.md#object-ally_rewards) | Object | Loot logic triggered if an ally dies. | 18 |
| [`statuses`](./Characters_and_Bosses.md#object-statuses) | Object | Status effects possessed by the character. | 5 |

</details>

---

### Object: `ally_rewards`


**Definition:** Loot logic triggered if an ally dies.
**Total Count:** 18


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`BirdRewards`](./Characters_and_Bosses.md#object-birdrewards)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 18 |

</details>

---

### Object: `alt_spawn_pool`


**Definition:** Alternative pools to draw minions from.
**Total Count:** 18


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Antidote`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Applies or references the 'Antidote' effect/state. | 5 |
| `Blessing` | Mixed | Applies or references the 'Blessing' effect/state. | 5 |
| `BigCatnip` | Number | Applies or references the 'BigCatnip' effect/state. | 4 |
| `BigScrap` | Number | Applies or references the 'BigScrap' effect/state. | 4 |
| `BiggestFood` | Number | Applies or references the 'BiggestFood' effect/state. | 4 |
| `Coin` | Number | Applies or references the 'Coin' effect/state. | 4 |
| `BigFood` | Number | Applies or references the 'BigFood' effect/state. | 2 |
| `Coin10` | Mixed | Applies or references the 'Coin10' effect/state. | 2 |
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

### Object: `CharacterLightSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`color`](./Arrays.md#array-color) | Array |  | 16 |
| `size` | Number |  | 16 |
| [`glow`](./Arrays.md#array-glow) | Array |  | 8 |

</details>

---

### Object: `HealthPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array |  | 15 |
| `stacks` | Number | Number of stacks or intensity to apply. | 15 |
| `stored_food_value` | Number |  | 15 |
| `anything_eats` | Boolean |  | 4 |
| `force_frame` | Number |  | 1 |

</details>

---

### Object: `ImmediateAbilityReaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 13 |
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

### Object: `effects`

> **Definition:** Non-damaging impact triggers.


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

> **Referenced by:** [`MeleeRevengeDamage`](./Characters_and_Bosses.md#object-meleerevengedamage), [`damage_instance`](./Characters_and_Bosses.md#object-damage_instance), [`eat_damage`](./Characters_and_Bosses.md#object-eat_damage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1886 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 552 |
| `BlackHoleSuck` | `Number` | Applies or references the 'BlackHoleSuck' effect/state. | 0 |
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 0 |

</details>

---

### Object: `AbilityHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 12 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 |
| `even_if_stunned` | Boolean |  | 6 |
| `immediate` | Boolean |  | 5 |
| `use_ai` | Boolean |  | 2 |
| [`threshold_min`](./Math_Equations.md) | Equation |  | 1 |
| `also_use_if_buddy_is_dead` | Boolean |  | 1 |

</details>

---

### Object: `PassiveGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#object-randompassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 |

</details>

---

### Object: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 12 |
| `good` | Boolean |  | 8 |
| `spawn_on_death_hit` | Boolean |  | 6 |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Probability (0.0 to 1.0) of executing this action. | 4 |
| `coins` | Number |  | 2 |
| [`auto_cast`](./Enums.md#enum-auto_cast) | Enum |  | 1 |
| `consider_all_layers` | Boolean |  | 1 |
| `melee_ability_only` | Boolean |  | 1 |

</details>

---

### Object: `round_end_bonusturn_pattern`


**Definition:** AI Logic: Ability usage pattern during round-end bonus turns.
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 6 |
| [`do`](./Enums.md#enum-do) | Enum |  | 3 |
| [`do_one`](./Arrays.md#array-do_one) | Array |  | 2 |
| [`do_random`](./Arrays.md#array-do_random) | Array |  | 2 |
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array |  | 1 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 1 |

</details>

---

### Object: `Normal`


**Definition:** Character Form: Behavior and stats for the \'Normal\' state.
**Total Count:** 11


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 5 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |

</details>

---

### Object: `DeathRattleRevive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 8 |
| `even_if_stunned` | Boolean |  | 8 |

</details>

---

### Object: `MoveWhenDamaged`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 7 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 1 |

</details>

---

### Object: `Rage`


**Definition:** Character Form: Behavior and stats for the \'Rage\' state.
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 8 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 6 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 4 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| `move_speed_multiplier` | Number |  | 1 |

</details>

---

### Object: `FormChangeOnElementInfluence`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 9 |
| [`form`](./Enums.md#enum-form) | Enum |  | 9 |
| [`exclude`](./Enums.md#enum-exclude) | Enum |  | 5 |
| [`particle`](./Enums.md#enum-particle) | Enum |  | 5 |
| [`sfx`](./Enums.md#enum-sfx) | Enum |  | 5 |

</details>

---

### Object: `ReflectProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
  | [`self_damage`](./Arrays.md#array-self_damage) | Object | Recoil or self-inflicted damage/effects applied to the caster. | 0 |

</details>

---

### Object: `StatusCollector`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `TransformInXTurns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#object-randompassivepool), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array |  | 8 |
| `stacks` | Number | Number of stacks or intensity to apply. | 8 |
| [`initiative`](./Enums.md#enum-initiative) | Enum |  | 4 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |
| [`turns`](./Arrays.md#array-turns) | Array | Turn counter tracking. | 1 |

</details>

---

### Object: `TransformOnElementInfluence`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 9 |
| [`object`](./Enums.md#enum-object) | Enum |  | 9 |

</details>

---

### Object: `statuses`


**Definition:** Status effects possessed by the character.
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`BirdRewards`](./Characters_and_Bosses.md#object-birdrewards), [`Cat`](./Characters_and_Bosses.md#object-cat), [`NonCat`](./Characters_and_Bosses.md#object-noncat)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |

</details>

---

### Object: `FormChangeOffMap`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_offmap`](./Enums.md#enum-form_offmap) | Enum |  | 8 |
| [`form_onmap`](./Enums.md#enum-form_onmap) | Enum |  | 8 |

</details>

---

### Object: `SmallRockBehavior`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 4 |
| `knockback` | Number |  | 4 |
| `chain` | Boolean |  | 2 |

</details>

---

### Object: `ChanceToSpitOnDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 7 |
| `flat_chance` | Number |  | 5 |
| `chance_per_damage` | Number |  | 3 |
| `backstabs_only` | Boolean |  | 1 |
| `even_on_0_damage_if_knockback` | Boolean |  | 1 |

</details>

---

### Object: `MovementReaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 7 |
| `enemies_only` | Boolean |  | 3 |
| `objects_too` | Boolean |  | 2 |
| `on_self_move_too` | Boolean |  | 2 |
| `blind_spot` | Boolean |  | 1 |
| `forward_only` | Boolean |  | 1 |
| `self_move_exclude_self_abilities` | Boolean |  | 1 |

</details>

---

### Object: `CaveFamilyEnrage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 6 |
| `count` | Number | The numerical quantity. | 6 |

</details>

---

### Object: `FormChangeWhilePrimingAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`not_priming`](./Enums.md#enum-not_priming) | Enum |  | 6 |
| [`priming`](./Enums.md#enum-priming) | Enum |  | 6 |

</details>

---

### Object: `MoveTowardsDamageSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`check_in_form`](./Enums.md#enum-check_in_form) | Enum |  | 2 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 2 |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`check_has_status`](./Enums.md#enum-check_has_status) | Enum |  | 1 |
| [`ignore_tagged_sources`](./Enums.md#enum-ignore_tagged_sources) | Enum |  | 1 |
| `can_move_zero` | Boolean |  | 1 |
| `do_not_move_on_top` | Boolean |  | 1 |
| `face_towards_after` | Boolean |  | 1 |
| `move_far` | Boolean |  | 1 |
| `move_short` | Boolean |  | 1 |

</details>

---

### Object: `SecurityBotProtect`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 5 |
| [`move`](./Enums.md#enum-move) | Enum |  | 3 |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum |  | 3 |
| `enemies_only` | Boolean |  | 3 |
| `not_on_kill` | Boolean |  | 2 |

</details>

---

### Object: `HasCat`


**Definition:** Character Form: Behavior and stats for the \'HasCat\' state.
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 7 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 5 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 5 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 4 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |

</details>

---

### Object: `MoveTowardsKillers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`character_filter`](./Arrays.md#array-character_filter) | Array |  | 3 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 3 |

</details>

---

### Object: `PassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 5 |

</details>

---

### Object: `TransformOnDeathImmediately`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum |  | 4 |
| [`obj`](./Enums.md#enum-obj) | Enum |  | 4 |

</details>

---

### Object: `BaitAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `range` | Number | Distance or area of effect in tiles. | 4 |

</details>

---

### Object: `Consumed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`statuses`](./Characters_and_Bosses.md#object-statuses)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 23 |
| `use_placeholder` | Boolean |  | 2 |
| `do_not_pop_corpse` | `Boolean` |  | 0 |
| [`drop_on_death`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` |  | 0 |
| `force_contact` | `Boolean` | If true, enforces physical overlap. | 0 |
| `instant` | `Boolean` |  | 0 |
| [`mount_mode`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | If true, treats the consumption as riding/mounting instead of eating. | 0 |
| [`struggle_ability`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Ability triggered by the consumed entity while inside the consumer. | 0 |

</details>

---

### Object: `ForceUseAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`FinalBossHitCountdownBoris`](./Characters_and_Bosses.md#object-finalbosshitcountdownboris), [`FinalBossHitCountdownExplosive`](./Characters_and_Bosses.md#object-finalbosshitcountdownexplosive)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| `show_name` | Boolean |  | 2 |

</details>

---

### Object: `MoveAway`


**Definition:** AI Movement: Moves away from the target.
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 4 |

</details>

---

### Object: `MoveClose`


**Definition:** AI Movement: Moves into melee range.
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 4 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 3 |

</details>

---

### Object: `OffMap`


**Definition:** Character Form: Behavior and stats for the 'OffMap' state.
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 3 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |

</details>

---

### Object: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 42 |

</details>

---

### Object: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 20 |
  | `BrittleCharismaUp` | Integer | Applies or references the 'BrittleCharismaUp' effect/state. | 0 |
  | `BrittleConstitutionUp` | Integer | Applies or references the 'BrittleConstitutionUp' effect/state. | 0 |
  | `BrittleDexterityUp` | Integer | Applies or references the 'BrittleDexterityUp' effect/state. | 0 |
  | `BrittleIntelligenceUp` | Integer | Applies or references the 'BrittleIntelligenceUp' effect/state. | 0 |
  | `BrittleLuckUp` | Integer | Applies or references the 'BrittleLuckUp' effect/state. | 0 |
  | `BrittleSpeedUp` | Integer | Applies or references the 'BrittleSpeedUp' effect/state. | 0 |
  | `BrittleStrengthUp` | Integer | Applies or references the 'BrittleStrengthUp' effect/state. | 0 |
  | [`UseAbility_NonStack`](./Enums.md#enum-useability_nonstack) | Enum | Applies or references the 'UseAbility_NonStack' effect/state. | 0 |

</details>

---

### Object: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `StunImmunity`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean |  | 1 |

</details>

---

### Object: `Trapper`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| `cancel_movement` | Boolean |  | 2 |
| `pathfinding_avoidance` | Number |  | 2 |
| `range` | Number | Distance or area of effect in tiles. | 2 |

</details>

---

### Object: `default`


**Definition:** Baseline configuration.
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
  | `passives` | Array | List of {Status and Passive Keys}. | 0 |

</details>

---

### Object: `hot`


**Definition:** Visual effect indicator.
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 4 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 4 |

</details>

---

### Object: `keyword_tooltips`


**Definition:** Forces specific UI tooltips to appear.
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`Die`](./Characters_and_Bosses.md#object-die), [`Dumb`](./Characters_and_Bosses.md#object-dumb), [`Obey`](./Characters_and_Bosses.md#object-obey), [`Stop`](./Characters_and_Bosses.md#object-stop)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TVBotDie` | Number | Applies or references the 'TVBotDie' effect/state. | 1 |
| `TVBotDumb` | Number | Applies or references the 'TVBotDumb' effect/state. | 1 |
| `TVBotObey` | Number | Applies or references the 'TVBotObey' effect/state. | 1 |
| `TVBotStop` | Number | Applies or references the 'TVBotStop' effect/state. | 1 |

</details>

---

### Object: `AllAlive`


**Definition:** Encounter State: Logic executed when all specific entities are currently alive.
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
  | `passives` | Array | List of {Status and Passive Keys}. | 0 |

</details>

---

### Object: `ArmorPickup`


**Definition:** Pickup Logic: Defines what happens when an armor item is collected.
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array |  | 3 |
| `stacks` | Number | Number of stacks or intensity to apply. | 3 |

</details>

---

### Object: `Buddy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`obj`](./Enums.md#enum-obj) | Enum |  | 3 |
| `allies_only` | Boolean |  | 3 |
| `reclaim_if_lost` | Boolean |  | 1 |

</details>

---

### Object: `Cat`


**Definition:** Character Form: Base form for standard cats.
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#object-mothertumorpassive), [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#object-mothertumorspawnincapture)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum |  | 3 |
| [`statuses`](./Characters_and_Bosses.md#object-statuses) | Object | Status effects possessed by the character. | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |

</details>

---

### Object: `Down`


**Definition:** Character Form: Behavior and stats for the \'Down\' state.
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |

</details>

---

### Object: `FormChangeHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_above`](./Enums.md#enum-form_above) | Enum |  | 3 |
| [`form_below`](./Enums.md#enum-form_below) | Enum |  | 3 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| `count_shield` | Boolean |  | 1 |

</details>

---

### Object: `Full`


**Definition:** Character Form: Behavior and stats for the \'Full\' state.
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`statuses_on_enter_form`](./Characters_and_Bosses.md#object-statuses_on_enter_form) | Object | Status effects instantly applied upon transitioning into this form. | 2 |

</details>

---

### Object: `ManaPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array |  | 3 |
| `stacks` | Number | Number of stacks or intensity to apply. | 3 |

</details>

---

### Object: `NonCat`


**Definition:** Character Form: Behavior and stats for the 'NonCat' state.
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#object-mothertumorpassive), [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#object-mothertumorspawnincapture)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum |  | 3 |
| [`statuses`](./Characters_and_Bosses.md#object-statuses) | Object | Status effects possessed by the character. | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |

</details>

---

### Object: `OneAlive`


**Definition:** Encounter State: Logic executed when exactly one target is alive.
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 3 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `RandomPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 22 |

</details>

---

### Object: `ReplaceBrain`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`StacyMutant_Fire`](./Characters_and_Bosses.md#object-stacymutant_fire), [`StacyMutant_Ice`](./Characters_and_Bosses.md#object-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#object-stacymutant_lightning)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 3 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 3 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 3 |
| [`pattern`](./Characters_and_Bosses.md#object-pattern) | Object | AI sequence logic. | 3 |

</details>

---

### Object: `SupportFormChangeInsteadOfRun`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| `wait_till_turn` | Boolean |  | 1 |

</details>

---

### Object: `TwoAlive`


**Definition:** Encounter State: Logic executed when exactly two targets are alive.
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 3 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

---

### Object: `Up`


**Definition:** Character Form: Behavior and stats for the \'Up\' state.
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Object: `AbilityOnRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| `force_display_name` | Boolean |  | 2 |

</details>

---

### Object: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 2 |
| `range` | Number | Distance or area of effect in tiles. | 2 |

</details>

---

### Object: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Fury` | Number | Applies or references the 'Fury' effect/state. | 2 |

</details>

---

### Object: `AutocastEachRound`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 1 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 1 |

</details>

---

### Object: `Big`


**Definition:** Character Form / AI State: Behavior and stats for the \'Big\' state.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`animation_suffix`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Object: `Boris`


**Definition:** Character Form / AI State: Behavior and stats for the \'Boris\' state.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `BungaEntrance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum |  | 2 |
| `even_if_stunned` | Boolean |  | 2 |
| `health_threshold` | Number |  | 2 |

</details>

---

### Object: `CaveMan`


**Definition:** Character Form: Behavior and stats for the \'CaveMan\' state.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Object: `CaveManSpear`


**Definition:** Character Form: Behavior and stats for the \'CaveManSpear\' state.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Object: `CherubimReaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Leave`](./Enums.md#enum-leave) | Enum | Applies or references the 'Leave' effect/state. | 2 |
| [`Return`](./Enums.md#enum-return) | Enum | Applies or references the 'Return' effect/state. | 2 |

</details>

---

### Object: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ally_rewards`](./Characters_and_Bosses.md#object-ally_rewards)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 2 |

</details>

---

### Object: `DashRandomly`


**Definition:** AI Movement: Dashes to a random valid tile.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 2 |

</details>

---

### Object: `DiesToElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `instant` | `Boolean` |  | 0 |

</details>

---

### Object: `Empty`


**Definition:** Character Form: Behavior and stats for the \'Empty\' state.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |

</details>

---

### Object: `Escape`


**Definition:** AI Movement: Logic for fleeing or escaping the map.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Object: `Explosive`


**Definition:** Character Form: Behavior and stats for the \'Explosive\' state.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `FaceLastDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean |  | 1 |

</details>

---

### Object: `FormChangeDuringWeatherElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 2 |
| [`form`](./Enums.md#enum-form) | Enum |  | 2 |

</details>

---

### Object: `Holding`


**Definition:** Character Form: Behavior and stats for the \'Holding\' state.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |

</details>

---

### Object: `Holy`


**Definition:** Character Form: Behavior and stats for the \'Holy\' state.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `KnockUpAndAway`

> **Definition:** Logic: Applies vertical and horizontal displacement.


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#object-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#object-conditional_isphysicalattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `displace` | Boolean |  | 2 |
| `distance` | Number | The distance in tiles to knock the target away. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |
  | `circular_variance` | Number | Examples: `2` | 0 |
  | [`self_damage`](./Arrays.md#array-self_damage) | Object | Recoil or self-inflicted damage/effects applied to the caster. | 0 |
  | `bonus_melee_ability_damage` | Any | Explicit empirical property. | 0 |
  | [`BounceObject`](./Enums.md#enum-bounceobject) | Enum | Spawns a physics object that visually bounces off the target. | 0 |
  | `height` | Number | Examples: `9, 5, 7` | 0 |

</details>

---

### Object: `MotherTumorSpawnInCapture`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Cat`](./Characters_and_Bosses.md#object-cat) | Object | Character Form: Base form for standard cats. | 2 |
| [`NonCat`](./Characters_and_Bosses.md#object-noncat) | Object | Character Form: Behavior and stats for the 'NonCat' state. | 2 |
| [`Nothing`](./Characters_and_Bosses.md#object-nothing) | Object | Character Form: Behavior and stats for the 'Nothing' state. | 1 |

</details>

---

### Object: `MoveCenter`


**Definition:** AI Movement: Moves toward the center of the map.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Object: `MoveForThrow`


**Definition:** AI Movement: Repositions to gain line of sight for throwing.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Object: `NotPriming`


**Definition:** Character Form: Behavior and stats when not charging an ability.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |
  | `passives` | Array | List of {Status and Passive Keys}. | 0 |

</details>

---

### Object: `PassiveWhileNotHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 2 |

</details>

---

### Object: `Priming`


**Definition:** Character Form: Behavior and stats when charging an ability.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `ProtectTargetedAllies`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`target_filter`](./Enums.md#enum-target_filter) | Enum |  | 2 |

</details>

---

### Object: `Rain`

> **Definition:** Character Form: Behavior and stats for the 'Rain' state.


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |

</details>

---

### Object: `RemoveStatusStacks`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusOnEndMove`](./Characters_and_Bosses.md#object-statusonendmove), [`StatusOnTookDamage`](./Characters_and_Bosses.md#object-statusontookdamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 2 |
| `stacks` | Number | The number of stacks to remove. | 2 |

</details>

---

### Object: `SlotMachineRollPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SlotResult_Jackpot_Coins` | Number | Applies or references the 'SlotResult_Jackpot_Coins' effect/state. | 2 |
| `SlotResult_Explode` | Number | Applies or references the 'SlotResult_Explode' effect/state. | 1 |
| `SlotResult_Nothing` | Number | Applies or references the 'SlotResult_Nothing' effect/state. | 1 |
| `SlotResult_RandomPickup` | Number | Applies or references the 'SlotResult_RandomPickup' effect/state. | 1 |

</details>

---

### Object: `Small`


**Definition:** Character Form: Behavior and stats for the \'Small\' state.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Object: `SpearRun`


**Definition:** AI Movement: Specific movement logic for Spear enemies.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Object: `SquirrelForm`


**Definition:** Character Form: Behavior and stats for the 'SquirrelForm' state.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 1 |

</details>

---

### Object: `StatusGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`RandomStatusFromPool`](./Characters_and_Bosses.md#object-randomstatusfrompool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |

</details>

---

### Object: `StatusOnSpawnIn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 0 |
  | `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. | 0 |

</details>

---

### Object: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 30 |

</details>

---

### Object: `TempPassiveUntilSettled`

> **Definition:** Passive: Active only until the physics engine stops moving the character.


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#object-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#object-conditional_isphysicalattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `TinkererBasicAttackSwitching`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`PassiveGroup`](./Characters_and_Bosses.md#object-passivegroup), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum |  | 2 |
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum |  | 2 |

</details>

---

### Object: `TransformOnElementInfluencex`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 2 |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |

</details>

---

### Object: `Turtled`


**Definition:** Character Form: Behavior and stats for the 'Turtled' state.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |

</details>

---

### Object: `active`


**Definition:** Defines actively executed abilities.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
  | `passives` | Array | List of {Status and Passive Keys}. | 0 |

</details>

---

### Object: `alternate_energized_effect`


**Definition:** Overrides default energized visuals.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`Robot`](./Characters_and_Bosses.md#object-robot)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `dispersed_bonusturn_pattern`


**Definition:** AI Logic: Alternative bonus turn ability pattern.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum |  | 3 |

</details>

---

### Object: `passive`


**Definition:** Intrinsic passive modifier.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |

</details>

---

### Object: `statuses_on_enter_form`


**Definition:** Status effects instantly applied upon transitioning into this form.
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`Full`](./Characters_and_Bosses.md#object-full)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
  | [`UseAbility`](./Enums.md#enum-useability) | Enum | Forces the character or target to instantly use a specified ability. | 0 |
  | `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 0 |

</details>

---

### Object: `AddStatusToReceivedDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`Conditional_IsPhysicalAttack`](#conditional_isphysicalattack) | Object | Conditional: Executes logic if the triggering attack is physical. | 0 |
  | [`Else`](#else) | Object | Fallback block that executes if the preceding `Conditional_` block evaluated to false. | 0 |

</details>

---

### Object: `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `Leech` | Number | Applies or references the 'Leech' effect/state. | 0 |
  | `LeechPercent` | Integer | Applies the 'LeechPercent' effect. | 0 |
  | [`Conditional_Enemy`](#conditionalenemy) | Object | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 0 |

</details>

---

### Object: `AddStatusToTrampleDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`PassiveWhenDead`](./Characters_and_Bosses.md#object-passivewhendead)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `Cleave` | Object | Causes the attack to hit adjacent enemies alongside the primary target. | 0 |
  | `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 0 |

</details>

---

### Object: `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `AdventureTokenPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 |

</details>

---

### Object: `AggroTargetIsGovernedByHitEffect`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean |  | 1 |

</details>

---

### Object: `Alert`


**Definition:** AI State: The behavior profile used when the character is alerted to enemies.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |

</details>

---

### Object: `AllStatsAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`aura_requires_tag`](./Enums.md#enum-aura_requires_tag) | Enum |  | 1 |
| [`range`](./Enums.md#enum-range) | Enum | Distance or area of effect in tiles. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Object: `Angry`


**Definition:** Character Form / AI State: Behavior and stats for the \'Angry\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |

</details>

---

### Object: `Attacker`


**Definition:** AI Role: Designates the character as an attacker rather than support.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Object: `BackflipWhenTargeted`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnGainCoins`](./Characters_and_Bosses.md#object-statusongaincoins)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific dodge ability to trigger (e.g., DestroyerDodge). | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Object: `BattlefieldUniqueRandomPassive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Number | Applies or references the 'DemonicGlyph_Bite' effect/state. | 1 |
| `DemonicGlyph_Bounce` | Number | Applies or references the 'DemonicGlyph_Bounce' effect/state. | 1 |
| `DemonicGlyph_Fire` | Number | Applies or references the 'DemonicGlyph_Fire' effect/state. | 1 |
| `DemonicGlyph_Movement` | Number | Applies or references the 'DemonicGlyph_Movement' effect/state. | 1 |
| `DemonicGlyph_Summon` | Number | Applies or references the 'DemonicGlyph_Summon' effect/state. | 1 |

</details>

---

### Object: `BellyFull`


**Definition:** Character Form / AI State: Behavior and stats for the \'BellyFull\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |

</details>

---

### Object: `BigHolding`


**Definition:** Character Form / AI State: Behavior and stats for the \'BigHolding\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `BigHoldingCat`


**Definition:** Character Form / AI State: Behavior and stats for the \'BigHoldingCat\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `Bishop`


**Definition:** Character Form / AI State: Behavior and stats for the \'Bishop\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Object: `BlackHole`


**Definition:** Character Form / AI State: Behavior and stats for the \'BlackHole\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Object: `Bomb`


**Definition:** Character Form / AI State: Behavior and stats for the 'Bomb' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |

</details>

---

### Object: `Bully`


**Definition:** Character Form / AI State: Behavior and stats for the 'Bully' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `BungaCheers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ally_damage`](./Enums.md#enum-ally_damage) | Enum |  | 1 |
| [`ally_dead`](./Enums.md#enum-ally_dead) | Enum |  | 1 |
| [`enemy_damage`](./Enums.md#enum-enemy_damage) | Enum |  | 1 |
| [`enemy_dead`](./Enums.md#enum-enemy_dead) | Enum |  | 1 |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum |  | 1 |

</details>

---

### Object: `CaveBaby`


**Definition:** Character Form: Behavior and stats for the \'CaveBaby\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Object: `CaveWoman`


**Definition:** Character Form: Behavior and stats for the \'CaveWoman\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Object: `CaveWomanHasCat`


**Definition:** Character Form: Behavior and stats for the \'CaveWomanHasCat\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Object: `CerberubsAggroTargetBehavior`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alert_form`](./Enums.md#enum-alert_form) | Enum |  | 1 |
| [`default_form`](./Enums.md#enum-default_form) | Enum |  | 1 |

</details>

---

### Object: `CerberubsJumpBlind`


**Definition:** AI Logic: Blind jump attack pattern for Cerberubs.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |

</details>

---

### Object: `CerberubsJumpNormal`


**Definition:** AI Logic: Normal jump attack pattern for Cerberubs.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |

</details>

---

### Object: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| `chance` | Number | Probability (0.0 to 1.0) of executing this action. | 1 |

</details>

---

### Object: `ChanceToFormChangeOnAbilityDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum |  | 1 |
| `chance` | Number | Probability (0.0 to 1.0) of executing this action. | 1 |

</details>

---

### Object: `ChaosBossFormChangeGuide`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array |  | 1 |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array |  | 1 |
| `passives_health_threshold` | Number |  | 1 |

</details>

---

### Object: `ChaosBossPieces`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array |  | 1 |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array |  | 1 |

</details>

---

### Object: `ChaosHeadDropIn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`new_music`](./Enums.md#enum-new_music) | Enum |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 1 |

</details>

---

### Object: `Charging`


**Definition:** Character Form / AI State: Behavior when charging an attack.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |

</details>

---

### Object: `Close`


**Definition:** AI Movement logic: Maneuvers into close/melee range.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `CloseConvert`


**Definition:** AI State: Logic for converting adjacent units.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusEachTurnEnd`](./Characters_and_Bosses.md#object-statuseachturnend)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 1 |

</details>

---

### Object: `Conditional_HasKnockback`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Else`](./Characters_and_Bosses.md#object-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`KnockUpAndAway`](./Characters_and_Bosses.md#object-knockupandaway) | Object | Logic: Applies vertical and horizontal displacement. | 0 |
| `RemoveKnockback` | `Number` | Applies or references the 'RemoveKnockback' effect/state. | 0 |
| [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#object-temppassiveuntilsettled) | Object | Passive: Active only until the physics engine stops moving the character. | 0 |

</details>

---

### Object: `Conditional_IsPhysicalAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#object-addstatustoreceiveddamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`KnockUpAndAway`](./Characters_and_Bosses.md#object-knockupandaway) | Object | Logic: Applies vertical and horizontal displacement. | 0 |
| `RemoveKnockback` | `Number` | Applies or references the 'RemoveKnockback' effect/state. | 0 |
| [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#object-temppassiveuntilsettled) | Object | Passive: Active only until the physics engine stops moving the character. | 0 |

</details>

---

### Object: `CounterAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| `without_orienting` | Boolean |  | 1 |

</details>

---

### Object: `CreateGlobalModifiers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 |
| `BloodRain` | `Number` | Applies or references the 'BloodRain' effect/state. | 0 |
| [`LowerAmbientLight`](./Characters_and_Bosses.md#object-lowerambientlight) | Object | Visual: Dims the map lighting. | 0 |

</details>

---

### Object: `Cultist`


**Definition:** Character Form: Behavior and stats for the \'Cultist\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Object: `Damaged`


**Definition:** Character Form / AI State: Behavior when health is critically low.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Object: `Default_Ceiling`


**Definition:** Character Form: The baseline behavior state while attached to the ceiling.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |
  | `passives` | Array | List of {Status and Passive Keys}. | 0 |

</details>

---

### Object: `Default_Ground`


**Definition:** Character Form: The baseline behavior state while on the ground.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |
  | `passives` | Array | List of {Status and Passive Keys}. | 0 |

</details>

---

### Object: `DelayedAutoRevive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 1 |
| `rounds` | Number |  | 1 |

</details>

---

### Object: `DesireMech`


**Definition:** Character Form: Behavior and stats for the 'DesireMech' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Object: `DiceBehavior`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dice_size` | Number |  | 1 |
| `knockback_damage` | Number |  | 1 |

</details>

---

### Object: `Die`

> **Definition:** Character Form / Logic: Forces the character to die.


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear. | 1 |
  | `passives` | Array | List of {Status and Passive Keys}. | 0 |

</details>

---

### Object: `DiesToPiercingAndSpikes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `deferred` | Boolean |  | 1 |

</details>

---

### Object: `DodgeWhenTargeted`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |

</details>

---

### Object: `Drunker`


**Definition:** Character Form: Behavior and stats for the 'Drunker' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |

</details>

---

### Object: `DualSword`


**Definition:** Character Form: Behavior and stats for the \'DualSword\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| `move_speed_multiplier` | Number |  | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `DualSword_Primed`


**Definition:** Character Form: Behavior and stats for the \'DualSword_Primed\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| `move_speed_multiplier` | Number |  | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `Dumb`


**Definition:** AI Profile: A simplified, less optimal decision-making profile.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `DybbukPossessionFallback`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum |  | 1 |
| [`form`](./Enums.md#enum-form) | Enum |  | 1 |

</details>

---

### Object: `Else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#object-addstatustoreceiveddamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 71 |
| [`Conditional_HasKnockback`](./Characters_and_Bosses.md#object-conditional-hasknockback) | Object | Conditional: Executes logic if the triggering attack deals knockback. | 0 |
| [`KnockUpAndAway`](./Characters_and_Bosses.md#object-knockupandaway) | Object | Logic: Applies vertical and horizontal displacement. | 0 |
| `RemoveKnockback` | Number | Applies or references the 'RemoveKnockback' effect/state. | 0 |
| [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#object-temppassiveuntilsettled) | Object | Passive: Active only until the physics engine stops moving the character. | 0 |

</details>

---

### Object: `Explody`


**Definition:** Character Form: Behavior and stats for the 'Explody' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |

</details>

---

### Object: `FaceAwayLastDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean |  | 1 |
| `override_hit_animation` | Boolean |  | 1 |
| `use_turn_animations` | Boolean |  | 1 |

</details>

---

### Object: `FightPhase`


**Definition:** Boss Logic: Main combat phase.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |

</details>

---

### Object: `FinalBossBeamQueue`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`queue`](./Enums.md#enum-queue) | Enum |  | 1 |
| [`release`](./Enums.md#enum-release) | Enum |  | 1 |
| [`transform`](./Enums.md#enum-transform) | Enum |  | 1 |

</details>

---

### Object: `FinalBossBecomeTheChild`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| [`GlobalSpawnCharacter`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'GlobalSpawnCharacter' effect/state. | 0 |
| `PlayBackground` | `Number` | Applies or references the 'PlayBackground' effect/state. | 0 |
| [`SwitchMusic`](./Characters_and_Bosses.md#object-switchmusic) | Object | Event Trigger: Changes background music track. | 0 |

</details>

---

### Object: `FinalBossHitCountdownBoris`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `icon_ready` | Number |  | 1 |
| `icon` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Object: `FinalBossHitCountdownExplosive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `icon_ready` | Number |  | 1 |
| `icon` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Object: `FinalBossHitCountdownHoly`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `icon_ready` | Number |  | 1 |
| `icon` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Object: `FinalBossPupils`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`look_at_offset`](./Arrays.md#array-look_at_offset) | Array |  | 1 |
| [`reset_center_because_no_target_halflife`](./Enums.md#enum-reset_center_because_no_target_halflife) | Enum |  | 1 |
| [`reset_center_because_of_animation_halflife`](./Enums.md#enum-reset_center_because_of_animation_halflife) | Enum |  | 1 |
| [`teleport_tracking_halflife`](./Enums.md#enum-teleport_tracking_halflife) | Enum |  | 1 |
| [`tracking_acquisition_halflife`](./Enums.md#enum-tracking_acquisition_halflife) | Enum |  | 1 |
| [`virtual_head_position`](./Arrays.md#array-virtual_head_position) | Array |  | 1 |
| `radius` | Number | Distance or area of effect in tiles. | 1 |

</details>

---

### Object: `FinalBossShieldHealth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`break_ability`](./Enums.md#enum-break_ability) | Enum |  | 1 |
| [`state_health`](./Arrays.md#array-state_health) | Array |  | 1 |

</details>

---

### Object: `FinalBossSyncAnimations`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`other_character`](./Enums.md#enum-other_character) | Enum |  | 1 |
| [`other_form_change_abilities`](./Characters_and_Bosses.md#object-other_form_change_abilities) | Object | Lists secondary abilities used to change forms. | 1 |

</details>

---

### Object: `Fire`


**Definition:** Character Form: Behavior and stats for the 'Fire' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `FireFull`


**Definition:** Character Form: Behavior and stats for the 'FireFull' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Object: `Flop`


**Definition:** Character Form: Behavior and stats for the \'Flop\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Object: `Flop2`


**Definition:** Character Form: Behavior and stats for the \'Flop2\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Object: `Flush`


**Definition:** Character Form: Behavior and stats for the 'Flush' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Object: `FlushBubs`


**Definition:** Character Form: Behavior and stats for the 'FlushBubs' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `FlushHost`


**Definition:** Character Form: Behavior and stats for the 'FlushHost' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `FlushNettle`


**Definition:** Character Form: Behavior and stats for the 'FlushNettle' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `FoodMove`


**Definition:** AI Movement: Logic for seeking out food items.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `ForceTrample`


**Definition:** Logic: Forces movement to act as a trample attack.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |

</details>

---

### Object: `GainDisorderFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](./Characters_and_Bosses.md#object-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0) of executing this action. | 1 |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 1 |

</details>

---

### Object: `Grappling`


**Definition:** Character Form / AI State: Behavior while grappling an opponent.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit_animations`](./Characters_and_Bosses.md#object-exit_animations) | Object | Animations played when leaving a form/state. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |

</details>

---

### Object: `Grown`


**Definition:** Character Form: Behavior and stats for the \'Grown\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| `uifloaters_offset` | Number |  | 1 |
| `weak_threshold` | Number |  | 1 |

</details>

---

### Object: `GuaranteedJackpot`


**Definition:** Loot Logic: Guarantees a high-tier drop.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
  | `passives` | Array | List of {Status and Passive Keys}. | 0 |

</details>

---

### Object: `Guarding`


**Definition:** Character Form / AI State: Defensive behavior state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |

</details>

---

### Object: `HPAltStates`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`clipname`](./Enums.md#enum-clipname) | Enum |  | 1 |
| [`thresholds`](./Arrays.md#array-thresholds) | Array |  | 1 |

</details>

---

### Object: `HalfDead`


**Definition:** Character Form: Behavior and stats for the \'HalfDead\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Object: `HasDeadCat`


**Definition:** Character Form: Behavior and stats for the \'HasDeadCat\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Object: `HasRock`


**Definition:** Character Form: Behavior and stats for the \'HasRock\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Object: `Headless`


**Definition:** Character Form: Behavior and stats for the \'Headless\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Object: `HealNeighborsEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Object: `Hint_CrackedVisuals`


**Definition:** Visual: Overlay effects for cracked/damaged terrain or objects.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Object: `Hint_CrackedVisuals2`


**Definition:** Visual: Secondary cracked visual overlay.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Object: `Hint_CrackedVisuals3`


**Definition:** Visual: Tertiary cracked visual overlay.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Object: `HitlerExecute`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `HumanDead`


**Definition:** Character Form: Behavior and stats for the \'HumanDead\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Object: `InfiniteRebirth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 1 |
| `immediate` | Boolean |  | 1 |
| `playercat_health` | Number |  | 1 |

</details>

---

### Object: `InitialPhase`


**Definition:** Boss Logic: The starting phase of an encounter.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |

</details>

---

### Object: `Insane_Ceiling`


**Definition:** Character Form: Insane behavior state while attached to the ceiling.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `Insane_Ground`


**Definition:** Character Form: Insane behavior state while on the ground.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |

</details>

---

### Object: `Johnny`


**Definition:** Character Form: Behavior and stats for the 'Johnny' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Object: `JohnnyBubs`


**Definition:** Character Form: Behavior and stats for the 'JohnnyBubs' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `JohnnyHost`


**Definition:** Character Form: Behavior and stats for the 'JohnnyHost' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `JohnnyNeedsWashing`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_unwashed`](./Enums.md#enum-form_unwashed) | Enum |  | 1 |
| [`form_washed`](./Enums.md#enum-form_washed) | Enum |  | 1 |

</details>

---

### Object: `JohnnyNettle`


**Definition:** Character Form: Behavior and stats for the 'JohnnyNettle' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `Joystick`


**Definition:** Character Form: Behavior and stats for the \'Joystick\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `LastHit`


**Definition:** Logic: Executes logic on the final hit of a multi-hit attack.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |

</details>

---

### Object: `LeapClose`


**Definition:** AI Movement: Executes a jumping maneuver to close distance.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `Lifted`


**Definition:** Character Form: Behavior and stats for the \'Lifted\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |

</details>

---

### Object: `Lit`


**Definition:** Character Form: Behavior and stats for the 'Lit' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `LowerAmbientLight`

> **Definition:** Visual: Dims the map lighting.


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`CreateGlobalModifiers`](./Characters_and_Bosses.md#object-createglobalmodifiers)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`amount`](./Arrays.md#array-amount) | Array | The target opacity/dimness level. | 1 |
| `speed` | Number | The transition speed. | 1 |

</details>

---

### Object: `MegaDinoDropController`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`head_drop`](./Enums.md#enum-head_drop) | Enum |  | 1 |
| [`leg_leave`](./Enums.md#enum-leg_leave) | Enum |  | 1 |
| [`leg_return`](./Enums.md#enum-leg_return) | Enum |  | 1 |
| `stable_legs` | Number |  | 1 |

</details>

---

### Object: `ModularPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`sound_event`](./Enums.md#enum-sound_event) | Enum |  | 1 |
  | `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 0 |

</details>

---

### Object: `MonkCatReactionAbilities`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`spell`](./Enums.md#enum-spell) | Enum |  | 1 |
| [`trinket`](./Enums.md#enum-trinket) | Enum |  | 1 |
| [`weapon`](./Enums.md#enum-weapon) | Enum | Weapon item constraint. | 1 |

</details>

---

### Object: `MotherGrowController`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eat_damage`](./Characters_and_Bosses.md#object-eat_damage) | Object | Damage dealt when this entity consumes another. | 1 |
| [`tumor_object`](./Enums.md#enum-tumor_object) | Enum |  | 1 |

</details>

---

### Object: `MotherTumorPassive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Cat`](./Characters_and_Bosses.md#object-cat) | Object | Character Form: Base form for standard cats. | 1 |
| [`NonCat`](./Characters_and_Bosses.md#object-noncat) | Object | Character Form: Behavior and stats for the 'NonCat' state. | 1 |
| [`considered_forms`](./Arrays.md#array-considered_forms) | Array |  | 1 |
| [`grow_ability`](./Enums.md#enum-grow_ability) | Enum |  | 1 |
| [`pass_ani`](./Enums.md#enum-pass_ani) | Enum |  | 1 |
| [`receive_ani`](./Enums.md#enum-receive_ani) | Enum |  | 1 |

</details>

---

### Object: `Mount`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eject_ability`](./Enums.md#enum-eject_ability) | Enum |  | 1 |
| [`enter_ability`](./Enums.md#enum-enter_ability) | Enum |  | 1 |

</details>

---

### Object: `Mounted`


**Definition:** Character Form: Behavior and stats for the \'Mounted\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Object: `MouthFull`


**Definition:** Character Form: Behavior and stats for the \'MouthFull\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `MoveAfterAnyAttemptedAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 1 |

</details>

---

### Object: `MoveAwayFromDamageSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 1 |

</details>

---

### Object: `MoveAwayWhenEnemyAdjacent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 1 |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 1 |
| `once_per_turn` | Boolean |  | 1 |

</details>

---

### Object: `MoveForBarrage`


**Definition:** AI Movement: Repositions to optimize a barrage attack.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `MoveForDash`


**Definition:** AI Movement: Repositions to set up a dash attack line.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `MoveForGrass`


**Definition:** AI Movement: Moves toward grass tiles.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `MoveForPounce`


**Definition:** AI Movement: Repositions to optimize a pounce trajectory.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `MoveForSpin`


**Definition:** AI Movement: Repositions into a cluster of enemies for a spin attack.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `MoveOneForPuke`


**Definition:** AI Movement: Specific positioning logic for puke attacks.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `MoveSpaced`


**Definition:** AI Movement: Moves to maintain a specific distance from targets.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `MoveToHead`


**Definition:** AI Movement: Navigates toward the 'head' or primary target.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `MoveTowards`


**Definition:** AI Movement: Moves toward the nearest target.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `MultiSpawnOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array | The numerical quantity. | 1 |
| [`obj`](./Enums.md#enum-obj) | Enum |  | 1 |

</details>

---

### Object: `Mutant`


**Definition:** Character Form: Behavior and stats for the \'Mutant\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move_speed_multiplier`](./Enums.md#enum-move_speed_multiplier) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |

</details>

---

### Object: `NCGravecrawlFAR`


**Definition:** AI Movement: Specific grapple/crawl logic.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `NeutronStar`


**Definition:** Character Form: Behavior and stats for the 'NeutronStar' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Object: `NoEyes`


**Definition:** Character Form: Behavior and stats for the \'NoEyes\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Object: `NoStick`


**Definition:** Character Form: Behavior and stats for the 'NoStick' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Object: `NormalFull`


**Definition:** Character Form: Behavior and stats for the 'NormalFull' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Object: `Nothing`


**Definition:** Character Form: Behavior and stats for the 'Nothing' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#object-mothertumorspawnincapture)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |

</details>

---

### Object: `Nuke`


**Definition:** Character Form: Behavior and stats for the 'Nuke' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |

</details>

---

### Object: `Obey`


**Definition:** AI State: Enforced compliance logic (e.g., when Charmed).
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `Off`


**Definition:** Character Form: Behavior and stats for the 'Off' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |

</details>

---

### Object: `OffScreen`


**Definition:** Character Form: Behavior and stats for the 'OffScreen' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |
  | `passives` | Array | List of {Status and Passive Keys}. | 0 |

</details>

---

### Object: `OneEye`


**Definition:** Character Form: Behavior and stats for the \'OneEye\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `Open`


**Definition:** Character Form: Behavior and stats for the 'Open' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Object: `OpenCat`


**Definition:** Character Form: Behavior and stats for the 'OpenCat' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `Out`


**Definition:** Character Form: Behavior and stats for the 'Out' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 30 |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 1 |

</details>

---

### Object: `PassiveWhenDead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`StatusEachRoundEnd`](#statuseachroundend) | Object | Applies or references the 'StatusEachRoundEnd' effect/state. | 0 |
  | [`StatusEachTurnBegin`](#statuseachturnbegin) | Object | Event Trigger: Applies nested statuses to each turn begin. | 0 |
  | [`AddStatusToTrampleDamage`](#addstatustotrampledamage) | Object | Applies the 'AddStatusToTrampleDamage' effect. | 0 |
  | [`AutocastEachRound`](#autocasteachround) | Object | Forces the character to automatically cast a specific ability at the start of each combat round. | 0 |

</details>

---

### Object: `Possessing`


**Definition:** Character Form: Behavior and stats for the \'Possessing\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |

</details>

---

### Object: `Primed`


**Definition:** Character Form: Behavior and stats for the 'Primed' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |

</details>

---

### Object: `Pulp2`


**Definition:** Character Form: Behavior and stats for the 'Pulp2' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Object: `Pulp3`


**Definition:** Character Form: Behavior and stats for the 'Pulp3' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Object: `Pulp4`


**Definition:** Character Form: Behavior and stats for the 'Pulp4' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Object: `Pulp5`


**Definition:** Character Form: Behavior and stats for the 'Pulp5' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Object: `Pulp6`


**Definition:** Character Form: Behavior and stats for the 'Pulp6' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Object: `Pulp7`


**Definition:** Character Form: Behavior and stats for the 'Pulp7' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Object: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ally_rewards`](./Characters_and_Bosses.md#object-ally_rewards)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 31 |

</details>

---

### Object: `ReturnA`


**Definition:** Boss Logic: Specific phase return trigger.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 1 |
| `damage` | Number | The base damage properties of an attack. | 1 |
| `knockback` | Number |  | 1 |

</details>

---

### Object: `RunFar`


**Definition:** AI Movement: Maximize distance from targets.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `RunWhenLastPlayerCatIsCharmed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`legacy_savekey`](./Enums.md#enum-legacy_savekey) | Enum |  | 1 |
| `allow_decision_mid_turn` | Boolean |  | 1 |

</details>

---

### Object: `ScalingAttackAnimation`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`default`](./Enums.md#enum-default) | Enum | Baseline configuration. | 1 |
| [`thresholds`](./Arrays.md#array-thresholds) | Array |  | 1 |

</details>

---

### Object: `SharePickups`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `include_coins` | Boolean |  | 1 |

</details>

---

### Object: `Sitting`


**Definition:** Character Form: Behavior and stats for the 'Sitting' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |

</details>

---

### Object: `SkipFirstRounds`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `pop_chance` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Object: `SmallHolding`


**Definition:** Character Form: Behavior and stats for the \'SmallHolding\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `SmallHoldingCat`


**Definition:** Character Form: Behavior and stats for the \'SmallHoldingCat\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `SpawningPhase`


**Definition:** Boss Logic: Phase focused on summoning minions.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `SpewerAltGraphics`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FireFull` | Number | Character Form: Behavior and stats for the 'FireFull' state. | 1 |
| `Fire` | Number | Character Form: Behavior and stats for the 'Fire' state. | 1 |
| `NormalFull` | Number | Character Form: Behavior and stats for the 'NormalFull' state. | 1 |
| `Normal` | Number | Character Form: Behavior and stats for the 'Normal' state. | 1 |
| `TarFull` | Number | Character Form: Behavior and stats for the 'TarFull' state. | 1 |
| `Tar` | Number | Character Form: Behavior and stats for the 'Tar' state. | 1 |

</details>

---

### Object: `StacyMutant_Brace`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StacyMutant_Counter`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StacyMutant_Damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StacyMutant_DoubleHead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StacyMutant_Fire`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StacyMutant_Health`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StacyMutant_Holy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StacyMutant_Ice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StacyMutant_Lightning`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StacyMutant_Mirror`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

### Object: `StacyMutant_Speed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StacyMutant_Thorns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `Standing`


**Definition:** Character Form: Behavior and stats for the 'Standing' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |

</details>

---

### Object: `Standing2`


**Definition:** Character Form: Behavior and stats for the 'Standing2' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 1 |

</details>

---

### Object: `Start_Ceiling`


**Definition:** Character Form: Behavior and stats for the 'Start_Ceiling' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusAfterXTurns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Object: `StatusEachTurnBeginIfHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| `consume` | Boolean |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StacyMutant_Mirror`](./Characters_and_Bosses.md#object-stacymutant_mirror)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `StatusEachTurnEndIfEnabledAtStartOfTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | `RemoveStatusStacks` | Object | Removes a specific number of stacks of a status effect. | 0 |
  | [`Conditional_FirstApplicationThisTurn`](#conditionalfirstapplicationthisturn) | Object | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 0 |
  | [`DivineShield`](./Arrays.md#array-divineshield) | Number | Applies or references the 'DivineShield' effect/state. | 0 |
  | [`Conditional_GoodRoll`](#conditional_goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 0 |
  | [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | Applies or references the 'ImmediateUseAbility' effect/state. | 0 |
  | `Charge` | Number | Applies or references the 'Charge' effect/state. | 0 |
  | `SpeedUp_WithoutInitiative` | Integer | Applies or references the 'SpeedUp_WithoutInitiative' effect/state. | 0 |
  | `ForceAttack` | Object | Forces the character to execute an immediate attack. | 0 |
  | `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 0 |

</details>

---

### Object: `StatusOnEnemyConfused`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
  | [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | Applies or references the 'ImmediateUseAbility' effect/state. | 0 |

</details>

---

### Object: `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

---

### Object: `StatusOverlappingCharactersAndDie`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `StatusWhenStatusCompletelyRemoved`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |
  | [`UseAbility`](./Enums.md#enum-useability) | Enum | Forces the character or target to instantly use a specified ability. | 0 |

</details>

---

### Object: `Stop`


**Definition:** AI Movement: Forces the character to cease movement.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `SuckMF`


**Definition:** Character Form: Behavior and stats for the 'SuckMF' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `SupportDieInsteadOfRun`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alt_dead_ani`](./Enums.md#enum-alt_dead_ani) | Enum |  | 1 |
| [`alt_dying_ani`](./Enums.md#enum-alt_dying_ani) | Enum |  | 1 |

</details>

---

### Object: `SwimmingFormChange`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_in`](./Enums.md#enum-form_in) | Enum |  | 1 |
| [`form_out`](./Enums.md#enum-form_out) | Enum |  | 1 |

</details>

---

### Object: `SwitchMusic`

> **Definition:** Event Trigger: Changes background music track.


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FinalBossBecomeTheChild`](./Characters_and_Bosses.md#object-finalbossbecomethechild)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | The specific audio layer to transition to (e.g., map, battle). | 1 |
| [`new_song`](./Enums.md#enum-new_song) | Enum | The ID of the new music track. | 1 |

</details>

---

### Object: `SwordAndShield`


**Definition:** Character Form: Behavior and stats for the 'SwordAndShield' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `SwordAndShield_Primed`


**Definition:** Character Form: Behavior and stats for the \'SwordAndShield_Primed\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Object: `SyncFormsWithBuddy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`no_buddy`](./Enums.md#enum-no_buddy) | Enum |  | 1 |

</details>

---

### Object: `T3HitlerSpawningPhase`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`spell_use_groups`](./Arrays.md#array-spell_use_groups) | Array |  | 1 |

</details>

---

### Object: `TF_TargetAllies`


**Definition:** AI Targeting: Prioritizes allies.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |

</details>

---

### Object: `TF_TargetEnemies`


**Definition:** AI Targeting: Prioritizes enemies.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |

</details>

---

### Object: `TVBotScreen`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `Dumb` | Number | AI Profile: A simplified, less optimal decision-making profile. | 1 |
| `Fuck` | Number | Applies or references the 'Fuck' effect/state. | 1 |
| `Obey` | Number | AI State: Enforced compliance logic (e.g., when Charmed). | 1 |
| `Shit` | Number | Applies or references the 'Shit' effect/state. | 1 |
| `Stop` | Number | AI Movement: Forces the character to cease movement. | 1 |
| `Die` | `Number` | Character Form / Logic: Forces the character to die. | 0 |

</details>

---

### Object: `Tar`


**Definition:** Character Form: Behavior and stats for the 'Tar' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `TarFull`


**Definition:** Character Form: Behavior and stats for the 'TarFull' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Object: `Terminator2Run`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `TerminatorChase`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |

</details>

---

### Object: `TerminatorSkin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`groups`](./Arrays.md#array-groups) | Array |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |

</details>

---

### Object: `Throb`


**Definition:** Character Form: Behavior and stats for the 'Throb' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Object: `ThrobBubs`


**Definition:** Character Form: Behavior and stats for the 'ThrobBubs' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `ThrobHost`


**Definition:** Character Form: Behavior and stats for the 'ThrobHost' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `ThrobNettle`


**Definition:** Character Form: Behavior and stats for the 'ThrobNettle' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `TransformOnStatusThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `Transformed`


**Definition:** Character Form: Behavior and stats for the 'Transformed' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Object: `TwisterFling`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| `max_dist` | Number |  | 1 |
| `min_dist` | Number |  | 1 |

</details>

---

### Object: `TwoEyes`


**Definition:** Character Form: Behavior and stats for the 'TwoEyes' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
  | `passives` | Array | List of {Status and Passive Keys}. | 0 |

</details>

---

### Object: `Unflip`


**Definition:** Logic: Reverses a flipped state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Object: `UnlimitedDeathRattleRevive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| `even_if_stunned` | Boolean |  | 1 |

</details>

---

### Object: `Unlit`


**Definition:** Character Form: Behavior and stats for the 'Unlit' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |

</details>

---

### Object: `Unwashed`


**Definition:** Character Form: Behavior and stats for the 'Unwashed' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |

</details>

---

### Object: `UseAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusWhenStatusCompletelyRemoved`](./Characters_and_Bosses.md#object-statuswhenstatuscompletelyremoved)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger. | 1 |
| `respect_prime` | Boolean | If true, respects the ability's prime/cooldown state. | 1 |

</details>

---

### Object: `UseAbilityWhenOutOfStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |

</details>

---

### Object: `Washed`


**Definition:** Character Form: Behavior and stats for the 'Washed' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `Washer`


**Definition:** Character Form: Behavior and stats for the \'Washer\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Object: `Water`


**Definition:** Character Form: Behavior and stats for the \'Water\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |

</details>

---

### Object: `WereMan`


**Definition:** Character Form: Behavior and stats for the \'WereMan\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Object: `Zealot`


**Definition:** Character Form: Behavior and stats for the \'Zealot\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Object: `ZealotBomb`


**Definition:** Character Form: Behavior and stats for the \'ZealotBomb\' state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Object: `additional_statuses`


**Definition:** Generic statuses added to the character.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`SpawnOnDeath`](./Characters_and_Bosses.md#object-spawnondeath)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

---

### Object: `ai_if_spawned_as_enemy`


**Definition:** AI logic override used only if the character is spawned as an enemy.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |
| [`pattern`](./Characters_and_Bosses.md#object-pattern) | Object | AI sequence logic. | 1 |

</details>

---

### Object: `damage_instance`

**Definition:** Defines damage logic on contact.
**Total Count:** 1



<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1731 |
| [`effects`](./Characters_and_Bosses.md#object-effects) | Object | Non-damaging impact triggers. | 0 |

</details>

---

### Object: `eat_damage`

**Definition:** Damage dealt when this entity consumes another.
**Total Count:** 1



<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`MotherGrowController`](./Characters_and_Bosses.md#object-mothergrowcontroller)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 1 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
| `damage` | Number | The base damage properties of an attack. | 1 |
| `cant_miss` | `Boolean` |  | 0 |
| [`effects`](./Characters_and_Bosses.md#object-effects) | Object | Non-damaging impact triggers. | 0 |
| `makes_contact` | `Boolean` |  | 0 |
| `piercing` | `Boolean` |  | 0 |

</details>

---

### Object: `exit_animations`


**Definition:** Animations played when leaving a form/state.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`Grappling`](./Characters_and_Bosses.md#object-grappling)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Default`](./Enums.md#enum-default) | Enum | Character Form: The baseline default behavior state. | 1 |

</details>

---

### Object: `other_form_change_abilities`


**Definition:** Lists secondary abilities used to change forms.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`FinalBossSyncAnimations`](./Characters_and_Bosses.md#object-finalbosssyncanimations)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Boris`](./Enums.md#enum-boris) | Enum | Character Form / AI State: Behavior and stats for the 'Boris' state. | 1 |
| [`Explosive`](./Enums.md#enum-explosive) | Enum | Character Form: Behavior and stats for the 'Explosive' state. | 1 |
| [`Holy`](./Enums.md#enum-holy) | Enum | Character Form: Behavior and stats for the 'Holy' state. | 1 |

</details>

---

### Object: `round_start_bonusturn_pattern`


**Definition:** AI Logic: Ability usage pattern during round-start bonus turns.
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>


> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 1 |

</details>

---

