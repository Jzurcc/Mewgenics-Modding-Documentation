# Mewgenics Mod Developer Documentation: Exhaustive Enemy Attacks Reference

This file lists all enemies categorized by Tier. Under each enemy is an exhaustive list of all abilities they use, broken down by their internal mechanical engine properties.

# Bosses

## Boris

### MoveOne (`MoveOne`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Trample Dash (`TrampleDash`)

- **Template:** `trample_dash`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 8+bonus_melee_damage`

---

## Bumblefoot

### Fart (`BumbleButt`)

- **Template:** `spell`
- **Cost:** `cantrip true, mana 4`
- **Target/Shape:** `target_mode none, aoe_mode standard, min_aoe 1, max_aoe 1, aoe_considers_character_size true, aoe_excludes_self true, dont_orient true`
- **Damage/Effects:** `damage 0, knockback 1, Poison 2`

### Feast (`BumblefootAttemptEatCat`)

- **Template:** `teleport`
- **Cost:** `act_points 1`
- **Target/Shape:** `max_range 20, aoe_restrictions must_have_animate_character, restrictions [must_be_moveable aoe_must_exist], knockback_mode zero`
- **Damage/Effects:** `type melee, damage 5+bonus_melee_damage, makes_contact true, override_trample_damage true, SetDistanceDisplace 5, IgnoreSelf 1`

### Bone Spurt (`BumblefootBoneShot`)

- **Template:** `lobbed_attack`
- **Cost:** `act_points 1`
- **Target/Shape:** `target_mode none, max_aoe 2, aoe_considers_character_size true, aoe_excludes_self true, max_targets 6, can_multihit true, aoe_restrictions [must_not_have_corpse]`
- **Damage/Effects:** `ai_base_score 9999, Bruise 1`

### Feast (`BumblefootEatCat`)

- **Template:** `teleport`
- **Cost:** `act_points 1`
- **Target/Shape:** `max_range 20, aoe_restrictions must_have_animate_character, restrictions [must_be_moveable aoe_must_exist], ally_priority 1, corpse_priority 5, enemy_priority 10, knockback_mode zero`
- **Damage/Effects:** `type melee, damage 0, piercing true, cant_miss true, makes_contact true, Vaporize 20, IgnoreSelf 1`

### Feast (`BumblefootEatCorpse`)

- **Template:** `teleport`
- **Cost:** `act_points 1`
- **Target/Shape:** `max_range 20, aoe_restrictions must_have_destructible_corpse, restrictions [must_be_moveable aoe_must_exist], corpse_priority 10, knockback_mode zero`
- **Damage/Effects:** `type melee, damage 0, piercing true, cant_miss true, ai_base_score 9999, makes_contact true, Vaporize 20, IgnoreSelf 1`

### Bumble Jump (`BumblefootLeap`)

- **Template:** `jump_attack`
- **Cost:** `act_points 1`
- **Target/Shape:** `min_range 4, max_range 6, min_aoe 0, max_aoe 1`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1, ai_base_score 9999, IgnoreSelf 1`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## C-1000

### DoNothing (`DoNothing`)

- **Template:** `placeholder`
- **Cost:** `cant_cast true`
- **Target/Shape:** `target_mode none, aoe_mode none, range_mode none`
- **Damage/Effects:** `None`

### T2Clone (`T2Clone`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, Cleanse 0, RemoveStatus DodgeChance_Status, RemoveStatus SpeedUp_WithoutInitiative`

### T2GoopRun (`T2GoopRun`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### T2SpearMelee (`T2SpearMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 3`
- **Damage/Effects:** `damage 10+bonus_melee_damage, piercing true`

### T2UnClone (`T2UnClone`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, RemoveStatus T2CopyCatInternal, Cleanse 0`

---

## C-800

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### MoveOne (`MoveOne`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

### T1ChokeReaction (`T1ChokeReaction`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode tile_to_character, aoe_considers_character_size false, target_mode tile, restrictions must_have_character, range_mode standard, aoe_mode standard, min_range 1, max_range 1, min_aoe 0, max_aoe 0`
- **Damage/Effects:** `damage 5+bonus_melee_damage, Stun 1`

### T1Pummel (`T1Pummel`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `aoe_considers_character_size false, target_mode tile, restrictions must_have_character, range_mode standard, aoe_mode standard, min_range 1, max_range 1, min_aoe 0, max_aoe 0, multihit 6`
- **Damage/Effects:** `damage -3+bonus_melee_damage, IntelligenceUp -1, FaceAway 1`

### T1SwapWeapon (`T1SwapWeapon`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, pool [TerminatorShotgun TerminatorSniper TerminatorUzi]`

### Throw Grenade (`T1ThrowGrenadeA`)

- **Template:** `spawn`
- **Cost:** `cantrip true`
- **Target/Shape:** `range_mode standard, min_range 3, max_range 6`
- **Damage/Effects:** `custom_additional_ai_weight spread_grenades`

### T1ThrowGrenadeB (`T1ThrowGrenadeB`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Chubs

### ChubsGoop (`ChubsGoop`)

- **Template:** `straightshot_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_aoe 10`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, Poison 2`

### ChubsRage (`ChubsRage`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "Rage"`

### Chub Spin (`ChubsSpin`)

- **Template:** `melee_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode square, knockback_mode character_to_tile`
- **Damage/Effects:** `damage 5+bonus_melee_damage`

---

## Crater Maker

### Consume! (`AlienBeastEat`)

- **Template:** `melee_attack`
- **Cost:** `requires_exact_character_aux 1`
- **Target/Shape:** `aoe_mode custom, aoe_symmetry none, custom_aoe [[2, 0]], aoe_considers_character_size false, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 99999, cant_miss true, ai_base_score 999999, Vaporize 1, VaporizeInanimate 1`

### AlienBeastGoop (`AlienBeastGoop`)

- **Template:** `straightshot_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode custom, custom_aoe      [[0,  1], [0, 1], [0, 1],    [0,  -1], [0, -1], [0, -1]], custom_aoe_util [[-1, 1], [0, 1], [1, 1],    [-1, -1], [0, -1], [1, -1]]`
- **Damage/Effects:** `damage 4+bonus_ranged_damage, Poison 1`

### AlienBeastMoveOne (`AlienBeastMoveOne`)

- **Template:** `*(None)*`
- **Cost:** `requires_exact_character_aux 2`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### AlienBeastOpenEyes (`AlienBeastOpenEyes`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 999999, change -1, max 3`

### Pukewave (`AlienBeastPuke`)

- **Template:** `lobbed_attack`
- **Cost:** `requires_exact_character_aux 2`
- **Target/Shape:** `target_mode none, aoe_mode custom, aoe_symmetry eight_way, custom_aoe [ [1 1] [2 2] [3 3] [4 4] [5 5] [6 6] [7 7] [8 8] [9 9], [0 1] [1 2] [2 3] [3 4] [4 5] [5 6] [6 7] [7 8] [8 9] [9 9] ], aoe_excludes_self true, aoe_considers_character_size false, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, ai_base_score 999999, Poison 1, SpawnCreep 1`

### Rampage! (`AlienBeastRampage`)

- **Template:** `trample_dash`
- **Cost:** `requires_exact_character_aux 3`
- **Target/Shape:** `target_mode direction, max_range 16, max_bounces 3, restrictions aoe_must_exist, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 3+bonus_melee_damage, ai_base_score 999999, Immobile [1 .5]`

### Crater Howl! (`AlienBeastScream`)

- **Template:** `spell`
- **Cost:** `requires_exact_character_aux 0`
- **Target/Shape:** `target_mode none, aoe_mode all, prioritize_dont_change_direction true, aoe_excludes_self true`
- **Damage/Effects:** `damage 10, ai_base_score 999999, Stun [1 .5], Immobile [1 .5]`

### Melee Attack (`BasicBigMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range`
- **Damage/Effects:** `None`

---

## Debug_MegaGuppyPhase3

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### DbgBackgroundTransitionTest (`DbgBackgroundTransitionTest`)

- **Template:** `self_buff`
- **Cost:** `mana 0, infcantrip true, allow_offmap_casts true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 999999`

---

## Dreadnoughtus

### MD_HeadDrop (`MD_HeadDrop`)

- **Template:** `return`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20, aoe_excludes_self true, max_aoe 1, aoe_mode square, aoe_considers_character_size true, restrictions none`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 5, override_trample_damage true, IgnoreSelf 1, tag megadino, IgnoreDamage 1`

### MD_HeadLeave (`MD_HeadLeave`)

- **Template:** `leave`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 99999`

### MD_Kick (`MD_Kick`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `restrictions must_match_locked_orientation`
- **Damage/Effects:** `damage 7+bonus_melee_damage, tag megadino`

### MD_LegLeave (`MD_LegLeave`)

- **Template:** `leave`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### MD_LegReturn (`MD_LegReturn`)

- **Template:** `return`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `damage 3, ForceDisplace 1, IgnoreSelf 1`

### MD_Lift (`MD_Lift`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form Default, FormChange Lifted`

### Defecate (`MD_Poop`)

- **Template:** `self_buff`
- **Cost:** `allow_offmap_casts true, must_be_offmap true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 999`

### MD_Stomp (`MD_Stomp`)

- **Template:** `spell`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode none, aoe_mode square, min_aoe 0, max_aoe 1, knockback_mode character_to_tile, aoe_excludes_self true, prioritize_dont_change_direction true, aoe_considers_character_size true`
- **Damage/Effects:** `damage 7+bonus_melee_damage, knockback 1, IgnoreSelf 1, time 2, intensity 10`

### MD_Walk (`MD_Walk`)

- **Template:** `jump_move`
- **Cost:** `Free`
- **Target/Shape:** `aoe_considers_character_size false, range_considers_character_size false`
- **Damage/Effects:** `damage 5+bonus_melee_damage`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Dust Devil

### Dust Dash (`DustDash`)

- **Template:** `dash_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode cross, knockback_mode character_to_tile, restrictions dash_must_move`
- **Damage/Effects:** `damage 3+bonus_melee_damage, custom_additional_ai_weight favor_tile_far_away, min_dist 2, max_dist 3, damage inherit, exclude_prefix Twister`

### DustMelee (`DustMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, Bruise 1`

### DustMove (`DustMove`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `restrictions [must_be_moveable must_move must_be_empty]`
- **Damage/Effects:** `None`

### DustTeleport (`DustTeleport`)

- **Template:** `teleport`
- **Cost:** `cantrip true, move_points 0, mana 5`
- **Target/Shape:** `max_range 6`
- **Damage/Effects:** `None`

---

## Dybbuk

### DybbukEscape (`DybbukEscape`)

- **Template:** `jump_move`
- **Cost:** `Free`
- **Target/Shape:** `min_range 2, max_range 5, restrictions [must_be_moveable must_move]`
- **Damage/Effects:** `None`

### DybbukLick (`DybbukLick`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ManaSteal -1`

### Possess (`DybbukPossess`)

- **Template:** `jump_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `remain_off_map true, aoe_excludes_self false, max_aoe 0, min_aoe 0, max_range 20, restrictions must_have_cat`
- **Damage/Effects:** `damage 0, cant_miss true, type spell, makes_contact false, IgnoreSelf 1`

### DybbukRePossess (`DybbukRePossess`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Reanimate (`DybbukReanimate`)

- **Template:** `targeted_status`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 3, max_aoe 0, aoe_restrictions must_have_corpse, restrictions aoe_must_exist`
- **Damage/Effects:** `Reanimate 100%`

### Return (`DybbukReturn`)

- **Template:** `jump_move`
- **Cost:** `allow_offmap_casts true`
- **Target/Shape:** `max_aoe 0, min_aoe 0, max_range 20`
- **Damage/Effects:** `None`

### DybbukWisps (`DybbukWisps`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, max_aoe 1, max_targets 2, multihit 2, stagger_multihit_targets true`
- **Damage/Effects:** `None`

---

## Gemini Cats

### Bite (`GeminiBite`)

- **Template:** `melee_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee`

### Geminado (`GeminiSpecial`)

- **Template:** `spell`
- **Cost:** `mana 5`
- **Target/Shape:** `target_mode direction, aoe_mode square, min_aoe 0, max_aoe 10, aoe_excludes_self true, knockback_mode to_map_center`
- **Damage/Effects:** `damage 0, knockback 3`

### Swipe (`GeminiSwipe`)

- **Template:** `melee_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode custom, aoe_symmetry none, custom_aoe [[1, -1] [1, 0] [1, 1]]`
- **Damage/Effects:** `damage 1+bonus_melee_damage, type melee, Bruise 1`

---

## Hitler

### DoNothing (`DoNothing`)

- **Template:** `placeholder`
- **Cost:** `cant_cast true`
- **Target/Shape:** `target_mode none, aoe_mode none, range_mode none`
- **Damage/Effects:** `None`

### GooseStep (`GooseStep`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 3, override_trample_damage true, SetDistanceDisplace 5`

### HitlerHeadGrowA (`HitlerHeadGrowA`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, max_aoe 20, aoe_restrictions [must_have_tag must_have_living_character], target_requires_tag hitler_clone_fetus, max_targets 2`
- **Damage/Effects:** `damage 0, cant_miss true, type status_spell, ImmediateUseAbility HitlerCloneTransform`

### HitlerHeadGrowB (`HitlerHeadGrowB`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### HitlerHeadTransform (`HitlerHeadTransform`)

- **Template:** `self_buff`
- **Cost:** `cant_cast X`
- **Target/Shape:** `X_is custom`
- **Damage/Effects:** `None`

### HitlerHeil (`HitlerHeil`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, max_aoe 20, aoe_restrictions [must_have_tag must_have_living_character], target_requires_tag hitler_clone, knockback_mode tile_to_character`
- **Damage/Effects:** `damage 0, cant_miss true, type status_spell, tag grown_hitler_clone, FaceAway 1, ImmediateUseAbility HitlerCloneHeil`

### Nuke (`HitlerNuke`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode all, target_mode none, aoe_excludes_self true, aoe_restrictions must_have_piercing_line_of_sight`
- **Damage/Effects:** `damage 50, CorpseVaporizer 1`

### HitlerPulp1 (`HitlerPulp1`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode all`
- **Damage/Effects:** `type status_spell, ai_base_score 9999, cant_miss true, Cleanse 0, Adrenaline 10`

### HitlerPulp2 (`HitlerPulp2`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `FormChange Pulp3`

### HitlerPulp3 (`HitlerPulp3`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `FormChange Pulp4`

### HitlerPulp4 (`HitlerPulp4`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `FormChange Pulp5`

### HitlerPulp5 (`HitlerPulp5`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `FormChange Pulp6`

### HitlerPulp6 (`HitlerPulp6`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `FormChange Pulp7`

### HitlerShoot (`HitlerShoot`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20, min_range 1`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, tag hitler_clone, can_instapop false, force_no_hit_animation true`

### HitlerSuicide (`HitlerSuicide`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, min_range 0, max_range 0, min_aoe 0, max_aoe 0, aoe_excludes_self false, aoe_mode standard, multihit 2`
- **Damage/Effects:** `damage 0, type status_spell, cant_miss true, DelayCastAbility HitlerNuke`

### T3Counter (`T3Counter`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `knockback 3`

### T3Intro (`T3Intro`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `prioritize_face_camera true`
- **Damage/Effects:** `ai_base_score 99999`

### T3JoinFight (`T3JoinFight`)

- **Template:** `return`
- **Cost:** `allow_offmap_casts true, must_be_offmap true, cantrip true, once_per_fight true, cant_cast X`
- **Target/Shape:** `max_range 20, min_range 0, X_is custom, force_ai_target_as_spell true, prioritize_face_camera true, allow_any_orientation true`
- **Damage/Effects:** `ai_base_score 100`

### T3RipAndTear (`T3RipAndTear`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1`
- **Damage/Effects:** `type melee, damage 0, piercing true, cant_miss true, Vaporize 20`

### T3Spawn_Butcher (`T3Spawn_Butcher`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### T3Spawn_Colorless (`T3Spawn_Colorless`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### T3Spawn_Druid (`T3Spawn_Druid`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### T3Spawn_Fighter (`T3Spawn_Fighter`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### T3Spawn_Hunter (`T3Spawn_Hunter`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### T3Spawn_Jester (`T3Spawn_Jester`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### T3Spawn_Mage (`T3Spawn_Mage`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### T3Spawn_Medic (`T3Spawn_Medic`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### T3Spawn_Monk (`T3Spawn_Monk`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### T3Spawn_Necromancer (`T3Spawn_Necromancer`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### T3Spawn_Psychic (`T3Spawn_Psychic`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### T3Spawn_Tank (`T3Spawn_Tank`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### T3Spawn_Thief (`T3Spawn_Thief`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### T3Spawn_Tinkerer (`T3Spawn_Tinkerer`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Johnny

### Mind Blast (`JohnnyBlast`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode circle, min_aoe 0, max_aoe 2, aoe_excludes_self true, aoe_considers_character_size true`
- **Damage/Effects:** `damage 3+bonus_basic_spell_damage, knockback 2, Stun [1 .1]`

### JohnnyCryOne (`JohnnyCryOne`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `JohnnyCriesForWashers 1`

### JohnnyCryTwo (`JohnnyCryTwo`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `JohnnyCriesForWashers 2`

### Mega Mind Blast (`JohnnyMegaBlast`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode circle, min_aoe 0, max_aoe 20, aoe_excludes_self true, aoe_considers_character_size true`
- **Damage/Effects:** `damage 3+bonus_basic_spell_damage, knockback 10, OverrideKnockbackDamage 3+bonus_basic_spell_damage, Stun [1 .1]`

### Mind Control (`JohnnyMindControl`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 0, max_range 20`
- **Damage/Effects:** `damage 0, type spell, custom_additional_ai_weight avoid_redundant_debuffs_strict, Charmed 1`

### JohnnyPull (`JohnnyPull`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode target_to_character`
- **Damage/Effects:** `None`

### Telekinesis (`JohnnyPush`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 0, max_range 20, knockback_mode character_to_target`
- **Damage/Effects:** `damage 3+bonus_basic_spell_damage, knockback 10, OverrideKnockbackDamage 3+bonus_basic_spell_damage`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Lord Bunga

### BungaEatCat (`BungaEatCat`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1, restrictions cant_target_behind`
- **Damage/Effects:** `type melee, damage 0, piercing true, cant_miss true, Vaporize 20`

### BungaEntrance (`BungaEntrance`)

- **Template:** `jump_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode random_farthest_tile, range_mode custom, custom_range [ [0 0] [-1 0] [-2 0] [-3 0] [-4 0] ], max_range 4, max_aoe 2, aoe_mode circle, aoe_considers_character_size false, range_considers_character_size false`
- **Damage/Effects:** `damage 0, IgnoreSelf true, stacks 3, distance 3`

### Booga! (`BungaRoar`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode all, prioritize_dont_change_direction true, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, ai_base_score 999999, Slow 2`

### BungaSwipe (`BungaSwipe`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_leading_edge_only true, aoe_mode custom, aoe_symmetry none, custom_aoe [[0, -1] [0, 0] [0, 1] [1, -1] [1, 0] [1, 1] [2, 0]], restrictions cant_target_behind`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, knockback 3`

### DoNothing (`DoNothing`)

- **Template:** `placeholder`
- **Cost:** `cant_cast true`
- **Target/Shape:** `target_mode none, aoe_mode none, range_mode none`
- **Damage/Effects:** `None`

---

## Man In The Moon

### MoonHead_Barrage (`MoonHead_Barrage`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `range_mode none, target_mode direction, aoe_mode cone, max_aoe 10, min_aoe 1, aoe_leading_edge_only true, aoe_considers_character_size true, aoe_excludes_self true, can_multihit false, restrictions must_match_locked_orientation`
- **Damage/Effects:** `damage 10+bonus_ranged_damage, ai_base_score 999999, Bruise 1`

### :O (`MoonHead_BeginCharge`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "Charging"`

### MoonHead_Blow (`MoonHead_Blow`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `range_mode none, target_mode direction, aoe_mode cone, max_aoe 10, min_aoe 1, aoe_leading_edge_only true, aoe_considers_character_size true, aoe_excludes_self true, can_multihit false, restrictions must_match_locked_orientation, knockback_mode orientation`
- **Damage/Effects:** `damage 0, ai_base_score 999999, knockback 10, tag moonhand, IgnoreDamage 1`

### Call for Help (`MoonHead_CallForHelp`)

- **Template:** `spawn`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `target_mode none, aoe_mode square, max_aoe 20, max_targets 4`
- **Damage/Effects:** `None`

### MoonHead_ChewCat (`MoonHead_ChewCat`)

- **Template:** `self_buff`
- **Cost:** `must_be_consuming true`
- **Target/Shape:** `target_mode none, knockback_mode none, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, contact_requires_adjacency false, ai_base_score 9999`

### MoonHead_CommandHeadPunch (`MoonHead_CommandHeadPunch`)

- **Template:** `targeted_status`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `aoe_mode all, restrictions [must_have_tag must_have_living_character], target_requires_tag moonhand`
- **Damage/Effects:** `type none, damage 0, ai_base_score 999999, cant_miss true, tag moonhand, form Default, UseAbility MoonHandPunchHead`

### MoonHead_Digest (`MoonHead_Digest`)

- **Template:** `self_buff`
- **Cost:** `must_be_consuming true`
- **Target/Shape:** `target_mode none, knockback_mode none, prioritize_dont_change_direction true`
- **Damage/Effects:** `Vaporize 1`

### MoonHead_EatCat (`MoonHead_EatCat`)

- **Template:** `targeted_status`
- **Cost:** `mana 0, must_not_be_consuming true, cantrip true`
- **Target/Shape:** `max_range 2, min_range 2, range_mode cross, range_considers_character_size false, aoe_considers_character_size false, restrictions [must_have_living_character must_match_locked_orientation must_not_have_large_character]`
- **Damage/Effects:** `type none, damage 0, cant_miss true, layer characters, ai_base_score 99999, FormChange HasCat`

### MoonHead_Finisher (`MoonHead_Finisher`)

- **Template:** `spell`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode none, aoe_mode square, max_aoe 20`
- **Damage/Effects:** `damage 0, type none, cant_miss true, makes_contact false, ai_base_score 999999, tag moonhand, ImmediateUseAbility MoonHandMegaSqueeze`

### MoonHead_RefreshBrace (`MoonHead_RefreshBrace`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `custom_additional_ai_weight moonhead_use_if_cracked, RemoveStatus Brace, Brace 10, ReformMoonHead 1`

### MoonHead_SacrificeHand (`MoonHead_SacrificeHand`)

- **Template:** `targeted_status`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `max_range 20, target_mode random_tile, restrictions [must_have_tag must_have_living_character], target_requires_tag moonhand`
- **Damage/Effects:** `type none, damage 0, cant_miss true, layer characters, ai_base_score 999999, Die 1`

### MoonHead_SpawnHand (`MoonHead_SpawnHand`)

- **Template:** `spawn`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode none, aoe_mode square, min_aoe 2, max_aoe 20, min_targets 1, max_targets 1, aoe_restrictions [must_be_empty]`
- **Damage/Effects:** `None`

### MoonHead_SpitCat (`MoonHead_SpitCat`)

- **Template:** `throw_attack`
- **Cost:** `mana 0, must_be_consuming true`
- **Target/Shape:** `target_mode tile, max_range 20, min_range 3, range_mode standard, restrictions must_match_locked_orientation, prioritize_dont_change_direction true, throw_consumed_character true`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, blocked_damage 5+bonus_melee_ability_damage, ai_base_score 9999, custom_additional_ai_weight toss_far`

### MoonHead_SpitCat_AndDie (`MoonHead_SpitCat_AndDie`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Moon Hand

### MoonHandDash (`MoonHandDash`)

- **Template:** `dash_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction8, consider_trample true`
- **Damage/Effects:** `damage 10+bonus_melee_damage, knockback 10, tag moonhead, RemoveStatus Brace, BonusDamage 10, CrackMoonHead 1`

### MoonHandDrop (`MoonHandDrop`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `target_mode random_tile, restrictions none, prioritize_dont_change_direction true, allow_any_orientation true`
- **Damage/Effects:** `None`

### MoonHandDrop_Deathrattle (`MoonHandDrop_Deathrattle`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### MoonHandGrab (`MoonHandGrab`)

- **Template:** `targeted_status`
- **Cost:** `mana 0, must_not_be_consuming true, cantrip true`
- **Target/Shape:** `max_range 1, range_mode cross, restrictions [must_have_living_character /*must_have_cat*/]`
- **Damage/Effects:** `type none, damage 0, cant_miss true, layer characters, instant true, mount_mode auto, force_contact true, drop_body_ability MoonHandDrop, do_not_pop_corpse true, struggle_ability MoonHandFlail`

### MoonHandMegaSqueeze (`MoonHandMegaSqueeze`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, knockback_mode none, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 999, type melee, contact_requires_adjacency false, ai_base_score 9999, Vaporize 1`

### MoonHandPunchHead (`MoonHandPunchHead`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `custom_additional_ai_weight moonhead_punchself, IgnoreDamage 1`

