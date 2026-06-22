# Mewgenics Mod Developer Documentation: Enum & String Dictionary

This document provides exhaustive lists of all enum and string values found in the base game's `.gon` files for every applicable property key.

> **Note on Values:** The lists below represent *Confirmed Values* extracted directly from the base game's source files. It is highly likely that there are other valid enum or string values supported by the engine that are simply not used in the vanilla files. You will need to experiment or rely on context clues to discover undocumented values.

## Enums Dictionary

### Enum: `template`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `spell` | |
| `self_buff` | |
| `melee_attack` | |
| `lobbed_attack` | |
| `spawn` | |
| `targeted_status` | |
| `straightshot_attack` | |
| `move` | |
| `dash_attack` | |
| `jump_attack` | |
| `teleport` | |
| `throw_attack` | |
| `ranged_attack` | |
| `tile_targeted_melee_attack` | |
| `placeholder` | |
| `swap` | |
| `trample_dash` | |
| `melee_spell` | |
| `return` | |
| `laser` | |
| `leave` | |
| `jump_move` | |
| `multihit_self_buff` | |

</details>


---

### Enum: `animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics), [`meta`](./Abilities_and_Spells.md#context-meta), [`Cat`](./Characters_and_Bosses.md#context-cat), [`NonCat`](./Characters_and_Bosses.md#context-noncat), [`Nothing`](./Characters_and_Bosses.md#context-nothing), [`StatusEachTurnBeginIfHasStatus`](./Characters_and_Bosses.md#context-statuseachturnbeginifhasstatus), [`TransformInXTurns`](./Characters_and_Bosses.md#context-transforminxturns), [`10coins`](./Events_and_Encounters.md#context-10coins), [`5coins`](./Events_and_Encounters.md#context-5coins), [`ROOT`](./Events_and_Encounters.md#context-root), [`a`](./Events_and_Encounters.md#context-a), [`activate_p`](./Events_and_Encounters.md#context-activate_p), [`activate_z`](./Events_and_Encounters.md#context-activate_z), [`attach_amplifier`](./Events_and_Encounters.md#context-attach_amplifier), [`attach_antenna`](./Events_and_Encounters.md#context-attach_antenna), [`attach_leech`](./Events_and_Encounters.md#context-attach_leech), [`b`](./Events_and_Encounters.md#context-b), [`bite`](./Events_and_Encounters.md#context-bite), [`blue`](./Events_and_Encounters.md#context-blue), [`boogers`](./Events_and_Encounters.md#context-boogers), [`book`](./Events_and_Encounters.md#context-book), [`brace`](./Events_and_Encounters.md#context-brace), [`button`](./Events_and_Encounters.md#context-button), [`buy1`](./Events_and_Encounters.md#context-buy1), [`c`](./Events_and_Encounters.md#context-c), [`counter`](./Events_and_Encounters.md#context-counter), [`d`](./Events_and_Encounters.md#context-d), [`damage`](./Events_and_Encounters.md#context-damage), [`donate`](./Events_and_Encounters.md#context-donate), [`donate_10`](./Events_and_Encounters.md#context-donate_10), [`donate_15`](./Events_and_Encounters.md#context-donate_15), [`donate_20`](./Events_and_Encounters.md#context-donate_20), [`donate_5`](./Events_and_Encounters.md#context-donate_5), [`double`](./Events_and_Encounters.md#context-double), [`enter`](./Events_and_Encounters.md#context-enter), [`examine`](./Events_and_Encounters.md#context-examine), [`fill_jar`](./Events_and_Encounters.md#context-fill_jar), [`find_another_way`](./Events_and_Encounters.md#context-find_another_way), [`fire`](./Events_and_Encounters.md#context-fire), [`future`](./Events_and_Encounters.md#context-future), [`go_around`](./Events_and_Encounters.md#context-go_around), [`holy`](./Events_and_Encounters.md#context-holy), [`home`](./Events_and_Encounters.md#context-home), [`hp`](./Events_and_Encounters.md#context-hp), [`ice`](./Events_and_Encounters.md#context-ice), [`ignore`](./Events_and_Encounters.md#context-ignore), [`infinite`](./Events_and_Encounters.md#context-infinite), [`intimidation`](./Events_and_Encounters.md#context-intimidation), [`itchies`](./Events_and_Encounters.md#context-itchies), [`knife`](./Events_and_Encounters.md#context-knife), [`leave`](./Events_and_Encounters.md#context-leave), [`leave_it_in`](./Events_and_Encounters.md#context-leave_it_in), [`lever`](./Events_and_Encounters.md#context-lever), [`lick`](./Events_and_Encounters.md#context-lick), [`lightning`](./Events_and_Encounters.md#context-lightning), [`loot`](./Events_and_Encounters.md#context-loot), [`loot_heart`](./Events_and_Encounters.md#context-loot_heart), [`makeup`](./Events_and_Encounters.md#context-makeup), [`nothanks`](./Events_and_Encounters.md#context-nothanks), [`past`](./Events_and_Encounters.md#context-past), [`pirouette`](./Events_and_Encounters.md#context-pirouette), [`place_gristle`](./Events_and_Encounters.md#context-place_gristle), [`poop`](./Events_and_Encounters.md#context-poop), [`protection`](./Events_and_Encounters.md#context-protection), [`put_in_coins`](./Events_and_Encounters.md#context-put_in_coins), [`receive`](./Events_and_Encounters.md#context-receive), [`red`](./Events_and_Encounters.md#context-red), [`reflect`](./Events_and_Encounters.md#context-reflect), [`run`](./Events_and_Encounters.md#context-run), [`run_again`](./Events_and_Encounters.md#context-run_again), [`sacrifice`](./Events_and_Encounters.md#context-sacrifice), [`sacrifice_full_favor`](./Events_and_Encounters.md#context-sacrifice_full_favor), [`sacrifice_normal`](./Events_and_Encounters.md#context-sacrifice_normal), [`sacrifice_partial_favor`](./Events_and_Encounters.md#context-sacrifice_partial_favor), [`sacrifice_quest`](./Events_and_Encounters.md#context-sacrifice_quest), [`skip`](./Events_and_Encounters.md#context-skip), [`speed`](./Events_and_Encounters.md#context-speed), [`surprise`](./Events_and_Encounters.md#context-surprise), [`take`](./Events_and_Encounters.md#context-take), [`take_blood`](./Events_and_Encounters.md#context-take_blood), [`tappytoes`](./Events_and_Encounters.md#context-tappytoes), [`thorns`](./Events_and_Encounters.md#context-thorns), [`touch`](./Events_and_Encounters.md#context-touch), [`w1`](./Events_and_Encounters.md#context-w1), [`w2`](./Events_and_Encounters.md#context-w2), [`w3`](./Events_and_Encounters.md#context-w3), [`w4`](./Events_and_Encounters.md#context-w4), [`w5`](./Events_and_Encounters.md#context-w5), [`w6`](./Events_and_Encounters.md#context-w6), [`wheezies`](./Events_and_Encounters.md#context-wheezies), [`CatAPultAnimation`](./Passives_and_Statuses.md#context-catapultanimation)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `choice_misc` | |
| `choice_leave` | |
| `shoot` | |
| `throwobject` | |
| `none` | |
| `attack` | |
| `pointout` | |
| `weaponswing` | |
| `floatingmagic` | |
| `choice_dex_alt` | |
| `eatTrinket` | |
| `showTrinket` | |
| `weaponpoke` | |
| `weaponshoot` | |
| `weaponthrowhigh` | |
| `weaponspell3` | |
| `spawn` | |
| `castspell` | |
| `throw` | |
| `weaponslam` | |
| `weaponthrowstraight` | |
| `sing3` | |
| `throwArrow` | |
| `dying` | |
| `druidTransform` | |
| `knockupatk` | |
| `selfHarm` | |
| `pray` | |
| `howl` | |
| `psyAttack1` | |
| `weaponspell` | |
| `drinkTrinket` | |
| `explode` | |
| `sliceOpen` | |
| `thinking` | |
| `angry` | |
| `spit` | |
| `transform` | |
| `grab` | |
| `lickAttack` | |
| `dashbite` | |
| `Default` | |
| `biteattack` | |
| `earthquakeSlam` | |
| `flex` | |
| `heal` | |
| `majormagic` | |
| `poopfart` | |
| `poopfartbehind` | |
| `pukeatk` | |
| `pulse` | |
| `roll` | |
| `slowPawMagic` | |
| `block` | |
| `blowFire` | |
| `buildRobot` | |
| `coinFlip` | |
| `createmagic` | |
| `doubleswat` | |
| `equipWeapon` | |
| `gulp` | |
| `hopinplace` | |
| `knockswatatk` | |
| `meow` | |
| `psyAttack3` | |
| `psyMegaAttack` | |
| `sing2` | |
| `singleSpin` | |
| `suck` | |
| `weaponstab` | |
| `blowUp` | |
| `buildRobotProjectile` | |
| `choice_coins_ten` | |
| `fartoom` | |
| `knead` | |
| `meditate` | |
| `revenge` | |
| `roar` | |
| `sing1` | |
| `spell` | |
| `thumbsup` | |
| `whistle` | |
| `backflipLoop` | |
| `bearHug` | |
| `bite` | |
| `brace` | |
| `bruise` | |
| `choice_con` | |
| `dash` | |
| `eat` | |
| `evilMagic` | |
| `groundpound` | |
| `holy` | |
| `idea` | |
| `invthrow` | |
| `jitter` | |
| `metronome` | |
| `scream` | |
| `spin` | |
| `stomp` | |
| `suplex` | |
| `tinker` | |
| `tinkerSelf` | |
| `change` | |
| `choice_coins_one` | |
| `choice_coins_twentyfive` | |
| `cry` | |
| `escape` | |
| `fart` | |
| `hadouken` | |
| `heaviestMelee` | |
| `kick` | |
| `poop` | |
| `portout` | |
| `puke` | |
| `rage` | |
| `reload` | |
| `run` | |
| `runincircles` | |
| `slam` | |
| `tauntwiggle` | |
| `tinyPunch` | |
| `turtlestart` | |
| `uppercutatk` | |
| `Quiver` | |
| `alertend` | |
| `bash` | |
| `bigkick` | |
| `birth` | |
| `blast1` | |
| `blowKiss` | |
| `bombardment` | |
| `call` | |
| `cartwheelLoop` | |
| `celebrate` | |
| `changechannel` | |
| `cheat` | |
| `chew` | |
| `consume` | |
| `counter` | |
| `dig` | |
| `digest` | |
| `doublevision` | |
| `drop` | |
| `enrage` | |
| `fail` | |
| `fire` | |
| `fizzle` | |
| `glare` | |
| `grow` | |
| `hatch` | |
| `headbutt` | |
| `headbuttUppercut` | |
| `heil` | |
| `ice` | |
| `magnet` | |
| `megabite` | |
| `megablast` | |
| `meteorshower` | |
| `monkAttack` | |
| `order` | |
| `pickup` | |
| `poke` | |
| `power` | |
| `proud` | |
| `psyAttack2` | |
| `puff` | |
| `pulp` | |
| `quarterswipe` | |
| `raise` | |
| `react` | |
| `scratchear` | |
| `shield` | |
| `spike` | |
| `spikes` | |
| `squeeze` | |
| `statusReaction` | |
| `stoneFists` | |
| `struggle` | |
| `summon` | |
| `swipe` | |
| `tailwhip` | |
| `transform1` | |
| `transform2` | |
| `transform3` | |
| `weaponAbsorb` | |
| `weaponSpinAttack` | |
| `web` | |
| `yell` | |
| `ColorlessStartTurn` | |
| `MonkStartTurn` | |
| `RocketFromAbove` | |
| `angryfail` | |
| `appear` | |
| `attach` | |
| `attack2` | |
| `attackL` | |
| `attackR` | |
| `attackRage` | |
| `beam` | |
| `beamin` | |
| `becomemutant` | |
| `becomezealot` | |
| `bellypound` | |
| `bigdoubleswat` | |
| `blast2` | |
| `bless` | |
| `blizzard` | |
| `bodypulse` | |
| `bomb` | |
| `bounce` | |
| `breakarm` | |
| `breakleg` | |
| `breakneck` | |
| `breakshield` | |
| `breathing` | |
| `burp` | |
| `butcherAttack` | |
| `buttScootLoop` | |
| `calmdown` | |
| `catdying` | |
| `charge` | |
| `chargedodges` | |
| `chargeholy` | |
| `charm` | |
| `chestpound` | |
| `chewing` | |
| `clapTogether` | |
| `controlmonster` | |
| `crash` | |
| `cry1` | |
| `cry2` | |
| `curlup` | |
| `curse` | |
| `cut` | |
| `dashend` | |
| `detonate` | |
| `dodge` | |
| `doom` | |
| `doublepunch` | |
| `drink` | |
| `egg` | |
| `eject` | |
| `entangle` | |
| `exhale` | |
| `exit` | |
| `falconPunch` | |
| `fast` | |
| `firestorm` | |
| `flames` | |
| `flip` | |
| `flush` | |
| `freeze` | |
| `fumble` | |
| `fumble2` | |
| `fury` | |
| `fx_statup` | |
| `grabCorpse` | |
| `growup` | |
| `guard` | |
| `gutball` | |
| `haunt` | |
| `heartattack` | |
| `heavyMelee` | |
| `hide` | |
| `hiss` | |
| `hithard` | |
| `hug` | |
| `humandie` | |
| `icebreath` | |
| `identify` | |
| `inhale` | |
| `insane` | |
| `intro` | |
| `jab` | |
| `jetloop` | |
| `karateKid` | |
| `kicksand` | |
| `kiss` | |
| `laserShoot` | |
| `launch` | |
| `lava` | |
| `leave` | |
| `lick` | |
| `lift` | |
| `liquidclone` | |
| `liquidmetalspear` | |
| `liquidunclone` | |
| `loot` | |
| `megaslap` | |
| `mindcontrol` | |
| `mouthbeam` | |
| `moveLoop` | |
| `necksnap` | |
| `nuke` | |
| `open` | |
| `openmouth` | |
| `peck` | |
| `pickpocket` | |
| `pissYourself` | |
| `portin` | |
| `powder` | |
| `powerup` | |
| `prime` | |
| `probe` | |
| `prouder` | |
| `pullin` | |
| `pullremote` | |
| `pulse2` | |
| `pulse3` | |
| `punchSelf` | |
| `radiant` | |
| `reaction` | |
| `recharge` | |
| `reflex` | |
| `releaseCommand1` | |
| `releaseCommand2` | |
| `releaseCommand3` | |
| `releaseCommand4` | |
| `resultExplode` | |
| `resultJackpot` | |
| `resultLose` | |
| `resultWin` | |
| `return` | |
| `revive` | |
| `ripandtear` | |
| `rise` | |
| `rumble` | |
| `scorpionSting` | |
| `scratch` | |
| `shake` | |
| `shocking` | |
| `shootForward` | |
| `shootLava` | |
| `shoulder` | |
| `showclaws` | |
| `shred` | |
| `shriek` | |
| `shrink` | |
| `spawnChild` | |
| `spawnHolding` | |
| `spawnHoldingCat` | |
| `spawnmama` | |
| `special` | |
| `spinAttack` | |
| `splashatk` | |
| `spore` | |
| `statup` | |
| `stompy` | |
| `strike` | |
| `suck1` | |
| `suck2` | |
| `suggest` | |
| `suicide` | |
| `swat` | |
| `swatupatk` | |
| `swing` | |
| `tailwag` | |
| `tantrum` | |
| `tapatk` | |
| `telekinesis` | |
| `terminatorPunch` | |
| `thrash` | |
| `throwbigelement` | |
| `throwboss` | |
| `throwshield` | |
| `tinkerAdjacent` | |
| `trip` | |
| `tripleswat` | |
| `turnOff` | |
| `uncrack` | |
| `unguard` | |
| `uppercut` | |
| `use` | |
| `uziShoot` | |
| `vomitrain` | |
| `walk` | |
| `walk2` | |
| `walkAngry` | |
| `weaponTina` | |
| `weaponspell2` | |
| `weaponswingup` | |
| `whisper` | |
| `wind` | |
| `wisps` | |
| `yell1` | |
| `yell2` | |
| `yell3` | |
| `yella` | |
| `yellb` | |
| `zombie` | |

</details>


---

### Enum: `class`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root), [`meta`](./Abilities_and_Spells.md#context-meta), [`ClassManaCostReduction`](./Cat_Mutations.md#context-classmanacostreduction), [`ClassManaCostReduction`](./Items_and_Equipment.md#context-classmanacostreduction), [`ClassManaCostReduction`](./Passives_and_Statuses.md#context-classmanacostreduction), [`ROOT`](./Passives_and_Statuses.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Colorless` | |
| `Disorder` | |
| `Druid` | |
| `Necromancer` | |
| `Mage` | |
| `Fighter` | |
| `Hunter` | |
| `Tank` | |
| `Butcher` | |
| `Medic` | |
| `Monk` | |
| `Thief` | |
| `Tinkerer` | |
| `Psychic` | |
| `PlaceholderMeleeAttackAbility` | |
| `DamageConsumedCharactersAbility` | |
| `MultiHitMeleeAttackAbility` | |
| `MeleeEatAbility` | |
| `AOESpellAbility` | |
| `Jester` | |
| `BounceDashAbility` | |
| `FullyAnimatedDashAttackAbility` | |
| `MeleeAttackAbility` | |
| `SuplexAbility` | |
| `CloneAbility` | |
| `JumpAttackAbility` | |
| `MultiTargetRangedAttackAbility` | |
| `PierceDashAbility` | |
| `RangedAttackAbility` | |
| `TeleportEatAbility` | |
| `DashAttackAbility` | |
| `GoOffMapAbility` | |
| `KaijuSpinThrowAbility` | |
| `LaserAbility` | |
| `MoveAbility` | |
| `ReturnToMapAbility` | |
| `SpawnAbility` | |
| `StraightShotRanged` | |
| `SwapperAbility` | |
| `TeleportAbility` | |
| `ThrowAbility` | |
| `TrampleDashAbility` | |

</details>


---

### Enum: `variant_of`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root), [`ROOT`](./Characters_and_Bosses.md#context-root), [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicMelee` | |
| `PlayerCat` | |
| `FoodBase` | |
| `SpawnTerminatorMini_Base` | |
| `cm_ClassSeal` | |
| `IrradiatedObject` | |
| `PickupBase` | |
| `wp_IrradiatedObject` | |
| `Coin` | |
| `static_object_template` | |
| `BasicJump` | |
| `Maggot` | |
| `CavePerson` | |
| `Cultist` | |
| `Fly` | |
| `BirdLarge` | |
| `BirdMed` | |
| `BirdSmall` | |
| `FlailBase` | |
| `HitlerPulpBase` | |
| `SpewerSuck_base` | |
| `wp_MoneyBag` | |
| `BasicBigMelee` | |
| `Bear` | |
| `BirdBase` | |
| `CovenRise1` | |
| `CrowFlap` | |
| `DefaultMove` | |
| `FormShrinkFour` | |
| `GrubFamiliarBase` | |
| `Hyde` | |
| `MechSuit` | |
| `Pooter` | |
| `Stick` | |
| `Toad` | |
| `Asteroid` | |
| `BasicStraightShot` | |
| `BirthSquirrel` | |
| `BreakShortCircuit` | |
| `Catbot` | |
| `ChargeyMaggot` | |
| `Clot` | |
| `CopBot` | |
| `Crow` | |
| `CrowFlutter` | |
| `Endeavor` | |
| `EscapeBase` | |
| `EvilIncarnate` | |
| `Fetus` | |
| `Flea` | |
| `FlySwarm` | |
| `FormGrowTwo` | |
| `Hadouken` | |
| `MagicMissile` | |
| `Metronome` | |
| `Pinky` | |
| `PlayerCat_FinalBossClone` | |
| `PsychicChoke` | |
| `Rat` | |
| `Reanimate` | |
| `Reset` | |
| `SpewerPill_Normal` | |
| `SpikyCactus` | |
| `Spit` | |
| `StruggleBase` | |
| `SwappyMaggot` | |
| `TVChangeObey` | |
| `TankSwap` | |
| `TinySpider` | |
| `TumorousMaggot` | |
| `ZombieCatFamiliar` | |
| `wp_MeatHook` | |
| `Absorb` | |
| `AbsorbSoul` | |
| `Adoubement` | |
| `Aftershock` | |
| `AirBurst` | |
| `AlterDNA` | |
| `Amoeba` | |
| `AncestralRecall` | |
| `Anchor` | |
| `AnimalEgg` | |
| `AnimateDead` | |
| `AnimatedBoulder` | |
| `AnimatedSmallRock` | |
| `Anoint` | |
| `AntlerSwipe` | |
| `Apprentice` | |
| `ArmorUp` | |
| `ArrowFlurry` | |
| `ArrowSmith` | |
| `AssBlast` | |
| `Assassinate` | |
| `AssertDominance` | |
| `AttackAgain` | |
| `AutoPilot` | |
| `Awaken` | |
| `BBQ` | |
| `BabyDeathWorm` | |
| `BackBreaker` | |
| `Backflip` | |
| `BadBone` | |
| `BadGas` | |
| `BallOfSpiders` | |
| `Baptism` | |
| `BarfBall` | |
| `BasicButcherMeleeWideSpin` | |
| `BasicMagicMissile` | |
| `BasicRanged` | |
| `BasicTankMelee` | |
| `BatterUp` | |
| `Battery` | |
| `BatteryNuke` | |
| `BattleCry` | |
| `BearHug` | |
| `BearTrap` | |
| `BearTrap_Enemy` | |
| `BecomeEntropy` | |
| `BelcherLavashot` | |
| `BellyFlop` | |
| `Benediction` | |
| `Berserk` | |
| `BerserkDash` | |
| `BestowWisdom` | |
| `BigDemon` | |
| `BigPunch` | |
| `BigRock` | |
| `BigStick` | |
| `BiggestStick` | |
| `Binge` | |
| `Blast` | |
| `BlindingFlash` | |
| `BlindingLight` | |
| `Blizzard` | |
| `Block` | |
| `BloodGeyser` | |
| `BloodMagic` | |
| `BloodRain` | |
| `Bloodletting` | |
| `Bloodzerk` | |
| `Blow` | |
| `BlowKiss` | |
| `Blur` | |
| `BodyGuard` | |
| `BodySlam` | |
| `Bolt` | |
| `BombExplode` | |
| `BombShot` | |
| `Bombchu` | |
| `BonusToss` | |
| `BoostBackstab` | |
| `BoostSpellRange` | |
| `Booster` | |
| `Bottles` | |
| `Boulder` | |
| `BounceShot` | |
| `Bowl` | |
| `BowlDash` | |
| `BowlOver` | |
| `BrainDrain` | |
| `BrambleBurst` | |
| `BrambleShot` | |
| `BreakingPoint` | |
| `Bruise` | |
| `BuddyUp` | |
| `BuildNuke` | |
| `BuildTurret` | |
| `Bump` | |
| `BungaWarrior1` | |
| `Bunker` | |
| `BurgeoningBarrier` | |
| `BurgeoningBattery` | |
| `BurgeoningBlast` | |
| `Burp` | |
| `Burst` | |
| `Butcher` | |
| `ButcherCat` | |
| `ButcherPurge` | |
| `ButtScoot` | |
| `BuyCatnip` | |
| `CPR` | |
| `CallOver` | |
| `CallTheWind` | |
| `Caltrops` | |
| `Camouflage` | |
| `CancerCat` | |
| `CannonBall` | |
| `CarrionShot` | |
| `CarrionShot_Afterlife` | |
| `Cartwheel` | |
| `CatNap` | |
| `CatapultJump` | |
| `CaveBaby` | |
| `ChaChaSlide` | |
| `ChainLightning` | |
| `Chakram` | |
| `Challenge` | |
| `ChaosShot` | |
| `ChaosSwap` | |
| `ChaosTeleport` | |
| `ChargeFists` | |
| `CharmTrap` | |
| `CharmedFetus` | |
| `CharmedFlea` | |
| `CharmedFly` | |
| `CharmedKitten` | |
| `Cheat` | |
| `Cheerlead` | |
| `Cherub` | |
| `Chew` | |
| `ChewCud` | |
| `Chomp` | |
| `Chonkwalk` | |
| `ChosenWarrior` | |
| `CircleOfProtection` | |
| `Clap` | |
| `Cleanse` | |
| `ClewOfLeeches` | |
| `CoffinFlop` | |
| `CoffinFlop_Afterlife` | |
| `CoinToss` | |
| `ColdShoulder` | |
| `CollectPelt` | |
| `ComboPull` | |
| `ComboThrow` | |
| `Confront` | |
| `Confusion` | |
| `Consume` | |
| `Contaminate` | |
| `Contort` | |
| `ControlAir` | |
| `ControlPlants` | |
| `ControlPlantsPartTwo` | |
| `ControlWater` | |
| `ControlWaterPartTwo` | |
| `Convert` | |
| `CookedBigFood` | |
| `Copycat` | |
| `Corrupt` | |
| `CosmicPunch` | |
| `Cough` | |
| `Craft` | |
| `CraftArrow` | |
| `Crate` | |
| `Creshendo` | |
| `CrimsonMask` | |
| `CrossShot` | |
| `Crossbow` | |
| `Crusade` | |
| `Crushinator` | |
| `CryoHeal` | |
| `CumulativeBlast` | |
| `CupidsArrow` | |
| `Curse` | |
| `CutPurse` | |
| `DaddyShark` | |
| `DarkStep` | |
| `Dart` | |
| `Dash` | |
| `DeathMetal` | |
| `DeathWind` | |
| `DeathWormTrampleDash` | |
| `Debone` | |
| `Declaw` | |
| `Decoy` | |
| `DeepDive` | |
| `Demolish` | |
| `DemonicPact` | |
| `Desecrate` | |
| `DetectWeakness` | |
| `DexterousHit` | |
| `DigUpTheDead` | |
| `Dip` | |
| `Discharge` | |
| `Distract` | |
| `Diversion` | |
| `Divide` | |
| `DivineGift` | |
| `DivineProtection` | |
| `DoctorBot` | |
| `DollUp` | |
| `Donate` | |
| `DonateBlood` | |
| `DonateBlood_Afterlife` | |
| `DonateEnergy` | |
| `DoomPunch` | |
| `Double` | |
| `DoubleDragon` | |
| `DoubleLoot` | |
| `DragonPunch` | |
| `DrawAttention` | |
| `DrillDown` | |
| `DruidCrow` | |
| `DruidSwap` | |
| `DumbMove` | |
| `Dummy` | |
| `Dump` | |
| `DustDevil` | |
| `DybbukPossess` | |
| `EagleEye` | |
| `Earthquake` | |
| `Echo` | |
| `EjectButton` | |
| `ElectricNail` | |
| `Electrolyze` | |
| `Emergency` | |
| `EmptyMind` | |
| `EnchantingPoop` | |
| `Encourage` | |
| `Enlarge` | |
| `Enlighten` | |
| `Enrage` | |
| `Entangle` | |
| `Ethereal` | |
| `ExhaustingBlow` | |
| `ExperimentalTeleporter` | |
| `ExtraTurnQuestion` | |
| `EyeForAnEye` | |
| `Fabricate` | |
| `Fade` | |
| `FamiliarSelfDestruct` | |
| `Fartoom` | |
| `FastForward` | |
| `FastHands` | |
| `FatMan` | |
| `FaultLine` | |
| `FeatherFeet` | |
| `FecalHood` | |
| `FecalMask` | |
| `FecalNecklace` | |
| `FighterCat` | |
| `FighterLeap` | |
| `FighterTaunt` | |
| `FindARock` | |
| `Finisher` | |
| `FireBolt` | |
| `FireFart` | |
| `FirePunch` | |
| `FireShot` | |
| `FireSurge` | |
| `Fireball` | |
| `Firecrackers` | |
| `Fissure` | |
| `FistOfFate` | |
| `FlashForward` | |
| `Flatline` | |
| `FleaShot` | |
| `FleshGolem` | |
| `FleshLad` | |
| `Flex` | |
| `Flicker` | |
| `Flip` | |
| `FlipFlop` | |
| `Floast` | |
| `Floater` | |
| `FlowerFeet` | |
| `Flush` | |
| `FlyingFist` | |
| `Focus` | |
| `FocusShot` | |
| `FollowUpDash` | |
| `ForbiddenFamine` | |
| `ForbiddenFart` | |
| `ForbiddenFlame` | |
| `ForbiddenFlood` | |
| `ForbiddenFrost` | |
| `ForbiddenFulmination` | |
| `ForceBlast` | |
| `ForceCone` | |
| `FormGrowThree` | |
| `FormShrinkOne` | |
| `FormShrinkTwo` | |
| `FreezeRay` | |
| `FreezerBurn` | |
| `FreshOffTheForge` | |
| `FriendOrFoe` | |
| `FromTheTrees` | |
| `FullForce` | |
| `FullMoon` | |
| `FurySwipes` | |
| `FurySwipes_Enemy` | |
| `FutureBot` | |
| `FutureBotPunch` | |
| `FutureSight` | |
| `FuzzerJump` | |
| `G3Shake` | |
| `GainThorns` | |
| `Gamble` | |
| `Gamete` | |
| `GangUp` | |
| `Gassy_AssBlast` | |
| `GeoLad` | |
| `GetDown` | |
| `Gib` | |
| `GigaDrain` | |
| `Glare` | |
| `GlassShard` | |
| `GlowingMushroom` | |
| `GlowingMushroomGiveMana` | |
| `GoLimp` | |
| `GoodBone` | |
| `Gore` | |
| `GrantLife` | |
| `Grapnel` | |
| `Grapple` | |
| `Gravecrawl` | |
| `GravitySlam` | |
| `GreedStep` | |
| `Grill` | |
| `Groom` | |
| `GuardianAngel` | |
| `GunCat` | |
| `Gust` | |
| `GymMembership` | |
| `HailOfNails` | |
| `HallowedGround` | |
| `Hallucinate` | |
| `HangerBot` | |
| `HardenSkin` | |
| `Harpoon` | |
| `Haste` | |
| `HeadButt` | |
| `HeadTumor` | |
| `HealingFall` | |
| `HealingSalve` | |
| `Heathens` | |
| `HeavyShot` | |
| `HereticMark` | |
| `HipToss` | |
| `HireHitman` | |
| `Hiss` | |
| `HitlerHeadGrowA` | |
| `HitlerPulp1` | |
| `HogRush` | |
| `HolyBlood` | |
| `HolyLight` | |
| `HolyStep` | |
| `HolyWeapon` | |
| `HomingBlasts` | |
| `Hone` | |
| `HookBind` | |
| `HopAndBlock` | |
| `HornyCat` | |
| `HoseOff` | |
| `Huddle` | |
| `HundredHandSlap` | |
| `Hunt` | |
| `Hurl` | |
| `Hush` | |
| `Husk` | |
| `HydroPump` | |
| `HyperBeam` | |
| `IceArmor` | |
| `IcePunch` | |
| `IceSurge` | |
| `IcicleTaser` | |
| `Improve` | |
| `IncreaseGravity` | |
| `Indigestion_Fart` | |
| `Inferno` | |
| `Infest` | |
| `Infiltrate` | |
| `Inhale` | |
| `InspirationalSong` | |
| `Inspire` | |
| `InstantBarrier` | |
| `Interchange` | |
| `Intimidate` | |
| `Inversion` | |
| `IronHead` | |
| `Itch` | |
| `JarHeadDeath` | |
| `JesterCat` | |
| `Jitter` | |
| `JohnnyPush` | |
| `Jolt` | |
| `Juiced` | |
| `Kamehameha` | |
| `KiBurst` | |
| `KineticCharge` | |
| `KirbyFetus` | |
| `Kitten` | |
| `Knead` | |
| `Lacerate` | |
| `Landscape` | |
| `LastGasp` | |
| `LastHit` | |
| `LastThought` | |
| `Leaper` | |
| `LeechSwarm` | |
| `Leeches` | |
| `LennyHug` | |
| `Lice` | |
| `LickHeal` | |
| `LifeDrain` | |
| `LifeDrain_Afterlife` | |
| `LightenTheLoad` | |
| `LightningSurge` | |
| `LineShot` | |
| `LodgeHook` | |
| `Log` | |
| `LookAtMe` | |
| `LootCorpse` | |
| `LotteryShottery` | |
| `LoveBot` | |
| `LoveTap` | |
| `LuckyPenny` | |
| `Lullaby` | |
| `LunchTime` | |
| `Lunge` | |
| `MCFlamethrower` | |
| `MD_Walk` | |
| `MageCat` | |
| `MageSwap` | |
| `MageTeleport` | |
| `MaggotLord` | |
| `Magnet` | |
| `MagnetPull` | |
| `Magnify` | |
| `Malaise` | |
| `Mammoth` | |
| `MammothBaby` | |
| `ManaBomb` | |
| `ManaDrain` | |
| `ManaMeld` | |
| `ManglerFumbleEven` | |
| `Mangy2` | |
| `Manifest` | |
| `MassHysteria` | |
| `MassManaLeech` | |
| `MassPsychosis` | |
| `Math` | |
| `MedicCat` | |
| `MedicObey` | |
| `Medusa` | |
| `MegaBlast` | |
| `MegaDinoLeg` | |
| `MegaGrav` | |
| `MegaGuppy_SlamRight` | |
| `MeleeHeal` | |
| `Metabolize` | |
| `MeteorSlam` | |
| `MeteorStorm` | |
| `Mimic` | |
| `MindBlast` | |
| `MindControl` | |
| `MindCrack` | |
| `MindCrack_EldritchVisage` | |
| `MindMeld` | |
| `MiniDistract` | |
| `MiniHook` | |
| `MockingbirdForm` | |
| `Momentum` | |
| `Monch` | |
| `MonkCat` | |
| `MonkeyThrow` | |
| `MoonHandDash` | |
| `MoonHandDrop` | |
| `MoonHandThrow` | |
| `MoonHead_SpitCat` | |
| `MotherTumor` | |
| `MoveAgain` | |
| `MoveOne` | |
| `MuscleMemory` | |
| `Mutilate` | |
| `MyTurn` | |
| `NailFlurry` | |
| `NaturesBlessing` | |
| `NecroCat` | |
| `NeedleShot` | |
| `Nerf` | |
| `NeutronStar` | |
| `Nightshade` | |
| `Nip` | |
| `Nirvana` | |
| `NubsJump` | |
| `Nudge` | |
| `NurseBot` | |
| `NurseBotHeal` | |
| `OnePunch` | |
| `OneTwoPunch` | |
| `OneWithTheWind` | |
| `OpenWounds` | |
| `Order` | |
| `Outskirts` | |
| `Pass` | |
| `PathOfTheMage` | |
| `PathOfThePsychic` | |
| `PathOfTheTank` | |
| `PathOfTheVoid` | |
| `Pawbreaker` | |
| `PerfectForm` | |
| `PersistentHunt` | |
| `PersuasionDevice` | |
| `Pestilence` | |
| `PickPocket` | |
| `Picnic` | |
| `Pierce` | |
| `PierceShot` | |
| `Pile` | |
| `Ping` | |
| `PissYourself` | |
| `PlantFeet` | |
| `PlantMushroom` | |
| `PlayDead` | |
| `PlayerCat_MiniMe` | |
| `PocketSand` | |
| `Pogo` | |
| `PoisonDip` | |
| `PoisonGas` | |
| `PoisonLace` | |
| `PoisonNail` | |
| `Poke` | |
| `PokeWound` | |
| `Ponder` | |
| `Poop` | |
| `Porcupine` | |
| `Position` | |
| `Pounce` | |
| `PoundOfFlesh` | |
| `PowerUp` | |
| `Prance` | |
| `Prayer` | |
| `PrepareToJump` | |
| `Propell` | |
| `PsyFlutter` | |
| `PsychicCat` | |
| `PullToSafety` | |
| `Pummel` | |
| `PunchBot` | |
| `Puppet` | |
| `Purge` | |
| `Purr` | |
| `Push` | |
| `PushMove` | |
| `PushThrough` | |
| `QuickAttack` | |
| `QuickRoll` | |
| `RNGCannon` | |
| `RagePunch` | |
| `RaiseTheDead` | |
| `Rally` | |
| `RallyCharge` | |
| `Ram` | |
| `RangedHeal` | |
| `RapidFlowSpin` | |
| `RaptorBaby` | |
| `RattleSnake` | |
| `Reach` | |
| `ReadMind` | |
| `RealityScramble` | |
| `ReallyFastRun` | |
| `Reap` | |
| `Reaper` | |
| `ReaperStep` | |
| `Rebound` | |
| `Rebuke` | |
| `Recycle` | |
| `RedCap` | |
| `Reduce` | |
| `RefineMaterials` | |
| `Reflect` | |
| `Reflux` | |
| `Regurge` | |
| `Rehook` | |
| `ReleaseEnergy` | |
| `RemoteDetonator` | |
| `Repair` | |
| `Replace` | |
| `Reposition` | |
| `Reprogram` | |
| `Research` | |
| `Rest` | |
| `Reverberate` | |
| `ReverseDamage` | |
| `Revive` | |
| `Roast` | |
| `RoboVac` | |
| `RoboVacuum` | |
| `RockBlast` | |
| `RockCrusher` | |
| `RockTomb` | |
| `RockToss` | |
| `RockToss_ColorlessCat` | |
| `RocketRide` | |
| `RocketSkates` | |
| `Roll` | |
| `RoughToss` | |
| `Rouse` | |
| `RussianRoulette` | |
| `SafetyDance` | |
| `Sandstorm` | |
| `Scare` | |
| `Scary` | |
| `ScatterShot` | |
| `Scavenge` | |
| `ScorpionCat` | |
| `ScoutMe` | |
| `ScuffItOff` | |
| `Seance` | |
| `Seance_Afterlife` | |
| `SecurityBot` | |
| `SelfMutilate` | |
| `Serenade` | |
| `SeverArtery` | |
| `Shadow` | |
| `Shadowshift` | |
| `Shank` | |
| `Shards` | |
| `SharpNail` | |
| `Sharpen` | |
| `SharpenClaws` | |
| `SharpenNail` | |
| `ShedScrap` | |
| `Shift` | |
| `ShockTherapy` | |
| `Shockwave` | |
| `ShoddyJetpack` | |
| `ShortCircuit` | |
| `Shred` | |
| `Shriek` | |
| `SideSlash` | |
| `SideStep` | |
| `SkeletonCat` | |
| `SkeletonCatFamiliar` | |
| `SkeletonShambler` | |
| `SkinDisguise` | |
| `SkullBash` | |
| `SkyShatter` | |
| `Slapback` | |
| `SleeperHold` | |
| `Slice` | |
| `SliceAndDice` | |
| `SlingShade` | |
| `SlingShot` | |
| `SlipThrough` | |
| `Slipstream` | |
| `SlopThePigs` | |
| `SlotResult_Explode` | |
| `Slow` | |
| `Smack` | |
| `SmallRock` | |
| `SmartMetronome` | |
| `Smash` | |
| `SmellBlood` | |
| `Smolder` | |
| `Snacks` | |
| `Snake` | |
| `SnakeyBones` | |
| `Snatch` | |
| `SneakUp` | |
| `Snipe` | |
| `SoldierBot` | |
| `SongOfSpring` | |
| `SoothingGlow` | |
| `SoulLink` | |
| `SoulReap` | |
| `SoulSuck` | |
| `SoulTransfer` | |
| `SpareParts` | |
| `Sparks` | |
| `SpawnBaitTrap` | |
| `SpawnBomb` | |
| `SpawnDecoy` | |
| `SpawnMaggotFriend` | |
| `SpawnPooterFriend` | |
| `SpawnTomTomFriend` | |
| `SpewerPillTubeL` | |
| `SpiderEgg` | |
| `SpiderInjector` | |
| `SpikeTrap` | |
| `SpikyRock` | |
| `Spin` | |
| `SpiritBomb` | |
| `Spoil` | |
| `Spookie` | |
| `SpringShoes` | |
| `Spur` | |
| `SquirrelForm` | |
| `SquirrelFurySwipes` | |
| `SquirrelSquad` | |
| `StackTheDeck` | |
| `Stacy2p0` | |
| `StakeOut` | |
| `Stalk` | |
| `Stasis` | |
| `StealKidney` | |
| `StealTime` | |
| `SteelSkin` | |
| `StemCat` | |
| `Step` | |
| `Stimulants` | |
| `StoneGaze` | |
| `Stoopzerk` | |
| `SubwayRide` | |
| `Succ` | |
| `SuckerPunch` | |
| `Suggestion` | |
| `SummonBear` | |
| `SummonBones` | |
| `SummonBrambles` | |
| `SummonCatepillar` | |
| `SummonShade` | |
| `SummonSnake` | |
| `SummonSquirrel` | |
| `SummonToad` | |
| `SummonTurtle` | |
| `Sunburn` | |
| `SuperCrateBox` | |
| `Supernova` | |
| `Suplex` | |
| `Supper` | |
| `Suppress` | |
| `Surf` | |
| `Swallow` | |
| `Swat` | |
| `SwiftSanctify` | |
| `Switcheroo` | |
| `Synthesize` | |
| `T1ThrowGrenadeA` | |
| `THC_CoinRoll` | |
| `TacticalRetreat` | |
| `TailWhip` | |
| `Taint` | |
| `TaintedOffering` | |
| `TallBot` | |
| `TallSkeletonCat` | |
| `TallSpiderCat` | |
| `TankRockSong` | |
| `TankTantrum` | |
| `TankTrample` | |
| `TapLand` | |
| `TarBaby` | |
| `Taser` | |
| `Taunt` | |
| `Teach` | |
| `TeamFlex` | |
| `TeamFlex_Impl` | |
| `TeamSpin` | |
| `Tease` | |
| `Telefrag` | |
| `Telekinesis` | |
| `Teleport` | |
| `TerrainWalk` | |
| `TeslaCoil` | |
| `TheDestroyer` | |
| `Thicken` | |
| `ThiefCat` | |
| `ThiefSwap` | |
| `ThinkDeep` | |
| `ThinkTooHard` | |
| `ThornyFeet` | |
| `ThrobShot` | |
| `ThrowEgg` | |
| `ThrowShield` | |
| `ThrowSpiritBomb` | |
| `ThumpSlam` | |
| `ThunderPunch` | |
| `Thunderburst` | |
| `TigerForm` | |
| `TigerSwipes` | |
| `Till` | |
| `TimeWalk` | |
| `TinaBasicBigMelee` | |
| `TinkererCat` | |
| `TinkererTurret` | |
| `TinyTumor` | |
| `Tire` | |
| `ToTheRescue` | |
| `Toadie` | |
| `Toast` | |
| `TomTom` | |
| `TormentorThrow` | |
| `Toss` | |
| `Track` | |
| `TradeLife` | |
| `TradeLife_Afterlife` | |
| `TrailBlazer` | |
| `TrainArms` | |
| `TrainBody` | |
| `TrainLegs` | |
| `TrainMind` | |
| `TrampleMove` | |
| `Transcend` | |
| `TreeForm` | |
| `TriAttack` | |
| `TripleNails` | |
| `Trudge` | |
| `Tryptophan` | |
| `Tumble` | |
| `TurnFoe` | |
| `TwinShot` | |
| `Twister` | |
| `UnbridledHits` | |
| `Unearth` | |
| `UnimpededLunge` | |
| `UnreliableMissile` | |
| `UnreliableShield` | |
| `Upgrade` | |
| `Uppercut` | |
| `Vaccuum` | |
| `VenomBarrage` | |
| `VetVisit` | |
| `VoltTackle` | |
| `Vurp` | |
| `Waggle` | |
| `WallOfFire` | |
| `WarCry` | |
| `WarmupStretch` | |
| `Warp` | |
| `WasteTime` | |
| `WaterSphere` | |
| `WeAreOne` | |
| `WeAreTheChampions` | |
| `WeWillRockYou` | |
| `WeakeningNail` | |
| `Weakness` | |
| `WebTrap` | |
| `WetHairball` | |
| `Whisper` | |
| `WhiteRabbit` | |
| `WindSlash` | |
| `WindUp` | |
| `WindyStep` | |
| `Wish` | |
| `WitchHunt` | |
| `Withdraw` | |
| `WrathOfGod` | |
| `YeticatSnowball` | |
| `YouSeeNothing` | |
| `Zap` | |
| `Zealot` | |
| `Zoomzerk` | |
| `cWaggle` | |
| `cWaggle2x2` | |
| `cm_HealPercent` | |
| `face_FartFace` | |
| `head_SpiderInjector` | |
| `neck_NukeBonus` | |
| `tk_WaterBottle_Full` | |
| `wp_22Rifle` | |
| `wp_Blackjack` | |
| `wp_GlassCannon` | |
| `wp_Shotgun` | |
| `wp_Uzi` | |
| `wp_ZodiacsSixshooter` | |

</details>


---

### Enum: `kind`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `trinket` | |
| `weapon` | |
| `head` | |
| `face` | |
| `neck` | |
| `modifier` | |

</details>


---

### Enum: `rarity`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `rare` | |
| `uncommon` | |
| `very_rare` | |
| `common` | |
| `sidequest` | |
| `quest` | |
| `consumable_common` | |
| `consumable_rare` | |
| `consumable_uncommon` | |
| `consumable_very_rare` | |

</details>


---

### Enum: `object`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AfterImage`](./Abilities_and_Spells.md#context-afterimage), [`DustOnHit`](./Abilities_and_Spells.md#context-dustonhit), [`LeaveBehind`](./Abilities_and_Spells.md#context-leavebehind), [`ObjectOnHit`](./Abilities_and_Spells.md#context-objectonhit), [`ObjectOnHitCharacter`](./Abilities_and_Spells.md#context-objectonhitcharacter), [`PopAndSpawn`](./Abilities_and_Spells.md#context-popandspawn), [`spawn`](./Abilities_and_Spells.md#context-spawn), [`SpawnEachTurn`](./Cat_Mutations.md#context-spawneachturn), [`SpawnExtraThingsOnBattleStart`](./Cat_Mutations.md#context-spawnextrathingsonbattlestart), [`SpawnOnBattleStartRandomEmptyTile`](./Cat_Mutations.md#context-spawnonbattlestartrandomemptytile), [`SpawnThingOnDamage`](./Cat_Mutations.md#context-spawnthingondamage), [`SpawnThingOnDamage`](./Characters_and_Bosses.md#context-spawnthingondamage), [`TransformInXTurns`](./Characters_and_Bosses.md#context-transforminxturns), [`TransformOnElementInfluence`](./Characters_and_Bosses.md#context-transformonelementinfluence), [`TransformOnElementInfluencex`](./Characters_and_Bosses.md#context-transformonelementinfluencex), [`TransformOnStatusThreshold`](./Characters_and_Bosses.md#context-transformonstatusthreshold), [`SpawnOnBattleStart`](./Elite_Buffs.md#context-spawnonbattlestart), [`gain_clone_familiar`](./Events_and_Encounters.md#context-gain_clone_familiar), [`gain_familiar`](./Events_and_Encounters.md#context-gain_familiar), [`spawn_unit_next_fight`](./Events_and_Encounters.md#context-spawn_unit_next_fight), [`AllyInfested`](./House_and_Environment.md#context-allyinfested), [`GlobalSpawnOnRoundEnd`](./House_and_Environment.md#context-globalspawnonroundend), [`SpawnExtraThingsOnBattleStart`](./House_and_Environment.md#context-spawnextrathingsonbattlestart), [`SpawnVolcanoOnBattleStart`](./House_and_Environment.md#context-spawnvolcanoonbattlestart), [`ObjectDetector`](./Items_and_Equipment.md#context-objectdetector), [`ObjectOnHitCharacter`](./Items_and_Equipment.md#context-objectonhitcharacter), [`PoopWhenHit`](./Items_and_Equipment.md#context-poopwhenhit), [`SpawnCatCopyOnBattleStart`](./Items_and_Equipment.md#context-spawncatcopyonbattlestart), [`SpawnCatCopyWhenDowned`](./Items_and_Equipment.md#context-spawncatcopywhendowned), [`SpawnEachTurn`](./Items_and_Equipment.md#context-spawneachturn), [`SpawnExtraThingsOnBattleStart`](./Items_and_Equipment.md#context-spawnextrathingsonbattlestart), [`SpawnItemLinkedFamiliar`](./Items_and_Equipment.md#context-spawnitemlinkedfamiliar), [`SpawnObjectOnPopCorpse`](./Items_and_Equipment.md#context-spawnobjectonpopcorpse), [`SpawnOnBattleStart`](./Items_and_Equipment.md#context-spawnonbattlestart), [`SpawnOnBattleStartRandomEmptyTile`](./Items_and_Equipment.md#context-spawnonbattlestartrandomemptytile), [`SpawnThingOnDamage`](./Items_and_Equipment.md#context-spawnthingondamage), [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#context-objectonhitcharacter), [`SpawnCatCopyOnBattleStart`](./Passives_and_Statuses.md#context-spawncatcopyonbattlestart), [`SpawnEachTurn`](./Passives_and_Statuses.md#context-spawneachturn), [`SpawnOnBattleStart`](./Passives_and_Statuses.md#context-spawnonbattlestart), [`SpawnOnBattleStartRandomEmptyTile`](./Passives_and_Statuses.md#context-spawnonbattlestartrandomemptytile), [`SpawnThingOnDamage`](./Passives_and_Statuses.md#context-spawnthingondamage), [`ROOT`](./Spawns_and_Enemy_Pools.md#context-root), [`weather_element_alt`](./Spawns_and_Enemy_Pools.md#context-weather_element_alt)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CharmedFlea` | |
| `Coin` | |
| `SmallRock` | |
| `Food` | |
| `Maggot` | |
| `RandomPickup` | |
| `Boulder` | |
| `CharmedMaggot` | |
| `Poop` | |
| `Fly` | |
| `GasCloud` | |
| `Amoeba` | |
| `CharmedFly` | |
| `CharmedTinySpider` | |
| `Flea` | |
| `CharmedLeech` | |
| `ChumBag` | |
| `Clot` | |
| `HarpoonTrap` | |
| `Junk` | |
| `MegaFetus` | |
| `PlayerCat_Shade` | |
| `PlayerCat_ThiefShade` | |
| `Rat` | |
| `Squirrel` | |
| `ButtZombie` | |
| `CharmedPinky` | |
| `CharmedTinyTumor` | |
| `Fetus` | |
| `GreenProber` | |
| `Invader` | |
| `PlayerCat_MiniMe` | |
| `PoisonFood` | |
| `RANDOM_1X1_ENEMY` | |
| `Scrap` | |
| `Spookie` | |
| `Sprout` | |
| `Tire_Up` | |
| `TomTom` | |
| `Wisp` | |
| `chapter_corpse_medium` | |
| `AnimatedSmallRock` | |
| `Bait` | |
| `Bird` | |
| `BirdSmall` | |
| `Blessing` | |
| `Bomb` | |
| `BoyShade` | |
| `BrambleBaby` | |
| `Catnip` | |
| `CaveBaby` | |
| `CaveMan` | |
| `CaveManNoSpear` | |
| `CharmedLice` | |
| `CharmedRat` | |
| `CookedBait` | |
| `CookedBiggestFood` | |
| `CookedFood` | |
| `CookedPurifiedPoisonFood` | |
| `Crow` | |
| `DaddyShark` | |
| `Dip` | |
| `ElectricNail` | |
| `ExplodingDecoy` | |
| `FlySwarm` | |
| `GeoLad` | |
| `Grenade` | |
| `GunCat` | |
| `HeadTumor` | |
| `HuskG` | |
| `IceElemental` | |
| `Kitten` | |
| `Mammoth` | |
| `MeatMinion` | |
| `MiniNuke` | |
| `MiniVolcano` | |
| `MoonHand` | |
| `MotherTumor` | |
| `NeutralTwister` | |
| `PlayerCat_MiniMiniMe` | |
| `RandomCatnipPickup` | |
| `RandomDruidFamiliar` | |
| `RandomFoodPickup` | |
| `RandomNonCoinPickup` | |
| `RaptorBaby` | |
| `SpiderCat` | |
| `TankCat_Terminator` | |
| `TinySpider` | |
| `TrashBag` | |
| `TumorBarrier` | |
| `ZombieCat` | |
| `ZombieCatFamiliar` | |
| `twin` | |
| `AlbinoTomTom` | |
| `AlbinoTomTom_Elite` | |
| `AlienBeast` | |
| `AlienEgg` | |
| `AllyRotFly` | |
| `AllyRotFly_Champion` | |
| `Amoeba_Elite` | |
| `AngelicCat` | |
| `AngelicKitten` | |
| `Ankylosaurus` | |
| `Ankylosaurus_Elite` | |
| `Antidote` | |
| `Astro` | |
| `AstroZombie` | |
| `AstroZombieHead` | |
| `Astro_Elite` | |
| `AtomicKitten` | |
| `AtomicKitten_Elite` | |
| `BabyDeathWorm` | |
| `BabyDeathWorm_Elite` | |
| `BabyShark` | |
| `BabyShark_Elite` | |
| `BabySquirrel` | |
| `Bat` | |
| `Bat_Elite` | |
| `BeaniesRat` | |
| `Bear` | |
| `Bear2` | |
| `BeefyCharmedLeech` | |
| `Belcher` | |
| `Belcher_Elite` | |
| `BigAsteroid` | |
| `BigAsteroid_Elite` | |
| `BigDemon` | |
| `BigDemon_Elite` | |
| `BigFood` | |
| `BigSlime` | |
| `BigSlimeX` | |
| `BigUFO` | |
| `BigUFO_Elite` | |
| `Birthwort` | |
| `Birthwort_Elite` | |
| `BishopHat` | |
| `BishopHat_Elite` | |
| `BlackHole` | |
| `BombFly` | |
| `Bombchu` | |
| `BomberRat` | |
| `BoomerCat` | |
| `BoomerCat_Elite` | |
| `BoyDino` | |
| `BoyShadeClone` | |
| `BoyShade_Elite` | |
| `BrainDrain` | |
| `BrainDrain_Elite` | |
| `BrambleBaby_Elite` | |
| `Bumblefoot` | |
| `BungaWarrior1` | |
| `BungaWarrior2` | |
| `ButchTinkBoris` | |
| `ButcherCat` | |
| `ButcherCat_Terminator` | |
| `ButtZombie_Elite` | |
| `Cactus` | |
| `CanCreeper` | |
| `CancerCat` | |
| `CancerCat_Elite` | |
| `CandleBig` | |
| `CandleSmall` | |
| `Carcus` | |
| `Carcus_Elite` | |
| `Carnibulb` | |
| `Carnibulb_Elite` | |
| `CatCaller` | |
| `CatCaller_Elite` | |
| `CatCopyClot` | |
| `CatCultist` | |
| `CatCultist_Elite` | |
| `CatHuman` | |
| `CatHuman_Elite` | |
| `Catbot` | |
| `Catepillar` | |
| `CaveBaby_Elite` | |
| `CaveCatBaby` | |
| `CaveCatDad` | |
| `CaveCatMom` | |
| `CaveChief` | |
| `CaveChief_Elite` | |
| `CaveManNoSpear_Elite` | |
| `CaveMan_Elite` | |
| `CaveWoman` | |
| `CaveWoman_Elite` | |
| `Cerberubs` | |
| `Chaos` | |
| `ChaosStacy` | |
| `ChargeyMaggot` | |
| `CharmedAmoeba` | |
| `CharmedBigDemon` | |
| `CharmedCaveBaby` | |
| `CharmedClot` | |
| `CharmedCultist` | |
| `CharmedDip` | |
| `CharmedMaggot_Champion` | |
| `CharmedMammothBaby` | |
| `CharmedMegaDino` | |
| `CharmedPooter` | |
| `CharmedRattleSnake` | |
| `CharmedSpookie` | |
| `CharmedStacy` | |
| `CharmedTinaFly` | |
| `CharmedTomTom` | |
| `Cherub_FinalBoss` | |
| `Cherubim` | |
| `Chubs` | |
| `ChumBag_Elite` | |
| `Chummy` | |
| `Chummy_Elite` | |
| `Chupacabra` | |
| `CloakedDemon` | |
| `CloakedDemon_Elite` | |
| `CloningVat` | |
| `CollectiveCat` | |
| `CollectiveCat_Elite` | |
| `ColorlessCat_Tutorial` | |
| `ConjoinedHusk` | |
| `ConjoinedHusk_Elite` | |
| `CookedBigFood` | |
| `CookedPoisonBait` | |
| `CookedPoisonFood` | |
| `CopBot` | |
| `CopBot_Elite` | |
| `CoreFreak` | |
| `CoreFreak_Elite` | |
| `CovenCandle` | |
| `Crate` | |
| `Crate_WithItemChance` | |
| `CraterCreeper` | |
| `CraterCreeper_Elite` | |
| `Cultist` | |
| `CultistBishop` | |
| `CultistBishop_Elite` | |
| `CultistMutant` | |
| `CultistMutant_Elite` | |
| `CultistWasher` | |
| `CultistZealot` | |
| `CultistZealot_Elite` | |
| `Cultist_Elite` | |
| `DaddyShark_Elite` | |
| `DeadPinky` | |
| `Death` | |
| `DeathWorm` | |
| `DeathWorm_Elite` | |
| `Deathbot` | |
| `Debug_MegaGuppyPhase3` | |
| `DemonHooker` | |
| `DemonHooker_Elite` | |
| `Dice` | |
| `DinoEggs` | |
| `DinoEggs_Elite` | |
| `Dip_Elite` | |
| `DoctorBot` | |
| `DoctorBot_Elite` | |
| `DrDitto` | |
| `DrDitto_Elite` | |
| `DrMangler` | |
| `Drcat` | |
| `Drcat_Elite` | |
| `DruidCat` | |
| `DruidCat_Terminator` | |
| `DruidCrow` | |
| `DruidCrow_Terminator` | |
| `DustCloud` | |
| `DustDevil` | |
| `Dybbuk` | |
| `EventBountyHunter` | |
| `FamiliarFleshLad` | |
| `FastFetus` | |
| `FastRat` | |
| `FatCat` | |
| `FatCat_Elite` | |
| `FatMan` | |
| `FatMan_Elite` | |
| `FatWoman` | |
| `FatWoman_Elite` | |
| `Fatso` | |
| `FetusGusher` | |
| `FetusGusher_Elite` | |
| `FetusJar` | |
| `FetusJar_Elite` | |
| `FetusNoJar` | |
| `FetusNoJar_Elite` | |
| `Fetus_Elite` | |
| `FighterCat` | |
| `FighterCat_Terminator` | |
| `FlamingPoop` | |
| `Flea_Elite` | |
| `FleshLad` | |
| `FleshyMind` | |
| `Floast` | |
| `Floast_Elite` | |
| `Floater` | |
| `Floater_Elite` | |
| `FloatingHive` | |
| `Flushmaster` | |
| `FlySwarm_Elite` | |
| `Fly_Elite` | |
| `FrankFetus` | |
| `FrankPinky` | |
| `FutureBot` | |
| `FutureBot_Elite` | |
| `Fuzzer` | |
| `Fuzzer_Elite` | |
| `Gambit` | |
| `Gamete` | |
| `Gamete_Elite` | |
| `GasCan` | |
| `Gasper` | |
| `Gasper_Elite` | |
| `Gasser` | |
| `GassyCat` | |
| `GassyCat_Elite` | |
| `Gatekeeper` | |
| `GeoLad_Elite` | |
| `GirlDino` | |
| `GirlShade` | |
| `GirlShade_Elite` | |
| `GlassSpitter` | |
| `GlassSpitter_Elite` | |
| `GlowingBear` | |
| `GlowingMushroom` | |
| `GlowingMushroom2` | |
| `GolemCat` | |
| `Gorger` | |
| `Gorger_Elite` | |
| `GraveWorm` | |
| `GraveWorm_Elite` | |
| `GreenProber_Elite` | |
| `GreyAlien` | |
| `GreyAlien_Elite` | |
| `GroundedSpear` | |
| `Guillotina1` | |
| `Guillotina2Body` | |
| `Guillotina2Head` | |
| `Guillotina3Body` | |
| `Guillotina3Head` | |
| `GunCat_Elite` | |
| `HangerBot` | |
| `HangerBot_Elite` | |
| `HeadTumor_Elite` | |
| `HellHand` | |
| `Hellspawn` | |
| `Hemlock` | |
| `Hemlock_Elite` | |
| `HitlerClone` | |
| `HitlerHead` | |
| `Hive` | |
| `HornyCat` | |
| `HornyCat_Elite` | |
| `Host` | |
| `Host_Elite` | |
| `HumanCat` | |
| `HumanCat_Elite` | |
| `HunterCat` | |
| `HunterCat_Terminator` | |
| `Husk` | |
| `Husk_Elite` | |
| `Hydrant` | |
| `IceBlock` | |
| `Infested` | |
| `InfestedDuo` | |
| `Infested_Elite` | |
| `Invader_Elite` | |
| `JackCat` | |
| `JarHead` | |
| `JarHead_Elite` | |
| `Jekyll` | |
| `Jekyll_Elite` | |
| `JesterCat` | |
| `JesterCat_Terminator` | |
| `Johnny` | |
| `KillDozer` | |
| `KillDozer_Elite` | |
| `KirbyFetus` | |
| `KirbyFetus_Elite` | |
| `Kitten_Elite` | |
| `LabSupportPillar` | |
| `Leaper` | |
| `Leaper_Elite` | |
| `Lenny` | |
| `LightningElemental` | |
| `LordBunga` | |
| `LoveBot` | |
| `LoveBot_Elite` | |
| `Lumpy` | |
| `Lumpy_Elite` | |
| `MadLad` | |
| `MaddenedBear` | |
| `Maelestes` | |
| `Maelestes_Elite` | |
| `MageCat` | |
| `MageCat_Terminator` | |
| `MaggotLord` | |
| `Maggot_Elite` | |
| `MamaMaggotTina` | |
| `MammothBaby` | |
| `MammothBaby_Elite` | |
| `Mammoth_Elite` | |
| `ManglersMonster` | |
| `Mangy` | |
| `Mangy2` | |
| `Mangy2_Elite` | |
| `Mangy3` | |
| `Mangy3_Elite` | |
| `Mangy_Elite` | |
| `MeatSlime` | |
| `MechSuit` | |
| `MedSlime` | |
| `MedicCat` | |
| `MedicCat_Terminator` | |
| `MegaDinoHead` | |
| `MegaDinoLeg` | |
| `MegaFetus_Elite` | |
| `MegaMutant` | |
| `MegaMutant_Elite` | |
| `MegaTumor` | |
| `MegaTumor_Elite` | |
| `MonkCat` | |
| `MonkCat_Terminator` | |
| `MoonHead` | |
| `MoonWorm` | |
| `MoonWorm_Elite` | |
| `Moth` | |
| `MotherSpike` | |
| `MotherTumorBig` | |
| `Multicat` | |
| `NecroCat` | |
| `NecroCat_Terminator` | |
| `Needlecat` | |
| `Needlecat_Elite` | |
| `Nettle` | |
| `Nettle_Elite` | |
| `NeutralToad` | |
| `NeutralZombieKitten` | |
| `NeutronStar` | |
| `NoHead` | |
| `Nubs` | |
| `NubsCat` | |
| `NubsCat_Elite` | |
| `NurseBot` | |
| `OrganZodiac` | |
| `Parasaurolophus` | |
| `Parasaurolophus_Elite` | |
| `Parasiter` | |
| `Peashy` | |
| `Peashy_Elite` | |
| `Pebbles_Terminator` | |
| `Phylactery` | |
| `Pile` | |
| `Pile_Elite` | |
| `Pinky` | |
| `Pinky_Elite` | |
| `PlayerCat_AncestralShade` | |
| `PlayerCat_CambionMiniMe` | |
| `PlayerCat_ClotClone` | |
| `PlayerCat_FinalBossClone` | |
| `PlayerCat_FleshGolem` | |
| `PlayerCat_HuskShade` | |
| `PlayerCat_MachineClone` | |
| `PlayerCat_MonkMiniMe` | |
| `PlayerCat_MonkShade` | |
| `PlayerCat_NecroShade` | |
| `PlayerCat_StevenShade` | |
| `PoisonBait` | |
| `PoisonFrog` | |
| `PokerDemon` | |
| `PokerDemon_Elite` | |
| `PoopCat` | |
| `Pooter` | |
| `Pooter_Elite` | |
| `PopeyeCat` | |
| `PopeyeCat_Elite` | |
| `PrehistoricPooter` | |
| `PrehistoricPooter_Elite` | |
| `PsychicCat` | |
| `PsychicCat_Terminator` | |
| `Pterodactyl` | |
| `Pterodactyl_Elite` | |
| `PunchingBag` | |
| `PurifiedPoisonFood` | |
| `Pyrophina` | |
| `PyrophinaFamiliar` | |
| `PyrophinaVS` | |
| `QueenHippo` | |
| `RANDOM_SPECIFIC_CHAPTER_ENEMY_MEDIUM` | |
| `RandomArmorPickup` | |
| `Raptor` | |
| `RaptorBaby_Elite` | |
| `Raptor_Elite` | |
| `RatCat` | |
| `RatCat_Elite` | |
| `RatKing` | |
| `RatPile` | |
| `Rat_Elite` | |
| `RattleSnake` | |
| `RattleSnake_Elite` | |
| `Reaper` | |
| `Reaper_Elite` | |
| `RoboTom` | |
| `RoboTom_Elite` | |
| `RoboVacuum` | |
| `RoboVacuum2` | |
| `Rock` | |
| `RockHead` | |
| `RockHead_Elite` | |
| `RocketTurret` | |
| `RockyBobo` | |
| `Rover` | |
| `Rover_Elite` | |
| `RubberFistBot` | |
| `SabertoothCat` | |
| `SabertoothCat_Elite` | |
| `SabertoothCub` | |
| `SabertoothCub_Elite` | |
| `Scary` | |
| `Scary_Elite` | |
| `ScorpionCat` | |
| `ScorpionCat_Elite` | |
| `SecurityBot` | |
| `SecurityBot_Elite` | |
| `Seraphim` | |
| `ShadeCat` | |
| `ShadeCat_Elite` | |
| `ShadowCat` | |
| `Shambler` | |
| `Shambler_Elite` | |
| `SharkyCat` | |
| `SharkyCat_Elite` | |
| `Simon` | |
| `Siren` | |
| `Siren_Elite` | |
| `SkeletonCat` | |
| `SkeletonCatRevived` | |
| `SkeletonCatRevivedFamiliar` | |
| `SkeletonCat_Elite` | |
| `SkeletonShambler` | |
| `SkeletonShamblerRevived` | |
| `SkeletonShambler_Elite` | |
| `Skinned` | |
| `SkullOoze` | |
| `SkullOoze_Elite` | |
| `Slag` | |
| `Slag_Elite` | |
| `SlotMachine` | |
| `SlotMachineJackpotCoinsReward` | |
| `SlotMachineNormalPickupReward` | |
| `SmallAsteroid` | |
| `SmallAsteroid_Elite` | |
| `SmallSlime` | |
| `SmallUFO` | |
| `SmallUFO_Elite` | |
| `Snake` | |
| `Snake2` | |
| `SnakeyBones` | |
| `SnakeyBones_Elite` | |
| `SoldierBot` | |
| `SoldierBot_Elite` | |
| `Spewer` | |
| `SpewerPillTubeL` | |
| `SpewerPillTubeR` | |
| `SpewerPill_Fire` | |
| `SpewerPill_Normal` | |
| `SpewerPill_Tar` | |
| `SpiderCat_Elite` | |
| `SpiderQueen` | |
| `SpikedCat` | |
| `SpikedCat_Elite` | |
| `SpikyCactus` | |
| `SpikyCactus_2x2` | |
| `SpikyCactus_Tall` | |
| `SpikyRock` | |
| `Spookie_Elite` | |
| `Stacy2p0` | |
| `Stacy2p0_Elite` | |
| `StacyMutant` | |
| `Static1x1A` | |
| `Static1x1B` | |
| `Static1x1C` | |
| `Static2x2A` | |
| `Static2x2B` | |
| `StaticTallA` | |
| `StaticTallB` | |
| `SteelFly` | |
| `Stegosaurus` | |
| `Stegosaurus_Elite` | |
| `StemCat` | |
| `SwappyMaggot` | |
| `T3Hitler` | |
| `TCMechSuit` | |
| `TNTCrate` | |
| `TVBot` | |
| `TVBot_Elite` | |
| `TallBot` | |
| `TallBot_Elite` | |
| `TallRobes` | |
| `TallRobes_Elite` | |
| `TallSkeletonCat` | |
| `TallSkeletonCatRevived` | |
| `TallSkeletonCat_Elite` | |
| `TallSpiderCat` | |
| `TallSpiderCat_Elite` | |
| `TallTumor` | |
| `TallTumor_Elite` | |
| `TankCat` | |
| `TarBaby` | |
| `Tatters` | |
| `Tatters_Elite` | |
| `TenTickles` | |
| `TenTickles_Elite` | |
| `Terminator1` | |
| `Terminator2` | |
| `TeslaCoil` | |
| `TheBloat` | |
| `TheChild` | |
| `TheCoven` | |
| `TheCreator` | |
| `TheLost` | |
| `TheMother` | |
| `ThiefCat` | |
| `ThiefCat_Terminator` | |
| `ThrobbingKing` | |
| `ThrobbingTurret` | |
| `Thump` | |
| `Thump_Elite` | |
| `TinkererCat` | |
| `TinkererCat_Terminator` | |
| `TinkererTurret` | |
| `TinySpider_Elite` | |
| `Tire` | |
| `Toad` | |
| `Toad2` | |
| `Toadie` | |
| `Toadie_Elite` | |
| `Toadie_Hidden` | |
| `Toadie_Hidden_Elite` | |
| `TomTom_Elite` | |
| `Tombstone_Ghost` | |
| `Tombstone_ManaIdol` | |
| `Tombstone_Zombie` | |
| `TracyFetus` | |
| `Trampy` | |
| `Tremblo` | |
| `Tremblo_Elite` | |
| `Trex` | |
| `Trex_Elite` | |
| `Triachnid` | |
| `Triceratops` | |
| `Triceratops_Elite` | |
| `TumorBarrier_Elite` | |
| `TumorCat` | |
| `TumorCat_Elite` | |
| `TumorousMaggot` | |
| `Turtle` | |
| `Twister` | |
| `Waggle` | |
| `Waggle_Elite` | |
| `WallOfCats_Eye` | |
| `WallOfCats_Mouth` | |
| `WallOfCats_Wall` | |
| `WaterKitten` | |
| `WaterKitten_Elite` | |
| `WaterLeech` | |
| `WaterLeech_Elite` | |
| `WereMan` | |
| `WereMan_Elite` | |
| `Whisperer` | |
| `Whisperer_Elite` | |
| `WhiteRabbit` | |
| `Wisp_Elite` | |
| `WolfCat` | |
| `WolfCat_Elite` | |
| `Worm` | |
| `YellowBlaster` | |
| `YellowBlaster_Elite` | |
| `Yeti` | |
| `Yeti_Elite` | |
| `Yeticat` | |
| `Yeticat_Elite` | |
| `Zaratana` | |
| `ZaratanaFamiliar` | |
| `ZaratanaVS` | |
| `Zodiac` | |
| `ZombieCat_Elite` | |

</details>


---

### Enum: `set`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Furniture_and_Metaprogression.md#context-root), [`ROOT`](./Items_and_Equipment.md#context-root), [`StatusOnSetPieceBreak`](./Items_and_Equipment.md#context-statusonsetpiecebreak)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Steven` | |
| `Rock` | |
| `Bone` | |
| `Cleric` | |
| `Wood` | |
| `Parasite` | |
| `Radioactive` | |
| `Used` | |
| `Guts` | |
| `Experimental` | |
| `Paper` | |
| `Demonic` | |
| `Druid` | |
| `Feathered` | |
| `Fighter` | |
| `Mother` | |
| `80s` | |
| `90s` | |
| `Cool` | |
| `HumanFlesh` | |
| `Lead` | |
| `Space` | |
| `angelic` | |
| `atomic` | |
| `block` | |
| `bone` | |
| `cat` | |
| `crystal` | |
| `cute` | |
| `elegant` | |
| `guts` | |
| `junk` | |
| `modern` | |
| `monster` | |
| `mushroom` | |
| `retro` | |
| `robo` | |
| `rustic` | |
| `sewer` | |
| `sewn` | |
| `spider` | |
| `wooden` | |
| `Fecal` | |
| `Jester` | |
| `Scrap` | |
| `Flower` | |
| `Hybrid` | |
| `Leather` | |
| `Meat` | |
| `Necromancer` | |
| `Nurse` | |
| `Rag` | |
| `Rubber` | |
| `Tank` | |
| `Thief` | |
| `Twine` | |
| `Bionic` | |
| `Butcher` | |
| `DirtClod` | |
| `Fatty` | |
| `Frozen` | |
| `Gemstone` | |
| `Gimp` | |
| `Molten` | |
| `Obelisk` | |
| `Planet` | |
| `Rat` | |
| `Tinkerer` | |
| `Amoeba` | |
| `Baby` | |
| `Barbed` | |
| `Cardboard` | |
| `Fly` | |
| `Hunter` | |
| `Mage` | |
| `Medical` | |
| `Miner` | |
| `Ninja` | |
| `Recycled` | |
| `Superhero` | |
| `Brick` | |
| `CatHide` | |
| `Chip` | |
| `Cyborg` | |
| `Leafy` | |
| `Lucky` | |
| `Man` | |
| `Psychic` | |
| `Slimy` | |
| `Stunning` | |
| `Survivalist` | |
| `Wooly` | |
| `AdvancedAlloy` | |
| `Alloy` | |
| `Cactus` | |
| `Carapace` | |
| `Caveman` | |
| `Copycat` | |
| `Debris` | |
| `EliteAlloy` | |
| `Godhead` | |
| `Grub` | |
| `JankAlloy` | |
| `Leech` | |
| `Monk` | |
| `Mummy` | |
| `Prowler` | |
| `Rotten` | |
| `Sludge` | |
| `Tentacle` | |
| `Thrumming` | |
| `Transmitter` | |
| `Veiny` | |
| `Witch` | |
| `Collarless` | |
| `Hippie` | |
| `Rune` | |

</details>


---

### Enum: `tag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#context-conditional_sourceabilityhastag), [`ForceMoveTowardsTaggedObject`](./Abilities_and_Spells.md#context-forcemovetowardstaggedobject), [`-2`](./Cat_Mutations.md#context--2), [`1026`](./Cat_Mutations.md#context-1026), [`1500`](./Cat_Mutations.md#context-1500), [`300`](./Cat_Mutations.md#context-300), [`301`](./Cat_Mutations.md#context-301), [`302`](./Cat_Mutations.md#context-302), [`303`](./Cat_Mutations.md#context-303), [`304`](./Cat_Mutations.md#context-304), [`306`](./Cat_Mutations.md#context-306), [`307`](./Cat_Mutations.md#context-307), [`308`](./Cat_Mutations.md#context-308), [`309`](./Cat_Mutations.md#context-309), [`310`](./Cat_Mutations.md#context-310), [`311`](./Cat_Mutations.md#context-311), [`313`](./Cat_Mutations.md#context-313), [`314`](./Cat_Mutations.md#context-314), [`315`](./Cat_Mutations.md#context-315), [`316`](./Cat_Mutations.md#context-316), [`318`](./Cat_Mutations.md#context-318), [`319`](./Cat_Mutations.md#context-319), [`321`](./Cat_Mutations.md#context-321), [`322`](./Cat_Mutations.md#context-322), [`325`](./Cat_Mutations.md#context-325), [`327`](./Cat_Mutations.md#context-327), [`328`](./Cat_Mutations.md#context-328), [`329`](./Cat_Mutations.md#context-329), [`336`](./Cat_Mutations.md#context-336), [`337`](./Cat_Mutations.md#context-337), [`339`](./Cat_Mutations.md#context-339), [`343`](./Cat_Mutations.md#context-343), [`345`](./Cat_Mutations.md#context-345), [`353`](./Cat_Mutations.md#context-353), [`400`](./Cat_Mutations.md#context-400), [`401`](./Cat_Mutations.md#context-401), [`402`](./Cat_Mutations.md#context-402), [`403`](./Cat_Mutations.md#context-403), [`404`](./Cat_Mutations.md#context-404), [`405`](./Cat_Mutations.md#context-405), [`406`](./Cat_Mutations.md#context-406), [`407`](./Cat_Mutations.md#context-407), [`408`](./Cat_Mutations.md#context-408), [`409`](./Cat_Mutations.md#context-409), [`410`](./Cat_Mutations.md#context-410), [`411`](./Cat_Mutations.md#context-411), [`412`](./Cat_Mutations.md#context-412), [`413`](./Cat_Mutations.md#context-413), [`414`](./Cat_Mutations.md#context-414), [`415`](./Cat_Mutations.md#context-415), [`416`](./Cat_Mutations.md#context-416), [`417`](./Cat_Mutations.md#context-417), [`418`](./Cat_Mutations.md#context-418), [`419`](./Cat_Mutations.md#context-419), [`420`](./Cat_Mutations.md#context-420), [`421`](./Cat_Mutations.md#context-421), [`422`](./Cat_Mutations.md#context-422), [`423`](./Cat_Mutations.md#context-423), [`424`](./Cat_Mutations.md#context-424), [`425`](./Cat_Mutations.md#context-425), [`426`](./Cat_Mutations.md#context-426), [`427`](./Cat_Mutations.md#context-427), [`428`](./Cat_Mutations.md#context-428), [`429`](./Cat_Mutations.md#context-429), [`430`](./Cat_Mutations.md#context-430), [`431`](./Cat_Mutations.md#context-431), [`432`](./Cat_Mutations.md#context-432), [`433`](./Cat_Mutations.md#context-433), [`434`](./Cat_Mutations.md#context-434), [`435`](./Cat_Mutations.md#context-435), [`436`](./Cat_Mutations.md#context-436), [`437`](./Cat_Mutations.md#context-437), [`438`](./Cat_Mutations.md#context-438), [`439`](./Cat_Mutations.md#context-439), [`440`](./Cat_Mutations.md#context-440), [`441`](./Cat_Mutations.md#context-441), [`442`](./Cat_Mutations.md#context-442), [`700`](./Cat_Mutations.md#context-700), [`701`](./Cat_Mutations.md#context-701), [`702`](./Cat_Mutations.md#context-702), [`703`](./Cat_Mutations.md#context-703), [`704`](./Cat_Mutations.md#context-704), [`705`](./Cat_Mutations.md#context-705), [`706`](./Cat_Mutations.md#context-706), [`707`](./Cat_Mutations.md#context-707), [`750`](./Cat_Mutations.md#context-750), [`752`](./Cat_Mutations.md#context-752), [`753`](./Cat_Mutations.md#context-753), [`AbilityWhenTaggedCharacterMovesNear`](./Cat_Mutations.md#context-abilitywhentaggedcharactermovesnear), [`AbilityWhenTaggedCharacterMovesNear`](./Characters_and_Bosses.md#context-abilitywhentaggedcharactermovesnear), [`CaveFamilyEnrage`](./Characters_and_Bosses.md#context-cavefamilyenrage), [`ChaosHeadDropIn`](./Characters_and_Bosses.md#context-chaosheaddropin), [`HitlerExecute`](./Characters_and_Bosses.md#context-hitlerexecute), [`properties`](./Characters_and_Bosses.md#context-properties), [`CharacterTypeGainsStatusAtBattleStart`](./Events_and_Encounters.md#context-charactertypegainsstatusatbattlestart), [`random_mutation`](./Events_and_Encounters.md#context-random_mutation), [`CharacterTypeGainsStatusAtBattleStart`](./House_and_Environment.md#context-charactertypegainsstatusatbattlestart), [`Conditional_HasTag`](./House_and_Environment.md#context-conditional_hastag), [`FactionUprising`](./House_and_Environment.md#context-factionuprising), [`Conditional_HasTag`](./Items_and_Equipment.md#context-conditional_hastag), [`SpawnRandomPickupsOnTaggedUnitKilled`](./Items_and_Equipment.md#context-spawnrandompickupsontaggedunitkilled), [`AbilityWhenTaggedCharacterMovesNear`](./Passives_and_Statuses.md#context-abilitywhentaggedcharactermovesnear), [`Conditional_HasTag`](./Passives_and_Statuses.md#context-conditional_hastag), [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#context-conditional_sourcehastag), [`ManaCostReductionTagged`](./Passives_and_Statuses.md#context-manacostreductiontagged), [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#context-statusonuseabilitywithtag), [`TaggedPickupEffectReplacement`](./Passives_and_Statuses.md#context-taggedpickupeffectreplacement)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `common` | |
| `cat` | |
| `animal` | |
| `birth_defect` | |
| `blob` | |
| `rock` | |
| `humanoid` | |
| `robot` | |
| `worm` | |
| `bug` | |
| `fetus` | |
| `rat` | |
| `food` | |
| `plant` | |
| `poop` | |
| `cavefamily` | |
| `dinosaur` | |
| `extra` | |
| `musical` | |
| `tumor` | |
| `demon` | |
| `bird` | |
| `kaiju` | |
| `melted` | |
| `moonhand` | |
| `shapeshift` | |
| `bomb` | |
| `ghost` | |
| `megadino` | |
| `skeleton` | |
| `summon` | |
| `alien` | |
| `any` | |
| `container` | |
| `dog` | |
| `grown_hitler_clone` | |
| `moonhead` | |
| `pickup` | |
| `spear` | |
| `the_coven` | |
| `zombie` | |
| `angeljunk` | |
| `bishop_hat` | |
| `bonusbird` | |
| `candle` | |
| `cosmic` | |
| `crow` | |
| `god` | |
| `hitler_clone` | |
| `hitler_clone_fetus` | |
| `money` | |
| `pill` | |
| `riftheadguardian` | |
| `scrap` | |
| `the_nuke_bearer` | |
| `themotherspike` | |
| `trash` | |
| `weapon_throw` | |

</details>


---

### Enum: `type`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](./Abilities_and_Spells.md#context-dodamage), [`damage`](./Abilities_and_Spells.md#context-damage), [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance), [`self_damage`](./Abilities_and_Spells.md#context-self_damage), [`splash_damage`](./Abilities_and_Spells.md#context-splash_damage), [`MeleeRevengeDamage`](./Cat_Mutations.md#context-meleerevengedamage), [`RevengeDamage`](./Cat_Mutations.md#context-revengedamage), [`MeleeRevengeDamage`](./Characters_and_Bosses.md#context-meleerevengedamage), [`RevengeDamage`](./Characters_and_Bosses.md#context-revengedamage), [`eat_damage`](./Characters_and_Bosses.md#context-eat_damage), [`properties`](./Characters_and_Bosses.md#context-properties), [`DamageNeighborsAfterMove`](./Elite_Buffs.md#context-damageneighborsaftermove), [`AddAdvantageToEvent`](./Items_and_Equipment.md#context-addadvantagetoevent), [`DoDamage`](./Items_and_Equipment.md#context-dodamage), [`StatusOnTurnEndIfDidntCastAbilityTypes`](./Items_and_Equipment.md#context-statusonturnendifdidntcastabilitytypes), [`damage_instance`](./Items_and_Equipment.md#context-damage_instance), [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`battle`](./Map_Generation_and_Routing.md#context-battle), [`boss`](./Map_Generation_and_Routing.md#context-boss), [`event`](./Map_Generation_and_Routing.md#context-event), [`exit0`](./Map_Generation_and_Routing.md#context-exit0), [`exit1`](./Map_Generation_and_Routing.md#context-exit1), [`exit_desert`](./Map_Generation_and_Routing.md#context-exit_desert), [`exit_lab`](./Map_Generation_and_Routing.md#context-exit_lab), [`hard_initial`](./Map_Generation_and_Routing.md#context-hard_initial), [`home`](./Map_Generation_and_Routing.md#context-home), [`miniboss_event`](./Map_Generation_and_Routing.md#context-miniboss_event), [`mw_altar`](./Map_Generation_and_Routing.md#context-mw_altar), [`mw_battle1`](./Map_Generation_and_Routing.md#context-mw_battle1), [`mw_boss`](./Map_Generation_and_Routing.md#context-mw_boss), [`mw_earlyhome`](./Map_Generation_and_Routing.md#context-mw_earlyhome), [`mw_event1`](./Map_Generation_and_Routing.md#context-mw_event1), [`mw_hard1`](./Map_Generation_and_Routing.md#context-mw_hard1), [`mw_home`](./Map_Generation_and_Routing.md#context-mw_home), [`mw_quest_event`](./Map_Generation_and_Routing.md#context-mw_quest_event), [`mw_treasure`](./Map_Generation_and_Routing.md#context-mw_treasure), [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event), [`shop_cheapwater`](./Map_Generation_and_Routing.md#context-shop_cheapwater), [`shop_water`](./Map_Generation_and_Routing.md#context-shop_water), [`start`](./Map_Generation_and_Routing.md#context-start), [`time_machine`](./Map_Generation_and_Routing.md#context-time_machine), [`treasure`](./Map_Generation_and_Routing.md#context-treasure), [`weather_event`](./Map_Generation_and_Routing.md#context-weather_event), [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#context-damageneighborsaftermove), [`DamageNeighborsOnEndMove`](./Passives_and_Statuses.md#context-damageneighborsonendmove), [`GravityWell`](./Passives_and_Statuses.md#context-gravitywell), [`SelfDamageWhenDealDamage`](./Passives_and_Statuses.md#context-selfdamagewhendealdamage), [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#context-smiteenemieswhokill), [`StatusOnTurnEndIfDidntCastAbilityTypes`](./Passives_and_Statuses.md#context-statusonturnendifdidntcastabilitytypes), [`fire`](./Passives_and_Statuses.md#context-fire), [`ice`](./Passives_and_Statuses.md#context-ice), [`lightning`](./Passives_and_Statuses.md#context-lightning), [`triattack`](./Passives_and_Statuses.md#context-triattack), [`tracy_special_item`](./Progression_Unlocks.md#context-tracy_special_item)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `boss` | |
| `melee` | |
| `spell` | |
| `status_spell` | |
| `cat` | |
| `none` | |
| `object` | |
| `status` | |
| `small` | |
| `exit` | |
| `special_event` | |
| `ranged` | |
| `treasure` | |
| `special_foodbox` | |
| `random_unique_idol` | |
| `empty` | |
| `hard` | |
| `home` | |
| `physical_spell` | |
| `battle` | |
| `blankcollar` | |
| `event` | |
| `shop` | |
| `spell_cost` | |
| `attack` | |
| `bonus_rare_item` | |
| `enter` | |
| `generic_physical` | |
| `knockblock` | |
| `foodbox` | |
| `miniboss` | |
| `move` | |
| `npc` | |
| `optional_event` | |
| `spawn` | |
| `trample` | |
| `treasure_box` | |

</details>


---

### Enum: `desc`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`301`](./Cat_Mutations.md#context-301), [`306`](./Cat_Mutations.md#context-306), [`307`](./Cat_Mutations.md#context-307), [`309`](./Cat_Mutations.md#context-309), [`310`](./Cat_Mutations.md#context-310), [`311`](./Cat_Mutations.md#context-311), [`313`](./Cat_Mutations.md#context-313), [`314`](./Cat_Mutations.md#context-314), [`315`](./Cat_Mutations.md#context-315), [`900`](./Cat_Mutations.md#context-900), [`graphics`](./Characters_and_Bosses.md#context-graphics), [`ROOT`](./Furniture_and_Metaprogression.md#context-root), [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ARMOR_ASTEROIDBELT_DESC` | |
| `ARMOR_CATCOLLAR_DESC` | |
| `ARMOR_CATEARS_DESC` | |
| `ARMOR_CATWHISKERS_DESC` | |
| `ARMOR_DEATHMASK_DESC` | |
| `ARMOR_DEBRISARMOR_DESC` | |
| `ARMOR_DEBRISHAT_DESC` | |
| `ARMOR_DEBRISMASK_DESC` | |
| `ARMOR_DIVINERSCLOTH_DESC` | |
| `ARMOR_DRYBONEHAT_DESC` | |
| `ARMOR_DRYBONEMASK_DESC` | |
| `ARMOR_DRYBONENECKLACE_DESC` | |
| `ARMOR_EXPERIMENTALHAT_DESC` | |
| `ARMOR_EXPERIMENTALMASK_DESC` | |
| `ARMOR_EXPERIMENTALNECK_DESC` | |
| `ARMOR_FACEBRAND_DESC` | |
| `ARMOR_FACEWRAP_DESC` | |
| `ARMOR_FLESHSHROUD_DESC` | |
| `ARMOR_FLOWERHAT_DESC` | |
| `ARMOR_FLOWERMASK_DESC` | |
| `ARMOR_FLOWERNECKLACE_DESC` | |
| `ARMOR_GREENMANMASK_DESC` | |
| `ARMOR_HEADBRAND_DESC` | |
| `ARMOR_HEADWRAP_DESC` | |
| `ARMOR_HOOKEDNECKLACE_DESC` | |
| `ARMOR_HUMANFLESHARMOR_DESC` | |
| `ARMOR_HUMANFLESHHAT_DESC` | |
| `ARMOR_HUMANFLESHMASK_DESC` | |
| `ARMOR_IRONJAW_DESC` | |
| `ARMOR_LEECHNECKLACE_DESC` | |
| `ARMOR_MANGLASSES_DESC` | |
| `ARMOR_MANHAIR_DESC` | |
| `ARMOR_MANTIE_DESC` | |
| `ARMOR_MINIMOON_DESC` | |
| `ARMOR_MUSHROOMHAT_DESC` | |
| `ARMOR_MYSTICEYE_DESC` | |
| `ARMOR_NECKWRAP_DESC` | |
| `ARMOR_OBELISKARMOR_DESC` | |
| `ARMOR_OBELISKHAT_DESC` | |
| `ARMOR_OBELISKMASK_DESC` | |
| `ARMOR_PRAYERBEADS_DESC` | |
| `ARMOR_RINGOFMUSHROOMS_DESC` | |
| `ARMOR_ROCKYHAT_DESC` | |
| `ARMOR_ROCKYMASK_DESC` | |
| `ARMOR_ROCKYNECKLACE_DESC` | |
| `ARMOR_SCRAPPERSBACKPACK_DESC` | |
| `ARMOR_SCRAPPERSHAT_DESC` | |
| `ARMOR_SCRAPPERSMASK_DESC` | |
| `ARMOR_SPACEANTENNA_DESC` | |
| `ARMOR_SPACEBOOSTERS_DESC` | |
| `ARMOR_SPACEHELMET_DESC` | |
| `ARMOR_SPIDERHAT_DESC` | |
| `ARMOR_TENTACLEHAT_DESC` | |
| `ARMOR_TENTACLEMASK_DESC` | |
| `ARMOR_TENTACLENECK_DESC` | |
| `ARMOR_TINFOILHAT_DESC` | |
| `ARMOR_TINYPLANET_DESC` | |
| `ENEMY_FATWOMAN_DESC` | |
| `FURNITURE_DESC_AUTOFEEDER` | |
| `FURNITURE_DESC_CEILING_CAGE` | |
| `FURNITURE_DESC_CEILING_DISCOBALL` | |
| `FURNITURE_DESC_CEILING_FAN` | |
| `FURNITURE_DESC_HANGING_AIRFRESHINER` | |
| `FURNITURE_DESC_HANGING_CATHEAD` | |
| `FURNITURE_DESC_HANGING_FISH` | |
| `FURNITURE_DESC_OBJECT_BARREL` | |
| `FURNITURE_DESC_OBJECT_BATH1` | |
| `FURNITURE_DESC_OBJECT_BATH2` | |
| `FURNITURE_DESC_OBJECT_BBQ` | |
| `FURNITURE_DESC_OBJECT_BED` | |
| `FURNITURE_DESC_OBJECT_BIRDCAGE` | |
| `FURNITURE_DESC_OBJECT_BOOKS1` | |
| `FURNITURE_DESC_OBJECT_BOOKS10` | |
| `FURNITURE_DESC_OBJECT_BOOKS11` | |
| `FURNITURE_DESC_OBJECT_BOOKS12` | |
| `FURNITURE_DESC_OBJECT_BOOKS2` | |
| `FURNITURE_DESC_OBJECT_BOOKS3` | |
| `FURNITURE_DESC_OBJECT_BOOKS4` | |
| `FURNITURE_DESC_OBJECT_BOOKS5` | |
| `FURNITURE_DESC_OBJECT_BOOKS6` | |
| `FURNITURE_DESC_OBJECT_BOOKS7` | |
| `FURNITURE_DESC_OBJECT_BOOKS8` | |
| `FURNITURE_DESC_OBJECT_BOOKS9` | |
| `FURNITURE_DESC_OBJECT_BOX` | |
| `FURNITURE_DESC_OBJECT_BROOM` | |
| `FURNITURE_DESC_OBJECT_BUG_CENIPEDE` | |
| `FURNITURE_DESC_OBJECT_BUG_PILLBUG` | |
| `FURNITURE_DESC_OBJECT_BUG_SPIDER` | |
| `FURNITURE_DESC_OBJECT_CATTREE1` | |
| `FURNITURE_DESC_OBJECT_CATTREE2` | |
| `FURNITURE_DESC_OBJECT_CATTREE3` | |
| `FURNITURE_DESC_OBJECT_CHEST` | |
| `FURNITURE_DESC_OBJECT_CINDERBLOCK1` | |
| `FURNITURE_DESC_OBJECT_CINDERBLOCK2` | |
| `FURNITURE_DESC_OBJECT_CLOCK` | |
| `FURNITURE_DESC_OBJECT_COFFEN` | |
| `FURNITURE_DESC_OBJECT_CRATE` | |
| `FURNITURE_DESC_OBJECT_CRYSTALBALL` | |
| `FURNITURE_DESC_OBJECT_DIAMOND` | |
| `FURNITURE_DESC_OBJECT_DOLLHOUSE` | |
| `FURNITURE_DESC_OBJECT_DRYER` | |
| `FURNITURE_DESC_OBJECT_EASEL` | |
| `FURNITURE_DESC_OBJECT_ELECTRONICS_ARCADE1` | |
| `FURNITURE_DESC_OBJECT_ELECTRONICS_ARCADE2` | |
| `FURNITURE_DESC_OBJECT_ELECTRONICS_CRANEGAME` | |
| `FURNITURE_DESC_OBJECT_ELECTRONICS_DVDPLAYER` | |
| `FURNITURE_DESC_OBJECT_ELECTRONICS_FAN` | |
| `FURNITURE_DESC_OBJECT_ELECTRONICS_LAPTOP` | |
| `FURNITURE_DESC_OBJECT_ELECTRONICS_LAVALAMP` | |
| `FURNITURE_DESC_OBJECT_ELECTRONICS_MICROWAVE` | |
| `FURNITURE_DESC_OBJECT_ELECTRONICS_MICROWAVE2` | |
| `FURNITURE_DESC_OBJECT_ELECTRONICS_MICROWAVE3` | |
| `FURNITURE_DESC_OBJECT_ELECTRONICS_MONITOR` | |
| `FURNITURE_DESC_OBJECT_ELECTRONICS_ORB` | |
| `FURNITURE_DESC_OBJECT_ELECTRONICS_PC` | |
| `FURNITURE_DESC_OBJECT_ELECTRONICS_PRINTER` | |
| `FURNITURE_DESC_OBJECT_ELECTRONICS_SPEAKER` | |
| `FURNITURE_DESC_OBJECT_ELECTRONICS_VHS` | |
| `FURNITURE_DESC_OBJECT_FILINGCABINET` | |
| `FURNITURE_DESC_OBJECT_FIREPLACE` | |
| `FURNITURE_DESC_OBJECT_FISHTANK_BLOWFISH` | |
| `FURNITURE_DESC_OBJECT_FISHTANK_BOOZE` | |
| `FURNITURE_DESC_OBJECT_FISHTANK_CATFISH` | |
| `FURNITURE_DESC_OBJECT_FISHTANK_CHAMELEON` | |
| `FURNITURE_DESC_OBJECT_FISHTANK_MERMAID` | |
| `FURNITURE_DESC_OBJECT_FISHTANK_OCTOCAT` | |
| `FURNITURE_DESC_OBJECT_FISHTANK_SMALL_FISH` | |
| `FURNITURE_DESC_OBJECT_FISHTANK_SMALL_LILFISH` | |
| `FURNITURE_DESC_OBJECT_FISHTANK_SMALL_LILFISHES` | |
| `FURNITURE_DESC_OBJECT_FISHTANK_SMALL_POOP` | |
| `FURNITURE_DESC_OBJECT_FISHTANK_SMALL_SKULL` | |
| `FURNITURE_DESC_OBJECT_FISHTANK_SMALL_TADPOLES` | |
| `FURNITURE_DESC_OBJECT_FISHTANK_TADPOLES` | |
| `FURNITURE_DESC_OBJECT_FISHTANK_WHALE` | |
| `FURNITURE_DESC_OBJECT_FOOD_HAM` | |
| `FURNITURE_DESC_OBJECT_FOOD_TURKEY` | |
| `FURNITURE_DESC_OBJECT_FORTUNETELLER` | |
| `FURNITURE_DESC_OBJECT_GASTANK` | |
| `FURNITURE_DESC_OBJECT_GNOME` | |
| `FURNITURE_DESC_OBJECT_ICECHEST` | |
| `FURNITURE_DESC_OBJECT_IRONINGBOARD` | |
| `FURNITURE_DESC_OBJECT_IV` | |
| `FURNITURE_DESC_OBJECT_JAR_CAT` | |
| `FURNITURE_DESC_OBJECT_JAR_EGGS` | |
| `FURNITURE_DESC_OBJECT_JAR_EMPTY` | |
| `FURNITURE_DESC_OBJECT_JAR_FETUS` | |
| `FURNITURE_DESC_OBJECT_JAR_HEAD1` | |
| `FURNITURE_DESC_OBJECT_JAR_HEAD2` | |
| `FURNITURE_DESC_OBJECT_LOG` | |
| `FURNITURE_DESC_OBJECT_OLDSTOVE` | |
| `FURNITURE_DESC_OBJECT_OUTHOUSE` | |
| `FURNITURE_DESC_OBJECT_PLANT_BULB1` | |
| `FURNITURE_DESC_OBJECT_PLANT_BULB2` | |
| `FURNITURE_DESC_OBJECT_PLANT_BULB3` | |
| `FURNITURE_DESC_OBJECT_PLANT_BUSH` | |
| `FURNITURE_DESC_OBJECT_PLANT_CACTUS` | |
| `FURNITURE_DESC_OBJECT_PLANT_CUTECACTUS` | |
| `FURNITURE_DESC_OBJECT_PLANT_DAISY` | |
| `FURNITURE_DESC_OBJECT_PLANT_FLOWERS` | |
| `FURNITURE_DESC_OBJECT_PLANT_FLYTRAP` | |
| `FURNITURE_DESC_OBJECT_PLANT_MONSTERA` | |
| `FURNITURE_DESC_OBJECT_PLANT_MUSHROOM` | |
| `FURNITURE_DESC_OBJECT_PLANT_MUSHROOMS` | |
| `FURNITURE_DESC_OBJECT_PLANT_ORCHID` | |
| `FURNITURE_DESC_OBJECT_PLANT_PIRANHASPLANT` | |
| `FURNITURE_DESC_OBJECT_PLANT_POTATO` | |
| `FURNITURE_DESC_OBJECT_PLANT_RAFFLESIA` | |
| `FURNITURE_DESC_OBJECT_PLANT_SPIKEY` | |
| `FURNITURE_DESC_OBJECT_PLANT_SUNFLOWER` | |
| `FURNITURE_DESC_OBJECT_PLANT_TENTACLE` | |
| `FURNITURE_DESC_OBJECT_POTOPOTTY` | |
| `FURNITURE_DESC_OBJECT_PUNCHY` | |
| `FURNITURE_DESC_OBJECT_RADIO_30S` | |
| `FURNITURE_DESC_OBJECT_RADIO_40S` | |
| `FURNITURE_DESC_OBJECT_RADIO_50S` | |
| `FURNITURE_DESC_OBJECT_RADIO_60S` | |
| `FURNITURE_DESC_OBJECT_RADIO_70S` | |
| `FURNITURE_DESC_OBJECT_RADIO_80S` | |
| `FURNITURE_DESC_OBJECT_RADIO_90S` | |
| `FURNITURE_DESC_OBJECT_RADIO_ATOMIC` | |
| `FURNITURE_DESC_OBJECT_ROCK` | |
| `FURNITURE_DESC_OBJECT_SAFE` | |
| `FURNITURE_DESC_OBJECT_SHOWER` | |
| `FURNITURE_DESC_OBJECT_SINK` | |
| `FURNITURE_DESC_OBJECT_SMALLROCK` | |
| `FURNITURE_DESC_OBJECT_STATUE_BAST` | |
| `FURNITURE_DESC_OBJECT_STATUE_BUDDAH` | |
| `FURNITURE_DESC_OBJECT_STATUE_DARUMA` | |
| `FURNITURE_DESC_OBJECT_STATUE_DEVIL` | |
| `FURNITURE_DESC_OBJECT_STATUE_EASTERISLANDLARGE` | |
| `FURNITURE_DESC_OBJECT_STATUE_EASTERISLANDMEDIUM` | |
| `FURNITURE_DESC_OBJECT_STATUE_EASTERISLANDSMALL` | |
| `FURNITURE_DESC_OBJECT_STATUE_JESUS` | |
| `FURNITURE_DESC_OBJECT_STATUE_LION` | |
| `FURNITURE_DESC_OBJECT_STATUE_LOTUS` | |
| `FURNITURE_DESC_OBJECT_STATUE_LUCKYCAT` | |
| `FURNITURE_DESC_OBJECT_STATUE_MERMAID` | |
| `FURNITURE_DESC_OBJECT_STATUE_STONEHEAD` | |
| `FURNITURE_DESC_OBJECT_TAXIDERMY_BAT` | |
| `FURNITURE_DESC_OBJECT_TAXIDERMY_BEAR` | |
| `FURNITURE_DESC_OBJECT_TAXIDERMY_BIRD` | |
| `FURNITURE_DESC_OBJECT_TAXIDERMY_CROW` | |
| `FURNITURE_DESC_OBJECT_TAXIDERMY_FISH` | |
| `FURNITURE_DESC_OBJECT_TAXIDERMY_GOPHER` | |
| `FURNITURE_DESC_OBJECT_TAXIDERMY_LIZARD` | |
| `FURNITURE_DESC_OBJECT_TAXIDERMY_MOUSE` | |
| `FURNITURE_DESC_OBJECT_TAXIDERMY_PIG` | |
| `FURNITURE_DESC_OBJECT_TAXIDERMY_RAT` | |
| `FURNITURE_DESC_OBJECT_TAXIDERMY_SNAKE` | |
| `FURNITURE_DESC_OBJECT_TAXIDERMY_SQUIRREL` | |
| `FURNITURE_DESC_OBJECT_TAXIDERMY_TURTLE` | |
| `FURNITURE_DESC_OBJECT_TELEPHONE_10S` | |
| `FURNITURE_DESC_OBJECT_TOOLCHEST` | |
| `FURNITURE_DESC_OBJECT_TOXICWASTE` | |
| `FURNITURE_DESC_OBJECT_VACUUM` | |
| `FURNITURE_DESC_OBJECT_VASE_DASIY` | |
| `FURNITURE_DESC_OBJECT_VASE_LARGE` | |
| `FURNITURE_DESC_OBJECT_VASE_STICKS` | |
| `FURNITURE_DESC_OBJECT_VISIBLEMAN` | |
| `FURNITURE_DESC_OBJECT_WASHER` | |
| `FURNITURE_DESC_OBJECT_WATERTOWER` | |
| `FURNITURE_DESC_OBJECT_WOOD_TABLE` | |
| `FURNITURE_DESC_POOP` | |
| `FURNITURE_DESC_SET_80S_BED` | |
| `FURNITURE_DESC_SET_80S_CHAIR` | |
| `FURNITURE_DESC_SET_80S_COUCH` | |
| `FURNITURE_DESC_SET_80S_DRESSER` | |
| `FURNITURE_DESC_SET_80S_FRIGE` | |
| `FURNITURE_DESC_SET_80S_SHELF` | |
| `FURNITURE_DESC_SET_80S_SIDETABLE` | |
| `FURNITURE_DESC_SET_80S_STOVE` | |
| `FURNITURE_DESC_SET_80S_TABLE` | |
| `FURNITURE_DESC_SET_80S_TV` | |
| `FURNITURE_DESC_SET_90S_BED` | |
| `FURNITURE_DESC_SET_90S_CABINET` | |
| `FURNITURE_DESC_SET_90S_CABINET2` | |
| `FURNITURE_DESC_SET_90S_CHAIR` | |
| `FURNITURE_DESC_SET_90S_FRIGE` | |
| `FURNITURE_DESC_SET_90S_SHELF` | |
| `FURNITURE_DESC_SET_90S_SINK` | |
| `FURNITURE_DESC_SET_90S_STOOL` | |
| `FURNITURE_DESC_SET_90S_STOVE` | |
| `FURNITURE_DESC_SET_90S_SUSPENDEDSHELF` | |
| `FURNITURE_DESC_SET_ANGELIC_BED` | |
| `FURNITURE_DESC_SET_ANGELIC_CHAIR` | |
| `FURNITURE_DESC_SET_ANGELIC_DRESSER` | |
| `FURNITURE_DESC_SET_ANGELIC_LAMP` | |
| `FURNITURE_DESC_SET_ANGELIC_SHELF` | |
| `FURNITURE_DESC_SET_ANGELIC_SIDETABLE` | |
| `FURNITURE_DESC_SET_ANGELIC_SUSPENDEDSHELF` | |
| `FURNITURE_DESC_SET_ANGELIC_TABLE` | |
| `FURNITURE_DESC_SET_ANGELIC_TABLE2` | |
| `FURNITURE_DESC_SET_ANGELIC_TOILET` | |
| `FURNITURE_DESC_SET_ATOMIC_CHAIR` | |
| `FURNITURE_DESC_SET_ATOMIC_COUCH` | |
| `FURNITURE_DESC_SET_ATOMIC_FRIGE` | |
| `FURNITURE_DESC_SET_ATOMIC_LAMP` | |
| `FURNITURE_DESC_SET_ATOMIC_RADIO` | |
| `FURNITURE_DESC_SET_ATOMIC_SHELF` | |
| `FURNITURE_DESC_SET_ATOMIC_SIDETABLE` | |
| `FURNITURE_DESC_SET_ATOMIC_STOVE` | |
| `FURNITURE_DESC_SET_ATOMIC_TABLE` | |
| `FURNITURE_DESC_SET_ATOMIC_TV` | |
| `FURNITURE_DESC_SET_BLOCK_7` | |
| `FURNITURE_DESC_SET_BLOCK_DOWNL` | |
| `FURNITURE_DESC_SET_BLOCK_I` | |
| `FURNITURE_DESC_SET_BLOCK_L` | |
| `FURNITURE_DESC_SET_BLOCK_LAYINGL` | |
| `FURNITURE_DESC_SET_BLOCK_SIDEI` | |
| `FURNITURE_DESC_SET_BLOCK_SIDET` | |
| `FURNITURE_DESC_SET_BLOCK_SQUARE` | |
| `FURNITURE_DESC_SET_BLOCK_SQUARE2` | |
| `FURNITURE_DESC_SET_BLOCK_T` | |
| `FURNITURE_DESC_SET_BONE_CHAIR` | |
| `FURNITURE_DESC_SET_BONE_CHANDELIER` | |
| `FURNITURE_DESC_SET_BONE_COUCH` | |
| `FURNITURE_DESC_SET_BONE_LAMP` | |
| `FURNITURE_DESC_SET_BONE_PILE` | |
| `FURNITURE_DESC_SET_BONE_SHELF` | |
| `FURNITURE_DESC_SET_BONE_SIDETABLE` | |
| `FURNITURE_DESC_SET_BONE_SINK` | |
| `FURNITURE_DESC_SET_BONE_TABLE` | |
| `FURNITURE_DESC_SET_BONE_TV` | |
| `FURNITURE_DESC_SET_CAT_BED` | |
| `FURNITURE_DESC_SET_CAT_BENCH` | |
| `FURNITURE_DESC_SET_CAT_CHAIR` | |
| `FURNITURE_DESC_SET_CAT_COUCH` | |
| `FURNITURE_DESC_SET_CAT_DRESSER` | |
| `FURNITURE_DESC_SET_CAT_SHELF` | |
| `FURNITURE_DESC_SET_CAT_SUSPENDED_SHELF` | |
| `FURNITURE_DESC_SET_CAT_TABLE` | |
| `FURNITURE_DESC_SET_CAT_TABLE2` | |
| `FURNITURE_DESC_SET_CAT_TV` | |
| `FURNITURE_DESC_SET_CRYSTAL_CHAIR` | |
| `FURNITURE_DESC_SET_CRYSTAL_CHANDELIER` | |
| `FURNITURE_DESC_SET_CRYSTAL_COUCH` | |
| `FURNITURE_DESC_SET_CRYSTAL_DRESSER` | |
| `FURNITURE_DESC_SET_CRYSTAL_DRESSER2` | |
| `FURNITURE_DESC_SET_CRYSTAL_LAMP` | |
| `FURNITURE_DESC_SET_CRYSTAL_SHELF` | |
| `FURNITURE_DESC_SET_CRYSTAL_SIDETABLE` | |
| `FURNITURE_DESC_SET_CRYSTAL_TABLE` | |
| `FURNITURE_DESC_SET_CRYSTAL_TOILET` | |
| `FURNITURE_DESC_SET_CUTE_BED` | |
| `FURNITURE_DESC_SET_CUTE_CHAIR` | |
| `FURNITURE_DESC_SET_CUTE_COUCH` | |
| `FURNITURE_DESC_SET_CUTE_DRESSER` | |
| `FURNITURE_DESC_SET_CUTE_DRESSER2` | |
| `FURNITURE_DESC_SET_CUTE_SHELF` | |
| `FURNITURE_DESC_SET_CUTE_SIDETABLE` | |
| `FURNITURE_DESC_SET_CUTE_SIDETABLE2` | |
| `FURNITURE_DESC_SET_CUTE_STOOL` | |
| `FURNITURE_DESC_SET_CUTE_TABLE2` | |
| `FURNITURE_DESC_SET_ELEGANT_BED` | |
| `FURNITURE_DESC_SET_ELEGANT_CHAIR` | |
| `FURNITURE_DESC_SET_ELEGANT_DESK` | |
| `FURNITURE_DESC_SET_ELEGANT_DRESSER` | |
| `FURNITURE_DESC_SET_ELEGANT_DRESSER2` | |
| `FURNITURE_DESC_SET_ELEGANT_LAMP` | |
| `FURNITURE_DESC_SET_ELEGANT_SHELF` | |
| `FURNITURE_DESC_SET_ELEGANT_SIDETABLE` | |
| `FURNITURE_DESC_SET_ELEGANT_SIDETABLE2` | |
| `FURNITURE_DESC_SET_ELEGANT_TABLE` | |
| `FURNITURE_DESC_SET_GUTS_LAMP` | |
| `FURNITURE_DESC_SET_GUTS_LAMP2` | |
| `FURNITURE_DESC_SET_GUTS_SHELF` | |
| `FURNITURE_DESC_SET_GUTS_SIDETABLE` | |
| `FURNITURE_DESC_SET_GUTS_SIDETABLE2` | |
| `FURNITURE_DESC_SET_GUTS_SINK` | |
| `FURNITURE_DESC_SET_GUTS_SUSPENDEDSHELF` | |
| `FURNITURE_DESC_SET_GUTS_TABLE` | |
| `FURNITURE_DESC_SET_GUTS_TOILET` | |
| `FURNITURE_DESC_SET_GUTS_TV` | |
| `FURNITURE_DESC_SET_JUNK_BED` | |
| `FURNITURE_DESC_SET_JUNK_CABINET` | |
| `FURNITURE_DESC_SET_JUNK_CHAIR` | |
| `FURNITURE_DESC_SET_JUNK_DRESSER` | |
| `FURNITURE_DESC_SET_JUNK_LAMP` | |
| `FURNITURE_DESC_SET_JUNK_SHELF` | |
| `FURNITURE_DESC_SET_JUNK_SIDETABLE` | |
| `FURNITURE_DESC_SET_JUNK_SUSPENDEDSHELF` | |
| `FURNITURE_DESC_SET_JUNK_TOILET` | |
| `FURNITURE_DESC_SET_JUNK_TV` | |
| `FURNITURE_DESC_SET_MODERN_BED` | |
| `FURNITURE_DESC_SET_MODERN_CHAIR` | |
| `FURNITURE_DESC_SET_MODERN_COUCH` | |
| `FURNITURE_DESC_SET_MODERN_DESK` | |
| `FURNITURE_DESC_SET_MODERN_DRESSER` | |
| `FURNITURE_DESC_SET_MODERN_FRIGE` | |
| `FURNITURE_DESC_SET_MODERN_SIDETABLE` | |
| `FURNITURE_DESC_SET_MODERN_STOVE` | |
| `FURNITURE_DESC_SET_MODERN_TABLE` | |
| `FURNITURE_DESC_SET_MODERN_TV` | |
| `FURNITURE_DESC_SET_MONSTER_CHAIR` | |
| `FURNITURE_DESC_SET_MONSTER_DRESSER` | |
| `FURNITURE_DESC_SET_MONSTER_LAMP` | |
| `FURNITURE_DESC_SET_MONSTER_SHELF` | |
| `FURNITURE_DESC_SET_MONSTER_SIDETABLE` | |
| `FURNITURE_DESC_SET_MONSTER_SUSPENDEDSHELF` | |
| `FURNITURE_DESC_SET_MONSTER_SUSPENDEDSHELF2` | |
| `FURNITURE_DESC_SET_MONSTER_TABLE` | |
| `FURNITURE_DESC_SET_MONSTER_TABLE2` | |
| `FURNITURE_DESC_SET_MONSTER_TV` | |
| `FURNITURE_DESC_SET_MUSHROOM_CHAIR` | |
| `FURNITURE_DESC_SET_MUSHROOM_SHELF` | |
| `FURNITURE_DESC_SET_MUSHROOM_STOOL` | |
| `FURNITURE_DESC_SET_MUSHROOM_STOOL2` | |
| `FURNITURE_DESC_SET_MUSHROOM_STOOL3` | |
| `FURNITURE_DESC_SET_MUSHROOM_SUSPENDEDSHELF` | |
| `FURNITURE_DESC_SET_MUSHROOM_SUSPENDEDSHELF2` | |
| `FURNITURE_DESC_SET_MUSHROOM_TABLE` | |
| `FURNITURE_DESC_SET_MUSHROOM_TABLE1` | |
| `FURNITURE_DESC_SET_MUSHROOM_TOILET` | |
| `FURNITURE_DESC_SET_RETRO_BED` | |
| `FURNITURE_DESC_SET_RETRO_CHAIR` | |
| `FURNITURE_DESC_SET_RETRO_COUCH` | |
| `FURNITURE_DESC_SET_RETRO_DRESSER` | |
| `FURNITURE_DESC_SET_RETRO_DRESSER2` | |
| `FURNITURE_DESC_SET_RETRO_DRESSER3` | |
| `FURNITURE_DESC_SET_RETRO_FRIGE` | |
| `FURNITURE_DESC_SET_RETRO_LAMP` | |
| `FURNITURE_DESC_SET_RETRO_SIDETABLE` | |
| `FURNITURE_DESC_SET_RETRO_STOVE` | |
| `FURNITURE_DESC_SET_ROBO_DESK` | |
| `FURNITURE_DESC_SET_ROBO_DRESSER` | |
| `FURNITURE_DESC_SET_ROBO_HEAD` | |
| `FURNITURE_DESC_SET_ROBO_ROBOARMS` | |
| `FURNITURE_DESC_SET_ROBO_ROBOBODY` | |
| `FURNITURE_DESC_SET_ROBO_ROBOCHEST` | |
| `FURNITURE_DESC_SET_ROBO_SHELF` | |
| `FURNITURE_DESC_SET_ROBO_SINK` | |
| `FURNITURE_DESC_SET_ROBO_TABLE` | |
| `FURNITURE_DESC_SET_ROBO_TV` | |
| `FURNITURE_DESC_SET_RUSTIC_BENCH` | |
| `FURNITURE_DESC_SET_RUSTIC_CHAIR` | |
| `FURNITURE_DESC_SET_RUSTIC_DESK` | |
| `FURNITURE_DESC_SET_RUSTIC_DRESSER` | |
| `FURNITURE_DESC_SET_RUSTIC_SHELF` | |
| `FURNITURE_DESC_SET_RUSTIC_SIDETABLE` | |
| `FURNITURE_DESC_SET_RUSTIC_STOOL` | |
| `FURNITURE_DESC_SET_RUSTIC_SUSPENDEDSHELF` | |
| `FURNITURE_DESC_SET_RUSTIC_SUSPENDEDSHELF2` | |
| `FURNITURE_DESC_SET_RUSTIC_TABLE` | |
| `FURNITURE_DESC_SET_SEWER_CHAIR` | |
| `FURNITURE_DESC_SET_SEWER_DRESSER` | |
| `FURNITURE_DESC_SET_SEWER_LAMP` | |
| `FURNITURE_DESC_SET_SEWER_SHELF` | |
| `FURNITURE_DESC_SET_SEWER_SINK` | |
| `FURNITURE_DESC_SET_SEWER_SMALL_TABLE` | |
| `FURNITURE_DESC_SET_SEWER_STOOL` | |
| `FURNITURE_DESC_SET_SEWER_SUSPENDEDSHELF` | |
| `FURNITURE_DESC_SET_SEWER_TABLE` | |
| `FURNITURE_DESC_SET_SEWER_TV` | |
| `FURNITURE_DESC_SET_SEWN_CHAIR` | |
| `FURNITURE_DESC_SET_SEWN_COUCH` | |
| `FURNITURE_DESC_SET_SEWN_DOLL` | |
| `FURNITURE_DESC_SET_SEWN_DRESSER` | |
| `FURNITURE_DESC_SET_SEWN_SIDETABLE` | |
| `FURNITURE_DESC_SET_SEWN_STOOL1` | |
| `FURNITURE_DESC_SET_SEWN_STOOL2` | |
| `FURNITURE_DESC_SET_SEWN_TABLE` | |
| `FURNITURE_DESC_SET_SEWN_TOILET` | |
| `FURNITURE_DESC_SET_SEWN_TV` | |
| `FURNITURE_DESC_SET_SPIDER_BED` | |
| `FURNITURE_DESC_SET_SPIDER_CANDELABRA` | |
| `FURNITURE_DESC_SET_SPIDER_CHAIR` | |
| `FURNITURE_DESC_SET_SPIDER_DRESSER` | |
| `FURNITURE_DESC_SET_SPIDER_SHELF` | |
| `FURNITURE_DESC_SET_SPIDER_SIDETABLE` | |
| `FURNITURE_DESC_SET_SPIDER_TABLE` | |
| `FURNITURE_DESC_SET_SPIDER_TOILET` | |
| `FURNITURE_DESC_SET_SPIDER_TV` | |
| `FURNITURE_DESC_SET_SPIDER_VANITY` | |
| `FURNITURE_DESC_SET_WOODEN_CHAIR` | |
| `FURNITURE_DESC_SET_WOODEN_DRESSER` | |
| `FURNITURE_DESC_SET_WOODEN_LAMP` | |
| `FURNITURE_DESC_SET_WOODEN_SHELF` | |
| `FURNITURE_DESC_SET_WOODEN_SHELF2` | |
| `FURNITURE_DESC_SET_WOODEN_SINK` | |
| `FURNITURE_DESC_SET_WOODEN_SUSPENDEDSHELF` | |
| `FURNITURE_DESC_SET_WOODEN_TABLE` | |
| `FURNITURE_DESC_SET_WOODEN_TOILET` | |
| `FURNITURE_DESC_SET_WOODEN_TV` | |
| `FURNITURE_DESC_SMALL_90SPHONE` | |
| `FURNITURE_DESC_SMALL_90SPHONE2` | |
| `FURNITURE_DESC_SMALL_ALARMCLOCK1` | |
| `FURNITURE_DESC_SMALL_ALARMCLOCK2` | |
| `FURNITURE_DESC_SMALL_BED` | |
| `FURNITURE_DESC_SMALL_BELL` | |
| `FURNITURE_DESC_SMALL_BIGEGG` | |
| `FURNITURE_DESC_SMALL_BLACKBOX` | |
| `FURNITURE_DESC_SMALL_BOBBLE_ALONE` | |
| `FURNITURE_DESC_SMALL_BOBBLE_DAN` | |
| `FURNITURE_DESC_SMALL_BOBBLE_DARKCAT` | |
| `FURNITURE_DESC_SMALL_BOBBLE_DEVIL` | |
| `FURNITURE_DESC_SMALL_BOBBLE_GRUMP` | |
| `FURNITURE_DESC_SMALL_BOBBLE_GUPPY` | |
| `FURNITURE_DESC_SMALL_BOBBLE_HAPPY` | |
| `FURNITURE_DESC_SMALL_BOBBLE_MAD` | |
| `FURNITURE_DESC_SMALL_BOBBLE_MONEY` | |
| `FURNITURE_DESC_SMALL_BOBBLE_SPOTS` | |
| `FURNITURE_DESC_SMALL_BOBBLE_ZOMBIE` | |
| `FURNITURE_DESC_SMALL_BOTTLE_2BOTTLES` | |
| `FURNITURE_DESC_SMALL_BOTTLE_EMPTY` | |
| `FURNITURE_DESC_SMALL_BOTTLE_FULL` | |
| `FURNITURE_DESC_SMALL_BOWLINGBALL` | |
| `FURNITURE_DESC_SMALL_CANDLE_BLACK1` | |
| `FURNITURE_DESC_SMALL_CANDLE_BLACK2` | |
| `FURNITURE_DESC_SMALL_CANDLE_BLACK3` | |
| `FURNITURE_DESC_SMALL_CANDLE_BLACK4` | |
| `FURNITURE_DESC_SMALL_CANDLE_WHITE1` | |
| `FURNITURE_DESC_SMALL_CANDLE_WHITE2` | |
| `FURNITURE_DESC_SMALL_CANDLE_WHITE3` | |
| `FURNITURE_DESC_SMALL_CANDLE_WHITE4` | |
| `FURNITURE_DESC_SMALL_COUCH` | |
| `FURNITURE_DESC_SMALL_CRATE` | |
| `FURNITURE_DESC_SMALL_DEADRAT` | |
| `FURNITURE_DESC_SMALL_DOLL_AETHER` | |
| `FURNITURE_DESC_SMALL_DOLL_DUKE` | |
| `FURNITURE_DESC_SMALL_DOLL_GISH` | |
| `FURNITURE_DESC_SMALL_DOLL_GUPPY` | |
| `FURNITURE_DESC_SMALL_DOLL_ISAAC` | |
| `FURNITURE_DESC_SMALL_DOLL_STACY` | |
| `FURNITURE_DESC_SMALL_DOLL_STEVEN` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_BRAIN` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_CELLPHONE` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_DUCKPHONE` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_GAMEPAD` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_GAMESYSTEM` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_HANDRADIO` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_HANDRADIO2` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_JOYSTICK` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_LIPPHONE` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_MOON` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_MOUSE` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_MYSTERIOUSSKULL` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_OLDPHONE` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_OLDPHONE2` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_OLDPHONE3` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_OOZE` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_PHONE1` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_PHONE2` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_PHONE3` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_SPEAKER` | |
| `FURNITURE_DESC_SMALL_ELECTRONICS_WALKYTALKY` | |
| `FURNITURE_DESC_SMALL_EYEBALL` | |
| `FURNITURE_DESC_SMALL_FOOD_APPLE` | |
| `FURNITURE_DESC_SMALL_FOOD_BROCCOLI` | |
| `FURNITURE_DESC_SMALL_FOOD_CUPCAKE` | |
| `FURNITURE_DESC_SMALL_FOOD_CUPCAKE2` | |
| `FURNITURE_DESC_SMALL_FOOD_EGGPLANT` | |
| `FURNITURE_DESC_SMALL_FOOD_LEMON` | |
| `FURNITURE_DESC_SMALL_FOOD_ONION` | |
| `FURNITURE_DESC_SMALL_FOOD_ORANGE` | |
| `FURNITURE_DESC_SMALL_FOOD_PINEAPPLE` | |
| `FURNITURE_DESC_SMALL_FOOD_POTATO` | |
| `FURNITURE_DESC_SMALL_FOOD_PUMPKIN` | |
| `FURNITURE_DESC_SMALL_FOOD_RADISH` | |
| `FURNITURE_DESC_SMALL_FOOD_ROOT` | |
| `FURNITURE_DESC_SMALL_FOOD_SAUSAGE` | |
| `FURNITURE_DESC_SMALL_FOOD_SQUASH` | |
| `FURNITURE_DESC_SMALL_FRIGE` | |
| `FURNITURE_DESC_SMALL_GEM` | |
| `FURNITURE_DESC_SMALL_IRON` | |
| `FURNITURE_DESC_SMALL_JAR_COINS` | |
| `FURNITURE_DESC_SMALL_JAR_DISEASES` | |
| `FURNITURE_DESC_SMALL_JAR_EMPTY` | |
| `FURNITURE_DESC_SMALL_JAR_EMPTY2` | |
| `FURNITURE_DESC_SMALL_JAR_EMPTY3` | |
| `FURNITURE_DESC_SMALL_JAR_EYEBALLS` | |
| `FURNITURE_DESC_SMALL_JAR_FAIRY` | |
| `FURNITURE_DESC_SMALL_JAR_FISH` | |
| `FURNITURE_DESC_SMALL_JAR_FLYS` | |
| `FURNITURE_DESC_SMALL_JAR_GHOST` | |
| `FURNITURE_DESC_SMALL_JAR_HEART` | |
| `FURNITURE_DESC_SMALL_JAR_NAILS` | |
| `FURNITURE_DESC_SMALL_JAR_SPIDER` | |
| `FURNITURE_DESC_SMALL_JAR_TADPOLE` | |
| `FURNITURE_DESC_SMALL_JUG` | |
| `FURNITURE_DESC_SMALL_KETTLE` | |
| `FURNITURE_DESC_SMALL_KNOCKER` | |
| `FURNITURE_DESC_SMALL_LAB_FLASK` | |
| `FURNITURE_DESC_SMALL_LAB_FLASK2` | |
| `FURNITURE_DESC_SMALL_LAB_FLASK3` | |
| `FURNITURE_DESC_SMALL_LAB_FLASK4` | |
| `FURNITURE_DESC_SMALL_LAB_JUG1` | |
| `FURNITURE_DESC_SMALL_LAB_JUG2` | |
| `FURNITURE_DESC_SMALL_LAB_JUG3` | |
| `FURNITURE_DESC_SMALL_LAB_TANK1` | |
| `FURNITURE_DESC_SMALL_LAB_TANK2` | |
| `FURNITURE_DESC_SMALL_LAB_TESTTUBE` | |
| `FURNITURE_DESC_SMALL_LAB_TESTTUBE2` | |
| `FURNITURE_DESC_SMALL_LETTERBLOCK1` | |
| `FURNITURE_DESC_SMALL_LETTERBLOCK2` | |
| `FURNITURE_DESC_SMALL_LETTERBLOCK3` | |
| `FURNITURE_DESC_SMALL_LETTERBLOCK4` | |
| `FURNITURE_DESC_SMALL_LETTERBLOCK5` | |
| `FURNITURE_DESC_SMALL_LETTERBLOCK6` | |
| `FURNITURE_DESC_SMALL_LETTERBLOCK7` | |
| `FURNITURE_DESC_SMALL_LETTERBLOCK8` | |
| `FURNITURE_DESC_SMALL_LOTION` | |
| `FURNITURE_DESC_SMALL_MEDS_CATHEARTS` | |
| `FURNITURE_DESC_SMALL_MEDS_COUGHSYRUP` | |
| `FURNITURE_DESC_SMALL_MEDS_FISHOIL` | |
| `FURNITURE_DESC_SMALL_MEDS_MYSTERY2` | |
| `FURNITURE_DESC_SMALL_MEDS_MYSTERYBOTTLE` | |
| `FURNITURE_DESC_SMALL_MEDS_PILLS1` | |
| `FURNITURE_DESC_SMALL_MEDS_PILLS2` | |
| `FURNITURE_DESC_SMALL_MILK` | |
| `FURNITURE_DESC_SMALL_MUG` | |
| `FURNITURE_DESC_SMALL_MUG2` | |
| `FURNITURE_DESC_SMALL_PENCUP` | |
| `FURNITURE_DESC_SMALL_PERFUME` | |
| `FURNITURE_DESC_SMALL_PICTURE_CAN` | |
| `FURNITURE_DESC_SMALL_PICTURE_CAT` | |
| `FURNITURE_DESC_SMALL_PICTURE_SPOON` | |
| `FURNITURE_DESC_SMALL_PIGGYBANK` | |
| `FURNITURE_DESC_SMALL_PILLBOTTLE` | |
| `FURNITURE_DESC_SMALL_PIN` | |
| `FURNITURE_DESC_SMALL_RUBBERDUCK` | |
| `FURNITURE_DESC_SMALL_SHELF` | |
| `FURNITURE_DESC_SMALL_SHELL` | |
| `FURNITURE_DESC_SMALL_SIDETABLE` | |
| `FURNITURE_DESC_SMALL_SINK` | |
| `FURNITURE_DESC_SMALL_SNOWGLOBE` | |
| `FURNITURE_DESC_SMALL_STOVE` | |
| `FURNITURE_DESC_SMALL_TISSUES` | |
| `FURNITURE_DESC_SMALL_TRASH_APPLE` | |
| `FURNITURE_DESC_SMALL_TRASH_BANANA` | |
| `FURNITURE_DESC_SMALL_TRASH_BONE` | |
| `FURNITURE_DESC_SMALL_TRASH_BREAD` | |
| `FURNITURE_DESC_SMALL_TRASH_BROKENBOTTLE` | |
| `FURNITURE_DESC_SMALL_TRASH_CAN2` | |
| `FURNITURE_DESC_SMALL_TRASH_CANS` | |
| `FURNITURE_DESC_SMALL_TRASH_CHEESE` | |
| `FURNITURE_DESC_SMALL_TRASH_CUP` | |
| `FURNITURE_DESC_SMALL_TRASH_EGGS` | |
| `FURNITURE_DESC_SMALL_TRASH_MILK` | |
| `FURNITURE_DESC_SMALL_VASE1` | |
| `FURNITURE_DESC_SMALL_VASE2` | |
| `FURNITURE_DESC_SMALL_VASE3` | |
| `FURNITURE_DESC_SMALL_WATERBOTTLE` | |
| `FURNITURE_DESC_SMALL_WOBBLEBIRD` | |
| `FURNITURE_DESC_SPECIAL_APPEALIDOL` | |
| `FURNITURE_DESC_SPECIAL_COMFORTIDOL` | |
| `FURNITURE_DESC_SPECIAL_EVOLUTIONIDOL` | |
| `FURNITURE_DESC_SPECIAL_FIGHTIDOL` | |
| `FURNITURE_DESC_SPECIAL_FOODBOX` | |
| `FURNITURE_DESC_SPECIAL_HEALTHIDOL` | |
| `FURNITURE_DESC_SPECIAL_STIMULATIONIDOL` | |
| `FURNITURE_DESC_SPECIAL_SUPPRESSORIDOL` | |
| `FURNITURE_DESC_WALLMOUNTED_ATOMIC_CLOCK` | |
| `FURNITURE_DESC_WALLMOUNTED_BALLOON` | |
| `FURNITURE_DESC_WALLMOUNTED_BALLOON2` | |
| `FURNITURE_DESC_WALLMOUNTED_BALLOON3` | |
| `FURNITURE_DESC_WALLMOUNTED_BALLOON4` | |
| `FURNITURE_DESC_WALLMOUNTED_BALLOON5` | |
| `FURNITURE_DESC_WALLMOUNTED_BALLOON6` | |
| `FURNITURE_DESC_WALLMOUNTED_BALLOON7` | |
| `FURNITURE_DESC_WALLMOUNTED_BLOCK1` | |
| `FURNITURE_DESC_WALLMOUNTED_BLOCK2` | |
| `FURNITURE_DESC_WALLMOUNTED_BLOCK3` | |
| `FURNITURE_DESC_WALLMOUNTED_BRICKS1` | |
| `FURNITURE_DESC_WALLMOUNTED_BRICKS2` | |
| `FURNITURE_DESC_WALLMOUNTED_BRICKS3` | |
| `FURNITURE_DESC_WALLMOUNTED_BRICKS4` | |
| `FURNITURE_DESC_WALLMOUNTED_CLOCK` | |
| `FURNITURE_DESC_WALLMOUNTED_CLOUD` | |
| `FURNITURE_DESC_WALLMOUNTED_COWSKULL` | |
| `FURNITURE_DESC_WALLMOUNTED_CRACK` | |
| `FURNITURE_DESC_WALLMOUNTED_FURNACE` | |
| `FURNITURE_DESC_WALLMOUNTED_GHOST1` | |
| `FURNITURE_DESC_WALLMOUNTED_GHOST2` | |
| `FURNITURE_DESC_WALLMOUNTED_GHOST3` | |
| `FURNITURE_DESC_WALLMOUNTED_JOLLYROGER` | |
| `FURNITURE_DESC_WALLMOUNTED_JUNK_PAPER1` | |
| `FURNITURE_DESC_WALLMOUNTED_JUNK_PAPER2` | |
| `FURNITURE_DESC_WALLMOUNTED_MASK_BUNNY` | |
| `FURNITURE_DESC_WALLMOUNTED_MASK_HOCKY` | |
| `FURNITURE_DESC_WALLMOUNTED_MASK_INFAMY` | |
| `FURNITURE_DESC_WALLMOUNTED_MASK_TONETTA` | |
| `FURNITURE_DESC_WALLMOUNTED_MIRROR` | |
| `FURNITURE_DESC_WALLMOUNTED_OUTLET` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_BLUEBOY` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_CHE` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_DRAWING` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_ERASER` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_FRIDA` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_GOD` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_GOTHIC` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_HANG` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_JAWS` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_KEITH` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_LAMBS` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_LISA` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_MAGAZINE` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_NIGHT` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_OBEY` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_ORANGE` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_PEARL` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_PHOTO` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_PHOTO2` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_PHOTO3` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_PICASSO` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_POEM` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_ROSIE` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_SAILBOAT` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_SCARFACE` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_SCREAM` | |
| `FURNITURE_DESC_WALLMOUNTED_PICTURE_UFO` | |
| `FURNITURE_DESC_WALLMOUNTED_ROBO_PLATE1` | |
| `FURNITURE_DESC_WALLMOUNTED_ROBO_PLATE2` | |
| `FURNITURE_DESC_WALLMOUNTED_ROBO_PLATE3` | |
| `FURNITURE_DESC_WALLMOUNTED_ROBO_PLATE4` | |
| `FURNITURE_DESC_WALLMOUNTED_SAFE` | |
| `FURNITURE_DESC_WALLMOUNTED_SEWER_PIPES1` | |
| `FURNITURE_DESC_WALLMOUNTED_SEWER_PIPES2` | |
| `FURNITURE_DESC_WALLMOUNTED_SEWER_PIPES3` | |
| `FURNITURE_DESC_WALLMOUNTED_SEWN_CLOCK` | |
| `FURNITURE_DESC_WALLMOUNTED_SHRUNKINHEAD` | |
| `FURNITURE_DESC_WALLMOUNTED_SWITCH` | |
| `FURNITURE_DESC_WALLMOUNTED_TAXIDERMY_BUGS` | |
| `FURNITURE_DESC_WALLMOUNTED_TAXIDERMY_DEERHEAD` | |
| `FURNITURE_DESC_WALLMOUNTED_TAXIDERMY_FISH` | |
| `FURNITURE_DESC_WALLMOUNTED_TAXIDERMY_GUPPY` | |
| `FURNITURE_DESC_WALLMOUNTED_TORCH` | |
| `FURNITURE_DESC_WALLMOUNTED_TV` | |
| `FURNITURE_DESC_WALLMOUNTED_WOODEN_BOARDS1` | |
| `FURNITURE_DESC_WALLMOUNTED_WOODEN_BOARDS2` | |
| `FURNITURE_DESC_WALLMOUNTED_WOODEN_BOARDS3` | |
| `FURNITURE_DESC_WALLMOUNTED_WOODEN_BOARDS4` | |
| `FURNITURE_DESC_WALLMOUNTED_WOODEN_CLOCK` | |
| `MUTATION_EYEBROWS_301_DESC` | |
| `MUTATION_EYEBROWS_306_DESC` | |
| `MUTATION_EYEBROWS_307_DESC` | |
| `MUTATION_EYEBROWS_309_DESC` | |
| `MUTATION_EYEBROWS_310_DESC` | |
| `MUTATION_EYEBROWS_311_DESC` | |
| `MUTATION_EYEBROWS_313_DESC` | |
| `MUTATION_EYEBROWS_314_DESC` | |
| `MUTATION_EYEBROWS_315_DESC` | |
| `MUTATION_EYEBROWS_900_DESC` | |

</details>


---

### Enum: `name`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](./Abilities_and_Spells.md#context-meta), [`graphics`](./Characters_and_Bosses.md#context-graphics), [`ROOT`](./Furniture_and_Metaprogression.md#context-root), [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ARMOR_ASTEROIDBELT_NAME` | |
| `ARMOR_CATCOLLAR_NAME` | |
| `ARMOR_CATEARS_NAME` | |
| `ARMOR_CATWHISKERS_NAME` | |
| `ARMOR_DEATHMASK_NAME` | |
| `ARMOR_DEBRISARMOR_NAME` | |
| `ARMOR_DEBRISHAT_NAME` | |
| `ARMOR_DEBRISMASK_NAME` | |
| `ARMOR_DIVINERSCLOTH_NAME` | |
| `ARMOR_DRYBONEHAT_NAME` | |
| `ARMOR_DRYBONEMASK_NAME` | |
| `ARMOR_DRYBONENECKLACE_NAME` | |
| `ARMOR_EXPERIMENTALHAT_NAME` | |
| `ARMOR_EXPERIMENTALMASK_NAME` | |
| `ARMOR_EXPERIMENTALNECK_NAME` | |
| `ARMOR_FACEBRAND_NAME` | |
| `ARMOR_FACEWRAP_NAME` | |
| `ARMOR_FLESHSHROUD_NAME` | |
| `ARMOR_FLOWERHAT_NAME` | |
| `ARMOR_FLOWERMASK_NAME` | |
| `ARMOR_FLOWERNECKLACE_NAME` | |
| `ARMOR_GREENMANMASK_NAME` | |
| `ARMOR_HEADBRAND_NAME` | |
| `ARMOR_HEADWRAP_NAME` | |
| `ARMOR_HOOKEDNECKLACE_NAME` | |
| `ARMOR_HUMANFLESHARMOR_NAME` | |
| `ARMOR_HUMANFLESHHAT_NAME` | |
| `ARMOR_HUMANFLESHMASK_NAME` | |
| `ARMOR_IRONJAW_NAME` | |
| `ARMOR_LEECHNECKLACE_NAME` | |
| `ARMOR_MANGLASSES_NAME` | |
| `ARMOR_MANHAIR_NAME` | |
| `ARMOR_MANTIE_NAME` | |
| `ARMOR_MINIMOON_NAME` | |
| `ARMOR_MUSHROOMHAT_NAME` | |
| `ARMOR_MYSTICEYE_NAME` | |
| `ARMOR_NECKWRAP_NAME` | |
| `ARMOR_OBELISKARMOR_NAME` | |
| `ARMOR_OBELISKHAT_NAME` | |
| `ARMOR_OBELISKMASK_NAME` | |
| `ARMOR_PRAYERBEADS_NAME` | |
| `ARMOR_RINGOFMUSHROOMS_NAME` | |
| `ARMOR_ROCKYHAT_NAME` | |
| `ARMOR_ROCKYMASK_NAME` | |
| `ARMOR_ROCKYNECKLACE_NAME` | |
| `ARMOR_SCRAPPERSBACKPACK_NAME` | |
| `ARMOR_SCRAPPERSHAT_NAME` | |
| `ARMOR_SCRAPPERSMASK_NAME` | |
| `ARMOR_SPACEANTENNA_NAME` | |
| `ARMOR_SPACEBOOSTERS_NAME` | |
| `ARMOR_SPACEHELMET_NAME` | |
| `ARMOR_SPIDERHAT_NAME` | |
| `ARMOR_TENTACLEHAT_NAME` | |
| `ARMOR_TENTACLEMASK_NAME` | |
| `ARMOR_TENTACLENECK_NAME` | |
| `ARMOR_TINFOILHAT_NAME` | |
| `ARMOR_TINYPLANET_NAME` | |
| `EABILITY_BIRTH_NAME` | |
| `EABILITY_T3RIPANDTEAR_NAME` | |
| `ENEMY_CATHUMAN_NAME` | |
| `ENEMY_HUMANCAT_NAME` | |
| `FURNITURE_NAME_AUTOFEEDER` | |
| `FURNITURE_NAME_CEILING_CAGE` | |
| `FURNITURE_NAME_CEILING_DISCOBALL` | |
| `FURNITURE_NAME_CEILING_FAN` | |
| `FURNITURE_NAME_HANGING_AIRFRESHINER` | |
| `FURNITURE_NAME_HANGING_CATHEAD` | |
| `FURNITURE_NAME_HANGING_FISH` | |
| `FURNITURE_NAME_OBJECT_BARREL` | |
| `FURNITURE_NAME_OBJECT_BATH1` | |
| `FURNITURE_NAME_OBJECT_BATH2` | |
| `FURNITURE_NAME_OBJECT_BBQ` | |
| `FURNITURE_NAME_OBJECT_BED` | |
| `FURNITURE_NAME_OBJECT_BIRDCAGE` | |
| `FURNITURE_NAME_OBJECT_BOOKS1` | |
| `FURNITURE_NAME_OBJECT_BOOKS10` | |
| `FURNITURE_NAME_OBJECT_BOOKS11` | |
| `FURNITURE_NAME_OBJECT_BOOKS12` | |
| `FURNITURE_NAME_OBJECT_BOOKS2` | |
| `FURNITURE_NAME_OBJECT_BOOKS3` | |
| `FURNITURE_NAME_OBJECT_BOOKS4` | |
| `FURNITURE_NAME_OBJECT_BOOKS5` | |
| `FURNITURE_NAME_OBJECT_BOOKS6` | |
| `FURNITURE_NAME_OBJECT_BOOKS7` | |
| `FURNITURE_NAME_OBJECT_BOOKS8` | |
| `FURNITURE_NAME_OBJECT_BOOKS9` | |
| `FURNITURE_NAME_OBJECT_BOX` | |
| `FURNITURE_NAME_OBJECT_BROOM` | |
| `FURNITURE_NAME_OBJECT_BUG_CENIPEDE` | |
| `FURNITURE_NAME_OBJECT_BUG_PILLBUG` | |
| `FURNITURE_NAME_OBJECT_BUG_SPIDER` | |
| `FURNITURE_NAME_OBJECT_CATTREE1` | |
| `FURNITURE_NAME_OBJECT_CATTREE2` | |
| `FURNITURE_NAME_OBJECT_CATTREE3` | |
| `FURNITURE_NAME_OBJECT_CHEST` | |
| `FURNITURE_NAME_OBJECT_CINDERBLOCK1` | |
| `FURNITURE_NAME_OBJECT_CINDERBLOCK2` | |
| `FURNITURE_NAME_OBJECT_CLOCK` | |
| `FURNITURE_NAME_OBJECT_COFFEN` | |
| `FURNITURE_NAME_OBJECT_CRATE` | |
| `FURNITURE_NAME_OBJECT_CRYSTALBALL` | |
| `FURNITURE_NAME_OBJECT_DIAMOND` | |
| `FURNITURE_NAME_OBJECT_DOLLHOUSE` | |
| `FURNITURE_NAME_OBJECT_DRYER` | |
| `FURNITURE_NAME_OBJECT_EASEL` | |
| `FURNITURE_NAME_OBJECT_ELECTRONICS_ARCADE1` | |
| `FURNITURE_NAME_OBJECT_ELECTRONICS_ARCADE2` | |
| `FURNITURE_NAME_OBJECT_ELECTRONICS_CRANEGAME` | |
| `FURNITURE_NAME_OBJECT_ELECTRONICS_DVDPLAYER` | |
| `FURNITURE_NAME_OBJECT_ELECTRONICS_FAN` | |
| `FURNITURE_NAME_OBJECT_ELECTRONICS_LAPTOP` | |
| `FURNITURE_NAME_OBJECT_ELECTRONICS_LAVALAMP` | |
| `FURNITURE_NAME_OBJECT_ELECTRONICS_MICROWAVE` | |
| `FURNITURE_NAME_OBJECT_ELECTRONICS_MICROWAVE2` | |
| `FURNITURE_NAME_OBJECT_ELECTRONICS_MICROWAVE3` | |
| `FURNITURE_NAME_OBJECT_ELECTRONICS_MONITOR` | |
| `FURNITURE_NAME_OBJECT_ELECTRONICS_ORB` | |
| `FURNITURE_NAME_OBJECT_ELECTRONICS_PC` | |
| `FURNITURE_NAME_OBJECT_ELECTRONICS_PRINTER` | |
| `FURNITURE_NAME_OBJECT_ELECTRONICS_SPEAKER` | |
| `FURNITURE_NAME_OBJECT_ELECTRONICS_VHS` | |
| `FURNITURE_NAME_OBJECT_FILINGCABINET` | |
| `FURNITURE_NAME_OBJECT_FIREPLACE` | |
| `FURNITURE_NAME_OBJECT_FISHTANK_BLOWFISH` | |
| `FURNITURE_NAME_OBJECT_FISHTANK_BOOZE` | |
| `FURNITURE_NAME_OBJECT_FISHTANK_CATFISH` | |
| `FURNITURE_NAME_OBJECT_FISHTANK_CHAMELEON` | |
| `FURNITURE_NAME_OBJECT_FISHTANK_MERMAID` | |
| `FURNITURE_NAME_OBJECT_FISHTANK_OCTOCAT` | |
| `FURNITURE_NAME_OBJECT_FISHTANK_SMALL_FISH` | |
| `FURNITURE_NAME_OBJECT_FISHTANK_SMALL_LILFISH` | |
| `FURNITURE_NAME_OBJECT_FISHTANK_SMALL_LILFISHES` | |
| `FURNITURE_NAME_OBJECT_FISHTANK_SMALL_POOP` | |
| `FURNITURE_NAME_OBJECT_FISHTANK_SMALL_SKULL` | |
| `FURNITURE_NAME_OBJECT_FISHTANK_SMALL_TADPOLES` | |
| `FURNITURE_NAME_OBJECT_FISHTANK_TADPOLES` | |
| `FURNITURE_NAME_OBJECT_FISHTANK_WHALE` | |
| `FURNITURE_NAME_OBJECT_FOOD_HAM` | |
| `FURNITURE_NAME_OBJECT_FOOD_TURKEY` | |
| `FURNITURE_NAME_OBJECT_FORTUNETELLER` | |
| `FURNITURE_NAME_OBJECT_GASTANK` | |
| `FURNITURE_NAME_OBJECT_GNOME` | |
| `FURNITURE_NAME_OBJECT_ICECHEST` | |
| `FURNITURE_NAME_OBJECT_IRONINGBOARD` | |
| `FURNITURE_NAME_OBJECT_IV` | |
| `FURNITURE_NAME_OBJECT_JAR_CAT` | |
| `FURNITURE_NAME_OBJECT_JAR_EGGS` | |
| `FURNITURE_NAME_OBJECT_JAR_EMPTY` | |
| `FURNITURE_NAME_OBJECT_JAR_FETUS` | |
| `FURNITURE_NAME_OBJECT_JAR_HEAD1` | |
| `FURNITURE_NAME_OBJECT_JAR_HEAD2` | |
| `FURNITURE_NAME_OBJECT_LOG` | |
| `FURNITURE_NAME_OBJECT_OLDSTOVE` | |
| `FURNITURE_NAME_OBJECT_OUTHOUSE` | |
| `FURNITURE_NAME_OBJECT_PLANT_BULB1` | |
| `FURNITURE_NAME_OBJECT_PLANT_BULB2` | |
| `FURNITURE_NAME_OBJECT_PLANT_BULB3` | |
| `FURNITURE_NAME_OBJECT_PLANT_BUSH` | |
| `FURNITURE_NAME_OBJECT_PLANT_CACTUS` | |
| `FURNITURE_NAME_OBJECT_PLANT_CUTECACTUS` | |
| `FURNITURE_NAME_OBJECT_PLANT_DAISY` | |
| `FURNITURE_NAME_OBJECT_PLANT_FLOWERS` | |
| `FURNITURE_NAME_OBJECT_PLANT_FLYTRAP` | |
| `FURNITURE_NAME_OBJECT_PLANT_MONSTERA` | |
| `FURNITURE_NAME_OBJECT_PLANT_MUSHROOM` | |
| `FURNITURE_NAME_OBJECT_PLANT_MUSHROOMS` | |
| `FURNITURE_NAME_OBJECT_PLANT_ORCHID` | |
| `FURNITURE_NAME_OBJECT_PLANT_PIRANHASPLANT` | |
| `FURNITURE_NAME_OBJECT_PLANT_POTATO` | |
| `FURNITURE_NAME_OBJECT_PLANT_RAFFLESIA` | |
| `FURNITURE_NAME_OBJECT_PLANT_SPIKEY` | |
| `FURNITURE_NAME_OBJECT_PLANT_SUNFLOWER` | |
| `FURNITURE_NAME_OBJECT_PLANT_TENTACLE` | |
| `FURNITURE_NAME_OBJECT_POTOPOTTY` | |
| `FURNITURE_NAME_OBJECT_PUNCHY` | |
| `FURNITURE_NAME_OBJECT_RADIO_30S` | |
| `FURNITURE_NAME_OBJECT_RADIO_40S` | |
| `FURNITURE_NAME_OBJECT_RADIO_50S` | |
| `FURNITURE_NAME_OBJECT_RADIO_60S` | |
| `FURNITURE_NAME_OBJECT_RADIO_70S` | |
| `FURNITURE_NAME_OBJECT_RADIO_80S` | |
| `FURNITURE_NAME_OBJECT_RADIO_90S` | |
| `FURNITURE_NAME_OBJECT_RADIO_ATOMIC` | |
| `FURNITURE_NAME_OBJECT_ROCK` | |
| `FURNITURE_NAME_OBJECT_SAFE` | |
| `FURNITURE_NAME_OBJECT_SHOWER` | |
| `FURNITURE_NAME_OBJECT_SINK` | |
| `FURNITURE_NAME_OBJECT_SMALLROCK` | |
| `FURNITURE_NAME_OBJECT_STATUE_BAST` | |
| `FURNITURE_NAME_OBJECT_STATUE_BUDDAH` | |
| `FURNITURE_NAME_OBJECT_STATUE_DARUMA` | |
| `FURNITURE_NAME_OBJECT_STATUE_DEVIL` | |
| `FURNITURE_NAME_OBJECT_STATUE_EASTERISLANDLARGE` | |
| `FURNITURE_NAME_OBJECT_STATUE_EASTERISLANDMEDIUM` | |
| `FURNITURE_NAME_OBJECT_STATUE_EASTERISLANDSMALL` | |
| `FURNITURE_NAME_OBJECT_STATUE_JESUS` | |
| `FURNITURE_NAME_OBJECT_STATUE_LION` | |
| `FURNITURE_NAME_OBJECT_STATUE_LOTUS` | |
| `FURNITURE_NAME_OBJECT_STATUE_LUCKYCAT` | |
| `FURNITURE_NAME_OBJECT_STATUE_MERMAID` | |
| `FURNITURE_NAME_OBJECT_STATUE_STONEHEAD` | |
| `FURNITURE_NAME_OBJECT_TAXIDERMY_BAT` | |
| `FURNITURE_NAME_OBJECT_TAXIDERMY_BEAR` | |
| `FURNITURE_NAME_OBJECT_TAXIDERMY_BIRD` | |
| `FURNITURE_NAME_OBJECT_TAXIDERMY_CROW` | |
| `FURNITURE_NAME_OBJECT_TAXIDERMY_FISH` | |
| `FURNITURE_NAME_OBJECT_TAXIDERMY_GOPHER` | |
| `FURNITURE_NAME_OBJECT_TAXIDERMY_LIZARD` | |
| `FURNITURE_NAME_OBJECT_TAXIDERMY_MOUSE` | |
| `FURNITURE_NAME_OBJECT_TAXIDERMY_PIG` | |
| `FURNITURE_NAME_OBJECT_TAXIDERMY_RAT` | |
| `FURNITURE_NAME_OBJECT_TAXIDERMY_SNAKE` | |
| `FURNITURE_NAME_OBJECT_TAXIDERMY_SQUIRREL` | |
| `FURNITURE_NAME_OBJECT_TAXIDERMY_TURTLE` | |
| `FURNITURE_NAME_OBJECT_TELEPHONE_10S` | |
| `FURNITURE_NAME_OBJECT_TOOLCHEST` | |
| `FURNITURE_NAME_OBJECT_TOXICWASTE` | |
| `FURNITURE_NAME_OBJECT_VACUUM` | |
| `FURNITURE_NAME_OBJECT_VASE_DASIY` | |
| `FURNITURE_NAME_OBJECT_VASE_LARGE` | |
| `FURNITURE_NAME_OBJECT_VASE_STICKS` | |
| `FURNITURE_NAME_OBJECT_VISIBLEMAN` | |
| `FURNITURE_NAME_OBJECT_WASHER` | |
| `FURNITURE_NAME_OBJECT_WATERTOWER` | |
| `FURNITURE_NAME_OBJECT_WOOD_TABLE` | |
| `FURNITURE_NAME_POOP` | |
| `FURNITURE_NAME_SET_80S_BED` | |
| `FURNITURE_NAME_SET_80S_CHAIR` | |
| `FURNITURE_NAME_SET_80S_COUCH` | |
| `FURNITURE_NAME_SET_80S_DRESSER` | |
| `FURNITURE_NAME_SET_80S_FRIGE` | |
| `FURNITURE_NAME_SET_80S_SHELF` | |
| `FURNITURE_NAME_SET_80S_SIDETABLE` | |
| `FURNITURE_NAME_SET_80S_STOVE` | |
| `FURNITURE_NAME_SET_80S_TABLE` | |
| `FURNITURE_NAME_SET_80S_TV` | |
| `FURNITURE_NAME_SET_90S_BED` | |
| `FURNITURE_NAME_SET_90S_CABINET` | |
| `FURNITURE_NAME_SET_90S_CABINET2` | |
| `FURNITURE_NAME_SET_90S_CHAIR` | |
| `FURNITURE_NAME_SET_90S_FRIGE` | |
| `FURNITURE_NAME_SET_90S_SHELF` | |
| `FURNITURE_NAME_SET_90S_SINK` | |
| `FURNITURE_NAME_SET_90S_STOOL` | |
| `FURNITURE_NAME_SET_90S_STOVE` | |
| `FURNITURE_NAME_SET_90S_SUSPENDEDSHELF` | |
| `FURNITURE_NAME_SET_ANGELIC_BED` | |
| `FURNITURE_NAME_SET_ANGELIC_CHAIR` | |
| `FURNITURE_NAME_SET_ANGELIC_DRESSER` | |
| `FURNITURE_NAME_SET_ANGELIC_LAMP` | |
| `FURNITURE_NAME_SET_ANGELIC_SHELF` | |
| `FURNITURE_NAME_SET_ANGELIC_SIDETABLE` | |
| `FURNITURE_NAME_SET_ANGELIC_SUSPENDEDSHELF` | |
| `FURNITURE_NAME_SET_ANGELIC_TABLE` | |
| `FURNITURE_NAME_SET_ANGELIC_TABLE2` | |
| `FURNITURE_NAME_SET_ANGELIC_TOILET` | |
| `FURNITURE_NAME_SET_ATOMIC_CHAIR` | |
| `FURNITURE_NAME_SET_ATOMIC_COUCH` | |
| `FURNITURE_NAME_SET_ATOMIC_FRIGE` | |
| `FURNITURE_NAME_SET_ATOMIC_LAMP` | |
| `FURNITURE_NAME_SET_ATOMIC_RADIO` | |
| `FURNITURE_NAME_SET_ATOMIC_SHELF` | |
| `FURNITURE_NAME_SET_ATOMIC_SIDETABLE` | |
| `FURNITURE_NAME_SET_ATOMIC_STOVE` | |
| `FURNITURE_NAME_SET_ATOMIC_TABLE` | |
| `FURNITURE_NAME_SET_ATOMIC_TV` | |
| `FURNITURE_NAME_SET_BLOCK_7` | |
| `FURNITURE_NAME_SET_BLOCK_DOWNL` | |
| `FURNITURE_NAME_SET_BLOCK_I` | |
| `FURNITURE_NAME_SET_BLOCK_L` | |
| `FURNITURE_NAME_SET_BLOCK_LAYINGL` | |
| `FURNITURE_NAME_SET_BLOCK_SIDEI` | |
| `FURNITURE_NAME_SET_BLOCK_SIDET` | |
| `FURNITURE_NAME_SET_BLOCK_SQUARE` | |
| `FURNITURE_NAME_SET_BLOCK_SQUARE2` | |
| `FURNITURE_NAME_SET_BLOCK_T` | |
| `FURNITURE_NAME_SET_BONE_CHAIR` | |
| `FURNITURE_NAME_SET_BONE_CHANDELIER` | |
| `FURNITURE_NAME_SET_BONE_COUCH` | |
| `FURNITURE_NAME_SET_BONE_LAMP` | |
| `FURNITURE_NAME_SET_BONE_PILE` | |
| `FURNITURE_NAME_SET_BONE_SHELF` | |
| `FURNITURE_NAME_SET_BONE_SIDETABLE` | |
| `FURNITURE_NAME_SET_BONE_SINK` | |
| `FURNITURE_NAME_SET_BONE_TABLE` | |
| `FURNITURE_NAME_SET_BONE_TV` | |
| `FURNITURE_NAME_SET_CAT_BED` | |
| `FURNITURE_NAME_SET_CAT_BENCH` | |
| `FURNITURE_NAME_SET_CAT_CHAIR` | |
| `FURNITURE_NAME_SET_CAT_COUCH` | |
| `FURNITURE_NAME_SET_CAT_DRESSER` | |
| `FURNITURE_NAME_SET_CAT_SHELF` | |
| `FURNITURE_NAME_SET_CAT_SUSPENDED_SHELF` | |
| `FURNITURE_NAME_SET_CAT_TABLE` | |
| `FURNITURE_NAME_SET_CAT_TABLE2` | |
| `FURNITURE_NAME_SET_CAT_TV` | |
| `FURNITURE_NAME_SET_CRYSTAL_CHAIR` | |
| `FURNITURE_NAME_SET_CRYSTAL_CHANDELIER` | |
| `FURNITURE_NAME_SET_CRYSTAL_COUCH` | |
| `FURNITURE_NAME_SET_CRYSTAL_DRESSER` | |
| `FURNITURE_NAME_SET_CRYSTAL_DRESSER2` | |
| `FURNITURE_NAME_SET_CRYSTAL_LAMP` | |
| `FURNITURE_NAME_SET_CRYSTAL_SHELF` | |
| `FURNITURE_NAME_SET_CRYSTAL_SIDETABLE` | |
| `FURNITURE_NAME_SET_CRYSTAL_TABLE` | |
| `FURNITURE_NAME_SET_CRYSTAL_TOILET` | |
| `FURNITURE_NAME_SET_CUTE_BED` | |
| `FURNITURE_NAME_SET_CUTE_CHAIR` | |
| `FURNITURE_NAME_SET_CUTE_COUCH` | |
| `FURNITURE_NAME_SET_CUTE_DRESSER` | |
| `FURNITURE_NAME_SET_CUTE_DRESSER2` | |
| `FURNITURE_NAME_SET_CUTE_SHELF` | |
| `FURNITURE_NAME_SET_CUTE_SIDETABLE` | |
| `FURNITURE_NAME_SET_CUTE_SIDETABLE2` | |
| `FURNITURE_NAME_SET_CUTE_STOOL` | |
| `FURNITURE_NAME_SET_CUTE_TABLE2` | |
| `FURNITURE_NAME_SET_ELEGANT_BED` | |
| `FURNITURE_NAME_SET_ELEGANT_CHAIR` | |
| `FURNITURE_NAME_SET_ELEGANT_DESK` | |
| `FURNITURE_NAME_SET_ELEGANT_DRESSER` | |
| `FURNITURE_NAME_SET_ELEGANT_DRESSER2` | |
| `FURNITURE_NAME_SET_ELEGANT_LAMP` | |
| `FURNITURE_NAME_SET_ELEGANT_SHELF` | |
| `FURNITURE_NAME_SET_ELEGANT_SIDETABLE` | |
| `FURNITURE_NAME_SET_ELEGANT_SIDETABLE2` | |
| `FURNITURE_NAME_SET_ELEGANT_TABLE` | |
| `FURNITURE_NAME_SET_GUTS_LAMP` | |
| `FURNITURE_NAME_SET_GUTS_LAMP2` | |
| `FURNITURE_NAME_SET_GUTS_SHELF` | |
| `FURNITURE_NAME_SET_GUTS_SIDETABLE` | |
| `FURNITURE_NAME_SET_GUTS_SIDETABLE2` | |
| `FURNITURE_NAME_SET_GUTS_SINK` | |
| `FURNITURE_NAME_SET_GUTS_SUSPENDEDSHELF` | |
| `FURNITURE_NAME_SET_GUTS_TABLE` | |
| `FURNITURE_NAME_SET_GUTS_TOILET` | |
| `FURNITURE_NAME_SET_GUTS_TV` | |
| `FURNITURE_NAME_SET_JUNK_BED` | |
| `FURNITURE_NAME_SET_JUNK_CABINET` | |
| `FURNITURE_NAME_SET_JUNK_CHAIR` | |
| `FURNITURE_NAME_SET_JUNK_DRESSER` | |
| `FURNITURE_NAME_SET_JUNK_LAMP` | |
| `FURNITURE_NAME_SET_JUNK_SHELF` | |
| `FURNITURE_NAME_SET_JUNK_SIDETABLE` | |
| `FURNITURE_NAME_SET_JUNK_SUSPENDEDSHELF` | |
| `FURNITURE_NAME_SET_JUNK_TOILET` | |
| `FURNITURE_NAME_SET_JUNK_TV` | |
| `FURNITURE_NAME_SET_MODERN_BED` | |
| `FURNITURE_NAME_SET_MODERN_CHAIR` | |
| `FURNITURE_NAME_SET_MODERN_COUCH` | |
| `FURNITURE_NAME_SET_MODERN_DESK` | |
| `FURNITURE_NAME_SET_MODERN_DRESSER` | |
| `FURNITURE_NAME_SET_MODERN_FRIGE` | |
| `FURNITURE_NAME_SET_MODERN_SIDETABLE` | |
| `FURNITURE_NAME_SET_MODERN_STOVE` | |
| `FURNITURE_NAME_SET_MODERN_TABLE` | |
| `FURNITURE_NAME_SET_MODERN_TV` | |
| `FURNITURE_NAME_SET_MONSTER_CHAIR` | |
| `FURNITURE_NAME_SET_MONSTER_DRESSER` | |
| `FURNITURE_NAME_SET_MONSTER_LAMP` | |
| `FURNITURE_NAME_SET_MONSTER_SHELF` | |
| `FURNITURE_NAME_SET_MONSTER_SIDETABLE` | |
| `FURNITURE_NAME_SET_MONSTER_SUSPENDEDSHELF` | |
| `FURNITURE_NAME_SET_MONSTER_SUSPENDEDSHELF2` | |
| `FURNITURE_NAME_SET_MONSTER_TABLE` | |
| `FURNITURE_NAME_SET_MONSTER_TABLE2` | |
| `FURNITURE_NAME_SET_MONSTER_TV` | |
| `FURNITURE_NAME_SET_MUSHROOM_CHAIR` | |
| `FURNITURE_NAME_SET_MUSHROOM_SHELF` | |
| `FURNITURE_NAME_SET_MUSHROOM_STOOL` | |
| `FURNITURE_NAME_SET_MUSHROOM_STOOL2` | |
| `FURNITURE_NAME_SET_MUSHROOM_STOOL3` | |
| `FURNITURE_NAME_SET_MUSHROOM_SUSPENDEDSHELF` | |
| `FURNITURE_NAME_SET_MUSHROOM_SUSPENDEDSHELF2` | |
| `FURNITURE_NAME_SET_MUSHROOM_TABLE` | |
| `FURNITURE_NAME_SET_MUSHROOM_TABLE1` | |
| `FURNITURE_NAME_SET_MUSHROOM_TOILET` | |
| `FURNITURE_NAME_SET_RETRO_BED` | |
| `FURNITURE_NAME_SET_RETRO_CHAIR` | |
| `FURNITURE_NAME_SET_RETRO_COUCH` | |
| `FURNITURE_NAME_SET_RETRO_DRESSER` | |
| `FURNITURE_NAME_SET_RETRO_DRESSER2` | |
| `FURNITURE_NAME_SET_RETRO_DRESSER3` | |
| `FURNITURE_NAME_SET_RETRO_FRIGE` | |
| `FURNITURE_NAME_SET_RETRO_LAMP` | |
| `FURNITURE_NAME_SET_RETRO_SIDETABLE` | |
| `FURNITURE_NAME_SET_RETRO_STOVE` | |
| `FURNITURE_NAME_SET_ROBO_DESK` | |
| `FURNITURE_NAME_SET_ROBO_DRESSER` | |
| `FURNITURE_NAME_SET_ROBO_HEAD` | |
| `FURNITURE_NAME_SET_ROBO_ROBOARMS` | |
| `FURNITURE_NAME_SET_ROBO_ROBOBODY` | |
| `FURNITURE_NAME_SET_ROBO_ROBOCHEST` | |
| `FURNITURE_NAME_SET_ROBO_SHELF` | |
| `FURNITURE_NAME_SET_ROBO_SINK` | |
| `FURNITURE_NAME_SET_ROBO_TABLE` | |
| `FURNITURE_NAME_SET_ROBO_TV` | |
| `FURNITURE_NAME_SET_RUSTIC_BENCH` | |
| `FURNITURE_NAME_SET_RUSTIC_CHAIR` | |
| `FURNITURE_NAME_SET_RUSTIC_DESK` | |
| `FURNITURE_NAME_SET_RUSTIC_DRESSER` | |
| `FURNITURE_NAME_SET_RUSTIC_SHELF` | |
| `FURNITURE_NAME_SET_RUSTIC_SIDETABLE` | |
| `FURNITURE_NAME_SET_RUSTIC_STOOL` | |
| `FURNITURE_NAME_SET_RUSTIC_SUSPENDEDSHELF` | |
| `FURNITURE_NAME_SET_RUSTIC_SUSPENDEDSHELF2` | |
| `FURNITURE_NAME_SET_RUSTIC_TABLE` | |
| `FURNITURE_NAME_SET_SEWER_CHAIR` | |
| `FURNITURE_NAME_SET_SEWER_DRESSER` | |
| `FURNITURE_NAME_SET_SEWER_LAMP` | |
| `FURNITURE_NAME_SET_SEWER_SHELF` | |
| `FURNITURE_NAME_SET_SEWER_SINK` | |
| `FURNITURE_NAME_SET_SEWER_SMALL_TABLE` | |
| `FURNITURE_NAME_SET_SEWER_STOOL` | |
| `FURNITURE_NAME_SET_SEWER_SUSPENDEDSHELF` | |
| `FURNITURE_NAME_SET_SEWER_TABLE` | |
| `FURNITURE_NAME_SET_SEWER_TV` | |
| `FURNITURE_NAME_SET_SEWN_CHAIR` | |
| `FURNITURE_NAME_SET_SEWN_COUCH` | |
| `FURNITURE_NAME_SET_SEWN_DOLL` | |
| `FURNITURE_NAME_SET_SEWN_DRESSER` | |
| `FURNITURE_NAME_SET_SEWN_SIDETABLE` | |
| `FURNITURE_NAME_SET_SEWN_STOOL1` | |
| `FURNITURE_NAME_SET_SEWN_STOOL2` | |
| `FURNITURE_NAME_SET_SEWN_TABLE` | |
| `FURNITURE_NAME_SET_SEWN_TOILET` | |
| `FURNITURE_NAME_SET_SEWN_TV` | |
| `FURNITURE_NAME_SET_SPIDER_BED` | |
| `FURNITURE_NAME_SET_SPIDER_CANDELABRA` | |
| `FURNITURE_NAME_SET_SPIDER_CHAIR` | |
| `FURNITURE_NAME_SET_SPIDER_DRESSER` | |
| `FURNITURE_NAME_SET_SPIDER_SHELF` | |
| `FURNITURE_NAME_SET_SPIDER_SIDETABLE` | |
| `FURNITURE_NAME_SET_SPIDER_TABLE` | |
| `FURNITURE_NAME_SET_SPIDER_TOILET` | |
| `FURNITURE_NAME_SET_SPIDER_TV` | |
| `FURNITURE_NAME_SET_SPIDER_VANITY` | |
| `FURNITURE_NAME_SET_WOODEN_CHAIR` | |
| `FURNITURE_NAME_SET_WOODEN_DRESSER` | |
| `FURNITURE_NAME_SET_WOODEN_LAMP` | |
| `FURNITURE_NAME_SET_WOODEN_SHELF` | |
| `FURNITURE_NAME_SET_WOODEN_SHELF2` | |
| `FURNITURE_NAME_SET_WOODEN_SINK` | |
| `FURNITURE_NAME_SET_WOODEN_SUSPENDEDSHELF` | |
| `FURNITURE_NAME_SET_WOODEN_TABLE` | |
| `FURNITURE_NAME_SET_WOODEN_TOILET` | |
| `FURNITURE_NAME_SET_WOODEN_TV` | |
| `FURNITURE_NAME_SMALL_90SPHONE` | |
| `FURNITURE_NAME_SMALL_90SPHONE2` | |
| `FURNITURE_NAME_SMALL_ALARMCLOCK1` | |
| `FURNITURE_NAME_SMALL_ALARMCLOCK2` | |
| `FURNITURE_NAME_SMALL_BED` | |
| `FURNITURE_NAME_SMALL_BELL` | |
| `FURNITURE_NAME_SMALL_BIGEGG` | |
| `FURNITURE_NAME_SMALL_BLACKBOX` | |
| `FURNITURE_NAME_SMALL_BOBBLE_ALONE` | |
| `FURNITURE_NAME_SMALL_BOBBLE_DAN` | |
| `FURNITURE_NAME_SMALL_BOBBLE_DARKCAT` | |
| `FURNITURE_NAME_SMALL_BOBBLE_DEVIL` | |
| `FURNITURE_NAME_SMALL_BOBBLE_GRUMP` | |
| `FURNITURE_NAME_SMALL_BOBBLE_GUPPY` | |
| `FURNITURE_NAME_SMALL_BOBBLE_HAPPY` | |
| `FURNITURE_NAME_SMALL_BOBBLE_MAD` | |
| `FURNITURE_NAME_SMALL_BOBBLE_MONEY` | |
| `FURNITURE_NAME_SMALL_BOBBLE_SPOTS` | |
| `FURNITURE_NAME_SMALL_BOBBLE_ZOMBIE` | |
| `FURNITURE_NAME_SMALL_BOTTLE_2BOTTLES` | |
| `FURNITURE_NAME_SMALL_BOTTLE_EMPTY` | |
| `FURNITURE_NAME_SMALL_BOTTLE_FULL` | |
| `FURNITURE_NAME_SMALL_BOWLINGBALL` | |
| `FURNITURE_NAME_SMALL_CANDLE_BLACK1` | |
| `FURNITURE_NAME_SMALL_CANDLE_BLACK2` | |
| `FURNITURE_NAME_SMALL_CANDLE_BLACK3` | |
| `FURNITURE_NAME_SMALL_CANDLE_BLACK4` | |
| `FURNITURE_NAME_SMALL_CANDLE_WHITE1` | |
| `FURNITURE_NAME_SMALL_CANDLE_WHITE2` | |
| `FURNITURE_NAME_SMALL_CANDLE_WHITE3` | |
| `FURNITURE_NAME_SMALL_CANDLE_WHITE4` | |
| `FURNITURE_NAME_SMALL_COUCH` | |
| `FURNITURE_NAME_SMALL_CRATE` | |
| `FURNITURE_NAME_SMALL_DEADRAT` | |
| `FURNITURE_NAME_SMALL_DOLL_AETHER` | |
| `FURNITURE_NAME_SMALL_DOLL_DUKE` | |
| `FURNITURE_NAME_SMALL_DOLL_GISH` | |
| `FURNITURE_NAME_SMALL_DOLL_GUPPY` | |
| `FURNITURE_NAME_SMALL_DOLL_ISAAC` | |
| `FURNITURE_NAME_SMALL_DOLL_STACY` | |
| `FURNITURE_NAME_SMALL_DOLL_STEVEN` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_BRAIN` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_CELLPHONE` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_DUCKPHONE` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_GAMEPAD` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_GAMESYSTEM` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_HANDRADIO` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_HANDRADIO2` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_JOYSTICK` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_LIPPHONE` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_MOON` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_MOUSE` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_MYSTERIOUSSKULL` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_OLDPHONE` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_OLDPHONE2` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_OLDPHONE3` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_OOZE` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_PHONE1` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_PHONE2` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_PHONE3` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_SPEAKER` | |
| `FURNITURE_NAME_SMALL_ELECTRONICS_WALKYTALKY` | |
| `FURNITURE_NAME_SMALL_EYEBALL` | |
| `FURNITURE_NAME_SMALL_FOOD_APPLE` | |
| `FURNITURE_NAME_SMALL_FOOD_BROCCOLI` | |
| `FURNITURE_NAME_SMALL_FOOD_CUPCAKE` | |
| `FURNITURE_NAME_SMALL_FOOD_CUPCAKE2` | |
| `FURNITURE_NAME_SMALL_FOOD_EGGPLANT` | |
| `FURNITURE_NAME_SMALL_FOOD_LEMON` | |
| `FURNITURE_NAME_SMALL_FOOD_ONION` | |
| `FURNITURE_NAME_SMALL_FOOD_ORANGE` | |
| `FURNITURE_NAME_SMALL_FOOD_PINEAPPLE` | |
| `FURNITURE_NAME_SMALL_FOOD_POTATO` | |
| `FURNITURE_NAME_SMALL_FOOD_PUMPKIN` | |
| `FURNITURE_NAME_SMALL_FOOD_RADISH` | |
| `FURNITURE_NAME_SMALL_FOOD_ROOT` | |
| `FURNITURE_NAME_SMALL_FOOD_SAUSAGE` | |
| `FURNITURE_NAME_SMALL_FOOD_SQUASH` | |
| `FURNITURE_NAME_SMALL_FRIGE` | |
| `FURNITURE_NAME_SMALL_GEM` | |
| `FURNITURE_NAME_SMALL_IRON` | |
| `FURNITURE_NAME_SMALL_JAR_COINS` | |
| `FURNITURE_NAME_SMALL_JAR_DISEASES` | |
| `FURNITURE_NAME_SMALL_JAR_EMPTY` | |
| `FURNITURE_NAME_SMALL_JAR_EMPTY2` | |
| `FURNITURE_NAME_SMALL_JAR_EMPTY3` | |
| `FURNITURE_NAME_SMALL_JAR_EYEBALLS` | |
| `FURNITURE_NAME_SMALL_JAR_FAIRY` | |
| `FURNITURE_NAME_SMALL_JAR_FISH` | |
| `FURNITURE_NAME_SMALL_JAR_FLYS` | |
| `FURNITURE_NAME_SMALL_JAR_GHOST` | |
| `FURNITURE_NAME_SMALL_JAR_HEART` | |
| `FURNITURE_NAME_SMALL_JAR_NAILS` | |
| `FURNITURE_NAME_SMALL_JAR_SPIDER` | |
| `FURNITURE_NAME_SMALL_JAR_TADPOLE` | |
| `FURNITURE_NAME_SMALL_JUG` | |
| `FURNITURE_NAME_SMALL_KETTLE` | |
| `FURNITURE_NAME_SMALL_KNOCKER` | |
| `FURNITURE_NAME_SMALL_LAB_FLASK` | |
| `FURNITURE_NAME_SMALL_LAB_FLASK2` | |
| `FURNITURE_NAME_SMALL_LAB_FLASK3` | |
| `FURNITURE_NAME_SMALL_LAB_FLASK4` | |
| `FURNITURE_NAME_SMALL_LAB_JUG1` | |
| `FURNITURE_NAME_SMALL_LAB_JUG2` | |
| `FURNITURE_NAME_SMALL_LAB_JUG3` | |
| `FURNITURE_NAME_SMALL_LAB_TANK1` | |
| `FURNITURE_NAME_SMALL_LAB_TANK2` | |
| `FURNITURE_NAME_SMALL_LAB_TESTTUBE` | |
| `FURNITURE_NAME_SMALL_LAB_TESTTUBE2` | |
| `FURNITURE_NAME_SMALL_LETTERBLOCK1` | |
| `FURNITURE_NAME_SMALL_LETTERBLOCK2` | |
| `FURNITURE_NAME_SMALL_LETTERBLOCK3` | |
| `FURNITURE_NAME_SMALL_LETTERBLOCK4` | |
| `FURNITURE_NAME_SMALL_LETTERBLOCK5` | |
| `FURNITURE_NAME_SMALL_LETTERBLOCK6` | |
| `FURNITURE_NAME_SMALL_LETTERBLOCK7` | |
| `FURNITURE_NAME_SMALL_LETTERBLOCK8` | |
| `FURNITURE_NAME_SMALL_LOTION` | |
| `FURNITURE_NAME_SMALL_MEDS_CATHEARTS` | |
| `FURNITURE_NAME_SMALL_MEDS_COUGHSYRUP` | |
| `FURNITURE_NAME_SMALL_MEDS_FISHOIL` | |
| `FURNITURE_NAME_SMALL_MEDS_MYSTERY2` | |
| `FURNITURE_NAME_SMALL_MEDS_MYSTERYBOTTLE` | |
| `FURNITURE_NAME_SMALL_MEDS_PILLS1` | |
| `FURNITURE_NAME_SMALL_MEDS_PILLS2` | |
| `FURNITURE_NAME_SMALL_MILK` | |
| `FURNITURE_NAME_SMALL_MUG` | |
| `FURNITURE_NAME_SMALL_MUG2` | |
| `FURNITURE_NAME_SMALL_PENCUP` | |
| `FURNITURE_NAME_SMALL_PERFUME` | |
| `FURNITURE_NAME_SMALL_PICTURE_CAN` | |
| `FURNITURE_NAME_SMALL_PICTURE_CAT` | |
| `FURNITURE_NAME_SMALL_PICTURE_SPOON` | |
| `FURNITURE_NAME_SMALL_PIGGYBANK` | |
| `FURNITURE_NAME_SMALL_PILLBOTTLE` | |
| `FURNITURE_NAME_SMALL_PIN` | |
| `FURNITURE_NAME_SMALL_RUBBERDUCK` | |
| `FURNITURE_NAME_SMALL_SHELF` | |
| `FURNITURE_NAME_SMALL_SHELL` | |
| `FURNITURE_NAME_SMALL_SIDETABLE` | |
| `FURNITURE_NAME_SMALL_SINK` | |
| `FURNITURE_NAME_SMALL_SNOWGLOBE` | |
| `FURNITURE_NAME_SMALL_STOVE` | |
| `FURNITURE_NAME_SMALL_TISSUES` | |
| `FURNITURE_NAME_SMALL_TRASH_APPLE` | |
| `FURNITURE_NAME_SMALL_TRASH_BANANA` | |
| `FURNITURE_NAME_SMALL_TRASH_BONE` | |
| `FURNITURE_NAME_SMALL_TRASH_BREAD` | |
| `FURNITURE_NAME_SMALL_TRASH_BROKENBOTTLE` | |
| `FURNITURE_NAME_SMALL_TRASH_CAN2` | |
| `FURNITURE_NAME_SMALL_TRASH_CANS` | |
| `FURNITURE_NAME_SMALL_TRASH_CHEESE` | |
| `FURNITURE_NAME_SMALL_TRASH_CUP` | |
| `FURNITURE_NAME_SMALL_TRASH_EGGS` | |
| `FURNITURE_NAME_SMALL_TRASH_MILK` | |
| `FURNITURE_NAME_SMALL_VASE1` | |
| `FURNITURE_NAME_SMALL_VASE2` | |
| `FURNITURE_NAME_SMALL_VASE3` | |
| `FURNITURE_NAME_SMALL_WATERBOTTLE` | |
| `FURNITURE_NAME_SMALL_WOBBLEBIRD` | |
| `FURNITURE_NAME_SPECIAL_APPEALIDOL` | |
| `FURNITURE_NAME_SPECIAL_COMFORTIDOL` | |
| `FURNITURE_NAME_SPECIAL_EVOLUTIONIDOL` | |
| `FURNITURE_NAME_SPECIAL_FIGHTIDOL` | |
| `FURNITURE_NAME_SPECIAL_FOODBOX` | |
| `FURNITURE_NAME_SPECIAL_HEALTHIDOL` | |
| `FURNITURE_NAME_SPECIAL_STIMULATIONIDOL` | |
| `FURNITURE_NAME_SPECIAL_SUPPRESSORIDOL` | |
| `FURNITURE_NAME_WALLMOUNTED_ATOMIC_CLOCK` | |
| `FURNITURE_NAME_WALLMOUNTED_BALLOON` | |
| `FURNITURE_NAME_WALLMOUNTED_BALLOON2` | |
| `FURNITURE_NAME_WALLMOUNTED_BALLOON3` | |
| `FURNITURE_NAME_WALLMOUNTED_BALLOON4` | |
| `FURNITURE_NAME_WALLMOUNTED_BALLOON5` | |
| `FURNITURE_NAME_WALLMOUNTED_BALLOON6` | |
| `FURNITURE_NAME_WALLMOUNTED_BALLOON7` | |
| `FURNITURE_NAME_WALLMOUNTED_BLOCK1` | |
| `FURNITURE_NAME_WALLMOUNTED_BLOCK2` | |
| `FURNITURE_NAME_WALLMOUNTED_BLOCK3` | |
| `FURNITURE_NAME_WALLMOUNTED_BRICKS1` | |
| `FURNITURE_NAME_WALLMOUNTED_BRICKS2` | |
| `FURNITURE_NAME_WALLMOUNTED_BRICKS3` | |
| `FURNITURE_NAME_WALLMOUNTED_BRICKS4` | |
| `FURNITURE_NAME_WALLMOUNTED_CLOCK` | |
| `FURNITURE_NAME_WALLMOUNTED_CLOUD` | |
| `FURNITURE_NAME_WALLMOUNTED_COWSKULL` | |
| `FURNITURE_NAME_WALLMOUNTED_CRACK` | |
| `FURNITURE_NAME_WALLMOUNTED_FURNACE` | |
| `FURNITURE_NAME_WALLMOUNTED_GHOST1` | |
| `FURNITURE_NAME_WALLMOUNTED_GHOST2` | |
| `FURNITURE_NAME_WALLMOUNTED_GHOST3` | |
| `FURNITURE_NAME_WALLMOUNTED_JOLLYROGER` | |
| `FURNITURE_NAME_WALLMOUNTED_JUNK_PAPER1` | |
| `FURNITURE_NAME_WALLMOUNTED_JUNK_PAPER2` | |
| `FURNITURE_NAME_WALLMOUNTED_MASK_BUNNY` | |
| `FURNITURE_NAME_WALLMOUNTED_MASK_HOCKY` | |
| `FURNITURE_NAME_WALLMOUNTED_MASK_INFAMY` | |
| `FURNITURE_NAME_WALLMOUNTED_MASK_TONETTA` | |
| `FURNITURE_NAME_WALLMOUNTED_MIRROR` | |
| `FURNITURE_NAME_WALLMOUNTED_OUTLET` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_BLUEBOY` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_CHE` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_DRAWING` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_ERASER` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_FRIDA` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_GOD` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_GOTHIC` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_HANG` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_JAWS` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_KEITH` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_LAMBS` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_LISA` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_MAGAZINE` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_NIGHT` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_OBEY` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_ORANGE` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_PEARL` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_PHOTO` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_PHOTO2` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_PHOTO3` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_PICASSO` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_POEM` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_ROSIE` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_SAILBOAT` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_SCARFACE` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_SCREAM` | |
| `FURNITURE_NAME_WALLMOUNTED_PICTURE_UFO` | |
| `FURNITURE_NAME_WALLMOUNTED_ROBO_PLATE1` | |
| `FURNITURE_NAME_WALLMOUNTED_ROBO_PLATE2` | |
| `FURNITURE_NAME_WALLMOUNTED_ROBO_PLATE3` | |
| `FURNITURE_NAME_WALLMOUNTED_ROBO_PLATE4` | |
| `FURNITURE_NAME_WALLMOUNTED_SAFE` | |
| `FURNITURE_NAME_WALLMOUNTED_SEWER_PIPES1` | |
| `FURNITURE_NAME_WALLMOUNTED_SEWER_PIPES2` | |
| `FURNITURE_NAME_WALLMOUNTED_SEWER_PIPES3` | |
| `FURNITURE_NAME_WALLMOUNTED_SEWN_CLOCK` | |
| `FURNITURE_NAME_WALLMOUNTED_SHRUNKINHEAD` | |
| `FURNITURE_NAME_WALLMOUNTED_SWITCH` | |
| `FURNITURE_NAME_WALLMOUNTED_TAXIDERMY_BUGS` | |
| `FURNITURE_NAME_WALLMOUNTED_TAXIDERMY_DEERHEAD` | |
| `FURNITURE_NAME_WALLMOUNTED_TAXIDERMY_FISH` | |
| `FURNITURE_NAME_WALLMOUNTED_TAXIDERMY_GUPPY` | |
| `FURNITURE_NAME_WALLMOUNTED_TORCH` | |
| `FURNITURE_NAME_WALLMOUNTED_TV` | |
| `FURNITURE_NAME_WALLMOUNTED_WOODEN_BOARDS1` | |
| `FURNITURE_NAME_WALLMOUNTED_WOODEN_BOARDS2` | |
| `FURNITURE_NAME_WALLMOUNTED_WOODEN_BOARDS3` | |
| `FURNITURE_NAME_WALLMOUNTED_WOODEN_BOARDS4` | |
| `FURNITURE_NAME_WALLMOUNTED_WOODEN_CLOCK` | |

</details>


---

### Enum: `ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AutocastEachRound`](./Abilities_and_Spells.md#context-autocasteachround), [`BackflipWhenTargeted`](./Abilities_and_Spells.md#context-backflipwhentargeted), [`BodyGuard`](./Abilities_and_Spells.md#context-bodyguard), [`ChanceToBreakFree`](./Abilities_and_Spells.md#context-chancetobreakfree), [`ConjureBonusAbility`](./Abilities_and_Spells.md#context-conjurebonusability), [`DelayCastAbility`](./Abilities_and_Spells.md#context-delaycastability), [`ForceImmediateMoveAndAttack`](./Abilities_and_Spells.md#context-forceimmediatemoveandattack), [`ForceMoveTowardsTaggedObject`](./Abilities_and_Spells.md#context-forcemovetowardstaggedobject), [`ReplaceSpell`](./Abilities_and_Spells.md#context-replacespell), [`TeamCastAbility`](./Abilities_and_Spells.md#context-teamcastability), [`UseAbility`](./Abilities_and_Spells.md#context-useability), [`UseMoveAbilityWithAI`](./Abilities_and_Spells.md#context-usemoveabilitywithai), [`AbilityWhenTaggedCharacterMovesNear`](./Cat_Mutations.md#context-abilitywhentaggedcharactermovesnear), [`BackflipWhenTargeted`](./Cat_Mutations.md#context-backflipwhentargeted), [`ChanceToBackflip`](./Cat_Mutations.md#context-chancetobackflip), [`CounterAttack`](./Cat_Mutations.md#context-counterattack), [`AbilityHealthThreshold`](./Characters_and_Bosses.md#context-abilityhealththreshold), [`AbilityOnRoundEnd`](./Characters_and_Bosses.md#context-abilityonroundend), [`AbilityReaction`](./Characters_and_Bosses.md#context-abilityreaction), [`AbilityWhenTaggedCharacterMovesNear`](./Characters_and_Bosses.md#context-abilitywhentaggedcharactermovesnear), [`AutocastEachRound`](./Characters_and_Bosses.md#context-autocasteachround), [`BackflipWhenTargeted`](./Characters_and_Bosses.md#context-backflipwhentargeted), [`BungaEntrance`](./Characters_and_Bosses.md#context-bungaentrance), [`CaveFamilyEnrage`](./Characters_and_Bosses.md#context-cavefamilyenrage), [`CerberubsJumpBlind`](./Characters_and_Bosses.md#context-cerberubsjumpblind), [`CerberubsJumpNormal`](./Characters_and_Bosses.md#context-cerberubsjumpnormal), [`ChanceToBackflip`](./Characters_and_Bosses.md#context-chancetobackflip), [`ChanceToSpitOnDamage`](./Characters_and_Bosses.md#context-chancetospitondamage), [`ChaosHeadDropIn`](./Characters_and_Bosses.md#context-chaosheaddropin), [`CloseConvert`](./Characters_and_Bosses.md#context-closeconvert), [`CounterAttack`](./Characters_and_Bosses.md#context-counterattack), [`DashRandomly`](./Characters_and_Bosses.md#context-dashrandomly), [`DeathRattle`](./Characters_and_Bosses.md#context-deathrattle), [`DeathRattleRevive`](./Characters_and_Bosses.md#context-deathrattlerevive), [`DodgeWhenTargeted`](./Characters_and_Bosses.md#context-dodgewhentargeted), [`Escape`](./Characters_and_Bosses.md#context-escape), [`FoodMove`](./Characters_and_Bosses.md#context-foodmove), [`ForceTrample`](./Characters_and_Bosses.md#context-forcetrample), [`ForceUseAbility`](./Characters_and_Bosses.md#context-forceuseability), [`HitlerExecute`](./Characters_and_Bosses.md#context-hitlerexecute), [`ImmediateAbilityReaction`](./Characters_and_Bosses.md#context-immediateabilityreaction), [`LeapClose`](./Characters_and_Bosses.md#context-leapclose), [`MoveAway`](./Characters_and_Bosses.md#context-moveaway), [`MoveCenter`](./Characters_and_Bosses.md#context-movecenter), [`MoveClose`](./Characters_and_Bosses.md#context-moveclose), [`MoveForBarrage`](./Characters_and_Bosses.md#context-moveforbarrage), [`MoveForDash`](./Characters_and_Bosses.md#context-movefordash), [`MoveForGrass`](./Characters_and_Bosses.md#context-moveforgrass), [`MoveForPounce`](./Characters_and_Bosses.md#context-moveforpounce), [`MoveForSpin`](./Characters_and_Bosses.md#context-moveforspin), [`MoveForThrow`](./Characters_and_Bosses.md#context-moveforthrow), [`MoveOneForPuke`](./Characters_and_Bosses.md#context-moveoneforpuke), [`MoveSpaced`](./Characters_and_Bosses.md#context-movespaced), [`MoveToHead`](./Characters_and_Bosses.md#context-movetohead), [`MoveTowards`](./Characters_and_Bosses.md#context-movetowards), [`MoveTowardsDamageSource`](./Characters_and_Bosses.md#context-movetowardsdamagesource), [`MovementReaction`](./Characters_and_Bosses.md#context-movementreaction), [`NCGravecrawlFAR`](./Characters_and_Bosses.md#context-ncgravecrawlfar), [`ProtectTargetedAllies`](./Characters_and_Bosses.md#context-protecttargetedallies), [`ReturnA`](./Characters_and_Bosses.md#context-returna), [`RunFar`](./Characters_and_Bosses.md#context-runfar), [`SecurityBotProtect`](./Characters_and_Bosses.md#context-securitybotprotect), [`SpearRun`](./Characters_and_Bosses.md#context-spearrun), [`SuckMF`](./Characters_and_Bosses.md#context-suckmf), [`SupportFormChangeInsteadOfRun`](./Characters_and_Bosses.md#context-supportformchangeinsteadofrun), [`TF_TargetAllies`](./Characters_and_Bosses.md#context-tf_targetallies), [`TF_TargetEnemies`](./Characters_and_Bosses.md#context-tf_targetenemies), [`TerminatorChase`](./Characters_and_Bosses.md#context-terminatorchase), [`Trapper`](./Characters_and_Bosses.md#context-trapper), [`Unflip`](./Characters_and_Bosses.md#context-unflip), [`UnlimitedDeathRattleRevive`](./Characters_and_Bosses.md#context-unlimiteddeathrattlerevive), [`UseAbility`](./Characters_and_Bosses.md#context-useability), [`UseAbilityWhenOutOfStatus`](./Characters_and_Bosses.md#context-useabilitywhenoutofstatus), [`AbilityHealthThreshold`](./Items_and_Equipment.md#context-abilityhealththreshold), [`AbilityOnRoundEndOnce`](./Items_and_Equipment.md#context-abilityonroundendonce), [`AutocastEachRound`](./Items_and_Equipment.md#context-autocasteachround), [`BackflipWhenTargeted`](./Items_and_Equipment.md#context-backflipwhentargeted), [`ChanceToBackflip`](./Items_and_Equipment.md#context-chancetobackflip), [`CounterAttack`](./Items_and_Equipment.md#context-counterattack), [`DeathRattle`](./Items_and_Equipment.md#context-deathrattle), [`ForceUseAbilityOnTarget`](./Items_and_Equipment.md#context-forceuseabilityontarget), [`ImmediateUseAbility`](./Items_and_Equipment.md#context-immediateuseability), [`MovementReaction`](./Items_and_Equipment.md#context-movementreaction), [`ROOT`](./Items_and_Equipment.md#context-root), [`AbilityReaction`](./Passives_and_Statuses.md#context-abilityreaction), [`AbilityWhenTaggedCharacterMovesNear`](./Passives_and_Statuses.md#context-abilitywhentaggedcharactermovesnear), [`AllyBonusAbilityAura`](./Passives_and_Statuses.md#context-allybonusabilityaura), [`AutocastEachRound`](./Passives_and_Statuses.md#context-autocasteachround), [`AutocastEachTurnBegin`](./Passives_and_Statuses.md#context-autocasteachturnbegin), [`CatAPultAnimation`](./Passives_and_Statuses.md#context-catapultanimation), [`ChanceToBackflip`](./Passives_and_Statuses.md#context-chancetobackflip), [`DamageIfDidntUseSpecificAbility`](./Passives_and_Statuses.md#context-damageifdidntusespecificability), [`DeathRattle`](./Passives_and_Statuses.md#context-deathrattle), [`ForceUseAbility`](./Passives_and_Statuses.md#context-forceuseability), [`MovementReaction`](./Passives_and_Statuses.md#context-movementreaction), [`SecurityBotProtect`](./Passives_and_Statuses.md#context-securitybotprotect)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `move` | |
| `attack` | |
| `BackflipDodge` | |
| `None` | |
| `cm_Heal` | |
| `BlinkDodge` | |
| `CaveCatEnrageOne` | |
| `CaveCatEnrageTwo` | |
| `SpewerSpit` | |
| `XXX` | |
| `ZaratanaVSRevenge` | |
| `cm_Catnip` | |
| `weapon` | |
| `wp_MeatHookB` | |
| `CaveManSpearRun` | |
| `CerberubsJump` | |
| `DestroyerRaise` | |
| `DybbukEscape` | |
| `HitlerPulp1` | |
| `MoonHandDrop` | |
| `MoveTwo` | |
| `PteroEscape` | |
| `PyrophinaVSRun` | |
| `ShadowstepDodge` | |
| `ShamblerDash` | |
| `SwapPositions_TankCat` | |
| `TinaSpit` | |
| `TinaSpit2` | |
| `TwistingFlames` | |
| `tk_EstusFlask` | |
| `tk_WaterBottle_Half` | |
| `wp_BearTraps` | |
| `wp_BucketOfLard` | |
| `wp_ChumBucket` | |
| `wp_GnarledClaw` | |
| `wp_NuclearKnife` | |
| `wp_OddRemote` | |
| `wp_RailSpikes` | |
| `wp_SleepDart` | |
| `wp_SmallBomb` | |
| `wp_SpiderWebber` | |
| `wp_Stick` | |
| `AZ_LoseHead` | |
| `AlienBeam` | |
| `AlienBeastGoop` | |
| `AlienBeastMoveOne` | |
| `BBPullBomb` | |
| `BecomeTheDestroyer` | |
| `BirthwortTrample` | |
| `BloatLoseFirstEye` | |
| `BloatLoseSecondEye` | |
| `BloatSideLaser` | |
| `BodyGuardSwap` | |
| `BodyGuardSwap2` | |
| `Bowl` | |
| `Bowl2` | |
| `BoyDinoHeadBash` | |
| `BungaEntrance` | |
| `ButtFlip` | |
| `ButtWeb` | |
| `ButtWeb_AlreadyEnraged` | |
| `CBShoot_ZodiacStyle` | |
| `CHuskDrop` | |
| `CatapultJump` | |
| `CatapultJump2` | |
| `CaveBabyFoodMove` | |
| `CaveBabyGrow` | |
| `CaveWomanDrop` | |
| `ChainLightning` | |
| `ChaosSpawnIn` | |
| `CherubDoom` | |
| `Class` | |
| `CollectiveCounterImpl` | |
| `CollectiveSpinImpl` | |
| `Colorless` | |
| `CrohnsPoop` | |
| `Dash_BabyDeathWorm` | |
| `Destroyer2HolyAttack` | |
| `Destroyer2Pulse` | |
| `DestroyerDodge` | |
| `DestroyerPulse` | |
| `DoubleDistanceMove` | |
| `DybbukBackflipDodge` | |
| `DybbukPossess` | |
| `DysenteryPoop` | |
| `ExtraMove` | |
| `FetusAirstrike` | |
| `FetusAirstrikeTrigger` | |
| `FetusJarDeath` | |
| `FetusPullBomb` | |
| `FormShrinkFour` | |
| `FormShrinkOne` | |
| `FormShrinkOneSnakey` | |
| `FormShrinkThree` | |
| `FormShrinkTwo` | |
| `FormShrinkTwoSnakey` | |
| `G3CallForHelp` | |
| `G3GrabHead` | |
| `G3RunToHead` | |
| `G3SpawnMama` | |
| `GKLeap` | |
| `GirlDinoHeadBash` | |
| `Groom` | |
| `Guillotina1Rage` | |
| `HangerBotLeave` | |
| `HangerBotReturn` | |
| `HellHandGrab` | |
| `HitlerPulp2` | |
| `HitlerPulp3` | |
| `HitlerPulp4` | |
| `HitlerPulp5` | |
| `HitlerPulp6` | |
| `HitlerShoot` | |
| `HitlerSuicide` | |
| `JarHeadDeath` | |
| `LEPortFar` | |
| `LabPillarDrop` | |
| `LastGasp` | |
| `LastGasp2` | |
| `LennyDrop` | |
| `MD_Lift` | |
| `MM_Guard` | |
| `MarshmallowConvert` | |
| `MedicObey` | |
| `MedicObey2` | |
| `MiniNukeExplodey` | |
| `MoonHandDash` | |
| `MoonHandDrop_Deathrattle` | |
| `MoonHandGrab` | |
| `MoonHeadCommandStopHittingYourself` | |
| `MoonHead_EatCat` | |
| `MoonHead_SpitCat` | |
| `MoveOneTrample` | |
| `MoveTwoCantrip` | |
| `MoveTwoTrample` | |
| `NCGravecrawl` | |
| `NubsCatJumpReaction` | |
| `PoxScratch` | |
| `QueenHippoHeartAttack` | |
| `RaiseTheDead` | |
| `RaiseTheDead2` | |
| `RatKingTransform` | |
| `RattleSnakeTrap` | |
| `RubberFistBotPunch` | |
| `SBotAnger` | |
| `SZBBackflipDodge` | |
| `SZBShoot` | |
| `SharpenNail2` | |
| `SlagSpawn` | |
| `SpontaneouslyCombust` | |
| `StegoGrassStomp` | |
| `StegoTailSwipe` | |
| `T1ChokeReaction` | |
| `T3Pebbles_BoulderDrop` | |
| `TVChangeDie` | |
| `Teleport` | |
| `TeleportFlipUp` | |
| `TheChild_Pulse` | |
| `TheChild_Wrath` | |
| `TheCreator_Reaction` | |
| `TigerForm` | |
| `TormentorSuck` | |
| `Transcend2` | |
| `TumorPrisonDeathrattle` | |
| `UFO_SpelunkyDeath` | |
| `YA_Laser` | |
| `ZodiacShoot` | |
| `ZodiacShootX` | |
| `ZombieTombstone` | |
| `cm_AllStatsBuff` | |
| `cm_Antidote` | |
| `cm_BigToe` | |
| `cm_Bullseye` | |
| `cm_ButcherSeal` | |
| `cm_ChaBuff` | |
| `cm_ClericSeal` | |
| `cm_ColorlessSeal` | |
| `cm_DexBuff` | |
| `cm_DruidSeal` | |
| `cm_EatHummingbird` | |
| `cm_Enema` | |
| `cm_ExperimentX` | |
| `cm_FighterSeal` | |
| `cm_ForbiddenFruit` | |
| `cm_ForbiddenPill` | |
| `cm_Gizzard` | |
| `cm_HealPercent` | |
| `cm_HealPercent_Auto` | |
| `cm_HunterSeal` | |
| `cm_IntBuff` | |
| `cm_JarOfChaos` | |
| `cm_JesterSeal` | |
| `cm_JokerCard` | |
| `cm_Kidney` | |
| `cm_KiloOfCatnip` | |
| `cm_Lard` | |
| `cm_LckBuff` | |
| `cm_MageSeal` | |
| `cm_MetalCoat` | |
| `cm_MonkSeal` | |
| `cm_NecromancerSeal` | |
| `cm_Nipple` | |
| `cm_PCP` | |
| `cm_Pearl` | |
| `cm_PsychicSeal` | |
| `cm_RaptorEgg` | |
| `cm_RedPill` | |
| `cm_RottenMeat` | |
| `cm_Shield` | |
| `cm_ShoePolish` | |
| `cm_SmellingSalts` | |
| `cm_SpdBuff` | |
| `cm_Star` | |
| `cm_StemCells` | |
| `cm_Steven1` | |
| `cm_Steven2` | |
| `cm_StrBuff` | |
| `cm_SuperBandage` | |
| `cm_TankSeal` | |
| `cm_TheD6` | |
| `cm_ThiefSeal` | |
| `cm_TinkererSeal` | |
| `cm_UnstableDNA` | |
| `cm_ViperBottle` | |
| `cm_WishBone` | |
| `cm_WitchsEye` | |
| `face_StevenMask2` | |
| `head_IronJaw` | |
| `head_MiniMoonArmorAsteroid` | |
| `neck_TentacleArmorCounter` | |
| `set_HumanFleshSetCurse` | |
| `set_MummySetCurse` | |
| `set_PlanetSetGravity` | |
| `tk_BagOfBags` | |
| `tk_BagOfSeeds` | |
| `tk_Bishop` | |
| `tk_BloodyCoin` | |
| `tk_BloodyRazor` | |
| `tk_ButterBean` | |
| `tk_CambionConception` | |
| `tk_CarvingKnife` | |
| `tk_CatONineTails` | |
| `tk_CounterfeitCoin` | |
| `tk_DruidsWhistle` | |
| `tk_EggSack` | |
| `tk_ElectricCoin` | |
| `tk_EmptyHand` | |
| `tk_Fireworks` | |
| `tk_FriendshipBracelet` | |
| `tk_Glitch` | |
| `tk_GlowingCoin` | |
| `tk_Glue` | |
| `tk_GorgonsEye` | |
| `tk_GreenDrink` | |
| `tk_HolyWater` | |
| `tk_HotLunch` | |
| `tk_HuntersFlute` | |
| `tk_Knight` | |
| `tk_LegWhistle` | |
| `tk_LilBattery` | |
| `tk_LunchBox` | |
| `tk_Metronome` | |
| `tk_MonkStyleChange` | |
| `tk_MyShadow` | |
| `tk_Pawn` | |
| `tk_Pentagram` | |
| `tk_PurpleDrink` | |
| `tk_Queen` | |
| `tk_RageJuice` | |
| `tk_RazorBlade` | |
| `tk_RedDrink` | |
| `tk_Reset` | |
| `tk_Rook` | |
| `tk_SackOfMeat` | |
| `tk_SoulJar` | |
| `tk_SpawnTheLost` | |
| `tk_SpellBook` | |
| `tk_Steroids` | |
| `tk_TankJuice` | |
| `tk_TarotDeck` | |
| `tk_Technology` | |
| `tk_Teleport` | |
| `tk_TheBlackBox` | |
| `tk_WaterBottle_Empty` | |
| `tk_WaterBottle_Full` | |
| `tk_Whistle` | |
| `tr_SelfDestruct` | |
| `wp_22Rifle` | |
| `wp_AirHorn` | |
| `wp_AirHornFixed` | |
| `wp_AlienBlaster` | |
| `wp_AnarchistCookbook` | |
| `wp_AnointingOil` | |
| `wp_AstroTaser` | |
| `wp_BagOfGlass` | |
| `wp_BagOfGlitter` | |
| `wp_BagOfMeat` | |
| `wp_BagOfRocks` | |
| `wp_BagOfStuff` | |
| `wp_BallPeenHammer` | |
| `wp_BangGun` | |
| `wp_BarbedPaw` | |
| `wp_Battery` | |
| `wp_BattleAxe` | |
| `wp_BentSpoon` | |
| `wp_Bible` | |
| `wp_BigSpring` | |
| `wp_BigStick` | |
| `wp_BiggestStick` | |
| `wp_BlackMushroom` | |
| `wp_BlackShard` | |
| `wp_BlackShard_Glowing` | |
| `wp_Blackjack` | |
| `wp_Blackjack_Auto` | |
| `wp_BlessedAnointingOil` | |
| `wp_BloodBottles` | |
| `wp_BloodyBagOfGlass` | |
| `wp_BloodyButterflyKnife` | |
| `wp_BloodyMeatHook` | |
| `wp_BloodySoulClaw` | |
| `wp_Bo` | |
| `wp_Bomb` | |
| `wp_BoneClub` | |
| `wp_BookofBelial` | |
| `wp_Bottles` | |
| `wp_Bricks` | |
| `wp_BubbleBoyFixed` | |
| `wp_BucketOfAcid` | |
| `wp_BungaClub` | |
| `wp_BurningCoal` | |
| `wp_ButchersCleaver` | |
| `wp_ButterflyKnife` | |
| `wp_CarBattery` | |
| `wp_CatPaw` | |
| `wp_CaveCatClub` | |
| `wp_Chainsaw` | |
| `wp_Cheese` | |
| `wp_ChumShot` | |
| `wp_CreepyPhoto` | |
| `wp_CrispPaper` | |
| `wp_Crossbow` | |
| `wp_Crowbar` | |
| `wp_Deathbot` | |
| `wp_DeathsScythe` | |
| `wp_DemonDoom` | |
| `wp_DryIce` | |
| `wp_EnergyDrink` | |
| `wp_EtherSoakedRag` | |
| `wp_ExtraLimb` | |
| `wp_Fate` | |
| `wp_FeatherDarts` | |
| `wp_FeatheredWing` | |
| `wp_FingerBone` | |
| `wp_FireFlower` | |
| `wp_FlowerMix` | |
| `wp_FreyedWires` | |
| `wp_FuryArm` | |
| `wp_GambitsDice` | |
| `wp_Garbage` | |
| `wp_Geode` | |
| `wp_Girder` | |
| `wp_GlassCannon` | |
| `wp_GlassCannonFixed` | |
| `wp_GlassShard` | |
| `wp_GoldPickaxe` | |
| `wp_GrapplingHook` | |
| `wp_Grenade` | |
| `wp_GripTrainer` | |
| `wp_GunslingerPistol` | |
| `wp_HairSpray` | |
| `wp_HarpyClaw` | |
| `wp_HeavyMace` | |
| `wp_HolyGrail` | |
| `wp_Hose` | |
| `wp_IceCubes` | |
| `wp_InfinityArrow` | |
| `wp_IrradiatedObject` | |
| `wp_IrradiatedObject_Bleed` | |
| `wp_IrradiatedObject_Bruise` | |
| `wp_IrradiatedObject_Burn` | |
| `wp_IrradiatedObject_Charmed` | |
| `wp_IrradiatedObject_Confusion` | |
| `wp_IrradiatedObject_Fear` | |
| `wp_IrradiatedObject_Poison` | |
| `wp_IrradiatedObject_Sleep` | |
| `wp_IrradiatedObject_Stun` | |
| `wp_IrradiatedObject_Weakness` | |
| `wp_Jitte` | |
| `wp_Kandarian` | |
| `wp_Kebab` | |
| `wp_LacedNeedle` | |
| `wp_Lighter` | |
| `wp_LilKitty` | |
| `wp_LilSlugger` | |
| `wp_LipFiller` | |
| `wp_Log` | |
| `wp_Lugar` | |
| `wp_Manhole` | |
| `wp_MeatCleaver` | |
| `wp_MeatHook` | |
| `wp_MeatSlugger` | |
| `wp_MegaAlienBlaster` | |
| `wp_MelonBaller` | |
| `wp_MetalRod` | |
| `wp_MiniJetpack` | |
| `wp_MiniNuke` | |
| `wp_Mjolnir` | |
| `wp_ModelingClay` | |
| `wp_Molars` | |
| `wp_MomsKnife` | |
| `wp_MomsToeNail` | |
| `wp_MoneyBag_Huge` | |
| `wp_MoneyBag_Large` | |
| `wp_MoneyBag_Medium` | |
| `wp_MoneyBag_Small` | |
| `wp_MysteriousBone` | |
| `wp_NailBoard` | |
| `wp_NailGun` | |
| `wp_NecroSoulDagger` | |
| `wp_NecroSoulDaggerCharged` | |
| `wp_Necronomicon` | |
| `wp_NuclearKnifeExplode` | |
| `wp_NuclearKnifeFixed` | |
| `wp_ObsidianChunk` | |
| `wp_Ocarina` | |
| `wp_OddRemoteEnemy` | |
| `wp_OldExtinguisher` | |
| `wp_PartyDetonator` | |
| `wp_PartyDetonatorFixed` | |
| `wp_PersuasionDevice` | |
| `wp_PharaohStaff` | |
| `wp_Pickaxe` | |
| `wp_Pinwheel` | |
| `wp_Pipe` | |
| `wp_Pliers` | |
| `wp_PogoStick` | |
| `wp_PoisonVial` | |
| `wp_PolymorphRemote` | |
| `wp_PopCap` | |
| `wp_Probe` | |
| `wp_PurpleMushroom` | |
| `wp_PuzzleBox` | |
| `wp_RainStaff` | |
| `wp_RainbowRemote` | |
| `wp_Rally` | |
| `wp_RatBomb` | |
| `wp_RedMushroom` | |
| `wp_Revolver` | |
| `wp_RocketLauncher` | |
| `wp_Rocks` | |
| `wp_RollOfPennies` | |
| `wp_RubberBat` | |
| `wp_RubberFist` | |
| `wp_RustedRod` | |
| `wp_RustyRazor` | |
| `wp_SawBlades` | |
| `wp_ScaldingOrb` | |
| `wp_SeedBomb` | |
| `wp_SharpStraw` | |
| `wp_ShoeHorn` | |
| `wp_Shotgun` | |
| `wp_ShotgunSteven` | |
| `wp_Shovel` | |
| `wp_SignalAmplifier` | |
| `wp_SignalAmplifierSpawnTerminator` | |
| `wp_SixPack` | |
| `wp_SlagMight` | |
| `wp_SlingShot` | |
| `wp_Sniper` | |
| `wp_SoulClaw` | |
| `wp_SpawnStacy` | |
| `wp_SpearOfDestiny` | |
| `wp_Spitball` | |
| `wp_SpringBoard` | |
| `wp_StaffOfFlame` | |
| `wp_SteelBall` | |
| `wp_StevenWeapon1` | |
| `wp_StevenWeapon2` | |
| `wp_StevensBagOfRocks` | |
| `wp_StevensBottles` | |
| `wp_Stoolatk` | |
| `wp_StopwatchFixed` | |
| `wp_StrongMagnet` | |
| `wp_StunGun` | |
| `wp_Taser` | |
| `wp_TerminatorShotgun` | |
| `wp_TerminatorSniper` | |
| `wp_TerminatorUzi` | |
| `wp_TeslaCannon` | |
| `wp_Textbook` | |
| `wp_TheLoner` | |
| `wp_TheLonerFixed` | |
| `wp_ThePact` | |
| `wp_ThrobbingGristle` | |
| `wp_TinaScream` | |
| `wp_TractorBeam` | |
| `wp_TrashCanLid` | |
| `wp_Trowel` | |
| `wp_TuskThrow` | |
| `wp_USAShield` | |
| `wp_UnderworldStaff` | |
| `wp_UraniumRod` | |
| `wp_Uzi` | |
| `wp_Whetstone` | |
| `wp_ZodiacsSixshooter` | |
| `wp_ZodiacsSixshooter_Auto` | |

</details>


---

### Enum: `brain`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ReplaceBrain`](./Characters_and_Bosses.md#context-replacebrain), [`ai`](./Characters_and_Bosses.md#context-ai), [`ai_if_spawned_as_enemy`](./Characters_and_Bosses.md#context-ai_if_spawned_as_enemy), [`ReplaceBrain`](./Passives_and_Statuses.md#context-replacebrain)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `PatternBrain` | |
| `GenericBrain` | |
| `NoBrain` | |
| `PlayerBrain` | |
| `DicerBrain` | |
| `MountBrain` | |

</details>


---

### Enum: `faction`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance), [`spawn`](./Abilities_and_Spells.md#context-spawn), [`SpawnOnDeath`](./Characters_and_Bosses.md#context-spawnondeath), [`properties`](./Characters_and_Bosses.md#context-properties), [`AllyInfested`](./House_and_Environment.md#context-allyinfested), [`SpawnOnDeath`](./Items_and_Equipment.md#context-spawnondeath)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `enemies` | |
| `allies` | |
| `self` | |
| `none` | |
| `default` | |
| `cavemen` | |
| `solitary_enemies` | |
| `third_party` | |
| `sabertooths` | |
| `birds` | |
| `mammoths` | |
| `auto` | |
| `kaiju1` | |
| `kaiju2` | |

</details>


---

### Enum: `stat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`10coins`](./Events_and_Encounters.md#context-10coins), [`5coins`](./Events_and_Encounters.md#context-5coins), [`ROOT`](./Events_and_Encounters.md#context-root), [`a`](./Events_and_Encounters.md#context-a), [`activate_p`](./Events_and_Encounters.md#context-activate_p), [`activate_z`](./Events_and_Encounters.md#context-activate_z), [`altar_sacrifice`](./Events_and_Encounters.md#context-altar_sacrifice), [`arm`](./Events_and_Encounters.md#context-arm), [`attach_amplifier`](./Events_and_Encounters.md#context-attach_amplifier), [`attach_antenna`](./Events_and_Encounters.md#context-attach_antenna), [`attach_leech`](./Events_and_Encounters.md#context-attach_leech), [`attack`](./Events_and_Encounters.md#context-attack), [`b`](./Events_and_Encounters.md#context-b), [`bash`](./Events_and_Encounters.md#context-bash), [`bash_past_alt`](./Events_and_Encounters.md#context-bash_past_alt), [`bite`](./Events_and_Encounters.md#context-bite), [`bite_it_off`](./Events_and_Encounters.md#context-bite_it_off), [`blue`](./Events_and_Encounters.md#context-blue), [`blue_needle`](./Events_and_Encounters.md#context-blue_needle), [`body`](./Events_and_Encounters.md#context-body), [`boogers`](./Events_and_Encounters.md#context-boogers), [`book`](./Events_and_Encounters.md#context-book), [`brace`](./Events_and_Encounters.md#context-brace), [`break_lock`](./Events_and_Encounters.md#context-break_lock), [`bribe`](./Events_and_Encounters.md#context-bribe), [`button`](./Events_and_Encounters.md#context-button), [`buy1`](./Events_and_Encounters.md#context-buy1), [`c`](./Events_and_Encounters.md#context-c), [`catch`](./Events_and_Encounters.md#context-catch), [`challenge_to_game`](./Events_and_Encounters.md#context-challenge_to_game), [`chaos_ending`](./Events_and_Encounters.md#context-chaos_ending), [`chapter_cutscene`](./Events_and_Encounters.md#context-chapter_cutscene), [`charm`](./Events_and_Encounters.md#context-charm), [`charm_past_alt`](./Events_and_Encounters.md#context-charm_past_alt), [`climb`](./Events_and_Encounters.md#context-climb), [`comfort`](./Events_and_Encounters.md#context-comfort), [`communicate`](./Events_and_Encounters.md#context-communicate), [`concheck`](./Events_and_Encounters.md#context-concheck), [`counter`](./Events_and_Encounters.md#context-counter), [`crack_open`](./Events_and_Encounters.md#context-crack_open), [`cut_wires`](./Events_and_Encounters.md#context-cut_wires), [`d`](./Events_and_Encounters.md#context-d), [`damage`](./Events_and_Encounters.md#context-damage), [`damage_1`](./Events_and_Encounters.md#context-damage_1), [`damage_full`](./Events_and_Encounters.md#context-damage_full), [`damage_half`](./Events_and_Encounters.md#context-damage_half), [`desert_cutscene`](./Events_and_Encounters.md#context-desert_cutscene), [`destroy`](./Events_and_Encounters.md#context-destroy), [`dexcheck`](./Events_and_Encounters.md#context-dexcheck), [`dig`](./Events_and_Encounters.md#context-dig), [`disarm`](./Events_and_Encounters.md#context-disarm), [`dive`](./Events_and_Encounters.md#context-dive), [`donate`](./Events_and_Encounters.md#context-donate), [`donate_10`](./Events_and_Encounters.md#context-donate_10), [`donate_15`](./Events_and_Encounters.md#context-donate_15), [`donate_20`](./Events_and_Encounters.md#context-donate_20), [`donate_5`](./Events_and_Encounters.md#context-donate_5), [`double`](./Events_and_Encounters.md#context-double), [`drink`](./Events_and_Encounters.md#context-drink), [`eat`](./Events_and_Encounters.md#context-eat), [`eat_meat`](./Events_and_Encounters.md#context-eat_meat), [`enter`](./Events_and_Encounters.md#context-enter), [`enter_crater`](./Events_and_Encounters.md#context-enter_crater), [`examine`](./Events_and_Encounters.md#context-examine), [`fiddle`](./Events_and_Encounters.md#context-fiddle), [`fight`](./Events_and_Encounters.md#context-fight), [`fill_jar`](./Events_and_Encounters.md#context-fill_jar), [`find`](./Events_and_Encounters.md#context-find), [`find_another_way`](./Events_and_Encounters.md#context-find_another_way), [`fire`](./Events_and_Encounters.md#context-fire), [`follow`](./Events_and_Encounters.md#context-follow), [`free`](./Events_and_Encounters.md#context-free), [`future`](./Events_and_Encounters.md#context-future), [`go_around`](./Events_and_Encounters.md#context-go_around), [`hack`](./Events_and_Encounters.md#context-hack), [`holy`](./Events_and_Encounters.md#context-holy), [`home`](./Events_and_Encounters.md#context-home), [`hp`](./Events_and_Encounters.md#context-hp), [`ice`](./Events_and_Encounters.md#context-ice), [`ignore`](./Events_and_Encounters.md#context-ignore), [`infinite`](./Events_and_Encounters.md#context-infinite), [`inspect`](./Events_and_Encounters.md#context-inspect), [`intcheck`](./Events_and_Encounters.md#context-intcheck), [`intimidation`](./Events_and_Encounters.md#context-intimidation), [`investigate`](./Events_and_Encounters.md#context-investigate), [`itchies`](./Events_and_Encounters.md#context-itchies), [`join`](./Events_and_Encounters.md#context-join), [`jump`](./Events_and_Encounters.md#context-jump), [`jump_over`](./Events_and_Encounters.md#context-jump_over), [`kiss`](./Events_and_Encounters.md#context-kiss), [`kiss_meat`](./Events_and_Encounters.md#context-kiss_meat), [`knife`](./Events_and_Encounters.md#context-knife), [`leave`](./Events_and_Encounters.md#context-leave), [`leave_it_in`](./Events_and_Encounters.md#context-leave_it_in), [`leg`](./Events_and_Encounters.md#context-leg), [`lever`](./Events_and_Encounters.md#context-lever), [`lick`](./Events_and_Encounters.md#context-lick), [`lick_alt`](./Events_and_Encounters.md#context-lick_alt), [`lightning`](./Events_and_Encounters.md#context-lightning), [`listen`](./Events_and_Encounters.md#context-listen), [`looks`](./Events_and_Encounters.md#context-looks), [`loot`](./Events_and_Encounters.md#context-loot), [`loot_heart`](./Events_and_Encounters.md#context-loot_heart), [`makeup`](./Events_and_Encounters.md#context-makeup), [`mind`](./Events_and_Encounters.md#context-mind), [`move_closer`](./Events_and_Encounters.md#context-move_closer), [`nothanks`](./Events_and_Encounters.md#context-nothanks), [`open`](./Events_and_Encounters.md#context-open), [`outsmart`](./Events_and_Encounters.md#context-outsmart), [`past`](./Events_and_Encounters.md#context-past), [`patch_up`](./Events_and_Encounters.md#context-patch_up), [`pick_lock`](./Events_and_Encounters.md#context-pick_lock), [`pilfer`](./Events_and_Encounters.md#context-pilfer), [`pirouette`](./Events_and_Encounters.md#context-pirouette), [`place_gristle`](./Events_and_Encounters.md#context-place_gristle), [`play`](./Events_and_Encounters.md#context-play), [`poop`](./Events_and_Encounters.md#context-poop), [`power`](./Events_and_Encounters.md#context-power), [`protection`](./Events_and_Encounters.md#context-protection), [`pull`](./Events_and_Encounters.md#context-pull), [`pull_it_out`](./Events_and_Encounters.md#context-pull_it_out), [`purify`](./Events_and_Encounters.md#context-purify), [`push_through`](./Events_and_Encounters.md#context-push_through), [`put_in_coins`](./Events_and_Encounters.md#context-put_in_coins), [`put_out_of_misery`](./Events_and_Encounters.md#context-put_out_of_misery), [`reach_inside`](./Events_and_Encounters.md#context-reach_inside), [`read`](./Events_and_Encounters.md#context-read), [`receive`](./Events_and_Encounters.md#context-receive), [`red`](./Events_and_Encounters.md#context-red), [`red_needle`](./Events_and_Encounters.md#context-red_needle), [`reflect`](./Events_and_Encounters.md#context-reflect), [`remove`](./Events_and_Encounters.md#context-remove), [`remove_the_nail`](./Events_and_Encounters.md#context-remove_the_nail), [`repair`](./Events_and_Encounters.md#context-repair), [`repair_quest`](./Events_and_Encounters.md#context-repair_quest), [`repell`](./Events_and_Encounters.md#context-repell), [`rest`](./Events_and_Encounters.md#context-rest), [`revive`](./Events_and_Encounters.md#context-revive), [`rub`](./Events_and_Encounters.md#context-rub), [`run`](./Events_and_Encounters.md#context-run), [`run_again`](./Events_and_Encounters.md#context-run_again), [`run_away`](./Events_and_Encounters.md#context-run_away), [`sacrifice`](./Events_and_Encounters.md#context-sacrifice), [`sacrifice_full_favor`](./Events_and_Encounters.md#context-sacrifice_full_favor), [`sacrifice_normal`](./Events_and_Encounters.md#context-sacrifice_normal), [`sacrifice_partial_favor`](./Events_and_Encounters.md#context-sacrifice_partial_favor), [`sacrifice_quest`](./Events_and_Encounters.md#context-sacrifice_quest), [`scream`](./Events_and_Encounters.md#context-scream), [`shake`](./Events_and_Encounters.md#context-shake), [`skip`](./Events_and_Encounters.md#context-skip), [`slip_through`](./Events_and_Encounters.md#context-slip_through), [`smash`](./Events_and_Encounters.md#context-smash), [`sneak`](./Events_and_Encounters.md#context-sneak), [`sneak_by`](./Events_and_Encounters.md#context-sneak_by), [`sneak_past_alt`](./Events_and_Encounters.md#context-sneak_past_alt), [`soul`](./Events_and_Encounters.md#context-soul), [`speed`](./Events_and_Encounters.md#context-speed), [`surprise`](./Events_and_Encounters.md#context-surprise), [`sweet_talk`](./Events_and_Encounters.md#context-sweet_talk), [`swim`](./Events_and_Encounters.md#context-swim), [`tail`](./Events_and_Encounters.md#context-tail), [`take`](./Events_and_Encounters.md#context-take), [`take_blood`](./Events_and_Encounters.md#context-take_blood), [`talk`](./Events_and_Encounters.md#context-talk), [`talk_to`](./Events_and_Encounters.md#context-talk_to), [`tappytoes`](./Events_and_Encounters.md#context-tappytoes), [`teleport`](./Events_and_Encounters.md#context-teleport), [`thorns`](./Events_and_Encounters.md#context-thorns), [`throw`](./Events_and_Encounters.md#context-throw), [`timemachine`](./Events_and_Encounters.md#context-timemachine), [`touch`](./Events_and_Encounters.md#context-touch), [`turnon`](./Events_and_Encounters.md#context-turnon), [`upgrade_yourself`](./Events_and_Encounters.md#context-upgrade_yourself), [`use_item`](./Events_and_Encounters.md#context-use_item), [`use_toilet_con`](./Events_and_Encounters.md#context-use_toilet_con), [`use_toilet_str`](./Events_and_Encounters.md#context-use_toilet_str), [`w1`](./Events_and_Encounters.md#context-w1), [`w2`](./Events_and_Encounters.md#context-w2), [`w3`](./Events_and_Encounters.md#context-w3), [`w4`](./Events_and_Encounters.md#context-w4), [`w5`](./Events_and_Encounters.md#context-w5), [`w6`](./Events_and_Encounters.md#context-w6), [`wealth`](./Events_and_Encounters.md#context-wealth), [`wheezies`](./Events_and_Encounters.md#context-wheezies), [`wish_genes`](./Events_and_Encounters.md#context-wish_genes), [`wish_items`](./Events_and_Encounters.md#context-wish_items), [`wish_levelups`](./Events_and_Encounters.md#context-wish_levelups), [`wish_strength`](./Events_and_Encounters.md#context-wish_strength), [`withstand`](./Events_and_Encounters.md#context-withstand), [`yank_it_out`](./Events_and_Encounters.md#context-yank_it_out), [`yellow_needle`](./Events_and_Encounters.md#context-yellow_needle)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `none` | |
| `str` | |
| `int` | |
| `lck` | |
| `con` | |
| `dex` | |
| `cha` | |
| `spd` | |
| `quest` | |
| `coins` | |

</details>


---

### Enum: `move_weights`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`UseMoveAbilityWithAI`](./Abilities_and_Spells.md#context-usemoveabilitywithai), [`CloseConvert`](./Characters_and_Bosses.md#context-closeconvert), [`Escape`](./Characters_and_Bosses.md#context-escape), [`FoodMove`](./Characters_and_Bosses.md#context-foodmove), [`LeapClose`](./Characters_and_Bosses.md#context-leapclose), [`MoveAway`](./Characters_and_Bosses.md#context-moveaway), [`MoveCenter`](./Characters_and_Bosses.md#context-movecenter), [`MoveClose`](./Characters_and_Bosses.md#context-moveclose), [`MoveForBarrage`](./Characters_and_Bosses.md#context-moveforbarrage), [`MoveForDash`](./Characters_and_Bosses.md#context-movefordash), [`MoveForGrass`](./Characters_and_Bosses.md#context-moveforgrass), [`MoveForPounce`](./Characters_and_Bosses.md#context-moveforpounce), [`MoveForSpin`](./Characters_and_Bosses.md#context-moveforspin), [`MoveForThrow`](./Characters_and_Bosses.md#context-moveforthrow), [`MoveOneForPuke`](./Characters_and_Bosses.md#context-moveoneforpuke), [`MoveSpaced`](./Characters_and_Bosses.md#context-movespaced), [`MoveToHead`](./Characters_and_Bosses.md#context-movetohead), [`MoveTowards`](./Characters_and_Bosses.md#context-movetowards), [`NCGravecrawlFAR`](./Characters_and_Bosses.md#context-ncgravecrawlfar), [`ReplaceBrain`](./Characters_and_Bosses.md#context-replacebrain), [`ReturnA`](./Characters_and_Bosses.md#context-returna), [`RunFar`](./Characters_and_Bosses.md#context-runfar), [`SpearRun`](./Characters_and_Bosses.md#context-spearrun), [`SuckMF`](./Characters_and_Bosses.md#context-suckmf), [`Terminator2Run`](./Characters_and_Bosses.md#context-terminator2run), [`Unflip`](./Characters_and_Bosses.md#context-unflip), [`ai`](./Characters_and_Bosses.md#context-ai), [`ai_if_spawned_as_enemy`](./Characters_and_Bosses.md#context-ai_if_spawned_as_enemy), [`ReplaceBrain`](./Passives_and_Statuses.md#context-replacebrain)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `stay_close` | |
| `keep_distance` | |
| `keep_distance_always_move` | |
| `stay_close_always_move` | |
| `chaos_always_move` | |
| `random` | |
| `stay_far` | |
| `blind_move_far` | |
| `stay_near_allies` | |
| `chaotic` | |
| `chubs_and_nubs_blind` | |
| `keep_ranged_distance` | |
| `stay_close_avoid_allies` | |
| `stay_close_move_far` | |
| `stay_far_move_far` | |
| `util_minmove` | |
| `keep_far_distance` | |
| `stay_far_always_move` | |
| `towards_aggro_stay_close` | |
| `chaotic_runaway` | |
| `chubs_and_nubs_rage` | |
| `gunslinger_reposition` | |
| `keep_distance_always_move_prefer_water` | |
| `minimum_move` | |
| `prefer_tall_grass_always_move` | |
| `stay_near_map_center` | |
| `towards_aggro` | |
| `zombie` | |
| `bird` | |
| `drmangler` | |
| `dustdevil` | |
| `keep_close_distance_always_move` | |
| `keep_distance_always_move_towards_water` | |
| `keep_distance_face_camera` | |
| `keep_distance_popeye` | |
| `prefer_lava_always_move` | |
| `rattle_distance` | |
| `run_far` | |
| `security_bot` | |
| `semi_blind` | |
| `stay_close_lenny` | |
| `stay_close_move_if_possible` | |
| `stay_near_allies_siren` | |
| `terminator_keep_distance_always_move` | |
| `terminator_stay_close` | |
| `trampy_chaos` | |
| `wash_johnny` | |

</details>


---

### Enum: `attack`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`705`](./Cat_Mutations.md#context-705), [`2`](./Characters_and_Bosses.md#context-2), [`3`](./Characters_and_Bosses.md#context-3), [`4`](./Characters_and_Bosses.md#context-4), [`5`](./Characters_and_Bosses.md#context-5), [`Big`](./Characters_and_Bosses.md#context-big), [`Bishop`](./Characters_and_Bosses.md#context-bishop), [`CaveBaby`](./Characters_and_Bosses.md#context-cavebaby), [`CaveMan`](./Characters_and_Bosses.md#context-caveman), [`CaveManSpear`](./Characters_and_Bosses.md#context-cavemanspear), [`CaveWoman`](./Characters_and_Bosses.md#context-cavewoman), [`CaveWomanHasCat`](./Characters_and_Bosses.md#context-cavewomanhascat), [`Charging`](./Characters_and_Bosses.md#context-charging), [`Cultist`](./Characters_and_Bosses.md#context-cultist), [`Default`](./Characters_and_Bosses.md#context-default), [`Down`](./Characters_and_Bosses.md#context-down), [`DualSword`](./Characters_and_Bosses.md#context-dualsword), [`DualSword_Primed`](./Characters_and_Bosses.md#context-dualsword_primed), [`Explody`](./Characters_and_Bosses.md#context-explody), [`FightPhase`](./Characters_and_Bosses.md#context-fightphase), [`Fire`](./Characters_and_Bosses.md#context-fire), [`FireFull`](./Characters_and_Bosses.md#context-firefull), [`Full`](./Characters_and_Bosses.md#context-full), [`Grown`](./Characters_and_Bosses.md#context-grown), [`HalfDead`](./Characters_and_Bosses.md#context-halfdead), [`HasCat`](./Characters_and_Bosses.md#context-hascat), [`HasDeadCat`](./Characters_and_Bosses.md#context-hasdeadcat), [`HasRock`](./Characters_and_Bosses.md#context-hasrock), [`HumanDead`](./Characters_and_Bosses.md#context-humandead), [`InitialPhase`](./Characters_and_Bosses.md#context-initialphase), [`Lifted`](./Characters_and_Bosses.md#context-lifted), [`MonkCatReactionAbilities`](./Characters_and_Bosses.md#context-monkcatreactionabilities), [`Mutant`](./Characters_and_Bosses.md#context-mutant), [`NoStick`](./Characters_and_Bosses.md#context-nostick), [`Normal`](./Characters_and_Bosses.md#context-normal), [`NormalFull`](./Characters_and_Bosses.md#context-normalfull), [`Nuke`](./Characters_and_Bosses.md#context-nuke), [`Open`](./Characters_and_Bosses.md#context-open), [`Primed`](./Characters_and_Bosses.md#context-primed), [`Pulp2`](./Characters_and_Bosses.md#context-pulp2), [`Pulp3`](./Characters_and_Bosses.md#context-pulp3), [`Pulp4`](./Characters_and_Bosses.md#context-pulp4), [`Pulp5`](./Characters_and_Bosses.md#context-pulp5), [`Pulp6`](./Characters_and_Bosses.md#context-pulp6), [`Pulp7`](./Characters_and_Bosses.md#context-pulp7), [`Rage`](./Characters_and_Bosses.md#context-rage), [`Sitting`](./Characters_and_Bosses.md#context-sitting), [`Small`](./Characters_and_Bosses.md#context-small), [`SquirrelForm`](./Characters_and_Bosses.md#context-squirrelform), [`Standing`](./Characters_and_Bosses.md#context-standing), [`Standing2`](./Characters_and_Bosses.md#context-standing2), [`SwordAndShield`](./Characters_and_Bosses.md#context-swordandshield), [`SwordAndShield_Primed`](./Characters_and_Bosses.md#context-swordandshield_primed), [`Tar`](./Characters_and_Bosses.md#context-tar), [`TarFull`](./Characters_and_Bosses.md#context-tarfull), [`Turtled`](./Characters_and_Bosses.md#context-turtled), [`Washer`](./Characters_and_Bosses.md#context-washer), [`WereMan`](./Characters_and_Bosses.md#context-wereman), [`Zealot`](./Characters_and_Bosses.md#context-zealot), [`ZealotBomb`](./Characters_and_Bosses.md#context-zealotbomb), [`abilities`](./Characters_and_Bosses.md#context-abilities), [`ai`](./Characters_and_Bosses.md#context-ai), [`passive`](./Characters_and_Bosses.md#context-passive), [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicMelee` | |
| `None` | |
| `BasicBigMelee` | |
| `DoNothing` | |
| `BasicTankMelee` | |
| `FurySwipes_Enemy` | |
| `AnimatedRockAttack` | |
| `BasicMelee_Fighter` | |
| `DestroyerAttack` | |
| `SpewerSpit` | |
| `WideSwipe` | |
| `BasicRanged` | |
| `BasicRanged_Hunter` | |
| `BasicShortLobbed` | |
| `BasicShortLobbed_Water` | |
| `BungaSmash` | |
| `CancerMelee` | |
| `CatSpin` | |
| `CaveMan3HitCombo` | |
| `CaveManThrowSpear` | |
| `ColorlessCat_Push` | |
| `DestroyerAttack2` | |
| `DruidCatBasic` | |
| `FetusGush` | |
| `GuncatShoot` | |
| `HammerSmash` | |
| `KirbySpit` | |
| `KirbySuck` | |
| `LennyCatSlap` | |
| `LennyShove` | |
| `MegafetusSpin` | |
| `NubsJump` | |
| `PoisonShot` | |
| `PyrophinaSoloAttack` | |
| `ReaperSpin` | |
| `ShamblerDash` | |
| `SharkDash` | |
| `SpawnGas` | |
| `SpearPoke` | |
| `SpearPokeTest` | |
| `SpewerLobbed_Normal` | |
| `T3Shoot` | |
| `ZaratanaSoloBasic` | |
| `AZ_BreakNeck` | |
| `AcidShot` | |
| `AmoebaAttach` | |
| `AmoebaRockBash` | |
| `AngelcatWind` | |
| `AnkyloSwipe` | |
| `AtomicBurst` | |
| `BBExplode` | |
| `BBMutantSwipe` | |
| `BBStabby` | |
| `BBXLightning` | |
| `BabySharkMelee` | |
| `BadBone` | |
| `BasicButcherMelee` | |
| `BasicButcherMeleeWideSpin` | |
| `BasicDrainMelee` | |
| `BasicExplosiveShot` | |
| `BasicHook` | |
| `BasicMagicShortRanged` | |
| `BasicMedicMelee` | |
| `BasicMelee_2Hits` | |
| `BasicMelee_3Hits` | |
| `BasicMelee_4Hits` | |
| `BasicMelee_5Hits` | |
| `BasicMetronome` | |
| `BasicNecroRanged` | |
| `BasicPoke` | |
| `BasicPsychicPull` | |
| `BasicShortRanged` | |
| `BasicSpin` | |
| `BasicStraightShot` | |
| `BatFlurry` | |
| `BearFurySwipes` | |
| `BelcherLavashot` | |
| `BigAsteroidBarrage` | |
| `BigGunkShot` | |
| `BloatFrontLaser` | |
| `BombExplode` | |
| `BoneWormShotMed` | |
| `BoneWormShotSmall` | |
| `BoneWormShotTall` | |
| `BoyDinoBasic` | |
| `BrainDrainMagicMissile` | |
| `BramblePull` | |
| `ButtFart` | |
| `CHToss` | |
| `CHuskBone` | |
| `CHuskCatShade` | |
| `CarcusSpawn` | |
| `CarnibulbEat` | |
| `CaveBabyMelee` | |
| `CaveCatPounce` | |
| `CaveChiefSlam` | |
| `CaveDad_ClubBasic` | |
| `CaveMom_Basic` | |
| `CaveWomanCatSlap` | |
| `CaveWomanKick` | |
| `CerberubsJump` | |
| `ChainDash` | |
| `ChaosStacyAttack` | |
| `CherubMelee` | |
| `CherubimHeal` | |
| `ChubsSpin` | |
| `ChubsSpinRage` | |
| `ChumDash` | |
| `ChumShot_Damage` | |
| `CloakerHex` | |
| `CollectiveSpin` | |
| `CoreFreakAttack` | |
| `CraterCreeperRockBlast` | |
| `CreepRanged` | |
| `DH_Attack` | |
| `DaddyHungry` | |
| `Dash_BabyDeathWorm` | |
| `Dash_Enemy` | |
| `DeathWormTrampleDash` | |
| `DemonUppercut` | |
| `DinoEggsSpawn` | |
| `DipShot` | |
| `DoctorBotHeal` | |
| `DoubleDiagonalCreepshot` | |
| `DrDRockets` | |
| `DustMelee` | |
| `DybbukLick` | |
| `FatCatBellyFlop` | |
| `FatManLunge` | |
| `FetusSpit` | |
| `Flamethrower` | |
| `FleshLadDoublehit` | |
| `FleshyMindDisable` | |
| `FloastPull` | |
| `FloaterMelee` | |
| `Flush` | |
| `FurySwipes_Hitler` | |
| `FutureBotPunch` | |
| `G3PrisonSpit` | |
| `GA_Telekinesis` | |
| `GA_Telekinesis_Big` | |
| `GKSuck` | |
| `GSClosedAttack` | |
| `GSOpenAttack` | |
| `GameteInflate` | |
| `GameteSpawn` | |
| `GasBlast` | |
| `GasCanExplode` | |
| `GeminiBite` | |
| `GirlDinoMelee` | |
| `GorgerGorge` | |
| `GunkShot` | |
| `HCAttack` | |
| `HCSpin` | |
| `HangerBotAttack` | |
| `HeadTumorAttack` | |
| `HellHandGrab` | |
| `HemShot` | |
| `HexShot` | |
| `HitlerCloneSwipes` | |
| `HitlerShoot` | |
| `HornyToadShot` | |
| `HostSpit` | |
| `HuskSwipes` | |
| `IceElementalSpikes` | |
| `InvaderAttack` | |
| `IsaacBasicAttack` | |
| `JackAttack` | |
| `JohnnyBlast` | |
| `KillDoze` | |
| `LEBurst` | |
| `LeechDash` | |
| `LiceBite` | |
| `Lick` | |
| `LoveBotHeal` | |
| `MCMelee` | |
| `MD_Stomp` | |
| `MM_Slap` | |
| `MammothBabyThrow` | |
| `MammothThrow` | |
| `ManglerCommand` | |
| `ManglerJab` | |
| `ManglerMonsterDashAttack` | |
| `MeatMinionMelee` | |
| `MechSuitPunch` | |
| `MoonHandSlap` | |
| `MoonHandSqueeze` | |
| `MoonHead_Blow` | |
| `MoonHead_ChewCat` | |
| `MoonWormShot` | |
| `NurseBotHealCat` | |
| `Parasaurolophus_Push` | |
| `ParasiteShot` | |
| `ParasiterShoot` | |
| `PokerAttack` | |
| `PoopCatMelee` | |
| `PopeyeDash` | |
| `PrehistoricPooterShot` | |
| `PrisonShot` | |
| `PteroPeck` | |
| `QueenHippoAttack` | |
| `RaptorBabyBite` | |
| `RatKingDash` | |
| `RatKingToss` | |
| `RatLeap` | |
| `RattleSnakeAttack` | |
| `RocketSkates_Bombchu` | |
| `RocketTurretShot` | |
| `RockySlam` | |
| `Roomba_Bump` | |
| `RoverDash` | |
| `RubberFistBotPunch` | |
| `SBotAttack` | |
| `SCAttack` | |
| `SZBShoot` | |
| `SabertoothCatPounce` | |
| `SabertoothCubDoubleSwipe` | |
| `ScaryFear` | |
| `ScorpionSting` | |
| `SeraphimX` | |
| `ShadowDagger` | |
| `ShortCreepshot` | |
| `ShortCreepshotCrater` | |
| `SirenCall` | |
| `SkinnedTripleDash` | |
| `SlagBoner` | |
| `SmallAsteroidBarrage` | |
| `SmallTrampleDash` | |
| `SpawnMotherSpike` | |
| `SpawnSpewerPill` | |
| `SpewerLobbed_Lava` | |
| `SpewerLobbed_Tar` | |
| `SpiderSuicideMelee` | |
| `SpitGlass` | |
| `SpookieLick` | |
| `SproutSpore` | |
| `SquirrelFurySwipes` | |
| `StacyCharm` | |
| `StegoTailSwipe` | |
| `SuicideMelee` | |
| `T2SpearMelee` | |
| `TC_Attack` | |
| `THC_KnockCoinsRanged` | |
| `TKNG_GutBall` | |
| `TKNG_Laser` | |
| `TT_Thrash` | |
| `TallBotSuplex` | |
| `TallSpiderMelee` | |
| `TarBall` | |
| `TattersLeeches` | |
| `TenTicklesAttack` | |
| `TeslaBolt` | |
| `ThrobShot` | |
| `ThumpSlam` | |
| `TinaBasicBigMelee` | |
| `TinaBasicBigMeleeA` | |
| `TinaBodySlam` | |
| `TinaHeadGutSpear` | |
| `ToxExplode` | |
| `TrembloSmash` | |
| `TrexEat` | |
| `TriceratopsGore` | |
| `TumorDash` | |
| `TurretShot` | |
| `UFO_CrossLasers` | |
| `UFO_Dash` | |
| `WallBlow` | |
| `WallEyeShot` | |
| `WebShot` | |
| `WereManFurySwipes` | |
| `WhispererThrowDamage` | |
| `WolfDash` | |
| `YA_Laser` | |
| `YetiSlam` | |
| `YeticatSnowball` | |
| `ZaratanaBasic` | |
| `ZodiacShoot` | |
| `ZodiacShootX` | |
| `attack` | |

</details>


---

### Enum: `decision_weights`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CerberubsJumpBlind`](./Characters_and_Bosses.md#context-cerberubsjumpblind), [`CerberubsJumpNormal`](./Characters_and_Bosses.md#context-cerberubsjumpnormal), [`DashRandomly`](./Characters_and_Bosses.md#context-dashrandomly), [`ForceTrample`](./Characters_and_Bosses.md#context-forcetrample), [`ReplaceBrain`](./Characters_and_Bosses.md#context-replacebrain), [`SuckMF`](./Characters_and_Bosses.md#context-suckmf), [`TF_TargetAllies`](./Characters_and_Bosses.md#context-tf_targetallies), [`TF_TargetEnemies`](./Characters_and_Bosses.md#context-tf_targetenemies), [`ai`](./Characters_and_Bosses.md#context-ai), [`ai_if_spawned_as_enemy`](./Characters_and_Bosses.md#context-ai_if_spawned_as_enemy), [`ReplaceBrain`](./Passives_and_Statuses.md#context-replacebrain)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `default` | |
| `simple` | |
| `careless` | |
| `always_cast` | |
| `semi_simple` | |
| `blind` | |
| `extra_careless` | |
| `default_ignore_selfdamage` | |
| `terminator` | |
| `always_cast_careless` | |
| `angry` | |
| `cop` | |
| `default_no_revive` | |
| `default_spawn_at_preferred_distance` | |
| `heal_others` | |
| `reaper` | |
| `spawn_far` | |
| `zombie` | |
| `default_t3hitler` | |
| `dustdevil` | |
| `nubs_fakeblind` | |
| `peashy` | |
| `peashy_rage` | |
| `spawn_randomly` | |
| `teslacoil` | |
| `util_target_allies` | |
| `util_target_enemies` | |

</details>


---

### Enum: `damage`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TwisterDisplaceWithDamage`](./Abilities_and_Spells.md#context-twisterdisplacewithdamage), [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance), [`self_damage`](./Abilities_and_Spells.md#context-self_damage), [`splash_damage`](./Abilities_and_Spells.md#context-splash_damage), [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#context-damageneighborsaftermove), [`Earth`](./Passives_and_Statuses.md#context-earth)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `5+bonus_melee_damage` | |
| `5+bonus_melee_ability_damage` | |
| `5+bonus_ranged_damage` | |
| `4+bonus_melee_damage` | |
| `4+bonus_ranged_damage` | |
| `3+bonus_melee_ability_damage` | |
| `3+bonus_melee_damage` | |
| `1+bonus_melee_ability_damage` | |
| `3+bonus_ranged_damage` | |
| `1+bonus_ranged_damage` | |
| `1+bonus_melee_damage` | |
| `2+bonus_melee_damage` | |
| `2+bonus_melee_ability_damage` | |
| `2+bonus_ranged_damage` | |
| `3+bonus_basic_spell_damage` | |
| `10+bonus_melee_damage` | |
| `X` | |
| `10+bonus_melee_ability_damage` | |
| `7+bonus_ranged_damage` | |
| `8+bonus_melee_damage` | |
| `1+X` | |
| `1+bonus_basic_spell_damage` | |
| `10+bonus_ranged_damage` | |
| `15+bonus_melee_damage` | |
| `6+bonus_melee_damage` | |
| `7+bonus_melee_damage` | |
| `8+bonus_ranged_damage` | |
| `inherit` | |
| `2+bonus_basic_spell_damage` | |
| `5+bonus_basic_spell_damage` | |
| `15+bonus_melee_ability_damage` | |
| `25+bonus_melee_ability_damage` | |
| `4+bonus_melee_ability_damage` | |
| `6+bonus_basic_spell_damage` | |
| `durability` | |
| `item_aux` | |
| `str` | |
| `-3+bonus_melee_damage` | |
| `1+X*3` | |
| `1+X*4` | |
| `4+bonus_basic_spell_damage` | |
| `5+X` | |
| `6+bonus_melee_ability_damage` | |
| `6+bonus_ranged_damage` | |
| `7+bonus_melee_ability_damage` | |
| `9+bonus_ranged_damage` | |
| `X+1` | |
| `X+bonus_melee_damage` | |
| `con` | |
| `int` | |
| `level` | |

</details>


---

### Enum: `target_mode`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `none` | |
| `direction` | |
| `tile` | |
| `random_tile` | |
| `direction8` | |
| `random_closest_tile` | |
| `random_farthest_tile` | |

</details>


---

### Enum: `particle`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics), [`FormChangeOnElementInfluence`](./Characters_and_Bosses.md#context-formchangeonelementinfluence), [`spell_graphics_override`](./Passives_and_Statuses.md#context-spell_graphics_override)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `none` | |
| `Explosion` | |
| `fx_statup` | |
| `PoisonPoof` | |
| `Bolt` | |
| `MagicMissleBlast` | |
| `fx_windSpell` | |
| `IcePoof` | |
| `Earthquake` | |
| `Wave` | |
| `WaterConduct` | |
| `BigMagicMissileBlast` | |
| `Holybeam` | |
| `FearEffect` | |
| `FireBlastMushroom` | |
| `None` | |
| `FireExtinguish` | |
| `FireSpin` | |
| `HealSmall` | |
| `ExclamationPointEnemy` | |
| `MeteorFall` | |
| `fx_magicSplash` | |
| `fx_statdown` | |
| `Cleanse` | |
| `FireBlastMedium` | |
| `FireBlastSmall` | |
| `sytheCut` | |
| `ArrowFromAbove` | |
| `BurnTrigger` | |
| `CharmedHearts` | |
| `DustPoofLarge` | |
| `DustPoofMedium` | |
| `ExclamationPoint` | |
| `Glasspop` | |
| `HealBig` | |
| `HealMed` | |
| `HyperBeam` | |
| `Icequake` | |
| `Slash` | |
| `Spike` | |
| `VineWhip` | |
| `confusionStars` | |
| `CharmedOverlay` | |
| `IceBlast` | |
| `RocketFromAbove` | |
| `SparklingClean` | |
| `SpookyDarkness` | |
| `bloodywave` | |
| `clockanim` | |
| `fx_sandBlows` | |
| `fx_shield` | |
| `rebuke` | |

</details>


---

### Enum: `movieclip`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Characters_and_Bosses.md#context-graphics), [`Floor1_Large`](./House_and_Environment.md#context-floor1_large), [`Floor1_Small`](./House_and_Environment.md#context-floor1_small), [`ROOT`](./House_and_Environment.md#context-root), [`SmallAttic`](./House_and_Environment.md#context-smallattic), [`meta`](./Shops.md#context-meta)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `_CAT` | |
| `TreasureRoom` | |
| `Shop` | |
| `ArmorPickup` | |
| `ManaPickup` | |
| `Pyrophina` | |
| `Shambler` | |
| `Tombstone` | |
| `Zaratana` | |
| `BirdSmall` | |
| `CanCreeper` | |
| `CanCreeperOut` | |
| `Coin` | |
| `Crow` | |
| `Fetus` | |
| `FetusGusher` | |
| `FetusNoJar` | |
| `Flea` | |
| `Frog` | |
| `LoveBot` | |
| `Pooter` | |
| `Reaper` | |
| `Rock` | |
| `Snake` | |
| `Squirrel` | |
| `TNTCrate` | |
| `TracyOffice` | |
| `Tumor` | |
| `AcidOoze` | |
| `AlienBeast` | |
| `AlienEgg` | |
| `Amoeba` | |
| `Angel` | |
| `AngelicCatFetus` | |
| `AnimalEgg` | |
| `AntidotePickup` | |
| `AstroSkull` | |
| `AstroZombie` | |
| `BabyDeathWorm` | |
| `BabyShark` | |
| `BabySpider` | |
| `Bat` | |
| `BeaniesX` | |
| `Bear` | |
| `BigAsteroid` | |
| `BigDemon` | |
| `BigRock` | |
| `BigSlime` | |
| `BigSlimeX` | |
| `BigUFO` | |
| `BirdLarge` | |
| `BirdMed` | |
| `Birthwort` | |
| `BishopHat` | |
| `BloatEye` | |
| `BloatRat` | |
| `BloatyCorpse` | |
| `Bomb` | |
| `BombFly` | |
| `Bombchu` | |
| `BomberRat` | |
| `Boulder` | |
| `BoyDino` | |
| `BrambleBaby` | |
| `Bumblefoot` | |
| `BungaElite1` | |
| `BungaElite2` | |
| `BungaThrone` | |
| `BunkerBoy` | |
| `BunkerCandles2x2` | |
| `BunkerCandlesSmall` | |
| `Burfer` | |
| `ButchTinkX` | |
| `Cactus` | |
| `Carcus` | |
| `Carnibulb` | |
| `CatHuman` | |
| `Caterpillar` | |
| `CaveChief` | |
| `CavePerson` | |
| `Cerberubs` | |
| `Chaos` | |
| `ChargeyMaggot` | |
| `Chubs` | |
| `ChumBag` | |
| `Chummy` | |
| `CloakedDemon` | |
| `CloningVat` | |
| `Clot` | |
| `ConjoinedHusk` | |
| `CopBot` | |
| `CoreArm` | |
| `CoreFreak` | |
| `CovenCandle` | |
| `Crate` | |
| `Cutter` | |
| `DaddyShark` | |
| `DeathWorm` | |
| `Deathbot` | |
| `Decoy` | |
| `Decoy2` | |
| `DiggyMaggot` | |
| `DinoEggs` | |
| `Dip` | |
| `DocBot` | |
| `DrDitto` | |
| `DrMangler` | |
| `Dumpster` | |
| `DustCloud` | |
| `DustDevil` | |
| `Dybbuk` | |
| `ElectricNail` | |
| `EmptyV` | |
| `FatMan` | |
| `FatRat` | |
| `FatWoman` | |
| `Fatso` | |
| `FetusJar` | |
| `FinalBossMegaGuppy` | |
| `FinalBossPhase1` | |
| `FinalBossPhase2` | |
| `FinalBossPhase3` | |
| `FleshLad` | |
| `FleshyMind` | |
| `Floast` | |
| `Floater` | |
| `FloatingHive` | |
| `Flushmaster` | |
| `Fly` | |
| `FlySwarm` | |
| `Food` | |
| `FrankX` | |
| `Fuzzer` | |
| `Gambit` | |
| `GambitDice` | |
| `Gamete` | |
| `GasCan` | |
| `GasCloud` | |
| `Gasser` | |
| `Gatekeeper` | |
| `Gemini` | |
| `GeoLad` | |
| `GirlDino` | |
| `GlowingMushroom` | |
| `GraveWorm` | |
| `GreenProber` | |
| `Grenade` | |
| `GreyAlien` | |
| `GroundZombie` | |
| `GroundedSpear` | |
| `Guillotina1` | |
| `Guillotina2Body` | |
| `Guillotina2Head` | |
| `Guillotina3Body` | |
| `Guillotina3Head` | |
| `HangerBot` | |
| `HarpoonTrap` | |
| `HeadTumor` | |
| `Hemlock` | |
| `Hitler` | |
| `HitlerHead` | |
| `HitlerMech` | |
| `Hive` | |
| `HolyPickup` | |
| `Host` | |
| `HumanCat` | |
| `Husk` | |
| `Hydrant` | |
| `HydrantFountain` | |
| `IceCube` | |
| `IceElemental` | |
| `Invader` | |
| `JackOffice` | |
| `JarHead` | |
| `Johnny` | |
| `Junk` | |
| `KillDozer` | |
| `Kirby` | |
| `LabSupportPillar` | |
| `Lenny` | |
| `LightningElemental` | |
| `LordBunga` | |
| `MadLad` | |
| `Maggot` | |
| `MamaMaggot` | |
| `Mammoth` | |
| `ManglersMonster` | |
| `Mask` | |
| `MeatMinion` | |
| `MeatSlime` | |
| `MechSuit` | |
| `MedSlime` | |
| `MedSlimeX` | |
| `MegaDinoHead` | |
| `MegaDinoLeg` | |
| `MegaFetus` | |
| `MegaMutant` | |
| `MegaTumor` | |
| `MindFetus` | |
| `MiniVolcano` | |
| `MoonHand` | |
| `MoonHead` | |
| `MoonWorm` | |
| `Moth` | |
| `MotherSpike` | |
| `MotherTumor` | |
| `Multicat` | |
| `Nettle` | |
| `NeutronStar` | |
| `Nubs` | |
| `NubsCat` | |
| `OrganGrinderX` | |
| `OrganOffice` | |
| `Ornstein` | |
| `Parasiter` | |
| `Peashy` | |
| `PetBoulder` | |
| `PetRock` | |
| `Pile` | |
| `Pinky` | |
| `PinkyX` | |
| `PokerDemon` | |
| `Poop` | |
| `Pterodactyl` | |
| `Punchbot` | |
| `QueenHippo` | |
| `Rager` | |
| `Rat` | |
| `RatCat` | |
| `RatKing` | |
| `RatKing_New` | |
| `RatPile` | |
| `Revalark` | |
| `RockyBobo` | |
| `RoomBackgroundAttic` | |
| `RoomBackgroundBasement0` | |
| `RoomBackgroundBasement1` | |
| `RoomBackgroundBasement2` | |
| `RoomBackgroundBasement3` | |
| `RoomBackgroundBasement4` | |
| `RoomBackgroundLargeF1` | |
| `RoomBackgroundLargeF2` | |
| `RoomBackgroundSmallAttic` | |
| `RoomBackgroundSmallF1` | |
| `RoomBackgroundSmallF2` | |
| `Roomba` | |
| `Scary` | |
| `SecurityBot` | |
| `ShadeF` | |
| `ShadeM` | |
| `ShadeMShadow` | |
| `ShamblingShade` | |
| `Simon` | |
| `SimonFlop` | |
| `Slag` | |
| `SlotMachine` | |
| `SmallAsteroid` | |
| `SmallRock` | |
| `SmallSlime` | |
| `SmallSlimeX` | |
| `SmallUFO` | |
| `Smough` | |
| `SnakeyBones` | |
| `SoldierBot` | |
| `SpearTestGuy` | |
| `Spewer` | |
| `SpewerPill` | |
| `SpewerTube` | |
| `SpiderQueen` | |
| `SpikyCactus` | |
| `SpikyCactus2x2` | |
| `SpikyCactusTall` | |
| `SpikyRock` | |
| `Spookie` | |
| `Sprout` | |
| `Stegosaurus` | |
| `TallBot` | |
| `TallHaunt` | |
| `TallTumor` | |
| `TarBaby` | |
| `Tatters` | |
| `TenTickles` | |
| `TeslaCoil` | |
| `TheBloat` | |
| `TheCoven` | |
| `TheMother` | |
| `ThrobbingKing` | |
| `ThrobbingKing2` | |
| `ThrobbingTurret` | |
| `Thump` | |
| `Tire` | |
| `Tormentor` | |
| `Tox` | |
| `TracyX` | |
| `Trampy` | |
| `TrashBag` | |
| `Tremblo` | |
| `Trex` | |
| `Triachnid` | |
| `Triceratops` | |
| `TumorBarrier` | |
| `Turret` | |
| `Turtle` | |
| `Twister` | |
| `UltraOrnstein` | |
| `UltraSmough` | |
| `Waggle` | |
| `WaterLeech` | |
| `Whisperer` | |
| `WhiteBear` | |
| `Wisp` | |
| `Wizard` | |
| `WoC_Eye` | |
| `WoC_Mouth` | |
| `WoC_Wall` | |
| `Worm` | |
| `YellowBlaster` | |
| `Yeti` | |
| `Zodiac` | |
| `static_1x1_a` | |
| `static_1x1_b` | |
| `static_1x1_c` | |
| `static_2x2_a` | |
| `static_2x2_b` | |
| `static_tall_a` | |
| `static_tall_b` | |
| `test2x2` | |

</details>


---

### Enum: `move`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Default`](./Characters_and_Bosses.md#context-default), [`Down`](./Characters_and_Bosses.md#context-down), [`Explody`](./Characters_and_Bosses.md#context-explody), [`FightPhase`](./Characters_and_Bosses.md#context-fightphase), [`HasCat`](./Characters_and_Bosses.md#context-hascat), [`InitialPhase`](./Characters_and_Bosses.md#context-initialphase), [`Lifted`](./Characters_and_Bosses.md#context-lifted), [`MonkCatReactionAbilities`](./Characters_and_Bosses.md#context-monkcatreactionabilities), [`Nuke`](./Characters_and_Bosses.md#context-nuke), [`Pulp2`](./Characters_and_Bosses.md#context-pulp2), [`Pulp3`](./Characters_and_Bosses.md#context-pulp3), [`Pulp4`](./Characters_and_Bosses.md#context-pulp4), [`Pulp5`](./Characters_and_Bosses.md#context-pulp5), [`Pulp6`](./Characters_and_Bosses.md#context-pulp6), [`Pulp7`](./Characters_and_Bosses.md#context-pulp7), [`SecurityBotProtect`](./Characters_and_Bosses.md#context-securitybotprotect), [`Sitting`](./Characters_and_Bosses.md#context-sitting), [`Standing`](./Characters_and_Bosses.md#context-standing), [`Standing2`](./Characters_and_Bosses.md#context-standing2), [`TerminatorChase`](./Characters_and_Bosses.md#context-terminatorchase), [`Turtled`](./Characters_and_Bosses.md#context-turtled), [`abilities`](./Characters_and_Bosses.md#context-abilities), [`SecurityBotProtect`](./Passives_and_Statuses.md#context-securitybotprotect)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DefaultMove` | |
| `None` | |
| `Teleport` | |
| `DoNothing` | |
| `FloatMove` | |
| `BasicJump` | |
| `SwimmerMove` | |
| `HunterMinibossMove` | |
| `Swim` | |
| `WallMove` | |
| `move` | |
| `BungaJumpMove` | |
| `DustMove` | |
| `FuzzerJump` | |
| `GooseStep` | |
| `LennyTrampleMove` | |
| `MD_Walk` | |
| `MoveOne` | |
| `MoveThree` | |
| `SBotAngryMove` | |
| `SwapPositions` | |
| `TeleportFlipUp` | |
| `TenTicklesSwim` | |
| `ThumpSlam_Mov` | |
| `TwisterMove` | |

</details>


---

### Enum: `aoe_mode`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `all` | |
| `custom` | |
| `standard` | |
| `square` | |
| `line` | |
| `cone` | |
| `occupied_tiles` | |
| `circle` | |
| `cross` | |
| `diagcross` | |
| `hit_consumer` | |
| `narrow_cone` | |
| `all_except_edges` | |
| `all_except_random_empty` | |
| `area_around_all_player_cats` | |
| `map_edges` | |
| `perpline` | |
| `8cross` | |
| `cone8` | |
| `corner_square` | |
| `none` | |
| `normal` | |
| `pierce_cross` | |

</details>


---

### Enum: `prompt`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`good`](./Events_and_Encounters.md#context-good), [`main`](./Events_and_Encounters.md#context-main), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward), [`popup`](./Progression_Unlocks.md#context-popup)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ITEM_UNLOCK_GENERIC` | |
| `QEVENT_OBELISK_IGNORE` | |
| `QEVENT_OBELISK_REW1` | |
| `QEVENT_OBELISK_REW2` | |
| `QEVENT_OBELISK_REW3` | |
| `QEVENT_OBELISK_REW4` | |
| `QEVENT_THROBBINGARTERY_REW3` | |
| `QEVENT_OBELISK_QUES2` | |
| `QEVENT_OBELISK_REW_PYRO_WRONG` | |
| `QEVENT_OBELISK_REW_ZARA_WRONG` | |
| `QEVENT_VOLCANO_REW2` | |
| `QEVENT_VOLCANO_REW3` | |
| `AREA_UNLOCK_THERIFT` | |
| `CUTSCENE_OBELISK2_POPUP` | |
| `QEVENT_OBELISK_QUES1` | |
| `QEVENT_THROBBINGARTERY_REW1` | |
| `QEVENT_THROBBINGARTERY_REW2` | |
| `QEVENT_VOLCANO_REW1` | |
| `ABILITY_UNLOCK_BUTCHER` | |
| `ABILITY_UNLOCK_BUTCHER_COLORLESS` | |
| `ABILITY_UNLOCK_COLORLESS` | |
| `ABILITY_UNLOCK_COLORLESS_COLORLESS` | |
| `ABILITY_UNLOCK_DRUID` | |
| `ABILITY_UNLOCK_DRUID_COLORLESS` | |
| `ABILITY_UNLOCK_FIGHTER` | |
| `ABILITY_UNLOCK_FIGHTER_COLORLESS` | |
| `ABILITY_UNLOCK_HUNTER` | |
| `ABILITY_UNLOCK_HUNTER_COLORLESS` | |
| `ABILITY_UNLOCK_JESTER` | |
| `ABILITY_UNLOCK_JESTER_COLORLESS` | |
| `ABILITY_UNLOCK_MAGE` | |
| `ABILITY_UNLOCK_MAGE_COLORLESS` | |
| `ABILITY_UNLOCK_MEDIC` | |
| `ABILITY_UNLOCK_MEDIC_COLORLESS` | |
| `ABILITY_UNLOCK_MONK` | |
| `ABILITY_UNLOCK_MONK_COLORLESS` | |
| `ABILITY_UNLOCK_NECROMANCER` | |
| `ABILITY_UNLOCK_NECROMANCER_COLORLESS` | |
| `ABILITY_UNLOCK_PSYCHIC` | |
| `ABILITY_UNLOCK_PSYCHIC_COLORLESS` | |
| `ABILITY_UNLOCK_TANK` | |
| `ABILITY_UNLOCK_TANK_COLORLESS` | |
| `ABILITY_UNLOCK_THIEF` | |
| `ABILITY_UNLOCK_THIEF_COLORLESS` | |
| `ABILITY_UNLOCK_TINKERER` | |
| `ABILITY_UNLOCK_TINKERER_COLORLESS` | |
| `AREA_UNLOCK_BONEYARD` | |
| `AREA_UNLOCK_BUNKER` | |
| `AREA_UNLOCK_CAVES` | |
| `AREA_UNLOCK_CORE` | |
| `AREA_UNLOCK_CRATER` | |
| `AREA_UNLOCK_DESERT` | |
| `AREA_UNLOCK_ENDOFTIME` | |
| `AREA_UNLOCK_FUTURE` | |
| `AREA_UNLOCK_ICEAGE` | |
| `AREA_UNLOCK_JUNKYARD` | |
| `AREA_UNLOCK_JURASSIC` | |
| `AREA_UNLOCK_LAB` | |
| `AREA_UNLOCK_MEATWORLD` | |
| `AREA_UNLOCK_MEATWORLDFULL` | |
| `AREA_UNLOCK_MOON` | |
| `AREA_UNLOCK_SEWERS` | |
| `AREA_UNLOCK_THEEND` | |
| `CUTSCENE_GUILLOTINA_1` | |
| `CUTSCENE_GUILLOTINA_1_REMATCH` | |
| `CUTSCENE_GUILLOTINA_2` | |
| `CUTSCENE_GUILLOTINA_2_REMATCH` | |
| `CUTSCENE_GUILLOTINA_3` | |
| `CUTSCENE_GUILLOTINA_3_REMATCH` | |
| `CUTSCENE_KAIJUFIGHT` | |
| `CUTSCENE_KAIJUFIGHT_REMATCH` | |
| `CUTSCENE_OBELISK1_CORE_POPUP` | |
| `CUTSCENE_OBELISK1_MOON_POPUP` | |
| `CUTSCENE_PYROPHINA` | |
| `CUTSCENE_PYROPHINA_REMATCH` | |
| `CUTSCENE_TERMINATOR_1` | |
| `CUTSCENE_TERMINATOR_1_REMATCH` | |
| `CUTSCENE_TERMINATOR_2` | |
| `CUTSCENE_TERMINATOR_2_REMATCH` | |
| `CUTSCENE_TERMINATOR_3` | |
| `CUTSCENE_TERMINATOR_3_REMATCH` | |
| `CUTSCENE_ZARATANA` | |
| `CUTSCENE_ZARATANA_REMATCH` | |
| `EVENT_NEEDLES_AGAIN_QUES` | |
| `PASSIVE_UNLOCK_BUTCHER` | |
| `PASSIVE_UNLOCK_BUTCHER_COLORLESS` | |
| `PASSIVE_UNLOCK_COLORLESS` | |
| `PASSIVE_UNLOCK_COLORLESS_COLORLESS` | |
| `PASSIVE_UNLOCK_DRUID` | |
| `PASSIVE_UNLOCK_DRUID_COLORLESS` | |
| `PASSIVE_UNLOCK_FIGHTER` | |
| `PASSIVE_UNLOCK_FIGHTER_COLORLESS` | |
| `PASSIVE_UNLOCK_HUNTER` | |
| `PASSIVE_UNLOCK_HUNTER_COLORLESS` | |
| `PASSIVE_UNLOCK_JESTER` | |
| `PASSIVE_UNLOCK_JESTER_COLORLESS` | |
| `PASSIVE_UNLOCK_MAGE` | |
| `PASSIVE_UNLOCK_MAGE_COLORLESS` | |
| `PASSIVE_UNLOCK_MEDIC` | |
| `PASSIVE_UNLOCK_MEDIC_COLORLESS` | |
| `PASSIVE_UNLOCK_MONK` | |
| `PASSIVE_UNLOCK_MONK_COLORLESS` | |
| `PASSIVE_UNLOCK_NECROMANCER` | |
| `PASSIVE_UNLOCK_NECROMANCER_COLORLESS` | |
| `PASSIVE_UNLOCK_PSYCHIC` | |
| `PASSIVE_UNLOCK_PSYCHIC_COLORLESS` | |
| `PASSIVE_UNLOCK_TANK` | |
| `PASSIVE_UNLOCK_TANK_COLORLESS` | |
| `PASSIVE_UNLOCK_THIEF` | |
| `PASSIVE_UNLOCK_THIEF_COLORLESS` | |
| `PASSIVE_UNLOCK_TINKERER` | |
| `PASSIVE_UNLOCK_TINKERER_COLORLESS` | |
| `QEVENT_BROKENTIMEMACHINE_QUES` | |
| `QEVENT_BROKENTIMEMACHINE_REW2` | |
| `QEVENT_BROKENTIMEMACHINE_REW3` | |
| `QEVENT_BROKENTIMEMACHINE_REW4` | |
| `QEVENT_BROKENTIMEMACHINE_REW5` | |
| `QEVENT_DEADGOD_QUES` | |
| `QEVENT_DEADGOD_REW1` | |
| `QEVENT_DEADGOD_REW2` | |
| `QEVENT_DEADGOD_REW3` | |
| `QEVENT_DEADKING_QUES` | |
| `QEVENT_DEADKING_REW1` | |
| `QEVENT_DEADKING_REW2` | |
| `QEVENT_DEADKING_REW3` | |
| `QEVENT_DEADKING_REW4` | |
| `QEVENT_DEADKING_REW5` | |
| `QEVENT_DIMENSIONXPORTAL_ENTER_REW` | |
| `QEVENT_DIMENSIONXPORTAL_IGNORE_ANSW` | |
| `QEVENT_DIMENSIONXPORTAL_QUES` | |
| `QEVENT_GLOWINGORB_QUES` | |
| `QEVENT_GLOWINGORB_QUES2` | |
| `QEVENT_GLOWINGORB_REW1` | |
| `QEVENT_GLOWINGORB_REW2` | |
| `QEVENT_GLOWINGORB_REW3` | |
| `QEVENT_GLOWINGORB_REW4` | |
| `QEVENT_GLOWINGORB_REW5` | |
| `QEVENT_GLOWINGORB_REW6` | |
| `QEVENT_GLOWINGORB_REW7` | |
| `QEVENT_MEATALTAR_QUES1` | |
| `QEVENT_MEATALTAR_REW1` | |
| `QEVENT_MEATALTAR_REW2` | |
| `QEVENT_MEATALTAR_REW2B` | |
| `QEVENT_MEATALTAR_REW3` | |
| `QEVENT_MEATALTAR_REW3B` | |
| `QEVENT_MEATALTAR_REW_IGNORE` | |
| `QEVENT_OBELISK_CORE_REW_ZARA1` | |
| `QEVENT_OBELISK_CORE_REW_ZARA2` | |
| `QEVENT_OBELISK_CORE_REW_ZARA3` | |
| `QEVENT_OBELISK_MOON_REW_PYRO1` | |
| `QEVENT_OBELISK_MOON_REW_PYRO2` | |
| `QEVENT_OBELISK_MOON_REW_PYRO3` | |
| `QEVENT_OBELISK_QUES3` | |
| `QEVENT_THEHEAD_QUES` | |
| `QEVENT_THEHEAD_REW1` | |
| `QEVENT_THEHEAD_REW2` | |
| `QEVENT_THEHEAD_REW3` | |
| `QEVENT_THEHEAD_REW4` | |
| `QEVENT_THEHEAD_REW5` | |
| `QEVENT_THEHEAD_REW6` | |
| `QEVENT_THROBBINGARTERY2_QUES` | |
| `QEVENT_THROBBINGARTERY2_REW_IGNORE` | |
| `QEVENT_THROBBINGARTERY_QUES1` | |
| `QEVENT_THROBBINGARTERY_QUES2` | |
| `QEVENT_THROBBINGARTERY_REW5` | |
| `QEVENT_THROBBINGARTERY_REW6` | |
| `QEVENT_THROBBINGARTERY_REW_IGNORE` | |
| `QEVENT_TIMEMACHINE_FUTURE_QUES` | |
| `QEVENT_TIMEMACHINE_FUTURE_REW1` | |
| `QEVENT_TIMEMACHINE_FUTURE_REW2` | |
| `QEVENT_TIMEMACHINE_ICEAGE_QUES` | |
| `QEVENT_TIMEMACHINE_ICEAGE_REW1` | |
| `QEVENT_TIMEMACHINE_ICEAGE_REW2` | |
| `QEVENT_TIMEMACHINE_JURASSIC_QUES` | |
| `QEVENT_TIMEMACHINE_JURASSIC_REW1` | |
| `QEVENT_TIMEMACHINE_JURASSIC_REW2` | |
| `QEVENT_TIMEMACHINE_QUES` | |
| `QEVENT_TIMEMACHINE_REW1` | |
| `QEVENT_TIMEMACHINE_REW2` | |
| `QEVENT_TIMEMACHINE_REW3` | |
| `QEVENT_TIMEMACHINE_THEEND_QUES` | |
| `QEVENT_TIMEMACHINE_THEEND_REW1` | |
| `QEVENT_TIMEMACHINE_THEEND_REW2` | |
| `QEVENT_VOLCANO_QUES` | |
| `QEVENT_VOLCANO_QUES2` | |
| `QEVENT_VOLCANO_REW4` | |
| `QEVENT_VOLCANO_REW5` | |
| `QEVENT_VOLCANO_REW6` | |
| `QEVENT_VOLCANO_REW7` | |
| `QEVENT_WALLOFFLESH2_QUES` | |
| `QEVENT_WALLOFFLESH2_REW_IGNORE` | |
| `QEVENT_WALLOFFLESH_QUES1` | |
| `QEVENT_WALLOFFLESH_QUES2` | |
| `QEVENT_WALLOFFLESH_REW1` | |
| `QEVENT_WALLOFFLESH_REW10` | |
| `QEVENT_WALLOFFLESH_REW2` | |
| `QEVENT_WALLOFFLESH_REW3` | |
| `QEVENT_WALLOFFLESH_REW4` | |
| `QEVENT_WALLOFFLESH_REW5` | |
| `QEVENT_WALLOFFLESH_REW6` | |
| `QEVENT_WALLOFFLESH_REW7` | |
| `QEVENT_WALLOFFLESH_REW8` | |
| `QEVENT_WALLOFFLESH_REW9` | |
| `QEVENT_WALLOFFLESH_REW_IGNORE` | |
| `QUEST_BEGIN_AMPLIFIER` | |
| `QUEST_BEGIN_BLACKSHARD` | |
| `QUEST_BEGIN_COOLER` | |
| `QUEST_BEGIN_GUILLOTINASHEAD` | |
| `QUEST_BEGIN_JAR` | |
| `QUEST_BEGIN_NUKE` | |
| `QUEST_BEGIN_PUTRIDLEECH` | |
| `QUEST_BEGIN_PYROPHINASCOLLAR` | |
| `QUEST_BEGIN_RECEIVER` | |
| `QUEST_BEGIN_SCALDINGORB` | |
| `QUEST_BEGIN_THROBBINGGRISTLE` | |
| `QUEST_BEGIN_TRANSMITTER` | |
| `QUEST_BEGIN_ZARATANASCOLLAR` | |
| `SONG_UNLOCK_ALLEY` | |
| `SONG_UNLOCK_BONEYARD` | |
| `SONG_UNLOCK_BUNKER` | |
| `SONG_UNLOCK_CAVES` | |
| `SONG_UNLOCK_CHAOS_BACKWARD` | |
| `SONG_UNLOCK_CHAOS_FORWARD` | |
| `SONG_UNLOCK_CORE` | |
| `SONG_UNLOCK_CRATER` | |
| `SONG_UNLOCK_CREDITS_1` | |
| `SONG_UNLOCK_CREDITS_2` | |
| `SONG_UNLOCK_DESERT` | |
| `SONG_UNLOCK_DIMENSIONX` | |
| `SONG_UNLOCK_FINALBOSS` | |
| `SONG_UNLOCK_FUTURE` | |
| `SONG_UNLOCK_GUILLOTINA` | |
| `SONG_UNLOCK_HITLERIII` | |
| `SONG_UNLOCK_ICEAGE` | |
| `SONG_UNLOCK_JUNKYARD` | |
| `SONG_UNLOCK_JURASSIC` | |
| `SONG_UNLOCK_KAIJUS` | |
| `SONG_UNLOCK_LAB` | |
| `SONG_UNLOCK_MEATWORLD` | |
| `SONG_UNLOCK_MOON` | |
| `SONG_UNLOCK_SEWERS` | |
| `SONG_UNLOCK_TERMINATOR` | |
| `SONG_UNLOCK_THEEND` | |
| `SONG_UNLOCK_THEINFINITE` | |
| `SONG_UNLOCK_THROBBINGKING` | |

</details>


---

### Enum: `restrictions`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `none` | |
| `aoe_must_exist` | |
| `must_have_line_of_sight` | |
| `must_be_moveable` | |
| `must_be_empty` | |
| `must_have_character` | |
| `must_have_tag` | |
| `must_have_destructible_corpse` | |
| `must_match_locked_orientation` | |
| `aoe_must_be_displaceable` | |
| `must_have_ally` | |
| `must_have_enemy` | |
| `must_target_alpha_if_exists` | |
| `cant_target_behind` | |
| `diagonal_only` | |
| `must_fit_2x2_character` | |
| `must_have_buddy` | |
| `must_have_familiar` | |
| `aoe_must_be_force_displaceable` | |
| `must_be_movable_ignore_trample` | |
| `must_have_animate_character` | |
| `must_have_cat` | |
| `must_match_current_orientation` | |
| `require_empty_tile_in_front` | |
| `dash_must_move` | |
| `must_be_moveable_ignore_wall` | |
| `must_be_swappable` | |
| `must_fit_2x2` | |
| `must_have_line_of_sight_unpurgable` | |
| `must_have_liquid` | |

</details>


---

### Enum: `knockback_mode`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `character_to_tile` | |
| `zero` | |
| `none` | |
| `orientation` | |
| `tile_to_character` | |
| `pull_to_character` | |
| `character_to_target` | |
| `back_orientation` | |
| `target_to_character` | |
| `target_to_tile` | |
| `character_to_tile_4snap` | |
| `perp_towards_facing` | |
| `perp_towards_facing_middle_pull` | |
| `tile_to_character_4snap` | |
| `tile_to_target` | |
| `to_map_center` | |
| `pull_to_character_plus1` | |
| `random` | |
| `right_orientation` | |

</details>


---

### Enum: `projectile`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `source_weapon` | |
| `Bullet` | |
| `MagicMissileProjectile` | |
| `ArrowProjectile` | |
| `SmallRock` | |
| `BoneProjectile` | |
| `LeechProjectile` | |
| `HookProjectile` | |
| `DamageTrap` | |
| `GlassBall` | |
| `Creepball` | |
| `CupidsArrowProjectile` | |
| `None` | |
| `Projectile` | |
| `Projectile_Rocket` | |
| `WebTrap` | |
| `spitprojectile` | |
| `BrambleProjectile` | |
| `LavaBall` | |
| `LightningBallProjectile` | |
| `LobbedProjectile` | |
| `MaggotBall` | |
| `SpiderBall` | |
| `AcidshotProjectile` | |
| `Dip` | |
| `FireBallProjectile` | |
| `Froghook` | |
| `MagicSpikeProjectile` | |
| `NeedleProjectile` | |
| `Poisonball` | |
| `PukeBall` | |
| `Snowball` | |
| `SpikeProjectile` | |
| `Tarshot` | |
| `Webball` | |
| `AnimalEgg` | |
| `ArmorPickup` | |
| `BabySpider` | |
| `Bomb` | |
| `Bottleshot` | |
| `Boulder` | |
| `Bramblehook` | |
| `ChakramProjectile` | |
| `CharmTrap` | |
| `CoinProjectile` | |
| `Default` | |
| `EggSackTrap` | |
| `FinalBossShieldProjectile` | |
| `FireProjectile` | |
| `Firecracker` | |
| `Fishball` | |
| `Flea` | |
| `Foodball` | |
| `Gutball` | |
| `Harpoon` | |
| `HemlockFetus` | |
| `IcecubeParticle` | |
| `Joystick` | |
| `Maggot` | |
| `MagicMissileProjectileSmall` | |
| `Meatball` | |
| `Meteorball` | |
| `Pebble` | |
| `SpearProjectile` | |
| `Spidershot` | |
| `SpikeTrap` | |
| `Tumorball` | |
| `barbedwire` | |
| `bounceshot` | |
| `bubbleshot` | |
| `knifeprojectile` | |
| `source_trinket` | |

</details>


---

### Enum: `cat_choice`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`intro`](./Events_and_Encounters.md#context-intro)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `random` | |

</details>


---

### Enum: `event_clip`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`intro`](./Events_and_Encounters.md#context-intro)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `NonWheelEvent` | |

</details>


---

### Enum: `subject_clip`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`intro`](./Events_and_Encounters.md#context-intro)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `EventSubject` | |

</details>


---

### Enum: `subject_frame`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`intro`](./Events_and_Encounters.md#context-intro)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `unknown` | |
| `timemachine_fixed` | |
| `butch` | |
| `genie` | |
| `mysterious_machine` | |
| `beanies` | |
| `blessing` | |
| `body_of_glorg` | |
| `eliphants_foot_closer` | |
| `frank` | |
| `jagged_pathway` | |
| `monkey_paw_4fingers` | |
| `mysterious_stranger` | |
| `obelisk` | |
| `obelisk_glowing` | |
| `obelisk_raised` | |
| `tink` | |
| `watching_head` | |
| `a_beggar` | |
| `a_few_coins` | |
| `a_large_poop` | |
| `a_mega_large_poop` | |
| `a_poop` | |
| `a_puzzle_box` | |
| `a_rock` | |
| `a_small_pile_of_stones` | |
| `ball_of_cancer` | |
| `ballofflesh` | |
| `baphomet` | |
| `barbed_wire_fence` | |
| `bear_trap` | |
| `big_toe` | |
| `blood_stain` | |
| `bonepile` | |
| `bottle_of_viper_booze` | |
| `bottleofliquid` | |
| `box_with_a_hole` | |
| `boxmonster` | |
| `broken_canister` | |
| `broken_tv` | |
| `brokenwindow` | |
| `cat_bed` | |
| `cathole` | |
| `catorgy` | |
| `catpelts` | |
| `clam` | |
| `clogged_pipes` | |
| `coffin` | |
| `computer_console` | |
| `crack_in_the_earth` | |
| `crack_in_the_wall` | |
| `crashed_object` | |
| `crate` | |
| `crater_weather` | |
| `dark_den` | |
| `dead_god` | |
| `dead_king` | |
| `dead_mammoth` | |
| `deadcat` | |
| `deadrat` | |
| `death` | |
| `decaying_carcass` | |
| `demonic_idol` | |
| `dimensionx_head` | |
| `dimensionx_portal` | |
| `dumpster` | |
| `dust_storm` | |
| `dying_fetus` | |
| `eliphants_foot` | |
| `endorb` | |
| `fetus` | |
| `fountain` | |
| `frozen_humanoid` | |
| `fruit_basket` | |
| `giant_sleeping_shark` | |
| `grating_in_the_floor` | |
| `gutspile` | |
| `hairball` | |
| `happening` | |
| `head_in_a_tire` | |
| `hole_in_the_earth` | |
| `hollow_skull` | |
| `human_skin` | |
| `jack` | |
| `knife_in_the_wall` | |
| `locked_crate` | |
| `locked_trunk` | |
| `lockeddoor` | |
| `locket` | |
| `meat_golem` | |
| `meat_leaking` | |
| `meatworld_altar` | |
| `meteor` | |
| `mirage` | |
| `mirror` | |
| `monkey_paw_1finger` | |
| `monkey_paw_2fingers` | |
| `monkey_paw_3fingers` | |
| `mouse_nest` | |
| `mousetrap` | |
| `mummified_corpse` | |
| `mushroom` | |
| `mysterious_building` | |
| `mysterious_cave` | |
| `mysterious_cave_climb` | |
| `mysterious_cave_glowing_one` | |
| `mysterious_cave_hole` | |
| `mysterious_chamber` | |
| `mysterious_crater` | |
| `mysterious_creature` | |
| `mysterious_jar` | |
| `mysterious_manual` | |
| `mysterious_obelisk` | |
| `mysterious_tent` | |
| `mysterious_tomb_door` | |
| `mysterious_tomb_enter` | |
| `mysterious_tomb_mummy` | |
| `mysterious_tomb_sarcophagus` | |
| `mysterious_tomb_stairs` | |
| `mysteriousstain` | |
| `needles` | |
| `nest_of_eggs` | |
| `oasis` | |
| `odd_device` | |
| `old_can` | |
| `ominous_sign` | |
| `organgrinder` | |
| `pile_of_skulls` | |
| `pill_bottle` | |
| `pinata` | |
| `pit_of_snakes` | |
| `racy_magazine` | |
| `ratmob` | |
| `rotten_meat` | |
| `safe` | |
| `sealed_crypt` | |
| `severedhead` | |
| `shiny_thing_in_pool` | |
| `small_bird` | |
| `small_black_hole` | |
| `smelly_bag` | |
| `spiderwebs` | |
| `spookieapparation` | |
| `stacy_buff` | |
| `stacy_element` | |
| `stacy_special` | |
| `stacy_stats` | |
| `start_digging` | |
| `steven_fetus` | |
| `strange_flowers` | |
| `straycat` | |
| `strong_current` | |
| `stuck_corpse` | |
| `tall_grass` | |
| `tallfence` | |
| `tape_recorder` | |
| `tar_pits` | |
| `throbbing_artery` | |
| `throbbing_artery2` | |
| `time_capsule` | |
| `timemachine_broken` | |
| `toxicwastevat` | |
| `tracy` | |
| `tragedy` | |
| `trash_bags` | |
| `trashcan` | |
| `traverse_necropolis` | |
| `tuna_can` | |
| `unmarked_grave` | |
| `use_the_toilet` | |
| `vending_machine` | |
| `vibrating_meteor` | |
| `volcano` | |
| `wall_of_cats` | |
| `wall_of_flesh` | |
| `wall_of_flesh2` | |
| `watchingeyeballs` | |
| `weird_egg` | |
| `whispering_from_darkness` | |
| `white_rabbit` | |
| `womans_purse` | |
| `writhing_pile_of_maggots` | |

</details>


---

### Enum: `voice`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Custom_Cats.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `male4` | |
| `male1` | |
| `male2` | |
| `female43` | |
| `none` | |
| `female2` | |
| `male3` | |
| `male7` | |
| `male8` | |
| `female29` | |
| `male9` | |
| `sabertoothcat` | |
| `female1` | |
| `female12` | |
| `female3` | |
| `female30` | |
| `female6` | |
| `male19` | |
| `male29` | |
| `male5` | |
| `male51` | |
| `male6` | |
| `male70` | |
| `male79` | |
| `male80` | |
| `ankylosaurus` | |
| `female10` | |
| `female26` | |
| `female4` | |
| `female5` | |
| `female7` | |
| `female9` | |
| `futurebot` | |
| `male11` | |
| `male13` | |
| `mammothbaby` | |
| `parasaurolophus` | |
| `poopcat` | |
| `raptor` | |
| `raptorbaby` | |
| `robotom` | |
| `scorpioncat` | |
| `terminator_boss` | |
| `wolfcat` | |
| `yeticat` | |
| `female17` | |
| `female39` | |
| `female45` | |
| `male102` | |
| `male21` | |
| `male26` | |
| `male37` | |
| `male46` | |
| `male52` | |
| `male55` | |
| `male60` | |
| `male83` | |
| `male89` | |
| `male95` | |
| `spidercat` | |

</details>


---

### Enum: `do`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonusturn_pattern`](./Characters_and_Bosses.md#context-bonusturn_pattern), [`dispersed_bonusturn_pattern`](./Characters_and_Bosses.md#context-dispersed_bonusturn_pattern), [`fallback`](./Characters_and_Bosses.md#context-fallback), [`mainturn_pattern`](./Characters_and_Bosses.md#context-mainturn_pattern), [`pattern`](./Characters_and_Bosses.md#context-pattern), [`round_end_bonusturn_pattern`](./Characters_and_Bosses.md#context-round_end_bonusturn_pattern)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |
| `move` | |
| `**SimonFlopper_WiggleChance` | |
| `**SimonFlopper_WiggleFake` | |
| `Magnetize` | |
| `SpreadX` | |
| `JohnnyCryOne` | |
| `**BombRatTurtle` | |
| `**SimonFlopper_WiggleGuaranteed` | |
| `**TrampleDash` | |
| `*SpawnBomb` | |
| `*ZaratanaVSExitTurtle` | |
| `*attack` | |
| `ChainDash` | |
| `JohnnyBlast` | |
| `RockToss_ColorlessCat_AsCloseAsPossible` | |
| `SpearPoke` | |
| `YeetTowardsBuddy` | |
| `none` | |
| `weapon` | |
| `**G3Shake` | |
| `**RockySlam` | |
| `**ThumpSlam` | |
| `**ZaratanaSoloSpinDash` | |
| `*AtomicBurst` | |
| `*BellyPound` | |
| `*Digest` | |
| `*Flush` | |
| `*G3Scream_Hex` | |
| `*LEBurst` | |
| `*MM_Unguard` | |
| `*NubsNuke` | |
| `*SBotRecharge` | |
| `*SpawnJunk` | |
| `*T3Intro` | |
| `*TKNG_Trash` | |
| `*TinaSpit` | |
| `*YA_Charge` | |
| `AZ_Jump` | |
| `BHoleSuck` | |
| `BearTrap_Enemy` | |
| `BearTrap_Enemy_Cantrip` | |
| `BumblefootBoneShot` | |
| `BumblefootLeap` | |
| `CerberubsThrow` | |
| `CovenRise1` | |
| `CovenSummon` | |
| `CutterCut` | |
| `DbgBackgroundTransitionTest` | |
| `Dclaude_Declaw` | |
| `DustDash` | |
| `FatLeap` | |
| `G3CallForHelp` | |
| `G3TossHead` | |
| `GirlDinoThrow` | |
| `GlowingMushroomGiveMana` | |
| `GlowingMushroomGiveMana2` | |
| `GrenadeExplode` | |
| `HammerSmash` | |
| `HealSelf` | |
| `HitlerNuke` | |
| `JohnnyCryTwo` | |
| `JohnnyMegaBlast` | |
| `JohnnyMindControl` | |
| `KillDoze` | |
| `KirbySuck` | |
| `LennyHug` | |
| `MCKineticCharge` | |
| `MD_HeadLeave` | |
| `MD_Poop` | |
| `MegaGuppy_SlamLeft` | |
| `MegaGuppy_SlamRight` | |
| `MoonHead_BeginCharge` | |
| `MoonHead_Blow` | |
| `MoonHead_ChewCat` | |
| `PokerPokeAlly` | |
| `QueenHippoAttack` | |
| `RallyMaggots` | |
| `SM_MagicMissile` | |
| `ScorpionHold` | |
| `SharkDash` | |
| `SimonFlopper_Tentacle` | |
| `Simon_Tentacle` | |
| `Simon_Trash` | |
| `SirenCall` | |
| `SmallTrampleDash` | |
| `Spin_Enemy` | |
| `SuckMF` | |
| `TKNG_Spawn` | |
| `TallBotRocket` | |
| `TinaBodySlamRage` | |
| `TinaTantrum` | |
| `TrampyDump` | |
| `TrampyFleas` | |
| `TrampySleep` | |
| `TrampySpit` | |
| `TriceratopsTrample` | |
| `UFO_BigShield` | |
| `WolfLeap` | |
| `XLightning` | |
| `YetiIceBreath` | |

</details>


---

### Enum: `get_item_from_pool`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`10coins`](./Events_and_Encounters.md#context-10coins), [`5coins`](./Events_and_Encounters.md#context-5coins), [`ROOT`](./Events_and_Encounters.md#context-root), [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`options`](./Events_and_Encounters.md#context-options), [`random_chance`](./Events_and_Encounters.md#context-random_chance), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `consumables` | |
| `chapter_rare` | |
| `bone_equipment` | |
| `food` | |
| `chapter_common` | |
| `blood_altar_items` | |
| `fleshhead_items` | |
| `junkyard_items` | |
| `poop_items` | |
| `treasure_easy` | |
| `bone_armor` | |
| `chapter` | |
| `chapter_specific_item` | |
| `flesh_items` | |
| `pills` | |
| `rat_trinkets` | |
| `Coin_items` | |
| `any_chapter` | |
| `deadcat_equipment` | |
| `raptor_nest_eggs` | |
| `rock_items` | |
| `tech_items` | |
| `Bird_items` | |
| `grass_items` | |
| `grub_armor` | |
| `hide_items` | |
| `isaac_items` | |
| `rare` | |
| `Eye_items` | |
| `barbed_items` | |
| `bloody_items` | |
| `bone_weapons` | |
| `can_items_common` | |
| `can_items_rare` | |
| `cat_armor` | |
| `demon_themed_items` | |
| `eyes_nonrare` | |
| `glitched_items` | |
| `godly_items` | |
| `guts_items` | |
| `meat_items` | |
| `mom_items` | |
| `recycled_items` | |
| `rotten_armor` | |
| `unique` | |

</details>


---

### Enum: `frame`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`popup`](./Progression_Unlocks.md#context-popup)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `UnlockItem` | |
| `QuestUnlock_KaijuCollar` | |
| `UnlockArea_Meatworld` | |
| `UnlockArea_Rift` | |
| `QuestUnlock_Amplifier` | |
| `QuestUnlock_Cooler` | |
| `QuestUnlock_Gristle` | |
| `QuestUnlock_Head` | |
| `QuestUnlock_Jar` | |
| `QuestUnlock_Leech` | |
| `QuestUnlock_Nuke` | |
| `QuestUnlock_Orb` | |
| `QuestUnlock_Receiver` | |
| `QuestUnlock_Shard` | |
| `QuestUnlock_Transmitter` | |
| `UnlockArea_Boneyard` | |
| `UnlockArea_Bunker` | |
| `UnlockArea_Caves` | |
| `UnlockArea_Core` | |
| `UnlockArea_Crater` | |
| `UnlockArea_Desert` | |
| `UnlockArea_Future` | |
| `UnlockArea_IceAge` | |
| `UnlockArea_Infinite` | |
| `UnlockArea_Junkyard` | |
| `UnlockArea_Jurassic` | |
| `UnlockArea_Lab` | |
| `UnlockArea_Moon` | |
| `UnlockArea_Sewers` | |
| `UnlockArea_TheEnd` | |

</details>


---

### Enum: `max_range`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `5+bonus_range` | |
| `4+bonus_range` | |
| `mov` | |
| `3+bonus_range` | |
| `1+bonus_range` | |
| `7+bonus_range` | |
| `X` | |
| `2+bonus_range` | |
| `level` | |
| `5+2*level` | |
| `6+bonus_range` | |
| `8+bonus_range` | |
| `X*2` | |
| `X+1` | |
| `1+X` | |
| `1+X*2` | |
| `1+bonus_melee_range` | |
| `2*X` | |
| `2+level` | |
| `3+2*level` | |
| `5+level` | |
| `X*3` | |
| `mov*2` | |

</details>


---

### Enum: `aoe_restrictions`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `none` | |
| `must_have_line_of_sight_unpurgable` | |
| `enemies_only` | |
| `must_have_destructible_corpse` | |
| `must_have_line_of_sight` | |
| `must_have_corpse` | |
| `familiars_only` | |
| `must_have_piercing_line_of_sight` | |
| `exclude_allies` | |
| `must_have_animate_character` | |
| `allies_only` | |
| `must_have_cat_with_empty_weapon_slot` | |
| `must_be_empty` | |
| `must_have_tag` | |
| `checker_parity_even` | |
| `must_have_aggro_target` | |
| `must_have_low_health_character` | |
| `exclude_direct_target` | |
| `must_backstab` | |
| `must_be_displaceable` | |
| `must_have_cat` | |
| `must_have_corpse_or_sleeping` | |
| `must_have_living_character` | |
| `must_have_special_tag` | |
| `must_have_target_line_of_sight` | |
| `tile_must_have_element` | |

</details>


---

### Enum: `status`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasStatus`](./Abilities_and_Spells.md#context-conditional_hasstatus), [`Conditional_SourceHasStatus`](./Abilities_and_Spells.md#context-conditional_sourcehasstatus), [`RemoveStatusStacks`](./Abilities_and_Spells.md#context-removestatusstacks), [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#context-temppassivewhilehasstatus), [`Temporary`](./Abilities_and_Spells.md#context-temporary), [`PassiveWhileHasStatus`](./Cat_Mutations.md#context-passivewhilehasstatus), [`FormChangeWhileHasStatus`](./Characters_and_Bosses.md#context-formchangewhilehasstatus), [`PassiveWhileHasStatus`](./Characters_and_Bosses.md#context-passivewhilehasstatus), [`PassiveWhileNotHasStatus`](./Characters_and_Bosses.md#context-passivewhilenothasstatus), [`RemoveStatusStacks`](./Characters_and_Bosses.md#context-removestatusstacks), [`StatusEachTurnBeginIfHasStatus`](./Characters_and_Bosses.md#context-statuseachturnbeginifhasstatus), [`StatusWhenStatusCompletelyRemoved`](./Characters_and_Bosses.md#context-statuswhenstatuscompletelyremoved), [`TerminatorSkin`](./Characters_and_Bosses.md#context-terminatorskin), [`TransformOnStatusThreshold`](./Characters_and_Bosses.md#context-transformonstatusthreshold), [`UseAbilityWhenOutOfStatus`](./Characters_and_Bosses.md#context-useabilitywhenoutofstatus), [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus), [`RemoveStatusStacks`](./Items_and_Equipment.md#context-removestatusstacks), [`Temporary`](./Items_and_Equipment.md#context-temporary), [`AmplifyStatus`](./Passives_and_Statuses.md#context-amplifystatus), [`Conditional_HasStatus`](./Passives_and_Statuses.md#context-conditional_hasstatus), [`Temporary`](./Passives_and_Statuses.md#context-temporary)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Consuming` | |
| `Brace` | |
| `Thorns` | |
| `Petrify` | |
| `Bleed` | |
| `LuckUp` | |
| `AllStatsUp` | |
| `Uncontrollable` | |
| `AlphaCat` | |
| `KineticSpikes` | |
| `BleedThorns` | |
| `Counterspell` | |
| `DamageUp` | |
| `DemonicGlyph_Movement` | |
| `Freeze` | |
| `Marked` | |
| `MeleeRangeUp` | |
| `Sleep` | |
| `SpeedUp` | |
| `StrengthUp` | |
| `AddKnockbackToEverything` | |
| `AllDamageCrits` | |
| `AllDamageImmune` | |
| `BackflipWhenTargeted` | |
| `Burn` | |
| `ChainKnockback` | |
| `Confusion` | |
| `Consumed` | |
| `DemonicGlyph_Bite` | |
| `DemonicGlyph_Bounce` | |
| `DemonicGlyph_Fire` | |
| `DemonicGlyph_Summon` | |
| `DodgeChance_Status` | |
| `DybbukManualExitTag` | |
| `ExistUntilIdleUpkeep` | |
| `Fear` | |
| `FreeSpell` | |
| `Grappling` | |
| `Madness` | |
| `MaxAccuracy` | |
| `Poison` | |
| `T2CopyCatInternal` | |
| `Trample` | |
| `Undead` | |

</details>


---

### Enum: `custom_cat_data`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SkeletonCat` | |
| `GunCat` | |
| `RoboTom` | |
| `Stacy2p0` | |
| `TallSkeletonCat` | |
| `ZombieCat` | |
| `AlbinoTomTom` | |
| `AngelicCat` | |
| `Ankylosaurus` | |
| `Astro` | |
| `AtomicKitten` | |
| `BabyCat` | |
| `Beaver` | |
| `Belcher` | |
| `Bigfoot` | |
| `BoomerCat` | |
| `Bunny` | |
| `ButcherCat` | |
| `ButcherCat_Terminator` | |
| `CancerCat` | |
| `CatCaller` | |
| `CatCultist` | |
| `Chupacabra` | |
| `CollectiveCat` | |
| `CoreFreak` | |
| `DaddyCat` | |
| `Dclaude` | |
| `DemonHooker` | |
| `Dog` | |
| `Drcat` | |
| `DruidCat` | |
| `DruidCat_Terminator` | |
| `Edmund` | |
| `FatCat` | |
| `FighterCat` | |
| `FighterCat_Terminator` | |
| `FijiMermaid` | |
| `FutureBot` | |
| `GassyCat` | |
| `GlassSpitter` | |
| `GolemCat` | |
| `Grey` | |
| `Hellspawn1` | |
| `HornyCat` | |
| `HunterCat` | |
| `HunterCat_Terminator` | |
| `Hyde` | |
| `Infested` | |
| `InfestedDuo` | |
| `Isaac` | |
| `JackCat` | |
| `Jekyll` | |
| `JerseyDevil` | |
| `JesterCat` | |
| `JesterCat_Terminator` | |
| `Kitten` | |
| `LoanShark` | |
| `Maelestes` | |
| `MageCat` | |
| `MageCat_Terminator` | |
| `MammothBaby` | |
| `Mangy` | |
| `Mangy2` | |
| `Mangy3` | |
| `MedicCat` | |
| `MedicCat_Terminator` | |
| `MommyCat` | |
| `MonkCat` | |
| `MonkCat_Terminator` | |
| `Mothman` | |
| `NecroCat` | |
| `NecroCat_Terminator` | |
| `Needlecat` | |
| `Nessie` | |
| `NoHead` | |
| `Parasaurolophus` | |
| `Pebbles` | |
| `Pebbles_Terminator` | |
| `Pig` | |
| `PoopCat` | |
| `PopeyeCat` | |
| `Porcupine` | |
| `PsychicCat` | |
| `PsychicCat_Terminator` | |
| `Raptor` | |
| `RaptorBaby` | |
| `RockHead` | |
| `Rover` | |
| `SabertoothCat` | |
| `SabertoothCub` | |
| `ScorpionCat` | |
| `ShadeCat` | |
| `SharkyCat` | |
| `Siren` | |
| `Skinned` | |
| `Skunk` | |
| `Slenderman` | |
| `Sonichu` | |
| `SpiderCat` | |
| `SpikedCat` | |
| `StacyX` | |
| `StemCat` | |
| `TallSpiderCat` | |
| `TankCat` | |
| `TankCat_Terminator` | |
| `Terminator2Cat` | |
| `TerminatorCat` | |
| `ThiefCat` | |
| `ThiefCat_Terminator` | |
| `TinkererCat` | |
| `TinkererCat_Terminator` | |
| `Toadie` | |
| `TomTom` | |
| `TrailerCat` | |
| `Tyler` | |
| `WaterKitten` | |
| `WhiteRabbit` | |
| `WolfCat` | |
| `Yeticat` | |

</details>


---

### Enum: `unlock_item_immediate`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AnointingOil` | |
| `BagOfBags` | |
| `BagOfSeeds` | |
| `BallOfYarn` | |
| `BallPeenHammer` | |
| `BattleAxe` | |
| `BentSpoon` | |
| `Bo` | |
| `ButchersCleaver` | |
| `CambionConception` | |
| `CapAndBells` | |
| `CatCollar` | |
| `CatEars` | |
| `CatWhiskers` | |
| `ChildsCrown` | |
| `ClericHat` | |
| `ClericRelic` | |
| `ClericTears` | |
| `ClownMakeup` | |
| `Cookbook` | |
| `CopycatHat` | |
| `CopycatMask` | |
| `CopycatScarf` | |
| `CrownOfChaos` | |
| `DeathMask` | |
| `DivinersCloth` | |
| `DruidsWhistle` | |
| `EmptyHand` | |
| `FaceBrand` | |
| `FighterHelm` | |
| `FighterScar` | |
| `FighterShoulderPad` | |
| `Fireworks` | |
| `FleshShroud` | |
| `FriendshipBracelet` | |
| `Girder` | |
| `GreenmanMask` | |
| `HeadBrand` | |
| `HitlersToupe` | |
| `HolyWater` | |
| `HookedNecklace` | |
| `HunterCap` | |
| `HunterMonocle` | |
| `HunterQuiver` | |
| `HuntersFlute` | |
| `InfinityArrow` | |
| `IronJaw` | |
| `JokerCard` | |
| `LacedNeedle` | |
| `LeechNecklace` | |
| `LilKitty` | |
| `LiquidMetal` | |
| `LuckyCoinPurse` | |
| `MageHat` | |
| `MageRobe` | |
| `MageScarf` | |
| `MushroomHat` | |
| `MysticEye` | |
| `NinnyStick` | |
| `PrayerBeads` | |
| `PrayerCard` | |
| `PyrophinasToenail` | |
| `RageJuice` | |
| `RainStaff` | |
| `RingOfFrost` | |
| `RingOfMushrooms` | |
| `RoboticArm` | |
| `Ruffle` | |
| `SackOfMeat` | |
| `SatanicBible` | |
| `ScorchedEarth` | |
| `ScrapBag` | |
| `ScrappersBackpack` | |
| `ScrappersHat` | |
| `ScrappersMask` | |
| `SkillSplit` | |
| `SpellBook` | |
| `SpiderHat` | |
| `StaffOfFlame` | |
| `Steroids` | |
| `StevenHat1` | |
| `StevenHat2` | |
| `StevenMarrow` | |
| `StevenMask1` | |
| `StevenMask2` | |
| `StevenNeck1` | |
| `StevenNeck2` | |
| `StevenStone` | |
| `StevenTrinket1` | |
| `StevenTrinket2` | |
| `StevenWeapon1` | |
| `StevenWeapon2` | |
| `StevensBagofRocks` | |
| `StevensBottle` | |
| `StevensConsumable1` | |
| `StevensConsumable2` | |
| `StevensFartFace` | |
| `StevensFriend` | |
| `StevensGobbler` | |
| `StevensGristle` | |
| `StevensHat` | |
| `StevensHelmet` | |
| `StevensMustache` | |
| `StevensShotgun` | |
| `TankHelmet` | |
| `TankJuice` | |
| `TankPads` | |
| `TankTattoo` | |
| `TankToy` | |
| `TarotDeck` | |
| `TheBlackBox` | |
| `TheBox` | |
| `TheBoxCardboard` | |
| `TheBoxChest` | |
| `ThiefCloak` | |
| `ThiefHood` | |
| `ThiefTattoo` | |
| `ThrobbingCrown` | |
| `TinasBellyButton` | |
| `TinasFriend` | |
| `TinasLarynx` | |
| `TinfoilHat` | |
| `TinyCage` | |
| `TinyPebble` | |
| `ToyGun` | |
| `UnderworldStaff` | |
| `ZaratanaTurd` | |

</details>


---

### Enum: `range_mode`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cross` | |
| `standard` | |
| `8cross` | |
| `square` | |
| `custom` | |
| `diagcross` | |
| `normal` | |
| `none` | |
| `ground_move` | |
| `special_tagged_tiles` | |
| `last_targeted_tile` | |
| `map_edges` | |
| `water_move` | |

</details>


---

### Enum: `injury`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward), [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#context-passiveatinjurythreshold), [`StatusPerInjury`](./Passives_and_Statuses.md#context-statusperinjury)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `spd` | |
| `str` | |
| `random` | |
| `cha` | |
| `radiated` | |
| `con` | |
| `cursed` | |
| `int` | |
| `lck` | |
| `bleeding` | |
| `burned` | |
| `dex` | |

</details>


---

### Enum: `pool`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Craft`](./Abilities_and_Spells.md#context-craft), [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#context-destroyequipmentandattachparasite), [`EvolveAbilityFromPool`](./Abilities_and_Spells.md#context-evolveabilityfrompool), [`FindItemFromPool`](./Abilities_and_Spells.md#context-finditemfrompool), [`GainDisorderFromPool`](./Characters_and_Bosses.md#context-gaindisorderfrompool), [`get_item_from_pool`](./Events_and_Encounters.md#context-get_item_from_pool), [`Craft`](./Items_and_Equipment.md#context-craft), [`Craft`](./Passives_and_Statuses.md#context-craft), [`FindItemFromPool`](./Passives_and_Statuses.md#context-finditemfrompool), [`RepressedMemoriesMetronome`](./Passives_and_Statuses.md#context-repressedmemoriesmetronome), [`Item`](./Shops.md#context-item)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `chapter_common` | |
| `chapter_rare` | |
| `tinkerer_default` | |
| `chapter` | |
| `rare` | |
| `shop_common` | |
| `bombs` | |
| `current_chapter_rare` | |
| `Psychic` | |
| `eyes_nonrare` | |
| `parasites` | |
| `tracy_houseshop_common` | |
| `tracy_houseshop_common_item` | |
| `tracy_houseshop_item` | |
| `tracy_houseshop_rare` | |
| `Butcher` | |
| `Druid` | |
| `Fighter` | |
| `Hunter` | |
| `Jester` | |
| `JesterMinusColorless` | |
| `Mage` | |
| `Medic` | |
| `Monk` | |
| `Necromancer` | |
| `Tank` | |
| `Thief` | |
| `Tinkerer` | |
| `allsticks` | |
| `any_chapter` | |
| `diseases` | |
| `pelts` | |
| `pills` | |
| `stick` | |
| `treasure_easy` | |
| `treasure_hard` | |

</details>


---

### Enum: `label`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`activate_p`](./Events_and_Encounters.md#context-activate_p), [`activate_z`](./Events_and_Encounters.md#context-activate_z), [`attach_amplifier`](./Events_and_Encounters.md#context-attach_amplifier), [`attach_antenna`](./Events_and_Encounters.md#context-attach_antenna), [`attach_leech`](./Events_and_Encounters.md#context-attach_leech), [`bite`](./Events_and_Encounters.md#context-bite), [`body`](./Events_and_Encounters.md#context-body), [`bribe`](./Events_and_Encounters.md#context-bribe), [`charm`](./Events_and_Encounters.md#context-charm), [`drink`](./Events_and_Encounters.md#context-drink), [`eat`](./Events_and_Encounters.md#context-eat), [`enter`](./Events_and_Encounters.md#context-enter), [`examine`](./Events_and_Encounters.md#context-examine), [`fiddle`](./Events_and_Encounters.md#context-fiddle), [`fight`](./Events_and_Encounters.md#context-fight), [`fill_jar`](./Events_and_Encounters.md#context-fill_jar), [`future`](./Events_and_Encounters.md#context-future), [`home`](./Events_and_Encounters.md#context-home), [`ignore`](./Events_and_Encounters.md#context-ignore), [`infinite`](./Events_and_Encounters.md#context-infinite), [`lick`](./Events_and_Encounters.md#context-lick), [`looks`](./Events_and_Encounters.md#context-looks), [`loot`](./Events_and_Encounters.md#context-loot), [`loot_heart`](./Events_and_Encounters.md#context-loot_heart), [`mind`](./Events_and_Encounters.md#context-mind), [`past`](./Events_and_Encounters.md#context-past), [`place_gristle`](./Events_and_Encounters.md#context-place_gristle), [`power`](./Events_and_Encounters.md#context-power), [`repair`](./Events_and_Encounters.md#context-repair), [`repair_quest`](./Events_and_Encounters.md#context-repair_quest), [`sacrifice_normal`](./Events_and_Encounters.md#context-sacrifice_normal), [`sacrifice_quest`](./Events_and_Encounters.md#context-sacrifice_quest), [`sneak`](./Events_and_Encounters.md#context-sneak), [`soul`](./Events_and_Encounters.md#context-soul), [`take_blood`](./Events_and_Encounters.md#context-take_blood), [`talk`](./Events_and_Encounters.md#context-talk), [`touch`](./Events_and_Encounters.md#context-touch), [`wealth`](./Events_and_Encounters.md#context-wealth)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `EVENT_IGNORE_ANSW` | |
| `QEVENT_OBELISK_CORE_ACTIVATE_ANSW` | |
| `QEVENT_OBELISK_MOON_ACTIVATE_ANSW` | |
| `EVENT_SNEAKBY_ANSW` | |
| `QEVENT_TIMEMACHINE_HOME_ANSW` | |
| `QEVENT_OBELISK_CORE_TOUCH_ANSW` | |
| `QEVENT_OBELISK_MOON_TOUCH_ANSW` | |
| `EVENT_CHARM_ANSW` | |
| `EVENT_EXAMINE_ANSW` | |
| `EVENT_FIGHT_ANSW` | |
| `EVENT_REPAIR_ANSW` | |
| `QEVENT_MEATALTAR_SACRIFICE_ANSW` | |
| `QEVENT_THROBBINGARTERY_BITE_ANSW` | |
| `EVENT_BRIBE_ANSW` | |
| `EVENT_DRINK_ANSW` | |
| `EVENT_EAT_ANSW` | |
| `EVENT_GENIE_CHOICE_CURSEBODY` | |
| `EVENT_GENIE_CHOICE_CURSEMIND` | |
| `EVENT_GENIE_CHOICE_CURSESOUL` | |
| `EVENT_GENIE_CHOICE_LOOKS` | |
| `EVENT_GENIE_CHOICE_POWER` | |
| `EVENT_GENIE_CHOICE_WEALTH` | |
| `EVENT_LOOT_ANSW` | |
| `EVENT_RUN_ANSW` | |
| `EVENT_TALKTO_ANSW` | |
| `QEVENT_DEADKING_DRAINBLOOD_ANSW` | |
| `QEVENT_DEADKING_LOOTCORPSE_ANSW` | |
| `QEVENT_DEADKING_TAKEHEART_ANSW` | |
| `QEVENT_DIMENSIONXPORTAL_ENTER_ANSW` | |
| `QEVENT_GLOWINGORB_ANTENNA_ANSW` | |
| `QEVENT_GLOWINGORB_LICK_ANSW` | |
| `QEVENT_THEHEAD_AMPLIFIER_ANSW` | |
| `QEVENT_THEHEAD_FILLJAR_ANSW` | |
| `QEVENT_THROBBINGARTERY_ATTACH_ANSW` | |
| `QEVENT_TIMEMACHINE_FUTURE_ANSW` | |
| `QEVENT_TIMEMACHINE_FUTURE_FUTURE_ANSW` | |
| `QEVENT_TIMEMACHINE_ICEAGE_PAST_ANSW` | |
| `QEVENT_TIMEMACHINE_JURASSIC_INFINITE_ANSW` | |
| `QEVENT_TIMEMACHINE_PAST_ANSW` | |
| `QEVENT_TIMEMACHINE_THEEND_INFINITE_ANSW` | |
| `QEVENT_VOLCANO_ANTENNA_ANSW` | |
| `QEVENT_WALLOFFLESH_BITE2_ANSW` | |
| `QEVENT_WALLOFFLESH_BITE_ANSW` | |
| `QEVENT_WALLOFFLESH_PLACE_ANSW` | |

</details>


---

### Enum: `gain_disorder`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Stinky` | |
| `Anxiety` | |
| `Cancer` | |
| `Depression` | |
| `PuncturedEye` | |
| `Scatological` | |
| `Charred` | |
| `Necrosis` | |
| `Soulless` | |
| `BlessingOfGlorg` | |
| `IntestinalProlapse` | |
| `DeepCut` | |
| `Incontinence` | |
| `Rabies` | |
| `AcidReflux` | |
| `Albinism` | |
| `BloodFrenzy` | |
| `BorrowedTime` | |
| `BrainDamage` | |
| `BrainDead` | |
| `Brave` | |
| `Cannibal` | |
| `DarkOne` | |
| `Distemper` | |
| `Dyslexia` | |
| `EternalYouth` | |
| `ExplosiveGas` | |
| `Fossilized` | |
| `Gargantuan` | |
| `Gigachad` | |
| `HeadTrauma` | |
| `Infestation` | |
| `Leprosy` | |
| `LooseMeat` | |
| `Narcolepsy` | |
| `PTSD` | |
| `Paranoia` | |
| `PillPopper` | |
| `Shunned` | |
| `TamperedGenes` | |
| `Touched` | |
| `Vegan` | |

</details>


---

### Enum: `X_is`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `custom` | |
| `current_mana` | |
| `current_health` | |
| `turn_count` | |
| `current_shield` | |
| `enable_if_has_ammo` | |
| `is_at_max_mana` | |
| `max_health` | |
| `random_0_to_N` | |
| `this_ability_storm_count` | |
| `alpha_exists` | |
| `cast_count` | |
| `storm_count` | |
| `basic_attack_damage` | |
| `is_dead` | |
| `you_are_the_alpha` | |

</details>


---

### Enum: `scale`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root), [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.8` | |
| `.75` | |
| `.85` | |
| `.9` | |
| `.7` | |
| `.5` | |
| `.80` | |
| `.6` | |

</details>


---

### Enum: `custom_additional_ai_weight`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance), [`spawn`](./Abilities_and_Spells.md#context-spawn)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `toss_far` | |
| `tile_has_no_known_traps` | |
| `avoid_redundant_debuffs_strict` | |
| `tile_close_to_enemy` | |
| `toss_farthest` | |
| `must_target_buddy` | |
| `tile_exists` | |
| `avoid_redundant_debuffs` | |
| `magnetize_favorlineup` | |
| `prefer_dont_move` | |
| `target_closest` | |
| `dont_target_rock` | |
| `favor_tile_far_away` | |
| `toss_towards_buddy` | |
| `avoid_target_map_top` | |
| `dybbuk_possession` | |
| `enemy_is_webbed` | |
| `favor_enemy_already_moved` | |
| `moonhead_punchself` | |
| `moonhead_use_if_cracked` | |
| `must_heal_most_missing_health` | |
| `must_not_target_buddy` | |
| `no_coins_on_map` | |
| `no_redundant_formchange` | |
| `non_bramble_tile_close_to_enemy` | |
| `pills_only` | |
| `pyrophina_throw_to_lava` | |
| `spread_grenades` | |
| `target_farthest` | |
| `teslacoil_priorities` | |
| `thiefcat_coinroll` | |
| `thiefcat_roll` | |
| `tile_close_to_enemy_soft` | |
| `toss_towards_bottomleft` | |
| `tutorial_boulderdrop_miss_if_one_left` | |

</details>


---

### Enum: `water_mask`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `square` | |
| `medium` | |
| `medmed` | |
| `big` | |

</details>


---

### Enum: `has_token`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`requirements`](./Events_and_Encounters.md#context-requirements)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AdventureToken_BlueNeedle` | |
| `AdventureToken_RedNeedle` | |
| `AdventureToken_YellowNeedle` | |
| `AdventureToken_Mirage1` | |
| `AdventureToken_Mirage2` | |
| `AntennaQuest_Orb` | |
| `AntennaQuest_Rift` | |
| `AntennaQuest_Volcano` | |
| `AdventureToken_StevenTryAgain` | |
| `HasPlayedMysteriousStranger` | |
| `TimeMachineQuest_Began` | |
| `AdventureToken_HasRunFromDeath` | |
| `AdventureToken_MysteriousCave_FamiliarVoice` | |
| `AdventureToken_StevenTryAgain2` | |
| `HasHitPinata` | |
| `MeatWorldQuest_Gristle` | |
| `MeatWorldQuest_Leech` | |
| `WorldEventLegacyToken_MonkeyPaw1` | |
| `WorldEventLegacyToken_MonkeyPaw2` | |
| `WorldEventLegacyToken_MonkeyPaw3` | |
| `mapflag_EndOfTimeUnlocked` | |
| `mapflag_MeatWorldUnlocked` | |
| `AdventureToken_HasTakenNeedle` | |
| `AdventureToken_StevenTryAgain3` | |
| `AdventureToken_TrippedOnBigToe` | |
| `WorldEventLegacyToken_CryptOpened` | |
| `WorldEventLegacyToken_HasRunFromDeath` | |
| `WorldEventLegacyToken_MonkeyPaw4` | |
| `WorldEventLegacyToken_StacyMutant` | |
| `mapflag_FutureUnlocked` | |
| `mapflag_IceAgeUnlocked` | |
| `mapflag_JurassicUnlocked` | |
| `mapflag_TheEndUnlocked` | |

</details>


---

### Enum: `size`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](./Characters_and_Bosses.md#context-properties)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `2x2` | |
| `3x3` | |
| `1x1` | |
| `5x10` | |
| `gemini` | |

</details>


---

### Enum: `SpawnOnDeath`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives), [`passives`](./Elite_Buffs.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `RandomArmorPickup` | |
| `Antidote` | |
| `Maggot` | |
| `BiggestFood` | |
| `FrankPinky` | |
| `NonChampionFlySwarm` | |

</details>


---

### Enum: `gain_disorder_from_pool`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `all_disorders` | |
| `diseases` | |
| `physical_disorders` | |
| `mental_disorders` | |
| `Steven_disorders` | |
| `Crazy_disorders` | |
| `stomach_disorders` | |

</details>


---

### Enum: `element`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_AffectedByElement`](./Abilities_and_Spells.md#context-conditional_affectedbyelement), [`AddDamageToElementDamage`](./Cat_Mutations.md#context-adddamagetoelementdamage), [`PassiveWhenAffectedByElement`](./Cat_Mutations.md#context-passivewhenaffectedbyelement), [`DiesToElement`](./Characters_and_Bosses.md#context-diestoelement), [`FormChangeDuringWeatherElement`](./Characters_and_Bosses.md#context-formchangeduringweatherelement), [`FormChangeOnElementInfluence`](./Characters_and_Bosses.md#context-formchangeonelementinfluence), [`PassiveWhenAffectedByElement`](./Characters_and_Bosses.md#context-passivewhenaffectedbyelement), [`TransformOnElementInfluence`](./Characters_and_Bosses.md#context-transformonelementinfluence), [`TransformOnElementInfluencex`](./Characters_and_Bosses.md#context-transformonelementinfluencex), [`AddDamageToElementDamage`](./Items_and_Equipment.md#context-adddamagetoelementdamage), [`AddStatusToElementDamage`](./Items_and_Equipment.md#context-addstatustoelementdamage), [`PassiveWhenAffectedByElement`](./Items_and_Equipment.md#context-passivewhenaffectedbyelement), [`RefreshEquipmentAbilityOnElement`](./Items_and_Equipment.md#context-refreshequipmentabilityonelement), [`TransformItemOnElementInfluence`](./Items_and_Equipment.md#context-transformitemonelementinfluence), [`AddDamageToElementDamage`](./Passives_and_Statuses.md#context-adddamagetoelementdamage), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`AddStatusToElementDamage`](./Passives_and_Statuses.md#context-addstatustoelementdamage), [`ElementalManaCostReduction`](./Passives_and_Statuses.md#context-elementalmanacostreduction), [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement), [`StatusOnUseElementAbility`](./Passives_and_Statuses.md#context-statusonuseelementability), [`weather_element_alt`](./Spawns_and_Enemy_Pools.md#context-weather_element_alt)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `water` | |
| `Fire` | |
| `Gravity` | |
| `Electric` | |
| `Holy` | |
| `Water` | |
| `Greater_Water` | |
| `Ice` | |
| `very_hot` | |
| `wind` | |

</details>


---

### Enum: `move_block`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](./Characters_and_Bosses.md#context-properties)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `everything_even_when_dead` | |
| `nothing` | |

</details>


---

### Enum: `event_now_same_cat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `random` | |
| `Needles` | |
| `MonkeyPawWish` | |
| `MysteriousCave3` | |
| `MysteriousStranger` | |
| `MysteriousCave2` | |
| `ElephantsFootEvenCloser` | |
| `MysteriousCave1` | |
| `MysteriousStrangerForced` | |
| `MysteriousTomb1` | |
| `MysteriousTomb2` | |
| `Pinata` | |
| `Quest_DimensionXPortal` | |
| `Tragedy` | |
| `BigToe` | |
| `Blessing` | |
| `BodyOfGlorg_Gift` | |
| `CatHole` | |
| `ElephantsFootCloser` | |
| `Genie_Bad` | |
| `Genie_Good` | |
| `Happening` | |
| `JaggedPathwayStalactite` | |
| `MysteriousCave` | |
| `MysteriousJar` | |
| `MysteriousTomb3` | |
| `MysteriousTomb4` | |
| `Quest_TimeMachine` | |
| `SpookieApparation` | |
| `StevenFetus` | |
| `UnmarkedGrave` | |
| `UseTheToilet` | |

</details>


---

### Enum: `increment_legacy_counter`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `WorldEventLegacyCounter_Jack` | |
| `WorldEventLegacyCounter_ToiletFlushes` | |
| `WorldEventLegacyCounter_CrackInTheWall` | |
| `WorldEventLegacyToken_StartDigging` | |
| `WorldEventLegacyCounter_VolcanoSacrifices` | |
| `WorldEventLegacyCounter_SealedCrypt` | |
| `WorldEventLegacyCounter_TestLegacyFoo` | |

</details>


---

### Enum: `FormChange`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Conditional_HasStatus`](./Abilities_and_Spells.md#context-conditional_hasstatus), [`Conditional_InForm`](./Abilities_and_Spells.md#context-conditional_inform), [`Else`](./Abilities_and_Spells.md#context-else), [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects), [`PassiveGroup`](./Characters_and_Bosses.md#context-passivegroup), [`alternate_energized_effect`](./Characters_and_Bosses.md#context-alternate_energized_effect)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Default` | |
| `active` | |
| `Boris` | |
| `DualSword` | |
| `Explosive` | |
| `HasDeadCat` | |
| `Holy` | |
| `OffMap` | |
| `Pulp2` | |
| `passive` | |
| `Big` | |
| `BigHolding` | |
| `BigHoldingCat` | |
| `Bully` | |
| `Butcher` | |
| `Die` | |
| `Druid` | |
| `Drunker` | |
| `Dumb` | |
| `Fighter` | |
| `Grown` | |
| `GuaranteedJackpot` | |
| `HalfDead` | |
| `HasCat` | |
| `Hunter` | |
| `LastHit` | |
| `Lifted` | |
| `Mage` | |
| `Medic` | |
| `Monk` | |
| `Necromancer` | |
| `NoDeathrattle` | |
| `NoStick` | |
| `Nuke` | |
| `Obey` | |
| `Off` | |
| `Open` | |
| `Possessing` | |
| `Psychic` | |
| `Pulp3` | |
| `Pulp4` | |
| `Pulp5` | |
| `Pulp6` | |
| `Pulp7` | |
| `SpawningPhase` | |
| `SquirrelForm` | |
| `Standing` | |
| `Stop` | |
| `Tank` | |
| `Thief` | |
| `Tinkerer` | |

</details>


---

### Enum: `dash_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dash` | |
| `headbuttdash` | |
| `ramLoop` | |
| `dashing` | |
| `launchMid` | |
| `propelLoop` | |
| `dash2` | |
| `ram` | |
| `rampage` | |
| `roll` | |
| `spinattackloop` | |
| `thrustersLoop` | |
| `timberDash` | |

</details>


---

### Enum: `override_art`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`exit0`](./Map_Generation_and_Routing.md#context-exit0), [`exit1`](./Map_Generation_and_Routing.md#context-exit1), [`exit_desert`](./Map_Generation_and_Routing.md#context-exit_desert), [`exit_lab`](./Map_Generation_and_Routing.md#context-exit_lab), [`mw_altar`](./Map_Generation_and_Routing.md#context-mw_altar), [`mw_quest_event`](./Map_Generation_and_Routing.md#context-mw_quest_event), [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event), [`shop_cheapwater`](./Map_Generation_and_Routing.md#context-shop_cheapwater), [`shop_water`](./Map_Generation_and_Routing.md#context-shop_water), [`time_machine`](./Map_Generation_and_Routing.md#context-time_machine)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MapNode_TimeMachine` | |
| `MapNodeExit_DimensionX` | |
| `MapNodeExit_Infinite` | |
| `MapNodeExit_MeatWorld` | |
| `MapNode_Empty` | |
| `MapNode_ObeliskFull` | |
| `MapNode_ObeliskGlowing` | |
| `MapNode_ObeliskHalf` | |
| `MapNode_RiftPortal` | |
| `cheapwatershop` | |
| `MapNodeExit_Boneyard` | |
| `MapNodeExit_Bunker` | |
| `MapNodeExit_Caves` | |
| `MapNodeExit_Core` | |
| `MapNodeExit_Crater` | |
| `MapNodeExit_Desert` | |
| `MapNodeExit_Future` | |
| `MapNodeExit_IceAge` | |
| `MapNodeExit_Junkyard` | |
| `MapNodeExit_Jurassic` | |
| `MapNodeExit_Lab` | |
| `MapNodeExit_Moon` | |
| `MapNodeExit_Sewers` | |
| `MapNodeExit_TheEnd` | |
| `MapNode_BigMoneyBag` | |
| `MapNode_Bones` | |
| `MapNode_BrokenTimeMachine` | |
| `MapNode_CursedTreasure` | |
| `MapNode_DeadChaos` | |
| `MapNode_DeadChaosAntenna` | |
| `MapNode_DeadChild` | |
| `MapNode_DeadKing` | |
| `MapNode_FleshHole` | |
| `MapNode_FleshWall` | |
| `MapNode_FurnitureBox` | |
| `MapNode_FurnitureBox2` | |
| `MapNode_FurnitureBox3` | |
| `MapNode_GlowingBones` | |
| `MapNode_LargeMetor` | |
| `MapNode_MeatAltar` | |
| `MapNode_Needle` | |
| `MapNode_Orb` | |
| `MapNode_OrbAntenna` | |
| `MapNode_SmallMeteor` | |
| `MapNode_SmallMoneyBag` | |
| `MapNode_Veins` | |
| `MapNode_VeinsDrained` | |
| `MapNode_Volcano` | |
| `MapNode_VolcanoAntenna` | |
| `Rare_Treasure` | |

</details>


---

### Enum: `dash_start_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dashstart` | |
| `headbuttdashStart` | |
| `ramStart` | |
| `none` | |
| `launchStart` | |
| `propelStart` | |
| `dashbegin` | |
| `dashstart2` | |
| `thrustersStart` | |
| `timberStart` | |

</details>


---

### Enum: `ChangeTile`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects), [`AddStatusToBasicAttack`](./Cat_Mutations.md#context-addstatustobasicattack), [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack), [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `WaterTile` | |
| `GlassTile` | |
| `LavaTile` | |
| `BrambleTile` | |
| `TallGrassTile` | |
| `FloatingGlassTile` | |
| `BlankTile` | |
| `CreepTile` | |
| `DirtTile` | |
| `FireTile` | |
| `OilTile` | |
| `GrassTile` | |
| `IceShardsSmall` | |
| `IceTile` | |
| `RandomDifferentTile` | |
| `TallFlowerTile` | |
| `WaterTile_Current` | |

</details>


---

### Enum: `get_item`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Bottles` | |
| `EnchantingPoop` | |
| `GlassShard` | |
| `Rocks` | |
| `SlagMight` | |
| `BearTrapMask` | |
| `BearTraps` | |
| `BoneMarrow` | |
| `MomsKnife` | |
| `RaptorEgg` | |
| `AlienBlaster` | |
| `BagOfGrass` | |
| `BigToe` | |
| `BlinkingEyeball` | |
| `BrokenWindow` | |
| `Callus` | |
| `Catnip` | |
| `CatnipBig` | |
| `Chainsaw` | |
| `CryogenicTimeChamber_Full` | |
| `CursedStickman` | |
| `DeathsScythe` | |
| `EyeOfRa` | |
| `FurnitureBox` | |
| `Geode` | |
| `GoldenTooth` | |
| `HumanBrain` | |
| `MomsToeNail` | |
| `MysteriousBone` | |
| `Pearl` | |
| `PharaohStaff` | |
| `PuzzleBox` | |
| `RatBeezer` | |
| `RottenMeat` | |
| `SeedBombs` | |
| `SharkTooth` | |
| `SnaggleTooth` | |
| `StrangeMarble` | |
| `Technology` | |
| `TinyPebble` | |
| `ViperBottle` | |

</details>


---

### Enum: `pitch`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Custom_Cats.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.7` | |
| `.8` | |
| `.6` | |
| `.5` | |
| `.9` | |
| `.3` | |

</details>


---

### Enum: `layer`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance), [`spawn`](./Abilities_and_Spells.md#context-spawn), [`splash_damage`](./Abilities_and_Spells.md#context-splash_damage), [`properties`](./Characters_and_Bosses.md#context-properties)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pickups` | |
| `characters` | |
| `all` | |
| `gas` | |
| `tiles` | |
| `self` | |

</details>


---

### Enum: `set_adventure_token`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `HasPlayedMysteriousStranger` | |
| `AdventureToken_HasTakenNeedle` | |
| `AdventureToken_Mirage1` | |
| `AdventureToken_Mirage2` | |
| `MysteriousStranger_HasLostFinger` | |
| `AdventureToken_BlueNeedle` | |
| `AdventureToken_RedNeedle` | |
| `AdventureToken_YellowNeedle` | |
| `HasHitPinata` | |
| `AdventureToken_HasRunFromDeath` | |
| `AdventureToken_MysteriousCave_FamiliarVoice` | |
| `AdventureToken_MysteriousJarRepeat` | |
| `AdventureToken_StevenTryAgain` | |
| `AdventureToken_StevenTryAgain2` | |
| `AdventureToken_StevenTryAgain3` | |
| `AdventureToken_TrippedOnBigToe` | |
| `AdventureToken_UnmarkedGraveForced` | |
| `StacyMutant_Brace` | |
| `StacyMutant_Counter` | |
| `StacyMutant_Damage` | |
| `StacyMutant_DoubleHead` | |
| `StacyMutant_Fire` | |
| `StacyMutant_Health` | |
| `StacyMutant_Holy` | |
| `StacyMutant_Ice` | |
| `StacyMutant_Lightning` | |
| `StacyMutant_Mirror` | |
| `StacyMutant_Speed` | |
| `StacyMutant_Thorns` | |

</details>


---

### Enum: `alias`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Status_Effect_Keywords.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DamageUp` | |
| `DodgeChance_Status` | |
| `StrengthUp` | |
| `Brace` | |
| `Charmed` | |
| `EliteBuff_Twin` | |
| `MovementUp` | |
| `SpeedUp` | |
| `AllStatsUp` | |
| `DexterityUp` | |
| `DivineShield` | |
| `SpellDamageUp` | |
| `Brittle` | |
| `CritChanceUp` | |
| `EliteBuff_Absorbant` | |
| `EliteBuff_Bouncy` | |
| `EliteBuff_Damaging` | |
| `EliteBuff_Depressing` | |
| `EliteBuff_Hardy` | |
| `EliteBuff_Lucky` | |
| `EliteBuff_Protected` | |
| `EliteBuff_Reactive` | |
| `EliteBuff_SlightlyDepressing` | |
| `EliteBuff_Speedy` | |
| `EliteBuff_Static` | |
| `EliteBuff_Sticky` | |
| `Fragile` | |
| `Immobile` | |
| `Infested` | |
| `LuckUp` | |
| `Madness` | |
| `Shield` | |
| `TransformInXTurns` | |

</details>


---

### Enum: `initial_form`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Default` | |
| `Normal` | |
| `default` | |
| `hot` | |
| `Up` | |
| `CaveBaby` | |
| `CaveManSpear` | |
| `Empty` | |
| `active` | |
| `Big` | |
| `Bishop` | |
| `BlackHole` | |
| `CaveMan` | |
| `CaveWoman` | |
| `Cultist` | |
| `Down` | |
| `DualSword` | |
| `Flop` | |
| `Full` | |
| `Mutant` | |
| `Off` | |
| `OffMap` | |
| `Sitting` | |
| `Small` | |
| `Start_Ceiling` | |
| `Unwashed` | |
| `Washer` | |
| `Water` | |
| `WereMan` | |
| `Zealot` | |

</details>


---

### Enum: `play_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`main`](./Events_and_Encounters.md#context-main), [`options`](./Events_and_Encounters.md#context-options), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward), [`traverse`](./Events_and_Encounters.md#context-traverse)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `resultHole` | |
| `resultBad` | |
| `resultConfused` | |
| `resultVeryGood` | |
| `resultGood` | |
| `resultLeave` | |
| `resultVeryBad` | |

</details>


---

### Enum: `trigger_npc_sequence`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `beanies_begin_accepting_cats` | |
| `beanies_bombquest_2` | |
| `beanies_bombquest_3` | |
| `beanies_bombquest_amnesia` | |
| `beanies_bombquest_begin` | |
| `beanies_bombquest_fail_jarofblood` | |
| `beanies_bombquest_fail_jarofchaos` | |
| `beanies_bombquest_fail_jarofradiation` | |
| `beanies_bombquest_fail_nuke` | |
| `beanies_future_intro` | |
| `beanies_hitler3` | |
| `beanies_hitler3_defeat` | |
| `beanies_jurassic_intro` | |
| `beanies_lab_intro` | |
| `beanies_seefuture` | |
| `beanies_seetheend` | |
| `beanies_terminator1_defeat` | |
| `beanies_terminator2_defeat` | |
| `beanies_theend_intro` | |
| `beanies_timemachine_2` | |
| `beanies_timemachine_intro` | |
| `butch_first_house_boss_beat` | |
| `butch_pyro` | |
| `butch_tina1` | |
| `butch_tips_intro` | |
| `class_unlock_butcher` | |
| `class_unlock_druid` | |
| `class_unlock_jester` | |
| `class_unlock_medic` | |
| `class_unlock_monk` | |
| `class_unlock_necromancer` | |
| `class_unlock_psychic` | |
| `class_unlock_thief` | |
| `class_unlock_tinkerer` | |
| `frank_ending` | |
| `frank_terminator2` | |
| `jack_begin_accepting_cats` | |
| `jack_zara` | |
| `organ_throbbingdomain_intro` | |
| `organ_tina3` | |
| `steven_introduction` | |
| `steven_postendgame` | |
| `steven_unlock_act1_crazy` | |
| `steven_unlock_act1_impossible` | |
| `steven_unlock_act2_crazy` | |
| `steven_unlock_act2_hard` | |
| `steven_unlock_act2_impossible` | |
| `steven_unlock_act3_crazy` | |
| `steven_unlock_act3_hard` | |
| `steven_unlock_act3_impossible` | |
| `tink_terminator` | |
| `tink_tina2` | |
| `tink_tips_intro` | |
| `tracy_introduction` | |
| `tracy_kaijufight` | |

</details>


---

### Enum: `shadow_size`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.8` | |
| `.50` | |
| `.5` | |
| `.75` | |
| `.25` | |
| `.4` | |
| `.6` | |
| `.70` | |
| `.85` | |
| `.9` | |
| `.20` | |
| `.40` | |
| `.60` | |
| `.7` | |

</details>


---

### Enum: `gain_familiar`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`common`](./Events_and_Encounters.md#context-common), [`main`](./Events_and_Encounters.md#context-main), [`options`](./Events_and_Encounters.md#context-options), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CharmedMaggot` | |
| `CharmedPinky` | |
| `Snake` | |
| `CharmedRaptorBaby` | |
| `CharmedFetus` | |
| `CharmedTarBaby` | |
| `CharmedBear` | |
| `CharmedDaddyShark` | |
| `CharmedDustDevil` | |
| `CharmedFetus2` | |
| `CharmedFly` | |
| `CharmedHeadTumor` | |
| `CharmedHyde` | |
| `CharmedKitten` | |
| `CharmedLeaper` | |
| `CharmedMammoth` | |
| `CharmedMammothBaby` | |
| `CharmedRat` | |
| `CharmedWhiteRabbit` | |
| `FamiliarChargeyMaggot` | |
| `FamiliarFetus` | |
| `MechSuit` | |
| `Squirrel` | |
| `Toad` | |
| `Turtle` | |

</details>


---

### Enum: `ElementImmune`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./Abilities_and_Spells.md#context-applypassives), [`passives`](./Cat_Mutations.md#context-passives), [`StacyMutant_Fire`](./Characters_and_Bosses.md#context-stacymutant_fire), [`StacyMutant_Ice`](./Characters_and_Bosses.md#context-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#context-stacymutant_lightning), [`passives`](./Characters_and_Bosses.md#context-passives), [`passives`](./Elite_Buffs.md#context-passives), [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Fire` | |
| `Creep` | |
| `Ice` | |
| `Electric` | |

</details>


---

### Enum: `affected_particle`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `HealBig` | |
| `HealMed` | |
| `fx_tentaclestrangle` | |
| `Cleanse` | |
| `TakeAim` | |
| `HealSmall` | |
| `PoisonPoof` | |
| `fx_ManaHeal` | |
| `fx_haste` | |
| `ExclamationPointEnemy` | |
| `Purge` | |
| `fx_GravitySlam` | |
| `fx_heretic` | |
| `fx_shield` | |
| `fx_statdown` | |

</details>


---

### Enum: `tooltip`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Pulp2`](./Characters_and_Bosses.md#context-pulp2), [`Pulp3`](./Characters_and_Bosses.md#context-pulp3), [`Pulp4`](./Characters_and_Bosses.md#context-pulp4), [`Pulp5`](./Characters_and_Bosses.md#context-pulp5), [`Pulp6`](./Characters_and_Bosses.md#context-pulp6), [`Pulp7`](./Characters_and_Bosses.md#context-pulp7), [`SquirrelForm`](./Characters_and_Bosses.md#context-squirrelform), [`graphics`](./Characters_and_Bosses.md#context-graphics), [`ROOT`](./Status_Effect_Keywords.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `None` | |
| `ENEMY_TERMINATOR3_HITLERHEAD_DESC` | |
| `ENEMY_ANKYLOSAURUS_DESC` | |
| `ENEMY_BOMBFLY_DESC` | |
| `ENEMY_BOUNTYHUNTER_DESC` | |
| `ENEMY_DRAVENSQUIRRELFORM_DESC` | |
| `ENEMY_DUSTDEVIL_DESC` | |
| `ENEMY_RAPTORKITTEN_DESC` | |
| `ENEMY_STRANGEEGG_DESC` | |
| `ENEMY_TERMINATOR3_HITLER_DESC` | |
| `ENTITY_EGG_DESC` | |
| `ENTITY_GLOWMUSHROOM2_DESC` | |
| `ENTITY_GLOWMUSHROOM_DESC` | |

</details>


---

### Enum: `beat_house_boss`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pyrophina_vs_zaratana` | |
| `terminator_2` | |
| `guillotina_1` | |
| `guillotina_2` | |
| `guillotina_3` | |
| `pyrophina` | |
| `terminator_1` | |
| `terminator_3` | |
| `zaratana` | |
| `any` | |

</details>


---

### Enum: `clear_adventure_token`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`reward`](./Events_and_Encounters.md#context-reward)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AdventureToken_BlueNeedle` | |
| `AdventureToken_HasTakenNeedle` | |
| `AdventureToken_RedNeedle` | |
| `AdventureToken_YellowNeedle` | |

</details>


---

### Enum: `consumable_chance`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`boss`](./Combat_Rewards.md#context-boss), [`hard`](./Combat_Rewards.md#context-hard), [`miniboss`](./Combat_Rewards.md#context-miniboss), [`normal`](./Combat_Rewards.md#context-normal)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.25` | |
| `.3` | |
| `.5` | |

</details>


---

### Enum: `dash_attack_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dashatk` | |
| `headbuttdashEnd` | |
| `none` | |
| `dashend` | |
| `propelEnd` | |
| `ramEnd` | |
| `block` | |
| `dashEnd` | |
| `dashEnd2` | |
| `dashattack` | |
| `dashbite` | |
| `headbuttUppercut` | |
| `heaviestMelee` | |
| `knockswatatk` | |
| `spin` | |
| `spinattackloop` | |

</details>


---

### Enum: `level`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`boss`](./Map_Generation_and_Routing.md#context-boss), [`event`](./Map_Generation_and_Routing.md#context-event), [`miniboss_event`](./Map_Generation_and_Routing.md#context-miniboss_event), [`mw_altar`](./Map_Generation_and_Routing.md#context-mw_altar), [`mw_quest_event`](./Map_Generation_and_Routing.md#context-mw_quest_event), [`quest_event`](./Map_Generation_and_Routing.md#context-quest_event), [`shop_cheapwater`](./Map_Generation_and_Routing.md#context-shop_cheapwater), [`shop_water`](./Map_Generation_and_Routing.md#context-shop_water), [`time_machine`](./Map_Generation_and_Routing.md#context-time_machine), [`treasure`](./Map_Generation_and_Routing.md#context-treasure), [`weather_event`](./Map_Generation_and_Routing.md#context-weather_event)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Quest_DimensionXPortal` | |
| `Quest_TimeMachine` | |
| `Butch_Tutorial` | |
| `CraterWeatherEvent` | |
| `Quest_BrokenTimeMachine` | |
| `Quest_CoreObelisk` | |
| `Quest_CoreObeliskGlowing` | |
| `Quest_CoreObeliskRaised` | |
| `Quest_DeadGod` | |
| `Quest_DeadKing` | |
| `Quest_DimensionXRift` | |
| `Quest_MeatWorldAltar` | |
| `Quest_MoonObelisk` | |
| `Quest_MoonObeliskGlowing` | |
| `Quest_MoonObeliskRaised` | |
| `Quest_Orb` | |
| `Quest_ThrobbingArtery` | |
| `Quest_ThrobbingArtery2` | |
| `Quest_TimeMachineFuture` | |
| `Quest_TimeMachineIceAge` | |
| `Quest_TimeMachineJurassic` | |
| `Quest_TimeMachineTheEnd` | |
| `Quest_Volcano` | |
| `Quest_WallOfFlesh` | |
| `Quest_WallOfFlesh2` | |
| `StacyMutant1` | |
| `TreasureHard` | |
| `TreasureTutorial` | |
| `Treasure_AbilityNeedle` | |
| `Treasure_AncestorsSkull` | |
| `Treasure_FurnitureBox` | |
| `Treasure_GlowingBone` | |
| `Treasure_IrradiatedObject` | |
| `Treasure_LargeMeteor` | |
| `Treasure_LargeMoneyBag` | |
| `Treasure_MedFurnitureBox` | |
| `Treasure_RareFurnitureBox` | |
| `Treasure_SmallMeteor` | |
| `Treasure_SmallMoneyBag` | |
| `WaterShop` | |
| `WaterShopCheap` | |
| `spewer` | |
| `stacy` | |

</details>


---

### Enum: `animation_in`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `shadowStepIn` | |
| `digUp` | |
| `digin` | |
| `portin` | |
| `exitWater` | |
| `liquidteleportIn` | |
| `portIn` | |
| `teleportIn` | |

</details>


---

### Enum: `animation_out`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `shadowStepOut` | |
| `digDown` | |
| `digout` | |
| `portout` | |
| `enterWater` | |
| `liquidteleportOut` | |
| `portOut` | |
| `teleportOut` | |

</details>


---

### Enum: `max_aoe`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `3+bonus_range` | |
| `1+bonus_melee_range` | |
| `level` | |
| `10+bonus_range` | |
| `2+X` | |
| `5+bonus_range` | |
| `X` | |
| `X*.5` | |
| `X-1` | |
| `level-1` | |

</details>


---

### Enum: `get_parasite`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FecalHood_Cursed` | |
| `FecalMask_Cursed` | |
| `MetalRod` | |
| `PawShards` | |
| `BadSplinters` | |
| `BirdPoopHat` | |
| `CursedHairball` | |
| `CursedRock` | |
| `FecalNecklace_Cursed` | |
| `AlluringDoodie` | |
| `Beepis` | |
| `BigToeCursed` | |
| `BrainInAJar` | |
| `ChildSkull` | |
| `Clam` | |
| `CrimsonMask_Cursed` | |
| `Cunch` | |
| `CursedStickman` | |
| `EnchantingPoop_Cursed` | |
| `FaceShards` | |
| `Feebis` | |
| `MarkOfTheBeast` | |
| `PutridPile` | |
| `SlagTight` | |
| `SludgeHat` | |
| `SludgeMask` | |
| `SludgeNeck` | |
| `Splinters` | |

</details>


---

### Enum: `FindItemFromPool`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Cat_Mutations.md#context-statusonbattleend), [`Conditional_GoodRoll`](./Characters_and_Bosses.md#context-conditional_goodroll), [`StatusGroup`](./Characters_and_Bosses.md#context-statusgroup), [`ally_rewards`](./Characters_and_Bosses.md#context-ally_rewards), [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend), [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart), [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak), [`StatusOnDie`](./Items_and_Equipment.md#context-statusondie), [`StatusOnSetPieceBreak`](./Items_and_Equipment.md#context-statusonsetpiecebreak), [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend), [`statuses`](./Passives_and_Statuses.md#context-statuses)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `chapter` | |
| `consumables` | |
| `common` | |
| `parasites` | |
| `none` | |
| `pills` | |
| `blackbird_pool` | |
| `chapter_common` | |
| `chapter_specific_item` | |
| `cherub_pool` | |
| `chicken_pool` | |
| `common_bones` | |
| `dove_pool` | |
| `eagle_pool` | |
| `harpy_pool` | |
| `hummingbird_pool` | |
| `mutant_pool` | |
| `pigeon_pool` | |
| `rare` | |
| `raven_pool` | |
| `seagull_pool` | |
| `turkey_pool` | |

</details>


---

### Enum: `class_anis`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Custom_Cats.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Thief` | |
| `Butcher` | |
| `Druid` | |
| `Fighter` | |
| `Hunter` | |
| `Jester` | |
| `Mage` | |
| `Medic` | |
| `Monk` | |
| `Necromancer` | |
| `Psychic` | |
| `Tank` | |
| `Tinkerer` | |

</details>


---

### Enum: `target_requires_tag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pickup` | |
| `rock` | |
| `food` | |
| `moonhand` | |
| `robot` | |
| `bishop_hat` | |
| `bowling_ball` | |
| `hitler_clone` | |
| `hitler_clone_fetus` | |
| `humanoid` | |
| `money` | |
| `mount` | |
| `poker` | |
| `poop` | |
| `spear` | |
| `squirrel` | |
| `themotherspike` | |
| `unlit_candle` | |

</details>


---

### Enum: `VisualFXTile`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects), [`post_spawn_statuses`](./Abilities_and_Spells.md#context-post_spawn_statuses), [`AddStatusToBasicAttack`](./Cat_Mutations.md#context-addstatustobasicattack), [`effects`](./Elite_Buffs.md#context-effects), [`effects`](./Items_and_Equipment.md#context-effects), [`effects`](./Passives_and_Statuses.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `WaterConduct` | |
| `PoisonPoof` | |
| `BurnTrigger` | |
| `IcePoof` | |
| `Explosion` | |
| `MagicMissleBlast` | |
| `fx_windSpell` | |
| `Bolt` | |
| `FireBlastSmall` | |
| `HealBig` | |
| `sytheCut` | |

</details>


---

### Enum: `jump_attack_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `land` | |
| `bellyflopEnd` | |
| `none` | |
| `block` | |
| `entrance_land` | |
| `gravitySlamEnd` | |

</details>


---

### Enum: `set_legacy_token`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `WorldEventLegacyToken_StacyMutant` | |
| `WorldEventLegacyToken_HasRunFromDeath` | |
| `AlienOvergrowthUnlocked` | |
| `AntennaQuest_Orb` | |
| `AntennaQuest_Rift` | |
| `AntennaQuest_Volcano` | |
| `GeomagneticStormUnlocked` | |
| `MeatWorldQuest_Gristle` | |
| `MeatWorldQuest_Leech` | |
| `MeteorShowerUnlocked` | |
| `SolarFlareUnlocked` | |
| `StrangeEggsUnlocked` | |
| `TheRift_UsedPyrophina` | |
| `TheRift_UsedZaratana` | |
| `TheShimmerUnlocked` | |
| `TimeMachineQuest_Began` | |
| `WorldEventLegacyToken_CryptOpened` | |
| `WorldEventLegacyToken_HeadInTireCompleted` | |
| `WorldEventLegacyToken_MomsKnife` | |
| `WorldEventLegacyToken_MonkeyPaw1` | |
| `WorldEventLegacyToken_MonkeyPaw2` | |
| `WorldEventLegacyToken_MonkeyPaw3` | |
| `WorldEventLegacyToken_MonkeyPaw4` | |
| `WorldEventLegacyToken_MonkeyPawGenes` | |
| `WorldEventLegacyToken_MonkeyPawItems` | |
| `WorldEventLegacyToken_MonkeyPawKnowledge` | |
| `WorldEventLegacyToken_MonkeyPawStrength` | |
| `WorldEventLegacyToken_TapeRecorderDestroyed` | |
| `mapflag_ChaosAntennaAttached` | |
| `mapflag_OrbAntennaAttached` | |
| `mapflag_ThrobbingArteryDone` | |
| `mapflag_VolcanoAntennaAttached` | |
| `mapflag_WallOfFleshDone` | |

</details>


---

### Enum: `BounceObject`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects), [`effects`](./Items_and_Equipment.md#context-effects), [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SmallRock` | |
| `ZombieCatFamiliar` | |
| `CharmedTinySpider` | |
| `RandomPickup` | |
| `chapter_corpse_medium` | |
| `CharmedDip` | |
| `CharmedLeech` | |
| `AllyRotFly` | |
| `Amoeba` | |
| `BeefyCharmedLeech` | |
| `Bomb` | |
| `Boulder` | |
| `CharmedFlea` | |
| `CharmedFlea_Champion` | |
| `Dip` | |
| `GroundedSpear` | |
| `TinySpider` | |

</details>


---

### Enum: `complete_chapter`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `boneyard` | |
| `bunker` | |
| `sewers` | |
| `alley` | |
| `crater` | |
| `desert` | |
| `moon` | |
| `core` | |
| `future` | |
| `caves` | |
| `dimensionx` | |
| `endoftime` | |
| `iceage` | |
| `junkyard` | |
| `jurassic` | |
| `lab` | |

</details>


---

### Enum: `get_parasite_from_pool`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `parasites` | |
| `sludge_armor` | |
| `barbed_armor` | |
| `barbed_items` | |
| `cursed_items` | |
| `good_parasites` | |

</details>


---

### Enum: `item_chance`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`hard`](./Combat_Rewards.md#context-hard), [`miniboss`](./Combat_Rewards.md#context-miniboss), [`normal`](./Combat_Rewards.md#context-normal)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.25` | |
| `.5` | |

</details>


---

### Enum: `CounterAttack`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StacyMutant_Counter`](./Characters_and_Bosses.md#context-stacymutant_counter), [`passives`](./Characters_and_Bosses.md#context-passives), [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |
| `BungaSwipe` | |
| `LennyCatSlap` | |
| `MegafetusMelee` | |
| `Shove` | |
| `CloakerHex` | |
| `CollectiveCounter` | |
| `DeathWormTrampleDash_Reaction` | |
| `FleshyMindConfusion` | |
| `LoveBotCounter` | |
| `ReflexPunchJab` | |
| `ReflexPunchJab2` | |
| `SM_BleedCounter` | |
| `SpewerSuckLava` | |
| `SpewerSuckNormal` | |
| `SpewerSuckTar` | |
| `T3Counter` | |
| `TT_Thrash` | |
| `TattersFear` | |
| `TeslaBolt` | |
| `TrexSwitchTarget` | |
| `YeticatSnowball_Counter` | |

</details>


---

### Enum: `spawnin_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#context-spawn), [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `portin` | |
| `skeletonDie` | |
| `revive` | |
| `beamin` | |
| `beaminButcher` | |
| `beaminDruid` | |
| `beaminFighter` | |
| `beaminHunter` | |
| `beaminJester` | |
| `beaminMage` | |
| `beaminMedic` | |
| `beaminMonk` | |
| `beaminNecro` | |
| `beaminPsychic` | |
| `beaminTank` | |
| `beaminThief` | |
| `beaminTinkerer` | |
| `digUp` | |
| `disassemble` | |
| `grow` | |
| `howl` | |
| `poofIntoExistance` | |
| `reassemble` | |
| `skeletonRevive` | |
| `spawn` | |
| `spawnin` | |
| `summonspawnin` | |
| `tinaspawnin` | |

</details>


---

### Enum: `value`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveIfStrAuxEquals`](./Items_and_Equipment.md#context-passiveifstrauxequals), [`SetItemAux`](./Items_and_Equipment.md#context-setitemaux), [`ROOT`](./Spawns_and_Enemy_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |
| `cha` | |
| `con` | |
| `dex` | |
| `int` | |
| `item_aux+1` | |
| `item_aux+2` | |
| `item_aux-1` | |
| `lck` | |
| `spd` | |
| `str` | |

</details>


---

### Enum: `negative_weight_scale`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Enemy_AI.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.99` | |

</details>


---

### Enum: `ontrigger`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sounds`](./Abilities_and_Spells.md#context-sounds)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_AnkylosaurusAttack` | |
| `SE_ParasaurolophusAttack` | |
| `OldHose_Start_Trigger` | |
| `SE_AstroTaserPoke` | |
| `SE_BullRushDash` | |
| `SE_CatWeaponPoke_Chainsaw` | |
| `SE_ChainDash` | |
| `SE_FuturebotPunch` | |
| `SE_FuturebotSuplex` | |
| `SE_PetRock_Dash` | |
| `SE_PoopCatHug` | |
| `SE_SabertoothCatPounce` | |
| `SE_SabertoothCatSwipe` | |
| `SE_SabertoothCubLick` | |
| `SE_SabertoothCubSwipe` | |
| `SE_ScorpionCatAngry` | |
| `SE_ScorpionCatHug` | |
| `SE_WeaponShoot_Crossbow` | |
| `SE_WeaponShoot_GlassCannon` | |
| `SE_WeaponShoot_Nailgun` | |
| `SE_WeaponShoot_Slingshot` | |
| `SE_WeaponShoot_SpiderWebber` | |
| `SE_WeaponShoot_Taser` | |
| `SE_WeaponShoot_TeslaCannon` | |
| `SE_WeaponShoot_TractorBeam` | |
| `SE_WolfCatAttack` | |
| `SE_WolfCatLeap` | |
| `Spawn_Donate` | |
| `Spiderweb_Break` | |
| `Twister_move` | |

</details>


---

### Enum: `spend_mana_scale`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Enemy_AI.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.99` | |

</details>


---

### Enum: `beat_chapter_boss`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dimensionx` | |
| `endoftime` | |
| `meatworld` | |
| `alley` | |
| `boneyard` | |
| `bunker` | |
| `core` | |
| `crater` | |
| `crystaline_dreams` | |
| `desert` | |
| `future` | |
| `iceage` | |
| `junkyard` | |
| `jurassic` | |
| `lab` | |
| `moon` | |
| `sewers` | |
| `theend` | |

</details>


---

### Enum: `hidden_tag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](./Characters_and_Bosses.md#context-properties)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `riftheadguardian` | |
| `cavefamily` | |
| `zaratana` | |
| `dinofamily` | |
| `angeljunk` | |
| `bird` | |
| `bloateye` | |
| `bungawarrior` | |
| `collective` | |
| `container` | |
| `dc_cat` | |
| `dc_crow` | |
| `finalboss_clonecat` | |
| `grub_familiar` | |
| `hitler_clone` | |
| `husk` | |
| `megadino` | |
| `poison_cloud_immune` | |
| `sp_pill_fire` | |
| `sp_pill_normal` | |
| `sp_pill_tar` | |
| `sprout` | |
| `the_coven` | |

</details>


---

### Enum: `unlock_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BallOfSpiders` | |
| `Bump` | |
| `Ethereal` | |
| `HundredHandSlap` | |
| `HyperBeam` | |
| `MechSuit` | |
| `Metronome` | |
| `NailFlurry` | |
| `PathOfTheButcher` | |
| `PathOfTheCleric` | |
| `PathOfTheDruid` | |
| `PathOfTheFighter` | |
| `PathOfTheHunter` | |
| `PathOfTheJester` | |
| `PathOfTheMage` | |
| `PathOfTheMonk` | |
| `PathOfTheNecromancer` | |
| `PathOfThePsychic` | |
| `PathOfTheTank` | |
| `PathOfTheThief` | |
| `PathOfTheTinkerer` | |
| `PathOfTheVoid` | |
| `Pawbreaker` | |
| `PowerUp` | |
| `RNGCannon` | |
| `SliceAndDice` | |
| `SmartMetronome` | |
| `SummonBear` | |
| `SummonShade` | |
| `Supernova` | |
| `Suplex` | |

</details>


---

### Enum: `form_hasnot`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeWhileHasStatus`](./Characters_and_Bosses.md#context-formchangewhilehasstatus)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Default` | |
| `Normal` | |
| `Big` | |
| `Empty` | |
| `Fire` | |
| `Rage` | |
| `Small` | |
| `Tar` | |
| `CaveWoman` | |
| `Close` | |

</details>


---

### Enum: `not_has_token`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`requirements`](./Events_and_Encounters.md#context-requirements)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AdventureToken_StevenTryAgain2` | |
| `AdventureToken_MysteriousJarRepeat` | |
| `AdventureToken_StevenTryAgain3` | |
| `WorldEventLegacyToken_MonkeyPaw2` | |
| `WorldEventLegacyToken_MonkeyPaw3` | |
| `AdventureToken_BlueNeedle` | |
| `AdventureToken_HasRunFromDeath` | |
| `AdventureToken_RedNeedle` | |
| `AdventureToken_StevenTryAgain` | |
| `AdventureToken_UnmarkedGraveForced` | |
| `AdventureToken_YellowNeedle` | |
| `HasPlayedMysteriousStranger` | |
| `TimeMachineQuest_Began` | |
| `WorldEventLegacyToken_CryptOpened` | |
| `WorldEventLegacyToken_HeadInTireCompleted` | |
| `WorldEventLegacyToken_MomsKnife` | |
| `WorldEventLegacyToken_MonkeyPaw1` | |
| `WorldEventLegacyToken_MonkeyPaw4` | |
| `WorldEventLegacyToken_MonkeyPawGenes` | |
| `WorldEventLegacyToken_MonkeyPawItems` | |
| `WorldEventLegacyToken_MonkeyPawKnowledge` | |
| `WorldEventLegacyToken_MonkeyPawStrength` | |
| `WorldEventLegacyToken_StartDigging` | |
| `WorldEventLegacyToken_TapeRecorderDestroyed` | |

</details>


---

### Enum: `spawn_side`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn_unit_next_fight`](./Events_and_Encounters.md#context-spawn_unit_next_fight)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cats` | |
| `enemies` | |
| `anywhere` | |

</details>


---

### Enum: `ai_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicBigMelee` | |
| `BasicMelee` | |
| `MegafetusMelee_ai` | |
| `RockBlast_AI` | |
| `AZ_Jump_AI` | |
| `BungaSwipe_ai` | |
| `CerberubsJump_AI` | |
| `CollectiveCounterImpl_ai` | |
| `CollectiveSpinImpl` | |
| `DeathWormTrampleDash_Reaction_ai` | |
| `DrDRockets_ai` | |
| `IceElementalBreath_ai` | |
| `KirbySpitAI` | |
| `MD_PoopChainAI` | |
| `Magnetize_AI` | |
| `NubsJump_AI` | |
| `SkinnedTripleDash_AI` | |
| `SpawnBomb_AI` | |
| `SpawnTerminatorMini_Base` | |
| `SpewerSpit_AI` | |
| `TC_DashReaction_AI` | |
| `TormentorThrow_spAI` | |
| `TrembloSmash_AI` | |

</details>


---

### Enum: `mode`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics), [`PassiveAtHealthThreshold`](./Items_and_Equipment.md#context-passiveathealththreshold), [`PassiveAtStatThreshold`](./Items_and_Equipment.md#context-passiveatstatthreshold), [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#context-passiveathealththreshold), [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#context-passiveatinjurythreshold), [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `less_or_equal` | |
| `yeet` | |
| `equal` | |
| `greater` | |
| `greater_or_equal` | |

</details>


---

### Enum: `unlock_passive`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AlphaStrike` | |
| `ArmorSpecialist` | |
| `Bouncer` | |
| `ButchersSoul` | |
| `ClericsSoul` | |
| `DeathIncarnate` | |
| `DruidsSoul` | |
| `DualWield` | |
| `EnergyStorm` | |
| `EvilPatron` | |
| `FightersSoul` | |
| `Goofball` | |
| `GravityWell` | |
| `HuntersSoul` | |
| `Indigestion` | |
| `JestersSoul` | |
| `MagesSoul` | |
| `MonksSoul` | |
| `NecromancersSoul` | |
| `PsychicsSoul` | |
| `SkillShare` | |
| `SuicideSquad` | |
| `SuperLuck` | |
| `TanksSoul` | |
| `ThiefsSoul` | |
| `ThrillOfTheHunt` | |
| `TinkerersSoul` | |
| `Unstoppable` | |
| `VoidSoul` | |

</details>


---

### Enum: `unlock_song`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `alone_in_the_dark` | |
| `angel_wings` | |
| `bolt_of_lightning` | |
| `brush_your_teeth` | |
| `chaos` | |
| `chumbucket_kitty` | |
| `crack_of_doom` | |
| `crazy_days` | |
| `down_with_the_devil` | |
| `eatin_rats` | |
| `endless_misery` | |
| `feline_invader` | |
| `flush` | |
| `future_meets_the_past` | |
| `get_in_the_cage` | |
| `humanicide` | |
| `lonesome_road` | |
| `mom_i_really_hate_you` | |
| `queenhippo` | |
| `radio_final_boss` | |
| `radio_scrambled` | |
| `radio_throbbing_king` | |
| `so_high` | |
| `sweet_delicious` | |
| `taser_paws` | |
| `them_kitty_bones` | |
| `tuff` | |
| `were_dead` | |
| `you_know_who` | |

</details>


---

### Enum: `ForceUseAbility`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`VisualCountDownThenApplyStatus`](./Abilities_and_Spells.md#context-visualcountdownthenapplystatus), [`effects`](./Abilities_and_Spells.md#context-effects), [`FinalBossHitCountdownBoris`](./Characters_and_Bosses.md#context-finalbosshitcountdownboris), [`FinalBossHitCountdownExplosive`](./Characters_and_Bosses.md#context-finalbosshitcountdownexplosive), [`StatusAfterXTurns`](./Characters_and_Bosses.md#context-statusafterxturns), [`StatusEachTurnEndIfEnabledAtStartOfTurn`](./Characters_and_Bosses.md#context-statuseachturnendifenabledatstartofturn), [`AddSelfStatusToBasicAttack`](./Items_and_Equipment.md#context-addselfstatustobasicattack), [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll), [`StatusAfterXTurns`](./Items_and_Equipment.md#context-statusafterxturns), [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend), [`StatusEachTurnEndForEachTurn`](./Items_and_Equipment.md#context-statuseachturnendforeachturn), [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart), [`StatusOnKillEnemy`](./Items_and_Equipment.md#context-statusonkillenemy), [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend), [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#context-statusonstanceswitch), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CancerExplode` | |
| `DustDash` | |
| `Hallucinate_Disorder` | |
| `KidneyStone` | |
| `MiniFart` | |
| `MockingbirdForm` | |
| `MotherTumorGrow` | |
| `Ram_chained` | |
| `RapidFlowSpin` | |
| `RapidFlowSpin2` | |
| `Rest` | |
| `T2UnClone` | |
| `TheChild_TransformExplosive` | |
| `TheChild_TransformHoly` | |
| `cm_RaptorEggSpawn` | |
| `face_FartFace` | |
| `head_CatChestPound` | |
| `head_HitlersToupe` | |
| `neck_Brambles` | |
| `neck_ChefsApron` | |
| `neck_NukeExplode` | |
| `tk_Asteroid` | |
| `tk_DybbuksRib` | |
| `tk_JarOfRadiation` | |
| `tk_MadGhost_Spawn` | |
| `tk_RoboSucc` | |
| `tk_SuckStone` | |
| `tk_WeirdEgg_Spawn` | |

</details>


---

### Enum: `MulticlassLevelUp`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Fighter` | |
| `Hunter` | |
| `Mage` | |
| `Thief` | |
| `Butcher` | |
| `Druid` | |
| `Medic` | |
| `Monk` | |
| `Necromancer` | |
| `Psychic` | |
| `Tank` | |
| `Tinkerer` | |

</details>


---

### Enum: `TransformAbility`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BerserkDash` | |
| `BerserkDash2` | |
| `BirthSquirrel` | |
| `BirthSquirrel2` | |
| `HardenSkin` | |
| `HardenSkin2` | |
| `Lacerate` | |
| `Lacerate2` | |
| `LastThought` | |
| `LastThought2` | |
| `MonkeyThrow` | |
| `MonkeyThrow2` | |
| `Pounce` | |
| `Pounce2` | |
| `Prance` | |
| `Prance2` | |
| `Reposition` | |
| `Reposition2` | |
| `Scavenge` | |
| `Scavenge2` | |
| `SpiritBomb` | |
| `SpiritBomb2` | |
| `Synthesize` | |
| `Synthesize2` | |
| `Tease` | |
| `Tease2` | |
| `ThrowSpiritBomb` | |
| `ThrowSpiritBomb2` | |

</details>


---

### Enum: `aoe_symmetry`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `none` | |
| `four_way` | |
| `eight_way` | |

</details>


---

### Enum: `form`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_InForm`](./Abilities_and_Spells.md#context-conditional_inform), [`FormChange`](./Abilities_and_Spells.md#context-formchange), [`ChanceToFormChangeOnAbilityDamage`](./Characters_and_Bosses.md#context-chancetoformchangeonabilitydamage), [`DybbukPossessionFallback`](./Characters_and_Bosses.md#context-dybbukpossessionfallback), [`FormChangeDuringWeatherElement`](./Characters_and_Bosses.md#context-formchangeduringweatherelement), [`FormChangeOnElementInfluence`](./Characters_and_Bosses.md#context-formchangeonelementinfluence)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Up` | |
| `Default` | |
| `default` | |
| `hot` | |
| `Rage` | |
| `Rain` | |
| `Unlit` | |
| `BlackHole` | |
| `Down` | |
| `Flop2` | |
| `Lit` | |
| `Normal` | |
| `Possessing` | |
| `Small` | |
| `SmallHolding` | |
| `SmallHoldingCat` | |

</details>


---

### Enum: `icon_shell_frame`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](./Abilities_and_Spells.md#context-meta)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |
| `big_damage` | |
| `multihit_attack` | |
| `damage` | |
| `nodamage` | |

</details>


---

### Enum: `slot`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Craft`](./Abilities_and_Spells.md#context-craft), [`Craft`](./Items_and_Equipment.md#context-craft), [`SetItemAux`](./Items_and_Equipment.md#context-setitemaux), [`Craft`](./Passives_and_Statuses.md#context-craft), [`lock_item_slot`](./Passives_and_Statuses.md#context-lock_item_slot)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `weapon` | |
| `face` | |
| `trinket` | |
| `head` | |
| `random_empty_armor` | |
| `random_empty_armor_or_weapon` | |
| `neck` | |
| `random_empty` | |

</details>


---

### Enum: `spawn_object_distance_to_enemy`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Enemy_AI.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `-.01` | |

</details>


---

### Enum: `ReplaceBasicAttack`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./Abilities_and_Spells.md#context-applypassives), [`PassiveGroup`](./Characters_and_Bosses.md#context-passivegroup), [`StacyMutant_Fire`](./Characters_and_Bosses.md#context-stacymutant_fire), [`StacyMutant_Ice`](./Characters_and_Bosses.md#context-stacymutant_ice), [`StacyMutant_Lightning`](./Characters_and_Bosses.md#context-stacymutant_lightning), [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicDruidAbilityVersatile` | |
| `BasicMagicMissile` | |
| `BasicMedicRanged` | |
| `BasicButcherMelee` | |
| `BasicButcherMeleeWideDoubleSpin` | |
| `BasicButcherMeleeWideSpin` | |
| `BasicDruidAbility` | |
| `BasicMagicShortRanged` | |
| `BasicMedicMelee` | |
| `BasicMelee` | |
| `BasicMonkMelee` | |
| `BasicNecroRanged` | |
| `BasicPoke` | |
| `BasicPsychicPull` | |
| `BasicPuke` | |
| `BasicRanged` | |
| `BasicStraightShot` | |
| `BasicTankMelee` | |
| `SM_IceBreath` | |
| `SM_Lavashot` | |
| `SM_LightningDash` | |
| `head_Pestilence` | |

</details>


---

### Enum: `form_has`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeWhileHasStatus`](./Characters_and_Bosses.md#context-formchangewhilehasstatus)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `HasCat` | |
| `BellyFull` | |
| `FireFull` | |
| `Full` | |
| `Holding` | |
| `MouthFull` | |
| `NormalFull` | |
| `TarFull` | |
| `CaveWomanHasCat` | |
| `Grappling` | |
| `HasRock` | |
| `OpenCat` | |
| `Primed` | |
| `Transformed` | |

</details>


---

### Enum: `mana`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`cost`](./Abilities_and_Spells.md#context-cost)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |
| `10-X` | |
| `10-X*6` | |
| `15-X` | |
| `15-X*2` | |
| `16-X*16` | |
| `2+X*2` | |
| `22-X*3` | |
| `3+X*1` | |
| `3+X*2` | |
| `4-X` | |
| `6-X` | |
| `8-X*2` | |
| `spd` | |

</details>


---

### Enum: `ObjectOnHitCharacter`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects), [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak), [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool), [`StatusOnHealed`](./Passives_and_Statuses.md#context-statusonhealed)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CharmedLeech` | |
| `RandomPickup` | |
| `BloatEye` | |
| `Coin` | |
| `AllyRotFly` | |
| `BeefyCharmedLeech` | |
| `BestBud` | |
| `Fly` | |
| `Maggot` | |
| `SkeletonCatFamiliar` | |
| `SmallRock` | |

</details>


---

### Enum: `full_jump_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |
| `backflip` | |
| `jump` | |
| `attack1` | |
| `depossess` | |
| `djump` | |
| `fuzzjump` | |
| `hop` | |
| `jumpattack` | |
| `jumpmove` | |
| `jumpsmash` | |
| `leap` | |
| `leapattack` | |
| `moonjump` | |
| `possess` | |
| `pounce` | |
| `walk` | |

</details>


---

### Enum: `AddElementsToBasicAttack`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives), [`passives`](./Characters_and_Bosses.md#context-passives), [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Fire` | |
| `Water` | |
| `Electric` | |
| `Ice` | |
| `Holy` | |
| `Wind` | |
| `Gravity` | |

</details>


---

### Enum: `DeathRattle`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives), [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BoomerCatExplode` | |
| `DecoyExplode` | |
| `BBExplode` | |
| `BloatyExplodey` | |
| `BombFlyExplode` | |
| `GA_PrimeExplode` | |
| `GametePop` | |
| `GasserExplode` | |
| `GrenadeExplode` | |
| `IDBrambleBurst` | |
| `InvaderExplode` | |
| `ManglerMonsterExplode` | |
| `MechExplode` | |
| `MiniNukeExplodey` | |
| `MoonHead_KillHands` | |
| `SlotMachine_DeathExplode` | |
| `TKNG_DeathExplode` | |
| `TNTExplodey` | |
| `UFO_BigExplode` | |
| `neck_NukeExplode` | |

</details>


---

### Enum: `chance`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ArcLightning`](./Abilities_and_Spells.md#context-arclightning), [`BounceObject`](./Abilities_and_Spells.md#context-bounceobject), [`ChangeTile`](./Abilities_and_Spells.md#context-changetile), [`Cleave`](./Abilities_and_Spells.md#context-cleave), [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#context-destroyequipmentandattachparasite), [`FindItemFromPool`](./Abilities_and_Spells.md#context-finditemfrompool), [`KnockOutCoin`](./Abilities_and_Spells.md#context-knockoutcoin), [`ObjectOnHitCharacter`](./Abilities_and_Spells.md#context-objectonhitcharacter), [`GainDisorderFromPool`](./Characters_and_Bosses.md#context-gaindisorderfrompool), [`SpawnThingOnDamage`](./Characters_and_Bosses.md#context-spawnthingondamage), [`DestroyEquipmentAndAttachParasite`](./Items_and_Equipment.md#context-destroyequipmentandattachparasite), [`SpawnEachTurn`](./Items_and_Equipment.md#context-spawneachturn), [`SpawnThingOnDamage`](./Items_and_Equipment.md#context-spawnthingondamage), [`FindItemFromPool`](./Passives_and_Statuses.md#context-finditemfrompool), [`ForceUseAbility`](./Passives_and_Statuses.md#context-forceuseability), [`SpawnEachTurn`](./Passives_and_Statuses.md#context-spawneachturn)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |
| `.25` | |
| `.15` | |
| `.2` | |
| `.02` | |
| `.1` | |
| `.75` | |

</details>


---

### Enum: `set_mapgen_flag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BothObelisksUnlocked` | |
| `BoneyardUnlocked` | |
| `BunkerUnlocked` | |
| `CavesUnlocked` | |
| `CoreObeliskUnlocked` | |
| `CoreUnlocked` | |
| `CraterUnlocked` | |
| `DesertUnlocked` | |
| `DimensionXUnlocked` | |
| `EndOfTimeUnlocked` | |
| `FutureUnlocked` | |
| `HardPathUnlocked` | |
| `IceAgeUnlocked` | |
| `JunkyardUnlocked` | |
| `JurassicUnlocked` | |
| `LabUnlocked` | |
| `MeatWorldUnlocked` | |
| `MeatWorldUnlockedFull` | |
| `MoonObeliskUnlocked` | |
| `MoonUnlocked` | |
| `SewersUnlocked` | |
| `TheEndUnlocked` | |

</details>


---

### Enum: `shadow`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `none` | |
| `None` | |
| `MedSlimeShadow` | |
| `BigSlimeShadow` | |
| `SmallSlimeShadow` | |
| `TormentorShadow` | |

</details>


---

### Enum: `title`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`intro`](./Events_and_Encounters.md#context-intro)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `QEVENT_TIMEMACHINE_NAME` | |
| `QEVENT_WALLOFFLESH_NAME` | |
| `QEVENT_BROKENTIMEMACHINE_NAME` | |
| `QEVENT_DEADGOD_NAME` | |
| `QEVENT_DEADKING_NAME` | |
| `QEVENT_DIMENSIONXPORTAL_NAME` | |
| `QEVENT_GLOWINGORB_NAME` | |
| `QEVENT_MEATALTAR_NAME` | |
| `QEVENT_OBELISK_CORE_NAME` | |
| `QEVENT_OBELISK_CORE_NAME2` | |
| `QEVENT_OBELISK_CORE_NAME3` | |
| `QEVENT_OBELISK_MOON_NAME` | |
| `QEVENT_OBELISK_MOON_NAME2` | |
| `QEVENT_OBELISK_MOON_NAME3` | |
| `QEVENT_THEHEAD_NAME` | |
| `QEVENT_THROBBINGARTERY_NAME` | |
| `QEVENT_THROBBINGARTERY_NAME2` | |
| `QEVENT_VOLCANO_NAME` | |

</details>


---

### Enum: `amount`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root), [`reverb_empty`](./House_and_Environment.md#context-reverb_empty), [`reverb_full`](./House_and_Environment.md#context-reverb_full)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.25` | |
| `.65` | |

</details>


---

### Enum: `cat_has_item_equipped`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`requirements`](./Events_and_Encounters.md#context-requirements)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `PyrophinasCollar` | |
| `ZaratanasCollar` | |
| `CryogenicTimeChamber_Empty` | |
| `CryogenicTimeChamber_Full` | |
| `GuillotinasHead` | |
| `JarOfRadiatedBlood` | |
| `JarOfRadiation` | |
| `PutridLeech` | |
| `ReceiverAntenna` | |
| `SignalAmplifier` | |
| `ThrobbingGristle` | |
| `TransmitterAntenna` | |

</details>


---

### Enum: `dash_end_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dashend` | |
| `launchStop` | |
| `ramEnd` | |
| `none` | |
| `thrustersEnd` | |
| `timberEnd` | |

</details>


---

### Enum: `preset`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root), [`reverb_empty`](./House_and_Environment.md#context-reverb_empty), [`reverb_full`](./House_and_Environment.md#context-reverb_full)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `LIVINGROOM` | |
| `AUDITORIUM` | |
| `STONEROOM` | |

</details>


---

### Enum: `quest_reward_item`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `NuclearKnife_Fixed` | |
| `AirHorn_Fixed` | |
| `AngryFace_Fixed` | |
| `BubbleBoy_Fixed` | |
| `ChaosDevice_Fixed` | |
| `ExperimentalTreatment_Fixed` | |
| `FartFace_Fixed` | |
| `GlassCannon_Fixed` | |
| `HardPill_Fixed` | |
| `MagicMirror_Fixed` | |
| `MeStone_Fixed` | |
| `MysteriousDice_Fixed` | |
| `PartyDetonator_Fixed` | |
| `PersuasionDevice_Fixed` | |
| `PrincessHat_Fixed` | |
| `Redacted_Fixed` | |
| `SpiderInjector_Fixed` | |
| `Stopwatch_Fixed` | |
| `StorageLocker_Fixed` | |
| `TheLoner_Fixed` | |
| `UltraVision3000_Fixed` | |

</details>


---

### Enum: `tooltip_stackless`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Status_Effect_Keywords.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `none` | |
| `None` | |
| `KEYWORD_AUTOREVIVE_DESC` | |

</details>


---

### Enum: `add_weather`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`main`](./Events_and_Encounters.md#context-main), [`outcome`](./Events_and_Encounters.md#context-outcome), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `RestlessDead` | |
| `AlienOvergrowth` | |
| `GeomagneticStorm` | |
| `HauntedNight` | |
| `MeteorShower` | |
| `Sandstorm` | |
| `SolarFlare` | |
| `StrangeEggs` | |
| `TheShimmer` | |
| `Birdemic` | |

</details>


---

### Enum: `blocked_damage`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `5+bonus_melee_ability_damage` | |
| `3+bonus_melee_ability_damage` | |
| `5+bonus_melee_damage` | |
| `7+bonus_melee_ability_damage` | |

</details>


---

### Enum: `center_particle`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics), [`spell_graphics_override`](./Passives_and_Statuses.md#context-spell_graphics_override)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `none` | |
| `WaterConduct` | |
| `FireBlastMushroom` | |
| `Explosion` | |
| `NukeBlastLarge` | |
| `BigMagicMissileBlast` | |
| `Holybeam` | |
| `None` | |
| `TenTicklesAttack` | |

</details>


---

### Enum: `complete_item_quest`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good), [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Nuke` | |
| `BlackShard` | |
| `JarOfRadiatedBlood` | |
| `JarOfRadiation` | |
| `ScaldingOrb` | |
| `CryogenicTimeChamber_Empty` | |
| `CryogenicTimeChamber_Full` | |
| `GuillotinasHead` | |
| `PutridLeech` | |
| `PyrophinasCollar` | |
| `ReceiverAntenna` | |
| `SignalAmplifier` | |
| `ThrobbingGristle` | |
| `TransmitterAntenna` | |
| `ZaratanasCollar` | |

</details>


---

### Enum: `event_now`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Mirage` | |
| `StacyMutant2` | |
| `StacyMutant3` | |
| `StacyMutant4` | |
| `random` | |
| `MeatGolem` | |
| `MysteriousMachine_Bad` | |
| `MysteriousMachine_Good` | |

</details>


---

### Enum: `first_turn`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#context-spawn), [`TransformOnDeathImmediately`](./Characters_and_Bosses.md#context-transformondeathimmediately)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `initiative` | |
| `keep_turns` | |
| `end_of_round` | |
| `next_turn` | |
| `next_round` | |

</details>


---

### Enum: `ambience`
<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `amb_alley.ogg` | |
| `amb_boneyard.ogg` | |
| `amb_bunker.ogg` | |
| `amb_cave.ogg` | |
| `amb_core.ogg` | |
| `amb_crater.ogg` | |
| `amb_desert.ogg` | |
| `amb_dimensionx.ogg` | |
| `amb_endoftime.ogg` | |
| `amb_future.ogg` | |
| `amb_iceage.ogg` | |
| `amb_junkyard.ogg` | |
| `amb_jurassic.ogg` | |
| `amb_meatworld.ogg` | |
| `amb_moon.ogg` | |
| `amb_sewer.ogg` | |
| `amb_snow.ogg` | |
| `amb_theend.ogg` | |

</details>


---

### Enum: `area_particle`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics), [`spell_graphics_override`](./Passives_and_Statuses.md#context-spell_graphics_override)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `none` | |
| `WaterConduct` | |
| `FireBlastSmall` | |
| `Earthquake` | |
| `Bolt` | |
| `BurnTrigger` | |
| `Holybeam` | |
| `MagicMissleBlast` | |

</details>


---

### Enum: `chapter_id`
<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `alley` | |
| `boneyard` | |
| `bunker` | |
| `caves` | |
| `core` | |
| `crater` | |
| `debug` | |
| `desert` | |
| `dimensionx` | |
| `endoftime` | |
| `future` | |
| `iceage` | |
| `junkyard` | |
| `jurassic` | |
| `lab` | |
| `meatworld` | |
| `moon` | |
| `sewers` | |
| `theend` | |
| `tutorial` | |

</details>


---

### Enum: `common`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BossRewards`](./Characters_and_Bosses.md#context-bossrewards)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Asteroid` | |
| `Blubber` | |
| `BungasBone` | |
| `ChubsCollar` | |
| `CoffinArmor` | |
| `FriendlyAmoeba` | |
| `HitlersPistol` | |
| `JohnnysUndies` | |
| `LuciferSigil` | |
| `MegaPoop` | |
| `MissingNipple` | |
| `MothersTeeth` | |
| `NubsCollar` | |
| `PentagramSigil` | |
| `RatBomb` | |
| `RedPill` | |
| `SnakeEyes` | |
| `Spinnerets` | |
| `Stacy100` | |
| `ZodiacsPoncho` | |

</details>


---

### Enum: `folder`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `alley` | |
| `boneyard` | |
| `bunker` | |
| `caves` | |
| `core` | |
| `crater` | |
| `desert` | |
| `dimensionx` | |
| `future` | |
| `iceage` | |
| `junkyard` | |
| `jurassic` | |
| `lab` | |
| `meatworld` | |
| `moon` | |
| `sewer` | |
| `theend` | |
| `theinfinite` | |
| `tutorial` | |

</details>


---

### Enum: `graphics`
<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Map_Alley` | |
| `Map_Bunker` | |
| `Map_Caves` | |
| `Map_Core` | |
| `Map_Crater` | |
| `Map_Desert` | |
| `Map_DimensionX` | |
| `Map_EndOfTime` | |
| `Map_EventDebug` | |
| `Map_Future` | |
| `Map_Graves` | |
| `Map_IceAge` | |
| `Map_Junkyard` | |
| `Map_Jurassic` | |
| `Map_Lab` | |
| `Map_MeatWorld` | |
| `Map_Moon` | |
| `Map_Sewers` | |
| `Map_TheEnd` | |
| `Map_Tutorial` | |

</details>


---

### Enum: `music`
<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `jurassic` | |
| `alley` | |
| `boneyard` | |
| `bunker` | |
| `caves` | |
| `core` | |
| `crater` | |
| `desert` | |
| `dimensionx` | |
| `endoftime` | |
| `future` | |
| `iceage` | |
| `junkyard` | |
| `lab` | |
| `meatworld` | |
| `moon` | |
| `sewers` | |
| `theend` | |
| `tutorial` | |

</details>


---

### Enum: `next_map`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`exit0`](./Map_Generation_and_Routing.md#context-exit0), [`exit1`](./Map_Generation_and_Routing.md#context-exit1), [`exit_desert`](./Map_Generation_and_Routing.md#context-exit_desert), [`exit_lab`](./Map_Generation_and_Routing.md#context-exit_lab)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dimensionx.gon` | |
| `endoftime.gon` | |
| `meatworld.gon` | |
| `boneyard.gon` | |
| `bunker.gon` | |
| `caves.gon` | |
| `core.gon` | |
| `crater.gon` | |
| `desert.gon` | |
| `future.gon` | |
| `iceage.gon` | |
| `junkyard.gon` | |
| `jurassic.gon` | |
| `lab.gon` | |
| `moon.gon` | |
| `sewers.gon` | |
| `theend.gon` | |

</details>


---

### Enum: `spawn_object_distance_to_ally`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Enemy_AI.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.0001` | |
| `-.0001` | |
| `-.01` | |

</details>


---

### Enum: `tileset`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`boss`](./Map_Generation_and_Routing.md#context-boss)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `alley` | |
| `boneyard` | |
| `bunker` | |
| `caves` | |
| `core` | |
| `crater` | |
| `desert` | |
| `finalboss` | |
| `future` | |
| `iceage` | |
| `junkyard` | |
| `jurassic` | |
| `lab` | |
| `meatworld` | |
| `moon` | |
| `sewers` | |
| `theend` | |
| `theinfinite` | |
| `therift` | |
| `tutorial` | |

</details>


---

### Enum: `EliteParticle`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Lava_Distortion` | |
| `AbsorbBuff` | |
| `PassiveEnergized` | |
| `PassiveTar` | |
| `SparkleBuff` | |
| `SpikeBuff` | |
| `FireExtinguish_Steam` | |
| `FlyBuff` | |
| `SandStormBuff` | |
| `ShineBuff` | |
| `SmokeBuff` | |
| `ToxicBubbles` | |

</details>


---

### Enum: `area_name`
<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_ALLEY` | |
| `AREA_NAME_BONEYARD` | |
| `AREA_NAME_BUNKER` | |
| `AREA_NAME_CAVES` | |
| `AREA_NAME_CORE` | |
| `AREA_NAME_CRATER` | |
| `AREA_NAME_DESERT` | |
| `AREA_NAME_DIMENSIONX` | |
| `AREA_NAME_ENDOFTIME` | |
| `AREA_NAME_FUTURE` | |
| `AREA_NAME_ICEAGE` | |
| `AREA_NAME_JUNKYARD` | |
| `AREA_NAME_JURASSIC` | |
| `AREA_NAME_LAB` | |
| `AREA_NAME_MEATWORLD` | |
| `AREA_NAME_MOON` | |
| `AREA_NAME_SEWERS` | |
| `AREA_NAME_THEEND` | |
| `AREA_NAME_TUTORIAL` | |

</details>


---

### Enum: `chapter_item_pool`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `alleyitems` | |
| `boneyarditems` | |
| `bunkeritems` | |
| `cavesitems` | |
| `coreitems` | |
| `crateritems` | |
| `desertitems` | |
| `dimensionxitems` | |
| `futureitems` | |
| `iceageitems` | |
| `junkyarditems` | |
| `jurassicitems` | |
| `labitems` | |
| `meatworlditems` | |
| `moonitems` | |
| `seweritems` | |
| `theenditems` | |
| `theinfiniteitems` | |

</details>


---

### Enum: `disease`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpreadDisease`](./Abilities_and_Spells.md#context-spreaddisease), [`CureDisease`](./Passives_and_Statuses.md#context-curedisease), [`SpreadDisease`](./Passives_and_Statuses.md#context-spreaddisease)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CommonCold` | |
| `Ebola` | |
| `BirdFlu` | |
| `Covid` | |
| `FelineAids` | |
| `Flu` | |
| `Pox` | |
| `Cancer` | |
| `Rabies` | |
| `Toxoplasmosis` | |

</details>


---

### Enum: `tile`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChangeTile`](./Abilities_and_Spells.md#context-changetile), [`SpawnExtraThingsOnBattleStart`](./House_and_Environment.md#context-spawnextrathingsonbattlestart), [`SpawnTilePuddleOnBattleStart`](./House_and_Environment.md#context-spawntilepuddleonbattlestart), [`ChangeTile`](./Passives_and_Statuses.md#context-changetile)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `OilTile` | |
| `WaterTile` | |
| `BrambleTile` | |
| `FireTile` | |
| `GlassTile` | |
| `LavaTile` | |
| `CreepTile` | |
| `ShadowTile` | |
| `TallGrassTile` | |
| `ToxicTile` | |

</details>


---

### Enum: `world_name_frame`
<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `alley` | |
| `boneyard` | |
| `bunker` | |
| `caves` | |
| `crater` | |
| `desert` | |
| `future` | |
| `iceage` | |
| `junkyard` | |
| `jurassic` | |
| `meatworld` | |
| `sewers` | |
| `thecore` | |
| `theend` | |
| `theinfinite` | |
| `thelab` | |
| `themoon` | |
| `therift` | |
| `tutorial` | |

</details>


---

### Enum: `BonusAbility`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`keyword_tooltips`](./Abilities_and_Spells.md#context-keyword_tooltips), [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FeralMelee` | |
| `Seppuku` | |
| `Bloodzerk` | |
| `BonusToss` | |
| `BonusToss2` | |
| `DonateEnergy` | |
| `DonateEnergy2` | |
| `FighterBonusThrow` | |
| `Groom` | |
| `GrowHead` | |
| `SlitWrists` | |
| `ThrowSpiritBomb` | |
| `ThrowSpiritBomb2` | |
| `TinkererThrow` | |
| `WasteTime` | |
| `neck_NukeBonus` | |

</details>


---

### Enum: `InnateElement`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives), [`passives`](./Elite_Buffs.md#context-passives), [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Fire` | |
| `Ice` | |
| `Earth` | |
| `Electric` | |
| `Water` | |

</details>


---

### Enum: `AbilityOnBattleStart_Immediate`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`party_status_next_fight`](./Events_and_Encounters.md#context-party_status_next_fight), [`self_status_next_fight`](./Events_and_Encounters.md#context-self_status_next_fight)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BrambleRandomTileEvent` | |
| `SummonBrambles2` | |
| `FlowerEventSleep` | |
| `Flush` | |
| `GrassEvent` | |
| `RocksFallEvent` | |

</details>


---

### Enum: `ReplaceBasicMove`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives), [`passives`](./Items_and_Equipment.md#context-passives), [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#context-passivewhenatfullmana), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicJump` | |
| `Shadowstep` | |
| `ToadJump_BasicMove` | |
| `BellyFlop_BasicMove` | |
| `BasicDashAttackMove` | |
| `MaxTeleport` | |
| `Teleport` | |
| `head_HeadBrandJump` | |
| `set_SpaceArmorJump` | |
| `set_WitchJump` | |

</details>


---

### Enum: `ai_scale`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](./Characters_and_Bosses.md#context-properties)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |
| `.25` | |
| `.01` | |

</details>


---

### Enum: `ambient_sound`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root), [`Rain`](./House_and_Environment.md#context-rain), [`Snow`](./House_and_Environment.md#context-snow), [`Thunderstorm`](./House_and_Environment.md#context-thunderstorm), [`Windy`](./House_and_Environment.md#context-windy)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `amb_rain.ogg` | |
| `amb_windy.ogg` | |
| `amb_flyswarm.ogg` | |
| `amb_heavyrain.ogg` | |
| `amb_snow.ogg` | |
| `amb_acidrain.ogg` | |
| `amb_blizzard.ogg` | |
| `amb_butterflyswarm.ogg` | |
| `amb_sandstorm.ogg` | |
| `amb_thunderstorm.ogg` | |

</details>


---

### Enum: `boss_cutscene`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`boss`](./Map_Generation_and_Routing.md#context-boss), [`mw_boss`](./Map_Generation_and_Routing.md#context-mw_boss)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `alienqueen` | |
| `boris` | |
| `chaos` | |
| `chubsandnubs` | |
| `coven` | |
| `dybbuk` | |
| `hitler` | |
| `johnny` | |
| `lordbunga` | |
| `megadino` | |
| `moonhead` | |
| `pebbles` | |
| `radicalrat` | |
| `spiderkitten` | |
| `thecreator` | |
| `themother` | |
| `throbbingking` | |

</details>


---

### Enum: `level_display`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`beanies_quests_repeat`](./Progression_Unlocks.md#context-beanies_quests_repeat), [`frank_max_intro`](./Progression_Unlocks.md#context-frank_max_intro), [`frank_max_repeating`](./Progression_Unlocks.md#context-frank_max_repeating), [`jack_max_intro`](./Progression_Unlocks.md#context-jack_max_intro), [`jack_max_repeating`](./Progression_Unlocks.md#context-jack_max_repeating), [`organ_max_intro`](./Progression_Unlocks.md#context-organ_max_intro), [`organ_max_repeating`](./Progression_Unlocks.md#context-organ_max_repeating), [`steven_milliontrashed`](./Progression_Unlocks.md#context-steven_milliontrashed), [`tink_max_intro`](./Progression_Unlocks.md#context-tink_max_intro), [`tink_max_repeating`](./Progression_Unlocks.md#context-tink_max_repeating), [`tracy_max_intro`](./Progression_Unlocks.md#context-tracy_max_intro), [`tracy_max_repeating`](./Progression_Unlocks.md#context-tracy_max_repeating), [`upgrade_storage_repeating_crazy`](./Progression_Unlocks.md#context-upgrade_storage_repeating_crazy), [`upgrade_storage_repeating_hard`](./Progression_Unlocks.md#context-upgrade_storage_repeating_hard), [`upgrade_storage_repeating_impossible`](./Progression_Unlocks.md#context-upgrade_storage_repeating_impossible), [`upgrade_storage_repeating_intro`](./Progression_Unlocks.md#context-upgrade_storage_repeating_intro), [`upgrade_storage_repeating_normal`](./Progression_Unlocks.md#context-upgrade_storage_repeating_normal)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `max` | |

</details>


---

### Enum: `restrict`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`get_item_from_pool`](./Events_and_Encounters.md#context-get_item_from_pool)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `trinket` | |
| `consumables` | |
| `weapon` | |
| `armor` | |

</details>


---

### Enum: `struggle_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Consumed`](./Abilities_and_Spells.md#context-consumed), [`Consumed`](./Characters_and_Bosses.md#context-consumed)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Thrash` | |
| `LennyStruggle` | |
| `CHuskStruggle` | |
| `CaveWomanEscape` | |
| `MoonHandFlail` | |
| `MoonHeadFlail` | |
| `PteroTryEscape` | |
| `TinaFlail` | |
| `TinaFlailRage` | |

</details>


---

### Enum: `GainDisorderFromPool_PostCast`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToRandomPartyMemberIfPossible`](./Abilities_and_Spells.md#context-applytorandompartymemberifpossible), [`Conditional_GoodRoll`](./Abilities_and_Spells.md#context-conditional_goodroll), [`Else`](./Abilities_and_Spells.md#context-else)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `forbidden_spell_consequences` | |
| `forbidden_spell_consequences_crippling` | |

</details>


---

### Enum: `RemoveStatus`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss), [`Conditional_HasStatus`](./Abilities_and_Spells.md#context-conditional_hasstatus), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects), [`StatusOnTookDamage`](./Items_and_Equipment.md#context-statusontookdamage)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Petrify` | |
| `Brace` | |
| `AlphaCat` | |
| `DodgeChance_Status` | |
| `Drowsy` | |
| `DybbukPossessed` | |
| `Sleep` | |
| `SleepParalysis` | |
| `SpeedUp_WithoutInitiative` | |
| `T2CopyCatInternal` | |

</details>


---

### Enum: `SpawnOnBattleStart`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`innate_passives`](./Cat_Classes.md#context-innate_passives), [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BeefyCharmedLeech` | |
| `CharmedTinySpider` | |
| `BuffCharmedKitten` | |
| `CharmedCultist` | |
| `CharmedGamete` | |
| `Crow` | |
| `ZombieCatFamiliar` | |

</details>


---

### Enum: `SpawnThingOnDeath`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives), [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CharmedDemonKitten` | |
| `CharmedTinyTumor` | |
| `CharmedFlySwarm` | |
| `CharmedPooter` | |
| `Boulder` | |
| `CharmedReaper` | |
| `Food` | |
| `Gamete` | |
| `TheIntruder` | |
| `ZombieCatFamiliar` | |

</details>


---

### Enum: `auto_run_priority`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](./Characters_and_Bosses.md#context-properties)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `support` | |
| `stationary` | |
| `default` | |

</details>


---

### Enum: `default_face`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Cat_Classes.md#context-graphics), [`ROOT`](./Custom_Cats.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `mad` | |
| `worried` | |
| `happy` | |
| `angry` | |

</details>


---

### Enum: `face`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`equipment`](./Characters_and_Bosses.md#context-equipment)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AtomicMark` | |
| `ButcherMask` | |
| `ButcherMask_Terminator` | |
| `HuntersPatch` | |
| `HuntersPatch_Terminator` | |
| `MetalPlate` | |
| `MetalPlate_Terminator` | |
| `MonkMask` | |
| `MuggerMask` | |
| `NecromancerMask` | |
| `NecromancerMask_Terminator` | |
| `PsychicMask` | |
| `PsychicMask_Terminator` | |
| `Rabiesface` | |
| `TerminatorCoolGlasses` | |
| `WesternHat` | |

</details>


---

### Enum: `hint_destination`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `core` | |
| `meatworld` | |
| `dimensionx` | |
| `moon` | |
| `boneyard` | |
| `caves` | |
| `endoftime` | |
| `jurassic` | |
| `lab` | |
| `theend` | |

</details>


---

### Enum: `move_for_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MoveClose`](./Characters_and_Bosses.md#context-moveclose), [`MoveForBarrage`](./Characters_and_Bosses.md#context-moveforbarrage), [`MoveForDash`](./Characters_and_Bosses.md#context-movefordash), [`MoveForGrass`](./Characters_and_Bosses.md#context-moveforgrass), [`MoveForPounce`](./Characters_and_Bosses.md#context-moveforpounce), [`MoveForSpin`](./Characters_and_Bosses.md#context-moveforspin), [`MoveForThrow`](./Characters_and_Bosses.md#context-moveforthrow), [`MoveOneForPuke`](./Characters_and_Bosses.md#context-moveoneforpuke), [`MoveToHead`](./Characters_and_Bosses.md#context-movetohead), [`MoveTowards`](./Characters_and_Bosses.md#context-movetowards), [`SpearRun`](./Characters_and_Bosses.md#context-spearrun), [`Unflip`](./Characters_and_Bosses.md#context-unflip)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |
| `CaveManPickupSpear` | |
| `Spin_Enemy` | |
| `AlienBeastPuke` | |
| `G3GrabHead` | |
| `PyrophinaSoloCatThrow` | |
| `PyrophinaVSCatThrow` | |
| `PyrophinaVSSpinThrow` | |
| `StegoEatGrass` | |
| `ZaratanaVSBombardment` | |

</details>


---

### Enum: `rare`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BossRewards`](./Characters_and_Bosses.md#context-bossrewards)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AlienStalk` | |
| `AlienTech` | |
| `BorisBrain` | |
| `BungasCrown` | |
| `DybbuksRib` | |
| `ForbiddenPill` | |
| `GambitsDice` | |
| `GreenWhistle` | |
| `HitlersMustache` | |
| `JohnnysStool` | |
| `MothersLove` | |
| `QueensCrown` | |
| `RadGlasses` | |
| `SpiderBaby` | |
| `UnstableDNA` | |
| `ZodiacsSixshooter` | |

</details>


---

### Enum: `raw_damage`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |
| `X*2` | |
| `X-1` | |
| `2*X` | |
| `X*3` | |
| `X*6` | |
| `X+1` | |
| `int` | |
| `item_aux` | |

</details>


---

### Enum: `AbilityOnBattleStart`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`self_status_next_fight`](./Events_and_Encounters.md#context-self_status_next_fight), [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Flush` | |
| `Heathens` | |
| `Heathens2` | |
| `MegaFart` | |
| `RandomDualSoulLink` | |
| `RandomReap` | |
| `RandomReap2` | |
| `RandomSoulLink` | |
| `face_FartFace` | |
| `face_FartFaceFixed` | |
| `face_LeechBrood` | |
| `head_SpiderInjector` | |
| `head_SpiderInjectorFixed` | |
| `neck_ChefsApron` | |
| `wp_TheLonerAuto` | |

</details>


---

### Enum: `AbilityReaction`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives), [`passives`](./Characters_and_Bosses.md#context-passives), [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AnkyloSpin` | |
| `GSOpen` | |
| `Gassy_AssBlast` | |
| `Gassy_AssBlast2` | |
| `HeadTumorResponse` | |
| `HemBounce` | |
| `IDSprout` | |
| `MoonWormCurl` | |
| `PissYourself` | |
| `SCSneakUp` | |
| `SkunkTail` | |
| `TC_DashReaction` | |
| `ToxGasBlast` | |
| `attack` | |
| `head_EmoSong` | |

</details>


---

### Enum: `Buddy`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives), [`AddPassivesToMinions`](./Items_and_Equipment.md#context-addpassivestominions)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BoyDino` | |
| `CaveCatDad` | |
| `Chubs` | |
| `DrMangler` | |
| `GirlDino` | |
| `Guillotina2Body` | |
| `Guillotina2Head` | |
| `Guillotina3Body` | |
| `Guillotina3Head` | |
| `ManglersMonster` | |
| `Nubs` | |
| `Ornstein` | |
| `Smough` | |
| `choose_favorite_cat` | |
| `spawner` | |

</details>


---

### Enum: `chain_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BoyDinoDash` | |
| `ChaosStacyAttackChain` | |
| `ControlPlantsPartTwo` | |
| `ControlPlantsPartTwo2` | |
| `ControlWaterPartTwo` | |
| `ControlWaterPartTwo2` | |
| `Dump` | |
| `G3Rage` | |
| `GSChew` | |
| `GSSpit` | |
| `HitlerHeadTransform_Chain` | |
| `MegaGuppy_DropTrash` | |
| `MotherGrow` | |
| `T3Leave` | |
| `T3YellB` | |

</details>


---

### Enum: `kill`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cat` | |

</details>


---

### Enum: `move_then_do`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonusturn_pattern`](./Characters_and_Bosses.md#context-bonusturn_pattern), [`fallback`](./Characters_and_Bosses.md#context-fallback), [`mainturn_pattern`](./Characters_and_Bosses.md#context-mainturn_pattern), [`pattern`](./Characters_and_Bosses.md#context-pattern)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |
| `NubsJump` | |
| `CHuskCatShade` | |
| `CerberubsBarrage` | |
| `CerberubsCalm` | |
| `RatKingSpawn` | |
| `RockSong` | |
| `SimonFlopper_SpawnMinion` | |

</details>


---

### Enum: `str_aux_initialize`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `random_class_passive` | |
| `random_seed` | |
| `random_class_ability` | |
| `random_copyable_class_ability` | |
| `random_copyable_colorless_ability` | |
| `random_copyable_colorless_passive` | |
| `random_disorder` | |
| `random_passive_trinket` | |
| `random_stat` | |

</details>


---

### Enum: `ChangeCatClass`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Butcher` | |
| `Colorless` | |
| `Druid` | |
| `Fighter` | |
| `Hunter` | |
| `Jester` | |
| `Mage` | |
| `Medic` | |
| `Monk` | |
| `Necromancer` | |
| `Psychic` | |
| `Tank` | |
| `Thief` | |
| `Tinkerer` | |

</details>


---

### Enum: `HealthMultiplier`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.8` | |
| `.5` | |

</details>


---

### Enum: `TileTrail`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#context-temporary_effects), [`passives`](./Characters_and_Bosses.md#context-passives), [`passives`](./Elite_Buffs.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FireTile` | |
| `CreepTile` | |
| `FlowerTile` | |
| `GrassTile` | |
| `BrambleTile` | |
| `FloatingGlassTile` | |
| `GlassTile` | |
| `ShadowTile` | |
| `WaterTile` | |

</details>


---

### Enum: `TransformBasicAttack`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `HornCharge` | |
| `Pilfer` | |
| `ThrowPoop` | |
| `AntlerSwipe` | |
| `AntlerSwipe2` | |
| `Chitter` | |
| `MockSong` | |
| `MockSong2` | |
| `TigerSwipes` | |
| `TigerSwipes2` | |
| `Timber` | |

</details>


---

### Enum: `VisualFX`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss), [`effects`](./Abilities_and_Spells.md#context-effects), [`Conditional_HasCleansableDebuffs`](./Items_and_Equipment.md#context-conditional_hascleansabledebuffs), [`effects`](./Items_and_Equipment.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `WaterConduct` | |
| `MagicMissleBlast` | |
| `PartyExplosion` | |
| `BigMagicMissileBlast` | |
| `Bolt` | |
| `Cleanse` | |
| `Explosion` | |
| `Holyatk` | |

</details>


---

### Enum: `animation_suffix`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Big`](./Characters_and_Bosses.md#context-big), [`Explody`](./Characters_and_Bosses.md#context-explody), [`FireFull`](./Characters_and_Bosses.md#context-firefull), [`Grown`](./Characters_and_Bosses.md#context-grown), [`HumanDead`](./Characters_and_Bosses.md#context-humandead), [`NormalFull`](./Characters_and_Bosses.md#context-normalfull), [`Nuke`](./Characters_and_Bosses.md#context-nuke), [`Off`](./Characters_and_Bosses.md#context-off), [`Open`](./Characters_and_Bosses.md#context-open), [`OpenCat`](./Characters_and_Bosses.md#context-opencat), [`Sitting`](./Characters_and_Bosses.md#context-sitting), [`TarFull`](./Characters_and_Bosses.md#context-tarfull), [`Turtled`](./Characters_and_Bosses.md#context-turtled)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Full` | |
| `Turtle` | |
| `Big` | |
| `Chair` | |
| `DH` | |
| `Expl` | |
| `Grown` | |
| `Nuke` | |
| `Off` | |
| `Open` | |
| `OpenCat` | |

</details>


---

### Enum: `cant_cast`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`cost`](./Abilities_and_Spells.md#context-cost)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |
| `1-X` | |
| `2-X` | |
| `3-X` | |
| `5-X` | |
| `X-1` | |
| `X-5` | |
| `X-65` | |
| `X-75` | |

</details>


---

### Enum: `complete_checklist_with_class`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Butcher` | |
| `Colorless` | |
| `Druid` | |
| `Fighter` | |
| `Hunter` | |
| `Jester` | |
| `Mage` | |
| `Medic` | |
| `Monk` | |
| `Necromancer` | |
| `Psychic` | |
| `Tank` | |
| `Thief` | |
| `Tinkerer` | |

</details>


---

### Enum: `copy_results`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`blue`](./Events_and_Encounters.md#context-blue), [`button`](./Events_and_Encounters.md#context-button), [`examine`](./Events_and_Encounters.md#context-examine), [`open`](./Events_and_Encounters.md#context-open), [`smash`](./Events_and_Encounters.md#context-smash)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `examine` | |
| `smash` | |
| `open` | |
| `lever` | |
| `red` | |

</details>


---

### Enum: `corpse_health`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](./Characters_and_Bosses.md#context-properties)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `indestructible` | |

</details>


---

### Enum: `head`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`equipment`](./Characters_and_Bosses.md#context-equipment)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BabyHair` | |
| `Banana` | |
| `BulbHead` | |
| `CoinBag` | |
| `CoinBag_Terminator` | |
| `Dreadlocks` | |
| `JesterHat` | |
| `JesterHat_Terminator` | |
| `LoansharksFedora` | |
| `MonkMask_Terminator` | |
| `Pebble` | |
| `Pebble_Terminator` | |
| `TinkererHat` | |
| `TinkererHat_Terminator` | |

</details>


---

### Enum: `lose_item`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `inventory` | |
| `equipped` | |
| `parasite` | |
| `weapon` | |

</details>


---

### Enum: `move_start_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `startroll` | |
| `backflipStart` | |
| `buttScootStart` | |
| `cartwheelStart` | |
| `jetbegin` | |
| `moveStart` | |
| `none` | |
| `runStart` | |

</details>


---

### Enum: `preferred_distance`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Enemy_AI.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `mov` | |
| `mov+1` | |
| `mov+5` | |
| `mov+reach` | |
| `mov-2` | |
| `reach` | |

</details>


---

### Enum: `shop_now`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`main`](./Events_and_Encounters.md#context-main), [`rare`](./Events_and_Encounters.md#context-rare), [`traverse`](./Events_and_Encounters.md#context-traverse)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Event_SmallShop` | |
| `Event_RareShop` | |
| `TreasureHard` | |
| `TreasureEasy` | |

</details>


---

### Enum: `ClassFromNeutral,`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Cat_Classes.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ButcherFromNeutral` | |
| `DruidFromNeutral` | |
| `FighterFromNeutral` | |
| `HealerFromNeutral` | |
| `HunterFromNeutral` | |
| `JesterFromNeutral` | |
| `MageFromNeutral` | |
| `MonkFromNeutral` | |
| `NecromancerFromNeutral` | |
| `PsychicFromNeutral` | |
| `TankFromNeutral` | |
| `ThiefFromNeutral` | |
| `TinkererFromNeutral` | |

</details>


---

### Enum: `ClassToNeutral,`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Cat_Classes.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ButcherToNeutral` | |
| `DruidToNeutral` | |
| `FighterToNeutral` | |
| `HealerToNeutral` | |
| `HunterToNeutral` | |
| `JesterToNeutral` | |
| `MageToNeutral` | |
| `MonkToNeutral` | |
| `NecromancerToNeutral` | |
| `PsychicToNeutral` | |
| `TankToNeutral` | |
| `ThiefToNeutral` | |
| `TinkererToNeutral` | |

</details>


---

### Enum: `EvolveAbilityFromPool`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill), [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Butcher` | |
| `Druid` | |
| `Fighter` | |
| `Hunter` | |
| `JesterMinusColorless` | |
| `Mage` | |
| `Medic` | |
| `Monk` | |
| `Necromancer` | |
| `Psychic` | |
| `Tank` | |
| `Thief` | |
| `Tinkerer` | |

</details>


---

### Enum: `StartTurn,`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Cat_Classes.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ButcherStartTurn` | |
| `DruidStartTurn` | |
| `FighterStartTurn` | |
| `HealerStartTurn` | |
| `HunterStartTurn` | |
| `JesterStartTurn` | |
| `MageStartTurn` | |
| `MonkStartTurn` | |
| `NecromancerStartTurn` | |
| `PsychicStartTurn` | |
| `TankStartTurn` | |
| `ThiefStartTurn` | |
| `TinkererStartTurn` | |

</details>


---

### Enum: `Victory,`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Cat_Classes.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `butcherVictory` | |
| `clericVictory` | |
| `druidVictory` | |
| `fighterVictory` | |
| `hunterVictory` | |
| `jesterVictory` | |
| `mageVictory` | |
| `monkVictory` | |
| `necromancerVictory` | |
| `psychicVictory` | |
| `tankVictory` | |
| `thiefVictory` | |
| `tinkererVictory` | |

</details>


---

### Enum: `catdata`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#context-spawn)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `clone` | |
| `clone_consumed` | |
| `fleshgolem` | |
| `item_aux_catid` | |
| `teamclone` | |

</details>


---

### Enum: `deathsound`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Injuries.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Injury_Burn` | |
| `Injury_Cursed` | |
| `Injury_Bleed` | |
| `Injury_BrokenLeg` | |
| `Injury_BrokenPaw` | |
| `Injury_BrokenRib` | |
| `Injury_Concussion` | |
| `Injury_Disfigured` | |
| `Injury_Poison` | |
| `Injury_TornTendon` | |
| `Shade_Fade` | |

</details>


---

### Enum: `hidden_tags`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](./Characters_and_Bosses.md#context-properties)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `terminator_mini` | |

</details>


---

### Enum: `hint_chapter_exit`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`enter`](./Events_and_Encounters.md#context-enter), [`future`](./Events_and_Encounters.md#context-future), [`home`](./Events_and_Encounters.md#context-home), [`ignore`](./Events_and_Encounters.md#context-ignore), [`infinite`](./Events_and_Encounters.md#context-infinite), [`past`](./Events_and_Encounters.md#context-past)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `home` | |
| `endoftime` | |
| `dimensionx` | |
| `future` | |
| `iceage` | |
| `jurassic` | |
| `theend` | |

</details>


---

### Enum: `move_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MoveWhenDamaged`](./Cat_Mutations.md#context-movewhendamaged), [`MoveAwayFromDamageSource`](./Characters_and_Bosses.md#context-moveawayfromdamagesource), [`MoveAwayWhenEnemyAdjacent`](./Characters_and_Bosses.md#context-moveawaywhenenemyadjacent), [`MoveTowardsDamageSource`](./Characters_and_Bosses.md#context-movetowardsdamagesource), [`MoveTowardsKillers`](./Characters_and_Bosses.md#context-movetowardskillers), [`MoveWhenDamaged`](./Characters_and_Bosses.md#context-movewhendamaged), [`Terminator2Run`](./Characters_and_Bosses.md#context-terminator2run), [`MoveTowardsDamageSource`](./Passives_and_Statuses.md#context-movetowardsdamagesource)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SpiderReturn` | |
| `MoveOne` | |
| `BirdFly` | |
| `MD_WalkOne` | |
| `T2GoopRun` | |
| `TrampleMove` | |
| `TrampleMoveOne` | |
| `WaterTrailMove` | |
| `YA_Jetpack` | |
| `move` | |

</details>


---

### Enum: `move_end_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `endroll` | |
| `backflipEnd` | |
| `buttScootEnd` | |
| `cartwheelEnd` | |
| `jetend` | |
| `moveEnd` | |
| `none` | |

</details>


---

### Enum: `obj`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BounceObject`](./Abilities_and_Spells.md#context-bounceobject), [`Buddy`](./Characters_and_Bosses.md#context-buddy), [`MultiSpawnOnDeath`](./Characters_and_Bosses.md#context-multispawnondeath), [`SpawnOnDeath`](./Characters_and_Bosses.md#context-spawnondeath), [`TransformOnDeathImmediately`](./Characters_and_Bosses.md#context-transformondeathimmediately), [`SpawnOnDeath`](./Items_and_Equipment.md#context-spawnondeath)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `chapter_corpse_medium` | |
| `BeefyCharmedLeech` | |
| `Dice` | |
| `Maggot` | |
| `PyrophinaVS` | |
| `RiftKitten` | |
| `SkeletonCatCorpse` | |
| `SkeletonCatCorpseFamiliar` | |
| `SkeletonShamblerCorpse` | |
| `SmallLavaRock` | |
| `TallSkeletonCatCorpse` | |
| `ZaratanaVS` | |

</details>


---

### Enum: `portrait_face`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Cat_Classes.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `butcher_portrait` | |
| `druid_portrait` | |
| `fighter_portrait` | |
| `hunter_portrait` | |
| `jester_portrait` | |
| `mage_portrait` | |
| `medic_portrait` | |
| `monk_portrait` | |
| `necromancer_portrait` | |
| `psychic_portrait` | |
| `tank_portrait` | |
| `thief_portrait` | |
| `tinkerer_portrait` | |

</details>


---

### Enum: `trigger_adventure_unlock`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `end_of_time_unlock` | |
| `legacy_event_unlock_momsknife` | |
| `map_unlock_dimensionx` | |
| `meat_world_unlock` | |
| `map_unlock_iceage` | |
| `meat_world_open` | |
| `time_machine_quest_finalstep` | |
| `time_machine_quest_trigger` | |

</details>


---

### Enum: `unlock_quest_item`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BlackShard` | |
| `CryogenicTimeChamber_Empty` | |
| `GuillotinasHead` | |
| `JarOfRadiation` | |
| `Nuke` | |
| `PutridLeech` | |
| `PyrophinasCollar` | |
| `ReceiverAntenna` | |
| `ScaldingOrb` | |
| `SignalAmplifier` | |
| `ThrobbingGristle` | |
| `TransmitterAntenna` | |
| `ZaratanasCollar` | |

</details>


---

### Enum: `AddTag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./Abilities_and_Spells.md#context-applypassives), [`passives`](./Characters_and_Bosses.md#context-passives), [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `rock` | |
| `bug` | |
| `cat` | |
| `fetus` | |
| `plant` | |
| `squirrel` | |
| `tumor` | |

</details>


---

### Enum: `DeadAltAbility`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CarrionShot_Afterlife` | |
| `CarrionShot_Afterlife2` | |
| `CoffinFlop_Afterlife` | |
| `CoffinFlop_Afterlife2` | |
| `DonateBlood_Afterlife` | |
| `DonateBlood_Afterlife2` | |
| `LifeDrain_Afterlife` | |
| `LifeDrain_Afterlife2` | |
| `Seance_Afterlife` | |
| `Seance_Afterlife2` | |
| `TradeLife_Afterlife` | |
| `TradeLife_Afterlife2` | |

</details>


---

### Enum: `EquipTemporaryItem`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives), [`StatusAlliesOnBattleStart`](./Passives_and_Statuses.md#context-statusalliesonbattlestart), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ButcherHook_Temporary` | |
| `Necro_SoulDagger_Uncharged` | |
| `SleepDart` | |
| `SleepDart2` | |
| `Bottles` | |
| `FoodBig` | |
| `FoodMedium` | |
| `WaterBottle_Full` | |

</details>


---

### Enum: `ImmediateAbilityReaction`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CerberubsShotgunReactionX` | |
| `TVOff` | |
| `BirthwortReactionShot` | |
| `BumbleButt` | |
| `CatGoop` | |
| `CerberubsStraightReaction` | |
| `ChubsGoop` | |
| `NubsGoop` | |

</details>


---

### Enum: `SizeScale`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects), [`StacyMutant_Speed`](./Characters_and_Bosses.md#context-stacymutant_speed), [`passives`](./Elite_Buffs.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.75` | |
| `.6` | |
| `.8` | |
| `.4` | |
| `.7` | |

</details>


---

### Enum: `StatusImmunity`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives), [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Webbed` | |
| `Poison` | |
| `Burn` | |
| `Tarred` | |

</details>


---

### Enum: `TransformOnDeath`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BishopHat` | |
| `CanCreeperOut` | |
| `Carcus` | |
| `Chummy` | |
| `CraterCreeperOut` | |
| `Dip` | |
| `HydrantFountain` | |
| `RatKing` | |
| `SimonFlopper` | |
| `Tatters` | |
| `ThrobbingKing2` | |
| `TumorBarrier` | |

</details>


---

### Enum: `UseAbility`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_InForm`](./Abilities_and_Spells.md#context-conditional_inform), [`effects`](./Abilities_and_Spells.md#context-effects), [`StatusEachRoundEnd`](./Cat_Mutations.md#context-statuseachroundend), [`passives`](./Characters_and_Bosses.md#context-passives), [`statuses_on_enter_form`](./Characters_and_Bosses.md#context-statuses_on_enter_form), [`StatusAfterCastSpell`](./Items_and_Equipment.md#context-statusaftercastspell), [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `KirbySpit` | |
| `neck_DarkFriend` | |
| `GirlDinoPoop` | |
| `MD_PoopChain` | |
| `ManglerThrowRemote` | |
| `MegaGuppy_SummonTheChild` | |
| `MoonHandPunchHead` | |
| `MoonHead_CommandHeadPunch` | |
| `Spit` | |
| `TormentorRuneAbsorb` | |

</details>


---

### Enum: `begin_chapter`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `home` | |
| `endoftime.gon` | |
| `iceage.gon` | |
| `dimensionx.gon` | |
| `future.gon` | |
| `jurassic.gon` | |
| `theend.gon` | |

</details>


---

### Enum: `cantrip_group`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`cost`](./Abilities_and_Spells.md#context-cost)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `kaiju_roar` | |
| `cavemomtoss` | |
| `spewer_suck` | |
| `THC_CoinRoll` | |

</details>


---

### Enum: `heal`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `5+bonus_melee_damage` | |
| `10+bonus_ranged_damage` | |
| `X` | |
| `1+bonus_basic_spell_damage` | |
| `1+bonus_ranged_damage` | |
| `4+bonus_melee_damage` | |
| `X+1` | |
| `item_aux` | |

</details>


---

### Enum: `lose_specific_item`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SlagTight` | |
| `CryogenicTimeChamber_Full` | |
| `PutridLeech` | |
| `PyrophinasCollar` | |
| `ReceiverAntenna` | |
| `SignalAmplifier` | |
| `ThrobbingGristle` | |
| `TransmitterAntenna` | |
| `ZaratanasCollar` | |

</details>


---

### Enum: `palette`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CatPartsTransform`](./Characters_and_Bosses.md#context-catpartstransform)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Butcher` | |
| `Druid` | |
| `Fighter` | |
| `Hunter` | |
| `Mage` | |
| `Medic` | |
| `Monk` | |
| `Necromancer` | |
| `Psychic` | |
| `Tank` | |
| `Thief` | |
| `Tinkerer` | |

</details>


---

### Enum: `range`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AllStatsAura`](./Characters_and_Bosses.md#context-allstatsaura), [`DepressionAura`](./Elite_Buffs.md#context-depressionaura), [`AbilityWhenTaggedCharacterMovesNear`](./Passives_and_Statuses.md#context-abilitywhentaggedcharactermovesnear), [`AllyHealthRegenAura`](./Passives_and_Statuses.md#context-allyhealthregenaura), [`AllyManaRegenAura`](./Passives_and_Statuses.md#context-allymanaregenaura), [`DamageReductionAura`](./Passives_and_Statuses.md#context-damagereductionaura)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `global` | |

</details>


---

### Enum: `set_savefile_flag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root), [`tink_aggression`](./Progression_Unlocks.md#context-tink_aggression), [`tink_basestats`](./Progression_Unlocks.md#context-tink_basestats), [`tink_inbreeding`](./Progression_Unlocks.md#context-tink_inbreeding), [`tink_relationships`](./Progression_Unlocks.md#context-tink_relationships), [`tink_sexuality`](./Progression_Unlocks.md#context-tink_sexuality), [`tink_tags`](./Progression_Unlocks.md#context-tink_tags)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AlienInvasionUnlocked` | |
| `HauntedNightUnlocked` | |
| `PlotFlag_Beanies_Homeless` | |
| `PlotFlag_FrankBeanies` | |
| `RestlessDeadUnlocked` | |
| `RobotUprisingUnlocked` | |
| `catinfo_unlock_aggression` | |
| `catinfo_unlock_basestats` | |
| `catinfo_unlock_inbreeding` | |
| `catinfo_unlock_relationships` | |
| `catinfo_unlock_sexuality` | |
| `catinfo_unlock_tags` | |

</details>


---

### Enum: `YOffset`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./Abilities_and_Spells.md#context-applypassives), [`passives`](./Cat_Mutations.md#context-passives), [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.25` | |
| `.35` | |
| `-.18` | |

</details>


---

### Enum: `animation_fail`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`10coins`](./Events_and_Encounters.md#context-10coins), [`5coins`](./Events_and_Encounters.md#context-5coins), [`ROOT`](./Events_and_Encounters.md#context-root), [`buy1`](./Events_and_Encounters.md#context-buy1), [`donate_10`](./Events_and_Encounters.md#context-donate_10), [`donate_15`](./Events_and_Encounters.md#context-donate_15), [`donate_20`](./Events_and_Encounters.md#context-donate_20), [`donate_5`](./Events_and_Encounters.md#context-donate_5), [`put_in_coins`](./Events_and_Encounters.md#context-put_in_coins)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `choice_no_coins` | |

</details>


---

### Enum: `chain_distance`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.25` | |
| `.38` | |

</details>


---

### Enum: `chain_movieclip`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ChainLink` | |
| `Frogchain` | |
| `Bramblechain` | |

</details>


---

### Enum: `partial_animation_suffix`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Alert`](./Characters_and_Bosses.md#context-alert), [`Bomb`](./Characters_and_Bosses.md#context-bomb), [`Drunker`](./Characters_and_Bosses.md#context-drunker), [`FlushHost`](./Characters_and_Bosses.md#context-flushhost), [`Grappling`](./Characters_and_Bosses.md#context-grappling), [`JohnnyHost`](./Characters_and_Bosses.md#context-johnnyhost), [`Lit`](./Characters_and_Bosses.md#context-lit), [`Primed`](./Characters_and_Bosses.md#context-primed), [`ThrobHost`](./Characters_and_Bosses.md#context-throbhost), [`Unlit`](./Characters_and_Bosses.md#context-unlit), [`Unwashed`](./Characters_and_Bosses.md#context-unwashed)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Host` | |
| `Alert` | |
| `Button` | |
| `Drunk` | |
| `Grapple` | |
| `Lit` | |
| `Unlit` | |
| `Unwashed` | |
| `primed` | |

</details>


---

### Enum: `prereq`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BasementUpgrade`](./House_and_Environment.md#context-basementupgrade), [`BasementUpgrade2`](./House_and_Environment.md#context-basementupgrade2), [`BasementUpgrade3`](./House_and_Environment.md#context-basementupgrade3), [`BasementUpgrade4`](./House_and_Environment.md#context-basementupgrade4), [`BasementUpgrade5`](./House_and_Environment.md#context-basementupgrade5), [`LargeHouse`](./House_and_Environment.md#context-largehouse), [`LargeHouse_Floor2Large`](./House_and_Environment.md#context-largehouse_floor2large), [`LargeHouse_Floor2Small`](./House_and_Environment.md#context-largehouse_floor2small), [`MediumHouse`](./House_and_Environment.md#context-mediumhouse), [`MediumHouse_SmallRoom`](./House_and_Environment.md#context-mediumhouse_smallroom), [`SmallHouse_Attic`](./House_and_Environment.md#context-smallhouse_attic)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MediumHouse` | |
| `Default` | |
| `LargeHouse` | |
| `BasementUpgrade` | |
| `BasementUpgrade2` | |
| `BasementUpgrade3` | |
| `BasementUpgrade4` | |

</details>


---

### Enum: `weights`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MoveWhenDamaged`](./Cat_Mutations.md#context-movewhendamaged), [`MoveAfterAnyAttemptedAttack`](./Characters_and_Bosses.md#context-moveafteranyattemptedattack), [`MoveAwayWhenEnemyAdjacent`](./Characters_and_Bosses.md#context-moveawaywhenenemyadjacent), [`MoveWhenDamaged`](./Characters_and_Bosses.md#context-movewhendamaged), [`MoveWhenDamaged`](./Passives_and_Statuses.md#context-movewhendamaged)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `stay_far_always_move` | |
| `chaotic` | |
| `bat_chaos_runaway` | |
| `stay_near_allies_always_move` | |

</details>


---

### Enum: `ImmediateUseAbility`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](./Abilities_and_Spells.md#context-conditional_goodroll), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects), [`StatusOnEnemyConfused`](./Characters_and_Bosses.md#context-statusonenemyconfused), [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend), [`StatusOnEndMove`](./Items_and_Equipment.md#context-statusonendmove)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `HitlerCloneTransform` | |
| `FuzzerReact` | |
| `HitlerCloneHeil` | |
| `MoonHandMegaSqueeze` | |
| `cm_Lard_Impl` | |
| `head_MagnetoAttract` | |
| `head_ThrobbingCrown` | |
| `tk_ButterBean_Mega` | |
| `tk_ButterBean_Normal` | |

</details>


---

### Enum: `Shield`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects), [`StatusOnGainCoins`](./Items_and_Equipment.md#context-statusongaincoins)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |
| `-X` | |
| `2*X` | |
| `3*X` | |
| `5+bonus_ranged_damage` | |
| `8+X` | |
| `X+1` | |
| `item_aux` | |

</details>


---

### Enum: `SpawnThingIfHitKills`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#context-conditional_healththreshold), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Food` | |
| `Bait` | |
| `BigFood` | |
| `BiggestFood` | |

</details>


---

### Enum: `beam_cap`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `thinlasercap` | |
| `fx_bloatlasercap` | |
| `greenlasercap` | |
| `Gambitmouthbeamcap` | |
| `fx_kingbloodlasercap` | |
| `greenmegalasercap` | |

</details>


---

### Enum: `beam_clip`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `thinlaser` | |
| `fx_bloatlaser` | |
| `greenlaser` | |
| `Gambitmouthbeam` | |
| `fx_kingbloodlaser` | |
| `greenmegalaser` | |

</details>


---

### Enum: `end`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `spinattackend` | |
| `attack` | |
| `lickAttack` | |
| `monkAttack` | |
| `upswipe` | |

</details>


---

### Enum: `jump_start_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bellyflopStart` | |
| `none` | |
| `enterbattle` | |
| `gravitySlamStart` | |
| `leapattackwindup` | |

</details>


---

### Enum: `learn_passive`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DirtyClaws` | |
| `MiniMe` | |
| `Blessed` | |
| `CobraStyle` | |
| `DeathProof` | |
| `Host` | |
| `IcePaws` | |
| `PoisonTips` | |

</details>


---

### Enum: `loop`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |
| `spinattackloop` | |
| `lickAttack` | |
| `monkAttack` | |

</details>


---

### Enum: `move_speed_multiplier`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Mutant`](./Characters_and_Bosses.md#context-mutant), [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |
| `.66` | |
| `.75` | |

</details>


---

### Enum: `neck`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`equipment`](./Characters_and_Bosses.md#context-equipment)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AngelicAura` | |
| `AngelicAura_Terminator` | |
| `DruidNeck` | |
| `DruidNeck_Terminator` | |
| `MageCollar` | |
| `MageCollar_Terminator` | |
| `Poncho` | |
| `SamsonsChains` | |
| `SamsonsChains_Terminator` | |
| `Slime` | |

</details>


---

### Enum: `override_basic_attack`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Passives_and_Statuses.md#context-1), [`2`](./Passives_and_Statuses.md#context-2), [`ROOT`](./Passives_and_Statuses.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicDruidAbilityVersatile` | |
| `BasicMagicMissile` | |
| `BasicMedicRanged` | |
| `BasicButcherMeleeWideDoubleSpin` | |
| `BasicButcherMeleeWideSpin` | |
| `BasicMelee` | |
| `GerdShot` | |

</details>


---

### Enum: `prime_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `chargeholy` | |
| `pointout` | |
| `angry` | |
| `command1` | |
| `command2` | |
| `command3` | |
| `command4` | |
| `prouder` | |

</details>


---

### Enum: `stack_key`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnEachTurn`](./Items_and_Equipment.md#context-spawneachturn), [`StackingFlowerTrail`](./Items_and_Equipment.md#context-stackingflowertrail), [`StatusAfterXStacks`](./Items_and_Equipment.md#context-statusafterxstacks)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CATHIDE` | |
| `FLOWER_SET` | |
| `EMPTY_GENERATOR` | |
| `FANNY_PACK` | |

</details>


---

### Enum: `start`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |
| `spinattackstart` | |
| `lickAttack` | |
| `monkAttack` | |

</details>


---

### Enum: `trigger_house_boss`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pyrophina_vs_zaratana` | |
| `guillotina_1` | |
| `guillotina_2` | |
| `guillotina_3` | |
| `pyrophina` | |
| `terminator_1` | |
| `terminator_2` | |
| `terminator_3` | |
| `zaratana` | |

</details>


---

### Enum: `unlock_room`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BasementUpgrade`](./House_and_Environment.md#context-basementupgrade), [`BasementUpgrade2`](./House_and_Environment.md#context-basementupgrade2), [`BasementUpgrade3`](./House_and_Environment.md#context-basementupgrade3), [`BasementUpgrade4`](./House_and_Environment.md#context-basementupgrade4), [`BasementUpgrade5`](./House_and_Environment.md#context-basementupgrade5), [`Default`](./House_and_Environment.md#context-default), [`LargeHouse_Floor2Large`](./House_and_Environment.md#context-largehouse_floor2large), [`LargeHouse_Floor2Small`](./House_and_Environment.md#context-largehouse_floor2small), [`MediumHouse_SmallRoom`](./House_and_Environment.md#context-mediumhouse_smallroom), [`SmallHouse_Attic`](./House_and_Environment.md#context-smallhouse_attic)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Attic` | |
| `Basement0` | |
| `Basement1` | |
| `Basement2` | |
| `Basement3` | |
| `Basement4` | |
| `Floor1_Large` | |
| `Floor1_Small` | |
| `Floor2_Large` | |
| `Floor2_Small` | |

</details>


---

### Enum: `weapon`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`innate_items`](./Cat_Classes.md#context-innate_items), [`MonkCatReactionAbilities`](./Characters_and_Bosses.md#context-monkcatreactionabilities), [`equipment`](./Characters_and_Bosses.md#context-equipment)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ButcherHook` | |
| `GunslingerPistol` | |
| `AstroTaser` | |
| `CaveCatClub` | |
| `MonkFist` | |
| `OddRemote_Enemy` | |
| `attack` | |

</details>


---

### Enum: `weight`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`main`](./Events_and_Encounters.md#context-main), [`options`](./Events_and_Encounters.md#context-options)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.25` | |
| `.5` | |

</details>


---

### Enum: `AmplifyStatus`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Poison` | |
| `Bleed` | |
| `Rot` | |
| `Burn` | |

</details>


---

### Enum: `ChangeTilesUnder`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects), [`Conditional_GoodRoll`](./Cat_Mutations.md#context-conditional_goodroll), [`StatusOnTookDamage`](./Cat_Mutations.md#context-statusontookdamage), [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `WaterTile` | |
| `GlassTile` | |
| `LavaTile` | |
| `DirtTile` | |
| `TallGrassTile` | |

</details>


---

### Enum: `champ_chance_mini`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`easy`](./Difficulties.md#context-easy), [`hard`](./Difficulties.md#context-hard)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.25` | |
| `.5` | |

</details>


---

### Enum: `choose_cat_with_item`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`intro`](./Events_and_Encounters.md#context-intro)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `PutridLeech` | |
| `ThrobbingGristle` | |
| `TransmitterAntenna` | |
| `CryogenicTimeChamber_Full` | |
| `GuillotinasHead` | |
| `ReceiverAntenna` | |

</details>


---

### Enum: `dead,`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Injuries.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cursedLoop` | |
| `blank` | |
| `brokenLegLoop` | |
| `brokenPawLoop` | |
| `concussionLoop` | |
| `disfiguredLoop` | |
| `dislocatedShoulderLoop` | |
| `intestinalProlapseLoop` | |

</details>


---

### Enum: `intro_cutscene`
<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bunker` | |
| `caves` | |
| `core` | |
| `crater` | |
| `graveyard` | |
| `junkyard` | |
| `moon` | |
| `none` | |
| `sewers` | |

</details>


---

### Enum: `level_up`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `self` | |
| `all` | |

</details>


---

### Enum: `repeat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`beanies_quests_repeat`](./Progression_Unlocks.md#context-beanies_quests_repeat), [`frank_max_repeating`](./Progression_Unlocks.md#context-frank_max_repeating), [`jack_max_repeating`](./Progression_Unlocks.md#context-jack_max_repeating), [`organ_max_repeating`](./Progression_Unlocks.md#context-organ_max_repeating), [`steven_milliontrashed`](./Progression_Unlocks.md#context-steven_milliontrashed), [`tink_max_repeating`](./Progression_Unlocks.md#context-tink_max_repeating), [`tracy_max_repeating`](./Progression_Unlocks.md#context-tracy_max_repeating), [`upgrade_storage_repeating_impossible`](./Progression_Unlocks.md#context-upgrade_storage_repeating_impossible)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `infinite` | |
| `never` | |

</details>


---

### Enum: `set_subject`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`reward`](./Events_and_Encounters.md#context-reward)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dimensionx_head2` | |
| `endorb2` | |
| `monkey_paw_1finger` | |
| `monkey_paw_2fingers` | |
| `monkey_paw_3fingers` | |
| `monkey_paw_4fingers` | |
| `throbbing_artery_noflesh` | |
| `volcano2` | |
| `wall_of_flesh_noartery` | |

</details>


---

### Enum: `AddElement`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToExplosions`](./Passives_and_Statuses.md#context-addstatustoexplosions)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Fire` | |
| `Napalm` | |

</details>


---

### Enum: `ForceSpecificInjury`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cha` | |
| `int` | |
| `lck` | |
| `spd` | |

</details>


---

### Enum: `FreePathfindElement`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives), [`passives`](./Characters_and_Bosses.md#context-passives), [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Grass` | |
| `Water` | |

</details>


---

### Enum: `SpawnOnDowned`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives), [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CharmedKitten` | |
| `CharmedFly` | |
| `CharmedSpookie` | |

</details>


---

### Enum: `crit_chance`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance), [`BoostWeaponDamage`](./Items_and_Equipment.md#context-boostweapondamage), [`BoostWeaponDamage`](./Passives_and_Statuses.md#context-boostweapondamage), [`Shadow`](./Passives_and_Statuses.md#context-shadow)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |
| `.05*X` | |
| `.25` | |

</details>


---

### Enum: `deadhit,`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Injuries.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cursedHit` | |
| `brokenLegHit` | |
| `brokenPawHit` | |
| `concussionHit` | |
| `disfiguredHit` | |
| `dislocatedShoulderHit` | |
| `intestinalProlapseHit` | |

</details>


---

### Enum: `form_offmap`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeOffMap`](./Characters_and_Bosses.md#context-formchangeoffmap)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Default_Ceiling` | |
| `Insane_Ceiling` | |
| `OffMap` | |
| `SpawningPhase` | |
| `Start_Ceiling` | |

</details>


---

### Enum: `form_onmap`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeOffMap`](./Characters_and_Bosses.md#context-formchangeoffmap)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Default_Ground` | |
| `Default` | |
| `Insane_Ground` | |
| `FightPhase` | |

</details>


---

### Enum: `formula`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_FormulaIsPositive`](./Abilities_and_Spells.md#context-conditional_formulaispositive)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |
| `X*10` | |
| `X+1` | |
| `X-1` | |
| `X-2` | |
| `spd` | |

</details>


---

### Enum: `knockback`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance), [`Wind`](./Passives_and_Statuses.md#context-wind)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |
| `2*X` | |
| `X*2` | |
| `X+1` | |
| `level` | |
| `str` | |

</details>


---

### Enum: `odds`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_BadRoll`](./Abilities_and_Spells.md#context-conditional_badroll), [`Conditional_GoodRoll`](./House_and_Environment.md#context-conditional_goodroll), [`Conditional_BadRoll`](./Items_and_Equipment.md#context-conditional_badroll), [`Conditional_BadRoll`](./Passives_and_Statuses.md#context-conditional_badroll)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.1` | |
| `.16666666` | |
| `.3` | |
| `.5` | |

</details>


---

### Enum: `on_store`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `become_aux_coins` | |
| `become_furniture` | |
| `become_rare_furniture` | |

</details>


---

### Enum: `prevent_chain_tag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnOnBattleStart`](./Elite_Buffs.md#context-spawnonbattlestart), [`SpawnCatCopyOnBattleStart`](./Items_and_Equipment.md#context-spawncatcopyonbattlestart), [`SpawnCatCopyWhenDowned`](./Items_and_Equipment.md#context-spawncatcopywhendowned), [`SpawnCatCopyOnBattleStart`](./Passives_and_Statuses.md#context-spawncatcopyonbattlestart)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `minime_clone` | |
| `eb_twin` | |
| `ancestorset_shade` | |
| `necroset_shade` | |

</details>


---

### Enum: `queue_cutscene_immediate`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `caves_intro` | |
| `core_intro` | |
| `desert_intro` | |
| `dybbuk` | |
| `jurassic_intro` | |
| `lab_intro` | |
| `moon_intro` | |
| `theend_intro` | |

</details>


---

### Enum: `reset_npc_sequence`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `beanies_bombquest_2` | |
| `beanies_bombquest_3` | |
| `beanies_bombquest_amnesia` | |
| `beanies_bombquest_begin` | |
| `beanies_bombquest_fail_jarofblood` | |
| `beanies_bombquest_fail_jarofchaos` | |
| `beanies_bombquest_fail_jarofradiation` | |
| `beanies_bombquest_fail_nuke` | |

</details>


---

### Enum: `sub_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CollectiveCounterImpl` | |
| `CollectiveSpinImpl` | |
| `HomingBlasts2_sub` | |
| `HomingBlasts_sub` | |
| `Huddle_Impl` | |
| `Spin` | |
| `TeamFlex_Impl` | |
| `neck_NukeExplode` | |

</details>


---

### Enum: `type_icon`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](./Abilities_and_Spells.md#context-meta)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `magic` | |
| `attack` | |
| `buff` | |
| `melee` | |
| `movement` | |
| `spawn` | |

</details>


---

### Enum: `AbilityWhenBuddyDies`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Guillotina2Rage` | |
| `BoyDinoCry` | |
| `ChubsRage` | |
| `GirlDinoCry` | |
| `ManglerEnrage` | |
| `ManglerMonsterHeartAttack` | |

</details>


---

### Enum: `BrittleDuringElement`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `water` | |

</details>


---

### Enum: `OverrideBasicAttack`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicExplosiveShot` | |
| `BasicMelee` | |
| `BasicMetronome` | |
| `BasicSpin` | |
| `BasicTankMelee` | |
| `GerdShot` | |
| `IsaacBasicAttack` | |

</details>


---

### Enum: `elite_chance_mini`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`easy`](./Difficulties.md#context-easy), [`hard`](./Difficulties.md#context-hard)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.25` | |
| `.5` | |

</details>


---

### Enum: `land_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `none` | |

</details>


---

### Enum: `miss_particle`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `fx_tentaclestrangleMiss` | |

</details>


---

### Enum: `new_layer`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SwitchMusic`](./Abilities_and_Spells.md#context-switchmusic), [`SwitchMusic`](./Characters_and_Bosses.md#context-switchmusic)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `battle` | |
| `event` | |
| `map` | |

</details>


---

### Enum: `npc_script`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](./Shops.md#context-meta)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `tracy_adventure_shop_script.gon` | |

</details>


---

### Enum: `AddHiddenTag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives), [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bowling_ball` | |
| `grown_hitler_clone` | |
| `hitler_clone_fetus` | |
| `the_nuke_bearer` | |
| `unlit_candle` | |

</details>


---

### Enum: `ConjureBonusAbility`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects), [`passives`](./Cat_Mutations.md#context-passives), [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `random` | |
| `Class` | |
| `Colorless` | |
| `Mage` | |

</details>


---

### Enum: `Divide4OnDeath`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BiggestFood` | |
| `Clot` | |
| `MedSlime` | |
| `MedSlimeX` | |
| `SmallSlime` | |
| `SmallSlimeX` | |

</details>


---

### Enum: `ForceUseAbility_NonStack`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll), [`StatusOnOverHealed`](./Passives_and_Statuses.md#context-statusonoverhealed)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Endeavor_Auto` | |
| `Indigestion_Fart` | |
| `Indigestion_Fart2` | |

</details>


---

### Enum: `Imprison`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_FinishedSpawning`](./Abilities_and_Spells.md#context-conditional_finishedspawning), [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Tumor` | |
| `BeefyCharmedLeech` | |
| `CharmedLeech` | |
| `Fly` | |

</details>


---

### Enum: `LevelUpClassOverride`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Jester` | |
| `Colorless` | |

</details>


---

### Enum: `ManaGain`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool), [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |
| `X-1` | |
| `X+2` | |
| `item_aux` | |

</details>


---

### Enum: `ReplaceBasicAttackWhenCastable`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicSuplex` | |
| `Hone` | |
| `Hone2` | |
| `Shank` | |
| `Shank2` | |

</details>


---

### Enum: `SetFragileImmune`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Bionic` | |
| `Cardboard` | |
| `Cool` | |
| `Lucky` | |
| `Paper` | |
| `Wood` | |

</details>


---

### Enum: `TagGreed`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bishop_hat` | |
| `pickup` | |
| `food` | |

</details>


---

### Enum: `ability_icon`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](./Abilities_and_Spells.md#context-meta)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicButcherMeleeWideSpin` | |
| `BasicMelee` | |
| `BasicRanged` | |
| `BasicStraightShot` | |
| `Pestilence` | |
| `Poke` | |

</details>


---

### Enum: `air_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bellyflop_air` | |
| `entrance` | |
| `gravitySlam_air` | |

</details>


---

### Enum: `custom_priming_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `priming` | |
| `idleCommand1` | |
| `idleCommand2` | |
| `idleCommand3` | |
| `idleCommand4` | |

</details>


---

### Enum: `decrement_legacy_counter`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `WorldEventLegacyCounter_CrackInTheWall` | |
| `WorldEventLegacyToken_StartDigging` | |

</details>


---

### Enum: `event`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`next_event_from_set`](./Events_and_Encounters.md#context-next_event_from_set), [`ChanceToForceEvent`](./Items_and_Equipment.md#context-chancetoforceevent)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Tragedy` | |
| `Blessing` | |
| `Death` | |

</details>


---

### Enum: `exclude`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeOnElementInfluence`](./Characters_and_Bosses.md#context-formchangeonelementinfluence), [`BuffImmunity`](./Items_and_Equipment.md#context-buffimmunity)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `water` | |
| `SpellDamageUp` | |
| `fire` | |

</details>


---

### Enum: `fall_randomize_timing`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.3` | |

</details>


---

### Enum: `formchange`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Cat`](./Characters_and_Bosses.md#context-cat), [`NonCat`](./Characters_and_Bosses.md#context-noncat)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BigHolding` | |
| `BigHoldingCat` | |
| `SmallHolding` | |
| `SmallHoldingCat` | |

</details>


---

### Enum: `house_upgrade`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`house_upgrade_4throom`](./Progression_Unlocks.md#context-house_upgrade_4throom), [`house_upgrade_attic`](./Progression_Unlocks.md#context-house_upgrade_attic), [`house_upgrade_largehouse`](./Progression_Unlocks.md#context-house_upgrade_largehouse), [`house_upgrade_mediumhouse`](./Progression_Unlocks.md#context-house_upgrade_mediumhouse)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `LargeHouse` | |
| `LargeHouse_Floor2Large` | |
| `LargeHouse_Floor2Small` | |
| `MediumHouse` | |
| `MediumHouse_SmallRoom` | |
| `SmallHouse_Attic` | |

</details>


---

### Enum: `interstitial_bg_frame`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Floor1_Large`](./House_and_Environment.md#context-floor1_large), [`Floor1_Small`](./House_and_Environment.md#context-floor1_small), [`ROOT`](./House_and_Environment.md#context-root), [`SmallAttic`](./House_and_Environment.md#context-smallattic)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attic` | |
| `room1` | |
| `room2` | |
| `room3` | |
| `room4` | |

</details>


---

### Enum: `key`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_FirstApplicationThisTurn`](./Abilities_and_Spells.md#context-conditional_firstapplicationthisturn), [`Conditional_OncePerBattle`](./Abilities_and_Spells.md#context-conditional_onceperbattle), [`Conditional_OncePerBattle`](./Items_and_Equipment.md#context-conditional_onceperbattle)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `gamewin` | |
| `EtherSoakedRag` | |
| `JewelOfDrog` | |
| `TaintedOffering` | |
| `TaintedOffering2` | |

</details>


---

### Enum: `new_song`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SwitchMusic`](./Abilities_and_Spells.md#context-switchmusic), [`SwitchMusic`](./Characters_and_Bosses.md#context-switchmusic)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `same` | |

</details>


---

### Enum: `not_priming`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeWhilePrimingAbility`](./Characters_and_Bosses.md#context-formchangewhileprimingability)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DualSword` | |
| `NotPriming` | |
| `SwordAndShield` | |

</details>


---

### Enum: `orientation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Spawns_and_Enemy_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `east` | |
| `north` | |
| `south` | |
| `west` | |

</details>


---

### Enum: `preempt_npc_sequence`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `beanies_bombquest_2` | |
| `beanies_bombquest_3` | |
| `beanies_bombquest_amnesia` | |

</details>


---

### Enum: `priming`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeWhilePrimingAbility`](./Characters_and_Bosses.md#context-formchangewhileprimingability)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DualSword_Primed` | |
| `Priming` | |
| `SwordAndShield_Primed` | |

</details>


---

### Enum: `requires_flag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`main`](./Events_and_Encounters.md#context-main)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AlienOvergrowthUnlocked` | |
| `GeomagneticStormUnlocked` | |
| `MeteorShowerUnlocked` | |
| `SolarFlareUnlocked` | |
| `StrangeEggsUnlocked` | |
| `TheShimmerUnlocked` | |

</details>


---

### Enum: `toss_direction_restriction`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `forwards` | |
| `backwards` | |

</details>


---

### Enum: `unlock_boss`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bumblefoot` | |
| `gambit` | |
| `infestedduo` | |
| `jestercat` | |
| `queenhippo` | |
| `ratking` | |

</details>


---

### Enum: `BlacklistPickupType`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `food` | |
| `catnip` | |

</details>


---

### Enum: `Burn`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_FormulaIsPositive`](./Abilities_and_Spells.md#context-conditional_formulaispositive), [`effects`](./Abilities_and_Spells.md#context-effects), [`Fire`](./Passives_and_Statuses.md#context-fire)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |
| `3+bonus_melee_ability_damage` | |
| `X+1` | |

</details>


---

### Enum: `CompleteItemQuest`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill), [`Conditional_OncePerBattle`](./Abilities_and_Spells.md#context-conditional_onceperbattle), [`ScaldingOrbMoonBossOneShot`](./Items_and_Equipment.md#context-scaldingorbmoonbossoneshot)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BlackShard` | |
| `Nuke` | |
| `ScaldingOrb` | |

</details>


---

### Enum: `DeathRattleRevive`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives), [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DoNothing` | |
| `HCHumanDie` | |
| `ToxPuff` | |
| `tk_PetrifiedPinky` | |

</details>


---

### Enum: `DisableAbilitiesWithTag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `consumable` | |
| `musical` | |
| `meat` | |

</details>


---

### Enum: `EquipPermanentItem`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`StatusOnKill`](./Items_and_Equipment.md#context-statusonkill), [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BoneClub` | |
| `Kidney` | |

</details>


---

### Enum: `MoveTowardsDamageSource`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives), [`passives`](./Elite_Buffs.md#context-passives), [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MoveOne` | |

</details>


---

### Enum: `ObjectOnHit`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToTile`](./Abilities_and_Spells.md#context-applytotile), [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Bait` | |
| `BiggestFood` | |
| `Carcus` | |
| `FetusNoJar` | |

</details>


---

### Enum: `ObjectOnHitEmpty`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AnimalEgg` | |
| `AnimalEgg2` | |
| `HeadTumor` | |
| `Maggot` | |
| `SmallRock` | |

</details>


---

### Enum: `OverrideKnockbackDamage`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_FormulaIsPositive`](./Abilities_and_Spells.md#context-conditional_formulaispositive), [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `3+bonus_basic_spell_damage` | |
| `3+bonus_melee_ability_damage` | |
| `X*10` | |
| `str` | |

</details>


---

### Enum: `SetBrittleImmune`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AdvancedAlloy` | |
| `Alloy` | |
| `EliteAlloy` | |
| `JankAlloy` | |
| `Paper` | |

</details>


---

### Enum: `SpawnObjectOnPopCorpse`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Food` | |
| `Catnip` | |
| `Coin` | |

</details>


---

### Enum: `SpecificInjury`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `int` | |
| `str` | |
| `spd` | |

</details>


---

### Enum: `XIsLivingAlliesWithTag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dc_crow` | |
| `terminator_mini` | |
| `hitler_clone_fetus` | |

</details>


---

### Enum: `aoe_tile_requires_element`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Grass` | |
| `Water` | |
| `Earth` | |

</details>


---

### Enum: `current_chapter_common`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `current_chapter_rare`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `current_chapter_uncommon`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `current_chapter_very_rare`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `cutscene_on_exit`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good), [`reward`](./Events_and_Encounters.md#context-reward)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `infinite_intro` | |
| `king_intro` | |

</details>


---

### Enum: `dead`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SetAnimationAlts`](./Abilities_and_Spells.md#context-setanimationalts), [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `skeletonDead` | |
| `deadShot` | |
| `empty` | |

</details>


---

### Enum: `depth_offset`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `-.1` | |
| `.01` | |
| `.015` | |
| `.1` | |

</details>


---

### Enum: `detatched_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `WaterGush` | |
| `LiquidMetalSpear` | |
| `SpearGuyAttack` | |
| `TinaSpear` | |

</details>


---

### Enum: `distance_to_enemy`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Enemy_AI.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.01` | |
| `-.01` | |
| `-.5` | |

</details>


---

### Enum: `drop_on_death`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Consumed`](./Abilities_and_Spells.md#context-consumed), [`Consumed`](./Characters_and_Bosses.md#context-consumed)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `deferred` | |

</details>


---

### Enum: `dying`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SetAnimationAlts`](./Abilities_and_Spells.md#context-setanimationalts), [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dead` | |
| `dyingDisassembled` | |
| `shot` | |

</details>


---

### Enum: `empty_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `empty` | |

</details>


---

### Enum: `hint_prerequisite_flag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `mapflag_BothObelisksUnlocked` | |
| `mapflag_DimensionXUnlocked` | |
| `mapflag_MeatWorldUnlocked` | |
| `mapflag_MeatWorldUnlockedFull` | |

</details>


---

### Enum: `icon_damage_display_eq`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](./Abilities_and_Spells.md#context-meta)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `1+bonus_spell_damage_display` | |
| `3+bonus_melee_ability_damage` | |
| `X*10` | |
| `item_aux` | |

</details>


---

### Enum: `item`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TransformItemOnElementInfluence`](./Items_and_Equipment.md#context-transformitemonelementinfluence)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `EstusFlask_Full` | |
| `WaterBottle_Full` | |
| `GallonOfWater` | |

</details>


---

### Enum: `minion_alt`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Elite_Buffs.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SlightlyDepressing` | |
| `SubTwin` | |
| `SubUndying` | |

</details>


---

### Enum: `mount_mode`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Consumed`](./Abilities_and_Spells.md#context-consumed), [`Consumed`](./Characters_and_Bosses.md#context-consumed)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `sfx`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeOnElementInfluence`](./Characters_and_Bosses.md#context-formchangeonelementinfluence)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FireExtinguish` | |

</details>


---

### Enum: `speed`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `tag_location`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Spawns_and_Enemy_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ChaosValidPosition` | |
| `FinalBossCloneSpot` | |
| `FinalBossTheChildLocation` | |
| `HitlerMiniInitial` | |

</details>


---

### Enum: `tag_restriction`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TeamCastAbility`](./Abilities_and_Spells.md#context-teamcastability), [`SecurityBotProtect`](./Characters_and_Bosses.md#context-securitybotprotect)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `collective` | |
| `dinofamily` | |
| `dc_cat` | |

</details>


---

### Enum: `threshold`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AbilityHealthThreshold`](./Characters_and_Bosses.md#context-abilityhealththreshold), [`FormChangeHealthThreshold`](./Characters_and_Bosses.md#context-formchangehealththreshold)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `1*champion_multiplier` | |
| `2*champion_multiplier` | |
| `3*champion_multiplier` | |
| `4*champion_multiplier` | |
| `X-4` | |

</details>


---

### Enum: `walk`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `stompwalk` | |
| `zombieWalk` | |
| `raptorWalk` | |

</details>


---

### Enum: `AbilityAfterEnemyCastSpell_Stackable`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ThornUpX` | |
| `ThornUp` | |

</details>


---

### Enum: `Bird`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CookedChickenLeg` | |

</details>


---

### Enum: `BounceRock`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SmallLavaRock` | |
| `LavaBoulder` | |
| `SmallRock` | |

</details>


---

### Enum: `BreakIntoRocks`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SmallRock` | |
| `Coin` | |

</details>


---

### Enum: `ChangeTileOnPop`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CreepTile` | |
| `GlitchTile` | |
| `OilTile` | |

</details>


---

### Enum: `DisableAbilities`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `all_items` | |
| `all_spells` | |
| `basic_attack` | |

</details>


---

### Enum: `DisplayDangerAOE`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `GrenadeExplode` | |
| `MoonHead_Blow` | |
| `TheChild_Wrath` | |
| `attack` | |

</details>


---

### Enum: `DownRankAIIfWeaponUsable`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.001` | |

</details>


---

### Enum: `EnableWeather`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `KaijuFirestorm` | |
| `KaijuMeteornado` | |
| `KaijuMeteornadoSolo` | |
| `VisualFlySwarm` | |

</details>


---

### Enum: `FragileDuringElement`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `water` | |

</details>


---

### Enum: `GroundFlopper`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DefaultMove` | |
| `MoveOne` | |

</details>


---

### Enum: `KillsToMeat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Food` | |

</details>


---

### Enum: `LoopingSoundWhileAlive`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Bomb_FuseLoop` | |
| `BigUFO_ambient_looping` | |
| `Twister_loop` | |

</details>


---

### Enum: `PopAndSpawn`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Sprout` | |
| `StemCat_HalfHealth` | |
| `TheDestroyer` | |
| `Tormentor` | |

</details>


---

### Enum: `RemoveItem`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill), [`ScaldingOrbMoonBossOneShot`](./Items_and_Equipment.md#context-scaldingorbmoonbossoneshot)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BlackShard_Glowing` | |
| `BlackShard` | |
| `ScaldingOrb` | |

</details>


---

### Enum: `TeamCastAbility`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Huddle_Impl` | |
| `Spin` | |
| `TeamFlex_Impl` | |
| `TeamFlex_Impl2` | |

</details>


---

### Enum: `TileTrail_Ahead`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#context-temporary_effects), [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FireTile` | |
| `FlowerTile` | |
| `OilTile` | |
| `WaterTile` | |

</details>


---

### Enum: `WeremanTransformationReceiver`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CaveManTransform` | |
| `CaveWomanDropTransform` | |

</details>


---

### Enum: `adventure_weather`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Rain`](./House_and_Environment.md#context-rain), [`Snow`](./House_and_Environment.md#context-snow), [`Thunderstorm`](./House_and_Environment.md#context-thunderstorm), [`Windy`](./House_and_Environment.md#context-windy)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Rain` | |
| `Snow` | |
| `Thunderstorm` | |
| `Windy` | |

</details>


---

### Enum: `aoe_chance`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |
| `.33` | |
| `.4+.2*level` | |

</details>


---

### Enum: `damage_tiles`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](./Abilities_and_Spells.md#context-dodamage), [`DoDamage`](./Items_and_Equipment.md#context-dodamage)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `all` | |

</details>


---

### Enum: `fail_item_quest`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `JarOfChaos` | |
| `JarOfRadiatedBlood` | |
| `JarOfRadiation` | |
| `Nuke` | |

</details>


---

### Enum: `goto`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `end` | |

</details>


---

### Enum: `hit`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `skeletonCorpseHit` | |
| `hitDisassembled` | |

</details>


---

### Enum: `initiative`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TransformInXTurns`](./Characters_and_Bosses.md#context-transforminxturns)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `keep_turns_end_turn` | |

</details>


---

### Enum: `learn_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BarfBall` | |
| `FutureSight` | |

</details>


---

### Enum: `max_targets`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `-X` | |

</details>


---

### Enum: `min_aoe`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `1+size` | |
| `2+X` | |
| `2+size` | |

</details>


---

### Enum: `post_combat_cutscene`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `obelisk1_core` | |
| `obelisk1_moon` | |
| `obelisk2_core` | |
| `obelisk2_moon` | |

</details>


---

### Enum: `skybox_frame`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Rain`](./House_and_Environment.md#context-rain), [`Snow`](./House_and_Environment.md#context-snow), [`Thunderstorm`](./House_and_Environment.md#context-thunderstorm), [`Windy`](./House_and_Environment.md#context-windy)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `day_rain` | |
| `day_snow` | |
| `day_thunderstorm` | |
| `day_windy` | |

</details>


---

### Enum: `stacks`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyMultipleTimes`](./Abilities_and_Spells.md#context-applymultipletimes), [`KnockUpAndAway`](./Abilities_and_Spells.md#context-knockupandaway), [`ScatterCoins`](./Abilities_and_Spells.md#context-scattercoins)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `5+bonus_melee_ability_damage` | |
| `X` | |
| `item_aux` | |

</details>


---

### Enum: `status_explosion_override`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`EMP`](./Passives_and_Statuses.md#context-emp)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `WaterConduct` | |

</details>


---

### Enum: `stunned`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dead` | |
| `idleDisassembled` | |

</details>


---

### Enum: `tag_filter`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusCharactersOnRoundEnd`](./House_and_Environment.md#context-statuscharactersonroundend), [`AddPassivesToMinions`](./Items_and_Equipment.md#context-addpassivestominions), [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `crow` | |
| `grub_familiar` | |
| `rock` | |

</details>


---

### Enum: `tags`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `consumable` | |

</details>


---

### Enum: `time`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoScreenShake`](./Abilities_and_Spells.md#context-doscreenshake)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |
| `.75` | |

</details>


---

### Enum: `trap`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnExtraThingsOnBattleStart`](./House_and_Environment.md#context-spawnextrathingsonbattlestart), [`ROOT`](./Spawns_and_Enemy_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BearTrap` | |
| `LandMine` | |
| `WaterKittenTrap` | |
| `WebTrap` | |

</details>


---

### Enum: `trigger_npc_sequence_tomorrow`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `butch_boneyard_intro` | |
| `frank_caves_intro` | |
| `jack_desert_intro` | |
| `organ_boneyard_intro` | |

</details>


---

### Enum: `uifloaters_offset`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `unlock_npc_tomorrow`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `beanies` | |
| `jack` | |
| `steven` | |
| `tracy` | |

</details>


---

### Enum: `upgrade_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `random` | |

</details>


---

### Enum: `visit_chapter`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dimensionx` | |
| `future` | |
| `iceage` | |
| `theend` | |

</details>


---

### Enum: `weak`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dead` | |
| `idleDisassembled` | |

</details>


---

### Enum: `AbilityEnableIfConsumedCharacterHasTag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `sp_pill_fire` | |
| `sp_pill_normal` | |
| `sp_pill_tar` | |

</details>


---

### Enum: `Antidote`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`alt_spawn_pool`](./Characters_and_Bosses.md#context-alt_spawn_pool)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `BaseStatMultiply`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.25` | |
| `.5` | |
| `.666` | |

</details>


---

### Enum: `Blessing`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`alt_spawn_pool`](./Characters_and_Bosses.md#context-alt_spawn_pool)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `BonusDamage`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#context-conditional_healththreshold), [`Conditional_Shielded`](./Abilities_and_Spells.md#context-conditional_shielded), [`Else`](./Abilities_and_Spells.md#context-else)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `20+bonus_melee_damage` | |
| `str` | |

</details>


---

### Enum: `BreakOnElement`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `water` | |

</details>


---

### Enum: `CobraReflex`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicMonkMelee` | |

</details>


---

### Enum: `CollideWithConsumed`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `1+bonus_melee_damage` | |
| `4+bonus_melee_damage` | |
| `5+bonus_melee_damage` | |

</details>


---

### Enum: `DigestDeadBodies`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Digest` | |
| `LennyCatDies` | |
| `MoonHead_Digest` | |

</details>


---

### Enum: `DoubleStatus`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Bleed` | |
| `Burn` | |
| `Poison` | |

</details>


---

### Enum: `DropAsFamiliarOnArmorBreak`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FaceGrubFamiliar` | |
| `HeadGrubFamiliar` | |
| `NeckGrubFamiliar` | |

</details>


---

### Enum: `FactionUprising`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `alien` | |
| `ghost` | |
| `robot` | |

</details>


---

### Enum: `FindExtraItemFromPoolOnBattleEnd`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects), [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pills` | |
| `combat_reward_easy` | |

</details>


---

### Enum: `FindItem`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend), [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BoneClub` | |
| `Molars` | |
| `Pearl` | |

</details>


---

### Enum: `GlobalSpawnCharacter`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects), [`FinalBossBecomeTheChild`](./Characters_and_Bosses.md#context-finalbossbecomethechild)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MegaGuppy` | |

</details>


---

### Enum: `KnockbackDirectionIsFacingDirection`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `flip` | |
| `rotate_right` | |

</details>


---

### Enum: `MoveAndUseAbilityEachTurnBeginIfPossible`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Cannibalize` | |
| `EatShit` | |
| `face_EatNeverstone` | |

</details>


---

### Enum: `MoveWhenDamaged`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `move` | |
| `TKNG_Hop` | |

</details>


---

### Enum: `MutateViaAbility`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BBTransformMutant` | |

</details>


---

### Enum: `PoopWhenHit`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Poop` | |

</details>


---

### Enum: `ReplaceBasicMove_Mutation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicJump` | |
| `BasicDig` | |

</details>


---

### Enum: `SetDefaultFace`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects), [`PassiveGroup`](./Passives_and_Statuses.md#context-passivegroup)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `happy` | |
| `insane` | |
| `sad` | |

</details>


---

### Enum: `SetDefaultFacePassive`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `euphoric` | |
| `insane` | |

</details>


---

### Enum: `Slow`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_FormulaIsPositive`](./Abilities_and_Spells.md#context-conditional_formulaispositive), [`Ice`](./Passives_and_Statuses.md#context-ice)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |

</details>


---

### Enum: `SpawnCustomTrap`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CharmTrap` | |
| `EggSackTrap` | |
| `SpikeTrap` | |

</details>


---

### Enum: `TempStrengthUp`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |

</details>


---

### Enum: `TowerDefenseReflex`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |
| `BasicRanged_1DMG` | |

</details>


---

### Enum: `UseAbility_NonStack`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnKill`](./Characters_and_Bosses.md#context-statusonkill)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BBTransformZealot` | |
| `GenericRage` | |

</details>


---

### Enum: `accuracy`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `aoe_pierce_mode`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](./Characters_and_Bosses.md#context-properties)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `block` | |

</details>


---

### Enum: `bg_placements_frame`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`House1`](./House_and_Environment.md#context-house1), [`House2`](./House_and_Environment.md#context-house2), [`House3`](./House_and_Environment.md#context-house3)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `large` | |
| `small` | |

</details>


---

### Enum: `craft_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TinkererBasicAttackSwitching`](./Cat_Classes.md#context-tinkererbasicattackswitching), [`TinkererBasicAttackSwitching`](./Characters_and_Bosses.md#context-tinkererbasicattackswitching)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TinkererCraft` | |

</details>


---

### Enum: `dash_decelerating_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dashslow` | |

</details>


---

### Enum: `deadhit`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `skeletonCorpseHit` | |

</details>


---

### Enum: `disallow_items`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](./Characters_and_Bosses.md#context-properties)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Nuke` | |
| `all` | |

</details>


---

### Enum: `fail_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChanceToBreakFree`](./Abilities_and_Spells.md#context-chancetobreakfree)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CHuskDropFail` | |
| `LennyStruggleFail` | |
| `XXX` | |

</details>


---

### Enum: `form_above`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeHealthThreshold`](./Characters_and_Bosses.md#context-formchangehealththreshold)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Default` | |
| `Full` | |
| `Standing` | |

</details>


---

### Enum: `form_below`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeHealthThreshold`](./Characters_and_Bosses.md#context-formchangehealththreshold)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Damaged` | |
| `DesireMech` | |
| `Standing2` | |

</details>


---

### Enum: `from`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TransformEquipment`](./Abilities_and_Spells.md#context-transformequipment), [`TransformWeapon`](./Abilities_and_Spells.md#context-transformweapon), [`TransformWeapon`](./Items_and_Equipment.md#context-transformweapon)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `JarOfChaos` | |
| `Necro_SoulDagger_Charged` | |
| `Necro_SoulDagger_Uncharged` | |

</details>


---

### Enum: `gift_item`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`organ_max_intro`](./Progression_Unlocks.md#context-organ_max_intro), [`organ_max_repeating`](./Progression_Unlocks.md#context-organ_max_repeating), [`tink_prettybow`](./Progression_Unlocks.md#context-tink_prettybow)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `disorder_needle` | |
| `TinksBow` | |

</details>


---

### Enum: `grab_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `grab` | |

</details>


---

### Enum: `heal_disorder`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Anxiety` | |
| `diseases` | |
| `mental_disorders` | |

</details>


---

### Enum: `icon_damage_type`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](./Abilities_and_Spells.md#context-meta)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `magic` | |
| `physical` | |

</details>


---

### Enum: `icon_hint`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `passive_syringe` | |
| `ability_syringe` | |

</details>


---

### Enum: `image_tint`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`editor`](./Spawns_and_Enemy_Pools.md#context-editor)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `red` | |
| `blue` | |

</details>


---

### Enum: `jestercat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `learn_ability_from_pool`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Necromancer` | |
| `AnyUnlocked` | |

</details>


---

### Enum: `lob_yoff`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `-.5` | |

</details>


---

### Enum: `lose_item_from_inventory`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cat` | |

</details>


---

### Enum: `make_old`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `self` | |

</details>


---

### Enum: `movieclip_bg`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`House1`](./House_and_Environment.md#context-house1), [`House2`](./House_and_Environment.md#context-house2), [`House3`](./House_and_Environment.md#context-house3)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `HouseBackground1` | |
| `HouseBackground2` | |
| `HouseBackground3` | |

</details>


---

### Enum: `movieclip_fg`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`House1`](./House_and_Environment.md#context-house1), [`House2`](./House_and_Environment.md#context-house2), [`House3`](./House_and_Environment.md#context-house3)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `HouseForeground1` | |
| `HouseForeground2` | |
| `HouseForeground3` | |

</details>


---

### Enum: `multihit`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |
| `X*2+1` | |
| `X+1` | |

</details>


---

### Enum: `oncast`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sounds`](./Abilities_and_Spells.md#context-sounds)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AbilitySnd_BoulderDrop` | |
| `AbilitySnd_Assassinate` | |

</details>


---

### Enum: `oncastpoint`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sounds`](./Abilities_and_Spells.md#context-sounds)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AirHorn` | |
| `Batterup_Swing_Castpoint` | |

</details>


---

### Enum: `override_music`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`boss`](./Map_Generation_and_Routing.md#context-boss), [`mw_boss`](./Map_Generation_and_Routing.md#context-mw_boss)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `chaos_boss` | |
| `finalboss` | |
| `throbbingking` | |

</details>


---

### Enum: `requires_unlocked_npc`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `frank` | |
| `jack` | |
| `tracy` | |

</details>


---

### Enum: `return_as`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`leave_party_temporarily`](./Events_and_Encounters.md#context-leave_party_temporarily)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `enemy` | |

</details>


---

### Enum: `return_during`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`leave_party_temporarily`](./Events_and_Encounters.md#context-leave_party_temporarily)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `boss` | |

</details>


---

### Enum: `set_house`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Default`](./House_and_Environment.md#context-default), [`LargeHouse`](./House_and_Environment.md#context-largehouse), [`MediumHouse`](./House_and_Environment.md#context-mediumhouse)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `House1` | |
| `House2` | |
| `House3` | |

</details>


---

### Enum: `side`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn_unit_next_fight`](./Events_and_Encounters.md#context-spawn_unit_next_fight)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `enemies` | |

</details>


---

### Enum: `special_tile_tag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ChaosValidPosition` | |
| `FinalBossCloneSpot` | |
| `FinalBossTheChildLocation` | |

</details>


---

### Enum: `throw_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TinkererBasicAttackSwitching`](./Cat_Classes.md#context-tinkererbasicattackswitching), [`TinkererBasicAttackSwitching`](./Characters_and_Bosses.md#context-tinkererbasicattackswitching)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TinkererThrow` | |

</details>


---

### Enum: `tint`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `blue` | |
| `green` | |
| `yellow` | |

</details>


---

### Enum: `to`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TransformEquipment`](./Abilities_and_Spells.md#context-transformequipment), [`TransformWeapon`](./Abilities_and_Spells.md#context-transformweapon), [`TransformWeapon`](./Items_and_Equipment.md#context-transformweapon)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `JarOfNothing` | |
| `Necro_SoulDagger_Charged` | |
| `Necro_SoulDagger_Uncharged` | |

</details>


---

### Enum: `unlock_item_quest`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CryogenicTimeChamber_Full` | |
| `JarOfChaos` | |
| `JarOfRadiatedBlood` | |

</details>


---

### Enum: `upgrade_passive`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `random` | |

</details>


---

### Enum: `walk,`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Injuries.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `brokenLegWalk` | |
| `brokenPawWalk` | |
| `dislocatedShoulderWalk` | |

</details>


---

### Enum: `warrior_tag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BungaCheers`](./Characters_and_Bosses.md#context-bungacheers), [`BungaEntrance`](./Characters_and_Bosses.md#context-bungaentrance)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bungawarrior` | |
| `finalboss_clonecat` | |

</details>


---

### Enum: `weak,`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Injuries.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `brokenLegIdle` | |
| `brokenPawIdle` | |
| `dislocatedShoulderIdle` | |

</details>


---

### Enum: `zoomout_catvolume`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`House1`](./House_and_Environment.md#context-house1), [`House2`](./House_and_Environment.md#context-house2), [`House3`](./House_and_Environment.md#context-house3)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.6` | |
| `.7` | |
| `.8` | |

</details>


---

### Enum: `AOEPuddle`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Water`](./Passives_and_Statuses.md#context-water)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X-1` | |

</details>


---

### Enum: `AbilityEnabledIfHasStatus`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DemonicGlyph_Bite` | |
| `DemonicGlyph_Summon` | |

</details>


---

### Enum: `AddElementsToWeapon`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhileWearingMetal`](./Passives_and_Statuses.md#context-passivewhilewearingmetal)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Electric` | |

</details>


---

### Enum: `AfterImage`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `PlayerCat_ThiefShade` | |
| `PlayerCat_ThiefShade2` | |

</details>


---

### Enum: `AllyBonusAbilityAura`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `NubbyToss` | |

</details>


---

### Enum: `AllyDamageReaction`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |

</details>


---

### Enum: `AllyMoveAbilityAura`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CatapultJump` | |
| `CatapultJump2` | |

</details>


---

### Enum: `AutocastEachTurn`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DarkOneStrike` | |
| `ViolentOutburst` | |

</details>


---

### Enum: `AutocastEachTurnBegin`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MindCrack_EldritchVisage` | |
| `MindCrack_EldritchVisage2` | |

</details>


---

### Enum: `ChangeFaction`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `sabertooths` | |

</details>


---

### Enum: `ChangeTileOnDeath`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `WaterTile` | |

</details>


---

### Enum: `ChargeSpiritBombAura`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DonateEnergy` | |
| `DonateEnergy2` | |

</details>


---

### Enum: `Chicken`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.01` | |
| `.1` | |

</details>


---

### Enum: `DexterityUp`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |
| `item_aux` | |

</details>


---

### Enum: `EliteTint`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `red` | |

</details>


---

### Enum: `EnterMount`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects), [`post_spawn_statuses`](./Abilities_and_Spells.md#context-post_spawn_statuses)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `enter` | |

</details>


---

### Enum: `EquipRandomTemporaryItemFromPool`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pills` | |
| `weapons` | |

</details>


---

### Enum: `FamiliarBonusAbility`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FamiliarSelfDestruct` | |
| `FamiliarSelfDestruct2` | |

</details>


---

### Enum: `FinalBossShield`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DestroyerShieldBash` | |
| `None` | |

</details>


---

### Enum: `FlatLeech`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Holy`](./Passives_and_Statuses.md#context-holy)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |

</details>


---

### Enum: `FollowUp`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FollowUpDash` | |
| `FollowUpDash2` | |

</details>


---

### Enum: `ForceMoveTowardsEnemies`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DumbMove_Impl` | |
| `MoveOne` | |

</details>


---

### Enum: `GainDisorder`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](./Abilities_and_Spells.md#context-conditional_goodroll), [`StatusOnBreak`](./Items_and_Equipment.md#context-statusonbreak)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Chungus` | |
| `Psychosis` | |

</details>


---

### Enum: `GainDisorderFromPool`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToRandomPartyMemberIfPossible`](./Items_and_Equipment.md#context-applytorandompartymemberifpossible)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `all_disorders` | |

</details>


---

### Enum: `HealthGain`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TaggedPickupEffectReplacement`](./Passives_and_Statuses.md#context-taggedpickupeffectreplacement)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `2*X` | |
| `3*X` | |

</details>


---

### Enum: `HideEquipment`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassivesToSpawnerWhileAlive`](./Abilities_and_Spells.md#context-applypassivestospawnerwhilealive), [`additional_passives`](./Abilities_and_Spells.md#context-additional_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `neck` | |

</details>


---

### Enum: `HolyShieldTransferToTaggedMinions`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `any` | |
| `crow` | |

</details>


---

### Enum: `ImmediateUseDirectionalAbility`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BowlDash` | |
| `BowlDash2` | |

</details>


---

### Enum: `IntelligenceUp`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `-int` | |
| `item_aux` | |

</details>


---

### Enum: `KaijuWinCon`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pyrophina` | |
| `zaratana` | |

</details>


---

### Enum: `Leave`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CherubimReaction`](./Characters_and_Bosses.md#context-cherubimreaction)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CherubimLeave` | |
| `LELeave` | |

</details>


---

### Enum: `LeaveBehindOnceEachMove`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Poop` | |
| `Scrap` | |

</details>


---

### Enum: `MiniVolcanoReaction`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MiniVolcano_Spurt` | |
| `ThrobShot_Reaction` | |

</details>


---

### Enum: `MoveAwayFromDamageSource`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicJump` | |
| `MoveOne` | |

</details>


---

### Enum: `MoveSpeedMultiplier`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives), [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `MoveTowardsKillers`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ReaperRevenge` | |

</details>


---

### Enum: `Poison`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Grass`](./Passives_and_Statuses.md#context-grass)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |

</details>


---

### Enum: `ProtectTargetedAllies`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SwapPositions_WideLoad` | |
| `SwapPositions_WideLoad2` | |

</details>


---

### Enum: `RandomTaggedMutation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Abilities_and_Spells.md#context-statusonbattleend)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bird` | |
| `melted` | |

</details>


---

### Enum: `ReplaceBasicAttackWhenDead`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Haunt` | |

</details>


---

### Enum: `Return`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CherubimReaction`](./Characters_and_Bosses.md#context-cherubimreaction)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CherubimReturn` | |
| `LEReturn` | |

</details>


---

### Enum: `SE_Cat_StompLegMove`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](./Characters_and_Bosses.md#context-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_Terminator1_WalkLeg` | |
| `SE_Terminator2_WalkLeg` | |

</details>


---

### Enum: `ShovingMatch`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |

</details>


---

### Enum: `SpeedUp`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `item_aux` | |

</details>


---

### Enum: `StrengthUp`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |
| `item_aux` | |

</details>


---

### Enum: `TempDexterityUp`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |

</details>


---

### Enum: `TransformWhenBuddyDies`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `UltraOrnstein` | |
| `UltraSmough` | |

</details>


---

### Enum: `TriggerWerewolfTransform`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `UpgradeLevelUpClassActives`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Colorless` | |

</details>


---

### Enum: `UpgradeLevelUpClassPassives`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Colorless` | |

</details>


---

### Enum: `UpgradeTaggedSpawnsToChampions`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bug` | |
| `worm` | |

</details>


---

### Enum: `Weakness`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Gravity`](./Passives_and_Statuses.md#context-gravity)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |

</details>


---

### Enum: `XIsLivingCharactersWithTag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `husk` | |
| `rock` | |

</details>


---

### Enum: `cha`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`permanent_stats`](./Events_and_Encounters.md#context-permanent_stats), [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `+1` | |
| `aux` | |

</details>


---

### Enum: `check_in_form`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MoveTowardsDamageSource`](./Characters_and_Bosses.md#context-movetowardsdamagesource)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Boris` | |
| `Default` | |

</details>


---

### Enum: `clear_surviving_kaiju`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pyrophina` | |
| `zaratana` | |

</details>


---

### Enum: `cloned_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |

</details>


---

### Enum: `coins_bonus`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Combat_Rewards.md#context-1), [`2`](./Combat_Rewards.md#context-2)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |
| `.75` | |

</details>


---

### Enum: `complete_adventure`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `anywhere` | |

</details>


---

### Enum: `default_attack_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack2` | |
| `bite1` | |

</details>


---

### Enum: `delay`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.1` | |
| `.25` | |

</details>


---

### Enum: `enabled_formula`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`cost`](./Abilities_and_Spells.md#context-cost)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `1-X` | |
| `X` | |

</details>


---

### Enum: `enemy_type`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`KillEnemyOfTypeAtBattleStart`](./Events_and_Encounters.md#context-killenemyoftypeatbattlestart)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `any` | |
| `cat` | |

</details>


---

### Enum: `exit_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DybbukPossessed`](./Abilities_and_Spells.md#context-dybbukpossessed), [`DybbukPossessionFallback`](./Characters_and_Bosses.md#context-dybbukpossessionfallback)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DybbukReturn` | |

</details>


---

### Enum: `follow_character_tag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Big`](./House_and_Environment.md#context-big)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `zaratana` | |

</details>


---

### Enum: `gain_immortal_familiar`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CharmedFlea` | |
| `CharmedFleaSpecial` | |

</details>


---

### Enum: `generate_beanies_quest`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`beanies_quests_intro`](./Progression_Unlocks.md#context-beanies_quests_intro), [`beanies_quests_repeat`](./Progression_Unlocks.md#context-beanies_quests_repeat)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `intro` | |
| `main_pool` | |

</details>


---

### Enum: `get_and_equip_item`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Catnip` | |
| `FlyLarva` | |

</details>


---

### Enum: `gift_item_from_pool`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`frank_max_intro`](./Progression_Unlocks.md#context-frank_max_intro), [`frank_max_repeating`](./Progression_Unlocks.md#context-frank_max_repeating)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `parasites` | |

</details>


---

### Enum: `icon`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`2`](./Passives_and_Statuses.md#context-2), [`3`](./Passives_and_Statuses.md#context-3)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DejaVu2` | |
| `DejaVu3` | |

</details>


---

### Enum: `id`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./House_and_Environment.md#context-root), [`SmallAttic`](./House_and_Environment.md#context-smallattic)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Attic` | |

</details>


---

### Enum: `is_move`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](./Abilities_and_Spells.md#context-meta)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `learn_passive_from_pool`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AnyUnlocked` | |
| `Necromancer` | |

</details>


---

### Enum: `mask_center`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SpearMaskCenter` | |

</details>


---

### Enum: `mask_extent`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SpearMaskExtent` | |

</details>


---

### Enum: `musiclayer`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root), [`mw_hard1`](./Map_Generation_and_Routing.md#context-mw_hard1)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `boss` | |

</details>


---

### Enum: `next_event_from_set`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Tragedy` | |
| `WatchingHead2` | |

</details>


---

### Enum: `not_cat_has_item_equipped`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`requirements`](./Events_and_Encounters.md#context-requirements)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CryogenicTimeChamber_Full` | |
| `GuillotinasHead` | |

</details>


---

### Enum: `override_move`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`310`](./Cat_Mutations.md#context-310), [`331`](./Cat_Mutations.md#context-331)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicJump` | |

</details>


---

### Enum: `particle_mat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `shadow_occluded_spelldissolve` | |

</details>


---

### Enum: `preturn_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `alertstart` | |

</details>


---

### Enum: `pseudoprojectile`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `RocketFromAbove` | |

</details>


---

### Enum: `quest_item_alias`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BlackShard` | |
| `NuclearKnife` | |

</details>


---

### Enum: `range_bonuses`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `include_alpha` | |

</details>


---

### Enum: `require_beat_house_boss`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pyrophina` | |
| `zaratana` | |

</details>


---

### Enum: `require_mapgen_flag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CoreObeliskUnlocked` | |
| `MoonObeliskUnlocked` | |

</details>


---

### Enum: `scramble_abilities`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `all` | |

</details>


---

### Enum: `spin`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `again` | |

</details>


---

### Enum: `surviving_kaiju`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pyrophina` | |
| `zaratana` | |

</details>


---

### Enum: `target_filter`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ProtectTargetedAllies`](./Characters_and_Bosses.md#context-protecttargetedallies)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Kitten` | |
| `any` | |

</details>


---

### Enum: `tinkerer_0`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AlternateCraftingPools`](./Passives_and_Statuses.md#context-alternatecraftingpools)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `tinkerer_0_bombs` | |

</details>


---

### Enum: `tinkerer_1`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AlternateCraftingPools`](./Passives_and_Statuses.md#context-alternatecraftingpools)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `tinkerer_1_bombs` | |

</details>


---

### Enum: `tooltip_stacks_singular`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Status_Effect_Keywords.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `KEYWORD_PETRIFY_DESC_SINGULAR` | |
| `KEYWORD_POSSESSED_DESC_SIGNULAR` | |

</details>


---

### Enum: `trinket`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`innate_items`](./Cat_Classes.md#context-innate_items), [`MonkCatReactionAbilities`](./Characters_and_Bosses.md#context-monkcatreactionabilities)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MCHadouken` | |
| `MonkStyleChanger` | |

</details>


---

### Enum: `unlock_levelgroup`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bigsharklevels` | |

</details>


---

### Enum: `very_rare`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.01` | |

</details>


---

### Enum: `welcome_message`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](./Shops.md#context-meta)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `welcome_water` | |
| `welcome_water_cheap` | |

</details>


---

### Enum: `#`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Spawns_and_Enemy_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ID` | |

</details>


---

### Enum: `10,`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScalingAttackAnimation`](./Characters_and_Bosses.md#context-scalingattackanimation)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bite3` | |

</details>


---

### Enum: `1x1_object`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`WaggleClone`](./Abilities_and_Spells.md#context-waggleclone)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cWaggle` | |

</details>


---

### Enum: `2x2_object`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`WaggleClone`](./Abilities_and_Spells.md#context-waggleclone)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cWaggle2x2` | |

</details>


---

### Enum: `3x3_object`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`WaggleClone`](./Abilities_and_Spells.md#context-waggleclone)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cWaggle3x3` | |

</details>


---

### Enum: `AbilityEnabledIfNotHasStatus`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BackflipWhenTargeted` | |

</details>


---

### Enum: `AbilityEnabledIfSpecificItemEquipped`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Neverstone` | |

</details>


---

### Enum: `AbilityOnBattleStart_UseAI`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TheCreator_SpawnCloneTeam` | |

</details>


---

### Enum: `AddElementsToSpells`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Earth` | |

</details>


---

### Enum: `AddWeaponAux`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `-item_aux` | |

</details>


---

### Enum: `AllStatsUp`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `item_aux` | |

</details>


---

### Enum: `AlternateIdleAnimation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `berserkIdle` | |

</details>


---

### Enum: `AutocastEachRound`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SpiderReturn` | |

</details>


---

### Enum: `BackflipWhenTargeted`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusIfUnusedActPoints`](./Items_and_Equipment.md#context-statusifunusedactpoints)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |

</details>


---

### Enum: `BackstabCritChance`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.25` | |

</details>


---

### Enum: `BagOfSeeds`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.3` | |

</details>


---

### Enum: `BasicAttackCritChance`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.1` | |

</details>


---

### Enum: `BirdFeed`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.3` | |

</details>


---

### Enum: `BirdPoopHat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.3` | |

</details>


---

### Enum: `BloatEyePassive2`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BloatEyeMovement2` | |

</details>


---

### Enum: `BonusAbility_DelayedApplication`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Slap` | |

</details>


---

### Enum: `Boris`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`other_form_change_abilities`](./Characters_and_Bosses.md#context-other_form_change_abilities)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MegaGuppy_TransformBoris` | |

</details>


---

### Enum: `Brace`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleStart`](./Items_and_Equipment.md#context-statusonbattlestart)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `item_aux` | |

</details>


---

### Enum: `CanMutateTo`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Hyde` | |

</details>


---

### Enum: `CastAgain`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#context-temporary_effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `9+X` | |

</details>


---

### Enum: `ChangeTileUnderCharacterAtStart`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`self_status_next_fight`](./Events_and_Encounters.md#context-self_status_next_fight)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `GlassTile` | |

</details>


---

### Enum: `CharismaUp`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `item_aux` | |

</details>


---

### Enum: `Charmed`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `level` | |

</details>


---

### Enum: `Coin10`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`alt_spawn_pool`](./Characters_and_Bosses.md#context-alt_spawn_pool)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.1` | |

</details>


---

### Enum: `CoinTossBounce`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |

</details>


---

### Enum: `ConfusionEffectOnTaggedAbilities`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `consumable` | |

</details>


---

### Enum: `ConjureSingleUseBonusAbility`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `random` | |

</details>


---

### Enum: `ConstitutionUp`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `item_aux` | |

</details>


---

### Enum: `CounterAttackAfterEnemyCastSpell`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Telekinesis` | |

</details>


---

### Enum: `DeadHummingbird`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.3` | |

</details>


---

### Enum: `DeathwormUnderground`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DeathWormEat` | |

</details>


---

### Enum: `Default`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`exit_animations`](./Characters_and_Bosses.md#context-exit_animations)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `release` | |

</details>


---

### Enum: `DelayCastAbility`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_LastHit`](./Abilities_and_Spells.md#context-conditional_lasthit)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `HitlerNuke` | |

</details>


---

### Enum: `DiesToElement`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Wind` | |

</details>


---

### Enum: `DinoLegAnimation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `poop` | |

</details>


---

### Enum: `DisguisedTrapper`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FearMelee` | |

</details>


---

### Enum: `DoubleCastTaggedSpells`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `musical` | |

</details>


---

### Enum: `DropAsFamiliarOnTookDamage`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `PhantomMaskRock` | |

</details>


---

### Enum: `DropSoulJarOnDeath`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SoulJar_Full` | |

</details>


---

### Enum: `ElementWeakness`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Fire` | |

</details>


---

### Enum: `ExcludeFromEvents`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Tragedy` | |

</details>


---

### Enum: `Explosive`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`other_form_change_abilities`](./Characters_and_Bosses.md#context-other_form_change_abilities)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MegaGuppy_TransformExplosive` | |

</details>


---

### Enum: `ExtraTurnsPerTaggedUnit`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `sprout` | |

</details>


---

### Enum: `FlushmasterCelebration`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `celebrate` | |

</details>


---

### Enum: `FormChangeWhenBuddyDies`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Rage` | |

</details>


---

### Enum: `GlowingSeed`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.3` | |

</details>


---

### Enum: `GoldenEgg`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.3` | |

</details>


---

### Enum: `HarpoonTrapPassive`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `HarpoonTrapPull` | |

</details>


---

### Enum: `HarpysClaw`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `Holy`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`other_form_change_abilities`](./Characters_and_Bosses.md#context-other_form_change_abilities)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MegaGuppy_TransformHoly` | |

</details>


---

### Enum: `ImmediateUseAbility_Instant`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasStatus`](./Items_and_Equipment.md#context-conditional_hasstatus)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `head_CrownOfHorns` | |

</details>


---

### Enum: `JohnnyWasher`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BBTransformZealot` | |

</details>


---

### Enum: `JumpAttackLeaveBehind`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#context-temporary_effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BungaThrone` | |

</details>


---

### Enum: `KnockOutClone`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_PlayerCat`](./Abilities_and_Spells.md#context-conditional_playercat)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `PlayerCat_MiniMiniMe` | |

</details>


---

### Enum: `LaunchOffScreen`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Displaceable`](./Abilities_and_Spells.md#context-conditional_displaceable)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `10+bonus_melee_ability_damage` | |

</details>


---

### Enum: `LeaveBehind`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#context-temporary_effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Bait` | |

</details>


---

### Enum: `LegacySpawnSavedCatIfExists`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Legacy_Marshmallow_StolenCatID` | |

</details>


---

### Enum: `LimitedTileTrail`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FlowerTile` | |

</details>


---

### Enum: `LineOfSightTrueSightAura`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `LostSoul`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `LuckUp`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `item_aux` | |

</details>


---

### Enum: `Madness`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `level` | |

</details>


---

### Enum: `MagicSeed`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.3` | |

</details>


---

### Enum: `ManglerMonsterPassive`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ManglerMonsterDashAttack` | |

</details>


---

### Enum: `MoonHeadCrackedVisual`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Cracked` | |

</details>


---

### Enum: `ObjectOnHitFullyEmpty`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `RandomArmorPickup` | |

</details>


---

### Enum: `OverrideChainKnockbackDamage`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `3+bonus_melee_ability_damage` | |

</details>


---

### Enum: `Paranoia`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ParanoiaBasicMelee` | |

</details>


---

### Enum: `Parousworm`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `PeaceSymbol`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.3` | |

</details>


---

### Enum: `PeaceSymbolFacePaint`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.3` | |

</details>


---

### Enum: `PersistentElement`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./House_and_Environment.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Holy` | |

</details>


---

### Enum: `PreventSpecificInjury`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `int` | |

</details>


---

### Enum: `QueueUseAbility`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Spider_GoInsane` | |

</details>


---

### Enum: `RaptorEgg`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.1` | |

</details>


---

### Enum: `RavenFeather`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.3` | |

</details>


---

### Enum: `ReloadOnElementalDamageReceived`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Holy` | |

</details>


---

### Enum: `ReloadOnKillTagged`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `rock` | |

</details>


---

### Enum: `RemoveAmbientLightEffects`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `ReplaceBasicAttack_Mutation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Cat_Mutations.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FetusSpit` | |

</details>


---

### Enum: `ReplaceBlankTilesOnBattleStart`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `GlassTile` | |

</details>


---

### Enum: `ReplaceSpellsWhenDead`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Spook` | |

</details>


---

### Enum: `RockyArmorSalvage`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.75` | |

</details>


---

### Enum: `SE_CatSwishThrow`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](./Characters_and_Bosses.md#context-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_ThrowGrenade` | |

</details>


---

### Enum: `SE_Cat_ShadowStepIn`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](./Characters_and_Bosses.md#context-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_Terminator_ShadowStepIn` | |

</details>


---

### Enum: `SE_Cat_ShadowStepOut`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](./Characters_and_Bosses.md#context-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_Terminator_ShadowStepOut` | |

</details>


---

### Enum: `SE_Cat_WeaponLower`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](./Characters_and_Bosses.md#context-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_Terminator_WeaponLower` | |

</details>


---

### Enum: `SE_Cat_WeaponRaise`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](./Characters_and_Bosses.md#context-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_Terminator_WeaponRaise` | |

</details>


---

### Enum: `SE_Cat_bearHug`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](./Characters_and_Bosses.md#context-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_Terminator_bearHug` | |

</details>


---

### Enum: `SE_Cat_equipWeapon`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](./Characters_and_Bosses.md#context-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_TerminatorSwapWeapon` | |

</details>


---

### Enum: `SE_PetRock_Dash`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](./Characters_and_Bosses.md#context-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_PetBoulder_Dash` | |

</details>


---

### Enum: `SafeDoomed`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#context-additional_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `level` | |

</details>


---

### Enum: `Set`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Monk` | |

</details>


---

### Enum: `SetFaction`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `enemies` | |

</details>


---

### Enum: `SoundEventOnHit`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Batterup_Connect` | |

</details>


---

### Enum: `SourceSwapsBackEndOfTurn`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ThiefSwapBack` | |

</details>


---

### Enum: `SpawnMeatOnMove`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Food` | |

</details>


---

### Enum: `SpecialBossMultipartInstakill`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `moonboss` | |

</details>


---

### Enum: `StealEquipment`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `any` | |

</details>


---

### Enum: `SupportFormChangeInsteadOfRun`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Attacker` | |

</details>


---

### Enum: `TagMetronome`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `musical` | |

</details>


---

### Enum: `TallTumorManaBurn`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TT_ManaBurn` | |

</details>


---

### Enum: `TeamBonusAbility`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ShootHere` | |

</details>


---

### Enum: `TeleportBackAtTurnEnd`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FlashBack` | |

</details>


---

### Enum: `TempMovement`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `mov` | |

</details>


---

### Enum: `TempSpeedUp`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |

</details>


---

### Enum: `Terminator2Chase`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `move` | |

</details>


---

### Enum: `TickDownStatus`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ShortCircuit` | |

</details>


---

### Enum: `TieDyeBandana`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.3` | |

</details>


---

### Enum: `TileElementDamageImmunity`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Ice` | |

</details>


---

### Enum: `TilesMovedToNeighborHeal`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `level` | |

</details>


---

### Enum: `TrackAmountKilledByPlayer`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BonusBirdsKilled` | |

</details>


---

### Enum: `TrailBlazer`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `mov` | |

</details>


---

### Enum: `TransformBasicMove`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicDashAttackMove_NoKnockback` | |

</details>


---

### Enum: `TransformNow`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Hitler` | |

</details>


---

### Enum: `TransformOnDeathImmediately`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `NoHead` | |

</details>


---

### Enum: `TurnControlDelay`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.25` | |

</details>


---

### Enum: `UseAbilityWhenShieldDepleted`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `T3Pebbles_PrimeBoulderDrop` | |

</details>


---

### Enum: `UseAbility_Madness`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `weapon` | |

</details>


---

### Enum: `WeaponAuxMultiplier`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `WeirdEgg`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.3` | |

</details>


---

### Enum: `WhitelistPickupType`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `food` | |

</details>


---

### Enum: `WishBone`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.3` | |

</details>


---

### Enum: `XIsCountStatusStacks`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DodgeChance_Status` | |

</details>


---

### Enum: `XIsFormulaLockedUntilComplete`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dex` | |

</details>


---

### Enum: `abandonedones`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `adjust_target`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `stalk` | |

</details>


---

### Enum: `affected_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `statDown` | |

</details>


---

### Enum: `alert_form`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CerberubsAggroTargetBehavior`](./Characters_and_Bosses.md#context-cerberubsaggrotargetbehavior)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Alert` | |

</details>


---

### Enum: `ally_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `lickAttack` | |

</details>


---

### Enum: `ally_damage`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BungaCheers`](./Characters_and_Bosses.md#context-bungacheers)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `littleboo` | |

</details>


---

### Enum: `ally_dead`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BungaCheers`](./Characters_and_Bosses.md#context-bungacheers)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bigboo` | |

</details>


---

### Enum: `alt_art`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Tangled`](./Abilities_and_Spells.md#context-tangled)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TangledMeat` | |

</details>


---

### Enum: `alt_dead_ani`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SupportDieInsteadOfRun`](./Characters_and_Bosses.md#context-supportdieinsteadofrun)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `off` | |

</details>


---

### Enum: `alt_dying_ani`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SupportDieInsteadOfRun`](./Characters_and_Bosses.md#context-supportdieinsteadofrun)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `shutdown` | |

</details>


---

### Enum: `animate_name`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pointout` | |

</details>


---

### Enum: `animation_prefix`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](./Characters_and_Bosses.md#context-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `RattleSnake` | |

</details>


---

### Enum: `apex_time`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.35` | |

</details>


---

### Enum: `appearance`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#context-spawn)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `GolemCat` | |

</details>


---

### Enum: `aura_requires_tag`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AllStatsAura`](./Characters_and_Bosses.md#context-allstatsaura)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `humanoid` | |

</details>


---

### Enum: `auto_cast`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnThingOnDamage`](./Characters_and_Bosses.md#context-spawnthingondamage)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Dash_Enemy` | |

</details>


---

### Enum: `auto_cast_on_spawn`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#context-spawn)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Dash_Enemy` | |

</details>


---

### Enum: `break_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossShieldHealth`](./Characters_and_Bosses.md#context-finalbossshieldhealth)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DestroyerBreakShield` | |

</details>


---

### Enum: `bumblefoot`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `butchercat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `cancreeper`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `cat_has_item_slot_equipped`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`requirements`](./Events_and_Encounters.md#context-requirements)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `weapon` | |

</details>


---

### Enum: `cavecatfamily`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `cerberubs`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `chapter`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#context-spawn)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `alley` | |

</details>


---

### Enum: `check_has_status`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MoveTowardsDamageSource`](./Characters_and_Bosses.md#context-movetowardsdamagesource)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FinalBossHitCountdownBoris` | |

</details>


---

### Enum: `choose_cat_with_highest_stat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`intro`](./Events_and_Encounters.md#context-intro)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `int` | |

</details>


---

### Enum: `choose_cat_with_item_slot_equipped`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`intro`](./Events_and_Encounters.md#context-intro)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `weapon` | |

</details>


---

### Enum: `clericcat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `clipname`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`HPAltStates`](./Characters_and_Bosses.md#context-hpaltstates)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `poopmain` | |

</details>


---

### Enum: `con`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `aux` | |

</details>


---

### Enum: `core`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`prereqs`](./Progression_Unlocks.md#context-prereqs)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `mapflag_IceAgeUnlocked` | |

</details>


---

### Enum: `damage_ally`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Enemy_AI.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `damage_enemy_corpse`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Enemy_AI.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.1` | |

</details>


---

### Enum: `danger_avoidance`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Enemy_AI.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.1` | |

</details>


---

### Enum: `dash_bonk_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bonk` | |

</details>


---

### Enum: `debuff_ally`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Enemy_AI.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `default`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScalingAttackAnimation`](./Characters_and_Bosses.md#context-scalingattackanimation)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bite1` | |

</details>


---

### Enum: `default_form`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CerberubsAggroTargetBehavior`](./Characters_and_Bosses.md#context-cerberubsaggrotargetbehavior)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Normal` | |

</details>


---

### Enum: `dex`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `aux` | |

</details>


---

### Enum: `dimensionx`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`prereqs`](./Progression_Unlocks.md#context-prereqs)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `mapflag_IceAgeUnlocked` | |

</details>


---

### Enum: `dinocouple`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `distance_to_ally`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Enemy_AI.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `-.1` | |

</details>


---

### Enum: `distance_to_corpse`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Enemy_AI.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `-.1` | |

</details>


---

### Enum: `distance_to_water`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Enemy_AI.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `-.0001` | |

</details>


---

### Enum: `dodge`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `liquidmetaldodge` | |

</details>


---

### Enum: `drmangler`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `drop_body_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Consumed`](./Abilities_and_Spells.md#context-consumed)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MoonHandDrop` | |

</details>


---

### Enum: `druidcat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `eject_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Mount`](./Characters_and_Bosses.md#context-mount)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MechSuitEject` | |

</details>


---

### Enum: `empty!`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Spawns_and_Enemy_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `editor` | |

</details>


---

### Enum: `endoftime`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`prereqs`](./Progression_Unlocks.md#context-prereqs)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `endoftime` | |

</details>


---

### Enum: `enemy_damage`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BungaCheers`](./Characters_and_Bosses.md#context-bungacheers)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `littlecheer` | |

</details>


---

### Enum: `enemy_dead`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BungaCheers`](./Characters_and_Bosses.md#context-bungacheers)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bigcheer` | |

</details>


---

### Enum: `enter_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Mount`](./Characters_and_Bosses.md#context-mount)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `EnterMech` | |

</details>


---

### Enum: `equip_sound`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_CatWeaponPoke_Chainsaw` | |

</details>


---

### Enum: `exclude_characters_tagged`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Enemy_AI.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `siren` | |

</details>


---

### Enum: `exclude_prefix`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TwisterDisplaceWithDamage`](./Abilities_and_Spells.md#context-twisterdisplacewithdamage)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Twister` | |

</details>


---

### Enum: `fail_adventure`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `anywhere` | |

</details>


---

### Enum: `fightercat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `final_hit_bonus_damage`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `5+bonus_melee_ability_damage` | |

</details>


---

### Enum: `finish_quest`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `JarOfChaos` | |

</details>


---

### Enum: `fixed_jump_speed`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.8` | |

</details>


---

### Enum: `flushmaster`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `form_in`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SwimmingFormChange`](./Characters_and_Bosses.md#context-swimmingformchange)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Water` | |

</details>


---

### Enum: `form_out`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SwimmingFormChange`](./Characters_and_Bosses.md#context-swimmingformchange)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Out` | |

</details>


---

### Enum: `form_unwashed`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`JohnnyNeedsWashing`](./Characters_and_Bosses.md#context-johnnyneedswashing)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Unwashed` | |

</details>


---

### Enum: `form_washed`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`JohnnyNeedsWashing`](./Characters_and_Bosses.md#context-johnnyneedswashing)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Washed` | |

</details>


---

### Enum: `gambit`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `general_common`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `general_rare`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `general_uncommon`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `general_very_rare`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Item_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `get_full_item_set_from_pool`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `common` | |

</details>


---

### Enum: `grant_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Rest` | |

</details>


---

### Enum: `grow_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#context-mothertumorpassive)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MotherTumorGrow` | |

</details>


---

### Enum: `hang_time`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.6` | |

</details>


---

### Enum: `head_drop`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MegaDinoDropController`](./Characters_and_Bosses.md#context-megadinodropcontroller)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MD_HeadDrop` | |

</details>


---

### Enum: `hit_animation_alt`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `catch` | |

</details>


---

### Enum: `huntercat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `iceelemental`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `ignore_if_str_aux_equals`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TintItem`](./Items_and_Equipment.md#context-tintitem)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ModelingClay_Default` | |

</details>


---

### Enum: `ignore_tagged_sources`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MoveTowardsDamageSource`](./Characters_and_Bosses.md#context-movetowardsdamagesource)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `megadino` | |

</details>


---

### Enum: `increment_savefile_counter`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `GameStat_CountNukeQuestCompletions` | |

</details>


---

### Enum: `infestedduo`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `int`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `aux` | |

</details>


---

### Enum: `jump_height_multiplier`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.25` | |

</details>


---

### Enum: `jurassic`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`prereqs`](./Progression_Unlocks.md#context-prereqs)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `endoftime` | |

</details>


---

### Enum: `kill_enemy`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Enemy_AI.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.2` | |

</details>


---

### Enum: `knockback_modifier`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `rotate_cw` | |

</details>


---

### Enum: `lck`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `aux` | |

</details>


---

### Enum: `leg_leave`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MegaDinoDropController`](./Characters_and_Bosses.md#context-megadinodropcontroller)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MD_LegLeave` | |

</details>


---

### Enum: `leg_return`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MegaDinoDropController`](./Characters_and_Bosses.md#context-megadinodropcontroller)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MD_LegReturn` | |

</details>


---

### Enum: `legacy_savekey`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RunWhenLastPlayerCatIsCharmed`](./Characters_and_Bosses.md#context-runwhenlastplayercatischarmed)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Legacy_Marshmallow_StolenCatID` | |

</details>


---

### Enum: `lenny`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `lightningelemental`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `lob_speed`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `lose_all_equipped_items`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cat` | |

</details>


---

### Enum: `low_health_character_threshold`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `item_aux` | |

</details>


---

### Enum: `magecat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `mamamaggot`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `min_radius`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnVolcanoOnBattleStart`](./House_and_Environment.md#context-spawnvolcanoonbattlestart)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.2` | |

</details>


---

### Enum: `min_throw_height`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.25` | |

</details>


---

### Enum: `monkcat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `moon`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`prereqs`](./Progression_Unlocks.md#context-prereqs)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `mapflag_IceAgeUnlocked` | |

</details>


---

### Enum: `name_mod`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CAT_NAME_MOD_DEMONIC` | |

</details>


---

### Enum: `necrocat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `new_music`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChaosHeadDropIn`](./Characters_and_Bosses.md#context-chaosheaddropin)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `chaos_boss_part2` | |

</details>


---

### Enum: `no_buddy`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SyncFormsWithBuddy`](./Characters_and_Bosses.md#context-syncformswithbuddy)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Rage` | |

</details>


---

### Enum: `once_per_fight`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`cost`](./Abilities_and_Spells.md#context-cost)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `3-X` | |

</details>


---

### Enum: `ontrigger_intentional`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sounds`](./Abilities_and_Spells.md#context-sounds)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Lenny_HereKitty` | |

</details>


---

### Enum: `other_character`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossSyncAnimations`](./Characters_and_Bosses.md#context-finalbosssyncanimations)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MegaGuppy` | |

</details>


---

### Enum: `override_end_option_prompt`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `EVENT_USETHETOILET_AGAIN` | |

</details>


---

### Enum: `override_portrait`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Characters_and_Bosses.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Cherub` | |

</details>


---

### Enum: `party_injury`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `random` | |

</details>


---

### Enum: `pass_ani`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#context-mothertumorpassive)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pass` | |

</details>


---

### Enum: `play_result_animation`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `resultVeryGood` | |

</details>


---

### Enum: `post_absorb_move_weights`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `minimum_move` | |

</details>


---

### Enum: `precast_delay`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#context-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.25` | |

</details>


---

### Enum: `prioritize_throw_target_with_passive`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `NubbyTossPriority` | |

</details>


---

### Enum: `psychiccat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `puddle_tile`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnVolcanoOnBattleStart`](./House_and_Environment.md#context-spawnvolcanoonbattlestart)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `LavaTile` | |

</details>


---

### Enum: `punch_self_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DybbukPossessed`](./Abilities_and_Spells.md#context-dybbukpossessed)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Dybbuk_StopHittingYourself` | |

</details>


---

### Enum: `queenhippo`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `queue`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossBeamQueue`](./Characters_and_Bosses.md#context-finalbossbeamqueue)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TheChild_TargetBeam` | |

</details>


---

### Enum: `radicalrat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `range_symmetry`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `eight_way` | |

</details>


---

### Enum: `ratking`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `receive_ani`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](./Characters_and_Bosses.md#context-mothertumorpassive)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `receive` | |

</details>


---

### Enum: `release`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossBeamQueue`](./Characters_and_Bosses.md#context-finalbossbeamqueue)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TheChild_ReleaseBeams` | |

</details>


---

### Enum: `reserved`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Spawns_and_Enemy_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `for` | |

</details>


---

### Enum: `reset_center_because_no_target_halflife`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossPupils`](./Characters_and_Bosses.md#context-finalbosspupils)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.1` | |

</details>


---

### Enum: `reset_center_because_of_animation_halflife`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossPupils`](./Characters_and_Bosses.md#context-finalbosspupils)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.05` | |

</details>


---

### Enum: `reset_str_aux_on_store`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ModelingClay_Default` | |

</details>


---

### Enum: `reset_unlock`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `nuke_quest_begin` | |

</details>


---

### Enum: `restructions`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](./Abilities_and_Spells.md#context-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `aoe_must_exist` | |

</details>


---

### Enum: `rockybobo`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `roll_ability`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](./Characters_and_Bosses.md#context-ai)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `RollDice` | |

</details>


---

### Enum: `scramble_basic_attack`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `all` | |

</details>


---

### Enum: `scramble_passives`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `all` | |

</details>


---

### Enum: `select_item_from_pool_for_cutscene_only`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `glitched_items` | |

</details>


---

### Enum: `shader`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPostProcessEffect`](./House_and_Environment.md#context-addpostprocesseffect)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `shimmervignette` | |

</details>


---

### Enum: `shield`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `aux` | |

</details>


---

### Enum: `slime`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `sound_event`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ModularPickup`](./Characters_and_Bosses.md#context-modularpickup)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `EatAntidote` | |

</details>


---

### Enum: `spawn_node`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `start` | |

</details>


---

### Enum: `spd`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `aux` | |

</details>


---

### Enum: `spell`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MonkCatReactionAbilities`](./Characters_and_Bosses.md#context-monkcatreactionabilities)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MCHadouken` | |

</details>


---

### Enum: `spewer`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `stacy`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `str`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `aux` | |

</details>


---

### Enum: `str_aux`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Items_and_Equipment.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ModelingClay_Default` | |

</details>


---

### Enum: `tankcat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `teleport_tracking_halflife`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossPupils`](./Characters_and_Bosses.md#context-finalbosspupils)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.01` | |

</details>


---

### Enum: `thebloat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `theend`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`prereqs`](./Progression_Unlocks.md#context-prereqs)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `endoftime` | |

</details>


---

### Enum: `thiefcat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `threshold_expr`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#context-conditional_healththreshold)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `item_aux` | |

</details>


---

### Enum: `threshold_min`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AbilityHealthThreshold`](./Characters_and_Bosses.md#context-abilityhealththreshold)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `X` | |

</details>


---

### Enum: `tinkerercat`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `total_distance_moved`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Enemy_AI.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |

</details>


---

### Enum: `tracking_acquisition_halflife`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossPupils`](./Characters_and_Bosses.md#context-finalbosspupils)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.1` | |

</details>


---

### Enum: `trampy`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `transform`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossBeamQueue`](./Characters_and_Bosses.md#context-finalbossbeamqueue)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TheChild_TransformBoris` | |

</details>


---

### Enum: `tumor_object`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherGrowController`](./Characters_and_Bosses.md#context-mothergrowcontroller)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MotherTumor` | |

</details>


---

### Enum: `unlock_item`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Progression_Unlocks.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MomsKnife` | |

</details>


---

### Enum: `unlockcheck_on_complete`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`boss`](./Map_Generation_and_Routing.md#context-boss)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `map_unlock_junkyard` | |

</details>


---

### Enum: `utility`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Spawns_and_Enemy_Pools.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `PlayerSpawn` | |

</details>


---

### Enum: `zodiac`
<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#context-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `math_equation`
<details>
<summary><b>Expand</b></summary>

This is not a strict Enum, but rather a representation of inline math equations. In the Mewgenics engine, many numeric fields can accept a math equation string instead of a raw number.

**Supported Functions:**<br>
`max(a, b)`, `min(a, b)`, `floor(x)`, `ceil(x)`, `abs(x)`, `round(x)`

**Common Variables:**<br>
`str`, `dex`, `int`, `con`, `cha`, `lck`, `mov`, `lvl`, `health`, `bonus_melee_damage`, `bonus_ranged_damage`, `bonus_range`, `bonus_basic_spell_damage`

**Examples:**<br>`"max(str, int) + 5"`, `mov+2`, `"floor(lvl/2)"`


</details>

---
