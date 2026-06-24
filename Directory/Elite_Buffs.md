# Elite Buffs Directory

### `Spiky`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 500 |

<details>
<summary><b>Raw .gon</b></summary>

```
Spiky {
	value 1
	icon_frame 500
	passives {
		EliteParticle SpikeBuff
		Thorns 2
		EliteTint [.6 .6 .6 .50]
	}
}
```

</details>

---

### `Reactive`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 501 |

<details>
<summary><b>Raw .gon</b></summary>

```
Reactive {
	value 1
	icon_frame 501
	passives {
		EliteParticle SparkleBuff
		KineticSpikes 1
		EliteFlatTint [1.1 1.1 1.1]
	}
}
```

</details>

---

### `Damaging`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 502 |

<details>
<summary><b>Raw .gon</b></summary>

```
Damaging {
	value 1
	icon_frame 502
	passives {
		EliteTint red
		DamageUp 2 
	}
}
```

</details>

---

### `Tough`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 503 |

<details>
<summary><b>Raw .gon</b></summary>

```
Tough {
	value 1
	icon_frame 503
	passives {
		Brace 2
		EliteTint [.4 .4 .4]
	}
}
```

</details>

---

### `Shielded1`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 504 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Shielded2`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 504 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Shielded3`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 504 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Shielded4`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 504 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Protected`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 505 |

<details>
<summary><b>Raw .gon</b></summary>

```
Protected {
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

</details>

---

### `Speedy`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 506 |

<details>
<summary><b>Raw .gon</b></summary>

```
Speedy {
	value 1
	icon_frame 506
	passives {
		EliteFlatTint [1.1 1.1 1]
		SpeedUp 4
	}
}
```

</details>

---

### `Flaming`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 507 |

<details>
<summary><b>Raw .gon</b></summary>

```
Flaming {
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

</details>

---

### `Creepy`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 508 |

<details>
<summary><b>Raw .gon</b></summary>

```
Creepy { 
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

</details>

---

### `Static`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 509 |

<details>
<summary><b>Raw .gon</b></summary>

```
Static { 
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

</details>

---

### `Lucky`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 510 |

<details>
<summary><b>Raw .gon</b></summary>

```
Lucky { 
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

</details>

---

### `Bouncy`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 511 |

<details>
<summary><b>Raw .gon</b></summary>

```
Bouncy {
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

</details>

---

### `Mirror`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 512 |

<details>
<summary><b>Raw .gon</b></summary>

```
Mirror { 
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

</details>

---

### `Resonant`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 513 |

<details>
<summary><b>Raw .gon</b></summary>

```
Resonant { 
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

</details>

---

### `Undying`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 514 |

<details>
<summary><b>Raw .gon</b></summary>

```
Undying { 
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

</details>

---

### `SubUndying`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 514 |

<details>
<summary><b>Raw .gon</b></summary>

```
SubUndying { 
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

</details>

---

### `Healthy`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 515 |

<details>
<summary><b>Raw .gon</b></summary>

```
Healthy {
	value 1
	icon_frame 515
	passives {
		EliteTint [1 .7 .7 1]
		HealthRegenUp 3
		AddUnfilledMaxHealth 20
	}
}
```

</details>

---

### `Sandy`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 516 |

<details>
<summary><b>Raw .gon</b></summary>

```
Sandy {
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

</details>

---

### `Infested`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 517 |

<details>
<summary><b>Raw .gon</b></summary>

```
Infested {
	value 1
	icon_frame 517
	passives {
		EliteParticle FlyBuff
		SpawnOnDeath NonChampionFlySwarm
		AddCorpseHealth -999999
	}
}
```

</details>

---

### `Absorbant`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 518 |

<details>
<summary><b>Raw .gon</b></summary>

```
Absorbant {
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

</details>

---

### `Depressing`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 519 |

<details>
<summary><b>Raw .gon</b></summary>

```
Depressing { 
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

</details>

---

### `SlightlyDepressing`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 528 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Evolving`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 520 |

<details>
<summary><b>Raw .gon</b></summary>

```
Evolving {
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

</details>

---

### `Plow`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 521 |

<details>
<summary><b>Raw .gon</b></summary>

```
Plow { 
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

</details>

---

### `Mega`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 522 |

<details>
<summary><b>Raw .gon</b></summary>

```
Mega {
	value 1
	icon_frame 522
	unique true

	passives {
		ExtraDispersedTurns -1
		HealthMultiplier 1.5
		AbilityDamageMultiplier 1.5
		RemoveExtraDispersedTurn 1 
		SizeScale 1.2
	}
}
```

</details>

---

### `Mad`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 523 |

<details>
<summary><b>Raw .gon</b></summary>

```
Mad {
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

</details>

---

### `Twin`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 524 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `SubTwin`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 524 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Hardy`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 525 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Sticky`
**Source:** `elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 526 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Spiky`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 600 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Reactive`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 601 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Damaging`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 602 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Tough`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 603 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Shielded1`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 604 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Shielded2`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 604 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Shielded3`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 604 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Shielded4`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 604 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Protected`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 605 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Speedy`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 606 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Flaming`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 607 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Static`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 609 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Lucky`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 610 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Bouncy`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 611 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Absorbant`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 618 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Depressing`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 619 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `SlightlyDepressing`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 628 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Mad`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 623 |

<details>
<summary><b>Raw .gon</b></summary>

```
Mad {
	value 1
	icon_frame 623
	unique true

	passives {
		PermanentMadness 1
		StatusOnKill {
			AllStatsUp 1
			HealthGain 4
		}
	}
}
```

</details>

---

### `Twin`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 624 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `SubTwin`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 624 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Hardy`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Unique | true |
| Icon Frame | 625 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Sticky`
**Source:** `boss_elite_buffs.gon`  

| Field | Value |
| :--- | :--- |
| Value | 1 |
| Icon Frame | 626 |

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

