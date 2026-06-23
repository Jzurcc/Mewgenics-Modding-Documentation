# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Characters & Bosses

> **Associated Files:** `data/characters/`


### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 600

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`properties`](./Characters_and_Bosses.md#context-properties) | Block | {'type': '`Block`', 'df': 'General engine properties. | 600 |
| [`graphics`](./Characters_and_Bosses.md#context-graphics) | Block | {'type': '`Block`', 'df': 'Visual parameters and animation bindings. | 558 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1549 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 464 |
| [`abilities`](./Characters_and_Bosses.md#context-abilities) | Block | {'type': '`Block`', 'df': 'Lists the ability IDs the character possesses. | 458 |
| [`stats`](./Characters_and_Bosses.md#context-stats) | Block | {'type': '`Block`', 'df': 'Core character metrics (Health, Strength, etc.). | 388 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum | {'type': '`Enum/String`', 'df': ''} | 240 |
| [`sound`](./Characters_and_Bosses.md#context-sound) | Block | {'type': '`Block`', 'df': "Audio bindings. | 62 |
| [`equipment`](./Characters_and_Bosses.md#context-equipment) | Block | {'type': '`Block`', 'df': 'List of item IDs the character spawns equipped with. | 44 |
| [`alt_spawn_pool`](./Characters_and_Bosses.md#context-alt_spawn_pool) | Block | {'type': '`Block`', 'df': "Alternative pools to draw minions from. | 18 |
| [`brain`](./Enums.md#enum-brain) | Enum | {'type': 'Enum/String', 'df': ''} | 5 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | {'type': 'Enum/String', 'df': ''} | 5 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': 'Enum/String', 'df': ''} | 5 |
| `animation_suffix` | Number | Examples: `3, 4, 2` | 3 |
| `initial_form` | Number | Examples: `1, 5, 0` | 3 |
| `partial_animation_suffix` | Number | Examples: `3, 2, 1` | 3 |
| [`pattern`](./Characters_and_Bosses.md#context-pattern) | Block | {'type': 'Block', 'df': 'AI sequence logic.'} | 3 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': 'Enum/String', 'df': ''} | 2 |
| `end_turn_on_formswitch` | Boolean | {'type': 'Boolean', 'df': ''} | 2 |
| [`ai_if_spawned_as_enemy`](./Characters_and_Bosses.md#context-ai_if_spawned_as_enemy) | Block | {'type': '`Block`', 'df': 'AI logic override used only if the character is spawned as an enemy. | 1 |
| `consider_spells` | Boolean | {'type': 'Boolean', 'df': ''} | 1 |
| [`damage_instance`](./Characters_and_Bosses.md#context-damage_instance) | Block | {'type': '`Block`', 'df': 'Defines damage logic on contact. | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4118 |

</details>

---

### Context: `passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 733

> **Referenced by:** [`Alert`](./Characters_and_Bosses.md#context-alert), [`AllAlive`](./Characters_and_Bosses.md#context-allalive), [`BellyFull`](./Characters_and_Bosses.md#context-bellyfull), [`Big`](./Characters_and_Bosses.md#context-big), [`BigHolding`](./Characters_and_Bosses.md#context-bigholding), [`BigHoldingCat`](./Characters_and_Bosses.md#context-bigholdingcat), [`Bishop`](./Characters_and_Bosses.md#context-bishop), [`BlackHole`](./Characters_and_Bosses.md#context-blackhole), [`Bomb`](./Characters_and_Bosses.md#context-bomb), [`Boris`](./Characters_and_Bosses.md#context-boris), [`Bully`](./Characters_and_Bosses.md#context-bully), [`CaveBaby`](./Characters_and_Bosses.md#context-cavebaby), [`CaveMan`](./Characters_and_Bosses.md#context-caveman), [`CaveManSpear`](./Characters_and_Bosses.md#context-cavemanspear), [`CaveWoman`](./Characters_and_Bosses.md#context-cavewoman), [`CaveWomanHasCat`](./Characters_and_Bosses.md#context-cavewomanhascat), [`Charging`](./Characters_and_Bosses.md#context-charging), [`Close`](./Characters_and_Bosses.md#context-close), [`Cultist`](./Characters_and_Bosses.md#context-cultist), [`Default`](./Characters_and_Bosses.md#context-default), and 97 more...

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2609 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Examples: `{ ... }` | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': 'Enum/String', 'df': ''} | 2 |
| `partial_animation_suffix` | Number | Examples: `4, 2` | 2 |
| `animation_suffix` | Number | Examples: `1` | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 166 |

</details>

---

### Context: `properties`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 600

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum | {'type': '`Enum/String`', 'df': ''} | 505 |
| `health` | Number | {'type': '`Number`', 'df': ''} | 427 |
| [`tag`](./Arrays.md#array-tag) | Array | {'type': '`Array`', 'df': 'Specific entity tag required.'} | 399 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'Classification/category type.'} | 280 |
| `movement` | Number | {'type': '`Number`', 'df': ''} | 278 |
| `corpse_health` | Mixed | {'type': '`Enum/String`', 'df': ''} | 195 |
| `inherit_faction` | Boolean | {'type': '`Boolean`', 'df': ''} | 115 |
| `dispersed_bonus_turns` | Number | {'type': '`Number`', 'df': ''} | 104 |
| `base_mana_regen` | Number | {'type': '`Number`', 'df': ''} | 90 |
| [`size`](./Enums.md#enum-size) | Enum | {'type': '`Enum/String`', 'df': ''} | 80 |
| `shield` | Number | {'type': '`Number`', 'df': ''} | 74 |
| [`move_block`](./Enums.md#enum-move_block) | Enum | {'type': '`Enum/String`', 'df': ''} | 73 |
| `kill_required` | Boolean | {'type': '`Boolean`', 'df': ''} | 69 |
| `can_be_backstabbed` | Boolean | {'type': '`Boolean`', 'df': ''} | 68 |
| `initiative` | Number | {'type': '`Number`', 'df': ''} | 61 |
| `takes_turns` | Boolean | {'type': '`Boolean`', 'df': ''} | 61 |
| `mana_regen` | Number | {'type': '`Number`', 'df': ''} | 51 |
| `mana` | Number | {'type': '`Number`', 'df': 'Base maximum mana pool.'} | 50 |
| `flying` | Boolean | {'type': '`Boolean`', 'df': ''} | 47 |
| [`banned_elite_buffs`](./Arrays.md#array-banned_elite_buffs) | Array | {'type': '`Array`', 'df': ''} | 45 |
| [`hidden_tag`](./Arrays.md#array-hidden_tag) | Array | {'type': '`Enum/String`', 'df': ''} | 38 |
| `weak_threshold` | Number | {'type': '`Number`', 'df': ''} | 32 |
| `knockback_immune` | Boolean | {'type': '`Boolean`', 'df': ''} | 25 |
| `can_be_champion` | Boolean | {'type': '`Boolean`', 'df': ''} | 20 |
| [`lock_orientation`](./Arrays.md#array-lock_orientation) | Array | {'type': '`Array`', 'df': ''} | 19 |
| [`ai_scale`](./Enums.md#enum-ai_scale) | Enum | {'type': '`Enum/String`', 'df': ''} | 18 |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 539 |
| [`auto_run_priority`](./Enums.md#enum-auto_run_priority) | Enum | {'type': '`Enum/String`', 'df': ''} | 16 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 16 |
| `inanimate` | Boolean | {'type': '`Boolean`', 'df': ''} | 16 |
| `disperse_main_turns` | Boolean | {'type': '`Boolean`', 'df': ''} | 15 |
| [`hidden_tags`](./Arrays.md#array-hidden_tags) | Array | {'type': '`Enum/String`', 'df': ''} | 14 |
| [`tags`](./Arrays.md#array-tags) | Array | {'type': '`Array`', 'df': ''} | 14 |
| `evenly_dispersed_bonus_turns` | Number | {'type': '`Number`', 'df': ''} | 13 |
| `exclude_from_hallucinate` | Boolean | {'type': '`Boolean`', 'df': ''} | 13 |
| `round_end_bonus_turns` | Number | {'type': '`Number`', 'df': ''} | 13 |
| `can_be_overkilled` | Boolean | {'type': '`Boolean`', 'df': ''} | 12 |
| `can_collect_coins` | Boolean | {'type': '`Boolean`', 'df': ''} | 10 |
| `deathpoof_size` | Number | {'type': '`Number`', 'df': ''} | 10 |
| `dispersed_bonus_turns_consider_initiative` | Boolean | {'type': '`Boolean`', 'df': ''} | 10 |
| [`held_coins`](./Arrays.md#array-held_coins) | Array | {'type': '`Number`', 'df': ''} | 10 |
| `initial_health` | Number | {'type': '`Number`', 'df': ''} | 10 |
| `can_eat_food` | Boolean | {'type': '`Boolean`', 'df': ''} | 9 |
| `can_grant_extra_turns` | Boolean | {'type': '`Boolean`', 'df': ''} | 8 |
| `tall` | Boolean | {'type': '`Boolean`', 'df': ''} | 8 |
| `dispersed_bonus_turns_before_cats` | Boolean | {'type': '`Boolean`', 'df': ''} | 7 |
| `divine_shield` | Number | {'type': '`Number`', 'df': ''} | 7 |
| `is_player_cat` | Boolean | {'type': '`Boolean`', 'df': ''} | 7 |
| `boss_minions_runaway` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |
| `mana_matters` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |
| `access_to_player_inventory` | Boolean | {'type': '`Boolean`', 'df': ''} | 5 |
| `act_points` | Number | {'type': '`Number`', 'df': ''} | 5 |
| `takes_main_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 5 |
| `visually_spiky` | Boolean | {'type': '`Boolean`', 'df': ''} | 5 |
| `allow_passive_spelltransforming` | Boolean | {'type': '`Boolean`', 'df': ''} | 4 |
| `base_crit_chance` | Number | {'type': '`Number`', 'df': ''} | 4 |
| `last_turn_is_main_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 4 |
| `round_start_bonus_turns` | Number | {'type': '`Number`', 'df': ''} | 4 |
| `view_bleeding_characters_as_enemies` | Boolean | {'type': '`Boolean`', 'df': ''} | 4 |
| [`aoe_pierce_mode`](./Enums.md#enum-aoe_pierce_mode) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| `base_initiative` | Number | {'type': '`Number`', 'df': ''} | 3 |
| `base_movement` | Number | {'type': '`Number`', 'df': ''} | 3 |
| `catdata_ignore_skills` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| [`disallow_items`](./Enums.md#enum-disallow_items) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| `always_triggers_traps` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `base_health` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `base_health_regen` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `base_initial_mana` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `base_mana` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `blocking` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `can_be_elite` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `can_run` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `champion` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `force_not_familiar` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `hint_no_corpse` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `must_start_facing_camera` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `tile_desire_cost` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `uncapturable` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `aggro_target_is_enemy` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `allow_flying_effect` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `allow_offmap_corpse` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `allow_replacebrain` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `always_face_forward` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `capture_as_cat` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `elite` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `first_turn_is_main_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `ignore_mouseover` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `ignore_tiles` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`inanimate_can_receive_specific_statuses`](./Arrays.md#array-inanimate_can_receive_specific_statuses) | Array | {'type': '`Array`', 'df': ''} | 1 |
| `mouseover_priority` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `move_points` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `pickup_type` | Number | {'type': '`Number`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 155 |
| `speculative_inanimate` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `static` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `two_fronts` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `two_fronts_switch` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `view_bugs_as_enemies` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `ai`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 583

> **Referenced by:** [`Alert`](./Characters_and_Bosses.md#context-alert), [`Angry`](./Characters_and_Bosses.md#context-angry), [`Attacker`](./Characters_and_Bosses.md#context-attacker), [`BellyFull`](./Characters_and_Bosses.md#context-bellyfull), [`Bishop`](./Characters_and_Bosses.md#context-bishop), [`BlackHole`](./Characters_and_Bosses.md#context-blackhole), [`Bully`](./Characters_and_Bosses.md#context-bully), [`CaveBaby`](./Characters_and_Bosses.md#context-cavebaby), [`CaveMan`](./Characters_and_Bosses.md#context-caveman), [`CaveManSpear`](./Characters_and_Bosses.md#context-cavemanspear), [`CaveWoman`](./Characters_and_Bosses.md#context-cavewoman), [`CaveWomanHasCat`](./Characters_and_Bosses.md#context-cavewomanhascat), [`Charging`](./Characters_and_Bosses.md#context-charging), [`Cultist`](./Characters_and_Bosses.md#context-cultist), [`Damaged`](./Characters_and_Bosses.md#context-damaged), [`Default`](./Characters_and_Bosses.md#context-default), [`Default_Ceiling`](./Characters_and_Bosses.md#context-default_ceiling), [`Default_Ground`](./Characters_and_Bosses.md#context-default_ground), [`DesireMech`](./Characters_and_Bosses.md#context-desiremech), [`Down`](./Characters_and_Bosses.md#context-down), and 64 more...

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum | {'type': '`Enum/String`', 'df': ''} | 573 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 493 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 490 |
| [`pattern`](./Characters_and_Bosses.md#context-pattern) | Block | {'type': '`Block`', 'df': 'AI sequence logic. | 289 |
| [`mainturn_pattern`](./Characters_and_Bosses.md#context-mainturn_pattern) | Block | {'type': '`Block`', 'df': 'AI Logic: Determines standard ability usage during the main turn. | 44 |
| `end_turn_on_formswitch` | Boolean | {'type': '`Boolean`', 'df': ''} | 39 |
| [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities) | Block | {'type': '`Block`', 'df': "Abilities that are evaluated but not directly castable by the player. | 35 |
| `auto_orient` | Boolean | {'type': '`Boolean`', 'df': ''} | 31 |
| `reset_pattern_on_formswitch` | Boolean | {'type': '`Boolean`', 'df': ''} | 31 |
| `stun_advances_pattern` | Boolean | {'type': '`Boolean`', 'df': ''} | 30 |
| `fallback_advances_pattern` | Boolean | {'type': '`Boolean`', 'df': ''} | 28 |
| [`bonusturn_pattern`](./Characters_and_Bosses.md#context-bonusturn_pattern) | Block | {'type': '`Block`', 'df': 'AI Logic: Determines ability usage during bonus turns. | 27 |
| [`fallback`](./Characters_and_Bosses.md#context-fallback) | Block | {'type': '`Block`', 'df': 'Logic executed if primary options fail. | 23 |
| [`round_end_bonusturn_pattern`](./Characters_and_Bosses.md#context-round_end_bonusturn_pattern) | Block | {'type': '`Block`', 'df': 'AI Logic: Ability usage pattern during round-end bonus turns. | 12 |
| `consider_spells` | Boolean | {'type': '`Boolean`', 'df': ''} | 11 |
| `animate_choice` | Boolean | {'type': '`Boolean`', 'df': ''} | 8 |
| `clamp_pattern` | Boolean | {'type': '`Boolean`', 'df': ''} | 5 |
| `randomize_pattern_start` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| [`dispersed_bonusturn_pattern`](./Characters_and_Bosses.md#context-dispersed_bonusturn_pattern) | Block | {'type': '`Block`', 'df': 'AI Logic: Alternative bonus turn ability pattern. | 2 |
| `random_orient` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`dice_abilities`](./Arrays.md#array-dice_abilities) | Array | {'type': '`Array`', 'df': ''} | 1 |
| `never_hit_ally_corpses` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`post_absorb_move_weights`](./Enums.md#enum-post_absorb_move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `reset_pattern_on_round_begin` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`roll_ability`](./Enums.md#enum-roll_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`round_start_bonusturn_pattern`](./Characters_and_Bosses.md#context-round_start_bonusturn_pattern) | Block | {'type': '`Block`', 'df': 'AI Logic: Ability usage pattern during round-start bonus turns. | 1 |

</details>

---

### Context: `graphics`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 558

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2458 |

</details>

---

### Context: `abilities`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 458

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 436 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 433 |
| [`spells`](./Arrays.md#array-spells) | Array | {'type': '`Array`', 'df': ''} | 381 |
| `can_get_bonus` | Boolean | {'type': '`Boolean`', 'df': ''} | 30 |
| `BoneWormShotSmall` | Flag |  | 1 |

</details>

---

### Context: `stats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 388

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `strength` | Number | {'type': '`Number`', 'df': ''} | 386 |
| `constitution` | Number | {'type': '`Number`', 'df': ''} | 380 |
| `dexterity` | Number | {'type': '`Number`', 'df': ''} | 380 |
| `charisma` | Number | {'type': '`Number`', 'df': ''} | 379 |
| `intelligence` | Number | {'type': '`Number`', 'df': ''} | 379 |
| `speed` | Number | {'type': '`Number`', 'df': 'Base speed/initiative stat.'} | 379 |
| `luck` | Number | {'type': '`Number`', 'df': ''} | 160 |

</details>

---

### Context: `pattern`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 296

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root), [`ReplaceBrain`](./Characters_and_Bosses.md#context-replacebrain), [`ai`](./Characters_and_Bosses.md#context-ai), [`ai_if_spawned_as_enemy`](./Characters_and_Bosses.md#context-ai_if_spawned_as_enemy)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum | {'type': '`Enum/String`', 'df': ''} | 128 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array | {'type': '`Array`', 'df': ''} | 106 |
| [`do_all`](./Arrays.md#array-do_all) | Array | {'type': '`Array`', 'df': ''} | 101 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum | {'type': '`Enum/String`', 'df': ''} | 11 |
| [`do_random`](./Arrays.md#array-do_random) | Array | {'type': '`Array`', 'df': ''} | 10 |
| [`do_strict`](./Arrays.md#array-do_strict) | Array | {'type': '`Array`', 'df': ''} | 6 |
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array | {'type': '`Array`', 'df': ''} | 3 |
| [`move_then_do_priority`](./Arrays.md#array-move_then_do_priority) | Array | {'type': '`Array`', 'df': ''} | 3 |
| [`move_then_do_random`](./Arrays.md#array-move_then_do_random) | Array | {'type': '`Array`', 'df': ''} | 3 |
| [`do_all_shuffle`](./Arrays.md#array-do_all_shuffle) | Array | {'type': '`Array`', 'df': ''} | 2 |
| [`do_best`](./Arrays.md#array-do_best) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`do_best_multiple`](./Arrays.md#array-do_best_multiple) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`do_priority_alternating`](./Arrays.md#array-do_priority_alternating) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`move_then_do_all`](./Arrays.md#array-move_then_do_all) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

### Context: `FormChanger`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 106

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`initial_form`](./Enums.md#enum-initial_form) | Enum | {'type': '`Enum/String`', 'df': ''} | 56 |
| [`Default`](./Characters_and_Bosses.md#context-default) | Block | {'type': '`Block`', 'df': 'Character Form: The baseline default behavior state. | 37 |
| [`Normal`](./Characters_and_Bosses.md#context-normal) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Normal\' state. | 11 |
| [`Rage`](./Characters_and_Bosses.md#context-rage) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Rage\' state. | 10 |
| [`HasCat`](./Characters_and_Bosses.md#context-hascat) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'HasCat\' state. | 5 |
| [`OffMap`](./Characters_and_Bosses.md#context-offmap) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'OffMap' state. | 4 |
| [`default`](./Characters_and_Bosses.md#context-default) | Block | {'type': '`Block`', 'df': 'Baseline configuration. | 4 |
| [`hot`](./Characters_and_Bosses.md#context-hot) | Block | {'type': '`Block`', 'df': 'Visual effect indicator. | 4 |
| [`AllAlive`](./Characters_and_Bosses.md#context-allalive) | Block | {'type': '`Block`', 'df': 'Encounter State: Logic executed when all specific entities are currently alive. | 3 |
| [`Down`](./Characters_and_Bosses.md#context-down) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Down\' state. | 3 |
| [`Full`](./Characters_and_Bosses.md#context-full) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Full\' state. | 3 |
| [`OneAlive`](./Characters_and_Bosses.md#context-onealive) | Block | {'type': '`Block`', 'df': 'Encounter State: Logic executed when exactly one target is alive. | 3 |
| [`TwoAlive`](./Characters_and_Bosses.md#context-twoalive) | Block | {'type': '`Block`', 'df': 'Encounter State: Logic executed when exactly two targets are alive. | 3 |
| [`Up`](./Characters_and_Bosses.md#context-up) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Up\' state. | 3 |
| [`Big`](./Characters_and_Bosses.md#context-big) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior and stats for the \'Big\' state. | 2 |
| [`Boris`](./Characters_and_Bosses.md#context-boris) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior and stats for the \'Boris\' state. | 2 |
| [`CaveMan`](./Characters_and_Bosses.md#context-caveman) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'CaveMan\' state. | 2 |
| [`CaveManSpear`](./Characters_and_Bosses.md#context-cavemanspear) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'CaveManSpear\' state. | 2 |
| [`Empty`](./Characters_and_Bosses.md#context-empty) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Empty\' state. | 2 |
| [`Explosive`](./Characters_and_Bosses.md#context-explosive) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Explosive\' state. | 2 |
| [`Holding`](./Characters_and_Bosses.md#context-holding) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Holding\' state. | 2 |
| [`Holy`](./Characters_and_Bosses.md#context-holy) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Holy\' state. | 2 |
| [`NotPriming`](./Characters_and_Bosses.md#context-notpriming) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats when not charging an ability. | 2 |
| [`Priming`](./Characters_and_Bosses.md#context-priming) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats when charging an ability. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`Small`](./Characters_and_Bosses.md#context-small) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Small\' state. | 2 |
| [`SquirrelForm`](./Characters_and_Bosses.md#context-squirrelform) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'SquirrelForm' state. | 2 |
| [`Turtled`](./Characters_and_Bosses.md#context-turtled) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Turtled' state. | 2 |
| [`active`](./Characters_and_Bosses.md#context-active) | Block | {'type': '`Block`', 'df': 'Defines actively executed abilities. | 2 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': 'Block', 'df': 'Core block defining the AI behavior logic and weights.'} | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': 'Enum/String', 'df': ''} | 2 |
| `partial_animation_suffix` | Number | {'type': 'String', 'df': ''} | 2 |
| [`passive`](./Characters_and_Bosses.md#context-passive) | Block | {'type': '`Block`', 'df': 'Intrinsic passive modifier. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 120 |
| [`Alert`](./Characters_and_Bosses.md#context-alert) | Block | {'type': '`Block`', 'df': 'AI State: The behavior profile used when the character is alerted to enemies. | 1 |
| [`Angry`](./Characters_and_Bosses.md#context-angry) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior and stats for the \'Angry\' state. | 1 |
| [`Attacker`](./Characters_and_Bosses.md#context-attacker) | Block | {'type': '`Block`', 'df': 'AI Role: Designates the character as an attacker rather than support. | 1 |
| [`BellyFull`](./Characters_and_Bosses.md#context-bellyfull) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior and stats for the \'BellyFull\' state. | 1 |
| [`BigHolding`](./Characters_and_Bosses.md#context-bigholding) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior and stats for the \'BigHolding\' state. | 1 |
| [`BigHoldingCat`](./Characters_and_Bosses.md#context-bigholdingcat) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior and stats for the \'BigHoldingCat\' state. | 1 |
| [`Bishop`](./Characters_and_Bosses.md#context-bishop) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior and stats for the \'Bishop\' state. | 1 |
| [`BlackHole`](./Characters_and_Bosses.md#context-blackhole) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior and stats for the \'BlackHole\' state. | 1 |
| [`Bomb`](./Characters_and_Bosses.md#context-bomb) | Block | {'type': '`Block`', 'df': "Character Form / AI State: Behavior and stats for the 'Bomb' state. | 1 |
| [`Bully`](./Characters_and_Bosses.md#context-bully) | Block | {'type': '`Block`', 'df': "Character Form / AI State: Behavior and stats for the 'Bully' state. | 1 |
| `Butcher` | Block | {'type': '`Block`', 'df': "Applies or references the 'Butcher' effect/state."} | 1 |
| [`CaveBaby`](./Characters_and_Bosses.md#context-cavebaby) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'CaveBaby\' state. | 1 |
| [`CaveWoman`](./Characters_and_Bosses.md#context-cavewoman) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'CaveWoman\' state. | 1 |
| [`CaveWomanHasCat`](./Characters_and_Bosses.md#context-cavewomanhascat) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'CaveWomanHasCat\' state. | 1 |
| [`Charging`](./Characters_and_Bosses.md#context-charging) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior when charging an attack. | 1 |
| [`Close`](./Characters_and_Bosses.md#context-close) | Block | {'type': '`Block`', 'df': 'AI Movement logic: Maneuvers into close/melee range. | 1 |
| `Colorless` | Block | {'type': '`Block`', 'df': "Applies or references the 'Colorless' effect/state."} | 1 |
| [`Cultist`](./Characters_and_Bosses.md#context-cultist) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Cultist\' state. | 1 |
| [`Damaged`](./Characters_and_Bosses.md#context-damaged) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior when health is critically low. | 1 |
| [`Default_Ceiling`](./Characters_and_Bosses.md#context-default_ceiling) | Block | {'type': '`Block`', 'df': 'Character Form: The baseline behavior state while attached to the ceiling. | 1 |
| [`Default_Ground`](./Characters_and_Bosses.md#context-default_ground) | Block | {'type': '`Block`', 'df': 'Character Form: The baseline behavior state while on the ground. | 1 |
| [`DesireMech`](./Characters_and_Bosses.md#context-desiremech) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'DesireMech' state. | 1 |
| `Druid` | Block | {'type': '`Block`', 'df': "Applies or references the 'Druid' effect/state."} | 1 |
| [`Drunker`](./Characters_and_Bosses.md#context-drunker) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Drunker' state. | 1 |
| [`DualSword`](./Characters_and_Bosses.md#context-dualsword) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'DualSword\' state. | 1 |
| [`DualSword_Primed`](./Characters_and_Bosses.md#context-dualsword_primed) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'DualSword_Primed\' state. | 1 |
| [`Dumb`](./Characters_and_Bosses.md#context-dumb) | Block | {'type': '`Block`', 'df': 'AI Profile: A simplified, less optimal decision-making profile. | 1 |
| [`Explody`](./Characters_and_Bosses.md#context-explody) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Explody' state. | 1 |
| [`FightPhase`](./Characters_and_Bosses.md#context-fightphase) | Block | {'type': '`Block`', 'df': 'Boss Logic: Main combat phase. | 1 |
| `Fighter` | Block | {'type': '`Block`', 'df': "Applies or references the 'Fighter' effect/state."} | 1 |
| [`Fire`](./Characters_and_Bosses.md#context-fire) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Fire' state. | 1 |
| [`FireFull`](./Characters_and_Bosses.md#context-firefull) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'FireFull' state. | 1 |
| [`Flop`](./Characters_and_Bosses.md#context-flop) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Flop\' state. | 1 |
| [`Flop2`](./Characters_and_Bosses.md#context-flop2) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Flop2\' state. | 1 |
| [`Flush`](./Characters_and_Bosses.md#context-flush) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Flush' state. | 1 |
| [`FlushBubs`](./Characters_and_Bosses.md#context-flushbubs) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'FlushBubs' state. | 1 |
| [`FlushHost`](./Characters_and_Bosses.md#context-flushhost) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'FlushHost' state. | 1 |
| [`FlushNettle`](./Characters_and_Bosses.md#context-flushnettle) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'FlushNettle' state. | 1 |
| [`Grappling`](./Characters_and_Bosses.md#context-grappling) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior while grappling an opponent. | 1 |
| [`Grown`](./Characters_and_Bosses.md#context-grown) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Grown\' state. | 1 |
| [`GuaranteedJackpot`](./Characters_and_Bosses.md#context-guaranteedjackpot) | Block | {'type': '`Block`', 'df': 'Loot Logic: Guarantees a high-tier drop. | 1 |
| [`Guarding`](./Characters_and_Bosses.md#context-guarding) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Defensive behavior state. | 1 |
| [`HalfDead`](./Characters_and_Bosses.md#context-halfdead) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'HalfDead\' state. | 1 |
| [`HasDeadCat`](./Characters_and_Bosses.md#context-hasdeadcat) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'HasDeadCat\' state. | 1 |
| [`HasRock`](./Characters_and_Bosses.md#context-hasrock) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'HasRock\' state. | 1 |
| [`Headless`](./Characters_and_Bosses.md#context-headless) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Headless\' state. | 1 |
| [`Hint_CrackedVisuals`](./Characters_and_Bosses.md#context-hint_crackedvisuals) | Block | {'type': '`Block`', 'df': 'Visual: Overlay effects for cracked/damaged terrain or objects. | 1 |
| [`Hint_CrackedVisuals2`](./Characters_and_Bosses.md#context-hint_crackedvisuals2) | Block | {'type': '`Block`', 'df': 'Visual: Secondary cracked visual overlay. | 1 |
| [`Hint_CrackedVisuals3`](./Characters_and_Bosses.md#context-hint_crackedvisuals3) | Block | {'type': '`Block`', 'df': 'Visual: Tertiary cracked visual overlay. | 1 |
| [`HumanDead`](./Characters_and_Bosses.md#context-humandead) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'HumanDead\' state. | 1 |
| `Hunter` | Block | {'type': '`Block`', 'df': "Applies or references the 'Hunter' effect/state."} | 1 |
| [`InitialPhase`](./Characters_and_Bosses.md#context-initialphase) | Block | {'type': '`Block`', 'df': 'Boss Logic: The starting phase of an encounter. | 1 |
| [`Insane_Ceiling`](./Characters_and_Bosses.md#context-insane_ceiling) | Block | {'type': '`Block`', 'df': 'Character Form: Insane behavior state while attached to the ceiling. | 1 |
| [`Insane_Ground`](./Characters_and_Bosses.md#context-insane_ground) | Block | {'type': '`Block`', 'df': 'Character Form: Insane behavior state while on the ground. | 1 |
| [`Johnny`](./Characters_and_Bosses.md#context-johnny) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Johnny' state. | 1 |
| [`JohnnyBubs`](./Characters_and_Bosses.md#context-johnnybubs) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'JohnnyBubs' state. | 1 |
| [`JohnnyHost`](./Characters_and_Bosses.md#context-johnnyhost) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'JohnnyHost' state. | 1 |
| [`JohnnyNettle`](./Characters_and_Bosses.md#context-johnnynettle) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'JohnnyNettle' state. | 1 |
| [`Joystick`](./Characters_and_Bosses.md#context-joystick) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Joystick\' state. | 1 |
| [`LastHit`](./Characters_and_Bosses.md#context-lasthit) | Block | {'type': '`Block`', 'df': 'Logic: Executes logic on the final hit of a multi-hit attack. | 1 |
| [`Lifted`](./Characters_and_Bosses.md#context-lifted) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Lifted\' state. | 1 |
| [`Lit`](./Characters_and_Bosses.md#context-lit) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Lit' state. | 1 |
| `Mage` | Block | {'type': '`Block`', 'df': "Applies or references the 'Mage' effect/state."} | 1 |
| `Medic` | Block | {'type': '`Block`', 'df': "Applies or references the 'Medic' effect/state."} | 1 |
| `Monk` | Block | {'type': '`Block`', 'df': "Applies or references the 'Monk' effect/state."} | 1 |
| [`Mounted`](./Characters_and_Bosses.md#context-mounted) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Mounted\' state. | 1 |
| [`MouthFull`](./Characters_and_Bosses.md#context-mouthfull) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'MouthFull\' state. | 1 |
| [`Mutant`](./Characters_and_Bosses.md#context-mutant) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Mutant\' state. | 1 |
| `Necromancer` | Block | {'type': '`Block`', 'df': "Applies or references the 'Necromancer' effect/state."} | 1 |
| [`NeutronStar`](./Characters_and_Bosses.md#context-neutronstar) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'NeutronStar' state. | 1 |
| `NoDeathRattle` | Block | {'type': '`Block`', 'df': "Applies or references the 'NoDeathRattle' effect/state."} | 1 |
| [`NoEyes`](./Characters_and_Bosses.md#context-noeyes) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'NoEyes\' state. | 1 |
| [`NoStick`](./Characters_and_Bosses.md#context-nostick) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'NoStick' state. | 1 |
| [`NormalFull`](./Characters_and_Bosses.md#context-normalfull) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'NormalFull' state. | 1 |
| [`Nuke`](./Characters_and_Bosses.md#context-nuke) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Nuke' state. | 1 |
| [`Obey`](./Characters_and_Bosses.md#context-obey) | Block | {'type': '`Block`', 'df': 'AI State: Enforced compliance logic (e.g., when Charmed). | 1 |
| [`Off`](./Characters_and_Bosses.md#context-off) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Off' state. | 1 |
| [`OffScreen`](./Characters_and_Bosses.md#context-offscreen) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'OffScreen' state. | 1 |
| [`OneEye`](./Characters_and_Bosses.md#context-oneeye) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'OneEye\' state. | 1 |
| [`Open`](./Characters_and_Bosses.md#context-open) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Open' state. | 1 |
| [`OpenCat`](./Characters_and_Bosses.md#context-opencat) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'OpenCat' state. | 1 |
| [`Out`](./Characters_and_Bosses.md#context-out) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Out' state. | 1 |
| [`Possessing`](./Characters_and_Bosses.md#context-possessing) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Possessing\' state. | 1 |
| [`Primed`](./Characters_and_Bosses.md#context-primed) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Primed' state. | 1 |
| `Psychic` | Block | {'type': '`Block`', 'df': "Applies or references the 'Psychic' effect/state."} | 1 |
| [`Pulp2`](./Characters_and_Bosses.md#context-pulp2) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Pulp2' state. | 1 |
| [`Pulp3`](./Characters_and_Bosses.md#context-pulp3) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Pulp3' state. | 1 |
| [`Pulp4`](./Characters_and_Bosses.md#context-pulp4) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Pulp4' state. | 1 |
| [`Pulp5`](./Characters_and_Bosses.md#context-pulp5) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Pulp5' state. | 1 |
| [`Pulp6`](./Characters_and_Bosses.md#context-pulp6) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Pulp6' state. | 1 |
| [`Pulp7`](./Characters_and_Bosses.md#context-pulp7) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Pulp7' state. | 1 |
| [`Sitting`](./Characters_and_Bosses.md#context-sitting) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Sitting' state. | 1 |
| [`SmallHolding`](./Characters_and_Bosses.md#context-smallholding) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'SmallHolding\' state. | 1 |
| [`SmallHoldingCat`](./Characters_and_Bosses.md#context-smallholdingcat) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'SmallHoldingCat\' state. | 1 |
| [`SpawningPhase`](./Characters_and_Bosses.md#context-spawningphase) | Block | {'type': '`Block`', 'df': 'Boss Logic: Phase focused on summoning minions. | 1 |
| [`Standing`](./Characters_and_Bosses.md#context-standing) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Standing' state. | 1 |
| [`Standing2`](./Characters_and_Bosses.md#context-standing2) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Standing2' state. | 1 |
| [`Start_Ceiling`](./Characters_and_Bosses.md#context-start_ceiling) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Start_Ceiling' state. | 1 |
| [`Stop`](./Characters_and_Bosses.md#context-stop) | Block | {'type': '`Block`', 'df': 'AI Movement: Forces the character to cease movement. | 1 |
| [`SwordAndShield`](./Characters_and_Bosses.md#context-swordandshield) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'SwordAndShield' state. | 1 |
| [`SwordAndShield_Primed`](./Characters_and_Bosses.md#context-swordandshield_primed) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'SwordAndShield_Primed\' state. | 1 |
| `Tank` | Block | {'type': '`Block`', 'df': "Applies or references the 'Tank' effect/state."} | 1 |
| [`Tar`](./Characters_and_Bosses.md#context-tar) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Tar' state. | 1 |
| [`TarFull`](./Characters_and_Bosses.md#context-tarfull) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'TarFull' state. | 1 |
| `Thief` | Block | {'type': '`Block`', 'df': "Applies or references the 'Thief' effect/state."} | 1 |
| [`Throb`](./Characters_and_Bosses.md#context-throb) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Throb' state. | 1 |
| [`ThrobBubs`](./Characters_and_Bosses.md#context-throbbubs) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'ThrobBubs' state. | 1 |
| [`ThrobHost`](./Characters_and_Bosses.md#context-throbhost) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'ThrobHost' state. | 1 |
| [`ThrobNettle`](./Characters_and_Bosses.md#context-throbnettle) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'ThrobNettle' state. | 1 |
| `Tinkerer` | Block | {'type': '`Block`', 'df': "Applies or references the 'Tinkerer' effect/state."} | 1 |
| [`Transformed`](./Characters_and_Bosses.md#context-transformed) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Transformed' state. | 1 |
| [`TwoEyes`](./Characters_and_Bosses.md#context-twoeyes) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'TwoEyes' state. | 1 |
| [`Unlit`](./Characters_and_Bosses.md#context-unlit) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Unlit' state. | 1 |
| `Unmounted` | Block | {'type': '`Block`', 'df': "Applies or references the 'Unmounted' effect/state."} | 1 |
| [`Unwashed`](./Characters_and_Bosses.md#context-unwashed) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Unwashed' state. | 1 |
| [`Washed`](./Characters_and_Bosses.md#context-washed) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Washed' state. | 1 |
| [`Washer`](./Characters_and_Bosses.md#context-washer) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Washer\' state. | 1 |
| [`Water`](./Characters_and_Bosses.md#context-water) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Water\' state. | 1 |
| [`WereMan`](./Characters_and_Bosses.md#context-wereman) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'WereMan\' state. | 1 |
| [`Zealot`](./Characters_and_Bosses.md#context-zealot) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Zealot\' state. | 1 |
| [`ZealotBomb`](./Characters_and_Bosses.md#context-zealotbomb) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'ZealotBomb\' state. | 1 |
| `sync_brain_patterns` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 76 |

</details>

---

### Context: `SpawnOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 79

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`obj`](./Arrays.md#array-obj) | Array | {'type': '`Array`', 'df': ''} | 3 |
| [`additional_statuses`](./Characters_and_Bosses.md#context-additional_statuses) | Block | {'type': '`Block`', 'df': "Generic statuses added to the character. | 1 |

</details>

---

### Context: `sound`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 62

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alt_sounds`](./Arrays.md#array-alt_sounds) | Array | {'type': '`Array`', 'df': ''} | 61 |
| [`animation_prefix`](./Enums.md#enum-animation_prefix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Robot`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 46

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alternate_energized_effect`](./Characters_and_Bosses.md#context-alternate_energized_effect) | Block | {'type': '`Block`', 'df': "Overrides default energized visuals. | 2 |

</details>

---

### Context: `turns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 45

> **Referenced by:** [`Bishop`](./Characters_and_Bosses.md#context-bishop), [`Bully`](./Characters_and_Bosses.md#context-bully), [`Default`](./Characters_and_Bosses.md#context-default), [`Default_Ceiling`](./Characters_and_Bosses.md#context-default_ceiling), [`Default_Ground`](./Characters_and_Bosses.md#context-default_ground), [`FightPhase`](./Characters_and_Bosses.md#context-fightphase), [`Holding`](./Characters_and_Bosses.md#context-holding), [`InitialPhase`](./Characters_and_Bosses.md#context-initialphase), [`Insane_Ceiling`](./Characters_and_Bosses.md#context-insane_ceiling), [`Insane_Ground`](./Characters_and_Bosses.md#context-insane_ground), [`LastHit`](./Characters_and_Bosses.md#context-lasthit), [`Lifted`](./Characters_and_Bosses.md#context-lifted), [`Mutant`](./Characters_and_Bosses.md#context-mutant), [`Normal`](./Characters_and_Bosses.md#context-normal), [`NotPriming`](./Characters_and_Bosses.md#context-notpriming), [`Nuke`](./Characters_and_Bosses.md#context-nuke), [`OffMap`](./Characters_and_Bosses.md#context-offmap), [`OffScreen`](./Characters_and_Bosses.md#context-offscreen), [`OneAlive`](./Characters_and_Bosses.md#context-onealive), [`Possessing`](./Characters_and_Bosses.md#context-possessing), and 13 more...

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `takes_turns` | Boolean | {'type': '`Boolean`', 'df': ''} | 23 |
| `dispersed_bonus_turns` | Number | {'type': '`Number`', 'df': ''} | 18 |
| `takes_main_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 10 |
| `evenly_dispersed_bonus_turns` | Number | {'type': '`Number`', 'df': ''} | 7 |
| `round_end_bonus_turns` | Number | {'type': '`Number`', 'df': ''} | 5 |
| `wait_till_next_round_to_update_turns` | Boolean | {'type': '`Boolean`', 'df': ''} | 4 |
| `round_start_bonus_turns` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `equipment`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 44

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`face`](./Enums.md#enum-face) | Enum | {'type': '`Enum/String`', 'df': ''} | 16 |
| [`head`](./Enums.md#enum-head) | Enum | {'type': '`Enum/String`', 'df': ''} | 14 |
| [`neck`](./Enums.md#enum-neck) | Enum | {'type': '`Enum/String`', 'df': ''} | 10 |
| [`weapon`](./Enums.md#enum-weapon) | Enum | {'type': '`Enum/String`', 'df': 'Weapon item constraint.'} | 7 |

</details>

---

### Context: `mainturn_pattern`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 44

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum | {'type': '`Enum/String`', 'df': ''} | 23 |
| [`do_all`](./Arrays.md#array-do_all) | Array | {'type': '`Array`', 'df': ''} | 9 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array | {'type': '`Array`', 'df': ''} | 8 |
| [`do_strict`](./Arrays.md#array-do_strict) | Array | {'type': '`Array`', 'df': ''} | 2 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `Default`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 37

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 9 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 10 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |

</details>

---

### Context: `FormChangeWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 35 |
| [`form_hasnot`](./Enums.md#enum-form_hasnot) | Enum | {'type': '`Enum/String`', 'df': ''} | 30 |
| [`form_has`](./Enums.md#enum-form_has) | Enum | {'type': '`Enum/String`', 'df': ''} | 25 |

</details>

---

### Context: `virtual_abilities`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`MoveAway`](./Characters_and_Bosses.md#context-moveaway) | Block | {'type': '`Block`', 'df': 'AI Movement: Moves away from the target. | 4 |
| [`MoveClose`](./Characters_and_Bosses.md#context-moveclose) | Block | {'type': '`Block`', 'df': 'AI Movement: Moves into melee range. | 4 |
| [`DashRandomly`](./Characters_and_Bosses.md#context-dashrandomly) | Block | {'type': '`Block`', 'df': 'AI Movement: Dashes to a random valid tile. | 2 |
| [`Escape`](./Characters_and_Bosses.md#context-escape) | Block | {'type': '`Block`', 'df': 'AI Movement: Logic for fleeing or escaping the map. | 2 |
| [`MoveCenter`](./Characters_and_Bosses.md#context-movecenter) | Block | {'type': '`Block`', 'df': 'AI Movement: Moves toward the center of the map. | 2 |
| [`MoveForThrow`](./Characters_and_Bosses.md#context-moveforthrow) | Block | {'type': '`Block`', 'df': 'AI Movement: Repositions to gain line of sight for throwing. | 2 |
| [`SpearRun`](./Characters_and_Bosses.md#context-spearrun) | Block | {'type': '`Block`', 'df': 'AI Movement: Specific movement logic for Spear enemies. | 2 |
| [`CerberubsJumpBlind`](./Characters_and_Bosses.md#context-cerberubsjumpblind) | Block | {'type': '`Block`', 'df': 'AI Logic: Blind jump attack pattern for Cerberubs. | 1 |
| [`CerberubsJumpNormal`](./Characters_and_Bosses.md#context-cerberubsjumpnormal) | Block | {'type': '`Block`', 'df': 'AI Logic: Normal jump attack pattern for Cerberubs. | 1 |
| [`CloseConvert`](./Characters_and_Bosses.md#context-closeconvert) | Block | {'type': '`Block`', 'df': 'AI State: Logic for converting adjacent units. | 1 |
| [`FoodMove`](./Characters_and_Bosses.md#context-foodmove) | Block | {'type': '`Block`', 'df': 'AI Movement: Logic for seeking out food items. | 1 |
| [`ForceTrample`](./Characters_and_Bosses.md#context-forcetrample) | Block | {'type': '`Block`', 'df': 'Logic: Forces movement to act as a trample attack. | 1 |
| [`LeapClose`](./Characters_and_Bosses.md#context-leapclose) | Block | {'type': '`Block`', 'df': 'AI Movement: Executes a jumping maneuver to close distance. | 1 |
| [`MoveForBarrage`](./Characters_and_Bosses.md#context-moveforbarrage) | Block | {'type': '`Block`', 'df': 'AI Movement: Repositions to optimize a barrage attack. | 1 |
| [`MoveForDash`](./Characters_and_Bosses.md#context-movefordash) | Block | {'type': '`Block`', 'df': 'AI Movement: Repositions to set up a dash attack line. | 1 |
| [`MoveForGrass`](./Characters_and_Bosses.md#context-moveforgrass) | Block | {'type': '`Block`', 'df': 'AI Movement: Moves toward grass tiles. | 1 |
| [`MoveForPounce`](./Characters_and_Bosses.md#context-moveforpounce) | Block | {'type': '`Block`', 'df': 'AI Movement: Repositions to optimize a pounce trajectory. | 1 |
| [`MoveForSpin`](./Characters_and_Bosses.md#context-moveforspin) | Block | {'type': '`Block`', 'df': 'AI Movement: Repositions into a cluster of enemies for a spin attack. | 1 |
| [`MoveOneForPuke`](./Characters_and_Bosses.md#context-moveoneforpuke) | Block | {'type': '`Block`', 'df': 'AI Movement: Specific positioning logic for puke attacks. | 1 |
| [`MoveSpaced`](./Characters_and_Bosses.md#context-movespaced) | Block | {'type': '`Block`', 'df': 'AI Movement: Moves to maintain a specific distance from targets. | 1 |
| [`MoveToHead`](./Characters_and_Bosses.md#context-movetohead) | Block | {'type': '`Block`', 'df': "AI Movement: Navigates toward the 'head' or primary target. | 1 |
| [`MoveTowards`](./Characters_and_Bosses.md#context-movetowards) | Block | {'type': '`Block`', 'df': 'AI Movement: Moves toward the nearest target. | 1 |
| [`NCGravecrawlFAR`](./Characters_and_Bosses.md#context-ncgravecrawlfar) | Block | {'type': '`Block`', 'df': 'AI Movement: Specific grapple/crawl logic. | 1 |
| [`ReturnA`](./Characters_and_Bosses.md#context-returna) | Block | {'type': '`Block`', 'df': 'Boss Logic: Specific phase return trigger. | 1 |
| [`RunFar`](./Characters_and_Bosses.md#context-runfar) | Block | {'type': '`Block`', 'df': 'AI Movement: Maximize distance from targets. | 1 |
| [`SuckMF`](./Characters_and_Bosses.md#context-suckmf) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'SuckMF' state. | 1 |
| [`TF_TargetAllies`](./Characters_and_Bosses.md#context-tf_targetallies) | Block | {'type': '`Block`', 'df': 'AI Targeting: Prioritizes allies. | 1 |
| [`TF_TargetEnemies`](./Characters_and_Bosses.md#context-tf_targetenemies) | Block | {'type': '`Block`', 'df': 'AI Targeting: Prioritizes enemies. | 1 |
| [`Unflip`](./Characters_and_Bosses.md#context-unflip) | Block | {'type': '`Block`', 'df': 'Logic: Reverses a flipped state. | 1 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 32

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#context-randompassivepool), [`StacyMutant_Counter`](./Characters_and_Bosses.md#context-stacymutant_counter), [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 119 |

</details>

---

### Context: `DeathRattle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 29

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 8 |
| `is_dying_animation` | Boolean | {'type': '`Boolean`', 'df': ''} | 7 |
| `pop_corpse` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |
| `cancel_knockback` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `immediate` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `must_target_killer` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `target_killer` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `bonusturn_pattern`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 27

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum | {'type': '`Enum/String`', 'df': ''} | 19 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array | {'type': '`Array`', 'df': ''} | 11 |
| [`do_strict`](./Arrays.md#array-do_strict) | Array | {'type': '`Array`', 'df': ''} | 5 |
| [`do_all`](./Arrays.md#array-do_all) | Array | {'type': '`Array`', 'df': ''} | 4 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `CatPartsTransform`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 25

> **Referenced by:** [`PassiveGroup`](./Characters_and_Bosses.md#context-passivegroup), [`StacyMutant_Brace`](./Characters_and_Bosses.md#context-stacymutant_brace), [`StacyMutant_Counter`](./Characters_and_Bosses.md#context-stacymutant_counter), [`StacyMutant_Damage`](./Characters_and_Bosses.md#context-stacymutant_damage), [`StacyMutant_DoubleHead`](./Characters_and_Bosses.md#context-stacymutant_doublehead), [`StacyMutant_Fire`](./Characters_and_Bosses.md#context-stacymutant_fire), [`StacyMutant_Health`](./Characters_and_Bosses.md#context-stacymutant_health), [`StacyMutant_Holy`](./Characters_and_Bosses.md#context-stacymutant_holy), [`StacyMutant_Ice`](./Characters_and_Bosses.md#context-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#context-stacymutant_lightning), [`StacyMutant_Mirror`](./Characters_and_Bosses.md#context-stacymutant_mirror), [`StacyMutant_Speed`](./Characters_and_Bosses.md#context-stacymutant_speed), [`StacyMutant_Thorns`](./Characters_and_Bosses.md#context-stacymutant_thorns), [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 17 |
| `arm1` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the front arm.'} | 3 |
| `arm2` | Number | {'type': '`Number`', 'df': ''} | 3 |
| `body` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the body.'} | 3 |
| `ear1` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the front ear.'} | 3 |
| `head` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the head.'} | 3 |
| `leg1` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the front leg.'} | 3 |
| `leg2` | Number | {'type': '`Number`', 'df': ''} | 3 |
| `tail` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the tail.'} | 3 |
| `texture` | Number | {'type': '`Number`', 'df': ''} | 3 |
| `eye1` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `eye2` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `ear2` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `fallback`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 23

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum | {'type': '`Enum/String`', 'df': ''} | 12 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array | {'type': '`Array`', 'df': ''} | 6 |
| [`do_all`](./Arrays.md#array-do_all) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`do_best`](./Arrays.md#array-do_best) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`do_random`](./Arrays.md#array-do_random) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `BossRewards`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 20 |

</details>

---

### Context: `AbilityReaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 19

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 9 |
| `ability_damage_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |
| `backstabs_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| `only_when_not_your_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| `cancel_knockback` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `enemies_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `even_on_0_damage` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `even_on_0_damage_if_knockback` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `match_knockback_direction` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `ranged_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `verify_target` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 19

> **Referenced by:** [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#context-temppassiveuntilsettled), [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 11 |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 36 |
| `knockback` | Number | {'type': '`Number`', 'df': ''} | 9 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'Classification/category type.'} | 8 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 5 |

</details>

---

### Context: `BirdRewards`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ally_rewards`](./Characters_and_Bosses.md#context-ally_rewards) | Block | {'type': '`Block`', 'df': 'Loot logic triggered if an ally dies. | 18 |
| [`statuses`](./Characters_and_Bosses.md#context-statuses) | Block | {'type': '`Block`', 'df': "Status effects possessed by the character. | 5 |

</details>

---

### Context: `ally_rewards`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

> **Referenced by:** [`BirdRewards`](./Characters_and_Bosses.md#context-birdrewards)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 18 |

</details>

---

### Context: `alt_spawn_pool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Antidote` | Mixed | {'type': '`Number`', 'df': "Applies or references the 'Antidote' effect/state."} | 5 |
| `Blessing` | Mixed | {'type': '`Number`', 'df': "Applies or references the 'Blessing' effect/state."} | 5 |
| `BigCatnip` | Number | {'type': '`Number`', 'df': "Applies or references the 'BigCatnip' effect/state."} | 4 |
| `BigScrap` | Number | {'type': '`Number`', 'df': "Applies or references the 'BigScrap' effect/state."} | 4 |
| `BiggestFood` | Number | {'type': '`Number`', 'df': "Applies or references the 'BiggestFood' effect/state."} | 4 |
| `Coin` | Number | {'type': '`Number`', 'df': "Applies or references the 'Coin' effect/state."} | 4 |
| `BigFood` | Number | {'type': '`Number`', 'df': "Applies or references the 'BigFood' effect/state."} | 2 |
| `Coin10` | Mixed | {'type': '`Number`', 'df': "Applies or references the 'Coin10' effect/state."} | 2 |
| `Coin3` | Number | {'type': '`Number`', 'df': "Applies or references the 'Coin3' effect/state."} | 2 |
| `Coin4` | Number | {'type': '`Number`', 'df': "Applies or references the 'Coin4' effect/state."} | 2 |
| `MedCatnip` | Number | {'type': '`Number`', 'df': "Applies or references the 'MedCatnip' effect/state."} | 2 |
| `MedScrap` | Number | {'type': '`Number`', 'df': "Applies or references the 'MedScrap' effect/state."} | 2 |
| `RandomArmorPickup` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomArmorPickup' effect/state."} | 2 |
| `RandomCatnipPickup` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomCatnipPickup' effect/state."} | 2 |
| `RandomFoodPickup` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomFoodPickup' effect/state."} | 2 |
| `Bear` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bear' effect/state."} | 1 |
| `BlackBird` | Number | {'type': '`Number`', 'df': "Applies or references the 'BlackBird' effect/state."} | 1 |
| `Catepillar` | Number | {'type': '`Number`', 'df': "Applies or references the 'Catepillar' effect/state."} | 1 |
| `Catnip` | Number | {'type': '`Number`', 'df': "Applies or references the 'Catnip' effect/state."} | 1 |
| `CharmedDip` | Number | {'type': '`Number`', 'df': "Applies or references the 'CharmedDip' effect/state."} | 1 |
| `CharmedFloater` | Number | {'type': '`Number`', 'df': "Applies or references the 'CharmedFloater' effect/state."} | 1 |
| `CharmedPile` | Number | {'type': '`Number`', 'df': "Applies or references the 'CharmedPile' effect/state."} | 1 |
| `Cherub` | Number | {'type': '`Number`', 'df': "Applies or references the 'Cherub' effect/state."} | 1 |
| `Chicken` | Number | {'type': '`Number`', 'df': "Applies or references the 'Chicken' effect/state."} | 1 |
| `Coin2` | Number | {'type': '`Number`', 'df': "Applies or references the 'Coin2' effect/state."} | 1 |
| `Dove` | Number | {'type': '`Number`', 'df': "Applies or references the 'Dove' effect/state."} | 1 |
| `Eagle` | Number | {'type': '`Number`', 'df': "Applies or references the 'Eagle' effect/state."} | 1 |
| `Food` | Number | {'type': '`Number`', 'df': "Applies or references the 'Food' effect/state."} | 1 |
| `Harpy` | Number | {'type': '`Number`', 'df': "Applies or references the 'Harpy' effect/state."} | 1 |
| `HummingBird` | Number | {'type': '`Number`', 'df': "Applies or references the 'HummingBird' effect/state."} | 1 |
| `LargeBirdPool` | Number | {'type': '`Number`', 'df': "Applies or references the 'LargeBirdPool' effect/state."} | 1 |
| `MedBirdPool` | Number | {'type': '`Number`', 'df': "Applies or references the 'MedBirdPool' effect/state."} | 1 |
| `Mutant` | Number | {'type': '`Number`', 'df': "Character Form: Behavior and stats for the 'Mutant' state."} | 1 |
| `Pigeon` | Number | {'type': '`Number`', 'df': "Applies or references the 'Pigeon' effect/state."} | 1 |
| `RandomBiggerArmorPickup` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomBiggerArmorPickup' effect/state."} | 1 |
| `RandomBiggerCatnipPickup` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomBiggerCatnipPickup' effect/state."} | 1 |
| `RandomBiggerFoodPickup` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomBiggerFoodPickup' effect/state."} | 1 |
| `Raven` | Number | {'type': '`Number`', 'df': "Applies or references the 'Raven' effect/state."} | 1 |
| `Scrap` | Number | {'type': '`Number`', 'df': "Applies or references the 'Scrap' effect/state."} | 1 |
| `Seagull` | Number | {'type': '`Number`', 'df': "Applies or references the 'Seagull' effect/state."} | 1 |
| `SmallBirdPool` | Number | {'type': '`Number`', 'df': "Applies or references the 'SmallBirdPool' effect/state."} | 1 |
| `Snake` | Number | {'type': '`Number`', 'df': "Applies or references the 'Snake' effect/state."} | 1 |
| `Squirrel` | Number | {'type': '`Number`', 'df': "Applies or references the 'Squirrel' effect/state."} | 1 |
| `Toad` | Number | {'type': '`Number`', 'df': "Applies or references the 'Toad' effect/state."} | 1 |
| `Turkey` | Number | {'type': '`Number`', 'df': "Applies or references the 'Turkey' effect/state."} | 1 |
| `Turtle` | Number | {'type': '`Number`', 'df': "Applies or references the 'Turtle' effect/state."} | 1 |

</details>

---

### Context: `CharacterLightSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`color`](./Arrays.md#array-color) | Array | {'type': '`Array`', 'df': ''} | 16 |
| `size` | Number | {'type': '`Number`', 'df': ''} | 16 |
| [`glow`](./Arrays.md#array-glow) | Array | {'type': '`Array`', 'df': ''} | 8 |

</details>

---

### Context: `HealthPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array | {'type': '`Array`', 'df': ''} | 15 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 15 |
| `stored_food_value` | Number | {'type': '`Number`', 'df': ''} | 15 |
| `anything_eats` | Boolean | {'type': '`Boolean`', 'df': ''} | 4 |
| `force_frame` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `ImmediateAbilityReaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 13 |
| `ability_damage_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |
| `backstabs_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `damage_threshold` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `even_if_blocked` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `health_threshold` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `buddy_damage_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `target_furthest_valid` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

> **Referenced by:** [`MeleeRevengeDamage`](./Characters_and_Bosses.md#context-meleerevengedamage), [`damage_instance`](./Characters_and_Bosses.md#context-damage_instance), [`eat_damage`](./Characters_and_Bosses.md#context-eat_damage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 552 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1886 |

</details>

---

### Context: `AbilityHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root), [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 12 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 12 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |
| `immediate` | Boolean | {'type': '`Boolean`', 'df': ''} | 5 |
| `use_ai` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `also_use_if_buddy_is_dead` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`threshold_min`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `PassiveGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#context-randompassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 14 |

</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 12 |
| `good` | Boolean | {'type': '`Boolean`', 'df': ''} | 8 |
| `spawn_on_death_hit` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |
| `chance` | Mixed | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0) of executing this action.'} | 4 |
| `coins` | Number | {'type': '`Number`', 'df': ''} | 2 |
| [`auto_cast`](./Enums.md#enum-auto_cast) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `consider_all_layers` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `melee_ability_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `round_end_bonusturn_pattern`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_all`](./Arrays.md#array-do_all) | Array | {'type': '`Array`', 'df': ''} | 6 |
| [`do`](./Enums.md#enum-do) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`do_one`](./Arrays.md#array-do_one) | Array | {'type': '`Array`', 'df': ''} | 2 |
| [`do_random`](./Arrays.md#array-do_random) | Array | {'type': '`Array`', 'df': ''} | 2 |
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

### Context: `Normal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 5 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `DeathRattleRevive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 8 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': ''} | 8 |

</details>

---

### Context: `MoveWhenDamaged`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 7 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Rage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 8 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 9 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 6 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String | {'type': '`String`', 'df': ''} | 4 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `FormChangeOnElementInfluence`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 9 |
| [`form`](./Enums.md#enum-form) | Enum | {'type': '`Enum/String`', 'df': ''} | 9 |
| [`exclude`](./Enums.md#enum-exclude) | Enum | {'type': '`Enum/String`', 'df': ''} | 5 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 5 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | {'type': '`Enum/String`', 'df': ''} | 5 |

</details>

---

### Context: `ReflectProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 8 |

</details>

---

### Context: `StatusCollector`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `TransformInXTurns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#context-randompassivepool), [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array | {'type': '`Array`', 'df': ''} | 8 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 8 |
| [`initiative`](./Enums.md#enum-initiative) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`turns`](./Arrays.md#array-turns) | Array | {'type': '`Array`', 'df': 'Turn counter tracking.'} | 1 |

</details>

---

### Context: `TransformOnElementInfluence`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 9 |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 9 |

</details>

---

### Context: `statuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`BirdRewards`](./Characters_and_Bosses.md#context-birdrewards), [`Cat`](./Characters_and_Bosses.md#context-cat), [`NonCat`](./Characters_and_Bosses.md#context-noncat)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |

</details>

---

### Context: `FormChangeOffMap`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_offmap`](./Enums.md#enum-form_offmap) | Enum | {'type': '`Enum/String`', 'df': ''} | 8 |
| [`form_onmap`](./Enums.md#enum-form_onmap) | Enum | {'type': '`Enum/String`', 'df': ''} | 8 |

</details>

---

### Context: `SmallRockBehavior`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 4 |
| `knockback` | Number | {'type': '`Number`', 'df': ''} | 4 |
| `chain` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>

---

### Context: `ChanceToSpitOnDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 7 |
| `flat_chance` | Number | {'type': '`Number`', 'df': ''} | 5 |
| `chance_per_damage` | Number | {'type': '`Number`', 'df': ''} | 3 |
| `backstabs_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `even_on_0_damage_if_knockback` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `MovementReaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 7 |
| `enemies_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| `objects_too` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `on_self_move_too` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `blind_spot` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `forward_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `self_move_exclude_self_abilities` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `CaveFamilyEnrage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 6 |
| `count` | Number | {'type': '`Number`', 'df': 'The numerical quantity.'} | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'Specific entity tag required.'} | 6 |

</details>

---

### Context: `FormChangeWhilePrimingAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`not_priming`](./Enums.md#enum-not_priming) | Enum | {'type': '`Enum/String`', 'df': ''} | 6 |
| [`priming`](./Enums.md#enum-priming) | Enum | {'type': '`Enum/String`', 'df': ''} | 6 |

</details>

---

### Context: `MoveTowardsDamageSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`check_in_form`](./Enums.md#enum-check_in_form) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| `can_move_zero` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`check_has_status`](./Enums.md#enum-check_has_status) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `do_not_move_on_top` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `face_towards_after` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`ignore_tagged_sources`](./Enums.md#enum-ignore_tagged_sources) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `move_far` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `move_short` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `SecurityBotProtect`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 5 |
| `enemies_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| `not_on_kill` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>

---

### Context: `HasCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 5 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 5 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |

</details>

---

### Context: `MoveTowardsKillers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`character_filter`](./Arrays.md#array-character_filter) | Array | {'type': '`Array`', 'df': ''} | 3 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |

</details>

---

### Context: `PassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 10 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 5 |

</details>

---

### Context: `TransformOnDeathImmediately`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |
| [`obj`](./Enums.md#enum-obj) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |

</details>

---

### Context: `BaitAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `range` | Number | {'type': '`Number`', 'df': 'Distance or area of effect in tiles.'} | 4 |

</details>

---

### Context: `Consumed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`statuses`](./Characters_and_Bosses.md#context-statuses)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 23 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 20 |

</details>

---

### Context: `ForceUseAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`FinalBossHitCountdownBoris`](./Characters_and_Bosses.md#context-finalbosshitcountdownboris), [`FinalBossHitCountdownExplosive`](./Characters_and_Bosses.md#context-finalbosshitcountdownexplosive)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 2 |
| `show_name` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>

---

### Context: `MoveAway`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 4 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |

</details>

---

### Context: `MoveClose`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 4 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |

</details>

---

### Context: `OffMap`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 3 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 42 |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 20 |

</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `StunImmunity`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `Trapper`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 4 |
| `cancel_movement` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `pathfinding_avoidance` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `range` | Number | {'type': '`Number`', 'df': 'Distance or area of effect in tiles.'} | 2 |

</details>

---

### Context: `default`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `hot`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 4 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`Die`](./Characters_and_Bosses.md#context-die), [`Dumb`](./Characters_and_Bosses.md#context-dumb), [`Obey`](./Characters_and_Bosses.md#context-obey), [`Stop`](./Characters_and_Bosses.md#context-stop)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TVBotDie` | Number | {'type': '`Number`', 'df': "Applies or references the 'TVBotDie' effect/state."} | 1 |
| `TVBotDumb` | Number | {'type': '`Number`', 'df': "Applies or references the 'TVBotDumb' effect/state."} | 1 |
| `TVBotObey` | Number | {'type': '`Number`', 'df': "Applies or references the 'TVBotObey' effect/state."} | 1 |
| `TVBotStop` | Number | {'type': '`Number`', 'df': "Applies or references the 'TVBotStop' effect/state."} | 1 |

</details>

---

### Context: `AllAlive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `ArmorPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array | {'type': '`Array`', 'df': ''} | 3 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 3 |

</details>

---

### Context: `Buddy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| [`obj`](./Enums.md#enum-obj) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| `reclaim_if_lost` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `Cat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#context-mothertumorpassive), [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#context-mothertumorspawnincapture)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`statuses`](./Characters_and_Bosses.md#context-statuses) | Block | {'type': '`Block`', 'df': "Status effects possessed by the character. | 2 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `Down`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `FormChangeHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_above`](./Enums.md#enum-form_above) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`form_below`](./Enums.md#enum-form_below) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| `count_shield` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `Full`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`statuses_on_enter_form`](./Characters_and_Bosses.md#context-statuses_on_enter_form) | Block | {'type': '`Block`', 'df': 'Status effects instantly applied upon transitioning into this form. | 2 |

</details>

---

### Context: `ManaPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array | {'type': '`Array`', 'df': ''} | 3 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 3 |

</details>

---

### Context: `NonCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#context-mothertumorpassive), [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#context-mothertumorspawnincapture)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`statuses`](./Characters_and_Bosses.md#context-statuses) | Block | {'type': '`Block`', 'df': "Status effects possessed by the character. | 2 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `OneAlive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 3 |

</details>

---

### Context: `RandomPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 22 |

</details>

---

### Context: `ReplaceBrain`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`StacyMutant_Fire`](./Characters_and_Bosses.md#context-stacymutant_fire), [`StacyMutant_Ice`](./Characters_and_Bosses.md#context-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#context-stacymutant_lightning)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`pattern`](./Characters_and_Bosses.md#context-pattern) | Block | {'type': '`Block`', 'df': 'AI sequence logic. | 3 |

</details>

---

### Context: `SupportFormChangeInsteadOfRun`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 2 |
| `wait_till_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `TwoAlive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 3 |

</details>

---

### Context: `Up`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 2 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `AbilityOnRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 2 |
| `force_display_name` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 2 |
| `range` | Number | {'type': '`Number`', 'df': 'Distance or area of effect in tiles.'} | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'Specific entity tag required.'} | 2 |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Fury` | Number | {'type': '`Number`', 'df': "Applies or references the 'Fury' effect/state."} | 2 |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to autocast.'} | 1 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': 'If true, bypasses stun and hard-CC restrictions to cast anyway.'} | 1 |

</details>

---

### Context: `Big`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Mixed | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `Boris`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `BungaEntrance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 2 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `health_threshold` | Number | {'type': '`Number`', 'df': ''} | 2 |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `CaveMan`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `CaveManSpear`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `CherubimReaction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Leave`](./Enums.md#enum-leave) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'Leave' effect/state."} | 2 |
| [`Return`](./Enums.md#enum-return) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'Return' effect/state."} | 2 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ally_rewards`](./Characters_and_Bosses.md#context-ally_rewards)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 14 |
| `odds` | Number | {'type': '`Number`', 'df': "The probability (0.0 to 1.0) of triggering the 'good roll' success state."} | 2 |

</details>

---

### Context: `DashRandomly`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 2 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `DiesToElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `Empty`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 2 |

</details>

---

### Context: `Escape`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `Explosive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `FaceLastDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `FormChangeDuringWeatherElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 2 |
| [`form`](./Enums.md#enum-form) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `Holding`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `Holy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#context-conditional_isphysicalattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `displace` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `distance` | Number | {'type': '`Number`', 'df': 'The distance in tiles to knock the target away.'} | 2 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 2 |

</details>

---

### Context: `MotherTumorSpawnInCapture`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Cat`](./Characters_and_Bosses.md#context-cat) | Block | {'type': '`Block`', 'df': 'Character Form: Base form for standard cats. | 2 |
| [`NonCat`](./Characters_and_Bosses.md#context-noncat) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'NonCat' state. | 2 |
| [`Nothing`](./Characters_and_Bosses.md#context-nothing) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Nothing' state. | 1 |

</details>

---

### Context: `MoveCenter`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `MoveForThrow`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `NotPriming`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `PassiveWhileNotHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 2 |

</details>

---

### Context: `Priming`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 2 |

</details>

---

### Context: `ProtectTargetedAllies`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 2 |
| [`target_filter`](./Enums.md#enum-target_filter) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `Rain`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 2 |

</details>

---

### Context: `RemoveStatusStacks`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusOnEndMove`](./Characters_and_Bosses.md#context-statusonendmove), [`StatusOnTookDamage`](./Characters_and_Bosses.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks to remove.'} | 2 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'The specific status effect ID to remove.'} | 2 |

</details>

---

### Context: `SlotMachineRollPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SlotResult_Jackpot_Coins` | Number | {'type': '`Number`', 'df': "Applies or references the 'SlotResult_Jackpot_Coins' effect/state."} | 2 |
| `SlotResult_Explode` | Number | {'type': '`Number`', 'df': "Applies or references the 'SlotResult_Explode' effect/state."} | 1 |
| `SlotResult_Nothing` | Number | {'type': '`Number`', 'df': "Applies or references the 'SlotResult_Nothing' effect/state."} | 1 |
| `SlotResult_RandomPickup` | Number | {'type': '`Number`', 'df': "Applies or references the 'SlotResult_RandomPickup' effect/state."} | 1 |

</details>

---

### Context: `Small`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `SpearRun`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `SquirrelForm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 7 |

</details>

---

### Context: `StatusGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`RandomStatusFromPool`](./Characters_and_Bosses.md#context-randomstatusfrompool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `StatusOnSpawnIn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 30 |

</details>

---

### Context: `TempPassiveUntilSettled`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#context-conditional_isphysicalattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `TinkererBasicAttackSwitching`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`PassiveGroup`](./Characters_and_Bosses.md#context-passivegroup), [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `TransformOnElementInfluencex`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 2 |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `Turtled`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `active`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `alternate_energized_effect`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Robot`](./Characters_and_Bosses.md#context-robot)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `dispersed_bonusturn_pattern`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |

</details>

---

### Context: `passive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>

---

### Context: `statuses_on_enter_form`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Full`](./Characters_and_Bosses.md#context-full)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `AddStatusToReceivedDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#context-conditional_isphysicalattack) | Block | {'type': '`Block`', 'df': "Conditional: Executes logic if the triggering attack is physical. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `AddStatusToTrampleDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`PassiveWhenDead`](./Characters_and_Bosses.md#context-passivewhendead)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `AdventureTokenPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 12 |

</details>

---

### Context: `AggroTargetIsGovernedByHitEffect`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `Alert`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `AllStatsAura`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`aura_requires_tag`](./Enums.md#enum-aura_requires_tag) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`range`](./Enums.md#enum-range) | Enum | {'type': '`Enum/String`', 'df': 'Distance or area of effect in tiles.'} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `Angry`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |

</details>

---

### Context: `Attacker`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnGainCoins`](./Characters_and_Bosses.md#context-statusongaincoins)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific dodge ability to trigger (e.g., DestroyerDodge).'} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `BattlefieldUniqueRandomPassive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Number | {'type': '`Number`', 'df': "Applies or references the 'DemonicGlyph_Bite' effect/state."} | 1 |
| `DemonicGlyph_Bounce` | Number | {'type': '`Number`', 'df': "Applies or references the 'DemonicGlyph_Bounce' effect/state."} | 1 |
| `DemonicGlyph_Fire` | Number | {'type': '`Number`', 'df': "Applies or references the 'DemonicGlyph_Fire' effect/state."} | 1 |
| `DemonicGlyph_Movement` | Number | {'type': '`Number`', 'df': "Applies or references the 'DemonicGlyph_Movement' effect/state."} | 1 |
| `DemonicGlyph_Summon` | Number | {'type': '`Number`', 'df': "Applies or references the 'DemonicGlyph_Summon' effect/state."} | 1 |

</details>

---

### Context: `BellyFull`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `BigHolding`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `BigHoldingCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `Bishop`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `BlackHole`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `Bomb`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `Bully`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `BungaCheers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ally_damage`](./Enums.md#enum-ally_damage) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`ally_dead`](./Enums.md#enum-ally_dead) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`enemy_damage`](./Enums.md#enum-enemy_damage) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`enemy_dead`](./Enums.md#enum-enemy_dead) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `CaveBaby`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `CaveWoman`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `CaveWomanHasCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `CerberubsAggroTargetBehavior`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alert_form`](./Enums.md#enum-alert_form) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`default_form`](./Enums.md#enum-default_form) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `CerberubsJumpBlind`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `CerberubsJumpNormal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0) of executing this action.'} | 1 |

</details>

---

### Context: `ChanceToFormChangeOnAbilityDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0) of executing this action.'} | 1 |
| [`form`](./Enums.md#enum-form) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `ChaosBossFormChangeGuide`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array | {'type': '`Array`', 'df': ''} | 1 |
| `passives_health_threshold` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `ChaosBossPieces`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

### Context: `ChaosHeadDropIn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`new_music`](./Enums.md#enum-new_music) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'Specific entity tag required.'} | 1 |

</details>

---

### Context: `Charging`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `Close`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `CloseConvert`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusEachTurnEnd`](./Characters_and_Bosses.md#context-statuseachturnend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 6 |
| `odds` | Number | {'type': '`Number`', 'df': "The probability (0.0 to 1.0) of triggering the 'bad roll' failure state."} | 1 |

</details>

---

### Context: `Conditional_HasKnockback`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Else`](./Characters_and_Bosses.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `Conditional_IsPhysicalAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#context-addstatustoreceiveddamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `CounterAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| `without_orienting` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `CreateGlobalModifiers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | All valid keys from the specified engine key are applicable to this context/block. | 5 |

</details>

---

### Context: `Cultist`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 5 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `Damaged`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `Default_Ceiling`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `Default_Ground`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `DelayedAutoRevive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `rounds` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `DesireMech`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `DiceBehavior`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dice_size` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `knockback_damage` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `Die`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#context-keyword_tooltips) | Block | {'type': '`Block`', 'df': "Forces specific UI tooltips to appear. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `DiesToPiercingAndSpikes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `deferred` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `DodgeWhenTargeted`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |

</details>

---

### Context: `Drunker`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `DualSword`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `DualSword_Primed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `Dumb`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#context-keyword_tooltips) | Block | {'type': '`Block`', 'df': "Forces specific UI tooltips to appear. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `DybbukPossessionFallback`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`form`](./Enums.md#enum-form) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#context-addstatustoreceiveddamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 71 |

</details>

---

### Context: `Explody`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `FaceAwayLastDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `override_hit_animation` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `use_turn_animations` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `FightPhase`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `FinalBossBeamQueue`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`queue`](./Enums.md#enum-queue) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`release`](./Enums.md#enum-release) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`transform`](./Enums.md#enum-transform) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `FinalBossBecomeTheChild`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `FinalBossHitCountdownBoris`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `icon` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `icon_ready` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `FinalBossHitCountdownExplosive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `icon` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `icon_ready` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `FinalBossHitCountdownHoly`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `icon` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `icon_ready` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `FinalBossPupils`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`look_at_offset`](./Arrays.md#array-look_at_offset) | Array | {'type': '`Array`', 'df': ''} | 1 |
| `radius` | Number | {'type': '`Number`', 'df': 'Distance or area of effect in tiles.'} | 1 |
| [`reset_center_because_no_target_halflife`](./Enums.md#enum-reset_center_because_no_target_halflife) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`reset_center_because_of_animation_halflife`](./Enums.md#enum-reset_center_because_of_animation_halflife) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`teleport_tracking_halflife`](./Enums.md#enum-teleport_tracking_halflife) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`tracking_acquisition_halflife`](./Enums.md#enum-tracking_acquisition_halflife) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`virtual_head_position`](./Arrays.md#array-virtual_head_position) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

### Context: `FinalBossShieldHealth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`break_ability`](./Enums.md#enum-break_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`state_health`](./Arrays.md#array-state_health) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

### Context: `FinalBossSyncAnimations`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`other_character`](./Enums.md#enum-other_character) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`other_form_change_abilities`](./Characters_and_Bosses.md#context-other_form_change_abilities) | Block | {'type': '`Block`', 'df': "Lists secondary abilities used to change forms. | 1 |

</details>

---

### Context: `Fire`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `FireFull`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `Flop`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `Flop2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `Flush`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `FlushBubs`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `FlushHost`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `FlushNettle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `FoodMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `ForceTrample`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `GainDisorderFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](./Characters_and_Bosses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | {'type': '`Enum/String`', 'df': 'Probability (0.0 to 1.0) of executing this action.'} | 1 |
| [`pool`](./Enums.md#enum-pool) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Grappling`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit_animations`](./Characters_and_Bosses.md#context-exit_animations) | Block | {'type': '`Block`', 'df': 'Animations played when leaving a form/state. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Grown`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `weak_threshold` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `GuaranteedJackpot`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `Guarding`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `HPAltStates`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`clipname`](./Enums.md#enum-clipname) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`thresholds`](./Arrays.md#array-thresholds) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

### Context: `HalfDead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `HasDeadCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `HasRock`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Headless`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `HealNeighborsEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `Hint_CrackedVisuals`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |

</details>

---

### Context: `Hint_CrackedVisuals2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |

</details>

---

### Context: `Hint_CrackedVisuals3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |

</details>

---

### Context: `HitlerExecute`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'Specific entity tag required.'} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `HumanDead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `InfiniteRebirth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `immediate` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `playercat_health` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `InitialPhase`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `Insane_Ceiling`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `Insane_Ground`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `Johnny`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `JohnnyBubs`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `JohnnyHost`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `JohnnyNeedsWashing`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_unwashed`](./Enums.md#enum-form_unwashed) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`form_washed`](./Enums.md#enum-form_washed) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `JohnnyNettle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `Joystick`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `LastHit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `LeapClose`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Lifted`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `Lit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `LowerAmbientLight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`CreateGlobalModifiers`](./Characters_and_Bosses.md#context-createglobalmodifiers)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`amount`](./Arrays.md#array-amount) | Array | {'type': '`Array`', 'df': 'The target opacity/dimness level.'} | 1 |
| `speed` | Number | {'type': '`Number`', 'df': 'The transition speed.'} | 1 |

</details>

---

### Context: `MegaDinoDropController`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`head_drop`](./Enums.md#enum-head_drop) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`leg_leave`](./Enums.md#enum-leg_leave) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`leg_return`](./Enums.md#enum-leg_return) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `stable_legs` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `ModularPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| [`sound_event`](./Enums.md#enum-sound_event) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `MonkCatReactionAbilities`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`spell`](./Enums.md#enum-spell) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`trinket`](./Enums.md#enum-trinket) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`weapon`](./Enums.md#enum-weapon) | Enum | {'type': '`Enum/String`', 'df': 'Weapon item constraint.'} | 1 |

</details>

---

### Context: `MotherGrowController`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eat_damage`](./Characters_and_Bosses.md#context-eat_damage) | Block | {'type': '`Block`', 'df': 'Damage dealt when this entity consumes another. | 1 |
| [`tumor_object`](./Enums.md#enum-tumor_object) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `MotherTumorPassive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Cat`](./Characters_and_Bosses.md#context-cat) | Block | {'type': '`Block`', 'df': 'Character Form: Base form for standard cats. | 1 |
| [`NonCat`](./Characters_and_Bosses.md#context-noncat) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'NonCat' state. | 1 |
| [`considered_forms`](./Arrays.md#array-considered_forms) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`grow_ability`](./Enums.md#enum-grow_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`pass_ani`](./Enums.md#enum-pass_ani) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`receive_ani`](./Enums.md#enum-receive_ani) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Mount`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eject_ability`](./Enums.md#enum-eject_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`enter_ability`](./Enums.md#enum-enter_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Mounted`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |

</details>

---

### Context: `MouthFull`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `MoveAfterAnyAttemptedAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `MoveAwayFromDamageSource`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `MoveAwayWhenEnemyAdjacent`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `once_per_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`weights`](./Enums.md#enum-weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `MoveForBarrage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `MoveForDash`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `MoveForGrass`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `MoveForPounce`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `MoveForSpin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `MoveOneForPuke`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `MoveSpaced`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `MoveToHead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `MoveTowards`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `MultiSpawnOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array | {'type': '`Array`', 'df': 'The numerical quantity.'} | 1 |
| [`obj`](./Enums.md#enum-obj) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `Mutant`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `NCGravecrawlFAR`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `NeutronStar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `NoEyes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |

</details>

---

### Context: `NoStick`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `NormalFull`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `Nothing`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#context-mothertumorspawnincapture)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `Nuke`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `Obey`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#context-keyword_tooltips) | Block | {'type': '`Block`', 'df': "Forces specific UI tooltips to appear. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `Off`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `OffScreen`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `OneEye`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `Open`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `OpenCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `Out`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 30 |

</details>

---

### Context: `PassiveWhenDead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `Possessing`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `Primed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `Pulp2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | {'type': '`Number`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `Pulp3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | {'type': '`Number`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `Pulp4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | {'type': '`Number`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `Pulp5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | {'type': '`Number`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `Pulp6`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | {'type': '`Number`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `Pulp7`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number | {'type': '`Number`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ally_rewards`](./Characters_and_Bosses.md#context-ally_rewards)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 31 |

</details>

---

### Context: `ReturnA`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| `knockback` | Number | {'type': '`Number`', 'df': ''} | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'Classification/category type.'} | 1 |

</details>

---

### Context: `RunFar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `RunWhenLastPlayerCatIsCharmed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`legacy_savekey`](./Enums.md#enum-legacy_savekey) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `ScalingAttackAnimation`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`default`](./Enums.md#enum-default) | Enum | {'type': '`Enum/String`', 'df': 'Baseline configuration.'} | 1 |
| [`thresholds`](./Arrays.md#array-thresholds) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

### Context: `SharePickups`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `include_coins` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `Sitting`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `SkipFirstRounds`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `pop_chance` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `SmallHolding`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `SmallHoldingCat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `SpawningPhase`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `SpewerAltGraphics`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Fire` | Number | {'type': '`Number`', 'df': "Character Form: Behavior and stats for the 'Fire' state."} | 1 |
| `FireFull` | Number | {'type': '`Number`', 'df': "Character Form: Behavior and stats for the 'FireFull' state."} | 1 |
| `Normal` | Number | {'type': '`Number`', 'df': "Character Form: Behavior and stats for the 'Normal' state."} | 1 |
| `NormalFull` | Number | {'type': '`Number`', 'df': "Character Form: Behavior and stats for the 'NormalFull' state."} | 1 |
| `Tar` | Number | {'type': '`Number`', 'df': "Character Form: Behavior and stats for the 'Tar' state."} | 1 |
| `TarFull` | Number | {'type': '`Number`', 'df': "Character Form: Behavior and stats for the 'TarFull' state."} | 1 |

</details>

---

### Context: `StacyMutant_Brace`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StacyMutant_Counter`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `StacyMutant_Damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StacyMutant_DoubleHead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StacyMutant_Fire`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StacyMutant_Health`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StacyMutant_Holy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StacyMutant_Ice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StacyMutant_Lightning`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StacyMutant_Mirror`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `StacyMutant_Speed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StacyMutant_Thorns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `Standing`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `Standing2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | {'type': '`Block`', 'df': 'Turn counter tracking. | 1 |

</details>

---

### Context: `Start_Ceiling`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusAfterXTurns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>

---

### Context: `StatusEachTurnBeginIfHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `consume` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 1 |

</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StacyMutant_Mirror`](./Characters_and_Bosses.md#context-stacymutant_mirror)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `StatusEachTurnEndIfEnabledAtStartOfTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |

</details>

---

### Context: `StatusOnEnemyConfused`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `StatusOverlappingCharactersAndDie`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `StatusWhenStatusCompletelyRemoved`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 1 |

</details>

---

### Context: `Stop`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#context-keyword_tooltips) | Block | {'type': '`Block`', 'df': "Forces specific UI tooltips to appear. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `SuckMF`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `SupportDieInsteadOfRun`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alt_dead_ani`](./Enums.md#enum-alt_dead_ani) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`alt_dying_ani`](./Enums.md#enum-alt_dying_ani) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `SwimmingFormChange`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_in`](./Enums.md#enum-form_in) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`form_out`](./Enums.md#enum-form_out) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `SwitchMusic`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FinalBossBecomeTheChild`](./Characters_and_Bosses.md#context-finalbossbecomethechild)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | {'type': '`Enum/String`', 'df': 'The specific audio layer to transition to (e.g., map, battle).'} | 1 |
| [`new_song`](./Enums.md#enum-new_song) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the new music track.'} | 1 |

</details>

---

### Context: `SwordAndShield`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `SwordAndShield_Primed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `SyncFormsWithBuddy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`no_buddy`](./Enums.md#enum-no_buddy) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `T3HitlerSpawningPhase`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`spell_use_groups`](./Arrays.md#array-spell_use_groups) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

### Context: `TF_TargetAllies`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `TF_TargetEnemies`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `TVBotScreen`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `Dumb` | Number | {'type': '`Number`', 'df': 'AI Profile: A simplified, less optimal decision-making profile.'} | 1 |
| `Fuck` | Number | {'type': '`Number`', 'df': "Applies or references the 'Fuck' effect/state."} | 1 |
| `Obey` | Number | {'type': '`Number`', 'df': 'AI State: Enforced compliance logic (e.g., when Charmed).'} | 1 |
| `Shit` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shit' effect/state."} | 1 |
| `Stop` | Number | {'type': '`Number`', 'df': 'AI Movement: Forces the character to cease movement.'} | 1 |

</details>

---

### Context: `Tar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `TarFull`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `Terminator2Run`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `TerminatorChase`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `TerminatorSkin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`groups`](./Arrays.md#array-groups) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 1 |

</details>

---

### Context: `Throb`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `ThrobBubs`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `ThrobHost`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `ThrobNettle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `TransformOnStatusThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `Transformed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `TwisterFling`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| `max_dist` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `min_dist` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>

---

### Context: `TwoEyes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `Unflip`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `UnlimitedDeathRattleRevive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>

---

### Context: `Unlit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `Unwashed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>

---

### Context: `UseAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusWhenStatusCompletelyRemoved`](./Characters_and_Bosses.md#context-statuswhenstatuscompletelyremoved)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger.'} | 1 |
| `respect_prime` | Boolean | {'type': '`Boolean`', 'df': "If true, respects the ability's prime/cooldown state."} | 1 |

</details>

---

### Context: `UseAbilityWhenOutOfStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 1 |

</details>

---

### Context: `Washed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `Washer`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `Water`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `WereMan`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `Zealot`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 5 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `ZealotBomb`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': '`Block`', 'df': 'Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String | {'type': '`String`', 'df': ''} | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `additional_statuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`SpawnOnDeath`](./Characters_and_Bosses.md#context-spawnondeath)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `ai_if_spawned_as_enemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`pattern`](./Characters_and_Bosses.md#context-pattern) | Block | {'type': '`Block`', 'df': 'AI sequence logic. | 1 |

</details>

---

### Context: `damage_instance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1731 |

</details>

---

### Context: `eat_damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`MotherGrowController`](./Characters_and_Bosses.md#context-mothergrowcontroller)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'Classification/category type.'} | 1 |

</details>

---

### Context: `exit_animations`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Grappling`](./Characters_and_Bosses.md#context-grappling)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Default`](./Enums.md#enum-default) | Enum | {'type': '`Enum/String`', 'df': 'Character Form: The baseline default behavior state.'} | 1 |

</details>

---

### Context: `other_form_change_abilities`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FinalBossSyncAnimations`](./Characters_and_Bosses.md#context-finalbosssyncanimations)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Boris`](./Enums.md#enum-boris) | Enum | {'type': '`Enum/String`', 'df': "Character Form / AI State: Behavior and stats for the 'Boris' state."} | 1 |
| [`Explosive`](./Enums.md#enum-explosive) | Enum | {'type': '`Enum/String`', 'df': "Character Form: Behavior and stats for the 'Explosive' state."} | 1 |
| [`Holy`](./Enums.md#enum-holy) | Enum | {'type': '`Enum/String`', 'df': "Character Form: Behavior and stats for the 'Holy' state."} | 1 |

</details>

---

### Context: `round_start_bonusturn_pattern`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_priority`](./Arrays.md#array-do_priority) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>

---

