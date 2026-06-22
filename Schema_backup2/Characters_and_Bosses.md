# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** Some keys labeled as `Number` actually support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Characters & Bosses

> **Associated Files:** `data/characters/`


### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 600

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Effect Blocks}`](./Engine_Effects.md) | Block | **(Supports Multiple)** Any valid effect. See Engine_Effects.md for the full list. |  |
| [`properties`](#context-properties) | Block | General engine properties. | 600 |
| [`graphics`](#context-graphics) | Block | Visual parameters and animation bindings. | 558 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 544 |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 460 |
| [`abilities`](#context-abilities) | Block | Lists the ability IDs the character possesses. | 458 |
| [`stats`](#context-stats) | Block | Core character metrics (Health, Strength, etc.). | 388 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum |  | 240 |
| [`sound`](#context-sound) | Block | Audio bindings. | 62 |
| [`equipment`](#context-equipment) | Block | List of item IDs the character spawns equipped with. | 44 |
| [`alt_spawn_pool`](#context-alt_spawn_pool) | Block | Alternative pools to draw minions from. | 18 |
| [`ai_if_spawned_as_enemy`](#context-ai_if_spawned_as_enemy) | Block | AI logic override used only if the character is spawned as an enemy. | 1 |
| [`damage_instance`](#context-damage_instance) | Block | Defines damage logic on contact. | 1 |
| [`scale`](./Enums.md#enum-scale) | Enum |  | 1 |

</details>

---

### Context: `passives`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 733

> **Referenced by:** [`1`](#context-1), [`2`](#context-2), [`3`](#context-3), [`4`](#context-4), [`5`](#context-5), [`Alert`](#context-alert), [`AllAlive`](#context-allalive), [`BellyFull`](#context-bellyfull), [`Big`](#context-big), [`BigHolding`](#context-bigholding), [`BigHoldingCat`](#context-bigholdingcat), [`Bishop`](#context-bishop), [`BlackHole`](#context-blackhole), [`Bomb`](#context-bomb), [`Boris`](#context-boris), [`Bully`](#context-bully), [`CaveBaby`](#context-cavebaby), [`CaveMan`](#context-caveman), [`CaveManSpear`](#context-cavemanspear), [`CaveWoman`](#context-cavewoman), [`CaveWomanHasCat`](#context-cavewomanhascat), [`Charging`](#context-charging), [`Close`](#context-close), [`Cultist`](#context-cultist), [`Default`](#context-default), [`Default_Ceiling`](#context-default_ceiling), [`Default_Ground`](#context-default_ground), [`Die`](#context-die), [`Down`](#context-down), [`DualSword`](#context-dualsword), [`DualSword_Primed`](#context-dualsword_primed), [`Dumb`](#context-dumb), [`Explody`](#context-explody), [`Explosive`](#context-explosive), [`FightPhase`](#context-fightphase), [`Fire`](#context-fire), [`FireFull`](#context-firefull), [`Flop`](#context-flop), [`Flop2`](#context-flop2), [`FlushBubs`](#context-flushbubs), [`FlushHost`](#context-flushhost), [`FlushNettle`](#context-flushnettle), [`Full`](#context-full), [`Grown`](#context-grown), [`GuaranteedJackpot`](#context-guaranteedjackpot), [`Guarding`](#context-guarding), [`HalfDead`](#context-halfdead), [`HasCat`](#context-hascat), [`HasDeadCat`](#context-hasdeadcat), [`Headless`](#context-headless), [`Holding`](#context-holding), [`Holy`](#context-holy), [`InitialPhase`](#context-initialphase), [`Insane_Ceiling`](#context-insane_ceiling), [`Insane_Ground`](#context-insane_ground), [`JohnnyBubs`](#context-johnnybubs), [`JohnnyHost`](#context-johnnyhost), [`JohnnyNettle`](#context-johnnynettle), [`Joystick`](#context-joystick), [`Lifted`](#context-lifted), [`Lit`](#context-lit), [`MouthFull`](#context-mouthfull), [`Mutant`](#context-mutant), [`NeutronStar`](#context-neutronstar), [`Normal`](#context-normal), [`NormalFull`](#context-normalfull), [`NotPriming`](#context-notpriming), [`Nuke`](#context-nuke), [`Obey`](#context-obey), [`OffScreen`](#context-offscreen), [`OneAlive`](#context-onealive), [`OneEye`](#context-oneeye), [`Open`](#context-open), [`OpenCat`](#context-opencat), [`Out`](#context-out), [`PassiveWhenAffectedByElement`](#context-passivewhenaffectedbyelement), [`PassiveWhileHasStatus`](#context-passivewhilehasstatus), [`PassiveWhileNotHasStatus`](#context-passivewhilenothasstatus), [`Possessing`](#context-possessing), [`Primed`](#context-primed), [`Priming`](#context-priming), [`Pulp2`](#context-pulp2), [`Pulp3`](#context-pulp3), [`Pulp4`](#context-pulp4), [`Pulp5`](#context-pulp5), [`Pulp6`](#context-pulp6), [`Pulp7`](#context-pulp7), [`ROOT`](#context-root), [`Rage`](#context-rage), [`Sitting`](#context-sitting), [`SmallHolding`](#context-smallholding), [`SmallHoldingCat`](#context-smallholdingcat), [`SpawningPhase`](#context-spawningphase), [`SquirrelForm`](#context-squirrelform), [`Standing`](#context-standing), [`Standing2`](#context-standing2), [`Start_Ceiling`](#context-start_ceiling), [`Stop`](#context-stop), [`SwordAndShield`](#context-swordandshield), [`SwordAndShield_Primed`](#context-swordandshield_primed), [`Tar`](#context-tar), [`TarFull`](#context-tarfull), [`ThrobBubs`](#context-throbbubs), [`ThrobHost`](#context-throbhost), [`ThrobNettle`](#context-throbnettle), [`Transformed`](#context-transformed), [`Turtled`](#context-turtled), [`TwoAlive`](#context-twoalive), [`TwoEyes`](#context-twoeyes), [`Unlit`](#context-unlit), [`Up`](#context-up), [`Washed`](#context-washed), [`Washer`](#context-washer), [`Water`](#context-water), [`WereMan`](#context-wereman), [`Zealot`](#context-zealot), [`ZealotBomb`](#context-zealotbomb), [`active`](#context-active), [`default`](#context-default), [`hot`](#context-hot)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damage Blocks}`](./Engine_Damage.md) | Block | **(Supports Multiple)** A damage hit definition. See Engine_Damage.md for the full schema. |  |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`AddStatusToBasicAttack`](#context-addstatustobasicattack) | Block | Modifier: Injects a status effect payload into the character's basic attacks. | 21 |
| [`MeleeRevengeDamage`](#context-meleerevengedamage) | Block | Reaction: Deals damage or status effects to an attacker upon receiving melee damage. | 17 |
| [`PassiveWhileHasStatus`](#context-passivewhilehasstatus) | Block | Passive: Activates only while the character has the specified status. | 5 |
| [`StatusEachTurnEnd`](#context-statuseachturnend) | Block | Event Trigger: Applies a status at the end of every turn. | 4 |
| [`StatusOnKill`](#context-statusonkill) | Block | Event Trigger: Applies statuses when the character kills an enemy. | 4 |
| [`StatusOnTookDamageFromAbility`](#context-statusontookdamagefromability) | Block | Event Trigger: Applies statuses when taking damage from an ability. | 4 |
| [`RandomPassivePool`](#context-randompassivepool) | Block | Logic: Grants a random passive from the specified pool upon spawning. | 3 |
| [`StatusOnTookDamage`](#context-statusontookdamage) | Block | Event Trigger: Applies statuses when the character takes damage. | 2 |
| [`AddStatusToSpells`](#context-addstatustospells) | Block | Modifier: Injects a status effect payload into all spells cast by the character. | 1 |
| [`AddStatusToWeapons`](#context-addstatustoweapons) | Block | Modifier: Injects a status effect into attacks made with weapons. | 1 |
| [`AdventureTokenPassivePool`](#context-adventuretokenpassivepool) | Block | Map/Metaprogression: Pool of passive modifiers applied by adventure tokens. | 1 |
| [`CreateGlobalModifiers`](#context-createglobalmodifiers) | Block | Encounter Rule: Generates map-wide modifiers. | 1 |
| [`PassiveWhenAffectedByElement`](#context-passivewhenaffectedbyelement) | Block | Passive: Activates only when afflicted by the specified element. | 1 |
| [`PassiveWhenDead`](#context-passivewhendead) | Block | Passive: Activates only while the character is dead (e.g., corpse effects). | 1 |
| [`RevengeDamage`](#context-revengedamage) | Block | Reaction: Deals damage when taking damage. | 1 |
| [`StatusAfterXTurns`](#context-statusafterxturns) | Block | Event Trigger: Applies a status effect after X turns have passed. | 1 |
| [`StatusOnDie`](#context-statusondie) | Block | Event Trigger: Applies statuses when the character dies. | 1 |
| [`StatusOnEndMove`](#context-statusonendmove) | Block | Event Trigger: Applies statuses when the character finishes moving. | 1 |
| [`StatusOnGainCoins`](#context-statusongaincoins) | Block | Event Trigger: Applies statuses when coins are collected. | 1 |

</details>

---

### Context: `properties`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 600

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 505 |
| `health` | Number |  | 427 |
| [`tag`](./Arrays.md#array-tag) | Array | Specific entity tag required. | 399 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 280 |
| `movement` | Number |  | 278 |
| `corpse_health` | Enum |  | 195 |
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
| [`hidden_tag`](./Arrays.md#array-hidden_tag) | Enum |  | 38 |
| `weak_threshold` | Number |  | 32 |
| `knockback_immune` | Boolean |  | 25 |
| `can_be_champion` | Boolean |  | 20 |
| [`lock_orientation`](./Arrays.md#array-lock_orientation) | Array |  | 19 |
| [`ai_scale`](./Enums.md#enum-ai_scale) | Enum |  | 18 |
| [`layer`](./Enums.md#enum-layer) | Enum |  | 17 |
| [`auto_run_priority`](./Enums.md#enum-auto_run_priority) | Enum |  | 16 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 16 |
| `inanimate` | Boolean |  | 16 |
| `disperse_main_turns` | Boolean |  | 15 |
| [`hidden_tags`](./Arrays.md#array-hidden_tags) | Enum |  | 14 |
| [`tags`](./Arrays.md#array-tags) | Array |  | 14 |
| `evenly_dispersed_bonus_turns` | Number |  | 13 |
| `exclude_from_hallucinate` | Boolean |  | 13 |
| `round_end_bonus_turns` | Number |  | 13 |
| `can_be_overkilled` | Boolean |  | 12 |
| `can_collect_coins` | Boolean |  | 10 |
| `deathpoof_size` | Number |  | 10 |
| `dispersed_bonus_turns_consider_initiative` | Boolean |  | 10 |
| `held_coins` | Number |  | 10 |
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

</details>

---

### Context: `ai`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 583

> **Referenced by:** [`0`](#context-0), [`1`](#context-1), [`2`](#context-2), [`3`](#context-3), [`4`](#context-4), [`Alert`](#context-alert), [`Angry`](#context-angry), [`Attacker`](#context-attacker), [`BellyFull`](#context-bellyfull), [`Bishop`](#context-bishop), [`BlackHole`](#context-blackhole), [`Bully`](#context-bully), [`CaveBaby`](#context-cavebaby), [`CaveMan`](#context-caveman), [`CaveManSpear`](#context-cavemanspear), [`CaveWoman`](#context-cavewoman), [`CaveWomanHasCat`](#context-cavewomanhascat), [`Charging`](#context-charging), [`Cultist`](#context-cultist), [`Damaged`](#context-damaged), [`Default`](#context-default), [`Default_Ceiling`](#context-default_ceiling), [`Default_Ground`](#context-default_ground), [`DesireMech`](#context-desiremech), [`Down`](#context-down), [`DualSword`](#context-dualsword), [`DualSword_Primed`](#context-dualsword_primed), [`Explody`](#context-explody), [`FightPhase`](#context-fightphase), [`Fire`](#context-fire), [`FireFull`](#context-firefull), [`Flop`](#context-flop), [`Flop2`](#context-flop2), [`Flush`](#context-flush), [`FlushBubs`](#context-flushbubs), [`FlushHost`](#context-flushhost), [`FlushNettle`](#context-flushnettle), [`Full`](#context-full), [`Grown`](#context-grown), [`Guarding`](#context-guarding), [`HalfDead`](#context-halfdead), [`HasCat`](#context-hascat), [`HasDeadCat`](#context-hasdeadcat), [`HasRock`](#context-hasrock), [`Headless`](#context-headless), [`Holding`](#context-holding), [`InitialPhase`](#context-initialphase), [`Insane_Ceiling`](#context-insane_ceiling), [`Insane_Ground`](#context-insane_ground), [`Johnny`](#context-johnny), [`JohnnyBubs`](#context-johnnybubs), [`JohnnyHost`](#context-johnnyhost), [`JohnnyNettle`](#context-johnnynettle), [`MouthFull`](#context-mouthfull), [`Mutant`](#context-mutant), [`NeutronStar`](#context-neutronstar), [`NoStick`](#context-nostick), [`Normal`](#context-normal), [`NormalFull`](#context-normalfull), [`Nuke`](#context-nuke), [`OffMap`](#context-offmap), [`Open`](#context-open), [`Primed`](#context-primed), [`ROOT`](#context-root), [`Rage`](#context-rage), [`Rain`](#context-rain), [`Sitting`](#context-sitting), [`SquirrelForm`](#context-squirrelform), [`Standing`](#context-standing), [`Standing2`](#context-standing2), [`SwordAndShield`](#context-swordandshield), [`SwordAndShield_Primed`](#context-swordandshield_primed), [`Tar`](#context-tar), [`TarFull`](#context-tarfull), [`Throb`](#context-throb), [`ThrobBubs`](#context-throbbubs), [`ThrobHost`](#context-throbhost), [`ThrobNettle`](#context-throbnettle), [`Transformed`](#context-transformed), [`Turtled`](#context-turtled), [`Unwashed`](#context-unwashed), [`Up`](#context-up), [`Washed`](#context-washed), [`Washer`](#context-washer), [`WereMan`](#context-wereman), [`Zealot`](#context-zealot), [`ZealotBomb`](#context-zealotbomb)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 578 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 498 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 495 |
| [`pattern`](#context-pattern) | Block | AI sequence logic. | 292 |
| [`mainturn_pattern`](#context-mainturn_pattern) | Block | AI Logic: Determines standard ability usage during the main turn. | 44 |
| `end_turn_on_formswitch` | Boolean |  | 41 |
| [`virtual_abilities`](#context-virtual_abilities) | Block | Abilities that are evaluated but not directly castable by the player. | 35 |
| `auto_orient` | Boolean |  | 31 |
| `reset_pattern_on_formswitch` | Boolean |  | 31 |
| `stun_advances_pattern` | Boolean |  | 30 |
| `fallback_advances_pattern` | Boolean |  | 28 |
| [`bonusturn_pattern`](#context-bonusturn_pattern) | Block | AI Logic: Determines ability usage during bonus turns. | 27 |
| [`fallback`](#context-fallback) | Block | Logic executed if primary options fail. | 23 |
| `consider_spells` | Boolean |  | 12 |
| [`round_end_bonusturn_pattern`](#context-round_end_bonusturn_pattern) | Block | AI Logic: Ability usage pattern during round-end bonus turns. | 12 |
| `animate_choice` | Boolean |  | 8 |
| `clamp_pattern` | Boolean |  | 5 |
| `randomize_pattern_start` | Boolean |  | 3 |
| [`dispersed_bonusturn_pattern`](#context-dispersed_bonusturn_pattern) | Block | AI Logic: Alternative bonus turn ability pattern. | 2 |
| `random_orient` | Boolean |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`dice_abilities`](./Arrays.md#array-dice_abilities) | Array |  | 1 |
| `never_hit_ally_corpses` | Boolean |  | 1 |
| [`post_absorb_move_weights`](./Enums.md#enum-post_absorb_move_weights) | Enum |  | 1 |
| `reset_pattern_on_round_begin` | Boolean |  | 1 |
| [`roll_ability`](./Enums.md#enum-roll_ability) | Enum |  | 1 |
| [`round_start_bonusturn_pattern`](#context-round_start_bonusturn_pattern) | Block | AI Logic: Ability usage pattern during round-start bonus turns. | 1 |

</details>

---

### Context: `graphics`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 558

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Graphic Blocks}`](./Engine_Graphics.md) | Block | **(Supports Multiple)** A visual/animation configuration. See Engine_Graphics.md. |  |
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

### Context: `abilities`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 458

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 436 |
| [`move`](./Enums.md#enum-move) | Enum |  | 433 |
| [`spells`](./Arrays.md#array-spells) | Array |  | 381 |
| `can_get_bonus` | Boolean |  | 30 |

</details>

---

### Context: `stats`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 388

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
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

**Total Count:** 296

> **Referenced by:** [`ReplaceBrain`](#context-replacebrain), [`ai`](#context-ai), [`ai_if_spawned_as_enemy`](#context-ai_if_spawned_as_enemy)

| Property Key | Type | Definition | Count |
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
| [`do_best`](./Arrays.md#array-do_best) | Array |  | 1 |
| [`do_best_multiple`](./Arrays.md#array-do_best_multiple) | Array |  | 1 |
| [`do_priority_alternating`](./Arrays.md#array-do_priority_alternating) | Array |  | 1 |
| [`move_then_do_all`](./Arrays.md#array-move_then_do_all) | Array |  | 1 |

</details>

---

### Context: `FormChanger`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 106

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Effect Blocks}`](./Engine_Effects.md) | Block | **(Supports Multiple)** Any valid effect. See Engine_Effects.md for the full list. |  |
| [`initial_form`](./Enums.md#enum-initial_form) | Enum |  | 59 |
| [`Default`](#context-default) | Block | Character Form: The baseline default behavior state. | 37 |
| [`Normal`](#context-normal) | Block | Character Form: Behavior and stats for the 'Normal' state. | 11 |
| [`Rage`](#context-rage) | Block | Character Form: Behavior and stats for the 'Rage' state. | 10 |
| [`HasCat`](#context-hascat) | Block | Character Form: Behavior and stats for the 'HasCat' state. | 5 |
| [`OffMap`](#context-offmap) | Block | Character Form: Behavior and stats for the 'OffMap' state. | 4 |
| [`default`](#context-default) | Block | Baseline configuration. | 4 |
| [`hot`](#context-hot) | Block | Visual effect indicator. | 4 |
| [`AllAlive`](#context-allalive) | Block | Encounter State: Logic executed when all specific entities are currently alive. | 3 |
| [`Down`](#context-down) | Block | Character Form: Behavior and stats for the 'Down' state. | 3 |
| [`Full`](#context-full) | Block | Character Form: Behavior and stats for the 'Full' state. | 3 |
| [`OneAlive`](#context-onealive) | Block | Encounter State: Logic executed when exactly one target is alive. | 3 |
| [`TwoAlive`](#context-twoalive) | Block | Encounter State: Logic executed when exactly two targets are alive. | 3 |
| [`Up`](#context-up) | Block | Character Form: Behavior and stats for the 'Up' state. | 3 |
| [`Big`](#context-big) | Block | Character Form / AI State: Behavior and stats for the 'Big' state. | 2 |
| [`Boris`](#context-boris) | Block | Character Form / AI State: Behavior and stats for the 'Boris' state. | 2 |
| [`CaveMan`](#context-caveman) | Block | Character Form: Behavior and stats for the 'CaveMan' state. | 2 |
| [`CaveManSpear`](#context-cavemanspear) | Block | Character Form: Behavior and stats for the 'CaveManSpear' state. | 2 |
| [`Empty`](#context-empty) | Block | Character Form: Behavior and stats for the 'Empty' state. | 2 |
| [`Explosive`](#context-explosive) | Block | Character Form: Behavior and stats for the 'Explosive' state. | 2 |
| [`Holding`](#context-holding) | Block | Character Form: Behavior and stats for the 'Holding' state. | 2 |
| [`Holy`](#context-holy) | Block | Character Form: Behavior and stats for the 'Holy' state. | 2 |
| [`NotPriming`](#context-notpriming) | Block | Character Form: Behavior and stats when not charging an ability. | 2 |
| [`Priming`](#context-priming) | Block | Character Form: Behavior and stats when charging an ability. | 2 |
| [`Rain`](#context-rain) | Block | Character Form: Behavior and stats for the 'Rain' state. | 2 |
| [`Small`](#context-small) | Block | Character Form: Behavior and stats for the 'Small' state. | 2 |
| [`SquirrelForm`](#context-squirrelform) | Block | Character Form: Behavior and stats for the 'SquirrelForm' state. | 2 |
| [`Turtled`](#context-turtled) | Block | Character Form: Behavior and stats for the 'Turtled' state. | 2 |
| [`active`](#context-active) | Block | Defines actively executed abilities. | 2 |
| [`passive`](#context-passive) | Block | Intrinsic passive modifier. | 2 |
| [`Alert`](#context-alert) | Block | AI State: The behavior profile used when the character is alerted to enemies. | 1 |
| [`Angry`](#context-angry) | Block | Character Form / AI State: Behavior and stats for the 'Angry' state. | 1 |
| [`Attacker`](#context-attacker) | Block | AI Role: Designates the character as an attacker rather than support. | 1 |
| [`BellyFull`](#context-bellyfull) | Block | Character Form / AI State: Behavior and stats for the 'BellyFull' state. | 1 |
| [`BigHolding`](#context-bigholding) | Block | Character Form / AI State: Behavior and stats for the 'BigHolding' state. | 1 |
| [`BigHoldingCat`](#context-bigholdingcat) | Block | Character Form / AI State: Behavior and stats for the 'BigHoldingCat' state. | 1 |
| [`Bishop`](#context-bishop) | Block | Character Form / AI State: Behavior and stats for the 'Bishop' state. | 1 |
| [`BlackHole`](#context-blackhole) | Block | Character Form / AI State: Behavior and stats for the 'BlackHole' state. | 1 |
| [`Bomb`](#context-bomb) | Block | Character Form / AI State: Behavior and stats for the 'Bomb' state. | 1 |
| [`Bully`](#context-bully) | Block | Character Form / AI State: Behavior and stats for the 'Bully' state. | 1 |
| `Butcher` | Block | Applies or references the 'Butcher' effect/state. | 1 |
| [`CaveBaby`](#context-cavebaby) | Block | Character Form: Behavior and stats for the 'CaveBaby' state. | 1 |
| [`CaveWoman`](#context-cavewoman) | Block | Character Form: Behavior and stats for the 'CaveWoman' state. | 1 |
| [`CaveWomanHasCat`](#context-cavewomanhascat) | Block | Character Form: Behavior and stats for the 'CaveWomanHasCat' state. | 1 |
| [`Charging`](#context-charging) | Block | Character Form / AI State: Behavior when charging an attack. | 1 |
| [`Close`](#context-close) | Block | AI Movement logic: Maneuvers into close/melee range. | 1 |
| `Colorless` | Block | Applies or references the 'Colorless' effect/state. | 1 |
| [`Cultist`](#context-cultist) | Block | Character Form: Behavior and stats for the 'Cultist' state. | 1 |
| [`Damaged`](#context-damaged) | Block | Character Form / AI State: Behavior when health is critically low. | 1 |
| [`Default_Ceiling`](#context-default_ceiling) | Block | Character Form: The baseline behavior state while attached to the ceiling. | 1 |
| [`Default_Ground`](#context-default_ground) | Block | Character Form: The baseline behavior state while on the ground. | 1 |
| [`DesireMech`](#context-desiremech) | Block | Character Form: Behavior and stats for the 'DesireMech' state. | 1 |
| [`Die`](#context-die) | Block | Character Form / Logic: Forces the character to die. | 1 |
| `Druid` | Block | Applies or references the 'Druid' effect/state. | 1 |
| [`Drunker`](#context-drunker) | Block | Character Form: Behavior and stats for the 'Drunker' state. | 1 |
| [`DualSword`](#context-dualsword) | Block | Character Form: Behavior and stats for the 'DualSword' state. | 1 |
| [`DualSword_Primed`](#context-dualsword_primed) | Block | Character Form: Behavior and stats for the 'DualSword_Primed' state. | 1 |
| [`Dumb`](#context-dumb) | Block | AI Profile: A simplified, less optimal decision-making profile. | 1 |
| [`Explody`](#context-explody) | Block | Character Form: Behavior and stats for the 'Explody' state. | 1 |
| [`FightPhase`](#context-fightphase) | Block | Boss Logic: Main combat phase. | 1 |
| `Fighter` | Block | Applies or references the 'Fighter' effect/state. | 1 |
| [`Fire`](#context-fire) | Block | Character Form: Behavior and stats for the 'Fire' state. | 1 |
| [`FireFull`](#context-firefull) | Block | Character Form: Behavior and stats for the 'FireFull' state. | 1 |
| [`Flop`](#context-flop) | Block | Character Form: Behavior and stats for the 'Flop' state. | 1 |
| [`Flop2`](#context-flop2) | Block | Character Form: Behavior and stats for the 'Flop2' state. | 1 |
| [`Flush`](#context-flush) | Block | Character Form: Behavior and stats for the 'Flush' state. | 1 |
| [`FlushBubs`](#context-flushbubs) | Block | Character Form: Behavior and stats for the 'FlushBubs' state. | 1 |
| [`FlushHost`](#context-flushhost) | Block | Character Form: Behavior and stats for the 'FlushHost' state. | 1 |
| [`FlushNettle`](#context-flushnettle) | Block | Character Form: Behavior and stats for the 'FlushNettle' state. | 1 |
| [`Grappling`](#context-grappling) | Block | Character Form / AI State: Behavior while grappling an opponent. | 1 |
| [`Grown`](#context-grown) | Block | Character Form: Behavior and stats for the 'Grown' state. | 1 |
| [`GuaranteedJackpot`](#context-guaranteedjackpot) | Block | Loot Logic: Guarantees a high-tier drop. | 1 |
| [`Guarding`](#context-guarding) | Block | Character Form / AI State: Defensive behavior state. | 1 |
| [`HalfDead`](#context-halfdead) | Block | Character Form: Behavior and stats for the 'HalfDead' state. | 1 |
| [`HasDeadCat`](#context-hasdeadcat) | Block | Character Form: Behavior and stats for the 'HasDeadCat' state. | 1 |
| [`HasRock`](#context-hasrock) | Block | Character Form: Behavior and stats for the 'HasRock' state. | 1 |
| [`Headless`](#context-headless) | Block | Character Form: Behavior and stats for the 'Headless' state. | 1 |
| [`Hint_CrackedVisuals`](#context-hint_crackedvisuals) | Block | Visual: Overlay effects for cracked/damaged terrain or objects. | 1 |
| [`Hint_CrackedVisuals2`](#context-hint_crackedvisuals2) | Block | Visual: Secondary cracked visual overlay. | 1 |
| [`Hint_CrackedVisuals3`](#context-hint_crackedvisuals3) | Block | Visual: Tertiary cracked visual overlay. | 1 |
| [`HumanDead`](#context-humandead) | Block | Character Form: Behavior and stats for the 'HumanDead' state. | 1 |
| `Hunter` | Block | Applies or references the 'Hunter' effect/state. | 1 |
| [`InitialPhase`](#context-initialphase) | Block | Boss Logic: The starting phase of an encounter. | 1 |
| [`Insane_Ceiling`](#context-insane_ceiling) | Block | Character Form: Insane behavior state while attached to the ceiling. | 1 |
| [`Insane_Ground`](#context-insane_ground) | Block | Character Form: Insane behavior state while on the ground. | 1 |
| [`Johnny`](#context-johnny) | Block | Character Form: Behavior and stats for the 'Johnny' state. | 1 |
| [`JohnnyBubs`](#context-johnnybubs) | Block | Character Form: Behavior and stats for the 'JohnnyBubs' state. | 1 |
| [`JohnnyHost`](#context-johnnyhost) | Block | Character Form: Behavior and stats for the 'JohnnyHost' state. | 1 |
| [`JohnnyNettle`](#context-johnnynettle) | Block | Character Form: Behavior and stats for the 'JohnnyNettle' state. | 1 |
| [`Joystick`](#context-joystick) | Block | Character Form: Behavior and stats for the 'Joystick' state. | 1 |
| [`LastHit`](#context-lasthit) | Block | Logic: Executes logic on the final hit of a multi-hit attack. | 1 |
| [`Lifted`](#context-lifted) | Block | Character Form: Behavior and stats for the 'Lifted' state. | 1 |
| [`Lit`](#context-lit) | Block | Character Form: Behavior and stats for the 'Lit' state. | 1 |
| `Mage` | Block | Applies or references the 'Mage' effect/state. | 1 |
| `Medic` | Block | Applies or references the 'Medic' effect/state. | 1 |
| `Monk` | Block | Applies or references the 'Monk' effect/state. | 1 |
| [`Mounted`](#context-mounted) | Block | Character Form: Behavior and stats for the 'Mounted' state. | 1 |
| [`MouthFull`](#context-mouthfull) | Block | Character Form: Behavior and stats for the 'MouthFull' state. | 1 |
| [`Mutant`](#context-mutant) | Block | Character Form: Behavior and stats for the 'Mutant' state. | 1 |
| `Necromancer` | Block | Applies or references the 'Necromancer' effect/state. | 1 |
| [`NeutronStar`](#context-neutronstar) | Block | Character Form: Behavior and stats for the 'NeutronStar' state. | 1 |
| `NoDeathRattle` | Block | Applies or references the 'NoDeathRattle' effect/state. | 1 |
| [`NoEyes`](#context-noeyes) | Block | Character Form: Behavior and stats for the 'NoEyes' state. | 1 |
| [`NoStick`](#context-nostick) | Block | Character Form: Behavior and stats for the 'NoStick' state. | 1 |
| [`NormalFull`](#context-normalfull) | Block | Character Form: Behavior and stats for the 'NormalFull' state. | 1 |
| [`Nuke`](#context-nuke) | Block | Character Form: Behavior and stats for the 'Nuke' state. | 1 |
| [`Obey`](#context-obey) | Block | AI State: Enforced compliance logic (e.g., when Charmed). | 1 |
| [`Off`](#context-off) | Block | Character Form: Behavior and stats for the 'Off' state. | 1 |
| [`OffScreen`](#context-offscreen) | Block | Character Form: Behavior and stats for the 'OffScreen' state. | 1 |
| [`OneEye`](#context-oneeye) | Block | Character Form: Behavior and stats for the 'OneEye' state. | 1 |
| [`Open`](#context-open) | Block | Character Form: Behavior and stats for the 'Open' state. | 1 |
| [`OpenCat`](#context-opencat) | Block | Character Form: Behavior and stats for the 'OpenCat' state. | 1 |
| [`Out`](#context-out) | Block | Character Form: Behavior and stats for the 'Out' state. | 1 |
| [`Possessing`](#context-possessing) | Block | Character Form: Behavior and stats for the 'Possessing' state. | 1 |
| [`Primed`](#context-primed) | Block | Character Form: Behavior and stats for the 'Primed' state. | 1 |
| `Psychic` | Block | Applies or references the 'Psychic' effect/state. | 1 |
| [`Pulp2`](#context-pulp2) | Block | Character Form: Behavior and stats for the 'Pulp2' state. | 1 |
| [`Pulp3`](#context-pulp3) | Block | Character Form: Behavior and stats for the 'Pulp3' state. | 1 |
| [`Pulp4`](#context-pulp4) | Block | Character Form: Behavior and stats for the 'Pulp4' state. | 1 |
| [`Pulp5`](#context-pulp5) | Block | Character Form: Behavior and stats for the 'Pulp5' state. | 1 |
| [`Pulp6`](#context-pulp6) | Block | Character Form: Behavior and stats for the 'Pulp6' state. | 1 |
| [`Pulp7`](#context-pulp7) | Block | Character Form: Behavior and stats for the 'Pulp7' state. | 1 |
| [`Sitting`](#context-sitting) | Block | Character Form: Behavior and stats for the 'Sitting' state. | 1 |
| [`SmallHolding`](#context-smallholding) | Block | Character Form: Behavior and stats for the 'SmallHolding' state. | 1 |
| [`SmallHoldingCat`](#context-smallholdingcat) | Block | Character Form: Behavior and stats for the 'SmallHoldingCat' state. | 1 |
| [`SpawningPhase`](#context-spawningphase) | Block | Boss Logic: Phase focused on summoning minions. | 1 |
| [`Standing`](#context-standing) | Block | Character Form: Behavior and stats for the 'Standing' state. | 1 |
| [`Standing2`](#context-standing2) | Block | Character Form: Behavior and stats for the 'Standing2' state. | 1 |
| [`Start_Ceiling`](#context-start_ceiling) | Block | Character Form: Behavior and stats for the 'Start_Ceiling' state. | 1 |
| [`Stop`](#context-stop) | Block | AI Movement: Forces the character to cease movement. | 1 |
| [`SwordAndShield`](#context-swordandshield) | Block | Character Form: Behavior and stats for the 'SwordAndShield' state. | 1 |
| [`SwordAndShield_Primed`](#context-swordandshield_primed) | Block | Character Form: Behavior and stats for the 'SwordAndShield_Primed' state. | 1 |
| `Tank` | Block | Applies or references the 'Tank' effect/state. | 1 |
| [`Tar`](#context-tar) | Block | Character Form: Behavior and stats for the 'Tar' state. | 1 |
| [`TarFull`](#context-tarfull) | Block | Character Form: Behavior and stats for the 'TarFull' state. | 1 |
| `Thief` | Block | Applies or references the 'Thief' effect/state. | 1 |
| [`Throb`](#context-throb) | Block | Character Form: Behavior and stats for the 'Throb' state. | 1 |
| [`ThrobBubs`](#context-throbbubs) | Block | Character Form: Behavior and stats for the 'ThrobBubs' state. | 1 |
| [`ThrobHost`](#context-throbhost) | Block | Character Form: Behavior and stats for the 'ThrobHost' state. | 1 |
| [`ThrobNettle`](#context-throbnettle) | Block | Character Form: Behavior and stats for the 'ThrobNettle' state. | 1 |
| `Tinkerer` | Block | Applies or references the 'Tinkerer' effect/state. | 1 |
| [`Transformed`](#context-transformed) | Block | Character Form: Behavior and stats for the 'Transformed' state. | 1 |
| [`TwoEyes`](#context-twoeyes) | Block | Character Form: Behavior and stats for the 'TwoEyes' state. | 1 |
| [`Unlit`](#context-unlit) | Block | Character Form: Behavior and stats for the 'Unlit' state. | 1 |
| `Unmounted` | Block | Applies or references the 'Unmounted' effect/state. | 1 |
| [`Unwashed`](#context-unwashed) | Block | Character Form: Behavior and stats for the 'Unwashed' state. | 1 |
| [`Washed`](#context-washed) | Block | Character Form: Behavior and stats for the 'Washed' state. | 1 |
| [`Washer`](#context-washer) | Block | Character Form: Behavior and stats for the 'Washer' state. | 1 |
| [`Water`](#context-water) | Block | Character Form: Behavior and stats for the 'Water' state. | 1 |
| [`WereMan`](#context-wereman) | Block | Character Form: Behavior and stats for the 'WereMan' state. | 1 |
| [`Zealot`](#context-zealot) | Block | Character Form: Behavior and stats for the 'Zealot' state. | 1 |
| [`ZealotBomb`](#context-zealotbomb) | Block | Character Form: Behavior and stats for the 'ZealotBomb' state. | 1 |
| `sync_brain_patterns` | Boolean |  | 1 |

</details>

---

### Context: `SpawnOnDeath`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 79

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 3 |
| [`obj`](./Arrays.md#array-obj) | Array |  | 3 |
| [`additional_statuses`](#context-additional_statuses) | Block | Generic statuses added to the character. | 1 |

</details>

---

### Context: `sound`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 62

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alt_sounds`](./Arrays.md#array-alt_sounds) | Array |  | 61 |
| [`SE_Cat_StompLegMove`](./Enums.md#enum-se_cat_stomplegmove) | Enum | Applies or references the 'SE_Cat_StompLegMove' effect/state. | 2 |
| [`SE_CatSwishThrow`](./Enums.md#enum-se_catswishthrow) | Enum | Applies or references the 'SE_CatSwishThrow' effect/state. | 1 |
| [`SE_Cat_ShadowStepIn`](./Enums.md#enum-se_cat_shadowstepin) | Enum | Applies or references the 'SE_Cat_ShadowStepIn' effect/state. | 1 |
| [`SE_Cat_ShadowStepOut`](./Enums.md#enum-se_cat_shadowstepout) | Enum | Applies or references the 'SE_Cat_ShadowStepOut' effect/state. | 1 |
| [`SE_Cat_WeaponLower`](./Enums.md#enum-se_cat_weaponlower) | Enum | Applies or references the 'SE_Cat_WeaponLower' effect/state. | 1 |
| [`SE_Cat_WeaponRaise`](./Enums.md#enum-se_cat_weaponraise) | Enum | Applies or references the 'SE_Cat_WeaponRaise' effect/state. | 1 |
| [`SE_Cat_bearHug`](./Enums.md#enum-se_cat_bearhug) | Enum | Applies or references the 'SE_Cat_bearHug' effect/state. | 1 |
| [`SE_Cat_equipWeapon`](./Enums.md#enum-se_cat_equipweapon) | Enum | Applies or references the 'SE_Cat_equipWeapon' effect/state. | 1 |
| [`SE_PetRock_Dash`](./Enums.md#enum-se_petrock_dash) | Enum | Applies or references the 'SE_PetRock_Dash' effect/state. | 1 |
| [`animation_prefix`](./Enums.md#enum-animation_prefix) | Enum |  | 1 |

</details>

---

### Context: `turns`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 45

> **Referenced by:** [`Bishop`](#context-bishop), [`Bully`](#context-bully), [`Default`](#context-default), [`Default_Ceiling`](#context-default_ceiling), [`Default_Ground`](#context-default_ground), [`FightPhase`](#context-fightphase), [`Holding`](#context-holding), [`InitialPhase`](#context-initialphase), [`Insane_Ceiling`](#context-insane_ceiling), [`Insane_Ground`](#context-insane_ground), [`LastHit`](#context-lasthit), [`Lifted`](#context-lifted), [`Mutant`](#context-mutant), [`Normal`](#context-normal), [`NotPriming`](#context-notpriming), [`Nuke`](#context-nuke), [`OffMap`](#context-offmap), [`OffScreen`](#context-offscreen), [`OneAlive`](#context-onealive), [`Possessing`](#context-possessing), [`Priming`](#context-priming), [`Pulp2`](#context-pulp2), [`Pulp3`](#context-pulp3), [`Pulp4`](#context-pulp4), [`Pulp5`](#context-pulp5), [`Pulp6`](#context-pulp6), [`Pulp7`](#context-pulp7), [`Rage`](#context-rage), [`Sitting`](#context-sitting), [`SpawningPhase`](#context-spawningphase), [`Standing`](#context-standing), [`Standing2`](#context-standing2), [`TwoAlive`](#context-twoalive)

| Property Key | Type | Definition | Count |
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

### Context: `equipment`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 44

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`face`](./Enums.md#enum-face) | Enum |  | 16 |
| [`head`](./Enums.md#enum-head) | Enum |  | 14 |
| [`neck`](./Enums.md#enum-neck) | Enum |  | 10 |
| [`weapon`](./Enums.md#enum-weapon) | Enum | Weapon item constraint. | 7 |

</details>

---

### Context: `mainturn_pattern`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 44

> **Referenced by:** [`ai`](#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum |  | 23 |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 9 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 8 |
| [`do_strict`](./Arrays.md#array-do_strict) | Array |  | 2 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum |  | 2 |

</details>

---

### Context: `Default`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 37

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 24 |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 10 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |

</details>

---

### Context: `FormChangeWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 35

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 35 |
| [`form_hasnot`](./Enums.md#enum-form_hasnot) | Enum |  | 30 |
| [`form_has`](./Enums.md#enum-form_has) | Enum |  | 25 |

</details>

---

### Context: `virtual_abilities`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 35

> **Referenced by:** [`ai`](#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`MoveAway`](#context-moveaway) | Block | AI Movement: Moves away from the target. | 4 |
| [`MoveClose`](#context-moveclose) | Block | AI Movement: Moves into melee range. | 4 |
| [`DashRandomly`](#context-dashrandomly) | Block | AI Movement: Dashes to a random valid tile. | 2 |
| [`Escape`](#context-escape) | Block | AI Movement: Logic for fleeing or escaping the map. | 2 |
| [`MoveCenter`](#context-movecenter) | Block | AI Movement: Moves toward the center of the map. | 2 |
| [`MoveForThrow`](#context-moveforthrow) | Block | AI Movement: Repositions to gain line of sight for throwing. | 2 |
| [`SpearRun`](#context-spearrun) | Block | AI Movement: Specific movement logic for Spear enemies. | 2 |
| [`CerberubsJumpBlind`](#context-cerberubsjumpblind) | Block | AI Logic: Blind jump attack pattern for Cerberubs. | 1 |
| [`CerberubsJumpNormal`](#context-cerberubsjumpnormal) | Block | AI Logic: Normal jump attack pattern for Cerberubs. | 1 |
| [`CloseConvert`](#context-closeconvert) | Block | AI State: Logic for converting adjacent units. | 1 |
| [`FoodMove`](#context-foodmove) | Block | AI Movement: Logic for seeking out food items. | 1 |
| [`ForceTrample`](#context-forcetrample) | Block | Logic: Forces movement to act as a trample attack. | 1 |
| [`LeapClose`](#context-leapclose) | Block | AI Movement: Executes a jumping maneuver to close distance. | 1 |
| [`MoveForBarrage`](#context-moveforbarrage) | Block | AI Movement: Repositions to optimize a barrage attack. | 1 |
| [`MoveForDash`](#context-movefordash) | Block | AI Movement: Repositions to set up a dash attack line. | 1 |
| [`MoveForGrass`](#context-moveforgrass) | Block | AI Movement: Moves toward grass tiles. | 1 |
| [`MoveForPounce`](#context-moveforpounce) | Block | AI Movement: Repositions to optimize a pounce trajectory. | 1 |
| [`MoveForSpin`](#context-moveforspin) | Block | AI Movement: Repositions into a cluster of enemies for a spin attack. | 1 |
| [`MoveOneForPuke`](#context-moveoneforpuke) | Block | AI Movement: Specific positioning logic for puke attacks. | 1 |
| [`MoveSpaced`](#context-movespaced) | Block | AI Movement: Moves to maintain a specific distance from targets. | 1 |
| [`MoveToHead`](#context-movetohead) | Block | AI Movement: Navigates toward the 'head' or primary target. | 1 |
| [`MoveTowards`](#context-movetowards) | Block | AI Movement: Moves toward the nearest target. | 1 |
| [`NCGravecrawlFAR`](#context-ncgravecrawlfar) | Block | AI Movement: Specific grapple/crawl logic. | 1 |
| [`ReturnA`](#context-returna) | Block | Boss Logic: Specific phase return trigger. | 1 |
| [`RunFar`](#context-runfar) | Block | AI Movement: Maximize distance from targets. | 1 |
| [`SuckMF`](#context-suckmf) | Block | Character Form: Behavior and stats for the 'SuckMF' state. | 1 |
| [`TF_TargetAllies`](#context-tf_targetallies) | Block | AI Targeting: Prioritizes allies. | 1 |
| [`TF_TargetEnemies`](#context-tf_targetenemies) | Block | AI Targeting: Prioritizes enemies. | 1 |
| [`Unflip`](#context-unflip) | Block | Logic: Reverses a flipped state. | 1 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 32

> **Referenced by:** [`RandomPassivePool`](#context-randompassivepool), [`StacyMutant_Counter`](#context-stacymutant_counter), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `bonusturn_pattern`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 27

> **Referenced by:** [`ai`](#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum |  | 19 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 11 |
| [`do_strict`](./Arrays.md#array-do_strict) | Array |  | 5 |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 4 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum |  | 1 |

</details>

---

### Context: `CatPartsTransform`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 25

> **Referenced by:** [`PassiveGroup`](#context-passivegroup), [`StacyMutant_Brace`](#context-stacymutant_brace), [`StacyMutant_Counter`](#context-stacymutant_counter), [`StacyMutant_Damage`](#context-stacymutant_damage), [`StacyMutant_DoubleHead`](#context-stacymutant_doublehead), [`StacyMutant_Fire`](#context-stacymutant_fire), [`StacyMutant_Health`](#context-stacymutant_health), [`StacyMutant_Holy`](#context-stacymutant_holy), [`StacyMutant_Ice`](#context-stacymutant_ice), [`StacyMutant_Lightning`](#context-stacymutant_lightning), [`StacyMutant_Mirror`](#context-stacymutant_mirror), [`StacyMutant_Speed`](#context-stacymutant_speed), [`StacyMutant_Thorns`](#context-stacymutant_thorns), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
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

### Context: `fallback`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 23

> **Referenced by:** [`ai`](#context-ai)

| Property Key | Type | Definition | Count |
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

### Context: `BossRewards`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 20

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`common`](./Enums.md#enum-common) | Enum |  | 20 |
| [`rare`](./Enums.md#enum-rare) | Enum |  | 16 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 19

> **Referenced by:** [`TempPassiveUntilSettled`](#context-temppassiveuntilsettled), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
| `damage` | Number | The base damage properties of an attack. | 11 |
| [`effects`](#context-effects) | Block | Non-damaging impact triggers. | 11 |
| `knockback` | Number |  | 9 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 8 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 5 |
| `cant_miss` | Boolean |  | 1 |

</details>

---

### Context: `BirdRewards`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 18

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ally_rewards`](#context-ally_rewards) | Block | Loot logic triggered if an ally dies. | 18 |
| [`statuses`](#context-statuses) | Block | Status effects possessed by the character. | 5 |

</details>

---

### Context: `ally_rewards`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 18

> **Referenced by:** [`BirdRewards`](#context-birdrewards)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum | Generates an item drop from the specified loot pool. | 16 |
| [`Conditional_GoodRoll`](#context-conditional_goodroll) | Block | Conditional: Executes logic on a good RNG roll. | 2 |
| [`RandomStatusFromPool`](#context-randomstatusfrompool) | Block | Logic: Applies a random status from the pool. | 1 |

</details>

---

### Context: `alt_spawn_pool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 18

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Antidote` | Number | Applies or references the 'Antidote' effect/state. | 5 |
| `Blessing` | Number | Applies or references the 'Blessing' effect/state. | 5 |
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

### Context: `CharacterLightSource`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 16

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`color`](./Arrays.md#array-color) | Array |  | 16 |
| `size` | Number |  | 16 |
| [`glow`](./Arrays.md#array-glow) | Array |  | 8 |

</details>

---

### Context: `HealthPickup`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 16

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
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

**Total Count:** 13

| Property Key | Type | Definition | Count |
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

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 13

> **Referenced by:** [`MeleeRevengeDamage`](#context-meleerevengedamage), [`damage_instance`](#context-damage_instance), [`eat_damage`](#context-eat_damage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damage Blocks}`](./Engine_Damage.md) | Block | **(Supports Multiple)** A damage hit definition. See Engine_Damage.md for the full schema. |  |
| [`{Global Modifiers}`](./Engine_GlobalModifiers.md) | Boolean | **(Supports Multiple)** Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |  |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Effect Blocks}`](./Engine_Effects.md) | Block | **(Supports Multiple)** Any valid effect. See Engine_Effects.md for the full list. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `AbilityHealthThreshold`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 12 |
| [`threshold`](./Enums.md#enum-threshold) | Number |  | 11 |
| `even_if_stunned` | Boolean |  | 6 |
| `immediate` | Boolean |  | 5 |
| `use_ai` | Boolean |  | 2 |
| `also_use_if_buddy_is_dead` | Boolean |  | 1 |
| [`threshold_min`](./Math_Equations.md) | Enum |  | 1 |

</details>

---

### Context: `PassiveGroup`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`RandomPassivePool`](#context-randompassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
</details>

---

### Context: `SpawnThingOnDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 12 |
| `good` | Boolean |  | 8 |
| `spawn_on_death_hit` | Boolean |  | 6 |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0) of executing this action. | 4 |
| `coins` | Number |  | 2 |
| [`auto_cast`](./Enums.md#enum-auto_cast) | Enum |  | 1 |
| `consider_all_layers` | Boolean |  | 1 |
| `melee_ability_only` | Boolean |  | 1 |

</details>

---

### Context: `round_end_bonusturn_pattern`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`ai`](#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 6 |
| [`do`](./Enums.md#enum-do) | Enum |  | 3 |
| [`do_one`](./Arrays.md#array-do_one) | Array |  | 2 |
| [`do_random`](./Arrays.md#array-do_random) | Array |  | 2 |
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array |  | 1 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 1 |

</details>

---

### Context: `Normal`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 11

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 10 |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 5 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `DeathRattleRevive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 10

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 8 |
| `even_if_stunned` | Boolean |  | 8 |

</details>

---

### Context: `Rage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 10

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 8 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 6 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 6 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 4 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| `move_speed_multiplier` | Number |  | 1 |

</details>

---

### Context: `AbilityReaction`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 9 |
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

**Total Count:** 9

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 9 |
| [`form`](./Enums.md#enum-form) | Enum |  | 9 |
| [`exclude`](./Enums.md#enum-exclude) | Enum |  | 5 |
| [`particle`](./Enums.md#enum-particle) | Enum |  | 5 |
| [`sfx`](./Enums.md#enum-sfx) | Enum |  | 5 |

</details>

---

### Context: `StatusCollector`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. | 7 |
| `Poison` | Number | Applies or references the 'Poison' effect/state. | 4 |
| `Slow` | Number | Applies or references the 'Slow' effect/state. | 4 |

</details>

---

### Context: `TransformInXTurns`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

> **Referenced by:** [`RandomPassivePool`](#context-randompassivepool), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array |  | 8 |
| `stacks` | Number | Number of stacks or intensity to apply. | 8 |
| [`initiative`](./Enums.md#enum-initiative) | Enum |  | 4 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |
| [`turns`](./Arrays.md#array-turns) | Array | Turn counter tracking. | 1 |

</details>

---

### Context: `TransformOnElementInfluence`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 9 |
| [`object`](./Enums.md#enum-object) | Enum |  | 9 |

</details>

---

### Context: `statuses`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

> **Referenced by:** [`BirdRewards`](#context-birdrewards), [`Cat`](#context-cat), [`NonCat`](#context-noncat)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
| [`Consumed`](#context-consumed) | Block | State triggered when the entity is eaten/consumed. | 4 |

</details>

---

### Context: `DeathRattle`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Property Key | Type | Definition | Count |
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

### Context: `FormChangeOffMap`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_offmap`](./Enums.md#enum-form_offmap) | Enum |  | 8 |
| [`form_onmap`](./Enums.md#enum-form_onmap) | Enum |  | 8 |

</details>

---

### Context: `ChanceToSpitOnDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 7 |
| `flat_chance` | Number |  | 5 |
| `chance_per_damage` | Number |  | 3 |
| `backstabs_only` | Boolean |  | 1 |
| `even_on_0_damage_if_knockback` | Boolean |  | 1 |

</details>

---

### Context: `MoveWhenDamaged`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 7 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 1 |

</details>

---

### Context: `MovementReaction`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
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

### Context: `ReflectProjectiles`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `self_damage` | Number | Recoil or self-inflicted damage/effects applied to the caster. | 7 |

</details>

---

### Context: `CaveFamilyEnrage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 6 |
| `count` | Number | The numerical quantity. | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 6 |

</details>

---

### Context: `FormChangeWhilePrimingAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`not_priming`](./Enums.md#enum-not_priming) | Enum |  | 6 |
| [`priming`](./Enums.md#enum-priming) | Enum |  | 6 |

</details>

---

### Context: `MoveTowardsDamageSource`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`check_in_form`](./Enums.md#enum-check_in_form) | Enum |  | 2 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 2 |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| `can_move_zero` | Boolean |  | 1 |
| [`check_has_status`](./Enums.md#enum-check_has_status) | Enum |  | 1 |
| `do_not_move_on_top` | Boolean |  | 1 |
| `face_towards_after` | Boolean |  | 1 |
| [`ignore_tagged_sources`](./Enums.md#enum-ignore_tagged_sources) | Enum |  | 1 |
| `move_far` | Boolean |  | 1 |
| `move_short` | Boolean |  | 1 |

</details>

---

### Context: `SecurityBotProtect`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 5 |
| `enemies_only` | Boolean |  | 3 |
| [`move`](./Enums.md#enum-move) | Enum |  | 3 |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum |  | 3 |
| `not_on_kill` | Boolean |  | 2 |

</details>

---

### Context: `HasCat`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 5 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 5 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 4 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 4 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |

</details>

---

### Context: `PassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 5 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 5 |

</details>

---

### Context: `BaitAura`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `range` | Number | Distance or area of effect in tiles. | 4 |

</details>

---

### Context: `Consumed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`statuses`](#context-statuses)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Effect Blocks}`](./Engine_Effects.md) | Block | **(Supports Multiple)** Any valid effect. See Engine_Effects.md for the full list. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
| `do_not_pop_corpse` | Boolean |  | 4 |
| [`drop_on_death`](./Enums.md#enum-drop_on_death) | Enum |  | 4 |
| `force_contact` | Boolean | If true, enforces physical overlap. | 4 |
| `instant` | Boolean |  | 4 |
| [`mount_mode`](./Enums.md#enum-mount_mode) | Enum | If true, treats the consumption as riding/mounting instead of eating. | 4 |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Ability triggered by the consumed entity while inside the consumer. | 4 |
| `use_placeholder` | Boolean |  | 2 |

</details>

---

### Context: `MoveAway`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 4 |

</details>

---

### Context: `MoveClose`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 4 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 3 |

</details>

---

### Context: `OffMap`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 3 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `SmallRockBehavior`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 4 |
| `knockback` | Number |  | 4 |
| `chain` | Boolean |  | 2 |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Damage Blocks}`](./Engine_Damage.md) | Block | **(Supports Multiple)** A damage hit definition. See Engine_Damage.md for the full schema. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Damage Blocks}`](./Engine_Damage.md) | Block | **(Supports Multiple)** A damage hit definition. See Engine_Damage.md for the full schema. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `TransformOnDeathImmediately`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum |  | 4 |
| [`obj`](./Enums.md#enum-obj) | Enum |  | 4 |

</details>

---

### Context: `Trapper`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| `cancel_movement` | Boolean |  | 2 |
| `pathfinding_avoidance` | Number |  | 2 |
| `range` | Number | Distance or area of effect in tiles. | 2 |

</details>

---

### Context: `default`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |

</details>

---

### Context: `hot`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 4 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 4 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 4 |

</details>

---

### Context: `keyword_tooltips`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

> **Referenced by:** [`Die`](#context-die), [`Dumb`](#context-dumb), [`Obey`](#context-obey), [`Stop`](#context-stop)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
| [`[keyword_id]`](./Engine_Statuses.md#all-confirmed-keyword_id-values) | String | A Status or Keyword ID whose tooltip text is defined here. See Engine_Statuses.md for all IDs. |  |
</details>

---

### Context: `AllAlive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |

</details>

---

### Context: `ArmorPickup`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array |  | 3 |
| `stacks` | Number | Number of stacks or intensity to apply. | 3 |

</details>

---

### Context: `Buddy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 3 |
| [`obj`](./Enums.md#enum-obj) | Enum |  | 3 |
| `reclaim_if_lost` | Boolean |  | 1 |

</details>

---

### Context: `Cat`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`MotherTumorPassive`](#context-mothertumorpassive), [`MotherTumorSpawnInCapture`](#context-mothertumorspawnincapture)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum |  | 3 |
| [`statuses`](#context-statuses) | Block | Status effects possessed by the character. | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |

</details>

---

### Context: `Down`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |

</details>

---

### Context: `FormChangeHealthThreshold`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_above`](./Enums.md#enum-form_above) | Enum |  | 3 |
| [`form_below`](./Enums.md#enum-form_below) | Enum |  | 3 |
| [`threshold`](./Math_Equations.md) | Enum |  | 3 |
| `count_shield` | Boolean |  | 1 |

</details>

---

### Context: `Full`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| [`statuses_on_enter_form`](#context-statuses_on_enter_form) | Block | Status effects instantly applied upon transitioning into this form. | 2 |

</details>

---

### Context: `ManaPickup`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array |  | 3 |
| `stacks` | Number | Number of stacks or intensity to apply. | 3 |

</details>

---

### Context: `MoveTowardsKillers`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`character_filter`](./Arrays.md#array-character_filter) | Array |  | 3 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 3 |

</details>

---

### Context: `NonCat`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`MotherTumorPassive`](#context-mothertumorpassive), [`MotherTumorSpawnInCapture`](#context-mothertumorspawnincapture)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum |  | 3 |
| [`statuses`](#context-statuses) | Block | Status effects possessed by the character. | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |

</details>

---

### Context: `OneAlive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 3 |

</details>

---

### Context: `RandomPassivePool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`PassiveGroup`](#context-passivegroup) | Block | Passive: A collection of passives grouped together for easier management. | 12 |
| [`AddStatusToBasicAttack`](#context-addstatustobasicattack) | Block | Modifier: Injects a status effect payload into the character's basic attacks. | 10 |

</details>

---

### Context: `ReplaceBrain`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`StacyMutant_Fire`](#context-stacymutant_fire), [`StacyMutant_Ice`](#context-stacymutant_ice), [`StacyMutant_Lightning`](#context-stacymutant_lightning)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 3 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 3 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 3 |
| [`pattern`](#context-pattern) | Block | AI sequence logic. | 3 |

</details>

---

### Context: `TwoAlive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 3 |

</details>

---

### Context: `Up`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `AbilityOnRoundEnd`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| `force_display_name` | Boolean |  | 2 |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| `range` | Number | Distance or area of effect in tiles. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 2 |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Fury` | Number | Applies or references the 'Fury' effect/state. | 2 |

</details>

---

### Context: `AutocastEachRound`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 1 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 1 |

</details>

---

### Context: `Big`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Boris`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `BungaEntrance`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| `even_if_stunned` | Boolean |  | 2 |
| `health_threshold` | Number |  | 2 |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum |  | 2 |

</details>

---

### Context: `CaveMan`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `CaveManSpear`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `CherubimReaction`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Leave`](./Enums.md#enum-leave) | Enum | Applies or references the 'Leave' effect/state. | 2 |
| [`Return`](./Enums.md#enum-return) | Enum | Applies or references the 'Return' effect/state. | 2 |

</details>

---

### Context: `Conditional_GoodRoll`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ally_rewards`](#context-ally_rewards)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Effect Blocks}`](./Engine_Effects.md) | Block | **(Supports Multiple)** Any valid effect. See Engine_Effects.md for the full list. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 2 |

</details>

---

### Context: `DashRandomly`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 2 |

</details>

---

### Context: `DiesToElement`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 1 |
| `instant` | Boolean |  | 1 |

</details>

---

### Context: `Empty`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |

</details>

---

### Context: `Escape`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Context: `Explosive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `ForceUseAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| `show_name` | Boolean |  | 2 |

</details>

---

### Context: `FormChangeDuringWeatherElement`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 2 |
| [`form`](./Enums.md#enum-form) | Enum |  | 2 |

</details>

---

### Context: `Holding`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Holy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `KnockUpAndAway`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`Conditional_HasKnockback`](#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](#context-conditional_isphysicalattack)

| Property Key | Type | Definition | Count |
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

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Cat`](#context-cat) | Block | Character Form: Base form for standard cats. | 2 |
| [`NonCat`](#context-noncat) | Block | Character Form: Behavior and stats for the 'NonCat' state. | 2 |
| [`Nothing`](#context-nothing) | Block | Character Form: Behavior and stats for the 'Nothing' state. | 1 |

</details>

---

### Context: `MoveCenter`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Context: `MoveForThrow`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Context: `NotPriming`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 2 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `PassiveWhileNotHasStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 2 |

</details>

---

### Context: `Priming`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 2 |

</details>

---

### Context: `ProtectTargetedAllies`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`target_filter`](./Enums.md#enum-target_filter) | Enum |  | 2 |

</details>

---

### Context: `Rain`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |

</details>

---

### Context: `RemoveStatusStacks`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`StatusOnEndMove`](#context-statusonendmove), [`StatusOnTookDamage`](#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks to remove. | 2 |
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 2 |

</details>

---

### Context: `Robot`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alternate_energized_effect`](#context-alternate_energized_effect) | Block | Overrides default energized visuals. | 2 |

</details>

---

### Context: `SlotMachineRollPool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SlotResult_Jackpot_Coins` | Number | Applies or references the 'SlotResult_Jackpot_Coins' effect/state. | 2 |
| `SlotResult_Explode` | Number | Applies or references the 'SlotResult_Explode' effect/state. | 1 |
| `SlotResult_Nothing` | Number | Applies or references the 'SlotResult_Nothing' effect/state. | 1 |
| `SlotResult_RandomPickup` | Number | Applies or references the 'SlotResult_RandomPickup' effect/state. | 1 |

</details>

---

### Context: `Small`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Context: `SpearRun`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Context: `SquirrelForm`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| [`tooltip`](./Enums.md#enum-tooltip) | String |  | 1 |

</details>

---

### Context: `StatusGroup`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`RandomStatusFromPool`](#context-randomstatusfrompool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `StatusOnSpawnIn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 1 |
| `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. | 1 |

</details>

---

### Context: `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `SupportFormChangeInsteadOfRun`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| `wait_till_turn` | Boolean |  | 1 |

</details>

---

### Context: `TempPassiveUntilSettled`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`Conditional_HasKnockback`](#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](#context-conditional_isphysicalattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`MeleeRevengeDamage`](#context-meleerevengedamage) | Block | Reaction: Deals damage or status effects to an attacker upon receiving melee damage. | 2 |

</details>

---

### Context: `TinkererBasicAttackSwitching`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`PassiveGroup`](#context-passivegroup), [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum |  | 2 |
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum |  | 2 |

</details>

---

### Context: `TransformOnElementInfluencex`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 2 |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |

</details>

---

### Context: `Turtled`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |

</details>

---

### Context: `active`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |

</details>

---

### Context: `alternate_energized_effect`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`Robot`](#context-robot)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`FormChange`](./Enums.md#enum-formchange) | Enum | Transforms the character into a different state or form (e.g., Rage, HasCat). | 1 |
| `SpellDamageUp` | Number | Applies or references the 'SpellDamageUp' effect/state. | 1 |

</details>

---

### Context: `dispersed_bonusturn_pattern`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ai`](#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum |  | 3 |

</details>

---

### Context: `passive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |

</details>

---

### Context: `statuses_on_enter_form`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`Full`](#context-full)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`UseAbility`](./Enums.md#enum-useability) | Enum | Logic: Forces execution of an ability. | 2 |

</details>

---

### Context: `AddStatusToReceivedDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
| [`Conditional_IsPhysicalAttack`](#context-conditional_isphysicalattack) | Block | Conditional: Executes logic if the triggering attack is physical. | 1 |
| [`Else`](#context-else) | Block | Fallback logic block for conditionals. | 1 |

</details>

---

### Context: `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `AddStatusToTrampleDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`PassiveWhenDead`](#context-passivewhendead)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `AdventureTokenPassivePool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
</details>

---

### Context: `AggroTargetIsGovernedByHitEffect`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean |  | 1 |

</details>

---

### Context: `Alert`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `AllStatsAura`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`aura_requires_tag`](./Enums.md#enum-aura_requires_tag) | Enum |  | 1 |
| [`range`](./Enums.md#enum-range) | Enum | Distance or area of effect in tiles. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `Angry`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |

</details>

---

### Context: `Attacker`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `BackflipWhenTargeted`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusOnGainCoins`](#context-statusongaincoins)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific dodge ability to trigger (e.g., DestroyerDodge). | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `BattlefieldUniqueRandomPassive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
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

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `BigHolding`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `BigHoldingCat`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Bishop`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `BlackHole`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `Bomb`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Bully`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `BungaCheers`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ally_damage`](./Enums.md#enum-ally_damage) | Enum |  | 1 |
| [`ally_dead`](./Enums.md#enum-ally_dead) | Enum |  | 1 |
| [`enemy_damage`](./Enums.md#enum-enemy_damage) | Enum |  | 1 |
| [`enemy_dead`](./Enums.md#enum-enemy_dead) | Enum |  | 1 |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum |  | 1 |

</details>

---

### Context: `CaveBaby`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `CaveWoman`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `CaveWomanHasCat`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `CerberubsAggroTargetBehavior`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alert_form`](./Enums.md#enum-alert_form) | Enum |  | 1 |
| [`default_form`](./Enums.md#enum-default_form) | Enum |  | 1 |

</details>

---

### Context: `CerberubsJumpBlind`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |

</details>

---

### Context: `CerberubsJumpNormal`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |

</details>

---

### Context: `ChanceToBackflip`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| `chance` | Number | Probability (0.0 to 1.0) of executing this action. | 1 |

</details>

---

### Context: `ChanceToFormChangeOnAbilityDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0) of executing this action. | 1 |
| [`form`](./Enums.md#enum-form) | Enum |  | 1 |

</details>

---

### Context: `ChaosBossFormChangeGuide`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array |  | 1 |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array |  | 1 |
| `passives_health_threshold` | Number |  | 1 |

</details>

---

### Context: `ChaosBossPieces`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array |  | 1 |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array |  | 1 |

</details>

---

### Context: `ChaosHeadDropIn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`new_music`](./Enums.md#enum-new_music) | Enum |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 1 |

</details>

---

### Context: `Charging`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Close`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `CloseConvert`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `Conditional_BadRoll`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusEachTurnEnd`](#context-statuseachturnend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Effect Blocks}`](./Engine_Effects.md) | Block | **(Supports Multiple)** Any valid effect. See Engine_Effects.md for the full list. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 1 |

</details>

---

### Context: `Conditional_HasKnockback`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`Else`](#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Effect Blocks}`](./Engine_Effects.md) | Block | **(Supports Multiple)** Any valid effect. See Engine_Effects.md for the full list. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `Conditional_IsPhysicalAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AddStatusToReceivedDamage`](#context-addstatustoreceiveddamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Effect Blocks}`](./Engine_Effects.md) | Block | **(Supports Multiple)** Any valid effect. See Engine_Effects.md for the full list. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `CounterAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| `without_orienting` | Boolean |  | 1 |

</details>

---

### Context: `CreateGlobalModifiers`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Global Modifiers}`](./Engine_GlobalModifiers.md) | Boolean | **(Supports Multiple)** Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |  |
</details>

---

### Context: `Cultist`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `Damaged`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `Default_Ceiling`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Default_Ground`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `DelayedAutoRevive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 1 |
| `rounds` | Number |  | 1 |

</details>

---

### Context: `DesireMech`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `DiceBehavior`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dice_size` | Number |  | 1 |
| `knockback_damage` | Number |  | 1 |

</details>

---

### Context: `Die`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `DiesToPiercingAndSpikes`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `deferred` | Boolean |  | 1 |

</details>

---

### Context: `DodgeWhenTargeted`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |

</details>

---

### Context: `Drunker`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |

</details>

---

### Context: `DualSword`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| `move_speed_multiplier` | Number |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `DualSword_Primed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| `move_speed_multiplier` | Number |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `Dumb`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `DybbukPossessionFallback`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum |  | 1 |
| [`form`](./Enums.md#enum-form) | Enum |  | 1 |

</details>

---

### Context: `Else`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AddStatusToReceivedDamage`](#context-addstatustoreceiveddamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Effect Blocks}`](./Engine_Effects.md) | Block | **(Supports Multiple)** Any valid effect. See Engine_Effects.md for the full list. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `Explody`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `FaceAwayLastDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean |  | 1 |
| `override_hit_animation` | Boolean |  | 1 |
| `use_turn_animations` | Boolean |  | 1 |

</details>

---

### Context: `FaceLastDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean |  | 1 |

</details>

---

### Context: `FightPhase`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `FinalBossBeamQueue`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`queue`](./Enums.md#enum-queue) | Enum |  | 1 |
| [`release`](./Enums.md#enum-release) | Enum |  | 1 |
| [`transform`](./Enums.md#enum-transform) | Enum |  | 1 |

</details>

---

### Context: `FinalBossBecomeTheChild`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Effect Blocks}`](./Engine_Effects.md) | Block | **(Supports Multiple)** Any valid effect. See Engine_Effects.md for the full list. |  |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | Applies or references the 'GlobalSpawnCharacter' effect/state. | 1 |
| `PlayBackground` | Number | Applies or references the 'PlayBackground' effect/state. | 1 |
| [`SwitchMusic`](#context-switchmusic) | Block | Event Trigger: Changes background music track. | 1 |

</details>

---

### Context: `FinalBossHitCountdownBoris`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | Logic: Forces the execution of a specific ability. | 2 |
| `icon` | Number |  | 1 |
| `icon_ready` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `FinalBossHitCountdownExplosive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | Logic: Forces the execution of a specific ability. | 2 |
| `icon` | Number |  | 1 |
| `icon_ready` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `FinalBossHitCountdownHoly`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `icon` | Number |  | 1 |
| `icon_ready` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `FinalBossPupils`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`look_at_offset`](./Arrays.md#array-look_at_offset) | Array |  | 1 |
| `radius` | Number | Distance or area of effect in tiles. | 1 |
| [`reset_center_because_no_target_halflife`](./Enums.md#enum-reset_center_because_no_target_halflife) | Enum |  | 1 |
| [`reset_center_because_of_animation_halflife`](./Enums.md#enum-reset_center_because_of_animation_halflife) | Enum |  | 1 |
| [`teleport_tracking_halflife`](./Enums.md#enum-teleport_tracking_halflife) | Enum |  | 1 |
| [`tracking_acquisition_halflife`](./Enums.md#enum-tracking_acquisition_halflife) | Enum |  | 1 |
| [`virtual_head_position`](./Arrays.md#array-virtual_head_position) | Array |  | 1 |

</details>

---

### Context: `FinalBossShieldHealth`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`break_ability`](./Enums.md#enum-break_ability) | Enum |  | 1 |
| [`state_health`](./Arrays.md#array-state_health) | Array |  | 1 |

</details>

---

### Context: `FinalBossSyncAnimations`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`other_character`](./Enums.md#enum-other_character) | Enum |  | 1 |
| [`other_form_change_abilities`](#context-other_form_change_abilities) | Block | Lists secondary abilities used to change forms. | 1 |

</details>

---

### Context: `Fire`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `FireFull`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Flop`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Flop2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Flush`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `FlushBubs`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `FlushHost`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `FlushNettle`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `FoodMove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `ForceTrample`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |

</details>

---

### Context: `GainDisorderFromPool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0) of executing this action. | 1 |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 1 |

</details>

---

### Context: `Grappling`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit_animations`](#context-exit_animations) | Block | Animations played when leaving a form/state. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |

</details>

---

### Context: `Grown`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| `uifloaters_offset` | Number |  | 1 |
| `weak_threshold` | Number |  | 1 |

</details>

---

### Context: `GuaranteedJackpot`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Guarding`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `HPAltStates`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`clipname`](./Enums.md#enum-clipname) | String |  | 1 |
| [`thresholds`](./Arrays.md#array-thresholds) | Array |  | 1 |

</details>

---

### Context: `HalfDead`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `HasDeadCat`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `HasRock`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Context: `Headless`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `HealNeighborsEachTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `Hint_CrackedVisuals`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Context: `Hint_CrackedVisuals2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Context: `Hint_CrackedVisuals3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Context: `HitlerExecute`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 1 |
| `threshold` | Number |  | 1 |

</details>

---

### Context: `HumanDead`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `InfiniteRebirth`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Effect Blocks}`](./Engine_Effects.md) | Block | **(Supports Multiple)** Any valid effect. See Engine_Effects.md for the full list. |  |
| `health` | Number |  | 1 |
| `immediate` | Boolean |  | 1 |
| `playercat_health` | Number |  | 1 |

</details>

---

### Context: `InitialPhase`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Insane_Ceiling`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Insane_Ground`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Johnny`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `JohnnyBubs`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `JohnnyHost`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `JohnnyNeedsWashing`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_unwashed`](./Enums.md#enum-form_unwashed) | Enum |  | 1 |
| [`form_washed`](./Enums.md#enum-form_washed) | Enum |  | 1 |

</details>

---

### Context: `JohnnyNettle`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Joystick`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `LastHit`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `LeapClose`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `Lifted`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Lit`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `LowerAmbientLight`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`CreateGlobalModifiers`](#context-createglobalmodifiers)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`amount`](./Arrays.md#array-amount) | Array | The target opacity/dimness level. | 1 |
| `speed` | Number | The transition speed. | 1 |

</details>

---

### Context: `MegaDinoDropController`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`head_drop`](./Enums.md#enum-head_drop) | Enum |  | 1 |
| [`leg_leave`](./Enums.md#enum-leg_leave) | Enum |  | 1 |
| [`leg_return`](./Enums.md#enum-leg_return) | Enum |  | 1 |
| `stable_legs` | Number |  | 1 |

</details>

---

### Context: `ModularPickup`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 1 |
| [`sound_event`](./Enums.md#enum-sound_event) | Enum |  | 1 |

</details>

---

### Context: `MonkCatReactionAbilities`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`spell`](./Enums.md#enum-spell) | Enum |  | 1 |
| [`trinket`](./Enums.md#enum-trinket) | Enum |  | 1 |
| [`weapon`](./Enums.md#enum-weapon) | Enum | Weapon item constraint. | 1 |

</details>

---

### Context: `MotherGrowController`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eat_damage`](#context-eat_damage) | Block | Damage dealt when this entity consumes another. | 1 |
| [`tumor_object`](./Enums.md#enum-tumor_object) | Enum |  | 1 |

</details>

---

### Context: `MotherTumorPassive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Cat`](#context-cat) | Block | Character Form: Base form for standard cats. | 1 |
| [`NonCat`](#context-noncat) | Block | Character Form: Behavior and stats for the 'NonCat' state. | 1 |
| [`considered_forms`](./Arrays.md#array-considered_forms) | Array |  | 1 |
| [`grow_ability`](./Enums.md#enum-grow_ability) | Enum |  | 1 |
| [`pass_ani`](./Enums.md#enum-pass_ani) | Enum |  | 1 |
| [`receive_ani`](./Enums.md#enum-receive_ani) | Enum |  | 1 |

</details>

---

### Context: `Mount`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eject_ability`](./Enums.md#enum-eject_ability) | Enum |  | 1 |
| [`enter_ability`](./Enums.md#enum-enter_ability) | Enum |  | 1 |

</details>

---

### Context: `Mounted`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Context: `MouthFull`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `MoveAfterAnyAttemptedAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 1 |

</details>

---

### Context: `MoveAwayFromDamageSource`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 1 |

</details>

---

### Context: `MoveAwayWhenEnemyAdjacent`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 1 |
| `once_per_turn` | Boolean |  | 1 |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 1 |

</details>

---

### Context: `MoveForBarrage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MoveForDash`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MoveForGrass`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MoveForPounce`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MoveForSpin`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MoveOneForPuke`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MoveSpaced`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MoveToHead`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MoveTowards`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MultiSpawnOnDeath`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array | The numerical quantity. | 1 |
| [`obj`](./Enums.md#enum-obj) | Enum |  | 1 |

</details>

---

### Context: `Mutant`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move_speed_multiplier`](./Enums.md#enum-move_speed_multiplier) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `NCGravecrawlFAR`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `NeutronStar`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `NoEyes`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Context: `NoStick`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Context: `NormalFull`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Nothing`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`MotherTumorSpawnInCapture`](#context-mothertumorspawnincapture)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |

</details>

---

### Context: `Nuke`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Obey`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Off`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |

</details>

---

### Context: `OffScreen`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `OneEye`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Open`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `OpenCat`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Out`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `PassiveWhenDead`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`AddStatusToTrampleDamage`](#context-addstatustotrampledamage) | Block | Modifier: Injects a status effect into the character's trample damage. | 1 |

</details>

---

### Context: `Possessing`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Primed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Pulp2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | String |  | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `Pulp3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | String |  | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `Pulp4`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | String |  | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `Pulp5`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | String |  | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `Pulp6`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | String |  | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `Pulp7`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | String |  | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ally_rewards`](#context-ally_rewards)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Damage Blocks}`](./Engine_Damage.md) | Block | **(Supports Multiple)** A damage hit definition. See Engine_Damage.md for the full schema. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
| [`StatusGroup`](#context-statusgroup) | Block | Logic: Groups statuses for batch application. | 2 |

</details>

---

### Context: `ReturnA`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
| `damage` | Number | The base damage properties of an attack. | 1 |
| `knockback` | Number |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 1 |

</details>

---

### Context: `RunFar`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `RunWhenLastPlayerCatIsCharmed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean |  | 1 |
| [`legacy_savekey`](./Enums.md#enum-legacy_savekey) | Enum |  | 1 |

</details>

---

### Context: `ScalingAttackAnimation`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`default`](./Enums.md#enum-default) | Enum | Baseline configuration. | 1 |
| [`thresholds`](./Arrays.md#array-thresholds) | Array |  | 1 |

</details>

---

### Context: `SharePickups`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `include_coins` | Boolean |  | 1 |

</details>

---

### Context: `Sitting`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `SkipFirstRounds`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `pop_chance` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `SmallHolding`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `SmallHoldingCat`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `SpawningPhase`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `SpewerAltGraphics`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
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

**Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| `Brace` | Number | Applies or references the 'Brace' effect/state. | 1 |
| [`CatPartsTransform`](#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |

</details>

---

### Context: `StacyMutant_Counter`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`AddStatusToBasicAttack`](#context-addstatustobasicattack) | Block | Modifier: Injects a status effect payload into the character's basic attacks. | 1 |
| [`CatPartsTransform`](#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| [`CounterAttack`](./Enums.md#enum-counterattack) | Enum | Reaction: Executes a counter-attack ability when hit. | 1 |

</details>

---

### Context: `StacyMutant_Damage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| `AddDamage` | Number | Applies or references the 'AddDamage' effect/state. | 1 |
| `AddMaxHealth` | Number | Applies or references the 'AddMaxHealth' effect/state. | 1 |
| [`CatPartsTransform`](#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |

</details>

---

### Context: `StacyMutant_DoubleHead`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`CatPartsTransform`](#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| `ExtraDispersedTurns` | Number | Applies or references the 'ExtraDispersedTurns' effect/state. | 1 |

</details>

---

### Context: `StacyMutant_Fire`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`CatPartsTransform`](#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | Applies or references the 'ElementImmune' effect/state. | 1 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | Applies or references the 'ReplaceBasicAttack' effect/state. | 1 |
| [`ReplaceBrain`](#context-replacebrain) | Block | AI Logic: Completely overrides the character's AI profile with a new one. | 1 |

</details>

---

### Context: `StacyMutant_Health`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| `AddMaxHealth` | Number | Applies or references the 'AddMaxHealth' effect/state. | 1 |
| `AddSpeed` | Number | Applies or references the 'AddSpeed' effect/state. | 1 |
| [`CatPartsTransform`](#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| `SizeScale` | Number | Applies or references the 'SizeScale' effect/state. | 1 |

</details>

---

### Context: `StacyMutant_Holy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`CatPartsTransform`](#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. | 1 |

</details>

---

### Context: `StacyMutant_Ice`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| `AddMovement` | Number | Applies or references the 'AddMovement' effect/state. | 1 |
| [`CatPartsTransform`](#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | Applies or references the 'ElementImmune' effect/state. | 1 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | Applies or references the 'ReplaceBasicAttack' effect/state. | 1 |
| [`ReplaceBrain`](#context-replacebrain) | Block | AI Logic: Completely overrides the character's AI profile with a new one. | 1 |

</details>

---

### Context: `StacyMutant_Lightning`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`CatPartsTransform`](#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | Applies or references the 'ElementImmune' effect/state. | 1 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | Applies or references the 'ReplaceBasicAttack' effect/state. | 1 |
| [`ReplaceBrain`](#context-replacebrain) | Block | AI Logic: Completely overrides the character's AI profile with a new one. | 1 |

</details>

---

### Context: `StacyMutant_Mirror`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`CatPartsTransform`](#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| `ReflectProjectiles` | Number | Passive: Reflects incoming projectiles back at the attacker. | 1 |
| [`StatusEachTurnEndForEachTurn`](#context-statuseachturnendforeachturn) | Block | Event Trigger: Applies a scaling status at the end of every turn based on turn count. | 1 |

</details>

---

### Context: `StacyMutant_Speed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| `AddDamage` | Number | Applies or references the 'AddDamage' effect/state. | 1 |
| `AddSpeed` | Number | Applies or references the 'AddSpeed' effect/state. | 1 |
| [`CatPartsTransform`](#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| [`SizeScale`](./Enums.md#enum-sizescale) | Enum | Applies or references the 'SizeScale' effect/state. | 1 |

</details>

---

### Context: `StacyMutant_Thorns`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`AdventureTokenPassivePool`](#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`CatPartsTransform`](#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. | 1 |

</details>

---

### Context: `Standing`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Standing2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Start_Ceiling`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `StatusAfterXTurns`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `StatusEachTurnBeginIfHasStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 1 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 1 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 1 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| `consume` | Boolean |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |

</details>

---

### Context: `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StacyMutant_Mirror`](#context-stacymutant_mirror)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `StatusEachTurnEndIfEnabledAtStartOfTurn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | Logic: Forces the execution of a specific ability. | 1 |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `StatusOnEnemyConfused`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | Applies or references the 'ImmediateUseAbility' effect/state. | 1 |

</details>

---

### Context: `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`{Statuses}`](./Engine_Statuses.md) | Number / Block | **(Supports Multiple)** Any valid Status ID. Value = stack count / duration. |  |
</details>

---

### Context: `StatusOverlappingCharactersAndDie`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| `Poison` | Number | Applies or references the 'Poison' effect/state. | 1 |

</details>

---

### Context: `StatusWhenStatusCompletelyRemoved`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| [`UseAbility`](#context-useability) | Block | Logic: Forces execution of an ability. | 1 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |

</details>

---

### Context: `Stop`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `StunImmunity`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean |  | 1 |

</details>

---

### Context: `SuckMF`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `SupportDieInsteadOfRun`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alt_dead_ani`](./Enums.md#enum-alt_dead_ani) | Enum |  | 1 |
| [`alt_dying_ani`](./Enums.md#enum-alt_dying_ani) | Enum |  | 1 |

</details>

---

### Context: `SwimmingFormChange`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_in`](./Enums.md#enum-form_in) | Enum |  | 1 |
| [`form_out`](./Enums.md#enum-form_out) | Enum |  | 1 |

</details>

---

### Context: `SwitchMusic`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FinalBossBecomeTheChild`](#context-finalbossbecomethechild)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | The specific audio layer to transition to (e.g., map, battle). | 1 |
| [`new_song`](./Enums.md#enum-new_song) | Enum | The ID of the new music track. | 1 |

</details>

---

### Context: `SwordAndShield`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `SwordAndShield_Primed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `SyncFormsWithBuddy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`no_buddy`](./Enums.md#enum-no_buddy) | Enum |  | 1 |

</details>

---

### Context: `T3HitlerSpawningPhase`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `T3JoinFight` | Flag | Applies or references the 'T3JoinFight' effect/state. | 1 |
| `T3Spawn_Colorless` | Flag | Applies or references the 'T3Spawn_Colorless' effect/state. | 1 |
| [`spell_use_groups`](./Arrays.md#array-spell_use_groups) | Array |  | 1 |

</details>

---

### Context: `TF_TargetAllies`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |

</details>

---

### Context: `TF_TargetEnemies`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |

</details>

---

### Context: `TVBotScreen`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Effect Blocks}`](./Engine_Effects.md) | Block | **(Supports Multiple)** Any valid effect. See Engine_Effects.md for the full list. |  |
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

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `TarFull`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Terminator2Run`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `TerminatorChase`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |

</details>

---

### Context: `TerminatorSkin`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`groups`](./Arrays.md#array-groups) | Array |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |

</details>

---

### Context: `Throb`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `ThrobBubs`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `ThrobHost`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `ThrobNettle`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `TransformOnStatusThreshold`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |
| `threshold` | Number |  | 1 |

</details>

---

### Context: `Transformed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `TwisterFling`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| `max_dist` | Number |  | 1 |
| `min_dist` | Number |  | 1 |

</details>

---

### Context: `TwoEyes`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Unflip`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`virtual_abilities`](#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `UnlimitedDeathRattleRevive`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| `even_if_stunned` | Boolean |  | 1 |

</details>

---

### Context: `Unlit`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Unwashed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |

</details>

---

### Context: `UseAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`StatusWhenStatusCompletelyRemoved`](#context-statuswhenstatuscompletelyremoved)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger. | 1 |
| `respect_prime` | Boolean | If true, respects the ability's prime/cooldown state. | 1 |

</details>

---

### Context: `UseAbilityWhenOutOfStatus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`passives`](#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |

</details>

---

### Context: `Washed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Washer`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `Water`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `WereMan`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `Zealot`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `ZealotBomb`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FormChanger`](#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `additional_statuses`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`SpawnOnDeath`](#context-spawnondeath)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Passives}`](./Engine_Passives.md) | Boolean / Block | **(Supports Multiple)** Any valid Passive ID. Value = `true` to grant it, or a Block to override defaults. |  |
| `PermanentMadness` | Number | Applies or references the 'PermanentMadness' effect/state. | 1 |

</details>

---

### Context: `ai_if_spawned_as_enemy`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |
| [`pattern`](#context-pattern) | Block | AI sequence logic. | 1 |

</details>

---

### Context: `damage_instance`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Damage Blocks}`](./Engine_Damage.md) | Block | **(Supports Multiple)** A damage hit definition. See Engine_Damage.md for the full schema. |  |
| [`effects`](#context-effects) | Block | Non-damaging impact triggers. | 1 |

</details>

---

### Context: `eat_damage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`MotherGrowController`](#context-mothergrowcontroller)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean |  | 1 |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](#context-effects) | Block | Non-damaging impact triggers. | 1 |
| `makes_contact` | Boolean |  | 1 |
| `piercing` | Boolean |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 1 |

</details>

---

### Context: `exit_animations`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`Grappling`](#context-grappling)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Default`](./Enums.md#enum-default) | Enum | Character Form: The baseline default behavior state. | 1 |

</details>

---

### Context: `other_form_change_abilities`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`FinalBossSyncAnimations`](#context-finalbosssyncanimations)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Boris`](./Enums.md#enum-boris) | Enum | Character Form / AI State: Behavior and stats for the 'Boris' state. | 1 |
| [`Explosive`](./Enums.md#enum-explosive) | Enum | Character Form: Behavior and stats for the 'Explosive' state. | 1 |
| [`Holy`](./Enums.md#enum-holy) | Enum | Character Form: Behavior and stats for the 'Holy' state. | 1 |

</details>

---

### Context: `round_start_bonusturn_pattern`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ai`](#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 1 |

</details>

---

### Numerical Contexts

> The following contexts are numeric keys or array indices.


### Context: `1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| `animation_suffix` | Number |  | 1 |
| `partial_animation_suffix` | Number |  | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| `partial_animation_suffix` | Number |  | 2 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| `animation_suffix` | Number |  | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| `partial_animation_suffix` | Number |  | 2 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| `animation_suffix` | Number |  | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `0`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `4`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| `partial_animation_suffix` | Number |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `5`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| `partial_animation_suffix` | Number |  | 1 |
| [`passives`](#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

