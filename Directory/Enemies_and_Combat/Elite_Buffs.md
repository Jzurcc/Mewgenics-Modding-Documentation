# Enemies and Combat/Elite Buffs Directory

## File: `elite_buffs.gon`

### `Spiky`
**Source:** `elite_buffs.gon`  

```
Spiky {//animated spikes
	value 1
	icon_frame 500
	passives {
		EliteParticle SpikeBuff
		Thorns 2
		EliteTint [.6 .6 .6 .50]
	}
}
```

---

### `Reactive`
**Source:** `elite_buffs.gon`  

```
Reactive {//sparkles
	value 1
	icon_frame 501
	passives {
		EliteParticle SparkleBuff
		KineticSpikes 1
		EliteFlatTint [1.1 1.1 1.1]
	}
}
```

---

### `Damaging`
**Source:** `elite_buffs.gon`  

```
Damaging {//red tint
	value 1
	icon_frame 502
	passives {
		EliteTint red
		DamageUp 2 //todo: for enemies make DamageUp apply to all of their spells
	}
}
```

---

### `Tough`
**Source:** `elite_buffs.gon`  

```
Tough {//grey tint
	value 1
	icon_frame 503
	passives {
		Brace 2
		EliteTint [.4 .4 .4]
	}
}
```

---

### `Shielded1`
**Source:** `elite_buffs.gon`  

```
Shielded1 {
	value 1
	icon_frame 504
	specific_chapter 1
	unique true

	passives {
		EliteTint [.7 .7 1 1]
		HealthMultiplier .8
		NonStackingShield 3
		StatusEachRoundBegin {
			NonStackingShield 3
		}
	}
}
```

---

### `Shielded2`
**Source:** `elite_buffs.gon`  

```
Shielded2 {
	value 1
	icon_frame 504
	specific_chapter 2
	unique true

	passives {
		EliteTint [.7 .7 1 1]
		HealthMultiplier .8
		NonStackingShield 5
		StatusEachRoundBegin {
			NonStackingShield 5
		}
	}
}
```

---

### `Shielded3`
**Source:** `elite_buffs.gon`  

```
Shielded3 {
	value 1
	icon_frame 504
	specific_chapter 3
	unique true

	passives {
		EliteTint [.7 .7 1 1]
		HealthMultiplier .8
		NonStackingShield 7
		StatusEachRoundBegin {
			NonStackingShield 7
		}
	}
}
```

---

### `Shielded4`
**Source:** `elite_buffs.gon`  

```
Shielded4 {
	value 1
	icon_frame 504
	specific_chapter 4
	unique true

	passives {
		EliteTint [.7 .7 1 1]
		HealthMultiplier .8
		NonStackingShield 9
		StatusEachRoundBegin {
			NonStackingShield 9
		}
	}
}
```

---

### `Protected`
**Source:** `elite_buffs.gon`  

```
Protected {//white aura
	icon_frame 505
	value 1
	unique true

	passives {
		EliteFlatTint [1.1 1.1 1.3]
		HealthMultiplier .8
		NonStackingDivineShield 1
		StatusEachTurnEnd {
			NonStackingDivineShield 1
		}
	}
}
```

---

### `Speedy`
**Source:** `elite_buffs.gon`  

```
Speedy {//sped up anis?
	value 1
	icon_frame 506
	passives {
		EliteFlatTint [1.1 1.1 1]
		SpeedUp 4
	}
}
```

---

### `Flaming`
**Source:** `elite_buffs.gon`  

```
Flaming {//flames
	value 1
	icon_frame 507
	unique true

	passives {
		EliteParticle Lava_Distortion
		EliteTint [1 .75 .5 .50]
		ElementImmune Fire
		TileTrail FireTile
		InnateElement Fire
	}
}
```

---

### `Creepy`
**Source:** `elite_buffs.gon`  

```
Creepy { //also: attack deals poison  //green tint
	value 1
	icon_frame 508
	unique true

	passives {
		EliteParticle ToxicBubbles
		EliteTint [.7 1 .7 .50]
		TileTrail CreepTile
		ElementImmune Creep
		AddStatusToBasicAttack {
			Poison 1
		}
	}
}
```

---

### `Static`
**Source:** `elite_buffs.gon`  

```
Static { //electric particles
	value 1
	icon_frame 509
	unique true

	passives {
		EliteParticle PassiveEnergized
		EliteTint [1 1 .7 .50]
		DamageNeighborsAfterMove {
            type spell
            damage 1

            effects {
                VisualFXTile WaterConduct
            }
            elements [
                Electric
            ]
        }
	}
}
```

