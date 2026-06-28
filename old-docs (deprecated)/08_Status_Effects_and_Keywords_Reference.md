# Mewgenics Mod Developer Documentation: Categorized Status Effects & Keywords

This exhaustive list of 294 keys has been programmatically categorized using the Wiki as a dictionary.

## Buffs
| Engine Keyword | In-Game Name | Definition |
| :--- | :--- | :--- |
| `Adrenaline` | Adrenaline | Keeps Exhaustion at 0. <br> +25% Crit Chance. <br> +25% Block Chance. |
| `AllStatsUp` | All Stats Up | All Stats increased by {stacks} <br>---<br> All Stats decreased by {absstacks} |
| `BackflipWhenTargeted` | Backflip | Backflips out of the way the next time it's targeted. |
| `BlastResistance` | Blast Resistance | Takes {stacks} less damage from explosions. <br>---<br> Reduces damage taken from explosions. |
| `BleedThorns` | Bleed Thorns | Deals {stacks} damage and inflicts Bleed {stacks} to units that contact you. <br>---<br> Deals damage and inflicts Bleed to units that contact you. |
| `BlessingOfPeace` | Blessing of Peace | Gain +{stacks} `[img:divineshield]` at the end of your turn. Lose this when you deal damage. <br>---<br> Gain `[img:divineshield]` at the end of your turn. Lose this when you deal damage. |
| `Bloodzerked` | Bloodzerked | When you deal health damage to a bleeding unit, heal that much health. |
| `BodyGuard` | Body Guard | The next time an ally is targeted, swap places with them first. |
| `Brace` | Brace | Takes {stacks} less damage from all sources. <br>---<br> Reduces all incoming damage. |
| `ChampionUpgradeNextMinion` | Promote | The next familiar you spawn is upgraded into a `[img:champion]` Champion. |
| `Charge` | Charge | Gains {stacks} mana at the start of its next turn. <br>---<br> Gains mana at the start of its next turn. |
| `ChargeFists` | Charge Fists | Your basic attack emits {stacks} Sparkles until the end of the turn. <br>---<br> Your basic attack emits a Sparkle until the end of the turn. <br>---<br> Your basic attack emits Sparkles until the end of the turn. |
| `CharismaUp` | Charisma Up | Charisma increased by {stacks}. <br> Charisma affects max mana and initial mana. <br>---<br> Charisma decreased by {absstacks}. <br> Charisma affects max mana and initial mana. <br>---<br> Charisma affects max mana and initial mana. |
| `ConstitutionUp` | Constitution Up | Constitution increased by {stacks}. <br> Constitution affects max health and post-battle health regen. <br>---<br> Constitution decreased by {absstacks}. <br> Constitution affects max health and post-battle health regen. <br>---<br> Constitution affects max health and post-combat health regen. |
| `CounterNextAttacks` | Counter Attack | Attack the next thing that damages you automatically. <br>---<br> Attack the next {stacks} things that damage you automatically. |
| `CritChanceUp` | Crit Chance Up | Crit Chance increased by {stacks}% <br>---<br> Adds Critical Hit chance to physical attacks and spells. Critical hits deal +100% damage. |
| `CurrentWeaponAddPoison` | Poison Lace (Weapon) | Your weapon inflicts +{stacks} Poison. <br>---<br> Your weapon inflicts Poison. |
| `DamageUp` | Damage Up | Basic attack damage increased by {stacks}. <br>---<br> Basic attack damage decreased by {absstacks}. <br>---<br> Increases the damage (or heal) of its basic attack. <br>---<br> Decreases the damage (or heal) of its basic attack. |
| `DexterityUp` | Dexterity Up | Dexterity increased by {stacks}. <br> Dexterity affects ranged attack and ranged ability damage. <br>---<br> Dexterity decreased by {absstacks}. <br> Dexterity affects ranged attack and ranged ability damage. <br>---<br> Dexterity affects ranged attack and ranged ability damage. |
| `DiminishingHealthRegen` | Health Regen (Diminishing) | Regen {stacks} health at the end of its turn, then decreases Health Regen by 1. <br>---<br> Regen health at the end of its turn, then decreases Health Regen by 1. |
| `DodgeChance_Status` | Dodge Chance | Dodge Chance increased by {stacks}%. <br>---<br> Increases Dodge Chance. |
| `DoubleCast` | Double Action | The next ability you use is used an additional time for free. |
| `DoubleCastSpell` | Double Cast | The next spell you cast is cast an additional time for free. |
| `DoubleCastSpellThisTurn` | Double Cast (This Turn) | The next spell you cast this turn is cast an additional time for free. |
| `EliteUpgradeNextMinion` | Promote+ | The next familiar you spawn is upgraded into an `[img:elite]` Elite. |
| `EmptyMind` | Empty Mind | Spells are disabled. Whenever it gets a kill, it takes an extra turn. |
| `ExtraBasicAttacks_Status` | Extra Attacks | Can attack {stacks} extra times each turn. <br>---<br> Can attack an extra time each turn |
| `ExtraBasicMoves_Status` | Extra Moves | Can move {stacks} extra times each turn. <br>---<br> Can move an extra time each turn |
| `FreeSpell` | Free Spell | The next spell you cast costs 0 mana. |
| `HealthRegenUp` | Health Regen | Regenerate {stacks} health at the end of its turn. <br>---<br> Regenerates health at the end of its turn. |
| `HeavyHits` | Heavy Hits | Basic attack inflicts Bruise {stacks} this turn. |
| `IntelligenceUp` | Intelligence Up | Intelligence increased by {stacks}. <br> Intelligence affects mana regen. <br>---<br> Intelligence decreased by {absstacks}. <br> Intelligence affects mana regen. <br>---<br> Intelligence affects mana regen. |
| `KineticSpikes` | Kinetic Spikes | When this takes damage, emit {stacks} Sparkles. <br>---<br> When this takes damage, emit a Sparkle. <br>---<br> When this takes damage, emit Sparkles. |
| `LateBloomer` | Late Bloomer | Gain All Stats Up 3 in {stacks} turns. <br>---<br> Gain All Stats Up 3 next turn. |
| `Leech` | Lifesteal | Heals you equal to the amount of health damage dealt. |
| `Lifesteal` | Lifesteal | The next {stacks} basic attacks you do heal you for the amount of health damage they inflict. <br>---<br> Your next basic attack heals you for the amount of health damage it inflicts. |
| `LuckUp` | Luck Up | Luck increased by {stacks}. <br> Luck affects base crit chance and all randomness. <br>---<br> Luck decreased by {absstacks}. <br> Luck affects base crit chance and all randomness. <br>---<br> Luck affects base crit chance and all randomness. |
| `MoveQuivered` | Bonus Move | An extra basic move that is saved across turns if unused. <br>---<br> {stacks} extra basic moves that are saved across turns if unused. |
| `MovementUp` | Movement Up | Basic movement range increased by {stacks}. <br>---<br> Basic movement range decreased by {stacks}. <br>---<br> Increases your basic movement's range. <br>---<br> Decreases your basic movement's range. |
| `NextAttackBonusRange` | Bonus Range | Your next basic attack has +{stacks} range. <br>---<br> Increases the range of your next basic attack. |
| `NextTurnDoubleRangedDamage` | Double Ranged Damage | All ranged physical attacks and abilities deal double damage. |
| `NoHealthRegen` | No Health Regen | Health won't regen automatically and does not regen at the end of battle. |
| `OldStealth` | OldStealth | *(No specific tooltip text defined)* |
| `PoisonLace` | Poison Lace | Basic attack inflicts +{stacks} Poison. <br>---<br> Basic attack inflicts Poison. |
| `PoisonThorns` | Poisonous | Inflicts Poison {stacks} to units that contact you. <br>---<br> Inflicts Poison to units that contact you. |
| `PreEmptiveCounterNextAttacks` | Preemptive Counter | Attack the next {stacks} things that target you before they attack you, automatically. <br>---<br> Attack the next thing that targets you before it attacks you, automatically. |
| `Quivered` | Bonus Attack | An extra basic attack that is saved across turns if unused. <br>---<br> {stacks} extra basic attacks that are saved across turns if unused. |
| `RangeUp` | Range Up | Range increased by {stacks}. <br>---<br> Increases the range of your basic attack and projectile abilities. |
| `ReduceManaCost` | Insight | Spells cost {stacks} less mana to cast. <br>---<br> Spells cost less mana to cast. |
| `ReduceManaCostExcludeBrainstorm` | Insight | Spells cost {stacks} less mana to cast, excluding Brainstorm. <br>---<br> Spells cost less mana to cast, excluding Brainstorm. (cannot reduce cost to 0). |
| `Reflect` | Reflect | Reflects the next {stacks} projectiles you are hit with back at the attacker. <br>---<br> Reflect the next projectile you're hit with back at the attacker. |
| `ReviveNextRound` | Auto Revive | Revives at the end of the round. <br>---<br> Revives at the end of the next round. |
| `Robot` | Energized | Takes an extra turn. Cannot be Energized again until after that turn ends. |
| `SerratedClaws` | Serrated Claws | Basic attack inflicts +{stacks} Bleed. <br>---<br> Basic attack inflicts Bleed. |
| `SpeedUp` | Speed Up | Speed increased by {stacks}. <br> Speed affects movement range and turn order. <br>---<br> Speed decreased by {absstacks}. <br> Speed affects movement range and turn order. <br>---<br> Speed affects movement range and turn order. |
| `SpellDamageUp` | Magic Damage Up | Magic damage you inflict does {stacks} extra damage. <br>---<br> Increases any magical damage you deal. |
| `Stealth` | Stealth | 50% Dodge Chance. Lose Stealth when you get hit. |
| `StealthUntilBasicAttack` | Stealth | 50% Dodge Chance. Lose Stealth when you get hit or use your basic attack. |
| `StrengthUp` | Strength Up | Strength increased by {stacks}. <br> Strength affects melee attack and melee ability damage. <br>---<br> Strength decreased by {absstacks}. <br> Strength affects melee attack and melee ability damage. <br>---<br> Strength affects melee attack and melee ability damage. |
| `Tech` | Tech | Increases the quality of the next item you craft or the next familiar you spawn. <br> Up to 3 Tech can be used at a time. |
| `TempBackstab` | Backstab Bonus | +{stacks}% Backstab Damage this turn. (Plus the default 25% backstab bonus.) <br>---<br> Increases the damage your Backstabs deal. |
| `TempBonusKnockback` | Bonus Knockback | Knockback you inflict is increased by {stacks}. |
| `TempBonusKnockbackDamage` | Bonus Knockback Damage | Knockback damage you deal is increased by {stacks}. |
| `TempCounterAttack` | Counter Attack | Attack things that damage you automatically. |
| `TempInitiativeChange` | Initiative Up | You take your turn earlier in the round. <br>---<br> You take your turn later in the round. |
| `TempInjuryImmunity` | Injury Immunity | Cannot receive Injuries for any reason. Lasts {stacks} turns. <br>---<br> Cannot receive Injuries for any reason. Lasts 1 turn. <br>---<br> Cannot receive Injuries for any reason. |
| `TempManaCostReduction` | Insight | Spells cost {stacks} less mana to cast until the end of the turn. <br>---<br> Spells cost less mana to cast until the end of the turn. |
| `TempPreEmptiveCounterAttack` | Preemptive Counter | Attack things that target you before they attack you, automatically. |
| `TempRangeUp` | Range Up (Temporary) | Range increased by {stacks} until the end of the turn. <br>---<br> Increases the range of your basic attack and projectile abilities until the end of the turn. |
| `Thorns` | Thorns | Deals {stacks} damage to units that contact you. <br>---<br> Deals damage to units that contact you. |
| `TowerDefenseStatus` | Sentry Mode | The next time an enemy ends its movement in your basic attack range, attack it. |
| `TowerDefenseStatus2` | Sentry Mode+ | When an enemy ends its movement in your basic attack range, attack it. Lasts {stacks} turns. <br>---<br> When an enemy ends its movement in your basic attack range, attack it. |

