---
title: "Enums Schema"
description: "Valid string identifiers for all enum-backed properties."
---

# Enums Schema

## Overview
> [!NOTE]
> This schema lists all hardcoded C++ enumerations, so you know exactly which keywords are valid for enum properties.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
ElementEnum {
    // e.g. valid inputs for "element" are Fire, Water, Earth, Electric
}
```

---

This document provides exhaustive lists of all enum and string values found in the base game's `.gon` files for every applicable property key.

> **Note on Values:** The lists below represent *Confirmed Values* extracted directly from the base game's source files. It is highly likely that there are other valid enum or string values supported by the engine that are simply not used in the vanilla files. You will need to experiment or rely on context clues to discover undocumented values.

## Enums Dictionary


#### Enum: `template`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-root)

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

| `template_dash_attack` | |
| `template_jump_attack` | |
| `template_jump_move` | |
| `template_laser` | |
| `template_leave` | |
| `template_lobbed_attack` | |
| `template_melee_attack` | |
| `template_melee_spell` | |
| `template_move` | |
| `template_multihit_self_buff` | |
| `template_placeholder` | |
| `template_ranged_attack` | |
| `template_return` | |
| `template_self_buff` | |
| `template_spawn` | |
| `template_spell` | |
| `template_straightshot_attack` | |
| `template_swap` | |
| `template_targeted_status` | |
| `template_teleport` | |
| `template_throw_attack` | |
| `template_tile_targeted_melee_attack` | |
| `template_trample_dash` | |

</details>


---

### Enum: `animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics), [`meta`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-meta), [`Cat`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cat), [`NonCat`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-noncat), [`Nothing`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-nothing), [`StatusEachTurnBeginIfHasStatus`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statuseachturnbeginifhasstatus), [`TransformInXTurns`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-transforminxturns), `10coins`, `5coins`, [`ROOT` (Events_and_Encounters)](../World_Maps_and_Events/Events_and_Encounters.md#object-root), [`a`](../World_Maps_and_Events/Events_and_Encounters.md#object-a), [`activate_p`](../World_Maps_and_Events/Events_and_Encounters.md#object-activate_p), [`activate_z`](../World_Maps_and_Events/Events_and_Encounters.md#object-activate_z), [`attach_amplifier`](../World_Maps_and_Events/Events_and_Encounters.md#object-attach_amplifier), [`attach_antenna`](../World_Maps_and_Events/Events_and_Encounters.md#object-attach_antenna), [`attach_leech`](../World_Maps_and_Events/Events_and_Encounters.md#object-attach_leech), [`b`](../World_Maps_and_Events/Events_and_Encounters.md#object-b), [`bite`](../World_Maps_and_Events/Events_and_Encounters.md#object-bite), [`blue`](../World_Maps_and_Events/Events_and_Encounters.md#object-blue), [`boogers`](../World_Maps_and_Events/Events_and_Encounters.md#object-boogers), [`book`](../World_Maps_and_Events/Events_and_Encounters.md#object-book), [`brace`](../World_Maps_and_Events/Events_and_Encounters.md#object-brace), [`button`](../World_Maps_and_Events/Events_and_Encounters.md#object-button), [`buy1`](../World_Maps_and_Events/Events_and_Encounters.md#object-buy1), [`c`](../World_Maps_and_Events/Events_and_Encounters.md#object-c), [`counter`](../World_Maps_and_Events/Events_and_Encounters.md#object-counter), [`d`](../World_Maps_and_Events/Events_and_Encounters.md#object-d), [`damage`](../World_Maps_and_Events/Events_and_Encounters.md#object-damage), [`donate`](../World_Maps_and_Events/Events_and_Encounters.md#object-donate), [`donate_10`](../World_Maps_and_Events/Events_and_Encounters.md#object-donate_10), [`donate_15`](../World_Maps_and_Events/Events_and_Encounters.md#object-donate_15), [`donate_20`](../World_Maps_and_Events/Events_and_Encounters.md#object-donate_20), [`donate_5`](../World_Maps_and_Events/Events_and_Encounters.md#object-donate_5), [`double`](../World_Maps_and_Events/Events_and_Encounters.md#object-double), [`enter`](../World_Maps_and_Events/Events_and_Encounters.md#object-enter), [`examine`](../World_Maps_and_Events/Events_and_Encounters.md#object-examine), [`fill_jar`](../World_Maps_and_Events/Events_and_Encounters.md#object-fill_jar), [`find_another_way`](../World_Maps_and_Events/Events_and_Encounters.md#object-find_another_way), [`fire`](../World_Maps_and_Events/Events_and_Encounters.md#object-fire), [`future`](../World_Maps_and_Events/Events_and_Encounters.md#object-future), [`go_around`](../World_Maps_and_Events/Events_and_Encounters.md#object-go_around), [`holy`](../World_Maps_and_Events/Events_and_Encounters.md#object-holy), [`home`](../World_Maps_and_Events/Events_and_Encounters.md#object-home), [`hp`](../World_Maps_and_Events/Events_and_Encounters.md#object-hp), [`ice`](../World_Maps_and_Events/Events_and_Encounters.md#object-ice), [`ignore`](../World_Maps_and_Events/Events_and_Encounters.md#object-ignore), [`infinite`](../World_Maps_and_Events/Events_and_Encounters.md#object-infinite), [`intimidation`](../World_Maps_and_Events/Events_and_Encounters.md#object-intimidation), [`itchies`](../World_Maps_and_Events/Events_and_Encounters.md#object-itchies), [`knife`](../World_Maps_and_Events/Events_and_Encounters.md#object-knife), [`leave`](../World_Maps_and_Events/Events_and_Encounters.md#object-leave), [`leave_it_in`](../World_Maps_and_Events/Events_and_Encounters.md#object-leave_it_in), [`lever`](../World_Maps_and_Events/Events_and_Encounters.md#object-lever), [`lick`](../World_Maps_and_Events/Events_and_Encounters.md#object-lick), [`lightning`](../World_Maps_and_Events/Events_and_Encounters.md#object-lightning), [`loot`](../World_Maps_and_Events/Events_and_Encounters.md#object-loot), [`loot_heart`](../World_Maps_and_Events/Events_and_Encounters.md#object-loot_heart), [`makeup`](../World_Maps_and_Events/Events_and_Encounters.md#object-makeup), [`nothanks`](../World_Maps_and_Events/Events_and_Encounters.md#object-nothanks), [`past`](../World_Maps_and_Events/Events_and_Encounters.md#object-past), [`pirouette`](../World_Maps_and_Events/Events_and_Encounters.md#object-pirouette), [`place_gristle`](../World_Maps_and_Events/Events_and_Encounters.md#object-place_gristle), [`poop`](../World_Maps_and_Events/Events_and_Encounters.md#object-poop), [`protection`](../World_Maps_and_Events/Events_and_Encounters.md#object-protection), [`put_in_coins`](../World_Maps_and_Events/Events_and_Encounters.md#object-put_in_coins), [`receive`](../World_Maps_and_Events/Events_and_Encounters.md#object-receive), [`red`](../World_Maps_and_Events/Events_and_Encounters.md#object-red), [`reflect`](../World_Maps_and_Events/Events_and_Encounters.md#object-reflect), [`run`](../World_Maps_and_Events/Events_and_Encounters.md#object-run), [`run_again`](../World_Maps_and_Events/Events_and_Encounters.md#object-run_again), [`sacrifice`](../World_Maps_and_Events/Events_and_Encounters.md#object-sacrifice), [`sacrifice_full_favor`](../World_Maps_and_Events/Events_and_Encounters.md#object-sacrifice_full_favor), [`sacrifice_normal`](../World_Maps_and_Events/Events_and_Encounters.md#object-sacrifice_normal), [`sacrifice_partial_favor`](../World_Maps_and_Events/Events_and_Encounters.md#object-sacrifice_partial_favor), [`sacrifice_quest`](../World_Maps_and_Events/Events_and_Encounters.md#object-sacrifice_quest), [`skip`](../World_Maps_and_Events/Events_and_Encounters.md#object-skip), [`speed`](../World_Maps_and_Events/Events_and_Encounters.md#object-speed), [`surprise`](../World_Maps_and_Events/Events_and_Encounters.md#object-surprise), [`take`](../World_Maps_and_Events/Events_and_Encounters.md#object-take), [`take_blood`](../World_Maps_and_Events/Events_and_Encounters.md#object-take_blood), [`tappytoes`](../World_Maps_and_Events/Events_and_Encounters.md#object-tappytoes), [`thorns`](../World_Maps_and_Events/Events_and_Encounters.md#object-thorns), [`touch`](../World_Maps_and_Events/Events_and_Encounters.md#object-touch), [`w1`](../World_Maps_and_Events/Events_and_Encounters.md#object-w1), [`w2`](../World_Maps_and_Events/Events_and_Encounters.md#object-w2), [`w3`](../World_Maps_and_Events/Events_and_Encounters.md#object-w3), [`w4`](../World_Maps_and_Events/Events_and_Encounters.md#object-w4), [`w5`](../World_Maps_and_Events/Events_and_Encounters.md#object-w5), [`w6`](../World_Maps_and_Events/Events_and_Encounters.md#object-w6), [`wheezies`](../World_Maps_and_Events/Events_and_Encounters.md#object-wheezies), [`CatAPultAnimation`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catapultanimation)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `alertend` | |
| `angry` | |
| `angryfail` | |
| `appear` | |
| `attach` | |
| `attack` | |
| `attack2` | |
| `attackL` | |
| `attackR` | |
| `attackRage` | |
| `backflipLoop` | |
| `bash` | |
| `beam` | |
| `beamin` | |
| `bearHug` | |
| `becomemutant` | |
| `becomezealot` | |
| `bellypound` | |
| `bigdoubleswat` | |
| `bigkick` | |
| `birth` | |
| `bite` | |
| `biteattack` | |
| `blast1` | |
| `blast2` | |
| `bless` | |
| `blizzard` | |
| `block` | |
| `blowFire` | |
| `blowKiss` | |
| `blowUp` | |
| `bodypulse` | |
| `bomb` | |
| `bombardment` | |
| `bounce` | |
| `brace` | |
| `breakarm` | |
| `breakleg` | |
| `breakneck` | |
| `breakshield` | |
| `breathing` | |
| `bruise` | |
| `buildRobot` | |
| `buildRobotProjectile` | |
| `burp` | |
| `butcherAttack` | |
| `buttScootLoop` | |
| `call` | |
| `calmdown` | |
| `cartwheelLoop` | |
| `castspell` | |
| `catdying` | |
| `celebrate` | |
| `change` | |
| `changechannel` | |
| `chargedodges` | |
| `chargeholy` | |
| `charm` | |
| `cheat` | |
| `chestpound` | |
| `chew` | |
| `chewing` | |
| `choice_coins_one` | |
| `choice_coins_ten` | |
| `choice_coins_twentyfive` | |
| `choice_con` | |
| `choice_dex_alt` | |
| `choice_leave` | |
| `choice_misc` | |
| `clapTogether` | |
| `coinFlip` | |
| `ColorlessStartTurn` | |
| `consume` | |
| `controlmonster` | |
| `counter` | |
| `crash` | |
| `createmagic` | |
| `cry` | |
| `cry1` | |
| `cry2` | |
| `curlup` | |
| `curse` | |
| `cut` | |
| `cuteIdle` | |
| `dash` | |
| `dashbite` | |
| `dashend` | |
| `Default` | |
| `detonate` | |
| `dig` | |
| `digest` | |
| `dodge` | |
| `doom` | |
| `doublepunch` | |
| `doubleswat` | |
| `doublevision` | |
| `drink` | |
| `drinkTrinket` | |
| `drop` | |
| `druidTransform` | |
| `dying` | |
| `earthquakeSlam` | |
| `eat` | |
| `eatTrinket` | |
| `egg` | |
| `eject` | |
| `enrage` | |
| `entangle` | |
| `equipWeapon` | |
| `escape` | |
| `evilMagic` | |
| `exhale` | |
| `exit` | |
| `explode` | |
| `fail` | |
| `falconPunch` | |
| `fart` | |
| `fartoom` | |
| `fast` | |
| `fire` | |
| `firestorm` | |
| `fizzle` | |
| `flames` | |
| `flex` | |
| `flip` | |
| `floatingmagic` | |
| `flush` | |
| `freeze` | |
| `fumble` | |
| `fumble2` | |
| `fury` | |
| `fx_statup` | |
| `girlyIdle` | |
| `glare` | |
| `grab` | |
| `grabCorpse` | |
| `groundpound` | |
| `grow` | |
| `growup` | |
| `guard` | |
| `gulp` | |
| `gutball` | |
| `hadouken` | |
| `hatch` | |
| `haunt` | |
| `headbutt` | |
| `headbuttUppercut` | |
| `heal` | |
| `heartattack` | |
| `heaviestMelee` | |
| `heavyMelee` | |
| `heil` | |
| `hide` | |
| `hiss` | |
| `hithard` | |
| `holy` | |
| `hopinplace` | |
| `howl` | |
| `hug` | |
| `humandie` | |
| `ice` | |
| `icebreath` | |
| `idea` | |
| `identify` | |
| `idle` | |
| `inhale` | |
| `insane` | |
| `intro` | |
| `invthrow` | |
| `jab` | |
| `jetloop` | |
| `jitter` | |
| `karateKid` | |
| `kick` | |
| `kicksand` | |
| `kiss` | |
| `knead` | |
| `knockswatatk` | |
| `knockupatk` | |
| `laserShoot` | |
| `launch` | |
| `lava` | |
| `leave` | |
| `lick` | |
| `lickAttack` | |
| `lift` | |
| `liquidclone` | |
| `liquidmetalspear` | |
| `liquidunclone` | |
| `loot` | |
| `magnet` | |
| `majormagic` | |
| `meditate` | |
| `megabite` | |
| `megablast` | |
| `megaslap` | |
| `meow` | |
| `meteorshower` | |
| `metronome` | |
| `mindcontrol` | |
| `monkAttack` | |
| `MonkStartTurn` | |
| `mouthbeam` | |
| `moveLoop` | |
| `necksnap` | |
| `none` | |
| `nuke` | |
| `open` | |
| `openmouth` | |
| `order` | |
| `peck` | |
| `pickpocket` | |
| `pickup` | |
| `pissYourself` | |
| `pointout` | |
| `poke` | |
| `poop` | |
| `poopfart` | |
| `poopfartbehind` | |
| `portin` | |
| `portout` | |
| `powder` | |
| `power` | |
| `powerup` | |
| `pray` | |
| `prime` | |
| `probe` | |
| `proud` | |
| `prouder` | |
| `psyAttack1` | |
| `psyAttack2` | |
| `psyAttack3` | |
| `psyMegaAttack` | |
| `puff` | |
| `puke` | |
| `pukeatk` | |
| `pullin` | |
| `pullremote` | |
| `pulp` | |
| `pulse` | |
| `pulse2` | |
| `pulse3` | |
| `punchSelf` | |
| `quarterswipe` | |
| `Quiver` | |
| `radiant` | |
| `rage` | |
| `raise` | |
| `react` | |
| `reaction` | |
| `recharge` | |
| `reflex` | |
| `releaseCommand1` | |
| `releaseCommand2` | |
| `releaseCommand3` | |
| `releaseCommand4` | |
| `reload` | |
| `resultExplode` | |
| `resultJackpot` | |
| `resultLeave` | |
| `resultLose` | |
| `resultWin` | |
| `return` | |
| `revenge` | |
| `revive` | |
| `ripandtear` | |
| `rise` | |
| `roar` | |
| `RocketFromAbove` | |
| `roll` | |
| `rumble` | |
| `run` | |
| `runincircles` | |
| `scorpionSting` | |
| `scratch` | |
| `scratchear` | |
| `scream` | |
| `selfHarm` | |
| `shake` | |
| `shield` | |
| `shocking` | |
| `shoot` | |
| `shootForward` | |
| `shootLava` | |
| `shoulder` | |
| `showclaws` | |
| `showTrinket` | |
| `shred` | |
| `shriek` | |
| `shrink` | |
| `sing1` | |
| `sing2` | |
| `sing3` | |
| `singleSpin` | |
| `slam` | |
| `sliceOpen` | |
| `slowPawMagic` | |
| `spawn` | |
| `spawnChild` | |
| `spawnHolding` | |
| `spawnHoldingCat` | |
| `spawnmama` | |
| `special` | |
| `spell` | |
| `spike` | |
| `spikes` | |
| `spin` | |
| `spinAttack` | |
| `spit` | |
| `splashatk` | |
| `spore` | |
| `squeeze` | |
| `statup` | |
| `statusReaction` | |
| `stomp` | |
| `stompy` | |
| `stoneFists` | |
| `strike` | |
| `struggle` | |
| `suck` | |
| `suck1` | |
| `suck2` | |
| `suggest` | |
| `suicide` | |
| `summon` | |
| `suplex` | |
| `swat` | |
| `swatupatk` | |
| `swing` | |
| `swipe` | |
| `tailwag` | |
| `tailwhip` | |
| `tantrum` | |
| `tapatk` | |
| `tauntwiggle` | |
| `telekinesis` | |
| `terminatorPunch` | |
| `thinking` | |
| `thrash` | |
| `throw` | |
| `throwArrow` | |
| `throwbigelement` | |
| `throwboss` | |
| `throwobject` | |
| `throwshield` | |
| `thumbsup` | |
| `tinker` | |
| `tinkerAdjacent` | |
| `tinkerSelf` | |
| `tinyPunch` | |
| `TinyTumorA` | |
| `TinyTumorB` | |
| `TinyTumorC` | |
| `transform` | |
| `transform1` | |
| `transform2` | |
| `transform3` | |
| `trip` | |
| `tripleswat` | |
| `turnOff` | |
| `turtlestart` | |
| `twitchyIdle` | |
| `uncrack` | |
| `unguard` | |
| `uppercut` | |
| `uppercutatk` | |
| `use` | |
| `uziShoot` | |
| `vomitrain` | |
| `walk` | |
| `walk2` | |
| `walkAngry` | |
| `weaponAbsorb` | |
| `weaponpoke` | |
| `weaponshoot` | |
| `weaponslam` | |
| `weaponspell` | |
| `weaponspell2` | |
| `weaponspell3` | |
| `weaponSpinAttack` | |
| `weaponstab` | |
| `weaponswing` | |
| `weaponswingup` | |
| `weaponthrowhigh` | |
| `weaponthrowstraight` | |
| `weaponTina` | |
| `web` | |
| `whisper` | |
| `whistle` | |
| `wind` | |
| `wisps` | |
| `yell` | |
| `yell1` | |
| `yell2` | |
| `yell3` | |
| `yella` | |
| `yellb` | |
| `zombie` | |

| `ClassFromNeutral` | |
| `ClassToNeutral` | |
| `HitGround` | |
| `StartTurn` | |
| `Victory` | |
| `bite2` | |

</details>


---

### Enum: `class`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-root), [`meta`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-meta), [`ClassManaCostReduction`](../Player_Progression_and_Cats/Cat_Mutations.md#object-classmanacostreduction), [`ClassManaCostReduction`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-classmanacostreduction), [`ClassManaCostReduction`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-classmanacostreduction), [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

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

> **Also Used In:** These values are also referenced by [`class_anis`](#enum-class_anis), [`MulticlassLevelUp`](#enum-multiclasslevelup), [`ChangeCatClass`](#enum-changecatclass), [`complete_checklist_with_class`](#enum-complete_checklist_with_class), [`EvolveAbilityFromPool`](#enum-evolveabilityfrompool), [`palette`](#enum-palette), [`ConjureBonusAbility`](#enum-conjurebonusability), [`LevelUpClassOverride`](#enum-levelupclassoverride).

</details>


---

### Enum: `variant_of`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-root), [`ROOT` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-root), [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root), `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicMelee` | |
| `Gibs_default` | |
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
| `BloodBounce` | |
| `BloodPoof` | |
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
| `BloodBounceCrit` | |
| `BloodGeyser` | |
| `BloodMagic` | |
| `BloodPoofCrit` | |
| `BloodPopCrit` | |
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
| `CaveDrip` | |
| `CaveSplash` | |
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

> **Also Used In:** These values are also referenced by [`unlock_ability`](#enum-unlock_ability), [`TransformAbility`](#enum-transformability), [`DeadAltAbility`](#enum-deadaltability), [`SpawnOnDowned`](#enum-spawnondowned), [`ability_icon`](#enum-ability_icon), [`ObjectOnHitEmpty`](#enum-objectonhitempty), [`learn_ability`](#enum-learn_ability), [`BreakIntoRocks`](#enum-breakintorocks), [`GroundFlopper`](#enum-groundflopper), [`TeamCastAbility`](#enum-teamcastability), [`trap`](#enum-trap), [`SpawnCustomTrap`](#enum-spawncustomtrap), [`MoveAwayFromDamageSource`](#enum-moveawayfromdamagesource).

</details>


---

### Enum: `kind`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `trinket` | |
| `weapon` | |
| `head` | |
| `face` | |
| `neck` | |
| `modifier` | |

> **See Also:** Values from [`slot`](#enum-slot) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`restrict`](#enum-restrict).

</details>


---

### Enum: `rarity`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

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

> **Referenced by:** [`AfterImage`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-afterimage), [`DustOnHit`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-dustonhit), [`LeaveBehind`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-leavebehind), [`ObjectOnHit`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-objectonhit), [`ObjectOnHitCharacter`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-objectonhitcharacter), [`PopAndSpawn`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-popandspawn), [`spawn`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-spawn), [`SpawnEachTurn`](../Player_Progression_and_Cats/Cat_Mutations.md#object-spawneachturn), [`SpawnExtraThingsOnBattleStart`](../Player_Progression_and_Cats/Cat_Mutations.md#object-spawnextrathingsonbattlestart), [`SpawnOnBattleStartRandomEmptyTile`](../Player_Progression_and_Cats/Cat_Mutations.md#object-spawnonbattlestartrandomemptytile), [`SpawnThingOnDamage`](../Player_Progression_and_Cats/Cat_Mutations.md#object-spawnthingondamage), [`SpawnThingOnDamage`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-spawnthingondamage), [`TransformInXTurns`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-transforminxturns), [`TransformOnElementInfluence`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-transformonelementinfluence), [`TransformOnElementInfluencex`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-transformonelementinfluencex), [`TransformOnStatusThreshold`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-transformonstatusthreshold), [`SpawnOnBattleStart`](../Core_Entities_and_Combat/Elite_Buffs.md#object-spawnonbattlestart), `ROOT`, [`gain_clone_familiar`](../World_Maps_and_Events/Events_and_Encounters.md#object-gain_clone_familiar), [`gain_familiar`](../World_Maps_and_Events/Events_and_Encounters.md#object-gain_familiar), [`spawn_unit_next_fight`](../World_Maps_and_Events/Events_and_Encounters.md#object-spawn_unit_next_fight), [`AllyInfested`](../World_Maps_and_Events/House_and_Environment.md#object-allyinfested), [`GlobalSpawnOnRoundEnd`](../World_Maps_and_Events/House_and_Environment.md#object-globalspawnonroundend), [`SpawnExtraThingsOnBattleStart`](../World_Maps_and_Events/House_and_Environment.md#object-spawnextrathingsonbattlestart), [`SpawnVolcanoOnBattleStart`](../World_Maps_and_Events/House_and_Environment.md#object-spawnvolcanoonbattlestart), [`ObjectDetector`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-objectdetector), [`ObjectOnHitCharacter`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-objectonhitcharacter), [`PoopWhenHit`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-poopwhenhit), `SpawnCatCopyOnBattleStart`, `SpawnCatCopyWhenDowned`, [`SpawnEachTurn`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-spawneachturn), [`SpawnExtraThingsOnBattleStart`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-spawnextrathingsonbattlestart), [`SpawnItemLinkedFamiliar`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-spawnitemlinkedfamiliar), [`SpawnObjectOnPopCorpse`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-spawnobjectonpopcorpse), [`SpawnOnBattleStart`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-spawnonbattlestart), [`SpawnOnBattleStartRandomEmptyTile`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-spawnonbattlestartrandomemptytile), [`SpawnThingOnDamage`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-spawnthingondamage), [`ObjectOnHitCharacter`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-objectonhitcharacter), [`SpawnCatCopyOnBattleStart`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawncatcopyonbattlestart), [`SpawnEachTurn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawneachturn), [`SpawnOnBattleStart`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnonbattlestart), [`SpawnOnBattleStartRandomEmptyTile`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnonbattlestartrandomemptytile), [`SpawnThingOnDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnthingondamage), [`ROOT` (Spawns_and_Enemy_Pools)](../World_Maps_and_Events/Spawns_and_Enemy_Pools.md#object-root), [`weather_element_alt`](../World_Maps_and_Events/Spawns_and_Enemy_Pools.md#object-weather_element_alt)

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
| `CharmedPooter` | |
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

> **Also Used In:** These values are also referenced by [`movieclip`](#enum-movieclip), [`custom_cat_data`](#enum-custom_cat_data), [`SpawnOnDeath`](#enum-spawnondeath), [`BounceObject`](#enum-bounceobject), [`ObjectOnHitCharacter`](#enum-objectonhitcharacter), [`SpawnOnBattleStart`](#enum-spawnonbattlestart), [`SpawnThingOnDeath`](#enum-spawnthingondeath), [`Buddy`](#enum-buddy), [`obj`](#enum-obj), [`TransformOnDeath`](#enum-transformondeath), [`SpawnThingIfHitKills`](#enum-spawnthingifhitkills), [`SpawnOnDowned`](#enum-spawnondowned), [`event`](#enum-event), [`Divide4OnDeath`](#enum-divide4ondeath), [`Imprison`](#enum-imprison), [`ObjectOnHit`](#enum-objectonhit), [`ObjectOnHitEmpty`](#enum-objectonhitempty), [`SpawnObjectOnPopCorpse`](#enum-spawnobjectonpopcorpse), [`BreakIntoRocks`](#enum-breakintorocks), [`gain_immortal_familiar`](#enum-gain_immortal_familiar), [`LeaveBehindOnceEachMove`](#enum-leavebehindonceeachmove).
| `GiantFly` | |
| `GooSlime` | |
| `Grandpa` | |
| `Legs` | |
| `MeatGolem` | |
| `MeowMutant` | |
| `Mimic` | |
| `small_trash_cans` | |
| `x` | |
| `contextual` | |

</details>


---

### Enum: `set`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Furniture_and_Metaprogression)](../World_Maps_and_Events/Furniture_and_Metaprogression.md#object-root), [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root), `StatusOnSetPieceBreak`

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

> **Also Used In:** These values are also referenced by [`class_anis`](#enum-class_anis), [`MulticlassLevelUp`](#enum-multiclasslevelup), [`ChangeCatClass`](#enum-changecatclass), [`complete_checklist_with_class`](#enum-complete_checklist_with_class), [`EvolveAbilityFromPool`](#enum-evolveabilityfrompool), [`palette`](#enum-palette), [`SetFragileImmune`](#enum-setfragileimmune), [`SetBrittleImmune`](#enum-setbrittleimmune).
| `Ancestor` | |
| `Dino` | |
| `Phoenix` | |

</details>


---

### Enum: `tag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_hastag), [`Conditional_SourceAbilityHasTag`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_sourceabilityhastag), [`ForceMoveTowardsTaggedObject`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-forcemovetowardstaggedobject), `-2`, `1026`, `1500`, `300`, `301`, `302`, `303`, `304`, `306`, `307`, `308`, `309`, `310`, `311`, `313`, `314`, `315`, `316`, `318`, `319`, `321`, `322`, `325`, `327`, `328`, `329`, `336`, `337`, `339`, `343`, `345`, `353`, `400`, `401`, `402`, `403`, `404`, `405`, `406`, `407`, `408`, `409`, `410`, `411`, `412`, `413`, `414`, `415`, `416`, `417`, `418`, `419`, `420`, `421`, `422`, `423`, `424`, `425`, `426`, `427`, `428`, `429`, `430`, `431`, `432`, `433`, `434`, `435`, `436`, `437`, `438`, `439`, `440`, `441`, `442`, `700`, `701`, `702`, `703`, `704`, `705`, `706`, `707`, `750`, `752`, `753`, [`AbilityWhenTaggedCharacterMovesNear`](../Player_Progression_and_Cats/Cat_Mutations.md#object-abilitywhentaggedcharactermovesnear), [`AbilityWhenTaggedCharacterMovesNear`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-abilitywhentaggedcharactermovesnear), [`CaveFamilyEnrage`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cavefamilyenrage), [`ChaosHeadDropIn`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-chaosheaddropin), [`HitlerExecute`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-hitlerexecute), [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties), [`CharacterTypeGainsStatusAtBattleStart`](./Miscellaneous.md#object-charactertypegainsstatusatbattlestart), `ROOT`, [`CharacterTypeGainsStatusAtBattleStart`](../World_Maps_and_Events/Events_and_Encounters.md#object-charactertypegainsstatusatbattlestart), [`random_mutation`](../World_Maps_and_Events/Events_and_Encounters.md#object-random_mutation), [`CharacterTypeGainsStatusAtBattleStart`](../World_Maps_and_Events/House_and_Environment.md#object-charactertypegainsstatusatbattlestart), [`Conditional_HasTag`](../World_Maps_and_Events/House_and_Environment.md#object-conditional_hastag), [`FactionUprising`](../World_Maps_and_Events/House_and_Environment.md#object-factionuprising), [`Conditional_HasTag`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_hastag), [`SpawnRandomPickupsOnTaggedUnitKilled`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-spawnrandompickupsontaggedunitkilled), [`AbilityWhenTaggedCharacterMovesNear`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-abilitywhentaggedcharactermovesnear), [`Conditional_HasTag`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_hastag), [`Conditional_SourceHasTag`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_sourcehastag), [`ManaCostReductionTagged`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-manacostreductiontagged), [`StatusOnUseAbilityWithTag`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonuseabilitywithtag), [`TaggedPickupEffectReplacement`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-taggedpickupeffectreplacement)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `common` | |
| `cat` | |
| `birth_defect` | |
| `animal` | |
| `blob` | |
| `rock` | |
| `humanoid` | |
| `robot` | |
| `worm` | |
| `rat` | |
| `bug` | |
| `fetus` | |
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
| `angel` | |
| `decoy` | |
| `elemental` | |
| `fish` | |
| `golem` | |
| `mount` | |
| `siren` | |
| `squirrel` | |
| `undead` | |

> **Also Used In:** These values are also referenced by [`target_requires_tag`](#enum-target_requires_tag), [`AddTag`](#enum-addtag), [`AddHiddenTag`](#enum-addhiddentag), [`TagGreed`](#enum-taggreed), [`tag_filter`](#enum-tag_filter), [`FactionUprising`](#enum-factionuprising), [`HolyShieldTransferToTaggedMinions`](#enum-holyshieldtransfertotaggedminions), [`RandomTaggedMutation`](#enum-randomtaggedmutation), [`UpgradeTaggedSpawnsToChampions`](#enum-upgradetaggedspawnstochampions), [`enemy_type`](#enum-enemy_type).
| `noncopyable` | |

</details>


---

### Enum: `type`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-dodamage), [`damage`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-damage), [`damage_instance`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-damage_instance), [`self_damage`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-self_damage), [`splash_damage`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-splash_damage), [`MeleeRevengeDamage`](../Player_Progression_and_Cats/Cat_Mutations.md#object-meleerevengedamage), [`RevengeDamage`](../Player_Progression_and_Cats/Cat_Mutations.md#object-revengedamage), [`MeleeRevengeDamage`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-meleerevengedamage), [`RevengeDamage`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-revengedamage), [`eat_damage`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-eat_damage), [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties), [`DamageNeighborsAfterMove`](../Core_Entities_and_Combat/Elite_Buffs.md#object-damageneighborsaftermove), [`AddAdvantageToEvent`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addadvantagetoevent), [`DoDamage`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-dodamage), [`StatusOnTurnEndIfDidntCastAbilityTypes`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonturnendifdidntcastabilitytypes), [`damage_instance`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-damage_instance), [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root), [`battle`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-battle), [`boss`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-boss), [`event`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-event), [`exit0`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-exit0), [`exit1`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-exit1), [`exit_desert`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-exit_desert), [`exit_lab`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-exit_lab), [`hard_initial`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-hard_initial), [`home`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-home), [`miniboss_event`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-miniboss_event), [`mw_altar`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-mw_altar), [`mw_battle1`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-mw_battle1), [`mw_boss`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-mw_boss), [`mw_earlyhome`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-mw_earlyhome), [`mw_event1`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-mw_event1), [`mw_hard1`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-mw_hard1), [`mw_home`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-mw_home), [`mw_quest_event`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-mw_quest_event), [`mw_treasure`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-mw_treasure), [`quest_event`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-quest_event), [`shop_cheapwater`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-shop_cheapwater), [`shop_water`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-shop_water), [`start`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-start), [`time_machine`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-time_machine), [`treasure`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-treasure), [`weather_event`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-weather_event), [`DamageNeighborsAfterMove`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-damageneighborsaftermove), [`DamageNeighborsOnEndMove`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-damageneighborsonendmove), [`GravityWell`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-gravitywell), [`SelfDamageWhenDealDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-selfdamagewhendealdamage), [`SmiteEnemiesWhoKill`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-smiteenemieswhokill), [`StatusOnTurnEndIfDidntCastAbilityTypes`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonturnendifdidntcastabilitytypes), [`fire`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-fire), [`ice`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-ice), [`lightning`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-lightning), [`triattack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-triattack), [`tracy_special_item`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_special_item)

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

> **Also Used In:** These values are also referenced by [`type_icon`](#enum-type_icon), [`new_layer`](#enum-new_layer).

</details>


---

### Enum: `name`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-meta), [`ROOT` (Boss_Cutscene_Info)](../World_Maps_and_Events/Boss_Cutscene_Info.md#object-root), [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics), [`ROOT` (Furniture_and_Metaprogression)](../World_Maps_and_Events/Furniture_and_Metaprogression.md#object-root), [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

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
| `BOSS_ABANDONEDONES_NAME` | |
| `BOSS_ALIENQUEEN_NAME` | |
| `BOSS_BORIS_NAME` | |
| `BOSS_BUMBLEFOOT_NAME` | |
| `BOSS_BUTCHERCAT_NAME` | |
| `BOSS_CANCREEPER_NAME` | |
| `BOSS_CAVECATFAMILY_NAME` | |
| `BOSS_CERBERUBS_NAME` | |
| `BOSS_CHAOS_NAME` | |
| `BOSS_CHUBSANDNUBS_NAME` | |
| `BOSS_CLERICCAT_NAME` | |
| `BOSS_COVEN_NAME` | |
| `BOSS_DINOCOUPLE_NAME` | |
| `BOSS_DRMANGLER_NAME` | |
| `BOSS_DRUIDCAT_NAME` | |
| `BOSS_DUSTDEVIL_NAME` | |
| `BOSS_DYBBUK_NAME` | |
| `BOSS_ERROR_MINIBOSS_NAME` | |
| `BOSS_ERROR_NAME` | |
| `BOSS_FIGHTERCAT_NAME` | |
| `BOSS_FLUSHMASTER_NAME` | |
| `BOSS_GAMBIT_NAME` | |
| `BOSS_GUILLOTINA_1_NAME` | |
| `BOSS_GUILLOTINA_2_NAME` | |
| `BOSS_GUILLOTINA_3_NAME` | |
| `BOSS_HITLER_NAME` | |
| `BOSS_HUNTERCAT_NAME` | |
| `BOSS_ICEELEMENTAL_NAME` | |
| `BOSS_INFESTEDDUO_NAME` | |
| `BOSS_JESTERCAT_NAME` | |
| `BOSS_JOHNNY_NAME` | |
| `BOSS_LENNY_NAME` | |
| `BOSS_LIGHTNINGELEMENTAL_NAME` | |
| `BOSS_LORDBUNGA_NAME` | |
| `BOSS_MAGECAT_NAME` | |
| `BOSS_MAMAMAGGOT_NAME` | |
| `BOSS_MEGADINO_NAME` | |
| `BOSS_MONKCAT_NAME` | |
| `BOSS_MOONHEAD_NAME` | |
| `BOSS_NECROCAT_NAME` | |
| `BOSS_PEBBLES_NAME` | |
| `BOSS_PSYCHICCAT_NAME` | |
| `BOSS_PYROPHINA_NAME` | |
| `BOSS_PYROPHINA_VS_ZARATANA_NAME` | |
| `BOSS_QUEENHIPPO_NAME` | |
| `BOSS_RADICALRAT_NAME` | |
| `BOSS_RATKING_NAME` | |
| `BOSS_ROCKYBOBO_NAME` | |
| `BOSS_SLIME_NAME` | |
| `BOSS_SPEWER_NAME` | |
| `BOSS_SPIDERKITTEN_NAME` | |
| `BOSS_SPIDERQUEEN_NAME` | |
| `BOSS_STACY_NAME` | |
| `BOSS_TANKCAT_NAME` | |
| `BOSS_TERMINATOR_1_NAME` | |
| `BOSS_TERMINATOR_2_NAME` | |
| `BOSS_TERMINATOR_3_NAME` | |
| `BOSS_THEBLOAT_NAME` | |
| `BOSS_THECREATOR_NAME` | |
| `BOSS_THEMOTHER_NAME` | |
| `BOSS_THIEFCAT_NAME` | |
| `BOSS_THROBBINGKING_NAME` | |
| `BOSS_TINKERERCAT_NAME` | |
| `BOSS_TRAMPY_NAME` | |
| `BOSS_ZARATANA_NAME` | |
| `BOSS_ZODIAC_NAME` | |
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

### Enum: `desc`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `301`, `306`, `307`, `309`, `310`, `311`, `313`, `314`, `315`, `900`, [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics), [`ROOT` (Furniture_and_Metaprogression)](../World_Maps_and_Events/Furniture_and_Metaprogression.md#object-root), [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

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

### Enum: `movieclip`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics), [`Floor1_Large`](../World_Maps_and_Events/House_and_Environment.md#object-floor1_large), [`Floor1_Small`](../World_Maps_and_Events/House_and_Environment.md#object-floor1_small), [`ROOT` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-root), [`SmallAttic`](../World_Maps_and_Events/House_and_Environment.md#object-smallattic), `ROOT`, `ROOT`, [`meta`](../World_Maps_and_Events/Shops.md#object-meta)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `_CAT` | |
| `ParticleTestNoRandom` | |
| `TreasureRoom` | |
| `RainParticle` | |
| `RainSplashParticle` | |
| `Shop` | |
| `Particle_BurnFlame` | |
| `Particle_InvertShards` | |
| `ParticleBlood` | |
| `ParticleSmoke1` | |
| `ParticleDrop` | |
| `ParticleFire2` | |
| `ParticleFire3` | |
| `Particle_HeatWaveDistortion` | |
| `SparkleParticle` | |
| `ArmorPickup` | |
| `FX_Ember` | |
| `Gibs_Default` | |
| `ManaPickup` | |
| `ParticleFire1` | |
| `ParticleFire4` | |
| `ParticleSpatter` | |
| `ParticleStinkCloudSlow` | |
| `Particle_GravityHoverRing` | |
| `Particle_WindLeaf` | |
| `PuffNoOutline` | |
| `Pyrophina` | |
| `Shambler` | |
| `Tombstone` | |
| `Zaratana` | |
| `BirdSmall` | |
| `CanCreeper` | |
| `CanCreeperOut` | |
| `Coin` | |
| `Crow` | |
| `FX_MoonRock` | |
| `Fetus` | |
| `FetusGusher` | |
| `FetusNoJar` | |
| `Flea` | |
| `FogParticle` | |
| `Frog` | |
| `LoveBot` | |
| `ManaParticle` | |
| `MegaBlastParticle` | |
| `ParticleDustCloudSlow` | |
| `ParticlePetals` | |
| `ParticleRocks` | |
| `Particle_BloodDrip` | |
| `Particle_WindDebris` | |
| `Particle_WindDust` | |
| `Particle_WindWisps` | |
| `Pooter` | |
| `Reaper` | |
| `Rock` | |
| `SandStormParticle` | |
| `Snake` | |
| `Squirrel` | |
| `TNTCrate` | |
| `TracyOffice` | |
| `Tumor` | |
| `AcidOoze` | |
| `AcidRainParticle` | |
| `AcidRainSplashParticle` | |
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
| `ConfettiParticle` | |
| `ConjoinedHusk` | |
| `CopBot` | |
| `CoreArm` | |
| `CoreFreak` | |
| `CovenCandle` | |
| `Crate` | |
| `CreepBubbleParticle` | |
| `Critter_Fly` | |
| `Cutter` | |
| `DaddyShark` | |
| `DarkFogParticle` | |
| `DeathWorm` | |
| `Deathbot` | |
| `Decoy` | |
| `Decoy2` | |
| `DiggyMaggot` | |
| `DinoEggs` | |
| `Dip` | |
| `DissolveDark` | |
| `DissolveParticle` | |
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
| `Gibs_Bag` | |
| `Gibs_Blob` | |
| `Gibs_Box` | |
| `Gibs_Bugs` | |
| `Gibs_Cactus` | |
| `Gibs_Demon` | |
| `Gibs_Fetus` | |
| `Gibs_Human` | |
| `Gibs_Plant` | |
| `Gibs_Poop` | |
| `Gibs_Rat` | |
| `Gibs_Robot` | |
| `Gibs_Rock` | |
| `Gibs_Undead` | |
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
| `KingBlood1` | |
| `KingBlood2` | |
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
| `ParticleColor` | |
| `ParticleDarkPuff` | |
| `ParticleDirt` | |
| `ParticleDustCloud` | |
| `ParticleFeather` | |
| `ParticleGuilchunk` | |
| `ParticleMusicNotes` | |
| `ParticlePuff` | |
| `ParticleTormentorGib` | |
| `Particle_Electric` | |
| `Particle_PoisonDrip` | |
| `Particle_TarDrip` | |
| `Particle_Thorns` | |
| `Particle_WaterDrip` | |
| `Particle_WindLeafCrater` | |
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
| `RedWaterParticle` | |
| `RedWaterSplashParticle` | |
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
| `ToxicBubbleParticle` | |
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

> **See Also:** Values from [`object`](#enum-object) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`Buddy`](#enum-buddy), [`TransformOnDeath`](#enum-transformondeath), [`Divide4OnDeath`](#enum-divide4ondeath), [`Imprison`](#enum-imprison), [`ObjectOnHit`](#enum-objectonhit), [`ObjectOnHitEmpty`](#enum-objectonhitempty), [`SpawnObjectOnPopCorpse`](#enum-spawnobjectonpopcorpse), [`BreakIntoRocks`](#enum-breakintorocks), [`PopAndSpawn`](#enum-popandspawn), [`TransformWhenBuddyDies`](#enum-transformwhenbuddydies).
| `AlbinoTomTom` | |
| `AllyRotFly` | |
| `AngelicCat` | |
| `AngelicKitten` | |
| `AnimalEgg2` | |
| `AnimatedBoulder` | |
| `AnimatedLavaBoulder` | |
| `AnimatedSmallLavaRock` | |
| `AnimatedSmallRock` | |
| `Ankylosaurus` | |
| `Antidote` | |
| `Astro` | |
| `AstroZombieHead` | |
| `AtomicKitten` | |
| `BabySquirrel` | |
| `Bait` | |
| `BeaniesRat` | |
| `Bear2` | |
| `Beaver` | |
| `BeefyCharmedLeech` | |
| `Belcher` | |
| `BestBud` | |
| `BigCatnip` | |
| `BigFood` | |
| `Bigfoot` | |
| `BiggestFood` | |
| `BigScrap` | |
| `Bird` | |
| `BirdBase` | |
| `BlackBird` | |
| `BlackHole` | |
| `Blessing` | |
| `BoomerCat` | |
| `BoyShade` | |
| `BoyShadeClone` | |
| `BrainDrain` | |
| `BuffCharmedKitten` | |
| `BuffFamiliarFlea` | |
| `BuffFamiliarFly` | |
| `BuffFamiliarMaggot` | |
| `BuffFamiliarPooter` | |
| `BungaWarrior1` | |
| `BungaWarrior2` | |
| `Bunny` | |
| `ButcherCat` | |
| `ButcherCat_Terminator` | |
| `ButchTinkBoris` | |
| `ButtZombie` | |
| `CancerCat` | |
| `CandleBig` | |
| `CandleSmall` | |
| `Catbot` | |
| `CatCaller` | |
| `CatCopyClot` | |
| `CatCultist` | |
| `Catepillar` | |
| `Catnip` | |
| `CaveBaby` | |
| `CaveCatBaby` | |
| `CaveCatDad` | |
| `CaveCatMom` | |
| `CaveMan` | |
| `CaveManNoSpear` | |
| `CaveWoman` | |
| `ChaosStacy` | |
| `CharmedAmoeba` | |
| `CharmedBabyDeathWorm` | |
| `CharmedBear` | |
| `CharmedBigDemon` | |
| `CharmedCancerCat` | |
| `CharmedCaveBaby` | |
| `CharmedChargeyMaggot` | |
| `CharmedClot` | |
| `CharmedCopBot` | |
| `CharmedCultist` | |
| `CharmedDaddyShark` | |
| `CharmedDemonKitten` | |
| `CharmedDip` | |
| `CharmedDoctorBot` | |
| `CharmedDustDevil` | |
| `CharmedFetus` | |
| `CharmedFetus2` | |
| `CharmedFlea` | |
| `CharmedFleaSpecial` | |
| `CharmedFloast` | |
| `CharmedFloater` | |
| `CharmedFly` | |
| `CharmedFlySwarm` | |
| `CharmedFutureBot` | |
| `CharmedGamete` | |
| `CharmedGeoLad` | |
| `CharmedGunCat` | |
| `CharmedHangerBot` | |
| `CharmedHeadTumor` | |
| `CharmedHornyCat` | |
| `CharmedHyde` | |
| `CharmedKitten` | |
| `CharmedLeaper` | |
| `CharmedLeech` | |
| `CharmedLice` | |
| `CharmedLoveBot` | |
| `CharmedMaggot` | |
| `CharmedMammoth` | |
| `CharmedMammothBaby` | |
| `CharmedMangy2` | |
| `CharmedMegaDino` | |
| `CharmedPile` | |
| `CharmedPinky` | |
| `CharmedPooter` | |
| `CharmedRaptorBaby` | |
| `CharmedRat` | |
| `CharmedRattleSnake` | |
| `CharmedReaper` | |
| `CharmedScorpionCat` | |
| `CharmedSecurityBot` | |
| `CharmedSnakeyBones` | |
| `CharmedSoldierBot` | |
| `CharmedSpookie` | |
| `CharmedStacy` | |
| `CharmedSwappyMaggot` | |
| `CharmedTallBot` | |
| `CharmedTarBaby` | |
| `CharmedTinaFly` | |
| `CharmedTinySpider` | |
| `CharmedTinyTumor` | |
| `CharmedTomTom` | |
| `CharmedTumorousMaggot` | |
| `CharmedWhiteRabbit` | |
| `Cherub` | |
| `Cherub_FinalBoss` | |
| `Cherubim` | |
| `Chicken` | |
| `Chupacabra` | |
| `Coin10` | |
| `Coin2` | |
| `Coin3` | |
| `Coin4` | |
| `Coin5` | |
| `Coin6` | |
| `Coin7` | |
| `Coin8` | |
| `Coin9` | |
| `CollectiveCat` | |
| `ColorlessCat_Tutorial` | |
| `CookedBait` | |
| `CookedBigFood` | |
| `CookedBiggestFood` | |
| `CookedChickenLeg` | |
| `CookedFood` | |
| `CookedPoisonBait` | |
| `CookedPoisonFood` | |
| `CookedPurifiedPoisonFood` | |
| `CopBot_Uprising` | |
| `Crate_WithItemChance` | |
| `CraterCreeper` | |
| `CraterCreeperOut` | |
| `Crow2` | |
| `Crow3` | |
| `Cultist` | |
| `CultistBishop` | |
| `CultistMutant` | |
| `CultistWasher` | |
| `CultistZealot` | |
| `CustomEnemyCat` | |
| `cWaggle` | |
| `cWaggle2x2` | |
| `cWaggle3x3` | |
| `Dclaude` | |
| `DeadPinky` | |
| `Death` | |
| `Debug_MegaGuppyPhase3` | |
| `DemonHooker` | |
| `Dice` | |
| `DoctorBot` | |
| `Dog` | |
| `Dove` | |
| `Drcat` | |
| `DruidCat` | |
| `DruidCat_Terminator` | |
| `DruidCrow` | |
| `DruidCrow_Terminator` | |
| `Dummy` | |
| `Dumpster_interactive` | |
| `Eagle` | |
| `Edmund` | |
| `EventBountyHunter` | |
| `ExplodingDecoy` | |
| `FaceGrubFamiliar` | |
| `FamiliarBrainDrain` | |
| `FamiliarChargeyMaggot` | |
| `FamiliarFetus` | |
| `FamiliarFetusGusher` | |
| `FamiliarFleshLad` | |
| `FamiliarKirbyFetus` | |
| `FamiliarMaggot` | |
| `FamiliarPooter` | |
| `FamiliarSwappyMaggot` | |
| `FamiliarTumorousMaggot` | |
| `FastFetus` | |
| `FastRat` | |
| `FatCat` | |
| `FeralZombieKitten` | |
| `FighterCat` | |
| `FighterCat_Terminator` | |
| `FijiMermaid` | |
| `FlamingPoop` | |
| `FoodBase` | |
| `FrankFetus` | |
| `FrankPinky` | |
| `FutureBot` | |
| `Gasper` | |
| `GassyCat` | |
| `GeminiCats` | |
| `GirlShade` | |
| `GlassSpitter` | |
| `GlowingBear` | |
| `GlowingMushroom2` | |
| `GolemCat` | |
| `Gorger` | |
| `Grey` | |
| `GrubFamiliarBase` | |
| `GunCat` | |
| `Harpy` | |
| `HeadGrubFamiliar` | |
| `HellHand` | |
| `Hellspawn` | |
| `HitlerClone` | |
| `HornyCat` | |
| `HummingBird` | |
| `HunterCat` | |
| `HunterCat_Terminator` | |
| `HuskG` | |
| `Hyde` | |
| `IceBlock` | |
| `Infested` | |
| `InfestedDuo` | |
| `Isaac` | |
| `JackCat` | |
| `Jekyll` | |
| `JerseyDevil` | |
| `JesterCat` | |
| `JesterCat_Terminator` | |
| `KirbyFetus` | |
| `Kitten` | |
| `LargeBirdPool` | |
| `LavaBoulder` | |
| `Leaper` | |
| `Lice` | |
| `LoanShark` | |
| `Lumpy` | |
| `MaddenedBear` | |
| `Maelestes` | |
| `MageCat` | |
| `MageCat_Terminator` | |
| `MaggotLord` | |
| `MamaMaggotTina` | |
| `MammothBaby` | |
| `Mangy` | |
| `Mangy2` | |
| `Mangy3` | |
| `MedBirdPool` | |
| `MedCatnip` | |
| `MedicCat` | |
| `MedicCat_Terminator` | |
| `MedScrap` | |
| `MegaGuppy` | |
| `MiniNuke` | |
| `MonkCat` | |
| `MonkCat_Terminator` | |
| `MotherTumorBig` | |
| `Mothman` | |
| `Mutant` | |
| `NeckGrubFamiliar` | |
| `NecroCat` | |
| `NecroCat_Terminator` | |
| `Needlecat` | |
| `Nessie` | |
| `NeutralToad` | |
| `NeutralTwister` | |
| `NeutralZombieKitten` | |
| `NoHead` | |
| `NonChampionFlySwarm` | |
| `NurseBot` | |
| `OrganZodiac` | |
| `Parasaurolophus` | |
| `Pebbles_Terminator` | |
| `PhantomMaskRock` | |
| `Phylactery` | |
| `PickupBase` | |
| `Pig` | |
| `Pigeon` | |
| `PlayerCat` | |
| `PlayerCat_AncestralShade` | |
| `PlayerCat_CambionMiniMe` | |
| `PlayerCat_ClotClone` | |
| `PlayerCat_FinalBossClone` | |
| `PlayerCat_FinalBossClone_Champion` | |
| `PlayerCat_FinalBossClone_Elite` | |
| `PlayerCat_FleshGolem` | |
| `PlayerCat_HuskShade` | |
| `PlayerCat_MachineClone` | |
| `PlayerCat_MiniMe` | |
| `PlayerCat_MiniMiniMe` | |
| `PlayerCat_MonkMiniMe` | |
| `PlayerCat_MonkShade` | |
| `PlayerCat_NecroShade` | |
| `PlayerCat_Shade` | |
| `PlayerCat_StevenShade` | |
| `PlayerCat_ThiefShade` | |
| `PlayerCat_ThiefShade2` | |
| `PoisonBait` | |
| `PoisonFood` | |
| `PoisonFrog` | |
| `PoopCat` | |
| `PopeyeCat` | |
| `Porcupine` | |
| `PrehistoricPooter` | |
| `PsychicCat` | |
| `PsychicCat_Terminator` | |
| `PunchingBag` | |
| `PurifiedPoisonFood` | |
| `PyrophinaFamiliar` | |
| `PyrophinaVS` | |
| `RandomArmorPickup` | |
| `RandomBiggerArmorPickup` | |
| `RandomBiggerCatnipPickup` | |
| `RandomBiggerFoodPickup` | |
| `RandomBiggerPickup` | |
| `RandomBiggestPickup` | |
| `RandomCatnipPickup` | |
| `RandomDruidFamiliar` | |
| `RandomFoodPickup` | |
| `RandomLivingPoop` | |
| `RandomNonCoinPickup` | |
| `RandomPickup` | |
| `Raptor` | |
| `RaptorBaby` | |
| `RatKing_Old` | |
| `RattleSnake` | |
| `Raven` | |
| `RiftKitten` | |
| `RoboTom` | |
| `RoboVacuum` | |
| `RoboVacuum2` | |
| `RocketTurret` | |
| `RockHead` | |
| `RotFly` | |
| `Rover` | |
| `RubberFistBot` | |
| `SabertoothCat` | |
| `SabertoothCub` | |
| `ScorpionCat` | |
| `Scrap` | |
| `Seagull` | |
| `SeducedBoulder` | |
| `Seraphim` | |
| `ShadeCat` | |
| `ShadowCat` | |
| `SharkyCat` | |
| `SimonFlopper` | |
| `Siren` | |
| `SkeletonCat` | |
| `SkeletonCatCorpse` | |
| `SkeletonCatCorpseFamiliar` | |
| `SkeletonCatFamiliar` | |
| `SkeletonCatRevived` | |
| `SkeletonCatRevivedFamiliar` | |
| `SkeletonShambler` | |
| `SkeletonShamblerCorpse` | |
| `SkeletonShamblerRevived` | |
| `Skinned` | |
| `SkullOoze` | |
| `Skunk` | |
| `SleepParalysisDemon` | |
| `Slenderman` | |
| `SlotMachineJackpotCoinsReward` | |
| `SlotMachineNormalPickupReward` | |
| `SmallBirdPool` | |
| `SmallLavaRock` | |
| `Snake2` | |
| `Sonichu` | |
| `SpearGuy` | |
| `SpewerPill_Fire` | |
| `SpewerPill_Normal` | |
| `SpewerPill_Tar` | |
| `SpewerPillTubeL` | |
| `SpewerPillTubeR` | |
| `SpiderCat` | |
| `SpikedCat` | |
| `SpikyCactus_2x2` | |
| `SpikyCactus_Tall` | |
| `Stacy2p0` | |
| `StacyMutant` | |
| `Static1x1A` | |
| `Static1x1B` | |
| `Static1x1C` | |
| `Static2x2A` | |
| `Static2x2B` | |
| `static_object_template` | |
| `StaticTallA` | |
| `StaticTallB` | |
| `SteelFly` | |
| `StemCat` | |
| `StemCat_HalfHealth` | |
| `SwappyMaggot` | |
| `T3Hitler` | |
| `TallRobes` | |
| `TallSkeletonCat` | |
| `TallSkeletonCatCorpse` | |
| `TallSkeletonCatRevived` | |
| `TallSpiderCat` | |
| `TankCat` | |
| `TankCat_Terminator` | |
| `TCMechSuit` | |
| `Terminator1` | |
| `Terminator2` | |
| `Test2x2` | |
| `TheChild` | |
| `TheCreator` | |
| `TheDestroyer` | |
| `TheDestroyer2` | |
| `TheIntruder` | |
| `TheLost` | |
| `ThiefCat` | |
| `ThiefCat_Terminator` | |
| `TinkererCat` | |
| `TinkererCat_Terminator` | |
| `TinkererTurret` | |
| `TinySpider` | |
| `TinyTumor` | |
| `Tire_Up` | |
| `Toad` | |
| `Toad2` | |
| `Toadie` | |
| `Toadie_Hidden` | |
| `Tombstone_Ghost` | |
| `Tombstone_ManaIdol` | |
| `Tombstone_Zombie` | |
| `TomTom` | |
| `TracyFetus` | |
| `TumorCat` | |
| `TumorousMaggot` | |
| `Turkey` | |
| `TVBot` | |
| `Tyler` | |
| `WallOfCats_Eye` | |
| `WallOfCats_Mouth` | |
| `WallOfCats_Wall` | |
| `WaterKitten` | |
| `WereMan` | |
| `WhiteRabbit` | |
| `WolfCat` | |
| `Yeticat` | |
| `ZaratanaFamiliar` | |
| `ZaratanaVS` | |
| `ZombieCat` | |
| `ZombieCatFamiliar` | |

</details>


---

### Enum: `ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AutocastEachRound`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-autocasteachround), [`BackflipWhenTargeted`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-backflipwhentargeted), [`BodyGuard`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bodyguard), [`ChanceToBreakFree`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-chancetobreakfree), [`ConjureBonusAbility`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conjurebonusability), [`DelayCastAbility`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-delaycastability), [`ForceImmediateMoveAndAttack`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-forceimmediatemoveandattack), [`ForceMoveTowardsTaggedObject`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-forcemovetowardstaggedobject), [`ReplaceSpell`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-replacespell), [`TeamCastAbility`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-teamcastability), [`UseAbility`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-useability), [`UseMoveAbilityWithAI`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-usemoveabilitywithai), [`AbilityWhenTaggedCharacterMovesNear`](../Player_Progression_and_Cats/Cat_Mutations.md#object-abilitywhentaggedcharactermovesnear), [`BackflipWhenTargeted`](../Player_Progression_and_Cats/Cat_Mutations.md#object-backflipwhentargeted), [`ChanceToBackflip`](../Player_Progression_and_Cats/Cat_Mutations.md#object-chancetobackflip), [`CounterAttack`](../Player_Progression_and_Cats/Cat_Mutations.md#object-counterattack), [`AbilityHealthThreshold`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-abilityhealththreshold), [`AbilityOnRoundEnd`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-abilityonroundend), [`AbilityReaction`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-abilityreaction), [`AbilityWhenTaggedCharacterMovesNear`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-abilitywhentaggedcharactermovesnear), [`AutocastEachRound`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-autocasteachround), [`BackflipWhenTargeted`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-backflipwhentargeted), [`BungaEntrance`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-bungaentrance), [`CaveFamilyEnrage`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cavefamilyenrage), [`CerberubsJumpBlind`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cerberubsjumpblind), [`CerberubsJumpNormal`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cerberubsjumpnormal), [`ChanceToBackflip`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-chancetobackflip), [`ChanceToSpitOnDamage`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-chancetospitondamage), [`ChaosHeadDropIn`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-chaosheaddropin), [`CloseConvert`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-closeconvert), [`CounterAttack`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-counterattack), [`DashRandomly`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-dashrandomly), [`DeathRattle`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-deathrattle), [`DeathRattleRevive`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-deathrattlerevive), [`DodgeWhenTargeted`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-dodgewhentargeted), [`Escape`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-escape), [`FoodMove`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-foodmove), [`ForceTrample`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-forcetrample), [`ForceUseAbility`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-forceuseability), [`HitlerExecute`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-hitlerexecute), [`ImmediateAbilityReaction`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-immediateabilityreaction), [`LeapClose`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-leapclose), [`MoveAway`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveaway), [`MoveCenter`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movecenter), [`MoveClose`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveclose), [`MoveForBarrage`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveforbarrage), [`MoveForDash`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movefordash), [`MoveForGrass`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveforgrass), [`MoveForPounce`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveforpounce), [`MoveForSpin`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveforspin), [`MoveForThrow`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveforthrow), [`MoveOneForPuke`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveoneforpuke), [`MoveSpaced`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movespaced), [`MoveToHead`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movetohead), [`MoveTowards`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movetowards), [`MoveTowardsDamageSource`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movetowardsdamagesource), [`MovementReaction`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movementreaction), [`NCGravecrawlFAR`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-ncgravecrawlfar), [`ProtectTargetedAllies`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-protecttargetedallies), [`ReturnA`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-returna), [`RunFar`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-runfar), [`SecurityBotProtect`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-securitybotprotect), [`SpearRun`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-spearrun), [`SuckMF`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-suckmf), [`SupportFormChangeInsteadOfRun`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-supportformchangeinsteadofrun), [`TF_TargetAllies`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-tf_targetallies), [`TF_TargetEnemies`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-tf_targetenemies), [`TerminatorChase`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-terminatorchase), [`Trapper`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-trapper), [`Unflip`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-unflip), [`UnlimitedDeathRattleRevive`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-unlimiteddeathrattlerevive), [`UseAbility`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-useability), [`UseAbilityWhenOutOfStatus`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-useabilitywhenoutofstatus), [`AbilityHealthThreshold`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-abilityhealththreshold), [`AbilityOnRoundEndOnce`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-abilityonroundendonce), [`AutocastEachRound`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-autocasteachround), [`BackflipWhenTargeted`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-backflipwhentargeted), [`ChanceToBackflip`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-chancetobackflip), [`CounterAttack`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-counterattack), `DeathRattle`, [`ForceUseAbilityOnTarget`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-forceuseabilityontarget), [`ImmediateUseAbility`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-immediateuseability), [`MovementReaction`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-movementreaction), [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root), [`AbilityReaction`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-abilityreaction), [`AbilityWhenTaggedCharacterMovesNear`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-abilitywhentaggedcharactermovesnear), [`AllyBonusAbilityAura`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-allybonusabilityaura), [`AutocastEachRound`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-autocasteachround), [`AutocastEachTurnBegin`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-autocasteachturnbegin), [`CatAPultAnimation`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catapultanimation), [`ChanceToBackflip`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-chancetobackflip), [`DamageIfDidntUseSpecificAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-damageifdidntusespecificability), [`DeathRattle`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-deathrattle), [`ForceUseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-forceuseability), [`MovementReaction`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-movementreaction), [`SecurityBotProtect`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-securitybotprotect)

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

> **Also Used In:** These values are also referenced by [`ConjureBonusAbility`](#enum-conjurebonusability), [`DisplayDangerAOE`](#enum-displaydangeraoe), [`AllyMoveAbilityAura`](#enum-allymoveabilityaura).

</details>


---

### Enum: `brain`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ReplaceBrain`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-replacebrain), [`ai`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-ai), [`ai_if_spawned_as_enemy`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-ai_if_spawned_as_enemy), [`ReplaceBrain`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-replacebrain)

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

> **Referenced by:** [`damage_instance`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-damage_instance), [`spawn`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-spawn), [`SpawnOnDeath`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-spawnondeath), [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties), [`AllyInfested`](../World_Maps_and_Events/House_and_Environment.md#object-allyinfested), [`SpawnOnDeath`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-spawnondeath)

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

### Enum: `move_weights`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`UseMoveAbilityWithAI`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-usemoveabilitywithai), [`CloseConvert`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-closeconvert), [`Escape`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-escape), [`FoodMove`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-foodmove), [`LeapClose`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-leapclose), [`MoveAway`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveaway), [`MoveCenter`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movecenter), [`MoveClose`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveclose), [`MoveForBarrage`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveforbarrage), [`MoveForDash`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movefordash), [`MoveForGrass`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveforgrass), [`MoveForPounce`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveforpounce), [`MoveForSpin`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveforspin), [`MoveForThrow`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveforthrow), [`MoveOneForPuke`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveoneforpuke), [`MoveSpaced`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movespaced), [`MoveToHead`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movetohead), [`MoveTowards`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movetowards), [`NCGravecrawlFAR`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-ncgravecrawlfar), [`ReplaceBrain`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-replacebrain), [`ReturnA`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-returna), [`RunFar`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-runfar), [`SpearRun`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-spearrun), [`SuckMF`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-suckmf), [`Terminator2Run`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-terminator2run), [`Unflip`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-unflip), [`ai`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-ai), [`ai_if_spawned_as_enemy`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-ai_if_spawned_as_enemy), [`ReplaceBrain`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-replacebrain)

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

> **Also Used In:** These values are also referenced by [`weights`](#enum-weights).

</details>


---

### Enum: `attack`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `705`, `2`, `3`, `4`, `5`, [`Big`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-big), [`Bishop`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-bishop), [`CaveBaby`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cavebaby), [`CaveMan`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-caveman), [`CaveManSpear`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cavemanspear), [`CaveWoman`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cavewoman), [`CaveWomanHasCat`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cavewomanhascat), [`Charging`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-charging), [`Cultist`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cultist), [`Default`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-default), [`Down`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-down), [`DualSword`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-dualsword), [`DualSword_Primed`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-dualsword_primed), [`Explody`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-explody), [`FightPhase`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-fightphase), [`Fire`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-fire), [`FireFull`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-firefull), [`Full`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-full), [`Grown`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-grown), [`HalfDead`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-halfdead), [`HasCat`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-hascat), [`HasDeadCat`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-hasdeadcat), [`HasRock`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-hasrock), [`HumanDead`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-humandead), [`InitialPhase`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-initialphase), [`Lifted`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-lifted), [`MonkCatReactionAbilities`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-monkcatreactionabilities), [`Mutant`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-mutant), [`NoStick`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-nostick), [`Normal`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-normal), [`NormalFull`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-normalfull), [`Nuke`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-nuke), [`Open`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-open), [`Primed`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-primed), [`Pulp2`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp2), [`Pulp3`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp3), [`Pulp4`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp4), [`Pulp5`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp5), [`Pulp6`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp6), [`Pulp7`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp7), [`Rage`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-rage), [`Sitting`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-sitting), [`Small`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-small), [`SquirrelForm`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-squirrelform), [`Standing`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-standing), [`Standing2`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-standing2), [`SwordAndShield`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-swordandshield), [`SwordAndShield_Primed`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-swordandshield_primed), [`Tar`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-tar), [`TarFull`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-tarfull), [`Turtled`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-turtled), [`Washer`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-washer), [`WereMan`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-wereman), [`Zealot`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-zealot), [`ZealotBomb`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-zealotbomb), [`abilities`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-abilities), [`ai`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-ai), [`passive`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passive), [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

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

> **Also Used In:** These values are also referenced by [`ReplaceBasicAttack`](#enum-replacebasicattack), [`OverrideBasicAttack`](#enum-overridebasicattack), [`ability_icon`](#enum-ability_icon), [`DisplayDangerAOE`](#enum-displaydangeraoe).

</details>


---

### Enum: `decision_weights`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CerberubsJumpBlind`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cerberubsjumpblind), [`CerberubsJumpNormal`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cerberubsjumpnormal), [`DashRandomly`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-dashrandomly), [`ForceTrample`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-forcetrample), [`ReplaceBrain`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-replacebrain), [`SuckMF`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-suckmf), [`TF_TargetAllies`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-tf_targetallies), [`TF_TargetEnemies`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-tf_targetenemies), [`ai`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-ai), [`ai_if_spawned_as_enemy`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-ai_if_spawned_as_enemy), [`ReplaceBrain`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-replacebrain)

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

### Enum: `target_mode`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

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

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics), [`FormChangeOnElementInfluence`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangeonelementinfluence), [`spell_graphics_override`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spell_graphics_override)

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

> **Also Used In:** These values are also referenced by [`affected_particle`](#enum-affected_particle), [`VisualFXTile`](#enum-visualfxtile), [`tooltip_stackless`](#enum-tooltip_stackless), [`center_particle`](#enum-center_particle), [`area_particle`](#enum-area_particle), [`VisualFX`](#enum-visualfx).

</details>


---

### Enum: `move`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Default`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-default), [`Down`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-down), [`Explody`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-explody), [`FightPhase`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-fightphase), [`HasCat`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-hascat), [`InitialPhase`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-initialphase), [`Lifted`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-lifted), [`MonkCatReactionAbilities`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-monkcatreactionabilities), [`Nuke`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-nuke), [`Pulp2`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp2), [`Pulp3`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp3), [`Pulp4`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp4), [`Pulp5`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp5), [`Pulp6`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp6), [`Pulp7`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp7), [`SecurityBotProtect`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-securitybotprotect), [`Sitting`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-sitting), [`Standing`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-standing), [`Standing2`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-standing2), [`TerminatorChase`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-terminatorchase), [`Turtled`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-turtled), [`abilities`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-abilities), [`SecurityBotProtect`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-securitybotprotect)

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

> **Also Used In:** These values are also referenced by [`GroundFlopper`](#enum-groundflopper), [`MoveAwayFromDamageSource`](#enum-moveawayfromdamagesource).

</details>


---

### Enum: `aoe_mode`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

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

> **Also Used In:** These values are also referenced by [`range_mode`](#enum-range_mode).

</details>


---

### Enum: `prompt`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](../World_Maps_and_Events/Events_and_Encounters.md#object-bad), [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`else`](../World_Maps_and_Events/Events_and_Encounters.md#object-else), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`main`](../World_Maps_and_Events/Events_and_Encounters.md#object-main), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward), [`popup`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-popup)

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

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

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

| `exclude_blocking` | |
| `must_be_adjacent_to_ally` | |
| `must_move` | |
| `must_not_have_corpse` | |
| `must_not_have_tag` | |
| `target_requires_element` | |
| `must_have_element` | |
| `must_have_enemy_or_robot` | |
| `must_have_player_cat` | |
| `must_be_partially_empty` | |

</details>


---

### Enum: `knockback_mode`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

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

### Enum: `stat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `10coins`, `5coins`, [`ROOT` (Events_and_Encounters)](../World_Maps_and_Events/Events_and_Encounters.md#object-root), [`a`](../World_Maps_and_Events/Events_and_Encounters.md#object-a), [`activate_p`](../World_Maps_and_Events/Events_and_Encounters.md#object-activate_p), [`activate_z`](../World_Maps_and_Events/Events_and_Encounters.md#object-activate_z), [`altar_sacrifice`](../World_Maps_and_Events/Events_and_Encounters.md#object-altar_sacrifice), [`attach_amplifier`](../World_Maps_and_Events/Events_and_Encounters.md#object-attach_amplifier), [`attach_antenna`](../World_Maps_and_Events/Events_and_Encounters.md#object-attach_antenna), [`attach_leech`](../World_Maps_and_Events/Events_and_Encounters.md#object-attach_leech), [`b`](../World_Maps_and_Events/Events_and_Encounters.md#object-b), [`blue`](../World_Maps_and_Events/Events_and_Encounters.md#object-blue), [`body`](../World_Maps_and_Events/Events_and_Encounters.md#object-body), [`boogers`](../World_Maps_and_Events/Events_and_Encounters.md#object-boogers), [`book`](../World_Maps_and_Events/Events_and_Encounters.md#object-book), [`brace`](../World_Maps_and_Events/Events_and_Encounters.md#object-brace), [`button`](../World_Maps_and_Events/Events_and_Encounters.md#object-button), [`buy1`](../World_Maps_and_Events/Events_and_Encounters.md#object-buy1), [`c`](../World_Maps_and_Events/Events_and_Encounters.md#object-c), [`chaos_ending`](../World_Maps_and_Events/Events_and_Encounters.md#object-chaos_ending), [`chapter_cutscene`](../World_Maps_and_Events/Events_and_Encounters.md#object-chapter_cutscene), [`counter`](../World_Maps_and_Events/Events_and_Encounters.md#object-counter), [`d`](../World_Maps_and_Events/Events_and_Encounters.md#object-d), [`damage`](../World_Maps_and_Events/Events_and_Encounters.md#object-damage), [`desert_cutscene`](../World_Maps_and_Events/Events_and_Encounters.md#object-desert_cutscene), [`donate`](../World_Maps_and_Events/Events_and_Encounters.md#object-donate), [`donate_10`](../World_Maps_and_Events/Events_and_Encounters.md#object-donate_10), [`donate_15`](../World_Maps_and_Events/Events_and_Encounters.md#object-donate_15), [`donate_20`](../World_Maps_and_Events/Events_and_Encounters.md#object-donate_20), [`donate_5`](../World_Maps_and_Events/Events_and_Encounters.md#object-donate_5), [`double`](../World_Maps_and_Events/Events_and_Encounters.md#object-double), [`enter`](../World_Maps_and_Events/Events_and_Encounters.md#object-enter), [`fiddle`](../World_Maps_and_Events/Events_and_Encounters.md#object-fiddle), [`fill_jar`](../World_Maps_and_Events/Events_and_Encounters.md#object-fill_jar), [`find`](../World_Maps_and_Events/Events_and_Encounters.md#object-find), [`fire`](../World_Maps_and_Events/Events_and_Encounters.md#object-fire), [`future`](../World_Maps_and_Events/Events_and_Encounters.md#object-future), [`go_around`](../World_Maps_and_Events/Events_and_Encounters.md#object-go_around), [`holy`](../World_Maps_and_Events/Events_and_Encounters.md#object-holy), [`home`](../World_Maps_and_Events/Events_and_Encounters.md#object-home), [`hp`](../World_Maps_and_Events/Events_and_Encounters.md#object-hp), [`ice`](../World_Maps_and_Events/Events_and_Encounters.md#object-ice), [`ignore`](../World_Maps_and_Events/Events_and_Encounters.md#object-ignore), [`infinite`](../World_Maps_and_Events/Events_and_Encounters.md#object-infinite), [`intimidation`](../World_Maps_and_Events/Events_and_Encounters.md#object-intimidation), [`itchies`](../World_Maps_and_Events/Events_and_Encounters.md#object-itchies), [`knife`](../World_Maps_and_Events/Events_and_Encounters.md#object-knife), [`leave`](../World_Maps_and_Events/Events_and_Encounters.md#object-leave), [`leave_it_in`](../World_Maps_and_Events/Events_and_Encounters.md#object-leave_it_in), [`lever`](../World_Maps_and_Events/Events_and_Encounters.md#object-lever), [`lick`](../World_Maps_and_Events/Events_and_Encounters.md#object-lick), [`lightning`](../World_Maps_and_Events/Events_and_Encounters.md#object-lightning), [`looks`](../World_Maps_and_Events/Events_and_Encounters.md#object-looks), [`loot_heart`](../World_Maps_and_Events/Events_and_Encounters.md#object-loot_heart), [`makeup`](../World_Maps_and_Events/Events_and_Encounters.md#object-makeup), [`mind`](../World_Maps_and_Events/Events_and_Encounters.md#object-mind), [`nothanks`](../World_Maps_and_Events/Events_and_Encounters.md#object-nothanks), [`past`](../World_Maps_and_Events/Events_and_Encounters.md#object-past), [`pirouette`](../World_Maps_and_Events/Events_and_Encounters.md#object-pirouette), [`place_gristle`](../World_Maps_and_Events/Events_and_Encounters.md#object-place_gristle), [`poop`](../World_Maps_and_Events/Events_and_Encounters.md#object-poop), [`power`](../World_Maps_and_Events/Events_and_Encounters.md#object-power), [`protection`](../World_Maps_and_Events/Events_and_Encounters.md#object-protection), [`pull_it_out`](../World_Maps_and_Events/Events_and_Encounters.md#object-pull_it_out), [`put_in_coins`](../World_Maps_and_Events/Events_and_Encounters.md#object-put_in_coins), [`receive`](../World_Maps_and_Events/Events_and_Encounters.md#object-receive), [`red`](../World_Maps_and_Events/Events_and_Encounters.md#object-red), [`reflect`](../World_Maps_and_Events/Events_and_Encounters.md#object-reflect), [`repair`](../World_Maps_and_Events/Events_and_Encounters.md#object-repair), [`repair_quest`](../World_Maps_and_Events/Events_and_Encounters.md#object-repair_quest), [`sacrifice`](../World_Maps_and_Events/Events_and_Encounters.md#object-sacrifice), [`sacrifice_full_favor`](../World_Maps_and_Events/Events_and_Encounters.md#object-sacrifice_full_favor), [`sacrifice_partial_favor`](../World_Maps_and_Events/Events_and_Encounters.md#object-sacrifice_partial_favor), [`sacrifice_quest`](../World_Maps_and_Events/Events_and_Encounters.md#object-sacrifice_quest), [`scream`](../World_Maps_and_Events/Events_and_Encounters.md#object-scream), [`skip`](../World_Maps_and_Events/Events_and_Encounters.md#object-skip), [`smash`](../World_Maps_and_Events/Events_and_Encounters.md#object-smash), [`soul`](../World_Maps_and_Events/Events_and_Encounters.md#object-soul), [`speed`](../World_Maps_and_Events/Events_and_Encounters.md#object-speed), [`surprise`](../World_Maps_and_Events/Events_and_Encounters.md#object-surprise), [`take_blood`](../World_Maps_and_Events/Events_and_Encounters.md#object-take_blood), [`tappytoes`](../World_Maps_and_Events/Events_and_Encounters.md#object-tappytoes), [`thorns`](../World_Maps_and_Events/Events_and_Encounters.md#object-thorns), [`timemachine`](../World_Maps_and_Events/Events_and_Encounters.md#object-timemachine), [`touch`](../World_Maps_and_Events/Events_and_Encounters.md#object-touch), [`w1`](../World_Maps_and_Events/Events_and_Encounters.md#object-w1), [`w2`](../World_Maps_and_Events/Events_and_Encounters.md#object-w2), [`w3`](../World_Maps_and_Events/Events_and_Encounters.md#object-w3), [`w4`](../World_Maps_and_Events/Events_and_Encounters.md#object-w4), [`w5`](../World_Maps_and_Events/Events_and_Encounters.md#object-w5), [`w6`](../World_Maps_and_Events/Events_and_Encounters.md#object-w6), [`wealth`](../World_Maps_and_Events/Events_and_Encounters.md#object-wealth), [`wheezies`](../World_Maps_and_Events/Events_and_Encounters.md#object-wheezies), [`wish_genes`](../World_Maps_and_Events/Events_and_Encounters.md#object-wish_genes), [`wish_items`](../World_Maps_and_Events/Events_and_Encounters.md#object-wish_items), [`wish_levelups`](../World_Maps_and_Events/Events_and_Encounters.md#object-wish_levelups), [`wish_strength`](../World_Maps_and_Events/Events_and_Encounters.md#object-wish_strength)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `none` | |
| `quest` | |
| `coins` | |

</details>


---

### Enum: `projectile`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

> **Also Used In:** These values are also referenced by [`ObjectOnHitEmpty`](#enum-objectonhitempty), [`SpawnCustomTrap`](#enum-spawncustomtrap).

</details>


---

### Enum: `cat_choice`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`intro`](../World_Maps_and_Events/Events_and_Encounters.md#object-intro)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `random` | |

</details>


---

### Enum: `event_clip`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`intro`](../World_Maps_and_Events/Events_and_Encounters.md#object-intro)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `NonWheelEvent` | |

</details>


---

### Enum: `subject_clip`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`intro`](../World_Maps_and_Events/Events_and_Encounters.md#object-intro)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `EventSubject` | |

</details>


---

### Enum: `subject_frame`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`intro`](../World_Maps_and_Events/Events_and_Encounters.md#object-intro)

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

> **Also Used In:** These values are also referenced by [`unlock_npc_tomorrow`](#enum-unlock_npc_tomorrow), [`requires_unlocked_npc`](#enum-requires_unlocked_npc).

</details>


---

### Enum: `voice`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Custom_Cats)](../Player_Progression_and_Cats/Custom_Cats.md#object-root)

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

> **Referenced by:** [`bonusturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-bonusturn_pattern), [`dispersed_bonusturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-dispersed_bonusturn_pattern), [`fallback`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-fallback), [`mainturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-mainturn_pattern), [`pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pattern), [`round_end_bonusturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-round_end_bonusturn_pattern)

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

> **Also Used In:** These values are also referenced by [`DisplayDangerAOE`](#enum-displaydangeraoe).

> **See Also:** The [`spells`](#enum-spells) enum is the full master list of all known ability IDs. The values here are a confirmed subset of it.

</details>


---

### Enum: `get_item_from_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `10coins`, `5coins`, [`ROOT` (Events_and_Encounters)](../World_Maps_and_Events/Events_and_Encounters.md#object-root), [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`options`](../World_Maps_and_Events/Events_and_Encounters.md#object-options), [`random_chance`](../World_Maps_and_Events/Events_and_Encounters.md#object-random_chance), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `consumables` | |
| `chapter_rare` | |
| `bone_equipment` | |
| `food` | |
| `chapter_common` | |
| `blood_altar_items` | |
| `chapter` | |
| `chapter_specific_item` | |
| `fleshhead_items` | |
| `junkyard_items` | |
| `poop_items` | |
| `treasure_easy` | |
| `bone_armor` | |
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
| `current_chapter_common` | |
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

> **Also Used In:** These values are also referenced by [`select_item_from_pool_for_cutscene_only`](#enum-select_item_from_pool_for_cutscene_only).

</details>


---

### Enum: `frame`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`popup`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-popup)

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

### Enum: `render_mode`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `separate` | |
| `default` | |

</details>


---

### Enum: `simulation_space`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `global` | |

</details>


---

### Enum: `projection_matrix`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `default` | |

</details>


---

### Enum: `aoe_restrictions`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

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

> **Referenced by:** [`Conditional_HasStatus`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_hasstatus), [`Conditional_SourceHasStatus`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_sourcehasstatus), [`RemoveStatusStacks`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-removestatusstacks), [`TempPassiveWhileHasStatus`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-temppassivewhilehasstatus), [`Temporary`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-temporary), [`PassiveWhileHasStatus`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passivewhilehasstatus), [`FormChangeWhileHasStatus`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangewhilehasstatus), [`PassiveWhileHasStatus`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passivewhilehasstatus), [`PassiveWhileNotHasStatus`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passivewhilenothasstatus), [`RemoveStatusStacks`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-removestatusstacks), [`StatusEachTurnBeginIfHasStatus`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statuseachturnbeginifhasstatus), [`StatusWhenStatusCompletelyRemoved`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statuswhenstatuscompletelyremoved), [`TerminatorSkin`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-terminatorskin), [`TransformOnStatusThreshold`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-transformonstatusthreshold), [`UseAbilityWhenOutOfStatus`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-useabilitywhenoutofstatus), [`Conditional_HasStatus`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_hasstatus), [`RemoveStatusStacks`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-removestatusstacks), [`Temporary`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-temporary), [`AmplifyStatus`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-amplifystatus), [`Conditional_HasStatus`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_hasstatus), [`Temporary`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-temporary)

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

> **Also Used In:** These values are also referenced by [`RemoveStatus`](#enum-removestatus), [`StatusImmunity`](#enum-statusimmunity), [`AmplifyStatus`](#enum-amplifystatus), [`DoubleStatus`](#enum-doublestatus), [`AbilityEnabledIfHasStatus`](#enum-abilityenabledifhasstatus).

</details>


---

### Enum: `custom_cat_data`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

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

> **See Also:** Values from [`object`](#enum-object) may also be valid here (overlapping enum).

</details>


---

### Enum: `unlock_item_immediate`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

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

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

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

> **See Also:** Values from [`aoe_mode`](#enum-aoe_mode) may also be valid here (overlapping enum).

</details>


---

### Enum: `pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Craft`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-craft), [`DestroyEquipmentAndAttachParasite`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-destroyequipmentandattachparasite), [`EvolveAbilityFromPool`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-evolveabilityfrompool), [`FindItemFromPool`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-finditemfrompool), [`GainDisorderFromPool`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-gaindisorderfrompool), `ROOT`, [`get_item_from_pool`](../World_Maps_and_Events/Events_and_Encounters.md#object-get_item_from_pool), [`Craft`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-craft), [`Craft`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-craft), [`FindItemFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finditemfrompool), [`RepressedMemoriesMetronome`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-repressedmemoriesmetronome), [`Item`](../World_Maps_and_Events/Shops.md#object-item)

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

> **Also Used In:** These values are also referenced by [`class_anis`](#enum-class_anis), [`MulticlassLevelUp`](#enum-multiclasslevelup), [`ChangeCatClass`](#enum-changecatclass), [`complete_checklist_with_class`](#enum-complete_checklist_with_class), [`EvolveAbilityFromPool`](#enum-evolveabilityfrompool), [`palette`](#enum-palette).

</details>


---

### Enum: `gain_disorder`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`else`](../World_Maps_and_Events/Events_and_Encounters.md#object-else), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Stinky` | |
| `Depression` | |
| `Anxiety` | |
| `Cancer` | |
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
| `CrohnsDisease` | |
| `Dysentery` | |
| `Gastritis` | |
| `IBS` | |

</details>


---

### Enum: `label`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`activate_p`](../World_Maps_and_Events/Events_and_Encounters.md#object-activate_p), [`activate_z`](../World_Maps_and_Events/Events_and_Encounters.md#object-activate_z), [`attach_amplifier`](../World_Maps_and_Events/Events_and_Encounters.md#object-attach_amplifier), [`attach_antenna`](../World_Maps_and_Events/Events_and_Encounters.md#object-attach_antenna), [`attach_leech`](../World_Maps_and_Events/Events_and_Encounters.md#object-attach_leech), [`bite`](../World_Maps_and_Events/Events_and_Encounters.md#object-bite), [`body`](../World_Maps_and_Events/Events_and_Encounters.md#object-body), [`bribe`](../World_Maps_and_Events/Events_and_Encounters.md#object-bribe), [`charm`](../World_Maps_and_Events/Events_and_Encounters.md#object-charm), [`drink`](../World_Maps_and_Events/Events_and_Encounters.md#object-drink), [`eat`](../World_Maps_and_Events/Events_and_Encounters.md#object-eat), [`enter`](../World_Maps_and_Events/Events_and_Encounters.md#object-enter), [`examine`](../World_Maps_and_Events/Events_and_Encounters.md#object-examine), [`fiddle`](../World_Maps_and_Events/Events_and_Encounters.md#object-fiddle), [`fight`](../World_Maps_and_Events/Events_and_Encounters.md#object-fight), [`fill_jar`](../World_Maps_and_Events/Events_and_Encounters.md#object-fill_jar), [`future`](../World_Maps_and_Events/Events_and_Encounters.md#object-future), [`home`](../World_Maps_and_Events/Events_and_Encounters.md#object-home), [`ignore`](../World_Maps_and_Events/Events_and_Encounters.md#object-ignore), [`infinite`](../World_Maps_and_Events/Events_and_Encounters.md#object-infinite), [`lick`](../World_Maps_and_Events/Events_and_Encounters.md#object-lick), [`looks`](../World_Maps_and_Events/Events_and_Encounters.md#object-looks), [`loot`](../World_Maps_and_Events/Events_and_Encounters.md#object-loot), [`loot_heart`](../World_Maps_and_Events/Events_and_Encounters.md#object-loot_heart), [`mind`](../World_Maps_and_Events/Events_and_Encounters.md#object-mind), [`past`](../World_Maps_and_Events/Events_and_Encounters.md#object-past), [`place_gristle`](../World_Maps_and_Events/Events_and_Encounters.md#object-place_gristle), [`power`](../World_Maps_and_Events/Events_and_Encounters.md#object-power), [`repair`](../World_Maps_and_Events/Events_and_Encounters.md#object-repair), [`repair_quest`](../World_Maps_and_Events/Events_and_Encounters.md#object-repair_quest), [`sacrifice_normal`](../World_Maps_and_Events/Events_and_Encounters.md#object-sacrifice_normal), [`sacrifice_quest`](../World_Maps_and_Events/Events_and_Encounters.md#object-sacrifice_quest), [`sneak`](../World_Maps_and_Events/Events_and_Encounters.md#object-sneak), [`soul`](../World_Maps_and_Events/Events_and_Encounters.md#object-soul), [`take_blood`](../World_Maps_and_Events/Events_and_Encounters.md#object-take_blood), [`talk`](../World_Maps_and_Events/Events_and_Encounters.md#object-talk), [`touch`](../World_Maps_and_Events/Events_and_Encounters.md#object-touch), [`wealth`](../World_Maps_and_Events/Events_and_Encounters.md#object-wealth)

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

### Enum: `X_is`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

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

### Enum: `custom_additional_ai_weight`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`damage_instance`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-damage_instance), [`spawn`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-spawn)

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

### Enum: `size`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties), `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `2x2` | |
| `3x3` | |
| `.5` | |
| `1x1` | |
| `.2` | |
| `5x10` | |
| `gemini` | |

</details>


---

### Enum: `water_mask`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

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

> **Referenced by:** [`requirements`](./Miscellaneous.md#object-requirements), [`requirements`](../World_Maps_and_Events/Events_and_Encounters.md#object-requirements)

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
| `WorldEventLegacyCounter_FooCounter` | |
| `WorldEventLegacyToken_Bar` | |
| `WorldEventLegacyToken_CryptOpened` | |
| `WorldEventLegacyToken_HasRunFromDeath` | |
| `WorldEventLegacyToken_MonkeyPaw4` | |
| `WorldEventLegacyToken_StacyMutant` | |
| `mapflag_FutureUnlocked` | |
| `mapflag_IceAgeUnlocked` | |
| `mapflag_JurassicUnlocked` | |
| `mapflag_TheEndUnlocked` | |

> **Also Used In:** These values are also referenced by [`clear_adventure_token`](#enum-clear_adventure_token), [`not_has_token`](#enum-not_has_token), [`save_file_flag`](#enum-save_file_flag).

</details>


---

### Enum: `gain_disorder_from_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](../World_Maps_and_Events/Events_and_Encounters.md#object-bad), [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `all_disorders` | |
| `diseases` | |
| `mental_disorders` | |
| `physical_disorders` | |
| `Steven_disorders` | |
| `Crazy_disorders` | |
| `stomach_disorders` | |

> **Also Used In:** These values are also referenced by [`heal_disorder`](#enum-heal_disorder).

</details>


---

### Enum: `SpawnOnDeath`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`passives`](../Core_Entities_and_Combat/Elite_Buffs.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `RandomArmorPickup` | |
| `Antidote` | |
| `Maggot` | |
| `BiggestFood` | |
| `FrankPinky` | |
| `NonChampionFlySwarm` | |

> **See Also:** Values from [`object`](#enum-object) may also be valid here (overlapping enum).

</details>


---

### Enum: `element`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_AffectedByElement`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_affectedbyelement), [`AddDamageToElementDamage`](../Player_Progression_and_Cats/Cat_Mutations.md#object-adddamagetoelementdamage), [`PassiveWhenAffectedByElement`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passivewhenaffectedbyelement), [`DiesToElement`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-diestoelement), [`FormChangeDuringWeatherElement`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangeduringweatherelement), [`FormChangeOnElementInfluence`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangeonelementinfluence), [`PassiveWhenAffectedByElement`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passivewhenaffectedbyelement), [`TransformOnElementInfluence`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-transformonelementinfluence), [`TransformOnElementInfluencex`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-transformonelementinfluencex), [`AddDamageToElementDamage`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-adddamagetoelementdamage), [`AddStatusToElementDamage`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addstatustoelementdamage), [`PassiveWhenAffectedByElement`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passivewhenaffectedbyelement), [`RefreshEquipmentAbilityOnElement`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-refreshequipmentabilityonelement), [`TransformItemOnElementInfluence`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-transformitemonelementinfluence), [`AddDamageToElementDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-adddamagetoelementdamage), [`AddStatusToElementAbilities`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoelementabilities), [`AddStatusToElementDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoelementdamage), [`ElementalManaCostReduction`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-elementalmanacostreduction), [`PassiveWhenAffectedByElement`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhenaffectedbyelement), [`StatusOnUseElementAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonuseelementability), [`weather_element_alt`](../World_Maps_and_Events/Spawns_and_Enemy_Pools.md#object-weather_element_alt)

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
| `Bloom` | |
| `Break_Web` | |
| `Conducted` | |
| `Dust` | |
| `Earth` | |
| `Explosion` | |
| `Grass` | |
| `HOLY` | |
| `Heat` | |
| `Lesser_Water` | |
| `Metal` | |
| `Mutate` | |
| `Napalm` | |
| `Poison` | |
| `Quake` | |
| `Rock` | |
| `Shadow` | |
| `Spikes` | |
| `Wind` | |
| `dont_break_tentacles` | |

> **Also Used In:** These values are also referenced by [`ElementImmune`](#enum-elementimmune), [`AddElementsToBasicAttack`](#enum-addelementstobasicattack), [`InnateElement`](#enum-innateelement).

</details>


---

### Enum: `move_block`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties)

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

> **Referenced by:** [`bad`](../World_Maps_and_Events/Events_and_Encounters.md#object-bad), [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`else`](../World_Maps_and_Events/Events_and_Encounters.md#object-else), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `random` | |
| `Needles` | |
| `MonkeyPawWish` | |
| `MysteriousCave3` | |
| `MysteriousStranger` | |
| `MysteriousCave2` | |
| `Tragedy` | |
| `ElephantsFootEvenCloser` | |
| `MysteriousCave1` | |
| `MysteriousStrangerForced` | |
| `MysteriousTomb1` | |
| `MysteriousTomb2` | |
| `Pinata` | |
| `Quest_DimensionXPortal` | |
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

> **Also Used In:** These values are also referenced by [`event`](#enum-event), [`next_event_from_set`](#enum-next_event_from_set).

</details>


---

### Enum: `increment_legacy_counter`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`else`](./Miscellaneous.md#object-else), [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `WorldEventLegacyCounter_Jack` | |
| `WorldEventLegacyCounter_ToiletFlushes` | |
| `WorldEventLegacyCounter_CrackInTheWall` | |
| `WorldEventLegacyToken_StartDigging` | |
| `WorldEventLegacyCounter_VolcanoSacrifices` | |
| `WorldEventLegacyCounter_CustomTokenString` | |
| `WorldEventLegacyCounter_FooCounter` | |
| `WorldEventLegacyCounter_SealedCrypt` | |
| `WorldEventLegacyCounter_TestLegacyFoo` | |

> **Also Used In:** These values are also referenced by [`decrement_legacy_counter`](#enum-decrement_legacy_counter).

</details>


---

### Enum: `frame_label`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Boss_Cutscene_Info)](../World_Maps_and_Events/Boss_Cutscene_Info.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bumblefoot` | |
| `error` | |
| `AlienBeast` | |
| `ColorlessCat_Tutorial` | |
| `DrMangler` | |
| `GirlDino` | |
| `LightningElemental` | |
| `MegaDino` | |
| `MoonHead` | |
| `OGSteven` | |
| `RatKing` | |
| `StacyMutant` | |
| `TheBloat` | |
| `TheCoven` | |
| `TheCreator` | |
| `TheMother` | |
| `abandonedones` | |
| `boris` | |
| `butchercat` | |
| `cancreeper` | |
| `cave_family` | |
| `cerberubs` | |
| `chubsandnubs` | |
| `clericcat` | |
| `druidcat` | |
| `dustdevil` | |
| `dybbuk` | |
| `fightercat` | |
| `flushmaster` | |
| `gambit` | |
| `guillotina_1` | |
| `guillotina_2` | |
| `guillotina_3` | |
| `hitler` | |
| `huntercat` | |
| `ice_elemental` | |
| `infestedtwins` | |
| `jestercat` | |
| `johnny` | |
| `lenny` | |
| `lordbunga` | |
| `magecat` | |
| `mamamaggot` | |
| `monkcat` | |
| `necrocat` | |
| `psycat` | |
| `pyrophina` | |
| `pyrophina_vs_zaratana` | |
| `queenHippo` | |
| `radicalrat` | |
| `rockybobo` | |
| `slime` | |
| `spewer` | |
| `spiderkitten` | |
| `spiderqueen` | |
| `tankcat` | |
| `terminator_1` | |
| `terminator_2` | |
| `terminator_3` | |
| `thiefcat` | |
| `throbbingking` | |
| `tinkerercat` | |
| `trampy` | |
| `zaratana` | |
| `zodiac` | |

> **Also Used In:** These values are also referenced by [`beat_house_boss`](#enum-beat_house_boss), [`boss_cutscene`](#enum-boss_cutscene), [`trigger_house_boss`](#enum-trigger_house_boss), [`complete_house_boss`](#enum-complete_house_boss), [`initial_cutscene_night`](#enum-initial_cutscene_night), [`unlock_boss`](#enum-unlock_boss), [`KaijuWinCon`](#enum-kaijuwincon), [`clear_surviving_kaiju`](#enum-clear_surviving_kaiju), [`require_beat_house_boss`](#enum-require_beat_house_boss), [`surviving_kaiju`](#enum-surviving_kaiju).

</details>


---

### Enum: `FormChange`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytosource), [`Conditional_HasStatus`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_hasstatus), [`Conditional_InForm`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_inform), [`Else`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-else), [`TimeDelayStatusApplication`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-timedelaystatusapplication), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`PassiveGroup`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passivegroup), [`alternate_energized_effect`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-alternate_energized_effect)

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

> **Also Used In:** These values are also referenced by [`class_anis`](#enum-class_anis), [`MulticlassLevelUp`](#enum-multiclasslevelup), [`ChangeCatClass`](#enum-changecatclass), [`complete_checklist_with_class`](#enum-complete_checklist_with_class), [`EvolveAbilityFromPool`](#enum-evolveabilityfrompool), [`palette`](#enum-palette), [`formchange`](#enum-formchange), [`form_above`](#enum-form_above), [`check_in_form`](#enum-check_in_form).

</details>


---

### Enum: `dash_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root), [`exit0`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-exit0), [`exit1`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-exit1), [`exit_desert`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-exit_desert), [`exit_lab`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-exit_lab), [`mw_altar`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-mw_altar), [`mw_quest_event`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-mw_quest_event), [`quest_event`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-quest_event), [`shop_cheapwater`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-shop_cheapwater), [`shop_water`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-shop_water), [`time_machine`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-time_machine)

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

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`AddStatusToBasicAttack`](../Player_Progression_and_Cats/Cat_Mutations.md#object-addstatustobasicattack), [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addstatustobasicattack), [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicattack), [`AddStatusToElementAbilities`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoelementabilities)

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

> **See Also:** Values from [`tile`](#enum-tile) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`TileTrail`](#enum-tiletrail), [`ChangeTilesUnder`](#enum-changetilesunder), [`ChangeTileOnPop`](#enum-changetileonpop), [`TileTrail_Ahead`](#enum-tiletrail_ahead).

</details>


---

### Enum: `get_item`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward)

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
| `Antenna` | |
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

> **Also Used In:** These values are also referenced by [`get_and_equip_item`](#enum-get_and_equip_item).

</details>


---

### Enum: `set_adventure_token`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`else`](../World_Maps_and_Events/Events_and_Encounters.md#object-else), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward)

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
| `CustomTokenString` | |
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

> **Also Used In:** These values are also referenced by [`clear_adventure_token`](#enum-clear_adventure_token).

</details>


---

### Enum: `layer`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`damage_instance`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-damage_instance), [`spawn`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-spawn), [`splash_damage`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-splash_damage), [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pickups` | |
| `characters` | |
| `all` | |
| `gas` | |
| `tiles` | |
| `self` | |

> **Also Used In:** These values are also referenced by [`level_up`](#enum-level_up), [`make_old`](#enum-make_old).

</details>


---

### Enum: `initial_form`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChanger`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchanger)

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

> **Also Used In:** These values are also referenced by [`form_hasnot`](#enum-form_hasnot), [`form`](#enum-form), [`form_above`](#enum-form_above).

</details>


---

### Enum: `play_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](../World_Maps_and_Events/Events_and_Encounters.md#object-bad), [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`main`](../World_Maps_and_Events/Events_and_Encounters.md#object-main), [`options`](../World_Maps_and_Events/Events_and_Encounters.md#object-options), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward), [`traverse`](../World_Maps_and_Events/Events_and_Encounters.md#object-traverse)

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

| `grass` | |
| `resultBlessing` | |
| `resultTragedy` | |
| `resultWeather` | |

</details>


---

### Enum: `trigger_npc_sequence`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

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

> **Also Used In:** These values are also referenced by [`reset_npc_sequence`](#enum-reset_npc_sequence), [`preempt_npc_sequence`](#enum-preempt_npc_sequence).

</details>


---

### Enum: `complete_chapter`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root), `20`

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
| `meatworld` | |
| `theend` | |

> **See Also:** Values from [`beat_chapter_boss`](#enum-beat_chapter_boss), [`music`](#enum-music), [`event_piece_frame`](#enum-event_piece_frame), [`chapter_id`](#enum-chapter_id), [`folder`](#enum-folder), [`tileset`](#enum-tileset), [`world_name_frame`](#enum-world_name_frame) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`hint_destination`](#enum-hint_destination), [`hint_chapter_exit`](#enum-hint_chapter_exit), [`intro_cutscene`](#enum-intro_cutscene), [`visit_chapter`](#enum-visit_chapter).

</details>


---

### Enum: `alias`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Status_Effect_Keywords)](../Core_Entities_and_Combat/Status_Effect_Keywords.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DamageUp` | |
| `DodgeChance_Status` | |
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

### Enum: `gain_familiar`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Events_and_Encounters)](../World_Maps_and_Events/Events_and_Encounters.md#object-root), [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`main`](../World_Maps_and_Events/Events_and_Encounters.md#object-main), [`options`](../World_Maps_and_Events/Events_and_Encounters.md#object-options), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

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
| `CharmedPooter` | |
| `CharmedRat` | |
| `CharmedWhiteRabbit` | |
| `FamiliarChargeyMaggot` | |
| `FamiliarFetus` | |
| `MechSuit` | |
| `Squirrel` | |
| `Toad` | |
| `Turtle` | |

> **Also Used In:** These values are also referenced by [`SpawnOnDowned`](#enum-spawnondowned).

</details>


---

### Enum: `ElementImmune`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applypassives), [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives), [`StacyMutant_Fire`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_fire), [`StacyMutant_Ice`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_ice), [`StacyMutant_Lightning`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_lightning), [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`passives`](../Core_Entities_and_Combat/Elite_Buffs.md#object-passives), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Fire` | |
| `Creep` | |
| `Ice` | |
| `Electric` | |

> **See Also:** Values from [`element`](#enum-element), [`AddElementsToBasicAttack`](#enum-addelementstobasicattack), [`InnateElement`](#enum-innateelement) may also be valid here (overlapping enum).

</details>


---

### Enum: `affected_particle`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

> **See Also:** Values from [`particle`](#enum-particle) may also be valid here (overlapping enum).

</details>


---

### Enum: `tooltip`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Pulp2`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp2), [`Pulp3`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp3), [`Pulp4`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp4), [`Pulp5`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp5), [`Pulp6`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp6), [`Pulp7`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pulp7), [`SquirrelForm`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-squirrelform), [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics), [`ROOT` (Status_Effect_Keywords)](../Core_Entities_and_Combat/Status_Effect_Keywords.md#object-root)

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

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

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

> **See Also:** Values from [`frame_label`](#enum-frame_label) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`trigger_house_boss`](#enum-trigger_house_boss), [`complete_house_boss`](#enum-complete_house_boss), [`initial_cutscene_night`](#enum-initial_cutscene_night), [`KaijuWinCon`](#enum-kaijuwincon), [`clear_surviving_kaiju`](#enum-clear_surviving_kaiju), [`require_beat_house_boss`](#enum-require_beat_house_boss), [`surviving_kaiju`](#enum-surviving_kaiju).

</details>


---

### Enum: `clear_adventure_token`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AdventureToken_BlueNeedle` | |
| `AdventureToken_HasTakenNeedle` | |
| `AdventureToken_RedNeedle` | |
| `AdventureToken_YellowNeedle` | |

> **See Also:** Values from [`has_token`](#enum-has_token), [`set_adventure_token`](#enum-set_adventure_token), [`not_has_token`](#enum-not_has_token) may also be valid here (overlapping enum).

</details>


---

### Enum: `dash_attack_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

> **See Also:** Values from [`animation`](#enum-animation) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`dash_end_animation`](#enum-dash_end_animation).

</details>


---

### Enum: `level`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root), [`boss`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-boss), [`event`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-event), [`miniboss_event`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-miniboss_event), [`mw_altar`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-mw_altar), [`mw_quest_event`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-mw_quest_event), [`quest_event`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-quest_event), [`shop_cheapwater`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-shop_cheapwater), [`shop_water`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-shop_water), [`time_machine`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-time_machine), [`treasure`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-treasure), [`weather_event`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-weather_event)

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

### Enum: `adventure_unlock`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `1`, `20`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `class_unlock_monocolorless_face` | |
| `class_unlock_monocolorless_head` | |
| `class_unlock_monocolorless_neck` | |
| `map_unlock_iceage` | |
| `nuke_quest_complete` | |
| `nuke_quest_get_nuke` | |
| `nuke_quest_jar1` | |
| `steven_unlock_infinite_crazy` | |
| `steven_unlock_infinite_hard` | |
| `steven_unlock_infinite_impossible` | |
| `steven_unlock_kfight_crazy` | |
| `steven_unlock_kfight_hard` | |
| `steven_unlock_kfight_impossible` | |
| `steven_unlock_pyro_crazy` | |
| `steven_unlock_pyro_hard` | |
| `steven_unlock_pyro_impossible` | |
| `steven_unlock_rift_crazy` | |
| `steven_unlock_rift_hard` | |
| `steven_unlock_rift_impossible` | |
| `steven_unlock_t1_crazy` | |
| `steven_unlock_t1_hard` | |
| `steven_unlock_t1_impossible` | |
| `steven_unlock_t2_crazy` | |
| `steven_unlock_t2_hard` | |
| `steven_unlock_t2_impossible` | |
| `steven_unlock_t3_crazy` | |
| `steven_unlock_t3_hard` | |
| `steven_unlock_t3_impossible` | |
| `steven_unlock_throb_crazy` | |
| `steven_unlock_throb_hard` | |
| `steven_unlock_throb_impossible` | |
| `steven_unlock_tina1_crazy` | |
| `steven_unlock_tina1_hard` | |
| `steven_unlock_tina1_impossible` | |
| `steven_unlock_tina2_crazy` | |
| `steven_unlock_tina2_hard` | |
| `steven_unlock_tina2_impossible` | |
| `steven_unlock_tina3_crazy` | |
| `steven_unlock_tina3_hard` | |
| `steven_unlock_tina3_impossible` | |
| `steven_unlock_zara_crazy` | |
| `steven_unlock_zara_hard` | |
| `steven_unlock_zara_impossible` | |
| `time_machine_quest_finalstep` | |

</details>


---

### Enum: `animation_in`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

### Enum: `tile`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChangeTile`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-changetile), [`SpawnExtraThingsOnBattleStart`](../World_Maps_and_Events/House_and_Environment.md#object-spawnextrathingsonbattlestart), [`SpawnTilePuddleOnBattleStart`](../World_Maps_and_Events/House_and_Environment.md#object-spawntilepuddleonbattlestart), [`ChangeTile`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-changetile), `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `OilTile` | |
| `WaterTile` | |
| `WaterTile_Current` | |
| `BrambleTile` | |
| `FireTile` | |
| `GlassTile` | |
| `LavaTile` | |
| `CreepTile` | |
| `ShadowTile` | |
| `ToxicTile` | |
| `DirtTile` | |
| `FlowerTile` | |
| `GlitchTile` | |
| `IceTile` | |
| `MetalTile` | |
| `RoadTile` | |
| `RockTile` | |
| `SnowTile` | |
| `StalagmiteTile` | |
| `SupercooledWater` | |
| `TallFlowerTile` | |
| `TallGrassTile` | |

> **Also Used In:** These values are also referenced by [`ChangeTile`](#enum-changetile), [`TileTrail`](#enum-tiletrail), [`ChangeTilesUnder`](#enum-changetilesunder), [`ChangeTileOnPop`](#enum-changetileonpop), [`TileTrail_Ahead`](#enum-tiletrail_ahead).

</details>


---

### Enum: `get_parasite`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](../World_Maps_and_Events/Events_and_Encounters.md#object-bad), [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FecalHood_Cursed` | |
| `FecalMask_Cursed` | |
| `MetalRod` | |
| `PawShards` | |
| `AlluringDoodie` | |
| `BadSplinters` | |
| `BirdPoopHat` | |
| `CursedHairball` | |
| `CursedRock` | |
| `FecalNecklace_Cursed` | |
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

> **Referenced by:** [`StatusOnBattleEnd`](../Player_Progression_and_Cats/Cat_Mutations.md#object-statusonbattleend), [`Conditional_GoodRoll`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-conditional_goodroll), [`StatusGroup`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statusgroup), [`ally_rewards`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-ally_rewards), [`Conditional_GoodRoll`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_goodroll), [`StatusOnBattleEnd`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonbattleend), [`StatusOnBattleStart`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonbattlestart), [`StatusOnBreak`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonbreak), [`StatusOnDie`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusondie), `StatusOnSetPieceBreak`, [`StatusOnBattleEnd`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonbattleend), [`statuses`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuses)

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

> **Referenced by:** [`ROOT` (Custom_Cats)](../Player_Progression_and_Cats/Custom_Cats.md#object-root)

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

> **See Also:** Values from [`class`](#enum-class), [`set`](#enum-set), [`pool`](#enum-pool), [`FormChange`](#enum-formchange), [`ChangeCatClass`](#enum-changecatclass), [`complete_checklist_with_class`](#enum-complete_checklist_with_class), [`EvolveAbilityFromPool`](#enum-evolveabilityfrompool) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`MulticlassLevelUp`](#enum-multiclasslevelup), [`palette`](#enum-palette).

</details>


---

### Enum: `target_requires_tag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

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

> **See Also:** Values from [`tag`](#enum-tag) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`AddHiddenTag`](#enum-addhiddentag), [`TagGreed`](#enum-taggreed).

</details>


---

### Enum: `VisualFXTile`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`post_spawn_statuses`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-post_spawn_statuses), [`AddStatusToBasicAttack`](../Player_Progression_and_Cats/Cat_Mutations.md#object-addstatustobasicattack), [`effects`](../Core_Entities_and_Combat/Elite_Buffs.md#object-effects), [`effects`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-effects), [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects)

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

> **See Also:** Values from [`particle`](#enum-particle) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`area_particle`](#enum-area_particle), [`VisualFX`](#enum-visualfx).

</details>


---

### Enum: `jump_attack_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

> **Referenced by:** [`bad`](../World_Maps_and_Events/Events_and_Encounters.md#object-bad), [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`else`](../World_Maps_and_Events/Events_and_Encounters.md#object-else), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward)

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
| `WorldEventLegacyToken_CustomTokenString` | |
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

> **Also Used In:** These values are also referenced by [`not_has_token`](#enum-not_has_token), [`save_file_flag`](#enum-save_file_flag), [`requires_flag`](#enum-requires_flag).

</details>


---

### Enum: `get_parasite_from_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](../World_Maps_and_Events/Events_and_Encounters.md#object-bad), [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward)

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

### Enum: `BounceObject`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`effects`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-effects), [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicattack)

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

> **See Also:** Values from [`object`](#enum-object) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`Imprison`](#enum-imprison).

</details>


---

### Enum: `preset`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-root), [`reverb_empty`](../World_Maps_and_Events/House_and_Environment.md#object-reverb_empty), [`reverb_full`](../World_Maps_and_Events/House_and_Environment.md#object-reverb_full), [`battle`](./Miscellaneous.md#object-battle)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `LIVINGROOM` | |
| `AUDITORIUM` | |
| `Cave` | |
| `Forest` | |
| `Alley` | |
| `ParkingLot` | |
| `STONEROOM` | |
| `StoneRoom` | |

</details>


---

### Enum: `CounterAttack`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StacyMutant_Counter`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_counter), [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`PassiveIfAllArmorEmpty`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveifallarmorempty), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Referenced by:** [`spawn`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-spawn), [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

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

### Enum: `injury`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `random` | |
| `radiated` | |
| `cursed` | |
| `bleeding` | |
| `burned` | |

</details>


---

### Enum: `ontrigger`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sounds`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-sounds)

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

### Enum: `plane`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ParticleBouncePlane`](./Miscellaneous.md#object-particlebounceplane)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `back` | |
| `right` | |

</details>


---

### Enum: `beat_chapter_boss`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

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

> **See Also:** Values from [`complete_chapter`](#enum-complete_chapter), [`music`](#enum-music), [`event_piece_frame`](#enum-event_piece_frame), [`chapter_id`](#enum-chapter_id), [`folder`](#enum-folder), [`tileset`](#enum-tileset), [`world_name_frame`](#enum-world_name_frame) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`hint_destination`](#enum-hint_destination), [`hint_chapter_exit`](#enum-hint_chapter_exit), [`intro_cutscene`](#enum-intro_cutscene), [`visit_chapter`](#enum-visit_chapter).

</details>


---

### Enum: `hidden_tag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties)

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

> **Also Used In:** These values are also referenced by [`tag_restriction`](#enum-tag_restriction), [`AbilityEnableIfConsumedCharacterHasTag`](#enum-abilityenableifconsumedcharacterhastag), [`warrior_tag`](#enum-warrior_tag).

</details>


---

### Enum: `not_has_token`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`requirements`](./Miscellaneous.md#object-requirements), [`requirements`](../World_Maps_and_Events/Events_and_Encounters.md#object-requirements)

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
| `WorldEventLegacyToken_Baz` | |
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

> **See Also:** Values from [`has_token`](#enum-has_token), [`set_legacy_token`](#enum-set_legacy_token) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`clear_adventure_token`](#enum-clear_adventure_token).

</details>


---

### Enum: `spawn_side`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`spawn_unit_next_fight`](../World_Maps_and_Events/Events_and_Encounters.md#object-spawn_unit_next_fight)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `enemies` | |
| `cats` | |
| `anywhere` | |

</details>


---

### Enum: `unlock_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

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

> **See Also:** Values from [`variant_of`](#enum-variant_of) may also be valid here (overlapping enum).

</details>


---

### Enum: `form_hasnot`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeWhileHasStatus`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangewhilehasstatus)

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

> **See Also:** Values from [`initial_form`](#enum-initial_form) may also be valid here (overlapping enum).

</details>


---

### Enum: `ai_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-root)

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

### Enum: `id`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-root), [`SmallAttic`](../World_Maps_and_Events/House_and_Environment.md#object-smallattic), [`ParticleGlobalForce`](./Miscellaneous.md#object-particleglobalforce)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Wind` | |
| `Attic` | |

</details>


---

### Enum: `mode`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics), [`PassiveAtHealthThreshold`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passiveathealththreshold), [`PassiveAtStatThreshold`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passiveatstatthreshold), [`PassiveAtHealthThreshold`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveathealththreshold), [`PassiveAtInjuryThreshold`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveatinjurythreshold), [`PassiveAtStatThreshold`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveatstatthreshold)

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

### Enum: `music`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `guillotina` | |
| `kaiju` | |
| `jurassic` | |
| `terminator` | |
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
| `hitler3` | |
| `iceage` | |
| `junkyard` | |
| `lab` | |
| `meatworld` | |
| `moon` | |
| `sewers` | |
| `theend` | |
| `tutorial` | |

> **Also Used In:** These values are also referenced by [`complete_chapter`](#enum-complete_chapter), [`beat_chapter_boss`](#enum-beat_chapter_boss), [`event_piece_frame`](#enum-event_piece_frame), [`chapter_id`](#enum-chapter_id), [`folder`](#enum-folder), [`tileset`](#enum-tileset), [`world_name_frame`](#enum-world_name_frame), [`hint_destination`](#enum-hint_destination), [`hint_chapter_exit`](#enum-hint_chapter_exit), [`intro_cutscene`](#enum-intro_cutscene), [`visit_chapter`](#enum-visit_chapter).

</details>


---

### Enum: `unlock_passive`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

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

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

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

> **Referenced by:** [`ApplyToSource`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytosource), [`VisualCountDownThenApplyStatus`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-visualcountdownthenapplystatus), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`FinalBossHitCountdownBoris`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-finalbosshitcountdownboris), [`FinalBossHitCountdownExplosive`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-finalbosshitcountdownexplosive), [`StatusAfterXTurns`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statusafterxturns), [`StatusEachTurnEndIfEnabledAtStartOfTurn`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statuseachturnendifenabledatstartofturn), [`AddSelfStatusToBasicAttack`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addselfstatustobasicattack), [`Conditional_GoodRoll`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_goodroll), [`StatusAfterXTurns`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusafterxturns), [`StatusEachTurnEnd`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statuseachturnend), [`StatusEachTurnEndForEachTurn`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statuseachturnendforeachturn), [`StatusOnBattleStart`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonbattlestart), [`StatusOnKillEnemy`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonkillenemy), [`StatusEachTurnEnd`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnend), [`StatusOnStanceSwitch`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonstanceswitch), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Referenced by:** [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **See Also:** Values from [`class`](#enum-class), [`set`](#enum-set), [`pool`](#enum-pool), [`FormChange`](#enum-formchange), [`class_anis`](#enum-class_anis), [`ChangeCatClass`](#enum-changecatclass), [`complete_checklist_with_class`](#enum-complete_checklist_with_class), [`EvolveAbilityFromPool`](#enum-evolveabilityfrompool), [`palette`](#enum-palette) may also be valid here (overlapping enum).

</details>


---

### Enum: `TransformAbility`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

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

> **See Also:** Values from [`variant_of`](#enum-variant_of) may also be valid here (overlapping enum).

</details>


---

### Enum: `aoe_symmetry`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

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

> **Referenced by:** [`Conditional_InForm`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_inform), [`FormChange`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-formchange), [`ChanceToFormChangeOnAbilityDamage`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-chancetoformchangeonabilitydamage), [`DybbukPossessionFallback`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-dybbukpossessionfallback), [`FormChangeDuringWeatherElement`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangeduringweatherelement), [`FormChangeOnElementInfluence`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangeonelementinfluence)

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

> **See Also:** Values from [`initial_form`](#enum-initial_form) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`formchange`](#enum-formchange).

</details>


---

### Enum: `icon_shell_frame`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-meta)

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

> **Referenced by:** [`Craft`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-craft), [`Craft`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-craft), [`SetItemAux`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-setitemaux), [`Craft`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-craft), [`lock_item_slot`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-lock_item_slot)

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

> **Also Used In:** These values are also referenced by [`kind`](#enum-kind), [`restrict`](#enum-restrict).

</details>


---

### Enum: `ReplaceBasicAttack`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applypassives), [`PassiveGroup`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passivegroup), [`StacyMutant_Fire`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_fire), [`StacyMutant_Ice`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_ice), [`StacyMutant_Lightning`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_lightning), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **See Also:** Values from [`attack`](#enum-attack) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`override_basic_attack`](#enum-override_basic_attack), [`ability_icon`](#enum-ability_icon).

</details>


---

### Enum: `form_has`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeWhileHasStatus`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangewhilehasstatus)

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

### Enum: `ObjectOnHitCharacter`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CanApplyToInanimate`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-canapplytoinanimate), [`Else`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-else), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`StatusOnBreak`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonbreak), [`CritsApplyStatus`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-critsapplystatus), [`RandomStatusFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-randomstatusfrompool), [`StatusOnHealed`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonhealed)

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

> **See Also:** Values from [`object`](#enum-object) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`Imprison`](#enum-imprison), [`BreakIntoRocks`](#enum-breakintorocks).

</details>


---

### Enum: `full_jump_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

> **Referenced by:** [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives), [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **See Also:** Values from [`element`](#enum-element) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`ElementImmune`](#enum-elementimmune), [`InnateElement`](#enum-innateelement).

</details>


---

### Enum: `DeathRattle`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

### Enum: `cat_has_item_equipped`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`requirements`](./Miscellaneous.md#object-requirements), [`requirements`](../World_Maps_and_Events/Events_and_Encounters.md#object-requirements)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `PyrophinasCollar` | |
| `ZaratanasCollar` | |
| `CryogenicTimeChamber_Empty` | |
| `CryogenicTimeChamber_Full` | |
| `FaceCovering` | |
| `GuillotinasHead` | |
| `JarOfRadiatedBlood` | |
| `JarOfRadiation` | |
| `PutridLeech` | |
| `ReceiverAntenna` | |
| `SignalAmplifier` | |
| `ThrobbingGristle` | |
| `TransmitterAntenna` | |

> **See Also:** Values from [`complete_item_quest`](#enum-complete_item_quest), [`unlock_quest_item`](#enum-unlock_quest_item) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`lose_specific_item`](#enum-lose_specific_item), [`choose_cat_with_item`](#enum-choose_cat_with_item), [`fail_item_quest`](#enum-fail_item_quest), [`unlock_item_quest`](#enum-unlock_item_quest), [`not_cat_has_item_equipped`](#enum-not_cat_has_item_equipped).

</details>


---

### Enum: `ownership`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `local` | |

</details>


---

### Enum: `set_mapgen_flag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

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

> **Also Used In:** These values are also referenced by [`require_mapgen_flag`](#enum-require_mapgen_flag).

</details>


---

### Enum: `shadow`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `none` | |
| `None` | |
| `MedSlimeShadow` | |
| `BigSlimeShadow` | |
| `SmallSlimeShadow` | |
| `TormentorShadow` | |

> **Also Used In:** These values are also referenced by [`tooltip_stackless`](#enum-tooltip_stackless).

</details>


---

### Enum: `title`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`intro`](../World_Maps_and_Events/Events_and_Encounters.md#object-intro)

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

### Enum: `add_weather`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Events_and_Encounters)](../World_Maps_and_Events/Events_and_Encounters.md#object-root), [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`main`](../World_Maps_and_Events/Events_and_Encounters.md#object-main), [`outcome`](../World_Maps_and_Events/Events_and_Encounters.md#object-outcome), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

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
| `Rain` | |

</details>


---

### Enum: `chain`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MiniSplatter` | |
| `firework_burst` | |
| `splashB` | |
| `splashF` | |
| `splashM2` | |
| `AcidSplash` | |
| `CaveSplash` | |
| `FireFullSmall` | |
| `Kingblood2` | |
| `MeatCaveSplash` | |
| `MiniSplatter2` | |
| `MiniSplatter3` | |
| `TsplashM` | |
| `firework_burst_recursive` | |
| `splash` | |
| `splashM` | |
| `test8` | |

</details>


---

### Enum: `complete_item_quest`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

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
| `TinasHead` | |
| `TransmitterAntenna` | |
| `ZaratanasCollar` | |

> **Also Used In:** These values are also referenced by [`cat_has_item_equipped`](#enum-cat_has_item_equipped), [`lose_specific_item`](#enum-lose_specific_item), [`unlock_quest_item`](#enum-unlock_quest_item), [`choose_cat_with_item`](#enum-choose_cat_with_item), [`CompleteItemQuest`](#enum-completeitemquest), [`RemoveItem`](#enum-removeitem), [`fail_item_quest`](#enum-fail_item_quest), [`unlock_item_quest`](#enum-unlock_item_quest), [`not_cat_has_item_equipped`](#enum-not_cat_has_item_equipped).

</details>


---

### Enum: `dash_end_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dashend` | |
| `launchStop` | |
| `ramEnd` | |
| `none` | |
| `thrustersEnd` | |
| `timberEnd` | |

> **See Also:** Values from [`dash_attack_animation`](#enum-dash_attack_animation) may also be valid here (overlapping enum).

</details>


---

### Enum: `event_now`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](../World_Maps_and_Events/Events_and_Encounters.md#object-bad), [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`else`](../World_Maps_and_Events/Events_and_Encounters.md#object-else), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward)

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
| `Tragedy` | |

</details>


---

### Enum: `quest_reward_item`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

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

> **Referenced by:** [`ROOT` (Status_Effect_Keywords)](../Core_Entities_and_Combat/Status_Effect_Keywords.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `none` | |
| `None` | |
| `KEYWORD_AUTOREVIVE_DESC` | |

> **See Also:** Values from [`particle`](#enum-particle), [`shadow`](#enum-shadow), [`center_particle`](#enum-center_particle) may also be valid here (overlapping enum).

</details>


---

### Enum: `center_particle`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics), [`spell_graphics_override`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spell_graphics_override)

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

> **See Also:** Values from [`particle`](#enum-particle) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`tooltip_stackless`](#enum-tooltip_stackless).

</details>


---

### Enum: `combat_background`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AlleyBGTest` | |
| `BoneYardBG` | |
| `BunkerBG` | |
| `CavesBG` | |
| `CoreBG` | |
| `CraterBG` | |
| `DesertBG` | |
| `HouseBG` | |
| `IceageBG` | |
| `JunkyardBG` | |
| `LabBG` | |
| `MoonBG` | |
| `SewerBG` | |
| `dinolandBG` | |
| `finalbossBG` | |
| `futureBG` | |
| `infiniteBG` | |
| `meatBGpulsing` | |
| `theendBG` | |
| `thepathBG` | |
| `theriftBG` | |

</details>


---

### Enum: `combat_ui_background`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CoreUI` | |
| `DesertUI` | |
| `LabUI` | |
| `MoonUI` | |
| `UI_Background` | |
| `UI_Background2` | |
| `UI_Background_Bunker` | |
| `UI_Background_Caves` | |
| `UI_Background_Crater` | |
| `UI_Background_Dino` | |
| `UI_Background_Graves` | |
| `UI_Background_Iceage` | |
| `UI_Background_Junkyard` | |
| `UI_Background_Sewers` | |
| `UI_End` | |
| `UI_FinalBoss` | |
| `UI_Future` | |
| `UI_Infinite` | |
| `UI_Meat` | |
| `UI_Rift` | |
| `UI_tutoral` | |

</details>


---

### Enum: `debris`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Debris` | |
| `infinitedebris` | |
| `CaveDebris` | |
| `Debris10` | |
| `Debris11` | |
| `Debris12` | |
| `Debris2` | |
| `Debris3` | |
| `Debris7` | |
| `Debris8` | |
| `Debris9` | |
| `DesertDebris` | |
| `GravesDebris` | |
| `dinodebris` | |
| `enddebris` | |
| `futuredebris` | |
| `meatdebris` | |
| `riftdebris` | |

</details>


---

### Enum: `event_piece_frame`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `theinfinite` | |
| `alley` | |
| `bunker` | |
| `caves` | |
| `core` | |
| `crater` | |
| `desert` | |
| `future` | |
| `graves` | |
| `house` | |
| `iceage` | |
| `junkyard` | |
| `jurassic` | |
| `lab` | |
| `meatworld` | |
| `moon` | |
| `sewers` | |
| `theend` | |
| `therift` | |
| `tutorial` | |

> **See Also:** Values from [`music`](#enum-music), [`chapter_id`](#enum-chapter_id), [`tileset`](#enum-tileset) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`complete_chapter`](#enum-complete_chapter), [`beat_chapter_boss`](#enum-beat_chapter_boss), [`folder`](#enum-folder), [`world_name_frame`](#enum-world_name_frame), [`hint_destination`](#enum-hint_destination), [`hint_chapter_exit`](#enum-hint_chapter_exit), [`intro_cutscene`](#enum-intro_cutscene), [`visit_chapter`](#enum-visit_chapter).

</details>


---

### Enum: `first_turn`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-spawn), [`TransformOnDeathImmediately`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-transformondeathimmediately)

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

### Enum: `particle_lifetime`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `.5` | |
| `.7` | |
| `.` | |
| `.025` | |
| `.35` | |

</details>


---

### Enum: `static_1x1_a`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Infiniteobjects` | |
| `Rubble` | |
| `BunkerObjects1` | |
| `CaveRock1` | |
| `CoreObjects1` | |
| `CraterObjects1` | |
| `DesertRocks` | |
| `Dinoobjects` | |
| `Endobjects` | |
| `Futureobjects` | |
| `GraveRocks1` | |
| `Iceageobjects1` | |
| `LabObjects1` | |
| `Meatobjects` | |
| `MoonObjects1` | |
| `Pathrubble` | |
| `Riftobjects` | |
| `SmallPipes` | |
| `StaticJunkSmall` | |

> **Also Used In:** These values are also referenced by [`static_1x1_c`](#enum-static_1x1_c).

</details>


---

### Enum: `static_1x1_b`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Bricks` | |
| `Infiniteobjects2` | |
| `Bricks3` | |
| `BunkerObjects2` | |
| `CaveRock2` | |
| `CoreObjects2` | |
| `CraterObjects2` | |
| `DesertCactus` | |
| `Dinoobjects` | |
| `Endobjects` | |
| `Futureobjects2` | |
| `GraveRocks2` | |
| `IceageObjects2` | |
| `Labobjects2` | |
| `Meatobjects2` | |
| `MoonObjects2` | |
| `Riftobjects` | |
| `Stump` | |

</details>


---

### Enum: `static_1x1_c`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Bricks` | |
| `Infiniteobjects` | |
| `SmallGravelPile` | |
| `CaveRock3` | |
| `CoreObjects3` | |
| `CraterObjects1` | |
| `DesertRocks` | |
| `Dinoobjects` | |
| `Endobjects` | |
| `Futureobjects` | |
| `GraveRocks2` | |
| `Iceageobjects1` | |
| `LabObjects1` | |
| `Meatobjects` | |
| `MoonObjects2` | |
| `Riftobjects` | |
| `Sludge` | |

> **See Also:** Values from [`static_1x1_a`](#enum-static_1x1_a) may also be valid here (overlapping enum).

</details>


---

### Enum: `static_2x2_a`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Dumpster` | |
| `Infinite2x2` | |
| `BigCaveRock1` | |
| `BigGraveRocks1` | |
| `BigPipes` | |
| `Bunker2x2` | |
| `Core2x2` | |
| `Crater2x2` | |
| `Desert2x2` | |
| `End2x2` | |
| `Iceage2x2` | |
| `Lab2x2` | |
| `Meat2x2` | |
| `Moon2x2` | |
| `Rift2x2` | |
| `StaticJunkCube` | |
| `dino2x2` | |
| `future2x2` | |
| `thepath2x2` | |

> **Also Used In:** These values are also referenced by [`static_2x2_b`](#enum-static_2x2_b).

</details>


---

### Enum: `static_2x2_b`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Dumpster` | |
| `Desert2x2` | |
| `BigGravelPile` | |
| `Moon2x22` | |
| `BigCaveRock1` | |
| `BigGraveRocks1` | |

> **See Also:** Values from [`static_2x2_a`](#enum-static_2x2_a) may also be valid here (overlapping enum).

</details>


---

### Enum: `static_tall_a`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `PowerPole` | |
| `infinitetall1` | |
| `BunkerTall1` | |
| `CoreTall1` | |
| `CraterTall1` | |
| `DesertTall` | |
| `Iceagetall1` | |
| `Labtall1` | |
| `Meatt` | |
| `MoonTall1` | |
| `TallCaveRock1` | |
| `TallGraveRocks1` | |
| `TallPipe` | |
| `Tree` | |
| `dinolandtall1` | |
| `endtall1` | |
| `futuretall1` | |
| `rifttall1` | |

</details>


---

### Enum: `static_tall_b`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `PhoneBooth` | |
| `infinitetall1` | |
| `BunkerTall2` | |
| `CoreTall2` | |
| `CraterTall2` | |
| `DesertTall2` | |
| `Endt` | |
| `Iceagetall2` | |
| `Labtall2` | |
| `MoonTall2` | |
| `Riftt` | |
| `StaticTires` | |
| `TallCaveRock2` | |
| `TallGraveRocks1` | |
| `dinolandtall0` | |
| `futuretall` | |
| `meattall1` | |

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

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics), [`spell_graphics_override`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spell_graphics_override)

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

> **See Also:** Values from [`particle`](#enum-particle), [`VisualFXTile`](#enum-visualfxtile) may also be valid here (overlapping enum).

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

> **See Also:** Values from [`music`](#enum-music), [`event_piece_frame`](#enum-event_piece_frame), [`tileset`](#enum-tileset) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`complete_chapter`](#enum-complete_chapter), [`beat_chapter_boss`](#enum-beat_chapter_boss), [`folder`](#enum-folder), [`world_name_frame`](#enum-world_name_frame), [`hint_destination`](#enum-hint_destination), [`hint_chapter_exit`](#enum-hint_chapter_exit), [`intro_cutscene`](#enum-intro_cutscene), [`visit_chapter`](#enum-visit_chapter).

</details>


---

### Enum: `common`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BossRewards`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-bossrewards)

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

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

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

> **See Also:** Values from [`music`](#enum-music), [`event_piece_frame`](#enum-event_piece_frame), [`chapter_id`](#enum-chapter_id), [`tileset`](#enum-tileset), [`world_name_frame`](#enum-world_name_frame) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`complete_chapter`](#enum-complete_chapter), [`beat_chapter_boss`](#enum-beat_chapter_boss), [`hint_destination`](#enum-hint_destination), [`hint_chapter_exit`](#enum-hint_chapter_exit), [`intro_cutscene`](#enum-intro_cutscene), [`visit_chapter`](#enum-visit_chapter).

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

### Enum: `next_map`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`exit0`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-exit0), [`exit1`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-exit1), [`exit_desert`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-exit_desert), [`exit_lab`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-exit_lab)

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

> **Also Used In:** These values are also referenced by [`begin_chapter`](#enum-begin_chapter).

</details>


---

### Enum: `tileset`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`boss`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-boss)

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

> **See Also:** Values from [`music`](#enum-music), [`event_piece_frame`](#enum-event_piece_frame), [`chapter_id`](#enum-chapter_id) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`complete_chapter`](#enum-complete_chapter), [`beat_chapter_boss`](#enum-beat_chapter_boss), [`folder`](#enum-folder), [`world_name_frame`](#enum-world_name_frame), [`hint_destination`](#enum-hint_destination), [`hint_chapter_exit`](#enum-hint_chapter_exit), [`intro_cutscene`](#enum-intro_cutscene), [`visit_chapter`](#enum-visit_chapter).

</details>


---

### Enum: `EliteParticle`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Elite_Buffs.md#object-passives)

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

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

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

> **Referenced by:** [`SpreadDisease`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-spreaddisease), [`CureDisease`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-curedisease), [`SpreadDisease`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spreaddisease)

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

> **See Also:** Values from [`music`](#enum-music), [`event_piece_frame`](#enum-event_piece_frame), [`chapter_id`](#enum-chapter_id), [`folder`](#enum-folder), [`tileset`](#enum-tileset) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`complete_chapter`](#enum-complete_chapter), [`beat_chapter_boss`](#enum-beat_chapter_boss), [`hint_destination`](#enum-hint_destination), [`hint_chapter_exit`](#enum-hint_chapter_exit), [`intro_cutscene`](#enum-intro_cutscene), [`visit_chapter`](#enum-visit_chapter).

</details>


---

### Enum: `BonusAbility`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`keyword_tooltips`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-keyword_tooltips), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Also Used In:** These values are also referenced by [`ChargeSpiritBombAura`](#enum-chargespiritbombaura).

</details>


---

### Enum: `InnateElement`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`passives`](../Core_Entities_and_Combat/Elite_Buffs.md#object-passives), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Fire` | |
| `Ice` | |
| `Earth` | |
| `Electric` | |
| `Water` | |

> **See Also:** Values from [`element`](#enum-element), [`AddElementsToBasicAttack`](#enum-addelementstobasicattack) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`ElementImmune`](#enum-elementimmune), [`aoe_tile_requires_element`](#enum-aoe_tile_requires_element).

</details>


---

### Enum: `restrict`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`get_item_from_pool`](../World_Maps_and_Events/Events_and_Encounters.md#object-get_item_from_pool)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `trinket` | |
| `weapon` | |
| `consumables` | |
| `armor` | |

> **See Also:** Values from [`kind`](#enum-kind), [`slot`](#enum-slot) may also be valid here (overlapping enum).

</details>


---

### Enum: `AbilityOnBattleStart_Immediate`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`party_status_next_fight`](../World_Maps_and_Events/Events_and_Encounters.md#object-party_status_next_fight), [`self_status_next_fight`](../World_Maps_and_Events/Events_and_Encounters.md#object-self_status_next_fight)

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

> **Referenced by:** [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`PassiveWhenAtFullMana`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhenatfullmana), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

### Enum: `ambient_sound`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-root), [`Rain`](../World_Maps_and_Events/House_and_Environment.md#object-rain), [`Snow`](../World_Maps_and_Events/House_and_Environment.md#object-snow), [`Thunderstorm`](../World_Maps_and_Events/House_and_Environment.md#object-thunderstorm), [`Windy`](../World_Maps_and_Events/House_and_Environment.md#object-windy)

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

> **Referenced by:** [`boss`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-boss), [`mw_boss`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-mw_boss)

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

> **See Also:** Values from [`frame_label`](#enum-frame_label) may also be valid here (overlapping enum).

</details>


---

### Enum: `level_display`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`beanies_quests_repeat`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-beanies_quests_repeat), [`frank_max_intro`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-frank_max_intro), [`frank_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-frank_max_repeating), [`jack_max_intro`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-jack_max_intro), [`jack_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-jack_max_repeating), [`organ_max_intro`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-organ_max_intro), [`organ_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-organ_max_repeating), [`steven_milliontrashed`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-steven_milliontrashed), [`tink_max_intro`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_max_intro), [`tink_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_max_repeating), [`tracy_max_intro`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_max_intro), [`tracy_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_max_repeating), [`upgrade_storage_repeating_crazy`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_repeating_crazy), [`upgrade_storage_repeating_hard`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_repeating_hard), [`upgrade_storage_repeating_impossible`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_repeating_impossible), [`upgrade_storage_repeating_intro`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_repeating_intro), [`upgrade_storage_repeating_normal`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_repeating_normal)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `max` | |

</details>


---

### Enum: `lose_item`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](../World_Maps_and_Events/Events_and_Encounters.md#object-bad), [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `inventory` | |
| `equipped` | |
| `parasite` | |
| `weapon` | |

</details>


---

### Enum: `struggle_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Consumed`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-consumed), [`Consumed`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-consumed)

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

> **Referenced by:** [`ApplyToRandomPartyMemberIfPossible`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytorandompartymemberifpossible), [`Conditional_GoodRoll`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_goodroll), [`Else`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-else)

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

> **Referenced by:** [`ApplyToSource`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytosource), [`Conditional_Boss`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_boss), [`Conditional_HasStatus`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_hasstatus), [`Conditional_HasTag`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_hastag), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`StatusOnTookDamage`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusontookdamage)

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

> **See Also:** Values from [`status`](#enum-status) may also be valid here (overlapping enum).

</details>


---

### Enum: `SpawnOnBattleStart`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`innate_passives`](../Player_Progression_and_Cats/Cat_Classes.md#object-innate_passives), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **See Also:** Values from [`object`](#enum-object) may also be valid here (overlapping enum).

</details>


---

### Enum: `SpawnThingOnDeath`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **See Also:** Values from [`object`](#enum-object) may also be valid here (overlapping enum).

</details>


---

### Enum: `auto_run_priority`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties)

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

> **Referenced by:** [`graphics`](../Player_Progression_and_Cats/Cat_Classes.md#object-graphics), [`ROOT` (Custom_Cats)](../Player_Progression_and_Cats/Custom_Cats.md#object-root)

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

> **Referenced by:** [`equipment`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-equipment)

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

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

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

> **See Also:** Values from [`complete_chapter`](#enum-complete_chapter), [`beat_chapter_boss`](#enum-beat_chapter_boss), [`music`](#enum-music), [`event_piece_frame`](#enum-event_piece_frame), [`chapter_id`](#enum-chapter_id), [`folder`](#enum-folder), [`tileset`](#enum-tileset), [`world_name_frame`](#enum-world_name_frame) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`hint_chapter_exit`](#enum-hint_chapter_exit), [`visit_chapter`](#enum-visit_chapter).

</details>


---

### Enum: `kill`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](../World_Maps_and_Events/Events_and_Encounters.md#object-bad), [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cat` | |

</details>


---

### Enum: `move_for_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MoveClose`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveclose), [`MoveForBarrage`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveforbarrage), [`MoveForDash`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movefordash), [`MoveForGrass`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveforgrass), [`MoveForPounce`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveforpounce), [`MoveForSpin`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveforspin), [`MoveForThrow`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveforthrow), [`MoveOneForPuke`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveoneforpuke), [`MoveToHead`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movetohead), [`MoveTowards`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movetowards), [`SpearRun`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-spearrun), [`Unflip`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-unflip)

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

> **Referenced by:** [`BossRewards`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-bossrewards)

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

### Enum: `AbilityOnBattleStart`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`self_status_next_fight`](../World_Maps_and_Events/Events_and_Encounters.md#object-self_status_next_fight), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Referenced by:** [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives), [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`AddPassivesToMinions`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addpassivestominions)

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

> **See Also:** Values from [`object`](#enum-object), [`movieclip`](#enum-movieclip) may also be valid here (overlapping enum).

</details>


---

### Enum: `chain_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-root)

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

### Enum: `move_then_do`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonusturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-bonusturn_pattern), [`fallback`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-fallback), [`mainturn_pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-mainturn_pattern), [`pattern`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-pattern)

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

### Enum: `shop_now`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`main`](../World_Maps_and_Events/Events_and_Encounters.md#object-main), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare), [`traverse`](../World_Maps_and_Events/Events_and_Encounters.md#object-traverse)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Event_SmallShop` | |
| `Event_RareShop` | |
| `TreasureHard` | |
| `Shop` | |
| `TreasureEasy` | |

</details>


---

### Enum: `str_aux_initialize`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

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

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

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

> **See Also:** Values from [`class`](#enum-class), [`set`](#enum-set), [`pool`](#enum-pool), [`FormChange`](#enum-formchange), [`complete_checklist_with_class`](#enum-complete_checklist_with_class) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`class_anis`](#enum-class_anis), [`MulticlassLevelUp`](#enum-multiclasslevelup), [`EvolveAbilityFromPool`](#enum-evolveabilityfrompool), [`palette`](#enum-palette), [`ConjureBonusAbility`](#enum-conjurebonusability), [`LevelUpClassOverride`](#enum-levelupclassoverride).

</details>


---

### Enum: `TileTrail`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-temporary_effects), [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`passives`](../Core_Entities_and_Combat/Elite_Buffs.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **See Also:** Values from [`ChangeTile`](#enum-changetile), [`tile`](#enum-tile) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`TileTrail_Ahead`](#enum-tiletrail_ahead).

</details>


---

### Enum: `TransformBasicAttack`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

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

> **Referenced by:** [`Conditional_Boss`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_boss), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), `Conditional_HasCleansableDebuffs`, [`effects`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-effects)

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

> **See Also:** Values from [`particle`](#enum-particle), [`VisualFXTile`](#enum-visualfxtile) may also be valid here (overlapping enum).

</details>


---

### Enum: `animation_suffix`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Big`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-big), [`Explody`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-explody), [`FireFull`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-firefull), [`Grown`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-grown), [`HumanDead`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-humandead), [`NormalFull`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-normalfull), [`Nuke`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-nuke), [`Off`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-off), [`Open`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-open), [`OpenCat`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-opencat), [`Sitting`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-sitting), [`TarFull`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-tarfull), [`Turtled`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-turtled)

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

### Enum: `complete_checklist_with_class`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

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

> **See Also:** Values from [`class`](#enum-class), [`set`](#enum-set), [`pool`](#enum-pool), [`FormChange`](#enum-formchange), [`ChangeCatClass`](#enum-changecatclass) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`class_anis`](#enum-class_anis), [`MulticlassLevelUp`](#enum-multiclasslevelup), [`EvolveAbilityFromPool`](#enum-evolveabilityfrompool), [`palette`](#enum-palette), [`ConjureBonusAbility`](#enum-conjurebonusability), [`LevelUpClassOverride`](#enum-levelupclassoverride).

</details>


---

### Enum: `copy_results`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Events_and_Encounters)](../World_Maps_and_Events/Events_and_Encounters.md#object-root), [`blue`](../World_Maps_and_Events/Events_and_Encounters.md#object-blue), [`button`](../World_Maps_and_Events/Events_and_Encounters.md#object-button), [`examine`](../World_Maps_and_Events/Events_and_Encounters.md#object-examine), [`open`](../World_Maps_and_Events/Events_and_Encounters.md#object-open), [`smash`](../World_Maps_and_Events/Events_and_Encounters.md#object-smash)

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

> **Referenced by:** [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `indestructible` | |

</details>


---

### Enum: `head`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`equipment`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-equipment)

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

### Enum: `move_start_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

### Enum: `ClassFromNeutral,`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Player_Progression_and_Cats/Cat_Classes.md#object-graphics)

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

> **Referenced by:** [`graphics`](../Player_Progression_and_Cats/Cat_Classes.md#object-graphics)

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

> **Referenced by:** [`ApplyToSource`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytosource), [`ApplyToSourceOnKill`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytosourceonkill), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

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

> **See Also:** Values from [`class`](#enum-class), [`set`](#enum-set), [`pool`](#enum-pool), [`FormChange`](#enum-formchange), [`class_anis`](#enum-class_anis), [`ChangeCatClass`](#enum-changecatclass), [`complete_checklist_with_class`](#enum-complete_checklist_with_class) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`MulticlassLevelUp`](#enum-multiclasslevelup), [`palette`](#enum-palette).

</details>


---

### Enum: `StartTurn,`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Player_Progression_and_Cats/Cat_Classes.md#object-graphics)

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

> **Referenced by:** [`graphics`](../Player_Progression_and_Cats/Cat_Classes.md#object-graphics)

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

### Enum: `begin_chapter`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `home` | |
| `iceage.gon` | |
| `endoftime.gon` | |
| `dimensionx.gon` | |
| `future.gon` | |
| `jurassic.gon` | |
| `theend.gon` | |

> **See Also:** Values from [`next_map`](#enum-next_map) may also be valid here (overlapping enum).

</details>


---

### Enum: `catdata`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-spawn)

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

> **Referenced by:** [`ROOT` (Injuries)](../Player_Progression_and_Cats/Injuries.md#object-root)

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

> **Referenced by:** [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `terminator_mini` | |

</details>


---

### Enum: `hint_chapter_exit`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`enter`](../World_Maps_and_Events/Events_and_Encounters.md#object-enter), [`future`](../World_Maps_and_Events/Events_and_Encounters.md#object-future), [`home`](../World_Maps_and_Events/Events_and_Encounters.md#object-home), [`ignore`](../World_Maps_and_Events/Events_and_Encounters.md#object-ignore), [`infinite`](../World_Maps_and_Events/Events_and_Encounters.md#object-infinite), [`past`](../World_Maps_and_Events/Events_and_Encounters.md#object-past)

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

> **See Also:** Values from [`complete_chapter`](#enum-complete_chapter), [`beat_chapter_boss`](#enum-beat_chapter_boss), [`music`](#enum-music), [`event_piece_frame`](#enum-event_piece_frame), [`chapter_id`](#enum-chapter_id), [`folder`](#enum-folder), [`tileset`](#enum-tileset), [`world_name_frame`](#enum-world_name_frame), [`hint_destination`](#enum-hint_destination) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`visit_chapter`](#enum-visit_chapter).

</details>


---

### Enum: `lose_specific_item`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SlagTight` | |
| `CryogenicTimeChamber_Full` | |
| `GuillotinasHead` | |
| `PutridLeech` | |
| `PyrophinasCollar` | |
| `ReceiverAntenna` | |
| `SignalAmplifier` | |
| `ThrobbingGristle` | |
| `TransmitterAntenna` | |
| `ZaratanasCollar` | |

> **See Also:** Values from [`cat_has_item_equipped`](#enum-cat_has_item_equipped), [`complete_item_quest`](#enum-complete_item_quest), [`unlock_quest_item`](#enum-unlock_quest_item) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`choose_cat_with_item`](#enum-choose_cat_with_item), [`not_cat_has_item_equipped`](#enum-not_cat_has_item_equipped).

</details>


---

### Enum: `move_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MoveWhenDamaged`](../Player_Progression_and_Cats/Cat_Mutations.md#object-movewhendamaged), [`MoveAwayFromDamageSource`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveawayfromdamagesource), [`MoveAwayWhenEnemyAdjacent`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveawaywhenenemyadjacent), [`MoveTowardsDamageSource`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movetowardsdamagesource), [`MoveTowardsKillers`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movetowardskillers), [`MoveWhenDamaged`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movewhendamaged), [`Terminator2Run`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-terminator2run), [`MoveTowardsDamageSource`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-movetowardsdamagesource)

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

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

> **Referenced by:** [`BounceObject`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bounceobject), [`Buddy`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-buddy), [`MultiSpawnOnDeath`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-multispawnondeath), [`SpawnOnDeath`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-spawnondeath), [`TransformOnDeathImmediately`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-transformondeathimmediately), [`SpawnOnDeath`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-spawnondeath)

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

> **See Also:** Values from [`object`](#enum-object) may also be valid here (overlapping enum).

</details>


---

### Enum: `portrait_face`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Player_Progression_and_Cats/Cat_Classes.md#object-graphics)

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

### Enum: `render_layer`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `background` | |
| `sorted_distortions` | |
| `splatters` | |
| `top` | |

</details>


---

### Enum: `trigger_adventure_unlock`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward)

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

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

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

> **See Also:** Values from [`cat_has_item_equipped`](#enum-cat_has_item_equipped), [`complete_item_quest`](#enum-complete_item_quest) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`lose_specific_item`](#enum-lose_specific_item), [`choose_cat_with_item`](#enum-choose_cat_with_item), [`CompleteItemQuest`](#enum-completeitemquest), [`RemoveItem`](#enum-removeitem), [`fail_item_quest`](#enum-fail_item_quest).

</details>


---

### Enum: `AddTag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applypassives), [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **See Also:** Values from [`tag`](#enum-tag) may also be valid here (overlapping enum).

</details>


---

### Enum: `DeadAltAbility`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bonus_passives)

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

> **See Also:** Values from [`variant_of`](#enum-variant_of) may also be valid here (overlapping enum).

</details>


---

### Enum: `EquipTemporaryItem`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives), [`StatusAlliesOnBattleStart`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusalliesonbattlestart), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

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

### Enum: `StatusImmunity`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Webbed` | |
| `Poison` | |
| `Burn` | |
| `Tarred` | |

> **See Also:** Values from [`status`](#enum-status), [`AmplifyStatus`](#enum-amplifystatus) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`DoubleStatus`](#enum-doublestatus).

</details>


---

### Enum: `TransformOnDeath`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

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

> **See Also:** Values from [`object`](#enum-object), [`movieclip`](#enum-movieclip) may also be valid here (overlapping enum).

</details>


---

### Enum: `UseAbility`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_hastag), [`Conditional_InForm`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_inform), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`StatusEachRoundEnd`](../Player_Progression_and_Cats/Cat_Mutations.md#object-statuseachroundend), [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`statuses_on_enter_form`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statuses_on_enter_form), [`StatusAfterCastSpell`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusaftercastspell), [`StatusEachTurnBegin`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statuseachturnbegin)

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

### Enum: `cantrip_group`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`cost`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-cost)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `kaiju_roar` | |
| `cavemomtoss` | |
| `spewer_suck` | |
| `THC_CoinRoll` | |

</details>


---

### Enum: `level_up`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`reward`](./Miscellaneous.md#object-reward), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `self` | |
| `all` | |

> **See Also:** Values from [`layer`](#enum-layer), [`make_old`](#enum-make_old) may also be valid here (overlapping enum).

</details>


---

### Enum: `palette`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CatPartsTransform`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-catpartstransform)

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

> **See Also:** Values from [`class`](#enum-class), [`set`](#enum-set), [`pool`](#enum-pool), [`FormChange`](#enum-formchange), [`class_anis`](#enum-class_anis), [`MulticlassLevelUp`](#enum-multiclasslevelup), [`ChangeCatClass`](#enum-changecatclass), [`complete_checklist_with_class`](#enum-complete_checklist_with_class), [`EvolveAbilityFromPool`](#enum-evolveabilityfrompool) may also be valid here (overlapping enum).

</details>


---

### Enum: `range`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AllStatsAura`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-allstatsaura), [`DepressionAura`](../Core_Entities_and_Combat/Elite_Buffs.md#object-depressionaura), [`AbilityWhenTaggedCharacterMovesNear`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-abilitywhentaggedcharactermovesnear), [`AllyHealthRegenAura`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-allyhealthregenaura), [`AllyManaRegenAura`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-allymanaregenaura), [`DamageReductionAura`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-damagereductionaura)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `global` | |

</details>


---

### Enum: `set_savefile_flag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root), [`tink_aggression`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_aggression), [`tink_basestats`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_basestats), [`tink_inbreeding`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_inbreeding), [`tink_relationships`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_relationships), [`tink_sexuality`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_sexuality), [`tink_tags`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_tags)

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

### Enum: `animation_fail`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `10coins`, `5coins`, [`ROOT` (Events_and_Encounters)](../World_Maps_and_Events/Events_and_Encounters.md#object-root), [`buy1`](../World_Maps_and_Events/Events_and_Encounters.md#object-buy1), [`donate_10`](../World_Maps_and_Events/Events_and_Encounters.md#object-donate_10), [`donate_15`](../World_Maps_and_Events/Events_and_Encounters.md#object-donate_15), [`donate_20`](../World_Maps_and_Events/Events_and_Encounters.md#object-donate_20), [`donate_5`](../World_Maps_and_Events/Events_and_Encounters.md#object-donate_5), [`put_in_coins`](../World_Maps_and_Events/Events_and_Encounters.md#object-put_in_coins)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `choice_no_coins` | |

</details>


---

### Enum: `chain_movieclip`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ChainLink` | |
| `Frogchain` | |
| `Bramblechain` | |

</details>


---

### Enum: `learn_passive`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

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
| `TowerDefense` | |

</details>


---

### Enum: `partial_animation_suffix`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Alert`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-alert), [`Bomb`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-bomb), [`Drunker`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-drunker), [`FlushHost`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-flushhost), [`Grappling`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-grappling), [`JohnnyHost`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-johnnyhost), [`Lit`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-lit), [`Primed`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-primed), [`ThrobHost`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-throbhost), [`Unlit`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-unlit), [`Unwashed`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-unwashed)

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

> **Referenced by:** [`BasementUpgrade`](../World_Maps_and_Events/House_and_Environment.md#object-basementupgrade), [`BasementUpgrade2`](../World_Maps_and_Events/House_and_Environment.md#object-basementupgrade2), [`BasementUpgrade3`](../World_Maps_and_Events/House_and_Environment.md#object-basementupgrade3), [`BasementUpgrade4`](../World_Maps_and_Events/House_and_Environment.md#object-basementupgrade4), [`BasementUpgrade5`](../World_Maps_and_Events/House_and_Environment.md#object-basementupgrade5), [`LargeHouse`](../World_Maps_and_Events/House_and_Environment.md#object-largehouse), [`LargeHouse_Floor2Large`](../World_Maps_and_Events/House_and_Environment.md#object-largehouse_floor2large), [`LargeHouse_Floor2Small`](../World_Maps_and_Events/House_and_Environment.md#object-largehouse_floor2small), [`MediumHouse`](../World_Maps_and_Events/House_and_Environment.md#object-mediumhouse), [`MediumHouse_SmallRoom`](../World_Maps_and_Events/House_and_Environment.md#object-mediumhouse_smallroom), [`SmallHouse_Attic`](../World_Maps_and_Events/House_and_Environment.md#object-smallhouse_attic)

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

### Enum: `set_subject`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`reward`](./Miscellaneous.md#object-reward), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `deadrat` | |
| `dimensionx_head2` | |
| `endorb2` | |
| `monkey_paw_1finger` | |
| `monkey_paw_2fingers` | |
| `monkey_paw_3fingers` | |
| `monkey_paw_4fingers` | |
| `subject_frame` | |
| `throbbing_artery_noflesh` | |
| `volcano2` | |
| `wall_of_flesh_noartery` | |

</details>


---

### Enum: `weights`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MoveWhenDamaged`](../Player_Progression_and_Cats/Cat_Mutations.md#object-movewhendamaged), [`MoveAfterAnyAttemptedAttack`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveafteranyattemptedattack), [`MoveAwayWhenEnemyAdjacent`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-moveawaywhenenemyadjacent), [`MoveWhenDamaged`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movewhendamaged), [`MoveWhenDamaged`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-movewhendamaged)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `stay_far_always_move` | |
| `chaotic` | |
| `bat_chaos_runaway` | |
| `stay_near_allies_always_move` | |

> **See Also:** Values from [`move_weights`](#enum-move_weights) may also be valid here (overlapping enum).

</details>


---

### Enum: `ImmediateUseAbility`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_goodroll), [`Conditional_HasTag`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_hastag), [`Else`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-else), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`StatusOnEnemyConfused`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statusonenemyconfused), [`StatusEachTurnEnd`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statuseachturnend), [`StatusOnEndMove`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonendmove)

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

### Enum: `SpawnThingIfHitKills`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HealthThreshold`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_healththreshold), [`Else`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-else), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Food` | |
| `Bait` | |
| `BigFood` | |
| `BiggestFood` | |

> **See Also:** Values from [`object`](#enum-object), [`ObjectOnHit`](#enum-objectonhit) may also be valid here (overlapping enum).

</details>


---

### Enum: `beam_cap`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

### Enum: `color`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Damage_Text_Styles)](../Assets_and_Localization/Damage_Text_Styles.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `gray` | |
| `black` | |
| `white` | |

</details>


---

### Enum: `end`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `spinattackend` | |
| `attack` | |
| `lickAttack` | |
| `monkAttack` | |
| `upswipe` | |

> **See Also:** Values from [`animation`](#enum-animation) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`loop`](#enum-loop), [`start`](#enum-start).

</details>


---

### Enum: `jump_start_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

### Enum: `loop`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |
| `spinattackloop` | |
| `lickAttack` | |
| `monkAttack` | |

> **See Also:** Values from [`animation`](#enum-animation), [`end`](#enum-end), [`start`](#enum-start) may also be valid here (overlapping enum).

</details>


---

### Enum: `neck`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`equipment`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-equipment)

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

### Enum: `orientation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Spawns_and_Enemy_Pools)](../World_Maps_and_Events/Spawns_and_Enemy_Pools.md#object-root), `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `east` | |
| `north` | |
| `south` | |
| `west` | |

</details>


---

### Enum: `override_basic_attack`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `1`, `2`, [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

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

> **See Also:** Values from [`ReplaceBasicAttack`](#enum-replacebasicattack) may also be valid here (overlapping enum).

</details>


---

### Enum: `prime_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

> **See Also:** Values from [`animation`](#enum-animation) may also be valid here (overlapping enum).

</details>


---

### Enum: `right_icon`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Damage_Text_Styles)](../Assets_and_Localization/Damage_Text_Styles.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `divineshield` | |
| `shield` | |
| `mana` | |
| `coin` | |
| `heal` | |

</details>


---

### Enum: `stack_key`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnEachTurn`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-spawneachturn), [`StackingFlowerTrail`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-stackingflowertrail), [`StatusAfterXStacks`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusafterxstacks)

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

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |
| `spinattackstart` | |
| `lickAttack` | |
| `monkAttack` | |

> **See Also:** Values from [`animation`](#enum-animation), [`end`](#enum-end), [`loop`](#enum-loop) may also be valid here (overlapping enum).

</details>


---

### Enum: `trigger_house_boss`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

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

> **See Also:** Values from [`frame_label`](#enum-frame_label), [`beat_house_boss`](#enum-beat_house_boss), [`complete_house_boss`](#enum-complete_house_boss) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`initial_cutscene_night`](#enum-initial_cutscene_night), [`KaijuWinCon`](#enum-kaijuwincon), [`clear_surviving_kaiju`](#enum-clear_surviving_kaiju), [`require_beat_house_boss`](#enum-require_beat_house_boss), [`surviving_kaiju`](#enum-surviving_kaiju).

</details>


---

### Enum: `unlock_room`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BasementUpgrade`](../World_Maps_and_Events/House_and_Environment.md#object-basementupgrade), [`BasementUpgrade2`](../World_Maps_and_Events/House_and_Environment.md#object-basementupgrade2), [`BasementUpgrade3`](../World_Maps_and_Events/House_and_Environment.md#object-basementupgrade3), [`BasementUpgrade4`](../World_Maps_and_Events/House_and_Environment.md#object-basementupgrade4), [`BasementUpgrade5`](../World_Maps_and_Events/House_and_Environment.md#object-basementupgrade5), [`Default`](../World_Maps_and_Events/House_and_Environment.md#object-default), [`LargeHouse_Floor2Large`](../World_Maps_and_Events/House_and_Environment.md#object-largehouse_floor2large), [`LargeHouse_Floor2Small`](../World_Maps_and_Events/House_and_Environment.md#object-largehouse_floor2small), [`MediumHouse_SmallRoom`](../World_Maps_and_Events/House_and_Environment.md#object-mediumhouse_smallroom), [`SmallHouse_Attic`](../World_Maps_and_Events/House_and_Environment.md#object-smallhouse_attic)

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

> **Referenced by:** [`innate_items`](../Player_Progression_and_Cats/Cat_Classes.md#object-innate_items), [`MonkCatReactionAbilities`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-monkcatreactionabilities), [`equipment`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-equipment)

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

### Enum: `AmplifyStatus`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Poison` | |
| `Bleed` | |
| `Rot` | |
| `Burn` | |

> **See Also:** Values from [`status`](#enum-status), [`StatusImmunity`](#enum-statusimmunity) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`DoubleStatus`](#enum-doublestatus).

</details>


---

### Enum: `ChangeTilesUnder`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_hastag), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`Conditional_GoodRoll`](../Player_Progression_and_Cats/Cat_Mutations.md#object-conditional_goodroll), [`StatusOnTookDamage`](../Player_Progression_and_Cats/Cat_Mutations.md#object-statusontookdamage), [`StatusOnBreak`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonbreak)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `WaterTile` | |
| `GlassTile` | |
| `LavaTile` | |
| `DirtTile` | |
| `TallGrassTile` | |

> **See Also:** Values from [`ChangeTile`](#enum-changetile), [`tile`](#enum-tile) may also be valid here (overlapping enum).

</details>


---

### Enum: `arrival_unlock`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `npc_houseboss_intro_guillotina_1` | |
| `npc_houseboss_intro_guillotina_2` | |
| `npc_houseboss_intro_guillotina_3` | |
| `npc_houseboss_intro_pyrophina` | |
| `npc_houseboss_intro_pyrophina_vs_zaratana` | |
| `npc_houseboss_intro_terminator_1` | |
| `npc_houseboss_intro_terminator_2` | |
| `npc_houseboss_intro_terminator_3` | |
| `npc_houseboss_intro_zaratana` | |

</details>


---

### Enum: `choose_cat_with_item`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`intro`](../World_Maps_and_Events/Events_and_Encounters.md#object-intro)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `PutridLeech` | |
| `ThrobbingGristle` | |
| `TransmitterAntenna` | |
| `CryogenicTimeChamber_Full` | |
| `GuillotinasHead` | |
| `ReceiverAntenna` | |

> **See Also:** Values from [`cat_has_item_equipped`](#enum-cat_has_item_equipped), [`complete_item_quest`](#enum-complete_item_quest), [`lose_specific_item`](#enum-lose_specific_item), [`unlock_quest_item`](#enum-unlock_quest_item) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`not_cat_has_item_equipped`](#enum-not_cat_has_item_equipped).

</details>


---

### Enum: `complete_house_boss`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `20`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `guillotina_1` | |
| `guillotina_2` | |
| `guillotina_3` | |
| `pyrophina` | |
| `pyrophina_vs_zaratana` | |
| `terminator_1` | |
| `terminator_2` | |
| `terminator_3` | |
| `zaratana` | |

> **See Also:** Values from [`frame_label`](#enum-frame_label), [`beat_house_boss`](#enum-beat_house_boss), [`trigger_house_boss`](#enum-trigger_house_boss) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`initial_cutscene_night`](#enum-initial_cutscene_night), [`KaijuWinCon`](#enum-kaijuwincon), [`clear_surviving_kaiju`](#enum-clear_surviving_kaiju), [`require_beat_house_boss`](#enum-require_beat_house_boss), [`surviving_kaiju`](#enum-surviving_kaiju).

</details>


---

### Enum: `dead,`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Injuries)](../Player_Progression_and_Cats/Injuries.md#object-root)

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

> **See Also:** Values from [`complete_chapter`](#enum-complete_chapter), [`beat_chapter_boss`](#enum-beat_chapter_boss), [`music`](#enum-music), [`event_piece_frame`](#enum-event_piece_frame), [`chapter_id`](#enum-chapter_id), [`folder`](#enum-folder), [`tileset`](#enum-tileset), [`world_name_frame`](#enum-world_name_frame) may also be valid here (overlapping enum).

</details>


---

### Enum: `repeat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root), [`beanies_quests_repeat`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-beanies_quests_repeat), [`frank_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-frank_max_repeating), [`jack_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-jack_max_repeating), [`organ_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-organ_max_repeating), [`steven_milliontrashed`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-steven_milliontrashed), [`tink_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_max_repeating), [`tracy_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tracy_max_repeating), [`upgrade_storage_repeating_impossible`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-upgrade_storage_repeating_impossible)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `infinite` | |
| `never` | |

</details>


---

### Enum: `save_file_flag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `20`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AntennaQuest_Orb` | |
| `AntennaQuest_Rift` | |
| `AntennaQuest_Volcano` | |
| `MeatWorldQuest_Gristle` | |
| `MeatWorldQuest_Leech` | |
| `mapflag_CoreObeliskUnlocked` | |
| `mapflag_DimensionXUnlocked` | |
| `mapflag_MeatWorldUnlockedFull` | |
| `mapflag_MoonObeliskUnlocked` | |

> **See Also:** Values from [`has_token`](#enum-has_token), [`set_legacy_token`](#enum-set_legacy_token) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`hint_prerequisite_flag`](#enum-hint_prerequisite_flag).

</details>


---

### Enum: `AddElement`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToExplosions`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoexplosions)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Fire` | |
| `Napalm` | |

</details>


---

### Enum: `FreePathfindElement`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives), [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`AddPassivesToMinions`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addpassivestominions), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Grass` | |
| `Water` | |

> **See Also:** Values from [`aoe_tile_requires_element`](#enum-aoe_tile_requires_element) may also be valid here (overlapping enum).

</details>


---

### Enum: `SpawnOnDowned`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CharmedKitten` | |
| `CharmedFly` | |
| `CharmedSpookie` | |

> **See Also:** Values from [`variant_of`](#enum-variant_of), [`object`](#enum-object), [`gain_familiar`](#enum-gain_familiar) may also be valid here (overlapping enum).

</details>


---

### Enum: `back_icon`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Damage_Text_Styles)](../Assets_and_Localization/Damage_Text_Styles.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bleed` | |
| `burn` | |
| `confusion` | |
| `knockback` | |
| `leech` | |
| `mana_leech` | |
| `poison` | |
| `thorns` | |

</details>


---

### Enum: `deadhit,`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Injuries)](../Player_Progression_and_Cats/Injuries.md#object-root)

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

> **Referenced by:** [`FormChangeOffMap`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangeoffmap)

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

> **Referenced by:** [`FormChangeOffMap`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangeoffmap)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Default_Ground` | |
| `Default` | |
| `Insane_Ground` | |
| `FightPhase` | |

</details>


---

### Enum: `max_range`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `level` | |
| `5+2*level` | |
| `2+level` | |
| `3+2*level` | |
| `5+level` | |

</details>


---

### Enum: `on_store`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

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

> **Referenced by:** [`SpawnOnBattleStart`](../Core_Entities_and_Combat/Elite_Buffs.md#object-spawnonbattlestart), `SpawnCatCopyOnBattleStart`, `SpawnCatCopyWhenDowned`, [`SpawnCatCopyOnBattleStart`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawncatcopyonbattlestart)

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

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

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

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

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

> **See Also:** Values from [`trigger_npc_sequence`](#enum-trigger_npc_sequence) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`preempt_npc_sequence`](#enum-preempt_npc_sequence).

</details>


---

### Enum: `sub_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-root)

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

> **Also Used In:** These values are also referenced by [`TeamCastAbility`](#enum-teamcastability).

</details>


---

### Enum: `type_icon`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-meta)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `magic` | |
| `attack` | |
| `buff` | |
| `melee` | |
| `movement` | |
| `spawn` | |

> **See Also:** Values from [`type`](#enum-type) may also be valid here (overlapping enum).

</details>


---

### Enum: `AbilityWhenBuddyDies`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `water` | |

</details>


---

### Enum: `OverrideBasicAttack`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **See Also:** Values from [`attack`](#enum-attack) may also be valid here (overlapping enum).

</details>


---

### Enum: `damage`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TwisterDisplaceWithDamage`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-twisterdisplacewithdamage), [`damage_instance`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-damage_instance)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `inherit` | |
| `durability` | |
| `level` | |

</details>


---

### Enum: `decrement_legacy_counter`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `WorldEventLegacyCounter_CrackInTheWall` | |
| `WorldEventLegacyToken_StartDigging` | |
| `WorldEventLegacyCounter_CustomTokenString` | |

> **See Also:** Values from [`increment_legacy_counter`](#enum-increment_legacy_counter) may also be valid here (overlapping enum).

</details>


---

### Enum: `event`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`next_event_from_set`](../World_Maps_and_Events/Events_and_Encounters.md#object-next_event_from_set), [`ChanceToForceEvent`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-chancetoforceevent)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Tragedy` | |
| `Blessing` | |
| `Death` | |

> **See Also:** Values from [`object`](#enum-object), [`event_now_same_cat`](#enum-event_now_same_cat) may also be valid here (overlapping enum).

</details>


---

### Enum: `land_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `none` | |

</details>


---

### Enum: `max_npc`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `20`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Beanies` | |
| `Butch` | |
| `Frank` | |
| `Jack` | |
| `OrganGrinder` | |
| `Tink` | |
| `Tracy` | |

</details>


---

### Enum: `miss_particle`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `fx_tentaclestrangleMiss` | |

</details>


---

### Enum: `new_layer`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SwitchMusic`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-switchmusic), [`SwitchMusic`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-switchmusic)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `battle` | |
| `event` | |
| `map` | |

> **See Also:** Values from [`type`](#enum-type) may also be valid here (overlapping enum).

</details>


---

### Enum: `npc_script`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](../World_Maps_and_Events/Shops.md#object-meta)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `tracy_adventure_shop_script.gon` | |

</details>


---

### Enum: `AddHiddenTag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bowling_ball` | |
| `grown_hitler_clone` | |
| `hitler_clone_fetus` | |
| `the_nuke_bearer` | |
| `unlit_candle` | |

> **See Also:** Values from [`tag`](#enum-tag), [`target_requires_tag`](#enum-target_requires_tag) may also be valid here (overlapping enum).

</details>


---

### Enum: `ConjureBonusAbility`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives), [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `random` | |
| `Class` | |
| `Colorless` | |
| `Mage` | |

> **See Also:** Values from [`class`](#enum-class), [`ability`](#enum-ability), [`ChangeCatClass`](#enum-changecatclass), [`complete_checklist_with_class`](#enum-complete_checklist_with_class) may also be valid here (overlapping enum).

</details>


---

### Enum: `Divide4OnDeath`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BiggestFood` | |
| `Clot` | |
| `MedSlime` | |
| `MedSlimeX` | |
| `SmallSlime` | |
| `SmallSlimeX` | |

> **See Also:** Values from [`object`](#enum-object), [`movieclip`](#enum-movieclip) may also be valid here (overlapping enum).

</details>


---

### Enum: `ForceUseAbility_NonStack`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_goodroll), [`StatusOnOverHealed`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonoverhealed)

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

> **Referenced by:** [`Conditional_FinishedSpawning`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_finishedspawning), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Tumor` | |
| `BeefyCharmedLeech` | |
| `CharmedLeech` | |
| `Fly` | |

> **See Also:** Values from [`object`](#enum-object), [`movieclip`](#enum-movieclip), [`BounceObject`](#enum-bounceobject), [`ObjectOnHitCharacter`](#enum-objectonhitcharacter) may also be valid here (overlapping enum).

</details>


---

### Enum: `LevelUpClassOverride`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Jester` | |
| `Colorless` | |

> **See Also:** Values from [`class`](#enum-class), [`ChangeCatClass`](#enum-changecatclass), [`complete_checklist_with_class`](#enum-complete_checklist_with_class) may also be valid here (overlapping enum).

</details>


---

### Enum: `ReplaceBasicAttackWhenCastable`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Bionic` | |
| `Cardboard` | |
| `Cool` | |
| `Lucky` | |
| `Paper` | |
| `Wood` | |

> **See Also:** Values from [`set`](#enum-set) may also be valid here (overlapping enum).

</details>


---

### Enum: `TagGreed`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bishop_hat` | |
| `pickup` | |
| `food` | |

> **See Also:** Values from [`tag`](#enum-tag), [`target_requires_tag`](#enum-target_requires_tag) may also be valid here (overlapping enum).

</details>


---

### Enum: `ability_icon`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-meta)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicButcherMeleeWideSpin` | |
| `BasicMelee` | |
| `BasicRanged` | |
| `BasicStraightShot` | |
| `Pestilence` | |
| `Poke` | |

> **See Also:** Values from [`variant_of`](#enum-variant_of), [`attack`](#enum-attack), [`ReplaceBasicAttack`](#enum-replacebasicattack) may also be valid here (overlapping enum).

</details>


---

### Enum: `air_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

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

### Enum: `exclude`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeOnElementInfluence`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangeonelementinfluence), [`BuffImmunity`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-buffimmunity)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `water` | |
| `SpellDamageUp` | |
| `fire` | |

</details>


---

### Enum: `formchange`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Cat`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cat), [`NonCat`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-noncat)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BigHolding` | |
| `BigHoldingCat` | |
| `SmallHolding` | |
| `SmallHoldingCat` | |

> **See Also:** Values from [`FormChange`](#enum-formchange), [`form`](#enum-form) may also be valid here (overlapping enum).

</details>


---

### Enum: `house_upgrade`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`house_upgrade_4throom`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-house_upgrade_4throom), [`house_upgrade_attic`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-house_upgrade_attic), [`house_upgrade_largehouse`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-house_upgrade_largehouse), [`house_upgrade_mediumhouse`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-house_upgrade_mediumhouse)

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

### Enum: `initial_cutscene_night`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `guillotina_1` | |
| `guillotina_2` | |
| `guillotina_3` | |
| `hitler_intro` | |
| `t1000_intro` | |
| `terminator_intro` | |

> **See Also:** Values from [`frame_label`](#enum-frame_label), [`beat_house_boss`](#enum-beat_house_boss), [`trigger_house_boss`](#enum-trigger_house_boss), [`complete_house_boss`](#enum-complete_house_boss) may also be valid here (overlapping enum).

</details>


---

### Enum: `interstitial_bg_frame`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Floor1_Large`](../World_Maps_and_Events/House_and_Environment.md#object-floor1_large), [`Floor1_Small`](../World_Maps_and_Events/House_and_Environment.md#object-floor1_small), [`ROOT` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-root), [`SmallAttic`](../World_Maps_and_Events/House_and_Environment.md#object-smallattic)

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

> **Referenced by:** [`Conditional_FirstApplicationThisTurn`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_firstapplicationthisturn), [`Conditional_OncePerBattle`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_onceperbattle), [`Conditional_OncePerBattle`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_onceperbattle)

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

> **Referenced by:** [`SwitchMusic`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-switchmusic), [`SwitchMusic`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-switchmusic)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `same` | |

</details>


---

### Enum: `not_priming`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeWhilePrimingAbility`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangewhileprimingability)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DualSword` | |
| `NotPriming` | |
| `SwordAndShield` | |

</details>


---

### Enum: `preempt_npc_sequence`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `beanies_bombquest_2` | |
| `beanies_bombquest_3` | |
| `beanies_bombquest_amnesia` | |

> **See Also:** Values from [`trigger_npc_sequence`](#enum-trigger_npc_sequence), [`reset_npc_sequence`](#enum-reset_npc_sequence) may also be valid here (overlapping enum).

</details>


---

### Enum: `priming`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeWhilePrimingAbility`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangewhileprimingability)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DualSword_Primed` | |
| `Priming` | |
| `SwordAndShield_Primed` | |

</details>


---

### Enum: `rematch_cutscene_night`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `house_boss_returns_t1` | |
| `house_boss_returns_t2` | |
| `house_boss_returns_t3` | |
| `house_boss_returns_tina1` | |
| `house_boss_returns_tina2` | |
| `house_boss_returns_tina3` | |

</details>


---

### Enum: `requires_flag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Events_and_Encounters)](../World_Maps_and_Events/Events_and_Encounters.md#object-root), [`main`](../World_Maps_and_Events/Events_and_Encounters.md#object-main)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AlienOvergrowthUnlocked` | |
| `GeomagneticStormUnlocked` | |
| `MeteorShowerUnlocked` | |
| `SolarFlareUnlocked` | |
| `StrangeEggsUnlocked` | |
| `TheShimmerUnlocked` | |

> **See Also:** Values from [`set_legacy_token`](#enum-set_legacy_token) may also be valid here (overlapping enum).

</details>


---

### Enum: `toss_direction_restriction`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

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

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bumblefoot` | |
| `gambit` | |
| `infestedduo` | |
| `jestercat` | |
| `queenhippo` | |
| `ratking` | |

> **See Also:** Values from [`frame_label`](#enum-frame_label) may also be valid here (overlapping enum).

</details>


---

### Enum: `upgrade_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `random` | |
| `Toss` | |

</details>


---

### Enum: `BlacklistPickupType`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `food` | |
| `catnip` | |

</details>


---

### Enum: `CompleteItemQuest`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSourceOnKill`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytosourceonkill), [`Conditional_OncePerBattle`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_onceperbattle), [`ScaldingOrbMoonBossOneShot`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-scaldingorbmoonbossoneshot)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BlackShard` | |
| `Nuke` | |
| `ScaldingOrb` | |

> **See Also:** Values from [`complete_item_quest`](#enum-complete_item_quest), [`unlock_quest_item`](#enum-unlock_quest_item), [`RemoveItem`](#enum-removeitem) may also be valid here (overlapping enum).

</details>


---

### Enum: `DeathRattleRevive`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

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

> **Referenced by:** [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Referenced by:** [`ApplyToSource`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytosource), [`StatusOnKill`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonkill), [`StatusOnKill`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonkill)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`passives`](../Core_Entities_and_Combat/Elite_Buffs.md#object-passives), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MoveOne` | |

</details>


---

### Enum: `ObjectOnHit`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToTile`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytotile), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Bait` | |
| `BiggestFood` | |
| `Carcus` | |
| `FetusNoJar` | |

> **See Also:** Values from [`object`](#enum-object), [`movieclip`](#enum-movieclip), [`SpawnThingIfHitKills`](#enum-spawnthingifhitkills) may also be valid here (overlapping enum).

</details>


---

### Enum: `ObjectOnHitEmpty`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AnimalEgg` | |
| `AnimalEgg2` | |
| `HeadTumor` | |
| `Maggot` | |
| `SmallRock` | |

> **See Also:** Values from [`variant_of`](#enum-variant_of), [`object`](#enum-object), [`movieclip`](#enum-movieclip), [`projectile`](#enum-projectile) may also be valid here (overlapping enum).

</details>


---

### Enum: `SetBrittleImmune`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AdvancedAlloy` | |
| `Alloy` | |
| `EliteAlloy` | |
| `JankAlloy` | |
| `Paper` | |

> **See Also:** Values from [`set`](#enum-set) may also be valid here (overlapping enum).

</details>


---

### Enum: `SpawnObjectOnPopCorpse`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Food` | |
| `Catnip` | |
| `Coin` | |

> **See Also:** Values from [`object`](#enum-object), [`movieclip`](#enum-movieclip) may also be valid here (overlapping enum).

</details>


---

### Enum: `XIsLivingAlliesWithTag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bonus_passives)

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

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Grass` | |
| `Water` | |
| `Earth` | |

> **See Also:** Values from [`InnateElement`](#enum-innateelement) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`FreePathfindElement`](#enum-freepathfindelement).

</details>


---

### Enum: `current_chapter_common`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `current_chapter_rare`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `current_chapter_uncommon`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `current_chapter_very_rare`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `cutscene_on_exit`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`reward`](../World_Maps_and_Events/Events_and_Encounters.md#object-reward)

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

> **Referenced by:** [`SetAnimationAlts`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-setanimationalts), [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `skeletonDead` | |
| `deadShot` | |
| `empty` | |

</details>


---

### Enum: `detatched_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `WaterGush` | |
| `LiquidMetalSpear` | |
| `SpearGuyAttack` | |
| `TinaSpear` | |

</details>


---

### Enum: `drop_on_death`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Consumed`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-consumed), [`Consumed`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-consumed)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `deferred` | |

</details>


---

### Enum: `dying`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SetAnimationAlts`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-setanimationalts), [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

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

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `empty` | |

</details>


---

### Enum: `hint_prerequisite_flag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `mapflag_BothObelisksUnlocked` | |
| `mapflag_DimensionXUnlocked` | |
| `mapflag_MeatWorldUnlocked` | |
| `mapflag_MeatWorldUnlockedFull` | |

> **See Also:** Values from [`save_file_flag`](#enum-save_file_flag) may also be valid here (overlapping enum).

</details>


---

### Enum: `item`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TransformItemOnElementInfluence`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-transformitemonelementinfluence)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `22Rifle` | |
| `AdvancedAlloyArmor` | |
| `AdvancedAlloyHat` | |
| `AdvancedAlloyMask` | |
| `AirHorn` | |
| `AlloyArmor` | |
| `AlloyHat` | |
| `AlloyMask` | |
| `AngryFace` | |
| `BagOfChum` | |
| `BagOfGlass` | |
| `BagOfGlitter` | |
| `BagOfGrass` | |
| `BagOfMeat` | |
| `BagOfRocks` | |
| `BagOfSeeds` | |
| `BagOfStuff` | |
| `BarbedHat` | |
| `BarbedMask` | |
| `BarbedNeck` | |
| `BarbedPaw` | |
| `BarbedScrap` | |
| `Battery` | |
| `BattleAxe` | |
| `BearTraps` | |
| `Bible` | |
| `BiggestStick` | |
| `BigRockHat` | |
| `BigRockMask` | |
| `BigRockNecklace` | |
| `BigSpring` | |
| `BigStick` | |
| `BionicArmor` | |
| `BionicHat` | |
| `BionicMask` | |
| `BirdFeed` | |
| `BirdHead` | |
| `BirdPoopHat` | |
| `BlackCandle` | |
| `Blackjack` | |
| `BlackMushroom` | |
| `BlessedAnointingOil` | |
| `BlessedHalo` | |
| `BlinkingEyeball` | |
| `BloodBucket` | |
| `BloodyBagOfGlass` | |
| `BloodyBearTraps` | |
| `BloodyButterflyKnife` | |
| `BloodyCoin` | |
| `BloodyMeatHook` | |
| `BloodyRazor` | |
| `BloodySoulClaw` | |
| `BloodySpikes` | |
| `BloodyStick` | |
| `Bomb` | |
| `BoneClub` | |
| `BoneMarrow` | |
| `BonesHat` | |
| `BonesMask` | |
| `BonesNeck` | |
| `Bottles` | |
| `BottlesOfBlood` | |
| `BrainCandy` | |
| `Breakfast` | |
| `Bricks` | |
| `BubbleBoy` | |
| `BucketOfAcid` | |
| `BucketOfBlood` | |
| `BucketOfLard` | |
| `BurningCoal` | |
| `ButterBean` | |
| `ButterflyKnife` | |
| `Cancer` | |
| `CarBattery` | |
| `CarvingKnife` | |
| `CatHideArmor` | |
| `CatHideHat` | |
| `CatHideMask` | |
| `Catnip` | |
| `CatnipBig` | |
| `CatPaw` | |
| `CatRib` | |
| `CavemanBeard` | |
| `CavemanEyebrows` | |
| `CavemanNecklace` | |
| `CavemanWig` | |
| `CerebralChip` | |
| `Chainsaw` | |
| `ChaosDevice` | |
| `Cheese` | |
| `Chicken` | |
| `ChumBucket` | |
| `Clover` | |
| `ConjoinedEye` | |
| `CoolRocks` | |
| `CounterfeitCoin` | |
| `CreepyPhoto` | |
| `CrimsonMask` | |
| `CrispPaper` | |
| `Crossbow` | |
| `Crowbar` | |
| `CrownOfHorns` | |
| `CrownOfThorns` | |
| `CryogenicTimeChamber_Empty` | |
| `CryogenicTimeChamber_Full` | |
| `CyborgArmor` | |
| `CyborgHat` | |
| `CyborgMask` | |
| `D6` | |
| `DarkFriend` | |
| `Deathbot` | |
| `DemonicHat` | |
| `DemonicMask` | |
| `DemonicNecklace` | |
| `DinoHat` | |
| `DinoMask` | |
| `DinoNecklace` | |
| `DirtyBionicArmor` | |
| `DiscoBiscuit` | |
| `DryBoneHat` | |
| `DryBoneMask` | |
| `DryBoneNecklace` | |
| `DryIce` | |
| `ElectricCoin` | |
| `EliteAlloyArmor` | |
| `EliteAlloyHat` | |
| `EliteAlloyMask` | |
| `Ember` | |
| `EnergyDrink` | |
| `EstusFlask_Full` | |
| `ExperimentalTreatment` | |
| `ExtraLimb` | |
| `Eyeball` | |
| `EyeOfGod` | |
| `FaceGrub` | |
| `FartFace` | |
| `Feather` | |
| `FeatheredMask` | |
| `FeatheredWing` | |
| `FetusInAJar` | |
| `FingerBone` | |
| `FireFlower` | |
| `FishHook` | |
| `FishNecklace` | |
| `FlowerMix` | |
| `FoodBig` | |
| `FoodMedium` | |
| `FrankBolts` | |
| `FreyedWires` | |
| `FrozenHat` | |
| `FrozenMask` | |
| `FrozenNecklace` | |
| `GallonOfWater` | |
| `Garbage` | |
| `GemstoneBones` | |
| `Geode` | |
| `GlassCannon` | |
| `GlassShard` | |
| `GlowingCoin` | |
| `GlowingSeed` | |
| `GnarledClaw` | |
| `GorgonsEye` | |
| `GrapplingHook` | |
| `Grenade` | |
| `GripTrainer` | |
| `GutsHeart` | |
| `GutsIntestines` | |
| `GutsLiver` | |
| `Hairspray` | |
| `HappyHelmet` | |
| `HardPill` | |
| `HeadGrub` | |
| `HeavyRock` | |
| `HolyTears` | |
| `HumanBrain` | |
| `HumanFleshArmor` | |
| `HumanFleshHat` | |
| `HumanFleshMask` | |
| `HumanHand` | |
| `HumanHead` | |
| `HumanHeart` | |
| `HumanLeg` | |
| `HumanToe` | |
| `HybridMask` | |
| `IceCubes` | |
| `ImmaculateHeart` | |
| `Ipecac` | |
| `JankAlloyArmor` | |
| `JankAlloyHat` | |
| `JankAlloyMask` | |
| `JarOfChaos` | |
| `JarOfRadiatedBlood` | |
| `JarOfRadiation` | |
| `Kandarian` | |
| `Kebab` | |
| `KiloOfCatnip` | |
| `LacedNeedle` | |
| `LargeMeteor` | |
| `LeafyHat` | |
| `LeafyMask` | |
| `LeafyNecklace` | |
| `LeakyBrain` | |
| `LeatherHideMask` | |
| `Lighter` | |
| `LilSlugger` | |
| `LipFiller` | |
| `Log` | |
| `LostSoul` | |
| `LuckyCoin` | |
| `LuckyMask` | |
| `LuckyTwine` | |
| `MagicMirror` | |
| `MagicSeed` | |
| `MatchStick` | |
| `MeatBomb` | |
| `MeatCleaver` | |
| `MeatHook` | |
| `MeatSlugger` | |
| `MeStone` | |
| `MindStone` | |
| `MinerArmor` | |
| `MinerHat` | |
| `MinerImplant` | |
| `MinerMask` | |
| `MiniJetpack` | |
| `MiniNuke` | |
| `Mjolnir` | |
| `ModelingClay` | |
| `Molars` | |
| `MomsKnife` | |
| `MomsRing` | |
| `MoneyBag_Huge` | |
| `MoneyBag_Large` | |
| `MoneyBag_Medium` | |
| `MoneyBag_Small` | |
| `MundaneStone` | |
| `Mushrooms` | |
| `MysteriousDice` | |
| `MysteriousEye` | |
| `NailBoard` | |
| `NailGun` | |
| `NeckGrub` | |
| `Neverstone` | |
| `NuclearKnife` | |
| `ObsidianChunk` | |
| `OcularChip` | |
| `OddRemote` | |
| `OldExtinguisher` | |
| `OldHose` | |
| `PaperRags` | |
| `PartyDetonator` | |
| `Pearl` | |
| `Percs` | |
| `PetrifiedPinky` | |
| `PhoenixHat` | |
| `PhoenixMask` | |
| `PhoenixNecklace` | |
| `Pickaxe` | |
| `Pinwheel` | |
| `Pipe` | |
| `PogoStick` | |
| `PoisonVial` | |
| `PopCap` | |
| `PoundOfFlesh` | |
| `PrincessHat` | |
| `PurpleMushroom` | |
| `PuzzleBox` | |
| `RadarDish` | |
| `RailSpikes` | |
| `RainbowRemote` | |
| `RatBeezer` | |
| `RatBomb` | |
| `RatHat` | |
| `RatHeart` | |
| `RatMask` | |
| `RatNecklace` | |
| `RatTail` | |
| `RazorBlade` | |
| `RecycledArmor` | |
| `RecycledGimpMask` | |
| `RecycledHat` | |
| `RecycledMask` | |
| `Redacted` | |
| `RedCap` | |
| `RedMushroom` | |
| `Revolver` | |
| `RoboArm` | |
| `RockArmor` | |
| `RocketLauncher` | |
| `RockHat` | |
| `RockMask` | |
| `Rocks` | |
| `RockyHat` | |
| `RockyMask` | |
| `RockyNecklace` | |
| `RoidRage` | |
| `RollOfPennies` | |
| `RottenArmor` | |
| `RottenGuts` | |
| `RottenHat` | |
| `RottenMask` | |
| `RottenMeat` | |
| `RubberArmor` | |
| `RubberBat` | |
| `RubberFist` | |
| `RubberHat` | |
| `RubberMask` | |
| `RustedRod` | |
| `RustyRazor` | |
| `SaberToothedHat` | |
| `SaberToothedPelt` | |
| `SackOfMeat` | |
| `SacredHeart` | |
| `SawBlades` | |
| `Scapular` | |
| `ScrapArmor` | |
| `ScrapHat` | |
| `ScrapMask` | |
| `SeedBombs` | |
| `SharpStraw` | |
| `ShoeHorn` | |
| `Shotgun` | |
| `Shovel` | |
| `SixPack` | |
| `SkillStone` | |
| `SlingShot` | |
| `SmallBomb` | |
| `SmallEye` | |
| `SmallMeteor` | |
| `SnaggleTooth` | |
| `Sniper` | |
| `SoulClaw` | |
| `SoyMilk` | |
| `special_appealidol` | |
| `special_comfortidol` | |
| `special_evolutionidol` | |
| `special_fightidol` | |
| `special_healthidol` | |
| `special_stimulationidol` | |
| `special_suppressoridol` | |
| `SpeedBall` | |
| `SpiderInjector` | |
| `SpinalChip` | |
| `Spitball` | |
| `SpoonBender` | |
| `SpottedMushroom` | |
| `SpringBoard` | |
| `StaffOfFlame` | |
| `Stick` | |
| `Stomach` | |
| `StoneHelmet` | |
| `StoneOrbit` | |
| `Stopwatch` | |
| `StorageLocker` | |
| `StrongMagnet` | |
| `StunGun` | |
| `Taser` | |
| `Technology` | |
| `Teleport` | |
| `TeslaCannon` | |
| `Textbook` | |
| `TheBody` | |
| `TheLoner` | |
| `TheMind` | |
| `TheSoul` | |
| `ThickHide` | |
| `ThirdEye` | |
| `TinkererBattery` | |
| `TinkererBiggestStick` | |
| `TinkererBigStick` | |
| `TinkererBottles` | |
| `TinkererCrossbow` | |
| `TinkererGlassShard` | |
| `TinkererLog` | |
| `TinkererSlingShot` | |
| `TinkererStick` | |
| `TinkererTaser` | |
| `TinyPebble` | |
| `TractorBeam` | |
| `TrashCanLid` | |
| `Trowel` | |
| `Turkey` | |
| `TwineArmor` | |
| `TwineHat` | |
| `TwineMask` | |
| `UltraVision3000` | |
| `Upper` | |
| `Uzi` | |
| `VibratingMeteorite` | |
| `VibratingSkull` | |
| `VisionPlugin` | |
| `Wafer` | |
| `WaterBottle_Full` | |
| `Whetstone` | |
| `WitchsEye` | |

| `AAABattery` | |
| `AFriendsFoot` | |
| `AirHorn_Fixed` | |
| `AlienBlaster` | |
| `AlienStalk` | |
| `AlienTech` | |
| `AlluringDoodie` | |
| `AmericanFlag` | |
| `AmoebaFace` | |
| `AmoebaHat` | |
| `AmoebaNeck` | |
| `AnarchistCookbook` | |
| `AncestorsBones` | |
| `AncestorsJaw` | |
| `AncestorsSkull` | |
| `AngelicAura` | |
| `AngelicAura_Terminator` | |
| `AngelicProtection` | |
| `AngelWing` | |
| `AngryFace_Fixed` | |
| `AngryWorm` | |
| `Ankh` | |
| `AnointingOil` | |
| `Antenna` | |
| `Antidote` | |
| `Asteroid` | |
| `AsteroidBelt` | |
| `AstroTaser` | |
| `AtomicMark` | |
| `AttractiveHairClip` | |
| `BabyHair` | |
| `Backpack` | |
| `BadSplinters` | |
| `BagOfBags` | |
| `BallOfBandages` | |
| `BallOfYarn` | |
| `BallPeenHammer` | |
| `Banana` | |
| `Bandage` | |
| `Bandages` | |
| `BanditMask` | |
| `BeanParasite` | |
| `BearTrapMask` | |
| `Beepis` | |
| `BeeStinger` | |
| `BentSpoon` | |
| `BestBud` | |
| `BigToe` | |
| `BigToeCursed` | |
| `Binoculars` | |
| `Bishop` | |
| `BlackBelt` | |
| `BlackShard` | |
| `BlackShard_Glowing` | |
| `BlessedAshes` | |
| `Bling` | |
| `Blubber` | |
| `Bo` | |
| `BodySpray` | |
| `Book` | |
| `BookOfBelial` | |
| `BorisBrain` | |
| `BotflyLarva` | |
| `BoxingCharm` | |
| `Bozo` | |
| `BrainChip` | |
| `BrainInAJar` | |
| `BrainMaggot` | |
| `Brambles` | |
| `BrassKnuckles` | |
| `BrickHat` | |
| `BrickMask` | |
| `BrickNecklace` | |
| `BrokenMirror` | |
| `BrokenMirrorHat` | |
| `BrokenWindow` | |
| `BrownBelt` | |
| `BubbleBoy_Fixed` | |
| `Bug` | |
| `BulbHead` | |
| `BulletproofVest` | |
| `Bullseye` | |
| `BungasBone` | |
| `BungasCrown` | |
| `ButcherHook` | |
| `ButcherHook_Temporary` | |
| `ButcherMask` | |
| `ButcherMask_Terminator` | |
| `ButchersCleaver` | |
| `ButcherSeal` | |
| `CactusHat` | |
| `CactusMask` | |
| `CactusNecklace` | |
| `Callus` | |
| `CambionConception` | |
| `CamoHat` | |
| `CapAndBells` | |
| `CarapaceHat` | |
| `CarapaceMask` | |
| `CarapaceNecklace` | |
| `CardboardArmor` | |
| `CardboardHat` | |
| `CardboardMask` | |
| `CatCollar` | |
| `CatEars` | |
| `CatONineTails` | |
| `CatWhiskers` | |
| `CaveCatClub` | |
| `ChampionsMask` | |
| `ChaosDevice_Fixed` | |
| `CharmingBaby` | |
| `CharonsObal` | |
| `ChefsApron` | |
| `ChildOfTheGlowingOne` | |
| `ChildOfTheGlowingOne2` | |
| `ChildsCrown` | |
| `ChildSkull` | |
| `ChubsCollar` | |
| `ChupacabraTongue` | |
| `CinderBlock` | |
| `Clam` | |
| `ClericHat` | |
| `ClericRelic` | |
| `ClericSeal` | |
| `ClericTears` | |
| `ClownMakeup` | |
| `CoffinArmor` | |
| `CoinBag` | |
| `CoinBag_Terminator` | |
| `CoinPurse` | |
| `ColorlessSeal` | |
| `ColostomyBag` | |
| `Conductor` | |
| `ConfusingHat` | |
| `ConjoinedAmeoba` | |
| `Cookbook` | |
| `CoolGlasses` | |
| `CoolHat` | |
| `CoolShirt` | |
| `Cooties` | |
| `CopycatHat` | |
| `CopycatMask` | |
| `CopycatScarf` | |
| `Cordyceps` | |
| `CowSkull` | |
| `CrimsonMask_Cursed` | |
| `CrownOfChaos` | |
| `CrownOfPestilence` | |
| `Crucifix` | |
| `CrustySock` | |
| `Cunch` | |
| `CursedHairball` | |
| `CursedRock` | |
| `CursedStickman` | |
| `CymothoaExigua` | |
| `DamageTransmitter` | |
| `DeadHummingbird` | |
| `DeathMask` | |
| `DeathShroud` | |
| `DeathsScythe` | |
| `Debris` | |
| `DebrisArmor` | |
| `DebrisHat` | |
| `DebrisMask` | |
| `DemonCore` | |
| `DirtClodHat` | |
| `DirtClodMask` | |
| `DirtClodNeck` | |
| `DivinersCloth` | |
| `DNAMultiplier` | |
| `DoodieMask` | |
| `Dreadlocks` | |
| `DreamCatcher` | |
| `DruidNeck` | |
| `DruidNeck_Terminator` | |
| `DruidSeal` | |
| `DruidsWhistle` | |
| `Dumbell` | |
| `DunceCap` | |
| `DustDevilsHorn` | |
| `DybbuksRib` | |
| `EggSack` | |
| `EmoWig` | |
| `EmptyGenerator` | |
| `EmptyHand` | |
| `EmptySack` | |
| `EmptySyringe` | |
| `EnchantingPoop` | |
| `EnchantingPoop_Cursed` | |
| `Enema` | |
| `EnergyTransmitter` | |
| `EstusFlask_Empty` | |
| `EstusFlask_Half` | |
| `EtherealEyes` | |
| `EtherealRings` | |
| `EtherSoakedRag` | |
| `EuhaplorchisCaliforniensis` | |
| `ExperimentalHat` | |
| `ExperimentalMask` | |
| `ExperimentalNeck` | |
| `ExperimentalTreatment_Fixed` | |
| `Experimentx` | |
| `ExtraSetOfEyes` | |
| `EyeOfRa` | |
| `EyeWorm` | |
| `FaceBrand` | |
| `FaceCovering` | |
| `FaceShards` | |
| `FaceWrap` | |
| `FannyPack` | |
| `FartFace_Fixed` | |
| `Fate` | |
| `FattyHat` | |
| `FattyMask` | |
| `FattyNecklace` | |
| `FeatherDarts` | |
| `FeatheredCap` | |
| `FeatheredNecklace` | |
| `FeatheredVeil` | |
| `FecalHood` | |
| `FecalHood_Cursed` | |
| `FecalMask` | |
| `FecalMask_Cursed` | |
| `FecalNecklace` | |
| `FecalNecklace_Cursed` | |
| `Feebis` | |
| `FeedBag` | |
| `FighterHelm` | |
| `FighterScar` | |
| `FighterSeal` | |
| `FighterShoulderPad` | |
| `Fireworks` | |
| `FleshKid` | |
| `FleshShroud` | |
| `Flower` | |
| `FlowerHat` | |
| `FlowerMask` | |
| `FlowerNecklace` | |
| `FlyHat` | |
| `FlyLarva` | |
| `FlyMask` | |
| `FlyNeck` | |
| `FocusBand` | |
| `ForbiddenFruit` | |
| `ForbiddenPill` | |
| `Fork` | |
| `FortuneNecklace` | |
| `FreezingBaby` | |
| `FriendlyAmoeba` | |
| `FriendshipBracelet` | |
| `FryingPan` | |
| `Fukumen` | |
| `FurnitureBox` | |
| `FurnitureBox_Rare` | |
| `FuryDice` | |
| `GambitsDice` | |
| `GemstoneArmor` | |
| `GemstoneHat` | |
| `GemstoneMask` | |
| `GimpArmor` | |
| `GimpHat` | |
| `GimpMask` | |
| `Girder` | |
| `Gizzard` | |
| `GlassCannon_Fixed` | |
| `Glasses` | |
| `Glitch` | |
| `GlowingBone` | |
| `GlowingPelt` | |
| `Glue` | |
| `GlyphOfProtection` | |
| `Gobbler` | |
| `GoldenEgg` | |
| `GoldenIdol` | |
| `GoldenPickaxe` | |
| `GoldenTooth` | |
| `GreenDrink` | |
| `GreenmanMask` | |
| `GreenWhistle` | |
| `GuillotinasHead` | |
| `GunslingerPistol` | |
| `Halo` | |
| `HardPill_Fixed` | |
| `HarpysClaw` | |
| `HeadBrand` | |
| `HeadCheese` | |
| `HeadSpring` | |
| `HeadWrap` | |
| `HealingGauze` | |
| `HealWorm` | |
| `Heartworm` | |
| `HeavyMace` | |
| `HellHook` | |
| `Helmet` | |
| `HexagramSigil` | |
| `HitlersMustache` | |
| `HitlersPistol` | |
| `HitlersToupe` | |
| `HockeyMask` | |
| `HolyGrail` | |
| `HolyWater` | |
| `HookedNecklace` | |
| `Hookworm` | |
| `Horns` | |
| `HorseBlinders` | |
| `HotLunch` | |
| `HumanFoot` | |
| `HunterCap` | |
| `HunterMonocle` | |
| `HunterQuiver` | |
| `HunterSeal` | |
| `HuntersFlute` | |
| `HuntersPatch` | |
| `HuntersPatch_Terminator` | |
| `HybridHat` | |
| `HybridNecklace` | |
| `InfamousMask` | |
| `InfinityArrow` | |
| `Intruder` | |
| `IronJaw` | |
| `IrradiatedObject` | |
| `IrradiatedObject_Bleed` | |
| `IrradiatedObject_Bruise` | |
| `IrradiatedObject_Burn` | |
| `IrradiatedObject_Charmed` | |
| `IrradiatedObject_Confusion` | |
| `IrradiatedObject_Fear` | |
| `IrradiatedObject_Poison` | |
| `IrradiatedObject_Sleep` | |
| `IrradiatedObject_Stun` | |
| `IrradiatedObject_Weakness` | |
| `JarOfLeeches` | |
| `JarOfNothing` | |
| `Jazzercise` | |
| `JesterCap` | |
| `JesterHat` | |
| `JesterHat_Terminator` | |
| `JesterSeal` | |
| `JewelOfDrog` | |
| `Jitte` | |
| `JohnnysStool` | |
| `JohnnysUndies` | |
| `JokerCard` | |
| `Kidney` | |
| `KingsCrown` | |
| `Knight` | |
| `Lard` | |
| `LeadHelmet` | |
| `LeadMask` | |
| `LeadShoulderPads` | |
| `LearnAbility` | |
| `LearnDisorder` | |
| `LearnPassive` | |
| `LeatherArmor` | |
| `LeatherHat` | |
| `LeatherJacket` | |
| `LeatherMask` | |
| `LeechBrood` | |
| `LeechNecklace` | |
| `Libra` | |
| `Lice` | |
| `LilBattery` | |
| `LilKitty` | |
| `LilTumor` | |
| `LionMane` | |
| `LiquidMetal` | |
| `LiquidNitrogen` | |
| `LoansharksFedora` | |
| `LuciferSigil` | |
| `LuckyArmor` | |
| `LuckyCoinPurse` | |
| `LuckyHat` | |
| `LuckyPenny` | |
| `LuckyToe` | |
| `LunchBox` | |
| `MageCollar` | |
| `MageCollar_Terminator` | |
| `MageHat` | |
| `MageRobe` | |
| `MageScarf` | |
| `MageSeal` | |
| `MagicMirror_Fixed` | |
| `Magneto` | |
| `Malaria` | |
| `MamaLeech` | |
| `MammothTusk` | |
| `ManGlasses` | |
| `MangyWig` | |
| `ManHair` | |
| `ManholeCover` | |
| `ManTie` | |
| `MarkIV` | |
| `MarkOfTheBeast` | |
| `MeatCube` | |
| `MedicalHat` | |
| `MedicalMask` | |
| `MedicalNecklace` | |
| `MedicHat` | |
| `MedievalHelmet` | |
| `MeekStone` | |
| `MegaAlienBlaster` | |
| `MegaPoop` | |
| `MelonBaller` | |
| `MeStone_Fixed` | |
| `MetalCoat` | |
| `MetalPlate` | |
| `MetalPlate_Terminator` | |
| `MetalRod` | |
| `MetalSquare` | |
| `Metronome` | |
| `MinersBeard` | |
| `MiniMoon` | |
| `MissingNipple` | |
| `ModelingClay_Default` | |
| `MoltenHat` | |
| `MoltenMask` | |
| `MoltenNecklace` | |
| `MomsToeNail` | |
| `MonkFist` | |
| `MonkMask` | |
| `MonkMask_Terminator` | |
| `MonkSeal` | |
| `MonkStyleChanger` | |
| `Monocle` | |
| `MorphineDrip` | |
| `MothersHat` | |
| `MothersLove` | |
| `MothersMask` | |
| `MothersNecklace` | |
| `MothersTeeth` | |
| `MudMask` | |
| `MuertosMask` | |
| `MuggerMask` | |
| `Multiplier` | |
| `MushroomHat` | |
| `Mustache` | |
| `Muzzle` | |
| `MyShadow` | |
| `MysteriousBone` | |
| `MysteriousDice_Fixed` | |
| `MysticalBlindfold` | |
| `MysticEye` | |
| `NaegleriaFowleri` | |
| `Natural20` | |
| `NeckWrap` | |
| `Necro_SoulDagger_Charged` | |
| `Necro_SoulDagger_Uncharged` | |
| `NecromancerMask` | |
| `NecromancerMask_Terminator` | |
| `NecromancerSeal` | |
| `Necronomicon` | |
| `NightmareHat` | |
| `Nightshade` | |
| `NinjaBandana` | |
| `NinnyStick` | |
| `NubsCollar` | |
| `NuclearKnife_Fixed` | |
| `NuclearKnife_Glowing` | |
| `Nuke` | |
| `NurseHat` | |
| `NurseMask` | |
| `NurseNecklace` | |
| `OakHelmet` | |
| `ObeliskArmor` | |
| `ObeliskHat` | |
| `ObeliskMask` | |
| `Obi` | |
| `Ocarina` | |
| `OddMedallion` | |
| `OddRemote_Enemy` | |
| `OldShoe` | |
| `PackOfBlades` | |
| `PaperArmor` | |
| `PaperHat` | |
| `PaperMask` | |
| `Parousworm` | |
| `PartyDetonator_Fixed` | |
| `Pawn` | |
| `PawShards` | |
| `PCP` | |
| `PeaceSymbol` | |
| `PeaceSymbolFacePaint` | |
| `Pebble` | |
| `Pebble_Terminator` | |
| `PentagramSigil` | |
| `PersuasionDevice` | |
| `PersuasionDevice_Fixed` | |
| `PetrifiedPoop` | |
| `PhantomMask` | |
| `PharaohStaff` | |
| `PinsAndNeedles` | |
| `Pinworm` | |
| `Pliers` | |
| `PolymorphRemote` | |
| `Polyp` | |
| `Poncho` | |
| `PoopHat` | |
| `PoundOfFlesh_Cursed` | |
| `PrayerBeads` | |
| `PrayerCard` | |
| `PrincessHat_Fixed` | |
| `Probe` | |
| `PropellerCap` | |
| `ProtectionTransmitter` | |
| `ProwlersCap` | |
| `ProwlersMask` | |
| `ProwlersVial` | |
| `PsychicMask` | |
| `PsychicMask_Terminator` | |
| `PsychicSeal` | |
| `PullTab` | |
| `PurpleDrink` | |
| `PutridLeech` | |
| `PutridPile` | |
| `PyrophinasCollar` | |
| `PyrophinasToenail` | |
| `QuartzNecklace` | |
| `Queen` | |
| `QueensCrown` | |
| `Rabiesface` | |
| `RadGlasses` | |
| `RadioactiveHat` | |
| `RadioactiveMask` | |
| `RadioactiveNecklace` | |
| `RagArmor` | |
| `RageJuice` | |
| `RagHood` | |
| `RagMask` | |
| `RainHat` | |
| `RainStaff` | |
| `RaptorEgg` | |
| `RavenFeather` | |
| `ReceiverAntenna` | |
| `Redacted_Fixed` | |
| `RedCap_Cursed` | |
| `RedDrink` | |
| `RedPill` | |
| `RhinestoneStickers` | |
| `RingOfFrost` | |
| `RingOfMushrooms` | |
| `Ringworm` | |
| `RisingSunBandana` | |
| `RoboticArm` | |
| `Rook` | |
| `Roundworm` | |
| `RubberBand` | |
| `RubberCement` | |
| `Ruffle` | |
| `RuneofHagalaz` | |
| `RuneofJera` | |
| `RuneofPerthro` | |
| `RustingHelmet` | |
| `SabertoothTigerPelt` | |
| `SacculinaCarcini` | |
| `SamsonsChains` | |
| `SamsonsChains_Terminator` | |
| `SatanicBible` | |
| `Scabies` | |
| `ScaldingOrb` | |
| `Scarf` | |
| `ScaryBaby` | |
| `ScorchedEarth` | |
| `ScrapBag` | |
| `ScrappersBackpack` | |
| `ScrappersHat` | |
| `ScrappersMask` | |
| `Scrubs` | |
| `SelfDestructButton` | |
| `SharkTooth` | |
| `ShoePolish` | |
| `SignalAmplifier` | |
| `SitrusBerry` | |
| `SkillSplit` | |
| `SkullClamp` | |
| `SkullOfGlorg` | |
| `SlagMight` | |
| `SlagTight` | |
| `SleepDart` | |
| `SleepDart2` | |
| `Slime` | |
| `SlimyHat` | |
| `SlimyMask` | |
| `SlimyNecklace` | |
| `SludgeHat` | |
| `SludgeMask` | |
| `SludgeNeck` | |
| `SmallRune` | |
| `SmellingSalts` | |
| `SnakeEyes` | |
| `SnakeskinHat` | |
| `SoulJar` | |
| `SoulJar_Full` | |
| `SoulSucker` | |
| `SpaceAntenna` | |
| `SpaceBoosters` | |
| `SpaceHelmet` | |
| `SpareParts` | |
| `SpearOfDestiny` | |
| `SpellBook` | |
| `SpiderBaby` | |
| `SpiderEgg` | |
| `SpiderHat` | |
| `SpiderInjector_Fixed` | |
| `SpiderWebber` | |
| `SpikedCollar` | |
| `Spinnerets` | |
| `SplinteredCrown` | |
| `Splinters` | |
| `Spring` | |
| `Stacy100` | |
| `Star` | |
| `SteelBall` | |
| `StemCells` | |
| `Steroids` | |
| `StevenHat1` | |
| `StevenHat2` | |
| `StevenMarrow` | |
| `StevenMask1` | |
| `StevenMask2` | |
| `StevenNeck1` | |
| `StevenNeck2` | |
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
| `StevenStone` | |
| `StevenTrinket1` | |
| `StevenTrinket2` | |
| `StevenWeapon1` | |
| `StevenWeapon2` | |
| `Stickman` | |
| `Stopwatch_Fixed` | |
| `StorageLocker_Fixed` | |
| `StrangeMarble` | |
| `StunningBeard` | |
| `StunningChain` | |
| `StunningHaircut` | |
| `SuperBandage` | |
| `SuperDunceCap` | |
| `SuperheroCape` | |
| `SuperheroHat` | |
| `SuperheroMask` | |
| `SurvivalistGaiter` | |
| `SurvivalistMask` | |
| `TankHelmet` | |
| `TankJuice` | |
| `TankPads` | |
| `TankSeal` | |
| `TankTattoo` | |
| `TankToy` | |
| `Tapeworm` | |
| `TarotDeck` | |
| `TatteredScrap` | |
| `TentacleHat` | |
| `TentacleMask` | |
| `TentacleNeck` | |
| `TerminatorCoolGlasses` | |
| `TerminatorCoolGlasses2` | |
| `TerminatorShotgun` | |
| `TerminatorSniper` | |
| `TerminatorUzi` | |
| `TheBlackBox` | |
| `TheBox` | |
| `TheBoxCardboard` | |
| `TheBoxChest` | |
| `TheLoner_Fixed` | |
| `ThePact` | |
| `TheRelic` | |
| `TheTick` | |
| `ThiefCloak` | |
| `ThiefHood` | |
| `ThiefSeal` | |
| `ThiefTattoo` | |
| `ThrobbingCrown` | |
| `ThrobbingGristle` | |
| `ThrummingCharm` | |
| `ThrummingCirclet` | |
| `ThrummingSpectacles` | |
| `TieDyeBandana` | |
| `TinasBellyButton` | |
| `TinasFriend` | |
| `TinasLarynx` | |
| `TinfoilHat` | |
| `TinkererHat` | |
| `TinkererHat_Terminator` | |
| `TinkererSeal` | |
| `TinkerTools` | |
| `TinksBow` | |
| `TinyCage` | |
| `TinyPlanet` | |
| `Tombstone` | |
| `ToolBox` | |
| `TopHat` | |
| `ToxicCanister` | |
| `ToyGun` | |
| `TrainingBand` | |
| `TransmitterAntenna` | |
| `TrashCan` | |
| `Triachnid` | |
| `TutorialStick` | |
| `TV` | |
| `TwoOfSpades` | |
| `UltraVision3000_Fixed` | |
| `UnderworldStaff` | |
| `UnstableDNA` | |
| `UraniumRod` | |
| `USAShield` | |
| `UsedArmor` | |
| `UsedHat` | |
| `UsedMask` | |
| `VeinyArmor` | |
| `VeinyHat` | |
| `VeinyMask` | |
| `VideoGameCart` | |
| `ViperBottle` | |
| `WaterBottle_Empty` | |
| `WaterBottle_Half` | |
| `WaterFeeder` | |
| `Weight` | |
| `WeirdEgg` | |
| `WesternHat` | |
| `Whistle` | |
| `WhiteBelt` | |
| `WhiteRabbitPaw` | |
| `Wig` | |
| `WishBone` | |
| `WitchesCape` | |
| `WitchesHat` | |
| `WitchesNose` | |
| `WizCheese` | |
| `WoodArmor` | |
| `WoodHat` | |
| `WoodMask` | |
| `ZaratanasCollar` | |
| `ZaratanaTurd` | |
| `ZodiacsPoncho` | |
| `ZodiacsSixshooter` | |
| `Zukin` | |

</details>


---

### Enum: `learn_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BarfBall` | |
| `FutureSight` | |
| `Toss` | |

> **See Also:** Values from [`variant_of`](#enum-variant_of) may also be valid here (overlapping enum).

</details>


---

### Enum: `make_old`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `self` | |
| `all` | |

> **See Also:** Values from [`layer`](#enum-layer), [`level_up`](#enum-level_up) may also be valid here (overlapping enum).

</details>


---

### Enum: `material`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `distorter` | |
| `mist` | |

</details>


---

### Enum: `minion_alt`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Elite_Buffs)](../Core_Entities_and_Combat/Elite_Buffs.md#object-root)

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

> **Referenced by:** [`Consumed`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-consumed), [`Consumed`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-consumed)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `sfx`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeOnElementInfluence`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangeonelementinfluence)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FireExtinguish` | |

</details>


---

### Enum: `spurt`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `GibsBloodSpurt` | |
| `GibsBloodSpurtHuge` | |
| `PassiveTarSplat` | |
| `VolcanoSpurt_Trail` | |

</details>


---

### Enum: `tag_location`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Spawns_and_Enemy_Pools)](../World_Maps_and_Events/Spawns_and_Enemy_Pools.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ChaosValidPosition` | |
| `FinalBossCloneSpot` | |
| `FinalBossTheChildLocation` | |
| `HitlerMiniInitial` | |

> **Also Used In:** These values are also referenced by [`special_tile_tag`](#enum-special_tile_tag).

</details>


---

### Enum: `tag_restriction`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TeamCastAbility`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-teamcastability), [`SecurityBotProtect`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-securitybotprotect)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `collective` | |
| `dinofamily` | |
| `dc_cat` | |

> **See Also:** Values from [`hidden_tag`](#enum-hidden_tag) may also be valid here (overlapping enum).

</details>


---

### Enum: `upgrade_passive`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `random` | |
| `TowerDefense` | |

</details>


---

### Enum: `walk`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CookedChickenLeg` | |

</details>


---

### Enum: `BounceRock`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

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

> **Referenced by:** [`CanApplyToInanimate`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-canapplytoinanimate)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SmallRock` | |
| `Coin` | |

> **See Also:** Values from [`variant_of`](#enum-variant_of), [`object`](#enum-object), [`movieclip`](#enum-movieclip), [`ObjectOnHitCharacter`](#enum-objectonhitcharacter) may also be valid here (overlapping enum).

</details>


---

### Enum: `ChangeTileOnPop`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CreepTile` | |
| `GlitchTile` | |
| `OilTile` | |

> **See Also:** Values from [`ChangeTile`](#enum-changetile), [`tile`](#enum-tile) may also be valid here (overlapping enum).

</details>


---

### Enum: `DisableAbilities`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `GrenadeExplode` | |
| `MoonHead_Blow` | |
| `TheChild_Wrath` | |
| `attack` | |

> **See Also:** Values from [`ability`](#enum-ability), [`attack`](#enum-attack), [`do`](#enum-do) may also be valid here (overlapping enum).

</details>


---

### Enum: `EnableWeather`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `water` | |

</details>


---

### Enum: `GroundFlopper`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DefaultMove` | |
| `MoveOne` | |

> **See Also:** Values from [`variant_of`](#enum-variant_of), [`move`](#enum-move) may also be valid here (overlapping enum).

</details>


---

### Enum: `KillsToMeat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Food` | |

</details>


---

### Enum: `LoopingSoundWhileAlive`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

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

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Sprout` | |
| `StemCat_HalfHealth` | |
| `TheDestroyer` | |
| `Tormentor` | |

> **See Also:** Values from [`movieclip`](#enum-movieclip) may also be valid here (overlapping enum).

</details>


---

### Enum: `RemoveItem`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSourceOnKill`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytosourceonkill), [`ScaldingOrbMoonBossOneShot`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-scaldingorbmoonbossoneshot)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BlackShard_Glowing` | |
| `BlackShard` | |
| `ScaldingOrb` | |

> **See Also:** Values from [`complete_item_quest`](#enum-complete_item_quest), [`unlock_quest_item`](#enum-unlock_quest_item), [`CompleteItemQuest`](#enum-completeitemquest) may also be valid here (overlapping enum).

</details>


---

### Enum: `TeamCastAbility`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Huddle_Impl` | |
| `Spin` | |
| `TeamFlex_Impl` | |
| `TeamFlex_Impl2` | |

> **See Also:** Values from [`variant_of`](#enum-variant_of), [`sub_ability`](#enum-sub_ability) may also be valid here (overlapping enum).

</details>


---

### Enum: `TileTrail_Ahead`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-temporary_effects), [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FireTile` | |
| `FlowerTile` | |
| `OilTile` | |
| `WaterTile` | |

> **See Also:** Values from [`ChangeTile`](#enum-changetile), [`tile`](#enum-tile), [`TileTrail`](#enum-tiletrail) may also be valid here (overlapping enum).

</details>


---

### Enum: `WeremanTransformationReceiver`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

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

> **Referenced by:** [`Rain`](../World_Maps_and_Events/House_and_Environment.md#object-rain), [`Snow`](../World_Maps_and_Events/House_and_Environment.md#object-snow), [`Thunderstorm`](../World_Maps_and_Events/House_and_Environment.md#object-thunderstorm), [`Windy`](../World_Maps_and_Events/House_and_Environment.md#object-windy)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Rain` | |
| `Snow` | |
| `Thunderstorm` | |
| `Windy` | |

</details>


---

### Enum: `damage_tiles`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-dodamage), [`DoDamage`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-dodamage)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `all` | |

</details>


---

### Enum: `fail_item_quest`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `JarOfChaos` | |
| `JarOfRadiatedBlood` | |
| `JarOfRadiation` | |
| `Nuke` | |

> **See Also:** Values from [`cat_has_item_equipped`](#enum-cat_has_item_equipped), [`complete_item_quest`](#enum-complete_item_quest), [`unlock_quest_item`](#enum-unlock_quest_item), [`unlock_item_quest`](#enum-unlock_item_quest) may also be valid here (overlapping enum).

</details>


---

### Enum: `goto`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](../World_Maps_and_Events/Events_and_Encounters.md#object-main)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `end` | |

</details>


---

### Enum: `heal_disorder`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `mental_disorders` | |
| `Anxiety` | |
| `diseases` | |

> **See Also:** Values from [`gain_disorder_from_pool`](#enum-gain_disorder_from_pool) may also be valid here (overlapping enum).

</details>


---

### Enum: `hit`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

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

> **Referenced by:** [`TransformInXTurns`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-transforminxturns)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `keep_turns_end_turn` | |

</details>


---

### Enum: `learn_ability_from_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Necromancer` | |
| `AnyUnlocked` | |

> **See Also:** Values from [`learn_passive_from_pool`](#enum-learn_passive_from_pool) may also be valid here (overlapping enum).

</details>


---

### Enum: `lose_item_from_inventory`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cat` | |

</details>


---

### Enum: `next_event_from_set`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](../World_Maps_and_Events/Events_and_Encounters.md#object-main), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CatHole` | |
| `Tragedy` | |
| `WatchingHead2` | |
| `misc_events.gon` | |

> **See Also:** Values from [`event_now_same_cat`](#enum-event_now_same_cat) may also be valid here (overlapping enum).

</details>


---

### Enum: `post_combat_cutscene`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `obelisk1_core` | |
| `obelisk1_moon` | |
| `obelisk2_core` | |
| `obelisk2_moon` | |

</details>


---

### Enum: `return_as`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`leave_party_temporarily`](../World_Maps_and_Events/Events_and_Encounters.md#object-leave_party_temporarily)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `enemy` | |

</details>


---

### Enum: `return_during`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`leave_party_temporarily`](../World_Maps_and_Events/Events_and_Encounters.md#object-leave_party_temporarily)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `boss` | |

</details>


---

### Enum: `skybox_frame`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Rain`](../World_Maps_and_Events/House_and_Environment.md#object-rain), [`Snow`](../World_Maps_and_Events/House_and_Environment.md#object-snow), [`Thunderstorm`](../World_Maps_and_Events/House_and_Environment.md#object-thunderstorm), [`Windy`](../World_Maps_and_Events/House_and_Environment.md#object-windy)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `day_rain` | |
| `day_snow` | |
| `day_thunderstorm` | |
| `day_windy` | |

</details>


---

### Enum: `status_explosion_override`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`EMP`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-emp)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `WaterConduct` | |

</details>


---

### Enum: `stunned`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dead` | |
| `idleDisassembled` | |

> **See Also:** Values from [`weak`](#enum-weak) may also be valid here (overlapping enum).

</details>


---

### Enum: `tag_filter`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusCharactersOnRoundEnd`](../World_Maps_and_Events/House_and_Environment.md#object-statuscharactersonroundend), [`AddPassivesToMinions`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addpassivestominions), [`AddPassivesToMinions`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addpassivestominions)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `crow` | |
| `grub_familiar` | |
| `rock` | |

> **See Also:** Values from [`tag`](#enum-tag) may also be valid here (overlapping enum).

</details>


---

### Enum: `tags`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `consumable` | |

</details>


---

### Enum: `threshold`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AbilityHealthThreshold`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-abilityhealththreshold)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `1*champion_multiplier` | |
| `2*champion_multiplier` | |
| `3*champion_multiplier` | |
| `4*champion_multiplier` | |

</details>


---

### Enum: `trap`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnExtraThingsOnBattleStart`](../World_Maps_and_Events/House_and_Environment.md#object-spawnextrathingsonbattlestart), [`ROOT` (Spawns_and_Enemy_Pools)](../World_Maps_and_Events/Spawns_and_Enemy_Pools.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BearTrap` | |
| `LandMine` | |
| `WaterKittenTrap` | |
| `WebTrap` | |

> **See Also:** Values from [`variant_of`](#enum-variant_of) may also be valid here (overlapping enum).

</details>


---

### Enum: `trigger_npc_sequence_tomorrow`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `butch_boneyard_intro` | |
| `frank_caves_intro` | |
| `jack_desert_intro` | |
| `organ_boneyard_intro` | |

</details>


---

### Enum: `unlock_item_quest`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CryogenicTimeChamber_Full` | |
| `JarOfChaos` | |
| `JarOfRadiatedBlood` | |
| `TinasHead` | |

> **See Also:** Values from [`cat_has_item_equipped`](#enum-cat_has_item_equipped), [`complete_item_quest`](#enum-complete_item_quest), [`fail_item_quest`](#enum-fail_item_quest) may also be valid here (overlapping enum).

</details>


---

### Enum: `unlock_npc_tomorrow`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `beanies` | |
| `jack` | |
| `steven` | |
| `tracy` | |

> **See Also:** Values from [`subject_frame`](#enum-subject_frame) may also be valid here (overlapping enum).

> **Also Used In:** These values are also referenced by [`requires_unlocked_npc`](#enum-requires_unlocked_npc).

</details>


---

### Enum: `visit_chapter`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dimensionx` | |
| `future` | |
| `iceage` | |
| `theend` | |

> **See Also:** Values from [`complete_chapter`](#enum-complete_chapter), [`beat_chapter_boss`](#enum-beat_chapter_boss), [`music`](#enum-music), [`event_piece_frame`](#enum-event_piece_frame), [`chapter_id`](#enum-chapter_id), [`folder`](#enum-folder), [`tileset`](#enum-tileset), [`world_name_frame`](#enum-world_name_frame), [`hint_destination`](#enum-hint_destination), [`hint_chapter_exit`](#enum-hint_chapter_exit) may also be valid here (overlapping enum).

</details>


---

### Enum: `weak`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dead` | |
| `idleDisassembled` | |

> **See Also:** Values from [`stunned`](#enum-stunned) may also be valid here (overlapping enum).

</details>


---

### Enum: `AbilityEnableIfConsumedCharacterHasTag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `sp_pill_fire` | |
| `sp_pill_normal` | |
| `sp_pill_tar` | |

> **See Also:** Values from [`hidden_tag`](#enum-hidden_tag) may also be valid here (overlapping enum).

</details>


---

### Enum: `BreakOnElement`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `water` | |

</details>


---

### Enum: `CobraReflex`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicMonkMelee` | |

</details>


---

### Enum: `DigestDeadBodies`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

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

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Bleed` | |
| `Burn` | |
| `Poison` | |

> **See Also:** Values from [`status`](#enum-status), [`StatusImmunity`](#enum-statusimmunity), [`AmplifyStatus`](#enum-amplifystatus) may also be valid here (overlapping enum).

</details>


---

### Enum: `DropAsFamiliarOnArmorBreak`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

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

> **Referenced by:** [`effects`](../World_Maps_and_Events/House_and_Environment.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `alien` | |
| `ghost` | |
| `robot` | |

> **See Also:** Values from [`tag`](#enum-tag) may also be valid here (overlapping enum).

</details>


---

### Enum: `FindExtraItemFromPoolOnBattleEnd`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../World_Maps_and_Events/House_and_Environment.md#object-effects), [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

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

> **Referenced by:** [`ApplyToSource`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytosource), [`StatusOnBattleEnd`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonbattleend), [`StatusOnBreak`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonbreak)

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

> **Referenced by:** [`TimeDelayStatusApplication`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-timedelaystatusapplication), [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`FinalBossBecomeTheChild`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-finalbossbecomethechild)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MegaGuppy` | |

</details>


---

### Enum: `KnockbackDirectionIsFacingDirection`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BBTransformMutant` | |

</details>


---

### Enum: `PoopWhenHit`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Poop` | |

</details>


---

### Enum: `ReplaceBasicMove_Mutation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives)

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

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`PassiveGroup`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivegroup)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `euphoric` | |
| `insane` | |

</details>


---

### Enum: `SpawnCustomTrap`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CharmTrap` | |
| `EggSackTrap` | |
| `SpikeTrap` | |

> **See Also:** Values from [`variant_of`](#enum-variant_of), [`projectile`](#enum-projectile) may also be valid here (overlapping enum).

</details>


---

### Enum: `TowerDefenseReflex`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Referenced by:** [`StatusOnKill`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statusonkill)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BBTransformZealot` | |
| `GenericRage` | |

</details>


---

### Enum: `aoe_pierce_mode`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `block` | |

</details>


---

### Enum: `background_extra_shader`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `crazyeye` | |
| `meatpulse` | |
| `water` | |

</details>


---

### Enum: `bg_placements_frame`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`House1`](../World_Maps_and_Events/House_and_Environment.md#object-house1), [`House2`](../World_Maps_and_Events/House_and_Environment.md#object-house2), [`House3`](../World_Maps_and_Events/House_and_Environment.md#object-house3)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `large` | |
| `small` | |

</details>


---

### Enum: `core`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas), [`prereqs`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-prereqs)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_CORE` | |
| `mapflag_CoreUnlocked` | |
| `mapflag_IceAgeUnlocked` | |

</details>


---

### Enum: `craft_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TinkererBasicAttackSwitching`](../Player_Progression_and_Cats/Cat_Classes.md#object-tinkererbasicattackswitching), [`TinkererBasicAttackSwitching`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-tinkererbasicattackswitching)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TinkererCraft` | |

</details>


---

### Enum: `dash_decelerating_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `dashslow` | |

</details>


---

### Enum: `deadhit`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `skeletonCorpseHit` | |

</details>


---

### Enum: `dimensionx`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas), [`prereqs`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-prereqs)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_DIMENSIONX` | |
| `mapflag_DimensionXUnlocked` | |
| `mapflag_IceAgeUnlocked` | |

</details>


---

### Enum: `disallow_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`properties`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-properties)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Nuke` | |
| `all` | |

</details>


---

### Enum: `emit_timespread_curve`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ease_out` | |

</details>


---

### Enum: `endoftime`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas), [`prereqs`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-prereqs)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_ENDOFTIME` | |
| `endoftime` | |
| `mapflag_EndOfTimeUnlocked` | |

</details>


---

### Enum: `fail_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChanceToBreakFree`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-chancetobreakfree)

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

> **Referenced by:** [`FormChangeHealthThreshold`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangehealththreshold)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Default` | |
| `Full` | |
| `Standing` | |

> **See Also:** Values from [`FormChange`](#enum-formchange), [`initial_form`](#enum-initial_form) may also be valid here (overlapping enum).

</details>


---

### Enum: `form_below`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FormChangeHealthThreshold`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-formchangehealththreshold)

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

> **Referenced by:** [`TransformEquipment`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-transformequipment), [`TransformWeapon`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-transformweapon), [`TransformWeapon`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-transformweapon)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `JarOfChaos` | |
| `Necro_SoulDagger_Charged` | |
| `Necro_SoulDagger_Uncharged` | |

> **See Also:** Values from [`to`](#enum-to) may also be valid here (overlapping enum).

</details>


---

### Enum: `gain_immortal_familiar`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](../World_Maps_and_Events/Events_and_Encounters.md#object-bad), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CharmedFlea` | |
| `CharmedFleaSpecial` | |
| `CharmedPooter` | |

> **See Also:** Values from [`object`](#enum-object) may also be valid here (overlapping enum).

</details>


---

### Enum: `get_and_equip_item`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Antenna` | |
| `Catnip` | |
| `FlyLarva` | |

> **See Also:** Values from [`get_item`](#enum-get_item) may also be valid here (overlapping enum).

</details>


---

### Enum: `gift_item`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`organ_max_intro`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-organ_max_intro), [`organ_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-organ_max_repeating), [`tink_prettybow`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-tink_prettybow)

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

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `grab` | |

</details>


---

### Enum: `icon_damage_type`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-meta)

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

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

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

> **Referenced by:** [`editor`](../World_Maps_and_Events/Spawns_and_Enemy_Pools.md#object-editor)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `red` | |
| `blue` | |
| `black` | |
| `brown` | |
| `cyan` | |
| `green` | |
| `grey` | |
| `none` | |
| `orange` | |
| `pink` | |
| `purple` | |
| `yellow` | |

</details>


---

### Enum: `initial_cutscene_day`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `kaiju_fight` | |
| `moonboss_intro` | |
| `pyro_intro` | |

</details>


---

### Enum: `jestercat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `jurassic`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas), [`prereqs`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-prereqs)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_JURASSIC` | |
| `endoftime` | |
| `mapflag_JurassicUnlocked` | |

</details>


---

### Enum: `learn_passive_from_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Necromancer` | |
| `AnyUnlocked` | |

> **See Also:** Values from [`learn_ability_from_pool`](#enum-learn_ability_from_pool) may also be valid here (overlapping enum).

</details>


---

### Enum: `max_aoe`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `level` | |
| `level-1` | |

</details>


---

### Enum: `min_aoe`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `1+size` | |
| `2+size` | |

</details>


---

### Enum: `moon`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas), [`prereqs`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-prereqs)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_MOON` | |
| `mapflag_IceAgeUnlocked` | |
| `mapflag_MoonUnlocked` | |

</details>


---

### Enum: `movieclip_bg`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`House1`](../World_Maps_and_Events/House_and_Environment.md#object-house1), [`House2`](../World_Maps_and_Events/House_and_Environment.md#object-house2), [`House3`](../World_Maps_and_Events/House_and_Environment.md#object-house3)

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

> **Referenced by:** [`House1`](../World_Maps_and_Events/House_and_Environment.md#object-house1), [`House2`](../World_Maps_and_Events/House_and_Environment.md#object-house2), [`House3`](../World_Maps_and_Events/House_and_Environment.md#object-house3)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `HouseForeground1` | |
| `HouseForeground2` | |
| `HouseForeground3` | |

</details>


---

### Enum: `not_cat_has_item_equipped`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`requirements`](./Miscellaneous.md#object-requirements), [`requirements`](../World_Maps_and_Events/Events_and_Encounters.md#object-requirements)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CryogenicTimeChamber_Full` | |
| `GuillotinasHead` | |
| `Horns` | |

> **See Also:** Values from [`cat_has_item_equipped`](#enum-cat_has_item_equipped), [`complete_item_quest`](#enum-complete_item_quest), [`lose_specific_item`](#enum-lose_specific_item), [`choose_cat_with_item`](#enum-choose_cat_with_item) may also be valid here (overlapping enum).

</details>


---

### Enum: `oncast`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sounds`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-sounds)

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

> **Referenced by:** [`sounds`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-sounds)

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

> **Referenced by:** [`boss`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-boss), [`mw_boss`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-mw_boss)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `chaos_boss` | |
| `finalboss` | |
| `throbbingking` | |

</details>


---

### Enum: `rematch_cutscene_day`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `house_boss_returns_kaijufight` | |
| `house_boss_returns_pyro` | |
| `house_boss_returns_zara` | |

</details>


---

### Enum: `requires_unlocked_npc`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `frank` | |
| `jack` | |
| `tracy` | |

> **See Also:** Values from [`subject_frame`](#enum-subject_frame), [`unlock_npc_tomorrow`](#enum-unlock_npc_tomorrow) may also be valid here (overlapping enum).

</details>


---

### Enum: `scramble_abilities`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good), [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `all` | |

</details>


---

### Enum: `set_house`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Default`](../World_Maps_and_Events/House_and_Environment.md#object-default), [`LargeHouse`](../World_Maps_and_Events/House_and_Environment.md#object-largehouse), [`MediumHouse`](../World_Maps_and_Events/House_and_Environment.md#object-mediumhouse)

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

> **Referenced by:** [`spawn_unit_next_fight`](../World_Maps_and_Events/Events_and_Encounters.md#object-spawn_unit_next_fight)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `enemies` | |

</details>


---

### Enum: `special_tile_tag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ChaosValidPosition` | |
| `FinalBossCloneSpot` | |
| `FinalBossTheChildLocation` | |

> **See Also:** Values from [`tag_location`](#enum-tag_location) may also be valid here (overlapping enum).

</details>


---

### Enum: `spin`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](../World_Maps_and_Events/Events_and_Encounters.md#object-common)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `again` | |

</details>


---

### Enum: `theend`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas), [`prereqs`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-prereqs)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_THEEND` | |
| `endoftime` | |
| `mapflag_TheEndUnlocked` | |

</details>


---

### Enum: `throw_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TinkererBasicAttackSwitching`](../Player_Progression_and_Cats/Cat_Classes.md#object-tinkererbasicattackswitching), [`TinkererBasicAttackSwitching`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-tinkererbasicattackswitching)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TinkererThrow` | |

</details>


---

### Enum: `tint`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

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

> **Referenced by:** [`TransformEquipment`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-transformequipment), [`TransformWeapon`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-transformweapon), [`TransformWeapon`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-transformweapon)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `JarOfNothing` | |
| `Necro_SoulDagger_Charged` | |
| `Necro_SoulDagger_Uncharged` | |

> **See Also:** Values from [`from`](#enum-from) may also be valid here (overlapping enum).

</details>


---

### Enum: `walk,`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Injuries)](../Player_Progression_and_Cats/Injuries.md#object-root)

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

> **Referenced by:** [`BungaCheers`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-bungacheers), [`BungaEntrance`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-bungaentrance)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bungawarrior` | |
| `finalboss_clonecat` | |

> **See Also:** Values from [`hidden_tag`](#enum-hidden_tag) may also be valid here (overlapping enum).

</details>


---

### Enum: `weak,`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Injuries)](../Player_Progression_and_Cats/Injuries.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `brokenLegIdle` | |
| `brokenPawIdle` | |
| `dislocatedShoulderIdle` | |

</details>


---

### Enum: `AbilityEnabledIfHasStatus`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DemonicGlyph_Bite` | |
| `DemonicGlyph_Summon` | |

> **See Also:** Values from [`status`](#enum-status) may also be valid here (overlapping enum).

</details>


---

### Enum: `AddElementsToWeapon`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhileWearingMetal`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhilewearingmetal)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Electric` | |

</details>


---

### Enum: `AfterImage`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `NubbyToss` | |

</details>


---

### Enum: `AllyDamageReaction`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |

</details>


---

### Enum: `AllyMoveAbilityAura`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CatapultJump` | |
| `CatapultJump2` | |

> **See Also:** Values from [`ability`](#enum-ability) may also be valid here (overlapping enum).

</details>


---

### Enum: `AutocastEachTurn`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `sabertooths` | |

</details>


---

### Enum: `ChangeTileOnDeath`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `WaterTile` | |

</details>


---

### Enum: `ChargeSpiritBombAura`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DonateEnergy` | |
| `DonateEnergy2` | |

> **See Also:** Values from [`BonusAbility`](#enum-bonusability) may also be valid here (overlapping enum).

</details>


---

### Enum: `EliteTint`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Elite_Buffs.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `red` | |

</details>


---

### Enum: `EnterMount`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`post_spawn_statuses`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-post_spawn_statuses)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `enter` | |

</details>


---

### Enum: `EquipRandomTemporaryItemFromPool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Referenced by:** [`AddPassivesToMinions`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addpassivestominions)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DestroyerShieldBash` | |
| `None` | |

</details>


---

### Enum: `FollowUp`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

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

> **Referenced by:** [`Conditional_GoodRoll`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_goodroll), [`StatusOnBreak`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonbreak)

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

> **Referenced by:** [`ApplyToRandomPartyMemberIfPossible`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-applytorandompartymemberifpossible)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `all_disorders` | |

</details>


---

### Enum: `HideEquipment`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassivesToSpawnerWhileAlive`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applypassivestospawnerwhilealive), [`additional_passives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-additional_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `neck` | |

</details>


---

### Enum: `HolyShieldTransferToTaggedMinions`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `any` | |
| `crow` | |

> **See Also:** Values from [`tag`](#enum-tag) may also be valid here (overlapping enum).

</details>


---

### Enum: `ImmediateUseDirectionalAbility`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BowlDash` | |
| `BowlDash2` | |

</details>


---

### Enum: `KaijuWinCon`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pyrophina` | |
| `zaratana` | |

> **See Also:** Values from [`frame_label`](#enum-frame_label), [`beat_house_boss`](#enum-beat_house_boss), [`trigger_house_boss`](#enum-trigger_house_boss), [`complete_house_boss`](#enum-complete_house_boss), [`clear_surviving_kaiju`](#enum-clear_surviving_kaiju), [`require_beat_house_boss`](#enum-require_beat_house_boss), [`surviving_kaiju`](#enum-surviving_kaiju) may also be valid here (overlapping enum).

</details>


---

### Enum: `Leave`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CherubimReaction`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cherubimreaction)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Poop` | |
| `Scrap` | |

> **See Also:** Values from [`object`](#enum-object) may also be valid here (overlapping enum).

</details>


---

### Enum: `MiniVolcanoReaction`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

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

> **Referenced by:** [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives), [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicJump` | |
| `MoveOne` | |

> **See Also:** Values from [`variant_of`](#enum-variant_of), [`move`](#enum-move) may also be valid here (overlapping enum).

</details>


---

### Enum: `MoveTowardsKillers`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ReaperRevenge` | |

</details>


---

### Enum: `ProtectTargetedAllies`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

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

> **Referenced by:** [`StatusOnBattleEnd`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-statusonbattleend)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bird` | |
| `melted` | |

> **See Also:** Values from [`tag`](#enum-tag) may also be valid here (overlapping enum).

</details>


---

### Enum: `ReplaceBasicAttackWhenDead`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Haunt` | |

</details>


---

### Enum: `Return`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CherubimReaction`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cherubimreaction)

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

> **Referenced by:** [`sound`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-sound)

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

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |

</details>


---

### Enum: `TransformWhenBuddyDies`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `UltraOrnstein` | |
| `UltraSmough` | |

> **See Also:** Values from [`movieclip`](#enum-movieclip) may also be valid here (overlapping enum).

</details>


---

### Enum: `UpgradeLevelUpClassActives`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Colorless` | |

</details>


---

### Enum: `UpgradeLevelUpClassPassives`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Colorless` | |

</details>


---

### Enum: `UpgradeTaggedSpawnsToChampions`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bug` | |
| `worm` | |

> **See Also:** Values from [`tag`](#enum-tag) may also be valid here (overlapping enum).

</details>


---

### Enum: `XIsLivingCharactersWithTag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `husk` | |
| `rock` | |

</details>


---

### Enum: `alley`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_ALLEY` | |
| `departed_first_real_adventure` | |

</details>


---

### Enum: `boneyard`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_BONEYARD` | |
| `mapflag_BoneyardUnlocked` | |

</details>


---

### Enum: `bunker`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_BUNKER` | |
| `mapflag_BunkerUnlocked` | |

</details>


---

### Enum: `caves`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_CAVES` | |
| `mapflag_CavesUnlocked` | |

</details>


---

### Enum: `cha`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`permanent_stats`](../World_Maps_and_Events/Events_and_Encounters.md#object-permanent_stats), [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

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

> **Referenced by:** [`MoveTowardsDamageSource`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movetowardsdamagesource)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Boris` | |
| `Default` | |

> **See Also:** Values from [`FormChange`](#enum-formchange) may also be valid here (overlapping enum).

</details>


---

### Enum: `clear_surviving_kaiju`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pyrophina` | |
| `zaratana` | |

> **See Also:** Values from [`frame_label`](#enum-frame_label), [`beat_house_boss`](#enum-beat_house_boss), [`trigger_house_boss`](#enum-trigger_house_boss), [`complete_house_boss`](#enum-complete_house_boss), [`KaijuWinCon`](#enum-kaijuwincon), [`require_beat_house_boss`](#enum-require_beat_house_boss), [`surviving_kaiju`](#enum-surviving_kaiju) may also be valid here (overlapping enum).

</details>


---

### Enum: `cloned_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack` | |

</details>


---

### Enum: `complete_adventure`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `anywhere` | |

</details>


---

### Enum: `crater`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_CRATER` | |
| `mapflag_CraterUnlocked` | |

</details>


---

### Enum: `default_attack_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `attack2` | |
| `bite1` | |

</details>


---

### Enum: `desert`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_DESERT` | |
| `mapflag_DesertUnlocked` | |

</details>


---

### Enum: `enemy_type`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`KillEnemyOfTypeAtBattleStart`](../World_Maps_and_Events/Events_and_Encounters.md#object-killenemyoftypeatbattlestart)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `any` | |
| `cat` | |

> **See Also:** Values from [`tag`](#enum-tag) may also be valid here (overlapping enum).

</details>


---

### Enum: `exit_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DybbukPossessed`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-dybbukpossessed), [`DybbukPossessionFallback`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-dybbukpossessionfallback)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DybbukReturn` | |

</details>


---

### Enum: `follow_character_tag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Big`](../World_Maps_and_Events/House_and_Environment.md#object-big)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `zaratana` | |

</details>


---

### Enum: `future`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_FUTURE` | |
| `mapflag_FutureUnlocked` | |

</details>


---

### Enum: `generate_beanies_quest`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`beanies_quests_intro`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-beanies_quests_intro), [`beanies_quests_repeat`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-beanies_quests_repeat)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `intro` | |
| `main_pool` | |

</details>


---

### Enum: `get_full_item_set_from_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `common` | |

</details>


---

### Enum: `gift_item_from_pool`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`frank_max_intro`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-frank_max_intro), [`frank_max_repeating`](../Player_Progression_and_Cats/Progression_Unlocks.md#object-frank_max_repeating)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `parasites` | |

</details>


---

### Enum: `iceage`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_ICEAGE` | |
| `mapflag_IceAgeUnlocked` | |

</details>


---

### Enum: `icon`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `2`, `3`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DejaVu2` | |
| `DejaVu3` | |

</details>


---

### Enum: `is_move`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-meta)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `junkyard`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_JUNKYARD` | |
| `mapflag_JunkyardUnlocked` | |

</details>


---

### Enum: `lab`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_LAB` | |
| `mapflag_LabUnlocked` | |

</details>


---

### Enum: `lose_all_equipped_items`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cat` | |

</details>


---

### Enum: `mask_center`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SpearMaskCenter` | |

</details>


---

### Enum: `mask_extent`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SpearMaskExtent` | |

</details>


---

### Enum: `meatworld`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_MEATWORLD` | |
| `mapflag_MeatWorldUnlockedFull` | |

</details>


---

### Enum: `musiclayer`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root), [`mw_hard1`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-mw_hard1)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `boss` | |

</details>


---

### Enum: `outline_color`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Damage_Text_Styles)](../Assets_and_Localization/Damage_Text_Styles.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `white` | |

</details>


---

### Enum: `override_move`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `310`, `331`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicJump` | |

</details>


---

### Enum: `particle_mat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `shadow_occluded_spelldissolve` | |

</details>


---

### Enum: `party_injury`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `random` | |

</details>


---

### Enum: `preturn_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `alertstart` | |

</details>


---

### Enum: `pseudoprojectile`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `RocketFromAbove` | |

</details>


---

### Enum: `quest_item_alias`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

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

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `include_alpha` | |

</details>


---

### Enum: `require_beat_house_boss`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pyrophina` | |
| `zaratana` | |

> **See Also:** Values from [`frame_label`](#enum-frame_label), [`beat_house_boss`](#enum-beat_house_boss), [`trigger_house_boss`](#enum-trigger_house_boss), [`complete_house_boss`](#enum-complete_house_boss), [`KaijuWinCon`](#enum-kaijuwincon), [`clear_surviving_kaiju`](#enum-clear_surviving_kaiju), [`surviving_kaiju`](#enum-surviving_kaiju) may also be valid here (overlapping enum).

</details>


---

### Enum: `require_mapgen_flag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CoreObeliskUnlocked` | |
| `MoonObeliskUnlocked` | |

> **See Also:** Values from [`set_mapgen_flag`](#enum-set_mapgen_flag) may also be valid here (overlapping enum).

</details>


---

### Enum: `scramble_basic_attack`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `all` | |

</details>


---

### Enum: `scramble_passives`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](../World_Maps_and_Events/Events_and_Encounters.md#object-good)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `all` | |

</details>


---

### Enum: `select_item_from_pool_for_cutscene_only`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](../World_Maps_and_Events/Events_and_Encounters.md#object-bad)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `chapter` | |
| `glitched_items` | |

> **See Also:** Values from [`get_item_from_pool`](#enum-get_item_from_pool) may also be valid here (overlapping enum).

</details>


---

### Enum: `sewers`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`, [`map_areas`](./Miscellaneous.md#object-map_areas)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_SEWERS` | |
| `mapflag_SewersUnlocked` | |

</details>


---

### Enum: `smallray_clip`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Lighting`](./Miscellaneous.md#object-lighting)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Bunkerlight` | |
| `labligtht` | |

</details>


---

### Enum: `surviving_kaiju`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pyrophina` | |
| `zaratana` | |

> **See Also:** Values from [`frame_label`](#enum-frame_label), [`beat_house_boss`](#enum-beat_house_boss), [`trigger_house_boss`](#enum-trigger_house_boss), [`complete_house_boss`](#enum-complete_house_boss), [`KaijuWinCon`](#enum-kaijuwincon), [`clear_surviving_kaiju`](#enum-clear_surviving_kaiju), [`require_beat_house_boss`](#enum-require_beat_house_boss) may also be valid here (overlapping enum).

</details>


---

### Enum: `target_filter`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ProtectTargetedAllies`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-protecttargetedallies)

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

> **Referenced by:** [`AlternateCraftingPools`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-alternatecraftingpools)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `tinkerer_0_bombs` | |

</details>


---

### Enum: `tinkerer_1`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AlternateCraftingPools`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-alternatecraftingpools)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `tinkerer_1_bombs` | |

</details>


---

### Enum: `tooltip_stacks_singular`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Status_Effect_Keywords)](../Core_Entities_and_Combat/Status_Effect_Keywords.md#object-root)

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

> **Referenced by:** [`innate_items`](../Player_Progression_and_Cats/Cat_Classes.md#object-innate_items), [`MonkCatReactionAbilities`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-monkcatreactionabilities)

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

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bigsharklevels` | |

</details>


---

### Enum: `water_alt_shader`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `blood` | |

</details>


---

### Enum: `water_alt_shroud`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BloodShroud` | |

</details>


---

### Enum: `water_alt_tile`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BloodTile` | |

</details>


---

### Enum: `welcome_message`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`meta`](../World_Maps_and_Events/Shops.md#object-meta)

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

> **Referenced by:** [`ROOT` (Spawns_and_Enemy_Pools)](../World_Maps_and_Events/Spawns_and_Enemy_Pools.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ID` | |

</details>


---

### Enum: `10,`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScalingAttackAnimation`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-scalingattackanimation)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bite3` | |

</details>


---

### Enum: `1x1_object`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`WaggleClone`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-waggleclone)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cWaggle` | |

</details>


---

### Enum: `2x2_object`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`WaggleClone`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-waggleclone)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cWaggle2x2` | |

</details>


---

### Enum: `3x3_object`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`WaggleClone`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-waggleclone)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cWaggle3x3` | |

</details>


---

### Enum: `AbilityEnabledIfNotHasStatus`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BackflipWhenTargeted` | |

</details>


---

### Enum: `AbilityEnabledIfSpecificItemEquipped`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Neverstone` | |

</details>


---

### Enum: `AbilityOnBattleStart_UseAI`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TheCreator_SpawnCloneTeam` | |

</details>


---

### Enum: `AddElementsToSpells`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Earth` | |

</details>


---

### Enum: `AlternateIdleAnimation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `berserkIdle` | |

</details>


---

### Enum: `AutocastEachRound`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SpiderReturn` | |

</details>


---

### Enum: `BloatEyePassive2`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BloatEyeMovement2` | |

</details>


---

### Enum: `BonusAbility_DelayedApplication`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Slap` | |

</details>


---

### Enum: `Boris`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`other_form_change_abilities`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-other_form_change_abilities)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MegaGuppy_TransformBoris` | |

</details>


---

### Enum: `CanMutateTo`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Hyde` | |

</details>


---

### Enum: `ChangeTileUnderCharacterAtStart`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`self_status_next_fight`](../World_Maps_and_Events/Events_and_Encounters.md#object-self_status_next_fight)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `GlassTile` | |

</details>


---

### Enum: `Charmed`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `level` | |

</details>


---

### Enum: `ConfusionEffectOnTaggedAbilities`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `consumable` | |

</details>


---

### Enum: `ConjureSingleUseBonusAbility`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `random` | |

</details>


---

### Enum: `CounterAttackAfterEnemyCastSpell`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Telekinesis` | |

</details>


---

### Enum: `DeathwormUnderground`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DeathWormEat` | |

</details>


---

### Enum: `Default`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`exit_animations`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-exit_animations)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `release` | |

</details>


---

### Enum: `DelayCastAbility`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_LastHit`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_lasthit)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `HitlerNuke` | |

</details>


---

### Enum: `DiesToElement`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Wind` | |

</details>


---

### Enum: `DinoLegAnimation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `poop` | |

</details>


---

### Enum: `DisguisedTrapper`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FearMelee` | |

</details>


---

### Enum: `DoubleCastTaggedSpells`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `musical` | |

</details>


---

### Enum: `DropAsFamiliarOnTookDamage`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `PhantomMaskRock` | |

</details>


---

### Enum: `DropSoulJarOnDeath`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SoulJar_Full` | |

</details>


---

### Enum: `ElementWeakness`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Fire` | |

</details>


---

### Enum: `ExcludeFromEvents`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Tragedy` | |

</details>


---

### Enum: `Explosive`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`other_form_change_abilities`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-other_form_change_abilities)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MegaGuppy_TransformExplosive` | |

</details>


---

### Enum: `ExtraTurnsPerTaggedUnit`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `sprout` | |

</details>


---

### Enum: `FlushmasterCelebration`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `celebrate` | |

</details>


---

### Enum: `FormChangeWhenBuddyDies`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Rage` | |

</details>


---

### Enum: `HarpoonTrapPassive`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `HarpoonTrapPull` | |

</details>


---

### Enum: `Holy`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`other_form_change_abilities`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-other_form_change_abilities)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MegaGuppy_TransformHoly` | |

</details>


---

### Enum: `ImmediateUseAbility_Instant`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasStatus`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_hasstatus)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `head_CrownOfHorns` | |

</details>


---

### Enum: `JohnnyWasher`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BBTransformZealot` | |

</details>


---

### Enum: `JumpAttackLeaveBehind`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-temporary_effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BungaThrone` | |

</details>


---

### Enum: `KnockOutClone`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_PlayerCat`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_playercat)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `PlayerCat_MiniMiniMe` | |

</details>


---

### Enum: `LeaveBehind`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-temporary_effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Bait` | |

</details>


---

### Enum: `LegacySpawnSavedCatIfExists`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Legacy_Marshmallow_StolenCatID` | |

</details>


---

### Enum: `LimitedTileTrail`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FlowerTile` | |

</details>


---

### Enum: `Madness`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `level` | |

</details>


---

### Enum: `ManglerMonsterPassive`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ManglerMonsterDashAttack` | |

</details>


---

### Enum: `MoonHeadCrackedVisual`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Cracked` | |

</details>


---

### Enum: `ObjectOnHitFullyEmpty`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `RandomArmorPickup` | |

</details>


---

### Enum: `Paranoia`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ParanoiaBasicMelee` | |

</details>


---

### Enum: `Peralta`


<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TikaFont` | |

</details>


---

### Enum: `PersistentElement`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../World_Maps_and_Events/House_and_Environment.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Holy` | |

</details>


---

### Enum: `QueueUseAbility`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Spider_GoInsane` | |

</details>


---

### Enum: `ReloadOnElementalDamageReceived`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Holy` | |

</details>


---

### Enum: `ReloadOnKillTagged`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `rock` | |

</details>


---

### Enum: `ReplaceBasicAttack_Mutation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FetusSpit` | |

</details>


---

### Enum: `ReplaceBlankTilesOnBattleStart`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `GlassTile` | |

</details>


---

### Enum: `ReplaceSpellsWhenDead`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Spook` | |

</details>


---

### Enum: `SE_CatSwishThrow`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_ThrowGrenade` | |

</details>


---

### Enum: `SE_Cat_ShadowStepIn`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_Terminator_ShadowStepIn` | |

</details>


---

### Enum: `SE_Cat_ShadowStepOut`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_Terminator_ShadowStepOut` | |

</details>


---

### Enum: `SE_Cat_WeaponLower`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_Terminator_WeaponLower` | |

</details>


---

### Enum: `SE_Cat_WeaponRaise`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_Terminator_WeaponRaise` | |

</details>


---

### Enum: `SE_Cat_bearHug`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_Terminator_bearHug` | |

</details>


---

### Enum: `SE_Cat_equipWeapon`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_TerminatorSwapWeapon` | |

</details>


---

### Enum: `SE_PetRock_Dash`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_PetBoulder_Dash` | |

</details>


---

### Enum: `SafeDoomed`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`additional_passives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-additional_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `level` | |

</details>


---

### Enum: `Set`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Monk` | |

</details>


---

### Enum: `SetFaction`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `enemies` | |

</details>


---

### Enum: `SoundEventOnHit`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Batterup_Connect` | |

</details>


---

### Enum: `SourceSwapsBackEndOfTurn`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ThiefSwapBack` | |

</details>


---

### Enum: `SpawnMeatOnMove`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Food` | |

</details>


---

### Enum: `SpecialBossMultipartInstakill`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `moonboss` | |

</details>


---

### Enum: `StealEquipment`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `any` | |

</details>


---

### Enum: `SupportFormChangeInsteadOfRun`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Attacker` | |

</details>


---

### Enum: `TagMetronome`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `musical` | |

</details>


---

### Enum: `TallTumorManaBurn`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TT_ManaBurn` | |

</details>


---

### Enum: `TeamBonusAbility`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ShootHere` | |

</details>


---

### Enum: `TeleportBackAtTurnEnd`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FlashBack` | |

</details>


---

### Enum: `Terminator2Chase`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `move` | |

</details>


---

### Enum: `TickDownStatus`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ShortCircuit` | |

</details>


---

### Enum: `TileElementDamageImmunity`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Ice` | |

</details>


---

### Enum: `TilesMovedToNeighborHeal`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `level` | |

</details>


---

### Enum: `TrackAmountKilledByPlayer`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BonusBirdsKilled` | |

</details>


---

### Enum: `TransformBasicMove`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BasicDashAttackMove_NoKnockback` | |

</details>


---

### Enum: `TransformNow`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Hitler` | |

</details>


---

### Enum: `TransformOnDeathImmediately`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `NoHead` | |

</details>


---

### Enum: `UseAbilityWhenShieldDepleted`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `T3Pebbles_PrimeBoulderDrop` | |

</details>


---

### Enum: `UseAbility_Madness`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnend)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `weapon` | |

</details>


---

### Enum: `WhitelistPickupType`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `food` | |

</details>


---

### Enum: `XIsCountStatusStacks`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bonus_passives)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DodgeChance_Status` | |

</details>


---

### Enum: `abandonedones`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `adjust_target`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `stalk` | |

</details>


---

### Enum: `affected_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `statDown` | |

</details>


---

### Enum: `alert_form`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CerberubsAggroTargetBehavior`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cerberubsaggrotargetbehavior)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Alert` | |

</details>


---

### Enum: `allow`


<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `skip` | |

</details>


---

### Enum: `ally_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `lickAttack` | |

</details>


---

### Enum: `ally_damage`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BungaCheers`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-bungacheers)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `littleboo` | |

</details>


---

### Enum: `ally_dead`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BungaCheers`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-bungacheers)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bigboo` | |

</details>


---

### Enum: `alt_art`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Tangled`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-tangled)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TangledMeat` | |

</details>


---

### Enum: `alt_dead_ani`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SupportDieInsteadOfRun`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-supportdieinsteadofrun)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `off` | |

</details>


---

### Enum: `alt_dying_ani`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SupportDieInsteadOfRun`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-supportdieinsteadofrun)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `shutdown` | |

</details>


---

### Enum: `ambush`


<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `putalevelhere.lvl` | |

</details>


---

### Enum: `animate_name`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pointout` | |

</details>


---

### Enum: `animation_prefix`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sound`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-sound)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `RattleSnake` | |

</details>


---

### Enum: `appearance`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-spawn)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `GolemCat` | |

</details>


---

### Enum: `aura_requires_tag`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AllStatsAura`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-allstatsaura)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `humanoid` | |

</details>


---

### Enum: `auto_cast`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnThingOnDamage`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-spawnthingondamage)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Dash_Enemy` | |

</details>


---

### Enum: `auto_cast_on_spawn`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-spawn)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Dash_Enemy` | |

</details>


---

### Enum: `background_shader`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `meatpulse_ground` | |

</details>


---

### Enum: `boss_background_alt`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CoreBossBG` | |

</details>


---

### Enum: `break_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossShieldHealth`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-finalbossshieldhealth)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `DestroyerBreakShield` | |

</details>


---

### Enum: `bumblefoot`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `butchercat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `cancreeper`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `cat_has_item_slot_equipped`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`requirements`](../World_Maps_and_Events/Events_and_Encounters.md#object-requirements)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `weapon` | |

</details>


---

### Enum: `cavecatfamily`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `cerberubs`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `chapter`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-spawn)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `alley` | |

</details>


---

### Enum: `check_has_status`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MoveTowardsDamageSource`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movetowardsdamagesource)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `FinalBossHitCountdownBoris` | |

</details>


---

### Enum: `choose_cat_with_item_slot_equipped`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`intro`](../World_Maps_and_Events/Events_and_Encounters.md#object-intro)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `weapon` | |

</details>


---

### Enum: `clericcat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `clipname`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`HPAltStates`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-hpaltstates)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `poopmain` | |

</details>


---

### Enum: `con`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `aux` | |

</details>


---

### Enum: `dash_bonk_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bonk` | |

</details>


---

### Enum: `default`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScalingAttackAnimation`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-scalingattackanimation)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bite1` | |

</details>


---

### Enum: `default_form`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CerberubsAggroTargetBehavior`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-cerberubsaggrotargetbehavior)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Normal` | |

</details>


---

### Enum: `default_tileset`


<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `alley` | |

</details>


---

### Enum: `dex`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `aux` | |

</details>


---

### Enum: `dinocouple`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `dodge`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `liquidmetaldodge` | |

</details>


---

### Enum: `drmangler`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `drop_body_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Consumed`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-consumed)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MoonHandDrop` | |

</details>


---

### Enum: `druidcat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `eject_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Mount`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-mount)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MechSuitEject` | |

</details>


---

### Enum: `empty!`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Spawns_and_Enemy_Pools)](../World_Maps_and_Events/Spawns_and_Enemy_Pools.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `editor` | |

</details>


---

### Enum: `ending_cutscene`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `hitler_end` | |

</details>


---

### Enum: `ending_cutscene2`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `credits_3` | |

</details>


---

### Enum: `enemy_damage`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BungaCheers`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-bungacheers)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `littlecheer` | |

</details>


---

### Enum: `enemy_dead`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BungaCheers`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-bungacheers)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `bigcheer` | |

</details>


---

### Enum: `enter_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Mount`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-mount)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `EnterMech` | |

</details>


---

### Enum: `equip_sound`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_CatWeaponPoke_Chainsaw` | |

</details>


---

### Enum: `exclude_characters_tagged`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Enemy_AI)](../Core_Entities_and_Combat/Enemy_AI.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `siren` | |

</details>


---

### Enum: `exclude_prefix`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TwisterDisplaceWithDamage`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-twisterdisplacewithdamage)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Twister` | |

</details>


---

### Enum: `fail_adventure`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `anywhere` | |

</details>


---

### Enum: `fightercat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `finish_quest`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `JarOfChaos` | |

</details>


---

### Enum: `flushmaster`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `form_in`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SwimmingFormChange`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-swimmingformchange)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Water` | |

</details>


---

### Enum: `form_out`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SwimmingFormChange`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-swimmingformchange)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Out` | |

</details>


---

### Enum: `form_unwashed`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`JohnnyNeedsWashing`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-johnnyneedswashing)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Unwashed` | |

</details>


---

### Enum: `form_washed`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`JohnnyNeedsWashing`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-johnnyneedswashing)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Washed` | |

</details>


---

### Enum: `gambit`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `general_common`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `general_rare`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `general_uncommon`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `general_very_rare`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Item_Pools)](./Item_Pools.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `get_and_equip_item_from_pool`


<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cursed_items` | |

</details>


---

### Enum: `grant_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Rest` | |

</details>


---

### Enum: `grow_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-mothertumorpassive)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MotherTumorGrow` | |

</details>


---

### Enum: `head_drop`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MegaDinoDropController`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-megadinodropcontroller)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MD_HeadDrop` | |

</details>


---

### Enum: `hit_animation_alt`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`damage_instance`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-damage_instance)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `catch` | |

</details>


---

### Enum: `huntercat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `iceelemental`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `ignore_if_str_aux_equals`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TintItem`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-tintitem)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ModelingClay_Default` | |

</details>


---

### Enum: `ignore_tagged_sources`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MoveTowardsDamageSource`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-movetowardsdamagesource)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `megadino` | |

</details>


---

### Enum: `increment_savefile_counter`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `GameStat_CountNukeQuestCompletions` | |

</details>


---

### Enum: `infestedduo`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `int`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `aux` | |

</details>


---

### Enum: `knockback`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`damage_instance`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-damage_instance)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `level` | |

</details>


---

### Enum: `knockback_modifier`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `rotate_cw` | |

</details>


---

### Enum: `lck`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `aux` | |

</details>


---

### Enum: `leg_leave`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MegaDinoDropController`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-megadinodropcontroller)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MD_LegLeave` | |

</details>


---

### Enum: `leg_return`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MegaDinoDropController`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-megadinodropcontroller)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MD_LegReturn` | |

</details>


---

### Enum: `legacy_savekey`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RunWhenLastPlayerCatIsCharmed`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-runwhenlastplayercatischarmed)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Legacy_Marshmallow_StolenCatID` | |

</details>


---

### Enum: `lenny`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `lightningelemental`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `magecat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `mamamaggot`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `monkcat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `name_mod`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `CAT_NAME_MOD_DEMONIC` | |

</details>


---

### Enum: `necrocat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `new_music`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChaosHeadDropIn`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-chaosheaddropin)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `chaos_boss_part2` | |

</details>


---

### Enum: `next_fight_from_set`


<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `putalevelhere.lvl` | |

</details>


---

### Enum: `no_buddy`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SyncFormsWithBuddy`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-syncformswithbuddy)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Rage` | |

</details>


---

### Enum: `nuke`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`map_areas`](./Miscellaneous.md#object-map_areas)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `PlotFlag_FrankBeanies` | |

</details>


---

### Enum: `ontrigger_intentional`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`sounds`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-sounds)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Lenny_HereKitty` | |

</details>


---

### Enum: `other_character`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossSyncAnimations`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-finalbosssyncanimations)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MegaGuppy` | |

</details>


---

### Enum: `override_end_option_prompt`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `EVENT_USETHETOILET_AGAIN` | |

</details>


---

### Enum: `override_portrait`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-graphics)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Cherub` | |

</details>


---

### Enum: `party_gain_disorder_from_pool`


<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `mental_disorders` | |

</details>


---

### Enum: `party_gain_disorder_from_pool_exclude_self`


<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `mental_disorders` | |

</details>


---

### Enum: `party_heal_disorder`


<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `mental_disorders` | |

</details>


---

### Enum: `pass_ani`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-mothertumorpassive)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `pass` | |

</details>


---

### Enum: `play_result_animation`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](../World_Maps_and_Events/Events_and_Encounters.md#object-rare)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `resultVeryGood` | |

</details>


---

### Enum: `play_sound`


<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `PickupCoin` | |

</details>


---

### Enum: `post_absorb_move_weights`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-ai)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `minimum_move` | |

</details>


---

### Enum: `preferred_distance`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Enemy_AI)](../Core_Entities_and_Combat/Enemy_AI.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `reach` | |

</details>


---

### Enum: `prioritize_throw_target_with_passive`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `NubbyTossPriority` | |

</details>


---

### Enum: `psychiccat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `puddle_tile`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`SpawnVolcanoOnBattleStart`](../World_Maps_and_Events/House_and_Environment.md#object-spawnvolcanoonbattlestart)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `LavaTile` | |

</details>


---

### Enum: `punch_self_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DybbukPossessed`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-dybbukpossessed)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `Dybbuk_StopHittingYourself` | |

</details>


---

### Enum: `queenhippo`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `queue`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossBeamQueue`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-finalbossbeamqueue)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TheChild_TargetBeam` | |

</details>


---

### Enum: `radicalrat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `range_symmetry`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `eight_way` | |

</details>


---

### Enum: `ratking`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `receive_ani`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherTumorPassive`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-mothertumorpassive)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `receive` | |

</details>


---

### Enum: `release`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossBeamQueue`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-finalbossbeamqueue)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TheChild_ReleaseBeams` | |

</details>


---

### Enum: `reserved`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Spawns_and_Enemy_Pools)](../World_Maps_and_Events/Spawns_and_Enemy_Pools.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `for` | |

</details>


---

### Enum: `reset_str_aux_on_store`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ModelingClay_Default` | |

</details>


---

### Enum: `reset_unlock`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `nuke_quest_begin` | |

</details>


---

### Enum: `restructions`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`target`](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-target)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `aoe_must_exist` | |

</details>


---

### Enum: `rockybobo`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `roll_ability`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ai`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-ai)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `RollDice` | |

</details>


---

### Enum: `shader`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPostProcessEffect`](../World_Maps_and_Events/House_and_Environment.md#object-addpostprocesseffect)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `shimmervignette` | |

</details>


---

### Enum: `shield`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `aux` | |

</details>


---

### Enum: `slime`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `sound_event`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ModularPickup`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-modularpickup)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `EatAntidote` | |

</details>


---

### Enum: `spawn_node`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `start` | |

</details>


---

### Enum: `spd`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `aux` | |

</details>


---

### Enum: `spell`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MonkCatReactionAbilities`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-monkcatreactionabilities)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MCHadouken` | |

</details>


---

### Enum: `spewer`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `stacy`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `str`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `aux` | |

</details>


---

### Enum: `str_aux`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ModelingClay_Default` | |

</details>


---

### Enum: `tankcat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `thebloat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `thiefcat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `tinkerercat`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `trampy`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---

### Enum: `transform`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`FinalBossBeamQueue`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-finalbossbeamqueue)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `TheChild_TransformBoris` | |

</details>


---

### Enum: `tumor_object`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MotherGrowController`](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-mothergrowcontroller)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MotherTumor` | |

</details>


---

### Enum: `tutorial`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** `ROOT`

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AREA_NAME_TUTORIAL` | |

</details>


---

### Enum: `unlock_item`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Progression_Unlocks)](../Player_Progression_and_Cats/Progression_Unlocks.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `MomsKnife` | |

</details>


---

### Enum: `unlockcheck_on_complete`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`boss`](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-boss)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `map_unlock_junkyard` | |

</details>


---

### Enum: `utility`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Spawns_and_Enemy_Pools)](../World_Maps_and_Events/Spawns_and_Enemy_Pools.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `PlayerSpawn` | |

</details>


---

### Enum: `zodiac`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT` (Map_Generation_and_Routing)](../World_Maps_and_Events/Map_Generation_and_Routing.md#object-root)

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `auto` | |

</details>


---


---

### Enum: `state_health`


<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `cracked1` | |
| `cracked2` | |
| `cracked3` | |
| `imminent` | |
| `scuffed` | |

</details>


---

### Enum: `sludge_armor`


<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SludgeHat` | |
| `SludgeMask` | |
| `SludgeNeck` | |

</details>


---

### Enum: `raptor_nest_eggs`


<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `GoldenEgg` | |
| `RaptorEgg` | |
| `WeirdEgg` | |

</details>


---

### Enum: `spells`


<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AZ_BreakArm` | |
| `AZ_BreakLeg` | |
| `AZ_Jump` | |
| `AZ_LoseHead` | |
| `AZ_Scream` | |
| `AlienBeastEat` | |
| `AlienBeastGoop` | |
| `AlienBeastMoveOne` | |
| `AlienBeastOpenEyes` | |
| `AlienBeastPuke` | |
| `AlienBeastRampage` | |
| `AlienBeastScream` | |
| `AnkyloSpin` | |
| `BBBless` | |
| `BBCut` | |
| `BBPickupCrown` | |
| `BBPullBomb` | |
| `BBSpin` | |
| `BBToss` | |
| `BBTransformMutant` | |
| `BBTransformZealot` | |
| `BHoleSuck` | |
| `BadBone_copy` | |
| `BearTrap_CaveBaby` | |
| `BearTrap_Enemy` | |
| `BearTrap_Enemy_Cantrip` | |
| `BecomeTheDestroyer` | |
| `BellyPound` | |
| `BirdFly` | |
| `BirthwortHeal` | |
| `BirthwortReactionShot` | |
| `BirthwortTrample` | |
| `BloatEyeMovement2` | |
| `BloatLeap` | |
| `BloatLoseFirstEye` | |
| `BloatLoseSecondEye` | |
| `BloatSideLaser` | |
| `BloatyExplodey` | |
| `BombRatTurtle` | |
| `BoomerCatExplode` | |
| `BoyDinoCry` | |
| `BoyDinoHeadBash` | |
| `BrambleBabyEntangle` | |
| `BumbleButt` | |
| `BumblefootAttemptEatCat` | |
| `BumblefootBoneShot` | |
| `BumblefootEatCat` | |
| `BumblefootEatCorpse` | |
| `BumblefootLeap` | |
| `BungaEatCat` | |
| `BungaEntrance` | |
| `BungaRoar` | |
| `BungaSwipe` | |
| `ButtFart` | |
| `ButtFlip` | |
| `ButtWeb` | |
| `ButtWeb_AlreadyEnraged` | |
| `CBReload` | |
| `CBShoot_ZodiacStyle` | |
| `CHCry` | |
| `CHSpawn` | |
| `CHuskCatShade` | |
| `CHuskDrop` | |
| `CHuskDropFail` | |
| `CHuskGrab` | |
| `CanCreeperSlide` | |
| `CancerExplode` | |
| `CatCall` | |
| `CatGoop` | |
| `CaveBabyFoodMove` | |
| `CaveBabyGrow` | |
| `CaveCatEnrageOne` | |
| `CaveCatEnrageTwo` | |
| `CaveChiefBat` | |
| `CaveChiefFear` | |
| `CaveChiefRally` | |
| `CaveManChestPound` | |
| `CaveManPickupSpear` | |
| `CaveManSpearRun` | |
| `CaveManTransform` | |
| `CaveMom_Heal` | |
| `CaveMom_TossDad` | |
| `CaveMom_TossElsewhere` | |
| `CaveWomanBirth` | |
| `CaveWomanDrop` | |
| `CaveWomanDropTransform` | |
| `CaveWomanGrab` | |
| `CaveWomanThrow` | |
| `CerberubsBarrage` | |
| `CerberubsCalm` | |
| `CerberubsShotgunReaction` | |
| `CerberubsShotgunReactionX` | |
| `CerberubsStraightReaction` | |
| `CerberubsThrow` | |
| `ChainDash` | |
| `ChaosSpawnIn` | |
| `ChaosSwitchForms` | |
| `ChaosSwitchSides` | |
| `CherubAttract` | |
| `CherubDoom` | |
| `CherubimLeave` | |
| `CherubimReturn` | |
| `ChubsGoop` | |
| `ChubsRage` | |
| `ChumShot_Maggot` | |
| `ClotEvolve` | |
| `ClotEvolveCatCopy` | |
| `ClotFailEvolve` | |
| `CollectiveCounter` | |
| `ColorlessCat_BoulderDrop` | |
| `CoreFreakFury` | |
| `Counterspell` | |
| `CovenFamine` | |
| `CovenPestilence` | |
| `CovenRise1` | |
| `CovenRise2` | |
| `CovenRise3` | |
| `CovenRise4` | |
| `CovenSummon` | |
| `CovenWar` | |
| `CraterCreeperSlide` | |
| `CrowFlap` | |
| `CrowFlap2` | |
| `CrowFlap3` | |
| `CrowFlutter` | |
| `CrowFlutter2` | |
| `CrowFlutter3` | |
| `CultistCut` | |
| `CutterCut` | |
| `D6Confused` | |
| `D6Fizzle` | |
| `D6Laser` | |
| `D6Poop` | |
| `D6Quake` | |
| `D6Storm` | |
| `D6Wrath` | |
| `DCAeroblast` | |
| `DCBirthSquirrel` | |
| `DCSquirrelForm` | |
| `DCT_SummonCrow` | |
| `DH_MeatHook` | |
| `DbgBackgroundTransitionTest` | |
| `DbgChaosSwitchFormsA` | |
| `DbgChaosSwitchFormsP` | |
| `Dclaude_Declaw` | |
| `DeathWormEat` | |
| `DeathWormReturn` | |
| `DeathWormTrampleDash_Reaction` | |
| `DecoyExplode` | |
| `DefaultMove` | |
| `DemonRockThrow` | |
| `Destroyer2HolyAttack` | |
| `Destroyer2Pulse` | |
| `DestroyerBreakShield` | |
| `DestroyerChargeBackflips` | |
| `DestroyerDashAttack` | |
| `DestroyerDodge` | |
| `DestroyerHolyAttack` | |
| `DestroyerPulse` | |
| `DestroyerRaise` | |
| `DestroyerThrowShield` | |
| `DiceLeap` | |
| `Digest` | |
| `Disguise` | |
| `DoNothing` | |
| `DoctorPickup` | |
| `DoctorSpawn` | |
| `DoubleDistanceMove` | |
| `DrDGlare` | |
| `DrinkUp` | |
| `DustDash` | |
| `DustTeleport` | |
| `DybbukEscape` | |
| `DybbukPossess` | |
| `DybbukRePossess` | |
| `DybbukReanimate` | |
| `DybbukReturn` | |
| `DybbukWisps` | |
| `ExtraMove` | |
| `FatLeap` | |
| `FearMelee` | |
| `FetusAirstrikeTrigger` | |
| `FetusPullBomb` | |
| `FleshLadUppercut` | |
| `FleshyMindConfusion` | |
| `FloastSpawn` | |
| `FloastThrow` | |
| `FlushX` | |
| `FormGrowThree` | |
| `FormGrowThreeSnakey` | |
| `FormGrowTwo` | |
| `FormGrowTwoSnakey` | |
| `FormShrinkFour` | |
| `FormShrinkOne` | |
| `FormShrinkOneSnakey` | |
| `FormShrinkThree` | |
| `FormShrinkTwo` | |
| `FormShrinkTwoSnakey` | |
| `FutureBotPunchAggro` | |
| `FutureBotSuplex` | |
| `FuzzerJump_post` | |
| `FuzzerReact` | |
| `G3CallForHelp` | |
| `G3CoughFly` | |
| `G3GrabHead` | |
| `G3RageShake` | |
| `G3RunToHead` | |
| `G3Scream_Hex` | |
| `G3Shake` | |
| `G3SpawnMama` | |
| `G3TossHead` | |
| `GA_Counterspell` | |
| `GA_Megablast` | |
| `GA_PrimeExplode` | |
| `GA_Suggest` | |
| `GKLeap` | |
| `GKSpawn` | |
| `GP_Probe` | |
| `GSOpen` | |
| `GSScream` | |
| `GSSuck` | |
| `GametePop` | |
| `GasserExplode` | |
| `GeminiSpecial` | |
| `GeminiSwipe` | |
| `GenericRage` | |
| `GirlDinoCry` | |
| `GirlDinoHeadBash` | |
| `GirlDinoPoop` | |
| `GirlDinoThrow` | |
| `GlowingMushroomGiveMana` | |
| `GlowingMushroomGiveMana2` | |
| `GoodBone` | |
| `GoodBone_copy` | |
| `GorgerRun` | |
| `GrenadeExplode` | |
| `Guillotina1Rage` | |
| `Guillotina2Rage` | |
| `GuillotinaTossCollide` | |
| `HCHumanDie` | |
| `HangerBotLeave` | |
| `HangerBotReturn` | |
| `HangerBotSpawn` | |
| `HarpoonTrapPull` | |
| `HeadTumorResponse` | |
| `HealSelf` | |
| `HemBounce` | |
| `HemDeathPop` | |
| `HemHeal` | |
| `HitlerCloneHeil` | |
| `HitlerCloneLick` | |
| `HitlerCloneTransform` | |
| `HitlerHeadGrowA` | |
| `HitlerHeadGrowB` | |
| `HitlerHeadTransform` | |
| `HitlerHeil` | |
| `HitlerNuke` | |
| `HitlerPulp1` | |
| `HitlerPulp2` | |
| `HitlerPulp3` | |
| `HitlerPulp4` | |
| `HitlerPulp5` | |
| `HitlerPulp6` | |
| `HitlerSuicide` | |
| `HostShove` | |
| `IDBrambleBurst` | |
| `IDBrambleShot` | |
| `IDSprout` | |
| `IceElementalBlizzard` | |
| `IceElementalBreath` | |
| `JackShield` | |
| `JarHeadOrder` | |
| `JohnnyBlast` | |
| `JohnnyCryOne` | |
| `JohnnyCryTwo` | |
| `JohnnyMegaBlast` | |
| `JohnnyMindControl` | |
| `JohnnyPull` | |
| `JohnnyPush` | |
| `LELeave` | |
| `LEPortFar` | |
| `LEReturn` | |
| `LabPillarDrop` | |
| `Leave` | |
| `LennyCatDies` | |
| `LennyCatSlap` | |
| `LennyDrop` | |
| `LennyGrab` | |
| `LennyGrabDead` | |
| `LennyHug` | |
| `LennyStruggleFail` | |
| `LickyLicky` | |
| `LoveBotCounter` | |
| `MCBlizzard` | |
| `MCFlamethrower` | |
| `MCHadouken` | |
| `MCKineticCharge` | |
| `MCStorm` | |
| `MD_HeadDrop` | |
| `MD_HeadLeave` | |
| `MD_Kick` | |
| `MD_LegLeave` | |
| `MD_LegReturn` | |
| `MD_Lift` | |
| `MD_Poop` | |
| `MM_Grab` | |
| `MM_Guard` | |
| `MM_Quake` | |
| `MM_Unguard` | |
| `MaelestesPickup` | |
| `MaelestesSteal` | |
| `Magnetize` | |
| `MammothBabyStomp` | |
| `MammothStomp` | |
| `MammothTrampleDash` | |
| `ManglerEnrage` | |
| `ManglerFumbleEven` | |
| `ManglerFumbleOdd` | |
| `ManglerMonsterExplode` | |
| `ManglerMonsterHeartAttack` | |
| `ManglerSpin` | |
| `ManglerThrowRemote` | |
| `MarshmallowConvert` | |
| `MarshmallowZealot` | |
| `MechSuitBarrage` | |
| `MechSuitDash` | |
| `MechSuitEject` | |
| `MegaGuppy_SlamLeft` | |
| `MegaGuppy_SlamRight` | |
| `MegaGuppy_SummonTheChild` | |
| `MegaGuppy_TransformBoris` | |
| `MegaGuppy_TransformExplosive` | |
| `MegaGuppy_TransformHoly` | |
| `MegablastX` | |
| `MegafetusMelee` | |
| `Metronome_Enemy` | |
| `MiniNukeExplodey` | |
| `MiniVolcano_Spurt` | |
| `MoonHandDash` | |
| `MoonHandDrop` | |
| `MoonHandDrop_Deathrattle` | |
| `MoonHandGrab` | |
| `MoonHandMegaSqueeze` | |
| `MoonHandPunchHead` | |
| `MoonHandThrow` | |
| `MoonHead_Barrage` | |
| `MoonHead_BeginCharge` | |
| `MoonHead_Blow` | |
| `MoonHead_CallForHelp` | |
| `MoonHead_ChewCat` | |
| `MoonHead_CommandHeadPunch` | |
| `MoonHead_Digest` | |
| `MoonHead_EatCat` | |
| `MoonHead_Finisher` | |
| `MoonHead_RefreshBrace` | |
| `MoonHead_SacrificeHand` | |
| `MoonHead_SpawnHand` | |
| `MoonHead_SpitCat` | |
| `MoonHead_SpitCat_AndDie` | |
| `MoonWormCurl` | |
| `MotherConsume` | |
| `MotherTumorGrow` | |
| `MoveOne` | |
| `MoveTwo` | |
| `MoveTwoCantrip` | |
| `MutateAOE` | |
| `NCGravecrawl` | |
| `NCReanimate` | |
| `NeckSnap` | |
| `NeutronExplode` | |
| `NeutronRumble` | |
| `NubsCatJumpReaction` | |
| `NubsGoop` | |
| `NubsNuke` | |
| `NurseBotHeal` | |
| `Parasaurolophus_Throw` | |
| `ParasiterSpawn` | |
| `PeashyStab` | |
| `PickupRock` | |
| `PokerPokeAlly` | |
| `PokerPokeCat` | |
| `PsychicCatBackflip` | |
| `PsychicChoke_Enemy` | |
| `PteroEscape` | |
| `PteroGrab` | |
| `PyrophinaSoloCatThrow` | |
| `PyrophinaSoloEarthquakeStomp` | |
| `PyrophinaSoloFlamethrower` | |
| `PyrophinaSoloRoar` | |
| `PyrophinaVSCatThrow` | |
| `PyrophinaVSEarthquakeStomp` | |
| `PyrophinaVSFlamethrower` | |
| `PyrophinaVSRoar` | |
| `PyrophinaVSRun` | |
| `PyrophinaVSSpinThrow` | |
| `PyrophinaVSWeatherRoar` | |
| `QuakeJump` | |
| `QueenHippoAttack` | |
| `QueenHippoHeartAttack` | |
| `QueenHippoTire` | |
| `QueenHippoUppercut` | |
| `QueenMinis` | |
| `QueenWeb` | |
| `RageUp` | |
| `RallyMaggots` | |
| `RangedHeal_Enemy` | |
| `RatKing2Spawn` | |
| `RatKingSpawn` | |
| `RatKingTransform` | |
| `RattleSnakeTrap` | |
| `ReaperRevenge` | |
| `Reload` | |
| `RockSong` | |
| `RockToss_BomberRat` | |
| `RockToss_CaveDad` | |
| `RockToss_ColorlessCat` | |
| `RockToss_ColorlessCat_AsCloseAsPossible` | |
| `RollDice` | |
| `SBotAnger` | |
| `SBotAngryMove` | |
| `SBotRecharge` | |
| `SCSneakUp` | |
| `SM_BleedCounter` | |
| `SM_Flamethrower` | |
| `SM_IceShards` | |
| `SM_LightningStorm` | |
| `SM_MagicMissile` | |
| `SZBBackflipDodge` | |
| `SZBReload` | |
| `SabertoothCatDoubleSwipe` | |
| `SabertoothCatTransformSwipe` | |
| `SabertoothCubLick` | |
| `ScaryHaunt` | |
| `ScorpionHold` | |
| `SeraphimRevive` | |
| `ShadeDuplicate` | |
| `ShadowstepDodge` | |
| `ShamblerToss` | |
| `SharkDash` | |
| `Shove` | |
| `SimonFlopper_SpawnMinion` | |
| `SimonFlopper_Tentacle` | |
| `SimonFlopper_WiggleChance` | |
| `SimonFlopper_WiggleFake` | |
| `SimonFlopper_WiggleGuaranteed` | |
| `SimonSays_ComeHere` | |
| `SimonSays_GoAway` | |
| `SimonSays_Scatter` | |
| `Simon_Shot` | |
| `Simon_Tentacle` | |
| `Simon_Trash` | |
| `SlagSpawn` | |
| `SleepPowder` | |
| `SlotMachine_DeathExplode` | |
| `SlotResult_Explode` | |
| `SlotResult_Jackpot_Coins` | |
| `SlotResult_Nothing` | |
| `SlotResult_RandomPickup` | |
| `SmallSpiderMelee` | |
| `SmallTrampleDash` | |
| `SpawnBomb` | |
| `SpawnClot` | |
| `SpawnDip` | |
| `SpawnGasAOE` | |
| `SpawnJunk` | |
| `SpawnMaggots` | |
| `SpawnRat` | |
| `SpawnWisp` | |
| `SpewerBarf_Lava` | |
| `SpewerBarf_Normal` | |
| `SpewerBarf_Tar` | |
| `SpewerSuckLava` | |
| `SpewerSuckNormal` | |
| `SpewerSuckPill` | |
| `SpewerSuckTar` | |
| `SpewerTransformFire` | |
| `SpewerTransformNormal` | |
| `SpewerTransformTar` | |
| `SpiderReturn` | |
| `SpiderSpawn` | |
| `Spider_CalmDown` | |
| `Spider_GoInsane` | |
| `Spin_Enemy` | |
| `SpreadX` | |
| `Sprout` | |
| `StacyHeal` | |
| `StegoEatGrass` | |
| `StegoGrassStomp` | |
| `StegoSpin` | |
| `SwapPositions_TankCat` | |
| `T1ChokeReaction` | |
| `T1Pummel` | |
| `T1SwapWeapon` | |
| `T1ThrowGrenadeA` | |
| `T1ThrowGrenadeB` | |
| `T2Clone` | |
| `T2GoopRun` | |
| `T2UnClone` | |
| `T3Counter` | |
| `T3Intro` | |
| `T3JoinFight` | |
| `T3LickyLicky` | |
| `T3Pebbles_BoulderDrop` | |
| `T3Pebbles_PrimeBoulderDrop` | |
| `T3RipAndTear` | |
| `T3Spawn_Butcher` | |
| `T3Spawn_Colorless` | |
| `T3Spawn_Druid` | |
| `T3Spawn_Fighter` | |
| `T3Spawn_Hunter` | |
| `T3Spawn_Jester` | |
| `T3Spawn_Mage` | |
| `T3Spawn_Medic` | |
| `T3Spawn_Monk` | |
| `T3Spawn_Necromancer` | |
| `T3Spawn_Psychic` | |
| `T3Spawn_Tank` | |
| `T3Spawn_Thief` | |
| `T3Spawn_Tinkerer` | |
| `TCCatBot` | |
| `TCMechSuit` | |
| `TC_DashReaction` | |
| `THC_CoinRoll` | |
| `THC_PoisonSwat` | |
| `THC_Roll` | |
| `TKNG_DeathExplode` | |
| `TKNG_GoAway` | |
| `TKNG_Hop` | |
| `TKNG_Kneel` | |
| `TKNG_Roulette` | |
| `TKNG_Spawn` | |
| `TKNG_Spread` | |
| `TKNG_Trash` | |
| `TNTExplodey` | |
| `TT_ManaBurn` | |
| `TVChangeDie` | |
| `TVChangeDumb` | |
| `TVChangeObey` | |
| `TVChangeStop` | |
| `TVOff` | |
| `TallBotRocket` | |
| `TattersFear` | |
| `Taunt` | |
| `TeleportFlipUp` | |
| `TheChild_Pulse` | |
| `TheChild_ReleaseBeams` | |
| `TheChild_TargetBeam` | |
| `TheChild_TransformBoris` | |
| `TheChild_TransformExplosive` | |
| `TheChild_TransformHoly` | |
| `TheChild_Wrath` | |
| `TheCreator_Reaction` | |
| `TheCreator_SpawnCloneTeam` | |
| `TheMother_Birth` | |
| `ThornUp` | |
| `ThornUpX` | |
| `ThrobShot_Reaction` | |
| `Tina2Call` | |
| `TinaBasicJump` | |
| `TinaBodySlamMax` | |
| `TinaBodySlamRage` | |
| `TinaJumpAttack` | |
| `TinaSpit` | |
| `TinaSpit2` | |
| `TinaSuck` | |
| `TinaSuck2` | |
| `TinaTantrum` | |
| `TinaThrow` | |
| `TormentorBite` | |
| `TormentorRuneAbsorb` | |
| `TormentorSpawn` | |
| `TormentorSuck` | |
| `ToxGasBlast` | |
| `TrampleDash` | |
| `TrampyDrink` | |
| `TrampyDump` | |
| `TrampyFleas` | |
| `TrampySleep` | |
| `TrampySpit` | |
| `TrembloEat` | |
| `TrembloSuck` | |
| `TrexReacquireTarget` | |
| `TrexStomp` | |
| `TrexSwitchTarget` | |
| `TriceratopsTrample` | |
| `TumorPowerup` | |
| `TwistingFlames` | |
| `UFO_BigShield` | |
| `UFO_Detect` | |
| `UFO_Megalaser` | |
| `UFO_Shield` | |
| `UFO_Summon` | |
| `WaggleClone` | |
| `WaterTrailMove` | |
| `WereManPounce` | |
| `WereManTransformSwipe` | |
| `WhispererThrowBuff` | |
| `WhispererWhisper` | |
| `WizBlizzard` | |
| `WizFlamethrower` | |
| `WizSpellShield` | |
| `WizStorm` | |
| `WolfLeap` | |
| `XLightning` | |
| `YA_Charge` | |
| `YA_Jetpack` | |
| `YeetTowardsBuddy` | |
| `YetiBite` | |
| `YetiIceBreath` | |
| `YetiKick` | |
| `ZaratanaSoloBombardment` | |
| `ZaratanaSoloMagnet` | |
| `ZaratanaSoloRoar` | |
| `ZaratanaSoloSpinDash` | |
| `ZaratanaSoloTurtle` | |
| `ZaratanaSoloWeatherRoar` | |
| `ZaratanaVSBombardment` | |
| `ZaratanaVSExitTurtle` | |
| `ZaratanaVSMagnet` | |
| `ZaratanaVSRevenge` | |
| `ZaratanaVSRoar` | |
| `ZaratanaVSSpinDash` | |
| `ZaratanaVSTurtle` | |
| `ZaratanaVSTurtleGuaranteed` | |
| `ZaratanaVSWeatherRoar` | |
| `ZombieFeast` | |
| `ZombieFeastSmall` | |
| `set_GrubFamiliarReturn` | |
| `tw_TriachnidSpawn` | |

| `Absorb` | |
| `Absorb2` | |
| `AbsorbSoul` | |
| `AbsorbSoul2` | |
| `AcidShot` | |
| `Adoubement` | |
| `Adoubement2` | |
| `AfterImage` | |
| `Aftershock` | |
| `Aftershock2` | |
| `Agile` | |
| `AirBurst` | |
| `AirBurst2` | |
| `AlienBeam` | |
| `AlienBeastWideSwipe` | |
| `AlterDNA` | |
| `AlterDNA2` | |
| `AmoebaAttach` | |
| `AmoebaFace` | |
| `AmoebaHat` | |
| `AmoebaNeck` | |
| `AmoebaRockBash` | |
| `AncestorsBones` | |
| `AncestorsJaw` | |
| `AncestorsSkull` | |
| `AncestralRecall` | |
| `AncestralRecall2` | |
| `Anchor` | |
| `Anchor2` | |
| `AngelcatWind` | |
| `AnimateDead` | |
| `AnimateDead2` | |
| `AnimatedRockAttack` | |
| `AnkyloSwipe` | |
| `Anneal` | |
| `Anneal2` | |
| `Anoint` | |
| `Anoint2` | |
| `AntlerSwipe` | |
| `AntlerSwipe2` | |
| `Apprentice` | |
| `Apprentice2` | |
| `ArmorUp` | |
| `ArmorUp2` | |
| `ArrowFlurry` | |
| `ArrowFlurry2` | |
| `ArrowSmith` | |
| `ArrowSmith2` | |
| `Assassinate` | |
| `Assassinate2` | |
| `AssBlast` | |
| `AssBlast2` | |
| `AssertDominance` | |
| `AssertDominance2` | |
| `Asteroid` | |
| `Asteroid2` | |
| `AtomicBurst` | |
| `attack` | |
| `ATTACK_PLACEHOLDER_JesterBasic` | |
| `AttackAgain` | |
| `AttackAgain2` | |
| `AutoPilot` | |
| `AutoPilot2` | |
| `Awaken` | |
| `Awaken2` | |
| `AZ_BreakNeck` | |
| `AZ_Jump_AI` | |
| `BabySharkMelee` | |
| `BackBreaker` | |
| `BackBreaker2` | |
| `Backflip` | |
| `Backflip2` | |
| `BackflipDodge` | |
| `BackgroundTransitionTest` | |
| `BadBone` | |
| `BadGas` | |
| `BadGas2` | |
| `BallOfSpiders` | |
| `BallOfSpiders2` | |
| `Baptism` | |
| `Baptism2` | |
| `BarbedWire` | |
| `BarbedWire2` | |
| `BarfBall` | |
| `BarfBall2` | |
| `BasicAttackPool` | |
| `BasicBigMelee` | |
| `BasicButcherMelee` | |
| `BasicButcherMeleeWide` | |
| `BasicButcherMeleeWideDoubleSpin` | |
| `BasicButcherMeleeWideSpin` | |
| `BasicDashAttackMove` | |
| `BasicDashAttackMove_NoKnockback` | |
| `BasicDig` | |
| `BasicDrainMelee` | |
| `BasicDruidAbility` | |
| `BasicDruidAbilityVersatile` | |
| `BasicExplosiveShot` | |
| `BasicHook` | |
| `BasicJump` | |
| `BasicMagicMissile` | |
| `BasicMagicShortRanged` | |
| `BasicMedicMelee` | |
| `BasicMedicRanged` | |
| `BasicMelee` | |
| `BasicMelee_2Hits` | |
| `BasicMelee_3Hits` | |
| `BasicMelee_4Hits` | |
| `BasicMelee_5Hits` | |
| `BasicMelee_Fighter` | |
| `BasicMetronome` | |
| `BasicMonkMelee` | |
| `BasicMonkRanged` | |
| `BasicNecroRanged` | |
| `BasicPoke` | |
| `BasicPsychicPull` | |
| `BasicPuke` | |
| `BasicRanged` | |
| `BasicRanged_1DMG` | |
| `BasicRanged_Hunter` | |
| `BasicShortLobbed` | |
| `BasicShortLobbed_Water` | |
| `BasicShortRanged` | |
| `BasicSpin` | |
| `BasicStraightShot` | |
| `BasicStraightShot_Thief` | |
| `BasicSuplex` | |
| `BasicTankMelee` | |
| `BasicTwoHitMelee` | |
| `BatFlurry` | |
| `BatterUp` | |
| `BatterUp2` | |
| `BatteryNuke` | |
| `BatteryNuke2` | |
| `BattleCry` | |
| `BattleCry2` | |
| `BBExplode` | |
| `BBMutantSwipe` | |
| `BBQ` | |
| `BBQ2` | |
| `BBStabby` | |
| `BBXLightning` | |
| `BearFurySwipes` | |
| `BearHug` | |
| `BearHug2` | |
| `BearTrap` | |
| `BearTrap2` | |
| `BecomeEntropy` | |
| `BecomeEntropy2` | |
| `BelcherLavashot` | |
| `BellyFlop` | |
| `BellyFlop2` | |
| `BellyFlop_BasicMove` | |
| `Benediction` | |
| `Benediction2` | |
| `Berserk` | |
| `Berserk2` | |
| `BerserkDash` | |
| `BerserkDash2` | |
| `BestowWisdom` | |
| `BestowWisdom2` | |
| `BigAsteroidBarrage` | |
| `BigGunkShot` | |
| `BigPunch` | |
| `BigPunch2` | |
| `BigRock` | |
| `BigRock2` | |
| `BigWind` | |
| `Binge` | |
| `Binge2` | |
| `BirthSquirrel` | |
| `BirthSquirrel2` | |
| `BlackMagic` | |
| `BlackMagic2` | |
| `Blast` | |
| `Blast2` | |
| `BlessingOfHolyFire` | |
| `BlessingOfSpirit` | |
| `BlindingFlash` | |
| `BlindingFlash2` | |
| `BlindingLight` | |
| `BlindingLight2` | |
| `BlinkDodge` | |
| `Blizzard` | |
| `Blizzard2` | |
| `BloatEyeMovement` | |
| `BloatFrontLaser` | |
| `Block` | |
| `Block2` | |
| `BlockingRanged` | |
| `BloodGeyser` | |
| `BloodGeyser2` | |
| `Bloodletting` | |
| `Bloodletting2` | |
| `BloodMagic` | |
| `BloodMagic2` | |
| `BloodRain` | |
| `BloodRain2` | |
| `Bloodzerk` | |
| `Bloodzerk2` | |
| `Blow` | |
| `Blow2` | |
| `BlowKiss` | |
| `BlowKiss2` | |
| `Blur` | |
| `Blur2` | |
| `BodyGuard` | |
| `BodyGuard2` | |
| `BodyGuardSwap` | |
| `BodyGuardSwap2` | |
| `BodySlam` | |
| `BodySlam2` | |
| `Bolt` | |
| `Bolt2` | |
| `Bombchu` | |
| `Bombchu2` | |
| `BombExplode` | |
| `BombFlyExplode` | |
| `BombShot` | |
| `BombShot2` | |
| `BoneWormShotMed` | |
| `BoneWormShotSmall` | |
| `BoneWormShotTall` | |
| `BonusToss` | |
| `BonusToss2` | |
| `BoostBackstab` | |
| `BoostBackstab2` | |
| `Booster` | |
| `Booster2` | |
| `BoostSpellRange` | |
| `BoostSpellRange2` | |
| `BornAgain` | |
| `BornAgain2` | |
| `BounceDashTest` | |
| `BounceShot` | |
| `BounceShot2` | |
| `BountyHunter` | |
| `Bowl` | |
| `Bowl2` | |
| `BowlDash` | |
| `BowlDash2` | |
| `BowlOver` | |
| `BowlOver2` | |
| `BoyDinoBasic` | |
| `BoyDinoDash` | |
| `Brace` | |
| `Brace2` | |
| `BrainDrainMagicMissile` | |
| `Brainstorm` | |
| `Brainstorm2` | |
| `BrambleBurst` | |
| `BrambleBurst2` | |
| `BramblePull` | |
| `BrambleRandomTileEvent` | |
| `BrambleShot` | |
| `BrambleShot2` | |
| `BreakingPoint` | |
| `BreakingPoint2` | |
| `BreakShortCircuit` | |
| `BreakShortCircuit_Familiar` | |
| `BreakShortCircuit_Manaless` | |
| `BreakWeb` | |
| `Bruise` | |
| `Bruise2` | |
| `BuddyUp` | |
| `BuddyUp2` | |
| `BuildNuke` | |
| `BuildNuke2` | |
| `BuildTurret` | |
| `BuildTurret2` | |
| `Bump` | |
| `Bump2` | |
| `BungaJumpMove` | |
| `BungaSmash` | |
| `BungaSwipe_ai` | |
| `Bunker` | |
| `Bunker2` | |
| `BurgeoningBarrier` | |
| `BurgeoningBarrier2` | |
| `BurgeoningBattery` | |
| `BurgeoningBattery2` | |
| `BurgeoningBlast` | |
| `BurgeoningBlast2` | |
| `Burp` | |
| `Burp2` | |
| `Burst` | |
| `Burst2` | |
| `Butcher` | |
| `Butcher2` | |
| `ButcherPurge` | |
| `ButcherPurge2` | |
| `ButtScoot` | |
| `ButtScoot2` | |
| `BuyCatnip` | |
| `BuyCatnip2` | |
| `CallOver` | |
| `CallOver2` | |
| `CallTheWind` | |
| `CallTheWind2` | |
| `Caltrops` | |
| `Caltrops2` | |
| `Camouflage` | |
| `Camouflage2` | |
| `CancerMelee` | |
| `Cannibalize` | |
| `CannonBall` | |
| `CannonBall2` | |
| `CarcusSpawn` | |
| `CarnibulbEat` | |
| `CarrionShot` | |
| `CarrionShot2` | |
| `CarrionShot_Afterlife` | |
| `CarrionShot_Afterlife2` | |
| `Cartwheel` | |
| `Cartwheel2` | |
| `CatAbilityPool` | |
| `CatapultJump` | |
| `CatapultJump2` | |
| `Catbot` | |
| `Catbot2` | |
| `CatchProjectiles` | |
| `CatGenAbilityPool` | |
| `CatNap` | |
| `CatNap2` | |
| `CatSpin` | |
| `CaveBabyMelee` | |
| `CaveCatPounce` | |
| `CaveChiefSlam` | |
| `CaveDad_ClubBasic` | |
| `CaveMan3HitCombo` | |
| `CaveManThrowSpear` | |
| `CaveMom_Basic` | |
| `CaveWomanCatSlap` | |
| `CaveWomanEscape` | |
| `CaveWomanKick` | |
| `CBShoot` | |
| `CerberubsJump` | |
| `CerberubsJump_AI` | |
| `ChaChaSlide` | |
| `ChaChaSlide2` | |
| `ChainKnockback` | |
| `ChainLightning` | |
| `ChainLightning2` | |
| `Chakram` | |
| `Chakram2` | |
| `Challenge` | |
| `Challenge2` | |
| `ChaosRampage` | |
| `ChaosRampage2` | |
| `ChaosShot` | |
| `ChaosShot2` | |
| `ChaosStacyAttack` | |
| `ChaosStacyAttackChain` | |
| `ChaosSwap` | |
| `ChaosSwap2` | |
| `ChaosTeleport` | |
| `ChaosTeleport2` | |
| `ChargeFists` | |
| `ChargeFists2` | |
| `CharmTrap` | |
| `CharmTrap2` | |
| `Cheat` | |
| `Cheat2` | |
| `Cheerlead` | |
| `Cheerlead2` | |
| `CherubimHeal` | |
| `CherubMelee` | |
| `Chew` | |
| `Chew2` | |
| `ChewCud` | |
| `ChewCud2` | |
| `Chitter` | |
| `Chomp` | |
| `Chomp2` | |
| `Chonkwalk` | |
| `Chonkwalk2` | |
| `ChosenWarrior` | |
| `ChosenWarrior2` | |
| `CHToss` | |
| `ChubsSpin` | |
| `ChubsSpinRage` | |
| `ChumDash` | |
| `ChumShot_Damage` | |
| `CHuskBone` | |
| `CHuskStruggle` | |
| `CircleOfProtection` | |
| `CircleOfProtection2` | |
| `Clap` | |
| `Clap2` | |
| `Cleanse` | |
| `Cleanse2` | |
| `ClewOfLeeches` | |
| `ClewOfLeeches2` | |
| `CloakerHex` | |
| `CloseConvert` | |
| `cm_AllStatsBuff` | |
| `cm_Antidote` | |
| `cm_BigToe` | |
| `cm_Bullseye` | |
| `cm_ButcherSeal` | |
| `cm_Catnip` | |
| `cm_ChaBuff` | |
| `cm_ClassSeal` | |
| `cm_ClericSeal` | |
| `cm_ColorlessSeal` | |
| `cm_ConBuff` | |
| `cm_DexBuff` | |
| `cm_DruidSeal` | |
| `cm_EatHummingbird` | |
| `cm_Enema` | |
| `cm_ExperimentX` | |
| `cm_FighterSeal` | |
| `cm_ForbiddenFruit` | |
| `cm_ForbiddenPill` | |
| `cm_Gizzard` | |
| `cm_Heal` | |
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
| `cm_Lard_Impl` | |
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
| `cm_RaptorEggSpawn` | |
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
| `CoffinFlop` | |
| `CoffinFlop2` | |
| `CoffinFlop_Afterlife` | |
| `CoffinFlop_Afterlife2` | |
| `CoinToss` | |
| `CoinToss2` | |
| `ColdShoulder` | |
| `ColdShoulder2` | |
| `CollectiveCounterImpl` | |
| `CollectiveCounterImpl_ai` | |
| `CollectiveSpin` | |
| `CollectiveSpinImpl` | |
| `CollectPelt` | |
| `CollectPelt2` | |
| `ColorlessAbilities` | |
| `ColorlessCat_Push` | |
| `ComboPull` | |
| `ComboPull2` | |
| `ComboThrow` | |
| `ComboThrow2` | |
| `Confront` | |
| `Confront2` | |
| `Confusion` | |
| `Confusion2` | |
| `Consume` | |
| `Consume2` | |
| `Contaminate` | |
| `Contaminate2` | |
| `Contort` | |
| `Contort2` | |
| `ControlAir` | |
| `ControlAir2` | |
| `ControlPlants` | |
| `ControlPlants2` | |
| `ControlPlantsPartTwo` | |
| `ControlPlantsPartTwo2` | |
| `ControlWater` | |
| `ControlWater2` | |
| `ControlWaterPartTwo` | |
| `ControlWaterPartTwo2` | |
| `Convert` | |
| `Convert2` | |
| `Copycat` | |
| `Copycat2` | |
| `CoreFreakAttack` | |
| `Corrupt` | |
| `Corrupt2` | |
| `CosmicPunch` | |
| `CosmicPunch2` | |
| `Cough` | |
| `Cough2` | |
| `Counter` | |
| `Counter2` | |
| `CPR` | |
| `CPR2` | |
| `Craft` | |
| `Craft2` | |
| `CraftArrow` | |
| `CraftArrow2` | |
| `CraterCreeperGush` | |
| `CraterCreeperRockBlast` | |
| `CreepMelee` | |
| `CreepRanged` | |
| `Creshendo` | |
| `Creshendo2` | |
| `CrohnsPoop` | |
| `CrossShot` | |
| `CrossShot2` | |
| `Crusade` | |
| `Crusade2` | |
| `Crushinator` | |
| `Crushinator2` | |
| `CryoHeal` | |
| `CryoHeal2` | |
| `CumulativeBlast` | |
| `CumulativeBlast2` | |
| `CupidsArrow` | |
| `CupidsArrow2` | |
| `Curse` | |
| `Curse2` | |
| `CutPurse` | |
| `CutPurse2` | |
| `D6Knives` | |
| `D6Leech` | |
| `DaddyHungry` | |
| `DarkOneStrike` | |
| `DarkStep` | |
| `DarkStep2` | |
| `Dart` | |
| `Dart2` | |
| `Dash` | |
| `Dash2` | |
| `Dash_BabyDeathWorm` | |
| `Dash_Enemy` | |
| `DashRandomly` | |
| `DealWithTheDevil` | |
| `DealWithTheDevil2` | |
| `DeathBloom` | |
| `DeathBloom2` | |
| `DeathMetal` | |
| `DeathMetal2` | |
| `DeathWind` | |
| `DeathWind2` | |
| `DeathWormTrampleDash` | |
| `DeathWormTrampleDash_Reaction_ai` | |
| `Debone` | |
| `Debone2` | |
| `Declaw` | |
| `Declaw2` | |
| `DecoySwap` | |
| `DeepDive` | |
| `DeepDive2` | |
| `DeliciousScent` | |
| `DeliciousScent2` | |
| `Demolish` | |
| `Demolish2` | |
| `DemonicPact` | |
| `DemonicPact2` | |
| `DemonUppercut` | |
| `Desecrate` | |
| `Desecrate2` | |
| `DestroyerAttack` | |
| `DestroyerAttack2` | |
| `DestroyerShieldBash` | |
| `DetectWeakness` | |
| `DetectWeakness2` | |
| `DexterousHit` | |
| `DexterousHit2` | |
| `DH_Attack` | |
| `DiagonalBasicMelee` | |
| `DiagonalDashTest` | |
| `DiagonalSpell` | |
| `DigUpTheDead` | |
| `DigUpTheDead2` | |
| `DinoEggsSpawn` | |
| `DipShot` | |
| `Discharge` | |
| `Discharge2` | |
| `Distract` | |
| `Distract2` | |
| `Diversion` | |
| `Diversion2` | |
| `Divide` | |
| `Divide2` | |
| `DivineGift` | |
| `DivineGift2` | |
| `DivineProtection` | |
| `DivineProtection2` | |
| `DoctorBotHeal` | |
| `DollUp` | |
| `DollUp2` | |
| `Donate` | |
| `Donate2` | |
| `DonateBlood` | |
| `DonateBlood2` | |
| `DonateBlood_Afterlife` | |
| `DonateBlood_Afterlife2` | |
| `DonateEnergy` | |
| `DonateEnergy2` | |
| `DoomPunch` | |
| `DoomPunch2` | |
| `Double` | |
| `Double2` | |
| `DoubleDiagonalCreepshot` | |
| `DoubleDragon` | |
| `DoubleDragon2` | |
| `DoubleLoot` | |
| `DoubleLoot2` | |
| `DragonPunch` | |
| `DragonPunch2` | |
| `DrawAttention` | |
| `DrawAttention2` | |
| `DrDRockets` | |
| `DrDRockets_ai` | |
| `DrillDown` | |
| `DrillDown2` | |
| `DruidCatBasic` | |
| `DruidSwap` | |
| `DruidSwap2` | |
| `DumbMove` | |
| `DumbMove2` | |
| `DumbMove_Impl` | |
| `DumbMuscle` | |
| `Dump` | |
| `Dump2` | |
| `DustMelee` | |
| `DustMove` | |
| `Dybbuk_StopHittingYourself` | |
| `DybbukBackflipDodge` | |
| `DybbukLick` | |
| `DysenteryPoop` | |
| `EagleEye` | |
| `EagleEye2` | |
| `Earthquake` | |
| `Earthquake2` | |
| `EatRock` | |
| `EatRock2` | |
| `EatShit` | |
| `Echo` | |
| `Echo2` | |
| `EjectButton` | |
| `EjectButton2` | |
| `ElectricNail` | |
| `ElectricNail2` | |
| `Electrolyze` | |
| `Electrolyze2` | |
| `ElementalAttunement` | |
| `ElkForm` | |
| `ElkForm2` | |
| `Emergency` | |
| `Emergency2` | |
| `EmptyMind` | |
| `EmptyMind2` | |
| `Encourage` | |
| `Encourage2` | |
| `Endeavor` | |
| `Endeavor2` | |
| `Endeavor_Auto` | |
| `Enlarge` | |
| `Enlarge2` | |
| `Enlighten` | |
| `Enlighten2` | |
| `Enrage` | |
| `Enrage2` | |
| `Entangle` | |
| `Entangle2` | |
| `EnterMech` | |
| `Escape` | |
| `EscapeBase` | |
| `Ethereal` | |
| `Ethereal2` | |
| `Eureka` | |
| `Eureka2` | |
| `EvilIncarnate` | |
| `EvilIncarnate2` | |
| `Exert` | |
| `Exert2` | |
| `ExhaustingBlow` | |
| `ExhaustingBlow2` | |
| `ExperimentalTeleporter` | |
| `ExperimentalTeleporter2` | |
| `Extend` | |
| `Extend2` | |
| `ExtraTurnQuestion` | |
| `ExtraTurnQuestion2` | |
| `EyeForAnEye` | |
| `EyeForAnEye2` | |
| `Fabricate` | |
| `Fabricate2` | |
| `face_EatNeverstone` | |
| `face_FartFace` | |
| `face_FartFaceFixed` | |
| `face_LeechBrood` | |
| `face_StevenMask2` | |
| `FaceGrub` | |
| `Fade` | |
| `Fade2` | |
| `FalconPunch` | |
| `FalconPunch2` | |
| `FamiliarSelfDestruct` | |
| `FamiliarSelfDestruct2` | |
| `Fartoom` | |
| `Fartoom2` | |
| `FastForward` | |
| `FastForward2` | |
| `FastHands` | |
| `FastHands2` | |
| `FatCatBellyFlop` | |
| `FatManLunge` | |
| `FaultLine` | |
| `FaultLine2` | |
| `FeatherFeet` | |
| `FeatherFeet2` | |
| `Feed` | |
| `Feed2` | |
| `FeralMelee` | |
| `FetusAirstrike` | |
| `FetusGush` | |
| `FetusJarDeath` | |
| `FetusSpit` | |
| `FighterBonusThrow` | |
| `FighterLeap` | |
| `FighterLeap2` | |
| `FighterTaunt` | |
| `FighterTaunt2` | |
| `FindARock` | |
| `FindARock2` | |
| `Finisher` | |
| `Finisher2` | |
| `FireArmor` | |
| `FireArmor2` | |
| `Fireball` | |
| `Fireball2` | |
| `FireBolt` | |
| `FireBolt2` | |
| `Firecrackers` | |
| `Firecrackers2` | |
| `FireFart` | |
| `FireFart2` | |
| `FirePunch` | |
| `FirePunch2` | |
| `FireShot` | |
| `FireShot2` | |
| `FireSurge` | |
| `FireSurge2` | |
| `Fissure` | |
| `Fissure2` | |
| `FistOfFate` | |
| `FistOfFate2` | |
| `Five` | |
| `FlailBase` | |
| `Flamethrower` | |
| `FlashBack` | |
| `FlashForward` | |
| `FlashForward2` | |
| `Flatline` | |
| `Flatline2` | |
| `FleaShot` | |
| `FleaShot2` | |
| `FleshGolem` | |
| `FleshGolem2` | |
| `FleshLadDoublehit` | |
| `FleshyMindDisable` | |
| `Flex` | |
| `Flex2` | |
| `Flicker` | |
| `Flicker2` | |
| `Flip` | |
| `Flip2` | |
| `FlipACoin` | |
| `FlipFlop` | |
| `FlipFlop2` | |
| `FloastPull` | |
| `FloaterMelee` | |
| `FloatMove` | |
| `FlowerEventSleep` | |
| `FlowerFeet` | |
| `FlowerFeet2` | |
| `Flush` | |
| `FlyHat` | |
| `FlyingFist` | |
| `FlyingFist2` | |
| `FlyMask` | |
| `FlyNeck` | |
| `Focus` | |
| `Focus2` | |
| `FocusShot` | |
| `FocusShot2` | |
| `FollowUpDash` | |
| `FollowUpDash2` | |
| `FoodMove` | |
| `ForbiddenFamine` | |
| `ForbiddenFamine2` | |
| `ForbiddenFart` | |
| `ForbiddenFart2` | |
| `ForbiddenFlame` | |
| `ForbiddenFlame2` | |
| `ForbiddenFlood` | |
| `ForbiddenFlood2` | |
| `ForbiddenFrost` | |
| `ForbiddenFrost2` | |
| `ForbiddenFulmination` | |
| `ForbiddenFulmination2` | |
| `ForceBlast` | |
| `ForceBlast2` | |
| `ForceCone` | |
| `ForceCone2` | |
| `ForceFeed` | |
| `ForceFeed2` | |
| `ForceTrample` | |
| `Four` | |
| `FreezeRay` | |
| `FreezeRay2` | |
| `FreezerBurn` | |
| `FreezerBurn2` | |
| `FreshOffTheForge` | |
| `FreshOffTheForge2` | |
| `FriendOrFoe` | |
| `FriendOrFoe2` | |
| `FromTheTrees` | |
| `FromTheTrees2` | |
| `FullForce` | |
| `FullForce2` | |
| `FullMoon` | |
| `FullMoon2` | |
| `FurnitureBox` | |
| `FurnitureBox_Rare` | |
| `FurySwipes` | |
| `FurySwipes2` | |
| `FurySwipes_Enemy` | |
| `FurySwipes_Hitler` | |
| `FutureBotPunch` | |
| `FutureSight` | |
| `FutureSight2` | |
| `FuzzerJump` | |
| `G3CoughMaggot` | |
| `G3PrisonSpit` | |
| `G3Rage` | |
| `G3Scream_Debuff` | |
| `G3Scream_Fear` | |
| `GA_Telekinesis` | |
| `GA_Telekinesis_Big` | |
| `GainThorns` | |
| `GainThorns2` | |
| `Gamble` | |
| `Gamble2` | |
| `GameteInflate` | |
| `GameteSpawn` | |
| `GangUp` | |
| `GangUp2` | |
| `GasBlast` | |
| `GasCanExplode` | |
| `Gassy_AssBlast` | |
| `Gassy_AssBlast2` | |
| `GeminiBite` | |
| `GerdShot` | |
| `GetDown` | |
| `GetDown2` | |
| `Gib` | |
| `Gib2` | |
| `GigaDrain` | |
| `GigaDrain2` | |
| `GirlDinoMelee` | |
| `GKSuck` | |
| `Glare` | |
| `Glare2` | |
| `GlowingBone` | |
| `GoLimp` | |
| `GoLimp2` | |
| `GooseStep` | |
| `Gore` | |
| `Gore2` | |
| `GorgerGorge` | |
| `Grace` | |
| `Grace2` | |
| `GrantLife` | |
| `GrantLife2` | |
| `Grapnel` | |
| `Grapnel2` | |
| `Grapple` | |
| `Grapple2` | |
| `GrassEvent` | |
| `Gravecrawl` | |
| `Gravecrawl2` | |
| `GravitySlam` | |
| `GravitySlam2` | |
| `GreedStep` | |
| `GreedStep2` | |
| `Grill` | |
| `Grill2` | |
| `Groom` | |
| `Groom2` | |
| `GrowHead` | |
| `GSChew` | |
| `GSClosedAttack` | |
| `GSOpenAttack` | |
| `GSSpit` | |
| `GuardianAngel` | |
| `GuardianAngel2` | |
| `GuncatShoot` | |
| `GunkShot` | |
| `Gust` | |
| `Gust2` | |
| `GymMembership` | |
| `GymMembership2` | |
| `Hadouken` | |
| `Hadouken2` | |
| `HailOfNails` | |
| `HailOfNails2` | |
| `HallowedGround` | |
| `HallowedGround2` | |
| `Hallucinate` | |
| `Hallucinate2` | |
| `Hallucinate_Disorder` | |
| `HammerSmash` | |
| `HangerBotAttack` | |
| `HardenSkin` | |
| `HardenSkin2` | |
| `Harpoon` | |
| `Harpoon2` | |
| `Haste` | |
| `Haste2` | |
| `Haunt` | |
| `Hazardous` | |
| `HCAttack` | |
| `HCSpin` | |
| `head_CatChestPound` | |
| `head_CrownOfHorns` | |
| `head_EmoSong` | |
| `head_HeadBrandJump` | |
| `head_HitlersToupe` | |
| `head_IronJaw` | |
| `head_MagnetoAttract` | |
| `head_MiniMoonArmorAsteroid` | |
| `head_Pestilence` | |
| `head_SpiderInjector` | |
| `head_SpiderInjectorFixed` | |
| `head_ThrobbingCrown` | |
| `HeadButt` | |
| `HeadButt2` | |
| `HeadGrub` | |
| `HeadTumorAttack` | |
| `HealBolt` | |
| `HealBolt2` | |
| `HealBomb` | |
| `HealingFall` | |
| `HealingFall2` | |
| `HealingSalve` | |
| `HealingSalve2` | |
| `Heathens` | |
| `Heathens2` | |
| `HeavyShot` | |
| `HeavyShot2` | |
| `HellHandGrab` | |
| `HemShot` | |
| `HereticMark` | |
| `HereticMark2` | |
| `HexShot` | |
| `HipToss` | |
| `HipToss2` | |
| `HireHitman` | |
| `HireHitman2` | |
| `Hiss` | |
| `Hiss2` | |
| `Hit` | |
| `HitlerCloneSwipes` | |
| `HitlerHeadTransform_Chain` | |
| `HitlerPulpBase` | |
| `HitlerShoot` | |
| `HitMe` | |
| `HogRush` | |
| `HogRush2` | |
| `HolyBlood` | |
| `HolyBlood2` | |
| `HolyLight` | |
| `HolyLight2` | |
| `HolyStep` | |
| `HolyStep2` | |
| `HolyWeapon` | |
| `HolyWeapon2` | |
| `HomingBlasts` | |
| `HomingBlasts2` | |
| `HomingBlasts2_sub` | |
| `HomingBlasts_sub` | |
| `Hone` | |
| `Hone2` | |
| `HookBind` | |
| `HookBind2` | |
| `HopAndBlock` | |
| `HopAndBlock2` | |
| `HornCharge` | |
| `HornyToadShot` | |
| `HoseOff` | |
| `HoseOff2` | |
| `Host` | |
| `HostSpit` | |
| `Huddle` | |
| `Huddle2` | |
| `Huddle_Impl` | |
| `HundredHandSlap` | |
| `HundredHandSlap2` | |
| `Hunt` | |
| `Hunt2` | |
| `HunterMinibossMove` | |
| `Hurl` | |
| `Hurl2` | |
| `Hush` | |
| `Hush2` | |
| `HuskSwipes` | |
| `HydroPump` | |
| `HydroPump2` | |
| `HyperBeam` | |
| `HyperBeam2` | |
| `IceArmor` | |
| `IceArmor2` | |
| `IceElementalBreath_ai` | |
| `IceElementalSpikes` | |
| `IcePunch` | |
| `IcePunch2` | |
| `IceSurge` | |
| `IceSurge2` | |
| `IcicleTaser` | |
| `IcicleTaser2` | |
| `Improve` | |
| `Improve2` | |
| `IncreaseGravity` | |
| `IncreaseGravity2` | |
| `Indigestion_Fart` | |
| `Indigestion_Fart2` | |
| `Inferno` | |
| `Inferno2` | |
| `Infest` | |
| `Infest2` | |
| `Infiltrate` | |
| `Infiltrate2` | |
| `Inhale` | |
| `Inhale2` | |
| `InspirationalSong` | |
| `InspirationalSong2` | |
| `Inspire` | |
| `Inspire2` | |
| `InstantBarrier` | |
| `InstantBarrier2` | |
| `Interchange` | |
| `Interchange2` | |
| `Intimidate` | |
| `Intimidate2` | |
| `InvaderAttack` | |
| `InvaderExplode` | |
| `Inversion` | |
| `Inversion2` | |
| `IronHead` | |
| `IronHead2` | |
| `IrradiatedObject_Bleed` | |
| `IrradiatedObject_Bruise` | |
| `IrradiatedObject_Burn` | |
| `IrradiatedObject_Charmed` | |
| `IrradiatedObject_Confusion` | |
| `IrradiatedObject_Fear` | |
| `IrradiatedObject_Poison` | |
| `IrradiatedObject_Sleep` | |
| `IrradiatedObject_Stun` | |
| `IrradiatedObject_Weakness` | |
| `IsaacBasicAttack` | |
| `Itch` | |
| `Itch2` | |
| `JackAttack` | |
| `JarHeadDeath` | |
| `Jitter` | |
| `Jitter2` | |
| `JohnnyMissile` | |
| `Jolt` | |
| `Jolt2` | |
| `Juiced` | |
| `Juiced2` | |
| `Kamehameha` | |
| `Kamehameha2` | |
| `KiBurst` | |
| `KiBurst2` | |
| `KidneyStone` | |
| `KillDoze` | |
| `KineticCharge` | |
| `KineticCharge2` | |
| `KirbySpit` | |
| `KirbySpitAI` | |
| `KirbySuck` | |
| `Knead` | |
| `Knead2` | |
| `KnockCoinsMelee` | |
| `Lacerate` | |
| `Lacerate2` | |
| `Landscape` | |
| `Landscape2` | |
| `LargeMeteor` | |
| `LaserBombTest` | |
| `LaserTest` | |
| `LastGasp` | |
| `LastGasp2` | |
| `LastHit` | |
| `LastHit2` | |
| `LastThought` | |
| `LastThought2` | |
| `LatentEnergy` | |
| `LeapClose` | |
| `LearnAbility` | |
| `LearnPassive` | |
| `LEBurst` | |
| `LeechDash` | |
| `Leeches` | |
| `Leeches2` | |
| `LeechSwarm` | |
| `LeechSwarm2` | |
| `LennyShove` | |
| `LennyStruggle` | |
| `LennyTrampleMove` | |
| `LiceBite` | |
| `Lick` | |
| `LickHeal` | |
| `LickHeal2` | |
| `LifeDrain` | |
| `LifeDrain2` | |
| `LifeDrain_Afterlife` | |
| `LifeDrain_Afterlife2` | |
| `LightenTheLoad` | |
| `LightenTheLoad2` | |
| `LightningSurge` | |
| `LightningSurge2` | |
| `LineShot` | |
| `LineShot2` | |
| `LodgeHook` | |
| `LodgeHook2` | |
| `LookAtMe` | |
| `LookAtMe2` | |
| `LookTowardsCenter` | |
| `LookTowardsMe` | |
| `LookTowardsMeOne` | |
| `LootCorpse` | |
| `LootCorpse2` | |
| `LotteryShottery` | |
| `LotteryShottery2` | |
| `LoveBotHeal` | |
| `LoveTap` | |
| `LoveTap2` | |
| `LuckyPenny` | |
| `LuckyPenny2` | |
| `Lullaby` | |
| `Lullaby2` | |
| `LunchTime` | |
| `LunchTime2` | |
| `Lunge` | |
| `Lunge2` | |
| `MageSwap` | |
| `MageSwap2` | |
| `MageTeleport` | |
| `MageTeleport2` | |
| `MaggotArmy` | |
| `MaggotArmy2` | |
| `MagicGuru` | |
| `MagicMissile` | |
| `MagicMissile2` | |
| `Magnet` | |
| `Magnet2` | |
| `Magnetize_AI` | |
| `MagnetPull` | |
| `MagnetPull2` | |
| `Magnify` | |
| `Magnify2` | |
| `Malaise` | |
| `Malaise2` | |
| `MammothBabyThrow` | |
| `MammothThrow` | |
| `ManaBomb` | |
| `ManaBomb2` | |
| `ManaDrain` | |
| `ManaDrain2` | |
| `ManaMeld` | |
| `ManaMeld2` | |
| `ManglerCommand` | |
| `ManglerJab` | |
| `ManglerMonsterDashAttack` | |
| `Manifest` | |
| `Manifest2` | |
| `Marked` | |
| `Marked2` | |
| `MarkJump` | |
| `MassHeal` | |
| `MassHysteria` | |
| `MassHysteria2` | |
| `MassManaLeech` | |
| `MassManaLeech2` | |
| `MassPsychosis` | |
| `MassPsychosis2` | |
| `Math` | |
| `Math2` | |
| `MaxTeleport` | |
| `MCMelee` | |
| `MCMonkStyleChange` | |
| `MD_PoopChain` | |
| `MD_PoopChainAI` | |
| `MD_Stomp` | |
| `MD_Walk` | |
| `MD_WalkOne` | |
| `MeatMinionMelee` | |
| `MechExplode` | |
| `MechSuit` | |
| `MechSuit2` | |
| `MechSuitPunch` | |
| `MedicObey` | |
| `MedicObey2` | |
| `Meditate` | |
| `Meditate2` | |
| `Medusa` | |
| `Medusa2` | |
| `MegaBlast` | |
| `MegaBlast2` | |
| `MegaFart` | |
| `MegafetusMelee_ai` | |
| `MegafetusSpin` | |
| `MegaGrav` | |
| `MegaGrav2` | |
| `MegaGuppy_DropTrash` | |
| `MeleeHeal` | |
| `MeleeHeal2` | |
| `Meow` | |
| `Meow2` | |
| `Metabolize` | |
| `Metabolize2` | |
| `MeteorSlam` | |
| `MeteorSlam2` | |
| `MeteorStorm` | |
| `MeteorStorm2` | |
| `Metronome` | |
| `Metronome2` | |
| `Mimic` | |
| `Mimic2` | |
| `MindBlast` | |
| `MindBlast2` | |
| `MindControl` | |
| `MindControl2` | |
| `MindCrack` | |
| `MindCrack2` | |
| `MindCrack_EldritchVisage` | |
| `MindCrack_EldritchVisage2` | |
| `MindMeld` | |
| `MindMeld2` | |
| `MiniDistract` | |
| `MiniDistract2` | |
| `MiniFart` | |
| `MiniHook` | |
| `MiniHook2` | |
| `MinorZap` | |
| `MM_Slap` | |
| `MockingbirdForm` | |
| `MockingbirdForm2` | |
| `MockSong` | |
| `MockSong2` | |
| `Momentum` | |
| `Momentum2` | |
| `Monch` | |
| `Monch2` | |
| `MoneyBag_Huge` | |
| `MoneyBag_Large` | |
| `MoneyBag_Medium` | |
| `MonkeyForm` | |
| `MonkeyForm2` | |
| `MonkeyThrow` | |
| `MonkeyThrow2` | |
| `MoonHandFlail` | |
| `MoonHandSlap` | |
| `MoonHandSqueeze` | |
| `MoonHead_KillHands` | |
| `MoonHeadCommandStopHittingYourself` | |
| `MoonHeadFlail` | |
| `MoonWormShot` | |
| `MostValuableCat` | |
| `MotherGrow` | |
| `MotherTumorForceGrow` | |
| `MotherTumorForcePass` | |
| `move` | |
| `MoveAgain` | |
| `MoveAgain2` | |
| `MoveAway` | |
| `MoveCenter` | |
| `MoveClose` | |
| `MoveForBarrage` | |
| `MoveForDash` | |
| `MoveForGrass` | |
| `MoveForPounce` | |
| `MoveForSpin` | |
| `MoveForThrow` | |
| `MoveFour` | |
| `MoveFourTrample` | |
| `MoveOneTrample` | |
| `MoveSpaced` | |
| `MoveThree` | |
| `MoveThreeTrample` | |
| `MoveTowards` | |
| `MoveTwoTrample` | |
| `MuscleMemory` | |
| `MuscleMemory2` | |
| `MutateOne` | |
| `Mutilate` | |
| `Mutilate2` | |
| `MyLeg` | |
| `MyTurn` | |
| `MyTurn2` | |
| `NailFlurry` | |
| `NailFlurry2` | |
| `NaturesBlessing` | |
| `NaturesBlessing2` | |
| `NCGravecrawlFAR` | |
| `neck_Brambles` | |
| `neck_ChefsApron` | |
| `neck_DarkFriend` | |
| `neck_NukeBonus` | |
| `neck_NukeBonus_remote` | |
| `neck_NukeExplode` | |
| `neck_TentacleArmorCounter` | |
| `NeckGrub` | |
| `NeedleShot` | |
| `NeedleShot2` | |
| `Nerf` | |
| `Nerf2` | |
| `Nightshade` | |
| `Nightshade2` | |
| `Nip` | |
| `Nip2` | |
| `Nirvana` | |
| `Nirvana2` | |
| `None` | |
| `Normal` | |
| `NubbyToss` | |
| `NubsJump` | |
| `NubsJump_AI` | |
| `Nudge` | |
| `Nudge2` | |
| `NurseBot` | |
| `NurseBot2` | |
| `NurseBotHealCat` | |
| `One` | |
| `OnePunch` | |
| `OnePunch2` | |
| `OneTwoPunch` | |
| `OneTwoPunch2` | |
| `OneWithTheWind` | |
| `OneWithTheWind2` | |
| `OpenWounds` | |
| `OpenWounds2` | |
| `Order` | |
| `Order2` | |
| `Outskirts` | |
| `Outskirts2` | |
| `ParanoiaBasicMelee` | |
| `Parasaurolophus_Gore` | |
| `Parasaurolophus_Push` | |
| `ParasiterShoot` | |
| `ParasiteShot` | |
| `Pass` | |
| `Pass2` | |
| `PathOfTheButcher` | |
| `PathOfTheButcher2` | |
| `PathOfTheCleric` | |
| `PathOfTheCleric2` | |
| `PathOfTheDruid` | |
| `PathOfTheDruid2` | |
| `PathOfTheFighter` | |
| `PathOfTheFighter2` | |
| `PathOfTheHunter` | |
| `PathOfTheHunter2` | |
| `PathOfTheJester` | |
| `PathOfTheJester2` | |
| `PathOfTheMage` | |
| `PathOfTheMage2` | |
| `PathOfTheMonk` | |
| `PathOfTheMonk2` | |
| `PathOfTheNecromancer` | |
| `PathOfTheNecromancer2` | |
| `PathOfThePsychic` | |
| `PathOfThePsychic2` | |
| `PathOfTheTank` | |
| `PathOfTheTank2` | |
| `PathOfTheThief` | |
| `PathOfTheThief2` | |
| `PathOfTheTinkerer` | |
| `PathOfTheTinkerer2` | |
| `PathOfTheVoid` | |
| `PathOfTheVoid2` | |
| `Pawbreaker` | |
| `Pawbreaker2` | |
| `PerfectForm` | |
| `PerfectForm2` | |
| `PersistentHunt` | |
| `PersistentHunt2` | |
| `Pestilence` | |
| `Pestilence2` | |
| `Pheromones` | |
| `Pheromones2` | |
| `PickPocket` | |
| `PickPocket2` | |
| `Picnic` | |
| `Picnic2` | |
| `Pierce` | |
| `Pierce2` | |
| `PierceShot` | |
| `PierceShot2` | |
| `PierceShotTest` | |
| `Pilfer` | |
| `Ping` | |
| `Ping2` | |
| `PissYourself` | |
| `PissYourself2` | |
| `PlantFeet` | |
| `PlantFeet2` | |
| `PlantMushroom` | |
| `PlantMushroom2` | |
| `PlayDead` | |
| `PlayDead2` | |
| `Plow` | |
| `PocketSand` | |
| `PocketSand2` | |
| `Pogo` | |
| `Pogo2` | |
| `PoisonDip` | |
| `PoisonDip2` | |
| `PoisonGas` | |
| `PoisonGas2` | |
| `PoisonKnife` | |
| `PoisonLace` | |
| `PoisonLace2` | |
| `PoisonNail` | |
| `PoisonNail2` | |
| `PoisonShot` | |
| `Poke` | |
| `Poke2` | |
| `PokerAttack` | |
| `PokeWound` | |
| `PokeWound2` | |
| `Ponder` | |
| `Ponder2` | |
| `PoopCatMelee` | |
| `PopeyeDash` | |
| `Porcupine` | |
| `Porcupine2` | |
| `Position` | |
| `Position2` | |
| `Pounce` | |
| `Pounce2` | |
| `PowerUp` | |
| `PowerUp2` | |
| `PoxScratch` | |
| `Prance` | |
| `Prance2` | |
| `Pray` | |
| `Pray2` | |
| `Prayer` | |
| `Prayer2` | |
| `PrehistoricPooterShot` | |
| `PrepareToJump` | |
| `PrepareToJump2` | |
| `PrisonShot` | |
| `Promote` | |
| `Promote2` | |
| `Propell` | |
| `Propell2` | |
| `Protection` | |
| `Protection2` | |
| `PsychicChoke` | |
| `PsychicChoke2` | |
| `PsyFlutter` | |
| `PsyFlutter2` | |
| `PteroPeck` | |
| `PteroTryEscape` | |
| `PullToSafety` | |
| `PullToSafety2` | |
| `Pummel` | |
| `Pummel2` | |
| `PunchBot` | |
| `PunchBot2` | |
| `Puppet` | |
| `Puppet2` | |
| `Purge` | |
| `Purge2` | |
| `Purr` | |
| `Purr2` | |
| `Push` | |
| `Push2` | |
| `PushMove` | |
| `PushMove2` | |
| `PushThrough` | |
| `PushThrough2` | |
| `PyrophinaSoloAttack` | |
| `QuickAttack` | |
| `QuickAttack2` | |
| `QuickRoll` | |
| `QuickRoll2` | |
| `RaccoonForm` | |
| `RaccoonForm2` | |
| `RagePunch` | |
| `RagePunch2` | |
| `RaiseTheDead` | |
| `RaiseTheDead2` | |
| `Rally` | |
| `Rally2` | |
| `RallyCharge` | |
| `RallyCharge2` | |
| `Ram` | |
| `Ram2` | |
| `Ram_chained` | |
| `RandomDualSoulLink` | |
| `RandomReap` | |
| `RandomReap2` | |
| `RandomSoulLink` | |
| `RangedHeal` | |
| `RangedHeal2` | |
| `RangedMedic` | |
| `RapidFlowSpin` | |
| `RapidFlowSpin2` | |
| `RaptorBabyBite` | |
| `RatKingDash` | |
| `RatKingToss` | |
| `RatLeap` | |
| `RattleSnakeAttack` | |
| `Reach` | |
| `Reach2` | |
| `ReadMind` | |
| `ReadMind2` | |
| `RealityScramble` | |
| `RealityScramble2` | |
| `ReallyFastRun` | |
| `ReallyFastRun2` | |
| `Reanimate` | |
| `Reanimate2` | |
| `Reap` | |
| `Reap2` | |
| `ReaperSpin` | |
| `ReaperStep` | |
| `ReaperStep2` | |
| `Rebirth` | |
| `Rebirth2` | |
| `Rebound` | |
| `Rebound2` | |
| `Rebuke` | |
| `Rebuke2` | |
| `Recycle` | |
| `Recycle2` | |
| `Reduce` | |
| `Reduce2` | |
| `RefineMaterials` | |
| `RefineMaterials2` | |
| `Reflect` | |
| `Reflect2` | |
| `ReflexPunchJab` | |
| `ReflexPunchJab2` | |
| `Reflux` | |
| `Reflux2` | |
| `Regurge` | |
| `Regurge2` | |
| `Rehook` | |
| `Rehook2` | |
| `ReleaseEnergy` | |
| `ReleaseEnergy2` | |
| `RemoteDetonator` | |
| `RemoteDetonator2` | |
| `Repair` | |
| `Repair2` | |
| `RepairArmor` | |
| `RepairArmor2` | |
| `Replace` | |
| `Replace2` | |
| `Replicate` | |
| `Replicate2` | |
| `Reposition` | |
| `Reposition2` | |
| `Reprogram` | |
| `Reprogram2` | |
| `Research` | |
| `Research2` | |
| `Reset` | |
| `Reset2` | |
| `Rest` | |
| `Rest2` | |
| `Return` | |
| `ReturnA` | |
| `ReturnAnywhere` | |
| `ReturnAnywhereIgnoreTrample` | |
| `Reverberate` | |
| `Reverberate2` | |
| `ReverseDamage` | |
| `ReverseDamage2` | |
| `Revive` | |
| `Revive2` | |
| `RhinoForm` | |
| `RhinoForm2` | |
| `RNGCannon` | |
| `RNGCannon2` | |
| `Roast` | |
| `Roast2` | |
| `RobesBuff` | |
| `RoboVac` | |
| `RoboVac2` | |
| `RockBlast` | |
| `RockBlast2` | |
| `RockBlast_AI` | |
| `RockCrusher` | |
| `RockCrusher2` | |
| `RocketRide` | |
| `RocketRide2` | |
| `RocketSkates` | |
| `RocketSkates2` | |
| `RocketSkates_Bombchu` | |
| `RocketTurretShot` | |
| `RocksFallEvent` | |
| `RockTomb` | |
| `RockTomb2` | |
| `RockToss` | |
| `RockToss2` | |
| `RockySlam` | |
| `Roll` | |
| `Roll2` | |
| `Roomba_Bump` | |
| `RoughToss` | |
| `RoughToss2` | |
| `Rouse` | |
| `Rouse2` | |
| `RoverDash` | |
| `RubberFistBotPunch` | |
| `RunFar` | |
| `RussianRoulette` | |
| `RussianRoulette2` | |
| `SabertoothCatPounce` | |
| `SabertoothCubDoubleSwipe` | |
| `SafetyDance` | |
| `SafetyDance2` | |
| `Sandstorm` | |
| `Sandstorm2` | |
| `SBotAttack` | |
| `Scare` | |
| `Scare2` | |
| `ScaryFear` | |
| `SCAttack` | |
| `ScatterShot` | |
| `ScatterShot2` | |
| `Scavenge` | |
| `Scavenge2` | |
| `ScorpionSting` | |
| `ScoutMe` | |
| `ScoutMe2` | |
| `ScuffItOff` | |
| `ScuffItOff2` | |
| `Seance` | |
| `Seance2` | |
| `Seance_Afterlife` | |
| `Seance_Afterlife2` | |
| `SelfMutilate` | |
| `SelfMutilate2` | |
| `SentryMode` | |
| `SentryMode2` | |
| `Seppuku` | |
| `SeraphimX` | |
| `Serenade` | |
| `Serenade2` | |
| `set_HumanFleshSetCurse` | |
| `set_MummySetCurse` | |
| `set_PlanetSetGravity` | |
| `set_SpaceArmorJump` | |
| `set_WitchJump` | |
| `SeverArtery` | |
| `SeverArtery2` | |
| `Shadow` | |
| `Shadow2` | |
| `ShadowDagger` | |
| `Shadowshift` | |
| `Shadowshift2` | |
| `Shadowstep` | |
| `ShamblerDash` | |
| `Shank` | |
| `Shank2` | |
| `Shards` | |
| `Shards2` | |
| `Sharpen` | |
| `Sharpen2` | |
| `SharpenClaws` | |
| `SharpenClaws2` | |
| `SharpenNail` | |
| `SharpenNail2` | |
| `SharpNail` | |
| `SharpNail2` | |
| `Shatter` | |
| `Shatter2` | |
| `ShedScrap` | |
| `ShedScrap2` | |
| `Shift` | |
| `Shift2` | |
| `ShockTherapy` | |
| `ShockTherapy2` | |
| `Shockwave` | |
| `Shockwave2` | |
| `ShoddyJetpack` | |
| `ShoddyJetpack2` | |
| `ShootHere` | |
| `ShortCircuit` | |
| `ShortCircuit2` | |
| `ShortCreepshot` | |
| `ShortCreepshotCrater` | |
| `ShoulderCheck` | |
| `ShovingMatch` | |
| `Shred` | |
| `Shred2` | |
| `Shriek` | |
| `Shriek2` | |
| `SideSlash` | |
| `SideSlash2` | |
| `SideStep` | |
| `SideStep2` | |
| `SirenCall` | |
| `SkinDisguise` | |
| `SkinDisguise2` | |
| `SkinnedTripleDash` | |
| `SkinnedTripleDash_AI` | |
| `SkullBash` | |
| `SkullBash2` | |
| `SkunkTail` | |
| `SkyShatter` | |
| `SkyShatter2` | |
| `SlagBoner` | |
| `Slap` | |
| `Slapback` | |
| `Slapback2` | |
| `SleepDarts` | |
| `SleeperHold` | |
| `SleeperHold2` | |
| `SleepTalk` | |
| `Slice` | |
| `Slice2` | |
| `SliceAndDice` | |
| `SliceAndDice2` | |
| `SlingShade` | |
| `SlingShade2` | |
| `Slipstream` | |
| `Slipstream2` | |
| `SlipThrough` | |
| `SlipThrough2` | |
| `SlitWrists` | |
| `SlopThePigs` | |
| `SlopThePigs2` | |
| `Slow` | |
| `Slow2` | |
| `SlowAndSteady` | |
| `SM_IceBreath` | |
| `SM_Lavashot` | |
| `SM_LightningDash` | |
| `SM_Snow` | |
| `Smack` | |
| `Smack2` | |
| `SmallAsteroidBarrage` | |
| `SmallMeteor` | |
| `SmartMetronome` | |
| `SmartMetronome2` | |
| `Smash` | |
| `Smash2` | |
| `SmellBlood` | |
| `SmellBlood2` | |
| `Smolder` | |
| `Smolder2` | |
| `Snacks` | |
| `Snacks2` | |
| `Snatch` | |
| `Snatch2` | |
| `SneakUp` | |
| `SneakUp2` | |
| `Snipe` | |
| `Snipe2` | |
| `SongOfSpring` | |
| `SongOfSpring2` | |
| `SoothingGlow` | |
| `SoothingGlow2` | |
| `SoothingShot` | |
| `SoothingShot2` | |
| `SoulLink` | |
| `SoulLink2` | |
| `SoulReap` | |
| `SoulReap2` | |
| `SoulSuck` | |
| `SoulSuck2` | |
| `SoulTransfer` | |
| `SoulTransfer2` | |
| `SpareParts` | |
| `SpareParts2` | |
| `Sparks` | |
| `Sparks2` | |
| `SpawnBaitTrap` | |
| `SpawnBaitTrap2` | |
| `SpawnBomb_AI` | |
| `SpawnDecoy` | |
| `SpawnDecoy2` | |
| `SpawnFlea` | |
| `SpawnGas` | |
| `SpawnMaggot` | |
| `SpawnMaggotFriend` | |
| `SpawnMaggotFriend2` | |
| `SpawnMotherSpike` | |
| `SpawnMotherTumor` | |
| `SpawnPooterFriend` | |
| `SpawnPooterFriend2` | |
| `SpawnSpewerPill` | |
| `SpawnTerminatorMini_Base` | |
| `SpawnTomTomFriend` | |
| `SpawnTomTomFriend2` | |
| `SpearPoke` | |
| `SpearPokeTest` | |
| `SpearRun` | |
| `SpewerLobbed_Lava` | |
| `SpewerLobbed_Normal` | |
| `SpewerLobbed_Tar` | |
| `SpewerSpit` | |
| `SpewerSpit_AI` | |
| `SpewerSuck_base` | |
| `SpiderEgg` | |
| `SpiderEgg2` | |
| `SpiderInjector` | |
| `SpiderInjector2` | |
| `SpiderSuicideMelee` | |
| `SpikeTrap` | |
| `SpikeTrap2` | |
| `Spin` | |
| `Spin2` | |
| `SpiritBomb` | |
| `SpiritBomb2` | |
| `Spit` | |
| `Spit2` | |
| `SpitGlass` | |
| `Spoil` | |
| `Spoil2` | |
| `SpontaneouslyCombust` | |
| `Spook` | |
| `SpookieLick` | |
| `SpringShoes` | |
| `SpringShoes2` | |
| `SproutSpore` | |
| `Spur` | |
| `Spur2` | |
| `SquirrelForm` | |
| `SquirrelForm2` | |
| `SquirrelFurySwipes` | |
| `SquirrelSquad` | |
| `SquirrelSquad2` | |
| `StackTheDeck` | |
| `StackTheDeck2` | |
| `StacyCharm` | |
| `StakeOut` | |
| `StakeOut2` | |
| `Stalk` | |
| `Stalk2` | |
| `STARTER_PLACEHOLDER_Butcher` | |
| `STARTER_PLACEHOLDER_Colorless` | |
| `STARTER_PLACEHOLDER_Druid` | |
| `STARTER_PLACEHOLDER_Fighter` | |
| `STARTER_PLACEHOLDER_Hunter` | |
| `STARTER_PLACEHOLDER_Jester` | |
| `STARTER_PLACEHOLDER_Mage` | |
| `STARTER_PLACEHOLDER_Medic` | |
| `STARTER_PLACEHOLDER_Monk` | |
| `STARTER_PLACEHOLDER_Necromancer` | |
| `STARTER_PLACEHOLDER_Psychic` | |
| `STARTER_PLACEHOLDER_Tank` | |
| `STARTER_PLACEHOLDER_Thief` | |
| `STARTER_PLACEHOLDER_Tinkerer` | |
| `Stasis` | |
| `Stasis2` | |
| `StealKidney` | |
| `StealKidney2` | |
| `StealLuck` | |
| `StealLuck2` | |
| `StealTime` | |
| `StealTime2` | |
| `SteelSkin` | |
| `SteelSkin2` | |
| `StegoTailSwipe` | |
| `Step` | |
| `Step2` | |
| `Stick` | |
| `Stick2` | |
| `StickyShot` | |
| `Stimulants` | |
| `Stimulants2` | |
| `StoneFists` | |
| `StoneFists2` | |
| `StoneGaze` | |
| `StoneGaze2` | |
| `Stoopzerk` | |
| `Stoopzerk2` | |
| `StruggleBase` | |
| `SubwayRide` | |
| `SubwayRide2` | |
| `Succ` | |
| `Succ2` | |
| `SuckerPunch` | |
| `SuckerPunch2` | |
| `Suggestion` | |
| `Suggestion2` | |
| `SuicideMelee` | |
| `SummonBear` | |
| `SummonBear2` | |
| `SummonBones` | |
| `SummonBones2` | |
| `SummonBrambles` | |
| `SummonBrambles2` | |
| `SummonCatepillar` | |
| `SummonCatepillar2` | |
| `SummonCrow` | |
| `SummonCrow2` | |
| `SummonShade` | |
| `SummonShade2` | |
| `SummonSnake` | |
| `SummonSnake2` | |
| `SummonSquirrel` | |
| `SummonSquirrel2` | |
| `SummonToad` | |
| `SummonToad2` | |
| `SummonTurtle` | |
| `SummonTurtle2` | |
| `Sunburn` | |
| `Sunburn2` | |
| `SuperCrateBox` | |
| `SuperCrateBox2` | |
| `Supernova` | |
| `Supernova2` | |
| `Suplex` | |
| `Suplex2` | |
| `Supper` | |
| `Supper2` | |
| `Suppress` | |
| `Suppress2` | |
| `Surf` | |
| `Surf2` | |
| `Survivalist` | |
| `Swallow` | |
| `Swallow2` | |
| `SwapPositions` | |
| `SwapPositions_WideLoad` | |
| `SwapPositions_WideLoad2` | |
| `Swat` | |
| `Swat2` | |
| `SwiftSanctify` | |
| `SwiftSanctify2` | |
| `Swim` | |
| `SwimmerMove` | |
| `Switcheroo` | |
| `Switcheroo2` | |
| `Synthesize` | |
| `Synthesize2` | |
| `SZBShoot` | |
| `T2SpearMelee` | |
| `T3Leave` | |
| `T3Shoot` | |
| `T3YellB` | |
| `TacticalRetreat` | |
| `TacticalRetreat2` | |
| `TailWhip` | |
| `TailWhip2` | |
| `Taint` | |
| `Taint2` | |
| `TaintedOffering` | |
| `TaintedOffering2` | |
| `TallBotSuplex` | |
| `TallSpiderMelee` | |
| `TankRockSong` | |
| `TankRockSong2` | |
| `TankSwap` | |
| `TankSwap2` | |
| `TankTantrum` | |
| `TankTantrum2` | |
| `TankTrample` | |
| `TankTrample2` | |
| `TapLand` | |
| `TapLand2` | |
| `TarBall` | |
| `TattersLeeches` | |
| `TattersSpin` | |
| `Taunt2` | |
| `TC_Attack` | |
| `TC_DashReaction_AI` | |
| `Teach` | |
| `Teach2` | |
| `TeamFlex` | |
| `TeamFlex2` | |
| `TeamFlex_Impl` | |
| `TeamFlex_Impl2` | |
| `TeamSpin` | |
| `TeamSpin2` | |
| `Tease` | |
| `Tease2` | |
| `Telefrag` | |
| `Telefrag2` | |
| `Telekinesis` | |
| `Telekinesis2` | |
| `Teleport` | |
| `TemporalShards` | |
| `TemporalShards2` | |
| `TenTicklesAttack` | |
| `TenTicklesSwim` | |
| `TerminatorShotgun` | |
| `TerminatorSniper` | |
| `TerminatorUzi` | |
| `TerrainWalk` | |
| `TerrainWalk2` | |
| `TeslaBolt` | |
| `TeslaCoil` | |
| `TeslaCoil2` | |
| `TestGameEndingSequence` | |
| `TF_TargetAllies` | |
| `TF_TargetEnemies` | |
| `THC_KnockCoinsRanged` | |
| `Thicken` | |
| `Thicken2` | |
| `ThickSkull` | |
| `ThiefSwap` | |
| `ThiefSwap2` | |
| `ThiefSwapBack` | |
| `ThinkDeep` | |
| `ThinkDeep2` | |
| `ThinkTooHard` | |
| `ThinkTooHard2` | |
| `ThornyFeet` | |
| `ThornyFeet2` | |
| `ThouShaltNotKill` | |
| `Thrash` | |
| `ThrobShot` | |
| `ThrowEgg` | |
| `ThrowEgg2` | |
| `ThrowPoop` | |
| `ThrowShield` | |
| `ThrowShield2` | |
| `ThrowSpiritBomb` | |
| `ThrowSpiritBomb2` | |
| `ThumpSlam` | |
| `ThumpSlam_Mov` | |
| `Thunderburst` | |
| `Thunderburst2` | |
| `ThunderPunch` | |
| `ThunderPunch2` | |
| `TigerForm` | |
| `TigerForm2` | |
| `TigerSwipes` | |
| `TigerSwipes2` | |
| `Till` | |
| `Till2` | |
| `Timber` | |
| `TimeWalk` | |
| `TimeWalk2` | |
| `TinaBasicBigMelee` | |
| `TinaBasicBigMeleeA` | |
| `TinaBodySlam` | |
| `TinaFlail` | |
| `TinaFlailRage` | |
| `TinaHeadGutSpear` | |
| `TinkererCraft` | |
| `TinkererThrow` | |
| `tk_Asteroid` | |
| `tk_BagOfBags` | |
| `tk_BagOfSeeds` | |
| `tk_Bishop` | |
| `tk_BloodyCoin` | |
| `tk_BloodyRazor` | |
| `tk_ButterBean` | |
| `tk_ButterBean_Mega` | |
| `tk_ButterBean_Normal` | |
| `tk_CambionConception` | |
| `tk_CarvingKnife` | |
| `tk_CatONineTails` | |
| `tk_Checkers` | |
| `tk_CounterfeitCoin` | |
| `tk_DruidsWhistle` | |
| `tk_DybbuksRib` | |
| `tk_EggSack` | |
| `tk_ElectricCoin` | |
| `tk_EmptyHand` | |
| `tk_EstusFlask` | |
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
| `tk_JarOfRadiation` | |
| `tk_Knight` | |
| `tk_LegWhistle` | |
| `tk_LilBattery` | |
| `tk_LunchBox` | |
| `tk_MadGhost_Spawn` | |
| `tk_Metronome` | |
| `tk_MonkStyleChange` | |
| `tk_MyShadow` | |
| `tk_Pawn` | |
| `tk_Pentagram` | |
| `tk_PetrifiedPinky` | |
| `tk_PurpleDrink` | |
| `tk_Queen` | |
| `tk_RageJuice` | |
| `tk_RazorBlade` | |
| `tk_RedDrink` | |
| `tk_Reset` | |
| `tk_RoboSucc` | |
| `tk_Rook` | |
| `tk_SackOfMeat` | |
| `tk_SoulJar` | |
| `tk_SpawnTheLost` | |
| `tk_SpellBook` | |
| `tk_Steroids` | |
| `tk_SuckStone` | |
| `tk_TankJuice` | |
| `tk_TarotDeck` | |
| `tk_Technology` | |
| `tk_Teleport` | |
| `tk_TheBlackBox` | |
| `tk_WaterBottle_Empty` | |
| `tk_WaterBottle_Full` | |
| `tk_WaterBottle_Half` | |
| `tk_WeirdEgg_Spawn` | |
| `tk_Whistle` | |
| `TKNG_GutBall` | |
| `TKNG_Laser` | |
| `ToadJump_BasicMove` | |
| `Toast` | |
| `Toast2` | |
| `TormentorMelee` | |
| `TormentorThrow` | |
| `TormentorThrow_sp` | |
| `TormentorThrow_spAI` | |
| `Toss` | |
| `Toss2` | |
| `ToTheRescue` | |
| `ToTheRescue2` | |
| `ToxExplode` | |
| `ToxPuff` | |
| `tr_SelfDestruct` | |
| `Track` | |
| `Track2` | |
| `TradeLife` | |
| `TradeLife2` | |
| `TradeLife_Afterlife` | |
| `TradeLife_Afterlife2` | |
| `TrailBlazer` | |
| `TrailBlazer2` | |
| `TrainArms` | |
| `TrainArms2` | |
| `TrainBody` | |
| `TrainBody2` | |
| `TrainLegs` | |
| `TrainLegs2` | |
| `TrainMind` | |
| `TrainMind2` | |
| `TrampleMove` | |
| `TrampleMoveOne` | |
| `Transcend` | |
| `Transcend2` | |
| `Traps` | |
| `TreeForm` | |
| `TreeForm2` | |
| `TrembloSmash` | |
| `TrembloSmash_AI` | |
| `TrexEat` | |
| `TriAttack` | |
| `TriAttack2` | |
| `TriceratopsGore` | |
| `trinket` | |
| `Trip` | |
| `Trip2` | |
| `TripleNails` | |
| `TripleNails2` | |
| `Tromp` | |
| `Tromp2` | |
| `Trudge` | |
| `Trudge2` | |
| `Tryptophan` | |
| `Tryptophan2` | |
| `TT_Thrash` | |
| `Tumble` | |
| `Tumble2` | |
| `TumorDash` | |
| `TumorPrisonDeathrattle` | |
| `TurnFoe` | |
| `TurnFoe2` | |
| `TurretShot` | |
| `TurtleUp` | |
| `TutorialStick` | |
| `TwinShot` | |
| `TwinShot2` | |
| `TwisterMove` | |
| `Two` | |
| `UFO_BigExplode` | |
| `UFO_CrossLasers` | |
| `UFO_Dash` | |
| `UFO_SpelunkyDeath` | |
| `UnbridledHits` | |
| `UnbridledHits2` | |
| `Unearth` | |
| `Unearth2` | |
| `Unflip` | |
| `UnimpededLunge` | |
| `UnimpededLunge2` | |
| `UnreliableMissile` | |
| `UnreliableMissile2` | |
| `UnreliableShield` | |
| `UnreliableShield2` | |
| `Upgrade` | |
| `Upgrade2` | |
| `Uppercut` | |
| `Uppercut2` | |
| `Vaccuum` | |
| `Vaccuum2` | |
| `VenomBarrage` | |
| `VenomBarrage2` | |
| `VetVisit` | |
| `VetVisit2` | |
| `ViolentOutburst` | |
| `Vivisect` | |
| `Vivisect2` | |
| `VoltTackle` | |
| `VoltTackle2` | |
| `Vurp` | |
| `Vurp2` | |
| `WallBlow` | |
| `WallEyeShot` | |
| `WallMove` | |
| `WallOfFire` | |
| `WallOfFire2` | |
| `WarCry` | |
| `WarCry2` | |
| `WarmupStretch` | |
| `WarmupStretch2` | |
| `Warp` | |
| `Warp2` | |
| `WasteTime` | |
| `WasteTime2` | |
| `WaterBottle_Empty` | |
| `WaterBottle_Full` | |
| `WaterBottle_Half` | |
| `WaterSphere` | |
| `WaterSphere2` | |
| `WeakeningNail` | |
| `WeakeningNail2` | |
| `Weakness` | |
| `Weakness2` | |
| `weapon` | |
| `WeAreOne` | |
| `WeAreOne2` | |
| `WeAreTheChampions` | |
| `WeAreTheChampions2` | |
| `WebShot` | |
| `WebTrap` | |
| `WebTrap2` | |
| `WereManFurySwipes` | |
| `WetHairball` | |
| `WetHairball2` | |
| `WeWillRockYou` | |
| `WeWillRockYou2` | |
| `Whisper` | |
| `Whisper2` | |
| `WhispererThrowDamage` | |
| `WideSwipe` | |
| `WindSlash` | |
| `WindSlash2` | |
| `WindUp` | |
| `WindUp2` | |
| `WindyStep` | |
| `WindyStep2` | |
| `Wish` | |
| `Wish2` | |
| `WitchHunt` | |
| `WitchHunt2` | |
| `Withdraw` | |
| `Withdraw2` | |
| `WolfDash` | |
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
| `wp_BearTraps` | |
| `wp_BentSpoon` | |
| `wp_Bible` | |
| `wp_BiggestStick` | |
| `wp_BigSpring` | |
| `wp_BigStick` | |
| `wp_Blackjack` | |
| `wp_Blackjack_Auto` | |
| `wp_BlackMushroom` | |
| `wp_BlackShard` | |
| `wp_BlackShard_Glowing` | |
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
| `wp_BucketOfLard` | |
| `wp_BungaClub` | |
| `wp_BurningCoal` | |
| `wp_ButchersCleaver` | |
| `wp_ButterflyKnife` | |
| `wp_CarBattery` | |
| `wp_CatPaw` | |
| `wp_CaveCatClub` | |
| `wp_Chainsaw` | |
| `wp_Cheese` | |
| `wp_ChumBucket` | |
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
| `wp_GnarledClaw` | |
| `wp_GoldPickaxe` | |
| `wp_GrapplingHook` | |
| `wp_Grenade` | |
| `wp_GripTrainer` | |
| `wp_GunslingerPistol` | |
| `wp_HairSpray` | |
| `wp_HarpyClaw` | |
| `wp_HeavyMace` | |
| `wp_HolyGrail` | |
| `wp_HolyWater` | |
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
| `wp_MeatHookB` | |
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
| `wp_MoneyBag` | |
| `wp_MoneyBag_Huge` | |
| `wp_MoneyBag_Large` | |
| `wp_MoneyBag_Medium` | |
| `wp_MoneyBag_Small` | |
| `wp_MonkFist` | |
| `wp_MysteriousBone` | |
| `wp_NailBoard` | |
| `wp_NailGun` | |
| `wp_Necronomicon` | |
| `wp_NecroSoulDagger` | |
| `wp_NecroSoulDaggerCharged` | |
| `wp_NuclearKnife` | |
| `wp_NuclearKnifeExplode` | |
| `wp_NuclearKnifeFixed` | |
| `wp_ObsidianChunk` | |
| `wp_Ocarina` | |
| `wp_OddRemote` | |
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
| `wp_RailSpikes` | |
| `wp_RainbowRemote` | |
| `wp_RainStaff` | |
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
| `wp_SleepDart` | |
| `wp_SlingShot` | |
| `wp_SmallBomb` | |
| `wp_Sniper` | |
| `wp_SoulClaw` | |
| `wp_SpawnCultist` | |
| `wp_SpawnStacy` | |
| `wp_SpearOfDestiny` | |
| `wp_SpiderWebber` | |
| `wp_Spitball` | |
| `wp_SpringBoard` | |
| `wp_StaffOfFlame` | |
| `wp_SteelBall` | |
| `wp_StevensBagOfRocks` | |
| `wp_StevensBottles` | |
| `wp_StevenWeapon1` | |
| `wp_StevenWeapon2` | |
| `wp_Stick` | |
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
| `wp_TheLonerAuto` | |
| `wp_TheLonerFixed` | |
| `wp_ThePact` | |
| `wp_ThrobbingGristle` | |
| `wp_TinaScream` | |
| `wp_TractorBeam` | |
| `wp_TrashCanLid` | |
| `wp_Trowel` | |
| `wp_TuskThrow` | |
| `wp_UnderworldStaff` | |
| `wp_UraniumRod` | |
| `wp_USAShield` | |
| `wp_Uzi` | |
| `wp_Whetstone` | |
| `wp_ZodiacsSixshooter` | |
| `wp_ZodiacsSixshooter_Auto` | |
| `WrathOfGod` | |
| `WrathOfGod2` | |
| `Wrestlemaniac` | |
| `YA_Laser` | |
| `YeticatSnowball` | |
| `YeticatSnowball_Counter` | |
| `YetiSlam` | |
| `YouSeeNothing` | |
| `YouSeeNothing2` | |
| `Zap` | |
| `Zap2` | |
| `ZaratanaBasic` | |
| `ZaratanaSoloBasic` | |
| `Zealot` | |
| `Zealot2` | |
| `ZodiacShoot` | |
| `ZodiacShootX` | |
| `ZombieTombstone` | |
| `Zoomzerk` | |
| `Zoomzerk2` | |

</details>


---

### Enum: `passive_pool`


<details>
<summary><b>Expand</b></summary>

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AfterImage` | |
| `Agile` | |
| `AlmsForThePoor` | |
| `AlphaStrike` | |
| `Amped` | |
| `Amplify` | |
| `AngelicInspiration` | |
| `AnimalControl` | |
| `AnimalHandler` | |
| `Animalistic` | |
| `ArmorSpecialist` | |
| `ArmoredPlating` | |
| `Avenger` | |
| `Backstabber` | |
| `Barbed` | |
| `BareMinimum` | |
| `BarkSkin` | |
| `Beckon` | |
| `BedBugs` | |
| `Blacksmith` | |
| `Blessed` | |
| `BlessingOfHolyFire` | |
| `BlessingOfSpirit` | |
| `Blink` | |
| `BloodLust` | |
| `Boned` | |
| `BoobyTrap` | |
| `Bouncer` | |
| `BountyHunter` | |
| `Bouquet` | |
| `BowlingBall` | |
| `BreathOfLife` | |
| `BrickSkin` | |
| `BroodMother` | |
| `BuddySystem` | |
| `Burgle` | |
| `BurningPaws` | |
| `ButchersSoul` | |
| `CambionConception` | |
| `Careful` | |
| `Caretaker` | |
| `CatAPult` | |
| `CatchProjectiles` | |
| `ChainKnockback` | |
| `ChainsOfGuilt` | |
| `ChargeUp` | |
| `Charming` | |
| `ClericsSoul` | |
| `CobraStyle` | |
| `Conductor` | |
| `Confrontational` | |
| `CorpseConnoisseur` | |
| `CounterBarrage` | |
| `Cripple` | |
| `Critical` | |
| `DancingLights` | |
| `DarkPriest` | |
| `Daunt` | |
| `Dealer` | |
| `DeathBoon` | |
| `DeathIncarnate` | |
| `DeathProof` | |
| `DeathsDoor` | |
| `DemoMan` | |
| `DirtyClaws` | |
| `DoubleThrow` | |
| `Drag` | |
| `DruidsSoul` | |
| `DualWield` | |
| `DuctTape` | |
| `DukeOfFlies` | |
| `DumbMuscle` | |
| `EMP` | |
| `ETank` | |
| `EldritchVisage` | |
| `ElementalAttunement` | |
| `EmptyVessels` | |
| `EnchantedRelic` | |
| `Encore` | |
| `Energizer` | |
| `EnergyFists` | |
| `EnergyStorm` | |
| `Enlightened` | |
| `EscapeSequence` | |
| `Eternal` | |
| `EternalHealth` | |
| `EvilPatron` | |
| `FastFooted` | |
| `FasterWhenHit` | |
| `Feral` | |
| `FightMe` | |
| `FightersSoul` | |
| `FireArmor` | |
| `FirstImpression` | |
| `Five` | |
| `Fleabag` | |
| `FlipACoin` | |
| `Flourish` | |
| `FlowState` | |
| `FlowerPower` | |
| `Flying` | |
| `FollowUp` | |
| `Four` | |
| `FreshMeat` | |
| `FullPower` | |
| `Furious` | |
| `FuzzyFeet` | |
| `Gassy` | |
| `Glow` | |
| `Glutton` | |
| `GodWarrior` | |
| `Godspeed` | |
| `GoldenClaws` | |
| `GoodVibrations` | |
| `Goofball` | |
| `GrapplingHook` | |
| `GravityFalls` | |
| `GravityWell` | |
| `Gurgitator` | |
| `Hack` | |
| `HamsterStyle` | |
| `HardHead` | |
| `Harden` | |
| `Hardy` | |
| `Harpooner` | |
| `HawkEye` | |
| `Hazardous` | |
| `HealingAura` | |
| `Heathens` | |
| `HeaveHook` | |
| `HeavyHanded` | |
| `HighAsYouCanCount` | |
| `HitMe` | |
| `HolyMantel` | |
| `HomeRun` | |
| `Hooked` | |
| `Host` | |
| `HotBlooded` | |
| `HuntersBoon` | |
| `HuntersSoul` | |
| `IceArmor` | |
| `IcePaws` | |
| `ImmortalLeeches` | |
| `Incubator` | |
| `Indigestion` | |
| `Infected` | |
| `Infested` | |
| `InfiniteRebirth` | |
| `Ingenuity` | |
| `IronSkin` | |
| `ItemProxy` | |
| `ItsAlive` | |
| `JaggedEdges` | |
| `JestersSoul` | |
| `JetFists` | |
| `KillsHeal` | |
| `LastGasp` | |
| `LateBloomer` | |
| `LatentEnergy` | |
| `Leader` | |
| `LearnFromMe` | |
| `Leechmother` | |
| `LightUpTheStage` | |
| `LightningArmor` | |
| `LightningPaws` | |
| `LightningRod` | |
| `LikeAFish` | |
| `LivingBattery` | |
| `LongArms` | |
| `LongCast` | |
| `LongShot` | |
| `LooseMeat` | |
| `LootHoarder` | |
| `Looter` | |
| `LordOfTheFlies` | |
| `LuckDrain` | |
| `LuckSwing` | |
| `Lucky` | |
| `MadVisage` | |
| `Maestro` | |
| `MagesSoul` | |
| `MagicGuru` | |
| `MainCourse` | |
| `Mange` | |
| `Mania` | |
| `Masochist` | |
| `MegaMinions` | |
| `MentalStorm` | |
| `MetalDetector` | |
| `Micronaps` | |
| `MindBreaker` | |
| `MindTempest` | |
| `MiniMe` | |
| `Mixup` | |
| `MonkeyStyle` | |
| `MonksSoul` | |
| `MoraleBoost` | |
| `MostValuableCat` | |
| `MountainForm` | |
| `MrMega` | |
| `MyLeg` | |
| `Nanobots` | |
| `Napalm` | |
| `NaturalHealer` | |
| `NaturalHealing` | |
| `NaturesGuidance` | |
| `NecromancersSoul` | |
| `NeverFull` | |
| `NumbingLeeches` | |
| `OffloadPain` | |
| `Omniscience` | |
| `One` | |
| `OneEighty` | |
| `OneWithNothing` | |
| `OverConfident` | |
| `Overflow` | |
| `Overload` | |
| `Overpowered` | |
| `PainGain` | |
| `Parasitic` | |
| `Pathfinder` | |
| `Patience` | |
| `PawMissile` | |
| `Penetrate` | |
| `PerfectTechnique` | |
| `PetRocks` | |
| `Pinpoint` | |
| `Plow` | |
| `PoisonIvy` | |
| `PoisonTips` | |
| `PowerUp` | |
| `PressurePoints` | |
| `PriorityTarget` | |
| `ProtectTheWeak` | |
| `Protection` | |
| `ProtectiveAura` | |
| `PsionicRepel` | |
| `PsySmack` | |
| `PsychicsSoul` | |
| `Pulp` | |
| `PunchFace` | |
| `Purifier` | |
| `Putrefy` | |
| `Quiver` | |
| `Radiation` | |
| `RangedMedic` | |
| `RapGod` | |
| `RapidFlow` | |
| `RatStyle` | |
| `RazorClaws` | |
| `ReactiveArmor` | |
| `RealityShatter` | |
| `Recharged` | |
| `Recoil` | |
| `ReflexPunch` | |
| `RelentlessDead` | |
| `RepressedMemories` | |
| `Resonance` | |
| `RobotArms` | |
| `RockAspect` | |
| `Rockin` | |
| `RubberArrows` | |
| `RunningJab` | |
| `SacrificialLamb` | |
| `SafeSwitching` | |
| `SantaSangre` | |
| `Scabs` | |
| `Scars` | |
| `Scavenger` | |
| `Schadenfreude` | |
| `Scrapper` | |
| `SelfAssured` | |
| `SerialKiller` | |
| `Shadow` | |
| `ShakeDown` | |
| `Shank` | |
| `SharingIsCaring` | |
| `Shiv` | |
| `ShoulderCheck` | |
| `ShovingMatch` | |
| `Shrapnel` | |
| `Shrapnel_Tinkerer` | |
| `SkillShare` | |
| `SkullSmash` | |
| `SlackOff` | |
| `SleepDarts` | |
| `SlowAndSteady` | |
| `Slugger` | |
| `Smash` | |
| `SneakAttack` | |
| `Sniper` | |
| `SoothingSong` | |
| `SoulBound` | |
| `SoulShatter` | |
| `SpecialFriends` | |
| `SplitShot` | |
| `Spotters` | |
| `SpreadSorrow` | |
| `SpreadThePain` | |
| `Stoic` | |
| `Stompy` | |
| `StrengthInNumbers` | |
| `Study` | |
| `SuicideSquad` | |
| `SuperCrow` | |
| `SuperLuck` | |
| `Superstition` | |
| `Survivalist` | |
| `SweetSpot` | |
| `SwiftKiller` | |
| `TaintedMother` | |
| `TakeAim` | |
| `TalkToAnimals` | |
| `TanksSoul` | |
| `Teamwork` | |
| `Tenderize` | |
| `Testy` | |
| `ThickSkull` | |
| `ThiefsSoul` | |
| `ThornArrows` | |
| `Thorns` | |
| `ThouShaltNotCovet` | |
| `ThouShaltNotKill` | |
| `ThouShaltObey` | |
| `ThrillOfTheHunt` | |
| `ThunderThighs` | |
| `TinkerersSoul` | |
| `ToadStyle` | |
| `TopOff` | |
| `Torpor` | |
| `TowerDefense` | |
| `Traps` | |
| `TrickyTraps` | |
| `TrueSight` | |
| `Turnabout` | |
| `TurtleStyle` | |
| `Twiddle` | |
| `Two` | |
| `UnburdenedMotion` | |
| `UnburdenedStrikes` | |
| `UnburdenedThoughts` | |
| `Undeath` | |
| `Unrestricted` | |
| `Unstoppable` | |
| `Untouched` | |
| `Vampirism` | |
| `VeneratedTouch` | |
| `Vengeful` | |
| `VersatileVocalist` | |
| `VersionTwo` | |
| `VoidSoul` | |
| `WeakSpot` | |
| `WeaponMaster` | |
| `WeaponProficiency` | |
| `WhipCracker` | |
| `WideLoad` | |
| `WideSwing` | |
| `Wiggly` | |
| `WildAnimals` | |
| `WildStyle` | |
| `Wither` | |
| `WormLord` | |
| `Worms` | |
| `Wrestlemaniac` | |
| `ZenkaiBoost` | |
| `Zip` | |

| `AcidReflux` | |
| `ADHD` | |
| `Albinism` | |
| `all_disorders` | |
| `Anemia` | |
| `Anxiety` | |
| `ASRFight` | |
| `ASRFlight` | |
| `Autism` | |
| `Bipolar` | |
| `BirdFlu` | |
| `birth_defects` | |
| `BlackFetin` | |
| `BlessingOfGlorg` | |
| `BloodBlooded` | |
| `BloodFrenzy` | |
| `Boils` | |
| `BorrowedTime` | |
| `BrainDamage` | |
| `BrainDead` | |
| `Brave` | |
| `BrokenLimb` | |
| `Cancer` | |
| `Cannibal` | |
| `Charred` | |
| `Chungus` | |
| `CommonCold` | |
| `Covid` | |
| `Crazy_disorders` | |
| `CrohnsDisease` | |
| `DarkOne` | |
| `DeathChill` | |
| `Deathless` | |
| `Declawed` | |
| `DeepCut` | |
| `DejaVu` | |
| `Depression` | |
| `Diabetes` | |
| `diseases` | |
| `Distemper` | |
| `DownsSyndrome` | |
| `Dwarfism` | |
| `Dysentery` | |
| `Dyskinesia` | |
| `Dyslexia` | |
| `EatingDisorder` | |
| `Ebola` | |
| `Elephantiasis` | |
| `Empath` | |
| `EternalYouth` | |
| `ExplosiveGas` | |
| `EyeCatchin` | |
| `FattyLiver` | |
| `FelineAids` | |
| `Fidgety` | |
| `FlamingFists` | |
| `Flu` | |
| `forbidden_spell_consequences` | |
| `forbidden_spell_consequences_crippling` | |
| `Fossilized` | |
| `FrozenKnee` | |
| `GamblingAddict` | |
| `Gargantuan` | |
| `Gastritis` | |
| `Gigachad` | |
| `Gigantism` | |
| `GlassBones` | |
| `HeadTrauma` | |
| `Hypersomnia` | |
| `Hypomania` | |
| `IBS` | |
| `ImposterSyndrome` | |
| `Incontinence` | |
| `Infestation` | |
| `Insomnia` | |
| `IntestinalProlapse` | |
| `Invincible` | |
| `Kamikazee` | |
| `KidneyStones` | |
| `Leprosy` | |
| `LongStrider` | |
| `low_hygeine_in_house_disorders` | |
| `Lycanthropy` | |
| `magic_disorders` | |
| `mental_disorders` | |
| `Narcolepsy` | |
| `Necrosis` | |
| `Nudist` | |
| `OCD` | |
| `OrangeFetin` | |
| `Pacifist` | |
| `Paralyzed` | |
| `Paranoia` | |
| `Phony` | |
| `physical_disorders` | |
| `Pica` | |
| `PillPopper` | |
| `Pox` | |
| `Premonitions` | |
| `PrimordialDwarf` | |
| `Psychosis` | |
| `PTSD` | |
| `PuncturedEye` | |
| `PurpleFetin` | |
| `Rabies` | |
| `SavantSyndrome` | |
| `ScalyScabs` | |
| `Scatological` | |
| `Schizophrenia` | |
| `SchrodingerDisorder` | |
| `Scleroderma` | |
| `SensoryOverloadFace` | |
| `SensoryOverloadHead` | |
| `SensoryOverloadNeck` | |
| `SensoryOverloadTrinket` | |
| `SensoryOverloadWeapon` | |
| `SeveredThumb` | |
| `Shunned` | |
| `Singleton` | |
| `SkillShare_Disorder` | |
| `SleepParalysis` | |
| `Sociopathy` | |
| `Soulless` | |
| `SpinaBifida` | |
| `SpontaneousCombustion` | |
| `STARTER_PLACEHOLDER_Butcher` | |
| `STARTER_PLACEHOLDER_Colorless` | |
| `STARTER_PLACEHOLDER_Druid` | |
| `STARTER_PLACEHOLDER_Fighter` | |
| `STARTER_PLACEHOLDER_Hunter` | |
| `STARTER_PLACEHOLDER_Jester` | |
| `STARTER_PLACEHOLDER_Mage` | |
| `STARTER_PLACEHOLDER_Medic` | |
| `STARTER_PLACEHOLDER_Monk` | |
| `STARTER_PLACEHOLDER_Necromancer` | |
| `STARTER_PLACEHOLDER_Psychic` | |
| `STARTER_PLACEHOLDER_Tank` | |
| `STARTER_PLACEHOLDER_Thief` | |
| `STARTER_PLACEHOLDER_Tinkerer` | |
| `Steven_disorders` | |
| `Stinky` | |
| `StockholmSyndrome` | |
| `stomach_disorders` | |
| `Tachysensia` | |
| `TamperedGenes` | |
| `TheHunger` | |
| `Touched` | |
| `Tourettes` | |
| `ToxicBlooded` | |
| `Toxoplasmosis` | |
| `Traumatophobia` | |
| `Triskaidekaphobia` | |
| `Vegan` | |
| `ViolentOutbursts` | |
| `WilliamsSyndrome` | |
| `WobblyCat` | |
| `WrenchedNeck` | |

</details>


---

### Enum: `disorder`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** Migrated from `Arrays.md` string arrays

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ADHD` | |
| `Albinism` | |
| `Anemia` | |
| `Anxiety` | |
| `ASRFight` | |
| `ASRFlight` | |
| `Autism` | |
| `Bipolar` | |
| `BloodFrenzy` | |
| `BorrowedTime` | |
| `BrainDamage` | |
| `Brave` | |
| `Cannibal` | |
| `Depression` | |
| `Diabetes` | |
| `DownsSyndrome` | |
| `Dwarfism` | |
| `Dyskinesia` | |
| `Dyslexia` | |
| `EatingDisorder` | |
| `Empath` | |
| `Fidgety` | |
| `GamblingAddict` | |
| `Gigantism` | |
| `GlassBones` | |
| `Hypersomnia` | |
| `Hypomania` | |
| `ImposterSyndrome` | |
| `Insomnia` | |
| `Invincible` | |
| `Lycanthropy` | |
| `Narcolepsy` | |
| `Nudist` | |
| `OCD` | |
| `Pacifist` | |
| `Paranoia` | |
| `Phony` | |
| `Pica` | |
| `Premonitions` | |
| `PrimordialDwarf` | |
| `Psychosis` | |
| `PTSD` | |
| `SavantSyndrome` | |
| `Scatological` | |
| `Schizophrenia` | |
| `Shunned` | |
| `Singleton` | |
| `SkillShare_Disorder` | |
| `SleepParalysis` | |
| `Sociopathy` | |
| `SpinaBifida` | |
| `StockholmSyndrome` | |
| `Tachysensia` | |
| `TheHunger` | |
| `Tourettes` | |
| `Traumatophobia` | |
| `Triskaidekaphobia` | |
| `Vegan` | |
| `ViolentOutbursts` | |
| `WilliamsSyndrome` | |
| `WobblyCat` | |

</details>


---

### Enum: `parasite`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** Migrated from `Arrays.md` string arrays

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AmoebaFace` | |
| `AmoebaHat` | |
| `AmoebaNeck` | |
| `AngryWorm` | |
| `BeanParasite` | |
| `BestBud` | |
| `BotflyLarva` | |
| `BrainMaggot` | |
| `Cooties` | |
| `Cordyceps` | |
| `CrimsonMask_Cursed` | |
| `CymothoaExigua` | |
| `EuhaplorchisCaliforniensis` | |
| `EyeWorm` | |
| `HealWorm` | |
| `Heartworm` | |
| `Hookworm` | |
| `Lice` | |
| `Malaria` | |
| `NaegleriaFowleri` | |
| `Parousworm` | |
| `Pinworm` | |
| `PoundOfFlesh_Cursed` | |
| `RedCap_Cursed` | |
| `Ringworm` | |
| `Roundworm` | |
| `SacculinaCarcini` | |
| `Scabies` | |
| `SoulSucker` | |
| `Tapeworm` | |
| `TheTick` | |

</details>


---

### Enum: `image`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** Migrated from `Arrays.md` string arrays

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `1.png` | |
| `albinotomtom.png` | |
| `alienbeast.png` | |
| `amoeba.png` | |
| `angelcat.png` | |
| `angelkitten.png` | |
| `ankylosaurus.png` | |
| `astro.png` | |
| `astrozombie.png` | |
| `atomickitten.png` | |
| `babydeathworm.png` | |
| `babyshark.png` | |
| `bat.png` | |
| `beaniesrat.png` | |
| `belcher.png` | |
| `bgcandle.png` | |
| `bigasteroid.png` | |
| `bigdemon.png` | |
| `biggravel.png` | |
| `bigslime.png` | |
| `bigufo.png` | |
| `birthwort.png` | |
| `bishop.png` | |
| `bishophat.png` | |
| `blackhole.png` | |
| `blessing.png` | |
| `bloat.png` | |
| `bomb.png` | |
| `bomberrat.png` | |
| `bombfly.png` | |
| `boomer.png` | |
| `boulder.png` | |
| `boydino.png` | |
| `boyshade.png` | |
| `braindrain.png` | |
| `bramblebaby.png` | |
| `bricks.png` | |
| `bumblefoot.png` | |
| `bungaelite.png` | |
| `butchercat.png` | |
| `butchtink.png` | |
| `buttzombie.png` | |
| `cactus.png` | |
| `cager.png` | |
| `cancercat.png` | |
| `cancreeper.png` | |
| `carcus.png` | |
| `carnibulb.png` | |
| `cat.png` | |
| `catcaller.png` | |
| `catcultist.png` | |
| `cathuman.png` | |
| `catnip.png` | |
| `cavebaby.png` | |
| `cavecatdad.png` | |
| `cavecatkitten.png` | |
| `cavecatmom.png` | |
| `cavechief.png` | |
| `caveman.png` | |
| `cavemannospear.png` | |
| `cavewoman.png` | |
| `cerberubs.png` | |
| `chaosboss.png` | |
| `chargeymaggot.png` | |
| `cherubim.png` | |
| `chubs.png` | |
| `chumbag.png` | |
| `chummy.png` | |
| `cloakeddemon.png` | |
| `cloningvat.png` | |
| `clot.png` | |
| `cloud.png` | |
| `coin.png` | |
| `collectivecat.png` | |
| `copbot.png` | |
| `corefreak.png` | |
| `corpse.png` | |
| `covencandle.png` | |
| `crate.png` | |
| `cratercreeper.png` | |
| `cultist.png` | |
| `daddyshark.png` | |
| `deathworm.png` | |
| `demonhooker.png` | |
| `dinoeggs.png` | |
| `dip.png` | |
| `doctorbot.png` | |
| `doublehusk.png` | |
| `drcat.png` | |
| `drditto.png` | |
| `drmangler.png` | |
| `druidcat.png` | |
| `druidcrow.png` | |
| `dumpster.png` | |
| `dustdevil.png` | |
| `dybbuk.png` | |
| `east_arrow.png` | |
| `enemycat.png` | |
| `fatcat.png` | |
| `fatman.png` | |
| `fatso.png` | |
| `fatwoman.png` | |
| `fetus.png` | |
| `fetusgusher.png` | |
| `fetusjar.png` | |
| `fetusnojar.png` | |
| `fightercat.png` | |
| `finalboss.png` | |
| `flea.png` | |
| `fleshlad.png` | |
| `fleshymind.png` | |
| `floast.png` | |
| `floater.png` | |
| `floatinghive.png` | |
| `flushmaster.png` | |
| `fly.png` | |
| `flyswarm.png` | |
| `food.png` | |
| `frankkorbee.png` | |
| `frankpinky.png` | |
| `futurebot.png` | |
| `fuzzer.png` | |
| `gambit.png` | |
| `gamete.png` | |
| `gascan.png` | |
| `gasper.png` | |
| `gasser.png` | |
| `gassy.png` | |
| `gatekeeper.png` | |
| `geolad.png` | |
| `ghosttombstone.png` | |
| `girldino.png` | |
| `girlshade.png` | |
| `glassspitter.png` | |
| `golemcat.png` | |
| `gorger.png` | |
| `gravel.png` | |
| `graveworm.png` | |
| `greenprober.png` | |
| `greyalien.png` | |
| `ground.png` | |
| `ground_shards.png` | |
| `ground_spots.png` | |
| `groundedspear.png` | |
| `guncat.png` | |
| `gunslinger.png` | |
| `hangerbot.png` | |
| `harpoontrap.png` | |
| `headtumor.png` | |
| `hellhand.png` | |
| `hemlock.png` | |
| `hitler.png` | |
| `hitlerfetus.png` | |
| `hitleriii.png` | |
| `hive.png` | |
| `hornycat.png` | |
| `host.png` | |
| `humancat.png` | |
| `huntercat.png` | |
| `husk.png` | |
| `hydrant.png` | |
| `icecube.png` | |
| `iceelemental.png` | |
| `infested.png` | |
| `infestedduo.png` | |
| `invader.png` | |
| `jackcat.png` | |
| `jarhead.png` | |
| `jekyll.png` | |
| `jestercat.png` | |
| `johnny.png` | |
| `junk.png` | |
| `killdozer.png` | |
| `kirbyfetus.png` | |
| `kitten.png` | |
| `labpillar.png` | |
| `leaper.png` | |
| `lenny.png` | |
| `lightning.png` | |
| `lordbunga.png` | |
| `lovebot.png` | |
| `lumpy.png` | |
| `madlad.png` | |
| `maelestes.png` | |
| `magecat.png` | |
| `maggot.png` | |
| `maggotlord.png` | |
| `mammoth.png` | |
| `mammothbaby.png` | |
| `manaidol.png` | |
| `manglersmonster.png` | |
| `mangy.png` | |
| `mangy2.png` | |
| `mangy3.png` | |
| `meatminion.png` | |
| `meatslime.png` | |
| `mediccat.png` | |
| `medslime.png` | |
| `megadinohead.png` | |
| `megadinoleg.png` | |
| `megafetus.png` | |
| `megagup.png` | |
| `megamutant.png` | |
| `megatumor.png` | |
| `mininuke.png` | |
| `minivolcano.png` | |
| `monkcat.png` | |
| `moonhand.png` | |
| `moonhead.png` | |
| `moonworm.png` | |
| `mothertumorbig.png` | |
| `mothertumorsmall.png` | |
| `multicat.png` | |
| `mutant.png` | |
| `necrocat.png` | |
| `needlecat.png` | |
| `nettle.png` | |
| `neutronstar.png` | |
| `nohead.png` | |
| `north_arrow.png` | |
| `nubs.png` | |
| `nubscat.png` | |
| `organzodiac.png` | |
| `ornstein.png` | |
| `parasaurolophus.png` | |
| `parasiter.png` | |
| `phonebooth.png` | |
| `pile.png` | |
| `pinky.png` | |
| `pokerdemon.png` | |
| `pole.png` | |
| `poop.png` | |
| `pooter.png` | |
| `popeye.png` | |
| `prehistoricpooter.png` | |
| `psychiccat.png` | |
| `pterodactyl.png` | |
| `pyrophina.png` | |
| `queenhippo.png` | |
| `raptor.png` | |
| `raptorbaby.png` | |
| `rat.png` | |
| `ratcat.png` | |
| `ratking.png` | |
| `ratpile.png` | |
| `rattlesnake.png` | |
| `reaper.png` | |
| `robotom.png` | |
| `rock.png` | |
| `rockhead.png` | |
| `rocky.png` | |
| `rover.png` | |
| `rubble.png` | |
| `sabertoothcat.png` | |
| `sabertoothcub.png` | |
| `scary.png` | |
| `scorpioncat.png` | |
| `scrap.png` | |
| `securitybot.png` | |
| `seraphim.png` | |
| `shadecat.png` | |
| `shadow.png` | |
| `shambler.png` | |
| `sharky.png` | |
| `siren.png` | |
| `skeletoncat.png` | |
| `skeletonshambler.png` | |
| `skinned.png` | |
| `skullooze.png` | |
| `slag.png` | |
| `slotmachine.png` | |
| `smallasteroid.png` | |
| `smallrock.png` | |
| `smallslime.png` | |
| `smallufo.png` | |
| `smcandle.png` | |
| `smough.png` | |
| `snakeybones.png` | |
| `soldierbot.png` | |
| `south_arrow.png` | |
| `spewer.png` | |
| `spewerpill.png` | |
| `spewerpilltube.png` | |
| `spidercat.png` | |
| `spiderqueen.png` | |
| `spiderweb.png` | |
| `spiky.png` | |
| `spikyrock.png` | |
| `spookie.png` | |
| `stacy2p0.png` | |
| `stacy3.png` | |
| `stacymutant.png` | |
| `staticcactus.png` | |
| `staticcactus_2x2.png` | |
| `staticcactus_tall.png` | |
| `stego.png` | |
| `stemcat.png` | |
| `stevenslime.png` | |
| `suseuspeashy.png` | |
| `swappymaggot.png` | |
| `tallbot.png` | |
| `tallrobes.png` | |
| `tallskeletoncat.png` | |
| `tallspidercat.png` | |
| `talltumor.png` | |
| `tankcat.png` | |
| `tarbaby.png` | |
| `tatters.png` | |
| `tentickles.png` | |
| `terminator1.png` | |
| `terminator2.png` | |
| `thechild.png` | |
| `thecoven.png` | |
| `themother.png` | |
| `thiefcat.png` | |
| `throb.png` | |
| `throbbingking.png` | |
| `throbbingturret.png` | |
| `thump.png` | |
| `tinkerercat.png` | |
| `tinyspider.png` | |
| `tire.png` | |
| `tnt.png` | |
| `toadie.png` | |
| `toadie_hidden.png` | |
| `tomtom.png` | |
| `tracyfetus.png` | |
| `trampy.png` | |
| `trash.png` | |
| `tremblo.png` | |
| `trex.png` | |
| `triceratops.png` | |
| `tumorbarrier.png` | |
| `tumorcat.png` | |
| `tvbot.png` | |
| `urn.png` | |
| `waggle.png` | |
| `waterkitten.png` | |
| `waterleech.png` | |
| `wereman.png` | |
| `west_arrow.png` | |
| `whisperer.png` | |
| `wisp.png` | |
| `woc_wall.png` | |
| `wolfcat.png` | |
| `worm.png` | |
| `yellowblaster.png` | |
| `yeti.png` | |
| `yeticat.png` | |
| `zaratana.png` | |
| `zealot.png` | |
| `zombiecat.png` | |
| `zombietombstone.png` | |

</details>


---

### Enum: `event_file`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** Migrated from `Arrays.md` string arrays

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `alley_events.gon` | |
| `boneyard_events.gon` | |
| `bunker_events.gon` | |
| `caves_events.gon` | |
| `common` | |
| `core_events.gon` | |
| `crater_events.gon` | |
| `dead_body.gon` | |
| `desert_events.gon` | |
| `future_events.gon` | |
| `iceage_events.gon` | |
| `junkyard_events.gon` | |
| `jurassic_events.gon` | |
| `lab_events.gon` | |
| `legacy_events.gon` | |
| `misc_events.gon` | |
| `monster.gon` | |
| `moon_events.gon` | |
| `npc_events.gon` | |
| `sewer_events.gon` | |
| `special_events.gon` | |
| `theend_events.gon` | |
| `treasure_box.gon` | |

</details>


---

### Enum: `combo_effect`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** Migrated from `Arrays.md` string arrays

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `BloodBounce` | |
| `BloodBounce_Absorb` | |
| `BloodBounceCrit` | |
| `BloodBounceCrit_Absorb` | |
| `BloodPoof` | |
| `BloodPoof_Absorb` | |
| `BloodPoofCrit` | |
| `BloodPoofCrit_Absorb` | |
| `BloodPopCrit` | |
| `BloodPopCrit_Absorb` | |
| `coolLaserBeamInner` | |
| `coolLaserBeamOuter` | |
| `fartoom_burst` | |
| `fartoom_trail` | |
| `FevaporateDark` | |
| `FevaporateLight` | |
| `FireBase` | |
| `FireBaseLarge` | |
| `FireBaseSmall` | |
| `FireExtinguish_Steam` | |
| `Firenado_Embers` | |
| `Firenado_Fire` | |
| `FirePlumes` | |
| `FirePlumesLarge` | |
| `FirePlumesSmall` | |
| `FireSmoke` | |
| `FireSmokeLarge` | |
| `FireSmokeSmall` | |
| `Firestorm_Distortion` | |
| `Firestorm_Embers` | |
| `Firestorm_Fire` | |
| `FireWaves` | |
| `FireWavesLarge` | |
| `FireWavesSmall` | |
| `FireWhites` | |
| `FireWhitesLarge` | |
| `FireWhitesSmall` | |
| `firework_bursta` | |
| `firework_burstb` | |
| `GravityBurstB` | |
| `GravityBurstS` | |
| `HeatWave_Distortion` | |
| `HeatWave_Particles` | |
| `MegaBlastA` | |
| `MegaBlastB` | |
| `RainB` | |
| `RainF` | |
| `RainM` | |
| `SnowB` | |
| `SnowF` | |
| `SnowM` | |
| `SplatterXL` | |
| `TormentorGuts` | |
| `TRainB` | |
| `TRainF` | |
| `TRainM` | |
| `WindDebris` | |
| `WindDust` | |
| `WindLeaves` | |
| `WindLeavesB` | |
| `WindLeavesF` | |
| `WindWisps` | |

</details>


---

### Enum: `sound`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** Migrated from `Arrays.md` string arrays

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `SE_BirdDying_Blackbird` | |
| `SE_BirdDying_Dove` | |
| `SE_BirdDying_Hummingbird` | |
| `SE_BirdSmall_DyingCall` | |

</details>


---

### Enum: `global_tags`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** Migrated from `Arrays.md` string arrays

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `all_cats_are_jester` | |
| `all_normal_events_are_weather` | |
| `always_ambushed` | |
| `disorder_levelup_quest` | |
| `fail_all_events` | |
| `increase_difficulty` | |
| `increase_event_difficulty` | |
| `item_levelup_quest` | |
| `pyrophina_following` | |
| `superchaos_levelups` | |
| `trigger_extra_event` | |
| `upgrade_basic_combats_to_hard` | |
| `zaratana_following` | |

</details>


---

### Enum: `global_particles`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** Migrated from `Arrays.md` string arrays

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `AngelClouds` | |
| `CaveDrip` | |
| `CoreHeatWave_Distortion` | |
| `CraterLeaves` | |
| `Embers` | |
| `GlitchShards` | |
| `MeatCaveDrip` | |
| `Mist` | |

| `AbsorbBuff` | |
| `AcidRain` | |
| `AcidSplash` | |
| `alienLaserCharge` | |
| `Blood` | |
| `Blood_Absorb` | |
| `BloodBounce` | |
| `BloodBounce_Absorb` | |
| `BloodBounceCrit` | |
| `BloodBounceCrit_Absorb` | |
| `BloodCrit` | |
| `BloodCrit_Absorb` | |
| `BloodPoof` | |
| `BloodPoof_Absorb` | |
| `BloodPoofCrit` | |
| `BloodPoofCrit_Absorb` | |
| `BloodPopCrit` | |
| `BloodPopCrit_Absorb` | |
| `BloodRain` | |
| `CaveSplash` | |
| `ChaosTPIn` | |
| `ChaosTPOut` | |
| `ChaosTPTracer` | |
| `Confetti` | |
| `coolLaserBeam` | |
| `coolLaserBeamInner` | |
| `coolLaserBeamOuter` | |
| `CreepBubbles` | |
| `DarkFog` | |
| `druidFlowers` | |
| `DruidFlowersVictory` | |
| `dustCloud` | |
| `EQRocks` | |
| `fartoom` | |
| `fartoom_burst` | |
| `fartoom_trail` | |
| `Feathers` | |
| `FevaporateDark` | |
| `FevaporateLight` | |
| `FightBallCloud` | |
| `FinalEvaporate` | |
| `FireBallTrail` | |
| `FireBase` | |
| `FireBaseLarge` | |
| `FireBaseSmall` | |
| `FireExtinguish` | |
| `FireExtinguish_Steam` | |
| `FireFull` | |
| `FireFullLarge` | |
| `FireFullSmall` | |
| `Firenado` | |
| `Firenado_Embers` | |
| `Firenado_Fire` | |
| `FirePlumes` | |
| `FirePlumesLarge` | |
| `FirePlumesSmall` | |
| `FireSmoke` | |
| `FireSmokeLarge` | |
| `FireSmokeSmall` | |
| `FireStorm` | |
| `Firestorm_Distortion` | |
| `Firestorm_Embers` | |
| `Firestorm_Fire` | |
| `FireTileSmall` | |
| `FireWaves` | |
| `FireWavesLarge` | |
| `FireWavesSmall` | |
| `FireWhites` | |
| `FireWhitesLarge` | |
| `FireWhitesSmall` | |
| `firework` | |
| `firework_burst` | |
| `firework_burst_recursive` | |
| `firework_bursta` | |
| `firework_burstb` | |
| `FloatingRocks` | |
| `FlyBuff` | |
| `Fog` | |
| `Gibs_animal` | |
| `Gibs_bag` | |
| `Gibs_blob` | |
| `Gibs_box` | |
| `Gibs_bug` | |
| `Gibs_cactus` | |
| `Gibs_cat` | |
| `Gibs_default` | |
| `Gibs_demon` | |
| `Gibs_fetus` | |
| `Gibs_huge` | |
| `Gibs_humanoid` | |
| `Gibs_Medium` | |
| `Gibs_plant` | |
| `Gibs_poop` | |
| `Gibs_rat` | |
| `Gibs_robot` | |
| `Gibs_rock` | |
| `Gibs_skeleton` | |
| `Gibs_terminatorskin` | |
| `GibsBloodSpurt` | |
| `GibsBloodSpurtHuge` | |
| `GlitchTile` | |
| `GravityBurst` | |
| `GravityBurstB` | |
| `GravityBurstS` | |
| `GravityHoverRings` | |
| `GroundPoof` | |
| `GuillotinaGuts` | |
| `HadoukenBall` | |
| `HairballTrail` | |
| `healing_gas` | |
| `HeatWave` | |
| `HeatWave_Distortion` | |
| `HeatWave_Particles` | |
| `Kingblood1` | |
| `Kingblood2` | |
| `Lava_Distortion` | |
| `MagicMissileTrail` | |
| `MagicMissileTrailSmall` | |
| `ManaDrain` | |
| `MeatCaveSplash` | |
| `MegaBlast` | |
| `MegaBlastA` | |
| `MegaBlastB` | |
| `Meteornado` | |
| `MiniSplatter` | |
| `MiniSplatter2` | |
| `MiniSplatter3` | |
| `musicalSwirl` | |
| `PassiveBleed` | |
| `PassiveEnergized` | |
| `PassiveFire` | |
| `PassivePoison` | |
| `PassiveScrambled` | |
| `PassiveStealth` | |
| `PassiveTar` | |
| `PassiveWet` | |
| `PointPoof` | |
| `PointSmoke` | |
| `Rain` | |
| `RainB` | |
| `RainF` | |
| `RainM` | |
| `RocketTrail` | |
| `SandStorm` | |
| `SandStormBuff` | |
| `ShineBuff` | |
| `SmallDirt` | |
| `SmokeBuff` | |
| `Snow` | |
| `SnowB` | |
| `SnowF` | |
| `SnowM` | |
| `SparkleBuff` | |
| `SpikeBuff` | |
| `splash` | |
| `splashB` | |
| `splashF` | |
| `splashM` | |
| `splashM2` | |
| `SplatterLarge` | |
| `SplatterMed` | |
| `SplatterSmall` | |
| `SplatterXL` | |
| `test` | |
| `test2` | |
| `test3` | |
| `test4` | |
| `test5` | |
| `test6` | |
| `test7` | |
| `test8` | |
| `test9` | |
| `test_tornado` | |
| `Thunderstorm` | |
| `TinkererVictoryFirework` | |
| `TormentorFull` | |
| `TormentorGuts` | |
| `ToxicBubbles` | |
| `TrackingTest` | |
| `TRainB` | |
| `TRainF` | |
| `TRainM` | |
| `TsplashM` | |
| `VolcanoSpurt` | |
| `VolcanoSpurt_Trail` | |
| `WindDebris` | |
| `WindDust` | |
| `WindFull` | |
| `WindLeaves` | |
| `WindLeavesB` | |
| `WindLeavesF` | |
| `WindWisps` | |

</details>


---

### Enum: `class_seals`


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** Migrated from `Arrays.md` string arrays

**Confirmed Values:**

| Value | Definition |
| :--- | :--- |
| `ButcherSeal` | |
| `ClericSeal` | |
| `ColorlessSeal` | |
| `DruidSeal` | |
| `FighterSeal` | |
| `HunterSeal` | |
| `JesterSeal` | |
| `MageSeal` | |
| `MonkSeal` | |
| `NecromancerSeal` | |
| `PsychicSeal` | |
| `TankSeal` | |
| `ThiefSeal` | |
| `TinkererSeal` | |

</details>