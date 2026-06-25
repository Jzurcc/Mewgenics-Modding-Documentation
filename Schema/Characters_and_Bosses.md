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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`properties`](./Characters_and_Bosses.md#object-properties) | Object | General engine properties. | 1200 |
| [`graphics`](./Characters_and_Bosses.md#object-graphics) | Object | Visual parameters and animation bindings. | 5218 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 928 |
| [`abilities`](./Characters_and_Bosses.md#object-abilities) | Object | Lists the ability IDs the character possesses. | 918 |
| [`stats`](./Characters_and_Bosses.md#object-stats) | Object | Core character metrics (Health, Strength, etc.). | 982 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum |  | 2364 |
| [`sound`](./Characters_and_Bosses.md#object-sound) | Object | Audio bindings. | 124 |
| [`equipment`](./Characters_and_Bosses.md#object-equipment) | Object | List of item IDs the character spawns equipped with. | 88 |
| [`alt_spawn_pool`](./Characters_and_Bosses.md#object-alt_spawn_pool) | Object | Alternative pools to draw minions from. | 36 |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 10 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 10 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 10 |
| `animation_suffix` | Number | Examples: `3, 4, 2` | 6 |
| `initial_form` | Number | Examples: `1, 5, 0` | 6 |
| `partial_animation_suffix` | Number | Examples: `3, 2, 1` | 6 |
| [`pattern`](./Characters_and_Bosses.md#object-pattern) | Object | AI sequence logic. | 6 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 26 |
| `end_turn_on_formswitch` | Boolean |  | 4 |
| [`ai_if_spawned_as_enemy`](./Characters_and_Bosses.md#object-ai_if_spawned_as_enemy) | Object | AI logic override used only if the character is spawned as an enemy. | 2 |
| `consider_spells` | Boolean |  | 2 |
| [`damage_instance`](./Characters_and_Bosses.md#object-damage_instance) | Object | Defines damage logic on contact. | 4688 |
| [`scale`](./Enums.md#enum-scale) | Enum |  | 6 |
| `uifloaters_offset` | Number |  | 2 |

</details>

---

### Object: `passives`



**Definition:** Object listing intrinsic passive modifiers.  
**Total Count:** 733


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Alert`](./Characters_and_Bosses.md#object-alert), [`AllAlive`](./Characters_and_Bosses.md#object-allalive), [`BellyFull`](./Characters_and_Bosses.md#object-bellyfull), [`Big`](./Characters_and_Bosses.md#object-big), [`BigHolding`](./Characters_and_Bosses.md#object-bigholding), [`BigHoldingCat`](./Characters_and_Bosses.md#object-bigholdingcat), [`Bishop`](./Characters_and_Bosses.md#object-bishop), [`BlackHole`](./Characters_and_Bosses.md#object-blackhole), [`Bomb`](./Characters_and_Bosses.md#object-bomb), [`Boris`](./Characters_and_Bosses.md#object-boris), [`Bully`](./Characters_and_Bosses.md#object-bully), [`CaveBaby`](./Characters_and_Bosses.md#object-cavebaby), [`CaveMan`](./Characters_and_Bosses.md#object-caveman), [`CaveManSpear`](./Characters_and_Bosses.md#object-cavemanspear), [`CaveWoman`](./Characters_and_Bosses.md#object-cavewoman), [`CaveWomanHasCat`](./Characters_and_Bosses.md#object-cavewomanhascat), [`Charging`](./Characters_and_Bosses.md#object-charging), [`Close`](./Characters_and_Bosses.md#object-close), [`Cultist`](./Characters_and_Bosses.md#object-cultist), [`Default`](./Characters_and_Bosses.md#object-default), and 97 more...

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ArmorPickup`](./Characters_and_Bosses.md#object-armorpickup) | Object | Pickup Logic: Defines what happens when an armor item is collected. | 6 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Examples: `{ ... }` | 4 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 16 |
| `partial_animation_suffix` | Number | Examples: `4, 2` | 4 |
| `animation_suffix` | Number | Examples: `1` | 2 |
| `uifloaters_offset` | Number | Examples: `2.2` | 2 |

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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 1010 |
| `health` | Number |  | 854 |
| [`tag`](./Arrays.md#array-tag) | Array | Specific entity tag required. | 508 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 560 |
| `movement` | Number |  | 556 |
| [`corpse_health`](./Enums.md#enum-corpse_health) | Mixed |  | 390 |
| `inherit_faction` | Boolean |  | 230 |
| `dispersed_bonus_turns` | Number |  | 208 |
| `base_mana_regen` | Number |  | 180 |
| [`size`](./Enums.md#enum-size) | Enum |  | 160 |
| `shield` | Number |  | 148 |
| [`move_block`](./Enums.md#enum-move_block) | Enum |  | 146 |
| `kill_required` | Boolean |  | 138 |
| `can_be_backstabbed` | Boolean |  | 136 |
| `initiative` | Number |  | 122 |
| `takes_turns` | Boolean |  | 122 |
| `mana_regen` | Number |  | 102 |
| `mana` | Number | Base maximum mana pool. | 100 |
| `flying` | Boolean |  | 94 |
| [`banned_elite_buffs`](./Arrays.md#array-banned_elite_buffs) | Array |  | 45 |
| [`hidden_tag`](./Arrays.md#array-hidden_tag) | Array |  | 62 |
| `weak_threshold` | Number |  | 64 |
| `knockback_immune` | Boolean |  | 50 |
| `can_be_champion` | Boolean |  | 40 |
| [`lock_orientation`](./Arrays.md#array-lock_orientation) | Array |  | 19 |
| [`ai_scale`](./Enums.md#enum-ai_scale) | Enum |  | 36 |
| [`auto_run_priority`](./Enums.md#enum-auto_run_priority) | Enum |  | 32 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 16 |
| `inanimate` | Boolean |  | 32 |
| `disperse_main_turns` | Boolean |  | 30 |
| [`hidden_tags`](./Arrays.md#array-hidden_tags) | Array |  | 26 |
| [`tags`](./Arrays.md#array-tags) | Array |  | 14 |
| `evenly_dispersed_bonus_turns` | Number |  | 26 |
| `exclude_from_hallucinate` | Boolean |  | 26 |
| `round_end_bonus_turns` | Number |  | 26 |
| `can_be_overkilled` | Boolean |  | 24 |
| `can_collect_coins` | Boolean |  | 20 |
| `deathpoof_size` | Number |  | 20 |
| `dispersed_bonus_turns_consider_initiative` | Boolean |  | 20 |
| [`held_coins`](./Arrays.md#array-held_coins) | Array |  | 6 |
| `initial_health` | Number |  | 20 |
| `can_eat_food` | Boolean |  | 18 |
| `can_grant_extra_turns` | Boolean |  | 16 |
| `tall` | Boolean |  | 16 |
| `dispersed_bonus_turns_before_cats` | Boolean |  | 14 |
| `divine_shield` | Number |  | 14 |
| `is_player_cat` | Boolean |  | 14 |
| `boss_minions_runaway` | Boolean |  | 12 |
| `mana_matters` | Boolean |  | 12 |
| `access_to_player_inventory` | Boolean |  | 10 |
| `act_points` | Number |  | 10 |
| `takes_main_turn` | Boolean |  | 10 |
| `visually_spiky` | Boolean |  | 10 |
| `allow_passive_spelltransforming` | Boolean |  | 8 |
| `base_crit_chance` | Number |  | 8 |
| `last_turn_is_main_turn` | Boolean |  | 8 |
| `round_start_bonus_turns` | Number |  | 8 |
| `view_bleeding_characters_as_enemies` | Boolean |  | 8 |
| [`aoe_pierce_mode`](./Enums.md#enum-aoe_pierce_mode) | Enum |  | 6 |
| `base_initiative` | Number |  | 6 |
| `base_movement` | Number |  | 6 |
| `catdata_ignore_skills` | Boolean |  | 6 |
| [`disallow_items`](./Enums.md#enum-disallow_items) | Enum |  | 6 |
| `always_triggers_traps` | Boolean |  | 4 |
| `base_health` | Number |  | 4 |
| `base_health_regen` | Number |  | 4 |
| `base_initial_mana` | Number |  | 4 |
| `base_mana` | Number |  | 4 |
| `blocking` | Boolean |  | 4 |
| `can_be_elite` | Boolean |  | 4 |
| `can_run` | Boolean |  | 4 |
| `champion` | Boolean |  | 4 |
| `force_not_familiar` | Boolean |  | 4 |
| `hint_no_corpse` | Boolean |  | 4 |
| `must_start_facing_camera` | Boolean |  | 4 |
| `tile_desire_cost` | Number |  | 4 |
| `uncapturable` | Boolean |  | 4 |
| `aggro_target_is_enemy` | Boolean |  | 2 |
| `allow_flying_effect` | Boolean |  | 2 |
| `allow_offmap_corpse` | Boolean |  | 2 |
| `allow_replacebrain` | Boolean |  | 2 |
| `always_face_forward` | Boolean |  | 2 |
| `capture_as_cat` | Boolean |  | 2 |
| `elite` | Boolean |  | 2 |
| `first_turn_is_main_turn` | Boolean |  | 2 |
| `ignore_mouseover` | Boolean |  | 2 |
| `ignore_tiles` | Boolean |  | 2 |
| [`inanimate_can_receive_specific_statuses`](./Arrays.md#array-inanimate_can_receive_specific_statuses) | Array |  | 1 |
| `mouseover_priority` | Number |  | 2 |
| `move_points` | Number |  | 2 |
| `pickup_type` | Number |  | 2 |
| `scale` | Number |  | 2 |
| `speculative_inanimate` | Boolean |  | 2 |
| `static` | Boolean |  | 2 |
| `two_fronts` | Boolean |  | 2 |
| `two_fronts_switch` | Boolean |  | 2 |
| `view_bugs_as_enemies` | Boolean |  | 2 |
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | `Enum/String` |  | 34 |

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
| [`brain`](./Enums.md#enum-brain) | Enum |  | 1146 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 986 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 980 |
| [`pattern`](./Characters_and_Bosses.md#object-pattern) | Object | AI sequence logic. | 578 |
| [`mainturn_pattern`](./Characters_and_Bosses.md#object-mainturn_pattern) | Object | AI Logic: Determines standard ability usage during the main turn. | 88 |
| `end_turn_on_formswitch` | Boolean |  | 78 |
| [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities) | Object | Abilities that are evaluated but not directly castable by the player. | 70 |
| `auto_orient` | Boolean |  | 62 |
| `reset_pattern_on_formswitch` | Boolean |  | 62 |
| `stun_advances_pattern` | Boolean |  | 60 |
| `fallback_advances_pattern` | Boolean |  | 56 |
| [`bonusturn_pattern`](./Characters_and_Bosses.md#object-bonusturn_pattern) | Object | AI Logic: Determines ability usage during bonus turns. | 54 |
| [`fallback`](./Characters_and_Bosses.md#object-fallback) | Object | Logic executed if primary options fail. | 46 |
| [`round_end_bonusturn_pattern`](./Characters_and_Bosses.md#object-round_end_bonusturn_pattern) | Object | AI Logic: Ability usage pattern during round-end bonus turns. | 24 |
| `consider_spells` | Boolean |  | 22 |
| `animate_choice` | Boolean |  | 16 |
| `clamp_pattern` | Boolean |  | 10 |
| `randomize_pattern_start` | Boolean |  | 6 |
| [`dispersed_bonusturn_pattern`](./Characters_and_Bosses.md#object-dispersed_bonusturn_pattern) | Object | AI Logic: Alternative bonus turn ability pattern. | 4 |
| `random_orient` | Boolean |  | 4 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`dice_abilities`](./Arrays.md#array-dice_abilities) | Array |  | 1 |
| [`post_absorb_move_weights`](./Enums.md#enum-post_absorb_move_weights) | Enum |  | 2 |
| [`roll_ability`](./Enums.md#enum-roll_ability) | Enum |  | 2 |
| [`round_start_bonusturn_pattern`](./Characters_and_Bosses.md#object-round_start_bonusturn_pattern) | Object | AI Logic: Ability usage pattern during round-start bonus turns. | 2 |
| `never_hit_ally_corpses` | Boolean |  | 2 |
| `reset_pattern_on_round_begin` | Boolean |  | 2 |

</details>

---

### Object: `graphics`




**Definition:** Object defining visual animations and sequence timings.  
**Total Count:** 2609


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1034 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  | 920 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 818 |
| `shadow_size` | Number |  | 302 |
| [`scale`](./Enums.md#enum-scale) | Enum |  | 298 |
| `uifloaters_offset` | Number |  | 298 |
| [`custom_cat_data`](./Enums.md#enum-custom_cat_data) | Enum |  | 254 |
| [`water_mask`](./Enums.md#enum-water_mask) | Enum |  | 166 |
| [`spawnin_animation`](./Strings.md#string-spawnin_animation) | String |  | 74 |
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array |  | 33 |
| `piece_alt_frame` | Number |  | 54 |
| [`shadow`](./Enums.md#enum-shadow) | Enum |  | 46 |
| `move_speed_sync_frames` | Number |  | 40 |
| `no_splatter` | Boolean |  | 34 |
| [`projectile_spawn_offset`](./Arrays.md#array-projectile_spawn_offset) | Array |  | 17 |
| [`tint`](./Arrays.md#array-tint) | Array |  | 6 |
| [`move_speed_multiplier`](./Enums.md#enum-move_speed_multiplier) | Enum |  | 32 |
| `dont_sink` | Boolean |  | 28 |
| `art_flip` | Number |  | 14 |
| [`depth_offset`](./Enums.md#enum-depth_offset) | Enum |  | 12 |
| [`walk`](./Enums.md#enum-walk) | Enum |  | 2 |
| [`dead`](./Enums.md#enum-dead) | Enum |  | 4 |
| [`dying`](./Enums.md#enum-dying) | Enum |  | 16 |
| `four_way_animations` | Boolean |  | 8 |
| [`hit`](./Enums.md#enum-hit) | Enum |  | 4 |
| [`stunned`](./Enums.md#enum-stunned) | Enum |  | 4 |
| [`weak`](./Enums.md#enum-weak) | Enum |  | 4 |
| [`deadhit`](./Enums.md#enum-deadhit) | Enum |  | 3 |
| `show_infinity_damage_warning` | Boolean |  | 6 |
| `always_huge_mask` | Boolean |  | 4 |
| [`default_attack_animation`](./Enums.md#enum-default_attack_animation) | Enum |  | 4 |
| [`desc`](./Strings.md#string-desc) | String | Localization key for the character's desc. | 4 |
| `shade_occluded_objects` | Boolean |  | 4 |
| [`dodge`](./Enums.md#enum-dodge) | Enum |  | 2 |
| `no_horizontal_flip` | Boolean |  | 2 |
| [`non_blocking_animations`](./Arrays.md#array-non_blocking_animations) | Array |  | 1 |
| [`override_portrait`](./Enums.md#enum-override_portrait) | Enum |  | 2 |
| `randomize_starting_frame` | Boolean |  | 2 |
| `status_display_count_max` | Number |  | 2 |

</details>

---

### Object: `abilities`




**Definition:** Lists the ability IDs the character possesses.  
**Total Count:** 460


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 874 |
| [`move`](./Enums.md#enum-move) | Enum |  | 866 |
| [`spells`](./Arrays.md#array-spells) | Array |  | 381 |
| `can_get_bonus` | Boolean |  | 60 |
| `BoneWormShotSmall` | Flag |  | 2 |

</details>

---

### Object: `stats`




**Definition:** Core character metrics (Health, Strength, etc.).  
**Total Count:** 497


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `strength` | Number |  | 772 |
| `constitution` | Number |  | 760 |
| `dexterity` | Number |  | 760 |
| `charisma` | Number |  | 758 |
| `intelligence` | Number |  | 758 |
| `speed` | Number | Base speed/initiative stat. | 758 |
| `luck` | Number |  | 320 |

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
| [`do`](./Enums.md#enum-do) | Enum |  | 256 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 106 |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 101 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum |  | 22 |
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



**Definition:** AI Role: Designates the character as one that frequently shifts forms.  
**Total Count:** 106


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`initial_form`](./Enums.md#enum-initial_form) | Enum |  | 112 |
| [`Default`](./Characters_and_Bosses.md#object-default) | Object | Character Form: The baseline default behavior state. | 82 |
| [`Normal`](./Characters_and_Bosses.md#object-normal) | Object | Character Form: Behavior and stats for the \'Normal\' state. | 22 |
| [`Rage`](./Characters_and_Bosses.md#object-rage) | Object | Character Form: Behavior and stats for the \'Rage\' state. | 20 |
| [`HasCat`](./Characters_and_Bosses.md#object-hascat) | Object | Character Form: Behavior and stats for the \'HasCat\' state. | 10 |
| [`default`](./Characters_and_Bosses.md#object-default) | Object | Baseline configuration. | 82 |
| [`hot`](./Characters_and_Bosses.md#object-hot) | Object | Visual effect indicator. | 8 |
| [`OffMap`](./Characters_and_Bosses.md#object-offmap) | Object | Character Form: Behavior and stats for the 'OffMap' state. | 8 |
| [`AllAlive`](./Characters_and_Bosses.md#object-allalive) | Object | Encounter State: Logic executed when all specific entities are currently alive. | 6 |
| [`Down`](./Characters_and_Bosses.md#object-down) | Object | Character Form: Behavior and stats for the \'Down\' state. | 6 |
| [`Full`](./Characters_and_Bosses.md#object-full) | Object | Character Form: Behavior and stats for the \'Full\' state. | 6 |
| [`OneAlive`](./Characters_and_Bosses.md#object-onealive) | Object | Encounter State: Logic executed when exactly one target is alive. | 6 |
| [`TwoAlive`](./Characters_and_Bosses.md#object-twoalive) | Object | Encounter State: Logic executed when exactly two targets are alive. | 6 |
| [`Up`](./Characters_and_Bosses.md#object-up) | Object | Character Form: Behavior and stats for the \'Up\' state. | 6 |
| [`active`](./Characters_and_Bosses.md#object-active) | Object | Defines actively executed abilities. | 4 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 4 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 4 |
| [`Big`](./Characters_and_Bosses.md#object-big) | Object | Character Form / AI State: Behavior and stats for the \'Big\' state. | 4 |
| [`Boris`](./Characters_and_Bosses.md#object-boris) | Object | Character Form / AI State: Behavior and stats for the \'Boris\' state. | 4 |
| [`CaveMan`](./Characters_and_Bosses.md#object-caveman) | Object | Character Form: Behavior and stats for the \'CaveMan\' state. | 4 |
| [`CaveManSpear`](./Characters_and_Bosses.md#object-cavemanspear) | Object | Character Form: Behavior and stats for the \'CaveManSpear\' state. | 4 |
| [`Empty`](./Characters_and_Bosses.md#object-empty) | Object | Character Form: Behavior and stats for the \'Empty\' state. | 4 |
| [`Explosive`](./Characters_and_Bosses.md#object-explosive) | Object | Character Form: Behavior and stats for the \'Explosive\' state. | 4 |
| [`Holding`](./Characters_and_Bosses.md#object-holding) | Object | Character Form: Behavior and stats for the \'Holding\' state. | 4 |
| [`Holy`](./Characters_and_Bosses.md#object-holy) | Object | Character Form: Behavior and stats for the \'Holy\' state. | 4 |
| [`NotPriming`](./Characters_and_Bosses.md#object-notpriming) | Object | Character Form: Behavior and stats when not charging an ability. | 4 |
| `partial_animation_suffix` | Number |  | 4 |
| [`passive`](./Characters_and_Bosses.md#object-passive) | Object | Intrinsic passive modifier. | 4 |
| [`Priming`](./Characters_and_Bosses.md#object-priming) | Object | Character Form: Behavior and stats when charging an ability. | 4 |
| [`Small`](./Characters_and_Bosses.md#object-small) | Object | Character Form: Behavior and stats for the \'Small\' state. | 4 |
| [`SquirrelForm`](./Characters_and_Bosses.md#object-squirrelform) | Object | Character Form: Behavior and stats for the 'SquirrelForm' state. | 4 |
| [`Turtled`](./Characters_and_Bosses.md#object-turtled) | Object | Character Form: Behavior and stats for the 'Turtled' state. | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`Alert`](./Characters_and_Bosses.md#object-alert) | Object | AI State: The behavior profile used when the character is alerted to enemies. | 2 |
| [`Angry`](./Characters_and_Bosses.md#object-angry) | Object | Character Form / AI State: Behavior and stats for the \'Angry\' state. | 2 |
| [`Attacker`](./Characters_and_Bosses.md#object-attacker) | Object | AI Role: Designates the character as an attacker rather than support. | 2 |
| [`BellyFull`](./Characters_and_Bosses.md#object-bellyfull) | Object | Character Form / AI State: Behavior and stats for the \'BellyFull\' state. | 2 |
| [`BigHolding`](./Characters_and_Bosses.md#object-bigholding) | Object | Character Form / AI State: Behavior and stats for the \'BigHolding\' state. | 2 |
| [`BigHoldingCat`](./Characters_and_Bosses.md#object-bigholdingcat) | Object | Character Form / AI State: Behavior and stats for the \'BigHoldingCat\' state. | 2 |
| [`Bishop`](./Characters_and_Bosses.md#object-bishop) | Object | Character Form / AI State: Behavior and stats for the \'Bishop\' state. | 2 |
| [`BlackHole`](./Characters_and_Bosses.md#object-blackhole) | Object | Character Form / AI State: Behavior and stats for the \'BlackHole\' state. | 2 |
| [`Bomb`](./Characters_and_Bosses.md#object-bomb) | Object | Character Form / AI State: Behavior and stats for the 'Bomb' state. | 2 |
| [`Bully`](./Characters_and_Bosses.md#object-bully) | Object | Character Form / AI State: Behavior and stats for the 'Bully' state. | 2 |
| [`Butcher`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Applies or references the 'Butcher' effect/state. | 2 |
| [`CaveBaby`](./Characters_and_Bosses.md#object-cavebaby) | Object | Character Form: Behavior and stats for the \'CaveBaby\' state. | 2 |
| [`CaveWoman`](./Characters_and_Bosses.md#object-cavewoman) | Object | Character Form: Behavior and stats for the \'CaveWoman\' state. | 2 |
| [`CaveWomanHasCat`](./Characters_and_Bosses.md#object-cavewomanhascat) | Object | Character Form: Behavior and stats for the \'CaveWomanHasCat\' state. | 2 |
| [`Charging`](./Characters_and_Bosses.md#object-charging) | Object | Character Form / AI State: Behavior when charging an attack. | 2 |
| [`Close`](./Characters_and_Bosses.md#object-close) | Object | AI Movement logic: Maneuvers into close/melee range. | 2 |
| [`Colorless`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | Applies or references the 'Colorless' effect/state. | 2 |
| [`Cultist`](./Characters_and_Bosses.md#object-cultist) | Object | Character Form: Behavior and stats for the \'Cultist\' state. | 2 |
| [`Damaged`](./Characters_and_Bosses.md#object-damaged) | Object | Character Form / AI State: Behavior when health is critically low. | 2 |
| [`Default_Ceiling`](./Characters_and_Bosses.md#object-default_ceiling) | Object | Character Form: The baseline behavior state while attached to the ceiling. | 2 |
| [`Default_Ground`](./Characters_and_Bosses.md#object-default_ground) | Object | Character Form: The baseline behavior state while on the ground. | 2 |
| [`DesireMech`](./Characters_and_Bosses.md#object-desiremech) | Object | Character Form: Behavior and stats for the 'DesireMech' state. | 2 |
| [`Druid`](./Engine_LogicKeys.md#valid-property-keys) | Object | Applies or references the 'Druid' effect/state. | 2 |
| [`Drunker`](./Characters_and_Bosses.md#object-drunker) | Object | Character Form: Behavior and stats for the 'Drunker' state. | 2 |
| [`DualSword`](./Characters_and_Bosses.md#object-dualsword) | Object | Character Form: Behavior and stats for the \'DualSword\' state. | 2 |
| [`DualSword_Primed`](./Characters_and_Bosses.md#object-dualsword_primed) | Object | Character Form: Behavior and stats for the \'DualSword_Primed\' state. | 2 |
| [`Dumb`](./Characters_and_Bosses.md#object-dumb) | Object | AI Profile: A simplified, less optimal decision-making profile. | 2 |
| [`Explody`](./Characters_and_Bosses.md#object-explody) | Object | Character Form: Behavior and stats for the 'Explody' state. | 2 |
| [`Fighter`](./Engine_LogicKeys.md#valid-property-keys) | Object | Applies or references the 'Fighter' effect/state. | 2 |
| [`FightPhase`](./Characters_and_Bosses.md#object-fightphase) | Object | Boss Logic: Main combat phase. | 2 |
| [`Fire`](./Characters_and_Bosses.md#object-fire) | Object | Character Form: Behavior and stats for the 'Fire' state. | 2 |
| [`FireFull`](./Characters_and_Bosses.md#object-firefull) | Object | Character Form: Behavior and stats for the 'FireFull' state. | 2 |
| [`Flop`](./Characters_and_Bosses.md#object-flop) | Object | Character Form: Behavior and stats for the \'Flop\' state. | 2 |
| [`Flop2`](./Characters_and_Bosses.md#object-flop2) | Object | Character Form: Behavior and stats for the \'Flop2\' state. | 2 |
| [`Flush`](./Characters_and_Bosses.md#object-flush) | Object | Character Form: Behavior and stats for the 'Flush' state. | 2 |
| [`FlushBubs`](./Characters_and_Bosses.md#object-flushbubs) | Object | Character Form: Behavior and stats for the 'FlushBubs' state. | 2 |
| [`FlushHost`](./Characters_and_Bosses.md#object-flushhost) | Object | Character Form: Behavior and stats for the 'FlushHost' state. | 2 |
| [`FlushNettle`](./Characters_and_Bosses.md#object-flushnettle) | Object | Character Form: Behavior and stats for the 'FlushNettle' state. | 2 |
| [`Grappling`](./Characters_and_Bosses.md#object-grappling) | Object | Character Form / AI State: Behavior while grappling an opponent. | 2 |
| [`Grown`](./Characters_and_Bosses.md#object-grown) | Object | Character Form: Behavior and stats for the \'Grown\' state. | 2 |
| [`GuaranteedJackpot`](./Characters_and_Bosses.md#object-guaranteedjackpot) | Object | Loot Logic: Guarantees a high-tier drop. | 2 |
| [`Guarding`](./Characters_and_Bosses.md#object-guarding) | Object | Character Form / AI State: Defensive behavior state. | 2 |
| [`HalfDead`](./Characters_and_Bosses.md#object-halfdead) | Object | Character Form: Behavior and stats for the \'HalfDead\' state. | 2 |
| [`HasDeadCat`](./Characters_and_Bosses.md#object-hasdeadcat) | Object | Character Form: Behavior and stats for the \'HasDeadCat\' state. | 2 |
| [`HasRock`](./Characters_and_Bosses.md#object-hasrock) | Object | Character Form: Behavior and stats for the \'HasRock\' state. | 2 |
| [`Headless`](./Characters_and_Bosses.md#object-headless) | Object | Character Form: Behavior and stats for the \'Headless\' state. | 2 |
| [`Hint_CrackedVisuals`](./Characters_and_Bosses.md#object-hint_crackedvisuals) | Object | Visual: Overlay effects for cracked/damaged terrain or objects. | 2 |
| [`Hint_CrackedVisuals2`](./Characters_and_Bosses.md#object-hint_crackedvisuals2) | Object | Visual: Secondary cracked visual overlay. | 2 |
| [`Hint_CrackedVisuals3`](./Characters_and_Bosses.md#object-hint_crackedvisuals3) | Object | Visual: Tertiary cracked visual overlay. | 2 |
| [`HumanDead`](./Characters_and_Bosses.md#object-humandead) | Object | Character Form: Behavior and stats for the \'HumanDead\' state. | 2 |
| [`Hunter`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | Applies or references the 'Hunter' effect/state. | 2 |
| [`InitialPhase`](./Characters_and_Bosses.md#object-initialphase) | Object | Boss Logic: The starting phase of an encounter. | 2 |
| [`Insane_Ceiling`](./Characters_and_Bosses.md#object-insane_ceiling) | Object | Character Form: Insane behavior state while attached to the ceiling. | 2 |
| [`Insane_Ground`](./Characters_and_Bosses.md#object-insane_ground) | Object | Character Form: Insane behavior state while on the ground. | 2 |
| [`Johnny`](./Characters_and_Bosses.md#object-johnny) | Object | Character Form: Behavior and stats for the 'Johnny' state. | 2 |
| [`JohnnyBubs`](./Characters_and_Bosses.md#object-johnnybubs) | Object | Character Form: Behavior and stats for the 'JohnnyBubs' state. | 2 |
| [`JohnnyHost`](./Characters_and_Bosses.md#object-johnnyhost) | Object | Character Form: Behavior and stats for the 'JohnnyHost' state. | 2 |
| [`JohnnyNettle`](./Characters_and_Bosses.md#object-johnnynettle) | Object | Character Form: Behavior and stats for the 'JohnnyNettle' state. | 2 |
| [`Joystick`](./Characters_and_Bosses.md#object-joystick) | Object | Character Form: Behavior and stats for the \'Joystick\' state. | 2 |
| [`LastHit`](./Characters_and_Bosses.md#object-lasthit) | Object | Logic: Executes logic on the final hit of a multi-hit attack. | 2 |
| [`Lifted`](./Characters_and_Bosses.md#object-lifted) | Object | Character Form: Behavior and stats for the \'Lifted\' state. | 2 |
| [`Lit`](./Characters_and_Bosses.md#object-lit) | Object | Character Form: Behavior and stats for the 'Lit' state. | 2 |
| [`Mage`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Applies or references the 'Mage' effect/state. | 2 |
| [`Medic`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | Applies or references the 'Medic' effect/state. | 2 |
| [`Monk`](./Engine_LogicKeys.md#valid-property-keys) | Object | Applies or references the 'Monk' effect/state. | 2 |
| [`Mounted`](./Characters_and_Bosses.md#object-mounted) | Object | Character Form: Behavior and stats for the \'Mounted\' state. | 2 |
| [`MouthFull`](./Characters_and_Bosses.md#object-mouthfull) | Object | Character Form: Behavior and stats for the \'MouthFull\' state. | 2 |
| [`Mutant`](./Characters_and_Bosses.md#object-mutant) | Object | Character Form: Behavior and stats for the \'Mutant\' state. | 2 |
| [`Necromancer`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Applies or references the 'Necromancer' effect/state. | 2 |
| [`NeutronStar`](./Characters_and_Bosses.md#object-neutronstar) | Object | Character Form: Behavior and stats for the 'NeutronStar' state. | 2 |
| [`NoDeathRattle`](./Engine_LogicKeys.md#valid-property-keys) | Object | Applies or references the 'NoDeathRattle' effect/state. | 2 |
| [`NoEyes`](./Characters_and_Bosses.md#object-noeyes) | Object | Character Form: Behavior and stats for the \'NoEyes\' state. | 2 |
| [`NormalFull`](./Characters_and_Bosses.md#object-normalfull) | Object | Character Form: Behavior and stats for the 'NormalFull' state. | 2 |
| [`NoStick`](./Characters_and_Bosses.md#object-nostick) | Object | Character Form: Behavior and stats for the 'NoStick' state. | 2 |
| [`Nuke`](./Characters_and_Bosses.md#object-nuke) | Object | Character Form: Behavior and stats for the 'Nuke' state. | 2 |
| [`Obey`](./Characters_and_Bosses.md#object-obey) | Object | AI State: Enforced compliance logic (e.g., when Charmed). | 2 |
| [`Off`](./Characters_and_Bosses.md#object-off) | Object | Character Form: Behavior and stats for the 'Off' state. | 2 |
| [`OffScreen`](./Characters_and_Bosses.md#object-offscreen) | Object | Character Form: Behavior and stats for the 'OffScreen' state. | 2 |
| [`OneEye`](./Characters_and_Bosses.md#object-oneeye) | Object | Character Form: Behavior and stats for the \'OneEye\' state. | 2 |
| [`Open`](./Characters_and_Bosses.md#object-open) | Object | Character Form: Behavior and stats for the 'Open' state. | 2 |
| [`OpenCat`](./Characters_and_Bosses.md#object-opencat) | Object | Character Form: Behavior and stats for the 'OpenCat' state. | 2 |
| [`Out`](./Characters_and_Bosses.md#object-out) | Object | Character Form: Behavior and stats for the 'Out' state. | 2 |
| [`Possessing`](./Characters_and_Bosses.md#object-possessing) | Object | Character Form: Behavior and stats for the \'Possessing\' state. | 2 |
| [`Primed`](./Characters_and_Bosses.md#object-primed) | Object | Character Form: Behavior and stats for the 'Primed' state. | 2 |
| [`Psychic`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Applies or references the 'Psychic' effect/state. | 2 |
| [`Pulp2`](./Characters_and_Bosses.md#object-pulp2) | Object | Character Form: Behavior and stats for the 'Pulp2' state. | 2 |
| [`Pulp3`](./Characters_and_Bosses.md#object-pulp3) | Object | Character Form: Behavior and stats for the 'Pulp3' state. | 2 |
| [`Pulp4`](./Characters_and_Bosses.md#object-pulp4) | Object | Character Form: Behavior and stats for the 'Pulp4' state. | 2 |
| [`Pulp5`](./Characters_and_Bosses.md#object-pulp5) | Object | Character Form: Behavior and stats for the 'Pulp5' state. | 2 |
| [`Pulp6`](./Characters_and_Bosses.md#object-pulp6) | Object | Character Form: Behavior and stats for the 'Pulp6' state. | 2 |
| [`Pulp7`](./Characters_and_Bosses.md#object-pulp7) | Object | Character Form: Behavior and stats for the 'Pulp7' state. | 2 |
| [`Sitting`](./Characters_and_Bosses.md#object-sitting) | Object | Character Form: Behavior and stats for the 'Sitting' state. | 2 |
| [`SmallHolding`](./Characters_and_Bosses.md#object-smallholding) | Object | Character Form: Behavior and stats for the \'SmallHolding\' state. | 2 |
| [`SmallHoldingCat`](./Characters_and_Bosses.md#object-smallholdingcat) | Object | Character Form: Behavior and stats for the \'SmallHoldingCat\' state. | 2 |
| [`SpawningPhase`](./Characters_and_Bosses.md#object-spawningphase) | Object | Boss Logic: Phase focused on summoning minions. | 2 |
| [`Standing`](./Characters_and_Bosses.md#object-standing) | Object | Character Form: Behavior and stats for the 'Standing' state. | 2 |
| [`Standing2`](./Characters_and_Bosses.md#object-standing2) | Object | Character Form: Behavior and stats for the 'Standing2' state. | 2 |
| [`Start_Ceiling`](./Characters_and_Bosses.md#object-start_ceiling) | Object | Character Form: Behavior and stats for the 'Start_Ceiling' state. | 2 |
| [`Stop`](./Characters_and_Bosses.md#object-stop) | Object | AI Movement: Forces the character to cease movement. | 2 |
| [`SwordAndShield`](./Characters_and_Bosses.md#object-swordandshield) | Object | Character Form: Behavior and stats for the 'SwordAndShield' state. | 2 |
| [`SwordAndShield_Primed`](./Characters_and_Bosses.md#object-swordandshield_primed) | Object | Character Form: Behavior and stats for the \'SwordAndShield_Primed\' state. | 2 |
| `sync_brain_patterns` | Boolean |  | 2 |
| [`Tank`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Applies or references the 'Tank' effect/state. | 2 |
| [`Tar`](./Characters_and_Bosses.md#object-tar) | Object | Character Form: Behavior and stats for the 'Tar' state. | 2 |
| [`TarFull`](./Characters_and_Bosses.md#object-tarfull) | Object | Character Form: Behavior and stats for the 'TarFull' state. | 2 |
| [`Thief`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Applies or references the 'Thief' effect/state. | 2 |
| [`Throb`](./Characters_and_Bosses.md#object-throb) | Object | Character Form: Behavior and stats for the 'Throb' state. | 2 |
| [`ThrobBubs`](./Characters_and_Bosses.md#object-throbbubs) | Object | Character Form: Behavior and stats for the 'ThrobBubs' state. | 2 |
| [`ThrobHost`](./Characters_and_Bosses.md#object-throbhost) | Object | Character Form: Behavior and stats for the 'ThrobHost' state. | 2 |
| [`ThrobNettle`](./Characters_and_Bosses.md#object-throbnettle) | Object | Character Form: Behavior and stats for the 'ThrobNettle' state. | 2 |
| [`Tinkerer`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | Applies or references the 'Tinkerer' effect/state. | 2 |
| [`Transformed`](./Characters_and_Bosses.md#object-transformed) | Object | Character Form: Behavior and stats for the 'Transformed' state. | 2 |
| [`TwoEyes`](./Characters_and_Bosses.md#object-twoeyes) | Object | Character Form: Behavior and stats for the 'TwoEyes' state. | 2 |
| `uifloaters_offset` | Number |  | 2 |
| [`Unlit`](./Characters_and_Bosses.md#object-unlit) | Object | Character Form: Behavior and stats for the 'Unlit' state. | 2 |
| [`Unmounted`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Applies or references the 'Unmounted' effect/state. | 2 |
| [`Unwashed`](./Characters_and_Bosses.md#object-unwashed) | Object | Character Form: Behavior and stats for the 'Unwashed' state. | 2 |
| [`Washed`](./Characters_and_Bosses.md#object-washed) | Object | Character Form: Behavior and stats for the 'Washed' state. | 2 |
| [`Washer`](./Characters_and_Bosses.md#object-washer) | Object | Character Form: Behavior and stats for the \'Washer\' state. | 2 |
| [`Water`](./Characters_and_Bosses.md#object-water) | Object | Character Form: Behavior and stats for the \'Water\' state. | 2 |
| [`WereMan`](./Characters_and_Bosses.md#object-wereman) | Object | Character Form: Behavior and stats for the \'WereMan\' state. | 2 |
| [`Zealot`](./Characters_and_Bosses.md#object-zealot) | Object | Character Form: Behavior and stats for the \'Zealot\' state. | 2 |
| [`ZealotBomb`](./Characters_and_Bosses.md#object-zealotbomb) | Object | Character Form: Behavior and stats for the \'ZealotBomb\' state. | 2 |
| [`Die`](./Characters_and_Bosses.md#object-die) | Object | Character Form / Logic: Forces the character to die. | 2 |
| [`Rain`](./Characters_and_Bosses.md#object-rain) | Object | Character Form: Behavior and stats for the 'Rain' state. | 4 |

</details>

---

### Object: `SpawnOnDeath`



**Definition:** No definition provided.  
**Total Count:** 79


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 8 |
| [`obj`](./Arrays.md#array-obj) | Array |  | 4 |
| [`additional_statuses`](./Characters_and_Bosses.md#object-additional_statuses) | Object | Generic statuses added to the character. | 2 |

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
| [`animation_prefix`](./Enums.md#enum-animation_prefix) | Enum |  | 2 |

</details>

---

### Object: `Robot`



**Definition:** No definition provided.  
**Total Count:** 46


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alternate_energized_effect`](./Characters_and_Bosses.md#object-alternate_energized_effect) | Object | Overrides default energized visuals. | 4 |

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
| `takes_turns` | Boolean |  | 46 |
| `dispersed_bonus_turns` | Number |  | 36 |
| `takes_main_turn` | Boolean |  | 20 |
| `evenly_dispersed_bonus_turns` | Number |  | 14 |
| `round_end_bonus_turns` | Number |  | 10 |
| `wait_till_next_round_to_update_turns` | Boolean |  | 8 |
| `round_start_bonus_turns` | Number |  | 2 |

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
| [`face`](./Enums.md#enum-face) | Enum |  | 32 |
| [`head`](./Enums.md#enum-head) | Enum |  | 28 |
| [`neck`](./Enums.md#enum-neck) | Enum |  | 20 |
| [`weapon`](./Enums.md#enum-weapon) | Enum | Weapon item constraint. | 14 |

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
| [`do`](./Enums.md#enum-do) | Enum |  | 46 |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 9 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 8 |
| [`do_strict`](./Arrays.md#array-do_strict) | Array |  | 2 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum |  | 4 |

</details>

---

### Object: `Default`




**Definition:** Character Form: The baseline default behavior state.  
**Total Count:** 38


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 20 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 4 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 2 |

</details>

---

### Object: `FormChangeWhileHasStatus`



**Definition:** Logic: Changes form automatically while possessing a specific status.  
**Total Count:** 35


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 70 |
| [`form_hasnot`](./Enums.md#enum-form_hasnot) | Enum |  | 60 |
| [`form_has`](./Enums.md#enum-form_has) | Enum |  | 50 |

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
| [`MoveAway`](./Characters_and_Bosses.md#object-moveaway) | Object | AI Movement: Moves away from the target. | 8 |
| [`MoveClose`](./Characters_and_Bosses.md#object-moveclose) | Object | AI Movement: Moves into melee range. | 8 |
| [`DashRandomly`](./Characters_and_Bosses.md#object-dashrandomly) | Object | AI Movement: Dashes to a random valid tile. | 4 |
| [`Escape`](./Characters_and_Bosses.md#object-escape) | Object | AI Movement: Logic for fleeing or escaping the map. | 4 |
| [`MoveCenter`](./Characters_and_Bosses.md#object-movecenter) | Object | AI Movement: Moves toward the center of the map. | 4 |
| [`MoveForThrow`](./Characters_and_Bosses.md#object-moveforthrow) | Object | AI Movement: Repositions to gain line of sight for throwing. | 4 |
| [`SpearRun`](./Characters_and_Bosses.md#object-spearrun) | Object | AI Movement: Specific movement logic for Spear enemies. | 4 |
| [`CerberubsJumpBlind`](./Characters_and_Bosses.md#object-cerberubsjumpblind) | Object | AI Logic: Blind jump attack pattern for Cerberubs. | 2 |
| [`CerberubsJumpNormal`](./Characters_and_Bosses.md#object-cerberubsjumpnormal) | Object | AI Logic: Normal jump attack pattern for Cerberubs. | 2 |
| [`CloseConvert`](./Characters_and_Bosses.md#object-closeconvert) | Object | AI State: Logic for converting adjacent units. | 2 |
| [`FoodMove`](./Characters_and_Bosses.md#object-foodmove) | Object | AI Movement: Logic for seeking out food items. | 2 |
| [`ForceTrample`](./Characters_and_Bosses.md#object-forcetrample) | Object | Logic: Forces movement to act as a trample attack. | 2 |
| [`LeapClose`](./Characters_and_Bosses.md#object-leapclose) | Object | AI Movement: Executes a jumping maneuver to close distance. | 2 |
| [`MoveForBarrage`](./Characters_and_Bosses.md#object-moveforbarrage) | Object | AI Movement: Repositions to optimize a barrage attack. | 2 |
| [`MoveForDash`](./Characters_and_Bosses.md#object-movefordash) | Object | AI Movement: Repositions to set up a dash attack line. | 2 |
| [`MoveForGrass`](./Characters_and_Bosses.md#object-moveforgrass) | Object | AI Movement: Moves toward grass tiles. | 2 |
| [`MoveForPounce`](./Characters_and_Bosses.md#object-moveforpounce) | Object | AI Movement: Repositions to optimize a pounce trajectory. | 2 |
| [`MoveForSpin`](./Characters_and_Bosses.md#object-moveforspin) | Object | AI Movement: Repositions into a cluster of enemies for a spin attack. | 2 |
| [`MoveOneForPuke`](./Characters_and_Bosses.md#object-moveoneforpuke) | Object | AI Movement: Specific positioning logic for puke attacks. | 2 |
| [`MoveSpaced`](./Characters_and_Bosses.md#object-movespaced) | Object | AI Movement: Moves to maintain a specific distance from targets. | 2 |
| [`MoveToHead`](./Characters_and_Bosses.md#object-movetohead) | Object | AI Movement: Navigates toward the 'head' or primary target. | 2 |
| [`MoveTowards`](./Characters_and_Bosses.md#object-movetowards) | Object | AI Movement: Moves toward the nearest target. | 2 |
| [`NCGravecrawlFAR`](./Characters_and_Bosses.md#object-ncgravecrawlfar) | Object | AI Movement: Specific grapple/crawl logic. | 2 |
| [`ReturnA`](./Characters_and_Bosses.md#object-returna) | Object | Boss Logic: Specific phase return trigger. | 2 |
| [`RunFar`](./Characters_and_Bosses.md#object-runfar) | Object | AI Movement: Maximize distance from targets. | 2 |
| [`SuckMF`](./Characters_and_Bosses.md#object-suckmf) | Object | Character Form: Behavior and stats for the 'SuckMF' state. | 2 |
| [`TF_TargetAllies`](./Characters_and_Bosses.md#object-tf_targetallies) | Object | AI Targeting: Prioritizes allies. | 2 |
| [`TF_TargetEnemies`](./Characters_and_Bosses.md#object-tf_targetenemies) | Object | AI Targeting: Prioritizes enemies. | 2 |
| [`Unflip`](./Characters_and_Bosses.md#object-unflip) | Object | Logic: Reverses a flipped state. | 2 |

</details>

---

### Object: `AddStatusToBasicAttack`



**Definition:** Injects a status effect payload that applies whenever the character performs a basic attack.  
**Total Count:** 32


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#object-randompassivepool), [`StacyMutant_Counter`](./Characters_and_Bosses.md#object-stacymutant_counter), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `DeathRattle`



**Definition:** No definition provided.  
**Total Count:** 29


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 26 |
| `is_dying_animation` | Boolean |  | 14 |
| `pop_corpse` | Boolean |  | 22 |
| `cancel_knockback` | Boolean |  | 2 |
| `immediate` | Boolean |  | 2 |
| `must_target_killer` | Boolean |  | 2 |
| `target_killer` | Boolean |  | 2 |

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
| [`do`](./Enums.md#enum-do) | Enum |  | 38 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 11 |
| [`do_strict`](./Arrays.md#array-do_strict) | Array |  | 5 |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 4 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum |  | 2 |

</details>

---

### Object: `CatPartsTransform`



**Definition:** Transforms specific body parts into different visual variants.  
**Total Count:** 25


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveGroup`](./Characters_and_Bosses.md#object-passivegroup), [`StacyMutant_Brace`](./Characters_and_Bosses.md#object-stacymutant_brace), [`StacyMutant_Counter`](./Characters_and_Bosses.md#object-stacymutant_counter), [`StacyMutant_Damage`](./Characters_and_Bosses.md#object-stacymutant_damage), [`StacyMutant_DoubleHead`](./Characters_and_Bosses.md#object-stacymutant_doublehead), [`StacyMutant_Fire`](./Characters_and_Bosses.md#object-stacymutant_fire), [`StacyMutant_Health`](./Characters_and_Bosses.md#object-stacymutant_health), [`StacyMutant_Holy`](./Characters_and_Bosses.md#object-stacymutant_holy), [`StacyMutant_Ice`](./Characters_and_Bosses.md#object-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#object-stacymutant_lightning), [`StacyMutant_Mirror`](./Characters_and_Bosses.md#object-stacymutant_mirror), [`StacyMutant_Speed`](./Characters_and_Bosses.md#object-stacymutant_speed), [`StacyMutant_Thorns`](./Characters_and_Bosses.md#object-stacymutant_thorns), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`palette`](./Enums.md#enum-palette) | Enum |  | 34 |
| `arm1` | Number | Sprite variant ID for the front arm. | 20 |
| `arm2` | Number |  | 22 |
| `body` | Number | Sprite variant ID for the body. | 10 |
| `ear1` | Number | Sprite variant ID for the front ear. | 26 |
| `head` | Number | Sprite variant ID for the head. | 12 |
| `leg1` | Number | Sprite variant ID for the front leg. | 16 |
| `leg2` | Number |  | 16 |
| `tail` | Number | Sprite variant ID for the tail. | 26 |
| `texture` | Number |  | 12 |
| `eye1` | Number |  | 6 |
| `eye2` | Number |  | 6 |
| `ear2` | Number |  | 20 |

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
| [`do`](./Enums.md#enum-do) | Enum |  | 24 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 6 |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 1 |
| [`do_best`](./Arrays.md#array-do_best) | Array |  | 1 |
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array |  | 1 |
| [`do_random`](./Arrays.md#array-do_random) | Array |  | 1 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum |  | 2 |

</details>

---

### Object: `BossRewards`



**Definition:** Loot logic: Rewards dropped upon defeating a boss.  
**Total Count:** 20


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`common`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 40 |
| [`rare`](./Engine_EventKeys.md#valid-property-keys) | `Enum/String` |  | 32 |

</details>

---

### Object: `AbilityReaction`



**Definition:** No definition provided.  
**Total Count:** 19


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 20 |
| `ability_damage_only` | Boolean |  | 14 |
| `backstabs_only` | Boolean |  | 6 |
| `only_when_not_your_turn` | Boolean |  | 6 |
| `cancel_knockback` | Boolean |  | 2 |
| `enemies_only` | Boolean |  | 2 |
| `even_on_0_damage_if_knockback` | Boolean |  | 2 |
| `even_on_0_damage` | Boolean |  | 2 |
| `match_knockback_direction` | Boolean |  | 2 |
| `ranged_only` | Boolean |  | 2 |
| `verify_target` | Boolean |  | 2 |

</details>

---

### Object: `MeleeRevengeDamage`



**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 19


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#object-temppassiveuntilsettled), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `damage` | Number | The base damage properties of an attack. | 44 |
| `knockback` | Number |  | 48 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 20 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 5 |
| `cant_miss` | `Boolean` |  | 2 |
| [`effects`](./Characters_and_Bosses.md#object-effects) | Object | Non-damaging impact triggers. | 94 |

</details>

---

### Object: `BirdRewards`



**Definition:** Loot logic: Rewards dropped by bird-type enemies.  
**Total Count:** 18


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ally_rewards`](./Characters_and_Bosses.md#object-ally_rewards) | Object | Loot logic triggered if an ally dies. | 36 |
| [`statuses`](./Characters_and_Bosses.md#object-statuses) | Object | Status effects possessed by the character. | 10 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`Antidote`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Applies or references the 'Antidote' effect/state. | 10 |
| `Blessing` | Mixed | Applies or references the 'Blessing' effect/state. | 10 |
| `BigCatnip` | Number | Applies or references the 'BigCatnip' effect/state. | 8 |
| `BigScrap` | Number | Applies or references the 'BigScrap' effect/state. | 8 |
| `BiggestFood` | Number | Applies or references the 'BiggestFood' effect/state. | 8 |
| `Coin` | Number | Applies or references the 'Coin' effect/state. | 8 |
| `BigFood` | Number | Applies or references the 'BigFood' effect/state. | 4 |
| `Coin10` | Mixed | Applies or references the 'Coin10' effect/state. | 4 |
| `Coin3` | Number | Applies or references the 'Coin3' effect/state. | 4 |
| `Coin4` | Number | Applies or references the 'Coin4' effect/state. | 4 |
| `MedCatnip` | Number | Applies or references the 'MedCatnip' effect/state. | 4 |
| `MedScrap` | Number | Applies or references the 'MedScrap' effect/state. | 4 |
| `RandomArmorPickup` | Number | Applies or references the 'RandomArmorPickup' effect/state. | 4 |
| `RandomCatnipPickup` | Number | Applies or references the 'RandomCatnipPickup' effect/state. | 4 |
| `RandomFoodPickup` | Number | Applies or references the 'RandomFoodPickup' effect/state. | 4 |
| `Bear` | Number | Applies or references the 'Bear' effect/state. | 2 |
| `BlackBird` | Number | Applies or references the 'BlackBird' effect/state. | 2 |
| `Catepillar` | Number | Applies or references the 'Catepillar' effect/state. | 2 |
| `Catnip` | Number | Applies or references the 'Catnip' effect/state. | 2 |
| `CharmedDip` | Number | Applies or references the 'CharmedDip' effect/state. | 2 |
| `CharmedFloater` | Number | Applies or references the 'CharmedFloater' effect/state. | 2 |
| `CharmedPile` | Number | Applies or references the 'CharmedPile' effect/state. | 2 |
| `Cherub` | Number | Applies or references the 'Cherub' effect/state. | 2 |
| `Chicken` | Number | Applies or references the 'Chicken' effect/state. | 2 |
| `Coin2` | Number | Applies or references the 'Coin2' effect/state. | 2 |
| `Dove` | Number | Applies or references the 'Dove' effect/state. | 2 |
| `Eagle` | Number | Applies or references the 'Eagle' effect/state. | 2 |
| `Food` | Number | Applies or references the 'Food' effect/state. | 2 |
| `Harpy` | Number | Applies or references the 'Harpy' effect/state. | 2 |
| `HummingBird` | Number | Applies or references the 'HummingBird' effect/state. | 2 |
| `LargeBirdPool` | Number | Applies or references the 'LargeBirdPool' effect/state. | 2 |
| `MedBirdPool` | Number | Applies or references the 'MedBirdPool' effect/state. | 2 |
| `Mutant` | Number | Character Form: Behavior and stats for the 'Mutant' state. | 2 |
| `Pigeon` | Number | Applies or references the 'Pigeon' effect/state. | 2 |
| `RandomBiggerArmorPickup` | Number | Applies or references the 'RandomBiggerArmorPickup' effect/state. | 2 |
| `RandomBiggerCatnipPickup` | Number | Applies or references the 'RandomBiggerCatnipPickup' effect/state. | 2 |
| `RandomBiggerFoodPickup` | Number | Applies or references the 'RandomBiggerFoodPickup' effect/state. | 2 |
| `Raven` | Number | Applies or references the 'Raven' effect/state. | 2 |
| `Scrap` | Number | Applies or references the 'Scrap' effect/state. | 2 |
| `Seagull` | Number | Applies or references the 'Seagull' effect/state. | 2 |
| `SmallBirdPool` | Number | Applies or references the 'SmallBirdPool' effect/state. | 2 |
| `Snake` | Number | Applies or references the 'Snake' effect/state. | 2 |
| `Squirrel` | Number | Applies or references the 'Squirrel' effect/state. | 2 |
| `Toad` | Number | Applies or references the 'Toad' effect/state. | 2 |
| `Turkey` | Number | Applies or references the 'Turkey' effect/state. | 2 |
| `Turtle` | Number | Applies or references the 'Turtle' effect/state. | 2 |

</details>

---

### Object: `CharacterLightSource`



**Definition:** Visual: Attaches a dynamic lighting source to the character.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`color`](./Arrays.md#array-color) | Array |  | 16 |
| `size` | Number |  | 32 |
| [`glow`](./Arrays.md#array-glow) | Array |  | 8 |

</details>

---

### Object: `HealthPickup`



**Definition:** Pickup Logic: Defines what happens when a health item is collected.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array |  | 15 |
| `stacks` | Number | Number of stacks or intensity to apply. | 30 |
| `stored_food_value` | Number |  | 30 |
| `anything_eats` | Boolean |  | 8 |
| `force_frame` | Number |  | 2 |

</details>

---

### Object: `ImmediateAbilityReaction`



**Definition:** No definition provided.  
**Total Count:** 13


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 26 |
| `ability_damage_only` | Boolean |  | 12 |
| `backstabs_only` | Boolean |  | 4 |
| `damage_threshold` | Number |  | 4 |
| `even_if_blocked` | Boolean |  | 4 |
| `even_if_stunned` | Boolean |  | 4 |
| `health_threshold` | Number |  | 4 |
| `buddy_damage_only` | Boolean |  | 2 |
| `target_furthest_valid` | Boolean |  | 2 |

</details>

---

### Object: `effects`





**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 13


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Characters_and_Bosses.md#object-meleerevengedamage), [`damage_instance`](./Characters_and_Bosses.md#object-damage_instance), [`eat_damage`](./Characters_and_Bosses.md#object-eat_damage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `BlackHoleSuck` | `Number` | Applies or references the 'BlackHoleSuck' effect/state. | 2 |
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 42 |

</details>

---

### Object: `AbilityHealthThreshold`



**Definition:** AI Trigger: Executes an ability when health drops below a specific threshold.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 26 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `even_if_stunned` | Boolean |  | 14 |
| `immediate` | Boolean |  | 12 |
| `use_ai` | Boolean |  | 4 |
| [`threshold_min`](./Math_Equations.md) | Equation |  | 2 |
| `also_use_if_buddy_is_dead` | Boolean |  | 2 |

</details>

---

### Object: `PassiveGroup`



**Definition:** Passive: A collection of passives grouped together for easier management.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#object-randompassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `SpawnThingOnDamage`



**Definition:** Applies or references the 'SpawnThingOnDamage' effect/state.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 76 |
| `good` | Boolean |  | 40 |
| `spawn_on_death_hit` | Boolean |  | 20 |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Probability (0.0 to 1.0) of executing this action. | 24 |
| `coins` | Number |  | 4 |
| [`auto_cast`](./Enums.md#enum-auto_cast) | Enum |  | 2 |
| `consider_all_layers` | Boolean |  | 4 |
| `melee_ability_only` | Boolean |  | 2 |

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
| [`do`](./Enums.md#enum-do) | Enum |  | 6 |
| [`do_one`](./Arrays.md#array-do_one) | Array |  | 2 |
| [`do_random`](./Arrays.md#array-do_random) | Array |  | 2 |
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array |  | 1 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 1 |

</details>

---

### Object: `Normal`




**Definition:** Character Form: Behavior and stats for the \'Normal\' state.  
**Total Count:** 231


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 10 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 4 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

</details>

---

### Object: `DeathRattleRevive`



**Definition:** No definition provided.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 16 |
| `even_if_stunned` | Boolean |  | 16 |

</details>

---

### Object: `MoveWhenDamaged`



**Definition:** No definition provided.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 18 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 4 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 16 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 12 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 8 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 4 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| `move_speed_multiplier` | Number |  | 2 |

</details>

---

### Object: `FormChangeOnElementInfluence`



**Definition:** Logic: Changes form when affected by an element.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 16 |
| [`form`](./Enums.md#enum-form) | Enum |  | 18 |
| [`exclude`](./Enums.md#enum-exclude) | Enum |  | 10 |
| [`particle`](./Enums.md#enum-particle) | Enum |  | 10 |
| [`sfx`](./Enums.md#enum-sfx) | Enum |  | 10 |

</details>

---

### Object: `ReflectProjectiles`



**Definition:** No definition provided.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusCollector`



**Definition:** Passive: Gains benefits based on the number of statuses applied to them.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `TransformInXTurns`



**Definition:** Logic: Forces a form change after X turns.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#object-randompassivepool), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array |  | 12 |
| `stacks` | Number | Number of stacks or intensity to apply. | 16 |
| [`initiative`](./Enums.md#enum-initiative) | Enum |  | 8 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 4 |
| [`turns`](./Arrays.md#array-turns) | Array | Turn counter tracking. | 1 |

</details>

---

### Object: `TransformOnElementInfluence`



**Definition:** Logic: Changes form when affected by elements.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 18 |
| [`object`](./Enums.md#enum-object) | Enum |  | 18 |

</details>

---

### Object: `statuses`




**Definition:** Status effects possessed by the character.  
**Total Count:** 14


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BirdRewards`](./Characters_and_Bosses.md#object-birdrewards), [`Cat`](./Characters_and_Bosses.md#object-cat), [`NonCat`](./Characters_and_Bosses.md#object-noncat)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `FormChangeOffMap`



**Definition:** Logic: Changes form when pushed off the map.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_offmap`](./Enums.md#enum-form_offmap) | Enum |  | 16 |
| [`form_onmap`](./Enums.md#enum-form_onmap) | Enum |  | 16 |

</details>

---

### Object: `SmallRockBehavior`



**Definition:** No definition provided.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 8 |
| `knockback` | Number |  | 8 |
| `chain` | Boolean |  | 4 |

</details>

---

### Object: `ChanceToSpitOnDamage`



**Definition:** Reaction: Probability to use a spit counter-attack when damaged.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 14 |
| `flat_chance` | Number |  | 10 |
| `chance_per_damage` | Number |  | 6 |
| `backstabs_only` | Boolean |  | 2 |
| `even_on_0_damage_if_knockback` | Boolean |  | 2 |

</details>

---

### Object: `MovementReaction`



**Definition:** Reaction: Triggers an effect or ability when forced to move.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 22 |
| `enemies_only` | Boolean |  | 14 |
| `objects_too` | Boolean |  | 4 |
| `on_self_move_too` | Boolean |  | 6 |
| `blind_spot` | Boolean |  | 2 |
| `forward_only` | Boolean |  | 2 |
| `self_move_exclude_self_abilities` | Boolean |  | 2 |

</details>

---

### Object: `CaveFamilyEnrage`



**Definition:** AI Trigger: Enrage logic triggered when a cave family member is killed.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 12 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 12 |
| `count` | Number | The numerical quantity. | 12 |

</details>

---

### Object: `FormChangeWhilePrimingAbility`



**Definition:** Logic: Changes form while preparing/priming a specific ability.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`not_priming`](./Enums.md#enum-not_priming) | Enum |  | 12 |
| [`priming`](./Enums.md#enum-priming) | Enum |  | 16 |

</details>

---

### Object: `MoveTowardsDamageSource`



**Definition:** No definition provided.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`check_in_form`](./Enums.md#enum-check_in_form) | Enum |  | 4 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 10 |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`check_has_status`](./Enums.md#enum-check_has_status) | Enum |  | 2 |
| [`ignore_tagged_sources`](./Enums.md#enum-ignore_tagged_sources) | Enum |  | 2 |
| `can_move_zero` | Boolean |  | 2 |
| `do_not_move_on_top` | Boolean |  | 2 |
| `face_towards_after` | Boolean |  | 2 |
| `move_far` | Boolean |  | 8 |
| `move_short` | Boolean |  | 2 |

</details>

---

### Object: `SecurityBotProtect`



**Definition:** AI Logic: Guarding behavior for Security Bot units.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 14 |
| [`move`](./Enums.md#enum-move) | Enum |  | 10 |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum |  | 6 |
| `enemies_only` | Boolean |  | 6 |
| `not_on_kill` | Boolean |  | 4 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 10 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 10 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 8 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 2 |

</details>

---

### Object: `MoveTowardsKillers`



**Definition:** No definition provided.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`character_filter`](./Arrays.md#array-character_filter) | Array |  | 3 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 6 |

</details>

---

### Object: `PassiveWhileHasStatus`



**Definition:** Passive: Activates only while the character has the specified status.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 12 |

</details>

---

### Object: `TransformOnDeathImmediately`



**Definition:** No definition provided.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum |  | 8 |
| [`obj`](./Enums.md#enum-obj) | Enum |  | 8 |

</details>

---

### Object: `BaitAura`



**Definition:** Passive: Projects an aura that attracts specific enemy types (e.g., flies/maggots).  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `range` | Number | Distance or area of effect in tiles. | 8 |

</details>

---

### Object: `Consumed`



**Definition:** State object triggered when this object or entity is eaten/consumed by another character.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`statuses`](./Characters_and_Bosses.md#object-statuses)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `use_placeholder` | Boolean |  | 6 |
| `do_not_pop_corpse` | `Boolean` |  | 22 |
| [`drop_on_death`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` |  | 22 |
| `force_contact` | `Boolean` | If true, enforces physical overlap. | 30 |
| `instant` | `Boolean` |  | 24 |
| [`mount_mode`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | If true, treats the consumption as riding/mounting instead of eating. | 24 |
| [`struggle_ability`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Ability triggered by the consumed entity while inside the consumer. | 34 |

</details>

---

### Object: `ForceUseAbility`



**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossHitCountdownBoris`](./Characters_and_Bosses.md#object-finalbosshitcountdownboris), [`FinalBossHitCountdownExplosive`](./Characters_and_Bosses.md#object-finalbosshitcountdownexplosive)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 10 |
| `show_name` | Boolean |  | 4 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 8 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 8 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 8 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 8 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 6 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 6 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

</details>

---

### Object: `StatusEachTurnEnd`



**Definition:** Applies or references the 'StatusEachTurnEnd' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StatusOnKill`



**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StatusOnTookDamageFromAbility`



**Definition:** Event Trigger: Applies statuses when taking damage from an ability.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StunImmunity`



**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean |  | 2 |

</details>

---

### Object: `Trapper`



**Definition:** Character Form: Behavior and stats for the 'Trapper' state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 8 |
| `cancel_movement` | Boolean |  | 4 |
| `pathfinding_avoidance` | Number |  | 4 |
| `range` | Number | Distance or area of effect in tiles. | 4 |

</details>

---

### Object: `default`




**Definition:** Character Form: The baseline default behavior state.  
**Total Count:** 13


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 8 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 8 |

</details>

---

### Object: `keyword_tooltips`




**Definition:** Forces specific UI tooltips to appear when hovering over the ability.  
**Total Count:** 35


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Die`](./Characters_and_Bosses.md#object-die), [`Dumb`](./Characters_and_Bosses.md#object-dumb), [`Obey`](./Characters_and_Bosses.md#object-obey), [`Stop`](./Characters_and_Bosses.md#object-stop)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TVBotDie` | Number | Applies or references the 'TVBotDie' effect/state. | 2 |
| `TVBotDumb` | Number | Applies or references the 'TVBotDumb' effect/state. | 2 |
| `TVBotObey` | Number | Applies or references the 'TVBotObey' effect/state. | 2 |
| `TVBotStop` | Number | Applies or references the 'TVBotStop' effect/state. | 2 |

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
| `stacks` | Number | Number of stacks or intensity to apply. | 6 |

</details>

---

### Object: `Buddy`



**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`obj`](./Enums.md#enum-obj) | Enum |  | 6 |
| `allies_only` | Boolean |  | 6 |
| `reclaim_if_lost` | Boolean |  | 2 |

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
| [`formchange`](./Enums.md#enum-formchange) | Enum |  | 6 |
| [`statuses`](./Characters_and_Bosses.md#object-statuses) | Object | Status effects possessed by the character. | 4 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 4 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 4 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |

</details>

---

### Object: `FormChangeHealthThreshold`



**Definition:** Logic: Changes form when health crosses a threshold.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_above`](./Enums.md#enum-form_above) | Enum |  | 6 |
| [`form_below`](./Enums.md#enum-form_below) | Enum |  | 6 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `count_shield` | Boolean |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 4 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 4 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 4 |
| [`statuses_on_enter_form`](./Characters_and_Bosses.md#object-statuses_on_enter_form) | Object | Status effects instantly applied upon transitioning into this form. | 4 |

</details>

---

### Object: `ManaPickup`



**Definition:** Pickup Logic: Defines what happens when a mana item is collected.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array |  | 3 |
| `stacks` | Number | Number of stacks or intensity to apply. | 6 |

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
| [`formchange`](./Enums.md#enum-formchange) | Enum |  | 6 |
| [`statuses`](./Characters_and_Bosses.md#object-statuses) | Object | Status effects possessed by the character. | 4 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |

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
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 6 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `RandomPassivePool`



**Definition:** Logic: Grants a random passive from the specified pool upon spawning.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `ReplaceBrain`



**Definition:** Applies the 'ReplaceBrain' effect.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StacyMutant_Fire`](./Characters_and_Bosses.md#object-stacymutant_fire), [`StacyMutant_Ice`](./Characters_and_Bosses.md#object-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#object-stacymutant_lightning)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 8 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 8 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 8 |
| [`pattern`](./Characters_and_Bosses.md#object-pattern) | Object | AI sequence logic. | 6 |

</details>

---

### Object: `SupportFormChangeInsteadOfRun`



**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| `wait_till_turn` | Boolean |  | 2 |

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
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 6 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 4 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 4 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |

</details>

---

### Object: `AbilityOnRoundEnd`



**Definition:** AI Trigger: Executes an ability at the end of the combat round.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| `force_display_name` | Boolean |  | 4 |

</details>

---

### Object: `AbilityWhenTaggedCharacterMovesNear`



**Definition:** AI Trigger: Executes an ability when a character with a specific tag moves adjacent.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 10 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 10 |
| `range` | Number | Distance or area of effect in tiles. | 10 |

</details>

---

### Object: `AddTemporaryEffectsToBasicAttack`



**Definition:** Applies the 'AddTemporaryEffectsToBasicAttack' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Fury` | Number | Applies or references the 'Fury' effect/state. | 8 |

</details>

---

### Object: `AutocastEachRound`



**Definition:** Forces the character to automatically cast a specific ability at the start of each combat round.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 18 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 12 |

</details>

---

### Object: `Big`




**Definition:** Character Form / AI State: Behavior and stats for the \'Big\' state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`animation_suffix`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed |  | 4 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `BungaEntrance`



**Definition:** Animation/AI State: Bunga entering the arena.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum |  | 4 |
| `even_if_stunned` | Boolean |  | 4 |
| `health_threshold` | Number |  | 4 |

</details>

---

### Object: `CaveMan`




**Definition:** Character Form: Behavior and stats for the \'CaveMan\' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 4 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 4 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 4 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 4 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 4 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 4 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |

</details>

---

### Object: `CherubimReaction`



**Definition:** Reaction: Custom reaction triggers for Cherubim enemies.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Leave`](./Enums.md#enum-leave) | Enum | Applies or references the 'Leave' effect/state. | 4 |
| [`Return`](./Enums.md#enum-return) | Enum | Applies or references the 'Return' effect/state. | 4 |

</details>

---

### Object: `Conditional_GoodRoll`



**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ally_rewards`](./Characters_and_Bosses.md#object-ally_rewards)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 72 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 4 |

</details>

---

### Object: `DiesToElement`



**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `instant` | `Boolean` |  | 2 |

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 4 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 4 |

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `FaceLastDamage`



**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean |  | 2 |

</details>

---

### Object: `FormChangeDuringWeatherElement`



**Definition:** Logic: Changes form automatically during specific weather conditions.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 4 |
| [`form`](./Enums.md#enum-form) | Enum |  | 4 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

</details>

---

### Object: `Holy`




**Definition:** Character Form: Behavior and stats for the \'Holy\' state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `KnockUpAndAway`





**Definition:** Displaces the target vertically and horizontally away from the source.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#object-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#object-conditional_isphysicalattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `displace` | Boolean |  | 4 |
| `distance` | Number | The distance in tiles to knock the target away. | 48 |
| `stacks` | Number | Number of stacks or intensity to apply. | 44 |

</details>

---

### Object: `MotherTumorSpawnInCapture`



**Definition:** Boss Logic: Logic for capturing entities inside the Mother's tumors upon spawning.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Cat`](./Characters_and_Bosses.md#object-cat) | Object | Character Form: Base form for standard cats. | 4 |
| [`NonCat`](./Characters_and_Bosses.md#object-noncat) | Object | Character Form: Behavior and stats for the 'NonCat' state. | 4 |
| [`Nothing`](./Characters_and_Bosses.md#object-nothing) | Object | Character Form: Behavior and stats for the 'Nothing' state. | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 4 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 4 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 4 |

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
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 4 |

</details>

---

### Object: `PassiveWhileNotHasStatus`



**Definition:** Passive: Activates only while the character does NOT have the specified status.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 4 |

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
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `ProtectTargetedAllies`



**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| [`target_filter`](./Enums.md#enum-target_filter) | Enum |  | 4 |

</details>

---

### Object: `Rain`





**Definition:** Character Form: Behavior and stats for the 'Rain' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 4 |

</details>

---

### Object: `RemoveStatusStacks`



**Definition:** Removes a specific number of stacks of a status effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Characters_and_Bosses.md#object-statusonendmove), [`StatusOnTookDamage`](./Characters_and_Bosses.md#object-statusontookdamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 8 |
| `stacks` | Number | The number of stacks to remove. | 8 |

</details>

---

### Object: `SlotMachineRollPool`



**Definition:** Logic: Defines the possible outcomes for slot machine enemies.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SlotResult_Jackpot_Coins` | Number | Applies or references the 'SlotResult_Jackpot_Coins' effect/state. | 4 |
| `SlotResult_Explode` | Number | Applies or references the 'SlotResult_Explode' effect/state. | 2 |
| `SlotResult_Nothing` | Number | Applies or references the 'SlotResult_Nothing' effect/state. | 2 |
| `SlotResult_RandomPickup` | Number | Applies or references the 'SlotResult_RandomPickup' effect/state. | 2 |

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 4 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 4 |

</details>

---

### Object: `SquirrelForm`




**Definition:** Character Form: Behavior and stats for the 'SquirrelForm' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 4 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 4 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 2 |

</details>

---

### Object: `StatusGroup`



**Definition:** Groups multiple status effects together for batch application.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Characters_and_Bosses.md#object-randomstatusfrompool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StatusOnSpawnIn`



**Definition:** Event Trigger: Applies statuses immediately when spawned.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnTookDamage`



**Definition:** Event Trigger: Applies nested statuses when took damage.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `TempPassiveUntilSettled`





**Definition:** Passive: Active only until the physics engine stops moving the character.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#object-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#object-conditional_isphysicalattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `TinkererBasicAttackSwitching`



**Definition:** Logic: Allows Tinkerer to swap basic attacks.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveGroup`](./Characters_and_Bosses.md#object-passivegroup), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum |  | 6 |
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum |  | 6 |

</details>

---

### Object: `TransformOnElementInfluencex`



**Definition:** Logic: Variant element influence transformation.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 4 |
| [`object`](./Enums.md#enum-object) | Enum |  | 4 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 4 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 4 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 4 |
| [`move`](./Enums.md#enum-move) | Enum |  | 4 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`do`](./Enums.md#enum-do) | Enum |  | 6 |

</details>

---

### Object: `passive`




**Definition:** Intrinsic passive modifier.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 4 |

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

</details>

---

### Object: `AddStatusToReceivedDamage`



**Definition:** Modifier: Applies a status effect whenever the character takes damage.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToSpells`



**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToTrampleDamage`



**Definition:** Applies the 'AddStatusToTrampleDamage' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Characters_and_Bosses.md#object-passivewhendead)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToWeapons`



**Definition:** Applies the 'AddStatusToWeapons' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `AdventureTokenPassivePool`



**Definition:** Map/Metaprogression: Pool of passive modifiers applied by adventure tokens.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `AggroTargetIsGovernedByHitEffect`



**Definition:** AI Logic: Forces the character's aggro to follow specific hit effects rather than default proximity.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 2 |

</details>

---

### Object: `AllStatsAura`



**Definition:** Passive: Projects an aura that modifies all primary stats of nearby characters.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`aura_requires_tag`](./Enums.md#enum-aura_requires_tag) | Enum |  | 2 |
| [`range`](./Enums.md#enum-range) | Enum | Distance or area of effect in tiles. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Object: `Angry`




**Definition:** Character Form / AI State: Behavior and stats for the \'Angry\' state.  
**Total Count:** 221


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |

</details>

---

### Object: `BackflipWhenTargeted`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnGainCoins`](./Characters_and_Bosses.md#object-statusongaincoins)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific dodge ability to trigger (e.g., DestroyerDodge). | 14 |
| `stacks` | Number | Number of stacks or intensity to apply. | 14 |

</details>

---

### Object: `BattlefieldUniqueRandomPassive`



**Definition:** Map Rule: Grants a unique random passive modifier to the battlefield.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Number | Applies or references the 'DemonicGlyph_Bite' effect/state. | 2 |
| `DemonicGlyph_Bounce` | Number | Applies or references the 'DemonicGlyph_Bounce' effect/state. | 2 |
| `DemonicGlyph_Fire` | Number | Applies or references the 'DemonicGlyph_Fire' effect/state. | 2 |
| `DemonicGlyph_Movement` | Number | Applies or references the 'DemonicGlyph_Movement' effect/state. | 2 |
| `DemonicGlyph_Summon` | Number | Applies or references the 'DemonicGlyph_Summon' effect/state. | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 2 |

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `Bishop`




**Definition:** Character Form / AI State: Behavior and stats for the \'Bishop\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |
| `uifloaters_offset` | Number |  | 2 |

</details>

---

### Object: `BlackHole`




**Definition:** Character Form / AI State: Behavior and stats for the \'BlackHole\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |

</details>

---

### Object: `Bomb`




**Definition:** Character Form / AI State: Behavior and stats for the 'Bomb' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `BungaCheers`



**Definition:** Animation/AI State: Bunga cheering animation logic.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ally_damage`](./Enums.md#enum-ally_damage) | Enum |  | 2 |
| [`ally_dead`](./Enums.md#enum-ally_dead) | Enum |  | 2 |
| [`enemy_damage`](./Enums.md#enum-enemy_damage) | Enum |  | 2 |
| [`enemy_dead`](./Enums.md#enum-enemy_dead) | Enum |  | 2 |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum |  | 2 |

</details>

---

### Object: `CaveBaby`




**Definition:** Character Form: Behavior and stats for the \'CaveBaby\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |

</details>

---

### Object: `CaveWoman`




**Definition:** Character Form: Behavior and stats for the \'CaveWoman\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |

</details>

---

### Object: `CerberubsAggroTargetBehavior`



**Definition:** AI Logic: Custom aggro targeting rules for Cerberubs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alert_form`](./Enums.md#enum-alert_form) | Enum |  | 2 |
| [`default_form`](./Enums.md#enum-default_form) | Enum |  | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 2 |

</details>

---

### Object: `ChanceToBackflip`



**Definition:** Applies or references the 'ChanceToBackflip' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 12 |
| `chance` | Number | Probability (0.0 to 1.0) of executing this action. | 12 |

</details>

---

### Object: `ChanceToFormChangeOnAbilityDamage`



**Definition:** Reaction: Probability to change forms when taking ability damage.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum |  | 2 |
| `chance` | Number | Probability (0.0 to 1.0) of executing this action. | 2 |

</details>

---

### Object: `ChaosBossFormChangeGuide`



**Definition:** Boss Logic: Maps the form transition phases for the Chaos Boss.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array |  | 1 |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array |  | 1 |
| `passives_health_threshold` | Number |  | 2 |

</details>

---

### Object: `ChaosBossPieces`



**Definition:** Boss Logic: Defines the separate destructible pieces of the Chaos Boss.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array |  | 1 |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array |  | 1 |

</details>

---

### Object: `ChaosHeadDropIn`



**Definition:** Boss Logic: Drop-in attack/animation for the Chaos Head.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`new_music`](./Enums.md#enum-new_music) | Enum |  | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Object: `Conditional_BadRoll`



**Definition:** Conditional trigger: Executes nested logic based on a randomized bad outcome probability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Characters_and_Bosses.md#object-statuseachturnend)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 16 |

</details>

---

### Object: `Conditional_HasKnockback`




**Definition:** Conditional: Executes logic if the triggering attack deals knockback.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Characters_and_Bosses.md#object-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`KnockUpAndAway`](./Characters_and_Bosses.md#object-knockupandaway) | Object | Logic: Applies vertical and horizontal displacement. | 2 |
| `RemoveKnockback` | `Number` | Applies or references the 'RemoveKnockback' effect/state. | 2 |
| [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#object-temppassiveuntilsettled) | Object | Passive: Active only until the physics engine stops moving the character. | 2 |

</details>

---

### Object: `Conditional_IsPhysicalAttack`



**Definition:** Conditional: Executes logic if the triggering attack is physical.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#object-addstatustoreceiveddamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`KnockUpAndAway`](./Characters_and_Bosses.md#object-knockupandaway) | Object | Logic: Applies vertical and horizontal displacement. | 2 |
| `RemoveKnockback` | `Number` | Applies or references the 'RemoveKnockback' effect/state. | 2 |
| [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#object-temppassiveuntilsettled) | Object | Passive: Active only until the physics engine stops moving the character. | 2 |

</details>

---

### Object: `CounterAttack`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 10 |
| `without_orienting` | Boolean |  | 2 |

</details>

---

### Object: `CreateGlobalModifiers`



**Definition:** Generates global map or encounter rules/modifiers.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `BloodRain` | `Number` | Applies or references the 'BloodRain' effect/state. | 6 |
| [`LowerAmbientLight`](./Characters_and_Bosses.md#object-lowerambientlight) | Object | Visual: Dims the map lighting. | 6 |

</details>

---

### Object: `Cultist`




**Definition:** Character Form: Behavior and stats for the \'Cultist\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

</details>

---

### Object: `DelayedAutoRevive`



**Definition:** Applies or references the 'DelayedAutoRevive' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 12 |
| `rounds` | Number |  | 12 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |

</details>

---

### Object: `DiceBehavior`



**Definition:** AI Logic: Custom behavior for Dice enemies.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dice_size` | Number |  | 2 |
| `knockback_damage` | Number |  | 2 |

</details>

---

### Object: `Die`





**Definition:** Character Form / Logic: Forces the character to die.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear. | 2 |

</details>

---

### Object: `DiesToPiercingAndSpikes`



**Definition:** Vulnerability: Character dies instantly if hit by piercing attacks or spikes.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `deferred` | Boolean |  | 2 |

</details>

---

### Object: `DodgeWhenTargeted`



**Definition:** Reaction: Executes a dodge maneuver when targeted.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |

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
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| `move_speed_multiplier` | Number |  | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| `move_speed_multiplier` | Number |  | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`keyword_tooltips`](./Characters_and_Bosses.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `DybbukPossessionFallback`



**Definition:** Logic: Fallback state when a Dybbuk possession fails.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum |  | 2 |
| [`form`](./Enums.md#enum-form) | Enum |  | 2 |

</details>

---

### Object: `Else`



**Definition:** Fallback object that executes if the preceding `Conditional_` block evaluated to false.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#object-addstatustoreceiveddamage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`Conditional_HasKnockback`](./Characters_and_Bosses.md#object-conditional-hasknockback) | Object | Conditional: Executes logic if the triggering attack deals knockback. | 2 |
| [`KnockUpAndAway`](./Characters_and_Bosses.md#object-knockupandaway) | Object | Logic: Applies vertical and horizontal displacement. | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |

</details>

---

### Object: `FaceAwayLastDamage`



**Definition:** Reaction: Forces the character to face away from the last damage source.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean |  | 2 |
| `override_hit_animation` | Boolean |  | 2 |
| `use_turn_animations` | Boolean |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

</details>

---

### Object: `FinalBossBeamQueue`



**Definition:** Boss Logic: Attack queue for the final boss beam.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`queue`](./Enums.md#enum-queue) | Enum |  | 2 |
| [`release`](./Enums.md#enum-release) | Enum |  | 2 |
| [`transform`](./Enums.md#enum-transform) | Enum |  | 2 |

</details>

---

### Object: `FinalBossBecomeTheChild`



**Definition:** Boss Logic: Phase transition for the final boss.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`GlobalSpawnCharacter`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'GlobalSpawnCharacter' effect/state. | 2 |
| `PlayBackground` | `Number` | Applies or references the 'PlayBackground' effect/state. | 2 |
| [`SwitchMusic`](./Characters_and_Bosses.md#object-switchmusic) | Object | Event Trigger: Changes background music track. | 2 |

</details>

---

### Object: `FinalBossHitCountdownBoris`



**Definition:** Boss Logic: Countdown trigger for Boris.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `icon_ready` | Number |  | 2 |
| `icon` | Number |  | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Object: `FinalBossHitCountdownExplosive`



**Definition:** Boss Logic: Countdown trigger for explosives.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `icon_ready` | Number |  | 2 |
| `icon` | Number |  | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Object: `FinalBossHitCountdownHoly`



**Definition:** Boss Logic: Countdown trigger for holy attacks.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `icon_ready` | Number |  | 2 |
| `icon` | Number |  | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Object: `FinalBossPupils`



**Definition:** Boss Logic: Pupil state management.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`look_at_offset`](./Arrays.md#array-look_at_offset) | Array |  | 1 |
| [`reset_center_because_no_target_halflife`](./Enums.md#enum-reset_center_because_no_target_halflife) | Enum |  | 2 |
| [`reset_center_because_of_animation_halflife`](./Enums.md#enum-reset_center_because_of_animation_halflife) | Enum |  | 2 |
| [`teleport_tracking_halflife`](./Enums.md#enum-teleport_tracking_halflife) | Enum |  | 2 |
| [`tracking_acquisition_halflife`](./Enums.md#enum-tracking_acquisition_halflife) | Enum |  | 2 |
| [`virtual_head_position`](./Arrays.md#array-virtual_head_position) | Array |  | 1 |
| `radius` | Number | Distance or area of effect in tiles. | 2 |

</details>

---

### Object: `FinalBossShieldHealth`



**Definition:** Boss Logic: Shield health management.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`break_ability`](./Enums.md#enum-break_ability) | Enum |  | 2 |
| [`state_health`](./Arrays.md#array-state_health) | Array |  | 1 |

</details>

---

### Object: `FinalBossSyncAnimations`



**Definition:** Boss Logic: Synchronizes multi-part boss animations.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`other_character`](./Enums.md#enum-other_character) | Enum |  | 2 |
| [`other_form_change_abilities`](./Characters_and_Bosses.md#object-other_form_change_abilities) | Object | Lists secondary abilities used to change forms. | 2 |

</details>

---

### Object: `Fire`




**Definition:** Character Form: Behavior and stats for the 'Fire' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `FireFull`




**Definition:** Character Form: Behavior and stats for the 'FireFull' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |

</details>

---

### Object: `Flush`




**Definition:** Character Form: Behavior and stats for the 'Flush' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 2 |

</details>

---

### Object: `GainDisorderFromPool`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Characters_and_Bosses.md#object-addstatustobasicattack)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0) of executing this action. | 2 |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 2 |

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
| [`exit_animations`](./Characters_and_Bosses.md#object-exit_animations) | Object | Animations played when leaving a form/state. | 2 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 2 |
| `uifloaters_offset` | Number |  | 2 |
| `weak_threshold` | Number |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 2 |

</details>

---

### Object: `HPAltStates`



**Definition:** Visual: Alternative sprite states based on current health.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`clipname`](./Enums.md#enum-clipname) | Enum |  | 2 |
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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |

</details>

---

### Object: `HealNeighborsEachTurn`



**Definition:** Passive: Restores health to adjacent allies at the start of the turn.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |

</details>

---

### Object: `HitlerExecute`



**Definition:** Boss Logic: Specific execution or ultimate attack state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |

</details>

---

### Object: `InfiniteRebirth`



**Definition:** Applies the 'InfiniteRebirth' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 6 |
| `immediate` | Boolean |  | 2 |
| `playercat_health` | Number |  | 6 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

</details>

---

### Object: `Johnny`




**Definition:** Character Form: Behavior and stats for the 'Johnny' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `JohnnyNeedsWashing`



**Definition:** Character Form: Behavior and stats for the 'JohnnyNeedsWashing' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_unwashed`](./Enums.md#enum-form_unwashed) | Enum |  | 2 |
| [`form_washed`](./Enums.md#enum-form_washed) | Enum |  | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `LastHit`




**Definition:** Logic: Executes logic on the final hit of a multi-hit attack.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

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
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `LowerAmbientLight`





**Definition:** A visual effect that dims the map's lighting.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CreateGlobalModifiers`](./Characters_and_Bosses.md#object-createglobalmodifiers)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`amount`](./Arrays.md#array-amount) | Array | The target opacity/dimness level. | 1 |
| `speed` | Number | The transition speed. | 6 |

</details>

---

### Object: `MegaDinoDropController`



**Definition:** Boss Logic: Manages loot drops for the Mega Dino.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`head_drop`](./Enums.md#enum-head_drop) | Enum |  | 2 |
| [`leg_leave`](./Enums.md#enum-leg_leave) | Enum |  | 2 |
| [`leg_return`](./Enums.md#enum-leg_return) | Enum |  | 2 |
| `stable_legs` | Number |  | 2 |

</details>

---

### Object: `ModularPickup`



**Definition:** Pickup Logic: Defines what happens when a modular item is collected.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`sound_event`](./Enums.md#enum-sound_event) | Enum |  | 2 |

</details>

---

### Object: `MonkCatReactionAbilities`



**Definition:** Reaction: Specific counter-attack or dodge abilities used by the Monk class.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 6 |
| [`move`](./Enums.md#enum-move) | Enum |  | 4 |
| [`spell`](./Enums.md#enum-spell) | Enum |  | 2 |
| [`trinket`](./Enums.md#enum-trinket) | Enum |  | 2 |
| [`weapon`](./Enums.md#enum-weapon) | Enum | Weapon item constraint. | 2 |

</details>

---

### Object: `MotherGrowController`



**Definition:** Boss Logic: Manages the growth phases of the Mother boss.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eat_damage`](./Characters_and_Bosses.md#object-eat_damage) | Object | Damage dealt when this entity consumes another. | 2 |
| [`tumor_object`](./Enums.md#enum-tumor_object) | Enum |  | 2 |

</details>

---

### Object: `MotherTumorPassive`



**Definition:** Boss Logic: Passive effects applied to the Mother's tumors.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Cat`](./Characters_and_Bosses.md#object-cat) | Object | Character Form: Base form for standard cats. | 2 |
| [`NonCat`](./Characters_and_Bosses.md#object-noncat) | Object | Character Form: Behavior and stats for the 'NonCat' state. | 2 |
| [`considered_forms`](./Arrays.md#array-considered_forms) | Array |  | 1 |
| [`grow_ability`](./Enums.md#enum-grow_ability) | Enum |  | 2 |
| [`pass_ani`](./Enums.md#enum-pass_ani) | Enum |  | 2 |
| [`receive_ani`](./Enums.md#enum-receive_ani) | Enum |  | 2 |

</details>

---

### Object: `Mount`



**Definition:** Character Form: Behavior and stats for the 'Mount' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eject_ability`](./Enums.md#enum-eject_ability) | Enum |  | 2 |
| [`enter_ability`](./Enums.md#enum-enter_ability) | Enum |  | 2 |

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `MoveAfterAnyAttemptedAttack`



**Definition:** AI Movement: Forces a move action immediately after attacking, even if it missed.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 2 |

</details>

---

### Object: `MoveAwayFromDamageSource`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 2 |

</details>

---

### Object: `MoveAwayWhenEnemyAdjacent`



**Definition:** AI Movement: Moves away if an enemy enters an adjacent tile.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 2 |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 2 |
| `once_per_turn` | Boolean |  | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Object: `MultiSpawnOnDeath`



**Definition:** Event Trigger: Spawns multiple entities upon death.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array | The numerical quantity. | 1 |
| [`obj`](./Enums.md#enum-obj) | Enum |  | 2 |

</details>

---

### Object: `Mutant`




**Definition:** Character Form: Behavior and stats for the \'Mutant\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move_speed_multiplier`](./Enums.md#enum-move_speed_multiplier) | Enum |  | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Object: `NeutronStar`




**Definition:** Character Form: Behavior and stats for the 'NeutronStar' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |

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
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |

</details>

---

### Object: `Nuke`




**Definition:** Character Form: Behavior and stats for the 'Nuke' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

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
| [`keyword_tooltips`](./Characters_and_Bosses.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 2 |

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
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |

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
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `PassiveWhenAffectedByElement`



**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 36 |

</details>

---

### Object: `PassiveWhenDead`



**Definition:** State Trigger: Grants passives when this condition is met.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `animation_suffix` | Number |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |
| `uifloaters_offset` | Number |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `animation_suffix` | Number |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |
| `uifloaters_offset` | Number |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `animation_suffix` | Number |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |
| `uifloaters_offset` | Number |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `animation_suffix` | Number |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |
| `uifloaters_offset` | Number |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `animation_suffix` | Number |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |
| `uifloaters_offset` | Number |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `animation_suffix` | Number |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |
| `uifloaters_offset` | Number |  | 2 |

</details>

---

### Object: `RandomStatusFromPool`



**Definition:** Selects and applies a random status effect from the provided nested object.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ally_rewards`](./Characters_and_Bosses.md#object-ally_rewards)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Object: `RevengeDamage`



**Definition:** Reaction trigger: Deals damage to the attacker when hit.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 10 |
| `damage` | Number | The base damage properties of an attack. | 16 |
| `knockback` | Number |  | 6 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Object: `RunWhenLastPlayerCatIsCharmed`



**Definition:** AI Logic: Flee logic when the player team is entirely crowd-controlled.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`legacy_savekey`](./Enums.md#enum-legacy_savekey) | Enum |  | 2 |
| `allow_decision_mid_turn` | Boolean |  | 2 |

</details>

---

### Object: `ScalingAttackAnimation`



**Definition:** Visual: Animation scales based on damage output.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`default`](./Enums.md#enum-default) | Enum | Baseline configuration. | 2 |
| [`thresholds`](./Arrays.md#array-thresholds) | Array |  | 1 |

</details>

---

### Object: `SharePickups`



**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `include_coins` | Boolean |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

</details>

---

### Object: `SkipFirstRounds`



**Definition:** AI Logic: Passes turn for the first X rounds of combat.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `pop_chance` | Number |  | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `SpewerAltGraphics`



**Definition:** Visual: Alternative graphics for Spewer enemies.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FireFull` | Number | Character Form: Behavior and stats for the 'FireFull' state. | 2 |
| `Fire` | Number | Character Form: Behavior and stats for the 'Fire' state. | 2 |
| `NormalFull` | Number | Character Form: Behavior and stats for the 'NormalFull' state. | 2 |
| `Normal` | Number | Character Form: Behavior and stats for the 'Normal' state. | 2 |
| `TarFull` | Number | Character Form: Behavior and stats for the 'TarFull' state. | 2 |
| `Tar` | Number | Character Form: Behavior and stats for the 'Tar' state. | 2 |

</details>

---

### Object: `StacyMutant_Brace`



**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Brace' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StacyMutant_Counter`



**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Counter' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StacyMutant_Damage`



**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Damage' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StacyMutant_DoubleHead`



**Definition:** Character Form: Behavior and stats for the 'StacyMutant_DoubleHead' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StacyMutant_Fire`



**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Fire' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StacyMutant_Health`



**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Health' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StacyMutant_Holy`



**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Holy' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StacyMutant_Ice`



**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Ice' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StacyMutant_Lightning`



**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Lightning' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StacyMutant_Mirror`



**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Mirror' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StacyMutant_Speed`



**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Speed' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StacyMutant_Thorns`



**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Thorns' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`turns`](./Characters_and_Bosses.md#object-turns) | Object | Turn counter tracking. | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StatusAfterXTurns`



**Definition:** Event Trigger: Applies a status effect after X turns have passed.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `stacks` | Number | Number of stacks or intensity to apply. | 4 |

</details>

---

### Object: `StatusEachTurnBeginIfHasStatus`



**Definition:** Event Trigger: Applies a status at the start of the turn if a prerequisite status is met.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |
| `consume` | Boolean |  | 2 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StatusEachTurnEndForEachTurn`



**Definition:** Event Trigger: Applies nested statuses to each turn end for each turn.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StacyMutant_Mirror`](./Characters_and_Bosses.md#object-stacymutant_mirror)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StatusEachTurnEndIfEnabledAtStartOfTurn`



**Definition:** Event Trigger: Applies a status at the end of the turn if an enabling condition was met at the start.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StatusOnDie`



**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StatusOnEndMove`



**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnEnemyConfused`



**Definition:** Event Trigger: Applies statuses when an enemy becomes confused.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnGainCoins`



**Definition:** Event Trigger: Applies nested statuses when gain coins.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StatusOverlappingCharactersAndDie`



**Definition:** Event Trigger: Applies statuses to overlapping entities, then destroys self.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `StatusWhenStatusCompletelyRemoved`



**Definition:** Event Trigger: Applies statuses when a tracked status effect is fully cleansed.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 2 |

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
| [`keyword_tooltips`](./Characters_and_Bosses.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Object: `SupportDieInsteadOfRun`



**Definition:** AI Logic: Forces a support unit to die rather than flee.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alt_dead_ani`](./Enums.md#enum-alt_dead_ani) | Enum |  | 2 |
| [`alt_dying_ani`](./Enums.md#enum-alt_dying_ani) | Enum |  | 2 |

</details>

---

### Object: `SwimmingFormChange`



**Definition:** Logic: Automates form change when entering/exiting water.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_in`](./Enums.md#enum-form_in) | Enum |  | 2 |
| [`form_out`](./Enums.md#enum-form_out) | Enum |  | 2 |

</details>

---

### Object: `SwitchMusic`





**Definition:** Changes the background music track or layer during combat.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossBecomeTheChild`](./Characters_and_Bosses.md#object-finalbossbecomethechild)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | The specific audio layer to transition to (e.g., map, battle). | 14 |
| [`new_song`](./Enums.md#enum-new_song) | Enum | The ID of the new music track. | 12 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |

</details>

---

### Object: `SyncFormsWithBuddy`



**Definition:** Logic: Forces this character's form to match their familiar/buddy.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`no_buddy`](./Enums.md#enum-no_buddy) | Enum |  | 2 |

</details>

---

### Object: `T3HitlerSpawningPhase`



**Definition:** Boss Logic: Minion spawn phase for the T3 Hitler boss.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 2 |

</details>

---

### Object: `TVBotScreen`



**Definition:** Visual: TV Bot screen state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `Dumb` | Number | AI Profile: A simplified, less optimal decision-making profile. | 2 |
| `Fuck` | Number | Applies or references the 'Fuck' effect/state. | 2 |
| `Obey` | Number | AI State: Enforced compliance logic (e.g., when Charmed). | 2 |
| `Shit` | Number | Applies or references the 'Shit' effect/state. | 2 |
| `Stop` | Number | AI Movement: Forces the character to cease movement. | 2 |
| `Die` | `Number` | Character Form / Logic: Forces the character to die. | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |

</details>

---

### Object: `Terminator2Run`



**Definition:** AI Movement: Specific run logic for Terminator2.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Object: `TerminatorChase`



**Definition:** AI Movement: Specific chase logic for Terminator.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |

</details>

---

### Object: `TerminatorSkin`



**Definition:** Visual: Skin definition for Terminator.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`groups`](./Arrays.md#array-groups) | Array |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

---

### Object: `TransformOnStatusThreshold`



**Definition:** Logic: Changes form when a status effect reaches a certain stack count.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |

</details>

---

### Object: `TwisterFling`



**Definition:** Logic: Fling behavior for tornado attacks.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 2 |
| `max_dist` | Number |  | 2 |
| `min_dist` | Number |  | 2 |

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
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Object: `UnlimitedDeathRattleRevive`



**Definition:** Logic: Endless resurrection on death.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| `even_if_stunned` | Boolean |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 2 |

</details>

---

### Object: `UseAbility`



**Definition:** Forces the character or target to instantly use a specified ability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusWhenStatusCompletelyRemoved`](./Characters_and_Bosses.md#object-statuswhenstatuscompletelyremoved)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger. | 4 |
| `respect_prime` | Boolean | If true, respects the ability's prime/cooldown state. | 4 |

</details>

---

### Object: `UseAbilityWhenOutOfStatus`



**Definition:** Logic: Casts a specific ability the moment a status effect expires.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 2 |

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
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 2 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |

</details>

---

### Object: `Water`




**Definition:** Character Form: Behavior and stats for the \'Water\' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 2 |

</details>

---

### Object: `WereMan`




**Definition:** Character Form: Behavior and stats for the \'WereMan\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |

</details>

---

### Object: `Zealot`




**Definition:** Character Form: Behavior and stats for the \'Zealot\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`ai`](./Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 2 |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

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
| [`brain`](./Enums.md#enum-brain) | Enum |  | 2 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |
| [`pattern`](./Characters_and_Bosses.md#object-pattern) | Object | AI sequence logic. | 2 |

</details>

---

### Object: `damage_instance`



**Definition:** Object defining the combat math and status effects applied upon successful hit.  
**Total Count:** 2346


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`effects`](./Characters_and_Bosses.md#object-effects) | Object | Non-damaging impact triggers. | 3574 |

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
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 2 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| `damage` | Number | The base damage properties of an attack. | 2 |
| `cant_miss` | `Boolean` |  | 2 |
| [`effects`](./Characters_and_Bosses.md#object-effects) | Object | Non-damaging impact triggers. | 2 |
| `makes_contact` | `Boolean` |  | 2 |
| `piercing` | `Boolean` |  | 2 |

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
| [`Default`](./Enums.md#enum-default) | Enum | Character Form: The baseline default behavior state. | 2 |

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
| [`Boris`](./Enums.md#enum-boris) | Enum | Character Form / AI State: Behavior and stats for the 'Boris' state. | 2 |
| [`Explosive`](./Enums.md#enum-explosive) | Enum | Character Form: Behavior and stats for the 'Explosive' state. | 2 |
| [`Holy`](./Enums.md#enum-holy) | Enum | Character Form: Behavior and stats for the 'Holy' state. | 2 |

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


<details>
<summary><b>AddStatusToReceivedDamage</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

<details>
<summary><b>AddStatusToSpells</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

<details>
<summary><b>AddStatusToTrampleDamage</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

<details>
<summary><b>PassiveWhenDead</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 |

</details>

<details>
<summary><b>StatusOnEnemyConfused</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

<details>
<summary><b>StatusOnSpawnIn</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>