---

### `Lucky`
**Source:** `elite_buffs.gon`  

```
Lucky { //yellow tiny
	value 1
	icon_frame 510
	passives {
		LuckUp 3
		CritChanceUp 10
		DodgeChance 10%
		SizeScale .8
		EliteTint [.8 1 .7 .50]
	}
}
```

---

### `Bouncy`
**Source:** `elite_buffs.gon`  

```
Bouncy {// bound distortion partcle
	value 1
	unique true
	icon_frame 511
	passives {
		MeleeRevengeDamage {
            knockback 1
        }
		MinimumKnockbackFromAllDamage 1
	}
}
```

---

### `Mirror`
**Source:** `elite_buffs.gon`  

```
Mirror { //todo: exclude this one on enemies that already reflect projectiles (Host) //add shine?
	value 1
	icon_frame 512
	unique true

	passives {
		EliteParticle ShineBuff
		ReflectProjectiles {
            self_damage 2
        }
	}
}
```

---

### `Resonant`
**Source:** `elite_buffs.gon`  

```
Resonant { //purple tint
	value 1
	icon_frame 513
	passives {
		EliteTint [.8 .7 .9 1.5]
		StatusOnEnemyCastSpell {
            AllStatsUp 1
			HealthGain 1
        }
	}
}
```

---

### `Undying`
**Source:** `elite_buffs.gon`  

```
Undying { //death particle
	value 1
	icon_frame 514
	unique true
	requires_corpse true
	minion_alt SubUndying

	passives {
		EliteTint [.3 .25 .3 .75]
		EliteParticle SmokeBuff
		AddCorpseHealth 2
		ChanceToRevive {
			stacks 100
			health 50%
			statuses {
				Zombie 1
			}
		}
	}
}
```

---

### `SubUndying`
**Source:** `elite_buffs.gon`  

```
SubUndying { //death particle
	value 1
	icon_frame 514
	unique true
	requires_corpse true
	rollable false

	passives {
		ChanceToRevive {
			stacks 100
			health 50%
			statuses {
				Zombie 1
			}
		}
	}
}
```

---

### `Healthy`
**Source:** `elite_buffs.gon`  

```
Healthy {//heart partcle
	value 1
	icon_frame 515
	passives {
		EliteTint [1 .7 .7 1]
		HealthRegenUp 3
		AddUnfilledMaxHealth 20
	}
}
```

---

### `Sandy`
**Source:** `elite_buffs.gon`  

```
Sandy {//sand partcle
	value 1
	icon_frame 516
	unique true

	passives {
		EliteParticle SandStormBuff
		DodgeChance 10%
		StatusOnDie {
			StackingSandstorm 1
		}
	}
}
```

---

### `Infested`
**Source:** `elite_buffs.gon`  

```
Infested {//flyswarm
	value 1
	icon_frame 517
	passives {
		EliteParticle FlyBuff
		SpawnOnDeath NonChampionFlySwarm
		AddCorpseHealth -999999
	}
}
```

---

### `Absorbant`
**Source:** `elite_buffs.gon`  

```
Absorbant {//mana suck partcile
	value 1
	icon_frame 518
	unique true

	passives {
		EliteParticle AbsorbBuff
		EliteFlatTint [.6 1 1]
		GlobalManaBurnAura -1
	}
}
```

---

### `Depressing`
**Source:** `elite_buffs.gon`  

```
Depressing { //todo: exclude from forwarding to spawns? //grey cloud
	value 1
	unique true
	icon_frame 519
	minion_alt SlightlyDepressing
	roll_limit 2

	passives {
		EliteTint [.5 .5 .8 1]
		DepressionAura {
			stacks 1
			range global
			aura_effects_allies false
		}
	}
}
```

---

### `SlightlyDepressing`
**Source:** `elite_buffs.gon`  

```
SlightlyDepressing {
	value 1
	unique true
	icon_frame 528
	rollable false

	passives {
		DepressionAura {
			stacks 1
			range 1
			aura_effects_allies false
		}
	}
}
```

---

### `Evolving`
**Source:** `elite_buffs.gon`  

```
Evolving {//colorshifting
	value 1
	icon_frame 520
	passives {
		EliteFlatTint [1.5 1 1.5]
		EliteParticle Lava_Distortion
		StatusEachRoundEnd {
			AddRandomEliteBuff 1
		}
	}
}
```

---

### `Plow`
**Source:** `elite_buffs.gon`  

```
Plow { //blue tint
	value 1
	icon_frame 521
	unique true

	passives {
		EliteTint [.7 .9 1 1]
		Trample 3
        MoveTowardsDamageSource MoveOne
	}
}
```

