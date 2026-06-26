# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Characters & Bosses

> **Associated Files:** `data/characters/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 600

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Visual parameters and animation bindings. | 2609 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage logic on contact. | 2344 ||
| [`variant_of`](./Enums.md#enum-variant_of) | Enum || 1195 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2985 ||
| [`properties`](#object-properties) | Object | General engine properties. | 600 ||
| [`stats`](#object-stats) | Object | Core character metrics (Health, Strength, etc.). | 461 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 459 ||
| [`abilities`](#object-abilities) | Object | Lists the ability IDs the character possesses. | 460 ||
| [`sound`](#object-sound) | Object | Audio bindings. | 62 ||
| [`equipment`](#object-equipment) | Object | List of item IDs the character spawns equipped with. | 44 ||
| [`alt_spawn_pool`](#object-alt_spawn_pool) | Object | Alternative pools to draw minions from. | 18 ||
| [`brain`](./Enums.md#enum-brain) | Enum || 5 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum || 5 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 5 ||
| `animation_suffix` | Enum / Integer | Examples: `3, 4, 2` | 1 ||
| `partial_animation_suffix` | Enum / Integer | Examples: `3, 2, 1` | 2 ||
| [`pattern`](#object-pattern) | Object | AI sequence logic. | 3 ||
| [`scale`](./Enums.md#enum-scale) | Number || 5 ||
| `end_turn_on_formswitch` | Boolean || 2 ||
| [`ai_if_spawned_as_enemy`](#object-ai_if_spawned_as_enemy) | Object | AI logic override used only if the character is spawned as an enemy. | 1 ||
| `consider_spells` | Boolean || 1 ||
| `uifloaters_offset` | Number || 1 ||
| [`accurate_knockback`](./Enums.md) | Boolean || 32 | false |
| [`buff_ally`](./Enums.md) | Integer || 32 | 0 |
| [`buff_enemy`](./Enums.md) | Integer || 32 | 0 |
| [`buff_self`](./Enums.md) | Integer || 32 | 0 |
| [`cap_distance_to_ally`](./Enums.md) | Integer || 4 | 2 |
| [`cap_distance_to_character`](./Enums.md) | Integer || 1 | 2 |
| [`cap_distance_to_enemy`](./Enums.md) | Integer || 2 | 2 |
| [`cap_total_distance_moved`](./Enums.md) | Integer || 1 | 1 |
| [`consider_aggro_target_enemy`](./Enums.md) | Boolean || 1 | true |
| [`consider_aoe`](./Enums.md) | Boolean || 3 | false |
| [`consider_overkill`](./Enums.md) | Boolean || 32 | false |
| [`consider_secondary_damage`](./Enums.md) | Boolean || 32 | false |
| [`consider_total_damage`](./Enums.md) | Boolean || 32 | false |
| [`count_nomove_in_eval`](./Enums.md) | Boolean || 1 | false |
| [`damage_ally`](./Enums.md) | Number || 32 | 0 |
| [`damage_ally_corpse`](./Enums.md) | Integer || 32 | 0 |
| [`damage_enemy`](./Enums.md) | Integer || 32 | 0 |
| [`damage_enemy_corpse`](./Enums.md) | Number || 32 | 0 |
| [`damage_self`](./Enums.md) | Number || 32 | 2 |
| [`danger_avoidance`](./Enums.md) | Number || 3 | 20 |
| [`debuff_ally`](./Enums.md) | Number || 32 | 0 |
| [`debuff_enemy`](./Enums.md) | Integer || 32 | 0 |
| [`debuff_self`](./Enums.md) | Number || 32 | 2 |
| [`distance_to_aggro_target`](./Enums.md) | Integer || 3 | -1 |
| [`distance_to_ally`](./Enums.md) | Number || 55 | 2 |
| [`distance_to_center`](./Enums.md) | Integer || 1 | -1 |
| [`distance_to_character`](./Enums.md) | Integer || 55 | 0 |
| [`distance_to_corpse`](./Enums.md) | Number || 3 | 0 |
| [`distance_to_enemy`](./Enums.md) | Number || 55 | 0 |
| [`distance_to_water`](./Enums.md) | Number || 2 | -1 |
| [`exclude_characters_tagged`](./Enums.md) | Enum || 1 | siren |
| [`face_aggro_target`](./Enums.md) | Integer || 2 | 10 |
| [`face_camera`](./Enums.md) | Integer || 1 | 1000 |
| [`face_closest_enemy`](./Enums.md) | Integer || 55 | 0 |
| [`flat_cast_bonus`](./Enums.md) | Integer || 5 | 99999 |
| [`heal_ally`](./Enums.md) | Integer || 32 | 0 |
| [`heal_enemy`](./Enums.md) | Integer || 32 | 0 |
| [`heal_self`](./Enums.md) | Integer || 32 | 0 |
| [`kill_ally`](./Enums.md) | Integer || 32 | 0 |
| [`kill_enemy`](./Enums.md) | Number || 32 | 0 |
| [`lava`](./Enums.md) | Integer || 1 | 5 |
| [`negative_weight_scale`](./Enums.md) | Number || 32 | .99 |
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1910 ||
| [`preferred_distance`](./Enums.md) | Enum / Integer || 55 | reach |
| [`randomness`](./Enums.md) | Integer || 5 | 50 |
| [`revive_ally_corpse`](./Enums.md) | Integer || 32 | 0 |
| [`revive_enemy_corpse`](./Enums.md) | Integer || 32 | 0 |
| [`simple`](./Enums.md) | Boolean || 3 | true |
| [`spawn_object`](./Enums.md) | Integer || 32 | 0 |
| [`spawn_object_distance_to_ally`](./Enums.md) | Number || 32 | .0001 |
| [`spawn_object_distance_to_enemy`](./Enums.md) | Number || 32 | 0 |
| [`spawn_object_preferred_distance`](./Enums.md) | Integer || 2 | 5 |
| [`spend_mana_scale`](./Enums.md) | Number || 32 | .99 |
| [`tall_grass`](./Enums.md) | Integer || 1 | 5 |
| [`total_distance_moved`](./Enums.md) | Number || 55 | 0 |

</details>

---

### Object: `graphics`


**Definition:** Object defining visual animations and sequence timings.  
**Total Count:** 2609


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 517 ||
| [`movieclip`](./Enums.md#enum-movieclip) | Array / Enum || 461 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 409 ||
| `shadow_size` | Number || 151 ||
| [`scale`](./Enums.md#enum-scale) | Number || 149 ||
| `uifloaters_offset` | Number || 149 ||
| [`custom_cat_data`](./Enums.md#enum-custom_cat_data) | Enum || 127 ||
| [`water_mask`](./Enums.md#enum-water_mask) | Enum || 83 ||
| [`spawnin_animation`](./Strings.md#string-spawnin_animation) | Enum || 37 ||
| `piece_alt_frame` | Integer || 27 ||
| [`shadow`](./Enums.md#enum-shadow) | Enum || 23 ||
| `move_speed_sync_frames` | Number || 20 ||
| `no_splatter` | Boolean || 17 ||
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array || 47 ||
| [`move_speed_multiplier`](./Enums.md#enum-move_speed_multiplier) | Number || 16 ||
| `dont_sink` | Boolean || 14 ||
| [`projectile_spawn_offset`](./Arrays.md#array-projectile_spawn_offset) | Array || 17 ||
| `art_flip` | Integer || 7 ||
| [`depth_offset`](./Enums.md#enum-depth_offset) | Number || 6 ||
| `four_way_animations` | Boolean || 4 ||
| `show_infinity_damage_warning` | Boolean || 3 ||
| [`tint`](./Arrays.md#array-tint) | Array / Enum || 17 ||
| `always_huge_mask` | Boolean || 2 ||
| [`default_attack_animation`](./Enums.md#enum-default_attack_animation) | Enum || 2 ||
| [`desc`](./Strings.md#string-desc) | Enum | Localization key for the character's desc. | 2 ||
| `shade_occluded_objects` | Boolean || 2 ||
| `no_horizontal_flip` | Boolean || 1 ||
| [`override_portrait`](./Enums.md#enum-override_portrait) | Enum || 1 ||
| `randomize_starting_frame` | Boolean || 1 ||
| `status_display_count_max` | Integer || 1 ||
| [`non_blocking_animations`](./Arrays.md#array-non_blocking_animations) | Array || 1 ||

</details>

---

### Object: `damage_instance`


**Definition:** Object defining the combat math and status effects applied upon successful hit.  
**Total Count:** 2346


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging impact triggers. | 1787 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2344 ||

</details>

---

### Object: `passives`


**Definition:** Object listing intrinsic passive modifiers.  
**Total Count:** 733


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Alert`](./Characters_and_Bosses.md#object-alert), [`AllAlive`](./Characters_and_Bosses.md#object-allalive), [`BellyFull`](./Characters_and_Bosses.md#object-bellyfull), [`Big`](./Characters_and_Bosses.md#object-big), [`BigHolding`](./Characters_and_Bosses.md#object-bigholding), [`BigHoldingCat`](./Characters_and_Bosses.md#object-bigholdingcat), [`Bishop`](./Characters_and_Bosses.md#object-bishop), [`BlackHole`](./Characters_and_Bosses.md#object-blackhole), [`Bomb`](./Characters_and_Bosses.md#object-bomb), [`Boris`](./Characters_and_Bosses.md#object-boris), [`Bully`](./Characters_and_Bosses.md#object-bully), [`CaveBaby`](./Characters_and_Bosses.md#object-cavebaby), [`CaveMan`](./Characters_and_Bosses.md#object-caveman), [`CaveManSpear`](./Characters_and_Bosses.md#object-cavemanspear), [`CaveWoman`](./Characters_and_Bosses.md#object-cavewoman), [`CaveWomanHasCat`](./Characters_and_Bosses.md#object-cavewomanhascat), [`Charging`](./Characters_and_Bosses.md#object-charging), [`Close`](./Characters_and_Bosses.md#object-close), [`Cultist`](./Characters_and_Bosses.md#object-cultist), [`Default`](./Characters_and_Bosses.md#object-default), and 97 more...

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2039 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 2 ||
| [`ArmorPickup`](#object-armorpickup) | Object | Pickup Logic: Defines what happens when an armor item is collected. | 3 ||
| [`ai`](#object-ai) | Object | Examples: `{ ... }` | 2 ||
| `partial_animation_suffix` | Enum / Integer | Examples: `4, 2` | 2 ||
| `animation_suffix` | Enum / Integer | Examples: `1` | 1 ||
| `uifloaters_offset` | Number | Examples: `2.2` | 1 ||
| [`AbilityAfterEnemyCastSpell_Stackable`](./Enums.md) | Enum || 4 | ThornUp |
| [`AbilityHealthThreshold`](#object-abilityhealththreshold) | Object || 12 ||
| [`AbilityOnBattleStart_UseAI`](./Enums.md) | Enum || 1 | TheCreator_SpawnCloneTeam |
| [`AbilityOnRoundEnd`](#object-abilityonroundend) | Object || 2 ||
| [`AbilityReaction`](#object-abilityreaction) | Enum / Object || 23 | MoonWormCurl |
| [`AbilityWhenBuddyDies`](./Enums.md) | Enum || 7 | Guillotina2Rage |
| [`AbilityWhenTaggedCharacterMovesNear`](Cat_Mutations.md#object-abilitywhentaggedcharactermovesnear) | Object || 3 ||
| [`AddCorpseHealth`](./Enums.md) | Integer || 14 | -999 |
| [`AddDamage`](./Enums.md) | Integer || 6 | 2 |
| [`AddElementsToBasicAttack`](./Enums.md) | Enum || 7 | Fire |
| [`AddHiddenTag`](./Enums.md) | Enum || 5 | hitler_clone_fetus |
| [`AddInitiative`](./Enums.md) | Integer || 7 | 999999 |
| [`AddMaxHealth`](./Enums.md) | Integer || 4 | -25 |
| [`AddMeleeKnockback`](./Enums.md) | Integer || 4 | 2 |
| [`AddMovement`](./Enums.md) | Integer || 20 | 2 |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object || 133 ||
| [`AddStatusToReceivedDamage`](#object-addstatustoreceiveddamage) | Object || 1 ||
| [`AddStatusToSpells`](#object-addstatustospells) | Object || 3 ||
| [`AddStatusToWeapons`](#object-addstatustoweapons) | Object || 4 ||
| [`AddTag`](./Enums.md) | Enum || 9 | fetus |
| [`AddTemporaryEffectsToBasicAttack`](Cat_Mutations.md#object-addtemporaryeffectstobasicattack) | Object || 4 ||
| [`AdvancedTint`](./Enums.md) | Array || 1 | [0] |
| [`AdventureTokenPassivePool`](#object-adventuretokenpassivepool) | Object || 1 ||
| [`AggroTargetIsBuddy`](./Enums.md) | Integer || 2 | 1 |
| [`AggroTargetIsCurrentTurn`](./Enums.md) | Integer || 3 | 1 |
| [`AggroTargetIsGovernedByHitEffect`](#object-aggrotargetisgovernedbyhiteffect) | Object || 1 ||
| [`AggroTargetIsLastEnemyThatDealtDamage`](./Enums.md) | Integer || 1 | 1 |
| [`AggroTargetIsLowestHealthEnemyTillItDies`](./Enums.md) | Integer || 1 | 1 |
| [`AggroTargetIsLowestMaxHealthCat`](./Enums.md) | Integer || 1 | 1 |
| [`AlienBeastDangerZones`](./Enums.md) | Array || 1 | [AlienBeastPuke] |
| [`AlienBeastEyeStalks`](./Enums.md) | Integer || 1 | 3 |
| [`AllDamageImmune_IncludingSpeculative`](./Enums.md) | Integer || 2 | 1 |
| [`AllSpellsCostActPoints`](./Enums.md) | Integer || 1 | 1 |
| [`AllStatsAura`](#object-allstatsaura) | Object || 1 ||
| [`AllStatsUp`](./Enums.md) | Integer || 14 | 2 |
| [`AlphaTurns`](./Enums.md) | Integer || 7 | 1 |
| [`AlwaysHitDifferentTargets`](./Enums.md) | Integer || 2 | 1 |
| [`Ammo`](./Enums.md) | Integer || 4 | 3 |
| [`Angel`](./Enums.md) | Integer || 5 | 1 |
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Enum / Object || 5 | SpiderReturn |
| [`AvoidDamagingCharmedEnemies`](./Enums.md) | Integer || 1 | 1 |
| [`AwardCoinsOnDeath`](./Enums.md) | Integer || 1 | 10 |
| [`BackstabAllDirections`](./Enums.md) | Integer || 4 | 1 |
| [`BackstabImmunity`](./Enums.md) | Integer || 9 | 1 |
| [`BaitAura`](#object-baitaura) | Object || 4 ||
| [`BaseStatMultiply`](./Enums.md) | Number || 3 | .5 |
| [`BasicAIDangerZone`](./Enums.md) | Integer || 1 | 2 |
| [`BattlefieldUniqueRandomPassive`](#object-battlefielduniquerandompassive) | Object || 1 ||
| [`Bird`](./Enums.md) | Enum || 4 | CookedChickenLeg |
| [`BirdRewards`](#object-birdrewards) | Object || 18 ||
| [`BlackHolePassive`](./Enums.md) | Integer || 1 | 1 |
| [`BloatEyePassive2`](./Enums.md) | Enum || 1 | BloatEyeMovement2 |
| [`BlockAllDamage`](./Enums.md) | Integer || 1 | 1 |
| [`BombBehavior`](./Enums.md) | Integer || 1 | 1 |
| [`BonusTurnPattern`](./Enums.md) | Array || 3 | [0] |
| [`BossRewards`](#object-bossrewards) | Object || 20 ||
| [`Brace`](./Enums.md) | Integer || 94 | 99 |
| [`Buddy`](#object-buddy) | Enum / Object || 17 | Guillotina3Head |
| [`BuffImmunity`](./Enums.md) | Integer || 4 | 1 |
| [`BungaCheers`](#object-bungacheers) | Object || 1 ||
| [`BungaEntrance`](#object-bungaentrance) | Object || 2 ||
| [`Burn`](./Enums.md) | Integer || 5 | 2 |
| [`CCImmunity`](./Enums.md) | Integer || 2 | 1 |
| [`CanMutateTo`](./Enums.md) | Array / Enum || 3 | [Leaper] |
| [`CanShield`](./Enums.md) | Integer || 2 | 1 |
| [`CapReceivedDamage`](./Enums.md) | Integer || 1 | 1 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 1 ||
| [`CaveFamilyEnrage`](#object-cavefamilyenrage) | Object || 6 ||
| [`CerberubsAggroTargetBehavior`](#object-cerberubsaggrotargetbehavior) | Object || 1 ||
| [`ChanceToBackflip`](Cat_Mutations.md#object-chancetobackflip) | Object || 4 ||
| [`ChanceToDisableActionsIfNotCharmed`](./Enums.md) | Integer || 2 | 75 |
| [`ChanceToFormChangeOnAbilityDamage`](#object-chancetoformchangeonabilitydamage) | Object || 1 ||
| [`ChanceToSpitOnDamage`](#object-chancetospitondamage) | Object || 7 ||
| [`ChangeTileOnDeath`](./Enums.md) | Enum || 2 | WaterTile |
| [`ChangeTileOnPop`](./Enums.md) | Enum || 4 | OilTile |
| [`ChaosBossFormChangeGuide`](#object-chaosbossformchangeguide) | Object || 1 ||
| [`ChaosBossPieces`](#object-chaosbosspieces) | Object || 1 ||
| [`ChaosHeadDropIn`](#object-chaosheaddropin) | Object || 1 ||
| [`CharacterLightSource`](#object-characterlightsource) | Object || 16 ||
| [`CherubimReaction`](#object-cherubimreaction) | Object || 2 ||
| [`CoinPickup`](./Enums.md) | Integer || 10 | 4 |
| [`ConjureBonusAbility`](./Enums.md) | Enum || 1 | random |
| [`CountAsCorpse`](./Enums.md) | Integer || 4 | 1 |
| [`CounterAttack`](Cat_Mutations.md#object-counterattack) | Array / Enum / Object || 34 | [GSScream] |
| [`CounterAttackAfterEnemyCastSpell`](./Enums.md) | Enum || 1 | Telekinesis |
| [`CreateGlobalModifiers`](Abilities_and_Spells.md#object-createglobalmodifiers) | Object || 2 ||
| [`CrowAttackLink`](./Enums.md) | Integer || 1 | 1 |
| [`DamageFromBehindOnly`](./Enums.md) | Integer || 1 | 1 |
| [`DeathRattle`](#object-deathrattle) | Enum / Object || 35 | BBExplode |
| [`DeathRattleRevive`](#object-deathrattlerevive) | Enum / Object || 13 | HCHumanDie |
| [`DebuffImmunity`](./Enums.md) | Integer || 7 | 1 |
| [`DelayedAutoRevive`](#object-delayedautorevive) | Object || 6 ||
| [`DemonicGlyphFrames`](./Enums.md) | Integer || 2 | 1 |
| [`DemonicGlyphStealer`](./Enums.md) | Integer || 1 | 1 |
| [`DiceBehavior`](#object-dicebehavior) | Object || 1 ||
| [`DicerArt`](./Enums.md) | Array || 1 | [50] |
| [`DieWhenOnlyGolemsLeft`](./Enums.md) | Integer || 1 | 1 |
| [`DieWhenSpawnerDies`](./Enums.md) | Integer || 1 | 1 |
| [`DiesToElement`](#object-diestoelement) | Enum / Object || 2 | Wind |
| [`DiesToPiercingAndSpikes`](#object-diestopiercingandspikes) | Object || 1 ||
| [`DigestDeadBodies`](./Enums.md) | Enum || 3 | MoonHead_Digest |
| [`DisableSpells`](./Enums.md) | Integer || 1 | 1 |
| [`Disguised`](./Enums.md) | Integer || 1 | 1 |
| [`DisguisedTrapper`](./Enums.md) | Enum || 1 | FearMelee |
| [`DisplayBuddyCatOnSpawn`](./Enums.md) | Integer || 1 | 3 |
| [`DisplayDangerAOE`](./Enums.md) | Enum || 4 | TheChild_Wrath |
| [`DissuadeInstakills`](./Enums.md) | Integer || 2 | 1 |
| [`Divide4OnDeath`](./Enums.md) | Enum || 6 | MedSlime |
| [`DivineShield`](./Enums.md) | Integer || 1 | 2 |
| [`DivineShieldPickup`](./Enums.md) | Integer || 1 | 1 |
| [`DodgeChance`](./Enums.md) | Integer || 14 | 50 |
| [`DodgeChanceWithBlindSpot`](./Enums.md) | Integer || 1 | 25 |
| [`DodgeChance_Status`](./Enums.md) | Integer || 6 | 66 |
| [`DodgeWhenTargeted`](#object-dodgewhentargeted) | Object || 1 ||
| [`DustCloudBehavior`](./Enums.md) | Integer || 1 | 1 |
| [`Dybbuk1HPTracker`](./Enums.md) | Integer || 1 | 1 |
| [`DybbukPossessionFallback`](#object-dybbukpossessionfallback) | Object || 1 ||
| [`ElectricArcs`](./Enums.md) | Integer || 1 | 1 |
| [`ElementImmune`](./Enums.md) | Enum || 39 | Ice |
| [`ElementWeakness`](./Enums.md) | Enum || 1 | Fire |
| [`EnrageOnDamage`](./Enums.md) | Integer || 1 | 1 |
| [`EraseSpawnCoins`](./Enums.md) | Integer || 1 | 1 |
| [`EventBounterHunterPassive`](./Enums.md) | Integer || 1 | 1 |
| [`ExpireOnSpawnerTurnEnd`](./Enums.md) | Integer || 2 | 1 |
| [`ExtraDispersedTurns`](./Enums.md) | Integer || 4 | 1 |
| [`ExtraMovePoints`](./Enums.md) | Integer || 3 | 1 |
| [`ExtraTurnsPerTaggedUnit`](./Enums.md) | Enum || 1 | sprout |
| [`FaceAwayLastDamage`](#object-faceawaylastdamage) | Object || 1 ||
| [`FaceLastDamage`](#object-facelastdamage) | Integer / Object || 2 | 1 |
| [`FaceShield`](./Enums.md) | Integer || 5 | 0 |
| [`FadeInsteadOfDie`](./Enums.md) | Integer || 8 | 1 |
| [`FinalBossBeamQueue`](#object-finalbossbeamqueue) | Object || 1 ||
| [`FinalBossBecomeTheChild`](#object-finalbossbecomethechild) | Object || 1 ||
| [`FinalBossHitCountdownBoris`](#object-finalbosshitcountdownboris) | Object || 1 ||
| [`FinalBossHitCountdownExplosive`](#object-finalbosshitcountdownexplosive) | Object || 1 ||
| [`FinalBossHitCountdownHoly`](#object-finalbosshitcountdownholy) | Object || 1 ||
| [`FinalBossPupils`](#object-finalbosspupils) | Object || 1 ||
| [`FinalBossShield`](./Enums.md) | Enum || 2 | None |
| [`FinalBossShieldHealth`](#object-finalbossshieldhealth) | Object || 1 ||
| [`FinalBossSyncAnimations`](#object-finalbosssyncanimations) | Object || 1 ||
| [`FlingObjectsOnTop`](./Enums.md) | Integer || 1 | 8 |
| [`FlushmasterCelebration`](./Enums.md) | Enum || 1 | celebrate |
| [`Flying`](./Enums.md) | Integer || 9 | 1 |
| [`ForceDodgeEverything`](./Enums.md) | Integer || 1 | 1 |
| [`FormChangeDuringWeatherElement`](#object-formchangeduringweatherelement) | Object || 2 ||
| [`FormChangeHealthThreshold`](#object-formchangehealththreshold) | Object || 3 ||
| [`FormChangeOffMap`](#object-formchangeoffmap) | Object || 8 ||
| [`FormChangeOnElementInfluence`](#object-formchangeonelementinfluence) | Object || 8 ||
| [`FormChangeWhenBuddyDies`](./Enums.md) | Enum || 1 | Rage |
| [`FormChangeWhileHasStatus`](#object-formchangewhilehasstatus) | Object || 35 ||
| [`FormChangeWhilePrimingAbility`](#object-formchangewhileprimingability) | Object || 6 ||
| [`FormChanger`](#object-formchanger) | Object || 106 ||
| [`FreePathfindElement`](./Enums.md) | Enum || 2 | Water |
| [`FullBlockEverything`](./Enums.md) | Integer || 1 | 1 |
| [`FullBlockEverythingTo0Damage`](./Enums.md) | Integer || 1 | 1 |
| [`GasCanBehavior`](./Enums.md) | Integer || 1 | 1 |
| [`GasCloudBehavior2`](./Enums.md) | Integer || 1 | 2 |
| [`GeminiTwin`](./Enums.md) | Integer || 1 | 1 |
| [`GlobalManaDrainAura`](./Enums.md) | Integer || 1 | -1 |
| [`GoopImmunity`](./Enums.md) | Integer || 1 | 1 |
| [`GoopWalk`](./Enums.md) | Integer || 2 | 1 |
| [`GroundFlopper`](./Enums.md) | Enum || 4 | DefaultMove |
| [`GuillotinaDeathHead`](./Enums.md) | Integer || 1 | 1 |
| [`HPAltStates`](#object-hpaltstates) | Object || 1 ||
| [`HarpoonTrapPassive`](./Enums.md) | Enum || 1 | HarpoonTrapPull |
| [`HealNeighborsEachTurn`](#object-healneighborseachturn) | Object || 1 ||
| [`HealthGain`](./Enums.md) | Integer || 6 | 5 |
| [`HealthPickup`](#object-healthpickup) | Object || 16 ||
| [`HealthRegenUp`](./Enums.md) | Integer || 52 | 2 |
| [`HiddenDoomed`](./Enums.md) | Integer || 1 | 2 |
| [`HitlerExecute`](#object-hitlerexecute) | Object || 1 ||
| [`IceBlockBehavior`](./Enums.md) | Integer || 1 | 1 |
| [`IgnoreTiles`](./Enums.md) | Integer || 6 | 1 |
| [`IllusionTint`](./Enums.md) | Integer || 1 | 1 |
| [`ImmediateAbilityReaction`](#object-immediateabilityreaction) | Array / Enum / Object || 26 | [ManglerFumbleEven] |
| [`ImmobilePassive`](./Enums.md) | Integer || 2 | 1 |
| [`InfiniteRebirth`](#object-infiniterebirth) | Object || 2 ||
| [`InheritSpawnerStats`](./Enums.md) | Integer || 1 | 1 |
| [`InjuryImmunity`](./Enums.md) | Integer || 5 | 1 |
| [`InnateElement`](./Enums.md) | Enum || 14 | Water |
| [`InsertIntoBackgroundPlaceholder`](./Enums.md) | Integer || 1 | 1 |
| [`JohnnyNeedsWashing`](#object-johnnyneedswashing) | Object || 1 ||
| [`JohnnyWasher`](./Enums.md) | Enum || 1 | BBTransformZealot |
| [`KaijuKnockbackImmune`](./Enums.md) | Integer || 6 | 1 |
| [`KaijuWinCon`](./Enums.md) | Enum || 2 | zaratana |
| [`KineticSpikes`](./Enums.md) | Integer || 15 | 5 |
| [`KnockbackImmunity`](./Enums.md) | Integer || 5 | 1 |
| [`LegacySpawnSavedCatIfExists`](./Enums.md) | Enum || 1 | Legacy_Marshmallow_StolenCatID |
| [`LimitDamage`](./Enums.md) | Integer || 10 | 1 |
| [`LimitHeal`](./Enums.md) | Integer || 9 | 0 |
| [`LockOrientationFaceTile`](./Enums.md) | Array || 1 | [0] |
| [`LoopingSoundWhileAlive`](./Enums.md) | Enum || 4 | Bomb_FuseLoop |
| [`MagicDamageImmune`](./Enums.md) | Integer || 2 | 1 |
| [`MamaCatAnimations`](./Enums.md) | Integer || 2 | 1 |
| [`ManaPickup`](#object-manapickup) | Object || 3 ||
| [`ManglerMonsterPassive`](./Enums.md) | Enum || 1 | ManglerMonsterDashAttack |
| [`MegaDinoDropController`](#object-megadinodropcontroller) | Object || 1 ||
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object || 59 ||
| [`MimicSpawnerAttacks`](./Enums.md) | Integer || 3 | -1 |
| [`MiniVolcanoReaction`](./Enums.md) | Enum || 2 | ThrobShot_Reaction |
| [`MinimumKnockbackFromAllDamage`](./Enums.md) | Integer || 7 | 1 |
| [`MinimumKnockbackFromPhysicalAttacks`](./Enums.md) | Integer || 3 | 1 |
| [`MissChance`](./Enums.md) | Integer || 9 | 20 |
| [`ModularPickup`](#object-modularpickup) | Object || 1 ||
| [`MonkCatReactionAbilities`](#object-monkcatreactionabilities) | Object || 1 ||
| [`MoonHeadCrackedVisual`](./Enums.md) | Enum || 1 | Cracked |
| [`MotherGrowController`](#object-mothergrowcontroller) | Object || 1 ||
| [`MotherTumorPassive`](#object-mothertumorpassive) | Object || 1 ||
| [`MotherTumorSpawnInCapture`](#object-mothertumorspawnincapture) | Object || 2 ||
| [`Mount`](#object-mount) | Object || 1 ||
| [`MoveAfterAnyAttemptedAttack`](#object-moveafteranyattemptedattack) | Object || 1 ||
| [`MoveAwayFromDamageSource`](#object-moveawayfromdamagesource) | Object || 2 ||
| [`MoveAwayWhenEnemyAdjacent`](#object-moveawaywhenenemyadjacent) | Object || 1 ||
| [`MoveTowardsDamageSource`](#object-movetowardsdamagesource) | Enum / Object || 10 | MoveOne |
| [`MoveTowardsKillers`](#object-movetowardskillers) | Enum / Object || 5 | ReaperRevenge |
| [`MoveWhenDamaged`](Cat_Mutations.md#object-movewhendamaged) | Enum / Object || 11 | move |
| [`MovementReaction`](#object-movementreaction) | Object || 9 ||
| [`MultiSpawnOnDeath`](#object-multispawnondeath) | Object || 1 ||
| [`MulticatHeads`](./Enums.md) | Integer || 1 | 0 |
| [`MutateAfterXTurns`](./Enums.md) | Integer || 1 | 3 |
| [`MutateViaAbility`](./Enums.md) | Enum || 3 | BBTransformMutant |
| [`MuteDemonicGlyphDisplay`](./Enums.md) | Integer || 1 | 1 |
| [`NoHealthOnlyShield`](./Enums.md) | Integer || 12 | 1 |
| [`OrthogonalAIDangerZone`](./Enums.md) | Integer || 1 | 10 |
| [`OverrideMaxHealth`](./Enums.md) | Integer || 7 | 25 |
| [`PackHunting`](./Enums.md) | Integer || 1 | 1 |
| [`PassiveWhenAffectedByElement`](Cat_Mutations.md#object-passivewhenaffectedbyelement) | Object || 4 ||
| [`PassiveWhenDead`](#object-passivewhendead) | Object || 4 ||
| [`PassiveWhileHasStatus`](Cat_Mutations.md#object-passivewhilehasstatus) | Object || 2 ||
| [`PassiveWhileNotHasStatus`](#object-passivewhilenothasstatus) | Object || 2 ||
| [`PermanentMadness`](./Enums.md) | Integer || 8 | 1 |
| [`Phasing`](./Enums.md) | Integer || 1 | 1 |
| [`Plant`](./Enums.md) | Integer || 8 | 1 |
| [`PoisonThorns`](./Enums.md) | Integer || 9 | 3 |
| [`PrioritizeAggroTarget`](./Enums.md) | Integer || 2 | 1 |
| [`PrioritizeFarAwayTargets`](./Enums.md) | Integer || 4 | 10 |
| [`PrioritizeHitDifferentTargets`](./Enums.md) | Integer || 3 | 1 |
| [`PrioritizePlayerCats`](./Enums.md) | Integer || 2 | 1 |
| [`PrioritizeWeakestEnemy`](./Enums.md) | Integer || 2 | 1 |
| [`ProtectTargetedAllies`](#object-protecttargetedallies) | Object || 3 ||
| [`RandomPassivePool`](#object-randompassivepool) | Object || 3 ||
| [`RandomizeAIWeightsEachTurn`](./Enums.md) | Array || 8 | [chubs_and_nubs_blind] |
| [`ReflectProjectiles`](#object-reflectprojectiles) | Integer / Object || 12 | 100 |
| [`ReturnBoundItemOnBattleEnd`](./Enums.md) | Integer || 1 | 1 |
| [`RevengeDamage`](Abilities_and_Spells.md#object-revengedamage) | Object || 15 ||
| [`Robot`](#object-robot) | Integer / Object || 47 | 1 |
| [`RunInXTurns`](./Enums.md) | Integer || 3 | 2 |
| [`RunWhenKittensDead`](./Enums.md) | Integer || 1 | 1 |
| [`RunWhenLastPlayerCatIsCharmed`](#object-runwhenlastplayercatischarmed) | Object || 1 ||
| [`SafeDoomed`](./Enums.md) | Integer || 2 | 1 |
| [`ScalingAttackAnimation`](#object-scalingattackanimation) | Object || 1 ||
| [`SecurityBotProtect`](#object-securitybotprotect) | Object || 7 ||
| [`SetSpellCosts`](./Enums.md) | Integer || 7 | 0 |
| [`SharePickups`](#object-sharepickups) | Object || 2 ||
| [`SharePickupsWithSpawner`](./Enums.md) | Integer || 3 | 0 |
| [`SharkySmellsBlood`](./Enums.md) | Integer || 5 | 1 |
| [`SkipFirstRounds`](#object-skipfirstrounds) | Object || 1 ||
| [`SlotMachineRollPool`](#object-slotmachinerollpool) | Object || 2 ||
| [`SmallRockBehavior`](#object-smallrockbehavior) | Integer / Object || 9 | 0 |
| [`SpawnCreepOnHit`](./Enums.md) | Integer || 3 | 1 |
| [`SpawnCreepOnHitKnockback`](./Enums.md) | Integer || 1 | 1 |
| [`SpawnOnDeath`](#object-spawnondeath) | Enum / Object || 21 | BiggestFood |
| [`SpawnThingOnDamage`](Cat_Mutations.md#object-spawnthingondamage) | Object || 28 ||
| [`SpawnThingOnDeath`](./Enums.md) | Enum || 12 | Boulder |
| [`SpawnerCatDataReference`](./Enums.md) | Integer || 1 | 1 |
| [`SpeedUp`](./Enums.md) | Integer || 7 | 2 |
| [`SpewerAltGraphics`](#object-speweraltgraphics) | Object || 1 ||
| [`SpreadWater`](./Enums.md) | Integer || 1 | 1 |
| [`SproutsGrantMovement`](./Enums.md) | Integer || 1 | 1 |
| [`StartDead`](./Enums.md) | Integer || 1 | 100 |
| [`StartOffMap`](./Enums.md) | Integer || 5 | 1 |
| [`StatusAfterXTurns`](#object-statusafterxturns) | Object || 2 ||
| [`StatusCollector`](#object-statuscollector) | Object || 9 ||
| [`StatusEachTurnBeginIfHasStatus`](#object-statuseachturnbeginifhasstatus) | Object || 1 ||
| [`StatusEachTurnEnd`](Cat_Mutations.md#object-statuseachturnend) | Object || 49 ||
| [`StatusEachTurnEndIfEnabledAtStartOfTurn`](#object-statuseachturnendifenabledatstartofturn) | Object || 1 ||
| [`StatusImmunity`](./Enums.md) | Array / Enum || 34 | [Burn] |
| [`StatusOnDie`](Cat_Mutations.md#object-statusondie) | Object || 8 ||
| [`StatusOnEndMove`](Cat_Mutations.md#object-statusonendmove) | Object || 7 ||
| [`StatusOnEnemyConfused`](#object-statusonenemyconfused) | Object || 1 ||
| [`StatusOnGainCoins`](#object-statusongaincoins) | Object || 4 ||
| [`StatusOnKill`](Cat_Mutations.md#object-statusonkill) | Object || 29 ||
| [`StatusOnSpawnIn`](#object-statusonspawnin) | Object || 2 ||
| [`StatusOnTookDamage`](Cat_Mutations.md#object-statusontookdamage) | Object || 29 ||
| [`StatusOnTookDamageFromAbility`](Cat_Mutations.md#object-statusontookdamagefromability) | Object || 6 ||
| [`StatusOverlappingCharactersAndDie`](#object-statusoverlappingcharactersanddie) | Object || 1 ||
| [`StatusWhenStatusCompletelyRemoved`](#object-statuswhenstatuscompletelyremoved) | Object || 1 ||
| [`StrengthUp`](./Enums.md) | Integer || 3 | 2 |
| [`StripStatuses`](./Enums.md) | Integer || 10 | 1 |
| [`StunImmunity`](#object-stunimmunity) | Integer / Object || 6 | 1 |
| [`SupportDieInsteadOfRun`](#object-supportdieinsteadofrun) | Object || 1 ||
| [`SupportFormChangeInsteadOfRun`](#object-supportformchangeinsteadofrun) | Enum / Object || 3 | Attacker |
| [`SurviveAt1HP`](./Enums.md) | Integer || 2 | 1 |
| [`SwimmingFormChange`](#object-swimmingformchange) | Object || 1 ||
| [`SyncFormsWithBuddy`](#object-syncformswithbuddy) | Object || 1 ||
| [`T3HitlerSpawningPhase`](#object-t3hitlerspawningphase) | Object || 1 ||
| [`TVBotDisableAttack`](./Enums.md) | Integer || 1 | 1 |
| [`TVBotDisableMove`](./Enums.md) | Integer || 1 | 1 |
| [`TVBotDisableSpells`](./Enums.md) | Integer || 1 | 1 |
| [`TVBotScreen`](#object-tvbotscreen) | Object || 1 ||
| [`TagGreed`](./Enums.md) | Enum || 6 | bishop_hat |
| [`TakeWeaponFromSpawner`](./Enums.md) | Integer || 1 | 1 |
| [`Tall`](./Enums.md) | Integer || 1 | 1 |
| [`TallTumorManaBurn`](./Enums.md) | Enum || 1 | TT_ManaBurn |
| [`Terminator2Chase`](./Enums.md) | Enum || 1 | move |
| [`Terminator2Run`](#object-terminator2run) | Object || 1 ||
| [`TerminatorChase`](#object-terminatorchase) | Object || 1 ||
| [`TerminatorSkin`](#object-terminatorskin) | Object || 1 ||
| [`Thorns`](./Enums.md) | Integer || 65 | 2 |
| [`TileElementDamageImmunity`](./Enums.md) | Enum || 1 | Ice |
| [`TileTrail`](./Enums.md) | Enum || 6 | ShadowTile |
| [`TileTrail_Ahead`](./Enums.md) | Enum || 3 | WaterTile |
| [`TinkererBasicAttackSwitching`](Cat_Classes.md#object-tinkererbasicattackswitching) | Object || 1 ||
| [`TireBehavior`](./Enums.md) | Integer || 1 | 1 |
| [`TormentorHeal`](./Enums.md) | Integer || 1 | 1 |
| [`TowerDefenseReflex`](./Enums.md) | Enum || 2 | attack |
| [`TrackAmountKilledByPlayer`](./Enums.md) | Enum || 1 | BonusBirdsKilled |
| [`Trample`](./Enums.md) | Integer || 88 | 3 |
| [`TransformInXTurns`](#object-transforminxturns) | Object || 7 ||
| [`TransformOnDeath`](./Enums.md) | Array / Enum || 13 | [Hive] |
| [`TransformOnDeathImmediately`](#object-transformondeathimmediately) | Enum / Object || 5 | NoHead |
| [`TransformOnElementInfluence`](#object-transformonelementinfluence) | Object || 9 ||
| [`TransformOnElementInfluencex`](#object-transformonelementinfluencex) | Object || 2 ||
| [`TransformOnStatusThreshold`](#object-transformonstatusthreshold) | Object || 1 ||
| [`TransformWhenBuddyDies`](./Enums.md) | Enum || 2 | UltraOrnstein |
| [`Trapper`](#object-trapper) | Object || 4 ||
| [`TutorialBossRiggedFight`](./Enums.md) | Integer || 1 | 16 |
| [`TwisterFling`](#object-twisterfling) | Object || 1 ||
| [`UncappedHP`](./Enums.md) | Integer || 2 | 1 |
| [`Undead`](./Enums.md) | Integer || 25 | 1 |
| [`UnlimitedDeathRattleRevive`](#object-unlimiteddeathrattlerevive) | Object || 1 ||
| [`UnlockOrientation`](./Enums.md) | Integer || 2 | 1 |
| [`UpTireBehavior`](./Enums.md) | Integer || 1 | 5 |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object || 2 | KirbySpit |
| [`UseAbilityWhenOutOfStatus`](#object-useabilitywhenoutofstatus) | Object || 1 ||
| [`UseAbilityWhenShieldDepleted`](./Enums.md) | Enum || 1 | T3Pebbles_PrimeBoulderDrop |
| [`Wall`](./Enums.md) | Integer || 1 | 1 |
| [`WaterWalk`](./Enums.md) | Integer || 14 | 1 |
| [`WeaponsDontLoseDurability`](./Enums.md) | Integer || 3 | 1 |
| [`WeremanTransformationReceiver`](./Enums.md) | Enum || 4 | CaveWomanDropTransform |
| [`WhitelistPickupType`](./Enums.md) | Enum || 1 | food |
| [`WideBackstab`](./Enums.md) | Integer || 1 | 1 |
| [`WispDodge`](./Enums.md) | Integer || 1 | 1 |
| [`YOffset`](./Enums.md) | Number || 6 | -.18 |
| [`ZeroKnockbackDamage`](./Enums.md) | Integer || 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |

</details>

---

### Object: `properties`


**Definition:** General engine properties.  
**Total Count:** 600


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum || 505 ||
| `health` | Integer || 427 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 280 ||
| `movement` | Integer || 277 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 538 ||
| [`tag`](./Arrays.md#array-tag) | Array / Enum | Specific entity tag required. | 399 ||
| [`corpse_health`](./Enums.md#enum-corpse_health) | Mixed || 195 ||
| `inherit_faction` | Boolean || 115 ||
| `dispersed_bonus_turns` | Integer || 104 ||
| `base_mana_regen` | Integer || 90 ||
| [`size`](./Enums.md#enum-size) | Enum / Number || 80 ||
| `shield` | Enum / Integer || 74 ||
| [`move_block`](./Enums.md#enum-move_block) | Enum || 73 ||
| `kill_required` | Boolean || 69 ||
| `can_be_backstabbed` | Boolean || 68 ||
| `initiative` | Enum / Integer || 61 ||
| `takes_turns` | Boolean || 61 ||
| `mana_regen` | Integer || 51 ||
| `mana` | Enum / Integer | Base maximum mana pool. | 50 ||
| `flying` | Boolean || 47 ||
| `weak_threshold` | Integer || 32 ||
| [`hidden_tag`](./Arrays.md#array-hidden_tag) | Array / Enum || 38 ||
| `knockback_immune` | Boolean || 25 ||
| [`banned_elite_buffs`](./Arrays.md#array-banned_elite_buffs) | Array || 45 ||
| `can_be_champion` | Boolean || 20 ||
| [`ai_scale`](./Enums.md#enum-ai_scale) | Number || 18 ||
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | `String` || 17 ||
| [`auto_run_priority`](./Enums.md#enum-auto_run_priority) | Enum || 16 ||
| `inanimate` | Boolean || 16 ||
| `disperse_main_turns` | Boolean || 15 ||
| `evenly_dispersed_bonus_turns` | Integer || 13 ||
| `exclude_from_hallucinate` | Boolean || 13 ||
| [`hidden_tags`](./Arrays.md#array-hidden_tags) | Array / Enum || 14 ||
| `round_end_bonus_turns` | Integer || 13 ||
| `can_be_overkilled` | Boolean || 12 ||
| `can_collect_coins` | Boolean || 10 ||
| `deathpoof_size` | Integer || 10 ||
| `dispersed_bonus_turns_consider_initiative` | Boolean || 10 ||
| `initial_health` | Integer || 10 ||
| [`lock_orientation`](./Arrays.md#array-lock_orientation) | Array || 19 ||
| `can_eat_food` | Boolean || 9 ||
| `can_grant_extra_turns` | Boolean || 8 ||
| [`elements`](./Arrays.md#array-elements) | Array || 16 ||
| `tall` | Boolean || 8 ||
| `dispersed_bonus_turns_before_cats` | Boolean || 7 ||
| `divine_shield` | Integer || 7 ||
| `is_player_cat` | Boolean || 7 ||
| [`tags`](./Arrays.md#array-tags) | Array / Enum || 14 ||
| `boss_minions_runaway` | Boolean || 6 ||
| `mana_matters` | Boolean || 6 ||
| `access_to_player_inventory` | Boolean || 5 ||
| `act_points` | Integer || 5 ||
| `takes_main_turn` | Boolean || 5 ||
| `visually_spiky` | Boolean || 5 ||
| `allow_passive_spelltransforming` | Boolean || 4 ||
| `base_crit_chance` | Integer || 4 ||
| `last_turn_is_main_turn` | Boolean || 4 ||
| `round_start_bonus_turns` | Integer || 4 ||
| `view_bleeding_characters_as_enemies` | Boolean || 4 ||
| [`aoe_pierce_mode`](./Enums.md#enum-aoe_pierce_mode) | Enum || 3 ||
| `base_initiative` | Integer || 3 ||
| `base_movement` | Integer || 3 ||
| `catdata_ignore_skills` | Boolean || 3 ||
| [`disallow_items`](./Enums.md#enum-disallow_items) | Enum || 3 ||
| [`held_coins`](./Arrays.md#array-held_coins) | Array / Integer || 10 ||
| `always_triggers_traps` | Boolean || 2 ||
| `base_health` | Integer || 2 ||
| `base_health_regen` | Integer || 2 ||
| `base_initial_mana` | Integer || 2 ||
| `base_mana` | Integer || 2 ||
| `blocking` | Boolean || 2 ||
| `can_be_elite` | Boolean || 2 ||
| `can_run` | Boolean || 2 ||
| `champion` | Boolean || 2 ||
| `force_not_familiar` | Boolean || 2 ||
| `hint_no_corpse` | Boolean || 2 ||
| `must_start_facing_camera` | Boolean || 2 ||
| `tile_desire_cost` | Integer || 2 ||
| `uncapturable` | Boolean || 2 ||
| `aggro_target_is_enemy` | Boolean || 1 ||
| `allow_flying_effect` | Boolean || 1 ||
| `allow_offmap_corpse` | Boolean || 1 ||
| `allow_replacebrain` | Boolean || 1 ||
| `always_face_forward` | Boolean || 1 ||
| `capture_as_cat` | Boolean || 1 ||
| `elite` | Boolean || 1 ||
| `first_turn_is_main_turn` | Boolean || 1 ||
| `ignore_mouseover` | Boolean || 1 ||
| `ignore_tiles` | Boolean || 1 ||
| `mouseover_priority` | Integer || 1 ||
| `move_points` | Integer || 1 ||
| `pickup_type` | Integer || 1 ||
| `scale` | Number || 1 ||
| `speculative_inanimate` | Boolean || 1 ||
| `static` | Boolean || 1 ||
| `two_fronts` | Boolean || 1 ||
| `two_fronts_switch` | Boolean || 1 ||
| `view_bugs_as_enemies` | Boolean || 1 ||
| [`inanimate_can_receive_specific_statuses`](./Arrays.md#array-inanimate_can_receive_specific_statuses) | Array || 1 ||

</details>

---

### Object: `ai`


**Definition:** Core block defining the AI behavior logic and weights.  
**Total Count:** 583


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Alert`](./Characters_and_Bosses.md#object-alert), [`Angry`](./Characters_and_Bosses.md#object-angry), [`Attacker`](./Characters_and_Bosses.md#object-attacker), [`BellyFull`](./Characters_and_Bosses.md#object-bellyfull), [`Bishop`](./Characters_and_Bosses.md#object-bishop), [`BlackHole`](./Characters_and_Bosses.md#object-blackhole), [`Bully`](./Characters_and_Bosses.md#object-bully), [`CaveBaby`](./Characters_and_Bosses.md#object-cavebaby), [`CaveMan`](./Characters_and_Bosses.md#object-caveman), [`CaveManSpear`](./Characters_and_Bosses.md#object-cavemanspear), [`CaveWoman`](./Characters_and_Bosses.md#object-cavewoman), [`CaveWomanHasCat`](./Characters_and_Bosses.md#object-cavewomanhascat), [`Charging`](./Characters_and_Bosses.md#object-charging), [`Cultist`](./Characters_and_Bosses.md#object-cultist), [`Damaged`](./Characters_and_Bosses.md#object-damaged), [`Default`](./Characters_and_Bosses.md#object-default), [`Default_Ceiling`](./Characters_and_Bosses.md#object-default_ceiling), [`Default_Ground`](./Characters_and_Bosses.md#object-default_ground), [`DesireMech`](./Characters_and_Bosses.md#object-desiremech), [`Down`](./Characters_and_Bosses.md#object-down), and 64 more...

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum || 573 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum || 493 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 490 ||
| [`pattern`](#object-pattern) | Object | AI sequence logic. | 289 ||
| [`mainturn_pattern`](#object-mainturn_pattern) | Object | AI Logic: Determines standard ability usage during the main turn. | 44 ||
| `end_turn_on_formswitch` | Boolean || 39 ||
| [`virtual_abilities`](#object-virtual_abilities) | Object | Abilities that are evaluated but not directly castable by the player. | 35 ||
| `auto_orient` | Boolean || 31 ||
| `reset_pattern_on_formswitch` | Boolean || 31 ||
| `stun_advances_pattern` | Boolean || 30 ||
| `fallback_advances_pattern` | Boolean || 28 ||
| [`bonusturn_pattern`](#object-bonusturn_pattern) | Object | AI Logic: Determines ability usage during bonus turns. | 27 ||
| [`fallback`](#object-fallback) | Object | Logic executed if primary options fail. | 23 ||
| [`round_end_bonusturn_pattern`](#object-round_end_bonusturn_pattern) | Object | AI Logic: Ability usage pattern during round-end bonus turns. | 12 ||
| `consider_spells` | Boolean || 11 ||
| `animate_choice` | Boolean || 8 ||
| `clamp_pattern` | Boolean || 5 ||
| `randomize_pattern_start` | Boolean || 3 ||
| [`dispersed_bonusturn_pattern`](#object-dispersed_bonusturn_pattern) | Object | AI Logic: Alternative bonus turn ability pattern. | 2 ||
| `random_orient` | Boolean || 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| `never_hit_ally_corpses` | Boolean || 1 ||
| [`post_absorb_move_weights`](./Enums.md#enum-post_absorb_move_weights) | Enum || 1 ||
| `reset_pattern_on_round_begin` | Boolean || 1 ||
| [`roll_ability`](./Enums.md#enum-roll_ability) | Enum || 1 ||
| [`round_start_bonusturn_pattern`](#object-round_start_bonusturn_pattern) | Object | AI Logic: Ability usage pattern during round-start bonus turns. | 1 ||
| [`dice_abilities`](./Arrays.md#array-dice_abilities) | Array || 1 ||

</details>

---

### Object: `stats`


**Definition:** Core character metrics (Health, Strength, etc.).  
**Total Count:** 497


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `strength` | Integer || 386 ||
| `constitution` | Integer || 380 ||
| `dexterity` | Integer || 380 ||
| `charisma` | Integer || 379 ||
| `intelligence` | Integer || 379 ||
| `speed` | Array / Number | Base speed/initiative stat. | 379 ||
| `luck` | Integer || 160 ||

</details>

---

### Object: `abilities`


**Definition:** Lists the ability IDs the character possesses.  
**Total Count:** 460


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum || 438 ||
| [`move`](./Enums.md#enum-move) | Enum || 433 ||
| [`spells`](./Arrays.md#array-spells) | Array || 381 ||
| `can_get_bonus` | Boolean || 30 ||

</details>

---

### Object: `pattern`


**Definition:** AI sequence logic.  
**Total Count:** 296


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root), [`ReplaceBrain`](./Characters_and_Bosses.md#object-replacebrain), [`ai`](./Characters_and_Bosses.md#object-ai), [`ai_if_spawned_as_enemy`](./Characters_and_Bosses.md#object-ai_if_spawned_as_enemy)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum || 101 ||
| [`do_priority`](./Arrays.md#array-do_priority) | Array || 82 ||
| [`do_all`](./Arrays.md#array-do_all) | Array || 91 ||
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum || 11 ||
| [`do_random`](./Arrays.md#array-do_random) | Array || 9 ||
| [`do_strict`](./Arrays.md#array-do_strict) | Array || 4 ||
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array || 3 ||
| [`move_then_do_priority`](./Arrays.md#array-move_then_do_priority) | Array || 2 ||
| [`move_then_do_random`](./Arrays.md#array-move_then_do_random) | Array || 3 ||
| [`do_all_shuffle`](./Arrays.md#array-do_all_shuffle) | Array || 2 ||
| [`do_best`](./Arrays.md#array-do_best) | Array || 1 ||
| [`do_best_multiple`](./Arrays.md#array-do_best_multiple) | Array || 1 ||
| [`do_priority_alternating`](./Arrays.md#array-do_priority_alternating) | Array || 1 ||
| [`move_then_do_all`](./Arrays.md#array-move_then_do_all) | Array || 1 ||

</details>

---

### Object: `Normal`


**Definition:** Character Form: Behavior and stats for the \'Normal\' state.  
**Total Count:** 231


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 5 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 10 ||

</details>

---

### Object: `Angry`


**Definition:** Character Form / AI State: Behavior and stats for the \'Angry\' state.  
**Total Count:** 221


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer || 1 ||

</details>

---

### Object: `FormChanger`


**Definition:** AI Role: Designates the character as one that frequently shifts forms.  
**Total Count:** 106


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 ||
| [`initial_form`](./Enums.md#enum-initial_form) | Enum / Integer || 56 ||
| [`Default`](#object-default) | Enum / Object | Character Form: The baseline default behavior state. | 37 ||
| [`default`](#object-default) | Enum / Object | Baseline configuration. | 4 ||
| [`Normal`](#object-normal) | Integer / Object | Character Form: Behavior and stats for the \'Normal\' state. | 11 ||
| [`Rage`](#object-rage) | Object | Character Form: Behavior and stats for the \'Rage\' state. | 10 ||
| [`HasCat`](#object-hascat) | Object | Character Form: Behavior and stats for the \'HasCat\' state. | 5 ||
| [`hot`](#object-hot) | Object | Visual effect indicator. | 4 ||
| [`OffMap`](#object-offmap) | Object | Character Form: Behavior and stats for the 'OffMap' state. | 4 ||
| [`AllAlive`](#object-allalive) | Object | Encounter State: Logic executed when all specific entities are currently alive. | 3 ||
| [`Down`](#object-down) | Object | Character Form: Behavior and stats for the \'Down\' state. | 3 ||
| [`Full`](#object-full) | Object | Character Form: Behavior and stats for the \'Full\' state. | 3 ||
| [`OneAlive`](#object-onealive) | Object | Encounter State: Logic executed when exactly one target is alive. | 3 ||
| [`TwoAlive`](#object-twoalive) | Object | Encounter State: Logic executed when exactly two targets are alive. | 3 ||
| [`Up`](#object-up) | Object | Character Form: Behavior and stats for the \'Up\' state. | 3 ||
| [`active`](#object-active) | Object | Defines actively executed abilities. | 2 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 2 ||
| [`Big`](#object-big) | Object | Character Form / AI State: Behavior and stats for the \'Big\' state. | 2 ||
| [`Boris`](#object-boris) | Enum / Object | Character Form / AI State: Behavior and stats for the \'Boris\' state. | 2 ||
| [`CaveMan`](#object-caveman) | Object | Character Form: Behavior and stats for the \'CaveMan\' state. | 2 ||
| [`CaveManSpear`](#object-cavemanspear) | Object | Character Form: Behavior and stats for the \'CaveManSpear\' state. | 2 ||
| [`Empty`](#object-empty) | Object | Character Form: Behavior and stats for the \'Empty\' state. | 2 ||
| [`Explosive`](#object-explosive) | Enum / Object | Character Form: Behavior and stats for the \'Explosive\' state. | 2 ||
| [`Holding`](#object-holding) | Object | Character Form: Behavior and stats for the \'Holding\' state. | 2 ||
| [`Holy`](#object-holy) | Enum / Object | Character Form: Behavior and stats for the \'Holy\' state. | 2 ||
| [`NotPriming`](#object-notpriming) | Object | Character Form: Behavior and stats when not charging an ability. | 2 ||
| `partial_animation_suffix` | Enum / Integer || 2 ||
| [`passive`](#object-passive) | Object | Intrinsic passive modifier. | 2 ||
| [`Priming`](#object-priming) | Object | Character Form: Behavior and stats when charging an ability. | 2 ||
| [`Rain`](#object-rain) | Object | Character Form: Behavior and stats for the 'Rain' state. | 2 ||
| [`Small`](#object-small) | Object | Character Form: Behavior and stats for the \'Small\' state. | 2 ||
| [`SquirrelForm`](#object-squirrelform) | Object | Character Form: Behavior and stats for the 'SquirrelForm' state. | 2 ||
| [`Turtled`](#object-turtled) | Object | Character Form: Behavior and stats for the 'Turtled' state. | 2 ||
| [`Alert`](#object-alert) | Object | AI State: The behavior profile used when the character is alerted to enemies. | 1 ||
| [`Angry`](#object-angry) | Object | Character Form / AI State: Behavior and stats for the \'Angry\' state. | 1 ||
| [`Attacker`](#object-attacker) | Object | AI Role: Designates the character as an attacker rather than support. | 1 ||
| [`BellyFull`](#object-bellyfull) | Object | Character Form / AI State: Behavior and stats for the \'BellyFull\' state. | 1 ||
| [`BigHolding`](#object-bigholding) | Object | Character Form / AI State: Behavior and stats for the \'BigHolding\' state. | 1 ||
| [`BigHoldingCat`](#object-bigholdingcat) | Object | Character Form / AI State: Behavior and stats for the \'BigHoldingCat\' state. | 1 ||
| [`Bishop`](#object-bishop) | Object | Character Form / AI State: Behavior and stats for the \'Bishop\' state. | 1 ||
| [`BlackHole`](#object-blackhole) | Object | Character Form / AI State: Behavior and stats for the \'BlackHole\' state. | 1 ||
| [`Bomb`](#object-bomb) | Object | Character Form / AI State: Behavior and stats for the 'Bomb' state. | 1 ||
| [`Bully`](#object-bully) | Object | Character Form / AI State: Behavior and stats for the 'Bully' state. | 1 ||
| [`Butcher`](Engine_LogicKeys.md#object-butcher) | Object | Applies or references the 'Butcher' effect/state. | 1 ||
| [`CaveBaby`](#object-cavebaby) | Object | Character Form: Behavior and stats for the \'CaveBaby\' state. | 1 ||
| [`CaveWoman`](#object-cavewoman) | Object | Character Form: Behavior and stats for the \'CaveWoman\' state. | 1 ||
| [`CaveWomanHasCat`](#object-cavewomanhascat) | Object | Character Form: Behavior and stats for the \'CaveWomanHasCat\' state. | 1 ||
| [`Charging`](#object-charging) | Object | Character Form / AI State: Behavior when charging an attack. | 1 ||
| [`Close`](#object-close) | Object | AI Movement logic: Maneuvers into close/melee range. | 1 ||
| [`Colorless`](Engine_LogicKeys.md#object-colorless) | Object | Applies or references the 'Colorless' effect/state. | 1 ||
| [`Cultist`](#object-cultist) | Object | Character Form: Behavior and stats for the \'Cultist\' state. | 1 ||
| [`Damaged`](#object-damaged) | Object | Character Form / AI State: Behavior when health is critically low. | 1 ||
| [`Default_Ceiling`](#object-default_ceiling) | Object | Character Form: The baseline behavior state while attached to the ceiling. | 1 ||
| [`Default_Ground`](#object-default_ground) | Object | Character Form: The baseline behavior state while on the ground. | 1 ||
| [`DesireMech`](#object-desiremech) | Object | Character Form: Behavior and stats for the 'DesireMech' state. | 1 ||
| [`Die`](#object-die) | Integer / Object | Character Form / Logic: Forces the character to die. | 1 ||
| [`Druid`](Engine_LogicKeys.md#object-druid) | Object | Applies or references the 'Druid' effect/state. | 1 ||
| [`Drunker`](#object-drunker) | Object | Character Form: Behavior and stats for the 'Drunker' state. | 1 ||
| [`DualSword`](#object-dualsword) | Object | Character Form: Behavior and stats for the \'DualSword\' state. | 1 ||
| [`DualSword_Primed`](#object-dualsword_primed) | Object | Character Form: Behavior and stats for the \'DualSword_Primed\' state. | 1 ||
| [`Dumb`](#object-dumb) | Integer / Object | AI Profile: A simplified, less optimal decision-making profile. | 1 ||
| [`Explody`](#object-explody) | Object | Character Form: Behavior and stats for the 'Explody' state. | 1 ||
| [`Fighter`](Engine_LogicKeys.md#object-fighter) | Object | Applies or references the 'Fighter' effect/state. | 1 ||
| [`FightPhase`](#object-fightphase) | Object | Boss Logic: Main combat phase. | 1 ||
| [`Fire`](#object-fire) | Integer / Object | Character Form: Behavior and stats for the 'Fire' state. | 1 ||
| [`FireFull`](#object-firefull) | Integer / Object | Character Form: Behavior and stats for the 'FireFull' state. | 1 ||
| [`Flop`](#object-flop) | Object | Character Form: Behavior and stats for the \'Flop\' state. | 1 ||
| [`Flop2`](#object-flop2) | Object | Character Form: Behavior and stats for the \'Flop2\' state. | 1 ||
| [`Flush`](#object-flush) | Object | Character Form: Behavior and stats for the 'Flush' state. | 1 ||
| [`FlushBubs`](#object-flushbubs) | Object | Character Form: Behavior and stats for the 'FlushBubs' state. | 1 ||
| [`FlushHost`](#object-flushhost) | Object | Character Form: Behavior and stats for the 'FlushHost' state. | 1 ||
| [`FlushNettle`](#object-flushnettle) | Object | Character Form: Behavior and stats for the 'FlushNettle' state. | 1 ||
| [`Grappling`](#object-grappling) | Object | Character Form / AI State: Behavior while grappling an opponent. | 1 ||
| [`Grown`](#object-grown) | Object | Character Form: Behavior and stats for the \'Grown\' state. | 1 ||
| [`GuaranteedJackpot`](#object-guaranteedjackpot) | Object | Loot Logic: Guarantees a high-tier drop. | 1 ||
| [`Guarding`](#object-guarding) | Object | Character Form / AI State: Defensive behavior state. | 1 ||
| [`HalfDead`](#object-halfdead) | Object | Character Form: Behavior and stats for the \'HalfDead\' state. | 1 ||
| [`HasDeadCat`](#object-hasdeadcat) | Object | Character Form: Behavior and stats for the \'HasDeadCat\' state. | 1 ||
| [`HasRock`](#object-hasrock) | Object | Character Form: Behavior and stats for the \'HasRock\' state. | 1 ||
| [`Headless`](#object-headless) | Object | Character Form: Behavior and stats for the \'Headless\' state. | 1 ||
| [`Hint_CrackedVisuals`](#object-hint_crackedvisuals) | Object | Visual: Overlay effects for cracked/damaged terrain or objects. | 1 ||
| [`Hint_CrackedVisuals2`](#object-hint_crackedvisuals2) | Object | Visual: Secondary cracked visual overlay. | 1 ||
| [`Hint_CrackedVisuals3`](#object-hint_crackedvisuals3) | Object | Visual: Tertiary cracked visual overlay. | 1 ||
| [`HumanDead`](#object-humandead) | Object | Character Form: Behavior and stats for the \'HumanDead\' state. | 1 ||
| [`Hunter`](Engine_LogicKeys.md#object-hunter) | Object | Applies or references the 'Hunter' effect/state. | 1 ||
| [`InitialPhase`](#object-initialphase) | Object | Boss Logic: The starting phase of an encounter. | 1 ||
| [`Insane_Ceiling`](#object-insane_ceiling) | Object | Character Form: Insane behavior state while attached to the ceiling. | 1 ||
| [`Insane_Ground`](#object-insane_ground) | Object | Character Form: Insane behavior state while on the ground. | 1 ||
| [`Johnny`](#object-johnny) | Object | Character Form: Behavior and stats for the 'Johnny' state. | 1 ||
| [`JohnnyBubs`](#object-johnnybubs) | Object | Character Form: Behavior and stats for the 'JohnnyBubs' state. | 1 ||
| [`JohnnyHost`](#object-johnnyhost) | Object | Character Form: Behavior and stats for the 'JohnnyHost' state. | 1 ||
| [`JohnnyNettle`](#object-johnnynettle) | Object | Character Form: Behavior and stats for the 'JohnnyNettle' state. | 1 ||
| [`Joystick`](#object-joystick) | Object | Character Form: Behavior and stats for the \'Joystick\' state. | 1 ||
| [`LastHit`](#object-lasthit) | Object | Logic: Executes logic on the final hit of a multi-hit attack. | 1 ||
| [`Lifted`](#object-lifted) | Object | Character Form: Behavior and stats for the \'Lifted\' state. | 1 ||
| [`Lit`](#object-lit) | Object | Character Form: Behavior and stats for the 'Lit' state. | 1 ||
| [`Mage`](Engine_LogicKeys.md#object-mage) | Object | Applies or references the 'Mage' effect/state. | 1 ||
| [`Medic`](Engine_LogicKeys.md#object-medic) | Object | Applies or references the 'Medic' effect/state. | 1 ||
| [`Monk`](Engine_LogicKeys.md#object-monk) | Object | Applies or references the 'Monk' effect/state. | 1 ||
| [`Mounted`](#object-mounted) | Object | Character Form: Behavior and stats for the \'Mounted\' state. | 1 ||
| [`MouthFull`](#object-mouthfull) | Object | Character Form: Behavior and stats for the \'MouthFull\' state. | 1 ||
| [`Mutant`](#object-mutant) | Integer / Object | Character Form: Behavior and stats for the \'Mutant\' state. | 1 ||
| [`Necromancer`](Engine_LogicKeys.md#object-necromancer) | Object | Applies or references the 'Necromancer' effect/state. | 1 ||
| [`NeutronStar`](#object-neutronstar) | Object | Character Form: Behavior and stats for the 'NeutronStar' state. | 1 ||
| [`NoDeathRattle`](./Engine_LogicKeys.md#valid-property-keys) | Object | Applies or references the 'NoDeathRattle' effect/state. | 1 ||
| [`NoEyes`](#object-noeyes) | Object | Character Form: Behavior and stats for the \'NoEyes\' state. | 1 ||
| [`NormalFull`](#object-normalfull) | Integer / Object | Character Form: Behavior and stats for the 'NormalFull' state. | 1 ||
| [`NoStick`](#object-nostick) | Object | Character Form: Behavior and stats for the 'NoStick' state. | 1 ||
| [`Nuke`](#object-nuke) | Object | Character Form: Behavior and stats for the 'Nuke' state. | 1 ||
| [`Obey`](#object-obey) | Integer / Object | AI State: Enforced compliance logic (e.g., when Charmed). | 1 ||
| [`Off`](#object-off) | Object | Character Form: Behavior and stats for the 'Off' state. | 1 ||
| [`OffScreen`](#object-offscreen) | Object | Character Form: Behavior and stats for the 'OffScreen' state. | 1 ||
| [`OneEye`](#object-oneeye) | Object | Character Form: Behavior and stats for the \'OneEye\' state. | 1 ||
| [`Open`](#object-open) | Object | Character Form: Behavior and stats for the 'Open' state. | 1 ||
| [`OpenCat`](#object-opencat) | Object | Character Form: Behavior and stats for the 'OpenCat' state. | 1 ||
| [`Out`](#object-out) | Object | Character Form: Behavior and stats for the 'Out' state. | 1 ||
| [`Possessing`](#object-possessing) | Object | Character Form: Behavior and stats for the \'Possessing\' state. | 1 ||
| [`Primed`](#object-primed) | Object | Character Form: Behavior and stats for the 'Primed' state. | 1 ||
| [`Psychic`](Engine_LogicKeys.md#object-psychic) | Object | Applies or references the 'Psychic' effect/state. | 1 ||
| [`Pulp2`](#object-pulp2) | Object | Character Form: Behavior and stats for the 'Pulp2' state. | 1 ||
| [`Pulp3`](#object-pulp3) | Object | Character Form: Behavior and stats for the 'Pulp3' state. | 1 ||
| [`Pulp4`](#object-pulp4) | Object | Character Form: Behavior and stats for the 'Pulp4' state. | 1 ||
| [`Pulp5`](#object-pulp5) | Object | Character Form: Behavior and stats for the 'Pulp5' state. | 1 ||
| [`Pulp6`](#object-pulp6) | Object | Character Form: Behavior and stats for the 'Pulp6' state. | 1 ||
| [`Pulp7`](#object-pulp7) | Object | Character Form: Behavior and stats for the 'Pulp7' state. | 1 ||
| [`Sitting`](#object-sitting) | Object | Character Form: Behavior and stats for the 'Sitting' state. | 1 ||
| [`SmallHolding`](#object-smallholding) | Object | Character Form: Behavior and stats for the \'SmallHolding\' state. | 1 ||
| [`SmallHoldingCat`](#object-smallholdingcat) | Object | Character Form: Behavior and stats for the \'SmallHoldingCat\' state. | 1 ||
| [`SpawningPhase`](#object-spawningphase) | Object | Boss Logic: Phase focused on summoning minions. | 1 ||
| [`Standing`](#object-standing) | Object | Character Form: Behavior and stats for the 'Standing' state. | 1 ||
| [`Standing2`](#object-standing2) | Object | Character Form: Behavior and stats for the 'Standing2' state. | 1 ||
| [`Start_Ceiling`](#object-start_ceiling) | Object | Character Form: Behavior and stats for the 'Start_Ceiling' state. | 1 ||
| [`Stop`](#object-stop) | Integer / Object | AI Movement: Forces the character to cease movement. | 1 ||
| [`SwordAndShield`](#object-swordandshield) | Object | Character Form: Behavior and stats for the 'SwordAndShield' state. | 1 ||
| [`SwordAndShield_Primed`](#object-swordandshield_primed) | Object | Character Form: Behavior and stats for the \'SwordAndShield_Primed\' state. | 1 ||
| `sync_brain_patterns` | Boolean || 1 ||
| [`Tank`](Engine_LogicKeys.md#object-tank) | Object | Applies or references the 'Tank' effect/state. | 1 ||
| [`Tar`](#object-tar) | Integer / Object | Character Form: Behavior and stats for the 'Tar' state. | 1 ||
| [`TarFull`](#object-tarfull) | Integer / Object | Character Form: Behavior and stats for the 'TarFull' state. | 1 ||
| [`Thief`](Engine_LogicKeys.md#object-thief) | Object | Applies or references the 'Thief' effect/state. | 1 ||
| [`Throb`](#object-throb) | Object | Character Form: Behavior and stats for the 'Throb' state. | 1 ||
| [`ThrobBubs`](#object-throbbubs) | Object | Character Form: Behavior and stats for the 'ThrobBubs' state. | 1 ||
| [`ThrobHost`](#object-throbhost) | Object | Character Form: Behavior and stats for the 'ThrobHost' state. | 1 ||
| [`ThrobNettle`](#object-throbnettle) | Object | Character Form: Behavior and stats for the 'ThrobNettle' state. | 1 ||
| [`Tinkerer`](Engine_LogicKeys.md#object-tinkerer) | Object | Applies or references the 'Tinkerer' effect/state. | 1 ||
| [`Transformed`](#object-transformed) | Object | Character Form: Behavior and stats for the 'Transformed' state. | 1 ||
| [`TwoEyes`](#object-twoeyes) | Object | Character Form: Behavior and stats for the 'TwoEyes' state. | 1 ||
| `uifloaters_offset` | Number || 1 ||
| [`Unlit`](#object-unlit) | Object | Character Form: Behavior and stats for the 'Unlit' state. | 1 ||
| [`Unmounted`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Object | Applies or references the 'Unmounted' effect/state. | 1 ||
| [`Unwashed`](#object-unwashed) | Object | Character Form: Behavior and stats for the 'Unwashed' state. | 1 ||
| [`Washed`](#object-washed) | Object | Character Form: Behavior and stats for the 'Washed' state. | 1 ||
| [`Washer`](#object-washer) | Object | Character Form: Behavior and stats for the \'Washer\' state. | 1 ||
| [`Water`](#object-water) | Object | Character Form: Behavior and stats for the \'Water\' state. | 1 ||
| [`WereMan`](#object-wereman) | Object | Character Form: Behavior and stats for the \'WereMan\' state. | 1 ||
| [`Zealot`](#object-zealot) | Object | Character Form: Behavior and stats for the \'Zealot\' state. | 1 ||
| [`ZealotBomb`](#object-zealotbomb) | Object | Character Form: Behavior and stats for the \'ZealotBomb\' state. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 56 ||

</details>

---

### Object: `SpawnOnDeath`


**Definition:** No definition provided.  
**Total Count:** 79


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum || 4 ||
| [`obj`](./Arrays.md#array-obj) | Array / Enum || 4 ||
| [`additional_statuses`](#object-additional_statuses) | Object | Generic statuses added to the character. | 1 ||

</details>

---

### Object: `sound`


**Definition:** Audio bindings.  
**Total Count:** 62


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_sounds`](./Arrays.md#array-alt_sounds) | Array || 61 ||
| [`animation_prefix`](./Enums.md#enum-animation_prefix) | Enum || 1 ||

</details>

---

### Object: `Robot`


**Definition:** No definition provided.  
**Total Count:** 46


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alternate_energized_effect`](#object-alternate_energized_effect) | Object | Overrides default energized visuals. | 2 ||

</details>

---

### Object: `turns`


**Definition:** Turn counter tracking.  
**Total Count:** 45


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Bishop`](./Characters_and_Bosses.md#object-bishop), [`Bully`](./Characters_and_Bosses.md#object-bully), [`Default`](./Characters_and_Bosses.md#object-default), [`Default_Ceiling`](./Characters_and_Bosses.md#object-default_ceiling), [`Default_Ground`](./Characters_and_Bosses.md#object-default_ground), [`FightPhase`](./Characters_and_Bosses.md#object-fightphase), [`Holding`](./Characters_and_Bosses.md#object-holding), [`InitialPhase`](./Characters_and_Bosses.md#object-initialphase), [`Insane_Ceiling`](./Characters_and_Bosses.md#object-insane_ceiling), [`Insane_Ground`](./Characters_and_Bosses.md#object-insane_ground), [`LastHit`](./Characters_and_Bosses.md#object-lasthit), [`Lifted`](./Characters_and_Bosses.md#object-lifted), [`Mutant`](./Characters_and_Bosses.md#object-mutant), [`Normal`](./Characters_and_Bosses.md#object-normal), [`NotPriming`](./Characters_and_Bosses.md#object-notpriming), [`Nuke`](./Characters_and_Bosses.md#object-nuke), [`OffMap`](./Characters_and_Bosses.md#object-offmap), [`OffScreen`](./Characters_and_Bosses.md#object-offscreen), [`OneAlive`](./Characters_and_Bosses.md#object-onealive), [`Possessing`](./Characters_and_Bosses.md#object-possessing), and 13 more...

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `takes_turns` | Boolean || 23 ||
| `dispersed_bonus_turns` | Integer || 18 ||
| `takes_main_turn` | Boolean || 10 ||
| `evenly_dispersed_bonus_turns` | Integer || 7 ||
| `round_end_bonus_turns` | Integer || 5 ||
| `wait_till_next_round_to_update_turns` | Boolean || 4 ||
| `round_start_bonus_turns` | Integer || 1 ||

</details>

---

### Object: `equipment`


**Definition:** List of item IDs the character spawns equipped with.  
**Total Count:** 44


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`face`](./Enums.md#enum-face) | Enum || 16 ||
| [`head`](./Enums.md#enum-head) | Enum / Number || 14 ||
| [`neck`](./Enums.md#enum-neck) | Enum || 10 ||
| [`weapon`](./Enums.md#enum-weapon) | Enum | Weapon item constraint. | 7 ||

</details>

---

### Object: `mainturn_pattern`


**Definition:** AI Logic: Determines standard ability usage during the main turn.  
**Total Count:** 44


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum || 23 ||
| [`do_all`](./Arrays.md#array-do_all) | Array || 9 ||
| [`do_priority`](./Arrays.md#array-do_priority) | Array || 8 ||
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum || 2 ||
| [`do_strict`](./Arrays.md#array-do_strict) | Array || 2 ||

</details>

---

### Object: `Default`


**Definition:** Character Form: The baseline default behavior state.  
**Total Count:** 38


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 10 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 28 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer || 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 24 ||

</details>

---

### Object: `FormChangeWhileHasStatus`


**Definition:** Logic: Changes form automatically while possessing a specific status.  
**Total Count:** 35


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 35 ||
| [`form_hasnot`](./Enums.md#enum-form_hasnot) | Enum || 30 ||
| [`form_has`](./Enums.md#enum-form_has) | Enum || 25 ||

</details>

---

### Object: `keyword_tooltips`


**Definition:** Forces specific UI tooltips to appear when hovering over the ability.  
**Total Count:** 35


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Die`](./Characters_and_Bosses.md#object-die), [`Dumb`](./Characters_and_Bosses.md#object-dumb), [`Obey`](./Characters_and_Bosses.md#object-obey), [`Stop`](./Characters_and_Bosses.md#object-stop)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TVBotDie` | Integer | Applies or references the 'TVBotDie' effect/state. | 1 ||
| `TVBotDumb` | Integer | Applies or references the 'TVBotDumb' effect/state. | 1 ||
| `TVBotObey` | Integer | Applies or references the 'TVBotObey' effect/state. | 1 ||
| `TVBotStop` | Integer | Applies or references the 'TVBotStop' effect/state. | 1 ||

</details>

---

### Object: `virtual_abilities`


**Definition:** Abilities that are evaluated but not directly castable by the player.  
**Total Count:** 35


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`MoveAway`](#object-moveaway) | Object | AI Movement: Moves away from the target. | 4 ||
| [`MoveClose`](#object-moveclose) | Object | AI Movement: Moves into melee range. | 4 ||
| [`DashRandomly`](#object-dashrandomly) | Object | AI Movement: Dashes to a random valid tile. | 2 ||
| [`Escape`](#object-escape) | Object | AI Movement: Logic for fleeing or escaping the map. | 2 ||
| [`MoveCenter`](#object-movecenter) | Object | AI Movement: Moves toward the center of the map. | 2 ||
| [`MoveForThrow`](#object-moveforthrow) | Object | AI Movement: Repositions to gain line of sight for throwing. | 2 ||
| [`SpearRun`](#object-spearrun) | Object | AI Movement: Specific movement logic for Spear enemies. | 2 ||
| [`CerberubsJumpBlind`](#object-cerberubsjumpblind) | Object | AI Logic: Blind jump attack pattern for Cerberubs. | 1 ||
| [`CerberubsJumpNormal`](#object-cerberubsjumpnormal) | Object | AI Logic: Normal jump attack pattern for Cerberubs. | 1 ||
| [`CloseConvert`](#object-closeconvert) | Object | AI State: Logic for converting adjacent units. | 1 ||
| [`FoodMove`](#object-foodmove) | Object | AI Movement: Logic for seeking out food items. | 1 ||
| [`ForceTrample`](#object-forcetrample) | Object | Logic: Forces movement to act as a trample attack. | 1 ||
| [`LeapClose`](#object-leapclose) | Object | AI Movement: Executes a jumping maneuver to close distance. | 1 ||
| [`MoveForBarrage`](#object-moveforbarrage) | Object | AI Movement: Repositions to optimize a barrage attack. | 1 ||
| [`MoveForDash`](#object-movefordash) | Object | AI Movement: Repositions to set up a dash attack line. | 1 ||
| [`MoveForGrass`](#object-moveforgrass) | Object | AI Movement: Moves toward grass tiles. | 1 ||
| [`MoveForPounce`](#object-moveforpounce) | Object | AI Movement: Repositions to optimize a pounce trajectory. | 1 ||
| [`MoveForSpin`](#object-moveforspin) | Object | AI Movement: Repositions into a cluster of enemies for a spin attack. | 1 ||
| [`MoveOneForPuke`](#object-moveoneforpuke) | Object | AI Movement: Specific positioning logic for puke attacks. | 1 ||
| [`MoveSpaced`](#object-movespaced) | Object | AI Movement: Moves to maintain a specific distance from targets. | 1 ||
| [`MoveToHead`](#object-movetohead) | Object | AI Movement: Navigates toward the 'head' or primary target. | 1 ||
| [`MoveTowards`](#object-movetowards) | Object | AI Movement: Moves toward the nearest target. | 1 ||
| [`NCGravecrawlFAR`](#object-ncgravecrawlfar) | Object | AI Movement: Specific grapple/crawl logic. | 1 ||
| [`ReturnA`](#object-returna) | Object | Boss Logic: Specific phase return trigger. | 1 ||
| [`RunFar`](#object-runfar) | Object | AI Movement: Maximize distance from targets. | 1 ||
| [`SuckMF`](#object-suckmf) | Object | Character Form: Behavior and stats for the 'SuckMF' state. | 1 ||
| [`TF_TargetAllies`](#object-tf_targetallies) | Object | AI Targeting: Prioritizes allies. | 1 ||
| [`TF_TargetEnemies`](#object-tf_targetenemies) | Object | AI Targeting: Prioritizes enemies. | 1 ||
| [`Unflip`](#object-unflip) | Object | Logic: Reverses a flipped state. | 1 ||

</details>

---

### Object: `AddStatusToBasicAttack`


**Definition:** Injects a status effect payload that applies whenever the character performs a basic attack.  
**Total Count:** 32


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#object-randompassivepool), [`StacyMutant_Counter`](./Characters_and_Bosses.md#object-stacymutant_counter), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 205 ||
| [`Bleed`](./Enums.md) | Integer || 30 | 2 |
| [`Bruise`](./Enums.md) | Integer || 12 | 1 |
| [`Burn`](./Enums.md) | Integer || 16 | 2 |
| [`Confusion`](./Enums.md) | Integer || 7 | 1 |
| [`DamageUp`](./Enums.md) | Integer || 1 | 2 |
| [`Fear`](./Enums.md) | Integer || 13 | 1 |
| [`GainDisorderFromPool`](#object-gaindisorderfrompool) | Object || 1 ||
| [`Knockback`](./Enums.md) | Integer || 24 | 3 |
| [`Leech`](./Enums.md) | Integer || 5 | 2 |
| [`Madness`](./Enums.md) | Integer || 3 | 1 |
| [`Poison`](./Enums.md) | Integer || 29 | 2 |
| [`Possessed`](./Enums.md) | Integer || 1 | 1 |
| [`RandomStatUp`](./Enums.md) | Integer || 1 | -1 |
| [`RemoteFlatLeech`](./Enums.md) | Integer || 1 | 1 |
| [`RemoteLeech`](./Enums.md) | Integer || 2 | 1 |
| [`Rot`](./Enums.md) | Integer || 5 | 1 |
| [`Slow`](./Enums.md) | Integer || 10 | 2 |
| [`Stun`](./Enums.md) | Integer || 8 | 1 |
| [`Weakness`](./Enums.md) | Integer || 7 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 56 |

</details>

---

### Object: `DeathRattle`


**Definition:** No definition provided.  
**Total Count:** 29


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 13 ||
| `pop_corpse` | Boolean || 11 ||
| `is_dying_animation` | Boolean || 7 ||
| `cancel_knockback` | Boolean || 1 ||
| `immediate` | Boolean || 1 ||
| `must_target_killer` | Boolean || 1 ||
| `target_killer` | Boolean || 1 ||

</details>

---

### Object: `bonusturn_pattern`


**Definition:** AI Logic: Determines ability usage during bonus turns.  
**Total Count:** 27


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum || 15 ||
| [`do_priority`](./Arrays.md#array-do_priority) | Array || 4 ||
| [`do_strict`](./Arrays.md#array-do_strict) | Array || 3 ||
| [`do_all`](./Arrays.md#array-do_all) | Array || 4 ||
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum || 1 ||

</details>

---

### Object: `CatPartsTransform`


**Definition:** Transforms specific body parts into different visual variants.  
**Total Count:** 25


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveGroup`](./Characters_and_Bosses.md#object-passivegroup), [`StacyMutant_Brace`](./Characters_and_Bosses.md#object-stacymutant_brace), [`StacyMutant_Counter`](./Characters_and_Bosses.md#object-stacymutant_counter), [`StacyMutant_Damage`](./Characters_and_Bosses.md#object-stacymutant_damage), [`StacyMutant_DoubleHead`](./Characters_and_Bosses.md#object-stacymutant_doublehead), [`StacyMutant_Fire`](./Characters_and_Bosses.md#object-stacymutant_fire), [`StacyMutant_Health`](./Characters_and_Bosses.md#object-stacymutant_health), [`StacyMutant_Holy`](./Characters_and_Bosses.md#object-stacymutant_holy), [`StacyMutant_Ice`](./Characters_and_Bosses.md#object-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#object-stacymutant_lightning), [`StacyMutant_Mirror`](./Characters_and_Bosses.md#object-stacymutant_mirror), [`StacyMutant_Speed`](./Characters_and_Bosses.md#object-stacymutant_speed), [`StacyMutant_Thorns`](./Characters_and_Bosses.md#object-stacymutant_thorns), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`palette`](./Enums.md#enum-palette) | Enum / Integer || 17 ||
| `ear1` | Integer | Sprite variant ID for the front ear. | 13 ||
| `tail` | Integer | Sprite variant ID for the tail. | 13 ||
| `arm2` | Number || 11 ||
| `arm1` | Number | Sprite variant ID for the front arm. | 10 ||
| `ear2` | Integer || 10 ||
| `leg1` | Integer | Sprite variant ID for the front leg. | 8 ||
| `leg2` | Integer || 8 ||
| `head` | Enum / Number | Sprite variant ID for the head. | 6 ||
| `texture` | Integer || 6 ||
| `body` | Number | Sprite variant ID for the body. | 5 ||
| `eye1` | Integer || 3 ||
| `eye2` | Integer || 3 ||

</details>

---

### Object: `fallback`


**Definition:** Logic executed if primary options fail.  
**Total Count:** 23


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum || 12 ||
| [`do_priority`](./Arrays.md#array-do_priority) | Array || 6 ||
| [`move_then_do`](./Enums.md#enum-move_then_do) | Enum || 1 ||
| [`do_all`](./Arrays.md#array-do_all) | Array || 1 ||
| [`do_best`](./Arrays.md#array-do_best) | Array || 1 ||
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array || 1 ||
| [`do_random`](./Arrays.md#array-do_random) | Array || 1 ||

</details>

---

### Object: `BossRewards`


**Definition:** Loot logic: Rewards dropped upon defeating a boss.  
**Total Count:** 20


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`common`](./Engine_EventKeys.md#valid-property-keys) | `String` || 20 ||
| [`rare`](./Engine_EventKeys.md#valid-property-keys) | `String` || 16 ||
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 20 ||

</details>

---

### Object: `AbilityReaction`


**Definition:** No definition provided.  
**Total Count:** 19


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 10 ||
| `ability_damage_only` | Boolean || 7 ||
| `backstabs_only` | Boolean || 3 ||
| `only_when_not_your_turn` | Boolean || 3 ||
| `cancel_knockback` | Boolean || 1 ||
| `enemies_only` | Boolean || 1 ||
| `even_on_0_damage` | Boolean || 1 ||
| `even_on_0_damage_if_knockback` | Boolean || 1 ||
| `match_knockback_direction` | Boolean || 1 ||
| `ranged_only` | Boolean || 1 ||
| `verify_target` | Boolean || 1 ||

</details>

---

### Object: `MeleeRevengeDamage`


**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 19


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#object-temppassiveuntilsettled), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging impact triggers. | 47 ||
| `knockback` | Enum / Integer || 24 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 22 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 70 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 10 ||
| [`elements`](./Arrays.md#array-elements) | Array || 10 ||
| `cant_miss` | `Boolean` || 1 ||

</details>

---

### Object: `ally_rewards`


**Definition:** Loot logic triggered if an ally dies.  
**Total Count:** 18


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BirdRewards`](./Characters_and_Bosses.md#object-birdrewards)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 18 ||
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object || 2 ||
| [`FindItemFromPool`](./Enums.md) | Enum || 16 | eagle_pool |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `alt_spawn_pool`


**Definition:** Alternative pools to draw minions from.  
**Total Count:** 18


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Antidote`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Applies or references the 'Antidote' effect/state. | 5 ||
| `Blessing` | Mixed | Applies or references the 'Blessing' effect/state. | 5 ||
| [`BigCatnip`](Engine_LogicKeys.md#object-bigcatnip) | Integer / Object | Applies or references the 'BigCatnip' effect/state. | 4 ||
| [`BiggestFood`](Engine_LogicKeys.md#object-biggestfood) | Integer / Object | Applies or references the 'BiggestFood' effect/state. | 4 ||
| [`BigScrap`](Engine_LogicKeys.md#object-bigscrap) | Number / Object | Applies or references the 'BigScrap' effect/state. | 4 ||
| [`Coin`](Engine_LogicKeys.md#object-coin) | Integer / Object | Applies or references the 'Coin' effect/state. | 4 ||
| [`BigFood`](Engine_LogicKeys.md#object-bigfood) | Integer / Object | Applies or references the 'BigFood' effect/state. | 2 ||
| `Coin10` | Mixed | Applies or references the 'Coin10' effect/state. | 2 ||
| [`Coin3`](Engine_LogicKeys.md#object-coin3) | Integer / Object | Applies or references the 'Coin3' effect/state. | 2 ||
| [`Coin4`](Engine_LogicKeys.md#object-coin4) | Integer / Object | Applies or references the 'Coin4' effect/state. | 2 ||
| [`MedCatnip`](Engine_LogicKeys.md#object-medcatnip) | Integer / Object | Applies or references the 'MedCatnip' effect/state. | 2 ||
| [`MedScrap`](Engine_LogicKeys.md#object-medscrap) | Integer / Object | Applies or references the 'MedScrap' effect/state. | 2 ||
| [`RandomArmorPickup`](Engine_LogicKeys.md#object-randomarmorpickup) | Number / Object | Applies or references the 'RandomArmorPickup' effect/state. | 2 ||
| [`RandomCatnipPickup`](Engine_LogicKeys.md#object-randomcatnippickup) | Integer / Object | Applies or references the 'RandomCatnipPickup' effect/state. | 2 ||
| [`RandomFoodPickup`](Engine_LogicKeys.md#object-randomfoodpickup) | Integer / Object | Applies or references the 'RandomFoodPickup' effect/state. | 2 ||
| [`Bear`](Engine_LogicKeys.md#object-bear) | Integer / Object | Applies or references the 'Bear' effect/state. | 1 ||
| [`BlackBird`](Engine_LogicKeys.md#object-blackbird) | Integer / Object | Applies or references the 'BlackBird' effect/state. | 1 ||
| [`Catepillar`](Engine_LogicKeys.md#object-catepillar) | Integer / Object | Applies or references the 'Catepillar' effect/state. | 1 ||
| [`Catnip`](Engine_LogicKeys.md#object-catnip) | Integer / Object | Applies or references the 'Catnip' effect/state. | 1 ||
| [`CharmedDip`](Engine_LogicKeys.md#object-charmeddip) | Integer / Object | Applies or references the 'CharmedDip' effect/state. | 1 ||
| [`CharmedFloater`](Engine_LogicKeys.md#object-charmedfloater) | Integer / Object | Applies or references the 'CharmedFloater' effect/state. | 1 ||
| [`CharmedPile`](Engine_LogicKeys.md#object-charmedpile) | Integer / Object | Applies or references the 'CharmedPile' effect/state. | 1 ||
| [`Cherub`](Engine_LogicKeys.md#object-cherub) | Integer / Object | Applies or references the 'Cherub' effect/state. | 1 ||
| [`Chicken`](Engine_LogicKeys.md#object-chicken) | Integer / Object | Applies or references the 'Chicken' effect/state. | 1 ||
| [`Coin2`](Engine_LogicKeys.md#object-coin2) | Integer / Object | Applies or references the 'Coin2' effect/state. | 1 ||
| [`Dove`](Engine_LogicKeys.md#object-dove) | Integer / Object | Applies or references the 'Dove' effect/state. | 1 ||
| [`Eagle`](Engine_LogicKeys.md#object-eagle) | Integer / Object | Applies or references the 'Eagle' effect/state. | 1 ||
| [`Food`](Engine_LogicKeys.md#object-food) | Integer / Object | Applies or references the 'Food' effect/state. | 1 ||
| [`Harpy`](Engine_LogicKeys.md#object-harpy) | Integer / Object | Applies or references the 'Harpy' effect/state. | 1 ||
| [`HummingBird`](Engine_LogicKeys.md#object-hummingbird) | Integer / Object | Applies or references the 'HummingBird' effect/state. | 1 ||
| [`LargeBirdPool`](Engine_LogicKeys.md#object-largebirdpool) | Integer / Object | Applies or references the 'LargeBirdPool' effect/state. | 1 ||
| [`MedBirdPool`](Engine_LogicKeys.md#object-medbirdpool) | Integer / Object | Applies or references the 'MedBirdPool' effect/state. | 1 ||
| [`Mutant`](#object-mutant) | Integer / Object | Character Form: Behavior and stats for the 'Mutant' state. | 1 ||
| [`Pigeon`](Engine_LogicKeys.md#object-pigeon) | Integer / Object | Applies or references the 'Pigeon' effect/state. | 1 ||
| [`RandomBiggerArmorPickup`](Engine_LogicKeys.md#object-randombiggerarmorpickup) | Number / Object | Applies or references the 'RandomBiggerArmorPickup' effect/state. | 1 ||
| [`RandomBiggerCatnipPickup`](Engine_LogicKeys.md#object-randombiggercatnippickup) | Integer / Object | Applies or references the 'RandomBiggerCatnipPickup' effect/state. | 1 ||
| [`RandomBiggerFoodPickup`](Engine_LogicKeys.md#object-randombiggerfoodpickup) | Integer / Object | Applies or references the 'RandomBiggerFoodPickup' effect/state. | 1 ||
| [`Raven`](Engine_LogicKeys.md#object-raven) | Integer / Object | Applies or references the 'Raven' effect/state. | 1 ||
| [`Scrap`](Engine_LogicKeys.md#object-scrap) | Integer / Object | Applies or references the 'Scrap' effect/state. | 1 ||
| [`Seagull`](Engine_LogicKeys.md#object-seagull) | Integer / Object | Applies or references the 'Seagull' effect/state. | 1 ||
| [`SmallBirdPool`](Engine_LogicKeys.md#object-smallbirdpool) | Integer / Object | Applies or references the 'SmallBirdPool' effect/state. | 1 ||
| [`Snake`](Engine_LogicKeys.md#object-snake) | Integer / Object | Applies or references the 'Snake' effect/state. | 1 ||
| [`Squirrel`](Engine_LogicKeys.md#object-squirrel) | Integer / Object | Applies or references the 'Squirrel' effect/state. | 1 ||
| [`Toad`](Engine_LogicKeys.md#object-toad) | Integer / Object | Applies or references the 'Toad' effect/state. | 1 ||
| [`Turkey`](Engine_LogicKeys.md#object-turkey) | Integer / Object | Applies or references the 'Turkey' effect/state. | 1 ||
| [`Turtle`](Engine_LogicKeys.md#object-turtle) | Integer / Object | Applies or references the 'Turtle' effect/state. | 1 ||

</details>

---

### Object: `BirdRewards`


**Definition:** Loot logic: Rewards dropped by bird-type enemies.  
**Total Count:** 18


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ally_rewards`](#object-ally_rewards) | Object | Loot logic triggered if an ally dies. | 18 ||
| [`statuses`](#object-statuses) | Object | Status effects possessed by the character. | 5 ||

</details>

---

### Object: `CharacterLightSource`


**Definition:** Visual: Attaches a dynamic lighting source to the character.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `size` | Enum / Number || 16 ||
| [`color`](./Arrays.md#array-color) | Array || 16 ||
| [`glow`](./Arrays.md#array-glow) | Array || 8 ||

</details>

---

### Object: `HealthPickup`


**Definition:** Pickup Logic: Defines what happens when a health item is collected.  
**Total Count:** 16


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 15 ||
| `stored_food_value` | Integer || 15 ||
| [`frame_range`](./Arrays.md#array-frame_range) | Array || 15 ||
| `anything_eats` | Boolean || 4 ||
| `force_frame` | Integer || 1 ||

</details>

---

### Object: `statuses`


**Definition:** Status effects possessed by the character.  
**Total Count:** 14


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BirdRewards`](./Characters_and_Bosses.md#object-birdrewards), [`Cat`](./Characters_and_Bosses.md#object-cat), [`NonCat`](./Characters_and_Bosses.md#object-noncat)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 ||
| [`AllStatsUp`](./Enums.md) | Integer || 4 | 2 |
| [`Consumed`](Abilities_and_Spells.md#object-consumed) | Object || 4 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `default`


**Definition:** Character Form: The baseline default behavior state.  
**Total Count:** 13


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `effects`
### Object: `effects`

**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 13


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Characters_and_Bosses.md#object-meleerevengedamage), [`damage_instance`](./Characters_and_Bosses.md#object-damage_instance), [`eat_damage`](./Characters_and_Bosses.md#object-eat_damage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 750 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1695 ||
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 21 ||
| `BlackHoleSuck` | `Number` | Applies or references the 'BlackHoleSuck' effect/state. | 1 ||
| [`Burn`](./Enums.md) | Integer || 85 | 2 |
| [`Confusion`](./Enums.md) | Integer || 37 | 1 |
| [`ConstitutionUp`](./Enums.md) | Integer || 22 | -1 |
| [`Stun`](./Enums.md) | Integer || 98 | 1 |
| [`Thorns`](./Enums.md) | Integer || 12 | 2 |

</details>

---

### Object: `ImmediateAbilityReaction`


**Definition:** No definition provided.  
**Total Count:** 13


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 13 ||
| `ability_damage_only` | Boolean || 6 ||
| `backstabs_only` | Boolean || 2 ||
| `damage_threshold` | Integer || 2 ||
| `even_if_blocked` | Boolean || 2 ||
| `even_if_stunned` | Boolean || 2 ||
| `health_threshold` | Integer || 2 ||
| `buddy_damage_only` | Boolean || 1 ||
| `target_furthest_valid` | Boolean || 1 ||

</details>

---

### Object: `AbilityHealthThreshold`


**Definition:** AI Trigger: Executes an ability when health drops below a specific threshold.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 13 ||
| `even_if_stunned` | Boolean || 7 ||
| `immediate` | Boolean || 6 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 12 ||
| `use_ai` | Boolean || 2 ||
| `also_use_if_buddy_is_dead` | Boolean || 1 ||
| [`threshold_min`](./Math_Equations.md) | Equation || 1 ||
| [`threshold`](./Enums.md) | Enum / Integer || 12 | 200 |

</details>

---

### Object: `PassiveGroup`


**Definition:** Passive: A collection of passives grouped together for easier management.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#object-randompassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 14 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 12 ||
| [`ExtraBasicAttacks`](./Enums.md) | Integer || 1 | 1 |
| [`FormChange`](./Enums.md) | Enum || 12 | Druid |
| [`ReplaceBasicAttack`](./Enums.md) | Enum || 11 | BasicStraightShot |
| [`SelfStatusCarefulness`](./Enums.md) | Integer || 2 | 1 |
| [`StatusCarefulness`](./Enums.md) | Integer || 2 | 1 |
| [`TinkererBasicAttackSwitching`](Cat_Classes.md#object-tinkererbasicattackswitching) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 13 |

</details>

---

### Object: `round_end_bonusturn_pattern`


**Definition:** AI Logic: Ability usage pattern during round-end bonus turns.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum || 3 ||
| [`do_all`](./Arrays.md#array-do_all) | Array || 6 ||
| [`do_one`](./Arrays.md#array-do_one) | Array || 2 ||
| [`do_random`](./Arrays.md#array-do_random) | Array || 2 ||
| [`do_nothing`](./Arrays.md#array-do_nothing) | Array || 1 ||
| [`do_priority`](./Arrays.md#array-do_priority) | Array || 1 ||

</details>

---

### Object: `SpawnThingOnDamage`


**Definition:** Applies or references the 'SpawnThingOnDamage' effect/state.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum || 38 ||
| `good` | Boolean || 20 ||
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Probability (0.0 to 1.0) of executing this action. | 12 ||
| `spawn_on_death_hit` | Boolean || 10 ||
| `coins` | Integer || 2 ||
| `consider_all_layers` | Boolean || 2 ||
| [`auto_cast`](./Enums.md#enum-auto_cast) | Enum || 1 ||
| `melee_ability_only` | Boolean || 1 ||

</details>

---

### Object: `DeathRattleRevive`


**Definition:** No definition provided.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 8 ||
| `even_if_stunned` | Boolean || 8 ||

</details>

---

### Object: `MoveWhenDamaged`


**Definition:** No definition provided.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Array / Enum || 9 ||
| [`move_ability`](./Enums.md#enum-move_ability) | Enum || 2 ||

</details>

---

### Object: `Rage`


**Definition:** Character Form: Behavior and stats for the \'Rage\' state.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 8 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 6 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 10 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer || 4 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| `move_speed_multiplier` | Number || 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 6 ||

</details>

---

### Object: `FormChangeOnElementInfluence`


**Definition:** Logic: Changes form when affected by an element.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum / Integer || 9 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 9 ||
| [`exclude`](./Enums.md#enum-exclude) | Enum || 5 ||
| [`particle`](./Enums.md#enum-particle) | Enum || 5 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum || 5 ||

</details>

---

### Object: `ReflectProjectiles`


**Definition:** No definition provided.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusCollector`


**Definition:** Passive: Gains benefits based on the number of statuses applied to them.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 ||
| [`Poison`](./Enums.md) | Integer || 4 | 2 |
| [`Slow`](./Enums.md) | Integer || 4 | 2 |
| [`StrengthUp`](./Enums.md) | Integer || 7 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `TransformInXTurns`


**Definition:** Logic: Forces a form change after X turns.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#object-randompassivepool), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 8 ||
| [`object`](./Arrays.md#array-object) | Array / Enum || 8 ||
| [`initiative`](./Enums.md#enum-initiative) | Enum / Integer || 4 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 2 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||

</details>

---

### Object: `TransformOnElementInfluence`


**Definition:** Logic: Changes form when affected by elements.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 9 ||
| [`object`](./Enums.md#enum-object) | Array / Enum || 9 ||

</details>

---

### Object: `FormChangeOffMap`


**Definition:** Logic: Changes form when pushed off the map.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_offmap`](./Enums.md#enum-form_offmap) | Enum || 8 ||
| [`form_onmap`](./Enums.md#enum-form_onmap) | Enum || 8 ||

</details>

---

### Object: `SmallRockBehavior`


**Definition:** No definition provided.  
**Total Count:** 8


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 4 ||
| `knockback` | Enum / Integer || 4 ||
| `chain` | Boolean || 2 ||

</details>

---

### Object: `ChanceToSpitOnDamage`


**Definition:** Reaction: Probability to use a spit counter-attack when damaged.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 7 ||
| `flat_chance` | Integer || 5 ||
| `chance_per_damage` | Integer || 3 ||
| `backstabs_only` | Boolean || 1 ||
| `even_on_0_damage_if_knockback` | Boolean || 1 ||

</details>

---

### Object: `MovementReaction`


**Definition:** Reaction: Triggers an effect or ability when forced to move.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 11 ||
| `enemies_only` | Boolean || 7 ||
| `on_self_move_too` | Boolean || 3 ||
| `objects_too` | Boolean || 2 ||
| `blind_spot` | Boolean || 1 ||
| `forward_only` | Boolean || 1 ||
| `self_move_exclude_self_abilities` | Boolean || 1 ||

</details>

---

### Object: `CaveFamilyEnrage`


**Definition:** AI Trigger: Enrage logic triggered when a cave family member is killed.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 6 ||
| `count` | Array / Integer | The numerical quantity. | 6 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specific entity tag required. | 6 ||

</details>

---

### Object: `FormChangeWhilePrimingAbility`


**Definition:** Logic: Changes form while preparing/priming a specific ability.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`priming`](./Enums.md#enum-priming) | Enum || 6 ||
| [`not_priming`](./Enums.md#enum-not_priming) | Enum || 6 ||

</details>

---

### Object: `MoveTowardsDamageSource`


**Definition:** No definition provided.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum || 5 ||
| `move_far` | Boolean || 4 ||
| [`check_in_form`](./Enums.md#enum-check_in_form) | Enum || 2 ||
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| `can_move_zero` | Boolean || 1 ||
| [`check_has_status`](./Enums.md#enum-check_has_status) | Enum || 1 ||
| `do_not_move_on_top` | Boolean || 1 ||
| `face_towards_after` | Boolean || 1 ||
| [`ignore_tagged_sources`](./Enums.md#enum-ignore_tagged_sources) | Enum || 1 ||
| `move_short` | Boolean || 1 ||

</details>

---

### Object: `SecurityBotProtect`


**Definition:** AI Logic: Guarding behavior for Security Bot units.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 7 ||
| [`move`](./Enums.md#enum-move) | Enum || 5 ||
| `enemies_only` | Boolean || 3 ||
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum || 3 ||
| `not_on_kill` | Boolean || 2 ||

</details>

---

### Object: `HasCat`


**Definition:** Character Form: Behavior and stats for the \'HasCat\' state.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 5 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 5 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer || 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 4 ||

</details>

---

### Object: `MoveTowardsKillers`


**Definition:** No definition provided.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum || 3 ||
| [`character_filter`](./Arrays.md#array-character_filter) | Array || 3 ||

</details>

---

### Object: `PassiveWhileHasStatus`


**Definition:** Passive: Activates only while the character has the specified status.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 6 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 6 ||

</details>

---

### Object: `TransformOnDeathImmediately`


**Definition:** No definition provided.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum || 4 ||
| [`obj`](./Enums.md#enum-obj) | Array / Enum || 4 ||

</details>

---

### Object: `BaitAura`


**Definition:** Passive: Projects an aura that attracts specific enemy types (e.g., flies/maggots).  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `range` | Enum / Integer | Distance or area of effect in tiles. | 4 ||

</details>

---

### Object: `Big`


**Definition:** Character Form / AI State: Behavior and stats for the \'Big\' state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed || 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Consumed`


**Definition:** State object triggered when this object or entity is eaten/consumed by another character.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`statuses`](./Characters_and_Bosses.md#object-statuses)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`struggle_ability`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Ability triggered by the consumed entity while inside the consumer. | 17 ||
| `force_contact` | `Boolean` | If true, enforces physical overlap. | 15 ||
| `instant` | `Boolean` || 12 ||
| [`mount_mode`](./Engine_LogicKeys.md#valid-property-keys) | `String` | If true, treats the consumption as riding/mounting instead of eating. | 12 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 22 ||
| `do_not_pop_corpse` | `Boolean` || 11 ||
| [`drop_on_death`](./Engine_LogicKeys.md#valid-property-keys) | `String` || 11 ||
| `use_placeholder` | Boolean || 3 ||

</details>

---

### Object: `ForceUseAbility`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossHitCountdownBoris`](./Characters_and_Bosses.md#object-finalbosshitcountdownboris), [`FinalBossHitCountdownExplosive`](./Characters_and_Bosses.md#object-finalbosshitcountdownexplosive)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 5 ||
| `show_name` | Boolean || 2 ||

</details>

---

### Object: `Holy`


**Definition:** Character Form: Behavior and stats for the \'Holy\' state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `hot`


**Definition:** Visual effect indicator.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 4 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 4 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 4 ||

</details>

---

### Object: `MoveAway`


**Definition:** AI Movement: Moves away from the target.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 4 ||

</details>

---

### Object: `MoveClose`


**Definition:** AI Movement: Moves into melee range.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 4 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum || 3 ||

</details>

---

### Object: `OffMap`


**Definition:** Character Form: Behavior and stats for the 'OffMap' state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 3 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||

</details>

---

### Object: `passive`


**Definition:** Intrinsic passive modifier.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum || 2 ||

</details>

---

### Object: `StatusEachTurnEnd`


**Definition:** Applies or references the 'StatusEachTurnEnd' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 55 ||
| [`AllStatsUp`](./Enums.md) | Integer || 1 | 2 |
| [`Conditional_BadRoll`](Abilities_and_Spells.md#object-conditional_badroll) | Object || 1 ||
| [`DivineShield`](./Enums.md) | Integer || 1 | 2 |
| [`HealthGain`](./Enums.md) | Integer || 1 | 5 |
| [`SpeedUp`](./Enums.md) | Integer || 5 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 5 |

</details>

---

### Object: `StatusOnKill`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 34 ||
| [`HealthGain`](./Enums.md) | Integer || 5 | 5 |
| [`UseAbility_NonStack`](./Enums.md) | Enum || 3 | BBTransformZealot |

</details>

---

### Object: `StatusOnTookDamageFromAbility`


**Definition:** Event Trigger: Applies statuses when taking damage from an ability.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`Bleed`](./Enums.md) | Integer || 1 | 2 |
| [`ExtraBasicAttacks_Status`](./Enums.md) | Integer || 2 | 1 |
| [`HealthRegenUp`](./Enums.md) | Integer || 1 | 2 |
| [`TakeExtraTurn`](./Enums.md) | Integer || 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Object: `StunImmunity`


**Definition:** No definition provided.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean || 1 ||

</details>

---

### Object: `Trapper`


**Definition:** Character Form: Behavior and stats for the 'Trapper' state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 4 ||
| `cancel_movement` | Boolean || 2 ||
| `pathfinding_avoidance` | Integer || 2 ||
| `range` | Enum / Integer | Distance or area of effect in tiles. | 2 ||

</details>

---

### Object: `AllAlive`


**Definition:** Encounter State: Logic executed when all specific entities are currently alive.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `ArmorPickup`


**Definition:** Pickup Logic: Defines what happens when an armor item is collected.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 3 ||
| [`frame_range`](./Arrays.md#array-frame_range) | Array || 3 ||

</details>

---

### Object: `Bomb`


**Definition:** Character Form / AI State: Behavior and stats for the 'Bomb' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer || 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Buddy`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean || 3 ||
| [`obj`](./Enums.md#enum-obj) | Array / Enum || 3 ||
| `reclaim_if_lost` | Boolean || 1 ||

</details>

---

### Object: `Cat`


**Definition:** Character Form: Base form for standard cats.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#object-mothertumorpassive), [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#object-mothertumorspawnincapture)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum || 3 ||
| [`statuses`](#object-statuses) | Object | Status effects possessed by the character. | 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||

</details>

---

### Object: `CaveMan`


**Definition:** Character Form: Behavior and stats for the \'CaveMan\' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 2 ||

</details>

---

### Object: `Down`


**Definition:** Character Form: Behavior and stats for the \'Down\' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 3 ||

</details>

---

### Object: `Fire`


**Definition:** Character Form: Behavior and stats for the 'Fire' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `FormChangeHealthThreshold`


**Definition:** Logic: Changes form when health crosses a threshold.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_above`](./Enums.md#enum-form_above) | Enum || 3 ||
| [`form_below`](./Enums.md#enum-form_below) | Enum || 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| `count_shield` | Boolean || 1 ||
| [`threshold`](./Enums.md) | Enum / Integer || 3 | 200 |

</details>

---

### Object: `Full`


**Definition:** Character Form: Behavior and stats for the \'Full\' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 2 ||
| [`statuses_on_enter_form`](#object-statuses_on_enter_form) | Object | Status effects instantly applied upon transitioning into this form. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 2 ||

</details>

---

### Object: `ManaPickup`


**Definition:** Pickup Logic: Defines what happens when a mana item is collected.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 3 ||
| [`frame_range`](./Arrays.md#array-frame_range) | Array || 3 ||

</details>

---

### Object: `NonCat`


**Definition:** Character Form: Behavior and stats for the 'NonCat' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#object-mothertumorpassive), [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#object-mothertumorspawnincapture)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`formchange`](./Enums.md#enum-formchange) | Enum || 3 ||
| [`statuses`](#object-statuses) | Object | Status effects possessed by the character. | 2 ||
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||

</details>

---

### Object: `OneAlive`


**Definition:** Encounter State: Logic executed when exactly one target is alive.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 3 ||

</details>

---

### Object: `RandomPassivePool`


**Definition:** Logic: Grants a random passive from the specified pool upon spawning.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object || 1 ||
| [`PassiveGroup`](#object-passivegroup) | Object || 2 ||
| [`TransformInXTurns`](#object-transforminxturns) | Object || 1 ||

</details>

---

### Object: `ReplaceBrain`


**Definition:** Applies the 'ReplaceBrain' effect.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StacyMutant_Fire`](./Characters_and_Bosses.md#object-stacymutant_fire), [`StacyMutant_Ice`](./Characters_and_Bosses.md#object-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#object-stacymutant_lightning)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum || 4 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum || 4 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 4 ||
| [`pattern`](#object-pattern) | Object | AI sequence logic. | 3 ||

</details>

---

### Object: `SquirrelForm`


**Definition:** Character Form: Behavior and stats for the 'SquirrelForm' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 2 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum || 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 2 ||

</details>

---

### Object: `SupportFormChangeInsteadOfRun`


**Definition:** No definition provided.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| `wait_till_turn` | Boolean || 1 ||

</details>

---

### Object: `TwoAlive`


**Definition:** Encounter State: Logic executed when exactly two targets are alive.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 3 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 3 ||

</details>

---

### Object: `Up`


**Definition:** Character Form: Behavior and stats for the \'Up\' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 2 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 3 ||

</details>

---

### Object: `Water`


**Definition:** Character Form: Behavior and stats for the \'Water\' state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `AbilityOnRoundEnd`


**Definition:** AI Trigger: Executes an ability at the end of the combat round.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| `force_display_name` | Boolean || 2 ||

</details>

---

### Object: `AbilityWhenTaggedCharacterMovesNear`


**Definition:** AI Trigger: Executes an ability when a character with a specific tag moves adjacent.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 5 ||
| `range` | Enum / Integer | Distance or area of effect in tiles. | 5 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specific entity tag required. | 5 ||

</details>

---

### Object: `active`


**Definition:** Defines actively executed abilities.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddTemporaryEffectsToBasicAttack`


**Definition:** Applies the 'AddTemporaryEffectsToBasicAttack' effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fury` | Integer | Applies or references the 'Fury' effect/state. | 4 ||

</details>

---

### Object: `alternate_energized_effect`


**Definition:** Overrides default energized visuals.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Robot`](./Characters_and_Bosses.md#object-robot)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`FormChange`](./Enums.md) | Enum || 1 | Druid |
| [`SpellDamageUp`](./Enums.md) | Integer || 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `AutocastEachRound`


**Definition:** Forces the character to automatically cast a specific ability at the start of each combat round.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 9 ||
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 6 ||

</details>

---

### Object: `Bishop`


**Definition:** Character Form / AI State: Behavior and stats for the \'Bishop\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| `uifloaters_offset` | Number || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `BlackHole`


**Definition:** Character Form / AI State: Behavior and stats for the \'BlackHole\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Boris`


**Definition:** Character Form / AI State: Behavior and stats for the \'Boris\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `BungaEntrance`


**Definition:** Animation/AI State: Bunga entering the arena.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| `even_if_stunned` | Boolean || 2 ||
| `health_threshold` | Integer || 2 ||
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum || 2 ||

</details>

---

### Object: `CaveBaby`


**Definition:** Character Form: Behavior and stats for the \'CaveBaby\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `CaveManSpear`


**Definition:** Character Form: Behavior and stats for the \'CaveManSpear\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 2 ||

</details>

---

### Object: `CaveWoman`


**Definition:** Character Form: Behavior and stats for the \'CaveWoman\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `CherubimReaction`


**Definition:** Reaction: Custom reaction triggers for Cherubim enemies.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Leave`](Engine_LogicKeys.md#object-leave) | Enum / Object | Applies or references the 'Leave' effect/state. | 2 ||
| [`Return`](Engine_LogicKeys.md#object-return) | Enum / Object | Applies or references the 'Return' effect/state. | 2 ||

</details>

---

### Object: `Conditional_GoodRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ally_rewards`](./Characters_and_Bosses.md#object-ally_rewards)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 37 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 28 ||
| [`FindItemFromPool`](./Enums.md) | Enum || 5 | eagle_pool |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | 37 | |

</details>

---

### Object: `Cultist`


**Definition:** Character Form: Behavior and stats for the \'Cultist\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `DashRandomly`


**Definition:** AI Movement: Dashes to a random valid tile.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum || 2 ||

</details>

---

### Object: `DiesToElement`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 1 ||
| `instant` | `Boolean` || 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

---

### Object: `dispersed_bonusturn_pattern`


**Definition:** AI Logic: Alternative bonus turn ability pattern.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do`](./Enums.md#enum-do) | Enum || 2 ||

</details>

---

### Object: `Empty`


**Definition:** Character Form: Behavior and stats for the \'Empty\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 2 ||

</details>

---

### Object: `Escape`


**Definition:** AI Movement: Logic for fleeing or escaping the map.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 2 ||

</details>

---

### Object: `Explosive`


**Definition:** Character Form: Behavior and stats for the \'Explosive\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `FaceLastDamage`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean || 1 ||

</details>

---

### Object: `FireFull`


**Definition:** Character Form: Behavior and stats for the 'FireFull' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Flush`


**Definition:** Character Form: Behavior and stats for the 'Flush' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||

</details>

---

### Object: `FormChangeDuringWeatherElement`


**Definition:** Logic: Changes form automatically during specific weather conditions.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 2 ||
| [`form`](./Enums.md#enum-form) | Enum / Integer || 2 ||

</details>

---

### Object: `Holding`


**Definition:** Character Form: Behavior and stats for the \'Holding\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Johnny`


**Definition:** Character Form: Behavior and stats for the 'Johnny' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||

</details>

---

### Object: `KnockUpAndAway`


**Definition:** Displaces the target vertically and horizontally away from the source.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#object-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#object-conditional_isphysicalattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The distance in tiles to knock the target away. | 24 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 22 ||
| `displace` | Boolean || 2 ||
| [`self_damage`](./Enums.md) | Boolean / Integer || 2 | 2 |
| [{Damaging Keys}](./Engine_DamagingKeys.md#valid-property-keys) | Object | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Object: `LastHit`


**Definition:** Logic: Executes logic on the final hit of a multi-hit attack.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||

</details>

---

### Object: `MotherTumorSpawnInCapture`


**Definition:** Boss Logic: Logic for capturing entities inside the Mother's tumors upon spawning.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](#object-cat) | Object | Character Form: Base form for standard cats. | 2 ||
| [`NonCat`](#object-noncat) | Object | Character Form: Behavior and stats for the 'NonCat' state. | 2 ||
| [`Nothing`](#object-nothing) | Object | Character Form: Behavior and stats for the 'Nothing' state. | 1 ||

</details>

---

### Object: `MoveCenter`


**Definition:** AI Movement: Moves toward the center of the map.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 2 ||

</details>

---

### Object: `MoveForThrow`


**Definition:** AI Movement: Repositions to gain line of sight for throwing.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum || 2 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 2 ||

</details>

---

### Object: `Mutant`


**Definition:** Character Form: Behavior and stats for the \'Mutant\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move_speed_multiplier`](./Enums.md#enum-move_speed_multiplier) | Number || 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `NeutronStar`


**Definition:** Character Form: Behavior and stats for the 'NeutronStar' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `NotPriming`


**Definition:** Character Form: Behavior and stats when not charging an ability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `Nuke`


**Definition:** Character Form: Behavior and stats for the 'Nuke' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `PassiveWhileNotHasStatus`


**Definition:** Passive: Activates only while the character does NOT have the specified status.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 2 ||

</details>

---

### Object: `Priming`


**Definition:** Character Form: Behavior and stats when charging an ability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 2 ||

</details>

---

### Object: `ProtectTargetedAllies`


**Definition:** No definition provided.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| [`target_filter`](./Enums.md#enum-target_filter) | Enum || 2 ||

</details>

---

### Object: `Rain`


**Definition:** Character Form: Behavior and stats for the 'Rain' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||

</details>

---

### Object: `RemoveStatusStacks`


**Definition:** Removes a specific number of stacks of a status effect.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Characters_and_Bosses.md#object-statusonendmove), [`StatusOnTookDamage`](./Characters_and_Bosses.md#object-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | The number of stacks to remove. | 4 ||
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 4 ||

</details>

---

### Object: `SlotMachineRollPool`


**Definition:** Logic: Defines the possible outcomes for slot machine enemies.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SlotResult_Jackpot_Coins`](Engine_LogicKeys.md#object-slotresult_jackpot_coins) | Integer / Object | Applies or references the 'SlotResult_Jackpot_Coins' effect/state. | 2 ||
| [`SlotResult_Explode`](Engine_LogicKeys.md#object-slotresult_explode) | Integer / Object | Applies or references the 'SlotResult_Explode' effect/state. | 1 ||
| [`SlotResult_Nothing`](Engine_LogicKeys.md#object-slotresult_nothing) | Integer / Object | Applies or references the 'SlotResult_Nothing' effect/state. | 1 ||
| [`SlotResult_RandomPickup`](Engine_LogicKeys.md#object-slotresult_randompickup) | Integer / Object | Applies or references the 'SlotResult_RandomPickup' effect/state. | 1 ||

</details>

---

### Object: `Small`


**Definition:** Character Form: Behavior and stats for the \'Small\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||

</details>

---

### Object: `SpearRun`


**Definition:** AI Movement: Specific movement logic for Spear enemies.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 2 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum || 2 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 2 ||

</details>

---

### Object: `statuses_on_enter_form`


**Definition:** Status effects instantly applied upon transitioning into this form.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Full`](./Characters_and_Bosses.md#object-full)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusGroup`


**Definition:** Groups multiple status effects together for batch application.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Characters_and_Bosses.md#object-randomstatusfrompool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 6 ||
| [`FindItemFromPool`](./Enums.md) | Enum || 2 | eagle_pool |

</details>

---

### Object: `StatusOnSpawnIn`


**Definition:** Event Trigger: Applies statuses immediately when spawned.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnTookDamage`


**Definition:** Event Trigger: Applies nested statuses when took damage.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 38 ||
| [`ConstitutionUp`](./Enums.md) | Integer || 3 | -1 |
| [`RemoveStatusStacks`](Abilities_and_Spells.md#object-removestatusstacks) | Object || 1 ||
| [`StrengthUp`](./Enums.md) | Integer || 4 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 14 |

</details>

---

### Object: `TempPassiveUntilSettled`


**Definition:** Passive: Active only until the physics engine stops moving the character.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#object-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#object-conditional_isphysicalattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 ||
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object || 2 ||

</details>

---

### Object: `TinkererBasicAttackSwitching`


**Definition:** Logic: Allows Tinkerer to swap basic attacks.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveGroup`](./Characters_and_Bosses.md#object-passivegroup), [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum || 3 ||
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum || 3 ||

</details>

---

### Object: `TransformOnElementInfluencex`


**Definition:** Logic: Variant element influence transformation.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 2 ||
| [`object`](./Enums.md#enum-object) | Array / Enum || 2 ||

</details>

---

### Object: `Turtled`


**Definition:** Character Form: Behavior and stats for the 'Turtled' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 2 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer || 2 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 2 ||
| [`move`](./Enums.md#enum-move) | Enum || 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 2 ||

</details>

---

### Object: `WereMan`


**Definition:** Character Form: Behavior and stats for the \'WereMan\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Zealot`


**Definition:** Character Form: Behavior and stats for the \'Zealot\' state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `additional_statuses`


**Definition:** Generic statuses added to the character.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnOnDeath`](./Characters_and_Bosses.md#object-spawnondeath)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`PermanentMadness`](./Enums.md) | Integer || 1 | 1 |

</details>

---

### Object: `AddStatusToReceivedDamage`


**Definition:** Modifier: Applies a status effect whenever the character takes damage.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToSpells`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToTrampleDamage`


**Definition:** Applies the 'AddStatusToTrampleDamage' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenDead`](./Characters_and_Bosses.md#object-passivewhendead)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `AddStatusToWeapons`


**Definition:** Applies the 'AddStatusToWeapons' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`Bleed`](./Enums.md) | Integer || 3 | 2 |

</details>

---

### Object: `AdventureTokenPassivePool`


**Definition:** Map/Metaprogression: Pool of passive modifiers applied by adventure tokens.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`StacyMutant_Brace`](#object-stacymutant_brace) | Object || 1 ||
| [`StacyMutant_Counter`](#object-stacymutant_counter) | Object || 1 ||
| [`StacyMutant_Damage`](#object-stacymutant_damage) | Object || 1 ||
| [`StacyMutant_DoubleHead`](#object-stacymutant_doublehead) | Object || 1 ||
| [`StacyMutant_Fire`](#object-stacymutant_fire) | Object || 1 ||
| [`StacyMutant_Health`](#object-stacymutant_health) | Object || 1 ||
| [`StacyMutant_Holy`](#object-stacymutant_holy) | Object || 1 ||
| [`StacyMutant_Ice`](#object-stacymutant_ice) | Object || 1 ||
| [`StacyMutant_Lightning`](#object-stacymutant_lightning) | Object || 1 ||
| [`StacyMutant_Mirror`](#object-stacymutant_mirror) | Object || 1 ||
| [`StacyMutant_Speed`](#object-stacymutant_speed) | Object || 1 ||
| [`StacyMutant_Thorns`](#object-stacymutant_thorns) | Object || 1 ||

</details>

---

### Object: `AggroTargetIsGovernedByHitEffect`


**Definition:** AI Logic: Forces the character's aggro to follow specific hit effects rather than default proximity.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean || 1 ||

</details>

---

### Object: `ai_if_spawned_as_enemy`


**Definition:** AI logic override used only if the character is spawned as an enemy.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum || 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum || 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||
| [`pattern`](#object-pattern) | Object | AI sequence logic. | 1 ||

</details>

---

### Object: `Alert`


**Definition:** AI State: The behavior profile used when the character is alerted to enemies.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `AllStatsAura`


**Definition:** Passive: Projects an aura that modifies all primary stats of nearby characters.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aura_requires_tag`](./Enums.md#enum-aura_requires_tag) | Enum || 1 ||
| [`range`](./Enums.md#enum-range) | Enum / Integer | Distance or area of effect in tiles. | 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||

</details>

---

### Object: `Attacker`


**Definition:** AI Role: Designates the character as an attacker rather than support.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||

</details>

---

### Object: `BackflipWhenTargeted`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnGainCoins`](./Characters_and_Bosses.md#object-statusongaincoins)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific dodge ability to trigger (e.g., DestroyerDodge). | 7 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 7 ||

</details>

---

### Object: `BattlefieldUniqueRandomPassive`


**Definition:** Map Rule: Grants a unique random passive modifier to the battlefield.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Integer | Applies or references the 'DemonicGlyph_Bite' effect/state. | 1 ||
| `DemonicGlyph_Bounce` | Integer | Applies or references the 'DemonicGlyph_Bounce' effect/state. | 1 ||
| `DemonicGlyph_Fire` | Integer | Applies or references the 'DemonicGlyph_Fire' effect/state. | 1 ||
| `DemonicGlyph_Movement` | Integer | Applies or references the 'DemonicGlyph_Movement' effect/state. | 1 ||
| `DemonicGlyph_Summon` | Integer | Applies or references the 'DemonicGlyph_Summon' effect/state. | 1 ||

</details>

---

### Object: `BellyFull`


**Definition:** Character Form / AI State: Behavior and stats for the \'BellyFull\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `BigHolding`


**Definition:** Character Form / AI State: Behavior and stats for the \'BigHolding\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `BigHoldingCat`


**Definition:** Character Form / AI State: Behavior and stats for the \'BigHoldingCat\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Bully`


**Definition:** Character Form / AI State: Behavior and stats for the 'Bully' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `BungaCheers`


**Definition:** Animation/AI State: Bunga cheering animation logic.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ally_damage`](./Enums.md#enum-ally_damage) | Enum || 1 ||
| [`ally_dead`](./Enums.md#enum-ally_dead) | Enum || 1 ||
| [`enemy_damage`](./Enums.md#enum-enemy_damage) | Enum || 1 ||
| [`enemy_dead`](./Enums.md#enum-enemy_dead) | Enum || 1 ||
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum || 1 ||

</details>

---

### Object: `CaveWomanHasCat`


**Definition:** Character Form: Behavior and stats for the \'CaveWomanHasCat\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `CerberubsAggroTargetBehavior`


**Definition:** AI Logic: Custom aggro targeting rules for Cerberubs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alert_form`](./Enums.md#enum-alert_form) | Enum || 1 ||
| [`default_form`](./Enums.md#enum-default_form) | Enum || 1 ||

</details>

---

### Object: `CerberubsJumpBlind`


**Definition:** AI Logic: Blind jump attack pattern for Cerberubs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum || 1 ||

</details>

---

### Object: `CerberubsJumpNormal`


**Definition:** AI Logic: Normal jump attack pattern for Cerberubs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum || 1 ||

</details>

---

### Object: `ChanceToBackflip`


**Definition:** Applies or references the 'ChanceToBackflip' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 6 ||
| `chance` | Number | Probability (0.0 to 1.0) of executing this action. | 6 ||

</details>

---

### Object: `ChanceToFormChangeOnAbilityDamage`


**Definition:** Reaction: Probability to change forms when taking ability damage.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | Probability (0.0 to 1.0) of executing this action. | 1 ||
| [`form`](./Enums.md#enum-form) | Enum / Integer || 1 ||

</details>

---

### Object: `ChaosBossFormChangeGuide`


**Definition:** Boss Logic: Maps the form transition phases for the Chaos Boss.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `passives_health_threshold` | Integer || 1 ||
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array || 1 ||
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array || 1 ||

</details>

---

### Object: `ChaosBossPieces`


**Definition:** Boss Logic: Defines the separate destructible pieces of the Chaos Boss.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array || 1 ||
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array || 1 ||

</details>

---

### Object: `ChaosHeadDropIn`


**Definition:** Boss Logic: Drop-in attack/animation for the Chaos Head.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`new_music`](./Enums.md#enum-new_music) | Enum || 1 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specific entity tag required. | 1 ||

</details>

---

### Object: `Charging`


**Definition:** Character Form / AI State: Behavior when charging an attack.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Close`


**Definition:** AI Movement logic: Maneuvers into close/melee range.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `CloseConvert`


**Definition:** AI State: Logic for converting adjacent units.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `Conditional_BadRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized bad outcome probability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Characters_and_Bosses.md#object-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 ||
| [`Madness`](./Enums.md) | Integer || 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |

</details>

---

### Object: `Conditional_HasKnockback`


**Definition:** Conditional: Executes logic if the triggering attack deals knockback.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Characters_and_Bosses.md#object-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Logic: Applies vertical and horizontal displacement. | 1 ||
| `RemoveKnockback` | `Number` | Applies or references the 'RemoveKnockback' effect/state. | 1 ||
| [`TempPassiveUntilSettled`](#object-temppassiveuntilsettled) | Object | Passive: Active only until the physics engine stops moving the character. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

---

### Object: `Conditional_IsPhysicalAttack`


**Definition:** Conditional: Executes logic if the triggering attack is physical.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#object-addstatustoreceiveddamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Logic: Applies vertical and horizontal displacement. | 1 ||
| `RemoveKnockback` | `Number` | Applies or references the 'RemoveKnockback' effect/state. | 1 ||
| [`TempPassiveUntilSettled`](#object-temppassiveuntilsettled) | Object | Passive: Active only until the physics engine stops moving the character. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

---

### Object: `CounterAttack`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 5 ||
| `without_orienting` | Boolean || 1 ||

</details>

---

### Object: `CreateGlobalModifiers`


**Definition:** Generates global map or encounter rules/modifiers.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BloodRain` | `Number` | Applies or references the 'BloodRain' effect/state. | 3 ||
| [`LowerAmbientLight`](Abilities_and_Spells.md#object-lowerambientlight) | Object | Visual: Dims the map lighting. | 3 ||
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||

</details>

---

### Object: `Damaged`


**Definition:** Character Form / AI State: Behavior when health is critically low.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||

</details>

---

### Object: `Default_Ceiling`


**Definition:** Character Form: The baseline behavior state while attached to the ceiling.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `Default_Ground`


**Definition:** Character Form: The baseline behavior state while on the ground.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `DelayedAutoRevive`


**Definition:** Applies or references the 'DelayedAutoRevive' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer || 6 ||
| `rounds` | Integer || 6 ||

</details>

---

### Object: `DesireMech`


**Definition:** Character Form: Behavior and stats for the 'DesireMech' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||

</details>

---

### Object: `DiceBehavior`


**Definition:** AI Logic: Custom behavior for Dice enemies.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dice_size` | Integer || 1 ||
| `knockback_damage` | Integer || 1 ||

</details>

---

### Object: `Die`


**Definition:** Character Form / Logic: Forces the character to die.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `DiesToPiercingAndSpikes`


**Definition:** Vulnerability: Character dies instantly if hit by piercing attacks or spikes.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `deferred` | Boolean || 1 ||

</details>

---

### Object: `DodgeWhenTargeted`


**Definition:** Reaction: Executes a dodge maneuver when targeted.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||

</details>

---

### Object: `Drunker`


**Definition:** Character Form: Behavior and stats for the 'Drunker' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer || 1 ||

</details>

---

### Object: `DualSword`


**Definition:** Character Form: Behavior and stats for the \'DualSword\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| `move_speed_multiplier` | Number || 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `DualSword_Primed`


**Definition:** Character Form: Behavior and stats for the \'DualSword_Primed\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| `move_speed_multiplier` | Number || 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Dumb`


**Definition:** AI Profile: A simplified, less optimal decision-making profile.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `DybbukPossessionFallback`


**Definition:** Logic: Fallback state when a Dybbuk possession fails.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum || 1 ||
| [`form`](./Enums.md#enum-form) | Enum / Integer || 1 ||

</details>

---

### Object: `eat_damage`


**Definition:** Damage dealt when this entity consumes another.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherGrowController`](./Characters_and_Bosses.md#object-mothergrowcontroller)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cant_miss` | `Boolean` || 1 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 1 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging impact triggers. | 1 ||
| `makes_contact` | `Boolean` || 1 ||
| `piercing` | `Boolean` || 1 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 1 ||
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||

</details>

---

### Object: `Else`


**Definition:** Fallback object that executes if the preceding `Conditional_` block evaluated to false.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#object-addstatustoreceiveddamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 23 ||
| [`Conditional_HasKnockback`](#object-conditional_hasknockback) | Object | Conditional: Executes logic if the triggering attack deals knockback. | 1 ||
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Logic: Applies vertical and horizontal displacement. | 1 ||

</details>

---

### Object: `exit_animations`


**Definition:** Animations played when leaving a form/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Grappling`](./Characters_and_Bosses.md#object-grappling)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Default`](#object-default) | Enum / Object | Character Form: The baseline default behavior state. | 1 ||

</details>

---

### Object: `Explody`


**Definition:** Character Form: Behavior and stats for the 'Explody' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `FaceAwayLastDamage`


**Definition:** Reaction: Forces the character to face away from the last damage source.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean || 1 ||
| `override_hit_animation` | Boolean || 1 ||
| `use_turn_animations` | Boolean || 1 ||

</details>

---

### Object: `FightPhase`


**Definition:** Boss Logic: Main combat phase.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `FinalBossBeamQueue`


**Definition:** Boss Logic: Attack queue for the final boss beam.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`queue`](./Enums.md#enum-queue) | Enum || 1 ||
| [`release`](./Enums.md#enum-release) | Enum || 1 ||
| [`transform`](./Enums.md#enum-transform) | Enum || 1 ||

</details>

---

### Object: `FinalBossBecomeTheChild`


**Definition:** Boss Logic: Phase transition for the final boss.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`GlobalSpawnCharacter`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'GlobalSpawnCharacter' effect/state. | 1 ||
| `PlayBackground` | `Number` | Applies or references the 'PlayBackground' effect/state. | 1 ||
| [`SwitchMusic`](Abilities_and_Spells.md#object-switchmusic) | Object | Event Trigger: Changes background music track. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `FinalBossHitCountdownBoris`


**Definition:** Boss Logic: Countdown trigger for Boris.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon` | Integer || 1 ||
| `icon_ready` | Integer || 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`ForceUseAbility`](#object-forceuseability) | Enum / Object || 1 | CancerExplode |

</details>

---

### Object: `FinalBossHitCountdownExplosive`


**Definition:** Boss Logic: Countdown trigger for explosives.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon` | Integer || 1 ||
| `icon_ready` | Integer || 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`ForceUseAbility`](#object-forceuseability) | Enum / Object || 1 | CancerExplode |

</details>

---

### Object: `FinalBossHitCountdownHoly`


**Definition:** Boss Logic: Countdown trigger for holy attacks.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon` | Integer || 1 ||
| `icon_ready` | Integer || 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||

</details>

---

### Object: `FinalBossPupils`


**Definition:** Boss Logic: Pupil state management.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `radius` | Array / Integer | Distance or area of effect in tiles. | 1 ||
| [`reset_center_because_no_target_halflife`](./Enums.md#enum-reset_center_because_no_target_halflife) | Number || 1 ||
| [`reset_center_because_of_animation_halflife`](./Enums.md#enum-reset_center_because_of_animation_halflife) | Number || 1 ||
| [`teleport_tracking_halflife`](./Enums.md#enum-teleport_tracking_halflife) | Number || 1 ||
| [`tracking_acquisition_halflife`](./Enums.md#enum-tracking_acquisition_halflife) | Number || 1 ||
| [`look_at_offset`](./Arrays.md#array-look_at_offset) | Array || 1 ||
| [`virtual_head_position`](./Arrays.md#array-virtual_head_position) | Array || 1 ||

</details>

---

### Object: `FinalBossShieldHealth`


**Definition:** Boss Logic: Shield health management.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`break_ability`](./Enums.md#enum-break_ability) | Enum || 1 ||
| [`state_health`](./Arrays.md#array-state_health) | Array || 1 ||

</details>

---

### Object: `FinalBossSyncAnimations`


**Definition:** Boss Logic: Synchronizes multi-part boss animations.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`other_character`](./Enums.md#enum-other_character) | Enum || 1 ||
| [`other_form_change_abilities`](#object-other_form_change_abilities) | Object | Lists secondary abilities used to change forms. | 1 ||

</details>

---

### Object: `Flop`


**Definition:** Character Form: Behavior and stats for the \'Flop\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Flop2`


**Definition:** Character Form: Behavior and stats for the \'Flop2\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `FlushBubs`


**Definition:** Character Form: Behavior and stats for the 'FlushBubs' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `FlushHost`


**Definition:** Character Form: Behavior and stats for the 'FlushHost' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `FlushNettle`


**Definition:** Character Form: Behavior and stats for the 'FlushNettle' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `FoodMove`


**Definition:** AI Movement: Logic for seeking out food items.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `ForceTrample`


**Definition:** Logic: Forces movement to act as a trample attack.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum || 1 ||

</details>

---

### Object: `GainDisorderFromPool`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Characters_and_Bosses.md#object-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Number | Probability (0.0 to 1.0) of executing this action. | 1 ||
| [`pool`](./Enums.md#enum-pool) | Array / Enum || 1 ||

</details>

---

### Object: `Grappling`


**Definition:** Character Form / AI State: Behavior while grappling an opponent.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit_animations`](#object-exit_animations) | Object | Animations played when leaving a form/state. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer || 1 ||

</details>

---

### Object: `Grown`


**Definition:** Character Form: Behavior and stats for the \'Grown\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| `uifloaters_offset` | Number || 1 ||
| `weak_threshold` | Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `GuaranteedJackpot`


**Definition:** Loot Logic: Guarantees a high-tier drop.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `Guarding`


**Definition:** Character Form / AI State: Defensive behavior state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `HalfDead`


**Definition:** Character Form: Behavior and stats for the \'HalfDead\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `HasDeadCat`


**Definition:** Character Form: Behavior and stats for the \'HasDeadCat\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `HasRock`


**Definition:** Character Form: Behavior and stats for the \'HasRock\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||

</details>

---

### Object: `Headless`


**Definition:** Character Form: Behavior and stats for the \'Headless\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `HealNeighborsEachTurn`


**Definition:** Passive: Restores health to adjacent allies at the start of the turn.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean || 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||

</details>

---

### Object: `Hint_CrackedVisuals`


**Definition:** Visual: Overlay effects for cracked/damaged terrain or objects.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||

</details>

---

### Object: `Hint_CrackedVisuals2`


**Definition:** Visual: Secondary cracked visual overlay.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||

</details>

---

### Object: `Hint_CrackedVisuals3`


**Definition:** Visual: Tertiary cracked visual overlay.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||

</details>

---

### Object: `HitlerExecute`


**Definition:** Boss Logic: Specific execution or ultimate attack state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specific entity tag required. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`threshold`](./Enums.md) | Enum / Integer || 1 | 200 |

</details>

---

### Object: `HPAltStates`


**Definition:** Visual: Alternative sprite states based on current health.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`clipname`](./Enums.md#enum-clipname) | Enum || 1 ||
| [`thresholds`](./Arrays.md#array-thresholds) | Array || 1 ||

</details>

---

### Object: `HumanDead`


**Definition:** Character Form: Behavior and stats for the \'HumanDead\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||

</details>

---

### Object: `InfiniteRebirth`


**Definition:** Applies the 'InfiniteRebirth' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer || 3 ||
| `playercat_health` | Integer || 3 ||
| `immediate` | Boolean || 1 ||

</details>

---

### Object: `InitialPhase`


**Definition:** Boss Logic: The starting phase of an encounter.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Insane_Ceiling`


**Definition:** Character Form: Insane behavior state while attached to the ceiling.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Insane_Ground`


**Definition:** Character Form: Insane behavior state while on the ground.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `JohnnyBubs`


**Definition:** Character Form: Behavior and stats for the 'JohnnyBubs' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `JohnnyHost`


**Definition:** Character Form: Behavior and stats for the 'JohnnyHost' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `JohnnyNeedsWashing`


**Definition:** Character Form: Behavior and stats for the 'JohnnyNeedsWashing' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_unwashed`](./Enums.md#enum-form_unwashed) | Enum || 1 ||
| [`form_washed`](./Enums.md#enum-form_washed) | Enum || 1 ||

</details>

---

### Object: `JohnnyNettle`


**Definition:** Character Form: Behavior and stats for the 'JohnnyNettle' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Joystick`


**Definition:** Character Form: Behavior and stats for the \'Joystick\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `LeapClose`


**Definition:** AI Movement: Executes a jumping maneuver to close distance.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `Lifted`


**Definition:** Character Form: Behavior and stats for the \'Lifted\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Lit`


**Definition:** Character Form: Behavior and stats for the 'Lit' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `LowerAmbientLight`


**Definition:** A visual effect that dims the map's lighting.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CreateGlobalModifiers`](./Characters_and_Bosses.md#object-createglobalmodifiers)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `speed` | Array / Number | The transition speed. | 3 ||
| [`amount`](./Arrays.md#array-amount) | Array | The target opacity/dimness level. | 3 ||

</details>

---

### Object: `MegaDinoDropController`


**Definition:** Boss Logic: Manages loot drops for the Mega Dino.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`head_drop`](./Enums.md#enum-head_drop) | Enum || 1 ||
| [`leg_leave`](./Enums.md#enum-leg_leave) | Enum || 1 ||
| [`leg_return`](./Enums.md#enum-leg_return) | Enum || 1 ||
| `stable_legs` | Integer || 1 ||

</details>

---

### Object: `ModularPickup`


**Definition:** Pickup Logic: Defines what happens when a modular item is collected.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`sound_event`](./Enums.md#enum-sound_event) | Enum || 1 ||
| [`Cleanse`](./Enums.md) | Integer || 1 | 0 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `MonkCatReactionAbilities`


**Definition:** Reaction: Specific counter-attack or dodge abilities used by the Monk class.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`spell`](./Enums.md#enum-spell) | Enum || 1 ||
| [`trinket`](./Enums.md#enum-trinket) | Enum || 1 ||
| [`weapon`](./Enums.md#enum-weapon) | Enum | Weapon item constraint. | 1 ||

</details>

---

### Object: `MotherGrowController`


**Definition:** Boss Logic: Manages the growth phases of the Mother boss.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eat_damage`](#object-eat_damage) | Object | Damage dealt when this entity consumes another. | 1 ||
| [`tumor_object`](./Enums.md#enum-tumor_object) | Enum || 1 ||

</details>

---

### Object: `MotherTumorPassive`


**Definition:** Boss Logic: Passive effects applied to the Mother's tumors.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](#object-cat) | Object | Character Form: Base form for standard cats. | 1 ||
| [`grow_ability`](./Enums.md#enum-grow_ability) | Enum || 1 ||
| [`NonCat`](#object-noncat) | Object | Character Form: Behavior and stats for the 'NonCat' state. | 1 ||
| [`pass_ani`](./Enums.md#enum-pass_ani) | Enum || 1 ||
| [`receive_ani`](./Enums.md#enum-receive_ani) | Enum || 1 ||
| [`considered_forms`](./Arrays.md#array-considered_forms) | Array || 1 ||

</details>

---

### Object: `Mount`


**Definition:** Character Form: Behavior and stats for the 'Mount' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eject_ability`](./Enums.md#enum-eject_ability) | Enum || 1 ||
| [`enter_ability`](./Enums.md#enum-enter_ability) | Enum || 1 ||

</details>

---

### Object: `Mounted`


**Definition:** Character Form: Behavior and stats for the \'Mounted\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||

</details>

---

### Object: `MouthFull`


**Definition:** Character Form: Behavior and stats for the \'MouthFull\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `MoveAfterAnyAttemptedAttack`


**Definition:** AI Movement: Forces a move action immediately after attacking, even if it missed.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Array / Enum || 1 ||

</details>

---

### Object: `MoveAwayFromDamageSource`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum || 1 ||

</details>

---

### Object: `MoveAwayWhenEnemyAdjacent`


**Definition:** AI Movement: Moves away if an enemy enters an adjacent tile.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum || 1 ||
| `once_per_turn` | Boolean || 1 ||
| [`weights`](./Enums.md#enum-weights) | Array / Enum || 1 ||

</details>

---

### Object: `MoveForBarrage`


**Definition:** AI Movement: Repositions to optimize a barrage attack.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum || 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `MoveForDash`


**Definition:** AI Movement: Repositions to set up a dash attack line.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum || 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `MoveForGrass`


**Definition:** AI Movement: Moves toward grass tiles.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum || 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `MoveForPounce`


**Definition:** AI Movement: Repositions to optimize a pounce trajectory.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum || 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `MoveForSpin`


**Definition:** AI Movement: Repositions into a cluster of enemies for a spin attack.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum || 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `MoveOneForPuke`


**Definition:** AI Movement: Specific positioning logic for puke attacks.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum || 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `MoveSpaced`


**Definition:** AI Movement: Moves to maintain a specific distance from targets.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `MoveToHead`


**Definition:** AI Movement: Navigates toward the 'head' or primary target.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum || 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `MoveTowards`


**Definition:** AI Movement: Moves toward the nearest target.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum || 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `MultiSpawnOnDeath`


**Definition:** Event Trigger: Spawns multiple entities upon death.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`obj`](./Enums.md#enum-obj) | Array / Enum || 1 ||
| [`count`](./Arrays.md#array-count) | Array / Integer | The numerical quantity. | 1 ||

</details>

---

### Object: `NCGravecrawlFAR`


**Definition:** AI Movement: Specific grapple/crawl logic.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `NoEyes`


**Definition:** Character Form: Behavior and stats for the \'NoEyes\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||

</details>

---

### Object: `NormalFull`


**Definition:** Character Form: Behavior and stats for the 'NormalFull' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `NoStick`


**Definition:** Character Form: Behavior and stats for the 'NoStick' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||

</details>

---

### Object: `Nothing`


**Definition:** Character Form: Behavior and stats for the 'Nothing' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorSpawnInCapture`](./Characters_and_Bosses.md#object-mothertumorspawnincapture)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||

</details>

---

### Object: `Obey`


**Definition:** AI State: Enforced compliance logic (e.g., when Charmed).  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Off`


**Definition:** Character Form: Behavior and stats for the 'Off' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer || 1 ||

</details>

---

### Object: `OffScreen`


**Definition:** Character Form: Behavior and stats for the 'OffScreen' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `OneEye`


**Definition:** Character Form: Behavior and stats for the \'OneEye\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Open`


**Definition:** Character Form: Behavior and stats for the 'Open' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `OpenCat`


**Definition:** Character Form: Behavior and stats for the 'OpenCat' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `other_form_change_abilities`


**Definition:** Lists secondary abilities used to change forms.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossSyncAnimations`](./Characters_and_Bosses.md#object-finalbosssyncanimations)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Boris`](#object-boris) | Enum / Object | Character Form / AI State: Behavior and stats for the 'Boris' state. | 1 ||
| [`Explosive`](#object-explosive) | Enum / Object | Character Form: Behavior and stats for the 'Explosive' state. | 1 ||
| [`Holy`](#object-holy) | Enum / Object | Character Form: Behavior and stats for the 'Holy' state. | 1 ||

</details>

---

### Object: `Out`


**Definition:** Character Form: Behavior and stats for the 'Out' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `PassiveWhenAffectedByElement`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specific element type required or applied. | 18 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 18 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 18 ||

</details>

---

### Object: `PassiveWhenDead`


**Definition:** State Trigger: Grants passives when this condition is met.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `Possessing`


**Definition:** Character Form: Behavior and stats for the \'Possessing\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Primed`


**Definition:** Character Form: Behavior and stats for the 'Primed' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Pulp2`


**Definition:** Character Form: Behavior and stats for the 'Pulp2' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| `uifloaters_offset` | Number || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Pulp3`


**Definition:** Character Form: Behavior and stats for the 'Pulp3' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| `uifloaters_offset` | Number || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Pulp4`


**Definition:** Character Form: Behavior and stats for the 'Pulp4' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| `uifloaters_offset` | Number || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Pulp5`


**Definition:** Character Form: Behavior and stats for the 'Pulp5' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| `uifloaters_offset` | Number || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Pulp6`


**Definition:** Character Form: Behavior and stats for the 'Pulp6' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| `uifloaters_offset` | Number || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Pulp7`


**Definition:** Character Form: Behavior and stats for the 'Pulp7' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `animation_suffix` | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`tooltip`](./Enums.md#enum-tooltip) | Enum || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| `uifloaters_offset` | Number || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `RandomStatusFromPool`


**Definition:** Selects and applies a random status effect from the provided nested object.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ally_rewards`](./Characters_and_Bosses.md#object-ally_rewards)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 33 ||
| [`StatusGroup`](Abilities_and_Spells.md#object-statusgroup) | Object || 3 ||

</details>

---

### Object: `ReturnA`


**Definition:** Boss Logic: Specific phase return trigger.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `RevengeDamage`


**Definition:** Reaction trigger: Deals damage to the attacker when hit.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 8 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 5 ||
| `knockback` | Enum / Integer || 3 ||

</details>

---

### Object: `round_start_bonusturn_pattern`


**Definition:** AI Logic: Ability usage pattern during round-start bonus turns.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#object-ai)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`do_priority`](./Arrays.md#array-do_priority) | Array || 1 ||

</details>

---


<details>
<summary><b>AddStatusToReceivedDamage</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>AddStatusToSpells</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>AddStatusToTrampleDamage</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>PassiveWhenDead</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>StatusOnEnemyConfused</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

<details>
<summary><b>StatusOnSpawnIn</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

### Object: `RunFar`


**Definition:** AI Movement: Maximize distance from targets.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `RunWhenLastPlayerCatIsCharmed`


**Definition:** AI Logic: Flee logic when the player team is entirely crowd-controlled.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean || 1 ||
| [`legacy_savekey`](./Enums.md#enum-legacy_savekey) | Enum || 1 ||

</details>

---

### Object: `ScalingAttackAnimation`


**Definition:** Visual: Animation scales based on damage output.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`default`](#object-default) | Enum / Object | Baseline configuration. | 1 ||
| [`thresholds`](./Arrays.md#array-thresholds) | Array || 1 ||

</details>

---

### Object: `SharePickups`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_coins` | Boolean || 1 ||

</details>

---

### Object: `Sitting`


**Definition:** Character Form: Behavior and stats for the 'Sitting' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `SkipFirstRounds`


**Definition:** AI Logic: Passes turn for the first X rounds of combat.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pop_chance` | Integer || 1 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 1 ||

</details>

---

### Object: `SmallHolding`


**Definition:** Character Form: Behavior and stats for the \'SmallHolding\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `SmallHoldingCat`


**Definition:** Character Form: Behavior and stats for the \'SmallHoldingCat\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `SpawningPhase`


**Definition:** Boss Logic: Phase focused on summoning minions.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `SpewerAltGraphics`


**Definition:** Visual: Alternative graphics for Spewer enemies.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Fire`](#object-fire) | Integer / Object | Character Form: Behavior and stats for the 'Fire' state. | 1 ||
| [`FireFull`](#object-firefull) | Integer / Object | Character Form: Behavior and stats for the 'FireFull' state. | 1 ||
| [`Normal`](#object-normal) | Integer / Object | Character Form: Behavior and stats for the 'Normal' state. | 1 ||
| [`NormalFull`](#object-normalfull) | Integer / Object | Character Form: Behavior and stats for the 'NormalFull' state. | 1 ||
| [`Tar`](#object-tar) | Integer / Object | Character Form: Behavior and stats for the 'Tar' state. | 1 ||
| [`TarFull`](#object-tarfull) | Integer / Object | Character Form: Behavior and stats for the 'TarFull' state. | 1 ||

</details>

---

### Object: `StacyMutant_Brace`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Brace' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Brace`](./Enums.md) | Integer || 1 | 99 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Counter`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Counter' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object || 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 1 ||
| [`CounterAttack`](Cat_Mutations.md#object-counterattack) | Array / Enum / Object || 1 | [GSScream] |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Damage`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Damage' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`AddDamage`](./Enums.md) | Integer || 1 | 2 |
| [`AddMaxHealth`](./Enums.md) | Integer || 1 | -25 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_DoubleHead`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_DoubleHead' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 1 ||
| [`ExtraDispersedTurns`](./Enums.md) | Integer || 1 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Fire`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Fire' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 1 ||
| [`ElementImmune`](./Enums.md) | Enum || 1 | Ice |
| [`ReplaceBasicAttack`](./Enums.md) | Enum || 1 | BasicStraightShot |
| [`ReplaceBrain`](#object-replacebrain) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Health`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Health' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`AddMaxHealth`](./Enums.md) | Integer || 1 | -25 |
| [`AddSpeed`](./Enums.md) | Integer || 1 | 6 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 1 ||
| [`SizeScale`](./Enums.md) | Number || 1 | .8 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Holy`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Holy' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 1 ||
| [`DivineShield`](./Enums.md) | Integer || 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Ice`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Ice' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`AddMovement`](./Enums.md) | Integer || 1 | 2 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 1 ||
| [`ElementImmune`](./Enums.md) | Enum || 1 | Ice |
| [`ReplaceBasicAttack`](./Enums.md) | Enum || 1 | BasicStraightShot |
| [`ReplaceBrain`](#object-replacebrain) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Lightning`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Lightning' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 1 ||
| [`ElementImmune`](./Enums.md) | Enum || 1 | Ice |
| [`ReplaceBasicAttack`](./Enums.md) | Enum || 1 | BasicStraightShot |
| [`ReplaceBrain`](#object-replacebrain) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Mirror`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Mirror' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 1 ||
| [`ReflectProjectiles`](#object-reflectprojectiles) | Integer / Object || 1 | 100 |
| [`StatusEachTurnEndForEachTurn`](#object-statuseachturnendforeachturn) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Speed`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Speed' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`AddDamage`](./Enums.md) | Integer || 1 | 2 |
| [`AddSpeed`](./Enums.md) | Integer || 1 | 6 |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 1 ||
| [`SizeScale`](./Enums.md) | Number || 1 | .8 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StacyMutant_Thorns`


**Definition:** Character Form: Behavior and stats for the 'StacyMutant_Thorns' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AdventureTokenPassivePool`](./Characters_and_Bosses.md#object-adventuretokenpassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 1 ||
| [`Thorns`](./Enums.md) | Integer || 1 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `Standing`


**Definition:** Character Form: Behavior and stats for the 'Standing' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Standing2`


**Definition:** Character Form: Behavior and stats for the 'Standing2' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||
| [`turns`](#object-turns) | Array / Integer / Object | Turn counter tracking. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Start_Ceiling`


**Definition:** Character Form: Behavior and stats for the 'Start_Ceiling' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `StatusAfterXTurns`


**Definition:** Event Trigger: Applies a status effect after X turns have passed.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 2 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 ||
| [`ForceUseAbility`](#object-forceuseability) | Enum / Object || 2 | CancerExplode |

</details>

---

### Object: `StatusEachTurnBeginIfHasStatus`


**Definition:** Event Trigger: Applies a status at the start of the turn if a prerequisite status is met.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum || 1 ||
| `consume` | Boolean || 1 ||
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`AllStatsUp`](./Enums.md) | Integer || 1 | 2 |
| [`DamageUp`](./Enums.md) | Integer || 1 | 2 |
| [`HealthGain`](./Enums.md) | Integer || 1 | 5 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Object: `StatusEachTurnEndForEachTurn`


**Definition:** Event Trigger: Applies nested statuses to each turn end for each turn.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StacyMutant_Mirror`](./Characters_and_Bosses.md#object-stacymutant_mirror)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 ||
| [`RandomMagicMissile`](./Enums.md) | Integer || 3 | 1 |

</details>

---

### Object: `StatusEachTurnEndIfEnabledAtStartOfTurn`


**Definition:** Event Trigger: Applies a status at the end of the turn if an enabling condition was met at the start.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`ForceUseAbility`](#object-forceuseability) | Enum / Object || 1 | CancerExplode |

</details>

---

### Object: `StatusOnDie`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 9 ||
| [`RemoveAmbientLightEffects`](./Enums.md) | Integer || 1 | 4 |
| [`RemoveGlobalModifiers`](./Enums.md) | Array || 1 | [BloodRain] |

</details>

---

### Object: `StatusOnEndMove`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnEnemyConfused`


**Definition:** Event Trigger: Applies statuses when an enemy becomes confused.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnGainCoins`


**Definition:** Event Trigger: Applies nested statuses when gain coins.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 5 ||
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Object || 1 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `StatusOverlappingCharactersAndDie`


**Definition:** Event Trigger: Applies statuses to overlapping entities, then destroys self.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`Poison`](./Enums.md) | Integer || 1 | 2 |

</details>

---

### Object: `StatusWhenStatusCompletelyRemoved`


**Definition:** Event Trigger: Applies statuses when a tracked status effect is fully cleansed.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object || 1 | KirbySpit |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `Stop`


**Definition:** AI Movement: Forces the character to cease movement.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `SuckMF`


**Definition:** Character Form: Behavior and stats for the 'SuckMF' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum || 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `SupportDieInsteadOfRun`


**Definition:** AI Logic: Forces a support unit to die rather than flee.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_dead_ani`](./Enums.md#enum-alt_dead_ani) | Enum || 1 ||
| [`alt_dying_ani`](./Enums.md#enum-alt_dying_ani) | Enum || 1 ||

</details>

---

### Object: `SwimmingFormChange`


**Definition:** Logic: Automates form change when entering/exiting water.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_in`](./Enums.md#enum-form_in) | Enum || 1 ||
| [`form_out`](./Enums.md#enum-form_out) | Enum || 1 ||

</details>

---

### Object: `SwitchMusic`


**Definition:** Changes the background music track or layer during combat.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossBecomeTheChild`](./Characters_and_Bosses.md#object-finalbossbecomethechild)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | The specific audio layer to transition to (e.g., map, battle). | 7 ||
| [`new_song`](./Enums.md#enum-new_song) | Enum | The ID of the new music track. | 6 ||

</details>

---

### Object: `SwordAndShield`


**Definition:** Character Form: Behavior and stats for the 'SwordAndShield' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `SwordAndShield_Primed`


**Definition:** Character Form: Behavior and stats for the \'SwordAndShield_Primed\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `SyncFormsWithBuddy`


**Definition:** Logic: Forces this character's form to match their familiar/buddy.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`no_buddy`](./Enums.md#enum-no_buddy) | Enum || 1 ||

</details>

---

### Object: `T3HitlerSpawningPhase`


**Definition:** Boss Logic: Minion spawn phase for the T3 Hitler boss.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spell_use_groups`](./Arrays.md#array-spell_use_groups) | Array || 1 ||

</details>

---

### Object: `Tar`


**Definition:** Character Form: Behavior and stats for the 'Tar' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `TarFull`


**Definition:** Character Form: Behavior and stats for the 'TarFull' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Terminator2Run`


**Definition:** AI Movement: Specific run logic for Terminator2.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum || 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `TerminatorChase`


**Definition:** AI Movement: Specific chase logic for Terminator.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move`](./Enums.md#enum-move) | Enum || 1 ||

</details>

---

### Object: `TerminatorSkin`


**Definition:** Visual: Skin definition for Terminator.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 ||
| [`groups`](./Arrays.md#array-groups) | Array || 1 ||

</details>

---

### Object: `TF_TargetAllies`


**Definition:** AI Targeting: Prioritizes allies.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum || 1 ||

</details>

---

### Object: `TF_TargetEnemies`


**Definition:** AI Targeting: Prioritizes enemies.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum || 1 ||

</details>

---

### Object: `Throb`


**Definition:** Character Form: Behavior and stats for the 'Throb' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||

</details>

---

### Object: `ThrobBubs`


**Definition:** Character Form: Behavior and stats for the 'ThrobBubs' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `ThrobHost`


**Definition:** Character Form: Behavior and stats for the 'ThrobHost' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `ThrobNettle`


**Definition:** Character Form: Behavior and stats for the 'ThrobNettle' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Transformed`


**Definition:** Character Form: Behavior and stats for the 'Transformed' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Object: `TransformOnStatusThreshold`


**Definition:** Logic: Changes form when a status effect reaches a certain stack count.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum || 1 ||
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`threshold`](./Enums.md) | Enum / Integer || 1 | 200 |

</details>

---

### Object: `TVBotScreen`


**Definition:** Visual: TV Bot screen state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Die` | `Number` | Character Form / Logic: Forces the character to die. | 1 ||
| [`Dumb`](#object-dumb) | Integer / Object | AI Profile: A simplified, less optimal decision-making profile. | 1 ||
| `Fuck` | Integer | Applies or references the 'Fuck' effect/state. | 1 ||
| [`Obey`](#object-obey) | Integer / Object | AI State: Enforced compliance logic (e.g., when Charmed). | 1 ||
| `Shit` | Integer | Applies or references the 'Shit' effect/state. | 1 ||
| [`Stop`](#object-stop) | Integer / Object | AI Movement: Forces the character to cease movement. | 1 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 ||

</details>

---

### Object: `TwisterFling`


**Definition:** Logic: Fling behavior for tornado attacks.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 1 ||
| `max_dist` | Integer || 1 ||
| `min_dist` | Integer || 1 ||

</details>

---

### Object: `TwoEyes`


**Definition:** Character Form: Behavior and stats for the 'TwoEyes' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `Unflip`


**Definition:** Logic: Reverses a flipped state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`virtual_abilities`](./Characters_and_Bosses.md#object-virtual_abilities)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`move_for_ability`](./Enums.md#enum-move_for_ability) | Enum || 1 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum || 1 ||

</details>

---

### Object: `UnlimitedDeathRattleRevive`


**Definition:** Logic: Endless resurrection on death.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| `even_if_stunned` | Boolean || 1 ||

</details>

---

### Object: `Unlit`


**Definition:** Character Form: Behavior and stats for the 'Unlit' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Unwashed`


**Definition:** Character Form: Behavior and stats for the 'Unwashed' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer || 1 ||

</details>

---

### Object: `UseAbility`


**Definition:** Forces the character or target to instantly use a specified ability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusWhenStatusCompletelyRemoved`](./Characters_and_Bosses.md#object-statuswhenstatuscompletelyremoved)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger. | 2 ||
| `respect_prime` | Boolean | If true, respects the ability's prime/cooldown state. | 2 ||

</details>

---

### Object: `UseAbilityWhenOutOfStatus`


**Definition:** Logic: Casts a specific ability the moment a status effect expires.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to cast. | 1 ||
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 1 ||

</details>

---

### Object: `Washed`


**Definition:** Character Form: Behavior and stats for the 'Washed' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `Washer`


**Definition:** Character Form: Behavior and stats for the \'Washer\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`partial_animation_suffix`](./Strings.md#string-partial_animation_suffix) | Enum / Integer || 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---

### Object: `ZealotBomb`


**Definition:** Character Form: Behavior and stats for the \'ZealotBomb\' state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#object-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ai`](#object-ai) | Object | Core block defining the AI behavior logic and weights. | 1 ||
| [`animation_suffix`](./Strings.md#string-animation_suffix) | Enum / Integer || 1 ||
| [`attack`](./Enums.md#enum-attack) | Enum || 1 ||
| [`name`](./Strings.md#string-name) | Enum | Localization key for the character's name. | 1 ||
| [`tooltip`](./Strings.md#string-tooltip) | Enum || 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object || 1 ||

</details>

---


---

## Auto-Discovered Objects


### Object: `BoneWormShotSmall`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>
