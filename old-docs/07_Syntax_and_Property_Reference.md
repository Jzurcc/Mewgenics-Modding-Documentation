# Mewgenics Mod Developer Documentation: Master Syntax & Property Reference

This is the definitive, exhaustive cheat sheet for the Mewgenics engine, containing every single property extracted directly from the base game's `.gon` files. Use these tables to discover undocumented hooks and parameters for your modding.

---

## 1. Targeting & Targeting Shapes (`target { ... }`)

| Property | Definition / Expected Behavior | Possible Inputs / Types |
| :--- | :--- | :--- |
| `adjust_target` | Tweaks target selection post-cast. | Enum: `stalk` |
| `allow_any_orientation` | Allows casting regardless of the character's facing direction. | Boolean (`true`/`false`) |
| `allow_diagonal_passthrough` | Permits diagonal targeting through tight corners. | Boolean (`true`/`false`) |
| `allow_diagonals` | Allows targeting on diagonal grid axes. | Boolean (`true`/`false`) |
| `ally_priority` | AI preference for targeting allies. | Boolean (`true`/`false`) |
| `always_bounce` | Forces the attack/projectile to bounce regardless of hit. | Boolean (`true`/`false`) |
| `aoe_chance` | Percentage chance for the AoE to trigger. | Enum: `.33`, `.4+.2*level`, `.5` |
| `aoe_considers_character_size` | Scales the AoE based on the caster's tile size (e.g., 2x2). | Boolean (`true`/`false`) |
| `aoe_display_exclude_restrictions` | Visual only: Hides invalid tiles from the AoE preview. | Boolean (`true`/`false`) |
| `aoe_excludes_self` | Prevents the AoE from hitting the caster. | Boolean (`true`/`false`) |
| `aoe_hint_teamcast` | Visual hint for cooperative casting abilities. | Boolean (`true`/`false`) |
| `aoe_leading_edge_only` | Only the outermost edge of the AoE shape applies effects. | Boolean (`true`/`false`) |
| `aoe_mode` | The shape of the area (`standard`, `line`, `cross`, `square`, `custom`). | Math Expression / Number (e.g. `5`, `X+1`) |
| `aoe_restrictions` | Array of conditions the AoE tiles must meet (e.g., `must_have_line_of_sight_unpurgable`). | Array `[allies_only, character_has_turns_left, character_must_be_affected_by_tile_with_element, enemies_only, exclude_allies, exclude_blocking, familiars_only, must_backstab, must_be_empty, must_be_partially_empty, must_have_cat, must_have_character, must_have_corpse, must_have_destructible_corpse, must_have_enemy_or_robot, must_have_line_of_sight, must_have_line_of_sight_unpurgable, must_have_living_character, must_have_player_cat, must_have_tag, must_not_have_corpse, tile_must_have_element]` |
| `aoe_rotate_around_character_center` | Anchors the AoE rotation to the character rather than the tile. | Boolean (`true`/`false`) |
| `aoe_spell_on_land` | Triggers the AoE only when a lobbed/jump ability lands. | Boolean (`true`/`false`) |
| `aoe_symmetry` | Determines if the AoE mirrors on axes. | Enum: `eight_way`, `four_way`, `none` |
| `aoe_tile_requires_element` | Only affects tiles painted with a specific element. | Enum: `Earth`, `Grass`, `Water` |
| `as_the_crow_flies` | Calculates range ignoring all pathing terrain obstacles. | Boolean (`true`/`false`) |
| `bonus_pathing_leniency` | Gives the AI leeway when calculating complex paths. | Enum: `4` |
| `can_multihit` | If true, overlapping AoEs can hit the same target multiple times. | Boolean (`true`/`false`) |
| `consider_trample` | AI consideration for moving through units. | Boolean (`true`/`false`) |
| `corpse_priority` | AI preference for targeting dead bodies. | Enum: `10`, `5` |
| `custom_aoe` | Array of exact coordinates for a custom shape (e.g., `[[1, -1] [1, 0]]`). | Array `[-1], -1],, -1][3,, -2], -2][3,, -3], 0], 0],, 0][-2,, 0][3,, 1, 1], 1],, 1][0, 1][3,, 2, 2], 2],, 3], 3],, 4], 5], 6], 7], 8], 9, 9], [-1, [-1,, [-2,, [-3,, [-4,, [0, [0,, [0,-1], [1, [1,, [1,-1], [2, [2,, [3, [3,, [4, [4,, [5, [5,, [6, [6,, [7, [7,, [8, [8,, [9, [9,]` |
| `custom_aoe_mirror` | How the custom shape mirrors when facing left vs right. | Array `[0], [1, [1,]` |
| `custom_aoe_util` / `_mirror` | Utility variants of custom AoE definitions. | Array `[-1], -1],, 0], 0],, 1], 1],, [-1,, [0,, [1,]` |
| `custom_range` | Overrides standard range scaling. | Array `[-1], -1][0, -2], -2][0, -3][0, -4][0, -5][0, -6][0, -7][0, -8][0, -9][0, 0], 0][0, 1], 1][0, 2], 2][0, 3][0, 4][0, 5][0, 6][0, 7][0, 8][0, 9], [-1, [-1,, [-2, [-3, [-4, [0, [1, [1,]` |
| `damage_collided_only` | Only damages the first entity the projectile/dash hits. | Boolean (`true`/`false`) |
| `delay` | Frame delay before the targeting takes effect. | Math Expression / Number (e.g. `5`, `X+1`) |
| `delay_from_map_edge` | Delays effect based on distance from the screen edge. | Boolean (`true`/`false`) |
| `delayed_trigger` | Delays the actual execution of the target effect. | Boolean (`true`/`false`) |
| `distance_sort_targets` | Prioritizes targets based on proximity. | Boolean (`true`/`false`) |
| `dont_orient` | Prevents the character from turning to face the target. | Boolean (`true`/`false`) |
| `dont_orient_aoe` | Prevents the AoE shape from rotating with the character. | Boolean (`true`/`false`) |
| `enemy_priority` | AI preference for targeting enemies. | Enum: `10` |
| `force_ai_target_as_spell` | Forces the AI to treat a physical move like a spell for targeting logic. | Boolean (`true`/`false`) |
| `force_no_contact` | Prevents physical contact (bypassing Thorns/Retaliate). | Boolean (`true`/`false`) |
| `hint_can_target_empty` | UI hint that the player can click an empty tile. | Boolean (`true`/`false`) |
| `hint_can_target_pickups` | UI hint that the player can target items on the ground. | Boolean (`true`/`false`) |
| `hint_can_target_static` | UI hint that the player can target inanimate objects. | Boolean (`true`/`false`) |
| `knockback_mode` | How physics vectors apply (`character_to_tile`, `pull_to_character`, `zero`, `orientation`). | Math Expression / Number (e.g. `5`, `X+1`) |
| `knockback_modifier` | Multiplier for the knockback physics force. | Enum: `rotate_cw` |
| `lingering` | Target zone remains active across multiple turns. | Boolean (`true`/`false`) |
| `low_gravity_boostable` | Can be affected by low gravity wind/effects. | Boolean (`true`/`false`) |
| `low_health_character_threshold` | AI targeting threshold for seeking weak targets. | Enum: `10`, `5`, `item_aux` |
| `max_aoe` / `min_aoe` | The maximum and minimum radius/length of the AoE. | String/Value (e.g. `6`, `5+bonus_range`) |
| `max_bounces` | Hard cap on how many times a bouncing effect can trigger. | Math Expression / Number (e.g. `5`, `X+1`) |
| `max_range` / `min_range` | The maximum and minimum distance required to cast. | String/Value (e.g. `6`, `5+bonus_range`) |
| `max_targets` / `min_targets` | Limits on how many distinct entities can be targeted. | Math Expression / Number (e.g. `5`, `X+1`) |
| `mirror_custom_aoe` | Flips the custom AoE array. | Boolean (`true`/`false`) |
| `mouse_offset` | Visual offset for the targeting cursor. | Array `[.5]` |
| `multihit` | Hardcoded number of times the ability hits the target. | Math Expression / Number (e.g. `5`, `X+1`) |
| `multihit_max` / `multihit_min` | Variable limits for random multihit abilities. | Math Expression / Number (e.g. `5`, `X+1`) |
| `N` | Variable modifier parameter. | Math Expression / Number (e.g. `5`, `X+1`) |
| `prioritize_change_direction` | AI preference to attack from different angles. | Boolean (`true`/`false`) |
| `prioritize_dont_change_direction` | AI preference to maintain current facing angle. | Boolean (`true`/`false`) |
| `prioritize_face_camera` | AI preference to face South. | Boolean (`true`/`false`) |
| `prioritize_throw_target_with_passive` | AI prefers throwing targets that have specific passives. | Enum: `NubbyTossPriority` |
| `randomize_knockback_direction_except_for_finisher` | Chaotic knockback unless it kills the target. | Boolean (`true`/`false`) |
| `randomize_target_within_range` | Picks a random valid tile instead of the user's click. | Enum: `0`, `2`, `3` |
| `range_bonuses` | How much extra range is added by stats/passives. | Enum: `include_alpha` |
| `range_considers_character_size` | Range calculation accounts for large entities. | Boolean (`true`/`false`) |
| `range_display_include_aoe` | Visual: shows the full AoE potential when previewing range. | Boolean (`true`/`false`) |
| `range_display_include_character_size` | Visual: offsets the range indicator for 2x2 units. | Boolean (`true`/`false`) |
| `range_display_include_direction` | Visual: shows directional arrows. | Boolean (`true`/`false`) |
| `range_excludes_blocking` | Cannot target through walls/obstacles. | Boolean (`true`/`false`) |
| `range_excludes_self` | Cannot click on the caster's tile. | Boolean (`true`/`false`) |
| `range_max` / `range_min` | Alternate syntax for `max_range`/`min_range`. | Enum: `4` |
| `range_mode` | How range is counted (`standard`, `ground_move`). | Math Expression / Number (e.g. `5`, `X+1`) |
| `range_symmetry` | Mirrors the range grid. | Enum: `eight_way` |
| `recalc_target_on_castpoint` | Re-checks if target is valid at the exact frame of cast. | Boolean (`true`/`false`) |
| `redirect_location_if_blocked` | Shifts target to adjacent tile if original is invalid. | Boolean (`true`/`false`) |
| `remain_off_map` | Keeps entity removed from the grid. | Boolean (`true`/`false`) |
| `reorient_thrown_character` | Forces a thrown entity to face a certain way. | Boolean (`true`/`false`) |
| `restrictions` / `restructions` | Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`). | Array `[/*must_have_cat*/, aoe_must_be_displaceable, aoe_must_be_force_displaceable, aoe_must_exist, must_be_adjacent_to_ally, must_be_adjacent_to_enemy_fistoffate, must_be_adjacent_to_most_hurt_ally, must_be_conductive, must_be_directly_behind_character, must_be_directly_behind_enemy, must_be_directly_in_front_of_enemy, must_be_empty, must_be_moveable, must_be_swappable, must_have_ally, must_have_animate_character, must_have_buddy, must_have_cat, must_have_character, must_have_corpse, must_have_element, must_have_enemy, must_have_line_of_sight, must_have_liquid, must_have_living_character, must_have_player_cat, must_have_tag, must_match_locked_orientation, must_move, must_not_be_knockback_immune_animate_character, must_not_have_boss, must_not_have_large_character, must_not_have_tag, must_target_alpha_if_exists, must_target_cat_with_empty_or_destructible_weapon_slot]` |
| `reverse_target_direction` | Inverts the targeting vector. | Boolean (`true`/`false`) |
| `shotgun_mode` | Deals more damage/hits if targets are closer. | Boolean (`true`/`false`) |
| `shuffle_tile_order` | Randomizes the execution order of AoE tiles. | Boolean (`true`/`false`) |
| `special_tile_tag` | Targets only tiles with this specific tag. | Enum: `ChaosValidPosition`, `FinalBossCloneSpot`, `FinalBossTheChildLocation` |
| `spin_steps` | Number of rotational increments for spin targeting. | Enum: `-16` |
| `splash_damage_aoe_begin` | At what radius splash damage starts applying. | Enum: `1`, `999` |
| `stagger_multihit_targets` | Delays hits slightly between multiple targets. | Boolean (`true`/`false`) |
| `straight_shot` | Ensures projectiles do not arc. | Boolean (`true`/`false`) |
| `target_mode` | How the cursor operates (`tile`, `direction`, `none`). | Math Expression / Number (e.g. `5`, `X+1`) |
| `target_requires_element` | Target must be afflicted with this element. | Array `[grass, water]` |
| `target_requires_tag` | Target must possess this exact character tag. | Math Expression / Number (e.g. `5`, `X+1`) |
| `throw_consumed_character` | Throws the entity currently held/eaten. | Boolean (`true`/`false`) |
| `toss_direction_restriction` | Limits which ways an entity can be tossed. | Enum: `backwards`, `forwards` |
| `track_target` | Projectile/Effect follows moving targets. | Boolean (`true`/`false`) |
| `trample_allies_too` | Trample movement damages allies in the path. | Boolean (`true`/`false`) |
| `uncounterable` | Bypasses counter-attack passives. | Boolean (`true`/`false`) |
| `upgrade_straight_shot_to_boomerang` | Makes the projectile return to caster. | Boolean (`true`/`false`) |
| `upgrade_straight_shot_to_piercing` | Allows the projectile to pass through multiple targets. | Boolean (`true`/`false`) |

---

## 2. Damage & Combat Math (`damage_instance { ... }`)

| Property | Definition / Expected Behavior | Possible Inputs / Types |
| :--- | :--- | :--- |
| `accuracy` | Hit chance modifier. | Enum: `.5` |
| `ai_base_score` | How highly the AI values using this ability. | Math Expression / Number (e.g. `5`, `X+1`) |
| `blocked_damage` | Base damage dealt if the attack is blocked. | Enum: `"(3+bonus_melee_ability_damage)*2"`, `3+bonus_melee_ability_damage`, `5`, `5+bonus_melee_ability_damage`, `5+bonus_melee_damage`, `7+bonus_melee_ability_damage` |
| `blocked_multiplier` | Multiplier applied when hitting a blocking target. | Enum: `2` |
| `can_collect_pickups` | The damage instance can grab items on the ground. | Boolean (`true`/`false`) |
| `can_instapop` | Allows the attack to instantly destroy specific weak entities. | Boolean (`true`/`false`) |
| `can_revive` | Healing instance that can bring dead allies back to life. | Boolean (`true`/`false`) |
| `cant_miss` | Guarantees the hit, bypassing dodge mechanics. | Boolean (`true`/`false`) |
| `contact_requires_adjacency` | Contact effects only trigger if standing next to the target. | Boolean (`true`/`false`) |
| `crit_chance` | Override for base critical hit probability. | String/Value (e.g. `25%`, `-999999`) |
| `custom_additional_ai_weight` | Granular AI preference adjustments (e.g., `prefer_dont_move`). | Math Expression / Number (e.g. `5`, `X+1`) |
| `damage` | Base damage output (can be an integer or mathematical string equation). | Object `{ ... }` |
| `damage_shield_only` | Depletes shields but cannot harm base health. | Boolean (`true`/`false`) |
| `disallow_modifications` | Prevents passives from altering this damage instance. | Boolean (`true`/`false`) |
| `dont_break_tentacles` | Specific interaction override for tentacle entities. | Enum: `]` |
| `elements` | Array of elemental tags to apply (e.g., `[Fire Holy]`). | Array `[Bloom, Break_Web, Conducted, Dust, Earth, Earth,, Electric, Explosion, Fire, Grass, Gravity, HOLY, Heat, Holy, Ice, Lesser_Water, Metal, Mutate, Napalm, Poison, Quake, Rock, Shadow, Spikes, Water, Wind, Wind,, already, conducting,, conduction, damage, dont_break_tentacles, everything, from, hits, irrelevant, is, it, prevents, since]` |
| `faction` | Associates the damage with a specific team alignment. | Math Expression / Number (e.g. `5`, `X+1`) |
| `final_hit_bonus_damage` | Extra damage applied on the last hit of a multihit. | Enum: `5+bonus_melee_ability_damage` |
| `force_adjacent_and_diagonal_contact` | Treats diagonal hits as physical contact. | Boolean (`true`/`false`) |
| `force_no_contact` | Bypasses all contact-based retaliation (Thorns, etc). | Boolean (`true`/`false`) |
| `force_no_knockback` | Prevents the target from being pushed. | Boolean (`true`/`false`) |
| `force_play_hit_animation` | Forces the flinch animation even on 0 damage. | Boolean (`true`/`false`) |
| `heal` | Restores health instead of dealing damage. | Array `[10, 5]` |
| `HealthRegenUp` | Modifies the target's native regeneration stat. | Object `{ ... }` |
| `hint_dont_lowgravboost` | AI hint to ignore wind physics. | Boolean (`true`/`false`) |
| `hit_animation_alt` | Custom flinch animation for the target. | Enum: `catch` |
| `incidentally_collects_pickups` | Automatically grabs items in the AoE. | Boolean (`true`/`false`) |
| `knockback` | The base physics pushing power (in tiles). | String/Value (e.g. `6`, `"ceil(X*.25/5)"`) |
| `layer` | Z-index targeting (e.g., `characters`, `self`). | Math Expression / Number (e.g. `5`, `X+1`) |
| `makes_contact` | If false, explicitly avoids triggering contact-based passives. | Boolean (`true`/`false`) |
| `Mutate` / `Napalm` / `Poison` / `Explosion` / `Spikes` | Hardcoded status/effect injections. | Enum: `Poison`, `]` |
| `non_lethal` | Reduces target to 1 HP but will never kill. | Boolean (`true`/`false`) |
| `override_trample_damage` | Custom damage value for trample moves. | Boolean (`true`/`false`) |
| `piercing` | Ignores a percentage of target defense/armor. | Boolean (`true`/`false`) |
| `ranged` | Boolean flagging the damage as explicitly ranged. | Enum: `Ranged`, `true` |
| `raw_damage` / `raw_heal` | Unmitigated, unscaled base numbers. | String/Value (e.g. `int`, `"max((X-1)*2, 0)"`) |
| `show_damage_on_0` | Forces the "-0" floater text to appear. | Boolean (`true`/`false`) |
| `two_way_contact` | Both caster and target trigger contact effects on each other. | Boolean (`true`/`false`) |
| `type` | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). | Array `[attack, move, spell]` |

---

## 3. Action Economy & Ability Costs (`cost { ... }`)

| Property | Definition / Expected Behavior | Possible Inputs / Types |
| :--- | :--- | :--- |
| `act_points` | Consumes primary action points (default 1). | Math Expression / Number (e.g. `5`, `X+1`) |
| `allow_offmap_casts` | Can be used while the character is hidden/removed from grid. | Boolean (`true`/`false`) |
| `can_be_refreshed` | Passives/Effects can reset this ability's cooldown. | Boolean (`true`/`false`) |
| `can_cast_while_dead` | Usable by corpses (e.g., DeathRattle triggers). | Boolean (`true`/`false`) |
| `can_pay_over_multiple_turns` | Allows channeling costs over time. | Boolean (`true`/`false`) |
| `can_self_refresh` | The ability has mechanics to reset its own cooldown. | Boolean (`true`/`false`) |
| `cant_cast` | Explicitly disables casting (used for passive-triggered only abilities). | Math Expression / Number (e.g. `5`, `X+1`) |
| `cantrip` | Does not end the turn when cast. | Boolean (`true`/`false`) |
| `cantrip_group` | Groups cantrips so using one exhausts the others. | Math Expression / Number (e.g. `5`, `X+1`) |
| `charge` | Cooldown timers measured in turns. | Enum: `"1-clamp(spd,0,1)"`, `0`, `1` |
| `coins` | Consumes currency to cast. | Array `[1, 10, 20, 6]` |
| `damage_cant_be_zero` | Requires the ability to have >0 calculated damage to cast. | Boolean (`true`/`false`) |
| `disallow_cost_modification` | Prevents passives from making this cheaper. | Boolean (`true`/`false`) |
| `durability` | Consumes item durability. | Array `[1, 10, 12, 14, 16, 2, 20, 3, 4, 4,, 5, 6, 7, 7,, 8, 9]` |
| `enabled_formula` | Mathematical string required to be >0 to cast. | Enum: `1`, `1-X`, `X` |
| `infcantrip` | Can be cast infinitely as long as costs are met. | Boolean (`true`/`false`) |
| `initial_charge` | How many turns it starts on cooldown at battle start. | Boolean (`true`/`false`) |
| `main_turn_only` | Cannot be cast during bonus or dispersed turns. | Boolean (`true`/`false`) |
| `mana` | Consumes the character's mana pool. | String/Value (e.g. `6`, `10-X*6`) |
| `manacost_cant_be_zero` | Fails to cast if mana cost is reduced to 0. | Boolean (`true`/`false`) |
| `minimum_con` / `minimum_spd` | Stat thresholds required to cast. | Boolean (`true`/`false`) |
| `move_points` | Consumes movement points. | Enum: `0`, `1`, `2` |
| `must_be_consuming` | Requires the character to be eating/holding something. | Boolean (`true`/`false`) |
| `must_be_first_action` | Can only be used at the very start of the turn. | Boolean (`true`/`false`) |
| `must_be_first_nonmove_action` | Can move first, but cannot use other abilities first. | Boolean (`true`/`false`) |
| `must_be_offmap` | Requires the character to be hidden/dug underground. | Boolean (`true`/`false`) |
| `must_have_weapon` | Requires a weapon equipped in the item slot. | Boolean (`true`/`false`) |
| `must_not_be_a_summon` | Summons/Familiars cannot cast this. | Boolean (`true`/`false`) |
| `must_not_be_consuming` | Cannot be holding/eating an entity. | Boolean (`true`/`false`) |
| `once_per_fight` | Exhausts for the remainder of combat after one use. | Enum: `3-X`, `false`, `true` |
| `prime` | Requires a "priming" turn before it fires. | Boolean (`true`/`false`) |
| `require_default_size` | 2x2 or altered characters cannot cast this. | Boolean (`true`/`false`) |
| `requires_attack_damage_threshold` | Needs a certain amount of innate damage. | Enum: `2` |
| `requires_consumed_trinket` | Must have eaten a specific item type. | Boolean (`true`/`false`) |
| `requires_destructible_weapon` | The equipped weapon must be breakable. | Boolean (`true`/`false`) |
| `requires_empty_trinket` | Must not have an accessory equipped. | Boolean (`true`/`false`) |
| `requires_exact_character_aux` | Hardcoded character specific lock. | Math Expression / Number (e.g. `5`, `X+1`) |
| `requires_hp_threshold` | Must be below/above a certain health percentage. | Enum: `200` |
| `requires_reload` | Must spend an action to reload before casting again. | Boolean (`true`/`false`) |
| `start_reloaded` | Spawns with the ability pre-loaded. | Boolean (`true`/`false`) |

---

## 4. Entity Graphics & Animations (`graphics { ... }`)

| Property | Definition / Expected Behavior | Possible Inputs / Types |
| :--- | :--- | :--- |
| `affected_animation` / `affected_particle` | Visuals applied to the target receiving the effect. | Enum: `statDown` |
| `air_animation` | Animation played while entity is airborne. | Enum: `bellyflop_air`, `entrance`, `gravitySlam_air` |
| `ally_animation` | Distinct animation used when targeting a friendly unit. | Enum: `lickAttack` |
| `alt_animations` | Array rerouting base flash labels (`[[old, new]]`). | Array `[ButcherIdle, ColorlessStartTurn, DruidIdle, FighterIdle, HealerIdle, HunterIdle, JesterIdle, MageIdle, MonkIdle, NecromancerIdle, PsychicIdle, TankIdle, ThiefIdle, TinkererIdle, [StartTurn,, [dead, [deadhit, [dying, [dying,, [hit, [idle, [idle,, [stunned, [weak, brokenLeg, brokenPaw, concussion, cursed, dead], disfigured, dislocatedShoulder, dyingDisassembled], empty], girlyIdle], hitDisassembled], idleDisassembled], intestinalProlapse, poofOutOfExistance, skeletonCorpseHit], skeletonDead]]` |
| `always_play_animations` | Bypasses speed-up/skip logic. | Boolean (`true`/`false`) |
| `animate_name` | Animates the ability name text on cast. | Enum: `false`, `pointout`, `true` |
| `animation` | The primary flash animation label triggered. | String/Value (e.g. `turtlestart`, `spinAttack`) |
| `animation_in` / `animation_out` | Used for transition states (like burrowing). | Math Expression / Number (e.g. `5`, `X+1`) |
| `aoe_spell_on_land` | Visual trigger when a jump lands. | Boolean (`true`/`false`) |
| `apex_distance` / `apex_time` | Calculations for the peak of a jump/lob arc. | Enum: `0.875` |
| `area_particle` / `center_particle` / `miss_particle` | Specific spawn points for particles. | Math Expression / Number (e.g. `5`, `X+1`) |
| `art_flip` | Horizontally mirrors the movieclip. | Enum: `-1` |
| `beam_cap` / `beam_clip` | Flash movieclips used to render continuous laser beams. | Math Expression / Number (e.g. `5`, `X+1`) |
| `bounce_on_hit` | Visual hop when striking a target. | Boolean (`true`/`false`) |
| `chain_distance` / `chain_movieclip` | Creates a tethered repeating graphic (like a hook). | Enum: `.25`, `.38` |
| `custom_cat_data` | Overrides base visual traits of the cat. | Math Expression / Number (e.g. `5`, `X+1`) |
| `custom_priming_animation` | Animation used while charging an ability. | Math Expression / Number (e.g. `5`, `X+1`) |
| `darken_screen` | Dims the background during the ability cast. | Boolean (`true`/`false`) |
| `dash_animation` / `dash_start_` / `dash_bonk_` / `dash_end_` | State-specific animations for trample/dash abilities. | Math Expression / Number (e.g. `5`, `X+1`) |
| `decelerate` | Visual slowdown at the end of a movement. | Enum: `5` |
| `delay` | Frame delay before firing projectile/effect. | Math Expression / Number (e.g. `5`, `X+1`) |
| `delay_from_map_center` / `edge` | Positional based timing delays. | Boolean (`true`/`false`) |
| `depth_offset` | Z-index rendering adjustment. | Math Expression / Number (e.g. `5`, `X+1`) |
| `detatched_animation` | Plays an animation separated from the character body. | Math Expression / Number (e.g. `5`, `X+1`) |
| `do_damage_immediately` | Applies math before the animation actually hits. | Boolean (`true`/`false`) |
| `easing` | Smoothing function for movement animations. | Boolean (`true`/`false`) |
| `face_targets` | Forces the sprite to look at the target tile. | Boolean (`true`/`false`) |
| `fall_from_sky` | Spawns the projectile from the top of the screen. | Boolean (`true`/`false`) |
| `jump_attack_animation` / `jump_height_multiplier` | Overrides for jump physics. | Math Expression / Number (e.g. `5`, `X+1`) |
| `lob_height` / `lob_speed` / `lob_yoff` | Adjustments for arcing projectiles. | Math Expression / Number (e.g. `5`, `X+1`) |
| `lock_orientation_during_dash` | Prevents the sprite from flipping mid-dash. | Boolean (`true`/`false`) |
| `start` / `loop` / `end` | Segments for continuous channeled animations. | Object `{ ... }` |
| `move_speed_multiplier` | Adjusts walking animation speed. | Math Expression / Number (e.g. `5`, `X+1`) |
| `movieclip` | Overrides the base flash symbol (e.g., `HumanCat`). | Array `[TinyTumorA, TinyTumorB, TinyTumorC]` |
| `no_horizontal_flip` | Prevents the engine from mirroring the sprite when facing left. | Boolean (`true`/`false`) |
| `palette` | Swaps the color palette ID. | Array `[50, 51, 52, 53, 54, 55, 62, 63, 64, 65, 66, 68]` |
| `particle` | References an impact or cast particle effect. | Math Expression / Number (e.g. `5`, `X+1`) |
| `portrait_face` | Overrides the UI portrait face. | Math Expression / Number (e.g. `5`, `X+1`) |
| `projectile` | References a projectile entity. | Math Expression / Number (e.g. `5`, `X+1`) |
| `random_delay` | Adds chaotic timing to multi-projectile casts. | Array `[0,, 100, 120, 30, 50, 70]` |
| `scale` | Multiplier for the visual size of the entity/effect. | Object `{ ... }` |
| `shade_occluded_objects` | Renders a shadow over things behind this object. | Boolean (`true`/`false`) |
| `shadow` / `shadow_size` | Toggles and scales the ground shadow drop. | Math Expression / Number (e.g. `5`, `X+1`) |
| `speed` | Base speed of the projectile/animation. | Object `{ ... }` |
| `tint` | Applies a color overlay to the movieclip. | Array `[.4,, .7, .7,, 0, 0,, 1]` |
| `use_super_armor` | Prevents flinch animations from interrupting this cast. | Boolean (`true`/`false`) |

---

## 5. Character & NPC Engine Properties (`properties { ... }` & `stats { ... }`)

| Property | Definition / Expected Behavior | Possible Inputs / Types |
| :--- | :--- | :--- |
| `access_to_player_inventory` | Allows the NPC to use items from the player's bag. | Boolean (`true`/`false`) |
| `aggro_target_is_enemy` | Reverses standard AI targeting to attack its own team. | Boolean (`true`/`false`) |
| `allow_offmap_corpse` | The body persists even if killed over a pit/off map. | Boolean (`true`/`false`) |
| `always_triggers_traps` | Cannot safely path over traps. | Boolean (`true`/`false`) |
| `banned_elite_buffs` | Array of elite modifiers this enemy is not allowed to roll. | Array `[Depressing, Mad, Protected, Shielded1, Shielded2, Shielded3, Shielded4, Twin]` |
| `boss_minions_runaway` | If this boss dies, all its minions flee the battle. | Boolean (`true`/`false`) |
| `can_be_backstabbed` | Susceptible to directional flank damage. | Boolean (`true`/`false`) |
| `can_be_champion` / `can_be_elite` | Allowed to spawn as higher-tier variants. | Boolean (`true`/`false`) |
| `can_run` | AI is allowed to flee combat when broken. | Boolean (`true`/`false`) |
| `champion` / `elite` | Hardcodes the entity to spawn as this tier. | Boolean (`true`/`false`) |
| `corpse_health` | HP of the dead body (0 means it vanishes instantly). | Math Expression / Number (e.g. `5`, `X+1`) |
| `deathpoof_size` | Size of the smoke cloud when killed. | Boolean (`true`/`false`) |
| `disperse_main_turns` | AI quirk: spreads out action points across the round. | Boolean (`true`/`false`) |
| `dispersed_bonus_turns` | Grants extra innate action points to the character. | Math Expression / Number (e.g. `5`, `X+1`) |
| `divine_shield` | Spawns with a shield that completely blocks 1 instance of damage. | Object `{ ... }` |
| `exclude_from_hallucinate` | Cannot be targeted by random hallucination effects. | Boolean (`true`/`false`) |
| `faction` | Determines alignment (`enemies`, `cats`, `neutral`). | Math Expression / Number (e.g. `5`, `X+1`) |
| `first_turn_is_main_turn` | Forces the entity to act early in the round logic. | Boolean (`true`/`false`) |
| `flying` | Ignores ground terrain and traps. | Boolean (`true`/`false`) |
| `health` / `base_health` | Current and starting Max HP. | String/Value (e.g. `400`, `185`) |
| `hidden_tag` / `tag` | Categorizes the entity for specific targeting conditionals. | Array `[bird, bonusbird, megadino, megadinoleg, moonboss, moonhand, moonhead, themother, themotherspike]` |
| `inanimate` / `speculative_inanimate` | Treats the unit as an object (like a rock or barrel). | Boolean (`true`/`false`) |
| `initiative` / `base_initiative` | Turn order calculation stat. | Math Expression / Number (e.g. `5`, `X+1`) |
| `kill_required` | The combat encounter will not end until this specific unit is dead. | Boolean (`true`/`false`) |
| `knockback_immune` | Cannot be pushed by physics vectors. | Boolean (`true`/`false`) |
| `mana` / `base_mana_regen` | MP pool and how much it restores per turn. | String/Value (e.g. `6`, `10-X*6`) |
| `move_block` | Controls pathing collision (e.g., `everything_even_when_dead`). | Enum: `everything_even_when_dead`, `nothing` |
| `movement` / `base_movement` | Base movement tiles per turn. | Math Expression / Number (e.g. `5`, `X+1`) |
| `shield` | Spawns the unit with innate temporary shielding. | Object `{ ... }` |
| `size` | Scales the grid footprint (e.g., `2x2`). | Array `[.1, .15, .2, .3, .4, .5, .6, .8, .85, .9, 0, 1, 1.2, 1.3, 1.5, 1.8, 2, 2.3, 3, 5]` |
| `takes_turns` / `takes_main_turn` | If false, the entity exists but never acts in combat. | Boolean (`true`/`false`) |
| `tall` | Blocks line of sight behind it. | Boolean (`true`/`false`) |
| `visually_spiky` | Renders a spiky outline (often paired with Thorns). | Boolean (`true`/`false`) |
| **Stats:** `strength`, `dexterity`, `constitution`, `intelligence`, `speed`, `charisma`, `luck` | The 7 core RPG attributes. (Aliases: `str`, `dex`, `con`, `int`, `spd`, `cha`, `lck`). |