---

### `Mega`
**Source:** `elite_buffs.gon`  

```
Mega {//XL
	value 1
	icon_frame 522
	unique true

	passives {
		ExtraDispersedTurns -1
		HealthMultiplier 1.5
		AbilityDamageMultiplier 1.5
		RemoveExtraDispersedTurn 1 //immediately remove the extra turn when this buff is applied
		SizeScale 1.2
	}
}
```

---

### `Mad`
**Source:** `elite_buffs.gon`  

```
Mad {//pulse red or madness partciles
	value 1
	icon_frame 523
	unique true

	passives {
		EliteParticle FireExtinguish_Steam
		EliteTint [1 .70 .70]
		ExtraDispersedTurns 1
		PermanentMadness 1
		StatusOnKill {
			AllStatsUp 1
			HealthGain 4
		}
	}
}
```

---

### `Twin`
**Source:** `elite_buffs.gon`  

```
Twin {
	value 1
	icon_frame 524
	unique true
	only_at_battle_start true
	minion_alt SubTwin

	passives {
		SpawnOnBattleStart {
			object twin
			prevent_chain_tag eb_twin
		}
		HealthMultiplier .5
		SizeScale .75
	}
}
```

---

### `SubTwin`
**Source:** `elite_buffs.gon`  

```
SubTwin {
	value 1
	unique true
	icon_frame 524
	rollable false

	passives {
		/*SpawnOnceWhenSettled {
			object twin
			prevent_chain_tag eb_twin
		}*/
		HealthMultiplier .5
		SizeScale .75
	}
}
```

---

### `Hardy`
**Source:** `elite_buffs.gon`  

```
Hardy {
	value 1
	icon_frame 525
	unique true

	passives {
		EliteTint [1 .75 .50 1]
		StunImmunity 1
		SizeScale 1.1
	}
}
```

---

### `Sticky`
**Source:** `elite_buffs.gon`  

```
Sticky {
	value 1
	icon_frame 526
	passives {
		EliteParticle PassiveTar
		EliteFlatTint [.05 .05 .05 .75]
		RevengeDamage {
			effects {
				Tarred 1
			}
		}
	}
}
```

---

## File: `boss_elite_buffs.gon`

### `Spiky`
**Source:** `boss_elite_buffs.gon`  

```
Spiky {
	value 1
	icon_frame 600
	passives {
		Thorns 1
		EliteParticle SpikeBuff
		EliteTint [.6 .6 .6 .50]
	}
}
```

---

### `Reactive`
**Source:** `boss_elite_buffs.gon`  

```
Reactive {
	value 1
	icon_frame 601
	passives {
		KineticSpikes 1
		EliteParticle SparkleBuff
		EliteFlatTint [1.1 1.1 1.1]
	}
}
```

---

### `Damaging`
**Source:** `boss_elite_buffs.gon`  

```
Damaging {
	value 1
	icon_frame 602
	passives {
		EliteTint red
		DamageUp 2
	}
}
```

---

### `Tough`
**Source:** `boss_elite_buffs.gon`  

```
Tough {
	value 1
	icon_frame 603
	passives {
		EliteTint [.4 .4 .4]
		Brace 1
	}
}
```

---

### `Shielded1`
**Source:** `boss_elite_buffs.gon`  

```
Shielded1 {
	value 1
	icon_frame 604
	specific_chapter 1
	unique true

	passives {
		EliteTint [.7 .7 1 1]
		HealthMultiplier .8
		NonStackingShield 4
		StatusEachRoundBegin {
			NonStackingShield 4
		}
	}
}
```

---

### `Shielded2`
**Source:** `boss_elite_buffs.gon`  

```
Shielded2 {
	value 1
	icon_frame 604
	specific_chapter 2
	unique true

	passives {
		EliteTint [.7 .7 1 1]
		HealthMultiplier .8
		NonStackingShield 8
		StatusEachRoundBegin {
			NonStackingShield 8
		}
	}
}
```

---

### `Shielded3`
**Source:** `boss_elite_buffs.gon`  

```
Shielded3 {
	value 1
	icon_frame 604
	specific_chapter 3
	unique true

	passives {
		EliteTint [.7 .7 1 1]
		HealthMultiplier .8
		NonStackingShield 12
		StatusEachRoundBegin {
			NonStackingShield 12
		}
	}
}
```

---

### `Shielded4`
**Source:** `boss_elite_buffs.gon`  

