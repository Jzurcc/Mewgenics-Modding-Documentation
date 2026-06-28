# Mewgenics Mod Developer Documentation: Exhaustive Enemies Reference

This file contains a complete scrape of all enemies defined in the game engine's `.gon` files, including their exact base stats, properties, abilities, and official descriptions. Enemies appear under every area they spawn in.

> [!NOTE]
> **Stat Defaults:** Unless otherwise specified, all core stats (`Str`, `Dex`, `Con`, `Int`, `Spd`, `Cha`) default to **5**. Only stats that deviate from 5 are shown in the Core Stats row to reduce clutter.

## Alley

### Cat Caller (`CatCaller`)
> Slows units. Counterattacks when hit.

**Core Stats:** HP: `7`, Move: `?`, Str: `4`

**Properties:** `tag: cat`, `type: cat`, `auto_run_priority: support`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** CatCall

**Passives:**
- `CounterAttack attack`

---

### Flea (`Flea`)
> Its melee attack damages itself.

**Core Stats:** HP: `2`, Move: `4`, Str: `4`

**Properties:** `tag: bug`, `corpse_health: 0`, `faction: enemies`, `type: small`, `deathpoof_size: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `SuicideMelee`

---

### Fly (`Fly`)
> Melee attacker. Flying.

**Core Stats:** HP: `1`, Move: `4`, Str: `2`, Spd: `2`

**Properties:** `tag: bug`, `faction: enemies`, `corpse_health: 0`, `base_mana_regen: 999`, `flying: true`, `type: small`, `deathpoof_size: 1`, `can_be_backstabbed: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### Kitten (`Kitten`)
> Runs away when damaged.

**Core Stats:** HP: `5`, Move: `?`, Str: `3`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### Leaper (`Leaper`)
> Its leap attack damages and knocks back all adjacent units.

**Core Stats:** HP: `9`, Move: `2`

**Properties:** `tag: [rat blob]`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `RatLeap`

---

### Lil' Rat (`Rat`)
> Dashes in a straight line.

**Core Stats:** HP: `5`, Move: `1`, Str: `4`

**Properties:** `tag: rat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `Dash_Enemy`

**Passives:**
- `CanMutateTo [Lumpy, Leaper]`

---

### Lumpy (`Lumpy`)
> Its ranged attack creates Creep. Spawns Creep when damaged.

**Core Stats:** HP: `9`, Move: `3`, Str: `3`, Dex: `4`

**Properties:** `tag: [rat blob]`, `faction: enemies`, `initiative: 5`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `CreepRanged`

**Passives:**
- `SpawnCreepOnHit 1`
- `ElementImmune Creep`

---

### Maggot (`Maggot`)
> Melee attacker.

**Core Stats:** HP: `1`, Move: `2`, Str: `2`, Dex: `1`

**Properties:** `tag: worm`, `corpse_health: 0`, `faction: enemies`, `type: small`, `initiative: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `CanMutateTo [TumorousMaggot, ChargeyMaggot, SwappyMaggot]`

---

### Mangy (`Mangy`)
> Its ranged attack may inflict Poison. Spawns maggots when damaged.

**Core Stats:** HP: `7`, Move: `?`, Str: `4`, Spd: `3`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `PoisonShot`

---

### Pinky (`Pinky`)
> Melee attacker. Moves randomly.

**Core Stats:** HP: `1`, Move: `2`, Str: `2`

**Properties:** `tag: rat`, `faction: enemies`, `type: small`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### Pooter (`Pooter`)
> Ranged attacker. Flying.

**Core Stats:** HP: `6`, Move: `2`

**Properties:** `tag: bug`, `faction: enemies`, `flying: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicShortLobbed`

---

### Tom Tom (`TomTom`)
> It's slow, but has a wide melee attack.

**Core Stats:** HP: `15`, Move: `?`, Str: `6`, Spd: `1`

**Properties:** `tag: cat`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `WideSwipe`

---

### Water Kitten (`WaterKitten`)
> Moves away when damaged. May be hiding in water...

**Core Stats:** HP: `5`, Move: `?`, Str: `3`

**Properties:** `tag: cat`, `type: cat`, `shield: 1`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** WaterTrailMove

**Passives:**
- `WaterWalk 1`

---

## Boneyard

### Butt Zombie (`ButtZombie`)
> Will attack all adjacent units with its melee attack when its backside is underground. Goes upside down when damaged. Undead.

**Core Stats:** HP: `15`, Move: `5`

**Properties:** `tag: zombie`, `faction: enemies`, `corpse_health: 0`, `act_points: 4`

**Abilities:** **move:** `Teleport` | **attack:** `BasicMelee` | **spells:** ButtFlip, Spin_Enemy, TeleportFlipUp, ButtFart

**Passives:**
- `Undead 1`

---

### Flea (`Flea`)
> Its melee attack damages itself.

**Core Stats:** HP: `2`, Move: `4`, Str: `4`

**Properties:** `tag: bug`, `corpse_health: 0`, `faction: enemies`, `type: small`, `deathpoof_size: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `SuicideMelee`

---

### Fly (`Fly`)
> Melee attacker. Flying.

**Core Stats:** HP: `1`, Move: `4`, Str: `2`, Spd: `2`

**Properties:** `tag: bug`, `faction: enemies`, `corpse_health: 0`, `base_mana_regen: 999`, `flying: true`, `type: small`, `deathpoof_size: 1`, `can_be_backstabbed: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### Grave Worm (`GraveWorm`)
> Ranged attacker. Digs away when damaged.

**Core Stats:** HP: `10`, Move: `4`

**Properties:** `tag: worm`, `faction: enemies`, `corpse_health: 0`

**Abilities:** **move:** `Teleport` | **attack:** `BasicRanged`

**Passives:**
- `MoveWhenDamaged move`

---

### Maggot (`Maggot`)
> Melee attacker.

**Core Stats:** HP: `1`, Move: `2`, Str: `2`, Dex: `1`

**Properties:** `tag: worm`, `corpse_health: 0`, `faction: enemies`, `type: small`, `initiative: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `CanMutateTo [TumorousMaggot, ChargeyMaggot, SwappyMaggot]`

---

### Reaper (`Reaper`)
> Performs a spin attack at the start of its turn. Teleports to units that kill its allies. Undead.

**Core Stats:** HP: `18`, Move: `2`

**Properties:** `tag: [ghost skeleton]`, `faction: enemies`, `corpse_health: 0`, `flying: true`

**Abilities:** **move:** `FloatMove` | **attack:** `ReaperSpin` | **spells:** ReaperRevenge

**Passives:**
- `MoveTowardsKillers ReaperRevenge`
- `Undead 1`

---

### Robes (`TallRobes`)
> Its ranged attack inflicts Leech. Can summon Wisps. Becomes a Tatters when killed. Undead.

**Core Stats:** HP: `4`, Move: `3`

**Properties:** `tag: [ghost skeleton]`, `faction: enemies`, `shield: 6`, `flying: true`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `HexShot` | **spells:** SpawnWisp

**Passives:**
- `Undead 1`
- `TransformOnDeath Tatters`

---

### Scary (`Scary`)
> Its melee attacks can inflict Fear or Doom! Undead.

**Core Stats:** HP: `14`, Move: `4`

**Properties:** `tag: ghost`, `faction: enemies`, `flying: true`, `corpse_health: 0`

**Abilities:** **move:** `Teleport` | **attack:** `ScaryFear` | **spells:** ScaryHaunt

**Passives:**
- `Undead 1`

---

### Shambler (`Shambler`)
> Will throw units it can reach. Lunges in a random direction at the end of its turn. Undead.

**Core Stats:** HP: `28`, Move: `3`, Spd: `3`

**Properties:** `tag: zombie`, `faction: enemies`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `ShamblerDash` | **spells:** ShamblerToss

**Passives:**
- `Trample 3`
- `Undead 1`

---

### Skeleton Cat (`SkeletonCat`)
> Comes back from the dead if its body isn't destroyed! Undead.

**Core Stats:** HP: `0`, Move: `3`, Str: `9`

**Properties:** `tag: [cat skeleton]`, `type: cat`, `shield: 1`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `NoHealthOnlyShield 1`
- `Undead 1`
- `StatusImmunity [Poison, Bleed]`

---

### Skeleton Cat (`SkeletonCatCorpse`)
> Will come back from the dead next turn! Undead.

**Core Stats:** HP: `0`, Move: `?`

**Properties:** `tag: [cat skeleton]`, `type: cat`, `shield: 12`, `faction: enemies`, `initiative: 10`, `corpse_health: 0`, `exclude_from_hallucinate: true`

**Abilities:** **move:** `None` | **attack:** `None`

**Passives:**
- `NoHealthOnlyShield 1`
- `Undead 1`
- `StatusImmunity [Poison, Bleed]`
- `CountAsCorpse 1`

---

### Spiderling (`TinySpider`)
> Burrows inside its victims, inflicting Infested.

**Core Stats:** HP: `2`, Move: `4`, Str: `3`

**Properties:** `tag: bug`, `corpse_health: 0`, `faction: enemies`, `type: small`, `deathpoof_size: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `SpiderSuicideMelee`

**Passives:**
- `StatusImmunity Webbed`

---

### Spookie (`Spookie`)
> Its melee attack drains mana. Undead.

**Core Stats:** HP: `9`, Move: `4`

**Properties:** `tag: ghost`, `faction: enemies`, `flying: true`, `corpse_health: 0`

**Abilities:** **move:** `Teleport` | **attack:** `SpookieLick` | **spells:** DefaultMove

**Passives:**
- `Undead 1`

---

### Tall Skeleton Cat (`TallSkeletonCat`)
> Its ranged attack can also give [img:shield] to its allies. Will come back from the dead if its body isn't destroyed! Undead.

**Core Stats:** HP: `0`, Move: `3`

**Properties:** `tag: [cat skeleton]`, `type: cat`, `shield: 15`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`, `corpse_health: 0`, `act_points: 2`

**Abilities:** **move:** `DefaultMove` | **attack:** `BadBone` | **spells:** BadBone_copy, GoodBone, GoodBone_copy

**Passives:**
- `YOffset .35`
- `Undead 1`
- `PrioritizeHitDifferentTargets 1`
- `NoHealthOnlyShield 1`
- `StatusImmunity [Poison, Bleed]`

---

### Tall Skeleton Cat (`TallSkeletonCatCorpse`)
> Will come back from the dead next turn! Undead.

**Core Stats:** HP: `0`, Move: `?`

**Properties:** `tag: [cat skeleton]`, `type: cat`, `shield: 1`, `faction: enemies`, `initiative: 10`, `corpse_health: 0`, `exclude_from_hallucinate: true`

**Abilities:** **move:** `None` | **attack:** `None`

**Passives:**
- `NoHealthOnlyShield 1`
- `Undead 1`
- `StatusImmunity [Poison, Bleed]`
- `CountAsCorpse 1`

---

### Tatters (`Tatters`)
> Its attack inflicts Leech to all units in an area. Will inflict Hex on units that damage it. Undead.

**Core Stats:** HP: `20`, Move: `5`

**Properties:** `tag: [ghost skeleton]`, `faction: enemies`, `initial_health: 1`, `shield: 8`, `flying: true`

**Abilities:** **move:** `Teleport` | **attack:** `TattersLeeches` | **spells:** TattersFear

**Passives:**
- `CounterAttack TattersFear`
- `Undead 1`

---

### Werecat (`WolfCat`)
> Can use both its dash attack and its leap attack in the same turn.

**Core Stats:** HP: `16`, Move: `2`, Spd: `6`

**Properties:** `tag: [cat dog]`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`, `act_points: 2`, `move_points: 2`

**Abilities:** **move:** `DefaultMove` | **attack:** `WolfDash` | **spells:** WolfLeap

**Passives:**
- `PrioritizeHitDifferentTargets 1`

---

### Wisp (`Wisp`)
> Its melee attack inflicts Burn. Dodges one attack per turn.

**Core Stats:** HP: `1`, Move: `4`, Str: `4`, Spd: `2`

**Properties:** `tag: ghost`, `faction: enemies`, `corpse_health: 0`, `base_mana_regen: 999`, `flying: true`, `type: small`, `deathpoof_size: 1`, `can_be_backstabbed: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `WispDodge 1`

---

### Zombie Cat (`ZombieCat`)
> Eats corpses and becomes stronger! Taking damage weakens it and spawns poison food. Undead.

**Core Stats:** HP: `20`, Move: `2`, Str: `7`, Con: `9`, Int: `1`, Spd: `3`

**Properties:** `tag: [cat zombie]`, `type: cat`, `dispersed_bonus_turns: 1`, `base_mana_regen: 999`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** ZombieFeast

**Passives:**
- `Undead 1`

---

## Bonus Birds

### Black Bird (`BlackBird`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### Chicken (`Chicken`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### Pigeon (`Pigeon`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

## Bunker

### Atomic Kitten (`AtomicKitten`)
> Emits a burst of radiation at the start of its turn. Teleports away when damaged. Explodes when killed.

**Core Stats:** HP: `1`, Move: `?`, Str: `3`

**Properties:** `tag: cat`, `type: cat`, `divine_shield: 2`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `Teleport` | **attack:** `AtomicBurst`

**Passives:**
- `DeathRattle BoomerCatExplode`

---

### Bishop Hat (`BishopHat`)
> Attracts Cultists. Can be picked up by a Cultist to promote them into a Bishop.

**Core Stats:** HP: `1`, Move: `?`

**Properties:** `tag: bishop_hat`, `faction: enemies`, `takes_turns: false`, `can_be_champion: false`, `shield: 5`, `kill_required: false`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `None`

---

### Blorb (`Hive`)
> Its ranged attack inflicts Slow in an area.

**Core Stats:** HP: `8`, Move: `2`, Str: `1`, Dex: `1`

**Properties:** `tag: tumor`, `faction: enemies`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `BigGunkShot`

---

### Cat Cultist (`CatCultist`)
> Melee attacker. Increases the amount of times it can attack each turn whenever it takes damage.

**Core Stats:** HP: `11`, Move: `?`, Str: `2`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`, `act_points: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** CultistCut

---

### Florb (`FloatingHive`)
> Its ranged attack inflicts Slow. Flying.

**Core Stats:** HP: `10`, Move: `3`

**Properties:** `tag: tumor`, `faction: enemies`, `flying: true`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `GunkShot`

---

### Killdozer (`KillDozer`)
> Moves towards what damages it. Trample.

**Core Stats:** HP: `8`, Move: `2`

**Properties:** `tag: [humanoid robot]`, `faction: enemies`, `mana_regen: 999`, `mana: 100`, `shield: 14`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `KillDoze` | **spells:** MoveOne

**Passives:**
- `Trample 3`
- `MoveTowardsDamageSource MoveOne`
- `Robot 1`
- `Brace 2`
- `Thorns 3`

---

### Love Bot (`LoveBot`)
> Heals and gives +1 [img:spd] to its allies. Its heal can grant an extra turn if healed over max.

**Core Stats:** HP: `0`, Move: `?`

**Properties:** `tag: robot`, `faction: enemies`, `auto_run_priority: support`, `shield: 13`, `can_be_overkilled: false`, `banned_elite_buffs: [Mad]`

**Abilities:** **move:** `DefaultMove` | **attack:** `LoveBotHeal` | **spells:** LoveBotCounter

**Passives:**
- `Brace 1`
- `NoHealthOnlyShield 1`
- `Robot 1`
- `CounterAttack LoveBotCounter`

---

### Robo-Cat (`RoboTom`)
> Its wide melee attacks have Knockback 10.

**Core Stats:** HP: `1`, Move: `?`, Str: `6`, Spd: `1`

**Properties:** `tag: [cat robot]`, `type: cat`, `shield: 11`, `dispersed_bonus_turns: 1`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`

**Abilities:** **move:** `DefaultMove` | **attack:** `WideSwipe`

**Passives:**
- `Brace 3`
- `AddMeleeKnockback 10`
- `Robot 1`

---

### Security Bot (`SecurityBot`)
> When its allies are damaged, it will move towards the attacker and attempt to attack it. Gains +1 movement range at the end of its turn.

**Core Stats:** HP: `0`, Move: `1`

**Properties:** `tag: robot`, `faction: enemies`, `auto_run_priority: support`, `shield: 12`, `can_be_overkilled: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `SBotAttack` | **spells:** SBotAngryMove, SBotRecharge, SBotAnger

**Passives:**
- `Brace 2`
- `NoHealthOnlyShield 1`
- `Robot 1`

---

### Spiderling (`TinySpider`)
> Burrows inside its victims, inflicting Infested.

**Core Stats:** HP: `2`, Move: `4`, Str: `3`

**Properties:** `tag: bug`, `corpse_health: 0`, `faction: enemies`, `type: small`, `deathpoof_size: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `SpiderSuicideMelee`

**Passives:**
- `StatusImmunity Webbed`

---

## Caves

### Albino Tom Tom (`AlbinoTomTom`)
> Its wide melee attacks have Knockback 2.

**Core Stats:** HP: `17`, Move: `?`, Spd: `1`

**Properties:** `tag: cat`, `type: cat`, `round_end_bonus_turns: 1`, `base_mana_regen: 999`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `WideSwipe`

**Passives:**
- `AddMeleeKnockback 2`

---

### Bat (`Bat`)
> Its melee flurry inflicts Confusion. 50% Dodge Chance. Flying.

**Core Stats:** HP: `5`, Move: `6`, Str: `1`, Spd: `8`

**Properties:** `tag: fetus`, `faction: enemies`, `flying: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BatFlurry`

**Passives:**
- `DodgeChance 50%`

---

### Brain Drain (`BrainDrain`)
> Infinite ranged magic attacker. Will counter a spell once per turn. If it starts its turn with its counterspell still available, it absorbs it for a buff.

**Core Stats:** HP: `8`, Move: `1`, Str: `3`, Dex: `3`, Con: `3`, Int: `3`, Spd: `3`, Cha: `3`

**Properties:** `tag: fetus`, `faction: enemies`, `flying: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BrainDrainMagicMissile` | **spells:** Counterspell

---

### Fetus (`Fetus`)
> Ranged attacker. Can drink water to heal.

**Core Stats:** HP: `12`, Move: `2`, Dex: `4`

**Properties:** `tag: fetus`, `faction: enemies`, `initial_health: 8`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicShortLobbed_Water` | **spells:** DefaultMove, DrinkUp

**Passives:**
- `WaterWalk 1`

---

### Korbee (`KirbyFetus`)
> Will suck units in, then spit them out as far away as it can.

**Core Stats:** HP: `12`, Move: `4`, Spd: `2`

**Properties:** `tag: fetus`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `KirbySuck`

---

### Mega Fetus (`MegaFetus`)
> Performs a spin attack. Will try to counterattack with its left arm when hit.

**Core Stats:** HP: `25`, Move: `3`, Spd: `3`

**Properties:** `tag: fetus`, `faction: enemies`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `MegafetusSpin` | **spells:** MegafetusMelee

**Passives:**
- `Trample 3`
- `CounterAttack MegafetusMelee`

---

### Skull Ooze (`SkullOoze`)
> Its ranged attack destroys equipment.

**Core Stats:** HP: `12`, Move: `2`, Spd: `2`

**Properties:** `tag: blob`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `AcidShot`

---

### Spider Cat (`TallSpiderCat`)
> Its melee attack has Lifesteal. Will move away after it attacks. Immune to tile effects.

**Core Stats:** HP: `28`, Move: `6`, Str: `7`

**Properties:** `tag: [cat bug]`, `type: cat`, `initial_health: 14`, `base_mana_regen: 999`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `TallSpiderMelee`

**Passives:**
- `YOffset .35`
- `IgnoreTiles 1`
- `StatusImmunity Webbed`

---

### Spider Kitten (`SpiderCat`)
> Will Web units, then drain their HP. Immune to Webs.

**Core Stats:** HP: `20`, Move: `3`

**Properties:** `tag: [cat bug]`, `type: cat`, `initial_health: 10`, `dispersed_bonus_turns: 1`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 16`

**Abilities:** **move:** `DefaultMove` | **attack:** `WebShot` | **spells:** SmallSpiderMelee

**Passives:**
- `StatusImmunity Webbed`

---

### Spiderling (`TinySpider`)
> Burrows inside its victims, inflicting Infested.

**Core Stats:** HP: `2`, Move: `4`, Str: `3`

**Properties:** `tag: bug`, `corpse_health: 0`, `faction: enemies`, `type: small`, `deathpoof_size: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `SpiderSuicideMelee`

**Passives:**
- `StatusImmunity Webbed`

---

### Ten Tickles (`TenTickles`)
> Can attack any tile adjacent to water. Teleports through water tiles.

**Core Stats:** HP: `14`, Move: `20`

**Properties:** `tag: fetus`, `faction: enemies`, `base_mana_regen: 999`, `corpse_health: 0`

**Abilities:** **move:** `TenTicklesSwim` | **attack:** `TenTicklesAttack`

**Passives:**
- `TileTrail_Ahead WaterTile`

---

### Toadie (`Toadie`)
> Disguises itself as inanimate objects. While disguised, ambushes enemies that walk past it, causing Fear.

**Core Stats:** HP: `14`, Move: `4`

**Properties:** `tag: cat`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** Disguise, MoveTwoCantrip, FearMelee

**Passives:**
- `DisguisedTrapper FearMelee`

---

## Desert

### Baby Deathworm (`BabyDeathWorm`)
> Dash attacks units that end their movement in line with it. Can't dash backwards!

**Core Stats:** HP: `8`, Move: `4`

**Properties:** `tag: worm`, `faction: enemies`, `corpse_health: 0`

**Abilities:** **move:** `Teleport` | **attack:** `Dash_BabyDeathWorm`

---

### Bone Worm (`SnakeyBones`)
> Ranged attacker. Gains more range the taller it becomes. Loses height when it takes damage. Can only take 1 damage at a time when tall. Undead.

**Core Stats:** HP: `0`, Move: `?`

**Properties:** `tag: [worm skeleton]`, `auto_run_priority: stationary`, `shield: 8`, `faction: enemies`, `corpse_health: 0`, `can_be_overkilled: false`

**Abilities:** **move:** `None` | **spells:** attack, BoneWormShotSmall, FormShrinkTwoSnakey, FormShrinkOneSnakey, FormGrowTwoSnakey, FormGrowThreeSnakey, FormGrowTwo, FormGrowThree

**Passives:**
- `NoHealthOnlyShield 1`
- `Undead 1`
- `StatusImmunity [Poison, Bleed]`
- `PrioritizeHitDifferentTargets 1`

---

### Bounty Hunter (`GunCat`)
> Can shoot anywhere within its line of sight. Prefers long shots.

**Core Stats:** HP: `9`, Move: `2`, Str: `4`, Spd: `2`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `GuncatShoot`

**Passives:**
- `WeaponsDontLoseDurability 1`
- `PrioritizeFarAwayTargets 10`

---

### Bounty Hunter (`EventBountyHunter`)
> *(No Description)*

**Core Stats:** HP: `17`, Move: `2`, Str: `4`, Spd: `2`

**Properties:** `tag: cat`, `type: cat`, `faction: birds`, `base_mana_regen: 999`, `kill_required: false`, `can_collect_coins: true`, `held_coins: [5 10]`, `aggro_target_is_enemy: true`, `can_run: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `GuncatShoot`

**Passives:**
- `WeaponsDontLoseDurability 1`
- `EventBounterHunterPassive 1`

---

### Burfer Maggot (`TumorousMaggot`)
> Its attack surrounds units with Thorny lumps.

**Core Stats:** HP: `14`, Move: `3`

**Properties:** `tag: worm`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `PrisonShot`

---

### Carcass (`Carcus`)
> Spawns random types of Maggots.

**Core Stats:** HP: `1`, Move: `0`, Spd: `0`

**Properties:** `tag: animal`, `faction: enemies`, `corpse_health: 0`, `can_be_backstabbed: false`

**Abilities:** **move:** `None` | **attack:** `CarcusSpawn`

---

### Chargey Maggot (`ChargeyMaggot`)
> Its dash attack has trample.

**Core Stats:** HP: `9`, Move: `2`

**Properties:** `tag: worm`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `SmallTrampleDash`

---

### Death Worm (`DeathWorm`)
> Digs underground after its dash attack. Will eat any unit that ends movement on top of it while it's underground.

**Core Stats:** HP: `15`, Move: `1`

**Properties:** `tag: worm`, `faction: enemies`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `DeathWormTrampleDash` | **spells:** DeathWormEat, DeathWormReturn, DeathWormTrampleDash_Reaction

**Passives:**
- `Trample 3`
- `CounterAttack DeathWormTrampleDash_Reaction`

---

### Fly Swarm (`FlySwarm`)
> Performs a melee attack that hits once for each fly. Each time it's damaged it loses a fly.

**Core Stats:** HP: `5`, Move: `3`, Str: `1`, Spd: `2`

**Properties:** `tag: bug`, `faction: enemies`, `corpse_health: 0`, `base_mana_regen: 999`, `flying: true`, `deathpoof_size: 1`, `can_be_backstabbed: false`, `weak_threshold: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** FormShrinkFour, FormShrinkThree, FormShrinkTwo, FormShrinkOne

**Passives:**
- `LimitDamage 1`
- `LimitHeal 1`

---

### Horny Cat (`HornyCat`)
> Its ranged attack inflicts Blind.

**Core Stats:** HP: `7`, Move: `?`, Str: `4`, Dex: `3`, Spd: `3`

**Properties:** `tag: [cat animal]`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `HornyToadShot`

---

### Mummified Mangy (`Mangy2`)
> Its ranged attack may inflict Poison. Spawns Maggots when damaged. Becomes a Carcass when killed.

**Core Stats:** HP: `7`, Move: `?`, Str: `4`, Spd: `3`

**Properties:** `tag: [cat zombie]`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `PoisonShot`

**Passives:**
- `Undead 1`
- `TransformOnDeath Carcus`

---

### Peashy (`Peashy`)
> May attack its own allies. Blocks damage from the front. Becomes enraged when it kills something.

**Core Stats:** HP: `14`, Move: `3`, Dex: `4`

**Properties:** `tag: plant`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicStraightShot` | **spells:** GenericRage, PeashyStab

