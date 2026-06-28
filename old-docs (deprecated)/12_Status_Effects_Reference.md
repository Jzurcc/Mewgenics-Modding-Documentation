# Mewgenics Mod Developer Documentation: Status Effects & Keywords Reference

This reference extracts all Status Effects and Tooltip Keywords natively defined in the engine. Note: Internal mechanics like max stacks or decay modes are hardcoded in the C# engine and are not exposed to modders via `.gon` files.

| Keyword ID | Display Name | In-Game Description |
|---|---|---|
| `Adrenaline` | **Adrenaline** | Keeps Exhaustion at 0. +25% Crit Chance. +25% Block Chance. |
| `AllStatsUp` | **All Stats Up / All Stats Down** | All Stats increased by {stacks} <br><br> All Stats decreased by {absstacks} |
| `AllyDodgeChanceAura` | *(Alias of DodgeChance_Status)* | *(See DodgeChance_Status)* |
| `AllyInfested` | *(Alias of Infested)* | *(See Infested)* |
| `AlphaAllStatsUp` | *(Alias of AllStatsUp)* | *(See AllStatsUp)* |
| `AlphaCat` | **The Alpha** | This is the Alpha. Certain abilities care about this. <br><br> No effects on its own. Only one unit can be The Alpha. Certain spells and abilities provide bonuses for The Alpha. |
| `AlphaDodgeChance` | *(Alias of DodgeChance_Status)* | *(See DodgeChance_Status)* |
| `Ammo` | **Ammo** | {stacks} shots left. |
| `Appeal` | **[img:appeal] Appeal** | Affects the quality of the stray cats that show up each day |
| `Attraction` | **Attraction** | The thing attracting you is gone. Does nothing. <br><br> Moves towards you at the start of its turn. |
| `BackflipWhenTargeted` | **Backflip** | Backflips out of the way the next time it's targeted. |
| `BlastResistance` | **Blast Resistance** | Takes {stacks} less damage from explosions. <br><br> Reduces damage taken from explosions. |
| `Bleed` | **Bleed** | Takes {stacks} damage at the end of the round, then increase Bleed by 1. <br><br> Takes damage at the end of the round, then increase Bleed by 1. |
| `BleedThorns` | **Bleed Thorns** | Deals {stacks} damage and inflicts Bleed {stacks} to units that contact you. <br><br> Deals damage and inflicts Bleed to units that contact you. |
| `BlessingOfPeace` | **Blessing of Peace** | Gain +{stacks} [img:divineshield] at the end of your turn. Lose this when you deal damage. <br><br> Gain [img:divineshield] at the end of your turn. Lose this when you deal damage. |
| `Blind` | **Blind** | 30% miss chance for the next {stacks} turns. <br><br> 30% miss chance. |
| `Bloodzerked` | **Bloodzerked** | When you deal health damage to a bleeding unit, heal that much health. |
| `Blur` | *(Alias of DodgeChance_Status)* | *(See DodgeChance_Status)* |
| `BodyGuard` | **Body Guard** | The next time an ally is targeted, swap places with them first. |
| `BoostDamageAura` | *(Alias of DamageUp)* | *(See DamageUp)* |
| `BoostDamageGlobalAura` | *(Alias of DamageUp)* | *(See DamageUp)* |
| `Bounty` | **Bounty** | Takes 25% extra damage. If killed, gain {stacks} coins. <br><br> Takes 25% extra damage. If killed, gain coins. |
| `Brace` | **Brace** | Takes {stacks} less damage from all sources. <br><br> Reduces all incoming damage. |
| `BraceForEachNeighboringEnemy` | *(Alias of Brace)* | *(See Brace)* |
| `Brittle` | **Brittle** | This item has a 25% chance to break when you take damage. |
| `BrittleDuringElement` | *(Alias of Brittle)* | *(See Brittle)* |
| `Bruise` | **Bruise** | Takes {stacks} more damage from physical sources. <br><br> Increases all incoming physical damage. |
| `Burn` | **Burn** | Takes {stacks} damage at start of its turn, then decrease Burn by 1. <br><br> Takes damage at start of its turn, then decrease Burn by 1. |
| `CapturedFamiliarIcon` | **Captured Familiar** | Was once an enemy, is now on your team. Will follow you to future battles if it doesn't die. |
| `ChampionUpgradeNextMinion` | **Promote** | The next familiar you spawn is upgraded into a [img:champion] Champion. |
| `Charge` | **Charge** | Gains {stacks} mana at the start of its next turn. <br><br> Gains mana at the start of its next turn. |
| `ChargeFists` | **Charge Fists** | Your basic attack emits {stacks} Sparkles until the end of the turn. <br><br> Your basic attack emits Sparkles until the end of the turn. |
| `CharismaUp` | **Charisma Up / Charisma Down** | Charisma increased by {stacks}. Charisma affects max mana and initial mana. <br><br> Charisma decreased by {absstacks}. Charisma affects max mana and initial mana. |
| `CharmAllFlies` | *(Alias of Charmed)* | *(See Charmed)* |
| `Charmed` | **Charmed** | It's brainwashed! <br><br> Behaves as if it's on your team. |
| `Cleave` | **Cleave** | Cuts a chunk of meat off what it hits. |
| `Comfort` | **[img:comfort] Comfort** | Affects how often cats will breed or fight. |
| `Confusion` | **Confusion** | When performing an action, 33% chance to instead hit itself equal to its strength. Lasts {stacks} turns. <br><br> When performing an action, 33% chance to instead hit itself equal to its strength. |
| `ConstitutionUp` | **Constitution Up / Constitution Down** | Constitution increased by {stacks}. Constitution affects max health and post-battle health regen. <br><br> Constitution decreased by {absstacks}. Constitution affects max health and post-battle health regen. |
| `CounterNextAttacks` | **Counter Attack** | Attack the next {stacks} things that damage you automatically. |
| `CritChanceUp` | **Crit Chance Up** | Crit Chance increased by {stacks}% |
| `CurrentWeaponAddPoison` | **Poison Lace (Weapon)** | Your weapon inflicts +{stacks} Poison. <br><br> Your weapon inflicts Poison. |
| `Cursed` | **Cursed** | This item cannot be unequipped once equipped. |
| `DamageReductionAura` | *(Alias of Brace)* | *(See Brace)* |
| `DamageUp` | **Damage Up / Damage Down** | Basic attack damage increased by {stacks}. <br><br> Basic attack damage decreased by {absstacks}. |
| `DelayedPain` | **Delayed Pain** | Takes {stacks} damage at the end of its turn. <br><br> Delayed damage is taken all at once at the end of your turn. |
| `DemonicGlyph_Bite` | **Lucifer Rune** | Imbues its owner with an extra turn and the power to Bite |
| `DemonicGlyph_Bounce` | **Chaos Rune** | Imbues its owner with the ability to repel attackers. |
| `DemonicGlyph_Fire` | **Brimstone Rune** | Imbues its owner's basic attack with +2 Damage and +2 Burn. |
| `DemonicGlyph_Movement` | **Hexagram Rune** | Imbues its owner with +1 Movement Range and +3 Trample Damage |
| `DemonicGlyph_Summon` | **Pentagram Rune** | Imbues its owner with an extra turn and the power to Summon |
| `DepressionAura` | *(Alias of AllStatsUp)* | *(See AllStatsUp)* |
| `DexDownAura` | *(Alias of DexterityUp)* | *(See DexterityUp)* |
| `DexterityUp` | **Dexterity Up / Dexterity Down** | Dexterity increased by {stacks}. Dexterity affects ranged attack and ranged ability damage. <br><br> Dexterity decreased by {absstacks}. Dexterity affects ranged attack and ranged ability damage. |
| `DiminishingHealthRegen` | **Health Regen (Diminishing)** | Regen {stacks} health at the end of its turn, then decreases Health Regen by 1. <br><br> Regen health at the end of its turn, then decreases Health Regen by 1. |
| `DivineShield` | **Holy Shield** | Blocks an entire instance of incoming damage. |
| `Dodge` | **Dodge** | Dodges the next {stacks} attacks. <br><br> Dodges the next attack. |
| `DodgeChance_Status` | **Dodge Chance** | Dodge Chance increased by {stacks}%. |
| `Doomed` | **Doomed** | Ticks down at the end of your turn. When it hits 0, Die. |
| `DoubleCast` | **Double Action** | The next ability you use is used an additional time for free. |
| `DoubleCastSpell` | **Double Cast** | The next spell you cast is cast an additional time for free. |
| `DoubleCastSpellThisTurn` | **Double Cast (This Turn)** | The next spell you cast this turn is cast an additional time for free. |
| `Drowsy` | **Drowsy** | Falls asleep at the end of its turn. |
| `DybbukPossessed` | **Possessed by Dybbuk** | This cat is possessed by Dybbuk. Down this cat to exorcise him. |
| `EliteBuff_Absorbant` | **Elite Buff: Absorbent** | Drains all unused mana from units when they end their turn, and deals damage to them equal to the amount of mana drained. |
| `EliteBuff_BossAbsorbant` | *(Alias of EliteBuff_Absorbant)* | *(See EliteBuff_Absorbant)* |
| `EliteBuff_BossBouncy` | *(Alias of EliteBuff_Bouncy)* | *(See EliteBuff_Bouncy)* |
| `EliteBuff_BossDamaging` | *(Alias of EliteBuff_Damaging)* | *(See EliteBuff_Damaging)* |
| `EliteBuff_BossDepressing` | *(Alias of EliteBuff_Depressing)* | *(See EliteBuff_Depressing)* |
| `EliteBuff_BossFlaming` | **Elite Buff: Flaming** | Fire Immune. Leaves a trail of fire. Applies Burn 1 to attackers. |
| `EliteBuff_BossHardy` | *(Alias of EliteBuff_Hardy)* | *(See EliteBuff_Hardy)* |
| `EliteBuff_BossLucky` | *(Alias of EliteBuff_Lucky)* | *(See EliteBuff_Lucky)* |
| `EliteBuff_BossMad` | **Elite Buff: Mad** | Madness. Gains +1 all stats and heals 4 when it gets a kill. |
| `EliteBuff_BossProtected` | *(Alias of EliteBuff_Protected)* | *(See EliteBuff_Protected)* |
| `EliteBuff_BossReactive` | *(Alias of EliteBuff_Reactive)* | *(See EliteBuff_Reactive)* |
| `EliteBuff_BossShielded1` | **Elite Buff: Shielded** | At the start of each round, if it has less than 4 [img:shield], set [img:shield] to 4. -20% max health. |
| `EliteBuff_BossShielded2` | **Elite Buff: Shielded** | At the start of each round, if it has less than 8 [img:shield], set [img:shield] to 8. -20% max health. |
| `EliteBuff_BossShielded3` | **Elite Buff: Shielded** | At the start of each round, if it has less than 12 [img:shield], set [img:shield] to 12. -20% max health. |
| `EliteBuff_BossShielded4` | **Elite Buff: Shielded** | At the start of each round, if it has less than 16 [img:shield], set [img:shield] to 16. -20% max health. |
| `EliteBuff_BossSlightlyDepressing` | *(Alias of EliteBuff_SlightlyDepressing)* | *(See EliteBuff_SlightlyDepressing)* |
| `EliteBuff_BossSpeedy` | *(Alias of EliteBuff_Speedy)* | *(See EliteBuff_Speedy)* |
| `EliteBuff_BossSpiky` | **Elite Buff: Spiky** | +1 Thorns |
| `EliteBuff_BossStatic` | *(Alias of EliteBuff_Static)* | *(See EliteBuff_Static)* |
| `EliteBuff_BossSticky` | *(Alias of EliteBuff_Sticky)* | *(See EliteBuff_Sticky)* |
| `EliteBuff_BossSubTwin` | *(Alias of EliteBuff_Twin)* | *(See EliteBuff_Twin)* |
| `EliteBuff_BossTough` | **Elite Buff: Tough** | +1 Brace |
| `EliteBuff_BossTwin` | *(Alias of EliteBuff_Twin)* | *(See EliteBuff_Twin)* |
| `EliteBuff_Bouncy` | **Elite Buff: Bouncy** | When hit, bounces itself and its attacker apart. |
| `EliteBuff_Creepy` | **Elite Buff: Creepy** | Basic attack inflicts Poison. Leaves a trail of creep. |
| `EliteBuff_Damaging` | **Elite Buff: Damaging** | +2 Damage |
| `EliteBuff_Depressing` | **Elite Buff: Depressing** | While alive, its enemies have -1 to all stats. |
| `EliteBuff_Evolving` | **Elite Buff: Evolving** | At the end of each round, gain a random Elite Buff. |
| `EliteBuff_Flaming` | **Elite Buff: Flaming** | Fire Immune. Leaves a trail of fire. |
| `EliteBuff_Hardy` | **Elite Buff: Hardy** | Immune to stuns. |
| `EliteBuff_Healthy` | **Elite Buff: Healthy** | +3 Health Regen. +20 unfilled max health. |
| `EliteBuff_Infested` | **Elite Buff: Infested** | Spawns a fly swarm when it dies. |
| `EliteBuff_Lucky` | **Elite Buff: Lucky** | +3 [img:lck]. +10% Crit Chance. +10% Dodge Chance. |
| `EliteBuff_Mad` | **Elite Buff: Mad** | Madness. Takes an extra turn per round. Gains +1 all stats and heals 4 when it gets a kill. |
| `EliteBuff_Mega` | **Elite Buff: Mega** | Takes one less turn per round. +50% health and damage |
| `EliteBuff_Mirror` | **Elite Buff: Mirror** | Reflects all projectiles. Takes 2 damage when it reflects a projectile. |
| `EliteBuff_Plow` | **Elite Buff: Plow** | Trample. Moves one space towards attackers when damaged. |
| `EliteBuff_Protected` | **Elite Buff: Protected** | At the end of each turn, set [img:divineshield] to 1 if it had no [img:divineshield]. -20% max health. |
| `EliteBuff_Reactive` | **Elite Buff: Reactive** | +1 Kinetic Spikes |
| `EliteBuff_Resonant` | **Elite Buff: Resonant** | Whenever an enemy casts a spell, gain All Stats Up 1 and heal 1. |
| `EliteBuff_Sandy` | **Elite Buff: Sandy** | +10% Dodge Chance. Starts a sandstorm when it dies. |
| `EliteBuff_Shielded1` | **Elite Buff: Shielded** | At the start of each round, if it has less than 3 [img:shield], set [img:shield] to 3. -20% max health. |
| `EliteBuff_Shielded2` | **Elite Buff: Shielded** | At the start of each round, if it has less than 5 [img:shield], set [img:shield] to 5. -20% max health. |
| `EliteBuff_Shielded3` | **Elite Buff: Shielded** | At the start of each round, if it has less than 7 [img:shield], set [img:shield] to 7. -20% max health. |
| `EliteBuff_Shielded4` | **Elite Buff: Shielded** | At the start of each round, if it has less than 9 [img:shield], set [img:shield] to 9. -20% max health. |
| `EliteBuff_SlightlyDepressing` | **Elite Buff: Slightly Depressing** | While alive, adjacent enemies have -1 to all stats. |
| `EliteBuff_Speedy` | **Elite Buff: Speedy** | +4 [img:spd] |
| `EliteBuff_Spiky` | **Elite Buff: Spiky** | +2 Thorns |
| `EliteBuff_Static` | **Elite Buff: Static** | Arcs 1 electric damage to neighbors whenever it moves. |
| `EliteBuff_Sticky` | **Elite Buff: Sticky** | Anything that contacts or attacks this gets Tarred 1. |
| `EliteBuff_SubTwin` | *(Alias of EliteBuff_Twin)* | *(See EliteBuff_Twin)* |
| `EliteBuff_SubUndying` | **Elite Buff: Undying** | Revives to 50% health at the end of the round. |
| `EliteBuff_Tough` | **Elite Buff: Tough** | +2 Brace |
| `EliteBuff_Twin` | **Elite Buff: Twin** | Half health. Comes with a twin. |
| `EliteBuff_Undying` | **Elite Buff: Undying** | Revives to 50% health at the end of the round. +2 Corpse Health. |
| `EliteUpgradeNextMinion` | **Promote+** | The next familiar you spawn is upgraded into an [img:elite] Elite. |
| `EmptyMind` | **Empty Mind** | Spells are disabled. Whenever it gets a kill, it takes an extra turn. |
| `Enrage` | **[E]** | [N] |
| `EventBounty` | **Bounty** | Hunted by the bounty hunter. |
| `Evolution` | **[img:evolution] Mutation** | Adds a chance for cats to receive random mutations each night. |
| `Exhaustion` | **Exhaustion** | Takes {stacks} unblockable damage at the start of its turn, then increase Exhaustion by 1. Whenever it would gain mana or health, gain {stacks} less mana or health. Combat regen disabled. Cannot be removed. It's time to finish the fight. <br><br> Takes unblockable damage at the start of its turn, then increase Exhaustion by 1. Decreases mana and health gain. Combat regen disabled. |
| `ExtraBasicAttacks_Status` | **Extra Attacks** | Can attack {stacks} extra times each turn. |
| `ExtraBasicMoves_Status` | **Extra Moves** | Can move {stacks} extra times each turn. |
| `Fear` | **Fear** | Moves as far away from enemies as it can at the start of its turn. |
| `FinalBossHitCountdownBoris` | **The Child's Flame** | Counts down every time it gets hit. At 0, releases a pulse. |
| `FinalBossHitCountdownExplosive` | **The Child's Flame** | Counts down every time it gets hit. At 0, unleash a wrath of holy light. |
| `FinalBossHitCountdownHoly` | **The Child's Flame** | Counts down every time it gets hit. At 0, unleash the holy beams. |
| `FireArmor` | **[F]** | [N] |
| `FireArmor2` | **[F]** | [N] |
| `Flammable` | **Flammable** | This item burns up when hit with fire. |
| `FlyDamageIncrease` | *(Alias of DamageUp)* | *(See DamageUp)* |
| `Flying` | **Flying** | Ignores tiles and can pass over units and objects. |
| `Fragile` | **Fragile** | This item breaks when you're downed. |
| `FragileDuringElement` | *(Alias of Fragile)* | *(See Fragile)* |
| `FreeSpell` | **Free Spell** | The next spell you cast costs 0 mana. |
| `Freeze` | **Freeze** | Cannot take damage. Unfreezes at the start of its turn. |
| `GlobalFamiliarDamageBoost` | *(Alias of DamageUp)* | *(See DamageUp)* |
| `GlobalFamiliarMoveBoost` | *(Alias of MovementUp)* | *(See MovementUp)* |
| `Grappled` | **Grappled** | Immobile as long as it's next to the thing that grappled it. |
| `HealRandomInjury` | **Cure Random Injury** | Cure a random injury that was permanently lowering one of your stats, if you have any. |
| `Health` | **[img:health] Health** | Affects lifespan and chance to develop or cure disorders each night |
| `HealthRegenUp` | **Health Regen** | Regenerate {stacks} health at the end of its turn. <br><br> Regenerates health at the end of its turn. |
| `HeatWave` | **Heat Wave** | Heals are reduced by 1. Does not heal after battle. Can be mitigated with water. |
| `HeavierHits` | **Heavier Hits** | Physical damage inflicts Bruise {stacks} this turn. |
| `HeavyHits` | **Heavy Hits** | Basic attack inflicts Bruise {stacks} this turn. |
| `Hex` | **Hex** | Spells cost {stacks} more mana to cast. <br><br> Spells cost more mana to cast. |
| `IceArmor` | **[I]** | [N] |
| `ImbueBleed` | **[I]** | [N] |
| `ImbueKnockOutCoin` | **[I]** | [N] |
| `ImbueManaLeech` | **[I]** | [N] |
| `ImbuePoison` | **[I]** | [N] |
| `ImbueRandomStatDown` | **[I]** | [N] |
| `ImbueWeakness` | **[I]** | [N] |
| `Immobile` | **Immobile** | Cannot move. |
| `Infested` | **Infested** | The things infesting this pop out when it dies, destroying its corpse. |
| `IntelligenceUp` | **Intelligence Up / Intelligence Down** | Intelligence increased by {stacks}. Intelligence affects mana regen. <br><br> Intelligence decreased by {absstacks}. Intelligence affects mana regen. |
| `Invulnerable` | **Invulnerable** | Does not take damage. |
| `KineticSpikes` | **Kinetic Spikes** | When this takes damage, emit {stacks} Sparkles. <br><br> When this takes damage, emit Sparkles. |
| `Knockback` | **[K]** | [N] |
| `LateBloomer` | **Late Bloomer** | Gain All Stats Up 3 in {stacks} turns. |
| `Leech` | **Lifesteal** | Heals you equal to the amount of health damage dealt. |
| `Leeches` | **Leeches** | Drains {stacks} health at the end of the round. <br><br> Drains health from the leeched unit at the end of your turn. |
| `Lifesteal` | **Lifesteal** | The next {stacks} basic attacks you do heal you for the amount of health damage they inflict. <br><br> Your next basic attack heals you for the amount of health damage it inflicts. |
| `LoseShieldNextTurn` | **[L]** | [N] |
| `LowHealthAllyDodgeChanceAura` | *(Alias of DodgeChance_Status)* | *(See DodgeChance_Status)* |
| `LuckUp` | **Luck Up / Luck Down** | Luck increased by {stacks}. Luck affects base crit chance and all randomness. <br><br> Luck decreased by {absstacks}. Luck affects base crit chance and all randomness. |
| `Madness` | **Madness** | Thinks everything is an enemy. Uncontrollable. |
| `MagicWeakness` | **Magic Weakness** | Incoming magic damage has 100% Crit Chance and can't miss. |
| `ManaLeeches` | **Mana Leeches** | Drains {stacks} mana at the end of the round. <br><br> Drains mana from the leeched unit at the end of your turn. |
| `Marked` | **Marked** | Incoming physical damage has 100% Crit Chance, ignores shield, and can't miss. |
| `Meaty` | **Meaty** | Turns into meat when it dies. |
| `Metal` | **Metal** | This item is electrically conductive. |
| `MissChance` | **Miss Chance** | Miss chance increased by {stacks}%. |
| `MoveQuivered` | **Bonus Move** | {stacks} extra basic moves that are saved across turns if unused. |
| `MovementUp` | **Movement Up / Movement Down** | Basic movement range increased by {stacks}. <br><br> Basic movement range decreased by {stacks}. |
| `MutateAfterXTurns` | *(Alias of TransformInXTurns)* | *(See TransformInXTurns)* |
| `Muted` | **Muted** | {stacks} of your spells are disabled until {applier} dies. <br><br> Disables a random spell until the applier is killed. |
| `NextAbilityHeals` | **[N]** | [N] |
| `NextAbilityIncreaseRange` | **[N]** | [N] |
| `NextActionLuckUp` | *(Alias of LuckUp)* | *(See LuckUp)* |
| `NextAttackBonusRange` | **Bonus Range** | Your next basic attack has +{stacks} range. <br><br> Increases the range of your next basic attack. |
| `NextDamageReduceAndHealAllies` | **[N]** | [N] |
| `NextDamageReduceAndPushback` | **[N]** | [N] |
| `NextDamageReduceThisTurn` | **[N]** | [N] |
| `NextMoveRangeIncrease` | **[N]** | [N] |
| `NextSpellHealEqualToMana` | **[N]** | [N] |
| `NextTurnDoubleRangedDamage` | **Double Ranged Damage** | All ranged physical attacks and abilities deal double damage. |
| `NoHealthRegen` | **No Health Regen** | Health won't regen automatically and does not regen at the end of battle. |
| `NoManaRegen` | **No Mana Regen** | Mana won't regen automatically. |
| `NonStackingDivineShield` | *(Alias of DivineShield)* | *(See DivineShield)* |
| `OldStealth` | **[O]** | [N] |
| `OneUseSpellDamageUp` | *(Alias of SpellDamageUp)* | *(See SpellDamageUp)* |
| `Ostracized` | **Ostracized** | Every unit sees this as an enemy and will attack it with priority. |
| `PassiveBrace` | *(Alias of Brace)* | *(See Brace)* |
| `PermanentCharm` | *(Alias of Charmed)* | *(See Charmed)* |
| `PermanentConfusion` | **Confusion** | When performing an action, 33% chance to instead hit itself equal to its strength. |
| `PermanentImmobile` | *(Alias of Immobile)* | *(See Immobile)* |
| `PermanentMadness` | *(Alias of Madness)* | *(See Madness)* |
| `Petrify` | **Petrify** | It's a rock for {stacks} turns. <br><br> Becomes a rock temporarily. |
| `Poison` | **Poison** | Takes {stacks} damage at the start of each of its turns. Incoming healing is less effective but cures 1 Poison. <br><br> Takes damage at the start of every turn. Incoming healing is less effective but cures 1 Poison. |
| `PoisonLace` | **Poison Lace** | Basic attack inflicts +{stacks} Poison. <br><br> Basic attack inflicts Poison. |
| `PoisonThorns` | **Poisonous** | Inflicts Poison {stacks} to units that contact you. <br><br> Inflicts Poison to units that contact you. |
| `Possessed` | **Possessed** | Takes {stacks} extra turns and is uncontrollable and charmed on those turns. <br><br> Takes an extra Charmed turn. |
| `PreEmptiveCounterNextAttacks` | **Preemptive Counter** | Attack the next {stacks} things that target you before they attack you, automatically. <br><br> Attack the next thing that targets you before it attacks you, automatically. |
| `ProbeCharmed` | **Probed** | It's being controlled! Attack it to break the probe! <br><br> Behaves as if it's on your team. Attacks from allies will break the probe. |
| `Quivered` | **Bonus Attack** | {stacks} extra basic attacks that are saved across turns if unused. |
| `RandomInjury` | **Random Injury** | Gain a random injury that lowers one of your stats by 1, permanently. |
| `RandomMagicMissile` | **Sparkle** | A projectile that deals 1 magic damage to a random enemy. |
| `RangeUp` | **Range Up** | Range increased by {stacks}. <br><br> Increases the range of your basic attack and projectile abilities. |
| `Reduce` | **[R]** | [N] |
| `ReduceManaCost` | **Insight** | Spells cost {stacks} less mana to cast. <br><br> Spells cost less mana to cast. |
| `ReduceManaCostExcludeBrainstorm` | **Insight** | Spells cost {stacks} less mana to cast, excluding Brainstorm. <br><br> Spells cost less mana to cast, excluding Brainstorm. (cannot reduce cost to 0). |
| `Reflect` | **Reflect** | Reflects the next {stacks} projectiles you are hit with back at the attacker. |
| `Reload` | **Reload** | This action starts disabled and does not refresh on its own after use. Meet the condition to refresh it. |
| `ReloadB` | **Reload** | This action does not refresh on its own after use. Meet the condition to refresh it. |
| `ReviveNextRound` | **Auto Revive** | Revives at the end of the next round. |
| `Robot` | **Energized** | Takes an extra turn. Cannot be Energized again until after that turn ends. |
| `Rot` | **Rot** | Hatches a Fly at the end of its turn. Damage from worms and bugs always crits against this. |
| `SafeDoomed` | **Doomed** | Ticks down at the end of your turn. When it hits 0, Die (without being injured). |
| `Scrambled` | **Scrambled** | Abilities are scrambled, temporarily. |
| `SerratedClaws` | **Serrated Claws** | Basic attack inflicts +{stacks} Bleed. <br><br> Basic attack inflicts Bleed. |
| `Shield` | **Shield** | [N] <br><br> Blocks incoming damage. |
| `ShortCircuit` | **Short Circuit** | All actions are disabled. Cast Break Circuit to break. |
| `SkipNextTurn` | **[S]** | [N] |
| `Sleep` | **Sleep** | Skip the next {stacks} turns. Being attacked has a chance to wake you up. <br><br> Skip the next turn. Being attacked has a chance to wake you up. |
| `SleepParalysis` | **Sleep (Paralysis)** | You are asleep until your sleep paralysis demon is killed. |
| `Slow` | **Slow** | Movement range is reduced to 2 for the next {stacks} turns. Takes its turn later. <br><br> Movement range is reduced to 2. Takes its turn later. |
| `SoulLink` | **Soul Link** | Whenever a soul linked character loses health, all soul linked characters lose that health as well. |
| `SpdDownAura` | *(Alias of SpeedUp)* | *(See SpeedUp)* |
| `SpeedUp` | **Speed Up / Speed Down** | Speed increased by {stacks}. Speed affects movement range and turn order. <br><br> Speed decreased by {absstacks}. Speed affects movement range and turn order. |
| `SpeedUp_WithoutInitiative` | *(Alias of SpeedUp)* | *(See SpeedUp)* |
| `SpellDamageUp` | **Magic Damage Up** | Magic damage you inflict does {stacks} extra damage. <br><br> Increases any magical damage you deal. |
| `SpellShield` | **[S]** | [N] |
| `SpiderInfested` | **Infested** | The spiders infesting this pop out when it dies, destroying its corpse. |
| `SproutsGrantMovement` | *(Alias of MovementUp)* | *(See MovementUp)* |
| `StatBounty` | **Stat Bounty** | Whoever kills this gets All Stats Up {stacks}. <br><br> Whoever kills this gets All Stats Up. |
| `Stealth` | **Stealth** | 50% Dodge Chance. Lose Stealth when you get hit. |
| `StealthUntilBasicAttack` | **Stealth** | 50% Dodge Chance. Lose Stealth when you get hit or use your basic attack. |
| `Stimulation` | **[img:stimulation] Stimulation** | Affects the quality of newborn kittens. |
| `StrDownAura` | *(Alias of StrengthUp)* | *(See StrengthUp)* |
| `StrengthForEachNeighboringEnemy` | *(Alias of StrengthUp)* | *(See StrengthUp)* |
| `StrengthUp` | **Strength Up / Strength Down** | Strength increased by {stacks}. Strength affects melee attack and melee ability damage. <br><br> Strength decreased by {absstacks}. Strength affects melee attack and melee ability damage. |
| `Stun` | **Stun** | Skip the next {stacks} turns. <br><br> Skip the next turn. |
| `Switcheroo` | **[S]** | [N] |
| `TVBotDie` | **DIE** | It is too late. Win now or die. |
| `TVBotDumb` | **DUMB** | Spells of its enemies are disabled. |
| `TVBotObey` | **OBEY** | Basic attacks of its enemies are disabled. |
| `TVBotStop` | **STOP** | Basic movement of its enemies is disabled. |
| `Tangled` | **Entangled** | Immobile. Use basic attack to break free. |
| `Tarred` | **Tarred** | Speed decreased by {stacks}. Flammable. Speed affects movement range and turn order. <br><br> Decreases speed. Flammable. |
| `Taunted` | **[T]** | [N] |
| `Taunting` | **[T]** | [N] |
| `Tech` | **Tech** | Increases the quality of the next item you craft or the next familiar you spawn. Up to 3 Tech can be used at a time. |
| `TempBackstab` | **Backstab Bonus** | +{stacks}% Backstab Damage this turn. (Plus the default 25% backstab bonus.) <br><br> Increases the damage your Backstabs deal. |
| `TempBonusKnockback` | **Bonus Knockback** | Knockback you inflict is increased by {stacks}. <br><br> [N] |
| `TempBonusKnockbackDamage` | **Bonus Knockback Damage** | Knockback damage you deal is increased by {stacks}. <br><br> [N] |
| `TempCharmed` | *(Alias of Charmed)* | *(See Charmed)* |
| `TempCounterAttack` | **Counter Attack** | Attack things that damage you automatically. |
| `TempCritChanceUp` | *(Alias of CritChanceUp)* | *(See CritChanceUp)* |
| `TempDamageUp` | *(Alias of DamageUp)* | *(See DamageUp)* |
| `TempDexterityUp` | *(Alias of DexterityUp)* | *(See DexterityUp)* |
| `TempInitiativeChange` | **Initiative Up / Initiative Down** | You take your turn earlier in the round. <br><br> You take your turn later in the round. |
| `TempInjuryImmunity` | **Injury Immunity** | Cannot receive Injuries for any reason. Lasts {stacks} turns. |
| `TempManaCostReduction` | **Insight** | Spells cost {stacks} less mana to cast until the end of the turn. <br><br> Spells cost less mana to cast until the end of the turn. |
| `TempMovement` | *(Alias of MovementUp)* | *(See MovementUp)* |
| `TempPreEmptiveCounterAttack` | **Preemptive Counter** | Attack things that target you before they attack you, automatically. |
| `TempRangeUp` | **Range Up (Temporary)** | Range increased by {stacks} until the end of the turn. <br><br> Increases the range of your basic attack and projectile abilities until the end of the turn. |
| `TempSpeedUp` | *(Alias of SpeedUp)* | *(See SpeedUp)* |
| `TempSpellDamageUp` | *(Alias of SpellDamageUp)* | *(See SpellDamageUp)* |
| `TempStrengthUp` | *(Alias of StrengthUp)* | *(See StrengthUp)* |
| `TemporaryItem` | **Temporary Item** | Is lost at the end of the battle. |
| `Thorns` | **Thorns** | Deals {stacks} damage to units that contact you. <br><br> Deals damage to units that contact you. |
| `TilesMovedToCritChance` | **[T]** | [N] |
| `TilesMovedToHealth` | **[T]** | [N] |
| `TilesMovedToMana` | **[T]** | [N] |
| `TilesMovedToNeighborHeal` | **[T]** | [N] |
| `TilesMovedToStrength` | **[T]** | [N] |
| `TowerDefenseStatus` | **Sentry Mode** | The next time an enemy ends its movement in your basic attack range, attack it. |
| `TowerDefenseStatus2` | **Sentry Mode+** | When an enemy ends its movement in your basic attack range, attack it. Lasts {stacks} turns. <br><br> When an enemy ends its movement in your basic attack range, attack it. |
| `TrailBlazer` | **[T]** | [N] |
| `Trample` | **Trample** | [N] <br><br> You can move through other units, damaging and displacing them. |
| `TransformInXTurns` | **Transformation** | Transforms when the timer hits 0. |
| `VeinyBonus` | *(Alias of StrengthUp)* | *(See StrengthUp)* |
| `Weakness` | **Weakness** | -2 [img:dex], -2 [img:str], -2 [img:spd]. Lasts {stacks} turns. <br><br> -2 [img:dex], -2 [img:str], -2 [img:spd], temporarily. |
| `Webbed` | **Webbed** | Immobile. Use basic attack to break free. |
| `Wet` | **Wet** | Wet. |
| `Zombie` | **Zombie** | -2 [img:str]. -2 [img:int]. Takes damage from Holy Element heals. Does not get injured when downed. |
| `divine_shield` | *(Alias of DivineShield)* | *(See DivineShield)* |
| `shield` | *(Alias of Shield)* | *(See Shield)* |