### MoonHandSlap (`MoonHandSlap`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Bruise 1`

### MoonHandThrow (`MoonHandThrow`)

- **Template:** `throw_attack`
- **Cost:** `mana 0, must_be_consuming true`
- **Target/Shape:** `max_range 4, min_range 3, restrictions none, throw_consumed_character true`
- **Damage/Effects:** `damage 1, blocked_damage 5+bonus_melee_ability_damage, custom_additional_ai_weight toss_towards_bottomleft, Bruise 1`

---

## Nubs

### NubsGoop (`NubsGoop`)

- **Template:** `lobbed_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [[3, 0]]`
- **Damage/Effects:** `damage 8+bonus_ranged_damage, SpawnCreep 1, Poison 2`

### Nub Flub (`NubsJump`)

- **Template:** `jump_attack`
- **Cost:** `act_points 1`
- **Target/Shape:** `min_range 2, max_range 2, aoe_mode square`
- **Damage/Effects:** `damage 4+bonus_melee_damage, knockback 1, IgnoreSelf 1`

### Nuke (`NubsNuke`)

- **Template:** `spell`
- **Cost:** `mana 0, prime 1`
- **Target/Shape:** `aoe_mode all, target_mode none, aoe_excludes_self true, aoe_restrictions must_have_piercing_line_of_sight`
- **Damage/Effects:** `damage 50, CorpseVaporizer 1`

---

## Ornstein

### Gasp (`Magnetize`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [, [1, 1], [2, 1], [3, 1], [4, 1], [5, 1], [6, 1], [7, 1], [8, 1], [9, 1], [10, 1], [1, 0], [2, 0], [3, 0], [4, 0], [5, 0], [6, 0], [7, 0], [8, 0], [9, 0], [10, 0], [1,-1], [2,-1], [3,-1], [4,-1], [5,-1], [6,-1], [7,-1], [8,-1], [9,-1], [10,-1], ], knockback_mode perp_towards_facing_middle_pull`
- **Damage/Effects:** `damage 0, knockback 1, custom_additional_ai_weight magnetize_favorlineup, elements [, Wind, ]`

### SpearPoke (`SpearPoke`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_aoe 4`
- **Damage/Effects:** `damage 5+bonus_melee_damage`

### Toss (`YeetTowardsBuddy`)

- **Template:** `throw_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 7, restrictions none`
- **Damage/Effects:** `damage 1, blocked_damage 5+bonus_melee_ability_damage, custom_additional_ai_weight toss_towards_buddy`

---

## Pyrophina

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### PyrophinaSoloAttack (`PyrophinaSoloAttack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `knockback 3`

### PyrophinaSoloCatThrow (`PyrophinaSoloCatThrow`)

- **Template:** `throw_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 10, restrictions must_be_empty`
- **Damage/Effects:** `damage 2, custom_additional_ai_weight pyrophina_throw_to_lava`

### Volcano Stomp (`PyrophinaSoloEarthquakeStomp`)

- **Template:** `spell`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode none, aoe_mode map_edges`
- **Damage/Effects:** `damage 1, ai_base_score 9999, Burn 2`

### Fire Breath (`PyrophinaSoloFlamethrower`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode narrow_cone, aoe_leading_edge_only true, min_aoe 1, max_aoe 2, aoe_considers_character_size true, aoe_excludes_self true`
- **Damage/Effects:** `damage 1, ai_base_score 9999, custom_additional_ai_weight tile_close_to_enemy_soft, Burn 2, tag rock, ChangeTilesUnder LavaTile, VaporizeInanimate 1`

### PyrophinaSoloRoar (`PyrophinaSoloRoar`)

- **Template:** `spell`
- **Cost:** `cantrip true, cantrip_group kaiju_roar`
- **Target/Shape:** `prioritize_face_camera true, target_mode none, aoe_mode all`
- **Damage/Effects:** `type status_spell, ai_base_score 9999, cant_miss true, knockback 10`

### PyrophinaVSCatThrow (`PyrophinaVSCatThrow`)

- **Template:** `throw_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 20, restrictions must_have_buddy`
- **Damage/Effects:** `damage 5+bonus_melee_damage, ai_base_score 9999, custom_additional_ai_weight target_closest`

### Volcano Stomp (`PyrophinaVSEarthquakeStomp`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode map_edges`
- **Damage/Effects:** `damage 5, ai_base_score 9999, Burn 2`

### Fire Breath (`PyrophinaVSFlamethrower`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode narrow_cone, aoe_leading_edge_only true, min_aoe 1, max_aoe 10, aoe_considers_character_size true, aoe_excludes_self true`
- **Damage/Effects:** `damage 5, Burn 2, tag rock, ChangeTilesUnder LavaTile, VaporizeInanimate 1`

### PyrophinaVSRoar (`PyrophinaVSRoar`)

- **Template:** `spell`
- **Cost:** `cantrip true, cantrip_group kaiju_roar`
- **Target/Shape:** `prioritize_face_camera true, target_mode none, aoe_mode all`
- **Damage/Effects:** `type status_spell, ai_base_score 9999, cant_miss true, Fear [1 .3]`

### PyrophinaVSRun (`PyrophinaVSRun`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `max_range 8`
- **Damage/Effects:** `None`

### Spin Throw (`PyrophinaVSSpinThrow`)

- **Template:** `throw_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 10, min_range 3, max_aoe 2, aoe_mode circle, aoe_excludes_self true, aoe_considers_character_size true, range_considers_character_size false, restrictions must_fit_2x2, range_mode cross, toss_direction_restriction forwards, spin_steps -16, knockback_mode character_to_tile`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 2, makes_contact false, type melee, custom_additional_ai_weight target_farthest, CollideWithThrowTarget 0`

### Firestorm (`PyrophinaVSWeatherRoar`)

- **Template:** `self_buff`
- **Cost:** `cantrip true, cantrip_group kaiju_roar`
- **Target/Shape:** `prioritize_face_camera true`
- **Damage/Effects:** `ai_base_score 9999, EnableWeather KaijuFirestorm`

---

## Pyrophina (Friendly)

### PyrophinaSoloAttack (`PyrophinaSoloAttack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `knockback 3`

### Fire Breath (`PyrophinaSoloFlamethrower`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode narrow_cone, aoe_leading_edge_only true, min_aoe 1, max_aoe 2, aoe_considers_character_size true, aoe_excludes_self true`
- **Damage/Effects:** `damage 1, ai_base_score 9999, custom_additional_ai_weight tile_close_to_enemy_soft, Burn 2, tag rock, ChangeTilesUnder LavaTile, VaporizeInanimate 1`

---

## Queen Hippo

### QueenHippoAttack (`QueenHippoAttack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 4+bonus_melee_damage, knockback 3, type melee, Bruise 1, OverrideChainKnockback 3`

### QueenHippoHeartAttack (`QueenHippoHeartAttack`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 999999, DieViaAbilityInternally 1`

### QueenHippoTire (`QueenHippoTire`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `prioritize_face_camera true`
- **Damage/Effects:** `ai_base_score 999999, status Brace, stacks 1`

### QueenHippoUppercut (`QueenHippoUppercut`)

- **Template:** `melee_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 4+bonus_melee_damage, distance 2`

---

## Radical Rat

### Turtle (`BombRatTurtle`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `BombRatTurtle 1`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Bomb Toss (`RockToss_BomberRat`)

- **Template:** `lobbed_attack`
- **Cost:** `mana 5, cantrip true`
- **Target/Shape:** `max_range 5`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, Stun [1, .10], BounceObject Bomb`

### Spawn Bomb (`SpawnBomb`)

- **Template:** `spawn`
- **Cost:** `mana 5`
- **Target/Shape:** `max_range 5`
- **Damage/Effects:** `None`

---

## Rat King

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Healing Word (`RangedHeal_Enemy`)

- **Template:** `spell`
- **Cost:** `mana 5`
- **Target/Shape:** `max_aoe 0, min_range 0, max_range 3`
- **Damage/Effects:** `heal 5, type spell, elements [, Holy, ]`

---

## Rat Pile

### Heal (`HealSelf`)

- **Template:** `self_buff`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 5`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Spawn Rat (`SpawnRat`)

- **Template:** `spawn`
- **Cost:** `mana 5`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

---

## Robo-Draven

### DCBirthSquirrel (`DCBirthSquirrel`)

- **Template:** `*(None)*`
- **Cost:** `infcantrip false, cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Form of the Squirrel (`DCSquirrelForm`)

- **Template:** `self_buff`
- **Cost:** `cantrip true, cant_cast X`
- **Target/Shape:** `X_is custom`
- **Damage/Effects:** `FormChange SquirrelForm, mouth 1071, tail 1042, ear1 1036, ear2 1036`

### DCT_SummonCrow (`DCT_SummonCrow`)

- **Template:** `spawn`
- **Cost:** `cantrip true, cant_cast X, once_per_fight true`
- **Target/Shape:** `X_is custom`
- **Damage/Effects:** `None`

### Sing (`DruidCatBasic`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 2, max_range 5+bonus_range, aoe_excludes_self true`
- **Damage/Effects:** `heal 3, cant_miss true, DamageUp 1`

---

## Robo-Fenrir

### BasicRanged_Hunter (`BasicRanged_Hunter`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### BearTrap_Enemy_Cantrip (`BearTrap_Enemy_Cantrip`)

- **Template:** `*(None)*`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### HunterMinibossMove (`HunterMinibossMove`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `bonus_pathing_leniency 4`
- **Damage/Effects:** `None`

### Shove (`Shove`)

- **Template:** `melee_attack`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, knockback 2`

---

## Robo-Maisie

### Push Attack (`BasicTankMelee`)

- **Template:** `dash_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1+bonus_range, max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1`

### SwapPositions_TankCat (`SwapPositions_TankCat`)

- **Template:** `swap`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `None`

### T3LickyLicky (`T3LickyLicky`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 5, DamageUp 2, Cleanse 0`

---

## Robo-Pebbles

### Push (`ColorlessCat_Push`)

- **Template:** `dash_attack`
- **Cost:** `mana 0, act_points 1`
- **Target/Shape:** `target_mode direction8, max_range 1, max_aoe 1, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 4+bonus_melee_damage, knockback 10`

### Rock Toss (`RockToss_ColorlessCat`)

- **Template:** `lobbed_attack`
- **Cost:** `mana 0, act_points 1`
- **Target/Shape:** `min_range 3, max_range 5`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, BounceObject SmallRock`

### RockToss_ColorlessCat_AsCloseAsPossible (`RockToss_ColorlessCat_AsCloseAsPossible`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `custom_additional_ai_weight tile_close_to_enemy`

### Boulder Drop! (`T3Pebbles_BoulderDrop`)

- **Template:** `spawn`
- **Cost:** `prime 1`
- **Target/Shape:** `target_mode tile, min_range 1, max_range 6, max_aoe 2, range_excludes_blocking false, aoe_restrictions none, knockback_mode zero`
- **Damage/Effects:** `damage 999, cant_miss true, type ranged`

### Boulder Drop! (`T3Pebbles_PrimeBoulderDrop`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ability T3Pebbles_BoulderDrop, respect_prime true`

---

## Rocky Bobo

### Rock Song (`RockSong`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, aoe_mode all, prioritize_dont_change_direction true, aoe_excludes_self true`
- **Damage/Effects:** `type none, damage 0, tag rock, FloatingRockTrap 1`

### RockySlam (`RockySlam`)

- **Template:** `jump_attack`
- **Cost:** `act_points 1`
- **Target/Shape:** `max_range 2, min_range 2, range_mode cross, range_considers_character_size false, min_aoe 0, max_aoe 1, prioritize_dont_change_direction true`
- **Damage/Effects:** `type melee, damage 5+bonus_melee_damage, knockback 1, ai_base_score 9999, IgnoreSelf 1`

---

## Shadow Cat

### Shadow Dagger (`ShadowDagger`)

- **Template:** `straightshot_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `aoe_mode custom, custom_aoe [[1, 0]], max_aoe 3`
- **Damage/Effects:** `damage 4+bonus_ranged_damage, ShadowCrit 1, tile ShadowTile`

### ShadowstepDodge (`ShadowstepDodge`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

---

## Smough

### HammerSmash (`HammerSmash`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_aoe 2`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 10, OverrideKnockbackDamage 5`

---

## Spinnerette

### Melee Attack (`BasicBigMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range`
- **Damage/Effects:** `None`

### Butt Web (`ButtWeb`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [[-1 0]], knockback_mode none, aoe_considers_character_size true, aoe_excludes_self true, restrictions none, aoe_restrictions none`
- **Damage/Effects:** `damage 0, SpawnNeutralWebTrapOnMiss 1, Webbed 1`

### Butt Web (`ButtWeb_AlreadyEnraged`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [[-1 0]], knockback_mode none, aoe_considers_character_size true, aoe_excludes_self true, restrictions none, aoe_restrictions none`
- **Damage/Effects:** `damage 0, SpawnNeutralWebTrapOnMiss 1, Webbed 1`

### ExtraMove (`ExtraMove`)

- **Template:** `*(None)*`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Leave (`Leave`)

- **Template:** `leave`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 100`

### Spawn Spiderlings (`QueenMinis`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 3, max_aoe 1, max_targets 2, multihit 2, stagger_multihit_targets true, restrictions aoe_must_exist, aoe_restrictions [must_be_partially_empty]`
- **Damage/Effects:** `damage 0, ai_base_score 10, custom_additional_ai_weight tile_close_to_enemy, BounceObject TinySpider`

### Web (`QueenWeb`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 5, max_aoe 1, max_targets 4, multihit 2, stagger_multihit_targets true, restrictions [must_have_animate_character must_have_living_character]`
- **Damage/Effects:** `damage 0, ai_base_score 10, custom_additional_ai_weight tile_close_to_enemy, SpawnNeutralWebTrapOnMiss 1, Webbed 1`

### Return (`SpiderReturn`)

- **Template:** `return`
- **Cost:** `cantrip true`
- **Target/Shape:** `max_range 20, restrictions must_be_movable_ignore_trample`
- **Damage/Effects:** `ai_base_score 100`

### Spider Spawn (`SpiderSpawn`)

- **Template:** `spawn`
- **Cost:** `allow_offmap_casts true, must_be_offmap true`
- **Target/Shape:** `max_range 20, min_range 0, knockback_mode none`
- **Damage/Effects:** `None`

### Calm Down! (`Spider_CalmDown`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "Default_Ground"`

### Go Insane! (`Spider_GoInsane`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "Insane_Ground"`

---

## The Child

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Pulse (`TheChild_Pulse`)

- **Template:** `spell`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode none, aoe_mode circle, min_aoe 0, max_aoe 20, aoe_excludes_self true, aoe_considers_character_size true, distance_sort_targets true, aoe_restrictions must_have_animate_character`
- **Damage/Effects:** `damage 0, knockback 10`

### Purity (`TheChild_ReleaseBeams`)

- **Template:** `spell`
- **Cost:** `cantrip true`
- **Target/Shape:** `max_aoe 1, max_range 20, min_range 0, multihit 10`
- **Damage/Effects:** `damage 10, IgnoreSelf 1`

### TheChild_TargetBeam (`TheChild_TargetBeam`)

- **Template:** `targeted_status`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 0, max_range 20, min_range 0`
- **Damage/Effects:** `layer tiles, FinalBossQueueBeam 1`

### TheChild_TransformBoris (`TheChild_TransformBoris`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Cleanse 0, FormChange Boris`

### TheChild_TransformExplosive (`TheChild_TransformExplosive`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Cleanse 0, FormChange Explosive`

### TheChild_TransformHoly (`TheChild_TransformHoly`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Cleanse 0, FormChange Holy`

### Wrath (`TheChild_Wrath`)

- **Template:** `spell`
- **Cost:** `cantrip true`
- **Target/Shape:** `aoe_mode all, target_mode none, aoe_excludes_self true, aoe_restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 12, elements [, Holy, ]`

---