**Passives:**
- `Thorns 1`
- `FaceShield 0`

---

### Rattlesnek (`RattleSnake`)
> Ambushes enemies who walk past it. Its attacks inflict Poison.

**Core Stats:** HP: `3`, Move: `4`, Str: `4`, Dex: `2`, Con: `2`, Int: `2`, Cha: `2`

**Properties:** `tag: animal`, `type: small`, `faction: enemies`, `weak_threshold: 0`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `RattleSnakeAttack` | **spells:** RattleSnakeTrap

---

### Scorpion Cat (`ScorpionCat`)
> Its melee attacks can Poison or Immobilize.

**Core Stats:** HP: `5`, Move: `2`, Str: `3`, Dex: `3`

**Properties:** `tag: [cat bug]`, `type: cat`, `shield: 5`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `ScorpionSting` | **spells:** ScorpionHold

**Passives:**
- `Brace 1`

---

### Skeleton Shambler (`SkeletonShambler`)
> Will throw units it can reach. Lunges in a random direction at the end of its turn. Comes back from the dead if its body isn't destroyed! Undead.

**Core Stats:** HP: `0`, Move: `3`, Spd: `3`

**Properties:** `tag: skeleton`, `shield: 12`, `faction: enemies`, `size: 2x2`, `move_block: everything_even_when_dead`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `ShamblerDash` | **spells:** ShamblerToss

**Passives:**
- `Trample 3`
- `NoHealthOnlyShield 1`
- `Undead 1`
- `StatusImmunity [Poison, Bleed]`

---

### Skeleton Shambler (`SkeletonShamblerCorpse`)
> Comes back from the dead if its body isn't destroyed! Undead.

**Core Stats:** HP: `0`, Move: `?`, Spd: `3`

**Properties:** `tag: skeleton`, `shield: 3`, `faction: enemies`, `corpse_health: 0`, `can_be_overkilled: false`, `size: 2x2`, `move_block: everything_even_when_dead`, `exclude_from_hallucinate: true`

**Abilities:** **move:** `None` | **attack:** `None`

**Passives:**
- `NoHealthOnlyShield 1`
- `Undead 1`
- `StatusImmunity [Poison, Bleed]`
- `CountAsCorpse 1`

---

### Thump (`Thump`)
> Performs a jump attack. Can only be damaged from behind.

**Core Stats:** HP: `12`, Move: `3`

**Properties:** `tag: rock`, `faction: enemies`, `corpse_health: 0`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `ThumpSlam_Mov` | **attack:** `ThumpSlam`

**Passives:**
- `Trample 3`
- `DamageFromBehindOnly 1`

---

## Events

### Bounty Hunter (`GunCat`)
> Can shoot anywhere within its line of sight. Prefers long shots.

**Core Stats:** HP: `9`, Move: `2`, Str: `4`, Spd: `2`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `GuncatShoot`

**Passives:**
- `WeaponsDontLoseDurability 1`
- `PrioritizeFarAwayTargets 10`

---

### Bounty Hunter (`EventBountyHunter`)
> *(No Description)*

**Core Stats:** HP: `17`, Move: `2`, Str: `4`, Spd: `2`

