# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Characters & Bosses

> **Associated Files:** `data/characters/`


### Context: `ROOT` (600 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`properties`](./Characters_and_Bosses.md#context-properties) | Block | General engine properties. | 600 |
| [`graphics`](./Characters_and_Bosses.md#context-graphics) | Block | Visual parameters and animation bindings. | 558 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 544 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 460 |
| [`abilities`](./Characters_and_Bosses.md#context-abilities) | Block | Lists the ability IDs the character possesses. | 458 |
| [`stats`](./Characters_and_Bosses.md#context-stats) | Block | Core character metrics (Health, Strength, etc.). | 388 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum |  | 240 |
| [`sound`](./Characters_and_Bosses.md#context-sound) | Block | Audio bindings. | 62 |
| [`equipment`](./Characters_and_Bosses.md#context-equipment) | Block | List of item IDs the character spawns equipped with. | 44 |
| [`alt_spawn_pool`](./Characters_and_Bosses.md#context-alt_spawn_pool) | Block | Alternative pools to draw minions from. | 18 |
| [`ai_if_spawned_as_enemy`](./Characters_and_Bosses.md#context-ai_if_spawned_as_enemy) | Block | AI logic override used only if the character is spawned as an enemy. | 1 |
| [`damage_instance`](./Characters_and_Bosses.md#context-damage_instance) | Block | Defines damage logic on contact. | 1 |
| [`scale`](./Enums.md#enum-scale) | Enum |  | 1 |

</details>

---

### Context: `passives` (733 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Characters_and_Bosses.md#context-1), [`2`](./Characters_and_Bosses.md#context-2), [`3`](./Characters_and_Bosses.md#context-3), [`4`](./Characters_and_Bosses.md#context-4), [`5`](./Characters_and_Bosses.md#context-5), [`Alert`](./Characters_and_Bosses.md#context-alert), [`AllAlive`](./Characters_and_Bosses.md#context-allalive), [`BellyFull`](./Characters_and_Bosses.md#context-bellyfull), [`Big`](./Characters_and_Bosses.md#context-big), [`BigHolding`](./Characters_and_Bosses.md#context-bigholding), [`BigHoldingCat`](./Characters_and_Bosses.md#context-bigholdingcat), [`Bishop`](./Characters_and_Bosses.md#context-bishop), [`BlackHole`](./Characters_and_Bosses.md#context-blackhole), [`Bomb`](./Characters_and_Bosses.md#context-bomb), [`Boris`](./Characters_and_Bosses.md#context-boris), [`Bully`](./Characters_and_Bosses.md#context-bully), [`CaveBaby`](./Characters_and_Bosses.md#context-cavebaby), [`CaveMan`](./Characters_and_Bosses.md#context-caveman), [`CaveManSpear`](./Characters_and_Bosses.md#context-cavemanspear), [`CaveWoman`](./Characters_and_Bosses.md#context-cavewoman), [`CaveWomanHasCat`](./Characters_and_Bosses.md#context-cavewomanhascat), [`Charging`](./Characters_and_Bosses.md#context-charging), [`Close`](./Characters_and_Bosses.md#context-close), [`Cultist`](./Characters_and_Bosses.md#context-cultist), [`Default`](./Characters_and_Bosses.md#context-default), [`Default_Ceiling`](./Characters_and_Bosses.md#context-default_ceiling), [`Default_Ground`](./Characters_and_Bosses.md#context-default_ground), [`Die`](./Characters_and_Bosses.md#context-die), [`Down`](./Characters_and_Bosses.md#context-down), [`DualSword`](./Characters_and_Bosses.md#context-dualsword), [`DualSword_Primed`](./Characters_and_Bosses.md#context-dualsword_primed), [`Dumb`](./Characters_and_Bosses.md#context-dumb), [`Explody`](./Characters_and_Bosses.md#context-explody), [`Explosive`](./Characters_and_Bosses.md#context-explosive), [`FightPhase`](./Characters_and_Bosses.md#context-fightphase), [`Fire`](./Characters_and_Bosses.md#context-fire), [`FireFull`](./Characters_and_Bosses.md#context-firefull), [`Flop`](./Characters_and_Bosses.md#context-flop), [`Flop2`](./Characters_and_Bosses.md#context-flop2), [`FlushBubs`](./Characters_and_Bosses.md#context-flushbubs), [`FlushHost`](./Characters_and_Bosses.md#context-flushhost), [`FlushNettle`](./Characters_and_Bosses.md#context-flushnettle), [`Full`](./Characters_and_Bosses.md#context-full), [`Grown`](./Characters_and_Bosses.md#context-grown), [`GuaranteedJackpot`](./Characters_and_Bosses.md#context-guaranteedjackpot), [`Guarding`](./Characters_and_Bosses.md#context-guarding), [`HalfDead`](./Characters_and_Bosses.md#context-halfdead), [`HasCat`](./Characters_and_Bosses.md#context-hascat), [`HasDeadCat`](./Characters_and_Bosses.md#context-hasdeadcat), [`Headless`](./Characters_and_Bosses.md#context-headless), [`Holding`](./Characters_and_Bosses.md#context-holding), [`Holy`](./Characters_and_Bosses.md#context-holy), [`InitialPhase`](./Characters_and_Bosses.md#context-initialphase), [`Insane_Ceiling`](./Characters_and_Bosses.md#context-insane_ceiling), [`Insane_Ground`](./Characters_and_Bosses.md#context-insane_ground), [`JohnnyBubs`](./Characters_and_Bosses.md#context-johnnybubs), [`JohnnyHost`](./Characters_and_Bosses.md#context-johnnyhost), [`JohnnyNettle`](./Characters_and_Bosses.md#context-johnnynettle), [`Joystick`](./Characters_and_Bosses.md#context-joystick), [`Lifted`](./Characters_and_Bosses.md#context-lifted), [`Lit`](./Characters_and_Bosses.md#context-lit), [`MouthFull`](./Characters_and_Bosses.md#context-mouthfull), [`Mutant`](./Characters_and_Bosses.md#context-mutant), [`NeutronStar`](./Characters_and_Bosses.md#context-neutronstar), [`Normal`](./Characters_and_Bosses.md#context-normal), [`NormalFull`](./Characters_and_Bosses.md#context-normalfull), [`NotPriming`](./Characters_and_Bosses.md#context-notpriming), [`Nuke`](./Characters_and_Bosses.md#context-nuke), [`Obey`](./Characters_and_Bosses.md#context-obey), [`OffScreen`](./Characters_and_Bosses.md#context-offscreen), [`OneAlive`](./Characters_and_Bosses.md#context-onealive), [`OneEye`](./Characters_and_Bosses.md#context-oneeye), [`Open`](./Characters_and_Bosses.md#context-open), [`OpenCat`](./Characters_and_Bosses.md#context-opencat), [`Out`](./Characters_and_Bosses.md#context-out), [`PassiveWhenAffectedByElement`](./Characters_and_Bosses.md#context-passivewhenaffectedbyelement), [`PassiveWhileHasStatus`](./Characters_and_Bosses.md#context-passivewhilehasstatus), [`PassiveWhileNotHasStatus`](./Characters_and_Bosses.md#context-passivewhilenothasstatus), [`Possessing`](./Characters_and_Bosses.md#context-possessing), [`Primed`](./Characters_and_Bosses.md#context-primed), [`Priming`](./Characters_and_Bosses.md#context-priming), [`Pulp2`](./Characters_and_Bosses.md#context-pulp2), [`Pulp3`](./Characters_and_Bosses.md#context-pulp3), [`Pulp4`](./Characters_and_Bosses.md#context-pulp4), [`Pulp5`](./Characters_and_Bosses.md#context-pulp5), [`Pulp6`](./Characters_and_Bosses.md#context-pulp6), [`Pulp7`](./Characters_and_Bosses.md#context-pulp7), [`ROOT`](./Characters_and_Bosses.md#context-root), [`Rage`](./Characters_and_Bosses.md#context-rage), [`Sitting`](./Characters_and_Bosses.md#context-sitting), [`SmallHolding`](./Characters_and_Bosses.md#context-smallholding), [`SmallHoldingCat`](./Characters_and_Bosses.md#context-smallholdingcat), [`SpawningPhase`](./Characters_and_Bosses.md#context-spawningphase), [`SquirrelForm`](./Characters_and_Bosses.md#context-squirrelform), [`Standing`](./Characters_and_Bosses.md#context-standing), [`Standing2`](./Characters_and_Bosses.md#context-standing2), [`Start_Ceiling`](./Characters_and_Bosses.md#context-start_ceiling), [`Stop`](./Characters_and_Bosses.md#context-stop), [`SwordAndShield`](./Characters_and_Bosses.md#context-swordandshield), [`SwordAndShield_Primed`](./Characters_and_Bosses.md#context-swordandshield_primed), [`Tar`](./Characters_and_Bosses.md#context-tar), [`TarFull`](./Characters_and_Bosses.md#context-tarfull), [`ThrobBubs`](./Characters_and_Bosses.md#context-throbbubs), [`ThrobHost`](./Characters_and_Bosses.md#context-throbhost), [`ThrobNettle`](./Characters_and_Bosses.md#context-throbnettle), [`Transformed`](./Characters_and_Bosses.md#context-transformed), [`Turtled`](./Characters_and_Bosses.md#context-turtled), [`TwoAlive`](./Characters_and_Bosses.md#context-twoalive), [`TwoEyes`](./Characters_and_Bosses.md#context-twoeyes), [`Unlit`](./Characters_and_Bosses.md#context-unlit), [`Up`](./Characters_and_Bosses.md#context-up), [`Washed`](./Characters_and_Bosses.md#context-washed), [`Washer`](./Characters_and_Bosses.md#context-washer), [`Water`](./Characters_and_Bosses.md#context-water), [`WereMan`](./Characters_and_Bosses.md#context-wereman), [`Zealot`](./Characters_and_Bosses.md#context-zealot), [`ZealotBomb`](./Characters_and_Bosses.md#context-zealotbomb), [`active`](./Characters_and_Bosses.md#context-active), [`default`](./Characters_and_Bosses.md#context-default), [`hot`](./Characters_and_Bosses.md#context-hot)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`AddStatusToBasicAttack`](./Characters_and_Bosses.md#context-addstatustobasicattack) | Block | Modifier: Injects a status effect payload into the character's basic attacks. | 21 |
| [`MeleeRevengeDamage`](./Characters_and_Bosses.md#context-meleerevengedamage) | Block | Reaction: Deals damage or status effects to an attacker upon receiving melee damage. | 17 |
| [`PassiveWhileHasStatus`](./Characters_and_Bosses.md#context-passivewhilehasstatus) | Block | Passive: Activates only while the character has the specified status. | 5 |
| [`StatusEachTurnEnd`](./Characters_and_Bosses.md#context-statuseachturnend) | Block | Event Trigger: Applies a status at the end of every turn. | 4 |
| [`StatusOnKill`](./Characters_and_Bosses.md#context-statusonkill) | Block | Event Trigger: Applies statuses when the character kills an enemy. | 4 |
| [`StatusOnTookDamageFromAbility`](./Characters_and_Bosses.md#context-statusontookdamagefromability) | Block | Event Trigger: Applies statuses when taking damage from an ability. | 4 |
| [`RandomPassivePool`](./Characters_and_Bosses.md#context-randompassivepool) | Block | Logic: Grants a random passive from the specified pool upon spawning. | 3 |
| [`StatusOnTookDamage`](./Characters_and_Bosses.md#context-statusontookdamage) | Block | Event Trigger: Applies statuses when the character takes damage. | 2 |
| [`AddStatusToSpells`](./Characters_and_Bosses.md#context-addstatustospells) | Block | Modifier: Injects a status effect payload into all spells cast by the character. | 1 |
| [`AddStatusToWeapons`](./Characters_and_Bosses.md#context-addstatustoweapons) | Block | Modifier: Injects a status effect into attacks made with weapons. | 1 |
| [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool) | Block | Map/Metaprogression: Pool of passive modifiers applied by adventure tokens. | 1 |
| [`CreateGlobalModifiers`](./Characters_and_Bosses.md#context-createglobalmodifiers) | Block | Encounter Rule: Generates map-wide modifiers. | 1 |
| [`PassiveWhenAffectedByElement`](./Characters_and_Bosses.md#context-passivewhenaffectedbyelement) | Block | Passive: Activates only when afflicted by the specified element. | 1 |
| [`PassiveWhenDead`](./Characters_and_Bosses.md#context-passivewhendead) | Block | Passive: Activates only while the character is dead (e.g., corpse effects). | 1 |
| [`RevengeDamage`](./Characters_and_Bosses.md#context-revengedamage) | Block | Reaction: Deals damage when taking damage. | 1 |
| [`StatusAfterXTurns`](./Characters_and_Bosses.md#context-statusafterxturns) | Block | Event Trigger: Applies a status effect after X turns have passed. | 1 |
| [`StatusOnDie`](./Characters_and_Bosses.md#context-statusondie) | Block | Event Trigger: Applies statuses when the character dies. | 1 |
| [`StatusOnEndMove`](./Characters_and_Bosses.md#context-statusonendmove) | Block | Event Trigger: Applies statuses when the character finishes moving. | 1 |
| [`StatusOnGainCoins`](./Characters_and_Bosses.md#context-statusongaincoins) | Block | Event Trigger: Applies statuses when coins are collected. | 1 |

</details>

---

### Context: `properties` (600 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 505 |
| `health` | Number |  | 427 |
| [`tag`](./Arrays.md#array-tag) | Array | Specific entity tag required. | 399 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 280 |
| `movement` | Number |  | 278 |
| `corpse_health` | Number |  | 195 |
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
| [`layer`](./Enums.md#enum-layer) | Enum |  | 17 |
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

### Context: `ai` (583 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`0`](./Characters_and_Bosses.md#context-0), [`1`](./Characters_and_Bosses.md#context-1), [`2`](./Characters_and_Bosses.md#context-2), [`3`](./Characters_and_Bosses.md#context-3), [`4`](./Characters_and_Bosses.md#context-4), [`Alert`](./Characters_and_Bosses.md#context-alert), [`Angry`](./Characters_and_Bosses.md#context-angry), [`Attacker`](./Characters_and_Bosses.md#context-attacker), [`BellyFull`](./Characters_and_Bosses.md#context-bellyfull), [`Bishop`](./Characters_and_Bosses.md#context-bishop), [`BlackHole`](./Characters_and_Bosses.md#context-blackhole), [`Bully`](./Characters_and_Bosses.md#context-bully), [`CaveBaby`](./Characters_and_Bosses.md#context-cavebaby), [`CaveMan`](./Characters_and_Bosses.md#context-caveman), [`CaveManSpear`](./Characters_and_Bosses.md#context-cavemanspear), [`CaveWoman`](./Characters_and_Bosses.md#context-cavewoman), [`CaveWomanHasCat`](./Characters_and_Bosses.md#context-cavewomanhascat), [`Charging`](./Characters_and_Bosses.md#context-charging), [`Cultist`](./Characters_and_Bosses.md#context-cultist), [`Damaged`](./Characters_and_Bosses.md#context-damaged), [`Default`](./Characters_and_Bosses.md#context-default), [`Default_Ceiling`](./Characters_and_Bosses.md#context-default_ceiling), [`Default_Ground`](./Characters_and_Bosses.md#context-default_ground), [`DesireMech`](./Characters_and_Bosses.md#context-desiremech), [`Down`](./Characters_and_Bosses.md#context-down), [`DualSword`](./Characters_and_Bosses.md#context-dualsword), [`DualSword_Primed`](./Characters_and_Bosses.md#context-dualsword_primed), [`Explody`](./Characters_and_Bosses.md#context-explody), [`FightPhase`](./Characters_and_Bosses.md#context-fightphase), [`Fire`](./Characters_and_Bosses.md#context-fire), [`FireFull`](./Characters_and_Bosses.md#context-firefull), [`Flop`](./Characters_and_Bosses.md#context-flop), [`Flop2`](./Characters_and_Bosses.md#context-flop2), [`Flush`](./Characters_and_Bosses.md#context-flush), [`FlushBubs`](./Characters_and_Bosses.md#context-flushbubs), [`FlushHost`](./Characters_and_Bosses.md#context-flushhost), [`FlushNettle`](./Characters_and_Bosses.md#context-flushnettle), [`Full`](./Characters_and_Bosses.md#context-full), [`Grown`](./Characters_and_Bosses.md#context-grown), [`Guarding`](./Characters_and_Bosses.md#context-guarding), [`HalfDead`](./Characters_and_Bosses.md#context-halfdead), [`HasCat`](./Characters_and_Bosses.md#context-hascat), [`HasDeadCat`](./Characters_and_Bosses.md#context-hasdeadcat), [`HasRock`](./Characters_and_Bosses.md#context-hasrock), [`Headless`](./Characters_and_Bosses.md#context-headless), [`Holding`](./Characters_and_Bosses.md#context-holding), [`InitialPhase`](./Characters_and_Bosses.md#context-initialphase), [`Insane_Ceiling`](./Characters_and_Bosses.md#context-insane_ceiling), [`Insane_Ground`](./Characters_and_Bosses.md#context-insane_ground), [`Johnny`](./Characters_and_Bosses.md#context-johnny), [`JohnnyBubs`](./Characters_and_Bosses.md#context-johnnybubs), [`JohnnyHost`](./Characters_and_Bosses.md#context-johnnyhost), [`JohnnyNettle`](./Characters_and_Bosses.md#context-johnnynettle), [`MouthFull`](./Characters_and_Bosses.md#context-mouthfull), [`Mutant`](./Characters_and_Bosses.md#context-mutant), [`NeutronStar`](./Characters_and_Bosses.md#context-neutronstar), [`NoStick`](./Characters_and_Bosses.md#context-nostick), [`Normal`](./Characters_and_Bosses.md#context-normal), [`NormalFull`](./Characters_and_Bosses.md#context-normalfull), [`Nuke`](./Characters_and_Bosses.md#context-nuke), [`OffMap`](./Characters_and_Bosses.md#context-offmap), [`Open`](./Characters_and_Bosses.md#context-open), [`Primed`](./Characters_and_Bosses.md#context-primed), [`ROOT`](./Characters_and_Bosses.md#context-root), [`Rage`](./Characters_and_Bosses.md#context-rage), [`Rain`](./Characters_and_Bosses.md#context-rain), [`Sitting`](./Characters_and_Bosses.md#context-sitting), [`SquirrelForm`](./Characters_and_Bosses.md#context-squirrelform), [`Standing`](./Characters_and_Bosses.md#context-standing), [`Standing2`](./Characters_and_Bosses.md#context-standing2), [`SwordAndShield`](./Characters_and_Bosses.md#context-swordandshield), [`SwordAndShield_Primed`](./Characters_and_Bosses.md#context-swordandshield_primed), [`Tar`](./Characters_and_Bosses.md#context-tar), [`TarFull`](./Characters_and_Bosses.md#context-tarfull), [`Throb`](./Characters_and_Bosses.md#context-throb), [`ThrobBubs`](./Characters_and_Bosses.md#context-throbbubs), [`ThrobHost`](./Characters_and_Bosses.md#context-throbhost), [`ThrobNettle`](./Characters_and_Bosses.md#context-throbnettle), [`Transformed`](./Characters_and_Bosses.md#context-transformed), [`Turtled`](./Characters_and_Bosses.md#context-turtled), [`Unwashed`](./Characters_and_Bosses.md#context-unwashed), [`Up`](./Characters_and_Bosses.md#context-up), [`Washed`](./Characters_and_Bosses.md#context-washed), [`Washer`](./Characters_and_Bosses.md#context-washer), [`WereMan`](./Characters_and_Bosses.md#context-wereman), [`Zealot`](./Characters_and_Bosses.md#context-zealot), [`ZealotBomb`](./Characters_and_Bosses.md#context-zealotbomb)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 578 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 498 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 495 |
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
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`dice_abilities`](./Arrays.md#array-dice_abilities) | Array |  | 1 |
| `never_hit_ally_corpses` | Boolean |  | 1 |
| [`post_absorb_move_weights`](./Enums.md#enum-post_absorb_move_weights) | Enum |  | 1 |
| `reset_pattern_on_round_begin` | Boolean |  | 1 |
| [`roll_ability`](./Enums.md#enum-roll_ability) | Enum |  | 1 |
| [`round_start_bonusturn_pattern`](./Characters_and_Bosses.md#context-round_start_bonusturn_pattern) | Block | AI Logic: Ability usage pattern during round-start bonus turns. | 1 |

</details>

---

### Context: `graphics` (558 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

> **Engine Schema:** This block is a `[graphic_block]` container. [View all confirmed values in Engine_Graphics.md](./Engine_Graphics.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[graphic_block]`](./Engine_Graphics.md#all-confirmed-graphic-block-values) | Block | A visual/animation configuration. See Engine_Graphics.md for the full schema. |
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

### Context: `abilities` (458 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 436 |
| [`move`](./Enums.md#enum-move) | Enum |  | 433 |
| [`spells`](./Arrays.md#array-spells) | Array |  | 381 |
| `can_get_bonus` | Boolean |  | 30 |

</details>

---

### Context: `stats` (388 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

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

### Context: `pattern` (296 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ReplaceBrain`](./Characters_and_Bosses.md#context-replacebrain), [`ai`](./Characters_and_Bosses.md#context-ai), [`ai_if_spawned_as_enemy`](./Characters_and_Bosses.md#context-ai_if_spawned_as_enemy)

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

### Context: `FormChanger` (106 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`initial_form`](./Enums.md#enum-initial_form) | Enum |  | 59 |
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

### Context: `SpawnOnDeath` (79 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 3 |
| [`obj`](./Arrays.md#array-obj) | Array |  | 3 |
| [`additional_statuses`](./Characters_and_Bosses.md#context-additional_statuses) | Block | Generic statuses added to the character. | 1 |

</details>

---

### Context: `sound` (62 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

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

### Context: `turns` (45 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Bishop`](./Characters_and_Bosses.md#context-bishop), [`Bully`](./Characters_and_Bosses.md#context-bully), [`Default`](./Characters_and_Bosses.md#context-default), [`Default_Ceiling`](./Characters_and_Bosses.md#context-default_ceiling), [`Default_Ground`](./Characters_and_Bosses.md#context-default_ground), [`FightPhase`](./Characters_and_Bosses.md#context-fightphase), [`Holding`](./Characters_and_Bosses.md#context-holding), [`InitialPhase`](./Characters_and_Bosses.md#context-initialphase), [`Insane_Ceiling`](./Characters_and_Bosses.md#context-insane_ceiling), [`Insane_Ground`](./Characters_and_Bosses.md#context-insane_ground), [`LastHit`](./Characters_and_Bosses.md#context-lasthit), [`Lifted`](./Characters_and_Bosses.md#context-lifted), [`Mutant`](./Characters_and_Bosses.md#context-mutant), [`Normal`](./Characters_and_Bosses.md#context-normal), [`NotPriming`](./Characters_and_Bosses.md#context-notpriming), [`Nuke`](./Characters_and_Bosses.md#context-nuke), [`OffMap`](./Characters_and_Bosses.md#context-offmap), [`OffScreen`](./Characters_and_Bosses.md#context-offscreen), [`OneAlive`](./Characters_and_Bosses.md#context-onealive), [`Possessing`](./Characters_and_Bosses.md#context-possessing), [`Priming`](./Characters_and_Bosses.md#context-priming), [`Pulp2`](./Characters_and_Bosses.md#context-pulp2), [`Pulp3`](./Characters_and_Bosses.md#context-pulp3), [`Pulp4`](./Characters_and_Bosses.md#context-pulp4), [`Pulp5`](./Characters_and_Bosses.md#context-pulp5), [`Pulp6`](./Characters_and_Bosses.md#context-pulp6), [`Pulp7`](./Characters_and_Bosses.md#context-pulp7), [`Rage`](./Characters_and_Bosses.md#context-rage), [`Sitting`](./Characters_and_Bosses.md#context-sitting), [`SpawningPhase`](./Characters_and_Bosses.md#context-spawningphase), [`Standing`](./Characters_and_Bosses.md#context-standing), [`Standing2`](./Characters_and_Bosses.md#context-standing2), [`TwoAlive`](./Characters_and_Bosses.md#context-twoalive)

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

### Context: `equipment` (44 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`face`](./Enums.md#enum-face) | Enum |  | 16 |
| [`head`](./Enums.md#enum-head) | Enum |  | 14 |
| [`neck`](./Enums.md#enum-neck) | Enum |  | 10 |
| [`weapon`](./Enums.md#enum-weapon) | Enum | Weapon item constraint. | 7 |

</details>

---

### Context: `mainturn_pattern` (44 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum |  | 23 |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 9 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 8 |
| [`do_strict`](./Arrays.md#array-do_strict) | Array |  | 2 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum |  | 2 |

</details>

---

### Context: `Default` (37 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 24 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 10 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |

</details>

---

### Context: `FormChangeWhileHasStatus` (35 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 35 |
| [`form_hasnot`](./Enums.md#enum-form_hasnot) | Enum |  | 30 |
| [`form_has`](./Enums.md#enum-form_has) | Enum |  | 25 |

</details>

---

### Context: `virtual_abilities` (35 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count |
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

### Context: `AddStatusToBasicAttack` (32 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#context-randompassivepool), [`StacyMutant_Counter`](./Characters_and_Bosses.md#context-stacymutant_counter), [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `bonusturn_pattern` (27 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum |  | 19 |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 11 |
| [`do_strict`](./Arrays.md#array-do_strict) | Array |  | 5 |
| [`do_all`](./Arrays.md#array-do_all) | Array |  | 4 |
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum |  | 1 |

</details>

---

### Context: `CatPartsTransform` (25 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveGroup`](./Characters_and_Bosses.md#context-passivegroup), [`StacyMutant_Brace`](./Characters_and_Bosses.md#context-stacymutant_brace), [`StacyMutant_Counter`](./Characters_and_Bosses.md#context-stacymutant_counter), [`StacyMutant_Damage`](./Characters_and_Bosses.md#context-stacymutant_damage), [`StacyMutant_DoubleHead`](./Characters_and_Bosses.md#context-stacymutant_doublehead), [`StacyMutant_Fire`](./Characters_and_Bosses.md#context-stacymutant_fire), [`StacyMutant_Health`](./Characters_and_Bosses.md#context-stacymutant_health), [`StacyMutant_Holy`](./Characters_and_Bosses.md#context-stacymutant_holy), [`StacyMutant_Ice`](./Characters_and_Bosses.md#context-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#context-stacymutant_lightning), [`StacyMutant_Mirror`](./Characters_and_Bosses.md#context-stacymutant_mirror), [`StacyMutant_Speed`](./Characters_and_Bosses.md#context-stacymutant_speed), [`StacyMutant_Thorns`](./Characters_and_Bosses.md#context-stacymutant_thorns), [`passives`](./Characters_and_Bosses.md#context-passives)

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

### Context: `fallback` (23 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

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

### Context: `BossRewards` (20 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`common`](./Enums.md#enum-common) | Enum |  | 20 |
| [`rare`](./Enums.md#enum-rare) | Enum |  | 16 |

</details>

---

### Context: `MeleeRevengeDamage` (19 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#context-temppassiveuntilsettled), [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| `damage` | Number | The base damage properties of an attack. | 11 |
| [`effects`](./Characters_and_Bosses.md#context-effects) | Block | Non-damaging impact triggers. | 11 |
| `knockback` | Number |  | 9 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 8 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 5 |
| `cant_miss` | Boolean |  | 1 |

</details>

---

### Context: `BirdRewards` (18 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ally_rewards`](./Characters_and_Bosses.md#context-ally_rewards) | Block | Loot logic triggered if an ally dies. | 18 |
| [`statuses`](./Characters_and_Bosses.md#context-statuses) | Block | Status effects possessed by the character. | 5 |

</details>

---

### Context: `ally_rewards` (18 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BirdRewards`](./Characters_and_Bosses.md#context-birdrewards)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum | Generates an item drop from the specified loot pool. | 16 |
| [`Conditional_GoodRoll`](./Characters_and_Bosses.md#context-conditional_goodroll) | Block | Conditional: Executes logic on a good RNG roll. | 2 |
| [`RandomStatusFromPool`](./Characters_and_Bosses.md#context-randomstatusfrompool) | Block | Logic: Applies a random status from the pool. | 1 |

</details>

---

### Context: `alt_spawn_pool` (18 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

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

### Context: `CharacterLightSource` (16 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`color`](./Arrays.md#array-color) | Array |  | 16 |
| `size` | Number |  | 16 |
| [`glow`](./Arrays.md#array-glow) | Array |  | 8 |

</details>

---

### Context: `HealthPickup` (16 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array |  | 15 |
| `stacks` | Number | Number of stacks or intensity to apply. | 15 |
| `stored_food_value` | Number |  | 15 |
| `anything_eats` | Boolean |  | 4 |
| `force_frame` | Number |  | 1 |

</details>

---

### Context: `ImmediateAbilityReaction` (13 instances)

<details>
<summary><b>Expand</b></summary>

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

### Context: `effects` (13 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Characters_and_Bosses.md#context-meleerevengedamage), [`damage_instance`](./Characters_and_Bosses.md#context-damage_instance), [`eat_damage`](./Characters_and_Bosses.md#context-eat_damage)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `AbilityHealthThreshold` (12 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 12 |
| [`threshold`](./Enums.md#enum-threshold) | Enum |  | 11 |
| `even_if_stunned` | Boolean |  | 6 |
| `immediate` | Boolean |  | 5 |
| `use_ai` | Boolean |  | 2 |
| `also_use_if_buddy_is_dead` | Boolean |  | 1 |
| [`threshold_min`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `PassiveGroup` (12 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#context-randompassivepool)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |

</details>

---

### Context: `SpawnThingOnDamage` (12 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

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

### Context: `round_end_bonusturn_pattern` (12 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

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

### Context: `Normal` (11 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 10 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 5 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `DeathRattleRevive` (10 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 8 |
| `even_if_stunned` | Boolean |  | 8 |

</details>

---

### Context: `Rage` (10 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 8 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 6 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 6 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 4 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| `move_speed_multiplier` | Number |  | 1 |

</details>

---

### Context: `AbilityReaction` (9 instances)

<details>
<summary><b>Expand</b></summary>

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

### Context: `FormChangeOnElementInfluence` (9 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 9 |
| [`form`](./Enums.md#enum-form) | Enum |  | 9 |
| [`exclude`](./Enums.md#enum-exclude) | Enum |  | 5 |
| [`particle`](./Enums.md#enum-particle) | Enum |  | 5 |
| [`sfx`](./Enums.md#enum-sfx) | Enum |  | 5 |

</details>

---

### Context: `StatusCollector` (9 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. | 7 |
| `Poison` | Number | Applies or references the 'Poison' effect/state. | 4 |
| `Slow` | Number | Applies or references the 'Slow' effect/state. | 4 |

</details>

---

### Context: `TransformInXTurns` (9 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#context-randompassivepool), [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array |  | 8 |
| `stacks` | Number | Number of stacks or intensity to apply. | 8 |
| [`initiative`](./Enums.md#enum-initiative) | Enum |  | 4 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |
| [`turns`](./Arrays.md#array-turns) | Array | Turn counter tracking. | 1 |

</details>

---

### Context: `TransformOnElementInfluence` (9 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 9 |
| [`object`](./Enums.md#enum-object) | Enum |  | 9 |

</details>

---

### Context: `statuses` (9 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BirdRewards`](./Characters_and_Bosses.md#context-birdrewards), [`Cat`](./Characters_and_Bosses.md#context-cat), [`NonCat`](./Characters_and_Bosses.md#context-noncat)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`Consumed`](./Characters_and_Bosses.md#context-consumed) | Block | State triggered when the entity is eaten/consumed. | 4 |

</details>

---

### Context: `DeathRattle` (8 instances)

<details>
<summary><b>Expand</b></summary>

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

### Context: `FormChangeOffMap` (8 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_offmap`](./Enums.md#enum-form_offmap) | Enum |  | 8 |
| [`form_onmap`](./Enums.md#enum-form_onmap) | Enum |  | 8 |

</details>

---

### Context: `ChanceToSpitOnDamage` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 7 |
| `flat_chance` | Number |  | 5 |
| `chance_per_damage` | Number |  | 3 |
| `backstabs_only` | Boolean |  | 1 |
| `even_on_0_damage_if_knockback` | Boolean |  | 1 |

</details>

---

### Context: `MoveWhenDamaged` (7 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 7 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 1 |

</details>

---

### Context: `MovementReaction` (7 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

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

### Context: `ReflectProjectiles` (7 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `self_damage` | Number | Recoil or self-inflicted damage/effects applied to the caster. | 7 |

</details>

---

### Context: `CaveFamilyEnrage` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 6 |
| `count` | Number | The numerical quantity. | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 6 |

</details>

---

### Context: `FormChangeWhilePrimingAbility` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`not_priming`](./Enums.md#enum-not_priming) | Enum |  | 6 |
| [`priming`](./Enums.md#enum-priming) | Enum |  | 6 |

</details>

---

### Context: `MoveTowardsDamageSource` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

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

### Context: `SecurityBotProtect` (6 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 5 |
| `enemies_only` | Boolean |  | 3 |
| [`move`](./Enums.md#enum-move) | Enum |  | 3 |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum |  | 3 |
| `not_on_kill` | Boolean |  | 2 |

</details>

---

### Context: `HasCat` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 5 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 5 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 4 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 4 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |

</details>

---

### Context: `PassiveWhileHasStatus` (5 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 5 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 5 |

</details>

---

### Context: `BaitAura` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `range` | Number | Distance or area of effect in tiles. | 4 |

</details>

---

### Context: `Consumed` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`statuses`](./Characters_and_Bosses.md#context-statuses)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| `do_not_pop_corpse` | Boolean |  | 4 |
| [`drop_on_death`](./Enums.md#enum-drop_on_death) | Enum |  | 4 |
| `force_contact` | Boolean | If true, enforces physical overlap. | 4 |
| `instant` | Boolean |  | 4 |
| [`mount_mode`](./Enums.md#enum-mount_mode) | Enum | If true, treats the consumption as riding/mounting instead of eating. | 4 |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Ability triggered by the consumed entity while inside the consumer. | 4 |
| `use_placeholder` | Boolean |  | 2 |

</details>

---

### Context: `MoveAway` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 4 |

</details>

---

### Context: `MoveClose` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 4 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 3 |

</details>

---

### Context: `OffMap` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 3 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `SmallRockBehavior` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 4 |
| `knockback` | Number |  | 4 |
| `chain` | Boolean |  | 2 |

</details>

---

### Context: `StatusEachTurnEnd` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |

</details>

---

### Context: `StatusOnKill` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnTookDamageFromAbility` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `TransformOnDeathImmediately` (4 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum |  | 4 |
| [`obj`](./Enums.md#enum-obj) | Enum |  | 4 |

</details>

---

### Context: `Trapper` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 |
| `cancel_movement` | Boolean |  | 2 |
| `pathfinding_avoidance` | Number |  | 2 |
| `range` | Number | Distance or area of effect in tiles. | 2 |

</details>

---

### Context: `default` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |

</details>

---

### Context: `hot` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 4 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 4 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 4 |

</details>

---

### Context: `keyword_tooltips` (4 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Die`](./Characters_and_Bosses.md#context-die), [`Dumb`](./Characters_and_Bosses.md#context-dumb), [`Obey`](./Characters_and_Bosses.md#context-obey), [`Stop`](./Characters_and_Bosses.md#context-stop)

> **Engine Schema:** This block is a `[keyword_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[keyword_id]`](./Engine_Statuses.md#all-confirmed-keyword-id-values) | String | A Status or Keyword ID whose tooltip text is defined here. See Engine_Statuses.md for all IDs. |

</details>

---

### Context: `AllAlive` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |

</details>

---

### Context: `ArmorPickup` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array |  | 3 |
| `stacks` | Number | Number of stacks or intensity to apply. | 3 |

</details>

---

### Context: `Buddy` (3 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 3 |
| [`obj`](./Enums.md#enum-obj) | Enum |  | 3 |
| `reclaim_if_lost` | Boolean |  | 1 |

</details>

---

### Context: `Cat` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#context-mothertumorpassive), [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#context-mothertumorspawnincapture)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum |  | 3 |
| [`statuses`](./Characters_and_Bosses.md#context-statuses) | Block | Status effects possessed by the character. | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |

</details>

---

### Context: `Down` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |

</details>

---

### Context: `FormChangeHealthThreshold` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_above`](./Enums.md#enum-form_above) | Enum |  | 3 |
| [`form_below`](./Enums.md#enum-form_below) | Enum |  | 3 |
| [`threshold`](./Math_Equations.md) | Equation |  | 3 |
| `count_shield` | Boolean |  | 1 |

</details>

---

### Context: `Full` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| [`statuses_on_enter_form`](./Characters_and_Bosses.md#context-statuses_on_enter_form) | Block | Status effects instantly applied upon transitioning into this form. | 2 |

</details>

---

### Context: `ManaPickup` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array |  | 3 |
| `stacks` | Number | Number of stacks or intensity to apply. | 3 |

</details>

---

### Context: `MoveTowardsKillers` (3 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`character_filter`](./Arrays.md#array-character_filter) | Array |  | 3 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 3 |

</details>

---

### Context: `NonCat` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#context-mothertumorpassive), [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#context-mothertumorspawnincapture)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum |  | 3 |
| [`statuses`](./Characters_and_Bosses.md#context-statuses) | Block | Status effects possessed by the character. | 2 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |

</details>

---

### Context: `OneAlive` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 3 |

</details>

---

### Context: `RandomPassivePool` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`PassiveGroup`](./Characters_and_Bosses.md#context-passivegroup) | Block | Passive: A collection of passives grouped together for easier management. | 12 |
| [`AddStatusToBasicAttack`](./Characters_and_Bosses.md#context-addstatustobasicattack) | Block | Modifier: Injects a status effect payload into the character's basic attacks. | 10 |

</details>

---

### Context: `ReplaceBrain` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StacyMutant_Fire`](./Characters_and_Bosses.md#context-stacymutant_fire), [`StacyMutant_Ice`](./Characters_and_Bosses.md#context-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#context-stacymutant_lightning)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 3 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 3 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 3 |
| [`pattern`](./Characters_and_Bosses.md#context-pattern) | Block | AI sequence logic. | 3 |

</details>

---

### Context: `TwoAlive` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 3 |

</details>

---

### Context: `Up` (3 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 3 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `AbilityOnRoundEnd` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| `force_display_name` | Boolean |  | 2 |

</details>

---

### Context: `AbilityWhenTaggedCharacterMovesNear` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| `range` | Number | Distance or area of effect in tiles. | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 2 |

</details>

---

### Context: `AddTemporaryEffectsToBasicAttack` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Fury` | Number | Applies or references the 'Fury' effect/state. | 2 |

</details>

---

### Context: `AutocastEachRound` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 1 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 1 |

</details>

---

### Context: `Big` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Boris` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `BungaEntrance` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| `even_if_stunned` | Boolean |  | 2 |
| `health_threshold` | Number |  | 2 |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum |  | 2 |

</details>

---

### Context: `CaveMan` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `CaveManSpear` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `CherubimReaction` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Leave`](./Enums.md#enum-leave) | Enum | Applies or references the 'Leave' effect/state. | 2 |
| [`Return`](./Enums.md#enum-return) | Enum | Applies or references the 'Return' effect/state. | 2 |

</details>

---

### Context: `Conditional_GoodRoll` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ally_rewards`](./Characters_and_Bosses.md#context-ally_rewards)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 2 |

</details>

---

### Context: `DashRandomly` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 2 |

</details>

---

### Context: `DiesToElement` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 1 |
| `instant` | Boolean |  | 1 |

</details>

---

### Context: `Empty` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |

</details>

---

### Context: `Escape` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Context: `Explosive` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `ForceUseAbility` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| `show_name` | Boolean |  | 2 |

</details>

---

### Context: `FormChangeDuringWeatherElement` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 2 |
| [`form`](./Enums.md#enum-form) | Enum |  | 2 |

</details>

---

### Context: `Holding` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Holy` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `KnockUpAndAway` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#context-conditional_isphysicalattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `displace` | Boolean |  | 2 |
| `distance` | Number | The distance in tiles to knock the target away. | 2 |
| `self_damage` | Boolean | Recoil or self-inflicted damage/effects applied to the caster. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>

---

### Context: `MotherTumorSpawnInCapture` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Cat`](./Characters_and_Bosses.md#context-cat) | Block | Character Form: Base form for standard cats. | 2 |
| [`NonCat`](./Characters_and_Bosses.md#context-noncat) | Block | Character Form: Behavior and stats for the 'NonCat' state. | 2 |
| [`Nothing`](./Characters_and_Bosses.md#context-nothing) | Block | Character Form: Behavior and stats for the 'Nothing' state. | 1 |

</details>

---

### Context: `MoveCenter` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Context: `MoveForThrow` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Context: `NotPriming` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `PassiveWhileNotHasStatus` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 2 |

</details>

---

### Context: `Priming` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 2 |

</details>

---

### Context: `ProtectTargetedAllies` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`target_filter`](./Enums.md#enum-target_filter) | Enum |  | 2 |

</details>

---

### Context: `Rain` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |

</details>

---

### Context: `RemoveStatusStacks` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Characters_and_Bosses.md#context-statusonendmove), [`StatusOnTookDamage`](./Characters_and_Bosses.md#context-statusontookdamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks to remove. | 2 |
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 2 |

</details>

---

### Context: `Robot` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alternate_energized_effect`](./Characters_and_Bosses.md#context-alternate_energized_effect) | Block | Overrides default energized visuals. | 2 |

</details>

---

### Context: `SlotMachineRollPool` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SlotResult_Jackpot_Coins` | Number | Applies or references the 'SlotResult_Jackpot_Coins' effect/state. | 2 |
| `SlotResult_Explode` | Number | Applies or references the 'SlotResult_Explode' effect/state. | 1 |
| `SlotResult_Nothing` | Number | Applies or references the 'SlotResult_Nothing' effect/state. | 1 |
| `SlotResult_RandomPickup` | Number | Applies or references the 'SlotResult_RandomPickup' effect/state. | 1 |

</details>

---

### Context: `Small` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Context: `SpearRun` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 2 |

</details>

---

### Context: `SquirrelForm` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 1 |

</details>

---

### Context: `StatusGroup` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Characters_and_Bosses.md#context-randomstatusfrompool)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnSpawnIn` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 1 |
| `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. | 1 |

</details>

---

### Context: `StatusOnTookDamage` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `SupportFormChangeInsteadOfRun` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 |
| `wait_till_turn` | Boolean |  | 1 |

</details>

---

### Context: `TempPassiveUntilSettled` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#context-conditional_isphysicalattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`MeleeRevengeDamage`](./Characters_and_Bosses.md#context-meleerevengedamage) | Block | Reaction: Deals damage or status effects to an attacker upon receiving melee damage. | 2 |

</details>

---

### Context: `TinkererBasicAttackSwitching` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveGroup`](./Characters_and_Bosses.md#context-passivegroup), [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum |  | 2 |
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum |  | 2 |

</details>

---

### Context: `TransformOnElementInfluencex` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 2 |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |

</details>

---

### Context: `Turtled` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| [`move`](./Enums.md#enum-move) | Enum |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |

</details>

---

### Context: `active` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |

</details>

---

### Context: `alternate_energized_effect` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Robot`](./Characters_and_Bosses.md#context-robot)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`FormChange`](./Enums.md#enum-formchange) | Enum | Transforms the character into a different state or form (e.g., Rage, HasCat). | 1 |
| `SpellDamageUp` | Number | Applies or references the 'SpellDamageUp' effect/state. | 1 |

</details>

---

### Context: `dispersed_bonusturn_pattern` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum |  | 3 |

</details>

---

### Context: `passive` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |

</details>

---

### Context: `statuses_on_enter_form` (2 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Full`](./Characters_and_Bosses.md#context-full)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`UseAbility`](./Enums.md#enum-useability) | Enum | Logic: Forces execution of an ability. | 2 |

</details>

---

### Context: `AddStatusToReceivedDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#context-conditional_isphysicalattack) | Block | Conditional: Executes logic if the triggering attack is physical. | 1 |
| [`Else`](./Characters_and_Bosses.md#context-else) | Block | Fallback logic block for conditionals. | 1 |

</details>

---

### Context: `AddStatusToSpells` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `AddStatusToTrampleDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Characters_and_Bosses.md#context-passivewhendead)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `AddStatusToWeapons` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `AdventureTokenPassivePool` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |

</details>

---

### Context: `AggroTargetIsGovernedByHitEffect` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean |  | 1 |

</details>

---

### Context: `Alert` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `AllStatsAura` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`aura_requires_tag`](./Enums.md#enum-aura_requires_tag) | Enum |  | 1 |
| [`range`](./Enums.md#enum-range) | Enum | Distance or area of effect in tiles. | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `Angry` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |

</details>

---

### Context: `Attacker` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `BackflipWhenTargeted` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnGainCoins`](./Characters_and_Bosses.md#context-statusongaincoins)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific dodge ability to trigger (e.g., DestroyerDodge). | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `BattlefieldUniqueRandomPassive` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Number | Applies or references the 'DemonicGlyph_Bite' effect/state. | 1 |
| `DemonicGlyph_Bounce` | Number | Applies or references the 'DemonicGlyph_Bounce' effect/state. | 1 |
| `DemonicGlyph_Fire` | Number | Applies or references the 'DemonicGlyph_Fire' effect/state. | 1 |
| `DemonicGlyph_Movement` | Number | Applies or references the 'DemonicGlyph_Movement' effect/state. | 1 |
| `DemonicGlyph_Summon` | Number | Applies or references the 'DemonicGlyph_Summon' effect/state. | 1 |

</details>

---

### Context: `BellyFull` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `BigHolding` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `BigHoldingCat` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Bishop` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `BlackHole` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `Bomb` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Bully` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `BungaCheers` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ally_damage`](./Enums.md#enum-ally_damage) | Enum |  | 1 |
| [`ally_dead`](./Enums.md#enum-ally_dead) | Enum |  | 1 |
| [`enemy_damage`](./Enums.md#enum-enemy_damage) | Enum |  | 1 |
| [`enemy_dead`](./Enums.md#enum-enemy_dead) | Enum |  | 1 |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum |  | 1 |

</details>

---

### Context: `CaveBaby` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `CaveWoman` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `CaveWomanHasCat` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `CerberubsAggroTargetBehavior` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alert_form`](./Enums.md#enum-alert_form) | Enum |  | 1 |
| [`default_form`](./Enums.md#enum-default_form) | Enum |  | 1 |

</details>

---

### Context: `CerberubsJumpBlind` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |

</details>

---

### Context: `CerberubsJumpNormal` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |

</details>

---

### Context: `ChanceToBackflip` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| `chance` | Number | Probability (0.0 to 1.0) of executing this action. | 1 |

</details>

---

### Context: `ChanceToFormChangeOnAbilityDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0) of executing this action. | 1 |
| [`form`](./Enums.md#enum-form) | Enum |  | 1 |

</details>

---

### Context: `ChaosBossFormChangeGuide` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array |  | 1 |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array |  | 1 |
| `passives_health_threshold` | Number |  | 1 |

</details>

---

### Context: `ChaosBossPieces` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array |  | 1 |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array |  | 1 |

</details>

---

### Context: `ChaosHeadDropIn` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`new_music`](./Enums.md#enum-new_music) | Enum |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 1 |

</details>

---

### Context: `Charging` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Close` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `CloseConvert` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `Conditional_BadRoll` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Characters_and_Bosses.md#context-statuseachturnend)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 1 |

</details>

---

### Context: `Conditional_HasKnockback` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Characters_and_Bosses.md#context-else)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `Conditional_IsPhysicalAttack` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#context-addstatustoreceiveddamage)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |

</details>

---

### Context: `CounterAttack` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| `without_orienting` | Boolean |  | 1 |

</details>

---

### Context: `CreateGlobalModifiers` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[global_modifier_id]` container. [View all confirmed values in Engine_GlobalModifiers.md](./Engine_GlobalModifiers.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[global_modifier_id]`](./Engine_GlobalModifiers.md#all-confirmed-global-modifier-id-values) | Boolean | Any valid Global Modifier ID. See Engine_GlobalModifiers.md. |

</details>

---

### Context: `Cultist` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `Damaged` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `Default_Ceiling` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Default_Ground` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `DelayedAutoRevive` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 1 |
| `rounds` | Number |  | 1 |

</details>

---

### Context: `DesireMech` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `DiceBehavior` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dice_size` | Number |  | 1 |
| `knockback_damage` | Number |  | 1 |

</details>

---

### Context: `Die` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `DiesToPiercingAndSpikes` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `deferred` | Boolean |  | 1 |

</details>

---

### Context: `DodgeWhenTargeted` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |

</details>

---

### Context: `Drunker` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |

</details>

---

### Context: `DualSword` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| `move_speed_multiplier` | Number |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `DualSword_Primed` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| `move_speed_multiplier` | Number |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `Dumb` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `DybbukPossessionFallback` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum |  | 1 |
| [`form`](./Enums.md#enum-form) | Enum |  | 1 |

</details>

---

### Context: `Else` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#context-addstatustoreceiveddamage)

> **Engine Schema:** This block is a `[effect_block]` container. [View all confirmed values in Engine_Effects.md](./Engine_Effects.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect-block-values) | Block | Any valid effect. See Engine_Effects.md for the full list. |
| [`[effect_block]`](./Engine_Effects.md#all-confirmed-effect_block-values) | Block | Evaluates the nested condition before applying. |

</details>

---

### Context: `Explody` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `FaceAwayLastDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean |  | 1 |
| `override_hit_animation` | Boolean |  | 1 |
| `use_turn_animations` | Boolean |  | 1 |

</details>

---

### Context: `FaceLastDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean |  | 1 |

</details>

---

### Context: `FightPhase` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `FinalBossBeamQueue` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`queue`](./Enums.md#enum-queue) | Enum |  | 1 |
| [`release`](./Enums.md#enum-release) | Enum |  | 1 |
| [`transform`](./Enums.md#enum-transform) | Enum |  | 1 |

</details>

---

### Context: `FinalBossBecomeTheChild` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | Applies or references the 'GlobalSpawnCharacter' effect/state. | 1 |
| `PlayBackground` | Number | Applies or references the 'PlayBackground' effect/state. | 1 |
| [`SwitchMusic`](./Characters_and_Bosses.md#context-switchmusic) | Block | Event Trigger: Changes background music track. | 1 |

</details>

---

### Context: `FinalBossHitCountdownBoris` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | Logic: Forces the execution of a specific ability. | 2 |
| `icon` | Number |  | 1 |
| `icon_ready` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `FinalBossHitCountdownExplosive` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | Logic: Forces the execution of a specific ability. | 2 |
| `icon` | Number |  | 1 |
| `icon_ready` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `FinalBossHitCountdownHoly` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `icon` | Number |  | 1 |
| `icon_ready` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `FinalBossPupils` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

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

### Context: `FinalBossShieldHealth` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`break_ability`](./Enums.md#enum-break_ability) | Enum |  | 1 |
| [`state_health`](./Arrays.md#array-state_health) | Array |  | 1 |

</details>

---

### Context: `FinalBossSyncAnimations` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`other_character`](./Enums.md#enum-other_character) | Enum |  | 1 |
| [`other_form_change_abilities`](./Characters_and_Bosses.md#context-other_form_change_abilities) | Block | Lists secondary abilities used to change forms. | 1 |

</details>

---

### Context: `Fire` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `FireFull` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Flop` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Flop2` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Flush` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `FlushBubs` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `FlushHost` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `FlushNettle` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `FoodMove` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `ForceTrample` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |

</details>

---

### Context: `GainDisorderFromPool` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Characters_and_Bosses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0) of executing this action. | 1 |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 1 |

</details>

---

### Context: `Grappling` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit_animations`](./Characters_and_Bosses.md#context-exit_animations) | Block | Animations played when leaving a form/state. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |

</details>

---

### Context: `Grown` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| `uifloaters_offset` | Number |  | 1 |
| `weak_threshold` | Number |  | 1 |

</details>

---

### Context: `GuaranteedJackpot` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Guarding` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `HPAltStates` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`clipname`](./Enums.md#enum-clipname) | Enum |  | 1 |
| [`thresholds`](./Arrays.md#array-thresholds) | Array |  | 1 |

</details>

---

### Context: `HalfDead` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `HasDeadCat` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `HasRock` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Context: `Headless` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `HealNeighborsEachTurn` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `Hint_CrackedVisuals` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Context: `Hint_CrackedVisuals2` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Context: `Hint_CrackedVisuals3` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Context: `HitlerExecute` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 1 |
| `threshold` | Number |  | 1 |

</details>

---

### Context: `HumanDead` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `InfiniteRebirth` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 1 |
| `immediate` | Boolean |  | 1 |
| `playercat_health` | Number |  | 1 |

</details>

---

### Context: `InitialPhase` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Insane_Ceiling` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Insane_Ground` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Johnny` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `JohnnyBubs` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `JohnnyHost` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `JohnnyNeedsWashing` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_unwashed`](./Enums.md#enum-form_unwashed) | Enum |  | 1 |
| [`form_washed`](./Enums.md#enum-form_washed) | Enum |  | 1 |

</details>

---

### Context: `JohnnyNettle` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Joystick` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `LastHit` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `LeapClose` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `Lifted` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Lit` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `LowerAmbientLight` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CreateGlobalModifiers`](./Characters_and_Bosses.md#context-createglobalmodifiers)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`amount`](./Arrays.md#array-amount) | Array | The target opacity/dimness level. | 1 |
| `speed` | Number | The transition speed. | 1 |

</details>

---

### Context: `MegaDinoDropController` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`head_drop`](./Enums.md#enum-head_drop) | Enum |  | 1 |
| [`leg_leave`](./Enums.md#enum-leg_leave) | Enum |  | 1 |
| [`leg_return`](./Enums.md#enum-leg_return) | Enum |  | 1 |
| `stable_legs` | Number |  | 1 |

</details>

---

### Context: `ModularPickup` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 1 |
| [`sound_event`](./Enums.md#enum-sound_event) | Enum |  | 1 |

</details>

---

### Context: `MonkCatReactionAbilities` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`spell`](./Enums.md#enum-spell) | Enum |  | 1 |
| [`trinket`](./Enums.md#enum-trinket) | Enum |  | 1 |
| [`weapon`](./Enums.md#enum-weapon) | Enum | Weapon item constraint. | 1 |

</details>

---

### Context: `MotherGrowController` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eat_damage`](./Characters_and_Bosses.md#context-eat_damage) | Block | Damage dealt when this entity consumes another. | 1 |
| [`tumor_object`](./Enums.md#enum-tumor_object) | Enum |  | 1 |

</details>

---

### Context: `MotherTumorPassive` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Cat`](./Characters_and_Bosses.md#context-cat) | Block | Character Form: Base form for standard cats. | 1 |
| [`NonCat`](./Characters_and_Bosses.md#context-noncat) | Block | Character Form: Behavior and stats for the 'NonCat' state. | 1 |
| [`considered_forms`](./Arrays.md#array-considered_forms) | Array |  | 1 |
| [`grow_ability`](./Enums.md#enum-grow_ability) | Enum |  | 1 |
| [`pass_ani`](./Enums.md#enum-pass_ani) | Enum |  | 1 |
| [`receive_ani`](./Enums.md#enum-receive_ani) | Enum |  | 1 |

</details>

---

### Context: `Mount` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eject_ability`](./Enums.md#enum-eject_ability) | Enum |  | 1 |
| [`enter_ability`](./Enums.md#enum-enter_ability) | Enum |  | 1 |

</details>

---

### Context: `Mounted` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Context: `MouthFull` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `MoveAfterAnyAttemptedAttack` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 1 |

</details>

---

### Context: `MoveAwayFromDamageSource` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 1 |

</details>

---

### Context: `MoveAwayWhenEnemyAdjacent` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 1 |
| `once_per_turn` | Boolean |  | 1 |
| [`weights`](./Enums.md#enum-weights) | Enum |  | 1 |

</details>

---

### Context: `MoveForBarrage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MoveForDash` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MoveForGrass` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MoveForPounce` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MoveForSpin` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MoveOneForPuke` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MoveSpaced` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MoveToHead` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MoveTowards` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `MultiSpawnOnDeath` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array | The numerical quantity. | 1 |
| [`obj`](./Enums.md#enum-obj) | Enum |  | 1 |

</details>

---

### Context: `Mutant` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move_speed_multiplier`](./Enums.md#enum-move_speed_multiplier) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `NCGravecrawlFAR` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `NeutronStar` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `NoEyes` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |

</details>

---

### Context: `NoStick` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |

</details>

---

### Context: `NormalFull` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Nothing` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#context-mothertumorspawnincapture)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |

</details>

---

### Context: `Nuke` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Obey` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Off` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |

</details>

---

### Context: `OffScreen` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `OneEye` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Open` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `OpenCat` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Out` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `PassiveWhenAffectedByElement` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`element`](./Enums.md#enum-element) | Enum | Specific element type required or applied. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `PassiveWhenDead` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[passive_id]` container. [View all confirmed values in Engine_Passives.md](./Engine_Passives.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[passive_id]`](./Engine_Passives.md#all-confirmed-passive-id-values) | Boolean | Block | Any valid Passive ID. Value = `true` to grant it, or a Block to override its default values. See Engine_Passives.md for all confirmed IDs. |
| [`AddStatusToTrampleDamage`](./Characters_and_Bosses.md#context-addstatustotrampledamage) | Block | Modifier: Injects a status effect into the character's trample damage. | 1 |

</details>

---

### Context: `Possessing` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Primed` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Pulp2` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `Pulp3` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `Pulp4` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `Pulp5` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `Pulp6` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `Pulp7` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum |  | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `RandomStatusFromPool` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ally_rewards`](./Characters_and_Bosses.md#context-ally_rewards)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| [`StatusGroup`](./Characters_and_Bosses.md#context-statusgroup) | Block | Logic: Groups statuses for batch application. | 2 |

</details>

---

### Context: `ReturnA` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `RevengeDamage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| `damage` | Number | The base damage properties of an attack. | 1 |
| `knockback` | Number |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 1 |

</details>

---

### Context: `RunFar` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `RunWhenLastPlayerCatIsCharmed` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean |  | 1 |
| [`legacy_savekey`](./Enums.md#enum-legacy_savekey) | Enum |  | 1 |

</details>

---

### Context: `ScalingAttackAnimation` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`default`](./Enums.md#enum-default) | Enum | Baseline configuration. | 1 |
| [`thresholds`](./Arrays.md#array-thresholds) | Array |  | 1 |

</details>

---

### Context: `SharePickups` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `include_coins` | Boolean |  | 1 |

</details>

---

### Context: `Sitting` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `SkipFirstRounds` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `pop_chance` | Number |  | 1 |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `SmallHolding` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `SmallHoldingCat` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `SpawningPhase` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `SpewerAltGraphics` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

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

### Context: `StacyMutant_Brace` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | Applies or references the 'Brace' effect/state. | 1 |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |

</details>

---

### Context: `StacyMutant_Counter` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Characters_and_Bosses.md#context-addstatustobasicattack) | Block | Modifier: Injects a status effect payload into the character's basic attacks. | 1 |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| [`CounterAttack`](./Enums.md#enum-counterattack) | Enum | Reaction: Executes a counter-attack ability when hit. | 1 |

</details>

---

### Context: `StacyMutant_Damage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddDamage` | Number | Applies or references the 'AddDamage' effect/state. | 1 |
| `AddMaxHealth` | Number | Applies or references the 'AddMaxHealth' effect/state. | 1 |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |

</details>

---

### Context: `StacyMutant_DoubleHead` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| `ExtraDispersedTurns` | Number | Applies or references the 'ExtraDispersedTurns' effect/state. | 1 |

</details>

---

### Context: `StacyMutant_Fire` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | Applies or references the 'ElementImmune' effect/state. | 1 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | Applies or references the 'ReplaceBasicAttack' effect/state. | 1 |
| [`ReplaceBrain`](./Characters_and_Bosses.md#context-replacebrain) | Block | AI Logic: Completely overrides the character's AI profile with a new one. | 1 |

</details>

---

### Context: `StacyMutant_Health` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddMaxHealth` | Number | Applies or references the 'AddMaxHealth' effect/state. | 1 |
| `AddSpeed` | Number | Applies or references the 'AddSpeed' effect/state. | 1 |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| `SizeScale` | Number | Applies or references the 'SizeScale' effect/state. | 1 |

</details>

---

### Context: `StacyMutant_Holy` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. | 1 |

</details>

---

### Context: `StacyMutant_Ice` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddMovement` | Number | Applies or references the 'AddMovement' effect/state. | 1 |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | Applies or references the 'ElementImmune' effect/state. | 1 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | Applies or references the 'ReplaceBasicAttack' effect/state. | 1 |
| [`ReplaceBrain`](./Characters_and_Bosses.md#context-replacebrain) | Block | AI Logic: Completely overrides the character's AI profile with a new one. | 1 |

</details>

---

### Context: `StacyMutant_Lightning` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | Applies or references the 'ElementImmune' effect/state. | 1 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | Applies or references the 'ReplaceBasicAttack' effect/state. | 1 |
| [`ReplaceBrain`](./Characters_and_Bosses.md#context-replacebrain) | Block | AI Logic: Completely overrides the character's AI profile with a new one. | 1 |

</details>

---

### Context: `StacyMutant_Mirror` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| `ReflectProjectiles` | Number | Passive: Reflects incoming projectiles back at the attacker. | 1 |
| [`StatusEachTurnEndForEachTurn`](./Characters_and_Bosses.md#context-statuseachturnendforeachturn) | Block | Event Trigger: Applies a scaling status at the end of every turn based on turn count. | 1 |

</details>

---

### Context: `StacyMutant_Speed` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddDamage` | Number | Applies or references the 'AddDamage' effect/state. | 1 |
| `AddSpeed` | Number | Applies or references the 'AddSpeed' effect/state. | 1 |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| [`SizeScale`](./Enums.md#enum-sizescale) | Enum | Applies or references the 'SizeScale' effect/state. | 1 |

</details>

---

### Context: `StacyMutant_Thorns` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#context-adventuretokenpassivepool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform) | Block | Visual: Transforms specific body parts of the character. | 1 |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. | 1 |

</details>

---

### Context: `Standing` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Standing2` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`turns`](./Characters_and_Bosses.md#context-turns) | Block | Turn counter tracking. | 1 |

</details>

---

### Context: `Start_Ceiling` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `StatusAfterXTurns` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |
| `stacks` | Number | Number of stacks or intensity to apply. | 1 |

</details>

---

### Context: `StatusEachTurnBeginIfHasStatus` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 1 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 1 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 1 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 1 |
| `consume` | Boolean |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |

</details>

---

### Context: `StatusEachTurnEndForEachTurn` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StacyMutant_Mirror`](./Characters_and_Bosses.md#context-stacymutant_mirror)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusEachTurnEndIfEnabledAtStartOfTurn` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | Logic: Forces the execution of a specific ability. | 1 |

</details>

---

### Context: `StatusOnDie` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnEndMove` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOnEnemyConfused` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | Applies or references the 'ImmediateUseAbility' effect/state. | 1 |

</details>

---

### Context: `StatusOnGainCoins` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

> **Engine Schema:** This block is a `[status_id]` container. [View all confirmed values in Engine_Statuses.md](./Engine_Statuses.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[status_id]`](./Engine_Statuses.md#all-confirmed-status-id-values) | Number | Block | Any valid Status ID. Value = stack count / duration. See Engine_Statuses.md for all confirmed IDs. |

</details>

---

### Context: `StatusOverlappingCharactersAndDie` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Poison` | Number | Applies or references the 'Poison' effect/state. | 1 |

</details>

---

### Context: `StatusWhenStatusCompletelyRemoved` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`UseAbility`](./Characters_and_Bosses.md#context-useability) | Block | Logic: Forces execution of an ability. | 1 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |

</details>

---

### Context: `Stop` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#context-keyword_tooltips) | Block | Forces specific UI tooltips to appear. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `StunImmunity` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean |  | 1 |

</details>

---

### Context: `SuckMF` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `SupportDieInsteadOfRun` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alt_dead_ani`](./Enums.md#enum-alt_dead_ani) | Enum |  | 1 |
| [`alt_dying_ani`](./Enums.md#enum-alt_dying_ani) | Enum |  | 1 |

</details>

---

### Context: `SwimmingFormChange` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_in`](./Enums.md#enum-form_in) | Enum |  | 1 |
| [`form_out`](./Enums.md#enum-form_out) | Enum |  | 1 |

</details>

---

### Context: `SwitchMusic` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossBecomeTheChild`](./Characters_and_Bosses.md#context-finalbossbecomethechild)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | The specific audio layer to transition to (e.g., map, battle). | 1 |
| [`new_song`](./Enums.md#enum-new_song) | Enum | The ID of the new music track. | 1 |

</details>

---

### Context: `SwordAndShield` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `SwordAndShield_Primed` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `SyncFormsWithBuddy` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`no_buddy`](./Enums.md#enum-no_buddy) | Enum |  | 1 |

</details>

---

### Context: `T3HitlerSpawningPhase` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `T3JoinFight` | Flag | Applies or references the 'T3JoinFight' effect/state. | 1 |
| `T3Spawn_Colorless` | Flag | Applies or references the 'T3Spawn_Colorless' effect/state. | 1 |
| [`spell_use_groups`](./Arrays.md#array-spell_use_groups) | Array |  | 1 |

</details>

---

### Context: `TF_TargetAllies` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |

</details>

---

### Context: `TF_TargetEnemies` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |

</details>

---

### Context: `TVBotScreen` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Die` | Number | Character Form / Logic: Forces the character to die. | 1 |
| `Dumb` | Number | AI Profile: A simplified, less optimal decision-making profile. | 1 |
| `Fuck` | Number | Applies or references the 'Fuck' effect/state. | 1 |
| `Obey` | Number | AI State: Enforced compliance logic (e.g., when Charmed). | 1 |
| `Shit` | Number | Applies or references the 'Shit' effect/state. | 1 |
| `Stop` | Number | AI Movement: Forces the character to cease movement. | 1 |

</details>

---

### Context: `Tar` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `TarFull` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Terminator2Run` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `TerminatorChase` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move`](./Enums.md#enum-move) | Enum |  | 1 |

</details>

---

### Context: `TerminatorSkin` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`groups`](./Arrays.md#array-groups) | Array |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |

</details>

---

### Context: `Throb` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `ThrobBubs` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `ThrobHost` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `ThrobNettle` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `TransformOnStatusThreshold` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |
| `threshold` | Number |  | 1 |

</details>

---

### Context: `Transformed` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `TwisterFling` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 1 |
| `max_dist` | Number |  | 1 |
| `min_dist` | Number |  | 1 |

</details>

---

### Context: `TwoEyes` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Unflip` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#context-virtual_abilities)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |

</details>

---

### Context: `UnlimitedDeathRattleRevive` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| `even_if_stunned` | Boolean |  | 1 |

</details>

---

### Context: `Unlit` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Unwashed` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum |  | 1 |

</details>

---

### Context: `UseAbility` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusWhenStatusCompletelyRemoved`](./Characters_and_Bosses.md#context-statuswhenstatuscompletelyremoved)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger. | 1 |
| `respect_prime` | Boolean | If true, respects the ability's prime/cooldown state. | 1 |

</details>

---

### Context: `UseAbilityWhenOutOfStatus` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 |

</details>

---

### Context: `Washed` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `Washer` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `Water` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | String |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `WereMan` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `Zealot` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `ZealotBomb` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | String |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| [`name`](./Strings.md#string-name) | String | Localization key for the character's name. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |
| [`tooltip`](./Strings.md#string-tooltip) | String |  | 1 |

</details>

---

### Context: `additional_statuses` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnOnDeath`](./Characters_and_Bosses.md#context-spawnondeath)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PermanentMadness` | Number | Applies or references the 'PermanentMadness' effect/state. | 1 |

</details>

---

### Context: `ai_if_spawned_as_enemy` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum |  | 1 |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum |  | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum |  | 1 |
| [`pattern`](./Characters_and_Bosses.md#context-pattern) | Block | AI sequence logic. | 1 |

</details>

---

### Context: `damage_instance` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root)

> **Engine Schema:** This block is a `[damage_instance]` container. [View all confirmed values in Engine_Damage.md](./Engine_Damage.md)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`[damage_instance]`](./Engine_Damage.md#all-confirmed-damage-instance-values) | Block | A damage hit definition. See Engine_Damage.md for the full schema. |
| [`effects`](./Characters_and_Bosses.md#context-effects) | Block | Non-damaging impact triggers. | 1 |

</details>

---

### Context: `eat_damage` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherGrowController`](./Characters_and_Bosses.md#context-mothergrowcontroller)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean |  | 1 |
| `damage` | Number | The base damage properties of an attack. | 1 |
| [`effects`](./Characters_and_Bosses.md#context-effects) | Block | Non-damaging impact triggers. | 1 |
| `makes_contact` | Boolean |  | 1 |
| `piercing` | Boolean |  | 1 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 1 |

</details>

---

### Context: `exit_animations` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Grappling`](./Characters_and_Bosses.md#context-grappling)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Default`](./Enums.md#enum-default) | Enum | Character Form: The baseline default behavior state. | 1 |

</details>

---

### Context: `other_form_change_abilities` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossSyncAnimations`](./Characters_and_Bosses.md#context-finalbosssyncanimations)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Boris`](./Enums.md#enum-boris) | Enum | Character Form / AI State: Behavior and stats for the 'Boris' state. | 1 |
| [`Explosive`](./Enums.md#enum-explosive) | Enum | Character Form: Behavior and stats for the 'Explosive' state. | 1 |
| [`Holy`](./Enums.md#enum-holy) | Enum | Character Form: Behavior and stats for the 'Holy' state. | 1 |

</details>

---

### Context: `round_start_bonusturn_pattern` (1 instances)

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_priority`](./Arrays.md#array-do_priority) | Array |  | 1 |

</details>

---

### Numerical Contexts

> The following contexts are numeric keys or array indices.


### Context: `1` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| `animation_suffix` | Number |  | 1 |
| `partial_animation_suffix` | Number |  | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `2` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| `partial_animation_suffix` | Number |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| `animation_suffix` | Number |  | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `3` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 2 |
| `partial_animation_suffix` | Number |  | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 2 |
| `animation_suffix` | Number |  | 1 |
| `uifloaters_offset` | Number |  | 1 |

</details>

---

### Context: `0` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |

</details>

---

### Context: `4` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | Core block defining the AI behavior logic and weights. | 1 |
| `animation_suffix` | Number |  | 1 |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| `partial_animation_suffix` | Number |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

### Context: `5` (1 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum |  | 1 |
| `partial_animation_suffix` | Number |  | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | Block listing intrinsic passive modifiers. | 1 |

</details>

---