## Debuffs
| Engine Keyword | In-Game Name | Definition |
| :--- | :--- | :--- |
| `Attraction` | Attraction | The thing attracting you is gone. Does nothing. <br>---<br> Moves towards {applier} at the start of its turn. <br>---<br> Moves towards you at the start of its turn. |
| `Bleed` | Bleed | Takes {stacks} damage at the end of the round, then increase Bleed by 1. <br>---<br> Takes damage at the end of the round, then increase Bleed by 1. |
| `Blind` | Blind | 30% miss chance for the next {stacks} turns. <br>---<br> 30% miss chance for the next turn. <br>---<br> 30% miss chance. |
| `Bounty` | Bounty | Takes 25% extra damage. If killed, gain {stacks} coins. <br>---<br> Takes 25% extra damage. If killed, gain coins. |
| `Bruise` | Bruise | Takes {stacks} more damage from physical sources. <br>---<br> Increases all incoming physical damage. |
| `Burn` | Burn | Takes {stacks} damage at start of its turn, then decrease Burn by 1. <br>---<br> Takes damage at start of its turn, then decrease Burn by 1. |
| `Charmed` | Charmed | It's brainwashed! <br>---<br> Behaves as if it's on your team. |
| `Confusion` | Confusion | When performing an action, 33% chance to instead hit itself equal to its strength. Lasts {stacks} turns. <br>---<br> When performing an action, 33% chance to instead hit itself equal to its strength. |
| `DelayedPain` | Delayed Pain | Takes {stacks} damage at the end of its turn. <br>---<br> Delayed damage is taken all at once at the end of your turn. |
| `DemonicGlyph_Movement` | Hexagram Rune | Imbues its owner with +1 Movement Range and +3 Trample Damage |
| `Doomed` | Doomed | Ticks down at the end of your turn. When it hits 0, Die. |
| `Drowsy` | Drowsy | Falls asleep at the end of its turn. |
| `DybbukPossessed` | Possessed by Dybbuk | This cat is possessed by Dybbuk. Down this cat to exorcise him. |
| `EventBounty` | Bounty | Hunted by the bounty hunter. |
| `Exhaustion` | Exhaustion | Takes {stacks} unblockable damage at the start of its turn, then increase Exhaustion by 1. Whenever it would gain mana or health, gain {stacks} less mana or health. Combat regen disabled. Cannot be removed. It's time to finish the fight. <br>---<br> Takes unblockable damage at the start of its turn, then increase Exhaustion by 1. Decreases mana and health gain. Combat regen disabled. |
| `Fear` | Fear | Moves as far away from enemies as it can at the start of its turn. |
| `Freeze` | Freeze | Cannot take damage. Unfreezes at the start of its turn. |
| `Grappled` | Grappled | Immobile as long as it's next to the thing that grappled it. |
| `HeatWave` | Heat Wave | Heals are reduced by 1. Does not heal after battle. Can be mitigated with water. |
| `Hex` | Hex | Spells cost {stacks} more mana to cast. <br>---<br> Spells cost more mana to cast. |
| `ImbueBleed` | ImbueBleed | Next physical attack inflicts Bleed |
| `ImbuePoison` | ImbuePoison | *(No specific tooltip text defined)* |
| `ImbueWeakness` | ImbueWeakness | *(No specific tooltip text defined)* |
| `Immobile` | Immobile | Cannot move. |
| `Infested` | Infested | The things infesting this pop out when it dies, destroying its corpse. |
| `Leeches` | Leeches | Drains {stacks} health at the end of the round. <br>---<br> Drains {stacks} health at the end of {applier's} turn and gives it to {applier}. <br>---<br> Drains health from the leeched unit at the end of your turn. |
| `Madness` | Madness | Thinks everything is an enemy. Uncontrollable. |
| `MagicWeakness` | Magic Weakness | Incoming magic damage has 100% Crit Chance and can't miss. |
| `ManaLeeches` | Mana Leeches | Drains {stacks} mana at the end of the round. <br>---<br> Drains {stacks} mana at the end of {applier's} turn and gives it to {applier}. <br>---<br> Drains mana from the leeched unit at the end of your turn. |
| `Marked` | Marked | Incoming physical damage has 100% Crit Chance, ignores shield, and can't miss. |
| `Meaty` | Meaty | Turns into meat when it dies. |
| `MissChance` | Miss Chance | Miss chance increased by {stacks}%. <br>---<br> Increases miss chance |
| `Muted` | Muted | One of your spells is disabled until {applier} dies. <br>---<br> {stacks} of your spells are disabled until {applier} dies. <br>---<br> Disables a random spell until the applier is killed. |
| `NoManaRegen` | No Mana Regen | Mana won't regen automatically. |
| `Ostracized` | Ostracized | Every unit sees this as an enemy and will attack it with priority. |
| `PermanentConfusion` | Confusion | When performing an action, 33% chance to instead hit itself equal to its strength. |
| `Petrify` | Petrify | It's a rock for {stacks} turns. <br>---<br> Becomes a rock temporarily. |
| `Poison` | Poison | Takes {stacks} damage at the start of each of its turns. Incoming healing is less effective but cures 1 Poison. <br>---<br> Takes damage at the start of every turn. Incoming healing is less effective but cures 1 Poison. |
| `Possessed` | Possessed | Takes {stacks} extra turns and is uncontrollable and charmed on those turns. <br>---<br> Takes an extra Charmed turn. |
| `ProbeCharmed` | Probed | It's being controlled! Attack it to break the probe! <br>---<br> Behaves as if it's on your team. Attacks from allies will break the probe. |
| `Rot` | Rot | Hatches a Fly at the end of its turn. Damage from worms and bugs always crits against this. |
| `SafeDoomed` | Doomed | Ticks down at the end of your turn. When it hits 0, Die (without being injured). |
| `Scrambled` | Scrambled | Abilities are scrambled, temporarily. |
| `ShortCircuit` | Short Circuit | All actions are disabled. Cast Break Circuit to break. |
| `Sleep` | Sleep | Skip the next {stacks} turns. Being attacked has a chance to wake you up. <br>---<br> Skip the next turn. Being attacked has a chance to wake you up. |
| `SleepParalysis` | Sleep (Paralysis) | You are asleep until your sleep paralysis demon is killed. |
| `Slow` | Slow | Movement range is reduced to 2 for the next {stacks} turns. Takes its turn later. <br>---<br> Movement range is reduced to 2. Takes its turn later. |
| `SoulLink` | Soul Link | Whenever a soul linked character loses health, all soul linked characters lose that health as well. |
| `SpiderInfested` | Infested | The spiders infesting this pop out when it dies, destroying its corpse. |
| `StatBounty` | Stat Bounty | Whoever kills this gets All Stats Up {stacks}. <br>---<br> Whoever kills this gets All Stats Up. |
| `Stun` | Stun | Skip the next {stacks} turns. <br>---<br> Skip the next turn. |
| `Tangled` | Entangled | Immobile. Use basic attack to break free. |
| `Tarred` | Tarred | Speed decreased by {stacks}. Flammable. <br> Speed affects movement range and turn order. <br>---<br> Decreases speed. Flammable. |
| `Weakness` | Weakness | -2 `[img:dex]`, -2 `[img:str]`, -2 `[img:spd]`. Lasts {stacks} turns. <br>---<br> -2 `[img:dex]`, -2 `[img:str]`, -2 `[img:spd]`. Lasts 1 turn. <br>---<br> -2 `[img:dex]`, -2 `[img:str]`, -2 `[img:spd]`, temporarily. |
| `Webbed` | Webbed | Immobile. Use basic attack to break free. |
| `Zombie` | Zombie | -2 `[img:str]`. -2 `[img:int]`. Takes damage from Holy Element heals. Does not get injured when downed. |

## Neutral
| Engine Keyword | In-Game Name | Definition |
| :--- | :--- | :--- |
| `AlphaCat` | The Alpha | This is the Alpha. Certain abilities care about this. <br>---<br> No effects on its own. Only one unit can be The Alpha. Certain spells and abilities provide bonuses for The Alpha. |
| `CapturedFamiliarIcon` | Captured Familiar | Was once an enemy, is now on your team. Will follow you to future battles if it doesn't die. |
| `TransformInXTurns` | Transformation | Transforms when the timer hits 0. |
| `Wet` | Wet | Wet. |

## Elite Effects
| Engine Keyword | In-Game Name | Definition |
| :--- | :--- | :--- |
| `EliteBuff_Absorbant` | Elite Buff: Absorbent | Drains all unused mana from units when they end their turn, and deals damage to them equal to the amount of mana drained. |
| `EliteBuff_BossAbsorbant` | *(Alias of `EliteBuff_Absorbant`)* | Inherits properties and text from `EliteBuff_Absorbant`. |
| `EliteBuff_BossBouncy` | *(Alias of `EliteBuff_Bouncy`)* | Inherits properties and text from `EliteBuff_Bouncy`. |
| `EliteBuff_BossDamaging` | *(Alias of `EliteBuff_Damaging`)* | Inherits properties and text from `EliteBuff_Damaging`. |
| `EliteBuff_BossDepressing` | *(Alias of `EliteBuff_Depressing`)* | Inherits properties and text from `EliteBuff_Depressing`. |
| `EliteBuff_BossFlaming` | Elite Buff: Flaming | Fire Immune. Leaves a trail of fire. Applies Burn 1 to attackers. |
| `EliteBuff_BossHardy` | *(Alias of `EliteBuff_Hardy`)* | Inherits properties and text from `EliteBuff_Hardy`. |
| `EliteBuff_BossLucky` | *(Alias of `EliteBuff_Lucky`)* | Inherits properties and text from `EliteBuff_Lucky`. |
| `EliteBuff_BossMad` | Elite Buff: Mad | Madness. Gains +1 all stats and heals 4 when it gets a kill. |
| `EliteBuff_BossProtected` | *(Alias of `EliteBuff_Protected`)* | Inherits properties and text from `EliteBuff_Protected`. |
| `EliteBuff_BossReactive` | *(Alias of `EliteBuff_Reactive`)* | Inherits properties and text from `EliteBuff_Reactive`. |
| `EliteBuff_BossShielded1` | Elite Buff: Shielded | At the start of each round, if it has less than 4 `[img:shield]`, set `[img:shield]` to 4. -20% max health. |
| `EliteBuff_BossShielded2` | Elite Buff: Shielded | At the start of each round, if it has less than 8 `[img:shield]`, set `[img:shield]` to 8. -20% max health. |
| `EliteBuff_BossShielded3` | Elite Buff: Shielded | At the start of each round, if it has less than 12 `[img:shield]`, set `[img:shield]` to 12. -20% max health. |
| `EliteBuff_BossShielded4` | Elite Buff: Shielded | At the start of each round, if it has less than 16 `[img:shield]`, set `[img:shield]` to 16. -20% max health. |
| `EliteBuff_BossSlightlyDepressing` | *(Alias of `EliteBuff_SlightlyDepressing`)* | Inherits properties and text from `EliteBuff_SlightlyDepressing`. |
| `EliteBuff_BossSpeedy` | *(Alias of `EliteBuff_Speedy`)* | Inherits properties and text from `EliteBuff_Speedy`. |
| `EliteBuff_BossSpiky` | Elite Buff: Spiky | +1 Thorns |
| `EliteBuff_BossStatic` | *(Alias of `EliteBuff_Static`)* | Inherits properties and text from `EliteBuff_Static`. |
| `EliteBuff_BossSticky` | *(Alias of `EliteBuff_Sticky`)* | Inherits properties and text from `EliteBuff_Sticky`. |
| `EliteBuff_BossSubTwin` | *(Alias of `EliteBuff_Twin`)* | Inherits properties and text from `EliteBuff_Twin`. |
| `EliteBuff_BossTough` | Elite Buff: Tough | +1 Brace |
| `EliteBuff_BossTwin` | *(Alias of `EliteBuff_Twin`)* | Inherits properties and text from `EliteBuff_Twin`. |
| `EliteBuff_Bouncy` | Elite Buff: Bouncy | When hit, bounces itself and its attacker apart. |
| `EliteBuff_Creepy` | Elite Buff: Creepy | Basic attack inflicts Poison. Leaves a trail of creep. |
| `EliteBuff_Damaging` | Elite Buff: Damaging | +2 Damage |
| `EliteBuff_Depressing` | Elite Buff: Depressing | While alive, its enemies have -1 to all stats. |
| `EliteBuff_Evolving` | Elite Buff: Evolving | At the end of each round, gain a random Elite Buff. |
| `EliteBuff_Flaming` | Elite Buff: Flaming | Fire Immune. Leaves a trail of fire. |
| `EliteBuff_Hardy` | Elite Buff: Hardy | Immune to stuns. |
| `EliteBuff_Healthy` | Elite Buff: Healthy | +3 Health Regen. +20 unfilled max health. |
| `EliteBuff_Infested` | Elite Buff: Infested | Spawns a fly swarm when it dies. |
| `EliteBuff_Lucky` | Elite Buff: Lucky | +3 `[img:lck]`. +10% Crit Chance. +10% Dodge Chance. |
| `EliteBuff_Mad` | Elite Buff: Mad | Madness. Takes an extra turn per round. Gains +1 all stats and heals 4 when it gets a kill. |
| `EliteBuff_Mega` | Elite Buff: Mega | Takes one less turn per round. +50% health and damage |
| `EliteBuff_Mirror` | Elite Buff: Mirror | Reflects all projectiles. Takes 2 damage when it reflects a projectile. |
| `EliteBuff_Plow` | Elite Buff: Plow | Trample. Moves one space towards attackers when damaged. |
| `EliteBuff_Protected` | Elite Buff: Protected | At the end of each turn, set `[img:divineshield]` to 1 if it had no `[img:divineshield]`. -20% max health. |
| `EliteBuff_Reactive` | Elite Buff: Reactive | +1 Kinetic Spikes |
| `EliteBuff_Resonant` | Elite Buff: Resonant | Whenever an enemy casts a spell, gain All Stats Up 1 and heal 1. |
| `EliteBuff_Sandy` | Elite Buff: Sandy | +10% Dodge Chance. Starts a sandstorm when it dies. |
| `EliteBuff_Shielded1` | Elite Buff: Shielded | At the start of each round, if it has less than 3 `[img:shield]`, set `[img:shield]` to 3. -20% max health. |
| `EliteBuff_Shielded2` | Elite Buff: Shielded | At the start of each round, if it has less than 5 `[img:shield]`, set `[img:shield]` to 5. -20% max health. |
| `EliteBuff_Shielded3` | Elite Buff: Shielded | At the start of each round, if it has less than 7 `[img:shield]`, set `[img:shield]` to 7. -20% max health. |
| `EliteBuff_Shielded4` | Elite Buff: Shielded | At the start of each round, if it has less than 9 `[img:shield]`, set `[img:shield]` to 9. -20% max health. |
| `EliteBuff_SlightlyDepressing` | Elite Buff: Slightly Depressing | While alive, adjacent enemies have -1 to all stats. |
| `EliteBuff_Speedy` | Elite Buff: Speedy | +4 `[img:spd]` |
| `EliteBuff_Spiky` | Elite Buff: Spiky | +2 Thorns |
| `EliteBuff_Static` | Elite Buff: Static | Arcs 1 electric damage to neighbors whenever it moves. |
| `EliteBuff_Sticky` | Elite Buff: Sticky | Anything that contacts or attacks this gets Tarred 1. |
| `EliteBuff_SubTwin` | *(Alias of `EliteBuff_Twin`)* | Inherits properties and text from `EliteBuff_Twin`. |
| `EliteBuff_SubUndying` | Elite Buff: Undying | Revives to 50% health at the end of the round. |
| `EliteBuff_Tough` | Elite Buff: Tough | +2 Brace |
| `EliteBuff_Twin` | Elite Buff: Twin | Half health. Comes with a twin. |
| `EliteBuff_Undying` | Elite Buff: Undying | Revives to 50% health at the end of the round. +2 Corpse Health. |

## Keywords
| Engine Keyword | In-Game Name | Definition |
| :--- | :--- | :--- |
| `Brittle` | Brittle | This item has a 25% chance to break when you take damage. |
| `Cleave` | Cleave | Cuts a chunk of meat off what it hits. |
| `Cursed` | Cursed | This item cannot be unequipped once equipped. |
| `DivineShield` | Holy Shield | Blocks an entire instance of incoming damage. |
| `Flammable` | Flammable | This item burns up when hit with fire. |
| `Flying` | Flying | Ignores tiles and can pass over units and objects. |
| `Fragile` | Fragile | This item breaks when you're downed. |
| `HealRandomInjury` | Cure Random Injury | Cure a random injury that was permanently lowering one of your stats, if you have any. |
| `LoseShieldNextTurn` | LoseShieldNextTurn | *(No specific tooltip text defined)* |
| `Metal` | Metal | This item is electrically conductive. |
| `RandomInjury` | Random Injury | Gain a random injury that lowers one of your stats by 1, permanently. |
| `RandomMagicMissile` | Sparkle | A projectile that deals 1 magic damage to a random enemy. |
| `Reload` | Reload | This action starts disabled and does not refresh on its own after use. Meet the condition to refresh it. |
| `ReloadB` | Reload | This action does not refresh on its own after use. Meet the condition to refresh it. |
| `Shield` | Shield | Blocks incoming damage. |
| `SpellShield` | SpellShield | *(No specific tooltip text defined)* |
| `TVBotDie` | DIE | It is too late. Win now or die. |
| `TVBotDumb` | DUMB | Spells of its enemies are disabled. |
| `TVBotObey` | OBEY | Basic attacks of its enemies are disabled. |
| `TVBotStop` | STOP | Basic movement of its enemies is disabled. |
| `TemporaryItem` | Temporary Item | Is lost at the end of the battle. |
| `Trample` | Trample | You can move through other units, damaging and displacing them. |

## Hidden/Internal Properties
| Engine Keyword | In-Game Name | Definition |
| :--- | :--- | :--- |
| `AllyDodgeChanceAura` | *(Alias of `DodgeChance_Status`)* | Inherits properties and text from `DodgeChance_Status`. |
| `AllyInfested` | *(Alias of `Infested`)* | Inherits properties and text from `Infested`. |
| `AlphaAllStatsUp` | *(Alias of `AllStatsUp`)* | Inherits properties and text from `AllStatsUp`. |
| `AlphaDodgeChance` | *(Alias of `DodgeChance_Status`)* | Inherits properties and text from `DodgeChance_Status`. |
| `Ammo` | Ammo | {stacks} shots left. <br>---<br> Certain abilities require ammo to use. |
| `Appeal` | [img:appeal] Appeal | Affects the quality of the stray cats that show up each day |
| `Blur` | *(Alias of `DodgeChance_Status`)* | Inherits properties and text from `DodgeChance_Status`. |
| `BoostDamageAura` | *(Alias of `DamageUp`)* | Inherits properties and text from `DamageUp`. |
| `BoostDamageGlobalAura` | *(Alias of `DamageUp`)* | Inherits properties and text from `DamageUp`. |
| `BraceForEachNeighboringEnemy` | *(Alias of `Brace`)* | Inherits properties and text from `Brace`. |
| `BrittleDuringElement` | *(Alias of `Brittle`)* | Inherits properties and text from `Brittle`. |
| `CharmAllFlies` | *(Alias of `Charmed`)* | Inherits properties and text from `Charmed`. |
| `Comfort` | [img:comfort] Comfort | Affects how often cats will breed or fight. |
| `DamageReductionAura` | *(Alias of `Brace`)* | Inherits properties and text from `Brace`. |
| `DemonicGlyph_Bite` | Lucifer Rune | Imbues its owner with an extra turn and the power to Bite |
| `DemonicGlyph_Bounce` | Chaos Rune | Imbues its owner with the ability to repel attackers. |
| `DemonicGlyph_Fire` | Brimstone Rune | Imbues its owner's basic attack with +2 Damage and +2 Burn. |
| `DemonicGlyph_Summon` | Pentagram Rune | Imbues its owner with an extra turn and the power to Summon |
| `DepressionAura` | *(Alias of `AllStatsUp`)* | Inherits properties and text from `AllStatsUp`. |
| `DexDownAura` | *(Alias of `DexterityUp`)* | Inherits properties and text from `DexterityUp`. |
| `Dodge` | Dodge | Dodges the next {stacks} attacks. <br>---<br> Dodges the next attack. |
| `Enrage` | Enrage | *(No specific tooltip text defined)* |
| `Evolution` | [img:evolution] Mutation | Adds a chance for cats to receive random mutations each night. |
| `FinalBossHitCountdownBoris` | The Child's Flame | Counts down every time it gets hit. At 0, releases a pulse. |
| `FinalBossHitCountdownExplosive` | The Child's Flame | Counts down every time it gets hit. At 0, unleash a wrath of holy light. |
| `FinalBossHitCountdownHoly` | The Child's Flame | Counts down every time it gets hit. At 0, unleash the holy beams. |
| `FireArmor` | FireArmor | *(No specific tooltip text defined)* |
| `FireArmor2` | FireArmor2 | *(No specific tooltip text defined)* |
| `FlyDamageIncrease` | *(Alias of `DamageUp`)* | Inherits properties and text from `DamageUp`. |
| `FragileDuringElement` | *(Alias of `Fragile`)* | Inherits properties and text from `Fragile`. |
| `GlobalFamiliarDamageBoost` | *(Alias of `DamageUp`)* | Inherits properties and text from `DamageUp`. |
| `GlobalFamiliarMoveBoost` | *(Alias of `MovementUp`)* | Inherits properties and text from `MovementUp`. |
| `Health` | [img:health] Health | Affects lifespan and chance to develop or cure disorders each night |
| `HeavierHits` | Heavier Hits | Physical damage inflicts Bruise {stacks} this turn. |
| `IceArmor` | IceArmor | *(No specific tooltip text defined)* |
| `ImbueKnockOutCoin` | ImbueKnockOutCoin | *(No specific tooltip text defined)* |
| `ImbueManaLeech` | ImbueManaLeech | *(No specific tooltip text defined)* |
| `ImbueRandomStatDown` | ImbueRandomStatDown | *(No specific tooltip text defined)* |
| `Invulnerable` | Invulnerable | Does not take damage. |
| `Knockback` | Knockback | *(No specific tooltip text defined)* |
| `LowHealthAllyDodgeChanceAura` | *(Alias of `DodgeChance_Status`)* | Inherits properties and text from `DodgeChance_Status`. |
| `MutateAfterXTurns` | *(Alias of `TransformInXTurns`)* | Inherits properties and text from `TransformInXTurns`. |
| `NextAbilityHeals` | NextAbilityHeals | *(No specific tooltip text defined)* |
| `NextAbilityIncreaseRange` | NextAbilityIncreaseRange | *(No specific tooltip text defined)* |
| `NextActionLuckUp` | *(Alias of `LuckUp`)* | Inherits properties and text from `LuckUp`. |
| `NextDamageReduceAndHealAllies` | NextDamageReduceAndHealAllies | *(No specific tooltip text defined)* |
| `NextDamageReduceAndPushback` | NextDamageReduceAndPushback | *(No specific tooltip text defined)* |
| `NextDamageReduceThisTurn` | NextDamageReduceThisTurn | *(No specific tooltip text defined)* |
| `NextMoveRangeIncrease` | NextMoveRangeIncrease | *(No specific tooltip text defined)* |
| `NextSpellHealEqualToMana` | NextSpellHealEqualToMana | *(No specific tooltip text defined)* |
| `NonStackingDivineShield` | *(Alias of `DivineShield`)* | Inherits properties and text from `DivineShield`. |
| `OneUseSpellDamageUp` | *(Alias of `SpellDamageUp`)* | Inherits properties and text from `SpellDamageUp`. |
| `PassiveBrace` | *(Alias of `Brace`)* | Inherits properties and text from `Brace`. |
| `PermanentCharm` | *(Alias of `Charmed`)* | Inherits properties and text from `Charmed`. |
| `PermanentImmobile` | *(Alias of `Immobile`)* | Inherits properties and text from `Immobile`. |
| `PermanentMadness` | *(Alias of `Madness`)* | Inherits properties and text from `Madness`. |
| `Reduce` | Reduce | *(No specific tooltip text defined)* |
| `SkipNextTurn` | SkipNextTurn | *(No specific tooltip text defined)* |
| `SpdDownAura` | *(Alias of `SpeedUp`)* | Inherits properties and text from `SpeedUp`. |
| `SpeedUp_WithoutInitiative` | *(Alias of `SpeedUp`)* | Inherits properties and text from `SpeedUp`. |
| `SproutsGrantMovement` | *(Alias of `MovementUp`)* | Inherits properties and text from `MovementUp`. |
| `Stimulation` | [img:stimulation] Stimulation | Affects the quality of newborn kittens. |
| `StrDownAura` | *(Alias of `StrengthUp`)* | Inherits properties and text from `StrengthUp`. |
| `StrengthForEachNeighboringEnemy` | *(Alias of `StrengthUp`)* | Inherits properties and text from `StrengthUp`. |
| `Switcheroo` | Switcheroo | *(No specific tooltip text defined)* |
| `Taunted` | Taunted | *(No specific tooltip text defined)* |
| `Taunting` | Taunting | *(No specific tooltip text defined)* |
| `TempCharmed` | *(Alias of `Charmed`)* | Inherits properties and text from `Charmed`. |
| `TempCritChanceUp` | *(Alias of `CritChanceUp`)* | Inherits properties and text from `CritChanceUp`. |
| `TempDamageUp` | *(Alias of `DamageUp`)* | Inherits properties and text from `DamageUp`. |
| `TempDexterityUp` | *(Alias of `DexterityUp`)* | Inherits properties and text from `DexterityUp`. |
| `TempMovement` | *(Alias of `MovementUp`)* | Inherits properties and text from `MovementUp`. |
| `TempSpeedUp` | *(Alias of `SpeedUp`)* | Inherits properties and text from `SpeedUp`. |
| `TempSpellDamageUp` | *(Alias of `SpellDamageUp`)* | Inherits properties and text from `SpellDamageUp`. |
| `TempStrengthUp` | *(Alias of `StrengthUp`)* | Inherits properties and text from `StrengthUp`. |
| `TilesMovedToCritChance` | TilesMovedToCritChance | *(No specific tooltip text defined)* |
| `TilesMovedToHealth` | TilesMovedToHealth | *(No specific tooltip text defined)* |
| `TilesMovedToMana` | TilesMovedToMana | *(No specific tooltip text defined)* |
| `TilesMovedToNeighborHeal` | TilesMovedToNeighborHeal | *(No specific tooltip text defined)* |
| `TilesMovedToStrength` | TilesMovedToStrength | *(No specific tooltip text defined)* |
| `TrailBlazer` | Trail Blazer | *(No specific tooltip text defined)* |
| `VeinyBonus` | *(Alias of `StrengthUp`)* | Inherits properties and text from `StrengthUp`. |
| `divine_shield` | *(Alias of `DivineShield`)* | Inherits properties and text from `DivineShield`. |
| `shield` | *(Alias of `Shield`)* | Inherits properties and text from `Shield`. |