**Properties:** `tag: cat`, `type: cat`, `faction: birds`, `base_mana_regen: 999`, `kill_required: false`, `can_collect_coins: true`, `held_coins: [5 10]`, `aggro_target_is_enemy: true`, `can_run: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `GuncatShoot`

**Passives:**
- `WeaponsDontLoseDurability 1`
- `EventBounterHunterPassive 1`

---

### Death! (`Death`)
> He's here to take what he's owed.

**Core Stats:** HP: `60`, Move: `4`

**Properties:** `tag: [ghost skeleton]`, `faction: enemies`, `corpse_health: 0`, `flying: true`, `dispersed_bonus_turns: 3`

**Abilities:** **move:** `FloatMove` | **attack:** `ReaperSpin` | **spells:** ReaperRevenge

**Passives:**
- `MoveTowardsKillers ReaperRevenge`
- `Undead 1`

---

## Ice Age

### Caveman Chief (`CaveChief`)
> Its melee attack inflicts Stun. Goes for killing blows against enemies with 10 or fewer HP. Buffs its humanoid allies. Hates Cats!

**Core Stats:** HP: `30`, Move: `2`

**Properties:** `tag: humanoid`, `faction: cavemen`, `dispersed_bonus_turns: 1`, `shield: 15`

**Abilities:** **move:** `DefaultMove` | **attack:** `CaveChiefSlam` | **spells:** CaveChiefBat, CaveChiefRally, CaveChiefFear

---

### Fuzzer (`Fuzzer`)
> Melee attacker that inflicts Confusion, then runs away. Units that contact this gain Confusion. Heals whenever an enemy damages itself with Confusion.

**Core Stats:** HP: `10`, Move: `?`

**Properties:** `tag: blob`, `faction: enemies`, `corpse_health: 0`

**Abilities:** **move:** `FuzzerJump` | **attack:** `BasicMelee` | **spells:** FuzzerJump_post, FuzzerReact

**Passives:**
- `ZeroKnockbackDamage 1`
- `SmallRockBehavior 0`

---

### Mammoth Kitten (`MammothBaby`)
> Its melee attack knocks units into the air. Bruises and knocks back adjacent units at the start of its turn. Trample.

**Core Stats:** HP: `25`, Move: `?`, Str: `6`

**Properties:** `tag: [cat animal]`, `type: cat`, `base_mana_regen: 999`, `faction: mammoths`, `corpse_health: 3`

**Abilities:** **move:** `DefaultMove` | **attack:** `MammothBabyThrow` | **spells:** MammothBabyStomp

**Passives:**
- `SpawnOnDeath BiggestFood`
- `Trample 3`

---

### Sabertooth Cat (`SabertoothCat`)
> Pounces on units. Does a double-hit melee attack that inflicts bleed at the start of its turn if any enemies are adjacent. Hates Cavemen!

**Core Stats:** HP: `17`, Move: `?`

**Properties:** `tag: cat`, `type: cat`, `base_mana_regen: 999`, `faction: sabertooths`

**Abilities:** **move:** `DefaultMove` | **attack:** `SabertoothCatPounce` | **spells:** SabertoothCatTransformSwipe, SabertoothCatDoubleSwipe

---

### Sabertooth Kitten (`SabertoothCub`)
> Has a multi hit melee attack that inflicts Bleed. Can heal its allies. Hates Cavemen!

**Core Stats:** HP: `10`, Move: `?`

**Properties:** `tag: cat`, `type: cat`, `dispersed_bonus_turns: 1`, `base_mana_regen: 999`, `faction: sabertooths`

**Abilities:** **move:** `DefaultMove` | **attack:** `SabertoothCubDoubleSwipe` | **spells:** SabertoothCatTransformSwipe, SabertoothCubLick

---

### WereMan (`WereMan`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `faction: sabertooths`

---

### Wooly Mammoth (`Mammoth`)
> Has a melee attack that knocks units into the air, and a dash attack. Will Bruise and Knockback adjacent units at the start of its turn. Trample.

**Core Stats:** HP: `60`, Move: `2`

**Properties:** `tag: animal`, `faction: mammoths`, `dispersed_bonus_turns: 1`, `corpse_health: 5`, `size: 2x2`, `move_block: everything_even_when_dead`, `elements: [`

**Abilities:** **move:** `DefaultMove` | **attack:** `MammothThrow` | **spells:** MammothTrampleDash, MammothStomp

**Passives:**
- `Trample 3`
- `Divide4OnDeath BiggestFood`

---

### Yeti (`Yeti`)
> Has a triple-hit melee attack and a close-range Freeze attack.

**Core Stats:** HP: `40`, Move: `?`, Spd: `3`

**Properties:** `tag: humanoid`, `faction: enemies`, `dispersed_bonus_turns: 1`, `act_points: 3`

**Abilities:** **move:** `DefaultMove` | **attack:** `YetiSlam` | **spells:** YetiBite, YetiKick, YetiIceBreath

---

### Yeti Cat (`Yeticat`)
> Its ranged ice attack inflicts Slow and has a chance to inflict Freeze. Counter attacks melee attackers.

**Core Stats:** HP: `15`, Move: `2`, Str: `6`

**Properties:** `tag: [cat humanoid]`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `YeticatSnowball`

**Passives:**
- `CounterAttack YeticatSnowball_Counter`

---

## Junkyard

### Chum Bag (`ChumBag`)
> Its long range attack spawns Maggots if it hits an empty tile. Becomes a Chummy when killed. Stationary.

**Core Stats:** HP: `1`, Move: `4`, Spd: `3`

**Properties:** `tag: [blob trash]`, `hidden_tag: container`, `auto_run_priority: stationary`, `faction: enemies`, `corpse_health: 0`

**Abilities:** **move:** `None` | **attack:** `ChumShot_Damage` | **spells:** ChumShot_Maggot

**Passives:**
- `TransformOnDeath Chummy`

---

### Chummy (`Chummy`)
> Dashes in a straight line.

**Core Stats:** HP: `10`, Move: `3`, Str: `6`

**Properties:** `tag: blob`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `ChumDash`

---

### Fly (`Fly`)
> Melee attacker. Flying.

**Core Stats:** HP: `1`, Move: `4`, Str: `2`, Spd: `2`

**Properties:** `tag: bug`, `faction: enemies`, `corpse_health: 0`, `base_mana_regen: 999`, `flying: true`, `type: small`, `deathpoof_size: 1`, `can_be_backstabbed: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### Glass Spitter (`GlassSpitter`)
> Its ranged attack spawns glass and inflicts Bleed.

**Core Stats:** HP: `5`, Move: `?`

**Properties:** `tag: cat`, `type: cat`, `shield: 5`, `base_mana_regen: 999`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `SpitGlass`

---

### Host (`Host`)
> Shoots 3 projectiles in a spread. Reflects projectiles and knocks back units who contact it. Stationary.

**Core Stats:** HP: `13`, Move: `2`, Str: `3`, Dex: `3`

**Properties:** `tag: [blob undead]`, `auto_run_priority: stationary`, `faction: enemies`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `None` | **attack:** `HostSpit` | **spells:** HostShove

---

### Hyde (`Hyde`)
> Its melee attack can hit multiple times!

**Core Stats:** HP: `20`, Move: `?`, Str: `6`

**Properties:** `tag: cat`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `FurySwipes_Enemy`

---

### Jekyll (`Jekyll`)
> It will evolve in several turns.

**Core Stats:** HP: `7`, Move: `?`, Str: `2`

**Properties:** `tag: cat`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 12`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `CanMutateTo Hyde`
- `MutateAfterXTurns 3`

---

### Kitten (`Kitten`)
> Runs away when damaged.

**Core Stats:** HP: `5`, Move: `?`, Str: `3`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### Lumpy (`Lumpy`)
> Its ranged attack creates Creep. Spawns Creep when damaged.

**Core Stats:** HP: `9`, Move: `3`, Str: `3`, Dex: `4`

**Properties:** `tag: [rat blob]`, `faction: enemies`, `initiative: 5`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `CreepRanged`

**Passives:**
- `SpawnCreepOnHit 1`
- `ElementImmune Creep`

---

### Maggot (`Maggot`)
> Melee attacker.

**Core Stats:** HP: `1`, Move: `2`, Str: `2`, Dex: `1`

**Properties:** `tag: worm`, `corpse_health: 0`, `faction: enemies`, `type: small`, `initiative: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `CanMutateTo [TumorousMaggot, ChargeyMaggot, SwappyMaggot]`

---

### Popeye (`PopeyeCat`)
> Has a dash attack with knockback.

**Core Stats:** HP: `17`, Move: `?`, Str: `8`, Spd: `2`

**Properties:** `tag: cat`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `PopeyeDash`

---

### Siren (`Siren`)
> Calls its enemies towards it and heals its adjacent allies.

**Core Stats:** HP: `7`, Move: `?`

**Properties:** `tag: [cat siren]`, `type: cat`, `auto_run_priority: support`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 5`

**Abilities:** **move:** `DefaultMove` | **attack:** `SirenCall`

---

### Spiked Cat (`SpikedCat`)
> Be careful of its Thorns!

**Core Stats:** HP: `5`, Move: `?`

**Properties:** `type: cat`, `shield: 8`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `Thorns 3`

---

## Jurassic

### Ankylosaurus (`Ankylosaurus`)
> *(No Description)*

**Core Stats:** HP: `16`, Move: `?`, Str: `6`, Spd: `1`

**Properties:** `tag: [cat dinosaur]`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `AnkyloSwipe` | **spells:** AnkyloSpin

**Passives:**
- `Brace 2`
- `Thorns 2`
- `AbilityReaction AnkyloSpin`

---

### Dino Nest (`DinoEggs`)
> Spawns baby Raptors.

**Core Stats:** HP: `6`, Move: `0`, Spd: `0`

**Properties:** `tag: animal`, `faction: enemies`, `corpse_health: 0`, `can_be_backstabbed: false`

**Abilities:** **move:** `None` | **attack:** `DinoEggsSpawn`

---

### Maelestes (`Maelestes`)
> Steals equipment from cats. Collects pickups.

**Core Stats:** HP: `6`, Move: `?`, Str: `3`, Int: `10`

**Properties:** `tag: [cat rat]`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`, `can_collect_coins: true`, `can_eat_food: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** MaelestesPickup, MaelestesSteal

---

### Parasaurolophus (`Parasaurolophus`)
> Its attacks always crit against Wet units. Tries to toss units into water.

**Core Stats:** HP: `18`, Move: `1`, Str: `6`

**Properties:** `tag: [cat dinosaur]`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `Parasaurolophus_Push` | **spells:** Parasaurolophus_Throw

**Passives:**
- `YOffset .35`
- `WaterWalk 1`
- `FreePathfindElement Water`

---

### Prehistoric Pooter (`PrehistoricPooter`)
> Its ranged attack inflicts Stun. Flying.

**Core Stats:** HP: `13`, Move: `2`

**Properties:** `tag: bug`, `faction: enemies`, `flying: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `PrehistoricPooterShot`

---

### Pterodactyl (`Pterodactyl`)
> Will pick up cats and peck them. Flying.

**Core Stats:** HP: `30`, Move: `?`

**Properties:** `tag: dinosaur`, `faction: enemies`, `flying: true`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** PteroGrab, PteroEscape

---

### Raptor (`Raptor`)
> Its melee attack hits a random amount of times. Pack hunter.

**Core Stats:** HP: `12`, Move: `?`

**Properties:** `tag: [cat dinosaur]`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `FurySwipes_Enemy`

**Passives:**
- `YOffset .35`
- `PackHunting 1`

---

### Raptor Kitten (`RaptorBaby`)
> *(No Description)*

**Core Stats:** HP: `6`, Move: `3`, Str: `2`, Spd: `8`

**Properties:** `tag: [cat dinosaur]`, `type: cat`, `faction: enemies`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `RaptorBabyBite` | **spells:** DoubleDistanceMove

---

### Stegosaurus (`Stegosaurus`)
> Does a spin attack at the start of its turn. Will seek grass to consume. Will counterattack units that attack it from behind. Trample.

**Core Stats:** HP: `45`, Move: `2`

**Properties:** `tag: dinosaur`, `faction: enemies`, `dispersed_bonus_turns: 1`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `StegoTailSwipe` | **spells:** StegoEatGrass, StegoSpin, StegoGrassStomp

**Passives:**
- `Trample 3`

---

### T-Rex (`Trex`)
> Will seek out the last unit that damaged it and attempt to eat it. Will stomp and inflict Immobile on adjacent units at the end of its turn. Trample.

**Core Stats:** HP: `45`, Move: `2`

**Properties:** `tag: dinosaur`, `faction: enemies`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `TrexEat` | **spells:** TrexStomp, TrexSwitchTarget, TrexReacquireTarget

**Passives:**
- `Trample 3`
- `CounterAttack TrexSwitchTarget`
- `PrioritizeAggroTarget 1`

---

### Tar Baby (`TarBaby`)
> Its ranged attack creates Tar tiles. Leaves Tar tiles in its path.

**Core Stats:** HP: `9`, Move: `4`

**Properties:** `tag: blob`, `faction: enemies`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `TarBall`

**Passives:**
- `TileTrail_Ahead OilTile`
- `GoopWalk 1`
- `StatusImmunity Tarred`

---

### Triceratops (`Triceratops`)
> Has a dash attack. Counterattacks units that damage it and flings them backwards. Trample.

**Core Stats:** HP: `45`, Move: `2`

**Properties:** `tag: dinosaur`, `faction: enemies`, `round_end_bonus_turns: 1`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `TriceratopsGore` | **spells:** TriceratopsTrample

**Passives:**
- `Trample 3`
- `FaceLastDamage 1`
- `CounterAttack attack`
- `Brace 2`

---

## Recurrent

### Albino Tom Tom (`AlbinoTomTom`)
> Its wide melee attacks have Knockback 2.

**Core Stats:** HP: `17`, Move: `?`, Spd: `1`

**Properties:** `tag: cat`, `type: cat`, `round_end_bonus_turns: 1`, `base_mana_regen: 999`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `WideSwipe`

**Passives:**
- `AddMeleeKnockback 2`

---

### Astronaut (`Astro`)
> Its melee attack has a high chance to inflict Stun.

**Core Stats:** HP: `8`, Move: `1`

**Properties:** `tag: cat`, `type: cat`, `shield: 5`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `BasicJump` | **attack:** `BasicMelee`

---

### Big Asteroid (`BigAsteroid`)
> Its attack spawns a boulder. Gets knocked back with Chain Knockback when hit. Can only recieve 1 damage at a time. Immune to status effects.

**Core Stats:** HP: `5`, Move: `2`

**Properties:** `tag: rock`, `faction: enemies`, `shield: 7`, `flying: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BigAsteroidBarrage`

**Passives:**
- `LimitDamage 1`
- `LimitHeal 0`
- `StripStatuses 1`

---

### Birthwort (`Birthwort`)
> Blind. Can melee attack and dash with Trample in random directions. Fires shots that inflict Rot whenever it's attacked. Heals itself and its neighbors at the end of its turn.

**Core Stats:** HP: `24`, Move: `2`

**Properties:** `tag: plant`, `faction: enemies`, `initial_health: 18`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** BirthwortReactionShot, BirthwortTrample, BirthwortHeal

**Passives:**
- `Plant 1`
- `ElementImmune Creep`
- `ImmediateAbilityReaction BirthwortReactionShot`

---

### Bone Worm (`SnakeyBones`)
> Ranged attacker. Gains more range the taller it becomes. Loses height when it takes damage. Can only take 1 damage at a time when tall. Undead.

**Core Stats:** HP: `0`, Move: `?`

**Properties:** `tag: [worm skeleton]`, `auto_run_priority: stationary`, `shield: 8`, `faction: enemies`, `corpse_health: 0`, `can_be_overkilled: false`

**Abilities:** **move:** `None` | **spells:** attack, BoneWormShotSmall, FormShrinkTwoSnakey, FormShrinkOneSnakey, FormGrowTwoSnakey, FormGrowThreeSnakey, FormGrowTwo, FormGrowThree

**Passives:**
- `NoHealthOnlyShield 1`
- `Undead 1`
- `StatusImmunity [Poison, Bleed]`
- `PrioritizeHitDifferentTargets 1`

---

### Boomer (`BoomerCat`)
> Explodes when killed, damaging all nearby units.

**Core Stats:** HP: `15`, Move: `3`, Str: `4`

**Properties:** `tag: cat`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** BoomerCatExplode

**Passives:**
- `DeathRattle BoomerCatExplode`
- `AddMeleeKnockback 1`

---

### Bramble Baby (`BrambleBaby`)
> Spawns Bramble tiles and pulls units into them.

**Core Stats:** HP: `8`, Move: `?`

**Properties:** `tag: plant`, `faction: enemies`

**Abilities:** **move:** `Teleport` | **attack:** `BramblePull` | **spells:** BrambleBabyEntangle

**Passives:**
- `Plant 1`
- `ElementImmune Creep`
- `Thorns 1`

---

### Brute (`BigDemon`)
> Throws rocks that have a chance inflict Stun when at range. Will uppercut units above 50% health. Will instantly kill units below 50% health. Immune to Fire.

**Core Stats:** HP: `20`, Move: `2`

**Properties:** `tag: demon`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `DemonUppercut` | **spells:** DemonRockThrow, NeckSnap

**Passives:**
- `ElementImmune Fire`

---

### Carcass (`Carcus`)
> Spawns random types of Maggots.

**Core Stats:** HP: `1`, Move: `0`, Spd: `0`

**Properties:** `tag: animal`, `faction: enemies`, `corpse_health: 0`, `can_be_backstabbed: false`

**Abilities:** **move:** `None` | **attack:** `CarcusSpawn`

---

### Chain Demon (`DemonHooker`)
> Will hook and pull units toward itself. Immune to fire.

**Core Stats:** HP: `13`, Move: `?`

**Properties:** `tag: [cat demon]`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `DH_Attack` | **spells:** DH_MeatHook

**Passives:**
- `ElementImmune Fire`

---

### Chaos Stacy (`ChaosStacy`)
> Its melee attack inflicts Scrambled. Reflects projectiles and knocks back units that contact.

**Core Stats:** HP: `26`, Move: `4`, Spd: `3`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `ChaosStacyAttack`

**Passives:**
- `ReflectProjectiles 1`

---

### Chum Bag (`ChumBag`)
> Its long range attack spawns Maggots if it hits an empty tile. Becomes a Chummy when killed. Stationary.

**Core Stats:** HP: `1`, Move: `4`, Spd: `3`

**Properties:** `tag: [blob trash]`, `hidden_tag: container`, `auto_run_priority: stationary`, `faction: enemies`, `corpse_health: 0`

**Abilities:** **move:** `None` | **attack:** `ChumShot_Damage` | **spells:** ChumShot_Maggot

**Passives:**
- `TransformOnDeath Chummy`

---

### Cloaked Demon (`CloakedDemon`)
> Casts an area spell that inflicts Burn 3 to enemies and gives +1 Damage to allies. Inflicts Hex on units that damage it. Immune to Fire.

**Core Stats:** HP: `13`, Move: `2`

**Properties:** `tag: demon`, `faction: enemies`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `CloakerHex` | **spells:** TwistingFlames

**Passives:**
- `ElementImmune Fire`
- `CounterAttack CloakerHex`

---

### Crater Creeper (`CraterCreeper`)
> Shoots rocks or dashes forward leaving an Amoeba behind. Can only be damaged from the front.

**Core Stats:** HP: `8`, Move: `3`

**Properties:** `tag: [blob rock]`, `faction: enemies`, `dispersed_bonus_turns: 1`, `corpse_health: 0`, `mana_regen: 999`, `mana: 100`, `shield: 8`, `always_triggers_traps: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `CraterCreeperRockBlast` | **spells:** CraterCreeperSlide

**Passives:**
- `SpawnCreepOnHit 1`
- `SpawnCreepOnHitKnockback 1`
- `CanShield 1`
- `IgnoreTiles 1`
- `ChangeTileOnPop CreepTile`
- `TransformOnDeath CraterCreeperOut`
- `ElementImmune Creep`

---

### Crater Creeper (`CraterCreeperOut`)
> Its ranged attack spawns an Amoeba.

**Core Stats:** HP: `8`, Move: `?`, Spd: `8`

**Properties:** `tag: blob`, `faction: enemies`, `dispersed_bonus_turns: 1`, `corpse_health: 1`, `mana_regen: 999`, `mana: 100`

**Abilities:** **move:** `Swim` | **attack:** `ShortCreepshotCrater` | **spells:** MoveOne

**Passives:**
- `GroundFlopper MoveOne`
- `WaterWalk 1`
- `ElementImmune Creep`

---

### Daddy Shark (`DaddyShark`)
> Will instantly kill anything it can reach! Takes bonus turns for each bleeding unit. Focuses on bleeding units.

**Core Stats:** HP: `28`, Move: `1`, Spd: `1`

**Properties:** `tag: [cat fish]`, `faction: enemies`, `size: 2x2`, `move_block: everything_even_when_dead`, `view_bleeding_characters_as_enemies: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `DaddyHungry`

**Passives:**
- `Trample 3`
- `SharkySmellsBlood 1`

---

### Dip (`Dip`)
> Melee attacker.

**Core Stats:** HP: `1`, Move: `3`, Str: `3`

**Properties:** `tag: poop`, `corpse_health: 0`, `faction: enemies`, `type: small`, `inherit_faction: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### Flea (`Flea`)
> Its melee attack damages itself.

**Core Stats:** HP: `2`, Move: `4`, Str: `4`

**Properties:** `tag: bug`, `corpse_health: 0`, `faction: enemies`, `type: small`, `deathpoof_size: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `SuicideMelee`

---

### Floater (`Floater`)
> Melee attacker that moves away after it deals damage.

**Core Stats:** HP: `8`, Move: `3`

**Properties:** `tag: poop`, `faction: enemies`, `base_mana_regen: 999`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `FloaterMelee`

**Passives:**
- `WaterWalk 1`

---

### Fly (`Fly`)
> Melee attacker. Flying.

**Core Stats:** HP: `1`, Move: `4`, Str: `2`, Spd: `2`

**Properties:** `tag: bug`, `faction: enemies`, `corpse_health: 0`, `base_mana_regen: 999`, `flying: true`, `type: small`, `deathpoof_size: 1`, `can_be_backstabbed: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### Fly Swarm (`FlySwarm`)
> Performs a melee attack that hits once for each fly. Each time it's damaged it loses a fly.

**Core Stats:** HP: `5`, Move: `3`, Str: `1`, Spd: `2`

**Properties:** `tag: bug`, `faction: enemies`, `corpse_health: 0`, `base_mana_regen: 999`, `flying: true`, `deathpoof_size: 1`, `can_be_backstabbed: false`, `weak_threshold: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** FormShrinkFour, FormShrinkThree, FormShrinkTwo, FormShrinkOne

**Passives:**
- `LimitDamage 1`
- `LimitHeal 1`

---

### GeoLad (`GeoLad`)
> Performs a jump attack that damages and knocks back all units in an area.

**Core Stats:** HP: `4`, Move: `2`

**Properties:** `tag: rock`, `faction: enemies`, `shield: 8`, `can_be_backstabbed: false`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** QuakeJump

**Passives:**
- `Brace 1`

---

### Host (`Host`)
> Shoots 3 projectiles in a spread. Reflects projectiles and knocks back units who contact it. Stationary.

**Core Stats:** HP: `13`, Move: `2`, Str: `3`, Dex: `3`

**Properties:** `tag: [blob undead]`, `auto_run_priority: stationary`, `faction: enemies`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `None` | **attack:** `HostSpit` | **spells:** HostShove

---

### Hot Poker (`PokerDemon`)
> Has 2 melee attacks, one with Immobilize, the other with Burn that knocks a unit in the direction it's facing. Can give its allies extra turns. Immune to Fire.

**Core Stats:** HP: `11`, Move: `3`

**Properties:** `tag: [demon]`, `faction: enemies`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `PokerAttack` | **spells:** PokerPokeCat, PokerPokeAlly

**Passives:**
- `AlwaysHitDifferentTargets 1`
- `ElementImmune Fire`

---

### Kitten (`Kitten`)
> Runs away when damaged.

**Core Stats:** HP: `5`, Move: `?`, Str: `3`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### Leaper (`Leaper`)
> Its leap attack damages and knocks back all adjacent units.

**Core Stats:** HP: `9`, Move: `2`

**Properties:** `tag: [rat blob]`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `RatLeap`

---

### Lil' Rat (`Rat`)
> Dashes in a straight line.

**Core Stats:** HP: `5`, Move: `1`, Str: `4`

**Properties:** `tag: rat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `Dash_Enemy`

**Passives:**
- `CanMutateTo [Lumpy, Leaper]`

---

### Lumpy (`Lumpy`)
> Its ranged attack creates Creep. Spawns Creep when damaged.

**Core Stats:** HP: `9`, Move: `3`, Str: `3`, Dex: `4`

**Properties:** `tag: [rat blob]`, `faction: enemies`, `initiative: 5`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `CreepRanged`

**Passives:**
- `SpawnCreepOnHit 1`
- `ElementImmune Creep`

---

### Maggot (`Maggot`)
> Melee attacker.

**Core Stats:** HP: `1`, Move: `2`, Str: `2`, Dex: `1`

**Properties:** `tag: worm`, `corpse_health: 0`, `faction: enemies`, `type: small`, `initiative: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `CanMutateTo [TumorousMaggot, ChargeyMaggot, SwappyMaggot]`

---

### Mangy (`Mangy`)
> Its ranged attack may inflict Poison. Spawns maggots when damaged.

**Core Stats:** HP: `7`, Move: `?`, Str: `4`, Spd: `3`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `PoisonShot`

---

### Pile (`Pile`)
> Its ranged attack spawns Dips. Stationary.

**Core Stats:** HP: `8`, Move: `0`

**Properties:** `tag: poop`, `auto_run_priority: stationary`, `faction: enemies`, `corpse_health: 0`, `can_be_backstabbed: false`

**Abilities:** **move:** `None` | **attack:** `DipShot` | **spells:** SpawnDip

---

### Pinky (`Pinky`)
> Melee attacker. Moves randomly.

**Core Stats:** HP: `1`, Move: `2`, Str: `2`

**Properties:** `tag: rat`, `faction: enemies`, `type: small`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### Popeye (`PopeyeCat`)
> Has a dash attack with knockback.

**Core Stats:** HP: `17`, Move: `?`, Str: `8`, Spd: `2`

**Properties:** `tag: cat`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `PopeyeDash`

---

### Reaper (`Reaper`)
> Performs a spin attack at the start of its turn. Teleports to units that kill its allies. Undead.

**Core Stats:** HP: `18`, Move: `2`

**Properties:** `tag: [ghost skeleton]`, `faction: enemies`, `corpse_health: 0`, `flying: true`

**Abilities:** **move:** `FloatMove` | **attack:** `ReaperSpin` | **spells:** ReaperRevenge

**Passives:**
- `MoveTowardsKillers ReaperRevenge`
- `Undead 1`

---

### Robo-Cat (`RoboTom`)
> Its wide melee attacks have Knockback 10.

**Core Stats:** HP: `1`, Move: `?`, Str: `6`, Spd: `1`

**Properties:** `tag: [cat robot]`, `type: cat`, `shield: 11`, `dispersed_bonus_turns: 1`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`

**Abilities:** **move:** `DefaultMove` | **attack:** `WideSwipe`

**Passives:**
- `Brace 3`
- `AddMeleeKnockback 10`
- `Robot 1`

---

### Security Bot (`SecurityBot`)
> When its allies are damaged, it will move towards the attacker and attempt to attack it. Gains +1 movement range at the end of its turn.

**Core Stats:** HP: `0`, Move: `1`

**Properties:** `tag: robot`, `faction: enemies`, `auto_run_priority: support`, `shield: 12`, `can_be_overkilled: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `SBotAttack` | **spells:** SBotAngryMove, SBotRecharge, SBotAnger

**Passives:**
- `Brace 2`
- `NoHealthOnlyShield 1`
- `Robot 1`

---

### Skeleton Cat (`SkeletonCat`)
> Comes back from the dead if its body isn't destroyed! Undead.

**Core Stats:** HP: `0`, Move: `3`, Str: `9`

**Properties:** `tag: [cat skeleton]`, `type: cat`, `shield: 1`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `NoHealthOnlyShield 1`
- `Undead 1`
- `StatusImmunity [Poison, Bleed]`

---

### Skeleton Cat (`SkeletonCatCorpse`)
> Will come back from the dead next turn! Undead.

**Core Stats:** HP: `0`, Move: `?`

**Properties:** `tag: [cat skeleton]`, `type: cat`, `shield: 12`, `faction: enemies`, `initiative: 10`, `corpse_health: 0`, `exclude_from_hallucinate: true`

**Abilities:** **move:** `None` | **attack:** `None`

**Passives:**
- `NoHealthOnlyShield 1`
- `Undead 1`
- `StatusImmunity [Poison, Bleed]`
- `CountAsCorpse 1`

---

### Skeleton Shambler (`SkeletonShambler`)
> Will throw units it can reach. Lunges in a random direction at the end of its turn. Comes back from the dead if its body isn't destroyed! Undead.

**Core Stats:** HP: `0`, Move: `3`, Spd: `3`

**Properties:** `tag: skeleton`, `shield: 12`, `faction: enemies`, `size: 2x2`, `move_block: everything_even_when_dead`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `ShamblerDash` | **spells:** ShamblerToss

**Passives:**
- `Trample 3`
- `NoHealthOnlyShield 1`
- `Undead 1`
- `StatusImmunity [Poison, Bleed]`

---

### Skeleton Shambler (`SkeletonShamblerCorpse`)
> Comes back from the dead if its body isn't destroyed! Undead.

**Core Stats:** HP: `0`, Move: `?`, Spd: `3`

**Properties:** `tag: skeleton`, `shield: 3`, `faction: enemies`, `corpse_health: 0`, `can_be_overkilled: false`, `size: 2x2`, `move_block: everything_even_when_dead`, `exclude_from_hallucinate: true`

**Abilities:** **move:** `None` | **attack:** `None`

**Passives:**
- `NoHealthOnlyShield 1`
- `Undead 1`
- `StatusImmunity [Poison, Bleed]`
- `CountAsCorpse 1`

---

### Small Asteroid (`SmallAsteroid`)
> Its attack shoots rocks at random tiles in an area. Gets knocked back with Chain Knockback when hit. Can only recieve 1 damage at a time. Immune to status effects.

**Core Stats:** HP: `1`, Move: `3`

**Properties:** `tag: rock`, `faction: enemies`, `shield: 3`, `flying: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `SmallAsteroidBarrage`

**Passives:**
- `LimitDamage 1`
- `LimitHeal 0`
- `StripStatuses 1`

---

### Spiderling (`TinySpider`)
> Burrows inside its victims, inflicting Infested.

**Core Stats:** HP: `2`, Move: `4`, Str: `3`

**Properties:** `tag: bug`, `corpse_health: 0`, `faction: enemies`, `type: small`, `deathpoof_size: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `SpiderSuicideMelee`

**Passives:**
- `StatusImmunity Webbed`

---

### Spookie (`Spookie`)
> Its melee attack drains mana. Undead.

**Core Stats:** HP: `9`, Move: `4`

**Properties:** `tag: ghost`, `faction: enemies`, `flying: true`, `corpse_health: 0`

**Abilities:** **move:** `Teleport` | **attack:** `SpookieLick` | **spells:** DefaultMove

**Passives:**
- `Undead 1`

---

### Tall Skeleton Cat (`TallSkeletonCat`)
> Its ranged attack can also give [img:shield] to its allies. Will come back from the dead if its body isn't destroyed! Undead.

**Core Stats:** HP: `0`, Move: `3`

**Properties:** `tag: [cat skeleton]`, `type: cat`, `shield: 15`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`, `corpse_health: 0`, `act_points: 2`

**Abilities:** **move:** `DefaultMove` | **attack:** `BadBone` | **spells:** BadBone_copy, GoodBone, GoodBone_copy

**Passives:**
- `YOffset .35`
- `Undead 1`
- `PrioritizeHitDifferentTargets 1`
- `NoHealthOnlyShield 1`
- `StatusImmunity [Poison, Bleed]`

---

### Tall Skeleton Cat (`TallSkeletonCatCorpse`)
> Will come back from the dead next turn! Undead.

**Core Stats:** HP: `0`, Move: `?`

**Properties:** `tag: [cat skeleton]`, `type: cat`, `shield: 1`, `faction: enemies`, `initiative: 10`, `corpse_health: 0`, `exclude_from_hallucinate: true`

**Abilities:** **move:** `None` | **attack:** `None`

**Passives:**
- `NoHealthOnlyShield 1`
- `Undead 1`
- `StatusImmunity [Poison, Bleed]`
- `CountAsCorpse 1`

---

### Tall Tumor (`TallTumor`)
> Drains unspent mana from its enemies when they end their turn. Deals damage equal to the mana drained. Counterattacks with a spin attack when damaged.

**Core Stats:** HP: `16`, Move: `2`

**Properties:** `tag: tumor`, `faction: enemies`, `initial_health: 8`, `auto_run_priority: support`

**Abilities:** **move:** `DefaultMove` | **attack:** `TT_Thrash` | **spells:** TT_ManaBurn

**Passives:**
- `CounterAttack TT_Thrash`
- `TallTumorManaBurn TT_ManaBurn`

---

### Tom Tom (`TomTom`)
> It's slow, but has a wide melee attack.

**Core Stats:** HP: `15`, Move: `?`, Str: `6`, Spd: `1`

**Properties:** `tag: cat`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `WideSwipe`

---

### Tremblo (`Tremblo`)
> Its melee attack inflicts Stun and spawns rocks. Can suck rocks towards itself and eat them to gain Brace and Shield.

**Core Stats:** HP: `4`, Move: `2`

**Properties:** `tag: rock`, `faction: enemies`, `shield: 10`, `can_be_backstabbed: false`, `corpse_health: 0`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `TrembloSmash` | **spells:** TrembloSuck, TrembloEat

---

### Water Leech (`WaterLeech`)
> Seeks water when its out of water. While in water, dashes in a straight line with Lifesteal that passes through units.

**Core Stats:** HP: `18`, Move: `3`

**Properties:** `tag: worm`, `faction: enemies`, `initial_health: 8`, `base_mana_regen: 999`

**Abilities:** **move:** `SwimmerMove` | **attack:** `LeechDash` | **spells:** DefaultMove

**Passives:**
- `WaterWalk 1`

---

## Sewers

### Baby Shark (`BabyShark`)
> Its bite inflicts Bleed but does no damage. Takes bonus turns for each bleeding unit. Focuses on bleeding units.

**Core Stats:** HP: `5`, Move: `4`, Str: `1`

**Properties:** `tag: [cat fish]`, `faction: enemies`, `type: small`, `view_bleeding_characters_as_enemies: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BabySharkMelee`

**Passives:**
- `SharkySmellsBlood 1`

---

### Boomer (`BoomerCat`)
> Explodes when killed, damaging all nearby units.

**Core Stats:** HP: `15`, Move: `3`, Str: `4`

**Properties:** `tag: cat`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** BoomerCatExplode

**Passives:**
- `DeathRattle BoomerCatExplode`
- `AddMeleeKnockback 1`

---

### Cat Caller (`CatCaller`)
> Slows units. Counterattacks when hit.

**Core Stats:** HP: `7`, Move: `?`, Str: `4`

**Properties:** `tag: cat`, `type: cat`, `auto_run_priority: support`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** CatCall

**Passives:**
- `CounterAttack attack`

---

### Daddy Shark (`DaddyShark`)
> Will instantly kill anything it can reach! Takes bonus turns for each bleeding unit. Focuses on bleeding units.

**Core Stats:** HP: `28`, Move: `1`, Spd: `1`

**Properties:** `tag: [cat fish]`, `faction: enemies`, `size: 2x2`, `move_block: everything_even_when_dead`, `view_bleeding_characters_as_enemies: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `DaddyHungry`

**Passives:**
- `Trample 3`
- `SharkySmellsBlood 1`

---

### Dip (`Dip`)
> Melee attacker.

**Core Stats:** HP: `1`, Move: `3`, Str: `3`

**Properties:** `tag: poop`, `corpse_health: 0`, `faction: enemies`, `type: small`, `inherit_faction: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### Fetus (`Fetus`)
> Ranged attacker. Can drink water to heal.

**Core Stats:** HP: `12`, Move: `2`, Dex: `4`

**Properties:** `tag: fetus`, `faction: enemies`, `initial_health: 8`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicShortLobbed_Water` | **spells:** DefaultMove, DrinkUp

**Passives:**
- `WaterWalk 1`

---

### Fetus Gusher (`FetusGusher`)
> Its water attack pushes all units in a straight line. Must be in water to attack. Seeks water when out of water.

**Core Stats:** HP: `12`, Move: `3`

**Properties:** `tag: fetus`, `faction: enemies`, `base_mana_regen: 999`, `round_end_bonus_turns: 1`

**Abilities:** **move:** `SwimmerMove` | **attack:** `FetusGush` | **spells:** DefaultMove

**Passives:**
- `GroundFlopper DefaultMove`
- `WaterWalk 1`

---

### Floater (`Floater`)
> Melee attacker that moves away after it deals damage.

**Core Stats:** HP: `8`, Move: `3`

**Properties:** `tag: poop`, `faction: enemies`, `base_mana_regen: 999`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `FloaterMelee`

**Passives:**
- `WaterWalk 1`

---

### Gassy (`GassyCat`)
> Its farts inflict Poison 3. Farts and projects itself forward when damaged.

**Core Stats:** HP: `12`, Move: `5`

**Properties:** `tag: cat`, `type: cat`, `shield: 3`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`

**Abilities:** **move:** `DefaultMove` | **attack:** `GasBlast`

**Passives:**
- `AbilityReaction attack`

---

### Kitten (`Kitten`)
> Runs away when damaged.

**Core Stats:** HP: `5`, Move: `?`, Str: `3`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### Pile (`Pile`)
> Its ranged attack spawns Dips. Stationary.

**Core Stats:** HP: `8`, Move: `0`

**Properties:** `tag: poop`, `auto_run_priority: stationary`, `faction: enemies`, `corpse_health: 0`, `can_be_backstabbed: false`

**Abilities:** **move:** `None` | **attack:** `DipShot` | **spells:** SpawnDip

---

### Pinky (`Pinky`)
> Melee attacker. Moves randomly.

**Core Stats:** HP: `1`, Move: `2`, Str: `2`

**Properties:** `tag: rat`, `faction: enemies`, `type: small`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### Sharky (`SharkyCat`)
> Its bite inflicts Bleed. Takes bonus turns for each bleeding unit. Focuses on bleeding units.

**Core Stats:** HP: `7`, Move: `3`, Str: `2`

**Properties:** `tag: [cat fish]`, `type: cat`, `shield: 7`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`, `view_bleeding_characters_as_enemies: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `SharkDash`

**Passives:**
- `SharkySmellsBlood 1`
- `WaterWalk 1`

---

### Water Kitten (`WaterKitten`)
> Moves away when damaged. May be hiding in water...

**Core Stats:** HP: `5`, Move: `?`, Str: `3`

**Properties:** `tag: cat`, `type: cat`, `shield: 1`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** WaterTrailMove

**Passives:**
- `WaterWalk 1`

---

### Water Leech (`WaterLeech`)
> Seeks water when its out of water. While in water, dashes in a straight line with Lifesteal that passes through units.

**Core Stats:** HP: `18`, Move: `3`

**Properties:** `tag: worm`, `faction: enemies`, `initial_health: 8`, `base_mana_regen: 999`

**Abilities:** **move:** `SwimmerMove` | **attack:** `LeechDash` | **spells:** DefaultMove

**Passives:**
- `WaterWalk 1`

---

## Summons

### Bear (`Bear`)
> *(No Description)*

**Core Stats:** HP: `15`, Move: `3`

**Properties:** `tag: animal`, `faction: allies`, `inherit_faction: true`, `weak_threshold: 0`, `size: 2x2`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicBigMelee` | **can_get_bonus:** `true`

**Passives:**
- `Trample 3`

---

### Bounty Hunter (`GunCat`)
> Can shoot anywhere within its line of sight. Prefers long shots.

**Core Stats:** HP: `9`, Move: `2`, Str: `4`, Spd: `2`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `GuncatShoot`

**Passives:**
- `WeaponsDontLoseDurability 1`
- `PrioritizeFarAwayTargets 10`

---

### Bounty Hunter (`EventBountyHunter`)
> *(No Description)*

**Core Stats:** HP: `17`, Move: `2`, Str: `4`, Spd: `2`

**Properties:** `tag: cat`, `type: cat`, `faction: birds`, `base_mana_regen: 999`, `kill_required: false`, `can_collect_coins: true`, `held_coins: [5 10]`, `aggro_target_is_enemy: true`, `can_run: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `GuncatShoot`

**Passives:**
- `WeaponsDontLoseDurability 1`
- `EventBounterHunterPassive 1`

---

### Caterpillar (`Catepillar`)
> Gains All Stats Up each turn. Evolves into a Moth when it reaches All Stats Up 5.

**Core Stats:** HP: `1`, Move: `1`, Str: `1`, Dex: `1`, Con: `1`, Int: `1`, Spd: `1`, Cha: `1`

**Properties:** `tag: animal`, `type: small`, `faction: allies`, `inherit_faction: true`, `weak_threshold: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **can_get_bonus:** `true`

---

### Flea (`Flea`)
> Its melee attack damages itself.

**Core Stats:** HP: `2`, Move: `4`, Str: `4`

**Properties:** `tag: bug`, `corpse_health: 0`, `faction: enemies`, `type: small`, `deathpoof_size: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `SuicideMelee`

---

### Frog (`NeutralToad`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `faction: none`, `kill_required: false`

---

### Maggot (`Maggot`)
> Melee attacker.

**Core Stats:** HP: `1`, Move: `2`, Str: `2`, Dex: `1`

**Properties:** `tag: worm`, `corpse_health: 0`, `faction: enemies`, `type: small`, `initiative: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `CanMutateTo [TumorousMaggot, ChargeyMaggot, SwappyMaggot]`

---

### Pooter (`Pooter`)
> Ranged attacker. Flying.

**Core Stats:** HP: `6`, Move: `2`

**Properties:** `tag: bug`, `faction: enemies`, `flying: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicShortLobbed`

---

### Snake (`Snake`)
> *(No Description)*

**Core Stats:** HP: `1`, Move: `5`, Str: `2`, Dex: `2`, Con: `2`, Int: `2`, Cha: `2`

**Properties:** `tag: animal`, `type: small`, `faction: allies`, `inherit_faction: true`, `weak_threshold: 0`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **can_get_bonus:** `true`

---

### Spiderling (`TinySpider`)
> Burrows inside its victims, inflicting Infested.

**Core Stats:** HP: `2`, Move: `4`, Str: `3`

**Properties:** `tag: bug`, `corpse_health: 0`, `faction: enemies`, `type: small`, `deathpoof_size: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `SpiderSuicideMelee`

**Passives:**
- `StatusImmunity Webbed`

---

### Squirrel (`Squirrel`)
> *(No Description)*

**Core Stats:** HP: `1`, Move: `5`, Str: `2`, Dex: `1`, Con: `1`, Int: `1`, Spd: `8`, Cha: `1`

**Properties:** `tag: [animal squirrel]`, `type: small`, `faction: allies`, `inherit_faction: true`, `weak_threshold: 0`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `SquirrelFurySwipes` | **can_get_bonus:** `true`

---

### Tiny Tumor (`TinyTumor`)
> Its melee attack causes cats it hits to lose 1 [img:con] permanently and has a chance to give them cancer.

**Core Stats:** HP: `4`, Move: `4`, Str: `2`, Spd: `2`

**Properties:** `tag: tumor`, `faction: enemies`, `type: small`, `corpse_health: 0`, `flying: true`, `deathpoof_size: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `CancerMelee`

**Passives:**
- `Brace 2`

---

### Tom Tom (`TomTom`)
> It's slow, but has a wide melee attack.

**Core Stats:** HP: `15`, Move: `?`, Str: `6`, Spd: `1`

**Properties:** `tag: cat`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `WideSwipe`

---

### Turtle (`Turtle`)
> *(No Description)*

**Core Stats:** HP: `1`, Move: `1`, Str: `3`, Spd: `1`, Cha: `8`

**Properties:** `tag: [animal dog]`, `type: small`, `faction: allies`, `inherit_faction: true`, `shield: 10`, `weak_threshold: 0`, `corpse_health: 1`, `can_be_overkilled: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicTankMelee` | **can_get_bonus:** `true`

---

## The Core

### Belcher (`Belcher`)
> Its ranged attack inflicts Burn and creates a lava tile. Immune to fire.

**Core Stats:** HP: `12`, Move: `2`

**Properties:** `tag: [cat demon]`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `BelcherLavashot`

**Passives:**
- `ElementImmune Fire`

---

### Brute (`BigDemon`)
> Throws rocks that have a chance inflict Stun when at range. Will uppercut units above 50% health. Will instantly kill units below 50% health. Immune to Fire.

**Core Stats:** HP: `20`, Move: `2`

**Properties:** `tag: demon`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `DemonUppercut` | **spells:** DemonRockThrow, NeckSnap

**Passives:**
- `ElementImmune Fire`

---

### Chain Demon (`DemonHooker`)
> Will hook and pull units toward itself. Immune to fire.

**Core Stats:** HP: `13`, Move: `?`

**Properties:** `tag: [cat demon]`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `DH_Attack` | **spells:** DH_MeatHook

**Passives:**
- `ElementImmune Fire`

---

### Cloaked Demon (`CloakedDemon`)
> Casts an area spell that inflicts Burn 3 to enemies and gives +1 Damage to allies. Inflicts Hex on units that damage it. Immune to Fire.

**Core Stats:** HP: `13`, Move: `2`

**Properties:** `tag: demon`, `faction: enemies`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `CloakerHex` | **spells:** TwistingFlames

**Passives:**
- `ElementImmune Fire`
- `CounterAttack CloakerHex`

---

### Core Freak (`CoreFreak`)
> Can perform a flurry melee attack or a headbutt that inflicts Stun. Blind.

**Core Stats:** HP: `14`, Move: `2`

**Properties:** `tag: [humanoid tumor]`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `CoreFreakAttack` | **spells:** CoreFreakFury

---

### Hot Poker (`PokerDemon`)
> Has 2 melee attacks, one with Immobilize, the other with Burn that knocks a unit in the direction it's facing. Can give its allies extra turns. Immune to Fire.

**Core Stats:** HP: `11`, Move: `3`

**Properties:** `tag: [demon]`, `faction: enemies`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `PokerAttack` | **spells:** PokerPokeCat, PokerPokeAlly

**Passives:**
- `AlwaysHitDifferentTargets 1`
- `ElementImmune Fire`

---

### Mega Tumor (`MegaTumor`)
> Trample. Gains +1 movement range at the end of its turns. Immune to Fire.

**Core Stats:** HP: `20`, Move: `1`

**Properties:** `tag: tumor`, `faction: enemies`, `can_be_backstabbed: false`, `size: 2x2`, `lock_orientation: [0, -1]`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `TumorDash` | **spells:** TumorPowerup

**Passives:**
- `Trample 3`
- `Brace 2`
- `ElementImmune Fire`

---

### Tall Tumor (`TallTumor`)
> Drains unspent mana from its enemies when they end their turn. Deals damage equal to the mana drained. Counterattacks with a spin attack when damaged.

**Core Stats:** HP: `16`, Move: `2`

**Properties:** `tag: tumor`, `faction: enemies`, `initial_health: 8`, `auto_run_priority: support`

**Abilities:** **move:** `DefaultMove` | **attack:** `TT_Thrash` | **spells:** TT_ManaBurn

**Passives:**
- `CounterAttack TT_Thrash`
- `TallTumorManaBurn TT_ManaBurn`

---

### Tumor Cat (`TumorCat`)
> Will dash forward 10 tiles with Trample when damaged. Blind.

**Core Stats:** HP: `11`, Move: `?`

**Properties:** `tag: [cat tumor]`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `TC_Attack` | **spells:** TC_DashReaction

**Passives:**
- `AbilityReaction TC_DashReaction`
- `Brace 1`

---

### Tumorhead (`HeadTumor`)
> Its melee attack knocks units back 3 tiles. Dashes forward when damaged.

**Core Stats:** HP: `10`, Move: `2`

**Properties:** `tag: [humanoid tumor]`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `HeadTumorAttack` | **spells:** HeadTumorResponse

**Passives:**
- `Brace 1`
- `AbilityReaction HeadTumorResponse`

---

### Whisperer (`Whisperer`)
> Its ranged attack inflicts Bruise and -2 [img:spd] to enemies, and Brace and +2 [img:spd] to allies. Its melee attack inflicts Charm.

**Core Stats:** HP: `14`, Move: `2`

**Properties:** `tag: [humanoid tumor]`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `WhispererThrowDamage` | **spells:** WhispererThrowBuff, WhispererWhisper

---

## The Crater

### Amoeba (`Amoeba`)
> Can attach itself to equipment slots on cats, and will break existing equipment if it does. Will attempt to find a rock to defend itself.

**Core Stats:** HP: `3`, Move: `?`

**Properties:** `tag: blob`, `faction: enemies`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `AmoebaAttach` | **spells:** PickupRock

---

### Birthwort (`Birthwort`)
> Blind. Can melee attack and dash with Trample in random directions. Fires shots that inflict Rot whenever it's attacked. Heals itself and its neighbors at the end of its turn.

**Core Stats:** HP: `24`, Move: `2`

**Properties:** `tag: plant`, `faction: enemies`, `initial_health: 18`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** BirthwortReactionShot, BirthwortTrample, BirthwortHeal

**Passives:**
- `Plant 1`
- `ElementImmune Creep`
- `ImmediateAbilityReaction BirthwortReactionShot`

---

### Bramble Baby (`BrambleBaby`)
> Spawns Bramble tiles and pulls units into them.

**Core Stats:** HP: `8`, Move: `?`

**Properties:** `tag: plant`, `faction: enemies`

**Abilities:** **move:** `Teleport` | **attack:** `BramblePull` | **spells:** BrambleBabyEntangle

**Passives:**
- `Plant 1`
- `ElementImmune Creep`
- `Thorns 1`

---

### Carnibulb (`Carnibulb`)
> Will instantly kill anything it can reach. Has +1 movement range for each Sprout. Summons a Sprout at the end of its turn.

**Core Stats:** HP: `22`, Move: `1`, Spd: `0`

**Properties:** `tag: plant`, `faction: enemies`, `size: 2x2`, `move_block: everything_even_when_dead`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `CarnibulbEat` | **spells:** Sprout

**Passives:**
- `Trample 3`
- `Plant 1`
- `ElementImmune Creep`
- `AddMovement -1`
- `SproutsGrantMovement 1`

---

### Crater Creeper (`CraterCreeper`)
> Shoots rocks or dashes forward leaving an Amoeba behind. Can only be damaged from the front.

**Core Stats:** HP: `8`, Move: `3`

**Properties:** `tag: [blob rock]`, `faction: enemies`, `dispersed_bonus_turns: 1`, `corpse_health: 0`, `mana_regen: 999`, `mana: 100`, `shield: 8`, `always_triggers_traps: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `CraterCreeperRockBlast` | **spells:** CraterCreeperSlide

**Passives:**
- `SpawnCreepOnHit 1`
- `SpawnCreepOnHitKnockback 1`
- `CanShield 1`
- `IgnoreTiles 1`
- `ChangeTileOnPop CreepTile`
- `TransformOnDeath CraterCreeperOut`
- `ElementImmune Creep`

---

### Crater Creeper (`CraterCreeperOut`)
> Its ranged attack spawns an Amoeba.

**Core Stats:** HP: `8`, Move: `?`, Spd: `8`

**Properties:** `tag: blob`, `faction: enemies`, `dispersed_bonus_turns: 1`, `corpse_health: 1`, `mana_regen: 999`, `mana: 100`

**Abilities:** **move:** `Swim` | **attack:** `ShortCreepshotCrater` | **spells:** MoveOne

**Passives:**
- `GroundFlopper MoveOne`
- `WaterWalk 1`
- `ElementImmune Creep`

---

### GeoLad (`GeoLad`)
> Performs a jump attack that damages and knocks back all units in an area.

**Core Stats:** HP: `4`, Move: `2`

**Properties:** `tag: rock`, `faction: enemies`, `shield: 8`, `can_be_backstabbed: false`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** QuakeJump

**Passives:**
- `Brace 1`

---

### Headless (`NoHead`)
> Has a spin attack. Shoots a Poison shot when damaged. Blind.

**Core Stats:** HP: `7`, Move: `?`, Str: `6`, Spd: `1`

**Properties:** `tag: cat`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`

**Abilities:** **move:** `DefaultMove` | **attack:** `CatSpin` | **spells:** CatGoop

**Passives:**
- `ImmediateAbilityReaction CatGoop`
- `RandomizeAIWeightsEachTurn [`
- `]`

---

### Hemlock (`Hemlock`)
> Attacks units that move in range. Knocks back adjacent units when damaged. Heals allies.

**Core Stats:** HP: `10`, Move: `?`

**Properties:** `tag: plant`, `faction: enemies`, `flying: true`, `auto_run_priority: support`

**Abilities:** **move:** `DefaultMove` | **attack:** `HemShot` | **spells:** HemBounce, HemDeathPop, HemHeal

**Passives:**
- `Plant 1`
- `ElementImmune Creep`
- `AbilityReaction HemBounce`
- `TowerDefenseReflex attack`

---

### Infested Kitten (`Infested`)
> Its melee attack inflicts Possessed. Moves away when damaged.

**Core Stats:** HP: `7`, Move: `?`, Str: `3`, Spd: `3`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### Nettle (`Nettle`)
> Melee attacker. Each time one of its enemies casts a spell, this emits a Sparkle and gains +1 Thorns.

**Core Stats:** HP: `11`, Move: `?`

**Properties:** `tag: plant`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** ThornUp

**Passives:**
- `Plant 1`
- `ElementImmune Creep`
- `AbilityAfterEnemyCastSpell_Stackable ThornUp`

---

### Rock Head (`RockHead`)
> Has a spin attack and a dash attack with Trample. Blind.

**Core Stats:** HP: `1`, Move: `?`, Str: `6`, Spd: `1`

**Properties:** `tag: [cat rock]`, `type: cat`, `shield: 10`, `base_mana_regen: 999`, `dispersed_bonus_turns: 1`, `faction: enemies`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `CatSpin` | **spells:** SmallTrampleDash

**Passives:**
- `SpawnThingOnDeath Boulder`
- `TransformOnDeathImmediately NoHead`
- `FaceShield 0`
- `RandomizeAIWeightsEachTurn [`
- `]`

---

### Sprout (`Sprout`)
> Possesses adjacent units on its turn.

**Core Stats:** HP: `1`, Move: `?`

**Properties:** `tag: plant`, `hidden_tag: sprout`, `type: small`, `faction: enemies`, `initiative: -999`, `can_be_backstabbed: false`, `corpse_health: 0`

**Abilities:** **move:** `None` | **attack:** `SproutSpore`

**Passives:**
- `Plant 1`
- `ElementImmune Creep`

---

### Tremblo (`Tremblo`)
> Its melee attack inflicts Stun and spawns rocks. Can suck rocks towards itself and eat them to gain Brace and Shield.

**Core Stats:** HP: `4`, Move: `2`

**Properties:** `tag: rock`, `faction: enemies`, `shield: 10`, `can_be_backstabbed: false`, `corpse_health: 0`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `TrembloSmash` | **spells:** TrembloSuck, TrembloEat

---

## The End

### Cancer Cat (`CancerCat`)
> Its melee attack causes cats it hits to lose 1 [img:con] permanently and has a chance to give them cancer. Explodes after 3 turns.

**Core Stats:** HP: `8`, Move: `?`

**Properties:** `tag: [cat skeleton tumor]`, `type: cat`, `shield: 10`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `CancerMelee` | **spells:** CancerExplode

**Passives:**
- `Brace 2`

---

### Conjoined Husk (`ConjoinedHusk`)
> Its melee attack picks up cats. Creates evil copies of cats it's holding.

**Core Stats:** HP: `20`, Move: `3`

**Properties:** `tag: [tumor skeleton]`, `shield: 20`

**Abilities:** **move:** `DefaultMove` | **attack:** `CHuskBone` | **spells:** CHuskGrab, CHuskDrop, CHuskDropFail, CHuskCatShade

---

### Edema (`TumorBarrier`)
> Evolves into a Husk when its timer reaches 0. Spawns Thorny tumors when killed.

**Core Stats:** HP: `8`, Move: `0`, Spd: `1`

**Properties:** `tag: [tumor]`, `faction: enemies`, `corpse_health: 0`

**Abilities:** **move:** `None` | **attack:** `None`

---

### Floast (`Floast`)
> Has a melee throw attack and a ranged hook attack.

**Core Stats:** HP: `10`, Move: `2`

**Properties:** `tag: [tumor skeleton]`, `shield: 8`, `faction: enemies`, `flying: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `FloastPull` | **spells:** FloastThrow, FloastSpawn

---

### Fly Swarm (`FlySwarm`)
> Performs a melee attack that hits once for each fly. Each time it's damaged it loses a fly.

**Core Stats:** HP: `5`, Move: `3`, Str: `1`, Spd: `2`

**Properties:** `tag: bug`, `faction: enemies`, `corpse_health: 0`, `base_mana_regen: 999`, `flying: true`, `deathpoof_size: 1`, `can_be_backstabbed: false`, `weak_threshold: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** FormShrinkFour, FormShrinkThree, FormShrinkTwo, FormShrinkOne

**Passives:**
- `LimitDamage 1`
- `LimitHeal 1`

---

### Gasper (`Gasper`)
> Creates Poison clouds when it attacks or is damaged. Primes an explosion when killed.

**Core Stats:** HP: `17`, Move: `4`

**Properties:** `tag: blob`, `hidden_tag: poison_cloud_immune`, `faction: enemies`, `flying: true`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `SpawnGas` | **spells:** SpawnGasAOE, ToxGasBlast

**Passives:**
- `StatusImmunity Poison`

---

### Gorger (`Gorger`)
> Its melee attack consumes what it hits. Runs all the way towards its next target at the end of its turn. Trample.

**Core Stats:** HP: `60`, Move: `1`, Spd: `1`

**Properties:** `tag: [demon]`, `faction: enemies`, `size: 3x3`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `GorgerGorge` | **spells:** GorgerRun

**Passives:**
- `Trample 3`

---

### Herald (`BoyShade`)
> Melee attacker that summons shadows of itself.

**Core Stats:** HP: `30`, Move: `4`

**Properties:** `tag: [demon]`, `faction: enemies`

**Abilities:** **move:** `Teleport` | **attack:** `BasicMelee` | **spells:** ShadeDuplicate

---

### Heraldess (`GirlShade`)
> Melee attacker. Becomes scary when damaged.

**Core Stats:** HP: `33`, Move: `2`, Str: `8`

**Properties:** `tag: [demon]`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `GSClosedAttack` | **spells:** GSSuck, GSOpen, GSScream

---

### Husk (`Husk`)
> Has a multi-hit melee attack. Turns into an Edema when killed.

**Core Stats:** HP: `10`, Move: `3`, Spd: `1`

**Properties:** `tag: [tumor skeleton]`, `hidden_tag: husk`, `shield: 10`, `faction: enemies`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `HuskSwipes`

**Passives:**
- `TransformOnDeath TumorBarrier`

---

### Shade Cat (`ShadeCat`)
> Melee attacker. Teleports behind a random one of its enemies when damaged. Its backstabs cause Fear and always crit.

**Core Stats:** HP: `20`, Move: `?`

**Properties:** `tag: [cat demon]`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `SCAttack` | **spells:** SCSneakUp

**Passives:**
- `AbilityReaction SCSneakUp`

---

### Slag (`Slag`)
> Does a ranged area attack. Spawns Edemas when damaged by a melee attack and Fly Swarms when damaged by a ranged attack.

**Core Stats:** HP: `40`, Move: `2`, Spd: `1`

**Properties:** `tag: [tumor skeleton]`, `faction: enemies`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `SlagBoner` | **spells:** SlagSpawn

**Passives:**
- `Trample 3`

---

### Spiderling (`TinySpider`)
> Burrows inside its victims, inflicting Infested.

**Core Stats:** HP: `2`, Move: `4`, Str: `3`

**Properties:** `tag: bug`, `corpse_health: 0`, `faction: enemies`, `type: small`, `deathpoof_size: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `SpiderSuicideMelee`

**Passives:**
- `StatusImmunity Webbed`

---

### The Collective (`CollectiveCat`)
> Has a spin attack. Counterattacks when hit. Mimics the attacks and counters of all other cats in The Collective.

**Core Stats:** HP: `19`, Move: `?`

**Properties:** `tag: cat`, `hidden_tag: collective`, `type: cat`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `CollectiveSpin` | **spells:** CollectiveCounter

**Passives:**
- `CounterAttack CollectiveCounter`

---

## The Future

### Der Fötus (`FetusNoJar`)
> Multi-hit melee attacker. Calls an airstrike when at low health.

**Core Stats:** HP: `8`, Move: `5`

**Properties:** `tag: [humanoid fetus]`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `FurySwipes_Enemy` | **spells:** FetusAirstrikeTrigger, FetusPullBomb

---

### Doktorbot (`DoctorBot`)
> Heals its allies and gives them random buffs. Spawns Invaders. Collects Pickups.

**Core Stats:** HP: `8`, Move: `3`

**Properties:** `tag: [robot]`, `faction: enemies`, `shield: 10`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `DoctorBotHeal` | **spells:** DoctorPickup, DoctorSpawn

**Passives:**
- `Robot 1`
- `Brace 2`

---

### Fernsehbot (`TVBot`)
> Its commands restrict the actions of its enemies.

**Core Stats:** HP: `1`, Move: `3`

**Properties:** `tag: [robot]`, `auto_run_priority: support`, `faction: enemies`, `shield: 14`, `flying: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `None` | **spells:** TVOff, TVChangeObey, TVChangeStop, TVChangeDumb, TVChangeDie

**Passives:**
- `Robot 1`

---

### Fötusjar (`FetusJar`)
> Multi-hit melee attacker. Immune to Magic and Debuffs.

**Core Stats:** HP: `6`, Move: `3`

**Properties:** `tag: [humanoid fetus]`, `faction: enemies`, `shield: 8`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `FurySwipes_Enemy`

**Passives:**
- `Brace 2`
- `MagicDamageImmune 1`
- `DebuffImmunity 1`

---

### Großerbot (`TallBot`)
> Its suplex attack can Stun or Immobilize. Primes Airstrikes.

**Core Stats:** HP: `10`, Move: `2`

**Properties:** `tag: [robot]`, `faction: enemies`, `shield: 20`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `TallBotSuplex` | **spells:** TallBotRocket

**Passives:**
- `Robot 1`
- `Brace 2`

---

### Hängenbot (`HangerBot`)
> Its melee attack inflicts Short Circuit. Retracts when damaged. Spawns Invaders.

**Core Stats:** HP: `10`, Move: `3`

**Properties:** `tag: [robot]`, `faction: enemies`, `shield: 15`, `flying: true`, `banned_elite_buffs: [Protected]`

**Abilities:** **move:** `Teleport` | **attack:** `HangerBotAttack` | **spells:** HangerBotSpawn, HangerBotLeave, HangerBotReturn

**Passives:**
- `Robot 1`

---

### Katzebot (`FutureBot`)
> Melee attacker. Focuses its lowest health enemy. Will Suplex others out of the way.

**Core Stats:** HP: `6`, Move: `?`

**Properties:** `tag: cat`, `type: cat`, `shield: 12`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `FutureBotPunch` | **spells:** FutureBotPunchAggro, FutureBotSuplex

**Passives:**
- `Brace 2`
- `AggroTargetIsLowestHealthEnemyTillItDies 1`
- `Robot 1`

---

### Krughead (`JarHead`)
> Melee attacker. Gives its allies extra turns. Immune to Magic and Debuffs.

**Core Stats:** HP: `6`, Move: `5`, Str: `3`

**Properties:** `tag: [humanoid]`, `faction: enemies`, `shield: 12`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** JarHeadOrder

**Passives:**
- `Brace 2`
- `MagicDamageImmune 1`
- `DebuffImmunity 1`
- `CounterAttack attack`

---

### Schpidenbot (`Invader`)
> Melee attacker that inflicts Poison.

**Core Stats:** HP: `5`, Move: `4`, Str: `3`

**Properties:** `tag: [robot bug]`, `corpse_health: 0`, `faction: enemies`, `type: small`, `deathpoof_size: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `InvaderAttack`

**Passives:**
- `Brace 2`
- `StatusImmunity Webbed`
- `Robot 1`
- `DeathRattle InvaderExplode`

---

### Schutzbot (`SoldierBot`)
> Ranged attacker with limited ammo. Shoots at enemies that damage its allies. Expends the rest of its ammo and reloads at the end of its turn. Backflips one attack per turn.

**Core Stats:** HP: `8`, Move: `3`, Spd: `2`

**Properties:** `tag: [robot]`, `faction: enemies`, `shield: 20`

**Abilities:** **move:** `DefaultMove` | **attack:** `SZBShoot` | **spells:** SZBReload, SZBBackflipDodge

**Passives:**
- `Ammo 3`
- `Robot 1`

---

### Übercat (`FatCat`)
> Has a leap attack that does knockback in an area. Reflects Projectiles. Uncapped HP.

**Core Stats:** HP: `18`, Move: `2`

**Properties:** `tag: [cat blob]`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`, `can_eat_food: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `FatCatBellyFlop`

**Passives:**
- `YOffset -.18`
- `Trample 3`
- `UncappedHP 1`
- `TagGreed food`

---

### Überman (`FatMan`)
> Melee attacker with Knockback. Reflects projectiles. Units that contact it get knocked back. Trample.

**Core Stats:** HP: `20`, Move: `1`, Con: `10`, Int: `3`, Spd: `1`, Cha: `2`

**Properties:** `tag: [humanoid blob]`, `faction: enemies`, `corpse_health: 5`, `dispersed_bonus_turns: 1`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `FatManLunge`

**Passives:**
- `Trample 3`
- `RandomizeAIWeightsEachTurn [`
- `]`

---

### Überwoman (`FatWoman`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

## The Infinite

### Angelic Cat (`AngelicCat`)
> Has a Holy Wind area attack. Gains 1 [img:divineshield] at the end of its turn. Immune to Holy. Gains All Stats Up when struck with Holy Element.

**Core Stats:** HP: `30`, Move: `5`, Str: `6`

**Properties:** `tag: [cat angel]`, `type: cat`, `divine_shield: 1`, `faction: enemies`

**Abilities:** **move:** `BasicJump` | **attack:** `AngelcatWind`

**Passives:**
- `Angel 1`
- `PrioritizeFarAwayTargets 1`

---

### Angelic Kitten (`AngelicKitten`)
> Attracts units. Dooms what kills it. Immune to Holy. Gains All Stats Up when struck with Holy Element.

**Core Stats:** HP: `3`, Move: `3`

**Properties:** `tag: [cat angel]`, `faction: enemies`, `flying: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `CherubMelee` | **spells:** CherubAttract, CherubDoom

**Passives:**
- `Angel 1`

---

### Cherubim (`Cherubim`)
> Gives its allies [img:divineshield]. Primes an area attack when damaged. Immune to Holy. Gains All Stats Up when struck with Holy Element.

**Core Stats:** HP: `20`, Move: `2`

**Properties:** `tag: [bird angel]`, `faction: enemies`, `divine_shield: 1`, `flying: true`, `dispersed_bonus_turns: 1`, `corpse_health: 0`, `banned_elite_buffs: [Protected]`

**Abilities:** **move:** `DefaultMove` | **attack:** `CherubimHeal` | **spells:** CherubimLeave, CherubimReturn

**Passives:**
- `Bird CookedChickenLeg`
- `Angel 1`

---

### Gatekeeper (`Gatekeeper`)
> Goes after the cat with the lowest max health. Sucks the soul out of its target, instantly killing it and permanently lowering their [img:con] by 2. Summons Skeletons. Undead.

**Core Stats:** HP: `10`, Move: `2`, Spd: `2`

**Properties:** `tag: [zombie]`, `faction: enemies`, `shield: 20`

**Abilities:** **move:** `DefaultMove` | **attack:** `GKSuck` | **spells:** GKLeap, GKSpawn

**Passives:**
- `Undead 1`
- `AggroTargetIsLowestMaxHealthCat 1`

---

### Seraphim (`Seraphim`)
> Has a diagonal Holy attack. Can revive its downed allies. Units that contact or attack this get knocked back 5 tiles. Immune to Holy. Gains All Stats Up when struck with Holy Element.

**Core Stats:** HP: `15`, Move: `2`

**Properties:** `tag: [humanoid angel]`, `faction: enemies`, `divine_shield: 4`, `flying: true`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `SeraphimX` | **spells:** SeraphimRevive

**Passives:**
- `Angel 1`

---

## The Lab

### Cop Bot (`CopBot`)
> Melee attacker. Will shoot at enemies who damage its allies.

**Core Stats:** HP: `2`, Move: `3`

**Properties:** `tag: [robot]`, `faction: enemies`, `shield: 16`, `auto_run_priority: support`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** CBShoot_ZodiacStyle, CBReload

**Passives:**
- `Ammo 1`
- `AggroTargetIsLastEnemyThatDealtDamage 1`
- `FaceShield 0`
- `Robot 1`
- `Trample 3`

---

### Dr. Cat (`Drcat`)
> Will randomly cast one of 6 spells.

**Core Stats:** HP: `10`, Move: `?`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### Dr. Ditto (`DrDitto`)
> Fires explosive rockets that hit a random tile in an area. Will Fear units near it at the start of its turn. Its body revives at the end of the round.

**Core Stats:** HP: `9`, Move: `2`

**Properties:** `tag: [humanoid]`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `DrDRockets` | **spells:** DrDGlare

---

### Gamete (`Gamete`)
> Spawns random units.

**Core Stats:** HP: `8`, Move: `4`

**Properties:** `tag: blob`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `None` | **spells:** GametePop

---

### Half-Dog (`NubsCat`)
> Has a leap attack with Knockback. Leap attacks in the direction it's facing when damaged.

**Core Stats:** HP: `17`, Move: `1`, Dex: `8`

**Properties:** `tag: [dog cat]`, `faction: enemies`, `corpse_health: 0`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `NubsJump` | **spells:** NubsCatJumpReaction

---

### Half-Rat (`RatCat`)
> Does a chaining dash attack with a chance to spread diseases.

**Core Stats:** HP: `10`, Move: `1`

**Properties:** `tag: [rat cat]`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `ChainDash`

---

### Infested (`Mangy3`)
> Its ranged attack has a chance to break equipment and attach a parasite. Spawns a Gamete when killed.

**Core Stats:** HP: `10`, Move: `?`, Str: `4`, Spd: `3`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `ParasiteShot`

**Passives:**
- `SpawnThingOnDeath Gamete`

---

### Mega Mutant (`MegaMutant`)
> Melee attacks adjacent units with Knockback 10 at the start of its turn. Performs a straight, long-range quake attack. Can grab and instakill units if it can reach them. Gains +99 Brace until its next turn when damaged.

**Core Stats:** HP: `26`, Move: `1`

**Properties:** `tag: [humanoid cat]`, `faction: enemies`, `dispersed_bonus_turns: 1`, `size: 2x2`, `move_block: everything_even_when_dead`, `banned_elite_buffs: [Protected]`

**Abilities:** **move:** `DefaultMove` | **attack:** `MM_Slap` | **spells:** MM_Quake, MM_Guard, MM_Unguard, MM_Grab

**Passives:**
- `Trample 3`

---

### Spun Cat (`Needlecat`)
> Has a random class basic attack that inflicts a randomly assigned debuff.

**Core Stats:** HP: `10`, Move: `?`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

## The Moon

### Astronaut (`Astro`)
> Its melee attack has a high chance to inflict Stun.

**Core Stats:** HP: `8`, Move: `1`

**Properties:** `tag: cat`, `type: cat`, `shield: 5`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `BasicJump` | **attack:** `BasicMelee`

---

### B-Prober (`GreenProber`)
> Melee attacker. If it can melee attack a cat from behind it will inflict Charm. This Charm lasts until the Charmed cat takes damage.

**Core Stats:** HP: `10`, Move: `3`

**Properties:** `tag: [alien]`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** GP_Probe

---

### Big Asteroid (`BigAsteroid`)
> Its attack spawns a boulder. Gets knocked back with Chain Knockback when hit. Can only recieve 1 damage at a time. Immune to status effects.

**Core Stats:** HP: `5`, Move: `2`

**Properties:** `tag: rock`, `faction: enemies`, `shield: 7`, `flying: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BigAsteroidBarrage`

**Passives:**
- `LimitDamage 1`
- `LimitHeal 0`
- `StripStatuses 1`

---

### G-Alien (`GreyAlien`)
> Its ranged attack has Knockback. Primes a Counterspell at the end of its turn. Is powered up when Counterspell is primed.

**Core Stats:** HP: `10`, Move: `3`

**Properties:** `tag: [alien]`, `faction: enemies`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `GA_Telekinesis` | **spells:** GA_Counterspell, GA_Megablast, GA_Suggest, GA_PrimeExplode

---

### Megasaucer (`BigUFO`)
> Performs a random action on its turn. Has a dash attack that inflicts Stun. Has a charge up laser attack that instakills. Has the ability to summon B-Probers. Explodes when killed.

**Core Stats:** HP: `6`, Move: `2`

**Properties:** `tag: [alien robot]`, `faction: enemies`, `flying: true`, `shield: 10`, `divine_shield: 3`, `corpse_health: 0`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `UFO_Dash` | **spells:** UFO_Megalaser, UFO_Summon, UFO_BigShield

**Passives:**
- `Trample 3`
- `Robot 1`
- `DeathRattle UFO_BigExplode`
- `LoopingSoundWhileAlive BigUFO_ambient_looping`

---

### Moon Worm (`MoonWorm`)
> Lobs shots at all of its enemies within range. Gains +1 Brace when damaged.

**Core Stats:** HP: `12`, Move: `3`

**Properties:** `tag: worm`, `type: small`, `faction: enemies`

**Abilities:** **move:** `Teleport` | **attack:** `MoonWormShot` | **spells:** MoonWormCurl

**Passives:**
- `AbilityReaction MoonWormCurl`

---

### Rover (`Rover`)
> Has a chaining dash attack.

**Core Stats:** HP: `6`, Move: `2`

**Properties:** `tag: [robot cat]`, `type: cat`, `shield: 8`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `RoverDash`

**Passives:**
- `Brace 2`

---

### Saucie (`SmallUFO`)
> Fires energy shots in an X shape. Can inflict Marked on enemies or gain [img:divineshield]. Explodes when killed.

**Core Stats:** HP: `6`, Move: `1`

**Properties:** `tag: [alien robot]`, `faction: enemies`, `shield: 6`, `flying: true`, `dispersed_bonus_turns: 2`

**Abilities:** **move:** `DefaultMove` | **attack:** `UFO_CrossLasers` | **spells:** UFO_Detect, UFO_Shield

**Passives:**
- `Robot 1`

---

### Small Asteroid (`SmallAsteroid`)
> Its attack shoots rocks at random tiles in an area. Gets knocked back with Chain Knockback when hit. Can only recieve 1 damage at a time. Immune to status effects.

**Core Stats:** HP: `1`, Move: `3`

**Properties:** `tag: rock`, `faction: enemies`, `shield: 3`, `flying: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `SmallAsteroidBarrage`

**Passives:**
- `LimitDamage 1`
- `LimitHeal 0`
- `StripStatuses 1`

---

### Waggle (`Waggle`)
> Melee attacker. Will turn enemy familiars and low health allies into Waggles!

**Core Stats:** HP: `7`, Move: `3`

**Properties:** `tag: [blob]`, `faction: enemies`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** WaggleClone

---

### Y-Blaster (`YellowBlaster`)
> Shoots at units that cross its path. Gains +1 Damage at the end of its turn. Moves away when in danger.

**Core Stats:** HP: `12`, Move: `3`

**Properties:** `tag: [alien]`, `faction: enemies`, `auto_run_priority: support`

**Abilities:** **move:** `DefaultMove` | **attack:** `YA_Laser` | **spells:** YA_Charge, YA_Jetpack

**Passives:**
- `SupportFormChangeInsteadOfRun Attacker`

---

## The Rift

### Butch & Tink (`ButchTinkBoris`)
> Moves 1 tile toward whatever damages them. Will dash on their last turn. Trample.

**Core Stats:** HP: `160`, Move: `2`

**Properties:** `tag: [humanoid blob]`, `faction: enemies`, `dispersed_bonus_turns: 3`, `mana_regen: 999`, `mana: 100`, `size: 2x2`, `move_block: everything_even_when_dead`, `last_turn_is_main_turn: true`, `two_fronts: true`, `two_fronts_switch: true`, `can_be_backstabbed: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `None` | **spells:** TrampleDash, MoveOne

**Passives:**
- `Trample 3`
- `MoveTowardsDamageSource MoveOne`

---

### Chaos Stacy (`ChaosStacy`)
> Its melee attack inflicts Scrambled. Reflects projectiles and knocks back units that contact.

**Core Stats:** HP: `26`, Move: `4`, Spd: `3`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `ChaosStacyAttack`

**Passives:**
- `ReflectProjectiles 1`

---

### Dr. Beanies (`BeaniesRat`)
> Tosses bombs that explode at the end of the round.

**Core Stats:** HP: `67`, Move: `5`

**Properties:** `tag: humanoid`, `faction: enemies`, `mana_regen: 999`, `mana: 100`, `initiative: -100`, `dispersed_bonus_turns: 2`, `dispersed_bonus_turns_consider_initiative: false`, `dispersed_bonus_turns_before_cats: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `None` | **spells:** SpawnBomb, BombRatTurtle, RockToss_BomberRat

---

### Frank (`FrankFetus`)
> Will suck units in, then spit them out. Becomes Frank's Bean when killed.

**Core Stats:** HP: `12`, Move: `4`, Spd: `2`

**Properties:** `tag: humanoid`, `faction: enemies`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `KirbySuck`

**Passives:**
- `SpawnOnDeath FrankPinky`

---

### Frank's Bean (`FrankPinky`)
> Melee attacker. Moves randomly.

**Core Stats:** HP: `8`, Move: `2`

**Properties:** `tag: tumor`, `faction: enemies`, `type: small`, `dispersed_bonus_turns: 2`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `Brace 5`

---

### Jack (`JackCat`)
> Protects his allies.

**Core Stats:** HP: `16`, Move: `?`, Str: `3`

**Properties:** `tag: [cat humanoid]`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `JackAttack` | **spells:** JackShield

---

### Tracy (`TracyFetus`)
> Performs a spin attack. Will try to counterattack with her left arm when hit.

**Core Stats:** HP: `30`, Move: `4`, Spd: `3`

**Properties:** `tag: humanoid`, `faction: enemies`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `MegafetusSpin` | **spells:** MegafetusMelee

**Passives:**
- `Trample 3`
- `CounterAttack MegafetusMelee`

---

## Throbbing Domain

### Burfer Maggot (`TumorousMaggot`)
> Its attack surrounds units with Thorny lumps.

**Core Stats:** HP: `14`, Move: `3`

**Properties:** `tag: worm`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `PrisonShot`

---

### Chargey Maggot (`ChargeyMaggot`)
> Its dash attack has trample.

**Core Stats:** HP: `9`, Move: `2`

**Properties:** `tag: worm`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `SmallTrampleDash`

---

### Clot (`Clot`)
> Has a chance to become a Stem Cat at the end of its turn.

**Core Stats:** HP: `1`, Move: `4`, Str: `2`, Spd: `2`

**Properties:** `tag: blob`, `faction: enemies`, `inherit_faction: true`, `type: small`, `corpse_health: 0`, `deathpoof_size: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `None` | **spells:** ClotEvolve, ClotFailEvolve

---

### Diggy Maggot (`SwappyMaggot`)
> Its melee attack has a chance to Stun. Swaps places with a unit to move.

**Core Stats:** HP: `8`, Move: `20`, Str: `7`

**Properties:** `tag: worm`, `faction: enemies`, `corpse_health: 0`

**Abilities:** **move:** `SwapPositions` | **attack:** `Lick`

---

### Flesh Lad (`FleshLad`)
> Attacks as many times as it can, then uppercuts and inflicts Bruise. Gains an extra attack per turn each time it takes damage. Gains Speed at the end of its turn.

**Core Stats:** HP: `23`, Move: `2`, Spd: `3`

**Properties:** `tag: blob`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `FleshLadDoublehit` | **spells:** FleshLadUppercut

---

### Fleshy Mind (`FleshyMind`)
> Has a ranged attack that inflicts Muted. Inflicts Confusion on units that attack it.

**Core Stats:** HP: `23`, Move: `2`

**Properties:** `tag: blob`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `FleshyMindDisable` | **spells:** FleshyMindConfusion

**Passives:**
- `CounterAttack FleshyMindConfusion`

---

### Maggot (`Maggot`)
> Melee attacker.

**Core Stats:** HP: `1`, Move: `2`, Str: `2`, Dex: `1`

**Properties:** `tag: worm`, `corpse_health: 0`, `faction: enemies`, `type: small`, `initiative: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `CanMutateTo [TumorousMaggot, ChargeyMaggot, SwappyMaggot]`

---

### Meat Slime (`MeatSlime`)
> Splits into Clots on death.

**Core Stats:** HP: `16`, Move: `3`, Dex: `3`, Con: `3`, Int: `3`, Spd: `3`, Cha: `3`

**Properties:** `tag: blob`, `faction: enemies`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `Divide4OnDeath Clot`

---

### Skinned (`Skinned`)
> Does 3 dash attacks in a row with Knockback.

**Core Stats:** HP: `30`, Move: `?`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `SkinnedTripleDash`

---

### Stem Cat (`StemCat`)
> Melee attacker. Spawns a Clot when it takes damage.

**Core Stats:** HP: `13`, Move: `3`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `HealthRegenUp 2`

---

### Throbbing Servant (`Parasiter`)
> Ranged attacker that has a chance to destroy equipment and attach a parasite. Spawns Maggots.

**Core Stats:** HP: `15`, Move: `2`

**Properties:** `tag: humanoid`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `ParasiterShoot` | **spells:** ParasiterSpawn

---

### Throbbing Turret (`ThrobbingTurret`)
> Ranged area attack that inflicts Bleed. Spawns Clots if nothing is in range.

**Core Stats:** HP: `10`, Move: `0`

**Properties:** `tag: blob`, `faction: enemies`, `corpse_health: 0`, `can_be_backstabbed: false`

**Abilities:** **move:** `None` | **attack:** `ThrobShot` | **spells:** SpawnClot, ThrobShot_Reaction

**Passives:**
- `MiniVolcanoReaction ThrobShot_Reaction`

---

## Uncategorized / Internal

### Abandoned One (`AstroZombie`)
> Its melee attacks inflict random injuries.

**Core Stats:** HP: `40`, Move: `2`

**Properties:** `tag: [humanoid zombie]`, `faction: enemies`, `type: boss`, `disperse_main_turns: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `AZ_BreakNeck` | **spells:** AZ_Jump, AZ_BreakLeg, AZ_BreakArm, AZ_LoseHead

**Passives:**
- `Undead 1`

---

### Abandoned One (`AstroZombieHead`)
> Its melee attack inflicts Burn. Its scream will inflict Fear.

**Core Stats:** HP: `20`, Move: `3`

**Properties:** `tag: [humanoid zombie]`, `faction: enemies`, `type: boss`, `corpse_health: 0`, `flying: true`, `disperse_main_turns: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** AZ_Scream

**Passives:**
- `Undead 1`
- `InnateElement Fire`
- `ElementImmune Fire`
- `StatusImmunity [Burn]`
- `AddElementsToBasicAttack Fire`

---

### Alice (`PsychicCat`)
> Has a psychic choke attack that inflicts Bruise on a unit in her line of sight. Knocks back any enemy that casts a spell.

**Core Stats:** HP: `66`, Move: `?`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicPsychicPull` | **spells:** PsychicChoke_Enemy, PsychicCatBackflip

**Passives:**
- `CounterAttackAfterEnemyCastSpell Telekinesis`

---

### AnimalEgg2 (`AnimalEgg2`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### Arthur (`JesterCat`)
> Who knows what he will do!?

**Core Stats:** HP: `75`, Move: `?`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 2`, `base_crit_chance: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** Metronome_Enemy

**Passives:**
- `RandomizeAIWeightsEachTurn [`
- `]`

---

### Baby Squirrel (`BabySquirrel`)
> *(No Description)*

**Core Stats:** HP: `1`, Move: `6`, Str: `1`, Dex: `1`, Con: `1`, Int: `1`, Spd: `9`, Cha: `1`

**Properties:** `tag: [animal squirrel]`, `type: small`, `faction: allies`, `inherit_faction: true`, `weak_threshold: 0`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **can_get_bonus:** `true`

---

### Bear2 (`Bear2`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Abilities:** **attack:** `BearFurySwipes`

---

### Big Bird (`BirdLarge`)
> *(No Description)*

**Core Stats:** HP: `16`, Move: `3`

**Passives:**
- `RunInXTurns 3`

---

### Big Slime (`BigSlime`)
> Melee attacker. Splits into 4 medium Slimes on death.

**Core Stats:** HP: `64`, Move: `4`, Str: `10`, Dex: `6`, Con: `6`, Int: `6`, Spd: `6`, Cha: `6`

**Properties:** `tag: blob`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`, `corpse_health: 0`, `size: 2x2`, `move_block: everything_even_when_dead`, `banned_elite_buffs: [Shielded1 Shielded2 Shielded3 Shielded4]`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicBigMelee`

**Passives:**
- `Trample 3`
- `Divide4OnDeath MedSlime`

---

### Bird (`BirdBase`)
> Whoever kills this gets All Stats Up and finds a bonus item!

**Core Stats:** HP: `2`, Move: `3`

**Properties:** `tag: animal`, `hidden_tag: [bird bonusbird]`, `faction: birds`, `kill_required: false`, `initiative: -999`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** BirdFly

**Passives:**
- `CounterAttack attack`
- `Bird CookedChickenLeg`
- `TrackAmountKilledByPlayer BonusBirdsKilled`

---

### Bird (`Bird`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `can_be_champion: false`

---

### Bomb Fly (`BombFly`)
> *(No Description)*

**Core Stats:** HP: `6`, Move: `3`, Str: `3`

**Properties:** `tag: [bug bomb]`, `faction: enemies`, `flying: true`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `DeathRattle BombFlyExplode`

---

### Boris (`Fatso`)
> Moves 1 tile towards whatever damages it. Will Dash on its last turn. Trample.

**Core Stats:** HP: `200`, Move: `2`

**Properties:** `tag: [cat blob]`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 3`, `mana_regen: 999`, `mana: 100`, `size: 2x2`, `move_block: everything_even_when_dead`, `last_turn_is_main_turn: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `None` | **spells:** TrampleDash, MoveOne

**Passives:**
- `Trample 3`
- `MoveTowardsDamageSource MoveOne`

---

### Bumblefoot (`Bumblefoot`)
> Its leap attack will turn it upside down. When upside down it performs an area attack. Will eat any bodies in play, and living things if there are no bodies left.

**Core Stats:** HP: `150`, Move: `5`

**Properties:** `tag: rat`, `faction: enemies`, `type: boss`, `mana_regen: 999`, `mana: 100`, `dispersed_bonus_turns: 2`, `size: 2x2`, `move_block: everything_even_when_dead`, `knockback_immune: true`, `elements: [`

**Abilities:** **move:** `None` | **attack:** `None` | **spells:** BumblefootLeap, BumblefootEatCorpse, BumblefootAttemptEatCat, BumblefootEatCat, BumblefootBoneShot, BumbleButt

**Passives:**
- `Trample 3`

---

### Bunga's Champion (`BungaWarrior1`)
> One of Lord Bunga's top guys!

**Core Stats:** HP: `100`, Move: `?`

**Properties:** `tag: humanoid`, `hidden_tag: bungawarrior`, `faction: cavemen`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** WereManPounce, WereManTransformSwipe, CaveWomanGrab, CaveWomanDrop, CaveWomanBirth, CaveWomanThrow, CaveWomanDropTransform, CaveManPickupSpear, CaveManChestPound, CaveManTransform, CaveManSpearRun, CaveBabyGrow, CaveBabyFoodMove

---

### BungaWarrior2 (`BungaWarrior2`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### C-1000 (`Terminator2`)
> Primary objective: Destroy all cats, again!

**Core Stats:** HP: `500`, Move: `1`

**Properties:** `tag: [cat robot]`, `type: boss`, `faction: enemies`, `allow_passive_spelltransforming: true`, `evenly_dispersed_bonus_turns: 3`, `last_turn_is_main_turn: true`, `corpse_health: 0`, `allow_replacebrain: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `T2SpearMelee` | **spells:** DoNothing, DoNothing, DoNothing, DoNothing, DoNothing, T2Clone, T2UnClone, T2GoopRun

**Passives:**
- `Robot 1`
- `PrioritizePlayerCats 1`
- `AggroTargetIsCurrentTurn 1`

---

### C-800 (`Terminator1`)
> Primary objective: Destroy all cats.

**Core Stats:** HP: `250`, Move: `?`, Str: `10`, Dex: `8`, Con: `10`, Int: `6`, Spd: `6`, Cha: `4`

**Properties:** `tag: [cat robot]`, `type: boss`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 999`, `evenly_dispersed_bonus_turns: 2`, `first_turn_is_main_turn: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** T1Pummel, T1SwapWeapon, T1ThrowGrenadeA, T1ThrowGrenadeB, MoveOne, T1ChokeReaction

**Passives:**
- `Robot 1`
- `Brace 50`
- `Trample 3`
- `AggroTargetIsCurrentTurn 1`
- `PrioritizePlayerCats 1`

---

### Can Creeper (`CanCreeper`)
> Shoots diagonally or dashes forward leaving a Fly behind. Can only be damaged from the front. Spawns creep.

**Core Stats:** HP: `40`, Move: `3`

**Properties:** `tag: blob`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`, `corpse_health: 0`, `mana_regen: 999`, `mana: 100`, `always_triggers_traps: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `DoubleDiagonalCreepshot` | **spells:** CanCreeperSlide

**Passives:**
- `TileTrail CreepTile`
- `CanShield 1`
- `IgnoreTiles 1`
- `ChangeTileOnPop CreepTile`
- `TransformOnDeath CanCreeperOut`
- `ElementImmune Creep`

---

### Can Creeper (`CanCreeperOut`)
> Ranged attacker. Must be in creep to attack.

**Core Stats:** HP: `20`, Move: `?`, Spd: `8`

**Properties:** `tag: blob`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`, `corpse_health: 1`, `mana_regen: 999`, `mana: 100`

**Abilities:** **move:** `Swim` | **attack:** `ShortCreepshot` | **spells:** MoveOne

**Passives:**
- `GroundFlopper MoveOne`
- `WaterWalk 1`
- `ElementImmune Creep`

---

### CatHuman (`CatHuman`)
> Spawns Kittens. Its melee attack inflicts injuries. Can howl to Immobilize units.

**Core Stats:** HP: `18`, Move: `2`

**Properties:** `tag: [humanoid cat]`, `faction: enemies`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `CHToss` | **spells:** CHCry, CHSpawn

---

### CaveBaby (`CaveBaby`)
> *(No Description)*

**Core Stats:** HP: `20`, Move: `?`

**Properties:** `initial_health: 10`

---

### CaveMan (`CaveMan`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### CaveManNoSpear (`CaveManNoSpear`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### CaveWoman (`CaveWoman`)
> *(No Description)*

**Core Stats:** HP: `30`, Move: `?`

---

### Caveman (`CavePerson`)
> Has a multi-hit melee attack. Hates Cats!

**Core Stats:** HP: `32`, Move: `?`

**Properties:** `tag: humanoid`, `faction: cavemen`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** WereManPounce, WereManTransformSwipe, CaveWomanGrab, CaveWomanDrop, CaveWomanBirth, CaveWomanThrow, CaveWomanDropTransform, CaveManPickupSpear, CaveManChestPound, CaveManTransform, CaveManSpearRun, CaveBabyGrow, CaveBabyFoodMove

---

### Cerberubs (`Cerberubs`)
> Shoots Lava from its necks when damaged. Becomes enraged when hit from behind. Immune to Fire.

**Core Stats:** HP: `200`, Move: `2`

**Properties:** `tag: [dog demon]`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`, `mana_regen: 999`, `mana: 100`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `CerberubsJump` | **spells:** CerberubsShotgunReaction, CerberubsStraightReaction, CerberubsThrow, CerberubsBarrage, CerberubsCalm

**Passives:**
- `Trample 3`
- `ImmediateAbilityReaction CerberubsStraightReaction`
- `ElementImmune Fire`

---

### Chan Hung (`MonkCat`)
> Uses his own actions every time one of his enemies uses an action. Has a different response for move, attack/weapon, and spell/trinket.

**Core Stats:** HP: `65`, Move: `3`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `initiative: -20`

**Abilities:** **move:** `DefaultMove` | **attack:** `MCMelee` | **spells:** MCHadouken, MCKineticCharge

**Passives:**
- `AggroTargetIsCurrentTurn 1`
- `PrioritizeAggroTarget 1`
- `Brace 1`

---

### Cherub (`Cherub`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Passives:**
- `Angel 1`

---

### Cherub_FinalBoss (`Cherub_FinalBoss`)
> Whoever kills this gets All Stats Up!

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `hidden_tag: angeljunk`

---

### Chubs (`Chubs`)
> Blind. Shoots a Poison shot when damaged. Does a melee spin attack.

**Core Stats:** HP: `140`, Move: `3`, Dex: `8`

**Properties:** `tag: dog`, `faction: enemies`, `type: boss`, `mana_regen: 999`, `mana: 100`, `evenly_dispersed_bonus_turns: 1`, `disperse_main_turns: true`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `ChubsSpin` | **spells:** ChubsGoop, ChubsRage

**Passives:**
- `Buddy Nubs`
- `ImmediateAbilityReaction ChubsGoop`
- `AbilityWhenBuddyDies ChubsRage`

---

### Chupacabra (`Chupacabra`)
> More like chupa gato! Am I right?

**Core Stats:** HP: `77`, Move: `4`, Str: `3`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 2`, `dispersed_bonus_turns_consider_initiative: false`, `scale: 1.3`, `mana_regen: 999`, `mana: 100`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** WolfLeap, SharkDash

---

### CopBot_Uprising (`CopBot_Uprising`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `auto_run_priority: default`

---

### Crater Maker (`AlienBeast`)
> Changes its primed attack whenever it takes damage. Shoots from its sides when damaged.

**Core Stats:** HP: `280`, Move: `2`, Str: `9`, Dex: `9`, Con: `9`, Int: `9`, Spd: `9`, Cha: `9`

**Properties:** `tag: alien`, `faction: enemies`, `type: boss`, `size: 3x3`, `move_block: everything_even_when_dead`, `round_start_bonus_turns: 1`, `initiative: -999`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicBigMelee` | **spells:** AlienBeastScream, AlienBeastEat, AlienBeastPuke, AlienBeastRampage, AlienBeastGoop, AlienBeastOpenEyes, AlienBeastMoveOne

**Passives:**
- `Trample 3`
- `AlienBeastEyeStalks 3`
- `AlienBeastDangerZones [AlienBeastScream AlienBeastEat AlienBeastPuke AlienBeastRampage]`

---

### Crow2 (`Crow2`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Abilities:** **spells:** CrowFlutter2, CrowFlap2

---

### Crow3 (`Crow3`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Abilities:** **spells:** CrowFlutter3, CrowFlap3

---

### Cultist (`Cultist`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `tag: humanoid`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** BBPickupCrown, BBSpin, BBCut, BBPullBomb, BBTransformMutant, BBTransformZealot, BBToss, BBBless

---

### CultistBishop (`CultistBishop`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `hint_no_corpse: true`

**Passives:**
- `DivineShield 2`
- `KineticSpikes 1`

---

### CultistMutant (`CultistMutant`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `hint_no_corpse: true`

**Passives:**
- `Brace 2`

---

### CultistWasher (`CultistWasher`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### CultistZealot (`CultistZealot`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### Cutter (`Cutter`)
> *(No Description)*

**Core Stats:** HP: `50`, Move: `5`, Str: `2`

**Properties:** `faction: enemies`, `round_end_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** CutterCut

---

### D'Claude (`Dclaude`)
> 

**Core Stats:** HP: `75`, Move: `5`, Str: `3`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`, `dispersed_bonus_turns_consider_initiative: false`, `mana_regen: 999`, `mana: 100`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee_Fighter` | **spells:** Dclaude_Declaw, QueenHippoAttack

**Passives:**
- `CounterAttack attack`
- `RandomizeAIWeightsEachTurn [`
- `]`

---

### Dack (`ThiefCat`)
> His ranged attacks scatter held coins. Has a melee attack that inflicts Poison. Seeks coin pickups. Gains a Backflip every time he collects a coin.

**Core Stats:** HP: `60`, Move: `3`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 3`, `mana_regen: 999`, `mana: 100`, `can_collect_coins: true`, `held_coins: 5`

**Abilities:** **move:** `DefaultMove` | **attack:** `THC_KnockCoinsRanged` | **spells:** THC_PoisonSwat, THC_Roll, THC_CoinRoll

**Passives:**
- `EraseSpawnCoins 1`
- `AwardCoinsOnDeath 10`

---

### DeadPinky (`DeadPinky`)
> This poor little guy didn't stand a chance!

**Core Stats:** HP: `?`, Move: `?`

**Passives:**
- `StartDead 100%`

---

### Debug_MegaGuppyPhase3 (`Debug_MegaGuppyPhase3`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `takes_main_turn: false`, `round_start_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** DbgBackgroundTransitionTest

**Passives:**
- `StartOffMap 1`

---

### Dove (`Dove`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### Dr. Mangler (`DrMangler`)
> Controls the Monster.

**Core Stats:** HP: `185`, Move: `5`

**Properties:** `tag: [humanoid robot]`, `faction: enemies`, `type: boss`, `initiative: -10`, `evenly_dispersed_bonus_turns: 1`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `ManglerCommand` | **spells:** ManglerFumbleEven, ManglerFumbleOdd, ManglerEnrage, ManglerThrowRemote, ManglerSpin

**Passives:**
- `Robot 1`
- `Buddy ManglersMonster`
- `AbilityWhenBuddyDies ManglerEnrage`

---

### Draven (`DruidCat`)
> Heals and buffs his crows. Enters Squirrel Form once his crows die.

**Core Stats:** HP: `70`, Move: `?`, Str: `3`

**Properties:** `tag: cat`, `hidden_tag: dc_cat`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `DruidCatBasic` | **spells:** DCSquirrelForm, DCBirthSquirrel

---

### Draven's Crow (`DruidCrow`)
> Melee attacker than can also use a wind attack with Knockback. Will move and attack enemies that attack Draven.

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `tag: [animal crow]`, `hidden_tag: dc_crow`, `faction: enemies`, `base_movement: 4`, `mana_matters: false`, `corpse_health: 1`, `flying: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** DCAeroblast

**Passives:**
- `Bird CookedChickenLeg`

---

### Dreadnoughtus (`MegaDinoLeg`)
> Stomps towards units that damage it. Lifts when it takes enough damage.

**Core Stats:** HP: `55`, Move: `2`

**Properties:** `tag: [dinosaur]`, `hidden_tag: [megadino megadinoleg]`, `faction: enemies`, `type: boss`, `size: 2x2`, `move_block: everything_even_when_dead`, `corpse_health: indestructible`, `kill_required: false`, `disperse_main_turns: true`, `lock_orientation: [-1 0]`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `MD_Walk` | **attack:** `MD_Stomp` | **spells:** MD_Lift, MD_Kick, MD_LegLeave, MD_LegReturn

**Passives:**
- `Trample 3`

---

### Dreadnoughtus (`MegaDinoHead`)
> Now's your opportunity! Get him before he gets back up!

**Core Stats:** HP: `600`, Move: `0`

**Properties:** `tag: [dinosaur]`, `hidden_tag: megadino`, `faction: enemies`, `type: boss`, `size: 3x3`, `move_block: everything_even_when_dead`, `knockback_immune: true`, `initiative: -100`, `corpse_health: indestructible`, `lock_orientation: [-1 0]`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `None` | **attack:** `None` | **spells:** MD_HeadLeave, MD_HeadDrop, MD_Poop

**Passives:**
- `Trample 3`
- `StartOffMap 1`

---

### Dummy (`Dummy`)
> *(No Description)*

**Core Stats:** HP: `100`, Move: `?`

**Properties:** `tag: cat`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`, `exclude_from_hallucinate: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### Dust Devil (`DustDevil`)
> *(No Description)*

**Core Stats:** HP: `100`, Move: `1`, Str: `4`

**Properties:** `tag: demon`, `faction: enemies`, `type: boss`, `initiative: -999`, `dispersed_bonus_turns: 2`, `mana_regen: 999`, `mana: 100`, `elements: [`

**Abilities:** **move:** `DustMove` | **attack:** `DustMelee` | **spells:** DustDash, DustTeleport

---

### Dybbuk (`Dybbuk`)
> Avoids your attacks! Will get revenge on the cat who kills it!

**Core Stats:** HP: `85`, Move: `3`

**Properties:** `tag: [cat ghost]`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 2`, `corpse_health: 0`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `DybbukLick` | **spells:** DybbukWisps, DybbukReanimate, DybbukEscape, DybbukPossess, DybbukReturn, DybbukRePossess

**Passives:**
- `Dybbuk1HPTracker 1`
- `Undead 1`

---

### Eagle (`Eagle`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`, Str: `8`

---

### Egg (`AnimalEgg`)
> *(No Description)*

**Core Stats:** HP: `4`, Move: `0`

**Properties:** `tag: animal`, `faction: allies`, `inherit_faction: true`, `shield: 4`, `corpse_health: 0`, `can_be_overkilled: false`

**Abilities:** **move:** `None` | **attack:** `None`

---

### FastFetus (`FastFetus`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Passives:**
- `AlphaTurns 1`

---

### FastRat (`FastRat`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Passives:**
- `AlphaTurns 1`

---

### Fenrir (`HunterCat`)
> Tosses bear traps! Has an affinity for tall grass. Swats away melee attackers.

**Core Stats:** HP: `60`, Move: `?`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 4`, `mana_regen: 999`, `mana: 100`

**Abilities:** **move:** `HunterMinibossMove` | **attack:** `BasicRanged_Hunter` | **spells:** BearTrap_Enemy, Shove

**Passives:**
- `CounterAttack Shove`

---

### Flushmaster (`Flushmaster`)
> Pushes all units back 10 tiles in the direction its facing.

**Core Stats:** HP: `100`, Move: `6`, Str: `6`, Dex: `6`, Con: `6`, Int: `6`, Spd: `0`, Cha: `6`

**Properties:** `tag: [elemental poop]`, `faction: enemies`, `type: boss`, `corpse_health: 0`, `initiative: -30`, `elements: [`

**Abilities:** **move:** `Teleport` | **attack:** `Flush`

**Passives:**
- `TransformOnDeath Dip`
- `FlushmasterCelebration celebrate`

---

### Franklin (`TinkererCat`)
> Spawns Robots and crafts weapons. Enters a Mech when at low HP.

**Core Stats:** HP: `45`, Move: `?`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `shield: 20`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** TCMechSuit, TCCatBot

---

### Frod Rocksnow (`CaveCatDad`)
> Has a wide melee attack with Knockback and a chance to stun. Can throw rocks.

**Core Stats:** HP: `70`, Move: `2`, Str: `8`, Spd: `3`

**Properties:** `tag: cat`, `hidden_tag: cavefamily`, `type: boss`, `base_mana_regen: 999`, `faction: enemies`, `disperse_main_turns: true`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `CaveDad_ClubBasic` | **spells:** RockToss_CaveDad, CaveCatEnrageOne, CaveCatEnrageTwo

---

### Frostbiter (`IceElemental`)
> Slows and knocks back units. Freezes adjacent units.

**Core Stats:** HP: `200`, Move: `4`

**Properties:** `tag: [elemental poop]`, `faction: enemies`, `type: boss`, `corpse_health: 0`, `round_end_bonus_turns: 1`, `initiative: -999`, `dispersed_bonus_turns: 1`, `takes_main_turn: false`, `elements: [`

**Abilities:** **move:** `DefaultMove` | **attack:** `IceElementalSpikes` | **spells:** IceElementalBlizzard, IceElementalBreath

**Passives:**
- `ElementImmune Ice`
- `ElementWeakness Fire`
- `TileElementDamageImmunity Ice`

---

### Führerfötus (`HitlerClone`)
> Has a multi-hit melee attack. Follows orders.

**Core Stats:** HP: `17`, Move: `3`

**Properties:** `tag: [humanoid]`, `hidden_tag: hitler_clone`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `FurySwipes_Hitler` | **spells:** HitlerCloneTransform, HitlerCloneLick, HitlerCloneHeil

---

### Gambit (`Gambit`)
> Has 6 special moves tied to the number on its dice! Higher numbers are more deadly.

**Core Stats:** HP: `110`, Move: `?`, Str: `4`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `round_start_bonus_turns: 1`, `round_end_bonus_turns: 1`, `mana_regen: 999`, `mana: 100`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** DiceLeap, RollDice, D6Fizzle, D6Confused, D6Poop, D6Laser, D6Quake, D6Storm, D6Wrath

**Passives:**
- `DicerArt [59 52 65 50 54 63 64]`

---

### Gasser (`Gasser`)
> *(No Description)*

**Core Stats:** HP: `15`, Move: `?`

**Properties:** `tag: blob`, `faction: enemies`, `flying: true`, `mana_regen: 999`, `exclude_from_hallucinate: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `SpawnGas` | **spells:** GasserExplode

**Passives:**
- `StatusImmunity Poison`
- `DeathRattle GasserExplode`

---

### Gein (`ButcherCat`)
> Hooks and pulls units that end their movement in range, inflicting Bleed. Does a melee spin attack that spawns meat. Seeks meat pickups. Trample.

**Core Stats:** HP: `73`, Move: `1`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `can_eat_food: true`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicButcherMeleeWideSpin` | **spells:** MoveTwo

**Passives:**
- `Trample 3`

---

### Gemini Cats (`GeminiCats`)
> *(No Description)*

**Core Stats:** HP: `100`, Move: `?`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `mana_regen: 999`, `mana: 100`, `size: gemini`

**Abilities:** **move:** `DefaultMove` | **attack:** `GeminiBite` | **spells:** GeminiSwipe, GeminiSpecial

**Passives:**
- `GeminiTwin 1`

---

### Glowing Bear (`GlowingBear`)
> It glows with an eternal light.

**Core Stats:** HP: `100`, Move: `2`

**Properties:** `tag: animal`, `faction: enemies`, `type: boss`, `weak_threshold: 25`, `evenly_dispersed_bonus_turns: 1`, `size: 2x2`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicBigMelee`

**Passives:**
- `Trample 3`
- `HealthRegenUp 4`

---

### Glowing Mushroom (`GlowingMushroom`)
> *(No Description)*

**Core Stats:** HP: `1`, Move: `?`

**Properties:** `type: object`, `tag: plant`, `faction: allies`, `inherit_faction: true`, `corpse_health: 0`, `can_be_backstabbed: false`, `kill_required: false`, `ai_scale: .01`

**Abilities:** **move:** `None` | **attack:** `None` | **spells:** GlowingMushroomGiveMana

**Passives:**
- `Plant 1`
- `ElementImmune Creep`

---

### GlowingMushroom2 (`GlowingMushroom2`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Abilities:** **spells:** GlowingMushroomGiveMana2

---

### Golem (`GolemCat`)
> Invulnerable. Dies when all of its allies are dead.

**Core Stats:** HP: `15`, Move: `2`, Str: `15`, Spd: `2`

**Properties:** `tag: [cat golem]`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 10`, `kill_required: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `BlockAllDamage 1`
- `DieWhenOnlyGolemsLeft 1`
- `AddMeleeKnockback 2`

---

### Good {Catname} (`PlayerCat_FinalBossClone`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `faction: enemies`, `hidden_tag: finalboss_clonecat`, `can_be_overkilled: true`, `allow_passive_spelltransforming: true`, `access_to_player_inventory: false`, `corpse_health: 1`, `is_player_cat: false`, `exclude_from_hallucinate: true`, `base_initiative: -1`, `disallow_items: all`, `force_not_familiar: true`, `banned_elite_buffs: [Depressing]`

**Passives:**
- `AdvancedTint [`
- `.6, .6, .6, 1`
- `.5, .5, .5, 0`
- `]`

---

### Guillotina (`Guillotina2Head`)
> It may be separated from her body, but they are still working together.

**Core Stats:** HP: `250`, Move: `?`, Str: `4`, Spd: `8`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 2`, `dispersed_bonus_turns_before_cats: true`, `initiative: 999`, `corpse_health: indestructible`, `mana_regen: 999`, `mana: 100`, `weak_threshold: 50`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `TinaHeadGutSpear` | **spells:** YeetTowardsBuddy, Magnetize, Guillotina2Rage, GuillotinaTossCollide, Tina2Call

**Passives:**
- `Buddy Guillotina2Body`

---

### Guillotina (`Guillotina2Body`)
> It may be separated from her head, but they are still working together.

**Core Stats:** HP: `250`, Move: `1`, Str: `8`, Spd: `2`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `initiative: -999`, `corpse_health: indestructible`, `size: 2x2`, `move_block: everything_even_when_dead`, `mana_regen: 999`, `mana: 100`, `weak_threshold: 50`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `TinaBodySlam` | **spells:** TinaBodySlamMax, Guillotina2Rage, TinaBodySlamRage, TinaTantrum

**Passives:**
- `Buddy Guillotina2Head`
- `Trample 3`

---

### Guillotina (`Guillotina1`)
> She lusts with a never ending hunger!

**Core Stats:** HP: `400`, Move: `3`, Spd: `4`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `corpse_health: indestructible`, `size: 2x2`, `move_block: everything_even_when_dead`, `dispersed_bonus_turns: 2`, `mana_regen: 999`, `mana: 100`, `weak_threshold: 50`

**Abilities:** **move:** `DefaultMove` | **attack:** `TinaBasicBigMelee` | **spells:** TinaBasicJump, TinaJumpAttack, TinaSuck, TinaSpit, TinaThrow, Guillotina1Rage, BellyPound, Digest, TinaSuck2, TinaSpit2

**Passives:**
- `Trample 3`
- `GuillotinaDeathHead 1`

---

### Guillotina (`Guillotina3Body`)
> It's trying to find it's head...

**Core Stats:** HP: `400`, Move: `2`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `corpse_health: 0`, `size: 2x2`, `move_block: everything_even_when_dead`, `dispersed_bonus_turns: 2`, `mana_regen: 999`, `mana: 100`, `weak_threshold: 50`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `None` | **spells:** G3RunToHead, G3GrabHead, G3TossHead, G3Scream_Hex, G3Shake, G3SpawnMama, G3RageShake

**Passives:**
- `Trample 3`
- `Buddy Guillotina3Head`

---

### Guillotina (`Guillotina3Head`)
> Sorry I'm dead...

**Core Stats:** HP: `200`, Move: `?`, Str: `4`, Spd: `2`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `corpse_health: indestructible`, `mana_regen: 999`, `mana: 100`, `weak_threshold: 50`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `None` | **attack:** `G3PrisonSpit` | **spells:** G3CoughFly, G3CallForHelp

**Passives:**
- `Buddy Guillotina3Body`
- `MinimumKnockbackFromPhysicalAttacks 1`
- `Trample 3`

---

### Gun (`RiftKitten`)
> Thank you for releasing me!

**Core Stats:** HP: `16`, Move: `?`, Str: `4`, Dex: `4`, Con: `4`, Int: `4`, Spd: `4`, Cha: `4`

**Properties:** `tag: cat`, `type: cat`, `faction: allies`, `mana_matters: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **can_get_bonus:** `true`

**Passives:**
- `ConjureBonusAbility random`

---

### Harpy (`Harpy`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### Hellspawn (`Hellspawn`)
> It has such sights to show you!

**Core Stats:** HP: `69`, Move: `1`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `can_eat_food: true`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicButcherMelee` | **spells:** MoveTwo

---

### Herald's Shadow (`BoyShadeClone`)
> Melee attacker. Dies when the original dies.

**Core Stats:** HP: `1`, Move: `4`

**Properties:** `tag: [demon]`, `faction: enemies`, `initiative: -99`, `corpse_health: 0`

**Abilities:** **move:** `Teleport` | **attack:** `BasicMelee`

**Passives:**
- `DieWhenSpawnerDies 1`

---

### Hitler (`HitlerHead`)
> Grows his army of Hitlers!

**Core Stats:** HP: `200`, Move: `2`

**Properties:** `tag: [humanoid robot]`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 2`, `shield: 200`, `size: 2x2`, `lock_orientation: [-1 0]`, `move_block: everything_even_when_dead`, `boss_minions_runaway: false`

**Abilities:** **move:** `DoNothing` | **attack:** `DoNothing` | **spells:** HitlerHeadGrowA, HitlerHeadGrowB, HitlerHeadTransform

**Passives:**
- `Trample 3`
- `Brace 1`
- `Robot 1`

---

### Hitler (`Hitler`)
> Rallies his army. Has a ranged attack and Trample.

**Core Stats:** HP: `200`, Move: `4`

**Properties:** `tag: [humanoid robot]`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 2`, `shield: 200`, `size: 2x2`, `move_block: everything_even_when_dead`, `boss_minions_runaway: false`

**Abilities:** **move:** `GooseStep` | **attack:** `HitlerShoot` | **spells:** HitlerHeil, HitlerSuicide, HitlerNuke

**Passives:**
- `Trample 3`
- `Robot 1`

---

### Hitler (`T3Hitler`)
> *(No Description)*

**Core Stats:** HP: `100`, Move: `4`, Str: `2`, Dex: `7`

**Properties:** `tag: [humanoid robot]`, `faction: enemies`, `type: boss`, `corpse_health: 0`, `takes_turns: false`, `flying: true`, `shield: 100`, `banned_elite_buffs: [Mad Twin]`

**Abilities:** **move:** `DoNothing` | **attack:** `DoNothing` | **spells:** T3RipAndTear, T3Counter, T3Spawn_Tank, T3Spawn_Mage, T3Spawn_Hunter, T3Spawn_Thief, T3Spawn_Medic, T3Spawn_Fighter, T3Spawn_Colorless, T3Spawn_Necromancer, T3Spawn_Tinkerer, T3Spawn_Butcher, T3Spawn_Psychic, T3Spawn_Druid, T3Spawn_Monk, T3Spawn_Jester, T3Intro, T3JoinFight, HitlerPulp1, HitlerPulp2, HitlerPulp3, HitlerPulp4, HitlerPulp5, HitlerPulp6

**Passives:**
- `Robot 1`

---

### HumanCat (`HumanCat`)
> Melee attacker that Immobilizes. May dodge attacks unless attacked from the human side.

**Core Stats:** HP: `9`, Move: `3`

**Properties:** `tag: [humanoid cat]`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `HCAttack` | **spells:** HCHumanDie

---

### Hummingbird (`HummingBird`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### HuskG (`HuskG`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### Johnny (`Johnny`)
> Calls in Cultists for help. Can only use his psychic spells while being washed.

**Core Stats:** HP: `250`, Move: `2`

**Properties:** `tag: humanoid`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 2`, `knockback_immune: true`, `size: 2x2`, `lock_orientation: [0, -1]`, `move_block: everything_even_when_dead`, `boss_minions_runaway: false`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `None` | **attack:** `None` | **spells:** JohnnyCryOne, JohnnyCryTwo, JohnnyPush, JohnnyPull, JohnnyMindControl, JohnnyBlast, JohnnyMegaBlast

**Passives:**
- `Trample 3`

---

### LargeBirdPool (`LargeBirdPool`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `can_be_champion: false`

---

### Lenny (`Lenny`)
> Loves kitties! Especially {buddyname}!

**Core Stats:** HP: `130`, Move: `4`, Str: `8`, Int: `0`

**Properties:** `tag: [humanoid]`, `faction: enemies`, `type: boss`, `corpse_health: 1`, `dispersed_bonus_turns: 2`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `LennyShove` | **spells:** LennyGrab, LennyHug, LennyCatSlap, LennyCatDies, LennyDrop, LennyStruggleFail, LennyGrabDead

**Passives:**
- `Buddy choose_favorite_cat`
- `DisplayBuddyCatOnSpawn 3`

---

### Little Bird (`BirdSmall`)
> *(No Description)*

**Core Stats:** HP: `2`, Move: `5`

**Passives:**
- `RunInXTurns 1`

---

### Loan Shark (`LoanShark`)
> Its bite inflicts Bleed. Takes bonus turns for each bleeding unit. Focuses on bleeding units.

**Core Stats:** HP: `37`, Move: `4`, Str: `2`

**Properties:** `tag: [cat fish]`, `type: cat`, `shield: 37`, `base_mana_regen: 999`, `faction: enemies`, `initiative: 100`, `view_bleeding_characters_as_enemies: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `SharkDash`

**Passives:**
- `SharkySmellsBlood 1`
- `WaterWalk 1`

---

### Lord Bunga (`LordBunga`)
> Retaliates when hit. Consumes adjacent units at the start of his turn. Blind to units behind him.

**Core Stats:** HP: `300`, Move: `2`

**Properties:** `tag: humanoid`, `faction: cavemen`, `type: boss`, `dispersed_bonus_turns: 2`, `size: 2x2`, `lock_orientation: [-1 0]`, `move_block: everything_even_when_dead`, `boss_minions_runaway: false`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DoNothing` | **attack:** `DoNothing` | **spells:** BungaEntrance, BungaEatCat, BungaSwipe, BungaRoar

**Passives:**
- `Trample 3`

---

### Louse (`Lice`)
> Its melee attacks inflict Bruise.

**Core Stats:** HP: `1`, Move: `3`, Str: `4`

**Properties:** `tag: bug`, `corpse_health: 0`, `faction: enemies`, `type: small`, `deathpoof_size: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `LiceBite`

---

### Lucy (`MageCat`)
> Her powerful spells take time to charge up.

**Core Stats:** HP: `75`, Move: `?`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `initiative: -999`, `evenly_dispersed_bonus_turns: 1`, `/*mana_regen: -2`, `mana: 100`, `initial_mana: 100`, `mana_matters: true*/`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMagicShortRanged` | **spells:** MCBlizzard, MCFlamethrower, MCStorm

---

### Mad Lad (`MadLad`)
> *(No Description)*

**Core Stats:** HP: `30`, Move: `?`, Str: `3`

**Properties:** `tag: blob`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `EnrageOnDamage 1`
- `CounterAttack attack`

---

### MaddenedBear (`MaddenedBear`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `faction: enemies`

**Passives:**
- `PermanentMadness 1`

---

### Magnus (`FighterCat`)
> Has a chaining dash attack and a spin attack.

**Core Stats:** HP: `70`, Move: `2`, Str: `3`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`, `dispersed_bonus_turns_consider_initiative: false`, `mana_regen: 999`, `mana: 100`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee_Fighter` | **spells:** ChainDash, Spin_Enemy

---

### Maisie (`TankCat`)
> Protects her kittens when they are attacked.

**Core Stats:** HP: `90`, Move: `5`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `corpse_health: 3`, `dispersed_bonus_turns: 1`, `dispersed_bonus_turns_consider_initiative: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicTankMelee` | **spells:** SwapPositions_TankCat, LickyLicky

**Passives:**
- `MamaCatAnimations 1`
- `RunWhenKittensDead 1`

---

### Mama Maggot (`MaggotLord`)
> Spawns Maggots, evolves them and gives them bonus turns. Trample.

**Core Stats:** HP: `125`, Move: `3`

**Properties:** `tag: worm`, `faction: enemies`, `type: boss`, `mana_regen: 999`, `mana: 100`, `round_start_bonus_turns: 1`, `round_end_bonus_turns: 1`, `size: 2x2`, `move_block: everything_even_when_dead`, `boss_minions_runaway: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `None` | **spells:** SpawnMaggots, MutateAOE, RallyMaggots

**Passives:**
- `Trample 3`

---

### MamaMaggotTina (`MamaMaggotTina`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### Man In The Moon (`MoonHead`)
> Its breath attack will push all units back 10 tiles. Loses its Brace if it punches itself. What could be inside?

**Core Stats:** HP: `400`, Move: `0`

**Properties:** `tag: [alien rock]`, `hidden_tag: [moonhead moonboss]`, `faction: enemies`, `type: boss`, `size: 3x3`, `move_block: everything_even_when_dead`, `round_end_bonus_turns: 1`, `initiative: 100`, `knockback_immune: true`, `corpse_health: 0`, `lock_orientation: [-1 0]`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `None` | **attack:** `None` | **spells:** MoonHead_BeginCharge, MoonHead_EatCat, MoonHead_Barrage, MoonHead_Blow, MoonHead_Finisher, MoonHead_Digest, MoonHead_SpitCat, MoonHead_ChewCat, MoonHead_SacrificeHand, MoonHead_SpawnHand, MoonHead_SpitCat_AndDie, MoonHead_CommandHeadPunch, MoonHead_RefreshBrace, MoonHead_CallForHelp

**Passives:**
- `Brace 10`
- `DeathRattle MoonHead_KillHands`
- `MoonHeadCrackedVisual Cracked`

---

### Mangler's Monster (`ManglersMonster`)
> Controlled by the Doctor.

**Core Stats:** HP: `250`, Move: `1`, Str: `8`

**Properties:** `tag: [humanoid blob]`, `faction: enemies`, `type: boss`, `size: 3x3`, `move_block: everything_even_when_dead`, `takes_turns: false`, `can_be_backstabbed: false`, `knockback_immune: true`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `None` | **attack:** `ManglerMonsterDashAttack` | **spells:** ManglerMonsterExplode, ManglerMonsterHeartAttack

**Passives:**
- `Trample 3`
- `Buddy DrMangler`
- `ManglerMonsterPassive ManglerMonsterDashAttack`
- `OrthogonalAIDangerZone 10`
- `CCImmunity 1`
- `AbilityWhenBuddyDies ManglerMonsterHeartAttack`

---

### Marshmallow (`MedicCat`)
> Her lick attack Charms units.

**Core Stats:** HP: `60`, Move: `3`, Dex: `1`, Con: `3`, Int: `4`, Spd: `4`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 2`, `mana_regen: 999`, `mana: 100`, `divine_shield: 2`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMedicMelee` | **spells:** MarshmallowConvert, MarshmallowZealot

**Passives:**
- `AvoidDamagingCharmedEnemies 1`
- `LegacySpawnSavedCatIfExists Legacy_Marshmallow_StolenCatID`

---

### Meat Minion (`MeatMinion`)
> *(No Description)*

**Core Stats:** HP: `2`, Move: `3`, Str: `3`

**Properties:** `tag: blob`, `corpse_health: 0`, `faction: enemies`, `type: small`, `deathpoof_size: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `MeatMinionMelee`

**Passives:**
- `SpawnThingOnDeath Food`

---

### MedBirdPool (`MedBirdPool`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `can_be_champion: false`

---

### Medium Bird (`BirdMed`)
> *(No Description)*

**Core Stats:** HP: `7`, Move: `4`

**Passives:**
- `RunInXTurns 2`

---

### Medium Slime (`MedSlime`)
> Melee attacker. Splits into 4 small Slimes on death.

**Core Stats:** HP: `16`, Move: `3`, Dex: `3`, Con: `3`, Int: `3`, Spd: `3`, Cha: `3`

**Properties:** `tag: blob`, `faction: enemies`, `type: boss`, `corpse_health: 0`, `banned_elite_buffs: [Shielded1 Shielded2 Shielded3 Shielded4]`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `Divide4OnDeath SmallSlime`

---

### Moon Hand (`MoonHand`)
> Will grab units that end movement directly in front of it. Attack it to turn it away from you. Attacking it from behind will force it to dash attack or drop what its holding.

**Core Stats:** HP: `100`, Move: `3`

**Properties:** `tag: [alien rock]`, `hidden_tag: [moonhand moonboss]`, `faction: enemies`, `type: boss`, `flying: true`, `disperse_main_turns: true`, `kill_required: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `MoonHandSlap` | **spells:** MoonHandGrab, MoonHandDash, MoonHandThrow, MoonHandDrop_Deathrattle, MoonHandDrop, MoonHandMegaSqueeze, MoonHandPunchHead

**Passives:**
- `WideBackstab 1`
- `LimitDamage 1`
- `LimitHeal 0`
- `StripStatuses 1`

---

### Morana (`NecroCat`)
> Its ranged attack inflicts Leech. Reanimates dead bodies. Revives through dead bodies.

**Core Stats:** HP: `75`, Move: `?`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `corpse_health: 5`, `dispersed_bonus_turns: 1`, `round_end_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicNecroRanged` | **spells:** NCReanimate, NCGravecrawl

---

### Moth (`Moth`)
> *(No Description)*

**Core Stats:** HP: `24`, Move: `5`, Str: `8`, Dex: `8`, Con: `8`, Int: `8`, Spd: `8`, Cha: `8`

**Properties:** `tag: animal`, `type: small`, `faction: allies`, `inherit_faction: true`, `flying: true`, `mana_matters: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicShortLobbed` | **can_get_bonus:** `true` | **spells:** CrowFlutter, SleepPowder

---

### MotherTumorBig (`MotherTumorBig`)
> *(No Description)*

**Core Stats:** HP: `9`, Move: `?`

---

### Multicat (`Multicat`)
> *(No Description)*

**Core Stats:** HP: `30`, Move: `?`, Str: `4`

**Properties:** `tag: cat`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `MulticatHeads 0`

---

### Mutant (`Mutant`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### NonChampionFlySwarm (`NonChampionFlySwarm`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `can_be_champion: false`

---

### Nubs (`Nubs`)
> Blind. Lobs a Poison creep shot when damaged. Does a leap attack with Knockback.

**Core Stats:** HP: `100`, Move: `1`, Dex: `8`

**Properties:** `tag: dog`, `faction: enemies`, `type: boss`, `mana_regen: 999`, `mana: 100`, `corpse_health: 0`, `evenly_dispersed_bonus_turns: 1`, `disperse_main_turns: true`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `NubsJump` | **spells:** NubsNuke, NubsGoop

**Passives:**
- `Buddy Chubs`
- `ImmediateAbilityReaction NubsGoop`
- `FormChangeWhenBuddyDies Rage`

---

### Ornstein (`Ornstein`)
> *(No Description)*

**Core Stats:** HP: `75`, Move: `?`, Str: `4`

**Properties:** `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 2`, `mana_regen: 999`, `mana: 100`

**Abilities:** **move:** `DefaultMove` | **attack:** `SpearPoke` | **spells:** YeetTowardsBuddy, Magnetize

**Passives:**
- `Buddy Smough`
- `TransformWhenBuddyDies UltraOrnstein`

---

### Pachysaurus [img:female] (`GirlDino`)
> Melee attacker. Defends its partner.

**Core Stats:** HP: `50`, Move: `2`, Str: `7`, Spd: `2`

**Properties:** `tag: dinosaur`, `hidden_tag: dinofamily`, `faction: enemies`, `type: boss`, `shield: 50`, `size: 2x2`, `move_block: everything_even_when_dead`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `GirlDinoMelee` | **spells:** GirlDinoHeadBash, GirlDinoCry, GirlDinoThrow, GirlDinoPoop

**Passives:**
- `Trample 3`
- `Brace 2`
- `Buddy BoyDino`
- `AbilityWhenBuddyDies GirlDinoCry`

---

### Pachysaurus [img:male] (`BoyDino`)
> Melee attacker. Defends its partner.

**Core Stats:** HP: `50`, Move: `3`, Str: `3`, Spd: `8`

**Properties:** `tag: dinosaur`, `hidden_tag: dinofamily`, `faction: enemies`, `type: boss`, `shield: 25`, `size: 2x2`, `move_block: everything_even_when_dead`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `BoyDinoBasic` | **spells:** BoyDinoHeadBash, BoyDinoCry

**Passives:**
- `Trample 3`
- `Brace 1`
- `Buddy GirlDino`
- `AbilityWhenBuddyDies BoyDinoCry`

---

### Paraisaria (`InfestedDuo`)
> Takes an extra turn for each Sprout.

**Core Stats:** HP: `65`, Move: `1`, Spd: `1`

**Properties:** `tag: [cat plant]`, `type: boss`, `base_mana_regen: 999`, `faction: enemies`, `disperse_main_turns: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** IDSprout, IDBrambleBurst, IDBrambleShot

**Passives:**
- `Plant 1`
- `ElementImmune Creep`
- `Thorns 2`
- `AbilityReaction IDSprout`
- `ExtraTurnsPerTaggedUnit sprout`
- `DeathRattle IDBrambleBurst`

---

### Pebbles (`ColorlessCat_Tutorial`)
> Its melee attack knocks units back. Can throw rocks.

**Core Stats:** HP: `50`, Move: `4`, Str: `3`, Dex: `3`, Con: `3`, Int: `3`, Spd: `3`, Cha: `3`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`, `dispersed_bonus_turns_consider_initiative: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `ColorlessCat_Push` | **spells:** RockToss_ColorlessCat, RockToss_ColorlessCat_AsCloseAsPossible, ColorlessCat_BoulderDrop

**Passives:**
- `TutorialBossRiggedFight 16`

---

### PlayerCat_FinalBossClone_Champion (`PlayerCat_FinalBossClone_Champion`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `disallow_items: Nuke`, `champion: true`

---

### PlayerCat_FinalBossClone_Elite (`PlayerCat_FinalBossClone_Elite`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `disallow_items: Nuke`, `champion: true`, `elite: true`

---

### PlayerCat_HuskShade (`PlayerCat_HuskShade`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `corpse_health: 0`, `can_grant_extra_turns: false`, `faction: enemies`, `is_player_cat: false`, `access_to_player_inventory: false`, `allow_passive_spelltransforming: true`, `force_not_familiar: true`

**Passives:**
- `FadeInsteadOfDie 1`

---

### Poison Frog (`PoisonFrog`)
> *(No Description)*

**Core Stats:** HP: `5`, Move: `?`

**Properties:** `faction: enemies`, `kill_required: true`

---

### Poobles Rocksnow (`CaveCatBaby`)
> Places bear traps. Has a jumping melee attack.

**Core Stats:** HP: `50`, Move: `?`, Str: `3`, Spd: `9`

**Properties:** `tag: cat`, `hidden_tag: cavefamily`, `type: boss`, `base_mana_regen: 999`, `faction: enemies`, `disperse_main_turns: true`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `CaveCatPounce` | **spells:** BearTrap_CaveBaby, CaveCatEnrageOne, CaveCatEnrageTwo

---

### Poop Cat (`PoopCat`)
> Nasty.

**Core Stats:** HP: `25`, Move: `?`, Str: `2`, Spd: `1`

**Properties:** `tag: [cat poop]`, `type: cat`, `base_mana_regen: 999`, `faction: enemies`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `PoopCatMelee`

**Passives:**
- `PoisonThorns 3`

---

### Pyrophina (`Pyrophina`)
> Pyrophina was baptized in the fires of hell and survived!

**Core Stats:** HP: `600`, Move: `3`

**Properties:** `tag: kaiju`, `faction: enemies`, `type: boss`, `corpse_health: indestructible`, `size: 2x2`, `move_block: everything_even_when_dead`, `evenly_dispersed_bonus_turns: 2`, `dispersed_bonus_turns_before_cats: false`, `initiative: -100`, `mana_regen: 999`, `mana: 100`, `weak_threshold: 150`

**Abilities:** **move:** `DefaultMove` | **attack:** `PyrophinaSoloAttack` | **spells:** PyrophinaVSWeatherRoar, PyrophinaSoloCatThrow, PyrophinaSoloFlamethrower, PyrophinaSoloEarthquakeStomp, PyrophinaSoloRoar, PyrophinaVSRun

**Passives:**
- `Trample 3`
- `KaijuKnockbackImmune 1`
- `ElementImmune Fire`

---

### Pyrophina (`PyrophinaVS`)
> She wants to kill Zaratana!

**Core Stats:** HP: `1000`, Move: `3`

**Properties:** `tag: kaiju`, `faction: kaiju1`, `type: boss`, `corpse_health: indestructible`, `size: 2x2`, `move_block: everything_even_when_dead`, `disperse_main_turns: true`, `dispersed_bonus_turns_before_cats: true`, `mana_regen: 999`, `mana: 100`, `weak_threshold: 150`, `must_start_facing_camera: false`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** PyrophinaVSSpinThrow, PyrophinaVSWeatherRoar, PyrophinaVSCatThrow, PyrophinaVSFlamethrower, PyrophinaVSEarthquakeStomp, PyrophinaVSRoar, PyrophinaVSRun

**Passives:**
- `Trample 3`
- `KaijuKnockbackImmune 1`
- `KaijuWinCon pyrophina`
- `ElementImmune Fire`
- `BonusTurnPattern [`
- `]`

---

### Pyrophina (Friendly) (`PyrophinaFamiliar`)
> Shes here to help, and trying her best!

**Core Stats:** HP: `600`, Move: `3`

**Properties:** `tag: kaiju`, `faction: allies`, `inherit_faction: true`, `type: boss`, `corpse_health: indestructible`, `size: 2x2`, `move_block: everything_even_when_dead`, `initiative: -5`, `mana_regen: 999`, `mana: 100`, `weak_threshold: 150`, `ai_scale: .25`

**Abilities:** **move:** `DefaultMove` | **attack:** `PyrophinaSoloAttack` | **spells:** PyrophinaSoloFlamethrower

**Passives:**
- `Trample 3`
- `KaijuKnockbackImmune 1`
- `DissuadeInstakills 1`
- `ElementImmune Fire`
- `ChanceToDisableActionsIfNotCharmed 75%`

---

### Queen Hippo (`QueenHippo`)
> Its melee attack deals Chain Knockback. Uppercuts any adjacent units at the start of its turn. Has heart problems...

**Core Stats:** HP: `80`, Move: `0`, Spd: `3`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`, `round_end_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `QueenHippoAttack` | **spells:** QueenHippoUppercut, QueenHippoTire, QueenHippoHeartAttack

**Passives:**
- `Brace 4`

---

### Radical Rat (`BomberRat`)
> Tosses bombs that explode at the end of the round.

**Core Stats:** HP: `67`, Move: `5`

**Properties:** `tag: rat`, `faction: enemies`, `type: boss`, `mana_regen: 999`, `mana: 100`, `initiative: -100`, `dispersed_bonus_turns: 2`, `dispersed_bonus_turns_consider_initiative: false`, `dispersed_bonus_turns_before_cats: true`, `last_turn_is_main_turn: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `None` | **spells:** SpawnBomb, BombRatTurtle, RockToss_BomberRat

---

### Rager (`Rager`)
> *(No Description)*

**Core Stats:** HP: `30`, Move: `3`

**Properties:** `tag: blob`, `faction: enemies`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** RageUp

---

### RandomDruidFamiliar (`RandomDruidFamiliar`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### Rat King (`RatKing_Old`)
> *(No Description)*

**Core Stats:** HP: `50`, Move: `?`, Int: `10`

**Properties:** `tag: rat`, `faction: enemies`, `type: boss`, `mana_regen: 999`, `mana: 100`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** RangedHeal_Enemy

---

### Rat King (`RatKing`)
> Spawns Lil' Rats and throws adjacent units.

**Core Stats:** HP: `100`, Move: `2`

**Properties:** `tag: [rat]`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `RatKingToss` | **spells:** RatKingSpawn, RatKing2Spawn, RatKingTransform

**Passives:**
- `Trample 3`

---

### Rat Pile (`RatPile`)
> *(No Description)*

**Core Stats:** HP: `50`, Move: `?`

**Properties:** `tag: rat`, `faction: enemies`, `type: boss`, `mana_regen: 999`, `mana: 100`, `size: 3x3`, `move_block: everything_even_when_dead`, `can_be_backstabbed: false`, `knockback_immune: true`, `corpse_health: 0`

**Abilities:** **move:** `None` | **attack:** `None` | **spells:** SpawnRat, HealSelf

**Passives:**
- `Trample 5`
- `TransformOnDeath RatKing`

---

### Raven (`Raven`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### Robo-Alice (`PsychicCat_Terminator`)
> *(No Description)*

**Core Stats:** HP: `25`, Move: `?`

**Properties:** `tags: [cat robot]`, `hidden_tags: terminator_mini`, `shield: 25`, `corpse_health: 0`

**Passives:**
- `Robot 1`
- `SpawnOnDeath Antidote`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`

---

### Robo-Arthur (`JesterCat_Terminator`)
> *(No Description)*

**Core Stats:** HP: `25`, Move: `?`

**Properties:** `tags: [cat robot]`, `hidden_tags: terminator_mini`, `shield: 25`, `corpse_health: 0`, `dispersed_bonus_turns: 1`

**Passives:**
- `Robot 1`
- `SpawnOnDeath Antidote`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`

---

### Robo-Chan Hung (`MonkCat_Terminator`)
> *(No Description)*

**Core Stats:** HP: `25`, Move: `?`

**Properties:** `tags: [cat robot]`, `hidden_tags: terminator_mini`, `shield: 25`, `corpse_health: 0`

**Passives:**
- `Robot 1`
- `SpawnOnDeath Antidote`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`

---

### Robo-Dack (`ThiefCat_Terminator`)
> *(No Description)*

**Core Stats:** HP: `25`, Move: `?`

**Properties:** `tags: [cat robot]`, `hidden_tags: terminator_mini`, `shield: 25`, `corpse_health: 0`, `dispersed_bonus_turns: 1`

**Passives:**
- `Robot 1`
- `SpawnOnDeath Antidote`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`

---

### Robo-Draven (`DruidCat_Terminator`)
> *(No Description)*

**Core Stats:** HP: `25`, Move: `?`, Str: `3`

**Properties:** `tags: [cat robot]`, `hidden_tags: [terminator_mini dc_cat]`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`, `shield: 25`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `DruidCatBasic` | **spells:** DCSquirrelForm, DCBirthSquirrel, DCT_SummonCrow

**Passives:**
- `Robot 1`
- `SpawnOnDeath Antidote`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`

---

### Robo-Draven's Crow (`DruidCrow_Terminator`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### Robo-Fenrir (`HunterCat_Terminator`)
> Tosses bear traps! Has an affinity for tall grass. Swats away melee attackes.

**Core Stats:** HP: `25`, Move: `?`

**Properties:** `tags: [cat robot]`, `hidden_tags: terminator_mini`, `shield: 25`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`, `corpse_health: 0`

**Abilities:** **move:** `HunterMinibossMove` | **attack:** `BasicRanged_Hunter` | **spells:** BearTrap_Enemy_Cantrip, Shove

**Passives:**
- `CounterAttack Shove`
- `Robot 1`
- `SpawnOnDeath Antidote`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`

---

### Robo-Franklin (`TinkererCat_Terminator`)
> *(No Description)*

**Core Stats:** HP: `25`, Move: `?`

**Properties:** `tags: [cat robot]`, `hidden_tags: terminator_mini`, `shield: 25`, `corpse_health: 0`

**Passives:**
- `Robot 1`
- `SpawnOnDeath Antidote`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`

---

### Robo-Gein (`ButcherCat_Terminator`)
> *(No Description)*

**Core Stats:** HP: `25`, Move: `?`

**Properties:** `tags: [cat robot]`, `hidden_tags: terminator_mini`, `shield: 25`, `corpse_health: 0`

**Passives:**
- `Robot 1`
- `SpawnOnDeath Antidote`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`

---

### Robo-Lucy (`MageCat_Terminator`)
> *(No Description)*

**Core Stats:** HP: `25`, Move: `?`

**Properties:** `tags: [cat robot]`, `hidden_tags: terminator_mini`, `shield: 25`, `corpse_health: 0`

**Passives:**
- `Robot 1`
- `SpawnOnDeath Antidote`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`

---

### Robo-Magnus (`FighterCat_Terminator`)
> *(No Description)*

**Core Stats:** HP: `25`, Move: `?`

**Properties:** `tags: [cat robot]`, `hidden_tags: terminator_mini`, `shield: 25`, `corpse_health: 0`

**Passives:**
- `Robot 1`
- `SpawnOnDeath Antidote`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`

---

### Robo-Maisie (`TankCat_Terminator`)
> Protects her allies when they are attacked.

**Core Stats:** HP: `25`, Move: `5`

**Properties:** `tags: [cat robot]`, `hidden_tags: terminator_mini`, `shield: 25`, `corpse_health: 0`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`, `dispersed_bonus_turns_consider_initiative: false`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicTankMelee` | **spells:** SwapPositions_TankCat, T3LickyLicky

**Passives:**
- `MamaCatAnimations 1`
- `Robot 1`
- `SpawnOnDeath Antidote`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`

---

### Robo-Marshmallow (`MedicCat_Terminator`)
> *(No Description)*

**Core Stats:** HP: `25`, Move: `?`

**Properties:** `tags: [cat robot]`, `hidden_tags: terminator_mini`, `shield: 25`, `divine_shield: 0`, `corpse_health: 0`, `dispersed_bonus_turns: 1`

**Passives:**
- `Robot 1`
- `SpawnOnDeath Antidote`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`

---

### Robo-Morana (`NecroCat_Terminator`)
> *(No Description)*

**Core Stats:** HP: `25`, Move: `?`

**Properties:** `tags: [cat robot]`, `hidden_tags: terminator_mini`, `shield: 25`, `corpse_health: 0`, `dispersed_bonus_turns: 0`

**Passives:**
- `Robot 1`
- `SpawnOnDeath Antidote`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`

---

### Robo-Pebbles (`Pebbles_Terminator`)
> *(No Description)*

**Core Stats:** HP: `25`, Move: `4`

**Properties:** `tags: [cat robot]`, `hidden_tags: terminator_mini`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`, `dispersed_bonus_turns_consider_initiative: false`, `shield: 25`, `corpse_health: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `ColorlessCat_Push` | **spells:** RockToss_ColorlessCat, RockToss_ColorlessCat_AsCloseAsPossible, T3Pebbles_BoulderDrop, T3Pebbles_PrimeBoulderDrop

**Passives:**
- `Robot 1`
- `SpawnOnDeath Antidote`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `SpawnOnDeath RandomArmorPickup`
- `UseAbilityWhenShieldDepleted T3Pebbles_PrimeBoulderDrop`

---

### Rocky Bobo (`RockyBobo`)
> Moves towards what damages it. Does a body slam attack in the direction he's facing. Can levitate rocks!

**Core Stats:** HP: `75`, Move: `4`

**Properties:** `tag: [cat rock]`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 2`, `mana_regen: 999`, `mana: 100`, `shield: 65`, `size: 2x2`, `move_block: everything_even_when_dead`, `elements: [`

**Abilities:** **move:** `DefaultMove` | **attack:** `RockySlam` | **spells:** RockSong

**Passives:**
- `Trample 3`

---

### Seagull (`Seagull`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### Seduced Boulder (`SeducedBoulder`)
> *(No Description)*

**Core Stats:** HP: `15`, Move: `4`, Int: `0`

**Properties:** `faction: allies`, `takes_turns: true`, `corpse_health: 0`, `can_be_backstabbed: false`, `elements: [`

**Abilities:** **move:** `DefaultMove` | **attack:** `None` | **can_get_bonus:** `true` | **spells:** Taunt

---

### Shadow Cat (`ShadowCat`)
> *(No Description)*

**Core Stats:** HP: `50`, Move: `5`

**Properties:** `tag: [cat demon]`, `faction: enemies`, `type: boss`, `corpse_health: 3`, `disperse_main_turns: true`, `elements: [`

**Abilities:** **move:** `DefaultMove` | **attack:** `ShadowDagger` | **spells:** ShadowstepDodge

**Passives:**
- `TileTrail ShadowTile`

---

### SkeletonCatRevived (`SkeletonCatRevived`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `exclude_from_hallucinate: true`

---

### SkeletonShamblerRevived (`SkeletonShamblerRevived`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `exclude_from_hallucinate: true`

---

### Small Slime (`SmallSlime`)
> Melee attacker.

**Core Stats:** HP: `4`, Move: `2`, Str: `2`, Dex: `1`, Con: `1`, Int: `1`, Spd: `1`, Cha: `1`

**Properties:** `tag: blob`, `faction: enemies`, `type: boss`, `corpse_health: 0`, `held_coins: [0 1]`, `banned_elite_buffs: [Shielded1 Shielded2 Shielded3 Shielded4]`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

---

### SmallBirdPool (`SmallBirdPool`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `can_be_champion: false`

---

### Smough (`Smough`)
> *(No Description)*

**Core Stats:** HP: `50`, Move: `1`, Spd: `2`

**Properties:** `faction: enemies`, `type: boss`, `initiative: -999`, `size: 2x2`, `move_block: everything_even_when_dead`, `mana_regen: 999`, `mana: 100`, `shield: 50`

**Abilities:** **move:** `DefaultMove` | **attack:** `HammerSmash`

**Passives:**
- `Buddy Ornstein`
- `TransformWhenBuddyDies UltraSmough`
- `Trample 3`

---

### Snake2 (`Snake2`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Passives:**
- `DodgeChance_Status 66`

---

### Soahc (`Chaos`)
> Stropelet eh emit hcae egnahc seitiliba sih.

**Core Stats:** HP: `400`, Move: `0`, Str: `8`, Dex: `8`, Con: `8`, Int: `8`, Spd: `8`, Cha: `8`

**Properties:** `tag: humanoid`, `faction: enemies`, `type: boss`, `evenly_dispersed_bonus_turns: 1`, `initiative: -999`, `corpse_health: 1`, `knockback_immune: true`, `flying: true`, `size: 2x2`, `move_block: everything_even_when_dead`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `None` | **attack:** `BasicBigMelee` | **spells:** ChaosSwitchSides, DbgChaosSwitchFormsA, DbgChaosSwitchFormsP, ChaosSwitchForms, SpreadX, MegablastX, FlushX, ThornUpX, CerberubsShotgunReactionX, ChaosSpawnIn

**Passives:**
- `Trample 3`
- `LockOrientationFaceTile [0 0]`
- `StartOffMap 1`

---

### SpearGuy (`SpearGuy`)
> *(No Description)*

**Core Stats:** HP: `30`, Move: `?`

**Properties:** `tag: blob`, `faction: enemies`, `exclude_from_hallucinate: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `SpearPokeTest` | **can_get_bonus:** `true`

---

### Spewer (`Spewer`)
> Will eat pills that heal him and change his form. Spits different kinds of liquids depending on his form.

**Core Stats:** HP: `100`, Move: `4`

**Properties:** `tag: blob`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 2`

**Abilities:** **move:** `DefaultMove` | **attack:** `SpewerLobbed_Normal` | **spells:** SpewerTransformNormal, SpewerTransformFire, SpewerTransformTar, SpewerSuckNormal, SpewerSuckTar, SpewerSuckLava, SpewerSuckPill, SpewerBarf_Normal, SpewerBarf_Tar, SpewerBarf_Lava

**Passives:**
- `GoopWalk 1`
- `GoopImmunity 1`

---

### Spinnerette (`SpiderQueen`)
> Does a bite attack. Has a chance to spawn Spiderlings when damaged. Enrages when hit from behind. Can spawn Spider Cats.

**Core Stats:** HP: `250`, Move: `3`, Str: `10`

**Properties:** `tag: bug`, `faction: enemies`, `type: boss`, `mana_regen: 999`, `mana: 100`, `takes_main_turn: false`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicBigMelee` | **spells:** Leave, SpiderSpawn, QueenWeb, QueenMinis, Spider_GoInsane, Spider_CalmDown, SpiderReturn, ButtWeb, ButtWeb_AlreadyEnraged, ExtraMove

**Passives:**
- `Trample 3`
- `StatusImmunity Webbed`

---

### Stacy #{stacy_number} (`Stacy2p0`)
> Its melee attack inflicts Charm. Can heal and grant All Stats Up to its allies.

**Core Stats:** HP: `11`, Move: `?`, Spd: `3`

**Properties:** `tag: cat`, `type: cat`, `faction: enemies`, `base_mana_regen: 999`

**Abilities:** **move:** `DefaultMove` | **attack:** `StacyCharm` | **spells:** StacyHeal

---

### Stacy Mutant (`StacyMutant`)
> ???

**Core Stats:** HP: `125`, Move: `?`

**Properties:** `tag: cat`, `type: boss`, `faction: enemies`, `base_mana_regen: 999`, `evenly_dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** SM_MagicMissile, SM_Flamethrower, SM_IceShards, SM_LightningStorm, SM_BleedCounter

---

### StemCat_HalfHealth (`StemCat_HalfHealth`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `initial_health: 4`

---

### Steven (`BigSlimeX`)
> Melee attacker. Splits into 4 medium Stevens on death.

**Core Stats:** HP: `64`, Move: `4`, Str: `10`, Dex: `6`, Con: `6`, Int: `6`, Spd: `6`, Cha: `6`

**Properties:** `tag: blob`, `hidden_tag: riftheadguardian`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`, `corpse_health: 0`, `size: 2x2`, `move_block: everything_even_when_dead`, `banned_elite_buffs: [Shielded1 Shielded2 Shielded3 Shielded4]`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicBigMelee`

**Passives:**
- `Trample 3`
- `Divide4OnDeath MedSlimeX`

---

### Steven (`MedSlimeX`)
> Melee attacker. Splits into 4 small Stevens on death.

**Core Stats:** HP: `16`, Move: `3`, Dex: `3`, Con: `3`, Int: `3`, Spd: `3`, Cha: `3`

**Properties:** `tag: blob`, `hidden_tag: riftheadguardian`, `faction: enemies`, `type: boss`, `corpse_health: 0`, `banned_elite_buffs: [Shielded1 Shielded2 Shielded3 Shielded4]`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `Divide4OnDeath SmallSlimeX`

---

### Steven (`SmallSlimeX`)
> Melee attacker. Becomes a glitch tile on death.

**Core Stats:** HP: `4`, Move: `2`, Str: `2`, Dex: `1`, Con: `1`, Int: `1`, Spd: `1`, Cha: `1`

**Properties:** `tag: blob`, `hidden_tag: riftheadguardian`, `faction: enemies`, `type: boss`, `corpse_health: 0`, `held_coins: [0 1]`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee`

**Passives:**
- `ChangeTileOnPop GlitchTile`

---

### Strange Egg (`AlienEgg`)
> *(No Description)*

**Core Stats:** HP: `1`, Move: `0`

**Properties:** `tag: alien`, `faction: enemies`, `inherit_faction: true`, `kill_required: false`, `corpse_health: 0`, `can_be_overkilled: false`

**Abilities:** **move:** `None` | **attack:** `None`

---

### TCMechSuit (`TCMechSuit`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`, Str: `4`, Dex: `3`

**Passives:**
- `AllSpellsCostActPoints 1`
- `SetSpellCosts 0`

---

### TallSkeletonCatRevived (`TallSkeletonCatRevived`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `exclude_from_hallucinate: true`

---

### Test2x2 (`Test2x2`)
> *(No Description)*

**Core Stats:** HP: `30`, Move: `?`

**Properties:** `tag: blob`, `faction: enemies`, `exclude_from_hallucinate: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `SpearPokeTest` | **can_get_bonus:** `true`

---

### The Bloat (`TheBloat`)
> Does a blood blast when units walk past its sides. Spawns Eyeballs.

**Core Stats:** HP: `250`, Move: `1`

**Properties:** `tag: [blob]`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 1`

**Abilities:** **move:** `DefaultMove` | **attack:** `BloatFrontLaser` | **spells:** BloatSideLaser, BloatLeap, BloatLoseFirstEye, BloatLoseSecondEye

**Passives:**
- `ElementImmune Creep`
- `Trample 3`

---

### The Child (`TheChild`)
> Respice Finem!

**Core Stats:** HP: `400`, Move: `3`

**Properties:** `faction: enemies`, `type: boss`, `tag: [god cat fetus]`, `size: 2x2`, `flying: true`, `move_block: everything_even_when_dead`, `takes_turns: false`, `corpse_health: indestructible`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `None` | **spells:** TheChild_ReleaseBeams, TheChild_TargetBeam, TheChild_Wrath, TheChild_Pulse, TheChild_TransformHoly, TheChild_TransformExplosive, TheChild_TransformBoris

**Passives:**
- `Trample 3`
- `StunImmunity 1`

---

### The Coven (`TheCoven`)
> Attempts to finish its ritual...

**Core Stats:** HP: `350`, Move: `1`

**Properties:** `tag: [humanoid tumor]`, `hidden_tag: the_coven`, `faction: enemies`, `type: boss`, `lock_orientation: [0, -1]`, `initiative: -999`, `size: 3x3`, `move_block: everything_even_when_dead`, `evenly_dispersed_bonus_turns: 1`, `can_be_backstabbed: false`, `knockback_immune: true`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `None` | **attack:** `BasicMelee` | **spells:** CovenRise1, CovenRise2, CovenRise3, CovenRise4, CovenSummon, CovenPestilence, CovenFamine, CovenWar

**Passives:**
- `Trample 3`
- `DemonicGlyphFrames 1`

---

### The Creator (`TheCreator`)
> Nosce te Ipsum!

**Core Stats:** HP: `999`, Move: `0`, Spd: `0`

**Properties:** `faction: enemies`, `type: boss`, `tag: [god humanoid]`, `size: 2x2`, `move_block: everything_even_when_dead`, `knockback_immune: true`, `takes_turns: false`, `lock_orientation: [0 -1]`, `banned_elite_buffs: [Twin Depressing]`

**Abilities:** **move:** `None` | **attack:** `None` | **spells:** TheCreator_SpawnCloneTeam, TheCreator_Reaction, BecomeTheDestroyer

**Passives:**
- `FullBlockEverythingTo0Damage 1`
- `AbilityOnBattleStart_UseAI TheCreator_SpawnCloneTeam`
- `DebuffImmunity 1`
- `BuffImmunity 1`

---

### The Destroyer (`TheDestroyer`)
> Memento Mori!

**Core Stats:** HP: `500`, Move: `3`, Str: `9`

**Properties:** `faction: enemies`, `type: boss`, `tag: [god cat]`, `size: 2x2`, `move_block: everything_even_when_dead`, `dispersed_bonus_turns: 1`, `corpse_health: 0`, `can_be_overkilled: false`, `banned_elite_buffs: [Twin]`, `weak_threshold: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `DestroyerAttack` | **spells:** DestroyerChargeBackflips, DestroyerHolyAttack, DestroyerThrowShield, DestroyerDashAttack, Destroyer2HolyAttack, DestroyerPulse, Destroyer2Pulse, DestroyerDodge, DestroyerBreakShield, DestroyerRaise

**Passives:**
- `Trample 3`

---

### The Father (`MegaGuppy`)
> *(No Description)*

**Core Stats:** HP: `999`, Move: `?`

**Properties:** `faction: enemies`, `type: boss`, `tag: [god cat]`, `size: 1x1`, `initiative: -999`, `move_block: everything_even_when_dead`, `can_be_champion: false`, `lock_orientation: [0 -1]`, `allow_offmap_corpse: true`, `weak_threshold: 0`

**Abilities:** **move:** `None` | **attack:** `None` | **spells:** MegaGuppy_SlamRight, MegaGuppy_SlamLeft, MegaGuppy_TransformHoly, MegaGuppy_TransformExplosive, MegaGuppy_TransformBoris, MegaGuppy_SummonTheChild

**Passives:**
- `StartOffMap 1`
- `InsertIntoBackgroundPlaceholder 1`
- `UseAbility MegaGuppy_SummonTheChild`

---

### The Mother (`MotherTumor`)
> Grabs units and pulls them towards The Mother.

**Core Stats:** HP: `5`, Move: `0`

**Properties:** `tag: [tumor]`, `hidden_tag: [themother]`, `faction: enemies`, `type: boss`, `takes_turns: false`, `corpse_health: 0`, `lock_orientation: [0 -1]`, `can_be_backstabbed: false`, `knockback_immune: true`, `held_coins: 0`, `kill_required: false`, `can_be_elite: false`

**Abilities:** **move:** `None` | **attack:** `None` | **spells:** MotherTumorGrow

**Passives:**
- `StunImmunity 1`

---

### The Mother (`TheMother`)
> The mother will take back what's hers...

**Core Stats:** HP: `450`, Move: `0`, Spd: `0`

**Properties:** `tag: [tumor]`, `hidden_tag: [themother]`, `faction: enemies`, `type: boss`, `size: 3x3`, `move_block: everything_even_when_dead`, `knockback_immune: true`, `evenly_dispersed_bonus_turns: 1`, `boss_minions_runaway: false`, `lock_orientation: [-1 0]`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `None` | **attack:** `SpawnMotherSpike` | **spells:** MotherConsume, TheMother_Birth

**Passives:**
- `PrioritizeFarAwayTargets 10`

---

### The Mother (`MotherSpike`)
> *(No Description)*

**Core Stats:** HP: `10`, Move: `0`

**Properties:** `tag: [tumor]`, `hidden_tag: [themother themotherspike]`, `faction: enemies`, `type: boss`, `visually_spiky: true`, `takes_turns: false`, `corpse_health: 0`, `can_be_backstabbed: false`, `knockback_immune: true`, `held_coins: 0`, `kill_required: false`, `can_be_elite: false`

**Abilities:** **move:** `None` | **attack:** `None`

**Passives:**
- `Thorns 5`

---

### TheDestroyer2 (`TheDestroyer2`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### Throbbing King (`Simon`)
> *(No Description)*

**Core Stats:** HP: `250`, Move: `3`

**Properties:** `tag: blob`, `faction: enemies`, `type: boss`, `mana_regen: 999`, `mana: 100`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicBigMelee` | **spells:** SimonSays_Scatter, SimonSays_ComeHere, SimonSays_GoAway, Simon_Tentacle, Simon_Trash, Simon_Shot

**Passives:**
- `BonusTurnPattern [`
- `]`
- `Trample 3`
- `TransformOnDeath SimonFlopper`

---

### Throbbing King (`SimonFlopper`)
> *(No Description)*

**Core Stats:** HP: `250`, Move: `5`

**Properties:** `tag: blob`, `faction: enemies`, `type: boss`, `mana_regen: 999`, `mana: 100`, `dispersed_bonus_turns: 3`, `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicBigMelee` | **spells:** SimonFlopper_WiggleFake, SimonFlopper_WiggleChance, SimonFlopper_WiggleGuaranteed, SimonFlopper_Tentacle, SimonFlopper_SpawnMinion

**Passives:**
- `Trample 3`

---

### Throbbing King (`ThrobbingKing`)
> Follow his orders! OR ELSE!

**Core Stats:** HP: `460`, Move: `3`

**Properties:** `tag: blob`, `faction: enemies`, `type: boss`, `mana_regen: 999`, `mana: 100`, `corpse_health: 0`, `size: 2x2`, `move_block: everything_even_when_dead`, `dispersed_bonus_turns: 2`, `round_end_bonus_turns: 1`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `TKNG_GutBall` | **spells:** TKNG_Trash, TKNG_Spread, TKNG_Kneel, TKNG_Roulette, TKNG_GoAway, TKNG_DeathExplode

**Passives:**
- `Trample 3`
- `TransformOnDeath ThrobbingKing2`
- `DeathRattle TKNG_DeathExplode`

---

### Throbbing King (`ThrobbingKing2`)
> Oh no, now hes agile!

**Core Stats:** HP: `150`, Move: `5`

**Properties:** `tag: blob`, `faction: enemies`, `type: boss`, `mana_regen: 999`, `mana: 100`, `dispersed_bonus_turns: 2`, `corpse_health: indestructible`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `TKNG_Laser` | **spells:** TKNG_Spawn, TKNG_Hop

**Passives:**
- `MoveWhenDamaged TKNG_Hop`

---

### Throne (`BungaThrone`)
> Built from the bones of his enemies.

**Core Stats:** HP: `0`, Move: `?`

**Properties:** `tag: skeleton`, `faction: none`, `type: object`, `takes_turns: false`, `kill_required: false`, `shield: 100`, `size: 2x2`, `lock_orientation: [-1 0]`, `move_block: everything_even_when_dead`

**Abilities:** **move:** `None` | **attack:** `None`

**Passives:**
- `Trample 3`
- `NoHealthOnlyShield 1`

---

### Toad (`Toad`)
> *(No Description)*

**Core Stats:** HP: `1`, Move: `4`, Str: `2`, Dex: `1`, Con: `2`, Int: `2`, Spd: `4`, Cha: `2`

**Properties:** `tag: animal`, `type: small`, `faction: allies`, `inherit_faction: true`, `view_bugs_as_enemies: true`, `weak_threshold: 0`, `corpse_health: 0`

**Abilities:** **move:** `BasicJump` | **attack:** `BasicHook` | **can_get_bonus:** `true`

---

### Toad2 (`Toad2`)
> *(No Description)*

**Core Stats:** HP: `4`, Move: `?`

**Passives:**
- `ExtraMovePoints 1`

---

### Toadie_Hidden (`Toadie_Hidden`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Passives:**
- `Disguised 1`

---

### Tormentor (`Tormentor`)
> Its demonic runes grant it powers and abilities.

**Core Stats:** HP: `170`, Move: `2`, Str: `8`, Dex: `8`, Con: `8`, Int: `8`, Spd: `8`, Cha: `8`

**Properties:** `tag: demon`, `faction: enemies`, `type: boss`, `flying: true`, `size: 3x3`, `move_block: everything_even_when_dead`, `dispersed_bonus_turns: 0`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** TormentorRuneAbsorb, TormentorBite, TormentorSpawn, TormentorSuck

**Passives:**
- `TormentorHeal 1`
- `UseAbility TormentorRuneAbsorb`
- `DemonicGlyphFrames 1`
- `DemonicGlyphStealer 1`

---

### TrailerCat2 (`TrailerCat2`)
> *(No Description)*

**Core Stats:** HP: `30`, Move: `5`, Str: `6`

**Properties:** `tag: [cat angel]`, `type: cat`, `divine_shield: 1`, `faction: enemies`

**Abilities:** **move:** `BasicJump` | **attack:** `AngelcatWind`

**Passives:**
- `Angel 1`
- `PrioritizeFarAwayTargets 1`

---

### TrailerCat3 (`TrailerCat3`)
> *(No Description)*

**Core Stats:** HP: `30`, Move: `5`, Str: `6`

**Properties:** `tag: [cat angel]`, `type: cat`, `divine_shield: 1`, `faction: enemies`

**Abilities:** **move:** `BasicJump` | **attack:** `AngelcatWind`

**Passives:**
- `Angel 1`
- `PrioritizeFarAwayTargets 1`

---

### TrailerCat4 (`TrailerCat4`)
> *(No Description)*

**Core Stats:** HP: `30`, Move: `5`, Str: `6`

**Properties:** `tag: [cat angel]`, `type: cat`, `divine_shield: 1`, `faction: enemies`

**Abilities:** **move:** `BasicJump` | **attack:** `AngelcatWind`

**Passives:**
- `Angel 1`
- `PrioritizeFarAwayTargets 1`

---

### TrailerCat5 (`TrailerCat5`)
> *(No Description)*

**Core Stats:** HP: `30`, Move: `5`, Str: `6`

**Properties:** `tag: [cat angel]`, `type: cat`, `divine_shield: 1`, `faction: enemies`

**Abilities:** **move:** `BasicJump` | **attack:** `AngelcatWind`

**Passives:**
- `Angel 1`
- `PrioritizeFarAwayTargets 1`

---

### Trampy (`Trampy`)
> Does a series of seemingly random things, but not in a random order! Drunk.

**Core Stats:** HP: `99`, Move: `3`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 3`, `base_crit_chance: 0`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **spells:** TrampyDrink, TrampyDump, TrampySpit, TrampyFleas, TrampySleep

**Passives:**
- `MissChance 20`

---

### Turkey (`Turkey`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### Ultra Ornstein (`UltraOrnstein`)
> *(No Description)*

**Core Stats:** HP: `100`, Move: `?`, Str: `4`, Spd: `7`

**Properties:** `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 3`, `mana_regen: 999`, `mana: 100`

**Abilities:** **move:** `Teleport` | **attack:** `SpearPoke` | **spells:** XLightning, Magnetize

---

### Ultra Smough (`UltraSmough`)
> *(No Description)*

**Core Stats:** HP: `75`, Move: `1`

**Properties:** `faction: enemies`, `type: boss`, `size: 2x2`, `move_block: everything_even_when_dead`, `dispersed_bonus_turns: 2`, `mana_regen: 999`, `mana: 100`

**Abilities:** **move:** `DefaultMove` | **attack:** `HammerSmash` | **spells:** SpawnJunk, FatLeap

**Passives:**
- `Trample 3`

---

### Wall of Cats (`WallOfCats_Wall`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `tag: cat`, `lock_orientation: [-1, 0]`, `faction: none`, `type: boss`, `size: 5x10`, `takes_turns: false`, `inanimate: true`, `knockback_immune: true`, `can_be_backstabbed: false`, `layer: all`, `kill_required: false`, `mouseover_priority: 10`

**Passives:**
- `Wall 1`

---

### Wall of Cats (`WallOfCats_Eye`)
> *(No Description)*

**Core Stats:** HP: `40`, Move: `?`

**Properties:** `tag: cat`, `lock_orientation: [-1, 0]`, `faction: enemies`, `ignore_tiles: true`, `type: boss`, `knockback_immune: true`, `can_be_backstabbed: false`, `kill_required: true`, `disperse_main_turns: true`, `corpse_health: 0`

**Abilities:** **move:** `WallMove` | **attack:** `WallEyeShot`

---

### Wall of Cats (`WallOfCats_Mouth`)
> *(No Description)*

**Core Stats:** HP: `70`, Move: `?`

**Properties:** `tag: cat`, `lock_orientation: [-1, 0]`, `faction: enemies`, `flying: true`, `type: boss`, `size: 2x2`, `knockback_immune: true`, `can_be_backstabbed: false`, `kill_required: true`, `disperse_main_turns: true`, `corpse_health: 0`

**Abilities:** **move:** `WallMove` | **attack:** `WallBlow`

---

### White Rabbit (`WhiteRabbit`)
> What's he do, nibble your bum?

**Core Stats:** HP: `50`, Move: `2`, Str: `3`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `dispersed_bonus_turns: 4`, `dispersed_bonus_turns_consider_initiative: false`, `mana_regen: 999`, `mana: 100`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee_Fighter` | **spells:** ChainDash

---

### Wizard (`Wizard`)
> *(No Description)*

**Core Stats:** HP: `75`, Move: `?`

**Properties:** `faction: enemies`, `type: boss`, `initiative: 999`, `dispersed_bonus_turns: 3`, `mana_regen: 999`, `mana: 100`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicShortRanged` | **spells:** WizSpellShield, WizBlizzard, WizFlamethrower, WizStorm

---

### Wolma Rocksnow (`CaveCatMom`)
> Has a ranged ice attack that inflicts Slow. Can heal its allies. Can throw enemies to her allies.

**Core Stats:** HP: `60`, Move: `3`

**Properties:** `tag: cat`, `hidden_tag: cavefamily`, `type: boss`, `base_mana_regen: 999`, `faction: enemies`, `disperse_main_turns: true`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `CaveMom_Basic` | **spells:** CaveMom_TossDad, CaveMom_TossElsewhere, CaveMom_Heal, CaveCatEnrageOne, CaveCatEnrageTwo

**Passives:**
- `Buddy CaveCatDad`

---

### Worm (`Worm`)
> Moves away when damaged.

**Core Stats:** HP: `5`, Move: `5`

**Properties:** `tag: worm`, `faction: enemies`

**Abilities:** **move:** `Teleport` | **attack:** `BasicRanged`

**Passives:**
- `MoveWhenDamaged move`

---

### Zapphauser (`LightningElemental`)
> Primes an attack when damaged. Attacks all tiles of the same parity as his own.

**Core Stats:** HP: `125`, Move: `3`, Con: `3`, Spd: `20`

**Properties:** `tag: [elemental]`, `faction: enemies`, `type: boss`, `corpse_health: 0`, `flying: true`, `dispersed_bonus_turns: 3`, `/*elements: [`, `banned_elite_buffs: [Protected]`

**Abilities:** **move:** `Teleport` | **attack:** `LEBurst` | **spells:** LELeave, LEReturn, LEPortFar

**Passives:**
- `ElementImmune Electric`

---

### Zaratana (`Zaratana`)
> Zaratana's body radiates with galactic energy!

**Core Stats:** HP: `600`, Move: `3`

**Properties:** `tag: [kaiju rock]`, `hidden_tag: zaratana`, `faction: enemies`, `type: boss`, `corpse_health: indestructible`, `size: 2x2`, `move_block: everything_even_when_dead`, `evenly_dispersed_bonus_turns: 2`, `dispersed_bonus_turns_before_cats: false`, `initiative: -100`, `mana_regen: 999`, `mana: 100`, `weak_threshold: 150`

**Abilities:** **move:** `DefaultMove` | **attack:** `ZaratanaSoloBasic` | **spells:** ZaratanaSoloMagnet, ZaratanaSoloBombardment, ZaratanaSoloTurtle, ZaratanaSoloRoar, ZaratanaSoloSpinDash, ZaratanaVSRevenge, ZaratanaSoloWeatherRoar, ZaratanaVSExitTurtle

**Passives:**
- `Trample 3`
- `KaijuKnockbackImmune 1`

---

### Zaratana (`ZaratanaVS`)
> She wants to kill Pyrophina!

**Core Stats:** HP: `1000`, Move: `3`

**Properties:** `tag: [kaiju rock]`, `hidden_tag: zaratana`, `faction: kaiju2`, `type: boss`, `corpse_health: indestructible`, `size: 2x2`, `move_block: everything_even_when_dead`, `disperse_main_turns: true`, `dispersed_bonus_turns_before_cats: true`, `mana_regen: 999`, `mana: 100`, `weak_threshold: 150`, `must_start_facing_camera: false`, `banned_elite_buffs: [Twin]`

**Abilities:** **move:** `DefaultMove` | **attack:** `ZaratanaBasic` | **spells:** ZaratanaVSSpinDash, ZaratanaVSWeatherRoar, ZaratanaVSMagnet, ZaratanaVSBombardment, ZaratanaVSTurtle, ZaratanaVSExitTurtle, ZaratanaVSRoar, ZaratanaVSRevenge, ZaratanaVSTurtleGuaranteed

**Passives:**
- `Trample 3`
- `KaijuKnockbackImmune 1`
- `KaijuWinCon zaratana`
- `BonusTurnPattern [`
- `]`

---

### Zaratana (Friendly) (`ZaratanaFamiliar`)
> Shes here to help, and trying her best!

**Core Stats:** HP: `600`, Move: `3`

**Properties:** `tag: [kaiju rock]`, `hidden_tag: zaratana`, `faction: allies`, `inherit_faction: true`, `type: boss`, `corpse_health: indestructible`, `size: 2x2`, `move_block: everything_even_when_dead`, `initiative: -5`, `mana_regen: 999`, `mana: 100`, `weak_threshold: 150`, `ai_scale: .25`

**Abilities:** **move:** `DefaultMove` | **attack:** `ZaratanaSoloBasic` | **spells:** ZaratanaSoloBombardment, ZaratanaVSRevenge

**Passives:**
- `Trample 3`
- `KaijuKnockbackImmune 1`
- `DissuadeInstakills 1`
- `ChanceToDisableActionsIfNotCharmed 75%`

---

### Zodiac (`Zodiac`)
> Will shoot at anything that moves! Limited ammo.

**Core Stats:** HP: `75`, Move: `6`

**Properties:** `tag: cat`, `faction: enemies`, `type: boss`, `mana_regen: 999`, `mana: 100`, `initiative: 1000`

**Abilities:** **move:** `DefaultMove` | **attack:** `ZodiacShoot` | **spells:** Reload

**Passives:**
- `WeaponsDontLoseDurability 1`
- `Ammo 6`

---

### cWaggle (`cWaggle`)
> *(No Description)*

**Core Stats:** HP: `?`, Move: `?`

---

### cWaggle2x2 (`cWaggle2x2`)
> *(No Description)*

**Core Stats:** HP: `18`, Move: `?`, Str: `10`

**Properties:** `size: 2x2`, `move_block: everything_even_when_dead`

**Abilities:** **attack:** `BasicBigMelee`

**Passives:**
- `Trample 3`

---

### cWaggle3x3 (`cWaggle3x3`)
> HOLY FUCKING SHIT

**Core Stats:** HP: `40`, Move: `?`, Str: `15`

**Properties:** `size: 3x3`

---

### {SpawnedBy}'s Crow (`Crow`)
> Inherits its owner's stats. Basic attack modifiers on its owner also get applied to the Crow. Flying.

**Core Stats:** HP: `?`, Move: `?`

**Properties:** `tag: [animal crow]`, `hidden_tag: bird`, `faction: allies`, `inherit_faction: true`, `base_movement: 4`, `base_initiative: 0`, `base_health: 0`, `base_mana: 0`, `base_mana_regen: 0`, `base_health_regen: 0`, `base_initial_mana: 0`, `base_crit_chance: 0`, `mana_matters: true`, `weak_threshold: 5`, `can_collect_coins: true`, `can_eat_food: true`, `access_to_player_inventory: true`, `corpse_health: 1`, `flying: true`

**Abilities:** **move:** `DefaultMove` | **attack:** `BasicMelee` | **can_get_bonus:** `true` | **spells:** CrowFlutter, CrowFlap

**Passives:**
- `InheritSpawnerStats 1`
- `CrowAttackLink 1`
- `Bird CookedChickenLeg`

---

### {organname} (`OrganZodiac`)
> Will shoot at anything that moves! Limited ammo.

**Core Stats:** HP: `80`, Move: `6`

**Properties:** `tag: cat`, `hidden_tag: riftheadguardian`, `faction: enemies`, `type: boss`, `mana_regen: 999`, `mana: 100`, `corpse_health: 0`, `initiative: 1000`, `banned_elite_buffs: [Shielded1 Shielded2 Shielded3 Shielded4]`

**Abilities:** **move:** `DefaultMove` | **attack:** `ZodiacShootX` | **spells:** Reload

**Passives:**
- `Ammo 6`
- `SpawnOnDeath Maggot`
- `SpawnOnDeath Maggot`
- `SpawnOnDeath Maggot`
- `SpawnOnDeath Maggot`

---