## The Coven

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Famine (`CovenFamine`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode square, aoe_considers_character_size true, aoe_excludes_self true, min_aoe 0, max_aoe 20`
- **Damage/Effects:** `damage 0, ai_base_score 999999, Imprison Fly`

### Pestilence (`CovenPestilence`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode square, max_aoe 20, max_targets 4`
- **Damage/Effects:** `None`

### CovenRise1 (`CovenRise1`)

- **Template:** `lobbed_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode none, max_targets 1, aoe_mode all, restrictions none, aoe_restrictions [must_have_tag], target_requires_tag unlit_candle`
- **Damage/Effects:** `damage 0, ai_base_score 999999, elements [, Fire, ]`

### CovenRise2 (`CovenRise2`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### CovenRise3 (`CovenRise3`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### CovenRise4 (`CovenRise4`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Death (`CovenSummon`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `PopAndSpawn Tormentor`

### War (`CovenWar`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode square, aoe_considers_character_size true, aoe_excludes_self true, min_aoe 0, max_aoe 20, max_targets 20`
- **Damage/Effects:** `ai_base_score 999999, damage 5+bonus_ranged_damage, Burn 2, ChangeTile LavaTile`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## The Creator

### BecomeTheDestroyer (`BecomeTheDestroyer`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ClearFinalBossBattlefield 1, PlayBackground 0, PopAndSpawn TheDestroyer, new_song same, new_layer map`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### TheCreator_Reaction (`TheCreator_Reaction`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, min_aoe 0, max_aoe 20, aoe_excludes_self true, aoe_considers_character_size true`
- **Damage/Effects:** `damage 0, knockback 10`

### TheCreator_SpawnCloneTeam (`TheCreator_SpawnCloneTeam`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, min_range 1, max_range 1, max_aoe 0, aoe_mode all, restructions aoe_must_exist, aoe_restrictions must_have_special_tag, special_tile_tag FinalBossCloneSpot, shuffle_tile_order true`
- **Damage/Effects:** `None`

---

## The Destroyer

### Destroyer2HolyAttack (`Destroyer2HolyAttack`)

- **Template:** `spell`
- **Cost:** `cantrip true, prime 1`
- **Target/Shape:** `target_mode none, aoe_considers_character_size true, aoe_excludes_self true, min_aoe 1, max_aoe 4, prioritize_face_camera true`
- **Damage/Effects:** `damage 16, ai_base_score 9999`

### Destroyer2Pulse (`Destroyer2Pulse`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_considers_character_size true, aoe_excludes_self true, min_aoe 1, max_aoe 4`
- **Damage/Effects:** `damage 0, knockback 1`

### DestroyerAttack (`DestroyerAttack`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### DestroyerBreakShield (`DestroyerBreakShield`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `CancelPrimedAbilities 1, SignalFinalBossShieldBroke 1, FormChange DualSword, FaceCamera 1, new_song same, new_layer battle`

### Precognition (`DestroyerChargeBackflips`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `prioritize_dont_change_direction true`
- **Damage/Effects:** `stacks 4, ability DestroyerDodge`

### Annihilation (`DestroyerDashAttack`)

- **Template:** `dash_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 10, consider_trample false, multihit 4, aoe_mode square, knockback_mode character_to_tile, max_aoe 1`
- **Damage/Effects:** `damage 2+bonus_melee_damage`

### DestroyerDodge (`DestroyerDodge`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `range_mode cross, max_range 2, min_range 2, restrictions [must_be_moveable must_move], straight_shot true, allow_any_orientation true, range_considers_character_size false`
- **Damage/Effects:** `None`

### Holy Blast (`DestroyerHolyAttack`)

- **Template:** `spell`
- **Cost:** `cantrip true, prime 1`
- **Target/Shape:** `target_mode none, aoe_considers_character_size true, aoe_excludes_self true, min_aoe 1, max_aoe 4, prioritize_face_camera true`
- **Damage/Effects:** `damage 16, ai_base_score 9999`

### DestroyerPulse (`DestroyerPulse`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_considers_character_size true, aoe_excludes_self true, min_aoe 1, max_aoe 4`
- **Damage/Effects:** `damage 0, knockback 1`

### Rise (`DestroyerRaise`)

- **Template:** `spell`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_restrictions [must_have_player_cat must_have_corpse], restrictions aoe_must_exist, prioritize_face_camera true`
- **Damage/Effects:** `Revive 50%, FlatAIBonus 999999`

### DestroyerThrowShield (`DestroyerThrowShield`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 20`
- **Damage/Effects:** `damage 99, tag the_nuke_bearer, OverrideDamage 1`

---

## The Father

### MegaGuppy_SlamLeft (`MegaGuppy_SlamLeft`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode right_orientation`
- **Damage/Effects:** `None`

### Slam (`MegaGuppy_SlamRight`)

- **Template:** `spell`
- **Cost:** `cantrip true, allow_offmap_casts true`
- **Target/Shape:** `target_mode none, aoe_mode all, knockback_mode orientation, aoe_restrictions must_have_animate_character, /*visual_delay_but_simultaneous_damage 50, delay_from_map_edge true, delay 5*/`
- **Damage/Effects:** `damage 0, knockback 10, OverrideKnockbackDamage 3, FastKnockback 4, tag god, IgnoreDamage 1`

### MegaGuppy_SummonTheChild (`MegaGuppy_SummonTheChild`)

- **Template:** `spawn`
- **Cost:** `mana 0, allow_offmap_casts true`
- **Target/Shape:** `target_mode tile, range_mode special_tagged_tiles, special_tile_tag FinalBossTheChildLocation, knockback_mode orientation, restrictions none, range_excludes_blocking false, aoe_restrictions none`
- **Damage/Effects:** `damage 0, ai_base_score 999999`

### MegaGuppy_TransformBoris (`MegaGuppy_TransformBoris`)

- **Template:** `self_buff`
- **Cost:** `cantrip true, allow_offmap_casts true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### MegaGuppy_TransformExplosive (`MegaGuppy_TransformExplosive`)

- **Template:** `self_buff`
- **Cost:** `cantrip true, allow_offmap_casts true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### MegaGuppy_TransformHoly (`MegaGuppy_TransformHoly`)

- **Template:** `self_buff`
- **Cost:** `cantrip true, allow_offmap_casts true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## The Mother

### MotherConsume (`MotherConsume`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TriggerMotherConsume 1`

### MotherTumorGrow (`MotherTumorGrow`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 4, InstantMaxHealthUp 4, form Small, FormChange Big`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### SpawnMotherSpike (`SpawnMotherSpike`)

- **Template:** `spawn`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 20, range_excludes_blocking false, aoe_restrictions none, knockback_mode tile_to_character`
- **Damage/Effects:** `damage 3, stacks 3, distance 2`

### TheMother_Birth (`TheMother_Birth`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, aoe_mode all, restrictions aoe_must_exist, aoe_restrictions [must_have_tag], target_requires_tag themotherspike`
- **Damage/Effects:** `type none, damage 0, cant_miss true, tag themotherspike, object BoyShade, no_splatter false`

---

## Throbbing King

### Melee Attack (`BasicBigMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range`
- **Damage/Effects:** `None`

### Meat Minion (`SimonFlopper_SpawnMinion`)

- **Template:** `spawn`
- **Cost:** `mana 0, charge 0`
- **Target/Shape:** `min_range 1, max_range 2`
- **Damage/Effects:** `None`

### Meat Tentacle (`SimonFlopper_Tentacle`)

- **Template:** `spell`
- **Cost:** `mana 5, cantrip true`
- **Target/Shape:** `min_range 0, max_range 8, max_aoe 0`
- **Damage/Effects:** `damage 0, custom_additional_ai_weight avoid_redundant_debuffs, Bound 3`

### Wiggle (`SimonFlopper_WiggleChance`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `chance 30%, form "Normal"`

### Wiggle (`SimonFlopper_WiggleFake`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 9999`

### Wiggle (`SimonFlopper_WiggleGuaranteed`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "Normal"`

### Kneel. (`SimonSays_ComeHere`)

- **Template:** `spell`
- **Cost:** `prime 1`
- **Target/Shape:** `target_mode none, aoe_mode square, aoe_considers_character_size true, aoe_excludes_self true, min_aoe 1+size, max_aoe 20`
- **Damage/Effects:** `damage 15, ai_base_score 9999`

### Hide. (`SimonSays_GoAway`)

- **Template:** `spell`
- **Cost:** `prime 1`
- **Target/Shape:** `target_mode none, aoe_mode all_except_edges, aoe_considers_character_size false, aoe_excludes_self true`
- **Damage/Effects:** `damage 15, ai_base_score 9999`

### Scatter. (`SimonSays_Scatter`)

- **Template:** `spell`
- **Cost:** `prime 1`
- **Target/Shape:** `target_mode none, aoe_mode all_except_random_empty, aoe_considers_character_size false, aoe_excludes_self true, min_aoe 6, max_aoe 10`
- **Damage/Effects:** `damage 15, ai_base_score 9999`

### Simon_Shot (`Simon_Shot`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 5`
- **Damage/Effects:** `damage 4+bonus_ranged_damage`

### Meat Tentacle (`Simon_Tentacle`)

- **Template:** `spell`
- **Cost:** `mana 5, cantrip true`
- **Target/Shape:** `min_range 0, max_range 8, max_aoe 0`
- **Damage/Effects:** `damage 0, custom_additional_ai_weight favor_enemy_already_moved, Bound 3`

### Litter (`Simon_Trash`)

- **Template:** `spawn`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, aoe_mode square, max_aoe 20, max_targets 10`
- **Damage/Effects:** `None`

### TKNG_DeathExplode (`TKNG_DeathExplode`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode circle, min_aoe 0, max_aoe 20, aoe_excludes_self true, aoe_considers_character_size true`
- **Damage/Effects:** `damage 0, knockback 10, ai_base_score 999999`

### Go Away. (`TKNG_GoAway`)

- **Template:** `spell`
- **Cost:** `prime 1`
- **Target/Shape:** `target_mode none, aoe_mode all_except_edges, aoe_considers_character_size false, aoe_excludes_self true, knockback_mode none, prioritize_face_camera true`
- **Damage/Effects:** `damage 16, ai_base_score 9999`

### TKNG_GutBall (`TKNG_GutBall`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 5`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, Slow 2, stacks 1, alt_art TangledMeat`

### TKNG_Hop (`TKNG_Hop`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Kneel. (`TKNG_Kneel`)

- **Template:** `spell`
- **Cost:** `prime 1`
- **Target/Shape:** `target_mode none, aoe_mode square, aoe_considers_character_size true, aoe_excludes_self true, min_aoe 1+size, max_aoe 20, knockback_mode none, prioritize_face_camera true`
- **Damage/Effects:** `damage 16, ai_base_score 9999`

### TKNG_Laser (`TKNG_Laser`)

- **Template:** `laser`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, Bleed 2`

### Roulette. (`TKNG_Roulette`)

- **Template:** `spell`
- **Cost:** `prime 1`
- **Target/Shape:** `target_mode none, aoe_mode all_except_random_empty, aoe_considers_character_size false, aoe_excludes_self true, min_aoe 6, max_aoe 10, knockback_mode none, prioritize_face_camera true`
- **Damage/Effects:** `damage 16, ai_base_score 9999`

### TKNG_Spawn (`TKNG_Spawn`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [[-1, 0]]`
- **Damage/Effects:** `None`

### Spread Out. (`TKNG_Spread`)

- **Template:** `spell`
- **Cost:** `prime 1`
- **Target/Shape:** `target_mode none, aoe_mode area_around_all_player_cats, aoe_considers_character_size false, aoe_excludes_self true, min_aoe 1, max_aoe 2, knockback_mode none, prioritize_face_camera true`
- **Damage/Effects:** `damage 16, ai_base_score 9999`

### Vomit Rain (`TKNG_Trash`)

- **Template:** `spawn`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, aoe_mode square, max_aoe 20, max_targets 14, multihit 14, stagger_multihit_targets true`
- **Damage/Effects:** `None`

---

## Throne

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Tormentor

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Lucifer (`TormentorBite`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1+bonus_melee_damage, type melee, RandomInjury 1`

### Imbue (`TormentorRuneAbsorb`)

- **Template:** `spell`
- **Cost:** `prime 1`
- **Target/Shape:** `target_mode none, prioritize_face_camera true, prioritize_dont_change_direction true, aoe_mode all`
- **Damage/Effects:** `damage 0, type status_spell, ai_base_score 999999, cant_miss true, StealDemonicGlyph 1`

### Pentagram (`TormentorSpawn`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `min_range 0, max_range 2`
- **Damage/Effects:** `None`

### Feast (`TormentorSuck`)

- **Template:** `spell`
- **Cost:** `prime 1`
- **Target/Shape:** `target_mode direction, aoe_considers_character_size true, aoe_excludes_self true, aoe_mode cone, min_aoe -1, max_aoe 10`
- **Damage/Effects:** `damage 0, type status_spell, custom_additional_ai_weight tile_exists, ai_base_score 999999, tag kaiju`

---

## Trampy

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### TrampyDrink (`TrampyDrink`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `multihit 2`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, ChangeTile GlassTile`

### Dump (`TrampyDump`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode line, min_aoe 1, max_aoe 1, knockback_mode orientation, restrictions [aoe_must_be_displaceable aoe_must_exist]`
- **Damage/Effects:** `damage 0, cant_miss true, Displace 1, Poison 2, object Poop`

### TrampyFleas (`TrampyFleas`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, max_aoe 1, max_targets 2, multihit 2, stagger_multihit_targets true`
- **Damage/Effects:** `None`

### TrampySleep (`TrampySleep`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 15, Sleep 3`

### Loogie (`TrampySpit`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 2, max_range 3`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, Blind 2, Slow 2`

---

## Ultra Ornstein

### Gasp (`Magnetize`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [, [1, 1], [2, 1], [3, 1], [4, 1], [5, 1], [6, 1], [7, 1], [8, 1], [9, 1], [10, 1], [1, 0], [2, 0], [3, 0], [4, 0], [5, 0], [6, 0], [7, 0], [8, 0], [9, 0], [10, 0], [1,-1], [2,-1], [3,-1], [4,-1], [5,-1], [6,-1], [7,-1], [8,-1], [9,-1], [10,-1], ], knockback_mode perp_towards_facing_middle_pull`
- **Damage/Effects:** `damage 0, knockback 1, custom_additional_ai_weight magnetize_favorlineup, elements [, Wind, ]`

### SpearPoke (`SpearPoke`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_aoe 4`
- **Damage/Effects:** `damage 5+bonus_melee_damage`

### Teleport (`Teleport`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### X Lightning (`XLightning`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode direction, aoe_mode cross, max_aoe 10, aoe_excludes_self true`
- **Damage/Effects:** `damage 2, Stun [1, .25]`

---

## Ultra Smough

### Fat Leap (`FatLeap`)

- **Template:** `jump_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 4`
- **Damage/Effects:** `damage 3+bonus_melee_damage, knockback 1`

### HammerSmash (`HammerSmash`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_aoe 2`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 10, OverrideKnockbackDamage 5`

### Tantrum (`SpawnJunk`)

- **Template:** `spawn`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, aoe_mode square, max_aoe 20, max_targets 15`
- **Damage/Effects:** `None`

---

## Wall of Cats

### Blow (`WallBlow`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode direction, aoe_mode line, min_aoe 1, max_aoe 10, aoe_considers_character_size true, aoe_excludes_self true, knockback_mode orientation`
- **Damage/Effects:** `damage 2, knockback 5, elements [, Wind, ]`

### Glare (`WallEyeShot`)

- **Template:** `straightshot_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `aoe_mode custom, custom_aoe [[1, 0]]`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, Weakness 1`

### WallMove (`WallMove`)

- **Template:** `teleport`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode tile, range_mode custom, custom_range [[0 -9][0 -8][0 -7][0 -6][0 -5][0 -4][0 -3][0 -2][0 -1][0 0][0 1][0 2][0 3][0 4][0 5][0 6][0 7][0 8][0 9]], restrictions must_be_moveable_ignore_wall`
- **Damage/Effects:** `None`

---

## Wizard

### Short Shot (`BasicShortRanged`)

- **Template:** `ranged_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 3+bonus_range`
- **Damage/Effects:** `None`

### Wiz Blizz (`WizBlizzard`)

- **Template:** `spell`
- **Cost:** `mana 5, prime 1, cantrip true`
- **Target/Shape:** `target_mode direction, aoe_mode square, min_aoe 1, max_aoe 1`
- **Damage/Effects:** `damage 3, knockback 1, Freeze 1`

### Flamethrower (`WizFlamethrower`)

- **Template:** `spell`
- **Cost:** `mana 5, prime 1, cantrip true`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [, [3, 2], [2, 1] [3, 1], [1, 0] [2, 0] [3, 0], [2,-1] [3,-1], [3,-2], ]`
- **Damage/Effects:** `damage 3, Burn 3`

### Spell Shield (`WizSpellShield`)

- **Template:** `self_buff`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `SpellShield 1`

### xXx_Thunder_xXx (`WizStorm`)

- **Template:** `spell`
- **Cost:** `mana 5, prime 1, cantrip true`
- **Target/Shape:** `max_range 5, aoe_mode custom, aoe_symmetry four_way, custom_aoe [[0, 0] [1, 1] [2, 2]]`
- **Damage/Effects:** `damage 3, Stun [1, .25]`

---

## Zaratana

### ZaratanaBasic (`ZaratanaBasic`)

- **Template:** `dash_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 2, consider_trample true`
- **Damage/Effects:** `damage 10+bonus_melee_damage, knockback 2`

### ZaratanaSoloBasic (`ZaratanaSoloBasic`)

- **Template:** `dash_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 2, consider_trample true`
- **Damage/Effects:** `damage 4+bonus_melee_damage, knockback 2, Bruise 1`

### Meteor Bombardment (`ZaratanaSoloBombardment`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 2, max_range 20, min_aoe 0, max_aoe 3, aoe_mode circle, aoe_excludes_self true, max_targets 5, multihit 5, stagger_multihit_targets true, shuffle_tile_order true, knockback_mode 0`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, custom_additional_ai_weight tile_exists, Displace 1, BounceRock SmallRock`

### Magnet Pull (`ZaratanaSoloMagnet`)

- **Template:** `spell`
- **Cost:** `cant_cast 2-X`
- **Target/Shape:** `target_mode none, aoe_mode all, distance_sort_targets 1, X_is custom, prioritize_face_camera true, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, ai_base_score 9999, tag rock, DisplaceTowardsSource 1, FloatingRockTrap 1`

### ZaratanaSoloRoar (`ZaratanaSoloRoar`)

- **Template:** `spell`
- **Cost:** `cantrip true, cantrip_group kaiju_roar`
- **Target/Shape:** `prioritize_face_camera true, target_mode none, aoe_mode all, aoe_excludes_self true`
- **Damage/Effects:** `type status_spell, ai_base_score 9999, cant_miss true, tag rock, FloatingRockTrap 1`

### Spin Dash (`ZaratanaSoloSpinDash`)

- **Template:** `dash_attack`
- **Cost:** `mana 0, prime 1`
- **Target/Shape:** `target_mode direction8, max_range 20, max_bounces -1, splash_damage_aoe_begin 999, restrictions diagonal_only`
- **Damage/Effects:** `damage 3+bonus_melee_ability_damage, ai_base_score 9999, SetDistanceDisplace 5, Bruise 1`

### Turtle (`ZaratanaSoloTurtle`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 9999, Cleanse 0, form "Turtled"`

### Meteornado (`ZaratanaSoloWeatherRoar`)

- **Template:** `self_buff`
- **Cost:** `cantrip true, cantrip_group kaiju_roar`
- **Target/Shape:** `prioritize_face_camera true`
- **Damage/Effects:** `ai_base_score 9999, EnableWeather KaijuMeteornadoSolo`

### Meteor Bombardment (`ZaratanaVSBombardment`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 2, max_range 20, min_aoe 0, max_aoe 3, aoe_mode circle, aoe_excludes_self true, max_targets 8, multihit 8, stagger_multihit_targets true, shuffle_tile_order true, restrictions must_have_buddy`
- **Damage/Effects:** `damage 10+bonus_ranged_damage, HitExplosion 5`

### ZaratanaVSExitTurtle (`ZaratanaVSExitTurtle`)

- **Template:** `melee_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode none, aoe_mode cross, knockback_mode character_to_tile`
- **Damage/Effects:** `ai_base_score 9999, damage 5+bonus_melee_damage, knockback 2`

### Magnet Pull (`ZaratanaVSMagnet`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode all, distance_sort_targets 1, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, ai_base_score 9999, DisplaceTowardsSource 1`

### ZaratanaVSRevenge (`ZaratanaVSRevenge`)

- **Template:** `straightshot_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode custom, custom_aoe      [[0, 1] [0, 1]   [0, -1] [0, -1]], custom_aoe_util [[0, 1] [1, 1]   [0,  0] [1,  0]]`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, BounceObject SmallRock`

### ZaratanaVSRoar (`ZaratanaVSRoar`)

- **Template:** `spell`
- **Cost:** `cantrip true, cantrip_group kaiju_roar`
- **Target/Shape:** `prioritize_face_camera true, target_mode none, aoe_mode all, aoe_excludes_self true`
- **Damage/Effects:** `type status_spell, ai_base_score 9999, cant_miss true, Fear [1 .3]`

### Spin Dash (`ZaratanaVSSpinDash`)

- **Template:** `dash_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode direction8, max_range 20, max_bounces -1, splash_damage_aoe_begin 999, restrictions diagonal_only`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, SetDistanceDisplace 5`

### Turtle (`ZaratanaVSTurtle`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 9999, Cleanse 0, form "Turtled"`

### Turtle (`ZaratanaVSTurtleGuaranteed`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 9999, Cleanse 0, form "Turtled"`

### Meteornado (`ZaratanaVSWeatherRoar`)

- **Template:** `self_buff`
- **Cost:** `cantrip true, cantrip_group kaiju_roar`
- **Target/Shape:** `prioritize_face_camera true`
- **Damage/Effects:** `ai_base_score 9999, EnableWeather KaijuMeteornado`

---

## Zaratana (Friendly)

### ZaratanaSoloBasic (`ZaratanaSoloBasic`)

- **Template:** `dash_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 2, consider_trample true`
- **Damage/Effects:** `damage 4+bonus_melee_damage, knockback 2, Bruise 1`

### Meteor Bombardment (`ZaratanaSoloBombardment`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 2, max_range 20, min_aoe 0, max_aoe 3, aoe_mode circle, aoe_excludes_self true, max_targets 5, multihit 5, stagger_multihit_targets true, shuffle_tile_order true, knockback_mode 0`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, custom_additional_ai_weight tile_exists, Displace 1, BounceRock SmallRock`

### ZaratanaVSRevenge (`ZaratanaVSRevenge`)

- **Template:** `straightshot_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode custom, custom_aoe      [[0, 1] [0, 1]   [0, -1] [0, -1]], custom_aoe_util [[0, 1] [1, 1]   [0,  0] [1,  0]]`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, BounceObject SmallRock`

---

# Mini-bosses

## Abandoned One

### AZ_BreakArm (`AZ_BreakArm`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode zero, restrictions must_have_character`
- **Damage/Effects:** `damage 15+bonus_melee_damage, SpecificInjury str`

### AZ_BreakLeg (`AZ_BreakLeg`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode zero, restrictions must_have_character`
- **Damage/Effects:** `damage 15+bonus_melee_damage, SpecificInjury spd`

### AZ_BreakNeck (`AZ_BreakNeck`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode zero, restrictions must_have_character`
- **Damage/Effects:** `damage 15+bonus_melee_damage, SpecificInjury int`

### AZ_Jump (`AZ_Jump`)

- **Template:** `jump_attack`
- **Cost:** `act_points 1`
- **Target/Shape:** `min_range 0, max_range 2, min_aoe 0, max_aoe 0`
- **Damage/Effects:** `damage 0`

### AZ_LoseHead (`AZ_LoseHead`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `target_mode random_tile, min_range 2, max_range 4`
- **Damage/Effects:** `None`

### Scream (`AZ_Scream`)

- **Template:** `spell`
- **Cost:** `mana 0, requires_exact_character_aux 0`
- **Target/Shape:** `target_mode none, max_aoe 3, prioritize_dont_change_direction true, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, type status_spell, Fear 1`

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Alice

### Psychic Pull (`BasicPsychicPull`)

- **Template:** `spell`
- **Cost:** `move_points 0, act_points 1`
- **Target/Shape:** `max_aoe 0, max_range 20, knockback_mode target_to_character`
- **Damage/Effects:** `damage 2+bonus_basic_spell_damage, knockback 1, elements [, Gravity, ]`

### Predict (`PsychicCatBackflip`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `stacks 1, ability Teleport`

### PsychicChoke_Enemy (`PsychicChoke_Enemy`)

- **Template:** `*(None)*`
- **Cost:** `infcantrip false, cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Arthur

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Metronome_Enemy (`Metronome_Enemy`)

- **Template:** `*(None)*`
- **Cost:** `infcantrip false, cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 999999, stacks 1, banned_abilities [BatteryNuke WeAreOne Metronome SmartMetronome BecomeEntropy ForbiddenFamine]`

---

## Big Slime

### Melee Attack (`BasicBigMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range`
- **Damage/Effects:** `None`

---

## Can Creeper

### Slide (`CanCreeperSlide`)

- **Template:** `trample_dash`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 6`
- **Damage/Effects:** `damage 4+bonus_melee_damage, ai_base_score 9999`

### DoubleDiagonalCreepshot (`DoubleDiagonalCreepshot`)

- **Template:** `straightshot_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode custom, custom_aoe [[1, 1] [1,-1]]`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, SpawnCreep 1`

### MoveOne (`MoveOne`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

### ShortCreepshot (`ShortCreepshot`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 1`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, SpawnCreep 1`

### Swim (`Swim`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `max_range 10, range_mode square, restrictions [must_be_moveable must_have_liquid]`
- **Damage/Effects:** `None`

---

## Cerberubs

### CerberubsBarrage (`CerberubsBarrage`)

- **Template:** `lobbed_attack`
- **Cost:** `prime 1`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe -1, max_aoe 10, aoe_considers_character_size true, restrictions none, max_targets 10, multihit 5, stagger_multihit_targets true`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, Burn 2, ChangeTile LavaTile, HitExplosion 5`

### CerberubsCalm (`CerberubsCalm`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "Normal"`

### Cerberub Flub (`CerberubsJump`)

- **Template:** `jump_attack`
- **Cost:** `act_points 1`
- **Target/Shape:** `min_range 2, max_range 2`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1, IgnoreSelf 1`

### CerberubsShotgunReaction (`CerberubsShotgunReaction`)

- **Template:** `straightshot_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 3+bonus_range, shotgun_mode true, aoe_mode custom, custom_aoe      [[4, 3], [4, 2], [4, 1], [4, 0], [4, -1], [4, -2]], custom_aoe_util [[1, 1], [1, 1], [1, 1], [1, 0], [1,  0], [1,  0]]`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, Burn 2, ChangeTile LavaTile`

### CerberubsStraightReaction (`CerberubsStraightReaction`)

- **Template:** `straightshot_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 5+bonus_range, aoe_mode custom, custom_aoe      [[1, 0], [1, 0]], custom_aoe_util [[1, 1] [1,  0]]`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, Burn 2, ChangeTile LavaTile`

### Maul (`CerberubsThrow`)

- **Template:** `throw_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 10, min_range 1, restrictions none, range_mode cross, toss_direction_restriction forwards`
- **Damage/Effects:** `damage 10+bonus_melee_damage, custom_additional_ai_weight toss_farthest`

---

## Chan Hung

### MCHadouken (`MCHadouken`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 8`

### Kinetic Charge (`MCKineticCharge`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, KineticSpikes 1`

### MCMelee (`MCMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage "(5+bonus_melee_damage+1)/2", Bruise 1`

---

## Chupacabra

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### SharkDash (`SharkDash`)

- **Template:** `dash_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `max_range 2`
- **Damage/Effects:** `damage 5+bonus_melee_damage, Bleed 1`

### Wolf Leap (`WolfLeap`)

- **Template:** `jump_attack`
- **Cost:** `mana 5, charge 1`
- **Target/Shape:** `max_range 4`
- **Damage/Effects:** `damage 3+bonus_melee_damage`

---

## D'Claude

### BasicMelee_Fighter (`BasicMelee_Fighter`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Declaw (`Dclaude_Declaw`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1+bonus_melee_ability_damage, piercing true, Bleed 1, DamageUp -1`

### QueenHippoAttack (`QueenHippoAttack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 4+bonus_melee_damage, knockback 3, type melee, Bruise 1, OverrideChainKnockback 3`

---

## Dack

### THC_CoinRoll (`THC_CoinRoll`)

- **Template:** `move`
- **Cost:** `cantrip true, cantrip_group THC_CoinRoll`
- **Target/Shape:** `force_ai_target_as_spell true, range_mode 8cross, max_range 10, restrictions [must_be_moveable must_move], straight_shot true, allow_diagonals true`
- **Damage/Effects:** `type none, damage 0, custom_additional_ai_weight thiefcat_coinroll`

### THC_KnockCoinsRanged (`THC_KnockCoinsRanged`)

- **Template:** `straightshot_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 3+bonus_range`
- **Damage/Effects:** `ScatterHeldCoin 1, ScatterHeldCoin [1 .3]`

### THC_PoisonSwat (`THC_PoisonSwat`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable, multihit 2`
- **Damage/Effects:** `damage 1, Poison 1`

### THC_Roll (`THC_Roll`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `custom_additional_ai_weight thiefcat_roll`

---

## Death

### Move (`FloatMove`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `as_the_crow_flies true`
- **Damage/Effects:** `None`

### ReaperRevenge (`ReaperRevenge`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `None`

### Spin (`ReaperSpin`)

- **Template:** `melee_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode square, knockback_mode character_to_tile, multihit 3, max_aoe 1`
- **Damage/Effects:** `damage 4+bonus_melee_damage`

---

## Dr. Mangler

### ManglerCommand (`ManglerCommand`)

- **Template:** `targeted_status`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `damage 0, type status_spell, ManglerAttack 1`

### ManglerEnrage (`ManglerEnrage`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `UseAbility ManglerThrowRemote`

### ManglerFumbleEven (`ManglerFumbleEven`)

- **Template:** `multihit_self_buff`
- **Cost:** `Free`
- **Target/Shape:** `multihit 4`
- **Damage/Effects:** `ManglerShuffle false`

### ManglerFumbleOdd (`ManglerFumbleOdd`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `multihit 5`
- **Damage/Effects:** `None`

### ManglerSpin (`ManglerSpin`)

- **Template:** `melee_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `aoe_mode square, multihit 4, knockback_mode character_to_tile`
- **Damage/Effects:** `damage 2+bonus_melee_damage, type melee`

### ManglerThrowRemote (`ManglerThrowRemote`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 20`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, Stun 1`

---

## Draven

### DCBirthSquirrel (`DCBirthSquirrel`)

- **Template:** `*(None)*`
- **Cost:** `infcantrip false, cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Form of the Squirrel (`DCSquirrelForm`)

- **Template:** `self_buff`
- **Cost:** `cantrip true, cant_cast X`
- **Target/Shape:** `X_is custom`
- **Damage/Effects:** `FormChange SquirrelForm, mouth 1071, tail 1042, ear1 1036, ear2 1036`

### Sing (`DruidCatBasic`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 2, max_range 5+bonus_range, aoe_excludes_self true`
- **Damage/Effects:** `heal 3, cant_miss true, DamageUp 1`

---

## Draven's Crow

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### DCAeroblast (`DCAeroblast`)

- **Template:** `*(None)*`
- **Cost:** `infcantrip false, cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Fenrir

### BasicRanged_Hunter (`BasicRanged_Hunter`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Bear Trap (`BearTrap_Enemy`)

- **Template:** `lobbed_attack`
- **Cost:** `mana 2`
- **Target/Shape:** `min_range 1, max_range 5, restrictions must_be_empty`
- **Damage/Effects:** `damage 0, ai_base_score 10, custom_additional_ai_weight tile_has_no_known_traps, SpawnBearTrap 1`

### HunterMinibossMove (`HunterMinibossMove`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `bonus_pathing_leniency 4`
- **Damage/Effects:** `None`

### Shove (`Shove`)

- **Template:** `melee_attack`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, knockback 2`

---

## Flushmaster

### Flush (`Flush`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, aoe_excludes_self true, knockback_mode orientation, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 0, knockback 10, OverrideKnockbackDamage 3`

### Teleport (`Teleport`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Franklin

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### TCCatBot (`TCCatBot`)

- **Template:** `*(None)*`
- **Cost:** `infcantrip false, cantrip true, requires_destructible_weapon true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### TCMechSuit (`TCMechSuit`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 999999`

---

## Frod Rocksnow

### CaveCatEnrageOne (`CaveCatEnrageOne`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "TwoAlive"`

### CaveCatEnrageTwo (`CaveCatEnrageTwo`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "OneAlive"`

### CaveDad_ClubBasic (`CaveDad_ClubBasic`)

- **Template:** `melee_attack`
- **Cost:** `must_have_weapon true`
- **Target/Shape:** `aoe_mode custom, aoe_symmetry none, custom_aoe [[1, -1] [1, 0] [1, 1]]`
- **Damage/Effects:** `damage 5+bonus_melee_damage, incidentally_collects_pickups false, knockback 10, Stun [1 .5]`

### Rock Toss (`RockToss_CaveDad`)

- **Template:** `lobbed_attack`
- **Cost:** `mana 0, act_points 1`
- **Target/Shape:** `min_range 1, max_range 20`
- **Damage/Effects:** `damage 2+bonus_ranged_damage, BounceObject SmallRock`

---

## Frostbiter

### Blizzard (`IceElementalBlizzard`)

- **Template:** `spell`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_excludes_self true, knockback_mode character_to_tile, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 0, knockback 1, SpeedUp -1`

### Frost Breath (`IceElementalBreath`)

- **Template:** `spell`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 2, max_aoe 10, aoe_excludes_self true, knockback_mode character_to_tile, aoe_restrictions must_have_piercing_line_of_sight`
- **Damage/Effects:** `damage 5, knockback 1, Slow 1`

### IceElementalSpikes (`IceElementalSpikes`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode square, max_aoe 1, aoe_excludes_self true, knockback_mode character_to_tile, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 5, knockback 1, Freeze 1, ChangeTile IceShardsSmall`

---

## Gambit

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### 1 : Confusion (`D6Confused`)

- **Template:** `self_buff`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, min_aoe 0, max_aoe 0`
- **Damage/Effects:** `Confusion 2`

### 0 : Fizzle (`D6Fizzle`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, min_aoe 0, max_aoe 0`
- **Damage/Effects:** `damage 6, Confusion 2`

### 3 : Laser (`D6Laser`)

- **Template:** `laser`
- **Cost:** `mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5`

### 2 : Poop (`D6Poop`)

- **Template:** `spawn`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [[-1, 0]]`
- **Damage/Effects:** `None`

### 4 : Quake (`D6Quake`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, aoe_mode diagcross, max_aoe 10, aoe_excludes_self true`
- **Damage/Effects:** `damage 5, Bruise 1, distance 2`

### 5 : Storm (`D6Storm`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `max_aoe 3, max_range 8, aoe_excludes_self true`
- **Damage/Effects:** `damage 5, Stun [1, .5]`

### 6 : Wrath (`D6Wrath`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, aoe_mode square, min_aoe 0, max_aoe 10, aoe_excludes_self true`
- **Damage/Effects:** `damage 10, Burn 3`

### DiceLeap (`DiceLeap`)

- **Template:** `jump_attack`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `range_mode square, max_range 10, aoe_mode standard, max_aoe 0, min_aoe 0, aoe_excludes_self false, restrictions none`
- **Damage/Effects:** `damage 0, VaporizeDice 1`

### Roll! (`RollDice`)

- **Template:** `spawn`
- **Cost:** `mana 0, charge 0`
- **Target/Shape:** `max_range 3`
- **Damage/Effects:** `None`

---

## Gein

### Spin Cleave (`BasicButcherMeleeWideSpin`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, max_aoe 1+bonus_melee_range, aoe_mode square`
- **Damage/Effects:** `damage 5+bonus_melee_damage, Cleave 1`

### MoveTwo (`MoveTwo`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `max_range 2`
- **Damage/Effects:** `None`

---

## Glowing Bear

### Melee Attack (`BasicBigMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range`
- **Damage/Effects:** `None`

---

## Hellspawn

### Cleave (`BasicButcherMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction8, max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 5+bonus_melee_damage, Cleave 1`

### MoveTwo (`MoveTwo`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `max_range 2`
- **Damage/Effects:** `None`

---

## Lenny

### LennyCatDies (`LennyCatDies`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, knockback_mode none`
- **Damage/Effects:** `damage 0, type none`

### Cat Slap (`LennyCatSlap`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `aoe_mode custom, aoe_symmetry none, custom_aoe [[1, -1] [1, 0] [1, 1]]`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 10, CollideWithConsumed 1+bonus_melee_damage`

### Drop Cat (`LennyDrop`)

- **Template:** `throw_attack`
- **Cost:** `mana 0, must_be_consuming true`
- **Target/Shape:** `max_range 1, min_range 1, restrictions none, throw_consumed_character true, prioritize_dont_change_direction true, reorient_thrown_character true, range_mode cross`
- **Damage/Effects:** `damage 0, ai_base_score 9999`

### LennyGrab (`LennyGrab`)

- **Template:** `targeted_status`
- **Cost:** `mana 0, must_not_be_consuming true, cantrip true`
- **Target/Shape:** `max_range 1, range_mode cross, restrictions [must_have_buddy must_have_living_character]`
- **Damage/Effects:** `type none, damage 0, cant_miss true, layer characters, instant true, mount_mode true, force_contact true, drop_on_death false, do_not_pop_corpse true, struggle_ability LennyStruggle`

### LennyGrabDead (`LennyGrabDead`)

- **Template:** `targeted_status`
- **Cost:** `mana 0, must_not_be_consuming true, cantrip true`
- **Target/Shape:** `max_range 1, range_mode cross, restrictions [must_have_buddy must_have_corpse]`
- **Damage/Effects:** `type none, damage 0, cant_miss true, layer characters, instant true, mount_mode true, force_contact true, drop_on_death false, do_not_pop_corpse true, struggle_ability LennyStruggle`

### Hug (`LennyHug`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, knockback_mode none, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 1+bonus_melee_damage, type melee, contact_requires_adjacency false, ai_base_score 9999`

### LennyShove (`LennyShove`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 10, custom_additional_ai_weight must_not_target_buddy`

### LennyStruggleFail (`LennyStruggleFail`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Lucy

### Magic Dart (`BasicMagicShortRanged`)

- **Template:** `ranged_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 5+bonus_range`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, type physical_spell, ranged true`

### MC Blizz (`MCBlizzard`)

- **Template:** `spell`
- **Cost:** `mana 5, prime 1`
- **Target/Shape:** `target_mode direction, aoe_mode circle, min_aoe 1, max_aoe 2`
- **Damage/Effects:** `damage 3, knockback 1, Freeze 1`

### MC Flamethrower (`MCFlamethrower`)

- **Template:** `spell`
- **Cost:** `mana 5, prime 1`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe 4`
- **Damage/Effects:** `damage 3, Burn 3`

### MC Thunder (`MCStorm`)

- **Template:** `spell`
- **Cost:** `mana 5, prime 1`
- **Target/Shape:** `max_range 5, target_mode direction, aoe_mode custom, aoe_symmetry four_way, custom_aoe [[1, 1] [2, 2] [3, 3] [4, 4] [5, 5] [6, 6] [7, 7] [8, 8] [9, 9]]`
- **Damage/Effects:** `damage 3, Stun [1, .5]`

---

## Magnus

### BasicMelee_Fighter (`BasicMelee_Fighter`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Chain Dash (`ChainDash`)

- **Template:** `dash_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1`

### Spin (`Spin_Enemy`)

- **Template:** `melee_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode cross, knockback_mode character_to_tile, multihit 3`
- **Damage/Effects:** `damage 2+bonus_melee_damage`

---

## Maisie

### Push Attack (`BasicTankMelee`)

- **Template:** `dash_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1+bonus_range, max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1`

### LickyLicky (`LickyLicky`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 1, StrengthUp 1, Cleanse 0`

### SwapPositions_TankCat (`SwapPositions_TankCat`)

- **Template:** `swap`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `None`

---

## Mama Maggot

### Mutate (`MutateAOE`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `min_range 0, max_range 6, max_aoe 1`
- **Damage/Effects:** `damage 0, elements [, Mutate, ]`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Rally, Maggots! (`RallyMaggots`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `min_range 0, max_range 4, max_aoe 2, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, AlliesTakeExtraTurn 1`

### Spawn Maggots (`SpawnMaggots`)

- **Template:** `spawn`
- **Cost:** `mana 5`
- **Target/Shape:** `min_range 0, max_range 2, max_aoe 1, max_targets 2`
- **Damage/Effects:** `None`

---

## Mangler's Monster

### ManglerMonsterDashAttack (`ManglerMonsterDashAttack`)

- **Template:** `dash_attack`
- **Cost:** `Free`
- **Target/Shape:** `consider_trample true`
- **Damage/Effects:** `damage 10+bonus_melee_damage, override_trample_damage true`

### ManglerMonsterExplode (`ManglerMonsterExplode`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode circle, min_aoe 0, max_aoe 20, aoe_excludes_self true, aoe_considers_character_size true`
- **Damage/Effects:** `damage 0, knockback 10, ai_base_score 999999`

### ManglerMonsterHeartAttack (`ManglerMonsterHeartAttack`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `FormChange NoDeathrattle, DieViaAbilityInternally 1`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Marshmallow

### Melee Attack / Heal (`BasicMedicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 5+bonus_melee_damage, ContextualHeal 1`

### Convert (`MarshmallowConvert`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `min_range 1, max_range level, max_aoe 0`
- **Damage/Effects:** `damage 0, type spell, Charmed 1, TakeExtraTurn 1, GenericDebuff 999`

### Zealot (`MarshmallowZealot`)

- **Template:** `self_buff`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `DivineShield 1`

---

## Medium Slime

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Morana

### Leech Shot (`BasicNecroRanged`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 3+bonus_range`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, Leeches 1`

### NCGravecrawl (`NCGravecrawl`)

- **Template:** `*(None)*`
- **Cost:** `infcantrip false, cantrip false, act_points 1`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 999999`

### NCReanimate (`NCReanimate`)

- **Template:** `*(None)*`
- **Cost:** `infcantrip false, cantrip false, act_points 1`
- **Target/Shape:** `max_range 3`
- **Damage/Effects:** `Reanimate 100%`

---

## Pachysaurus [img:female]

### GirlDinoCry (`GirlDinoCry`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "Rage"`

### GirlDinoHeadBash (`GirlDinoHeadBash`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Stun 1`

### GirlDinoMelee (`GirlDinoMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Stun 1`

### GirlDinoPoop (`GirlDinoPoop`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [[-1, 0][-2, 0]], aoe_considers_character_size true`
- **Damage/Effects:** `None`

### GirlDinoThrow (`GirlDinoThrow`)

- **Template:** `throw_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 10, min_range 1, restrictions none, range_mode cross`
- **Damage/Effects:** `damage 10+bonus_melee_damage, custom_additional_ai_weight toss_farthest`

---

## Pachysaurus [img:male]

### BoyDinoBasic (`BoyDinoBasic`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1, distance 2, stacks 3, height 2`

### BoyDinoCry (`BoyDinoCry`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "Rage"`

### BoyDinoHeadBash (`BoyDinoHeadBash`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `knockback 3`

---

## Paraisaria

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### IDBrambleBurst (`IDBrambleBurst`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, min_range 0, max_range 0, min_aoe 0, max_aoe 2`
- **Damage/Effects:** `damage 0, knockback 0, ChangeTile BrambleTile, PopAndSpawn Sprout`

### Bramble Shot (`IDBrambleShot`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 2, max_aoe 0`
- **Damage/Effects:** `damage 2, BramblesOnHit 1`

### Sprout (`IDSprout`)

- **Template:** `spawn`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, aoe_mode square, max_aoe 20, max_targets 1`
- **Damage/Effects:** `None`

---

## Pebbles

### Boulder Drop! (`ColorlessCat_BoulderDrop`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `target_mode tile, min_range 1, max_range 20, max_aoe 0, range_excludes_blocking false, aoe_restrictions none, knockback_mode zero`
- **Damage/Effects:** `damage 999, cant_miss true, type ranged, AIFavorLowHealth 100`

### Push (`ColorlessCat_Push`)

- **Template:** `dash_attack`
- **Cost:** `mana 0, act_points 1`
- **Target/Shape:** `target_mode direction8, max_range 1, max_aoe 1, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 4+bonus_melee_damage, knockback 10`

### Rock Toss (`RockToss_ColorlessCat`)

- **Template:** `lobbed_attack`
- **Cost:** `mana 0, act_points 1`
- **Target/Shape:** `min_range 3, max_range 5`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, BounceObject SmallRock`

### RockToss_ColorlessCat_AsCloseAsPossible (`RockToss_ColorlessCat_AsCloseAsPossible`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `custom_additional_ai_weight tile_close_to_enemy`

---

## Poobles Rocksnow

### Bear Trap (`BearTrap_CaveBaby`)

- **Template:** `lobbed_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `min_range 1, max_range 2, restrictions must_be_empty`
- **Damage/Effects:** `damage 0, ai_base_score 10, custom_additional_ai_weight tile_has_no_known_traps, SpawnBearTrap 1`

### CaveCatEnrageOne (`CaveCatEnrageOne`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "TwoAlive"`

### CaveCatEnrageTwo (`CaveCatEnrageTwo`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "OneAlive"`

### Pounce (`CaveCatPounce`)

- **Template:** `jump_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_excludes_self false, max_aoe 0, min_aoe 0, max_range 4, restrictions none, always_bounce true`
- **Damage/Effects:** `damage 5+bonus_melee_damage, IgnoreSelf 1`

---

## Rat King

### RatKing2Spawn (`RatKing2Spawn`)

- **Template:** `spawn`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [[-1 0]], knockback_mode none, aoe_considers_character_size true, aoe_excludes_self true, range_excludes_blocking false, restrictions aoe_must_exist, min_targets 1, max_targets 2, prioritize_dont_change_direction true`
- **Damage/Effects:** `None`

### RatKingSpawn (`RatKingSpawn`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode line, min_aoe 1, max_aoe 1, restrictions aoe_must_exist, aoe_considers_character_size true, aoe_excludes_self true, range_excludes_blocking false`
- **Damage/Effects:** `None`

### Toss (`RatKingToss`)

- **Template:** `throw_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 10, min_range 2, restrictions none, range_mode cross, toss_direction_restriction forwards`
- **Damage/Effects:** `damage 6+bonus_melee_damage, custom_additional_ai_weight toss_farthest`

### RatKingTransform (`RatKingTransform`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `FormChange HalfDead, DamageUp 3, MovementUp 2, Brace 1`

---

## Small Slime

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Spewer

### SpewerBarf_Lava (`SpewerBarf_Lava`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [[1 0] [2 -1] [2 0] [2 1] [3 -1] [3 0] [3 1] [4 -1] [4 0] [4 1]], max_targets 5`
- **Damage/Effects:** `damage 2+bonus_ranged_damage, ChangeTile LavaTile, Burn 4`

### SpewerBarf_Normal (`SpewerBarf_Normal`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [[1 0] [2 -1] [2 0] [2 1] [3 -1] [3 0] [3 1] [4 -1] [4 0] [4 1]], max_targets 5`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, ChangeTile CreepTile, Poison 1`

### SpewerBarf_Tar (`SpewerBarf_Tar`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [[1 0] [2 -1] [2 0] [2 1] [3 -1] [3 0] [3 1] [4 -1] [4 0] [4 1]], max_targets 5`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, ChangeTile OilTile, Tarred 2`

### SpewerLobbed_Normal (`SpewerLobbed_Normal`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 3, max_range 5`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, ChangeTile CreepTile, Poison 1`

### SpewerSuckLava (`SpewerSuckLava`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `wet false, Burn 4`

### SpewerSuckNormal (`SpewerSuckNormal`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `wet true, Poison 1`

### SpewerSuckPill (`SpewerSuckPill`)

- **Template:** `*(None)*`
- **Cost:** `act_points 0, cantrip true, cantrip_group spewer_suck`
- **Target/Shape:** `max_aoe 3, knockback_mode none`
- **Damage/Effects:** `custom_additional_ai_weight pills_only`

### SpewerSuckTar (`SpewerSuckTar`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `wet false, Tarred 2`

### SpewerTransformFire (`SpewerTransformFire`)

- **Template:** `self_buff`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `prioritize_dont_change_direction true`
- **Damage/Effects:** `heal 4, SpeedUp 1, DeleteObject 1`

### SpewerTransformNormal (`SpewerTransformNormal`)

- **Template:** `self_buff`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `prioritize_dont_change_direction true`
- **Damage/Effects:** `heal 4, DamageUp 1, DeleteObject 1`

### SpewerTransformTar (`SpewerTransformTar`)

- **Template:** `self_buff`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `prioritize_dont_change_direction true`
- **Damage/Effects:** `heal 4, Brace 1, DeleteObject 1`

---

## Stacy Mutant

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### SM_BleedCounter (`SM_BleedCounter`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Bleed 1`

### Flamethrower (`SM_Flamethrower`)

- **Template:** `*(None)*`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 3+bonus_basic_spell_damage, ai_base_score 999999, Burn 2`

### Shards of Ice (`SM_IceShards`)

- **Template:** `spell`
- **Cost:** `prime 1, cantrip true`
- **Target/Shape:** `target_mode direction, aoe_mode circle, min_aoe 1, max_aoe 2`
- **Damage/Effects:** `damage 6+bonus_basic_spell_damage, ai_base_score 999999, Freeze 1`

### Lightning Storm (`SM_LightningStorm`)

- **Template:** `spell`
- **Cost:** `cantrip true, prime 1`
- **Target/Shape:** `max_range 20, target_mode none, aoe_excludes_self true, aoe_mode all, knockback_mode none, aoe_restrictions checker_parity_even`
- **Damage/Effects:** `damage 3+bonus_basic_spell_damage, ai_base_score 999999, Stun [1, .1]`

### SM_MagicMissile (`SM_MagicMissile`)

- **Template:** `*(None)*`
- **Cost:** `cantrip false, infcantrip false, mana 0, act_points 1`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## The Bloat

### BloatFrontLaser (`BloatFrontLaser`)

- **Template:** `laser`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5, Bleed 1`

### Leap (`BloatLeap`)

- **Template:** `jump_attack`
- **Cost:** `act_points 1`
- **Target/Shape:** `min_range 1, max_range 7, min_aoe 0, max_aoe 2, aoe_excludes_self false, aoe_mode standard, restrictions must_be_moveable`
- **Damage/Effects:** `damage 4, IgnoreSelf 1, ChangeTile WaterTile`

### BloatLoseFirstEye (`BloatLoseFirstEye`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "OneEye"`

### BloatLoseSecondEye (`BloatLoseSecondEye`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "NoEyes"`

### BloatSideLaser (`BloatSideLaser`)

- **Template:** `laser`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode custom, custom_aoe [[0 1][0 -1]], restrictions must_match_current_orientation`
- **Damage/Effects:** `damage 5, Bleed 1`

---

## White Rabbit

### BasicMelee_Fighter (`BasicMelee_Fighter`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Chain Dash (`ChainDash`)

- **Template:** `dash_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1`

---

## Wolma Rocksnow

### CaveCatEnrageOne (`CaveCatEnrageOne`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "TwoAlive"`

### CaveCatEnrageTwo (`CaveCatEnrageTwo`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "OneAlive"`

### CaveMom_Basic (`CaveMom_Basic`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `Slow 1`

### CaveMom_Heal (`CaveMom_Heal`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 5, Cleanse 0`

### Toss (`CaveMom_TossDad`)

- **Template:** `throw_attack`
- **Cost:** `cantrip true, cantrip_group cavemomtoss`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `damage 1, blocked_damage 5+bonus_melee_ability_damage, custom_additional_ai_weight toss_towards_buddy`

### Toss (`CaveMom_TossElsewhere`)

- **Template:** `throw_attack`
- **Cost:** `cantrip true, cantrip_group cavemomtoss`
- **Target/Shape:** `max_range 20, restrictions none`
- **Damage/Effects:** `damage 1, blocked_damage 5+bonus_melee_ability_damage`

---

## Zapphauser

### Lightning Burst (`LEBurst`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_excludes_self true, max_aoe 20, prioritize_face_camera 1, knockback_mode none, aoe_restrictions checker_parity_even`
- **Damage/Effects:** `damage 2, elements [, Electric, ]`

### Leave (`LELeave`)

- **Template:** `leave`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 100`

### LEPortFar (`LEPortFar`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `max_range 9`
- **Damage/Effects:** `None`

### Zap (`LEReturn`)

- **Template:** `return`
- **Cost:** `prime 1, cantrip true`
- **Target/Shape:** `aoe_mode standard, max_range 20, restrictions must_be_moveable, aoe_mode diagcross, max_aoe 10, aoe_excludes_self true, allow_any_orientation true, prioritize_face_camera true, force_ai_target_as_spell true, aoe_spell_on_land true, knockback_mode none`
- **Damage/Effects:** `damage 5, type spell, ai_base_score 100, override_trample_damage true, ForceDisplace 1, Stun [0 .25], IgnoreSelf 1`

### Teleport (`Teleport`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Zodiac

### Reload (`Reload`)

- **Template:** `self_buff`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Ammo -99999, Ammo 6, FormChange active`

### ZodiacShoot (`ZodiacShoot`)

- **Template:** `straightshot_attack`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `target_mode tile, min_range 1, max_range 20, max_aoe 100, max_targets -X, X_is enable_if_has_ammo`
- **Damage/Effects:** `damage 7+bonus_ranged_damage`

---

# Regular Enemies

## Albino Tom Tom

### WideSwipe (`WideSwipe`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode custom, aoe_symmetry none, custom_aoe [[1, -1] [1, 0] [1, 1]]`
- **Damage/Effects:** `None`

---

## Amoeba

### AmoebaAttach (`AmoebaAttach`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `restrictions must_have_cat`
- **Damage/Effects:** `damage 0, force_play_hit_animation true, pool [AmoebaHat AmoebaNeck AmoebaFace]`

### PickupRock (`PickupRock`)

- **Template:** `*(None)*`
- **Cost:** `mana 0, must_not_be_consuming true, cantrip true`
- **Target/Shape:** `target_mode tile, min_range 0, max_range 1, min_aoe 0, max_aoe 0, restrictions [must_have_tag], target_requires_tag rock`
- **Damage/Effects:** `type none, damage 0, cant_miss true, layer characters, instant true, use_placeholder true, drop_on_death deferred, struggle_ability Thrash`

---

## Angelic Cat

### Holy Wind (`AngelcatWind`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe 2`
- **Damage/Effects:** `damage 3, knockback 4, Blind 2, OverrideKnockbackDamage 5`

### Jump (`BasicJump`)

- **Template:** `jump_attack`
- **Cost:** `move_points 1, act_points 0`
- **Target/Shape:** `target_mode tile, min_range 1, max_range mov, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, aoe_considers_character_size false, range_display_include_character_size true, restrictions must_be_moveable`
- **Damage/Effects:** `type none, damage 0`

---

## Angelic Kitten

### Allure (`CherubAttract`)

- **Template:** `targeted_status`
- **Cost:** `Free`
- **Target/Shape:** `max_range 5`
- **Damage/Effects:** `damage 0, Attraction 1`

### CherubDoom (`CherubDoom`)

- **Template:** `targeted_status`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `damage 0, Doomed 2`

### Poison Kiss (`CherubMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, Poison 5`

---

## Ankylosaurus

### AnkyloSpin (`AnkyloSpin`)

- **Template:** `melee_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `aoe_mode square, knockback_mode character_to_tile, prioritize_dont_change_direction 1`
- **Damage/Effects:** `knockback 2, Bruise 1`

### AnkyloSwipe (`AnkyloSwipe`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode custom, aoe_symmetry none, custom_aoe [[1, -1] [1, 0] [1, 1]]`
- **Damage/Effects:** `knockback 10, Stun [1 .33]`

---

## Astronaut

### Jump (`BasicJump`)

- **Template:** `jump_attack`
- **Cost:** `move_points 1, act_points 0`
- **Target/Shape:** `target_mode tile, min_range 1, max_range mov, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, aoe_considers_character_size false, range_display_include_character_size true, restrictions must_be_moveable`
- **Damage/Effects:** `type none, damage 0`

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Atomic Kitten

### Radiate (`AtomicBurst`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, min_aoe 1, max_aoe 2, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 3+bonus_basic_spell_damage, knockback 3, elements [, Mutate, ]`

### Teleport (`Teleport`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## B-Prober

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### GP_Probe (`GP_Probe`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `restrictions [aoe_must_exist], aoe_restrictions [must_backstab must_have_cat]`
- **Damage/Effects:** `type none, damage 0, cant_miss true, force_play_hit_animation true, ProbeCharmed 1`

---

## Baby Deathworm

### Dash (`Dash_BabyDeathWorm`)

- **Template:** `dash_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 4+bonus_melee_damage, FlatLeech 2`

### Teleport (`Teleport`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Baby Shark

### BabySharkMelee (`BabySharkMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, Bleed 1`

---

## Baby Squirrel

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Bat

### BatFlurry (`BatFlurry`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `multihit 4`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, Confusion [1 .5]`

---

## Bear

### Melee Attack (`BasicBigMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range`
- **Damage/Effects:** `None`

---

## Bear2

### Bear Swipes (`BearFurySwipes`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Beaver

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Belcher

### Spit Lava (`BelcherLavashot`)

- **Template:** `lobbed_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `min_range 1, max_range 2`
- **Damage/Effects:** `damage 2+bonus_ranged_damage, Burn 2, tile LavaTile`

---

## Big Asteroid

### BigAsteroidBarrage (`BigAsteroidBarrage`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_excludes_self true, aoe_considers_character_size true, aoe_mode line, max_aoe 1, min_aoe 1, multihit 3, stagger_multihit_targets true, multihit_target_distance_sort true`
- **Damage/Effects:** `damage 4+bonus_ranged_damage, BounceObject Boulder, damage 1, max_dist 2`

---

## Bigfoot

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Bird

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### BirdFly (`BirdFly`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `as_the_crow_flies true`
- **Damage/Effects:** `None`

---

## Birthwort

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### BirthwortHeal (`BirthwortHeal`)

- **Template:** `spell`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode none, aoe_excludes_self false`
- **Damage/Effects:** `heal 2, elements [, Grass, ]`

### Shot (`BirthwortReactionShot`)

- **Template:** `straightshot_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode custom, custom_aoe [[0, 1] [0,-1]]`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, Rot 1`

### Trample Dash (`BirthwortTrample`)

- **Template:** `trample_dash`
- **Cost:** `cantrip true`
- **Target/Shape:** `max_range 3`
- **Damage/Effects:** `damage 3+bonus_melee_damage`

---

## Bishop Hat

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Bloated Corpse

### Explode (`BloatyExplodey`)

- **Template:** `spell`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode cross, knockback_mode character_to_tile, target_mode none, min_range 0, max_range 0, min_aoe 1, max_aoe 1`
- **Damage/Effects:** `damage 1, knockback 1, Poison 1`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Blorb

### Gunk Ball (`BigGunkShot`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `min_range 2, max_range 3, max_aoe 1`
- **Damage/Effects:** `damage 3+bonus_basic_spell_damage, Slow 3`

---

## Bomb Fly

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Bombchu

### Bombchu Dash (`RocketSkates_Bombchu`)

- **Template:** `dash_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode standard, min_aoe 0, max_aoe 1, knockback_mode character_to_tile, aoe_excludes_self false`
- **Damage/Effects:** `damage 5, knockback 1, type spell, incidentally_collects_pickups false, VisualFXTile Explosion`

---

## Bone Worm

### Bone Shot (`BoneWormShotSmall`)

- **Template:** `lobbed_attack`
- **Cost:** `act_points 1`
- **Target/Shape:** `min_range 1, max_range 4`
- **Damage/Effects:** `damage 3+bonus_ranged_damage`

### FormGrowThree (`FormGrowThree`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form 3`

### FormGrowThreeSnakey (`FormGrowThreeSnakey`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Shield 1, EndTurn 1, DamageUp 1`

### FormGrowTwo (`FormGrowTwo`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form 2`

### FormGrowTwoSnakey (`FormGrowTwoSnakey`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Shield 1, EndTurn 1, DamageUp 1`

### FormShrinkOneSnakey (`FormShrinkOneSnakey`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `DamageUp -1`

### FormShrinkTwoSnakey (`FormShrinkTwoSnakey`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `DamageUp -1`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Boomer

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### BoomerCatExplode (`BoomerCatExplode`)

- **Template:** `spell`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode square, knockback_mode character_to_tile, aoe_excludes_self true, target_mode none, min_range 0, max_range 0, min_aoe 0, max_aoe 1`
- **Damage/Effects:** `damage 5, knockback 1, elements [, Explosion, ]`

---

## Boulder

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Bounty Hunter

### Shoot Gun (`GuncatShoot`)

- **Template:** `ranged_attack`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `min_range 1, max_range 20`
- **Damage/Effects:** `damage 4+bonus_ranged_damage`

---

## Brain Drain

### Brain Missile (`BrainDrainMagicMissile`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 3`

### Counterspell (`Counterspell`)

- **Template:** `self_buff`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Counterspell 1`

---

## Bramble Baby

### BrambleBabyEntangle (`BrambleBabyEntangle`)

- **Template:** `spell`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `target_mode none, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, Tangled 1, BramblesOnHit 1`

### BramblePull (`BramblePull`)

- **Template:** `straightshot_attack`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `max_range 10, knockback_mode pull_to_character`
- **Damage/Effects:** `damage 3+bonus_ranged_damage`

### Teleport (`Teleport`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Brute

### DemonRockThrow (`DemonRockThrow`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, Stun [1, .2], BounceObject SmallRock, BonusDamageBasedOnDistance 1`

### DemonUppercut (`DemonUppercut`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, stacks 3, distance 3`

### NeckSnap (`NeckSnap`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode tile_to_character, restrictions must_have_character`
- **Damage/Effects:** `damage 0, threshold_percent 50%, DieViolently 1`

---

## Bunga's Champion

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### CaveBabyFoodMove (`CaveBabyFoodMove`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `restrictions [must_be_moveable must_have_tag must_move], target_requires_tag food`
- **Damage/Effects:** `None`

### CaveBabyGrow (`CaveBabyGrow`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 20, form "CaveManSpear"`

### Fooga Bunga (`CaveManChestPound`)

- **Template:** `spell`
- **Cost:** `mana 0, requires_exact_character_aux 0`
- **Target/Shape:** `target_mode none, max_aoe 3, prioritize_dont_change_direction true, aoe_excludes_self false`
- **Damage/Effects:** `damage 0, type status_spell, tag humanoid, DamageUp 1`

### CaveManPickupSpear (`CaveManPickupSpear`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `restrictions must_have_tag, target_requires_tag spear`
- **Damage/Effects:** `damage 0, type none, makes_contact false, cant_miss true, tag spear, DeleteObject 1, form "CaveManSpear"`

### CaveManSpearRun (`CaveManSpearRun`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### CaveManTransform (`CaveManTransform`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "WereMan"`

### CaveWomanBirth (`CaveWomanBirth`)

- **Template:** `spawn`
- **Cost:** `mana 5`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [ [-1, 0] ]`
- **Damage/Effects:** `None`

### CaveWomanDrop (`CaveWomanDrop`)

- **Template:** `throw_attack`
- **Cost:** `mana 0, must_be_consuming true`
- **Target/Shape:** `max_range 1, min_range 1, restrictions none, throw_consumed_character true, prioritize_dont_change_direction true, reorient_thrown_character true, range_mode cross`
- **Damage/Effects:** `damage 0, ai_base_score 9999`

### CaveWomanDropTransform (`CaveWomanDropTransform`)

- **Template:** `throw_attack`
- **Cost:** `mana 0, must_be_consuming true`
- **Target/Shape:** `target_mode random_tile, max_range 5, min_range 3, restrictions none, throw_consumed_character true, prioritize_dont_change_direction true, reorient_thrown_character true, range_mode cross`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, blocked_damage 5+bonus_melee_ability_damage`

### CaveWomanGrab (`CaveWomanGrab`)

- **Template:** `targeted_status`
- **Cost:** `mana 0, must_not_be_consuming true, cantrip true`
- **Target/Shape:** `max_range 1, range_mode cross, restrictions [must_have_cat must_have_living_character]`
- **Damage/Effects:** `type none, damage 0, cant_miss true, layer characters, instant true, mount_mode true, force_contact true, drop_on_death true, drop_on_self_death true, do_not_pop_corpse true, struggle_ability CaveWomanEscape`

### CaveWomanThrow (`CaveWomanThrow`)

- **Template:** `throw_attack`
- **Cost:** `mana 0, must_be_consuming true, must_be_first_nonmove_action true`
- **Target/Shape:** `max_range 5, min_range 3, restrictions none, throw_consumed_character true`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, blocked_damage 5+bonus_melee_ability_damage`

### Pounce (`WereManPounce`)

- **Template:** `jump_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_excludes_self false, max_aoe 0, min_aoe 0, max_range 5, restrictions none`
- **Damage/Effects:** `damage 5+bonus_melee_damage, IgnoreSelf 1, Leech 1, Displace 1, TriggerWerewolfTransform [1 .5]`

### WereManTransformSwipe (`WereManTransformSwipe`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 2+bonus_melee_damage, type melee, non_lethal true, TriggerWerewolfTransform .5`

---

## Bunny

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Burfer Maggot

### Tumor Prison (`PrisonShot`)

- **Template:** `ranged_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 2, restrictions none`
- **Damage/Effects:** `damage 2+bonus_ranged_damage, Imprison Tumor`

---

## Butch & Tink

### MoveOne (`MoveOne`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Trample Dash (`TrampleDash`)

- **Template:** `trample_dash`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 8+bonus_melee_damage`

---

## Butt Zombie

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Fart (`ButtFart`)

- **Template:** `spell`
- **Cost:** `cantrip true, mana 4`
- **Target/Shape:** `target_mode none, aoe_mode standard, min_aoe 1, max_aoe 1, aoe_considers_character_size true, aoe_excludes_self true, dont_orient true`
- **Damage/Effects:** `damage 0, knockback 1, Poison 4`

### Flip (`ButtFlip`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "Down"`

### Spin (`Spin_Enemy`)

- **Template:** `melee_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode cross, knockback_mode character_to_tile, multihit 3`
- **Damage/Effects:** `damage 2+bonus_melee_damage`

### Teleport (`Teleport`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Flip (`TeleportFlipUp`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20, dont_orient true`
- **Damage/Effects:** `None`

---

## Cactus

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Cancer Cat

### CancerExplode (`CancerExplode`)

- **Template:** `spell`
- **Cost:** `mana 5`
- **Target/Shape:** `knockback_mode character_to_tile, aoe_excludes_self true, target_mode none, min_range 0, max_range 0, min_aoe 1, max_aoe 2`
- **Damage/Effects:** `damage 5, knockback 1, object GasCloud`

### CancerMelee (`CancerMelee`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ConstitutionUp -1, chance 30%, disease Cancer`

---

## Candle

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Carcass

### CarcusSpawn (`CarcusSpawn`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1, allow_any_orientation true`
- **Damage/Effects:** `None`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Carnibulb

### CarnibulbEat (`CarnibulbEat`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1`
- **Damage/Effects:** `type melee, damage 0, piercing true, cant_miss true, OverrideDamage 25`

### Sprout (`Sprout`)

- **Template:** `spawn`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, aoe_mode square, max_aoe 20, max_targets 1`
- **Damage/Effects:** `None`

---

## Cat Caller

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Cat Call (`CatCall`)

- **Template:** `spell`
- **Cost:** `mana 5, cantrip true`
- **Target/Shape:** `min_range 0, max_range 6, max_aoe 0`
- **Damage/Effects:** `damage 0, Slow 2`

---

## Cat Cultist

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Cut (`CultistCut`)

- **Template:** `self_buff`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1, ai_base_score 99999`

---

## CatHuman

### Howl (`CHCry`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, min_aoe 0, max_aoe 3, aoe_excludes_self true, aoe_considers_character_size true`
- **Damage/Effects:** `damage 0, type status_spell, Immobile [1, .5]`

### CHSpawn (`CHSpawn`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [ [-1, 0] ]`
- **Damage/Effects:** `None`

### Toss (`CHToss`)

- **Template:** `throw_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 4, min_range 2, restrictions none, range_mode cross, toss_direction_restriction backwards`
- **Damage/Effects:** `damage 1+bonus_melee_damage, custom_additional_ai_weight toss_farthest, RandomInjury 1`

---

## Catbot

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Caterpillar

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Caveman

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### CaveBabyFoodMove (`CaveBabyFoodMove`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `restrictions [must_be_moveable must_have_tag must_move], target_requires_tag food`
- **Damage/Effects:** `None`

### CaveBabyGrow (`CaveBabyGrow`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 20, form "CaveManSpear"`

### Fooga Bunga (`CaveManChestPound`)

- **Template:** `spell`
- **Cost:** `mana 0, requires_exact_character_aux 0`
- **Target/Shape:** `target_mode none, max_aoe 3, prioritize_dont_change_direction true, aoe_excludes_self false`
- **Damage/Effects:** `damage 0, type status_spell, tag humanoid, DamageUp 1`

### CaveManPickupSpear (`CaveManPickupSpear`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `restrictions must_have_tag, target_requires_tag spear`
- **Damage/Effects:** `damage 0, type none, makes_contact false, cant_miss true, tag spear, DeleteObject 1, form "CaveManSpear"`

### CaveManSpearRun (`CaveManSpearRun`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### CaveManTransform (`CaveManTransform`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "WereMan"`

### CaveWomanBirth (`CaveWomanBirth`)

- **Template:** `spawn`
- **Cost:** `mana 5`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [ [-1, 0] ]`
- **Damage/Effects:** `None`

### CaveWomanDrop (`CaveWomanDrop`)

- **Template:** `throw_attack`
- **Cost:** `mana 0, must_be_consuming true`
- **Target/Shape:** `max_range 1, min_range 1, restrictions none, throw_consumed_character true, prioritize_dont_change_direction true, reorient_thrown_character true, range_mode cross`
- **Damage/Effects:** `damage 0, ai_base_score 9999`

### CaveWomanDropTransform (`CaveWomanDropTransform`)

- **Template:** `throw_attack`
- **Cost:** `mana 0, must_be_consuming true`
- **Target/Shape:** `target_mode random_tile, max_range 5, min_range 3, restrictions none, throw_consumed_character true, prioritize_dont_change_direction true, reorient_thrown_character true, range_mode cross`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, blocked_damage 5+bonus_melee_ability_damage`

### CaveWomanGrab (`CaveWomanGrab`)

- **Template:** `targeted_status`
- **Cost:** `mana 0, must_not_be_consuming true, cantrip true`
- **Target/Shape:** `max_range 1, range_mode cross, restrictions [must_have_cat must_have_living_character]`
- **Damage/Effects:** `type none, damage 0, cant_miss true, layer characters, instant true, mount_mode true, force_contact true, drop_on_death true, drop_on_self_death true, do_not_pop_corpse true, struggle_ability CaveWomanEscape`

### CaveWomanThrow (`CaveWomanThrow`)

- **Template:** `throw_attack`
- **Cost:** `mana 0, must_be_consuming true, must_be_first_nonmove_action true`
- **Target/Shape:** `max_range 5, min_range 3, restrictions none, throw_consumed_character true`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, blocked_damage 5+bonus_melee_ability_damage`

### Pounce (`WereManPounce`)

- **Template:** `jump_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_excludes_self false, max_aoe 0, min_aoe 0, max_range 5, restrictions none`
- **Damage/Effects:** `damage 5+bonus_melee_damage, IgnoreSelf 1, Leech 1, Displace 1, TriggerWerewolfTransform [1 .5]`

### WereManTransformSwipe (`WereManTransformSwipe`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 2+bonus_melee_damage, type melee, non_lethal true, TriggerWerewolfTransform .5`

---

## Caveman Chief

### Gruk Oog Mooga (`CaveChiefBat`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, threshold_flat 10, BonusDamage 20+bonus_melee_damage`

### Raoog Fooba (`CaveChiefFear`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode cone, aoe_leading_edge_only true, min_aoe 1, max_aoe 10, aoe_considers_character_size true, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, Fear 1`

### Atook Thag Kat (`CaveChiefRally`)

- **Template:** `targeted_status`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20, min_range 1, restrictions must_have_tag, target_requires_tag humanoid`
- **Damage/Effects:** `damage 0, TakeExtraTurn 1`

### CaveChiefSlam (`CaveChiefSlam`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 2, aoe_restrictions none`
- **Damage/Effects:** `damage 5+bonus_melee_damage, Stun 1`

---

## Chain Demon

### DH_Attack (`DH_Attack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 4+bonus_melee_damage, Burn 2`

### DH_MeatHook (`DH_MeatHook`)

- **Template:** `straightshot_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `max_range 10, knockback_mode pull_to_character`
- **Damage/Effects:** `damage 0, BonusDamageBasedOnDistance 1, BonusDamage -1, CapDamage 1`

---

## Chaos Stacy

### ChaosStacyAttack (`ChaosStacyAttack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, GenericDebuff 10, Scrambled 1`

---

## Chargey Maggot

### Trample Dash (`SmallTrampleDash`)

- **Template:** `trample_dash`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 4+bonus_melee_damage`

---

## Cherubim

### Bless (`CherubimHeal`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 2, max_range 6, aoe_excludes_self true`
- **Damage/Effects:** `heal 4, DivineShield 1`

### Leave (`CherubimLeave`)

- **Template:** `leave`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 100`

### Crash (`CherubimReturn`)

- **Template:** `return`
- **Cost:** `prime 1, cantrip true`
- **Target/Shape:** `aoe_mode standard, max_range 20, restrictions must_be_moveable, max_aoe 2, allow_any_orientation true, prioritize_face_camera true, force_ai_target_as_spell true`
- **Damage/Effects:** `damage 15+bonus_melee_damage, ai_base_score 100, override_trample_damage true, ForceDisplace 1, Stun 1, IgnoreSelf 1`

---

## Chum Bag

### Chum Shot (`ChumShot_Damage`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `damage 4+bonus_ranged_damage`

### Chum Shot (`ChumShot_Maggot`)

- **Template:** `spawn`
- **Cost:** `mana 0, charge 0`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `None`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Chummy

### Chum Dash (`ChumDash`)

- **Template:** `dash_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1`

---

## Cloaked Demon

### CloakerHex (`CloakerHex`)

- **Template:** `targeted_status`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `damage 0, type status_spell, Hex 1`

### Twisting Flames (`TwistingFlames`)

- **Template:** `spell`
- **Cost:** `prime 1`
- **Target/Shape:** `min_range 3, max_range 4, min_aoe 0, max_aoe 2`
- **Damage/Effects:** `damage 4, ContextualHeal 1, Burn 3`

---

## Cloning Vat

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Clot

### ClotEvolve (`ClotEvolve`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 999999, PopAndSpawn StemCat_HalfHealth`

### ClotFailEvolve (`ClotFailEvolve`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 999999`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Conjoined Husk

### CHuskBone (`CHuskBone`)

- **Template:** `straightshot_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 4`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, Bruise 1`

### CHuskCatShade (`CHuskCatShade`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

### CHuskDrop (`CHuskDrop`)

- **Template:** `throw_attack`
- **Cost:** `mana 0, must_be_consuming true`
- **Target/Shape:** `max_range 7, min_range 2, restrictions none, throw_consumed_character true, prioritize_dont_change_direction true, reorient_thrown_character true, range_mode cross`
- **Damage/Effects:** `damage 0, ai_base_score 9999`

### CHuskDropFail (`CHuskDropFail`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, knockback_mode none, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 1+bonus_melee_damage, type melee, contact_requires_adjacency false, ai_base_score 9999`

### CHuskGrab (`CHuskGrab`)

- **Template:** `targeted_status`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1, range_mode cross, restrictions [must_have_cat must_have_living_character]`
- **Damage/Effects:** `type none, damage 0, cant_miss true, layer characters, instant true, mount_mode true, force_contact true, drop_on_death true, drop_on_self_death true, do_not_pop_corpse true, struggle_ability CHuskStruggle`

---

## Cop Bot

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Reload (`CBReload`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Ammo 1, FormChange active`

### CBShoot_ZodiacStyle (`CBShoot_ZodiacStyle`)

- **Template:** `straightshot_attack`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `target_mode tile, min_range 1, max_range 20, max_aoe 100, max_targets -X, X_is enable_if_has_ammo`
- **Damage/Effects:** `damage 7+bonus_ranged_damage`

---

## Core Freak

### CoreFreakAttack (`CoreFreakAttack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, Stun 1`

### Fury (`CoreFreakFury`)

- **Template:** `melee_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `multihit 3`
- **Damage/Effects:** `damage 3+bonus_melee_damage`

---

## Crate

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Crater Creeper

### CraterCreeperRockBlast (`CraterCreeperRockBlast`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `aoe_restrictions must_be_empty, restrictions aoe_must_exist`
- **Damage/Effects:** `damage 0, type melee, incidentally_collects_pickups false, SendRock 1`

### Slide (`CraterCreeperSlide`)

- **Template:** `trample_dash`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 6`
- **Damage/Effects:** `damage 3+bonus_melee_damage, ai_base_score 9999`

### MoveOne (`MoveOne`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

### ShortCreepshotCrater (`ShortCreepshotCrater`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 2`
- **Damage/Effects:** `damage 4+bonus_ranged_damage, SpawnCreep 1, BounceObject Amoeba`

### Swim (`Swim`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `max_range 10, range_mode square, restrictions [must_be_moveable must_have_liquid]`
- **Damage/Effects:** `None`

---

## Creep Pill

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Crow2

### CrowFlap2 (`CrowFlap2`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 10`
- **Damage/Effects:** `damage 2, knockback 2`

### CrowFlutter2 (`CrowFlutter2`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `max_range 4`
- **Damage/Effects:** `None`

---

## Crow3

### CrowFlap3 (`CrowFlap3`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 10`
- **Damage/Effects:** `damage 3, knockback 10`

### CrowFlutter3 (`CrowFlutter3`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `min_range 2, max_range 5`
- **Damage/Effects:** `None`

---

## Cultist

### Bless (`BBBless`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, aoe_mode square, min_aoe 0, max_aoe 10, aoe_excludes_self true, aoe_restrictions [allies_only]`
- **Damage/Effects:** `heal 5, DamageUp 1`

### Cut (`BBCut`)

- **Template:** `self_buff`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1, type melee, DamageUp 1`

### BBPickupCrown (`BBPickupCrown`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode tile, min_range 0, max_range 1, min_aoe 0, max_aoe 0, restrictions [must_have_tag], target_requires_tag bishop_hat`
- **Damage/Effects:** `type melee, damage 0, piercing true, cant_miss true, form "Bishop"`

### BBPullBomb (`BBPullBomb`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "ZealotBomb"`

### Spin (`BBSpin`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `aoe_mode cross, knockback_mode character_to_tile`
- **Damage/Effects:** `damage 4+bonus_melee_damage`

### Toss (`BBToss`)

- **Template:** `throw_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 4, min_range 2, restrictions none, range_mode cross, toss_direction_restriction backwards`
- **Damage/Effects:** `damage 1+bonus_melee_damage, custom_additional_ai_weight toss_far`

### BBTransformMutant (`BBTransformMutant`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "Mutant"`

### BBTransformZealot (`BBTransformZealot`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "Zealot"`

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Cutter

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Cut (`CutterCut`)

- **Template:** `self_buff`
- **Cost:** `mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Bleed 1, StrengthUp 2`

---

## D6

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Daddy Shark

### DaddyHungry (`DaddyHungry`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1`
- **Damage/Effects:** `type melee, damage 0, piercing true, cant_miss true, Vaporize 20, FlatLeech 10`

---

## Death Worm

### Eat (`DeathWormEat`)

- **Template:** `return`
- **Cost:** `Free`
- **Target/Shape:** `restrictions aoe_must_be_force_displaceable, min_range 0, max_range 0`
- **Damage/Effects:** `ai_base_score 100, Vaporize 1, IgnoreSelf 1`

### Return (`DeathWormReturn`)

- **Template:** `return`
- **Cost:** `move_points 0, act_points 1`
- **Target/Shape:** `restrictions aoe_must_be_force_displaceable, min_range 0, max_range 0`
- **Damage/Effects:** `None`

### Sand Rush (`DeathWormTrampleDash`)

- **Template:** `trample_dash`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage`

### DeathWormTrampleDash_Reaction (`DeathWormTrampleDash_Reaction`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Deathbot

### Flamethrower (`Flamethrower`)

- **Template:** `spell`
- **Cost:** `move_points 0, act_points 1`
- **Target/Shape:** `target_mode direction, aoe_mode line, max_aoe 3, aoe_considers_character_size true, aoe_excludes_self true, knockback_mode character_to_tile`
- **Damage/Effects:** `damage 5, Burn 3`

---

## Decoy

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Der Fötus

### FetusAirstrikeTrigger (`FetusAirstrikeTrigger`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ability FetusAirstrike, relative false, lingering true`

### FetusPullBomb (`FetusPullBomb`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "Bomb"`

### Fury Swipes (`FurySwipes_Enemy`)

- **Template:** `melee_attack`
- **Cost:** `mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 2+bonus_melee_damage, type melee`

---

## Diggy Maggot

### Lick (`Lick`)

- **Template:** `melee_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, Stun [1, .25]`

### Swap (`SwapPositions`)

- **Template:** `swap`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Dino Nest

### DinoEggsSpawn (`DinoEggsSpawn`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1, allow_any_orientation true`
- **Damage/Effects:** `None`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Dip

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Dog

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Doktorbot

### DoctorBotHeal (`DoctorBotHeal`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `multihit 3`
- **Damage/Effects:** `heal 3, PartialCleanse 1, Brace 1, Thorns 1, DivineShield 1, KineticSpikes 1, DamageUp 1, DamageUp 1, ConstitutionUp 1, ConstitutionUp 1, SpeedUp 1, SpeedUp 1`

### DoctorPickup (`DoctorPickup`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `restrictions [must_have_tag], target_requires_tag pickup`
- **Damage/Effects:** `layer pickups, damage 0, ForceCollectsPickups 1`

### DoctorSpawn (`DoctorSpawn`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

---

## Dr. Beanies

### Turtle (`BombRatTurtle`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `BombRatTurtle 1`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Bomb Toss (`RockToss_BomberRat`)

- **Template:** `lobbed_attack`
- **Cost:** `mana 5, cantrip true`
- **Target/Shape:** `max_range 5`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, Stun [1, .10], BounceObject Bomb`

### Spawn Bomb (`SpawnBomb`)

- **Template:** `spawn`
- **Cost:** `mana 5`
- **Target/Shape:** `max_range 5`
- **Damage/Effects:** `None`

---

## Dr. Cat

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Dr. Ditto

### DrDGlare (`DrDGlare`)

- **Template:** `spell`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode none, max_aoe 1, aoe_excludes_self true, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 0, Fear 1`

### DrDRockets (`DrDRockets`)

- **Template:** `spell`
- **Cost:** `cantrip true`
- **Target/Shape:** `max_aoe 2, min_range 1, max_range 3, max_targets 1, restrictions none, can_multihit true`
- **Damage/Effects:** `damage 0, HitExplosion 5`

---

## Dummy Cat

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Dumpster

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Dust Cloud

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## ENEMY_TRAILERCAT2_NAME

### Holy Wind (`AngelcatWind`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe 2`
- **Damage/Effects:** `damage 3, knockback 4, Blind 2, OverrideKnockbackDamage 5`

### Jump (`BasicJump`)

- **Template:** `jump_attack`
- **Cost:** `move_points 1, act_points 0`
- **Target/Shape:** `target_mode tile, min_range 1, max_range mov, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, aoe_considers_character_size false, range_display_include_character_size true, restrictions must_be_moveable`
- **Damage/Effects:** `type none, damage 0`

---

## ENEMY_TRAILERCAT3_NAME

### Holy Wind (`AngelcatWind`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe 2`
- **Damage/Effects:** `damage 3, knockback 4, Blind 2, OverrideKnockbackDamage 5`

### Jump (`BasicJump`)

- **Template:** `jump_attack`
- **Cost:** `move_points 1, act_points 0`
- **Target/Shape:** `target_mode tile, min_range 1, max_range mov, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, aoe_considers_character_size false, range_display_include_character_size true, restrictions must_be_moveable`
- **Damage/Effects:** `type none, damage 0`

---

## ENEMY_TRAILERCAT4_NAME

### Holy Wind (`AngelcatWind`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe 2`
- **Damage/Effects:** `damage 3, knockback 4, Blind 2, OverrideKnockbackDamage 5`

### Jump (`BasicJump`)

- **Template:** `jump_attack`
- **Cost:** `move_points 1, act_points 0`
- **Target/Shape:** `target_mode tile, min_range 1, max_range mov, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, aoe_considers_character_size false, range_display_include_character_size true, restrictions must_be_moveable`
- **Damage/Effects:** `type none, damage 0`

---

## ENEMY_TRAILERCAT5_NAME

### Holy Wind (`AngelcatWind`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe 2`
- **Damage/Effects:** `damage 3, knockback 4, Blind 2, OverrideKnockbackDamage 5`

### Jump (`BasicJump`)

- **Template:** `jump_attack`
- **Cost:** `move_points 1, act_points 0`
- **Target/Shape:** `target_mode tile, min_range 1, max_range mov, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, aoe_considers_character_size false, range_display_include_character_size true, restrictions must_be_moveable`
- **Damage/Effects:** `type none, damage 0`

---

## Edema

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Edmund

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Egg

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Electric Nail

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## ExplodingDecoy

### DecoyExplode (`DecoyExplode`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `knockback_mode character_to_tile, aoe_excludes_self true, target_mode none, min_range 0, max_range 0, min_aoe 0, max_aoe 1`
- **Damage/Effects:** `damage 5, knockback 1, elements [, Explosion, ]`

---

## Fernsehbot

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### TVChangeDie (`TVChangeDie`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, type status_spell, cant_miss true, Doomed 1`

### TVChangeDumb (`TVChangeDumb`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `FormChange Dumb`

### TVChangeObey (`TVChangeObey`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `FormChange Obey`

### TVChangeStop (`TVChangeStop`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `FormChange Stop`

### TVOff (`TVOff`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `FormChange Off`

---

## Fetus

### Lobbed Water Shot (`BasicShortLobbed_Water`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 2+bonus_range`
- **Damage/Effects:** `elements [, Water, ]`

### Bottoms Up (`DrinkUp`)

- **Template:** `self_buff`
- **Cost:** `mana 3`
- **Target/Shape:** `restrictions must_have_liquid`
- **Damage/Effects:** `heal 5`

---

## Fetus Gusher

### FetusGush (`FetusGush`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_aoe 10, aoe_restrictions must_have_piercing_line_of_sight`
- **Damage/Effects:** `type spell, damage 1, knockback 3, elements [, Water, ]`

### Move (`SwimmerMove`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `range_mode water_move`
- **Damage/Effects:** `None`

---

## Fiji Mermaid

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Fire Hydrant

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Flea

### Melee Attack (`SuicideMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Flesh Lad

### Double Hit (`FleshLadDoublehit`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `multihit 2`
- **Damage/Effects:** `damage 1+bonus_melee_damage`

### Uppercut (`FleshLadUppercut`)

- **Template:** `melee_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1+bonus_melee_damage, knockback 3, Bruise 1`

---

## Fleshy Mind

### FleshyMindConfusion (`FleshyMindConfusion`)

- **Template:** `targeted_status`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `damage 0, type status_spell, status Confusion, Confusion 1`

### Disable (`FleshyMindDisable`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode circle, aoe_excludes_self true, knockback_mode character_to_tile, max_aoe 3, aoe_restrictions [enemies_only]`
- **Damage/Effects:** `damage "3+bonus_basic_spell_damage", cant_miss true, type spell, Muted 1, VisualFXTile MagicMissleBlast`

---

## Floast

### FloastPull (`FloastPull`)

- **Template:** `straightshot_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 10, knockback_mode pull_to_character`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, PullSourceToKnockbackImmuneTarget 1`

### FloastSpawn (`FloastSpawn`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `max_range 3`
- **Damage/Effects:** `None`

### Maul (`FloastThrow`)

- **Template:** `throw_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 10, min_range 1, restrictions none, range_mode square, toss_direction_restriction forwards`
- **Damage/Effects:** `damage 8+bonus_melee_damage, custom_additional_ai_weight toss_farthest, Bruise 1, Confusion 1`

---

## Floater

### FloaterMelee (`FloaterMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, RefreshMovePointsIfHit 1`

---

## Florb

### GunkShot (`GunkShot`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 2, max_range 3, restrictions none`
- **Damage/Effects:** `Slow 1`

---

## Florian the Flea

### Drain Attack (`BasicDrainMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 5+bonus_melee_damage, Leech 1`

---

## Fly

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Fly Swarm

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### FormShrinkFour (`FormShrinkFour`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form 4`

### FormShrinkOne (`FormShrinkOne`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form 1`

### FormShrinkThree (`FormShrinkThree`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form 3`

### FormShrinkTwo (`FormShrinkTwo`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form 2`

---

## Fountain

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Frank

### Suck (`KirbySuck`)

- **Template:** `straightshot_attack`
- **Cost:** `mana 0, must_not_be_consuming true`
- **Target/Shape:** `max_aoe 10, knockback_mode none`
- **Damage/Effects:** `type none, damage 0, cant_miss true, layer characters, wet true, struggle_ability Thrash`

---

## Frank's Bean

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Fuzzer

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### FuzzerJump (`FuzzerJump`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### FuzzerJump_post (`FuzzerJump_post`)

- **Template:** `*(None)*`
- **Cost:** `move_points 0, cantrip true`
- **Target/Shape:** `min_range 3, max_range 5, target_mode random_tile`
- **Damage/Effects:** `ai_base_score 999`

### FuzzerReact (`FuzzerReact`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 5`

---

## Fötusjar

### Fury Swipes (`FurySwipes_Enemy`)

- **Template:** `melee_attack`
- **Cost:** `mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 2+bonus_melee_damage, type melee`

---

## Führerfötus

### Führer Swipes (`FurySwipes_Hitler`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### HitlerCloneHeil (`HitlerCloneHeil`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `SpeedUp 1, DamageUp 1`

### HitlerCloneLick (`HitlerCloneLick`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 7, Cleanse 0`

### HitlerCloneTransform (`HitlerCloneTransform`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `FormChange Grown, Cleanse 0, InstantMaxHealthUp 20, FullHeal 1, FaceCamera 1`

---

## G-Alien

### Counterspell (`GA_Counterspell`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Counterspell 1, EndTurn 1`

### Prime Blast (`GA_Megablast`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode circle, min_aoe 0, max_aoe 20, aoe_excludes_self true, aoe_considers_character_size true, aoe_restrictions [enemies_only]`
- **Damage/Effects:** `damage 2+bonus_basic_spell_damage, knockback 10, Confusion 1`

### GA_PrimeExplode (`GA_PrimeExplode`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode character_to_tile, aoe_considers_character_size true, aoe_mode circle, target_mode none, min_range 0, max_range 0, min_aoe 0, max_aoe 1`
- **Damage/Effects:** `damage 7, knockback 1, IgnoreSelf true`

### GA_Suggest (`GA_Suggest`)

- **Template:** `targeted_status`
- **Cost:** `cantrip true`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `damage 0, type status_spell, TakeExtraTurn 1`

### GA_Telekinesis (`GA_Telekinesis`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 0, max_range 20, knockback_mode character_to_target, restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 1+bonus_basic_spell_damage, knockback 3`

---

## Gamete

### GametePop (`GametePop`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, min_range 0, max_range 0, min_aoe 1, max_aoe 1`
- **Damage/Effects:** `damage 1, knockback 2, IgnoreSelf true`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Gas Can

### GasCanExplode (`GasCanExplode`)

- **Template:** `spell`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode cross, knockback_mode character_to_tile, target_mode none, min_range 0, max_range 0, min_aoe 0, max_aoe 1`
- **Damage/Effects:** `damage 10, elements [, Fire, Napalm, Explosion, ], ai_base_score 9999`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Gas Cloud

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Gasper

### SpawnGas (`SpawnGas`)

- **Template:** `spawn`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### SpawnGasAOE (`SpawnGasAOE`)

- **Template:** `spawn`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode none, max_aoe 1, prioritize_dont_change_direction true`
- **Damage/Effects:** `None`

### ToxGasBlast (`ToxGasBlast`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode back_orientation, target_mode direction, min_aoe 0, max_aoe 1, aoe_mode line`
- **Damage/Effects:** `None`

---

## Gasser

### GasserExplode (`GasserExplode`)

- **Template:** `spell`
- **Cost:** `mana 5`
- **Target/Shape:** `knockback_mode character_to_tile, target_mode none, min_range 0, max_range 0, min_aoe 1, max_aoe 2`
- **Damage/Effects:** `damage 5, knockback 1, object GasCloud`

### SpawnGas (`SpawnGas`)

- **Template:** `spawn`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Gassy

### GasBlast (`GasBlast`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode back_orientation, aoe_mode custom, custom_aoe [ [-1, 0] ]`
- **Damage/Effects:** `damage 0, type spell, Poison 3, VisualFXTile PoisonPoof`

---

## Gatekeeper

### GKLeap (`GKLeap`)

- **Template:** `jump_move`
- **Cost:** `cantrip true`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `None`

### GKSpawn (`GKSpawn`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

### Absorb Soul (`GKSuck`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode tile_to_character, restrictions must_have_character`
- **Damage/Effects:** `damage 0, makes_contact false, Die 1, PermanentConstitution -2, ConstitutionUp 2, HealthGain 8`

---

## GeoLad

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Quake Jump (`QuakeJump`)

- **Template:** `jump_attack`
- **Cost:** `act_points 1`
- **Target/Shape:** `min_range 1, max_range 3, max_aoe 2, aoe_mode standard`
- **Damage/Effects:** `damage 4+bonus_melee_damage, knockback 1, IgnoreSelf 1`

---

## Glass Spitter

### Spit Glass (`SpitGlass`)

- **Template:** `lobbed_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `min_range 1, max_range 5, max_aoe 1, max_targets 2`
- **Damage/Effects:** `damage 2+bonus_ranged_damage, tile GlassTile`

---

## Glowing Mushroom

### GlowingMushroomGiveMana (`GlowingMushroomGiveMana`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, max_aoe 3, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, cant_miss true, ManaGain 1`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## GlowingMushroom2

### GlowingMushroomGiveMana2 (`GlowingMushroomGiveMana2`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 1, cant_miss true, ManaGain 1`

---

## Golem

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Gorger

### GorgerGorge (`GorgerGorge`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode custom, aoe_symmetry none, custom_aoe [[2, 0]], aoe_considers_character_size false`
- **Damage/Effects:** `type melee, damage 0, piercing true, cant_miss true, Vaporize 20, FlatLeech 10`

### GorgerRun (`GorgerRun`)

- **Template:** `move`
- **Cost:** `act_points 1, move_points 1`
- **Target/Shape:** `max_range 6`
- **Damage/Effects:** `None`

---

## Grave Worm

### Lobbed Shot (`BasicRanged`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `damage 4+bonus_ranged_damage`

### Teleport (`Teleport`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Grenade

### GrenadeExplode (`GrenadeExplode`)

- **Template:** `spell`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode standard, knockback_mode character_to_tile, target_mode none, min_range 0, max_range 0, min_aoe 0, max_aoe 2`
- **Damage/Effects:** `damage 12, PartialPurge 1, PartialPurge 1, PartialPurge 1, PartialPurge 1, PartialPurge 1`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Grey Alien

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Großerbot

### Blitzkrieg (`TallBotRocket`)

- **Template:** `spell`
- **Cost:** `cantrip true, prime 1`
- **Target/Shape:** `max_aoe 2, min_range 1, max_range 20`
- **Damage/Effects:** `damage 8, elements [, Fire, Explosion, ]`

### Bewegen (`TallBotSuplex`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode zero, aoe_considers_character_size false, target_mode tile, restrictions [aoe_must_be_displaceable must_have_character], range_mode standard, aoe_mode standard, min_range 1, max_range 1, min_aoe 0, max_aoe 0`
- **Damage/Effects:** `damage 3+bonus_melee_ability_damage, type melee, blocked_multiplier 2, makes_contact false, Stun [1 .5], Immobile [1 .5]`

---

## Grub

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### set_GrubFamiliarReturn (`set_GrubFamiliarReturn`)

- **Template:** `targeted_status`
- **Cost:** `mana 0, move_points 0, act_points 1`
- **Target/Shape:** `min_range 1, max_range 1, range_mode cross, restrictions [must_have_buddy must_have_living_character]`
- **Damage/Effects:** `damage 0, type status_spell, GenericBuff 100, GiveBoundItemToTarget 1`

---

## Guillotina

### Belly Pound (`BellyPound`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, knockback_mode none`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, contact_requires_adjacency false, ai_base_score 9999`

### Digest (`Digest`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, knockback_mode none`
- **Damage/Effects:** `damage 0, type melee, cant_miss true, ai_base_score 9999, Vaporize 1`

### G3CallForHelp (`G3CallForHelp`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode all`
- **Damage/Effects:** `damage 0, type status_spell, cant_miss true, form Normal, ability G3GrabHead, even_if_cant_reach true`

### Cough (`G3CoughFly`)

- **Template:** `spawn`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode direction, aoe_mode line, max_aoe 1, aoe_considers_character_size false, aoe_excludes_self true, aoe_mode line, min_aoe 1, max_aoe 1, aoe_restrictions none, redirect_location_if_blocked true`
- **Damage/Effects:** `None`

### G3GrabHead (`G3GrabHead`)

- **Template:** `targeted_status`
- **Cost:** `mana 0, must_not_be_consuming true`
- **Target/Shape:** `max_range 1, range_mode cross`
- **Damage/Effects:** `type none, damage 0, cant_miss true, force_contact true, instant true`

### Prison (`G3PrisonSpit`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 5, restrictions none`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, Imprison Tumor, Poison 1`

### G3RageShake (`G3RageShake`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Head Charge (`G3RunToHead`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `max_range mov`
- **Damage/Effects:** `None`

### Shriek (`G3Scream_Hex`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, aoe_excludes_self true, prioritize_face_camera true`
- **Damage/Effects:** `damage 0, ai_base_score 9999, Hex 1, Poison 1`

### Shake (`G3Shake`)

- **Template:** `spawn`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, max_aoe 2, aoe_considers_character_size true, aoe_excludes_self true, max_targets 1`
- **Damage/Effects:** `None`

### G3SpawnMama (`G3SpawnMama`)

- **Template:** `spawn`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 5, aoe_mode custom, dont_orient_aoe true, custom_aoe [[0 0] [1 0] [0 1] [1 1]], range_excludes_blocking false, restrictions aoe_must_be_displaceable, aoe_restrictions none, range_display_include_aoe true, mouse_offset [.5 .5]`
- **Damage/Effects:** `None`

### Toss (`G3TossHead`)

- **Template:** `throw_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 20, restrictions none, damage_collided_only true, throw_consumed_character true, always_bounce true, reorient_thrown_character true`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, Bruise 1`

### Guillotina1Rage (`Guillotina1Rage`)

- **Template:** `self_buff`
- **Cost:** `requires_hp_threshold 200`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 50, form Rage`

### Guillotina2Rage (`Guillotina2Rage`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 100, form Rage`

### Toss (`GuillotinaTossCollide`)

- **Template:** `throw_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 7, restrictions none`
- **Damage/Effects:** `damage 1, blocked_damage 5+bonus_melee_ability_damage, custom_additional_ai_weight toss_far`

### Gasp (`Magnetize`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [, [1, 1], [2, 1], [3, 1], [4, 1], [5, 1], [6, 1], [7, 1], [8, 1], [9, 1], [10, 1], [1, 0], [2, 0], [3, 0], [4, 0], [5, 0], [6, 0], [7, 0], [8, 0], [9, 0], [10, 0], [1,-1], [2,-1], [3,-1], [4,-1], [5,-1], [6,-1], [7,-1], [8,-1], [9,-1], [10,-1], ], knockback_mode perp_towards_facing_middle_pull`
- **Damage/Effects:** `damage 0, knockback 1, custom_additional_ai_weight magnetize_favorlineup, elements [, Wind, ]`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Call (`Tina2Call`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `max_aoe 0, max_range 20, knockback_mode pull_to_character, restrictions must_have_buddy`
- **Damage/Effects:** `damage 0`

### TinaBasicBigMelee (`TinaBasicBigMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1`
- **Damage/Effects:** `knockback 10`

### TinaBasicJump (`TinaBasicJump`)

- **Template:** `jump_attack`
- **Cost:** `move_points 1, act_points 0`
- **Target/Shape:** `max_range mov, min_range 1, range_considers_character_size false, range_display_include_character_size true, aoe_considers_character_size false, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, restrictions must_be_moveable`
- **Damage/Effects:** `type none, damage 0`

### TinaBodySlam (`TinaBodySlam`)

- **Template:** `jump_attack`
- **Cost:** `act_points 1`
- **Target/Shape:** `max_range 2, min_range 1, range_mode cross, range_considers_character_size false, min_aoe 0, max_aoe 0`
- **Damage/Effects:** `type melee, damage 5+bonus_melee_damage, knockback 10, IgnoreSelf 1, Bruise 1, Stun [1 .5]`

### TinaBodySlamMax (`TinaBodySlamMax`)

- **Template:** `jump_attack`
- **Cost:** `act_points 1`
- **Target/Shape:** `max_range 2, min_range 2, range_mode cross, range_considers_character_size false, min_aoe 0, max_aoe 0`
- **Damage/Effects:** `type melee, damage 5+bonus_melee_damage, knockback 10, IgnoreSelf 1, Bruise 1, Stun [1 .5]`

### TinaBodySlamRage (`TinaBodySlamRage`)

- **Template:** `jump_attack`
- **Cost:** `act_points 1`
- **Target/Shape:** `max_range 3, min_range 1, range_considers_character_size false, min_aoe 0, max_aoe 0`
- **Damage/Effects:** `type melee, damage 5+bonus_melee_damage, knockback 10, IgnoreSelf 1, Bruise 1, Stun [1 .5]`

### TinaHeadGutSpear (`TinaHeadGutSpear`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_aoe 4`
- **Damage/Effects:** `damage 5+bonus_melee_damage, contact_requires_adjacency false`

### TinaJumpAttack (`TinaJumpAttack`)

- **Template:** `jump_attack`
- **Cost:** `act_points 1`
- **Target/Shape:** `max_range 3, min_range 1, range_considers_character_size false, min_aoe 0, max_aoe 0`
- **Damage/Effects:** `type melee, damage 5+bonus_melee_damage, knockback 4, IgnoreSelf 1, Bruise 1`

### Spit (`TinaSpit`)

- **Template:** `throw_attack`
- **Cost:** `mana 0, must_be_consuming true`
- **Target/Shape:** `max_range 5, min_range 3, range_mode cross, restrictions none, prioritize_dont_change_direction true, throw_consumed_character true`
- **Damage/Effects:** `damage 1, blocked_damage 5+bonus_melee_ability_damage, ai_base_score 9999, custom_additional_ai_weight toss_far`

### Spit (`TinaSpit2`)

- **Template:** `throw_attack`
- **Cost:** `mana 0, must_be_consuming true`
- **Target/Shape:** `max_range 5, min_range 3, restrictions none, throw_consumed_character true, prioritize_dont_change_direction true, range_mode cross`
- **Damage/Effects:** `damage 1, blocked_damage 5+bonus_melee_ability_damage, ai_base_score 9999`

### TinaSuck (`TinaSuck`)

- **Template:** `targeted_status`
- **Cost:** `mana 0, must_not_be_consuming true`
- **Target/Shape:** `max_range 20, range_mode cross, restrictions must_have_line_of_sight`
- **Damage/Effects:** `type none, damage 0, cant_miss true, layer characters, struggle_ability TinaFlail, force_contact true, wet true`

### TinaSuck2 (`TinaSuck2`)

- **Template:** `targeted_status`
- **Cost:** `mana 0, must_not_be_consuming true`
- **Target/Shape:** `max_range 20, restrictions must_have_line_of_sight`
- **Damage/Effects:** `type none, damage 0, cant_miss true, layer characters, struggle_ability TinaFlailRage, force_contact true, wet true`

### Tantrum (`TinaTantrum`)

- **Template:** `spawn`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, aoe_mode square, max_aoe 20, max_targets 15, multihit 5, stagger_multihit_targets true`
- **Damage/Effects:** `None`

### Toss (`TinaThrow`)

- **Template:** `throw_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 20, restrictions must_be_empty`
- **Damage/Effects:** `damage 5+bonus_melee_damage, custom_additional_ai_weight toss_far`

### Toss (`YeetTowardsBuddy`)

- **Template:** `throw_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 7, restrictions none`
- **Damage/Effects:** `damage 1, blocked_damage 5+bonus_melee_ability_damage, custom_additional_ai_weight toss_towards_buddy`

---

## Gun

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Half-Dog

### NubsCatJumpReaction (`NubsCatJumpReaction`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `range_mode cross, min_range 0, max_range 2, aoe_mode square`
- **Damage/Effects:** `None`

### Nub Flub (`NubsJump`)

- **Template:** `jump_attack`
- **Cost:** `act_points 1`
- **Target/Shape:** `min_range 2, max_range 2, aoe_mode square`
- **Damage/Effects:** `damage 4+bonus_melee_damage, knockback 1, IgnoreSelf 1`

---

## Half-Rat

### Chain Dash (`ChainDash`)

- **Template:** `dash_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1`

---

## Harpoon Trap

### HarpoonTrapPull (`HarpoonTrapPull`)

- **Template:** `straightshot_attack`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `max_range 10, knockback_mode pull_to_character`
- **Damage/Effects:** `damage 5+bonus_ranged_damage`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Headless

### CatGoop (`CatGoop`)

- **Template:** `straightshot_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_aoe 10`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, Poison 2`

### Big Spin (`CatSpin`)

- **Template:** `melee_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode square, knockback_mode character_to_tile`
- **Damage/Effects:** `damage 5+bonus_melee_damage`

---

## Hell Hand

### HellHandGrab (`HellHandGrab`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type melee, cant_miss true, Grappled 1`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Hemlock

### HemBounce (`HemBounce`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode cross, knockback_mode character_to_tile`
- **Damage/Effects:** `damage 0, type melee, knockback 3, makes_contact true`

### HemDeathPop (`HemDeathPop`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode random_closest_tile, recalc_target_on_castpoint true, min_range 1, max_range 20, restrictions [must_have_enemy must_have_living_character]`
- **Damage/Effects:** `Possessed 1, Poison 1`

### Healing Gas (`HemHeal`)

- **Template:** `melee_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `target_mode none, aoe_mode cross, knockback_mode character_to_tile, multihit 3`
- **Damage/Effects:** `heal 1+bonus_basic_spell_damage, type spell, makes_contact false`

### HemShot (`HemShot`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 3, restrictions [must_have_enemy must_have_living_character]`
- **Damage/Effects:** `damage 1+bonus_ranged_damage, Poison 1`

---

## Herald

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### ShadeDuplicate (`ShadeDuplicate`)

- **Template:** `spawn`
- **Cost:** `cantrip true`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

### Teleport (`Teleport`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Herald's Shadow

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Teleport (`Teleport`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Heraldess

### GSClosedAttack (`GSClosedAttack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `knockback 10, Bleed 1`

### GSOpen (`GSOpen`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `FormChange Open`

### GSScream (`GSScream`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode circle, max_aoe 3, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, ai_base_score 999999, Fear 1`

### GSSuck (`GSSuck`)

- **Template:** `straightshot_attack`
- **Cost:** `mana 0, must_not_be_consuming true`
- **Target/Shape:** `max_aoe 10, knockback_mode none, aoe_restrictions must_have_cat`
- **Damage/Effects:** `type none, damage 0, cant_miss true, layer characters, mount_mode true, struggle_ability Thrash`

---

## Horny Cat

### HornyToadShot (`HornyToadShot`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Blind 1`

---

## Host

### HostShove (`HostShove`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 2`

### Spit (`HostSpit`)

- **Template:** `straightshot_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode custom, custom_aoe [[1, 1] [1, 0] [1,-1]]`
- **Damage/Effects:** `damage 4+bonus_ranged_damage`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Hot Poker

### PokerAttack (`PokerAttack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 4+bonus_melee_damage, Immobile 1, RefreshMovePointsIfHit 1`

### Hot Poke (`PokerPokeAlly`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `restrictions [must_not_have_tag must_have_ally], target_requires_tag poker`
- **Damage/Effects:** `damage 1+bonus_melee_damage, ai_base_score 99999, Burn 1, TakeExtraTurn 1`

### Hot Poke (`PokerPokeCat`)

- **Template:** `melee_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1+bonus_melee_damage, knockback 10, Burn 1, KnockbackDirectionIsFacingDirection 1`

---

## HumanCat

### HCAttack (`HCAttack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1, Immobile 1`

### HCHumanDie (`HCHumanDie`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 999, form "HumanDead"`

---

## Husk

### HuskSwipes (`HuskSwipes`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `multihit X, X_is custom`
- **Damage/Effects:** `damage 3+bonus_melee_damage`

---

## Hyde

### Fury Swipes (`FurySwipes_Enemy`)

- **Template:** `melee_attack`
- **Cost:** `mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 2+bonus_melee_damage, type melee`

---

## Hängenbot

### HangerBotAttack (`HangerBotAttack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 3+bonus_basic_spell_damage, type spell, makes_contact false, ShortCircuit 1`

### HangerBotLeave (`HangerBotLeave`)

- **Template:** `leave`
- **Cost:** `move_points 1, act_points 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 100`

### HangerBotReturn (`HangerBotReturn`)

- **Template:** `return`
- **Cost:** `move_points 1, act_points 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 100`

### HangerBotSpawn (`HangerBotSpawn`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

### Teleport (`Teleport`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Ice Cube

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Infested

### ParasiteShot (`ParasiteShot`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 2, max_range 3, restrictions none`
- **Damage/Effects:** `chance .15, pool parasites`

---

## Infested Kitten

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Isaac

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Jack

### JackAttack (`JackAttack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, knockback 1`

### Protect (`JackShield`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 2, max_range 6`
- **Damage/Effects:** `heal 0, Shield 5`

---

## Jekyll

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Jersey Devil

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Junk

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Katzebot

### FutureBotPunch (`FutureBotPunch`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 10+bonus_melee_damage, type melee`

### Ausführen (`FutureBotPunchAggro`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `restrictions aoe_must_exist, aoe_restrictions must_have_aggro_target`
- **Damage/Effects:** `None`

### Bewegen (`FutureBotSuplex`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode zero, aoe_considers_character_size false, target_mode tile, restrictions [aoe_must_be_displaceable must_have_character], range_mode standard, aoe_mode standard, min_range 1, max_range 1, min_aoe 0, max_aoe 0`
- **Damage/Effects:** `damage 3+bonus_melee_ability_damage, type melee, blocked_multiplier 2, makes_contact false`

---

## Killdozer

### Killdoze (`KillDoze`)

- **Template:** `trample_dash`
- **Cost:** `Free`
- **Target/Shape:** `max_range 2`
- **Damage/Effects:** `damage 3+bonus_melee_damage`

### MoveOne (`MoveOne`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

---

## Kitten

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Korbee

### Suck (`KirbySuck`)

- **Template:** `straightshot_attack`
- **Cost:** `mana 0, must_not_be_consuming true`
- **Target/Shape:** `max_aoe 10, knockback_mode none`
- **Damage/Effects:** `type none, damage 0, cant_miss true, layer characters, wet true, struggle_ability Thrash`

---

## Krughead

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Befehl (`JarHeadOrder`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, TakeExtraTurn 1`

---

## Leaper

### Rat Leap (`RatLeap`)

- **Template:** `jump_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 3`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1`

---

## Lil' Rat

### Dash (`Dash_Enemy`)

- **Template:** `dash_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1`

---

## Loan Shark

### SharkDash (`SharkDash`)

- **Template:** `dash_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `max_range 2`
- **Damage/Effects:** `damage 5+bonus_melee_damage, Bleed 1`

---

## Louse

### LiceBite (`LiceBite`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Bruise 1`

---

## Love Bot

### Feel Bad Drugs (`LoveBotCounter`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 4+bonus_melee_damage, RandomStatDown 1, Bleed 1, Bleed 1, Bleed 1, Poison 1, Poison 1, Poison 1, Slow 1, Slow 1, Slow 1, Stun 1, Madness 1`

### Feel Good Drugs (`LoveBotHeal`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `restrictions [must_not_have_tag], target_requires_tag robot`
- **Damage/Effects:** `heal 4+bonus_melee_damage, SpeedUp 1, stack_scale 0, TakeExtraTurn 1`

---

## Lumpy

### CreepRanged (`CreepRanged`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 3, restrictions none`
- **Damage/Effects:** `SpawnCreep 1`

---

## Mad Lad

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Maelestes

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### MaelestesPickup (`MaelestesPickup`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `restrictions [must_have_tag], target_requires_tag pickup`
- **Damage/Effects:** `layer pickups, damage 0, CollectsPickups 1`

### MaelestesSteal (`MaelestesSteal`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `StealEquipment any`

---

## Maggot

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Mammoth Kitten

### MammothBabyStomp (`MammothBabyStomp`)

- **Template:** `melee_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode none, aoe_mode cross, min_aoe 0, knockback_mode character_to_tile, aoe_excludes_self false, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1, IgnoreSelf 1, Bruise 1, time .5, intensity 3`

### MammothBabyThrow (`MammothBabyThrow`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, stacks 3, distance 3`

---

## Mangy

### PoisonShot (`PoisonShot`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 2, max_range 3, restrictions none`
- **Damage/Effects:** `Poison [1, .25]`

---

## Meat Minion

### MeatMinionMelee (`MeatMinionMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, elements [, dont_break_tentacles, ]`

---

## Meat Slime

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Mech Suit

### Barrage (`MechSuitBarrage`)

- **Template:** `straightshot_attack`
- **Cost:** `mana 5, must_be_consuming true, infcantrip true`
- **Target/Shape:** `target_mode direction, max_aoe 10, min_aoe 1, multihit 6, stagger_multihit_targets true, aoe_mode custom, custom_aoe      [[1  0] [1  0]  [1, 0] [1, 0]  [1, 0] [1, 0]], custom_aoe_util [[1, 0] [1, 1]  [1, 0] [1, 1]  [1, 0] [1, 1]], custom_aoe_mirror      [[1  0] [1  0]  [1, 0] [1, 0]  [1, 0] [1, 0]], custom_aoe_util_mirror [[1, 1] [1, 0]  [1, 1] [1, 0]  [1, 1] [1, 0]], mirror_custom_aoe true`
- **Damage/Effects:** `damage 4+bonus_ranged_damage, elements [, Fire, Explosion, ]`

### Thrusters (`MechSuitDash`)

- **Template:** `trample_dash`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 3+bonus_melee_damage`

### Eject! (`MechSuitEject`)

- **Template:** `throw_attack`
- **Cost:** `mana 3, must_be_consuming true, infcantrip true`
- **Target/Shape:** `max_range 5, min_range 3, restrictions none, throw_consumed_character true`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, blocked_damage 5+bonus_melee_ability_damage, custom_additional_ai_weight toss_far, EndTurn 1`

### Mech Punch (`MechSuitPunch`)

- **Template:** `dash_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1+bonus_range, max_aoe 1+bonus_melee_range`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 3`

---

## Mega Fetus

### MegafetusMelee (`MegafetusMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_considers_character_size false, aoe_rotate_around_character_center true, aoe_mode custom, custom_aoe [[2, 1] [3, 1]]`
- **Damage/Effects:** `damage 8+bonus_melee_damage, contact_requires_adjacency false, time .5, intensity 3`

### Spin (`MegafetusSpin`)

- **Template:** `melee_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode square, knockback_mode character_to_tile`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1`

---

## Mega Mutant

### MM_Grab (`MM_Grab`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode tile_to_character, restrictions must_have_character, aoe_considers_character_size false`
- **Damage/Effects:** `damage 0, DieViolently 1`

### MM_Guard (`MM_Guard`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 999999, form "Guarding"`

### Quake (`MM_Quake`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode line, aoe_considers_character_size true, aoe_excludes_self true, min_aoe 1, max_aoe 10, aoe_leading_edge_only true`
- **Damage/Effects:** `damage 2, SpawnRock [1, .20], Petrify [1, .1]`

### MM_Slap (`MM_Slap`)

- **Template:** `melee_attack`
- **Cost:** `cantrip true, mana 0`
- **Target/Shape:** `max_aoe 1`
- **Damage/Effects:** `damage 1+bonus_melee_damage, knockback 10`

### MM_Unguard (`MM_Unguard`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `prioritize_dont_change_direction true`
- **Damage/Effects:** `ai_base_score 999999, form "Default"`

---

## Mega Tumor

### Tumor Dash (`TumorDash`)

- **Template:** `trample_dash`
- **Cost:** `mana 5`
- **Target/Shape:** `max_range mov, allow_any_orientation true`
- **Damage/Effects:** `damage 6+bonus_melee_damage, Bruise 1, Immobile 1`

### TumorPowerup (`TumorPowerup`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Cleanse 1, MovementUp 1`

---

## Megasaucer

### M-Shield (`UFO_BigShield`)

- **Template:** `self_buff`
- **Cost:** `act_points 1`
- **Target/Shape:** `Default`
- **Damage/Effects:** `DivineShield 2`

### M-Dash (`UFO_Dash`)

- **Template:** `trample_dash`
- **Cost:** `act_points 1`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 4+bonus_melee_damage, Stun 1`

### Annihilaser (`UFO_Megalaser`)

- **Template:** `spell`
- **Cost:** `prime 1, act_points 1`
- **Target/Shape:** `target_mode direction, aoe_mode line, aoe_considers_character_size true, max_aoe 10, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, OverrideDamage 25`

### Beam In (`UFO_Summon`)

- **Template:** `spawn`
- **Cost:** `act_points 1`
- **Target/Shape:** `max_range 5`
- **Damage/Effects:** `None`

---

## Mini Nuke

### MiniNukeExplodey (`MiniNukeExplodey`)

- **Template:** `spell`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode standard, knockback_mode character_to_tile, aoe_restrictions must_have_piercing_line_of_sight, target_mode none, min_range 0, max_range 0, min_aoe 0, max_aoe 3`
- **Damage/Effects:** `damage 7, knockback 1, elements [, Explosion, Mutate, ]`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Mini Volcano

### MiniVolcano_Spurt (`MiniVolcano_Spurt`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `range_mode 8cross, min_range 0, max_range 2`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, obj SmallLavaRock, slide 10`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Moon Worm

### MoonWormCurl (`MoonWormCurl`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Brace 1`

### MoonWormShot (`MoonWormShot`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, min_aoe 1, max_aoe 1, aoe_restrictions [enemies_only]`
- **Damage/Effects:** `damage 2+bonus_ranged_damage`

### Teleport (`Teleport`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Moth

### Short Lobbed Shot (`BasicShortLobbed`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 3+bonus_range`
- **Damage/Effects:** `None`

### Flutter (`CrowFlutter`)

- **Template:** `move`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 3, max_range 3, straight_shot true, as_the_crow_flies true, range_mode normal`
- **Damage/Effects:** `None`

### Sleep Powder (`SleepPowder`)

- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `min_range 1, max_range 3, max_aoe 0`
- **Damage/Effects:** `damage 0, type status_spell, Sleep 1`

---

## Mothman

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Multicat

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Mummified Mangy

### PoisonShot (`PoisonShot`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 2, max_range 3, restrictions none`
- **Damage/Effects:** `Poison [1, .25]`

---

## Nessie

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Nettle

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Thorn Up (`ThornUp`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Thorns 1, RandomMagicMissile 1`

---

## Neutron Star

### BHoleSuck (`BHoleSuck`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, min_aoe 0, max_aoe 20, aoe_excludes_self true, aoe_considers_character_size true, knockback_mode tile_to_character`
- **Damage/Effects:** `damage 0, knockback 1, hint_dont_lowgravboost true, ai_base_score 999999`

### NeutronExplode (`NeutronExplode`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode all, target_mode none, aoe_excludes_self true, aoe_restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 10, ai_base_score 999999, Blind 1`

### NeutronRumble (`NeutronRumble`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 999999`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Nothing

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Nurse Bot

### Give drugs! (`NurseBotHeal`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 5+bonus_melee_damage`

### NurseBotHealCat (`NurseBotHealCat`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `restrictions [must_not_have_tag], target_requires_tag robot`
- **Damage/Effects:** `None`

---

## Parasaurolophus

### Parasaurolophus_Push (`Parasaurolophus_Push`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, element Water, BonusCritChance 100`

### Parasaurolophus_Throw (`Parasaurolophus_Throw`)

- **Template:** `throw_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 4, restrictions [must_be_empty aoe_must_exist], aoe_restrictions [tile_must_have_element], aoe_tile_requires_element Water`
- **Damage/Effects:** `damage 3+bonus_melee_damage, custom_additional_ai_weight toss_far`

---

## Peashy

### Nail Throw (`BasicStraightShot`)

- **Template:** `straightshot_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 3+bonus_range`
- **Damage/Effects:** `damage 5+bonus_ranged_damage`

### GenericRage (`GenericRage`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "Rage"`

### PeashyStab (`PeashyStab`)

- **Template:** `melee_attack`
- **Cost:** `act_points 1`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 3+bonus_melee_damage, crit_chance 25%, Bleed 3`

---

## Peeper

### BloatEyeMovement2 (`BloatEyeMovement2`)

- **Template:** `move`
- **Cost:** `mana 0`
- **Target/Shape:** `range_mode 8cross, max_range 1, restrictions [must_be_moveable must_move], straight_shot true, allow_diagonals true`
- **Damage/Effects:** `damage 3+bonus_melee_ability_damage, override_trample_damage true, tag bloateye, stacks 20, min_dist 4`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Pet Boulder

### AnimatedRockAttack (`AnimatedRockAttack`)

- **Template:** `self_buff`
- **Cost:** `move_points 0, act_points 1`
- **Target/Shape:** `target_mode direction8, knockback_mode orientation, dont_orient_aoe true`
- **Damage/Effects:** `type melee, damage 0, knockback 10`

---

## Pet Rock

### AnimatedRockAttack (`AnimatedRockAttack`)

- **Template:** `self_buff`
- **Cost:** `move_points 0, act_points 1`
- **Target/Shape:** `target_mode direction8, knockback_mode orientation, dont_orient_aoe true`
- **Damage/Effects:** `type melee, damage 0, knockback 10`

---

## Phantom Mask

### AnimatedRockAttack (`AnimatedRockAttack`)

- **Template:** `self_buff`
- **Cost:** `move_points 0, act_points 1`
- **Target/Shape:** `target_mode direction8, knockback_mode orientation, dont_orient_aoe true`
- **Damage/Effects:** `type melee, damage 0, knockback 10`

---

## Phylactery

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Pig

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Pile

### DipShot (`DipShot`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 2, max_range 7+bonus_range`
- **Damage/Effects:** `damage 2+bonus_ranged_damage, BounceObject Dip`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Spawn Dip (`SpawnDip`)

- **Template:** `spawn`
- **Cost:** `mana 0, charge 0`
- **Target/Shape:** `min_range 1, max_range 1`
- **Damage/Effects:** `None`

---

## Pill Tube

### LabPillarDrop (`LabPillarDrop`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, min_aoe 1, max_aoe 2, min_targets 3, max_targets 5, aoe_restrictions none, knockback_mode zero`
- **Damage/Effects:** `damage 5`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### SpawnSpewerPill (`SpawnSpewerPill`)

- **Template:** `spawn`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode random_tile, min_range 3, max_range 6`
- **Damage/Effects:** `None`

---

## Pinky

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Poop

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Poop Cat

### PoopCatMelee (`PoopCatMelee`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode tile_to_character, aoe_considers_character_size false, target_mode tile, restrictions must_have_character, range_mode standard, aoe_mode standard, min_range 1, max_range 1, min_aoe 0, max_aoe 0`
- **Damage/Effects:** `damage 1+bonus_melee_damage, Poison 3, Slow 1`

---

## Pooter

### Short Lobbed Shot (`BasicShortLobbed`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 3+bonus_range`
- **Damage/Effects:** `None`

---

## Popeye

### Dash (`PopeyeDash`)

- **Template:** `dash_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `max_range 2`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 5`

---

## Porcupine

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Prehistoric Pooter

### PrehistoricPooterShot (`PrehistoricPooterShot`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 2+bonus_range`
- **Damage/Effects:** `knockback 3, Stun 1`

---

## Pterodactyl

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### PteroEscape (`PteroEscape`)

- **Template:** `throw_attack`
- **Cost:** `mana 0, must_be_consuming true`
- **Target/Shape:** `max_range 4, min_range 1, restrictions none, throw_consumed_character true, prioritize_dont_change_direction true, reorient_thrown_character true, range_mode cross`
- **Damage/Effects:** `damage 0, blocked_damage 5, ai_base_score 9999`

### PteroGrab (`PteroGrab`)

- **Template:** `targeted_status`
- **Cost:** `mana 0, must_not_be_consuming true`
- **Target/Shape:** `max_range 1, range_mode cross, restrictions [must_have_cat must_have_living_character]`
- **Damage/Effects:** `type none, damage 0, cant_miss true, layer characters, RefreshMovePointsIfHit 1, instant true, mount_mode true, force_contact true, drop_on_death true, drop_on_self_death true, do_not_pop_corpse true, struggle_ability PteroTryEscape`

---

## Punching Bag

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Rager

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Rage Up (`RageUp`)

- **Template:** `self_buff`
- **Cost:** `cantrip true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `StrengthUp 5`

---

## Raptor

### Fury Swipes (`FurySwipes_Enemy`)

- **Template:** `melee_attack`
- **Cost:** `mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 2+bonus_melee_damage, type melee`

---

## Raptor Kitten

### DoubleDistanceMove (`DoubleDistanceMove`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `max_range mov*2`
- **Damage/Effects:** `None`

### RaptorBabyBite (`RaptorBabyBite`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, Bleed 1, RefreshMovePointsIfHit 1`

---

## Rat Bomb

### BombExplode (`BombExplode`)

- **Template:** `spell`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode pierce_cross, knockback_mode character_to_tile, target_mode none, min_range 0, max_range 0, min_aoe 0, max_aoe 10`
- **Damage/Effects:** `damage 10, elements [, Fire, Explosion, ], ai_base_score 9999`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Rattlesnek

### Poison Attack (`RattleSnakeAttack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, Poison 1`

### Poison Attack (`RattleSnakeTrap`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, Poison 1`

---

## Reaper

### Move (`FloatMove`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `as_the_crow_flies true`
- **Damage/Effects:** `None`

### ReaperRevenge (`ReaperRevenge`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `None`

### Spin (`ReaperSpin`)

- **Template:** `melee_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode square, knockback_mode character_to_tile, multihit 3, max_aoe 1`
- **Damage/Effects:** `damage 4+bonus_melee_damage`

---

## Robes

### Leeches (`HexShot`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 20, restrictions none`
- **Damage/Effects:** `damage 0, Leeches 1`

### Spawn Wisp (`SpawnWisp`)

- **Template:** `spawn`
- **Cost:** `cantrip true`
- **Target/Shape:** `max_range 2`
- **Damage/Effects:** `None`

---

## Robo-Cat

### WideSwipe (`WideSwipe`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode custom, aoe_symmetry none, custom_aoe [[1, -1] [1, 0] [1, 1]]`
- **Damage/Effects:** `None`

---

## Robo-Vac

### Roomba_Bump (`Roomba_Bump`)

- **Template:** `dash_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1, max_aoe 1`
- **Damage/Effects:** `damage 5+bonus_melee_damage`

---

## Rock

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Rock Head

### Big Spin (`CatSpin`)

- **Template:** `melee_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode square, knockback_mode character_to_tile`
- **Damage/Effects:** `damage 5+bonus_melee_damage`

### Trample Dash (`SmallTrampleDash`)

- **Template:** `trample_dash`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 4+bonus_melee_damage`

---

## Rocket Turret

### RocketTurretShot (`RocketTurretShot`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 6, min_aoe 0, max_aoe 1`
- **Damage/Effects:** `damage 5, knockback 1, elements [, Fire, Explosion, ]`

---

## Rover

### Chain Dash (`RoverDash`)

- **Template:** `dash_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 4+bonus_melee_damage, knockback 1, damage 1, type generic_physical`

---

## Rubber Fist Bot

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### RubberFistBotPunch (`RubberFistBotPunch`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, knockback 10`

---

## STATIC OBJECT

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Sabertooth Cat

### SabertoothCatDoubleSwipe (`SabertoothCatDoubleSwipe`)

- **Template:** `melee_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `multihit 2`
- **Damage/Effects:** `damage 3+bonus_melee_damage, Bleed 1, TriggerWerewolfTransform [1 .20]`

### SabertoothCatPounce (`SabertoothCatPounce`)

- **Template:** `jump_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 4, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, aoe_excludes_self false, restrictions none`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, IgnoreSelf 1, TriggerWerewolfTransform [1 .5]`

### SabertoothCatTransformSwipe (`SabertoothCatTransformSwipe`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, non_lethal true, TriggerWerewolfTransform .5`

---

## Sabertooth Kitten

### SabertoothCatTransformSwipe (`SabertoothCatTransformSwipe`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, non_lethal true, TriggerWerewolfTransform .5`

### SabertoothCubDoubleSwipe (`SabertoothCubDoubleSwipe`)

- **Template:** `melee_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `multihit 2`
- **Damage/Effects:** `damage 3+bonus_melee_damage, Bleed 1, TriggerWerewolfTransform [1 .20]`

### SabertoothCubLick (`SabertoothCubLick`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 5+bonus_melee_damage`

---

## Saucie

### Zorp (`UFO_CrossLasers`)

- **Template:** `straightshot_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode custom, aoe_symmetry four_way, custom_aoe [[1, 1]], upgrade_straight_shot_to_piercing true`
- **Damage/Effects:** `damage 2+bonus_basic_spell_damage`

### Detect (`UFO_Detect`)

- **Template:** `targeted_status`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, max_aoe 3, aoe_excludes_self true`
- **Damage/Effects:** `Marked 1`

### Shields Up (`UFO_Shield`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `DivineShield 1`

---

## Scary

### ScaryFear (`ScaryFear`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type status_spell, Fear 1`

### DOOM (`ScaryHaunt`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type status_spell, custom_additional_ai_weight avoid_redundant_debuffs_strict, Doomed 3`

### Teleport (`Teleport`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Schpidenbot

### InvaderAttack (`InvaderAttack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `multihit 2`
- **Damage/Effects:** `damage 2+bonus_melee_damage, Poison 1`

---

## Schutzbot

### SZBBackflipDodge (`SZBBackflipDodge`)

- **Template:** `jump_move`
- **Cost:** `Free`
- **Target/Shape:** `range_mode cross, max_range 1, restrictions [must_be_moveable must_move], allow_any_orientation true`
- **Damage/Effects:** `None`

### Reload (`SZBReload`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Ammo 3, stacks 1, ability SZBBackflipDodge`

### SZBShoot (`SZBShoot`)

- **Template:** `straightshot_attack`
- **Cost:** `mana 0, infcantrip true, cant_cast 1-X`
- **Target/Shape:** `target_mode tile, min_range 1, max_range 20, max_aoe 100, max_targets -X, X_is enable_if_has_ammo`
- **Damage/Effects:** `damage 7+bonus_ranged_damage, RandomBonusDamage 25`

---

## Scorpion Cat

### Grapple (`ScorpionHold`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode tile_to_character, aoe_considers_character_size false, target_mode tile, restrictions must_have_character, range_mode standard, aoe_mode standard, min_range 1, max_range 1, min_aoe 0, max_aoe 0`
- **Damage/Effects:** `damage 1+bonus_melee_damage, Grappled 1, EndTurn 1`

### Sting (`ScorpionSting`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Poison 1`

---

## Security Bot

### SBotAnger (`SBotAnger`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "Angry"`

### SBotAngryMove (`SBotAngryMove`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### SBotAttack (`SBotAttack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `multihit 2`
- **Damage/Effects:** `damage 3+bonus_melee_damage, type melee, Bleed 1`

### Recharge (`SBotRecharge`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `prioritize_dont_change_direction true`
- **Damage/Effects:** `Shield 1, MovementUp 1`

---

## Seduced Boulder

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Taunt (`Taunt`)

- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Taunting 1`

---

## Seraphim

### Revive (`SeraphimRevive`)

- **Template:** `spell`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode none, aoe_excludes_self true, aoe_restrictions must_have_corpse`
- **Damage/Effects:** `heal 0, Revive 50%, FlatAIBonus 100`

### Holy Light (`SeraphimX`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `target_mode none, aoe_mode diagcross, max_aoe 10, aoe_excludes_self true`
- **Damage/Effects:** `damage 5+bonus_basic_spell_damage, elements [, Holy, ]`

---

## Shade Cat

### SCAttack (`SCAttack`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ForceMoveAway 1, BonusCritChance 100, Fear 1`

### SCSneakUp (`SCSneakUp`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `target_mode random_tile, max_range 20, restrictions [must_be_moveable must_be_directly_behind_enemy]`
- **Damage/Effects:** `None`

---

## Shambler

### ShamblerDash (`ShamblerDash`)

- **Template:** `dash_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 2, consider_trample true`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1`

### Toss (`ShamblerToss`)

- **Template:** `throw_attack`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `max_range 8, min_range 5, restrictions none`
- **Damage/Effects:** `damage 5+bonus_melee_damage, custom_additional_ai_weight toss_far`

---

## Sharky

### SharkDash (`SharkDash`)

- **Template:** `dash_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `max_range 2`
- **Damage/Effects:** `damage 5+bonus_melee_damage, Bleed 1`

---

## Siren

### Siren Call (`SirenCall`)

- **Template:** `spell`
- **Cost:** `mana 5, cantrip true`
- **Target/Shape:** `min_range 0, max_range 6, max_aoe 0`
- **Damage/Effects:** `damage 0, ForceMoveTowards 1`

---

## Skeleton Cat

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Skeleton Kitten

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Skeleton Shambler

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### ShamblerDash (`ShamblerDash`)

- **Template:** `dash_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 2, consider_trample true`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1`

### Toss (`ShamblerToss`)

- **Template:** `throw_attack`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `max_range 8, min_range 5, restrictions none`
- **Damage/Effects:** `damage 5+bonus_melee_damage, custom_additional_ai_weight toss_far`

---

## Skinned

### SkinnedTripleDash (`SkinnedTripleDash`)

- **Template:** `dash_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `damage 2+bonus_melee_damage, knockback 1`

---

## Skull Ooze

### Acid Shot (`AcidShot`)

- **Template:** `ranged_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 2`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, Burn 2, DissolveRandomArmorPiece 1`

---

## Skunk

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Slag

### Bone Shot (`SlagBoner`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1`
- **Damage/Effects:** `Bruise 1`

### SlagSpawn (`SlagSpawn`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode line, min_aoe 1, max_aoe 1, max_targets 1, restrictions aoe_must_exist, aoe_considers_character_size true, aoe_excludes_self true, range_excludes_blocking false`
- **Damage/Effects:** `None`

---

## Slendermann

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Slot Machine

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### SlotMachine_DeathExplode (`SlotMachine_DeathExplode`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### SlotResult_Explode (`SlotResult_Explode`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode standard, knockback_mode character_to_tile, target_mode none, min_range 0, max_range 0, min_aoe 0, max_aoe 2`
- **Damage/Effects:** `damage 10, knockback 2, elements [, Fire, Explosion, ]`

### SlotResult_Jackpot_Coins (`SlotResult_Jackpot_Coins`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe 4, restrictions none, min_targets 7, max_targets 7, stagger_multihit_targets true, multihit 7`
- **Damage/Effects:** `None`

### SlotResult_Nothing (`SlotResult_Nothing`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### SlotResult_RandomPickup (`SlotResult_RandomPickup`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode line, min_aoe 1, max_aoe 1, restrictions none`
- **Damage/Effects:** `None`

---

## Small Asteroid

### SmallAsteroidBarrage (`SmallAsteroidBarrage`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_excludes_self true, aoe_considers_character_size true, max_aoe 2, min_aoe 0, min_range 0, max_range 1, max_targets 3, multihit 3, stagger_multihit_targets true, knockback_mode zero`
- **Damage/Effects:** `damage 4+bonus_ranged_damage, BounceObject SmallRock, damage 1, max_dist 2`

---

## Small Rock

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Snake

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Soahc

### Melee Attack (`BasicBigMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range`
- **Damage/Effects:** `None`

### CerberubsShotgunReactionX (`CerberubsShotgunReactionX`)

- **Template:** `straightshot_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 3+bonus_range, shotgun_mode true, aoe_mode custom, custom_aoe      [[4, 3], [4, 2], [4, 1], [4, 0], [4, -1], [4, -2]], custom_aoe_util [[1, 1], [1, 1], [1, 1], [1, 0], [1,  0], [1,  0]]`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, Burn 2, ChangeTile LavaTile`

### ChaosSpawnIn (`ChaosSpawnIn`)

- **Template:** `return`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20, aoe_excludes_self true, restrictions none`
- **Damage/Effects:** `None`

### ChaosSwitchForms (`ChaosSwitchForms`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `PurgeAll 1, ChaosBossFormChange 1`

### ChaosSwitchSides (`ChaosSwitchSides`)

- **Template:** `teleport`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode tile, range_mode special_tagged_tiles, special_tile_tag ChaosValidPosition, restrictions [must_move]`
- **Damage/Effects:** `None`

### Dbg Switch Forms (Random Active) (`DbgChaosSwitchFormsA`)

- **Template:** `self_buff`
- **Cost:** `infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "Johnny"`

### Dbg Switch Forms (Random Active+Passive) (`DbgChaosSwitchFormsP`)

- **Template:** `self_buff`
- **Cost:** `infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `form "JohnnyHost"`

### Hsulf (`FlushX`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `OverrideKnockbackDamage 3`

### Tsalb Dnim Agem (`MegablastX`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode circle, min_aoe 0, max_aoe 20, aoe_excludes_self true, aoe_considers_character_size true, distance_sort_targets true, knockback_mode tile_to_character`
- **Damage/Effects:** `damage 0, layer characters, knockback 10, stacks 1, height 1`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### Tuo Daerps. (`SpreadX`)

- **Template:** `spell`
- **Cost:** `prime 1, cantrip true`
- **Target/Shape:** `target_mode none, aoe_mode area_around_all_player_cats, aoe_considers_character_size false, aoe_excludes_self true, min_aoe 1, max_aoe 2, knockback_mode none, prioritize_face_camera true`
- **Damage/Effects:** `damage 8, ai_base_score 9999`

### ThornUpX (`ThornUpX`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Thorns 1, RandomMagicMissile 1`

---

## Sonichu

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Spear

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Spear Test Guy

### SpearPokeTest (`SpearPokeTest`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_aoe 4`
- **Damage/Effects:** `damage 5+bonus_melee_damage`

---

## Spider Cat

### TallSpiderMelee (`TallSpiderMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, Leech 1`

---

## Spider Kitten

### SmallSpiderMelee (`SmallSpiderMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, Leech 1`

### WebShot (`WebShot`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 3, restrictions none, knockback_mode zero`
- **Damage/Effects:** `damage 0, Webbed 1`

---

## Spiderling

### SpiderSuicideMelee (`SpiderSuicideMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Infested 1`

---

## Spiked Cat

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Spiky Rock

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Spookie

### SpookieLick (`SpookieLick`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, ManaSteal -1`

### Teleport (`Teleport`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Sprout

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### SproutSpore (`SproutSpore`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, Possessed 1`

---

## Spun Cat

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Squirrel

### Squirrel Swipes (`SquirrelFurySwipes`)

- **Template:** `melee_attack`
- **Cost:** `move_points 0, act_points 1`
- **Target/Shape:** `multihit_min 1, multihit_max 3`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee`

---

## Stacy #{stacy_number}

### Charm (`StacyCharm`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, custom_additional_ai_weight avoid_redundant_debuffs_strict, Charmed 1`

### StacyHeal (`StacyHeal`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 5+bonus_melee_damage, AllStatsUp 1`

---

## Stegosaurus

### StegoEatGrass (`StegoEatGrass`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_restrictions tile_must_have_element, aoe_tile_requires_element Grass`
- **Damage/Effects:** `layer tiles, ChangeTile BlankTile`

### StegoGrassStomp (`StegoGrassStomp`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `None`

### StegoSpin (`StegoSpin`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, aoe_mode square, aoe_excludes_self true, min_aoe 0, max_aoe 1, knockback_mode character_to_tile, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 6+bonus_melee_damage, piercing true, Bleed 1`

### StegoTailSwipe (`StegoTailSwipe`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_aoe -1, max_aoe -1`
- **Damage/Effects:** `damage 6+bonus_melee_damage, piercing true, Bleed 1`

---

## Stem Cat

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Steven

### Melee Attack (`BasicBigMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range`
- **Damage/Effects:** `None`

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Strange Egg

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Support Pillar

### LabPillarDrop (`LabPillarDrop`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `target_mode none, min_aoe 1, max_aoe 2, min_targets 3, max_targets 5, aoe_restrictions none, knockback_mode zero`
- **Damage/Effects:** `damage 5`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## T-Rex

### TrexEat (`TrexEat`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1, aoe_restrictions must_have_aggro_target`
- **Damage/Effects:** `type melee, damage 0, piercing true, cant_miss true, Vaporize 20, FlatLeech 10`

### TrexReacquireTarget (`TrexReacquireTarget`)

- **Template:** `targeted_status`
- **Cost:** `cantrip true`
- **Target/Shape:** `max_range 20, restrictions [must_have_cat must_have_enemy]`
- **Damage/Effects:** `cant_miss true, GetAggroTarget 1`

### TrexStomp (`TrexStomp`)

- **Template:** `melee_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode none, aoe_mode square, aoe_excludes_self true, min_aoe 0, max_aoe 1, knockback_mode character_to_tile, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 5+bonus_melee_damage, Immobile 1, time 2, intensity 20`

### TrexSwitchTarget (`TrexSwitchTarget`)

- **Template:** `targeted_status`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `cant_miss true, GetAggroTarget 1`

---

## TNT

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### TNTExplodey (`TNTExplodey`)

- **Template:** `spell`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode cross, knockback_mode character_to_tile, target_mode none, min_range 0, max_range 0, min_aoe 1, max_aoe 1`
- **Damage/Effects:** `damage 5, knockback 1, elements [, Fire, Explosion, ]`

---

## Tall Skeleton Cat

### BadBone (`BadBone`)

- **Template:** `straightshot_attack`
- **Cost:** `mana 0, charge 1`
- **Target/Shape:** `max_aoe 10`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, Stun [1 .15]`

### BadBone_copy (`BadBone_copy`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### GoodBone (`GoodBone`)

- **Template:** `straightshot_attack`
- **Cost:** `mana 0, charge 1`
- **Target/Shape:** `max_range 10`
- **Damage/Effects:** `damage 0, Shield 5+bonus_ranged_damage`

### GoodBone_copy (`GoodBone_copy`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Tall Tumor

### TT_ManaBurn (`TT_ManaBurn`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20, max_aoe 0`
- **Damage/Effects:** `damage 0, BonusDamageBasedOnMana 1, ManaStealToHealth -1`

### TT_Thrash (`TT_Thrash`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode square, knockback_mode character_to_tile`
- **Damage/Effects:** `damage 4+bonus_melee_damage, knockback 1`

---

## Tar Baby

### TarBall (`TarBall`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 4`
- **Damage/Effects:** `damage 1+bonus_ranged_damage, Tarred 2, tile OilTile`

---

## Tatters

### TattersFear (`TattersFear`)

- **Template:** `targeted_status`
- **Cost:** `Free`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `damage 0, type status_spell, Hex 1`

### TattersLeeches (`TattersLeeches`)

- **Template:** `lobbed_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `target_mode none, aoe_mode circle, aoe_excludes_self true, knockback_mode character_to_tile, max_aoe 2, aoe_restrictions [enemies_only]`
- **Damage/Effects:** `damage 0, Leeches 1`

### Teleport (`Teleport`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Ten Tickles

### Ten Tickles (`TenTicklesAttack`)

- **Template:** `spell`
- **Cost:** `mana 0`
- **Target/Shape:** `aoe_mode custom, custom_aoe [[1, 0]], knockback_mode orientation, range_mode square, min_range 1, max_range 10, restrictions [must_have_liquid must_be_empty], allow_any_orientation true`
- **Damage/Effects:** `damage 4+bonus_melee_damage, type melee, contact_requires_adjacency false`

### TenTicklesSwim (`TenTicklesSwim`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `max_range 10, range_mode square, restrictions [must_be_moveable must_have_liquid]`
- **Damage/Effects:** `None`

---

## Tesla Coil

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### TeslaBolt (`TeslaBolt`)

- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 0, max_range 3, min_range 1`
- **Damage/Effects:** `damage 3, custom_additional_ai_weight teslacoil_priorities, Stun [1, .1]`

---

## Test 2x2

### SpearPokeTest (`SpearPokeTest`)

- **Template:** `melee_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_aoe 4`
- **Damage/Effects:** `damage 5+bonus_melee_damage`

---

## The Collective

### CollectiveCounter (`CollectiveCounter`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `aoe_hint_teamcast true`
- **Damage/Effects:** `ability CollectiveCounterImpl, tag_restriction collective, same_orientation true`

### CollectiveSpin (`CollectiveSpin`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `aoe_hint_teamcast true`
- **Damage/Effects:** `ability CollectiveSpinImpl, tag_restriction collective`

---

## Throbbing Servant

### ParasiterShoot (`ParasiterShoot`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 2`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, ObjectOnHitEmpty Maggot, odds 15%, pool parasites`

### ParasiterSpawn (`ParasiterSpawn`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 1`
- **Damage/Effects:** `None`

---

## Throbbing Turret

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### SpawnClot (`SpawnClot`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 1`
- **Damage/Effects:** `None`

### ThrobShot (`ThrobShot`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 3, max_range 7+bonus_range, max_aoe 1`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, Bleed 1, ChangeTile WaterTile`

### ThrobShot_Reaction (`ThrobShot_Reaction`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `max_range 3, range_mode 8cross`
- **Damage/Effects:** `None`

---

## Thump

### ThumpSlam (`ThumpSlam`)

- **Template:** `jump_attack`
- **Cost:** `act_points 1, move_points 0`
- **Target/Shape:** `max_range 2, min_range 2, range_mode cross, range_considers_character_size false, min_aoe 0, max_aoe 1`
- **Damage/Effects:** `type melee, damage 5+bonus_melee_damage, knockback 1, IgnoreSelf 1`

### ThumpSlam_Mov (`ThumpSlam_Mov`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Tiny Tumor

### CancerMelee (`CancerMelee`)

- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ConstitutionUp -1, chance 30%, disease Cancer`

---

## Tire

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Toad

### Hook (`BasicHook`)

- **Template:** `straightshot_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 3+bonus_range, knockback_mode pull_to_character`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, PullSourceToKnockbackImmuneTarget 1, CollectsPickups 1`

### Jump (`BasicJump`)

- **Template:** `jump_attack`
- **Cost:** `move_points 1, act_points 0`
- **Target/Shape:** `target_mode tile, min_range 1, max_range mov, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, aoe_considers_character_size false, range_display_include_character_size true, restrictions must_be_moveable`
- **Damage/Effects:** `type none, damage 0`

---

## Toadie

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Disguise (`Disguise`)

- **Template:** `self_buff`
- **Cost:** `mana 5, cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Disguised 1`

### FearMelee (`FearMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, type melee, Fear 1`

### MoveTwoCantrip (`MoveTwoCantrip`)

- **Template:** `move`
- **Cost:** `mana 5, cantrip true`
- **Target/Shape:** `max_range 2`
- **Damage/Effects:** `None`

---

## Tom Tom

### WideSwipe (`WideSwipe`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode custom, aoe_symmetry none, custom_aoe [[1, -1] [1, 0] [1, 1]]`
- **Damage/Effects:** `None`

---

## Tombstone

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Tracy

### MegafetusMelee (`MegafetusMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_considers_character_size false, aoe_rotate_around_character_center true, aoe_mode custom, custom_aoe [[2, 1] [3, 1]]`
- **Damage/Effects:** `damage 8+bonus_melee_damage, contact_requires_adjacency false, time .5, intensity 3`

### Spin (`MegafetusSpin`)

- **Template:** `melee_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_mode square, knockback_mode character_to_tile`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1`

---

## Trash Bag

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Tremblo

### TrembloEat (`TrembloEat`)

- **Template:** `targeted_status`
- **Cost:** `cantrip true`
- **Target/Shape:** `max_range 1, restrictions [must_have_tag], target_requires_tag rock`
- **Damage/Effects:** `type melee, damage 0, piercing true, cant_miss true, ai_base_score 99, Vaporize 20, Brace 1, Shield 1`

### TrembloSmash (`TrembloSmash`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode custom, aoe_symmetry none, custom_aoe [[0, -1] [0, 0] [0, 1]]`
- **Damage/Effects:** `damage 4+bonus_melee_damage, knockback 1, Stun 1`

### Suck (`TrembloSuck`)

- **Template:** `targeted_status`
- **Cost:** `mana 0, must_not_be_consuming true, cantrip true`
- **Target/Shape:** `max_range 10, range_mode cross, knockback_mode none, restrictions [must_have_tag], target_requires_tag rock, knockback_mode pull_to_character`
- **Damage/Effects:** `damage 0, cant_miss true, TempTrampleUntilSettled 3, BypassRockKnockback 1`

---

## Triachnid

### tw_TriachnidSpawn (`tw_TriachnidSpawn`)

- **Template:** `spawn`
- **Cost:** `Free`
- **Target/Shape:** `max_range 2`
- **Damage/Effects:** `None`

---

## Triceratops

### TriceratopsGore (`TriceratopsGore`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, stacks 3, distance -3`

### Trample Dash (`TriceratopsTrample`)

- **Template:** `dash_attack`
- **Cost:** `prime 1, cantrip true`
- **Target/Shape:** `consider_trample true`
- **Damage/Effects:** `damage 8+bonus_melee_damage, knockback 1, override_trample_damage true, SetKnockback 0`

---

## Tumor

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Tumor Cat

### TC_Attack (`TC_Attack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 4+bonus_melee_damage, knockback 3, Bruise 1`

### TC_DashReaction (`TC_DashReaction`)

- **Template:** `trample_dash`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 3+bonus_melee_damage`

---

## Tumorhead

### HeadTumorAttack (`HeadTumorAttack`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 2+bonus_melee_damage, knockback 3`

### HeadTumorResponse (`HeadTumorResponse`)

- **Template:** `melee_spell`
- **Cost:** `Free`
- **Target/Shape:** `aoe_mode custom, custom_aoe [[-1 0]], knockback_mode back_orientation`
- **Damage/Effects:** `type spell, damage 0, knockback 3, elements [, Wind, ]`

---

## Turret

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### TurretShot (`TurretShot`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 6`
- **Damage/Effects:** `damage 3+bonus_ranged_damage`

---

## Turtle

### Push Attack (`BasicTankMelee`)

- **Template:** `dash_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1+bonus_range, max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1`

---

## Twister

### None (`None`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

### TwisterMove (`TwisterMove`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `restrictions [must_move]`
- **Damage/Effects:** `None`

---

## Tyler

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Waggle

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### WaggleClone (`WaggleClone`)

- **Template:** `lobbed_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `min_range 1, max_range 3, knockback_mode none`
- **Damage/Effects:** `damage 0, stacks 5, 1x1_object cWaggle, 2x2_object cWaggle2x2, 3x3_object cWaggle3x3`

---

## Water Kitten

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### WaterTrailMove (`WaterTrailMove`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Water Leech

### Leech Dash (`LeechDash`)

- **Template:** `dash_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 4+bonus_melee_damage, piercing true, force_no_knockback true, Leech 1`

### Move (`SwimmerMove`)

- **Template:** `move`
- **Cost:** `Free`
- **Target/Shape:** `range_mode water_move`
- **Damage/Effects:** `None`

---

## Werecat

### WolfDash (`WolfDash`)

- **Template:** `dash_attack`
- **Cost:** `mana 5, charge 1`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `damage 7+bonus_melee_damage`

### Wolf Leap (`WolfLeap`)

- **Template:** `jump_attack`
- **Cost:** `mana 5, charge 1`
- **Target/Shape:** `max_range 4`
- **Damage/Effects:** `damage 3+bonus_melee_damage`

---

## Whisperer

### Tumor Throw (`WhispererThrowBuff`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 3`
- **Damage/Effects:** `heal 1+bonus_ranged_damage, SpeedUp 2, Brace 2`

### Tumor Throw (`WhispererThrowDamage`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 3`
- **Damage/Effects:** `damage 1+bonus_ranged_damage, SpeedUp -2, Bruise 2`

### Whisper (`WhispererWhisper`)

- **Template:** `tile_targeted_melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `knockback_mode tile_to_character, restrictions must_have_character`
- **Damage/Effects:** `damage 0, Charmed 1`

---

## Wisp

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

---

## Wooly Mammoth

### MammothStomp (`MammothStomp`)

- **Template:** `melee_attack`
- **Cost:** `cantrip true`
- **Target/Shape:** `target_mode none, aoe_mode square, min_aoe 0, max_aoe 1, knockback_mode character_to_tile, aoe_excludes_self false, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1, IgnoreSelf 1, Bruise 1, time 2, intensity 10`

### MammothThrow (`MammothThrow`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_damage, stacks 3, distance 3, circular_variance 2`

### Stampede (`MammothTrampleDash`)

- **Template:** `trample_dash`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 8+bonus_melee_damage`

---

## Worm

### Lobbed Shot (`BasicRanged`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `damage 4+bonus_ranged_damage`

### Teleport (`Teleport`)

- **Template:** `teleport`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

---

## Y-Blaster

### YA_Charge (`YA_Charge`)

- **Template:** `self_buff`
- **Cost:** `cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `DamageUp 1`

### YA_Jetpack (`YA_Jetpack`)

- **Template:** `move`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 3, max_range 4, straight_shot true, as_the_crow_flies true, range_mode normal`
- **Damage/Effects:** `None`

### YA_Laser (`YA_Laser`)

- **Template:** `laser`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction, aoe_mode line, max_aoe 10, aoe_excludes_self true`
- **Damage/Effects:** `damage 1+bonus_basic_spell_damage`

---

## Yeti

### YetiBite (`YetiBite`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 2+bonus_melee_damage, Bleed 2, Leech 1`

### Ice Breath (`YetiIceBreath`)

- **Template:** `spell`
- **Cost:** `act_points 3`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe 3`
- **Damage/Effects:** `damage 0, Freeze 1`

### YetiKick (`YetiKick`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 2+bonus_melee_damage, knockback 3`

### YetiSlam (`YetiSlam`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 3+bonus_melee_damage`

---

## Yeti Cat

### YeticatSnowball (`YeticatSnowball`)

- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 2, max_range 2`
- **Damage/Effects:** `Slow 1, Freeze [1 .25]`

---

## Zombie Cat

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Feast (`ZombieFeast`)

- **Template:** `melee_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_restrictions must_have_destructible_corpse, restrictions aoe_must_exist`
- **Damage/Effects:** `damage 10, VaporizeCorpse 1, ConstitutionUp 2, StrengthUp 3, HealthGain 8, TakeExtraTurn 1`

---

## Zombie Kitten

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Feast (`ZombieFeastSmall`)

- **Template:** `melee_attack`
- **Cost:** `mana 5`
- **Target/Shape:** `aoe_restrictions must_have_destructible_corpse, restrictions aoe_must_exist`
- **Damage/Effects:** `damage 10, VaporizeCorpse 1, ConstitutionUp 1, StrengthUp 1, HealthGain 4`

---

## cWaggle2x2

### Melee Attack (`BasicBigMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range`
- **Damage/Effects:** `None`

---

## {SpawnedBy}'s Clot

### ClotEvolveCatCopy (`ClotEvolveCatCopy`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 999999, object PlayerCat_ClotClone, clone_referenced_catdata true, clone_items false`

### ClotFailEvolve (`ClotFailEvolve`)

- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ai_base_score 999999`

---

## {SpawnedBy}'s Crow

### Melee Attack (`BasicMelee`)

- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

### Aeroblast (`CrowFlap`)

- **Template:** `spell`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `target_mode direction, aoe_mode line, min_aoe 1, max_aoe 3+bonus_range, aoe_considers_character_size true, aoe_excludes_self true, knockback_mode orientation`
- **Damage/Effects:** `damage 1, knockback 1, elements [, Wind, ]`

### Flutter (`CrowFlutter`)

- **Template:** `move`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 3, max_range 3, straight_shot true, as_the_crow_flies true, range_mode normal`
- **Damage/Effects:** `None`

---

## {organname}

### Reload (`Reload`)

- **Template:** `self_buff`
- **Cost:** `mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Ammo -99999, Ammo 6, FormChange active`

### ZodiacShootX (`ZodiacShootX`)

- **Template:** `straightshot_attack`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `target_mode tile, min_range 1, max_range 20, max_aoe 100, max_targets -X, X_is enable_if_has_ammo`
- **Damage/Effects:** `damage 7+bonus_ranged_damage, knockback 1`

---

## Übercat

### Lasagnefloppen (`FatCatBellyFlop`)

- **Template:** `jump_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 3, min_aoe 0, max_aoe 1, aoe_mode square, aoe_excludes_self false, restrictions none`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1, IgnoreSelf 1`

---

## Überman

### FatManLunge (`FatManLunge`)

- **Template:** `dash_attack`
- **Cost:** `mana 0`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 10`

---
