# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Chapter ID Enum

> **Associated Files:** `data/chapter_id_enum.gon`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`alley`](./Enums.md#enum-alley) | Enum |  | 2 |
| [`boneyard`](./Enums.md#enum-boneyard) | Enum |  | 2 |
| [`bunker`](./Enums.md#enum-bunker) | Enum |  | 2 |
| [`caves`](./Arrays.md#array-caves) | Array |  | 2 |
| [`core`](./Arrays.md#array-core) | Array |  | 2 |
| [`crater`](./Enums.md#enum-crater) | Enum |  | 2 |
| [`debug`](./Strings.md#string-debug) | String |  | 2 |
| [`desert`](./Arrays.md#array-desert) | Array |  | 2 |
| [`dimensionx`](./Enums.md#enum-dimensionx) | Enum |  | 2 |
| [`endoftime`](./Arrays.md#array-endoftime) | Array |  | 2 |
| [`future`](./Arrays.md#array-future) | Array |  | 2 |
| [`iceage`](./Arrays.md#array-iceage) | Array |  | 2 |
| [`junkyard`](./Enums.md#enum-junkyard) | Enum |  | 2 |
| [`jurassic`](./Arrays.md#array-jurassic) | Array |  | 2 |
| [`lab`](./Arrays.md#array-lab) | Array |  | 2 |
| [`meatworld`](./Enums.md#enum-meatworld) | Enum |  | 2 |
| [`moon`](./Enums.md#enum-moon) | Enum |  | 2 |
| [`sewers`](./Arrays.md#array-sewers) | Array |  | 2 |
| [`theend`](./Arrays.md#array-theend) | Array |  | 2 |
| [`tutorial`](./Strings.md#string-tutorial) | String |  | 2 |
| [`CompletionCheckmarkTooltip`](./Arrays.md#array-completioncheckmarktooltip) | Array |  | 1 |
| [`SmallCompletionCheckmarkTooltip`](./Arrays.md#array-smallcompletioncheckmarktooltip) | Array |  | 1 |
| [`major_class_checkmarks`](./Arrays.md#array-major_class_checkmarks) | Array |  | 1 |
| [`map_areas`](#context-map_areas) | Block |  | 1 |

</details>

---

### Context: `map_areas`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#chapter-id-enum)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alley`](./Enums.md#enum-alley) | Enum |  | 1 |
| [`boneyard`](./Enums.md#enum-boneyard) | Enum |  | 1 |
| [`bunker`](./Enums.md#enum-bunker) | Enum |  | 1 |
| [`caves`](./Enums.md#enum-caves) | Enum |  | 1 |
| [`core`](./Enums.md#enum-core) | Enum |  | 1 |
| [`crater`](./Enums.md#enum-crater) | Enum |  | 1 |
| [`desert`](./Enums.md#enum-desert) | Enum |  | 1 |
| [`dimensionx`](./Enums.md#enum-dimensionx) | Enum |  | 1 |
| [`endoftime`](./Enums.md#enum-endoftime) | Enum |  | 1 |
| [`future`](./Enums.md#enum-future) | Enum |  | 1 |
| [`iceage`](./Enums.md#enum-iceage) | Enum |  | 1 |
| [`junkyard`](./Enums.md#enum-junkyard) | Enum |  | 1 |
| [`jurassic`](./Enums.md#enum-jurassic) | Enum |  | 1 |
| [`lab`](./Enums.md#enum-lab) | Enum |  | 1 |
| [`meatworld`](./Enums.md#enum-meatworld) | Enum |  | 1 |
| [`moon`](./Enums.md#enum-moon) | Enum |  | 1 |
| [`nuke`](./Enums.md#enum-nuke) | Enum |  | 1 |
| [`sewers`](./Enums.md#enum-sewers) | Enum |  | 1 |
| [`theend`](./Enums.md#enum-theend) | Enum |  | 1 |

</details>

---

## Event Reward Samples

> **Associated Files:** `data/event_rewards_samples.gon`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| `Fights` | Number |  | 3 |
| `Poison` | Number |  | 3 |
| `count` | Number |  | 3 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 3 |
| `con` | Number |  | 2 |
| `ears` | Number |  | 2 |
| `fights_skipped` | Number |  | 2 |
| `mouth` | Number |  | 2 |
| [`object`](./Enums.md#enum-object) | Enum |  | 2 |
| `str` | Number |  | 2 |
| `tail` | Number |  | 2 |
| [`CharacterTypeGainsStatusAtBattleStart`](#context-charactertypegainsstatusatbattlestart) | Block |  | 1 |
| `asymmetric` | Boolean |  | 1 |
| `chance` | Number |  | 1 |
| `choose_cat_with_min_health` | Number |  | 1 |
| [`common`](#context-common) | Block |  | 1 |
| [`conditional_reward`](#context-conditional_reward) | Block |  | 1 |
| [`cutscene`](./Strings.md#string-cutscene) | String |  | 1 |
| [`else`](#context-else) | Block |  | 1 |
| [`event`](./Enums.md#enum-event) | Enum |  | 1 |
| `fights` | Number |  | 1 |
| `initial_health` | Number |  | 1 |
| [`mutation`](#context-mutation) | Block |  | 1 |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 1 |
| [`prompt`](./Strings.md#string-prompt) | String |  | 1 |
| `random` | Number |  | 1 |
| [`rare`](#context-rare) | Block |  | 1 |
| [`requirements`](#context-requirements) | Block |  | 1 |
| [`restrict`](./Enums.md#enum-restrict) | Enum |  | 1 |
| [`return_as`](./Enums.md#enum-return_as) | Enum |  | 1 |
| [`return_during`](./Enums.md#enum-return_during) | Enum |  | 1 |
| [`reward`](#context-reward) | Block |  | 1 |
| `same_cat` | Boolean |  | 1 |
| `set_frame` | Number |  | 1 |
| `skip_result_screen` | Boolean |  | 1 |
| [`spawn_side`](./Enums.md#enum-spawn_side) | Enum |  | 1 |

</details>

---

### Context: `requirements`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#event-reward-samples), [`conditional_reward`](#context-conditional_reward)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cat_has_item_equipped`](./Arrays.md#array-cat_has_item_equipped) | Array |  | 2 |
| [`has_token`](./Enums.md#enum-has_token) | Enum |  | 2 |
| [`counter_maximum`](./Arrays.md#array-counter_maximum) | Array |  | 1 |
| [`counter_minimum`](./Arrays.md#array-counter_minimum) | Array |  | 1 |
| [`counter_range`](./Arrays.md#array-counter_range) | Array |  | 1 |
| `has_parasite` | Boolean |  | 1 |
| [`not_cat_has_item_equipped`](./Enums.md#enum-not_cat_has_item_equipped) | Enum |  | 1 |
| [`not_has_token`](./Enums.md#enum-not_has_token) | Enum |  | 1 |

</details>

---

### Context: `reward`

> **Engine Dictionary:** This block accepts dynamic nodes. See [`Engine_Events.md`](./Engine_Events.md) for the full list of valid nested blocks.

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

> **Referenced by:** [`ROOT`](#event-reward-samples), [`conditional_reward`](#context-conditional_reward)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ambush_next_basic_fights` | Number |  | 1 |
| `gain_coins` | Number |  | 1 |
| [`level_up`](./Enums.md#enum-level_up) | Enum |  | 1 |
| [`prompt`](./Strings.md#string-prompt) | String |  | 1 |
| [`set_subject`](./Enums.md#enum-set_subject) | Enum |  | 1 |

</details>

---

### Context: `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#event-reward-samples)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Statuses / Passives}`](./Engine_Statuses_and_Passives.md#all-confirmed-status-passive-id-values) | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |  |
| `Fear` | Number |  | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum |  | 1 |

</details>

---

### Context: `common`

> **Engine Dictionary:** This block accepts dynamic nodes. See [`Engine_Events.md`](./Engine_Events.md) for the full list of valid nested blocks.

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#event-reward-samples)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prompt`](./Strings.md#string-prompt) | String |  | 1 |
| `set_frame` | Number |  | 1 |

</details>

---

### Context: `conditional_reward`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#event-reward-samples)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`requirements`](#context-requirements) | Block |  | 1 |
| [`reward`](#context-reward) | Block |  | 1 |

</details>

---

### Context: `else`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#event-reward-samples)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`increment_legacy_counter`](./Enums.md#enum-increment_legacy_counter) | Enum |  | 1 |
| `party_damage` | Number |  | 1 |
| [`prompt`](./Strings.md#string-prompt) | String |  | 1 |

</details>

---

### Context: `mutation`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#event-reward-samples)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `eyes` | Number |  | 1 |

</details>

---

### Context: `rare`

> **Engine Dictionary:** This block accepts dynamic nodes. See [`Engine_Events.md`](./Engine_Events.md) for the full list of valid nested blocks.

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`ROOT`](#event-reward-samples)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`prompt`](./Strings.md#string-prompt) | String |  | 1 |
| `set_frame` | Number |  | 1 |

</details>

---

## House Boss Info

> **Associated Files:** `data/house_boss_info.gon`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 9

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| `act` | Number |  | 9 |
| [`arrival_unlock`](./Enums.md#enum-arrival_unlock) | Enum |  | 9 |
| `index` | Number |  | 9 |
| [`initial_cooldown`](./Arrays.md#array-initial_cooldown) | Array |  | 9 |
| `lead_time` | Number |  | 9 |
| [`level`](./Math_Equations.md) | Equation |  | 9 |
| [`music`](./Enums.md#enum-music) | Enum |  | 9 |
| [`rematch_cooldown`](./Arrays.md#array-rematch_cooldown) | Array |  | 9 |
| [`savefile_string`](./Strings.md#string-savefile_string) | String |  | 9 |
| [`initial_cutscene_night`](./Enums.md#enum-initial_cutscene_night) | Enum |  | 6 |
| [`rematch_cutscene_night`](./Enums.md#enum-rematch_cutscene_night) | Enum |  | 6 |
| [`initial_cutscene_day`](./Enums.md#enum-initial_cutscene_day) | Enum |  | 3 |
| [`rematch_cutscene_day`](./Enums.md#enum-rematch_cutscene_day) | Enum |  | 3 |
| [`ending_cutscene`](./Enums.md#enum-ending_cutscene) | Enum |  | 1 |
| [`ending_cutscene2`](./Enums.md#enum-ending_cutscene2) | Enum |  | 1 |

</details>

---

## Particles

> **Associated Files:** `data/particles.gon`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 154

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  | 154 |
| [`render_mode`](./Enums.md#enum-render_mode) | Enum |  | 140 |
| `emit_amount` | Number |  | 139 |
| `emit_rate` | Number |  | 139 |
| [`particle_lifetime`](./Arrays.md#array-particle_lifetime) | Array |  | 138 |
| [`simulation_space`](./Enums.md#enum-simulation_space) | Enum |  | 138 |
| [`projection_matrix`](./Enums.md#enum-projection_matrix) | Enum |  | 137 |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array |  | 132 |
| `emit_spread` | Number |  | 125 |
| `speed_start` | Number |  | 120 |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array |  | 103 |
| [`size_start`](./Arrays.md#array-size_start) | Array |  | 94 |
| [`scripts`](#context-scripts) | Block |  | 90 |
| [`emit_box`](./Arrays.md#array-emit_box) | Array |  | 81 |
| `size_end` | Number |  | 76 |
| [`friction`](./Arrays.md#array-friction) | Array |  | 72 |
| `face_moving_direction` | Boolean |  | 64 |
| `alpha_end` | Number |  | 61 |
| [`speed_scale`](./Arrays.md#array-speed_scale) | Array |  | 58 |
| `alpha_start` | Number |  | 53 |
| [`rotation`](./Arrays.md#array-rotation) | Array |  | 52 |
| [`size`](./Enums.md#enum-size) | Enum |  | 44 |
| [`emit_radius`](./Enums.md#enum-emit_radius) | Enum |  | 30 |
| [`rotation_speed_start`](./Arrays.md#array-rotation_speed_start) | Array |  | 28 |
| [`force_start`](./Arrays.md#array-force_start) | Array |  | 26 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum |  | 26 |
| [`alpha_out`](./Enums.md#enum-alpha_out) | Enum |  | 25 |
| `alpha` | Number |  | 23 |
| [`ownership`](./Enums.md#enum-ownership) | Enum |  | 23 |
| [`alpha_in`](./Enums.md#enum-alpha_in) | Enum |  | 21 |
| [`combo`](./Arrays.md#array-combo) | Array |  | 19 |
| `rotation_speed_end` | Number |  | 19 |
| [`speed`](./Arrays.md#array-speed) | Array |  | 17 |
| `depth_bias` | Number |  | 16 |
| `flat_movement` | Boolean |  | 16 |
| [`force_end`](./Arrays.md#array-force_end) | Array |  | 16 |
| [`force`](./Arrays.md#array-force) | Array |  | 15 |
| [`chain`](./Enums.md#enum-chain) | Enum |  | 14 |
| `inherit_speed` | Number |  | 14 |
| [`rotation_speed`](./Arrays.md#array-rotation_speed) | Array |  | 12 |
| [`size_in`](./Enums.md#enum-size_in) | Enum |  | 11 |
| `unlit` | Boolean |  | 9 |
| [`render_layer`](./Enums.md#enum-render_layer) | Enum |  | 8 |
| [`rotation_start`](./Arrays.md#array-rotation_start) | Array |  | 8 |
| [`size_out`](./Enums.md#enum-size_out) | Enum |  | 8 |
| `emit_shell` | Number |  | 5 |
| [`emit_timespread`](./Enums.md#enum-emit_timespread) | Enum |  | 5 |
| [`friction_end`](./Arrays.md#array-friction_end) | Array |  | 5 |
| [`material`](./Enums.md#enum-material) | Enum |  | 5 |
| [`spurt`](./Enums.md#enum-spurt) | Enum |  | 5 |
| [`friction_start`](./Arrays.md#array-friction_start) | Array |  | 4 |
| [`emit_timespread_curve`](./Enums.md#enum-emit_timespread_curve) | Enum |  | 3 |
| `speed_end` | Number |  | 3 |
| `max_particles` | Number |  | 2 |
| [`movieclip_timescale`](./Enums.md#enum-movieclip_timescale) | Enum |  | 2 |
| [`chain_chance`](./Enums.md#enum-chain_chance) | Enum |  | 1 |
| `continual_emission` | Boolean |  | 1 |
| [`emitshape_scale`](./Arrays.md#array-emitshape_scale) | Array |  | 1 |
| `is_3D` | Boolean |  | 1 |

</details>

---

### Context: `scripts`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 90

> **Referenced by:** [`ROOT`](#particles)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ParticleBouncePlane`](#context-particlebounceplane) | Block |  | 69 |
| [`ParticleGlobalForce`](#context-particleglobalforce) | Block |  | 27 |
| [`ParticleTornadoForce`](#context-particletornadoforce) | Block |  | 19 |
| [`ParticleRandomForce`](./Arrays.md#array-particlerandomforce) | Array |  | 18 |
| `ParticleAttractor` | Number |  | 9 |
| [`ParticleCharacterCollision`](#context-particlecharactercollision) | Block |  | 1 |

</details>

---

### Context: `ParticleBouncePlane`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 69

> **Referenced by:** [`scripts`](#context-scripts)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dampening`](./Enums.md#enum-dampening) | Enum |  | 69 |
| `friction` | Number |  | 65 |
| [`plane`](./Enums.md#enum-plane) | Enum |  | 32 |
| `position` | Number |  | 32 |
| `rotation_dampening` | Number |  | 1 |

</details>

---

### Context: `ParticleGlobalForce`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 27

> **Referenced by:** [`scripts`](#context-scripts)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `amount` | Number |  | 27 |
| [`id`](./Enums.md#enum-id) | Enum |  | 27 |

</details>

---

### Context: `ParticleTornadoForce`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 19

> **Referenced by:** [`scripts`](#context-scripts)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`axis`](./Arrays.md#array-axis) | Array |  | 19 |
| `force` | Number |  | 19 |
| [`point`](./Arrays.md#array-point) | Array |  | 19 |

</details>

---

### Context: `ParticleAttractor`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`towards`](./Arrays.md#array-towards) | Array |  | 7 |
| `force_end` | Number |  | 6 |
| `force_start` | Number |  | 6 |
| `force` | Number |  | 1 |

</details>

---

### Context: `ParticleRandomForce`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`begin`](./Arrays.md#array-begin) | Array |  | 7 |
| [`end`](./Arrays.md#array-end) | Array |  | 7 |

</details>

---

### Context: `ParticleCharacterCollision`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`scripts`](#context-scripts)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `character_sphere_offset` | Number |  | 1 |
| [`inherit_velocity`](./Enums.md#enum-inherit_velocity) | Enum |  | 1 |
| `pushforce` | Number |  | 1 |

</details>

---

## Particles 2D

> **Associated Files:** `data/particles2d.gon`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 19

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`emit_amount`](./Arrays.md#array-emit_amount) | Array |  | 19 |
| [`emit_box`](./Arrays.md#array-emit_box) | Array |  | 19 |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array |  | 19 |
| `emit_rate` | Number |  | 19 |
| `emit_spread` | Number |  | 19 |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array |  | 19 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  | 19 |
| `particle_lifetime` | Number |  | 19 |
| [`projection_matrix`](./Enums.md#enum-projection_matrix) | Enum |  | 19 |
| [`render_mode`](./Enums.md#enum-render_mode) | Enum |  | 19 |
| [`simulation_space`](./Enums.md#enum-simulation_space) | Enum |  | 19 |
| [`speed_start`](./Arrays.md#array-speed_start) | Array |  | 19 |
| [`alpha`](./Enums.md#enum-alpha) | Enum |  | 18 |
| [`scripts`](#context-scripts) | Block |  | 18 |
| [`force`](./Arrays.md#array-force) | Array |  | 13 |
| `face_moving_direction` | Boolean |  | 12 |
| [`size_start`](./Enums.md#enum-size_start) | Enum |  | 11 |
| [`speed_scale`](./Enums.md#enum-speed_scale) | Enum |  | 11 |
| [`size`](./Arrays.md#array-size) | Array |  | 9 |
| [`chain`](./Enums.md#enum-chain) | Enum |  | 8 |
| [`friction_end`](./Arrays.md#array-friction_end) | Array |  | 5 |
| [`friction_start`](./Arrays.md#array-friction_start) | Array |  | 5 |
| [`render_layer`](./Enums.md#enum-render_layer) | Enum |  | 5 |
| `size_end` | Number |  | 5 |
| [`combo`](./Arrays.md#array-combo) | Array |  | 4 |
| [`size_out`](./Enums.md#enum-size_out) | Enum |  | 4 |
| [`alpha_in`](./Enums.md#enum-alpha_in) | Enum |  | 3 |
| [`alpha_out`](./Enums.md#enum-alpha_out) | Enum |  | 3 |
| [`rotation`](./Arrays.md#array-rotation) | Array |  | 3 |
| [`rotation_speed`](./Arrays.md#array-rotation_speed) | Array |  | 3 |
| `rotation_speed_end` | Number |  | 3 |
| [`size_in`](./Enums.md#enum-size_in) | Enum |  | 1 |

</details>

---

### Context: `scripts`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 18

> **Referenced by:** [`ROOT`](#particles-2d)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ParticleLineCollisions`](#context-particlelinecollisions) | Block |  | 8 |
| [`ParticleBouncePlane`](#context-particlebounceplane) | Block |  | 5 |
| [`ParticleRandomForce`](./Arrays.md#array-particlerandomforce) | Array |  | 2 |

</details>

---

### Context: `ParticleLineCollisions`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

> **Referenced by:** [`scripts`](#context-scripts)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dampening` | Number |  | 6 |
| `friction` | Number |  | 6 |
| `end_on_collision` | Boolean |  | 2 |

</details>

---

### Context: `ParticleBouncePlane`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

> **Referenced by:** [`scripts`](#context-scripts)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dampening` | Number |  | 5 |
| `friction` | Number |  | 5 |

</details>

---

## Save File Percentages

> **Associated Files:** `data/save_file_percentages.gon`

### Context: `complete_checkmarks`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

> **Referenced by:** [`1`](#context-1), [`20`](#context-20)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`areas`](./Arrays.md#array-areas) | Array |  | 6 |
| [`classes`](./Arrays.md#array-classes) | Array |  | 6 |
| `min_difficulty` | Number |  | 6 |
| `mono_cat_run` | Boolean |  | 6 |
| `solo_cat_run` | Boolean |  | 6 |

</details>

---

### Numerical Contexts

> The following contexts are numeric keys or array indices.

### Context: `1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 39

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_unlock`](./Enums.md#enum-adventure_unlock) | Enum |  | 39 |
| [`complete_checkmarks`](#context-complete_checkmarks) | Block |  | 5 |

</details>

---

### Context: `20`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 18

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`complete_chapter`](./Enums.md#enum-complete_chapter) | Enum |  | 18 |
| [`complete_house_boss`](./Enums.md#enum-complete_house_boss) | Enum |  | 9 |
| [`save_file_flag`](./Enums.md#enum-save_file_flag) | String |  | 9 |
| [`max_npc`](./Enums.md#enum-max_npc) | Enum |  | 7 |
| [`adventure_unlock`](./Enums.md#enum-adventure_unlock) | Enum |  | 5 |
| [`complete_checkmarks`](#context-complete_checkmarks) | Block |  | 1 |

</details>

---

## Team Names

> **Associated Files:** `data/teamnames.gon`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 15

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`adjectives`](./Arrays.md#array-adjectives) | Array |  | 15 |
| [`nouns`](./Arrays.md#array-nouns) | Array |  | 15 |
| [`format`](./Strings.md#string-format) | String |  | 1 |
| [`format2`](./Strings.md#string-format2) | String |  | 1 |

</details>

---

## Tiles

> **Associated Files:** `data/tiles.gon`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 27

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`editor`](#context-editor) | Block |  | 27 |
| [`tile`](./Enums.md#enum-tile) | Enum |  | 26 |
| [`orientation`](./Enums.md#enum-orientation) | Enum |  | 4 |

</details>

---

### Context: `editor`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 27

> **Referenced by:** [`ROOT`](#tiles)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`image`](./Strings.md#string-image) | String |  | 27 |
| [`name`](./Strings.md#string-name) | String |  | 27 |
| `category` | Number |  | 26 |
| [`image_tint`](./Arrays.md#array-image_tint) | Array |  | 26 |
| `paint` | Boolean |  | 26 |
| `subcategory` | Number |  | 26 |
| `tile_layer` | Number |  | 26 |

</details>

---

### Context: `tile`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BlankTile` | Number |  | 2 |
| `GrassTile` | Number |  | 2 |
| `TallGrassTile` | Number |  | 2 |

</details>

---

## Tilesets

> **Associated Files:** `data/tilesets.gon`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 22

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`global_objects`](#context-global_objects) | Block |  | 22 |
| [`combat_background`](./Enums.md#enum-combat_background) | Enum |  | 21 |
| [`combat_ui_background`](./Enums.md#enum-combat_ui_background) | Enum |  | 21 |
| [`debris`](./Enums.md#enum-debris) | Enum |  | 21 |
| [`event_piece_frame`](./Enums.md#enum-event_piece_frame) | Enum |  | 21 |
| [`static_1x1_a`](./Enums.md#enum-static_1x1_a) | Enum |  | 21 |
| [`static_1x1_b`](./Enums.md#enum-static_1x1_b) | Enum |  | 21 |
| [`static_1x1_c`](./Enums.md#enum-static_1x1_c) | Enum |  | 21 |
| [`static_2x2_a`](./Enums.md#enum-static_2x2_a) | Enum |  | 21 |
| [`static_2x2_b`](./Enums.md#enum-static_2x2_b) | Enum |  | 21 |
| [`static_tall_a`](./Enums.md#enum-static_tall_a) | Enum |  | 21 |
| [`static_tall_b`](./Enums.md#enum-static_tall_b) | Enum |  | 21 |
| [`reverb`](#context-reverb) | Block |  | 14 |
| [`global_particles`](./Arrays.md#array-global_particles) | Array |  | 11 |
| [`background_extra_shader`](./Enums.md#enum-background_extra_shader) | Enum |  | 3 |
| [`water_alt_shader`](./Enums.md#enum-water_alt_shader) | Enum |  | 2 |
| [`water_alt_shroud`](./Enums.md#enum-water_alt_shroud) | Enum |  | 2 |
| [`water_alt_tile`](./Enums.md#enum-water_alt_tile) | Enum |  | 2 |
| [`background_shader`](./Enums.md#enum-background_shader) | Enum |  | 1 |
| [`boss_background_alt`](./Enums.md#enum-boss_background_alt) | Enum |  | 1 |

</details>

---

### Context: `global_objects`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 22

> **Referenced by:** [`ROOT`](#tilesets)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Lighting`](#context-lighting) | Block |  | 10 |
| [`Fly`](#context-fly) | Block |  | 7 |
| [`Cockroach`](#context-cockroach) | Block |  | 3 |
| [`Firefly`](#context-firefly) | Block |  | 1 |

</details>

---

### Context: `battle`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 14

> **Referenced by:** [`reverb`](#context-reverb)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `volume_adjustment` | Number |  | 15 |
| [`amount`](./Enums.md#enum-amount) | Enum |  | 14 |
| [`preset`](./Enums.md#enum-preset) | Enum |  | 14 |
| `DecayTime` | Number |  | 11 |
| [`ReverbDelay`](./Enums.md#enum-reverbdelay) | Enum |  | 7 |

</details>

---

### Context: `reverb`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 14

> **Referenced by:** [`ROOT`](#tilesets)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`battle`](#context-battle) | Block |  | 14 |

</details>

---

### Context: `Lighting`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 10

> **Referenced by:** [`global_objects`](#context-global_objects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ambient`](./Enums.md#enum-ambient) | Enum |  | 10 |
| [`bigrays`](./Arrays.md#array-bigrays) | Array |  | 6 |
| [`smallrays`](./Arrays.md#array-smallrays) | Array |  | 6 |
| [`smallray_clip`](./Enums.md#enum-smallray_clip) | Enum |  | 2 |

</details>

---

### Context: `Fly`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

> **Referenced by:** [`global_objects`](#context-global_objects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array |  | 7 |

</details>

---

### Context: `Cockroach`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

> **Referenced by:** [`global_objects`](#context-global_objects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array |  | 3 |

</details>

---

### Context: `Firefly`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

> **Referenced by:** [`global_objects`](#context-global_objects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array |  | 1 |

</details>

---