```
Shielded4 {
	value 1
	icon_frame 604
	specific_chapter 4
	unique true

	passives {
		EliteTint [.7 .7 1 1]
		HealthMultiplier .8
		NonStackingShield 16
		StatusEachRoundBegin {
			NonStackingShield 16
		}
	}
}
```

---

### `Protected`
**Source:** `boss_elite_buffs.gon`  

```
Protected {
	value 1
	icon_frame 605
	unique true

	passives {
		EliteFlatTint [1.1 1.1 1.3]
		HealthMultiplier .8
		NonStackingDivineShield 1
		StatusEachTurnEnd {
			NonStackingDivineShield 1
		}
	}
}
```

---

### `Speedy`
**Source:** `boss_elite_buffs.gon`  

```
Speedy {
	value 1
	icon_frame 606
	passives {
		EliteFlatTint [1.1 1.1 1]
		SpeedUp 4
	}
}
```

---

### `Flaming`
**Source:** `boss_elite_buffs.gon`  

```
Flaming {
	value 1
	icon_frame 607
	unique true

	passives {
		EliteParticle Lava_Distortion
		EliteTint [1 .75 .5 .50]
		ElementImmune Fire
		TileTrail FireTile
		InnateElement Fire

		MeleeRevengeDamage {
			effects {
				Burn 1
			}
			elements [
				Fire
			]
		}
	}
}
```

---

### `Static`
**Source:** `boss_elite_buffs.gon`  

```
Static {
	value 1
	icon_frame 609
	unique true

	passives {
		EliteParticle PassiveEnergized
		EliteTint [1 1 .7 .50]
		DamageNeighborsAfterMove {
            type spell
            damage 1

            effects {
                VisualFXTile WaterConduct
            }
            elements [
                Electric
            ]
        }
	}
}
```

---

### `Lucky`
**Source:** `boss_elite_buffs.gon`  

```
Lucky {
	value 1
	icon_frame 610
	passives {
		LuckUp 3
		CritChanceUp 10
		DodgeChance 10%
		EliteTint [.8 1 .7 .50]
	}
}
```

---

### `Bouncy`
**Source:** `boss_elite_buffs.gon`  

```
Bouncy {
	value 1
	icon_frame 611
	unique true

	passives {
		MeleeRevengeDamage {
            knockback 1
        }
		MinimumKnockbackFromAllDamage 1
	}
}
```

---

### `Absorbant`
**Source:** `boss_elite_buffs.gon`  

```
Absorbant {
	value 1
	icon_frame 618
	unique true

	passives {
		EliteParticle AbsorbBuff
		EliteFlatTint [.6 1 1]
		GlobalManaBurnAura -1
	}
}
```

---

### `Depressing`
**Source:** `boss_elite_buffs.gon`  

```
Depressing {
	value 1
	unique true
	icon_frame 619
	minion_alt SlightlyDepressing
	roll_limit 2

	passives {
		EliteTint [.5 .5 .8 1]
		DepressionAura {
			stacks 1
			range global
			aura_effects_allies false
		}
	}
}
```

---

### `SlightlyDepressing`
**Source:** `boss_elite_buffs.gon`  

```
SlightlyDepressing {
	value 1
	unique true
	icon_frame 628
	rollable false

	passives {
		DepressionAura {
			stacks 1
			range 1
			aura_effects_allies false
		}
	}
}
```

---

### `Twin`
**Source:** `boss_elite_buffs.gon`  

```
Twin {
	value 1
	icon_frame 624
	unique true
	only_at_battle_start true
	minion_alt SubTwin

	passives {
		SpawnOnBattleStart {
			object twin
			prevent_chain_tag eb_twin
		}
		HealthMultiplier .5
		SizeScale .75
	}
}
```

---

### `SubTwin`
**Source:** `boss_elite_buffs.gon`  

```
SubTwin {
	value 1
	unique true
	icon_frame 624
	rollable false

	passives {
		/*SpawnOnceWhenSettled {
			object twin
			prevent_chain_tag eb_twin
		}*/
		HealthMultiplier .5
		SizeScale .75
	}
}
```

---

### `Hardy`
**Source:** `boss_elite_buffs.gon`  

```
Hardy {
	value 1
	icon_frame 625
	unique true

	passives {
		EliteTint [1 .75 .50 1]
		StunImmunity 1
		SizeScale 1.1
	}
}
```

---

### `Sticky`
**Source:** `boss_elite_buffs.gon`  

```
Sticky {
	value 1
	icon_frame 626

	passives {
		EliteParticle PassiveTar
		EliteFlatTint [.05 .05 .05 .75]
		RevengeDamage {
			effects {
				Tarred 1
			}
		}
	}
}
```

---

