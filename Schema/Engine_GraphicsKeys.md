# Mewgenics Mod Developer Documentation: Engine: Graphics Block

## Engine: Graphics Block

This document defines the `graphics {}` schema. This block configures all visual and animation properties for an ability, character, or class. It is shared across Abilities & Spells, Characters & Bosses, and Cat Classes.

> **Referenced by:** [`graphics` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-graphics), [`graphics` (Cat_Classes)](./Cat_Classes.md#context-graphics), [`graphics` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-graphics)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | The primary flash animation label triggered. | 1559 |
| `name` | String | Localization key for the character's name. | 517 |
| [`particle`](./Enums.md#enum-particle) | Enum | References an impact or cast particle effect. | 488 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  | 460 |
| `tooltip` | String |  | 409 |
| `true` | Variable |  | 336 |
| [`projectile`](./Enums.md#enum-projectile) | Enum | References a projectile entity. | 228 |
| `shadow_size` | Float |  | 151 |
| `scale` | Float |  | 149 |
| `uifloaters_offset` | Float |  | 149 |
| `lob` | Boolean |  | 130 |
| [`custom_cat_data`](./Enums.md#enum-custom_cat_data) | Enum |  | 127 |
| `_CAT` | Variable |  | 120 |
| `none` | Variable |  | 116 |
| `delay` | Float | Frame delay before firing projectile/effect. | 93 |
| `dont_visualize_ai` | Boolean |  | 86 |
| `dont_orient` | Boolean | Prevents the character from turning to face the target. | 83 |
| [`water_mask`](./Enums.md#enum-water_mask) | Enum |  | 83 |
| [`dash_animation`](./Enums.md#enum-dash_animation) | Enum | State-specific animations for trample/dash abilities. | 65 |
| [`dash_start_animation`](./Enums.md#enum-dash_start_animation) | Enum |  | 63 |
| `speed` | Float | Rotations per second. | 61 |
| [`affected_particle`](./Enums.md#enum-affected_particle) | Enum | Visuals applied to the target receiving the effect. | 51 |
| [`dash_attack_animation`](./Enums.md#enum-dash_attack_animation) | Enum |  | 45 |
| `lob_height` | Integer | Adjustments for arcing projectiles. | 45 |
| [`animation_in`](./Enums.md#enum-animation_in) | Enum | Used for transition states (like burrowing). | 43 |
| [`animation_out`](./Enums.md#enum-animation_out) | Enum | Used for transition states (like burrowing). | 43 |
| `dash` | Variable |  | 40 |
| `dashstart` | Variable |  | 40 |
| [`jump_attack_animation`](./Enums.md#enum-jump_attack_animation) | Enum | Overrides for jump physics. | 39 |
| [`{Damaging Keys}`](./Engine_DamageKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 38 |
| `spawnin_animation` | String |  | 37 |
| `shoot` | Variable |  | 35 |
| `use_projectile` | Boolean |  | 35 |
| `Explosion` | Variable |  | 33 |
| `palette` | Integer | Swaps the color palette ID. | 33 |
| `square` | Variable |  | 29 |
| `attack` | Variable |  | 28 |
| `piece_alt_frame` | Integer |  | 27 |
| [`full_jump_animation`](./Enums.md#enum-full_jump_animation) | Enum |  | 24 |
| `full_jump_sync_frames` | Integer |  | 24 |
| `throwobject` | Variable |  | 24 |
| `use_rotation` | Boolean |  | 24 |
| [`shadow`](./Enums.md#enum-shadow) | Enum |  | 23 |
| `shadowStepOut` | Variable |  | 23 |
| `weaponthrowhigh` | Variable |  | 23 |
| [`dash_end_animation`](./Enums.md#enum-dash_end_animation) | Enum |  | 22 |
| `floatingmagic` | Variable |  | 22 |
| `Bullet` | Variable |  | 21 |
| `MagicMissleBlast` | Variable |  | 21 |
| `full_jump_windup_frames` | Integer |  | 20 |
| `medmed` | Variable |  | 20 |
| `move_speed_sync_frames` | Float |  | 20 |
| `weaponshoot` | Variable |  | 20 |
| `Bolt` | Variable |  | 19 |
| `medium` | Variable |  | 18 |
| `visual_delay_but_simultaneous_damage` | Integer |  | 18 |
| `weaponthrowstraight` | Variable |  | 18 |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum | Specific spawn points for particles. | 17 |
| `no_splatter` | Boolean |  | 17 |
| `PoisonPoof` | Variable |  | 16 |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum | Specific spawn points for particles. | 16 |
| `fall_from_sky` | Boolean | Spawns the projectile from the top of the screen. | 16 |
| `move_speed_multiplier` | Float |  | 16 |
| `pointout` | Variable |  | 16 |
| `throw` | Variable |  | 16 |
| `dont_sink` | Boolean |  | 14 |
| [`move_start_animation`](./Enums.md#enum-move_start_animation) | Enum |  | 14 |
| `throwArrow` | Variable |  | 14 |
| `use_placeholder` | Variable |  | 14 |
| `fx_windSpell` | Variable |  | 13 |
| [`move_end_animation`](./Enums.md#enum-move_end_animation) | Enum |  | 13 |
| [`portrait_face`](./Enums.md#enum-portrait_face) | Enum |  | 13 |
| `Wave` | Variable |  | 12 |
| `face_toss_target` | Boolean |  | 12 |
| `ignore_slowtiles` | Boolean |  | 12 |
| `sing3` | Variable |  | 12 |
| `chain_distance` | Float | Creates a tethered repeating graphic (like a hook). | 11 |
| [`chain_movieclip`](./Enums.md#enum-chain_movieclip) | Enum | Creates a tethered repeating graphic (like a hook). | 11 |
| `darken_screen` | Boolean | Dims the background during the ability cast. | 11 |
| `weaponspell3` | Variable |  | 11 |
| `IcePoof` | Variable |  | 10 |
| `MagicMissileProjectile` | Variable |  | 10 |
| [`beam_cap`](./Enums.md#enum-beam_cap) | Enum | Flash movieclips used to render continuous laser beams. | 10 |
| [`beam_clip`](./Enums.md#enum-beam_clip) | Enum | Flash movieclips used to render continuous laser beams. | 10 |
| `big` | Variable |  | 10 |
| `bounce_on_hit` | Boolean | Visual hop when striking a target. | 10 |
| `darken_screen_exclude_characters_on_tile` | Boolean |  | 10 |
| [`end`](./Enums.md#enum-end) | Enum | Segments for continuous channeled animations. | 10 |
| `howl` | Variable |  | 10 |
| [`jump_start_animation`](./Enums.md#enum-jump_start_animation) | Enum |  | 10 |
| [`loop`](./Enums.md#enum-loop) | Enum | Segments for continuous channeled animations. | 10 |
| [`prime_animation`](./Enums.md#enum-prime_animation) | Enum |  | 10 |
| `source_weapon` | Variable |  | 10 |
| [`start`](./Enums.md#enum-start) | Enum | Segments for continuous channeled animations. | 10 |
| `BigMagicMissileBlast` | Variable |  | 9 |
| `FireBlastMushroom` | Variable |  | 9 |
| `Holybeam` | Variable |  | 9 |
| `SmallRock` | Variable |  | 9 |
| `digDown` | Variable |  | 9 |
| `fx_statup` | Variable |  | 9 |
| `max_tiles_single_loop` | Integer |  | 9 |
| `sync_speed` | Integer |  | 9 |
| `BoneProjectile` | Variable |  | 8 |
| `ChainLink` | Variable |  | 8 |
| `Earthquake` | Variable |  | 8 |
| [`dying`](./Enums.md#enum-dying) | Enum |  | 8 |
| `fx_is_placeholder_animation` | Boolean |  | 8 |
| `headbuttdash` | Variable |  | 8 |
| `headbuttdashStart` | Variable |  | 8 |
| `roll` | Variable |  | 8 |
| `HookProjectile` | Variable |  | 7 |
| `aoe_spell_on_land` | Boolean | Visual trigger when a jump lands. | 7 |
| `art_flip` | Integer |  | 7 |
| `earthquakeSlam` | Variable |  | 7 |
| `fx_random_flip` | Boolean |  | 7 |
| `fx_tentaclestrangle` | Variable |  | 7 |
| `fx_tentaclestrangleMiss` | Variable |  | 7 |
| [`land_animation`](./Enums.md#enum-land_animation) | Enum |  | 7 |
| [`miss_particle`](./Enums.md#enum-miss_particle) | Enum | Specific spawn points for particles. | 7 |
| `shadowStepIn` | Variable |  | 7 |
| `spit` | Variable |  | 7 |
| `startroll` | Variable |  | 7 |
| `use_super_armor` | Boolean | Prevents flinch animations from interrupting this cast. | 7 |
| [`air_animation`](./Enums.md#enum-air_animation) | Enum | Animation played while entity is airborne. | 6 |
| [`custom_priming_animation`](./Enums.md#enum-custom_priming_animation) | Enum | Animation used while charging an ability. | 6 |
| `darken_screen_exclude_self` | Boolean |  | 6 |
| `darken_screen_start_early` | Boolean |  | 6 |
| `dashend` | Variable |  | 6 |
| `depth_offset` | Float |  | 6 |
| `explode` | Variable |  | 6 |
| `fall_randomize_timing` | Float |  | 6 |
| `min_throw_height` | Float |  | 6 |
| `pray` | Variable |  | 6 |
| `single_projectile` | Boolean |  | 6 |
| `DamageTrap` | Variable |  | 5 |
| `FireBlastSmall` | Variable |  | 5 |
| `FireSpin` | Variable |  | 5 |
| `HealBig` | Variable |  | 5 |
| `HealMed` | Variable |  | 5 |
| `None` | Variable |  | 5 |
| [`detatched_animation`](./Enums.md#enum-detatched_animation) | Enum | Plays an animation separated from the character body. | 5 |
| `detatched_animation_reach` | Integer |  | 5 |
| `empty` | Variable |  | 5 |
| [`empty_animation`](./Enums.md#enum-empty_animation) | Enum |  | 5 |
| `lickAttack` | Variable |  | 5 |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 5 |
| `psyMegaAttack` | Variable |  | 5 |
| `showTrinket` | Variable |  | 5 |
| `spinattackloop` | Variable |  | 5 |
| `ArmorPickup` | Variable |  | 4 |
| `MeteorFall` | Variable |  | 4 |
| `Projectile_Rocket` | Variable |  | 4 |
| `SkeletonCat` | Variable |  | 4 |
| `WebTrap` | Variable |  | 4 |
| `bellyflopEnd` | Variable |  | 4 |
| `bellyflopStart` | Variable |  | 4 |
| `bellyflop_air` | Variable |  | 4 |
| `fixed_jump_height` | Float |  | 4 |
| `four_way_animations` | Boolean |  | 4 |
| `grab` | Variable |  | 4 |
| `holy` | Variable |  | 4 |
| `portin` | Variable |  | 4 |
| `psyAttack1` | Variable |  | 4 |
| `ramLoop` | Variable |  | 4 |
| `ramStart` | Variable |  | 4 |
| `roar` | Variable |  | 4 |
| [`rocket_swirl`](#rocket_swirl) | Block | Visual parameters for swirling projectile paths. | 4 |
| `spawn` | Variable |  | 4 |
| `spinattackstart` | Variable |  | 4 |
| `suck` | Variable |  | 4 |
| `sync_frames` | Integer |  | 4 |
| `transform` | Variable |  | 4 |
| `whistle` | Variable |  | 4 |
| `BrambleProjectile` | Variable |  | 3 |
| `BurnTrigger` | Variable |  | 3 |
| `CupidsArrowProjectile` | Variable |  | 3 |
| `FireBlastMedium` | Variable |  | 3 |
| `MedSlimeShadow` | Variable |  | 3 |
| `Pyrophina` | Variable |  | 3 |
| `RocketFromAbove` | Variable |  | 3 |
| `Shambler` | Variable |  | 3 |
| `TakeAim` | Variable |  | 3 |
| `Tombstone` | Variable |  | 3 |
| `WaterConduct` | Variable |  | 3 |
| `Zaratana` | Variable |  | 3 |
| `angry` | Variable |  | 3 |
| `backflip` | Variable |  | 3 |
| `castspell` | Variable |  | 3 |
| `chargeholy` | Variable |  | 3 |
| [`dash_decelerating_animation`](./Enums.md#enum-dash_decelerating_animation) | Enum |  | 3 |
| `dashslow` | Variable |  | 3 |
| `decelerate` | Integer | Visual slowdown at the end of a movement. | 3 |
| `delay_from_map_edge` | Boolean | Delays effect based on distance from the screen edge. | 3 |
| `digin` | Variable |  | 3 |
| `digout` | Variable |  | 3 |
| `drinkTrinket` | Variable |  | 3 |
| `easing` | Integer | Smoothing function for movement animations. | 3 |
| `escape` | Variable |  | 3 |
| `fixed_jump_speed` | Float |  | 3 |
| [`grab_animation`](./Enums.md#enum-grab_animation) | Enum |  | 3 |
| `invthrow` | Variable |  | 3 |
| `land` | Variable |  | 3 |
| `lob_yoff` | Float | Adjustments for arcing projectiles. | 3 |
| `lock_orientation_during_dash` | Boolean | Prevents the sprite from flipping mid-dash. | 3 |
| `puke` | Variable |  | 3 |
| `run` | Variable |  | 3 |
| `scream` | Variable |  | 3 |
| `show_infinity_damage_warning` | Boolean |  | 3 |
| `skeletonDie` | Variable |  | 3 |
| `slam` | Variable |  | 3 |
| `slowPawMagic` | Variable |  | 3 |
| `thinlaser` | Variable |  | 3 |
| [`tint`](./Arrays.md#array-tint) | Array |  | 3 |
| `use_projectile_spawn_offset` | Boolean |  | 3 |
| `use_rotation_once` | Boolean |  | 3 |
| `weaponspell` | Variable |  | 3 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| `AnimalEgg` | Variable |  | 2 |
| `ArrowFromAbove` | Variable |  | 2 |
| `ArrowProjectile` | Variable |  | 2 |
| `BabySpider` | Variable |  | 2 |
| `BigSlimeShadow` | Variable |  | 2 |
| `BirdSmall` | Variable |  | 2 |
| `Bomb` | Variable |  | 2 |
| `CanCreeper` | Variable |  | 2 |
| `CanCreeperOut` | Variable |  | 2 |
| `CoreFreak` | Variable |  | 2 |
| `Crow` | Variable |  | 2 |
| `Dip` | Variable |  | 2 |
| `Fetus` | Variable |  | 2 |
| `FetusGusher` | Variable |  | 2 |
| `FetusNoJar` | Variable |  | 2 |
| `Flea` | Variable |  | 2 |
| `Frog` | Variable |  | 2 |
| `Frogchain` | Variable |  | 2 |
| `Froghook` | Variable |  | 2 |
| `HyperBeam` | Variable |  | 2 |
| `LightningBallProjectile` | Variable |  | 2 |
| `LobbedProjectile` | Variable |  | 2 |
| `LoveBot` | Variable |  | 2 |
| `NeedleProjectile` | Variable |  | 2 |
| `NukeBlastLarge` | Variable |  | 2 |
| `Pooter` | Variable |  | 2 |
| `Projectile` | Variable |  | 2 |
| `PukeBall` | Variable |  | 2 |
| `Reaper` | Variable |  | 2 |
| `RoboTom` | Variable |  | 2 |
| `Rock` | Variable |  | 2 |
| `SmallSlimeShadow` | Variable |  | 2 |
| `SpearMaskCenter` | Variable |  | 2 |
| `Spike` | Variable |  | 2 |
| `SpikeProjectile` | Variable |  | 2 |
| `Squirrel` | Variable |  | 2 |
| `Stacy2p0` | Variable |  | 2 |
| `TNTCrate` | Variable |  | 2 |
| `TallSkeletonCat` | Variable |  | 2 |
| `TormentorShadow` | Variable |  | 2 |
| `Tumor` | Variable |  | 2 |
| `WaterGush` | Variable |  | 2 |
| `ZombieCat` | Variable |  | 2 |
| `alertstart` | Variable |  | 2 |
| `always_huge_mask` | Boolean |  | 2 |
| `always_play_animations` | Boolean | Bypasses speed-up/skip logic. | 2 |
| `blowFire` | Variable |  | 2 |
| `bombardment` | Variable |  | 2 |
| `call` | Variable |  | 2 |
| `dashing` | Variable |  | 2 |
| [`default_attack_animation`](./Enums.md#enum-default_attack_animation) | Enum |  | 2 |
| `desc` | String | Localization key for the character's desc. | 2 |
| `detatched_animation_cutoff` | Boolean |  | 2 |
| `do_damage_immediately` | Boolean | Applies math before the animation actually hits. | 2 |
| `drop` | Variable |  | 2 |
| `enrage` | Variable |  | 2 |
| `fart` | Variable |  | 2 |
| `fartoom` | Variable |  | 2 |
| `flex` | Variable |  | 2 |
| `fx_ManaHeal` | Variable |  | 2 |
| `fx_bloatlaser` | Variable |  | 2 |
| `fx_magicSplash` | Variable |  | 2 |
| `fx_shield` | Variable |  | 2 |
| `fx_statdown` | Variable |  | 2 |
| `glare` | Variable |  | 2 |
| `greenlaser` | Variable |  | 2 |
| `hadouken` | Variable |  | 2 |
| `ice` | Variable |  | 2 |
| `jump` | Variable |  | 2 |
| `jump_height_multiplier` | Float | Overrides for jump physics. | 2 |
| `knockupatk` | Variable |  | 2 |
| `launchMid` | Variable |  | 2 |
| `launchStart` | Variable |  | 2 |
| `magnet` | Variable |  | 2 |
| `majormagic` | Variable |  | 2 |
| [`mask_center`](./Enums.md#enum-mask_center) | Enum |  | 2 |
| [`mask_extent`](./Enums.md#enum-mask_extent) | Enum |  | 2 |
| `max_throw_height` | Float |  | 2 |
| `megabite` | Variable |  | 2 |
| `megablast` | Variable |  | 2 |
| `meow` | Variable |  | 2 |
| `meteorshower` | Variable |  | 2 |
| `monkAttack` | Variable |  | 2 |
| [`particle_mat`](./Enums.md#enum-particle_mat) | Enum |  | 2 |
| `poopfart` | Variable |  | 2 |
| `portout` | Variable |  | 2 |
| `power` | Variable |  | 2 |
| [`preturn_animation`](./Enums.md#enum-preturn_animation) | Enum |  | 2 |
| `primed_alt_animation` | String |  | 2 |
| `priming` | Variable |  | 2 |
| `propelLoop` | Variable |  | 2 |
| `propelStart` | Variable |  | 2 |
| [`pseudoprojectile`](./Enums.md#enum-pseudoprojectile) | Enum |  | 2 |
| `psyAttack2` | Variable |  | 2 |
| `pukeatk` | Variable |  | 2 |
| `pulse` | Variable |  | 2 |
| `raise` | Variable |  | 2 |
| `reverse_orientation` | Boolean |  | 2 |
| `selfHarm` | Variable |  | 2 |
| `self_damage_mid_port` | Boolean |  | 2 |
| `shade_occluded_objects` | Boolean |  | 2 |
| `shadow_occluded_spelldissolve` | Variable |  | 2 |
| `sing1` | Variable |  | 2 |
| `statusReaction` | Variable |  | 2 |
| `sytheCut` | Variable |  | 2 |
| `tauntwiggle` | Variable |  | 2 |
| `thinlasercap` | Variable |  | 2 |
| `throw_speed` | Integer |  | 2 |
| `use_hit_alts` | Boolean |  | 2 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `AcidOoze` | Variable |  | 1 |
| `AcidshotProjectile` | Variable |  | 1 |
| `AlbinoTomTom` | Variable |  | 1 |
| `AlienBeast` | Variable |  | 1 |
| `AlienEgg` | Variable |  | 1 |
| `Amoeba` | Variable |  | 1 |
| `AngelicCat` | Variable |  | 1 |
| `AngelicCatFetus` | Variable |  | 1 |
| `Ankylosaurus` | Variable |  | 1 |
| `AntidotePickup` | Variable |  | 1 |
| `Astro` | Variable |  | 1 |
| `AstroSkull` | Variable |  | 1 |
| `AstroZombie` | Variable |  | 1 |
| `AtomicKitten` | Variable |  | 1 |
| `BabyCat` | Variable |  | 1 |
| `BabyDeathWorm` | Variable |  | 1 |
| `BabyShark` | Variable |  | 1 |
| `Bat` | Variable |  | 1 |
| `BeaniesX` | Variable |  | 1 |
| `Bear` | Variable |  | 1 |
| `Beaver` | Variable |  | 1 |
| `Belcher` | Variable |  | 1 |
| `BigAsteroid` | Variable |  | 1 |
| `BigDemon` | Variable |  | 1 |
| `BigRock` | Variable |  | 1 |
| `BigSlime` | Variable |  | 1 |
| `BigSlimeX` | Variable |  | 1 |
| `BigUFO` | Variable |  | 1 |
| `Bigfoot` | Variable |  | 1 |
| `BirdLarge` | Variable |  | 1 |
| `BirdMed` | Variable |  | 1 |
| `Birthwort` | Variable |  | 1 |
| `BishopHat` | Variable |  | 1 |
| `BloatEye` | Variable |  | 1 |
| `BloatRat` | Variable |  | 1 |
| `BloatyCorpse` | Variable |  | 1 |
| `BombFly` | Variable |  | 1 |
| `Bombchu` | Variable |  | 1 |
| `BomberRat` | Variable |  | 1 |
| `BoomerCat` | Variable |  | 1 |
| `Bottleshot` | Variable |  | 1 |
| `BrambleBaby` | Variable |  | 1 |
| `Bramblechain` | Variable |  | 1 |
| `Bramblehook` | Variable |  | 1 |
| `Bumblefoot` | Variable |  | 1 |
| `BungaElite1` | Variable |  | 1 |
| `BungaThrone` | Variable |  | 1 |
| `BunkerBoy` | Variable |  | 1 |
| `BunkerCandles2x2` | Variable |  | 1 |
| `Bunny` | Variable |  | 1 |
| `Burfer` | Variable |  | 1 |
| `ButchTinkX` | Variable |  | 1 |
| `ButcherCat` | Variable |  | 1 |
| `ButcherCat_Terminator` | Variable |  | 1 |
| `Cactus` | Variable |  | 1 |
| `CancerCat` | Variable |  | 1 |
| `Carcus` | Variable |  | 1 |
| `Carnibulb` | Variable |  | 1 |
| `CatCaller` | Variable |  | 1 |
| `CatCultist` | Variable |  | 1 |
| `CatHuman` | Variable |  | 1 |
| `Caterpillar` | Variable |  | 1 |
| `CaveChief` | Variable |  | 1 |
| `CavePerson` | Variable |  | 1 |
| `Cerberubs` | Variable |  | 1 |
| `ChakramProjectile` | Variable |  | 1 |
| `Chaos` | Variable |  | 1 |
| `ChargeyMaggot` | Variable |  | 1 |
| `Cherub` | Variable |  | 1 |
| `ChumBag` | Variable |  | 1 |
| `Chummy` | Variable |  | 1 |
| `Chupacabra` | Variable |  | 1 |
| `CloakedDemon` | Variable |  | 1 |
| `CloningVat` | Variable |  | 1 |
| `Clot` | Variable |  | 1 |
| `CollectiveCat` | Variable |  | 1 |
| `ConjoinedHusk` | Variable |  | 1 |
| `CopBot` | Variable |  | 1 |
| `CoreArm` | Variable |  | 1 |
| `CovenCandle` | Variable |  | 1 |
| `Crate` | Variable |  | 1 |
| `Cutter` | Variable |  | 1 |
| `DaddyCat` | Variable |  | 1 |
| `DaddyShark` | Variable |  | 1 |
| `Dclaude` | Variable |  | 1 |
| `DeathWorm` | Variable |  | 1 |
| `Deathbot` | Variable |  | 1 |
| `Decoy` | Variable |  | 1 |
| `Decoy2` | Variable |  | 1 |
| `DemonHooker` | Variable |  | 1 |
| `DiggyMaggot` | Variable |  | 1 |
| `DinoEggs` | Variable |  | 1 |
| `DocBot` | Variable |  | 1 |
| `Dog` | Variable |  | 1 |
| `DrDitto` | Variable |  | 1 |
| `Drcat` | Variable |  | 1 |
| `DruidCat` | Variable |  | 1 |
| `DruidCat_Terminator` | Variable |  | 1 |
| `Dumpster` | Variable |  | 1 |
| `DustCloud` | Variable |  | 1 |
| `DustDevil` | Variable |  | 1 |
| `DustPoofLarge` | Variable |  | 1 |
| `DustPoofMedium` | Variable |  | 1 |
| `Dybbuk` | Variable |  | 1 |
| `ENEMY_ANKYLOSAURUS_DESC` | Variable |  | 1 |
| `ENEMY_BOUNTYHUNTER_DESC` | Variable |  | 1 |
| `ENEMY_CATHUMAN_NAME` | Variable |  | 1 |
| `ENEMY_DUSTDEVIL_DESC` | Variable |  | 1 |
| `ENEMY_HUMANCAT_NAME` | Variable |  | 1 |
| `ENEMY_RAPTORKITTEN_DESC` | Variable |  | 1 |
| `ENEMY_TERMINATOR3_HITLER_DESC` | Variable |  | 1 |
| `ENTITY_GLOWMUSHROOM_DESC` | Variable |  | 1 |
| `Edmund` | Variable |  | 1 |
| `ElectricNail` | Variable |  | 1 |
| `EmptyV` | Variable |  | 1 |
| `FatCat` | Variable |  | 1 |
| `FatMan` | Variable |  | 1 |
| `FatRat` | Variable |  | 1 |
| `FatWoman` | Variable |  | 1 |
| `Fatso` | Variable |  | 1 |
| `FearEffect` | Variable |  | 1 |
| `FetusJar` | Variable |  | 1 |
| `FighterCat` | Variable |  | 1 |
| `FighterCat_Terminator` | Variable |  | 1 |
| `FijiMermaid` | Variable |  | 1 |
| `FinalBossMegaGuppy` | Variable |  | 1 |
| `FinalBossPhase1` | Variable |  | 1 |
| `FinalBossPhase2` | Variable |  | 1 |
| `FinalBossPhase3` | Variable |  | 1 |
| `FinalBossShieldProjectile` | Variable |  | 1 |
| `FireBallProjectile` | Variable |  | 1 |
| `FleshLad` | Variable |  | 1 |
| `FleshyMind` | Variable |  | 1 |
| `Floast` | Variable |  | 1 |
| `Floater` | Variable |  | 1 |
| `FloatingHive` | Variable |  | 1 |
| `Flushmaster` | Variable |  | 1 |
| `Fly` | Variable |  | 1 |
| `FrankX` | Variable |  | 1 |
| `FutureBot` | Variable |  | 1 |
| `Fuzzer` | Variable |  | 1 |
| `Gambit` | Variable |  | 1 |
| `GambitDice` | Variable |  | 1 |
| `Gambitmouthbeam` | Variable |  | 1 |
| `Gamete` | Variable |  | 1 |
| `GasCan` | Variable |  | 1 |
| `GasCloud` | Variable |  | 1 |
| `Gasser` | Variable |  | 1 |
| `GassyCat` | Variable |  | 1 |
| `Gatekeeper` | Variable |  | 1 |
| `Gemini` | Variable |  | 1 |
| `GeoLad` | Variable |  | 1 |
| `GlassSpitter` | Variable |  | 1 |
| `GlowingMushroom` | Variable |  | 1 |
| `GolemCat` | Variable |  | 1 |
| `GraveWorm` | Variable |  | 1 |
| `GreenProber` | Variable |  | 1 |
| `Grenade` | Variable |  | 1 |
| `Grey` | Variable |  | 1 |
| `GreyAlien` | Variable |  | 1 |
| `GroundZombie` | Variable |  | 1 |
| `GroundedSpear` | Variable |  | 1 |
| `Guillotina1` | Variable |  | 1 |
| `GunCat` | Variable |  | 1 |
| `HangerBot` | Variable |  | 1 |
| `Harpoon` | Variable |  | 1 |
| `HarpoonTrap` | Variable |  | 1 |
| `HealSmall` | Variable |  | 1 |
| `Hellspawn1` | Variable |  | 1 |
| `Hemlock` | Variable |  | 1 |
| `HemlockFetus` | Variable |  | 1 |
| `Hitler` | Variable |  | 1 |
| `HitlerHead` | Variable |  | 1 |
| `HitlerMech` | Variable |  | 1 |
| `Hive` | Variable |  | 1 |
| `HolyPickup` | Variable |  | 1 |
| `HornyCat` | Variable |  | 1 |
| `HumanCat` | Variable |  | 1 |
| `HunterCat` | Variable |  | 1 |
| `HunterCat_Terminator` | Variable |  | 1 |
| `Husk` | Variable |  | 1 |
| `Hydrant` | Variable |  | 1 |
| `HydrantFountain` | Variable |  | 1 |
| `IceBlast` | Variable |  | 1 |
| `IceCube` | Variable |  | 1 |
| `IceElemental` | Variable |  | 1 |
| `IcecubeParticle` | Variable |  | 1 |
| `InfestedDuo` | Variable |  | 1 |
| `Invader` | Variable |  | 1 |
| `Isaac` | Variable |  | 1 |
| `JackCat` | Variable |  | 1 |
| `JarHead` | Variable |  | 1 |
| `Jekyll` | Variable |  | 1 |
| `JerseyDevil` | Variable |  | 1 |
| `JesterCat` | Variable |  | 1 |
| `JesterCat_Terminator` | Variable |  | 1 |
| `Johnny` | Variable |  | 1 |
| `Junk` | Variable |  | 1 |
| `KillDozer` | Variable |  | 1 |
| `Kirby` | Variable |  | 1 |
| `Kitten` | Variable |  | 1 |
| `LabSupportPillar` | Variable |  | 1 |
| `Lenny` | Variable |  | 1 |
| `LightningElemental` | Variable |  | 1 |
| `LiquidMetalSpear` | Variable |  | 1 |
| `LoanShark` | Variable |  | 1 |
| `LordBunga` | Variable |  | 1 |
| `MadLad` | Variable |  | 1 |
| `Maelestes` | Variable |  | 1 |
| `MageCat` | Variable |  | 1 |
| `MageCat_Terminator` | Variable |  | 1 |
| `MagicMissileProjectileSmall` | Variable |  | 1 |
| `MagicSpikeProjectile` | Variable |  | 1 |
| `MamaMaggot` | Variable |  | 1 |
| `Mammoth` | Variable |  | 1 |
| `MammothBaby` | Variable |  | 1 |
| `Mangy` | Variable |  | 1 |
| `Mangy2` | Variable |  | 1 |
| `Mangy3` | Variable |  | 1 |
| `Mask` | Variable |  | 1 |
| `MeatMinion` | Variable |  | 1 |
| `MeatSlime` | Variable |  | 1 |
| `MechSuit` | Variable |  | 1 |
| `MedSlime` | Variable |  | 1 |
| `MedSlimeX` | Variable |  | 1 |
| `MedicCat` | Variable |  | 1 |
| `MedicCat_Terminator` | Variable |  | 1 |
| `MegaDinoHead` | Variable |  | 1 |
| `MegaDinoLeg` | Variable |  | 1 |
| `MegaFetus` | Variable |  | 1 |
| `MegaMutant` | Variable |  | 1 |
| `MegaTumor` | Variable |  | 1 |
| `Meteorball` | Variable |  | 1 |
| `MindFetus` | Variable |  | 1 |
| `MiniVolcano` | Variable |  | 1 |
| `MommyCat` | Variable |  | 1 |
| `MonkCat` | Variable |  | 1 |
| `MonkCat_Terminator` | Variable |  | 1 |
| `MoonHand` | Variable |  | 1 |
| `MoonHead` | Variable |  | 1 |
| `MoonWorm` | Variable |  | 1 |
| `Moth` | Variable |  | 1 |
| `MotherSpike` | Variable |  | 1 |
| `MotherTumor` | Variable |  | 1 |
| `Mothman` | Variable |  | 1 |
| `Multicat` | Variable |  | 1 |
| `NecroCat` | Variable |  | 1 |
| `NecroCat_Terminator` | Variable |  | 1 |
| `Needlecat` | Variable |  | 1 |
| `Nessie` | Variable |  | 1 |
| `Nettle` | Variable |  | 1 |
| `NeutronStar` | Variable |  | 1 |
| `NubsCat` | Variable |  | 1 |
| `OrganGrinderX` | Variable |  | 1 |
| `Parasaurolophus` | Variable |  | 1 |
| `Parasiter` | Variable |  | 1 |
| `Peashy` | Variable |  | 1 |
| `Pebbles` | Variable |  | 1 |
| `Pebbles_Terminator` | Variable |  | 1 |
| `PetBoulder` | Variable |  | 1 |
| `PetRock` | Variable |  | 1 |
| `Pig` | Variable |  | 1 |
| `Pile` | Variable |  | 1 |
| `Pinky` | Variable |  | 1 |
| `PinkyX` | Variable |  | 1 |
| `PokerDemon` | Variable |  | 1 |
| `PoopCat` | Variable |  | 1 |
| `PopeyeCat` | Variable |  | 1 |
| `Porcupine` | Variable |  | 1 |
| `PsychicCat` | Variable |  | 1 |
| `PsychicCat_Terminator` | Variable |  | 1 |
| `Pterodactyl` | Variable |  | 1 |
| `Punchbot` | Variable |  | 1 |
| `QueenHippo` | Variable |  | 1 |
| `Rager` | Variable |  | 1 |
| `Raptor` | Variable |  | 1 |
| `RaptorBaby` | Variable |  | 1 |
| `Rat` | Variable |  | 1 |
| `RatCat` | Variable |  | 1 |
| `RatKing_New` | Variable |  | 1 |
| `RatPile` | Variable |  | 1 |
| `Revalark` | Variable |  | 1 |
| `RockHead` | Variable |  | 1 |
| `RockyBobo` | Variable |  | 1 |
| `Roomba` | Variable |  | 1 |
| `Rover` | Variable |  | 1 |
| `SabertoothCat` | Variable |  | 1 |
| `SabertoothCub` | Variable |  | 1 |
| `Scary` | Variable |  | 1 |
| `ScorpionCat` | Variable |  | 1 |
| `SecurityBot` | Variable |  | 1 |
| `ShadeCat` | Variable |  | 1 |
| `ShadeF` | Variable |  | 1 |
| `ShadeM` | Variable |  | 1 |
| `ShadeMShadow` | Variable |  | 1 |
| `ShamblingShade` | Variable |  | 1 |
| `SharkyCat` | Variable |  | 1 |
| `Simon` | Variable |  | 1 |
| `SimonFlop` | Variable |  | 1 |
| `Siren` | Variable |  | 1 |
| `Skinned` | Variable |  | 1 |
| `Skunk` | Variable |  | 1 |
| `Slag` | Variable |  | 1 |
| `Slash` | Variable |  | 1 |
| `Slenderman` | Variable |  | 1 |
| `SlotMachine` | Variable |  | 1 |
| `SmallAsteroid` | Variable |  | 1 |
| `SmallSlime` | Variable |  | 1 |
| `SmallSlimeX` | Variable |  | 1 |
| `SmallUFO` | Variable |  | 1 |
| `SnakeyBones` | Variable |  | 1 |
| `SoldierBot` | Variable |  | 1 |
| `Sonichu` | Variable |  | 1 |
| `SpearGuyAttack` | Variable |  | 1 |
| `SpearProjectile` | Variable |  | 1 |
| `SpearTestGuy` | Variable |  | 1 |
| `Spewer` | Variable |  | 1 |
| `SpewerPill` | Variable |  | 1 |
| `SpewerTube` | Variable |  | 1 |
| `SpiderCat` | Variable |  | 1 |
| `SpiderQueen` | Variable |  | 1 |
| `SpikeTrap` | Variable |  | 1 |
| `SpikedCat` | Variable |  | 1 |
| `SpikyCactus` | Variable |  | 1 |
| `SpikyCactus2x2` | Variable |  | 1 |
| `SpikyCactusTall` | Variable |  | 1 |
| `SpikyRock` | Variable |  | 1 |
| `Spookie` | Variable |  | 1 |
| `Sprout` | Variable |  | 1 |
| `StacyX` | Variable |  | 1 |
| `Stegosaurus` | Variable |  | 1 |
| `StemCat` | Variable |  | 1 |
| `TallBot` | Variable |  | 1 |
| `TallHaunt` | Variable |  | 1 |
| `TallSpiderCat` | Variable |  | 1 |
| `TallTumor` | Variable |  | 1 |
| `TankCat` | Variable |  | 1 |
| `TankCat_Terminator` | Variable |  | 1 |
| `TarBaby` | Variable |  | 1 |
| `Tatters` | Variable |  | 1 |
| `TenTickles` | Variable |  | 1 |
| `TenTicklesAttack` | Variable |  | 1 |
| `Terminator2Cat` | Variable |  | 1 |
| `TerminatorCat` | Variable |  | 1 |
| `TeslaCoil` | Variable |  | 1 |
| `TheBloat` | Variable |  | 1 |
| `TheCoven` | Variable |  | 1 |
| `TheMother` | Variable |  | 1 |
| `ThiefCat` | Variable |  | 1 |
| `ThiefCat_Terminator` | Variable |  | 1 |
| `ThrobbingKing` | Variable |  | 1 |
| `ThrobbingTurret` | Variable |  | 1 |
| `Thump` | Variable |  | 1 |
| `TinaSpear` | Variable |  | 1 |
| `TinkererCat` | Variable |  | 1 |
| `TinkererCat_Terminator` | Variable |  | 1 |
| `Tire` | Variable |  | 1 |
| `Toadie` | Variable |  | 1 |
| `TomTom` | Variable |  | 1 |
| `Tormentor` | Variable |  | 1 |
| `Tox` | Variable |  | 1 |
| `TracyX` | Variable |  | 1 |
| `TrailerCat` | Variable |  | 1 |
| `Trampy` | Variable |  | 1 |
| `TrashBag` | Variable |  | 1 |
| `Tremblo` | Variable |  | 1 |
| `Trex` | Variable |  | 1 |
| `Triachnid` | Variable |  | 1 |
| `Triceratops` | Variable |  | 1 |
| `TumorBarrier` | Variable |  | 1 |
| `Turret` | Variable |  | 1 |
| `Turtle` | Variable |  | 1 |
| `Twister` | Variable |  | 1 |
| `Tyler` | Variable |  | 1 |
| `UltraOrnstein` | Variable |  | 1 |
| `Waggle` | Variable |  | 1 |
| `WaterKitten` | Variable |  | 1 |
| `WaterLeech` | Variable |  | 1 |
| `Whisperer` | Variable |  | 1 |
| `WhiteBear` | Variable |  | 1 |
| `WhiteRabbit` | Variable |  | 1 |
| `Wisp` | Variable |  | 1 |
| `Wizard` | Variable |  | 1 |
| `WoC_Eye` | Variable |  | 1 |
| `WoC_Mouth` | Variable |  | 1 |
| `WoC_Wall` | Variable |  | 1 |
| `WolfCat` | Variable |  | 1 |
| `Worm` | Variable |  | 1 |
| `YellowBlaster` | Variable |  | 1 |
| `Yeti` | Variable |  | 1 |
| `Yeticat` | Variable |  | 1 |
| `Zodiac` | Variable |  | 1 |
| [`affected_animation`](./Enums.md#enum-affected_animation) | Enum | Visuals applied to the target receiving the effect. | 1 |
| `alertend` | Variable |  | 1 |
| [`ally_animation`](./Enums.md#enum-ally_animation) | Enum | Distinct animation used when targeting a friendly unit. | 1 |
| `animate_name` | String | Animates the ability name text on cast. | 1 |
| `apex_distance` | Float | Calculations for the peak of a jump/lob arc. | 1 |
| `apex_time` | Float | Calculations for the peak of a jump/lob arc. | 1 |
| `attack1` | Variable |  | 1 |
| `attack2` | Variable |  | 1 |
| `attackL` | Variable |  | 1 |
| `backflipEnd` | Variable |  | 1 |
| `backflipLoop` | Variable |  | 1 |
| `backflipStart` | Variable |  | 1 |
| `barbedwire` | Variable |  | 1 |
| `beam` | Variable |  | 1 |
| `beamin` | Variable |  | 1 |
| `beaminHunter` | Variable |  | 1 |
| `beaminTank` | Variable |  | 1 |
| `bite` | Variable |  | 1 |
| `blast1` | Variable |  | 1 |
| `blast2` | Variable |  | 1 |
| `bless` | Variable |  | 1 |
| `blizzard` | Variable |  | 1 |
| `blowUp` | Variable |  | 1 |
| `bodypulse` | Variable |  | 1 |
| `bounce` | Variable |  | 1 |
| `brace` | Variable |  | 1 |
| `bubbleshot` | Variable |  | 1 |
| `buttScootLoop` | Variable |  | 1 |
| `buttScootStart` | Variable |  | 1 |
| `bypass_combatspeed` | Boolean |  | 1 |
| `cartwheelLoop` | Variable |  | 1 |
| `cartwheelStart` | Variable |  | 1 |
| `celebrate` | Variable |  | 1 |
| `change` | Variable |  | 1 |
| `charm` | Variable |  | 1 |
| `command1` | Variable |  | 1 |
| `command2` | Variable |  | 1 |
| `command3` | Variable |  | 1 |
| `command4` | Variable |  | 1 |
| `controlmonster` | Variable |  | 1 |
| `crash` | Variable |  | 1 |
| `cry` | Variable |  | 1 |
| `curse` | Variable |  | 1 |
| [`damage_threshold_altanimations`](#damage_threshold_altanimations) | Block | Triggers different hit animations based on the amount of damage dealt. | 1 |
| `dash2` | Variable |  | 1 |
| [`dash_bonk_animation`](./Enums.md#enum-dash_bonk_animation) | Enum |  | 1 |
| `dashbegin` | Variable |  | 1 |
| `dashstart2` | Variable |  | 1 |
| [`default_face`](./Enums.md#enum-default_face) | Enum |  | 1 |
| `delay_from_map_center` | Boolean | Positional based timing delays. | 1 |
| `delay_from_reverse_map_edge` | Boolean |  | 1 |
| `depossess` | Variable |  | 1 |
| `detonate` | Variable |  | 1 |
| `digUp` | Variable |  | 1 |
| `disassemble` | Variable |  | 1 |
| `djump` | Variable |  | 1 |
| `do_animation_offscreen` | Boolean |  | 1 |
| `do_not_clear_placeholder` | Boolean |  | 1 |
| [`dodge`](./Enums.md#enum-dodge) | Enum |  | 1 |
| `doom` | Variable |  | 1 |
| `doublepunch` | Variable |  | 1 |
| `drink` | Variable |  | 1 |
| `eat` | Variable |  | 1 |
| `eatTrinket` | Variable |  | 1 |
| `egg` | Variable |  | 1 |
| `entangle` | Variable |  | 1 |
| `enterWater` | Variable |  | 1 |
| `enterbattle` | Variable |  | 1 |
| `entrance` | Variable |  | 1 |
| `entrance_land` | Variable |  | 1 |
| `exhale` | Variable |  | 1 |
| `face_targets` | Boolean | Forces the sprite to look at the target tile. | 1 |
| `firestorm` | Variable |  | 1 |
| `first_castpoint_is_self_damage_only` | Boolean |  | 1 |
| `fizzle` | Variable |  | 1 |
| `flush` | Variable |  | 1 |
| `freeze` | Variable |  | 1 |
| `fuzzjump` | Variable |  | 1 |
| `fx_GravitySlam` | Variable |  | 1 |
| `fx_haste` | Variable |  | 1 |
| `fx_heretic` | Variable |  | 1 |
| `fx_kingbloodlaser` | Variable |  | 1 |
| `fx_sandBlows` | Variable |  | 1 |
| `gravitySlamEnd` | Variable |  | 1 |
| `gravitySlamStart` | Variable |  | 1 |
| `gravitySlam_air` | Variable |  | 1 |
| `greenmegalaser` | Variable |  | 1 |
| `groundpound` | Variable |  | 1 |
| `grow` | Variable |  | 1 |
| `guard` | Variable |  | 1 |
| `gutball` | Variable |  | 1 |
| `hang_time` | Float |  | 1 |
| `happy` | Variable |  | 1 |
| `heil` | Variable |  | 1 |
| `hide` | Variable |  | 1 |
| `hiss` | Variable |  | 1 |
| `hop` | Variable |  | 1 |
| `hopinplace` | Variable |  | 1 |
| `hud_palette` | Integer |  | 1 |
| `icebreath` | Variable |  | 1 |
| `idleCommand1` | Variable |  | 1 |
| `idleCommand2` | Variable |  | 1 |
| `idleCommand3` | Variable |  | 1 |
| `idleCommand4` | Variable |  | 1 |
| `inhale` | Variable |  | 1 |
| `jetbegin` | Variable |  | 1 |
| `jetloop` | Variable |  | 1 |
| `jump_speed_multiplier` | Float |  | 1 |
| `jumpattack` | Variable |  | 1 |
| `jumpmove` | Variable |  | 1 |
| `jumpsmash` | Variable |  | 1 |
| `kick` | Variable |  | 1 |
| `knead` | Variable |  | 1 |
| `knifeprojectile` | Variable |  | 1 |
| `launch` | Variable |  | 1 |
| `lava` | Variable |  | 1 |
| `leap` | Variable |  | 1 |
| `leapattack` | Variable |  | 1 |
| `leapattackwindup` | Variable |  | 1 |
| `liquidmetalspear` | Variable |  | 1 |
| `liquidteleportOut` | Variable |  | 1 |
| `lob_speed` | Float | Adjustments for arcing projectiles. | 1 |
| `max_range` | Integer | The maximum and minimum distance required to cast. | 1 |
| `megaslap` | Variable |  | 1 |
| `min_range` | Integer | The maximum and minimum distance required to cast. | 1 |
| `mindcontrol` | Variable |  | 1 |
| `moonjump` | Variable |  | 1 |
| `mouthbeam` | Variable |  | 1 |
| `moveLoop` | Variable |  | 1 |
| `moveStart` | Variable |  | 1 |
| `no_horizontal_flip` | Boolean |  | 1 |
| `nuke` | Variable |  | 1 |
| `order` | Variable |  | 1 |
| `othercat_placeholder_available` | Boolean |  | 1 |
| [`override_portrait`](./Enums.md#enum-override_portrait) | Enum |  | 1 |
| `pissYourself` | Variable |  | 1 |
| `poopfartbehind` | Variable |  | 1 |
| `portOut` | Variable |  | 1 |
| `possess` | Variable |  | 1 |
| `pounce` | Variable |  | 1 |
| `precast_delay` | Float |  | 1 |
| `prouder` | Variable |  | 1 |
| `psyAttack3` | Variable |  | 1 |
| `puff` | Variable |  | 1 |
| `pulp` | Variable |  | 1 |
| `radiant` | Variable |  | 1 |
| `ram` | Variable |  | 1 |
| `ramEnd` | Variable |  | 1 |
| `rampage` | Variable |  | 1 |
| `randomize_starting_frame` | Boolean |  | 1 |
| `react` | Variable |  | 1 |
| `reaction` | Variable |  | 1 |
| `reflex` | Variable |  | 1 |
| `releaseCommand1` | Variable |  | 1 |
| `releaseCommand2` | Variable |  | 1 |
| `releaseCommand3` | Variable |  | 1 |
| `releaseCommand4` | Variable |  | 1 |
| `resultExplode` | Variable |  | 1 |
| `resultJackpot` | Variable |  | 1 |
| `resultWin` | Variable |  | 1 |
| `revenge` | Variable |  | 1 |
| `revive` | Variable |  | 1 |
| `rise` | Variable |  | 1 |
| `runStart` | Variable |  | 1 |
| `runincircles` | Variable |  | 1 |
| `shake` | Variable |  | 1 |
| `shocking` | Variable |  | 1 |
| `shootForward` | Variable |  | 1 |
| `sing2` | Variable |  | 1 |
| `source_trinket` | Variable |  | 1 |
| `spawnmama` | Variable |  | 1 |
| `special` | Variable |  | 1 |
| `spike` | Variable |  | 1 |
| `spore` | Variable |  | 1 |
| `static_2x2_a` | Variable |  | 1 |
| `static_2x2_b` | Variable |  | 1 |
| `static_tall_a` | Variable |  | 1 |
| `static_tall_b` | Variable |  | 1 |
| `status_display_count_max` | Integer |  | 1 |
| `stomp` | Variable |  | 1 |
| `summon` | Variable |  | 1 |
| `tailwag` | Variable |  | 1 |
| `teleportOut` | Variable |  | 1 |
| `terminatorPunch` | Variable |  | 1 |
| `test2x2` | Variable |  | 1 |
| `thinking` | Variable |  | 1 |
| `throwboss` | Variable |  | 1 |
| `throwshield` | Variable |  | 1 |
| `thrustersEnd` | Variable |  | 1 |
| `thrustersLoop` | Variable |  | 1 |
| `thrustersStart` | Variable |  | 1 |
| `timberDash` | Variable |  | 1 |
| `timberStart` | Variable |  | 1 |
| `tinkerAdjacent` | Variable |  | 1 |
| `uncatchable` | Boolean |  | 1 |
| `unguard` | Variable |  | 1 |
| `uppercutatk` | Variable |  | 1 |
| `use_directional_animations` | Boolean |  | 1 |
| `use_origin_offsets` | Boolean |  | 1 |
| `uziShoot` | Variable |  | 1 |
| `vomitrain` | Variable |  | 1 |
| [`walk`](./Enums.md#enum-walk) | Enum |  | 1 |
| `weaponAbsorb` | Variable |  | 1 |
| `weaponpoke` | Variable |  | 1 |
| `weaponslam` | Variable |  | 1 |
| `weaponswing` | Variable |  | 1 |
| `weaponswingup` | Variable |  | 1 |
| `yell` | Variable |  | 1 |
| `yell1` | Variable |  | 1 |

</details>

### Valid Nested Blocks

The following blocks all behave as `{Graphics Keys}` containers. Each has its own unique parameters listed below its entry.

---

#### `graphics`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2609

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | The primary flash animation label triggered. | 1559 |
| `name` | String | Localization key for the character's name. | 517 |
| [`particle`](./Enums.md#enum-particle) | Enum | References an impact or cast particle effect. | 488 |
| [`movieclip`](./Enums.md#enum-movieclip) | Enum |  | 460 |
| `tooltip` | String |  | 409 |
| [`projectile`](./Enums.md#enum-projectile) | Enum | References a projectile entity. | 228 |
| `shadow_size` | Float |  | 151 |
| `scale` | Float |  | 149 |
| `uifloaters_offset` | Float |  | 149 |
| `lob` | Boolean |  | 130 |
| [`custom_cat_data`](./Enums.md#enum-custom_cat_data) | Enum |  | 127 |
| `delay` | Float | Frame delay before firing projectile/effect. | 93 |
| `dont_visualize_ai` | Boolean |  | 86 |
| `dont_orient` | Boolean | Prevents the character from turning to face the target. | 83 |
| [`water_mask`](./Enums.md#enum-water_mask) | Enum |  | 83 |
| [`dash_animation`](./Enums.md#enum-dash_animation) | Enum | State-specific animations for trample/dash abilities. | 65 |
| [`dash_start_animation`](./Enums.md#enum-dash_start_animation) | Enum |  | 63 |
| `speed` | Float | Rotations per second. | 61 |
| [`affected_particle`](./Enums.md#enum-affected_particle) | Enum | Visuals applied to the target receiving the effect. | 51 |
| [`dash_attack_animation`](./Enums.md#enum-dash_attack_animation) | Enum |  | 45 |
| `lob_height` | Integer | Adjustments for arcing projectiles. | 45 |
| [`animation_in`](./Enums.md#enum-animation_in) | Enum | Used for transition states (like burrowing). | 43 |
| [`animation_out`](./Enums.md#enum-animation_out) | Enum | Used for transition states (like burrowing). | 43 |
| [`jump_attack_animation`](./Enums.md#enum-jump_attack_animation) | Enum | Overrides for jump physics. | 39 |
| `spawnin_animation` | String |  | 37 |
| `use_projectile` | Boolean |  | 35 |
| `palette` | Integer | Swaps the color palette ID. | 33 |
| `piece_alt_frame` | Integer |  | 27 |
| [`full_jump_animation`](./Enums.md#enum-full_jump_animation) | Enum |  | 24 |
| `full_jump_sync_frames` | Integer |  | 24 |
| `use_rotation` | Boolean |  | 24 |
| [`shadow`](./Enums.md#enum-shadow) | Enum |  | 23 |
| [`dash_end_animation`](./Enums.md#enum-dash_end_animation) | Enum |  | 22 |
| `full_jump_windup_frames` | Integer |  | 20 |
| `move_speed_sync_frames` | Float |  | 20 |
| `visual_delay_but_simultaneous_damage` | Integer |  | 18 |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum | Specific spawn points for particles. | 17 |
| `no_splatter` | Boolean |  | 17 |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum | Specific spawn points for particles. | 16 |
| `fall_from_sky` | Boolean | Spawns the projectile from the top of the screen. | 16 |
| `move_speed_multiplier` | Float |  | 16 |
| `dont_sink` | Boolean |  | 14 |
| [`move_start_animation`](./Enums.md#enum-move_start_animation) | Enum |  | 14 |
| `use_placeholder` | Boolean |  | 14 |
| [`move_end_animation`](./Enums.md#enum-move_end_animation) | Enum |  | 13 |
| [`portrait_face`](./Enums.md#enum-portrait_face) | Enum |  | 13 |
| `face_toss_target` | Boolean |  | 12 |
| `ignore_slowtiles` | Boolean |  | 12 |
| `chain_distance` | Float | Creates a tethered repeating graphic (like a hook). | 11 |
| [`chain_movieclip`](./Enums.md#enum-chain_movieclip) | Enum | Creates a tethered repeating graphic (like a hook). | 11 |
| `darken_screen` | Boolean | Dims the background during the ability cast. | 11 |
| [`beam_cap`](./Enums.md#enum-beam_cap) | Enum | Flash movieclips used to render continuous laser beams. | 10 |
| [`beam_clip`](./Enums.md#enum-beam_clip) | Enum | Flash movieclips used to render continuous laser beams. | 10 |
| `bounce_on_hit` | Boolean | Visual hop when striking a target. | 10 |
| `darken_screen_exclude_characters_on_tile` | Boolean |  | 10 |
| [`end`](./Enums.md#enum-end) | Enum | Segments for continuous channeled animations. | 10 |
| [`jump_start_animation`](./Enums.md#enum-jump_start_animation) | Enum |  | 10 |
| [`loop`](./Enums.md#enum-loop) | Enum | Segments for continuous channeled animations. | 10 |
| [`prime_animation`](./Enums.md#enum-prime_animation) | Enum |  | 10 |
| [`start`](./Enums.md#enum-start) | Enum | Segments for continuous channeled animations. | 10 |
| `max_tiles_single_loop` | Integer |  | 9 |
| `sync_speed` | Integer |  | 9 |
| [`dying`](./Enums.md#enum-dying) | Enum |  | 8 |
| `fx_is_placeholder_animation` | Boolean |  | 8 |
| `aoe_spell_on_land` | Boolean | Visual trigger when a jump lands. | 7 |
| `art_flip` | Integer |  | 7 |
| `fx_random_flip` | Boolean |  | 7 |
| [`land_animation`](./Enums.md#enum-land_animation) | Enum |  | 7 |
| [`miss_particle`](./Enums.md#enum-miss_particle) | Enum | Specific spawn points for particles. | 7 |
| `use_super_armor` | Boolean | Prevents flinch animations from interrupting this cast. | 7 |
| [`air_animation`](./Enums.md#enum-air_animation) | Enum | Animation played while entity is airborne. | 6 |
| [`custom_priming_animation`](./Enums.md#enum-custom_priming_animation) | Enum | Animation used while charging an ability. | 6 |
| `darken_screen_exclude_self` | Boolean |  | 6 |
| `darken_screen_start_early` | Boolean |  | 6 |
| `depth_offset` | Float |  | 6 |
| `fall_randomize_timing` | Float |  | 6 |
| `min_throw_height` | Float |  | 6 |
| `single_projectile` | Boolean |  | 6 |
| [`detatched_animation`](./Enums.md#enum-detatched_animation) | Enum | Plays an animation separated from the character body. | 5 |
| `detatched_animation_reach` | Integer |  | 5 |
| [`empty_animation`](./Enums.md#enum-empty_animation) | Enum |  | 5 |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 5 |
| `fixed_jump_height` | Float |  | 4 |
| `four_way_animations` | Boolean |  | 4 |
| [`rocket_swirl`](#rocket_swirl) | Block | Visual parameters for swirling projectile paths. | 4 |
| `sync_frames` | Integer |  | 4 |
| [`dash_decelerating_animation`](./Enums.md#enum-dash_decelerating_animation) | Enum |  | 3 |
| `decelerate` | Integer | Visual slowdown at the end of a movement. | 3 |
| `delay_from_map_edge` | Boolean | Delays effect based on distance from the screen edge. | 3 |
| `easing` | Integer | Smoothing function for movement animations. | 3 |
| `fixed_jump_speed` | Float |  | 3 |
| [`grab_animation`](./Enums.md#enum-grab_animation) | Enum |  | 3 |
| `lob_yoff` | Float | Adjustments for arcing projectiles. | 3 |
| `lock_orientation_during_dash` | Boolean | Prevents the sprite from flipping mid-dash. | 3 |
| `show_infinity_damage_warning` | Boolean |  | 3 |
| [`tint`](./Arrays.md#array-tint) | Array |  | 3 |
| `use_projectile_spawn_offset` | Boolean |  | 3 |
| `use_rotation_once` | Boolean |  | 3 |
| `always_huge_mask` | Boolean |  | 2 |
| `always_play_animations` | Boolean | Bypasses speed-up/skip logic. | 2 |
| [`default_attack_animation`](./Enums.md#enum-default_attack_animation) | Enum |  | 2 |
| `desc` | String | Localization key for the character's desc. | 2 |
| `detatched_animation_cutoff` | Boolean |  | 2 |
| `do_damage_immediately` | Boolean | Applies math before the animation actually hits. | 2 |
| `jump_height_multiplier` | Float | Overrides for jump physics. | 2 |
| [`mask_center`](./Enums.md#enum-mask_center) | Enum |  | 2 |
| [`mask_extent`](./Enums.md#enum-mask_extent) | Enum |  | 2 |
| `max_throw_height` | Float |  | 2 |
| [`particle_mat`](./Enums.md#enum-particle_mat) | Enum |  | 2 |
| [`preturn_animation`](./Enums.md#enum-preturn_animation) | Enum |  | 2 |
| `primed_alt_animation` | String |  | 2 |
| [`pseudoprojectile`](./Enums.md#enum-pseudoprojectile) | Enum |  | 2 |
| `reverse_orientation` | Boolean |  | 2 |
| `self_damage_mid_port` | Boolean |  | 2 |
| `shade_occluded_objects` | Boolean |  | 2 |
| `throw_speed` | Integer |  | 2 |
| `use_hit_alts` | Boolean |  | 2 |
| [`affected_animation`](./Enums.md#enum-affected_animation) | Enum | Visuals applied to the target receiving the effect. | 1 |
| [`ally_animation`](./Enums.md#enum-ally_animation) | Enum | Distinct animation used when targeting a friendly unit. | 1 |
| `animate_name` | String | Animates the ability name text on cast. | 1 |
| `apex_distance` | Float | Calculations for the peak of a jump/lob arc. | 1 |
| `apex_time` | Float | Calculations for the peak of a jump/lob arc. | 1 |
| `bypass_combatspeed` | Boolean |  | 1 |
| [`damage_threshold_altanimations`](#damage_threshold_altanimations) | Block | Triggers different hit animations based on the amount of damage dealt. | 1 |
| [`dash_bonk_animation`](./Enums.md#enum-dash_bonk_animation) | Enum |  | 1 |
| [`default_face`](./Enums.md#enum-default_face) | Enum |  | 1 |
| `delay_from_map_center` | Boolean | Positional based timing delays. | 1 |
| `delay_from_reverse_map_edge` | Boolean |  | 1 |
| `do_animation_offscreen` | Boolean |  | 1 |
| `do_not_clear_placeholder` | Boolean |  | 1 |
| [`dodge`](./Enums.md#enum-dodge) | Enum |  | 1 |
| `face_targets` | Boolean | Forces the sprite to look at the target tile. | 1 |
| `first_castpoint_is_self_damage_only` | Boolean |  | 1 |
| `hang_time` | Float |  | 1 |
| `hud_palette` | Integer |  | 1 |
| `jump_speed_multiplier` | Float |  | 1 |
| `lob_speed` | Float | Adjustments for arcing projectiles. | 1 |
| `max_range` | Integer | The maximum and minimum distance required to cast. | 1 |
| `min_range` | Integer | The maximum and minimum distance required to cast. | 1 |
| `no_horizontal_flip` | Boolean |  | 1 |
| `othercat_placeholder_available` | Boolean |  | 1 |
| [`override_portrait`](./Enums.md#enum-override_portrait) | Enum |  | 1 |
| `precast_delay` | Float |  | 1 |
| `randomize_starting_frame` | Boolean |  | 1 |
| `status_display_count_max` | Integer |  | 1 |
| `uncatchable` | Boolean |  | 1 |
| `use_directional_animations` | Boolean |  | 1 |
| `use_origin_offsets` | Boolean |  | 1 |
| [`walk`](./Enums.md#enum-walk) | Enum |  | 1 |
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array |  | 0 |
| [`dead`](./Enums.md#enum-dead) | Enum |  | 0 |
| [`deadhit`](./Enums.md#enum-deadhit) | Enum |  | 0 |
| [`hit`](./Enums.md#enum-hit) | Enum |  | 0 |
| [`miss_random_delay`](./Arrays.md#array-miss_random_delay) | Array |  | 0 |
| [`non_blocking_animations`](./Arrays.md#array-non_blocking_animations) | Array |  | 0 |
| [`projectile_spawn_offset`](./Arrays.md#array-projectile_spawn_offset) | Array |  | 0 |
| [`random_delay`](./Arrays.md#array-random_delay) | Array | Adds chaotic timing to multi-projectile casts. | 0 |
| [`spawn_offset`](./Arrays.md#array-spawn_offset) | Array |  | 0 |
| [`stunned`](./Enums.md#enum-stunned) | Enum |  | 0 |
| [`weak`](./Enums.md#enum-weak) | Enum |  | 0 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

