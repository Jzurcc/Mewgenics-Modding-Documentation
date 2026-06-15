# Mewgenics Mod Developer Documentation: Exhaustive Player Classes Reference

This file lists all Actives (Attacks/Abilities) and Passives available to each player class, mapped to their internal mechanical engine properties.

## Class: Butcher (`Butcher`)

### Actives & Attacks

#### Bad Gas (`BadGas`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `knockback_mode back_orientation, reverse_target_direction true, aoe_mode custom, custom_aoe [ [-1, 0] ]`
- **Damage/Effects:** `damage 0, type spell, Poison 3, VisualFXTile PoisonPoof`

#### Cleave (`BasicButcherMelee`)
- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction8, max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 5+bonus_melee_damage, Cleave 1`

#### Binge (`Binge`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 2, minimum_spd 1`
- **Target/Shape:** `Default`
- **Damage/Effects:** `SpeedUp -1, ConstitutionUp 1, StrengthUp 1`

#### Blood Magic (`BloodMagic`)
- **Template:** `self_buff`
- **Cost:** `mana 0, act_points 0, charge 1`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5, type none, cant_miss true, ManaGain 5`

#### Body Slam (`BodySlam`)
- **Template:** `jump_attack`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `max_range 2, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, aoe_excludes_self false, restrictions none, X_is current_health`
- **Damage/Effects:** `damage "floor(X*.25)", IgnoreSelf 1`

#### Burp (`Burp`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type status_spell, incidentally_collects_pickups false, ForceMoveAway 1, Rot 1`

#### Butcher (`Butcher`)
- **Template:** `spell`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero`
- **Damage/Effects:** `damage 0, type status_spell, threshold_flat 3, SpawnThingIfHitKills Food, Die 1`

#### Purge (`ButcherPurge`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 2, minimum_con 1`
- **Target/Shape:** `target_mode direction, aoe_mode line, min_aoe 1, max_aoe 1, aoe_considers_character_size true, aoe_excludes_self true, knockback_mode character_to_tile`
- **Damage/Effects:** `damage 1+bonus_ranged_damage, SpawnCreep 1`

#### Cannon Ball! (`CannonBall`)
- **Template:** `jump_attack`
- **Cost:** `mana 4, cantrip true`
- **Target/Shape:** `max_range 20, delayed_trigger true, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, aoe_excludes_self false, restrictions none`
- **Damage/Effects:** `damage 0, IgnoreSelf 1, Stun 1`

#### Chomp (`Chomp`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `hint_can_target_pickups true`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, can_collect_pickups true, Leech 1, StrengthUp 1`

#### Chonkwalk (`Chonkwalk`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5, type melee, cant_miss true, crit_chance -999999, RefreshMovePoints 1`

#### Consume (`Consume`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `target_mode none, max_aoe 20`
- **Damage/Effects:** `damage 0, type none, CollectsPickups 1`

#### Contaminate (`Contaminate`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `max_range 1, restrictions must_have_tag, target_requires_tag pickup`
- **Damage/Effects:** `damage 0, type status_spell, CurrentWeaponAddPoison 1`

#### Cough (`Cough`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Crushinator (`Crushinator`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 20, damage_shield_only true, Stun 1, Cleave 1`

#### Death Wind (`DeathWind`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe X, aoe_considers_character_size true, aoe_excludes_self true, X_is custom`
- **Damage/Effects:** `damage 0, knockback 1, type status_spell, Poison 4`

#### Delicious Scent (`DeliciousScent`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 10`
- **Target/Shape:** `target_mode none, max_aoe 4, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, Attraction 1`

#### Fartoom! (`Fartoom`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `target_mode none, aoe_mode standard, min_aoe 1, max_aoe 1, aoe_considers_character_size true, aoe_excludes_self true, X_is current_health`
- **Damage/Effects:** `damage "floor(X*.25)", knockback "ceil(X*.25/5)", elements [, Explosion, ]`

#### Fire Fart (`FireFart`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe 1, aoe_considers_character_size true, aoe_excludes_self true, X_is custom`
- **Damage/Effects:** `damage 0, type status_spell, Poison 2, Burn 2`

#### Force Feed (`ForceFeed`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 4, type spell, incidentally_collects_pickups false, ConstitutionUp 1, SpeedUp -1`

#### Gib (`Gib`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 3+bonus_melee_ability_damage, SpawnThingIfHitKills Food, SpawnThingIfHitKills Food, SpawnThingIfHitKills Food`

#### Grapnel (`Grapnel`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_range 10, range_mode 8cross`
- **Damage/Effects:** `damage 0, TempTrampleUntilSettled 3`

#### Grill (`Grill`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `max_aoe 0, max_range 20, restrictions [must_have_tag], target_requires_tag food`
- **Damage/Effects:** `damage 0, ChangeTile FireTile, Burn 1`

#### Hog Rush (`HogRush`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_range 100, restrictions [must_be_moveable must_have_tag must_move], target_requires_tag food, trample_allies_too true`
- **Damage/Effects:** `None`

#### Hook Bind (`HookBind`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, Immobile 1`

#### Lighten the Load (`LightenTheLoad`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 2, main_turn_only true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 25, type melee, cant_miss true, crit_chance -999999, TakeExtraTurn 1`

#### Lodge Hook (`LodgeHook`)
- **Template:** `melee_attack`
- **Cost:** `act_points 0, must_have_weapon true, once_per_fight true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type status_spell, Bleed 10, DisableWeapon 1`

#### Lunch Time (`LunchTime`)
- **Template:** `jump_attack`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `max_range 4, min_range 1, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, aoe_excludes_self false, restrictions [aoe_must_be_displaceable must_have_tag must_move], target_requires_tag food`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, IgnoreSelf 1`

#### Monch (`Monch`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `X_is custom`
- **Damage/Effects:** `damage X, Leech 1`

#### Mutilate (`Mutilate`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `multihit_min 3, multihit_max 5`
- **Damage/Effects:** `damage 1, Bleed 1`

#### My Turn! (`MyTurn`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `min_range 1, max_range 20, restrictions [must_have_ally must_have_player_cat]`
- **Damage/Effects:** `damage 0, StealTurn 1`

#### Reflux (`Reflux`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `min_range 1, max_range 2, knockback_mode character_to_tile`
- **Damage/Effects:** `damage 1+bonus_ranged_damage, ChangeTile LavaTile`

#### Regurge (`Regurge`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `min_range 1, max_range 3, restrictions [aoe_must_exist]`
- **Damage/Effects:** `None`

#### Rehook (`Rehook`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `RefreshWeaponAbility 1`

#### Roast (`Roast`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe 2, aoe_considers_character_size true, aoe_excludes_self true`
- **Damage/Effects:** `damage 3, Burn 1`

#### Rough Toss (`RoughToss`)
- **Template:** `throw_attack`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `min_range 3, max_range 4`
- **Damage/Effects:** `damage 7+bonus_melee_ability_damage, blocked_damage 7+bonus_melee_ability_damage`

#### Self Harm (`SelfMutilate`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, type generic_physical, Cleave 1, StrengthUp 2`

#### Sharpen (`Sharpen`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `CurrentWeaponDamageUp 1`

#### Shred (`Shred`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 12`
- **Target/Shape:** `multihit 5`
- **Damage/Effects:** `damage 1`

#### Skull Bash (`SkullBash`)
- **Template:** `dash_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `damage 2+bonus_melee_ability_damage, knockback 5, Stun 1, SelfStun 1`

#### Slice and Dice (`SliceAndDice`)
- **Template:** `dash_attack`
- **Cost:** `infcantrip true, mana 9`
- **Target/Shape:** `aoe_mode cross, knockback_mode character_to_tile, max_range 1`
- **Damage/Effects:** `damage 2+bonus_melee_ability_damage, Cleave 1`

#### Smell Blood (`SmellBlood`)
- **Template:** `self_buff`
- **Cost:** `mana 7, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `SmellBlood 1`

#### Spoil (`Spoil`)
- **Template:** `spell`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero`
- **Damage/Effects:** `damage 0, type status_spell, tag food, Vaporize 1, ObjectOnHitCharacter AllyRotFly`

#### SUCC (`Succ`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `target_mode tile, max_aoe 0, max_range 2, knockback_mode tile_to_character, hint_can_target_pickups true`
- **Damage/Effects:** `damage 0, type none, CollectsPickups 1`

#### Swallow (`Swallow`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_range 1, min_range 1`
- **Damage/Effects:** `damage 0, can_collect_pickups true, CollectsPickups 1, SwallowSmallCharacter 100%`

#### Tainted Offering (`TaintedOffering`)
- **Template:** `jump_attack`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `max_range 20, max_aoe 0, min_aoe 0`
- **Damage/Effects:** `None`

#### Track (`Track`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ability MoveOneTrample, tag food`

#### Tromp (`Tromp`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `range_mode cross, max_range 1, restrictions [must_be_moveable must_move], straight_shot true`
- **Damage/Effects:** `override_trample_damage true, damage 3, Bruise 1, Bruise 1`

#### Trudge (`Trudge`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana X`
- **Target/Shape:** `max_range 4, X_is custom`
- **Damage/Effects:** `None`

#### Yawn (`Tryptophan`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `target_mode none, max_aoe 1`
- **Damage/Effects:** `damage 0, Sleep 1`

#### Vurp (`Vurp`)
- **Template:** `self_buff`
- **Cost:** `mana 4, cantrip true, requires_empty_trinket true, requires_consumed_trinket true, once_per_fight true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Regurge 1`

### Passives

| Passive Name | Internal ID | Description |
| :--- | :--- | :--- |
| **Barbed** | `Barbed` | Your hook deals +1 damage and inflicts Bleed. |
| **Bowling Ball** | `BowlingBall` | Adjacent and diagonal allied cats get the bonus ability Bowl. |
| **Confrontational** | `Confrontational` | When you take damage, trample one tile towards the source of damage. |
| **Duke of Flies** | `DukeOfFlies` | At the end of the battle, all food pickups become allied flies. Allied flies stay with you between battles. |
| **Fresh Meat** | `FreshMeat` | When you eat food, gain +1 [img:str]. |
| **Glutton** | `Glutton` | When a food pickup spawns within 2 tiles of you, move to it. |
| **Grappling Hook** | `GrapplingHook` | Your hook pulls you toward knockback-immune objects. |
| **Gurgitator** | `Gurgitator` | Whenever you heal over your max HP, gain +1 [img:str]. |
| **Hack** | `Hack` | Your basic attack is always critical against enemies with [img:shield]. Your basic attack's critical hits remove buffs from units. |
| **Harpooner** | `Harpooner` | When an enemy moves in range, hook it. |
| **Heave Hook** | `HeaveHook` | Your hook can target tiles. Units pulled by your hook gain trample while being hooked. |
| **Hooked** | `Hooked` | You can use your hook 2 additional times on your turn. |
| **Incubator** | `Incubator` | Whenever you heal over your max HP, spawn a rot fly. |
| **Indigestion** | `Indigestion` | Whenever you heal over your max HP, fart and inflict Poison 3 on adjacent units. |
| **Loose Meat** | `LooseMeat` | When you take damage, spawn a food pickup. |
| **Lord of the Flies** | `LordOfTheFlies` | All flies are Charmed and get +1 Damage. Whenever you inflict Rot, you inflict +1 Rot. |
| **Supersize Me!** | `MainCourse` | Food and scrap pickups you spawn are bigger. |
| **Masochist** | `Masochist` | When you take damage, gain +1 [img:str], [img:con], or [img:spd] at random. |
| **Never Full** | `NeverFull` | You can heal over your max HP. Excess HP is lost between battles. |
| **Rankle** | `PainGain` | When you take damage, gain +2 Temp Damage. |
| **Putrefy** | `Putrefy` | Your basic attack inflicts Rot 1. |
| **Schadenfreude** | `Schadenfreude` | Your [img:str] and [img:con] are increased by 2 for each disorder your party has. |
| **Stompy!** | `Stompy` | You have Trample. Trample damage you deal has Cleave. |
| **Testy** | `Testy` | When you take damage, gain +1 movement range until the end of your turn. |
| **Spin to Win** | `WideSwing` | Your basic attack is a 3x3 tile spin attack with Cleave. |

---

## Class: Cleric (`Medic`)

### Actives & Attacks

#### Adoubment (`Adoubement`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_aoe 0, min_range 1, max_range 2, restrictions must_target_alpha_if_exists, range_bonuses include_alpha`
- **Damage/Effects:** `heal 4, Cleanse 0, AlphaCat 1, RandomStatUp 1`

#### Anoint (`Anoint`)
- **Template:** `melee_spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 0, type spell, DiminishingHealthRegen 2, RandomStatUp 1`

#### Awaken (`Awaken`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 1`
- **Target/Shape:** `aoe_restrictions must_have_corpse_or_sleeping, restrictions aoe_must_exist, max_range 5, max_aoe 0`
- **Damage/Effects:** `heal 1, type spell, can_revive true, RemoveStatus Sleep, RemoveStatus SleepParalysis, RemoveStatus Drowsy`

#### Fury Heal (`Baptism`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `multihit_min 2, multihit_max 6`
- **Damage/Effects:** `heal 2, type spell, incidentally_collects_pickups false, elements [, Holy, Water, ]`

#### Melee Attack / Heal (`BasicMedicMelee`)
- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 5+bonus_melee_damage, ContextualHeal 1`

#### Benediction (`Benediction`)
- **Template:** `spell`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero`
- **Damage/Effects:** `heal 2, elements [, Holy, ]`

#### Blinding Lights (`BlindingLight`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_range 5, max_aoe 2`
- **Damage/Effects:** `damage 0, Blind 1`

#### Booster (`Booster`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `max_aoe 0, max_range 1, min_range 1`
- **Damage/Effects:** `heal 4, type spell, incidentally_collects_pickups false, RandomStatUp 1`

#### Born Again (`BornAgain`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 10`
- **Target/Shape:** `aoe_restrictions must_have_corpse, restrictions aoe_must_exist, max_range 7`
- **Damage/Effects:** `heal 0, type spell, can_revive true, Revive 100%, AllStatsUp 1`

#### Buddy Up (`BuddyUp`)
- **Template:** `jump_attack`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `max_range 20, min_aoe 0, max_aoe 0, aoe_excludes_self true, restrictions [must_be_moveable must_be_adjacent_to_ally]`
- **Damage/Effects:** `damage 0, type none`

#### Call Over (`CallOver`)
- **Template:** `targeted_status`
- **Cost:** `mana 2, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 5, max_aoe 0, restrictions must_have_ally`
- **Damage/Effects:** `damage 0, ForceMoveTowards 1`

#### Chosen Warrior (`ChosenWarrior`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 5, restrictions must_target_alpha_if_exists`
- **Damage/Effects:** `DamageUp 1, status AlphaCat, Quivered 1`

#### Circle of Protection (`CircleOfProtection`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `max_aoe 2, target_mode none, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, DivineShield 1`

#### Cleanse (`Cleanse`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_aoe 0, max_range 5`
- **Damage/Effects:** `damage 0, Cleanse 0`

#### Convert (`Convert`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range level, max_aoe 0`
- **Damage/Effects:** `damage 0, type spell, Charmed 2`

#### Crusade (`Crusade`)
- **Template:** `spell`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero, aoe_restrictions [allies_only]`
- **Damage/Effects:** `damage 0, type status_spell, ForceMoveTowardsEnemies 1`

#### Divine Gift (`DivineGift`)
- **Template:** `self_buff`
- **Cost:** `cantrip true, mana 10-X`
- **Target/Shape:** `X_is custom`
- **Damage/Effects:** `AllStatsUp 1`

#### Divine Protection (`DivineProtection`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 10-X*6`
- **Target/Shape:** `min_range 1, max_range 4, restrictions must_target_alpha_if_exists, X_is alpha_exists`
- **Damage/Effects:** `DivineShield 1, KineticSpikes 1, AlphaCat 1`

#### Emergency (`Emergency`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `target_mode random_closest_tile, max_range 100, restrictions [must_be_moveable must_move must_be_adjacent_to_most_hurt_ally], trample_allies_too true`
- **Damage/Effects:** `None`

#### Enlighten (`Enlighten`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `max_range 5`
- **Damage/Effects:** `type status_spell, FreeSpell 1`

#### Ethereal (`Ethereal`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 16`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 2, DivineShield 4, Shield 3, Brace 1`

#### An Eye for an Eye (`EyeForAnEye`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 2+bonus_melee_ability_damage, Blind 5, Bleed 1, pool eyes_nonrare, slot trinket, temporary false`

#### Friend or Foe (`FriendOrFoe`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_aoe 0, min_range 1, max_range 4`
- **Damage/Effects:** `damage 3, type spell, DamageOrHealConditionally 1`

#### Stand In (`GetDown`)
- **Template:** `swap`
- **Cost:** `mana 2, infcantrip true`
- **Target/Shape:** `max_range 20, restrictions [must_be_swappable aoe_must_exist must_target_alpha_if_exists must_have_animate_character]`
- **Damage/Effects:** `type status_spell, cant_miss true, AlphaCat 1`

#### Grace (`Grace`)
- **Template:** `targeted_status`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `min_range 0, max_range 1`
- **Damage/Effects:** `heal 0, BonusDamage -5, BonusDamage -4, BonusDamage -3, DivineShield 1, GainCoins 1, Shield 2, RandomStatUp 1, RandomStatUp 1`

#### Guardian Angel (`GuardianAngel`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `min_range 1, max_range 4`
- **Damage/Effects:** `AlphaCat 1`

#### Hallowed Ground (`HallowedGround`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 1, max_range 4, restrictions [must_be_empty aoe_must_exist]`
- **Damage/Effects:** `None`

#### Haste (`Haste`)
- **Template:** `spell`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 5+2*level, max_aoe 0`
- **Damage/Effects:** `damage 0, TempSpeedUp 10`

#### Healing Fall (`HealingFall`)
- **Template:** `jump_attack`
- **Cost:** `mana 8, infcantrip true`
- **Target/Shape:** `max_range 4, restrictions [must_be_moveable]`
- **Damage/Effects:** `heal 5, type spell, elements [, Holy, ]`

#### Healing Salve (`HealingSalve`)
- **Template:** `targeted_status`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `min_range 0, max_range 1`
- **Damage/Effects:** `heal 0, HealthRegenUp 1`

#### Heretic Mark (`HereticMark`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 10`
- **Target/Shape:** `max_range 7, max_aoe 0`
- **Damage/Effects:** `damage 0, Ostracized 2`

#### Holy Light (`HolyLight`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 12`
- **Target/Shape:** `max_aoe 1, min_range 1, max_range 5`
- **Damage/Effects:** `damage 10, type spell, DamageOrHealConditionally 1`

#### Holy Weapon (`HolyWeapon`)
- **Template:** `dash_attack`
- **Cost:** `cantrip true, mana 0`
- **Target/Shape:** `X_is custom, max_range X`
- **Damage/Effects:** `raw_damage X, knockback X, show_damage_on_0 true, VisualFX Holyatk`

#### Malaise (`Malaise`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_aoe 1, max_range 4`
- **Damage/Effects:** `damage 0, Weakness 2`

#### Cure Wounds (`MeleeHeal`)
- **Template:** `melee_spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 10, type spell, incidentally_collects_pickups false, elements [, Holy, ]`

#### Open Wounds (`OpenWounds`)
- **Template:** `melee_spell`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, show_damage_on_0 true, type spell, DamageBasedOnMissingHealth 25`

#### Pray (`Pray`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_aoe 0, max_range 6`
- **Damage/Effects:** `damage 0, status LuckUp, stacks 5, turns 1, expires_on_end_turn true`

#### Prayer (`Prayer`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_aoe 2, max_range 6`
- **Damage/Effects:** `heal 2, elements [, Holy, ]`

#### Rally (`Rally`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `min_range 1, max_range 4, max_aoe 0, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, type status_spell, ForceAttack 1`

#### Holy Dash (`RallyCharge`)
- **Template:** `dash_attack`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 5, type spell, RandomStatUp 1`

#### Healing Word (`RangedHeal`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_aoe 0, min_range 1, max_range 3, aoe_excludes_self true`
- **Damage/Effects:** `heal 5, type spell, elements [, Holy, ]`

#### Rebuke (`Rebuke`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 1, max_range 20, min_aoe 0, max_aoe 0`
- **Damage/Effects:** `damage 0, type spell, show_damage_on_0 true, RebukeDamage 1`

#### Reverse Damage (`ReverseDamage`)
- **Template:** `melee_spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 0, type spell, UndoDamage 1`

#### Revive (`Revive`)
- **Template:** `melee_spell`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `aoe_restrictions must_have_corpse, restrictions aoe_must_exist`
- **Damage/Effects:** `heal 0, type spell, can_revive true, Revive 50%, HealRandomInjury 1`

#### Stimulants (`Stimulants`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `target_mode none, max_aoe 1`
- **Damage/Effects:** `damage 0, SpeedUp 2`

#### Swift Servant (`SwiftSanctify`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `min_range 1, max_range 4, restrictions must_target_alpha_if_exists`
- **Damage/Effects:** `MoveQuivered 1, status AlphaCat, MoveQuivered 1`

#### Turn Foe (`TurnFoe`)
- **Template:** `targeted_status`
- **Cost:** `mana 2, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 2, max_aoe 0`
- **Damage/Effects:** `damage 0, ForceMoveAway 1`

#### Wish (`Wish`)
- **Template:** `spell`
- **Cost:** `cantrip true, mana 3`
- **Target/Shape:** `delayed_trigger true, max_aoe 1, min_range 1, max_range 20`
- **Damage/Effects:** `heal 10, type spell, elements [, Holy, ]`

#### Witch Hunt (`WitchHunt`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_range 20, max_aoe 0`
- **Damage/Effects:** `damage 0, StatBounty 1`

#### Wrath of God (`WrathOfGod`)
- **Template:** `spell`
- **Cost:** `mana 10, infcantrip true`
- **Target/Shape:** `target_mode none, max_aoe 20, min_aoe 4`
- **Damage/Effects:** `damage 6, Blind 1, CorpseVaporizer 1`

#### Zealot (`Zealot`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `Default`
- **Damage/Effects:** `DivineShield 1`

### Passives

| Passive Name | Internal ID | Description |
| :--- | :--- | :--- |
| **Alms for the Poor** | `AlmsForThePoor` | When you gain coins, all allies heal +1 HP and gain +1 [img:lck]. |
| **Angelic Inspiration** | `AngelicInspiration` | When you heal an ally, they also gain +2 mana. |
| **Blessed** | `Blessed` | Gain +1 to 2 random stats at the start of each turn. |
| **Blessing of Holy Fire** | `BlessingOfHolyFire` | Holy-element spells deal double damage to enemies instead of healing and inflict Burn 2.  This blessing is lost when you kill a unit. |
| **Blessing of Spirit** | `BlessingOfSpirit` | When you end your turn, you and all allies heal 2 HP and gain 2 mana. This blessing is lost when you cast a spell. |
| **Breath of Life** | `BreathOfLife` | When you heal a downed unit, revive it. |
| **Caretaker** | `Caretaker` | When you heal another unit, heal yourself for half that amount. |
| **Enchanted Relic** | `EnchantedRelic` | Your trinket's passive and active effects are doubled. |
| **Eternal** | `Eternal` | When you are downed for the 1st time each battle, take no injuries and revive with half HP. |
| **Evil Patron** | `EvilPatron` | Your healing abilities deal damage to enemies. Gain +2 range on tile-targeted healing spells. |
| **God Warrior** | `GodWarrior` | When you kill an enemy, gain +1 [img:divineshield]. |
| **Godspeed** | `Godspeed` | When you heal something, gain +2 [img:spd]. |
| **Healing Aura** | `HealingAura` | +1 Health Regeneration Your Health Regeneration also applies to your allies. |
| **Heathens!** | `Heathens` | At the start of the battle, inflict Weakness 3 on all enemies. |
| **Morale Boost** | `MoraleBoost` | Allies gain All Stats Up whenever you kill something. |
| **Natural Healer** | `NaturalHealer` | Your heals heal for 2 extra. |
| **Protect the Weak** | `ProtectTheWeak` | Allies with 5 or fewer HP gain +50% dodge chance. |
| **Purifier** | `Purifier` | Your basic attack removes debuffs from allies. |
| **Ranged Medic** | `RangedMedic` | Your basic attack is a ranged lobbed attack that heals allies and damages enemies. |
| **Sharing is Caring** | `SharingIsCaring` | When you pick up a non-coin pickup, allies gain the same effects. |
| **Thou Shalt Not Covet** | `ThouShaltNotCovet` | When an enemy takes damage from an ability, it drops a random pickup. |
| **Thou Shalt Not Kill** | `ThouShaltNotKill` | When an enemy downs another unit, they take 10 holy damage. |
| **Thou Shalt Obey** | `ThouShaltObey` | At the end of each round, inflict Charm on a random adjacent enemy. |
| **Top Off** | `TopOff` | When you heal another unit over their max HP, you both gain +1 [img:shield]. |
| **Venerated Touch** | `VeneratedTouch` | Your basic attack inflicts Confusion 2 on enemies and gives +2 [img:shield] to allies. |

---

## Class: Collarless (`Colorless`)

### Actives & Attacks

#### BBQ (`BBQ`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_range 2`
- **Damage/Effects:** `None`

#### Barf Ball (`BarfBall`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 5`
- **Damage/Effects:** `raw_damage "(con+1)/2"`

#### Melee Attack (`BasicMelee`)
- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `None`

#### Short Lobbed Shot (`BasicShortLobbed`)
- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 3+bonus_range`
- **Damage/Effects:** `None`

#### Short Shot (`BasicShortRanged`)
- **Template:** `ranged_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 3+bonus_range`
- **Damage/Effects:** `None`

#### Block (`Block`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Shield 2`

#### Blow (`Blow`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe 2, aoe_considers_character_size true, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, knockback 1, elements [, Wind, ]`

#### Blow Kiss (`BlowKiss`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_aoe 0, min_range 1, max_range 20`
- **Damage/Effects:** `heal 1, elements [, Holy, Wind, ]`

#### Boost (`BoostSpellRange`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TempSpellDamageUp 1`

#### Brace (`Brace`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `status Brace, stacks 1, turns 1, expires_on_begin_turn true`

#### Brainstorm (`Brainstorm`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ReduceManaCostExcludeBrainstorm 1`

#### Burgeoning Barrier (`BurgeoningBarrier`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 0, once_per_fight true`
- **Target/Shape:** `X_is turn_count`
- **Damage/Effects:** `Shield "max((X-1)*2, 0)"`

#### Burgeoning Battery (`BurgeoningBattery`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 0, once_per_fight true`
- **Target/Shape:** `X_is turn_count`
- **Damage/Effects:** `ManaGain "max((X-1)*2, 0)"`

#### Burgeoning Blast (`BurgeoningBlast`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 0, once_per_fight true`
- **Target/Shape:** `max_aoe 0, max_range 3, X_is turn_count`
- **Damage/Effects:** `raw_damage "max((X-1)*2, 0)"`

#### Burst (`Burst`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7, once_per_fight true`
- **Target/Shape:** `max_aoe 0, max_range 20`
- **Damage/Effects:** `damage 10`

#### Butt Scoot (`ButtScoot`)
- **Template:** `move`
- **Cost:** `infcantrip true, move_points 0, mana 4`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

#### Buy Catnip (`BuyCatnip`)
- **Template:** `self_buff`
- **Cost:** `cantrip true, mana 0, coins 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ManaGain 10`

#### CPR (`CPR`)
- **Template:** `melee_spell`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `aoe_restrictions must_have_corpse, restrictions aoe_must_exist`
- **Damage/Effects:** `heal 1, type spell, can_revive true`

#### Cat Nap (`CatNap`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Cleanse 0, Sleep 1`

#### Cold Shoulder (`ColdShoulder`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `max_aoe 0, max_range 20`
- **Damage/Effects:** `damage 1, Slow 1`

#### Confusion (`Confusion`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_aoe 0, max_range 3`
- **Damage/Effects:** `damage 0, Confusion 2`

#### Invert (`Contort`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `Default`
- **Damage/Effects:** `SwapHighestAndLowestStat 1`

#### Copycat (`Copycat`)
- **Template:** `self_buff`
- **Cost:** `cant_cast true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

#### Dart (`Dart`)
- **Template:** `straightshot_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_aoe 3+bonus_range`
- **Damage/Effects:** `damage 2, piercing true`

#### Desecrate (`Desecrate`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 0`
- **Target/Shape:** `max_range 20, restrictions must_have_destructible_corpse`
- **Damage/Effects:** `damage 0, cant_miss true, VaporizeCorpse 1`

#### Dexterous Hit (`DexterousHit`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage "(dex+1)/2"`

#### Doll Up (`DollUp`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `Default`
- **Damage/Effects:** `CharismaUp 1`

#### Make a Wish (`Donate`)
- **Template:** `spawn`
- **Cost:** `mana 0, coins 1, cantrip true`
- **Target/Shape:** `target_mode none, aoe_mode square, max_aoe 20, min_targets 1, max_targets 1, aoe_restrictions [must_be_empty]`
- **Damage/Effects:** `None`

#### Dump (`Dump`)
- **Template:** `melee_attack`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `target_mode direction, aoe_mode line, min_aoe 1, max_aoe 1, restrictions [aoe_must_be_displaceable aoe_must_exist]`
- **Damage/Effects:** `damage 0, cant_miss true, incidentally_collects_pickups false, Displace 1, object Poop`

#### Second Wind (`Endeavor`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 8, once_per_fight true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `RefreshMovePoints 1, RefreshActPoints 1, RefreshItemAbilities 1`

#### Feather Feet (`FeatherFeet`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `SpeedUp 1`

#### Find a Rock (`FindARock`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

#### Flex (`Flex`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `aoe_mode standard, max_aoe 1, aoe_excludes_self true, knockback_mode character_to_tile`
- **Damage/Effects:** `damage 0, knockback 1, layer all`

#### Focus (`Focus`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `DexterityUp 1`

#### Forbidden Fart (`ForbiddenFart`)
- **Template:** `spell`
- **Cost:** `cantrip true, mana 0`
- **Target/Shape:** `target_mode none, aoe_mode circle, max_aoe 2, aoe_excludes_self true`
- **Damage/Effects:** `damage 4, Poison 4, distance 3`

#### Claws Out (`GainThorns`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Thorns 1`

#### Gamble (`Gamble`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `Default`
- **Damage/Effects:** `CritChanceUp 2, NextAttackSpecialCrit 1`

#### Gym Membership (`GymMembership`)
- **Template:** `self_buff`
- **Cost:** `cantrip true, mana 0, coins 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `AllStatsUp 1`

#### Healing Bolt (`HealBolt`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_aoe 0, max_range 3`
- **Damage/Effects:** `heal 5, Stun [1, .25]`

#### Hire Hitman (`HireHitman`)
- **Template:** `spawn`
- **Cost:** `cantrip true, mana 0, coins 7`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

#### Hiss (`Hiss`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `target_mode none, aoe_mode standard, min_aoe 1, max_aoe 1`
- **Damage/Effects:** `damage 0, ForceMoveAway 1, Fear [1 .25]`

#### Hose Off (`HoseOff`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5, once_per_fight true`
- **Target/Shape:** `min_range 0, max_range 20, max_aoe 0, knockback_mode none`
- **Damage/Effects:** `Cleanse 0, ChangeTile WaterTile`

#### Hunt (`Hunt`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 4`
- **Damage/Effects:** `damage 2+bonus_ranged_damage, SpawnThingIfHitKills BigFood`

#### Tunnel (`Infiltrate`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 3, once_per_fight true`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `None`

#### Interchange (`Interchange`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `InterchangeMoveActPoints 1`

#### Itch (`Itch`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1, type melee, cant_miss true, crit_chance -999999, object CharmedFlea, chance .5`

#### Knead (`Knead`)
- **Template:** `melee_attack`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, DamageUp 1`

#### Landscape (`Landscape`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 1`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `ChangeTile GrassTile`

#### Lick (`LickHeal`)
- **Template:** `melee_attack`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 2, elements [, Water, Holy, ]`

#### Look at me! (`LookAtMe`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `aoe_mode all, target_mode none, aoe_excludes_self true, knockback_mode tile_to_character`
- **Damage/Effects:** `damage 0, type status_spell, FaceAway 1`

#### Rat Roulette (`LotteryShottery`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `target_mode random_tile, min_range 0, max_range 20, restrictions must_have_animate_character`
- **Damage/Effects:** `damage 1, TakeExtraTurn 1`

#### Magnet (`Magnet`)
- **Template:** `spell`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `max_aoe 0, max_range 20, knockback_mode target_to_character, restrictions must_have_tag, target_requires_tag pickup`
- **Damage/Effects:** `damage 0, knockback 1`

#### Borrow Mana (`ManaDrain`)
- **Template:** `targeted_status`
- **Cost:** `mana 0, act_points 0, charge 1`
- **Target/Shape:** `min_range 1, max_range 20, restrictions [must_have_ally]`
- **Damage/Effects:** `ManaSteal 5`

#### Meow (`Meow`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ForceMoveTowards 1`

#### Metabolize (`Metabolize`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ConstitutionUp 1`

#### Metronome (`Metronome`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Metronome 1`

#### Over There! (`MiniDistract`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `target_mode none, aoe_mode standard, min_aoe 1, max_aoe 1, aoe_considers_character_size true, aoe_excludes_self true, knockback_mode character_to_tile_4snap`
- **Damage/Effects:** `damage 0, FaceAway 1`

#### Minihook (`MiniHook`)
- **Template:** `straightshot_attack`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `max_aoe 3, knockback_mode pull_to_character`
- **Damage/Effects:** `damage 0, CollectsPickups 1`

#### Nerf (`Nerf`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_range 3, max_aoe 0`
- **Damage/Effects:** `damage 0, DamageUp -1`

#### Path of the Butcher (`PathOfTheButcher`)
- **Template:** `targeted_status`
- **Cost:** `cantrip true, mana 1`
- **Target/Shape:** `max_range 1, restrictions must_have_tag, target_requires_tag food`
- **Damage/Effects:** `damage 0, type status_spell, CollectsPickups 1, EvolveAbilityFromPool Butcher`

#### Path of the Cleric (`PathOfTheCleric`)
- **Template:** `targeted_status`
- **Cost:** `cantrip true, mana 0`
- **Target/Shape:** `max_range 1, restrictions must_have_enemy`
- **Damage/Effects:** `Revive 100%, AllStatsUp 1, FullHeal 1, EvolveAbilityFromPool Medic`

#### Path of the Druid (`PathOfTheDruid`)
- **Template:** `self_buff`
- **Cost:** `cantrip true, mana 2`
- **Target/Shape:** `restrictions [must_have_element], target_requires_element [grass]`
- **Damage/Effects:** `layer all, EvolveAbilityFromPool Druid, FlowersOnHit 1`

#### Path of the Fighter (`PathOfTheFighter`)
- **Template:** `self_buff`
- **Cost:** `cantrip true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `EvolveAbilityFromPool Fighter, IntelligenceUp -int`

#### Path of the Hunter (`PathOfTheHunter`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `damage 1, EvolveAbilityFromPool Hunter`

#### Path of the Jester (`PathOfTheJester`)
- **Template:** `self_buff`
- **Cost:** `cantrip true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `EvolveAbilityFromPool JesterMinusColorless, RandomStatUp 10, RandomStatUp -5`

#### Path of the Mage (`PathOfTheMage`)
- **Template:** `self_buff`
- **Cost:** `cantrip true, mana 12`
- **Target/Shape:** `Default`
- **Damage/Effects:** `EvolveAbilityFromPool Mage`

#### Path of the Monk (`PathOfTheMonk`)
- **Template:** `self_buff`
- **Cost:** `cantrip true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `EvolveAbilityFromPool Monk, AllStatsUp -1`

#### Path of the Necromancer (`PathOfTheNecromancer`)
- **Template:** `melee_attack`
- **Cost:** `cantrip true, mana 0`
- **Target/Shape:** `aoe_restrictions must_have_destructible_corpse, restrictions aoe_must_exist`
- **Damage/Effects:** `damage 0, incidentally_collects_pickups false, VaporizeCorpse 1, EvolveAbilityFromPool Necromancer`

#### Path of the Psychic (`PathOfThePsychic`)
- **Template:** `self_buff`
- **Cost:** `cantrip true, mana 0, cant_cast 1-X`
- **Target/Shape:** `X_is is_at_max_mana`
- **Damage/Effects:** `EvolveAbilityFromPool Psychic`

#### Path of the Tank (`PathOfTheTank`)
- **Template:** `self_buff`
- **Cost:** `cantrip true, mana 0, cant_cast X-5`
- **Target/Shape:** `X_is current_health`
- **Damage/Effects:** `EvolveAbilityFromPool Tank`

#### Path of the Thief (`PathOfTheThief`)
- **Template:** `straightshot_attack`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_aoe 3+bonus_range`
- **Damage/Effects:** `damage 1, EvolveAbilityFromPool Thief`

#### Path of the Tinkerer (`PathOfTheTinkerer`)
- **Template:** `self_buff`
- **Cost:** `cantrip true, mana 0, requires_destructible_weapon true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `DestroyWeapon 1, EvolveAbilityFromPool Tinkerer`

#### Path Of The Void (`PathOfTheVoid`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 1`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ConjureBonusAbility Colorless`

#### Number One (`PissYourself`)
- **Template:** `spell`
- **Cost:** `mana 2, infcantrip true`
- **Target/Shape:** `target_mode none, max_aoe 1, aoe_excludes_self false`
- **Damage/Effects:** `heal 0, type status_spell, ChangeTile WaterTile`

#### Play Dead (`PlayDead`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `SafeDie 1`

#### Sudden Affliction (`PokeWound`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 1`
- **Damage/Effects:** `makes_contact true, TriggerDOTStatuses 0`

#### Ponder (`Ponder`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `IntelligenceUp 1`

#### Hop (`PrepareToJump`)
- **Template:** `jump_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `target_mode tile, min_range 1, max_range 2, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, range_display_include_character_size true, restrictions must_be_moveable`
- **Damage/Effects:** `type none, damage 0`

#### Purr (`Purr`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_aoe 1`
- **Damage/Effects:** `PartialCleanse 1`

#### Steam Roller (`PushMove`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `range_mode cross, max_range 1, restrictions [must_be_moveable must_move], straight_shot true`
- **Damage/Effects:** `override_trample_damage true, damage 3`

#### Reach (`Reach`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `NextAttackBonusRange 1`

#### Reduce (`Reduce`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5, once_per_fight true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `SpeedUp 4, DamageUp -2, DodgeChance_Status 20, SizeScale .6`

#### Reflect (`Reflect`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Reflect 1`

#### Rest (`Rest`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 10, Sleep 1`

#### Roll (`Roll`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `range_mode cross, max_range 3, restrictions [must_be_moveable must_move], straight_shot true`
- **Damage/Effects:** `None`

#### Rouse (`Rouse`)
- **Template:** `targeted_status`
- **Cost:** `cantrip true, mana 0`
- **Target/Shape:** `min_range 1, max_range 1`
- **Damage/Effects:** `Charge 2`

#### Russian Shorthair Roulette (`RussianRoulette`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `Default`
- **Damage/Effects:** `odds .16666666, DieViolently 1`

#### Shrug It Off (`ScuffItOff`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `raw_heal "(str+1)/2"`

#### Sharpen Claws (`SharpenClaws`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `StrengthUp 1`

#### Shift (`Shift`)
- **Template:** `swap`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

#### Slip Through (`SlipThrough`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `range_mode diagcross, max_range 2, restrictions [must_be_moveable must_move], straight_shot true, allow_diagonals true`
- **Damage/Effects:** `None`

#### Smack (`Smack`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 2, type melee`

#### Snacks (`Snacks`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_aoe 0, min_range 0, max_range 4`
- **Damage/Effects:** `heal 1, type spell`

#### Soothing Glow (`SoothingGlow`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 1, elements [, Holy, ]`

#### Soul Reap (`SoulReap`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_aoe 0, min_range 1, max_range 5`
- **Damage/Effects:** `damage 1, ManaGain 5`

#### Spit (`Spit`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `min_range 1, max_range 20`
- **Damage/Effects:** `damage 1, elements [, Water, ]`

#### Stack the Deck (`StackTheDeck`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `LuckUp 1`

#### Step (`Step`)
- **Template:** `move`
- **Cost:** `cantrip true, mana 0`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

#### Subway Ride (`SubwayRide`)
- **Template:** `teleport`
- **Cost:** `cantrip true, mana 0, coins 5`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `None`

#### Sunburn (`Sunburn`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `max_aoe 0, max_range 20`
- **Damage/Effects:** `damage 0, Burn 1, Blind 1`

#### Super Crate Box (`SuperCrateBox`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

#### Stun (`Suppress`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 5, once_per_fight true`
- **Target/Shape:** `max_aoe 0, max_range 20`
- **Damage/Effects:** `damage 1+bonus_ranged_damage, Stun 1, BounceObject SmallRock`

#### Swat (`Swat`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, knockback 3`

#### Proliferate (`Taint`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 8, once_per_fight true`
- **Target/Shape:** `min_range 1, max_range 1`
- **Damage/Effects:** `DoubleStatus Poison, DoubleStatus Bleed, DoubleStatus Burn`

#### Randomize (`Till`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `max_range 5`
- **Damage/Effects:** `ChangeTile RandomDifferentTile`

#### Toast (`Toast`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_aoe 0, min_range 1, max_range 1`
- **Damage/Effects:** `damage 0, Burn 1`

#### Trip (`Trip`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type melee, Immobile [1 .25]`

#### Vet Visit (`VetVisit`)
- **Template:** `self_buff`
- **Cost:** `cantrip true, mana 0, coins 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 10`

#### Waste Time (`WasteTime`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 1`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

#### Wet Hairball (`WetHairball`)
- **Template:** `spell`
- **Cost:** `mana 7, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 4+bonus_range, max_aoe 1, can_multihit false`
- **Damage/Effects:** `damage 2, elements [, Water, ]`

#### Zap (`Zap`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_aoe 0, max_range 20`
- **Damage/Effects:** `damage 1, elements [, Electric, ]`

### Passives

| Passive Name | Internal ID | Description |
| :--- | :--- | :--- |
| **Amped** | `Amped` | Gain +1 [img:spd] at the end of your turn. |
| **Amplify** | `Amplify` | +1 Magic Damage. |
| **Animal Handler** | `AnimalHandler` | You start each battle with a random vermin familiar with boosted damage and health. |
| **Bare Minimum** | `BareMinimum` | Your stats can't go below 5. |
| **Butcher's Soul** | `ButchersSoul` | Butcher abilities are offered when you level up. |
| **Careful** | `Careful` | Damage you deal to other allies is reduced to 0. |
| **Charming** | `Charming` | You have a 25% chance to inflict Charm on units that damage you. |
| **Cleric's Soul** | `ClericsSoul` | Cleric abilities are offered when you level up. |
| **Daunt** | `Daunt` | Small enemies won't attack you. |
| **Dealer** | `Dealer` | You can use consumables on other units. |
| **Death Boon** | `DeathBoon` | When you're downed, all allies gain All Stats Up. |
| **Deathproof** | `DeathProof` | While downed, you have a 25% chance to revive with 1 HP at the end of each round. |
| **Death's Door** | `DeathsDoor` | While you're at 1 HP, your spells cost 1 mana, but can only be cast once per turn. |
| **Dirty Claws** | `DirtyClaws` | Your physical attacks on Poisoned or Bleeding enemies inflict +1 Poison and/or Bleed. |
| **Druid's Soul** | `DruidsSoul` | Druid abilities are offered when you level up. |
| **E-Tank** | `ETank` | Start each battle with +20 unfilled max health. |
| **Fast Footsies** | `FastFooted` | You are immune to negative tile effects. |
| **Fighter's Soul** | `FightersSoul` | Fighter abilities are offered when you level up. |
| **First Impression** | `FirstImpression` | Start each battle with +1 Bonus Attack. |
| **Furious** | `Furious` | Gain +1 Damage each time you land a critical hit. +5% critical hit chance. |
| **Gassy** | `Gassy` | Whenever you take damage, knock back all adjacent units. |
| **Hot-Blooded** | `HotBlooded` | Burn you inflict is increased by 1. |
| **Hunter's Soul** | `HuntersSoul` | Hunter abilities are offered when you level up. |
| **Infested** | `Infested` | 50% chance to spawn a flea familiar when you end your turn. |
| **Jester's Soul** | `JestersSoul` | Abilities from any class are offered when you level up. You can reroll your level up options twice. |
| **Late Bloomer** | `LateBloomer` | On your 5th turn, you gain All Stats Up 3. |
| **Leader** | `Leader` | Adjacent allies have +1 Damage and +1 Range. |
| **Longshot** | `LongShot` | +1 Range. |
| **Luck Drain** | `LuckDrain` | Gain +1 [img:lck] whenever a unit is downed. |
| **Lucky** | `Lucky` |  |
| **Mage's Soul** | `MagesSoul` | Mage abilities are offered when you level up. |
| **Mange** | `Mange` | Inflict Poison 1 on units that contact you. |
| **Mania** | `Mania` | 10% chance to restore all your mana at the start of your turn. |
| **Metal Detector** | `MetalDetector` | 5% chance to spawn a coin when you move over a tile. |
| **Mini-Me** | `MiniMe` | Gain a half-sized copy of yourself that has 50% of your stats. The copy is AI controlled. |
| **Monk's Soul** | `MonksSoul` | Monk abilities are offered when you level up. |
| **Natural Healing** | `NaturalHealing` | You have +1 Health Regeneration |
| **Necromancer's Soul** | `NecromancersSoul` | Necromancer abilities are offered when you level up. |
| **180** | `OneEighty` | When you use your basic attack, turn around and use it again. |
| **Overconfident** | `OverConfident` | While at full HP, reduce the cost of your spells by 2, but take double damage. This can't reduce mana costs to less than 1. |
| **Patience** | `Patience` | If you end your turn without taking any actions, gain an extra turn at the end of the round. You don't regenerate mana on your main turn if you pass it. |
| **Might of the Meek** | `PressurePoints` | Damage you deal that's 2 or less is always critical. |
| **Protection** | `Protection` |  |
| **Psychic's Soul** | `PsychicsSoul` | Psychic abilities are offered when you level up. |
| **Pulp** | `Pulp` | When you kill a unit or destroy a corpse, it becomes meat. |
| **Rockin'** | `Rockin` | Spawn 4 small rocks at the start of each battle. |
| **Santa Sangre** | `SantaSangre` | When you're downed, allies heal 12 HP. Excess healing is converted to Shield. |
| **Scavenger** | `Scavenger` | If your trinket slot is empty, equip a small consumable food item at the start of each battle. |
| **Self-Assured** | `SelfAssured` | Gain a random stat up whenever you down a unit. |
| **Serial Killer** | `SerialKiller` | After you kill 3 units, gain +6 [img:spd] and backstabs have 100% crit chance. |
| **Skill Share** | `SkillShare` | Your other passive ability is shared with the other cats in your party at the start of each battle. |
| **Slugger** | `Slugger` | +1 Damage. |
| **Strength in Numbers** | `StrengthInNumbers` | Your familiars have +1 Damage for each other familiar you have. |
| **Study** | `Study` | Gain +1 [img:int] whenever you hit a new type of unit with an attack or ability. |
| **Tank's Soul** | `TanksSoul` | Tank abilities are offered when you level up. |
| **Thief's Soul** | `ThiefsSoul` | Thief abilities are offered when you level up. |
| **Tinkerer's Soul** | `TinkerersSoul` | Tinkerer abilities are offered when you level up. |
| **Unrestricted** | `Unrestricted` | Actions with a once per battle restriction can be cast once per turn instead. |
| **Unscarred** | `Untouched` | While at full hp you have 100% critical hit chance. |
| **Void Soul** | `VoidSoul` | Only upgraded Collarless abilities are offered when you level up |
| **Whipcracker** | `WhipCracker` | When you damage an ally they gain +1 Damage. |
| **Wiggly** | `Wiggly` | +25% dodge chance. |
| **Worms** | `Worms` | 50% chance to spawn a maggot familiar when you end your turn. |
| **Zenkai Boost** | `ZenkaiBoost` | If you end battle with 1 HP, gain +1 to a random stat permanently and start the next battle at full HP with All Stats Up 3. |

---

## Class: Druid (`Druid`)

### Actives & Attacks

#### Sing (`BasicDruidAbility`)
- **Template:** `spell`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 2, max_range 5+bonus_range`
- **Damage/Effects:** `heal 1, cant_miss true, TempDamageUp 1`

#### Battle Cry (`BattleCry`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `min_range 0, max_range 4, max_aoe 2`
- **Damage/Effects:** `damage 0, DamageUp 2`

#### Bestow Wisdom (`BestowWisdom`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `min_range 1, max_range 5`
- **Damage/Effects:** `IntelligenceUp 1`

#### Bramble Burst (`BrambleBurst`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 0, max_range 20, max_aoe 1, restrictions must_have_familiar`
- **Damage/Effects:** `damage 5, cant_miss true, VaporizeTarget 1, ChangeTile BrambleTile`

#### Call the Wind (`CallTheWind`)
- **Template:** `spell`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `target_mode direction, aoe_mode all, aoe_considers_character_size false, knockback_mode orientation`
- **Damage/Effects:** `damage 0, knockback 1, elements [, Wind, ]`

#### Cha Cha Slide (`ChaChaSlide`)
- **Template:** `spell`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false`
- **Damage/Effects:** `damage 0, knockback 10, RandomKnockbackDirection 4, KnockbackDamageImmuneUntilSettled 1, ThornsDamageImmuneUntilSettled 1, TileDamageImmuneUntilSettled 1`

#### Cheerlead (`Cheerlead`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 10`
- **Target/Shape:** `min_range 1, max_range 5`
- **Damage/Effects:** `AlphaCat 1`

#### Control Air (`ControlAir`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_aoe 0, min_range 1, max_range 4, knockback_mode character_to_target`
- **Damage/Effects:** `damage 0, knockback 10, OverrideKnockbackDamage 0`

#### Control Plants (`ControlPlants`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `min_range 1, max_range 4, max_aoe 0`
- **Damage/Effects:** `damage 1, type spell, ChangeTile TallGrassTile, OverrideDamage 0`

#### Control Water (`ControlWater`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `min_range 1, max_range 4, max_aoe 0`
- **Damage/Effects:** `heal 2, type spell, ChangeTile WaterTile, OverrideDamage 0`

#### Death Metal (`DeathMetal`)
- **Template:** `spell`
- **Cost:** `mana 13, infcantrip true`
- **Target/Shape:** `target_mode random_tile, max_aoe 0, max_range 20, restrictions [must_have_living_character must_have_enemy]`
- **Damage/Effects:** `damage 0, Fear 1, VisualFX Explosion, ExplodeCharacter_NoDie 5`

#### Step In (`DruidSwap`)
- **Template:** `swap`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `max_range 20, restrictions [must_be_swappable aoe_must_exist], aoe_restrictions [familiars_only]`
- **Damage/Effects:** `None`

#### Form of the Elk (`ElkForm`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TransformBasicAttack AntlerSwipe, TransformAbility Prance, SpeedUp 8, IntelligenceUp -2, ConstitutionUp -2, Trample 3, IgnoreTiles 1, YOffset .25`

#### Encourage (`Encourage`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `min_range 0, max_range 3, restrictions must_have_familiar`
- **Damage/Effects:** `damage 0, TakeExtraTurn 1`

#### Entangle (`Entangle`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 0, max_range 4, max_aoe 1`
- **Damage/Effects:** `damage 0, Tangled 1`

#### Flower Feet (`FlowerFeet`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `max_range 3`
- **Damage/Effects:** `None`

#### From the Trees! (`FromTheTrees`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `target_mode random_tile, min_range 1, max_range 20, max_aoe 0, range_excludes_blocking false, restrictions [aoe_must_exist must_have_enemy], aoe_restrictions none, knockback_mode zero`
- **Damage/Effects:** `damage 5`

#### Grant Life (`GrantLife`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `min_range 1, max_range 5, max_aoe 0`
- **Damage/Effects:** `damage 0, type spell, AllStatsUp 1`

#### Hydro Pump (`HydroPump`)
- **Template:** `spell`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `target_mode direction, aoe_mode line, min_aoe 1, max_aoe 3, aoe_considers_character_size true, aoe_excludes_self true, knockback_mode orientation`
- **Damage/Effects:** `damage 0, knockback 3, ChangeTile WaterTile`

#### Inspirational Song (`InspirationalSong`)
- **Template:** `spell`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero, aoe_excludes_self true, aoe_restrictions [allies_only]`
- **Damage/Effects:** `heal 1, TempDamageUp 1`

#### Lullaby (`Lullaby`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 12`
- **Target/Shape:** `min_range 0, max_range 4, max_aoe 2`
- **Damage/Effects:** `damage 0, Sleep 1`

#### Bloom (`ManaBomb`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 0, max_range 3, max_aoe 1, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, type spell, ManaGain 5`

#### Form of the Mockingbird (`MockingbirdForm`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TransformBasicAttack MockSong, TransformAbility Tease, LuckUp 2, StrengthUp -2, Flying 1`

#### Form of the Monkey (`MonkeyForm`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TransformBasicAttack ThrowPoop, TransformAbility MonkeyThrow, DexterityUp 2, LuckUp 2, ConstitutionUp -2, CharismaUp -2, tail 1502, ear1 1501, ear2 1501, mouth 1501, arm1 1501, arm2 1501, leg1 1501, leg2 1501`

#### Nature's Blessing (`NaturesBlessing`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 9`
- **Target/Shape:** `min_range 0, max_range 4, max_aoe 2`
- **Damage/Effects:** `damage 0, ChangeTile TallGrassTile, DiminishingHealthRegen 3`

#### Plant Mushroom (`PlantMushroom`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Promote (`Promote`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ChampionUpgradeNextMinion 1`

#### Protection (`Protection`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 0, max_range 4, max_aoe 0, restrictions aoe_must_exist, aoe_restrictions familiars_only`
- **Damage/Effects:** `damage 0, DivineShield 1`

#### Stand By Me (`PullToSafety`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `min_range 0, max_range 20, restrictions must_have_ally`
- **Damage/Effects:** `damage 0, DisplaceTowardsSource 1`

#### Form of the Raccoon (`RaccoonForm`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TransformBasicAttack Pilfer, TransformAbility Scavenge, IntelligenceUp 2, StrengthUp -2, tail 1504, head 1504, texture 1008`

#### Form of the Turtle (`RhinoForm`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TransformBasicAttack HornCharge, TransformAbility HardenSkin, ConstitutionUp 2, Shield 10, IntelligenceUp -2, SpeedUp -2, tail 1503, body 1029, mouth 1005`

#### Safety Dance (`SafetyDance`)
- **Template:** `spell`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero, aoe_excludes_self true, aoe_restrictions [allies_only]`
- **Damage/Effects:** `damage 0, Shield 1`

#### Serenade (`Serenade`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 0, max_range 4, max_aoe 1`
- **Damage/Effects:** `damage 0, HealthRegenUp 1`

#### Song of Spring (`SongOfSpring`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `min_range 0, max_range 5, max_aoe 1`
- **Damage/Effects:** `damage 0, type spell, FlowersOnHit 1`

#### Form of the Squirrel (`SquirrelForm`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 10`
- **Target/Shape:** `target_mode none, max_aoe 1`
- **Damage/Effects:** `None`

#### Squirrel Squad (`SquirrelSquad`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 13`
- **Target/Shape:** `min_range 0, max_range 3, max_aoe 1, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Summon Bear (`SummonBear`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 12`
- **Target/Shape:** `range_mode custom, custom_range [[-2 0] [-2 -1] [-1 -2] [0 -2] [-1 1] [0 1] [1 0] [1 -1]], aoe_mode custom, dont_orient_aoe true, custom_aoe [[0 0] [1 0] [0 1] [1 1]], range_excludes_blocking false, restrictions must_fit_2x2_character, aoe_restrictions none, range_display_include_aoe true, mouse_offset [.5 .5]`
- **Damage/Effects:** `None`

#### Summon Caterpillar (`SummonCatepillar`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Resummon Crow (`SummonCrow`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 11`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Summon Snake (`SummonSnake`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Summon Squirrel (`SummonSquirrel`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Summon Toad (`SummonToad`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Summon Turtle (`SummonTurtle`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Thorny Feet (`ThornyFeet`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `max_range 3`
- **Damage/Effects:** `None`

#### Throw Egg (`ThrowEgg`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `min_range 1, max_range 5+bonus_range`
- **Damage/Effects:** `damage 4+bonus_ranged_damage, ObjectOnHitEmpty AnimalEgg`

#### Form of the Wolf (`TigerForm`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TransformBasicAttack TigerSwipes, TransformAbility Pounce, SpeedUp 2, StrengthUp 2, LuckUp -2, IntelligenceUp -2, tail 4, body 31, head 12, arm1 1013, arm2 1013, leg1 41, leg2 41, ear1 23, ear2 23`

#### Form of the Tree (`TreeForm`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TransformBasicAttack Timber, TransformAbility Synthesize, IntelligenceUp -2, PermanentImmobile 1, Brace 2, Shield 5, KnockbackImmunity 1, AddTag plant, Plant 1, ElementImmune Creep`

#### War Cry (`WarCry`)
- **Template:** `spell`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero, aoe_excludes_self true, aoe_restrictions familiars_only`
- **Damage/Effects:** `damage 0, ForceAttack 1`

#### We Are the Champions (`WeAreTheChampions`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 7, once_per_fight true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_restrictions familiars_only`
- **Damage/Effects:** `heal 0, AllStatsUp 2, FullHeal 1`

#### We Will Rock You (`WeWillRockYou`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `min_range 0, max_range 7, max_aoe 0, restrictions aoe_must_exist, aoe_restrictions familiars_only`
- **Damage/Effects:** `damage 0, Shield 6, Petrify 1`

#### Windy Step (`WindyStep`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `min_range 1, max_range 5`
- **Damage/Effects:** `MoveQuivered 1`

### Passives

| Passive Name | Internal ID | Description |
| :--- | :--- | :--- |
| **Animalistic** | `Animalistic` | Familiars you spawn gain +2 Damage. When you shapeshift, gain +1 Damage. |
| **Bark Skin** | `BarkSkin` | +1 Brace. When you take damage, you get +1 temporary Brace until the start of your next turn. |
| **Bouquet** | `Bouquet` | Spawn a tall flower tile under you at the end of your turn. |
| **Buddy System** | `BuddySystem` | When you lose [img:divineshield], your crow gains +1 [img:divineshield]. When your crow loses [img:divineshield], gain +1 [img:divineshield]. |
| **Empty Vessels** | `EmptyVessels` | Familiars you spawn have +3 Health Regeneration and +10 max health. |
| **Encore** | `Encore` | When you use a musical ability, refresh your basic action. |
| **Feral** | `Feral` | Your bonus ability is Feral Attack. |
| **Flower Power** | `FlowerPower` | Units on flower tiles have +2 [img:str] and +2 Brace. When you move, plant flowers on the tile you moved from. |
| **Good Vibrations** | `GoodVibrations` | Allies have +1 Health Regeneration and +1 Mana Regeneration. |
| **Like a Fish** | `LikeAFish` | Water tiles don't slow you down. Gain +1 Holy Shield at the end of the turn if you're wet and have no Holy Shield. Familiars you spawn also have this passive. |
| **Maestro** | `Maestro` | Your musical spells cost 50% less mana. |
| **Mega Minions** | `MegaMinions` | Every 3rd familiar you spawn is upgraded into a Champion. |
| **Nature's Guidance** | `NaturesGuidance` | Allied familiars are immune to damage from tiles, knockback, thorns, and trample. |
| **Pathfinder** | `Pathfinder` | Grass tiles are free to move through for you and familiars you spawn. Plant grass as you walk. |
| **Poison Ivy** | `PoisonIvy` | You and familiar you spawn are Poisonous. |
| **Rap God** | `RapGod` | Your basic action also gives temporary +4 [img:spd]. |
| **Sneak Attack** | `SneakAttack` | Your spells that spawn familiars cost -3 mana. Familiars spawned by your spells gain +2 Damage and +2 Movement, but die after their first turn. |
| **Love Song** | `SoothingSong` | Your basic action has +2 area, and heals 1 additional HP. |
| **Super Friends** | `SpecialFriends` | Familiars spawned by spells gain All Stats Up 2, but that spell gets disabled until the spawned familiars die. |
| **Suicide Squad** | `SuicideSquad` | Your controllable familiars gain Self Destruct as their bonus ability. |
| **Super Crow!** | `SuperCrow` | Your crow has its abilities upgraded. |
| **Teamwork** | `Teamwork` | When one of your familiars kills something, all allies get +1 Damage. |
| **Versatile Vocalist** | `VersatileVocalist` | Your basic action deals 1 damage to enemies, and inflicts temporary -1 Damage. Your basic attack wont apply debuffs to allies or buffs to enemies. |
| **Wild Animals** | `WildAnimals` | Familiars you spawn attack a random enemy within their range when they are spawned. |
| **Wild Style** | `WildStyle` | The first time you shapeshift each turn, gain an extra turn. |

---

## Class: Fighter (`Fighter`)

### Actives & Attacks

#### Assert Dominance (`AssertDominance`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `X_is you_are_the_alpha`
- **Damage/Effects:** `damage "1+bonus_melee_ability_damage+X*5", AlphaCat 1`

#### BasicMelee_Fighter (`BasicMelee_Fighter`)
- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

#### Berserk (`Berserk`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `StrengthUp 5, Bruise 5, TransformAbility BerserkDash, AlternateIdleAnimation berserkIdle, SetDefaultFace insane`

#### Big Punch (`BigPunch`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 3+X*2`
- **Target/Shape:** `X_is cast_count`
- **Damage/Effects:** `damage 10+bonus_melee_ability_damage`

#### Bloodzerk (`Bloodzerk`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `SetHealth 1, Bloodzerked 1, TransformAbility Lacerate`

#### Breaking Point (`BreakingPoint`)
- **Template:** `melee_attack`
- **Cost:** `cantrip true, mana 15-X`
- **Target/Shape:** `X_is custom`
- **Damage/Effects:** `damage str, knockback str, OverrideKnockbackDamage str`

#### Mock (`Challenge`)
- **Template:** `spell`
- **Cost:** `mana 0, requires_reload true`
- **Target/Shape:** `min_range 1, max_range 4, max_aoe 0`
- **Damage/Effects:** `damage 0, ForceMoveTowards 1`

#### Chaos Rampage (`ChaosRampage`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3, main_turn_only true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Madness 1, Confusion 1`

#### Confront (`Confront`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_range 100, restrictions [must_be_moveable must_be_directly_in_front_of_enemy must_move]`
- **Damage/Effects:** `None`

#### Cosmic Punch (`CosmicPunch`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type melee, LaunchOffScreen 10+bonus_melee_ability_damage, TempInitiativeChange -100`

#### Counter (`Counter`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TempCounterAttack 1`

#### Bull Rush (`Dash`)
- **Template:** `dash_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 3+bonus_melee_ability_damage, knockback 1`

#### 1D Chess (`DumbMove`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ForceMoveTowardsEnemies DumbMove_Impl`

#### Enrage (`Enrage`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_aoe 0, min_range 0, max_range 3`
- **Damage/Effects:** `damage 0, StrengthUp 4, Confusion 2`

#### Exert (`Exert`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Drowsy 1, RefreshMovePoints 1, RefreshActPoints 1`

#### Exhausting Blow (`ExhaustingBlow`)
- **Template:** `dash_attack`
- **Cost:** `mana 2+X*2, infcantrip true`
- **Target/Shape:** `max_range 1+bonus_range, max_aoe 1, aoe_restrictions must_have_line_of_sight_unpurgable, X_is custom`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, knockback 1`

#### Falcon Punch (`FalconPunch`)
- **Template:** `melee_attack`
- **Cost:** `cantrip true, mana 2`
- **Target/Shape:** `delayed_trigger true`
- **Damage/Effects:** `damage 25+bonus_melee_ability_damage, knockback 10`

#### Leap (`FighterLeap`)
- **Template:** `jump_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `max_range 4`
- **Damage/Effects:** `damage 0, makes_contact false, Bruise 1`

#### Taunt! (`FighterTaunt`)
- **Template:** `spell`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `target_mode none, max_aoe 3, min_aoe 1`
- **Damage/Effects:** `damage 0, type status_spell, ForceMoveTowards 1`

#### Fire Punch (`FirePunch`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, type melee, Burn 3, VisualFXTile FireBlastSmall`

#### Fury Swipes (`FurySwipes`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 2+bonus_melee_ability_damage, type melee`

#### Grapple (`Grapple`)
- **Template:** `tile_targeted_melee_attack`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `knockback_mode tile_to_character`
- **Damage/Effects:** `damage 0, type melee, Grappled 1`

#### Gravity Slam (`GravitySlam`)
- **Template:** `jump_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `max_range 4, max_aoe 4, aoe_mode standard, distance_sort_targets 1`
- **Damage/Effects:** `damage 0, makes_contact false, type spell, DisplaceToAbilityTarget 1`

#### Huddle (`Huddle`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `aoe_hint_teamcast true`
- **Damage/Effects:** `TeamCastAbility Huddle_Impl`

#### Hurl (`Hurl`)
- **Template:** `throw_attack`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `target_mode random_tile, min_range 2, max_range 20, restrictions must_have_enemy`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, blocked_damage 5+bonus_melee_ability_damage`

#### Ice Punch (`IcePunch`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, type melee, Freeze 1`

#### Inhale (`Inhale`)
- **Template:** `spell`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `target_mode direction, aoe_mode line, min_aoe 1, max_aoe 10, aoe_considers_character_size true, aoe_excludes_self true, knockback_mode back_orientation`
- **Damage/Effects:** `damage 0, knockback 1, elements [, Wind, ]`

#### Juiced (`Juiced`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TempMovement mov`

#### Meteor Slam (`MeteorSlam`)
- **Template:** `jump_attack`
- **Cost:** `infcantrip true, mana 10`
- **Target/Shape:** `min_range 1, max_range 2, max_aoe 1, aoe_mode square, restrictions none`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, knockback 2, Burn 3, IgnoreSelf 1`

#### Muscle Memory (`MuscleMemory`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana "max(8-2*X,0)", damage_cant_be_zero true`
- **Target/Shape:** `X_is cast_count`
- **Damage/Effects:** `raw_damage "8-X"`

#### Nip (`Nip`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type melee, Bruise 1`

#### One-Two Punch (`OneTwoPunch`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `multihit 2`
- **Damage/Effects:** `damage 2+bonus_melee_ability_damage, type melee, Bruise 1`

#### Paw Breaker (`Pawbreaker`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 15+bonus_melee_ability_damage, SpecificInjury str`

#### Poke (`Poke`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1, type melee`

#### Push (`Push`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type melee, knockback 2`

#### Rage Punch (`RagePunch`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `X_is custom`
- **Damage/Effects:** `damage 1+X`

#### Ram (`Ram`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type melee, knockback 4, ForceUseAbility Ram_chained`

#### Side Slash (`SideSlash`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `aoe_mode custom, custom_aoe [ [1, 0], [0, -1], [0, 1], [1, 1], [1, -1] ], knockback_mode character_to_tile`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage`

#### Sleeper Hold (`SleeperHold`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type melee, Sleep 1`

#### Spin (`Spin`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `target_mode none, aoe_mode cross, knockback_mode character_to_tile, multihit 3`
- **Damage/Effects:** `damage 1+bonus_melee_ability_damage`

#### Stick! (`Stick`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `restrictions aoe_must_exist, aoe_restrictions must_have_cat_with_empty_weapon_slot`
- **Damage/Effects:** `damage 0, pool stick, slot weapon, works_with_tech true`

#### Stoopzerk (`Stoopzerk`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ExtraBasicAttacks_Status 1, IntelligenceUp "min(-int, 0)", TransformAbility LastThought`

#### Sucker Punch (`SuckerPunch`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Trapper_Status 1`

#### Tail Whip (`TailWhip`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `aoe_mode custom, custom_aoe [[1, 0] [2, 0], [-1, 0], [-2, 0]], max_aoe 2`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, type melee`

#### Flex Off (`TeamFlex`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `aoe_hint_teamcast true`
- **Damage/Effects:** `TeamCastAbility TeamFlex_Impl`

#### Synchro Spin (`TeamSpin`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `aoe_hint_teamcast true`
- **Damage/Effects:** `TeamCastAbility Spin`

#### Think Too Hard (`ThinkTooHard`)
- **Template:** `self_buff`
- **Cost:** `mana 2, infcantrip true, manacost_cant_be_zero true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `raw_damage int, FreeSpell 1`

#### Thunder Punch (`ThunderPunch`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, type melee, Stun [1, .25], VisualFXTile WaterConduct`

#### Tumble (`Tumble`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `range_mode diagcross, max_range level, restrictions [must_be_moveable must_move], straight_shot true, allow_diagonals true`
- **Damage/Effects:** `None`

#### Uppercut (`Uppercut`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, type melee, stacks 5+bonus_melee_ability_damage, distance 3`

#### Zoomzerk (`Zoomzerk`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TransformBasicMove BasicDashAttackMove_NoKnockback, TransformAbility Reposition`

### Passives

| Passive Name | Internal ID | Description |
| :--- | :--- | :--- |
| **Avenger** | `Avenger` | When an allied cat is downed, gain All Stats Up 2 and heal 8. |
| **Frenzy** | `BloodLust` | When you down a unit, gain +2 [img:str]. |
| **Boned** | `Boned` | When you kill a unit, if you don't have a weapon, gain a Bone Club. |
| **Dual Wield** | `DualWield` | When you use your weapon, automatically use it again for free. |
| **Dumb Muscle** | `DumbMuscle` | Lose 1 [img:int] each time you take damage. If you have 4 or less [img:int], gain +2 [img:str] and your basic attack inflicts Bruise. at 0 [img:int], gain +100% critical hit chance. |
| **Hulk Up** | `FasterWhenHit` | When you take damage, gain +2 [img:spd]. |
| **Underdog** | `FightMe` | You have +2 [img:str] and +1 Brace for each enemy adjacent to you. |
| **Hamster Style** | `HamsterStyle` | +1 Health Regeneration. Start with 2 Bonus Moves. |
| **Math?** | `HighAsYouCanCount` | Your spells cost 3 mana to cast, but each can be cast only once per turn. |
| **Hit Me** | `HitMe` | When you take damage from an ally, basic attack in the direction you're facing. Damage you take from allies is reduced to 1. |
| **Fervor** | `KillsHeal` | When you down a unit, you heal 5 HP. |
| **Most Valuable Cat** | `MostValuableCat` | When you or an ally downs another unit, they become the Alpha. If you're the Alpha, take an extra turn at the end of each round. |
| **OVERPOWERED!!!** | `Overpowered` | Excess damage you deal to units makes them explode, dealing the excess damage to units around it, except for you. |
| **Punch Face** | `PunchFace` | Your basic attacks are critical if they hit the front of a unit. |
| **Rat Style** | `RatStyle` | +10% dodge chance. |
| **Merciless** | `Recoil` | When you deal 10 or more damage in a single hit, gain +2 [img:shield] and refresh your movement action. [s:.7](This doesn't trigger during your movement action.)[/s] |
| **Patellar Reflex** | `ReflexPunch` | When a unit damages you, counter-attack dealing 1 damage and inflicting Bruise. |
| **Scars** | `Scars` | +1 Brace. |
| **Shoulder Check** | `ShoulderCheck` | If you're facing a unit after you move, automatically attack it at 33% damage. |
| **Skullcrack** | `SkullSmash` | Your basic attack inflicts Bruise. |
| **Smash!** | `Smash` | Your weapons deal triple damage, but they always break when you use them. Three Sticks are added to your inventory. |
| **Thick Skull** | `ThickSkull` | All injuries you get are Concussions. You get +3 [img:shield] for each concussion you have. This caps at 30 [img:shield]. |
| **Turtle Style** | `TurtleStyle` |  |
| **Vengeful** | `Vengeful` | Your basic attack is always critical on enemies that have damaged you. |
| **Weapon Master** | `WeaponMaster` | Your weapon and item abilities deal +2 Damage and get +25% critical chance. A pipe is added to your inventory. |

---

## Class: Hunter (`Hunter`)

### Actives & Attacks

#### Arrow Flurry (`ArrowFlurry`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `damage 2+bonus_ranged_damage, accuracy .5`

#### Arrowsmith (`ArrowSmith`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Quivered 1`

#### Ball of Spiders (`BallOfSpiders`)
- **Template:** `lobbed_attack`
- **Cost:** `mana 9, infcantrip true`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `damage 2, BounceObject CharmedTinySpider, BounceObject CharmedTinySpider, BounceObject CharmedTinySpider`

#### BasicRanged_Hunter (`BasicRanged_Hunter`)
- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

#### Bear Trap (`BearTrap`)
- **Template:** `lobbed_attack`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 5, restrictions must_be_empty`
- **Damage/Effects:** `damage 0, ai_base_score 10, custom_additional_ai_weight tile_has_no_known_traps, SpawnBearTrap 1`

#### Bomb Shot (`BombShot`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_aoe 1, min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `damage 5, type spell, knockback 1, elements [, Explosion, ]`

#### Bounce Shot (`BounceShot`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_aoe 1, min_aoe 1, min_range 0, max_range 5+bonus_range`
- **Damage/Effects:** `damage 0, type spell, distance 3, stacks 1`

#### Bramble Shot (`BrambleShot`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_aoe level, min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `damage 2, BramblesOnHit 1`

#### Hedge In (`Bunker`)
- **Template:** `lobbed_attack`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `target_mode none, min_aoe 1, max_aoe 1, aoe_restrictions must_be_empty, low_gravity_boostable false`
- **Damage/Effects:** `damage 0, ai_base_score 10, custom_additional_ai_weight tile_has_no_known_traps, SpawnBearTrap 1`

#### Chaos Shot (`ChaosShot`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `target_mode random_tile, min_range 3, max_range 5+bonus_range, restrictions must_have_animate_character`
- **Damage/Effects:** `damage 4+bonus_ranged_damage`

#### Charm Trap (`CharmTrap`)
- **Template:** `lobbed_attack`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 5, restrictions must_be_empty`
- **Damage/Effects:** `damage 2, ai_base_score 10, custom_additional_ai_weight tile_has_no_known_traps, SpawnCustomTrap CharmTrap, Charmed 1, Immobile 0`

#### Collect Pelt (`CollectPelt`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `aoe_restrictions must_have_destructible_corpse, restrictions aoe_must_exist`
- **Damage/Effects:** `damage 0, type melee, incidentally_collects_pickups false, VaporizeCorpse 1, slot random_empty_armor, pool pelts, temporary false`

#### Craft Arrow (`CraftArrow`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `max_range 1, restrictions must_have_tag, target_requires_tag pickup`
- **Damage/Effects:** `damage 0, type status_spell, Quivered 1`

#### Cross Shot (`CrossShot`)
- **Template:** `straightshot_attack`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `target_mode none, aoe_mode custom, aoe_symmetry four_way, custom_aoe [[1, 1]]`
- **Damage/Effects:** `damage 4+bonus_ranged_damage`

#### Cupid's Arrow (`CupidsArrow`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 12`
- **Target/Shape:** `min_range 3, max_range 8+bonus_range`
- **Damage/Effects:** `damage 6+bonus_ranged_damage, Charmed level`

#### Diversion (`Diversion`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range, max_aoe 3, aoe_restrictions exclude_allies`
- **Damage/Effects:** `damage 1, ForceMoveNonAlliesInRangeTowardsTile 3`

#### Extend (`Extend`)
- **Template:** `spell`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 4, max_aoe 0`
- **Damage/Effects:** `damage 0, TempRangeUp 3, status MeleeRangeUp, stacks 3, turns 1`

#### Fire Shot (`FireShot`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_aoe 1, min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `damage 2+bonus_ranged_damage, type ranged, Burn 2`

#### Flea Shot (`FleaShot`)
- **Template:** `lobbed_attack`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `damage 2, BounceObject CharmedFlea`

#### Focus Shot (`FocusShot`)
- **Template:** `lobbed_attack`
- **Cost:** `cantrip true, mana 7`
- **Target/Shape:** `delayed_trigger true, min_range 3, max_range 5+bonus_range, track_target true, hint_can_target_empty false`
- **Damage/Effects:** `damage 4+bonus_ranged_damage, piercing true, crit_chance 100%, cant_miss true`

#### Hail of Nails (`HailOfNails`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 9`
- **Target/Shape:** `target_mode tile, range_mode cross, min_range 3, max_range 10, aoe_mode perpline, min_aoe -10, max_aoe 10, knockback_mode zero, restrictions none, can_multihit true`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, type ranged`

#### Heavy Shot (`HeavyShot`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `damage 8+bonus_ranged_damage, accuracy .5`

#### Infest (`Infest`)
- **Template:** `lobbed_attack`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `damage 1+bonus_ranged_damage, SpiderInfested 1`

#### Last Hit (`LastHit`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `damage 1, RefreshActPoints 1`

#### Line Shot (`LineShot`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `target_mode direction, aoe_mode line, min_aoe 2+size, max_aoe 10, aoe_considers_character_size true, aoe_excludes_self true, knockback_mode character_to_tile, restrictions none, can_multihit true`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, type ranged`

#### Marked (`Marked`)
- **Template:** `targeted_status`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `Marked 1`

#### Needle Shot (`NeedleShot`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `damage 1, piercing true, Thorns 1`

#### Persistent Hunt (`PersistentHunt`)
- **Template:** `targeted_status`
- **Cost:** `mana 0, requires_reload true`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `Marked 5`

#### Pheromones (`Pheromones`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `damage 0, Charmed 1, TakeExtraTurn 1`

#### Picnic (`Picnic`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `target_mode none, max_aoe 1`
- **Damage/Effects:** `heal 5`

#### Poison Lace (`PoisonLace`)
- **Template:** `targeted_status`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `min_range 0, max_range 1, max_aoe 0`
- **Damage/Effects:** `PoisonLace 1`

#### Scatter Shot (`ScatterShot`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 10`
- **Target/Shape:** `max_aoe 3, min_range 3, max_range 6+bonus_range, aoe_chance .5, restrictions none, can_multihit true`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, type ranged`

#### Scout Me (`ScoutMe`)
- **Template:** `self_buff`
- **Cost:** `cantrip true, mana 7`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ShootHereReceiver 1, TeamBonusAbility ShootHere`

#### Sentry Mode (`SentryMode`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TowerDefenseStatus 1`

#### Shards (`Shards`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `min_range 1, max_range 4+bonus_range`
- **Damage/Effects:** `damage 1, type ranged, ChangeTile GlassTile`

#### Slop the Pigs (`SlopThePigs`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 5+bonus_range, max_aoe 1`
- **Damage/Effects:** `heal 2, BonusDamage -2, AllStatsUp 1`

#### Snipe (`Snipe`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 6, max_range 6`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, cant_miss true, piercing true`

#### Soothing Shot (`SoothingShot`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `heal 10+bonus_ranged_damage, Charmed 1`

#### Bait Trap (`SpawnBaitTrap`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 1, max_range 5, restrictions [must_be_empty aoe_must_exist]`
- **Damage/Effects:** `None`

#### Spawn Maggot Friend (`SpawnMaggotFriend`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `min_range 3, max_range 4`
- **Damage/Effects:** `None`

#### Spawn Pooter Friend (`SpawnPooterFriend`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `min_range 1, max_range 2`
- **Damage/Effects:** `None`

#### Call of the Wild (`SpawnTomTomFriend`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 9`
- **Target/Shape:** `min_range 1, max_range 1`
- **Damage/Effects:** `None`

#### Egg Sac Trap (`SpiderInjector`)
- **Template:** `lobbed_attack`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 5, restrictions must_be_empty`
- **Damage/Effects:** `damage 0, ai_base_score 10, custom_additional_ai_weight tile_has_no_known_traps, SpawnCustomTrap EggSackTrap, SpiderInfested 4`

#### Spike Trap (`SpikeTrap`)
- **Template:** `lobbed_attack`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 5, restrictions must_be_empty`
- **Damage/Effects:** `damage 8, ai_base_score 10, custom_additional_ai_weight tile_has_no_known_traps, SpawnCustomTrap SpikeTrap`

#### Stake Out (`StakeOut`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3, must_be_first_action true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `EndTurn 1, NextTurnDoubleRangedDamage 1`

#### Summon Brambles (`SummonBrambles`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_aoe level-1, min_range 1, max_range 20`
- **Damage/Effects:** `damage 0, BramblesOnHit 1`

#### Tactical Retreat (`TacticalRetreat`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 5`
- **Damage/Effects:** `None`

#### Terrain Walk (`TerrainWalk`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_range 20, restrictions [must_be_moveable must_have_element], target_requires_element [grass water]`
- **Damage/Effects:** `None`

#### Twin Shot (`TwinShot`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 9`
- **Target/Shape:** `min_range 3, max_range 5+bonus_range`
- **Damage/Effects:** `damage 4+bonus_ranged_damage`

#### Vivisect (`Vivisect`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, VaporizeCorpse 1, ObjectOnHit Bait, SpawnBearTrap 1`

#### Web Trap (`WebTrap`)
- **Template:** `lobbed_attack`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 5, restrictions must_be_empty`
- **Damage/Effects:** `damage 0, ai_base_score 10, custom_additional_ai_weight tile_has_no_known_traps, SpawnWebTrap 1`

### Passives

| Passive Name | Internal ID | Description |
| :--- | :--- | :--- |
| **Animal Control** | `AnimalControl` | Your basic attack causes units to immediately attack an enemy in range. |
| **Brood Mother** | `BroodMother` | Your familiars and units you charm gain +2 Damage and +5 HP. |
| **Catch Projectiles** | `CatchProjectiles` | 33% chance to block enemy projectiles and a 100% chance to block allied projectiles. If you block a projectile, gain +1 Bonus Attack. |
| **Fleabag** | `Fleabag` | At the end of your turn, spawn Flea familiars equal to the number of enemies you've killed this battle. |
| **Gravity Falls** | `GravityFalls` | Your basic attack deals +1 damage for each tile you shoot beyond range 3. |
| **Bullseye** | `HawkEye` | Your ranged attacks never miss. +25% critical hit chance. |
| **Hazardous** | `Hazardous` | Tile damage and effects are doubled. |
| **Host** | `Host` | Start each battle with 2 tiny spider familiars. A spider egg parasite is added to your inventory. You can unequip parasites freely. |
| **Hunter's Boon** | `HuntersBoon` | The first time you kill a unit each turn, gain 5 mana. |
| **Luck Swing** | `LuckSwing` | +50% critical hit chance but +25% chance to miss. |
| **Quiver** | `Quiver` | Save unused basic attacks for future turns. |
| **Rubber Arrows** | `RubberArrows` | Your projectiles bounce to another enemy within 3 tiles. |
| **Sleep Darts** | `SleepDarts` | At the start of each battle, you and all allies that don't have weapons gains a temporary Sleep Dart. |
| **Sniper** | `Sniper` | Critical hits deal +100% more damage and have a 25% chance to inflict Stun. |
| **Split Shot** | `SplitShot` | Your basic attack has +1 area but deals 50% less damage. |
| **Spotters** | `Spotters` | Your basic attack can target tiles adjacent to allies. |
| **Survivalist** | `Survivalist` | 6 healing consumables and a full water bottle are added to your inventory. You can use consumables on allies. Store +2 food at the end of each battle. |
| **Tainted Mother** | `TaintedMother` | Your familiars and units you charm gain +4 [img:spd] and inflict Poison and Bleed. |
| **Take Aim** | `TakeAim` | Gain +1 range and damage at the start of each turn. You lose this when you move. |
| **Talk to Animals** | `TalkToAnimals` | Your basic attack inflicts Charm 5 the first time you use it each battle. |
| **Thorn Arrows** | `ThornArrows` | Your basic attack spawns brambles. |
| **Thrill of the Hunt** | `ThrillOfTheHunt` | At the end of each battle, if you killed at least 3 enemies, gain +1 [img:dex] permanently and find a random consumable item. |
| **Tower Defense** | `TowerDefense` | When an enemy comes within range, shoot them for 1 damage. |
| **Traps** | `Traps` | Your basic attack spawns a bear trap if you shoot an empty tile. Whenever one of your traps triggers, gain +2 [img:dex]. |
| **Tricky Traps** | `TrickyTraps` | Damage and effects from your traps are doubled. |

---

## Class: Jester (`Jester`)

### Actives & Attacks

#### Cleave (`BasicButcherMelee`)
- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `target_mode direction8, max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 5+bonus_melee_damage, Cleave 1`

#### Magic Dart (`BasicMagicShortRanged`)
- **Template:** `ranged_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 5+bonus_range`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, type physical_spell, ranged true`

#### Melee Attack / Heal (`BasicMedicMelee`)
- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 5+bonus_melee_damage, ContextualHeal 1`

#### BasicMelee_Fighter (`BasicMelee_Fighter`)
- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

#### Leech Shot (`BasicNecroRanged`)
- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 3+bonus_range`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, Leeches 1`

#### Psychic Pull (`BasicPsychicPull`)
- **Template:** `spell`
- **Cost:** `move_points 0, act_points 1`
- **Target/Shape:** `max_aoe 0, max_range 20, knockback_mode target_to_character`
- **Damage/Effects:** `damage 2+bonus_basic_spell_damage, knockback 1, elements [, Gravity, ]`

#### BasicRanged_Hunter (`BasicRanged_Hunter`)
- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

#### BasicStraightShot_Thief (`BasicStraightShot_Thief`)
- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

#### Push Attack (`BasicTankMelee`)
- **Template:** `dash_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1+bonus_range, max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1`

#### Bump (`Bump`)
- **Template:** `targeted_status`
- **Cost:** `mana 1, infcantrip true`
- **Target/Shape:** `min_range 0, max_range 20, range_excludes_self false, knockback_mode none, restrictions aoe_must_be_displaceable`
- **Damage/Effects:** `damage 0, RandomDistanceDisplace 20`

#### Power Up (`PowerUp`)
- **Template:** `self_buff`
- **Cost:** `mana X, infcantrip true, X_cant_be_zero true, disallow_cost_modification true`
- **Target/Shape:** `X_is current_mana`
- **Damage/Effects:** `stacks X, Quivered 1, MoveQuivered 1, Thorns 1, Brace 1, Shield 1, DivineShield 1, BleedThorns 1, KineticSpikes 1, Reflect 1, DiminishingHealthRegen 1, Charge 1, AllStatsUp 1, StrengthUp 1, DexterityUp 1, SpeedUp 1, ConstitutionUp 1, IntelligenceUp 1, CharismaUp 1, LuckUp 1, PoisonLace 1, Lifesteal 1, CritChanceUp 1, DodgeChance_Status 1, HealthRegenUp 1, BackflipWhenTargeted 1, TempCounterAttack 1`

#### RNG Cannon (`RNGCannon`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 10`
- **Target/Shape:** `max_aoe 0, max_range 5, restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 0, show_damage_on_0 true, RNGCannonRandomDamage 100`

#### Smart Metronome (`SmartMetronome`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `SmartMetronome 20`

### Passives

| Passive Name | Internal ID | Description |
| :--- | :--- | :--- |
| **Goofball** | `Goofball` | Take an extra turn at the start of each round. |
| **Super Luck** | `SuperLuck` |  |

---

## Class: Mage (`Mage`)

### Actives & Attacks

#### Absorb (`Absorb`)
- **Template:** `self_buff`
- **Cost:** `mana X, infcantrip true, X_cant_be_zero true, disallow_cost_modification true`
- **Target/Shape:** `X_is current_mana`
- **Damage/Effects:** `heal X, elements [, Holy, ]`

#### Magic Dart (`BasicMagicShortRanged`)
- **Template:** `ranged_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 5+bonus_range`
- **Damage/Effects:** `damage 5+bonus_ranged_damage, type physical_spell, ranged true`

#### Black Magic (`BlackMagic`)
- **Template:** `self_buff`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `X_is current_health`
- **Damage/Effects:** `raw_damage X-1, piercing true, ManaGain X-1`

#### Energy Blast (`Blast`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_aoe 0, max_range 3`
- **Damage/Effects:** `damage 10`

#### Blizzard (`Blizzard`)
- **Template:** `spell`
- **Cost:** `mana 12, infcantrip true`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [, [1, 1], [2, 1], [3, 1], [4, 1], [5, 1], [6, 1], [7, 1], [8, 1], [9, 1], [10, 1], [1, 0], [2, 0], [3, 0], [4, 0], [5, 0], [6, 0], [7, 0], [8, 0], [9, 0], [10, 0], [1,-1], [2,-1], [3,-1], [4,-1], [5,-1], [6,-1], [7,-1], [8,-1], [9,-1], [10,-1], ], aoe_considers_character_size true, aoe_excludes_self true, knockback_mode orientation`
- **Damage/Effects:** `damage 16, knockback 1, Freeze 1`

#### Bolt (`Bolt`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_aoe 0, max_range 5`
- **Damage/Effects:** `damage 3, Stun [1, .25]`

#### Chain Lightning (`ChainLightning`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_aoe 0, max_range 4`
- **Damage/Effects:** `damage 4, stacks 100, enemies_only false, max_distance 2`

#### Chaos Teleport (`ChaosTeleport`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 1`
- **Target/Shape:** `target_mode random_tile, max_range 20`
- **Damage/Effects:** `None`

#### Corrupt (`Corrupt`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type spell_cost, cant_miss true, RandomInjury 1, SpellDamageUp 3`

#### Crescendo (`Creshendo`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 6-X, X_cant_be_zero true`
- **Target/Shape:** `max_aoe X*.5, max_range X, min_range 0, X_is custom`
- **Damage/Effects:** `raw_damage X, type spell, VisualFXTile MagicMissleBlast`

#### Cryo-Heal (`CryoHeal`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `max_aoe 0, min_range 0, max_range 3`
- **Damage/Effects:** `heal 10, type spell, Freeze 1`

#### Deal with the Devil (`DealWithTheDevil`)
- **Template:** `self_buff`
- **Cost:** `cantrip true, mana 0, once_per_fight true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type spell_cost, cant_miss true, RandomInjury 1, ManaGain 15`

#### Divide (`Divide`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3, requires_attack_damage_threshold 2`
- **Target/Shape:** `X_is basic_attack_damage`
- **Damage/Effects:** `ExtraBasicAttacks_Status 1, DamageUp "(-ceil(abs(X/2)))"`

#### Firebolt (`FireBolt`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `max_aoe 1, max_range 5, aoe_mode diagcross`
- **Damage/Effects:** `damage 4, Burn 1, Stun [1 .15]`

#### Fire Surge (`FireSurge`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_aoe "X/2", max_range X, X_is turn_count`
- **Damage/Effects:** `raw_damage X, formula X, Burn X`

#### Fire Blast (`Fireball`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_aoe 1, max_range 5`
- **Damage/Effects:** `damage 3, Burn 2`

#### Forbidden Flame (`ForbiddenFlame`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 0, once_per_fight true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero, aoe_restrictions exclude_allies`
- **Damage/Effects:** `damage 7, Burn 7`

#### Forbidden Flood (`ForbiddenFlood`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 0, once_per_fight true`
- **Target/Shape:** `target_mode direction, aoe_mode all, aoe_considers_character_size false, aoe_excludes_self false, knockback_mode orientation, prioritize_dont_change_direction true`
- **Damage/Effects:** `damage 15, knockback 10, ChangeTile WaterTile, KnockbackDamageImmuneUntilSettled 1, OverrideDamage 0`

#### Forbidden Frost (`ForbiddenFrost`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 0, once_per_fight true`
- **Target/Shape:** `target_mode tile, max_range 20, min_range 1, max_aoe 20, min_aoe 1, aoe_considers_character_size false, knockback_mode zero, aoe_excludes_self true, aoe_restrictions exclude_direct_target`
- **Damage/Effects:** `damage 10`

#### Forbidden Fulmination (`ForbiddenFulmination`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 0, once_per_fight true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero, aoe_restrictions enemies_only`
- **Damage/Effects:** `damage 10, Stun 1`

#### Frost Blast (`FreezeRay`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `target_mode direction, aoe_mode line, max_aoe 5, aoe_considers_character_size true, aoe_excludes_self true, knockback_mode character_to_tile, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 0, Freeze 1`

#### Freezer Burn (`FreezerBurn`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `target_mode none, max_aoe 3, aoe_excludes_self true`
- **Damage/Effects:** `damage 2, knockback 2, Burn 2, Slow 2`

#### Gust (`Gust`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `min_aoe 1, max_aoe 1, max_range 5`
- **Damage/Effects:** `damage 0, knockback 1, elements [, Wind, ]`

#### Homing Blasts (`HomingBlasts`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `Default`
- **Damage/Effects:** `stacks 3, full_size true`

#### Hyper Beam (`HyperBeam`)
- **Template:** `spell`
- **Cost:** `cantrip true, mana 3`
- **Target/Shape:** `delayed_trigger true, max_aoe 0, max_range 6`
- **Damage/Effects:** `damage 25`

#### Ice Surge (`IceSurge`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_aoe 0, max_range X, X_is turn_count`
- **Damage/Effects:** `raw_damage 0, formula X, Slow X`

#### Icicle Zapper (`IcicleTaser`)
- **Template:** `straightshot_attack`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `max_aoe 10`
- **Damage/Effects:** `damage 4, type spell, Slow 2, Stun [1 .25], Freeze [1 .25]`

#### Inferno (`Inferno`)
- **Template:** `spell`
- **Cost:** `mana 12, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode circle, max_aoe 2, min_aoe 1`
- **Damage/Effects:** `damage 8, Burn 8`

#### Inspire (`Inspire`)
- **Template:** `spell`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 6, max_aoe 0`
- **Damage/Effects:** `damage 0, ManaGain 2`

#### Jolt (`Jolt`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_aoe 0, min_range 1, max_range 5`
- **Damage/Effects:** `damage 1, knockback 3, KnockbackDirectionIsFacingDirection 1`

#### Lightning Surge (`LightningSurge`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_aoe 0, max_range X*2, X_is turn_count`
- **Damage/Effects:** `raw_damage X*2, Stun [1 X*.1]`

#### Switch (`MageSwap`)
- **Template:** `swap`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `None`

#### Teleport (`MageTeleport`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `None`

#### Magic Missile (`MagicMissile`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_aoe 0, max_range 20`
- **Damage/Effects:** `damage 3, cant_miss true`

#### Magnify (`Magnify`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TempRangeUp 1, TempBasicAttackBonusAOE 1`

#### Mana Meld (`ManaMeld`)
- **Template:** `spell`
- **Cost:** `mana X, infcantrip true, X_cant_be_zero true, disallow_cost_modification true`
- **Target/Shape:** `min_range 1, max_range 3, max_aoe 0, X_is current_mana, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, ManaGain X`

#### Mega Blast (`MegaBlast`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 13`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe 3, aoe_considers_character_size true, aoe_excludes_self true`
- **Damage/Effects:** `damage 15`

#### Meteor Storm (`MeteorStorm`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 10`
- **Target/Shape:** `max_aoe 3, max_range 5+level, aoe_chance .4+.2*level, knockback_mode zero, can_multihit true`
- **Damage/Effects:** `damage 10, Stun [1, .10+.1*level], SpawnFlames [1, .20+.1*level], BounceRock [1 .2]`

#### Replicate (`Replicate`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `DoubleCastSpell 1`

#### Shatter (`Shatter`)
- **Template:** `melee_attack`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1+bonus_melee_ability_damage, status Freeze, Slow 2`

#### Chill (`Slow`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `min_range 1, max_range 5+2*level, max_aoe 0`
- **Damage/Effects:** `damage 0, Slow 1`

#### Smolder (`Smolder`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_aoe 0, max_range 5`
- **Damage/Effects:** `damage 0, Burn 1, SpeedUp 1`

#### Surf (`Surf`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_aoe 2, max_range 4`
- **Damage/Effects:** `damage 3, knockback 2, elements [, Water, ]`

#### Teach (`Teach`)
- **Template:** `targeted_status`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 5`
- **Damage/Effects:** `TempManaCostReduction 1`

#### Telefrag (`Telefrag`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `max_range 20, restrictions [aoe_must_be_displaceable must_have_animate_character]`
- **Damage/Effects:** `damage 5, type spell, makes_contact true, IgnoreSelf 1`

#### Thunderburst (`Thunderburst`)
- **Template:** `spell`
- **Cost:** `mana 12, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode 8cross, max_aoe 10, min_aoe 1`
- **Damage/Effects:** `damage 12, Stun [1, .5]`

#### Tri-Attack (`TriAttack`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_aoe 0, max_range 5`
- **Damage/Effects:** `damage 4, Burn 1, Slow 1, Stun [1 .05]`

#### Wall of Fire (`WallOfFire`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `range_mode cross, max_range 10, aoe_mode perpline, min_aoe -10, max_aoe 10`
- **Damage/Effects:** `damage 0, Burn 1`

#### Warp (`Warp`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_range 20, range_mode diagcross, range_considers_character_size false`
- **Damage/Effects:** `None`

#### Whirlpool (`WaterSphere`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_aoe 2, max_range 4, knockback_mode target_to_tile, knockback_modifier rotate_cw`
- **Damage/Effects:** `damage 0, knockback 1, Confusion 1, ChangeTile WaterTile_Current, TurnRight 1`

#### Wind Slash (`WindSlash`)
- **Template:** `spell`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `target_mode direction, aoe_mode line, min_aoe 1, max_aoe 10, aoe_considers_character_size true, aoe_excludes_self true, knockback_mode orientation`
- **Damage/Effects:** `damage level, knockback level, elements [, Wind, ]`

### Passives

| Passive Name | Internal ID | Description |
| :--- | :--- | :--- |
| **Burning Paws** | `BurningPaws` | Your basic action inflicts Burn 2. |
| **Charge Up** | `ChargeUp` | If you end your turn with 0 mana, the next spell you cast is free |
| **Elemental Attunement** | `ElementalAttunement` | Casting elemental spells imbues your basic attack with those elements and relevant effects for the rest of the battle. |
| **Three** | `EnergyStorm` | Every 3rd spell you cast in a turn is cast twice. |
| **Fire Aspect** | `FireArmor` | Fire immunity. Inflict Burn 1 on units that contact you. Your Fire element damage is increased by 1 and inflicts +1 Burn. |
| **Five** | `Five` | When you end your turn with exactly 5 mana or HP, gain +5 [img:shield] and temporarily gain +5 Kinetic Spikes until the end of your next turn . |
| **Four** | `Four` | When you end your turn with exactly 4 mana or HP, gain +1 [img:int] and +1 Magic Damage. |
| **Force Field** | `HolyMantel` | At the start of every third turn, gain +1 [img:divineshield]. |
| **Ice Aspect** | `IceArmor` | Ice immunity. You can damage frozen units. Units that contact you take 1 Ice Damage, Slow 2, and have a 5% chance to Freeze. |
| **Ice Paws** | `IcePaws` | Your basic attack deals Ice Damage, inflicts Slow 2, and has a 20% chance to Freeze. You can damage frozen units. |
| **Latent Energy** | `LatentEnergy` | When an ally spends mana, Gain +2 Magic Damage until the next time you use magic. |
| **Learn From Me** | `LearnFromMe` | When you cast a spell, all allied cats gain that spell in their bonus slot. |
| **Light Up the Stage** | `LightUpTheStage` | At the end of your turn, emit 2 Sparkles for each turn you've taken. |
| **Lightning Aspect** | `LightningArmor` | Electric immunity. When you deal Electric Damage, gain +1 Charge. |
| **Lightning Paws** | `LightningPaws` | Your basic attack deals +2 Electric Damage and has a 15% chance to Stun. |
| **Long Cast** | `LongCast` | Tile-targeted spells gain +5 Range. |
| **Magic Guru** | `MagicGuru` | Your allies have +1 Mana Regeneration. When an ally spends 7+ mana to cast a spell, they gain All Stats Up. |
| **Synthesize** | `Micronaps` | Gain +1 [img:int] at the start of each turn. |
| **One** | `One` | When you end your turn, if you cast exactly 1 spell, double cast your next spell. |
| **Overload** | `Overload` | When you cast a spell, deal 3 random elemental damage to adjacent tiles. |
| **Paw Missile** | `PawMissile` | Your basic attack is Magic Missile. (its damage scales with [img:int]). |
| **Epiphany** | `Recharged` | +5 starting mana. +5 Mana Regeneration. Lose all unspent mana at the end of each of your turns |
| **Resonance** | `Resonance` | When you cast a spell gain +1 Magic Damage for the rest of the turn. |
| **Splash Damage** | `Shrapnel` | Your basic attack deals 2 Magic splash damage. |
| **Two** | `Two` | When you end your turn, if you cast exactly 2 spells, gain +1 Bonus Attack. When you end your turn, if you have exactly 2 mana, gain +1 Bonus Attack. |

---

## Class: Monk (`Monk`)

### Actives & Attacks

#### Air Burst (`AirBurst`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `min_aoe 1, max_aoe 1, max_range 5+bonus_range, aoe_mode diagcross`
- **Damage/Effects:** `damage 0, knockback 1, elements [, Wind, ]`

#### Anneal (`Anneal`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Shield 1`

#### Summon Apprentice (`Apprentice`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 9, must_not_be_a_summon true`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Melee Attack (`BasicMonkMelee`)
- **Template:** `melee_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage "(5+bonus_melee_damage+1)/2"`

#### Bruise (`Bruise`)
- **Template:** `self_buff`
- **Cost:** `mana 6, cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `HeavyHits 1`

#### Cartwheel (`Cartwheel`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `range_mode diagcross, max_range 4, restrictions [must_be_moveable must_move], straight_shot true, allow_diagonals true`
- **Damage/Effects:** `None`

#### Charge Fists (`ChargeFists`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ChargeFists 1`

#### Combo Pull (`ComboPull`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 2, max_range 4+bonus_range`
- **Damage/Effects:** `damage 1+bonus_ranged_damage, StanceSwitchToMelee 1, RefreshActPoints 1`

#### Combo Throw (`ComboThrow`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 2+bonus_melee_ability_damage, type melee, knockback 3, StanceSwitchToRanged 1, RefreshActPoints 1`

#### Deep Dive (`DeepDive`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `SafeDie 1, stacks 2, revive_health 1, Shield 15, AllStatsUp 1`

#### Ocular Pat Down (`DetectWeakness`)
- **Template:** `targeted_status`
- **Cost:** `mana 7, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 4+bonus_range`
- **Damage/Effects:** `Marked 1, MagicWeakness 1`

#### Five Point Palm Exploding Heart Technique (`DoomPunch`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, Doomed 1`

#### Double Dragon (`DoubleDragon`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 1, max_range 3, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Dragon Punch (`DragonPunch`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5, type spell, knockback 3, makes_contact false, Confusion 1, VisualFX MagicMissleBlast`

#### Empty Mind (`EmptyMind`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, once_per_fight true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `EmptyMind 1`

#### Finisher (`Finisher`)
- **Template:** `dash_attack`
- **Cost:** `cantrip true, mana 6`
- **Target/Shape:** `max_range 3, X_is storm_count`
- **Damage/Effects:** `raw_damage X*2, show_damage_on_0 true`

#### Fist of Fate (`FistOfFate`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `target_mode random_tile, max_range 20, min_range 1, restrictions [must_be_moveable must_be_adjacent_to_enemy_fistoffate]`
- **Damage/Effects:** `None`

#### Flying Fist (`FlyingFist`)
- **Template:** `melee_spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_aoe 2+X, max_aoe 2+X, X_is this_ability_storm_count, restrictions aoe_must_exist`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, type physical_spell, knockback 1, elements [, Wind, ]`

#### Hadouken (`Hadouken`)
- **Template:** `straightshot_attack`
- **Cost:** `infcantrip true, mana 9`
- **Target/Shape:** `max_aoe 10`
- **Damage/Effects:** `damage 10, type spell, VisualFX MagicMissleBlast`

#### Hip Toss (`HipToss`)
- **Template:** `throw_attack`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `max_range 2, min_range 2, restrictions none`
- **Damage/Effects:** `damage 3+bonus_melee_ability_damage`

#### Hop n' Block (`HopAndBlock`)
- **Template:** `jump_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `max_range 4`
- **Damage/Effects:** `damage 0, type none, cant_miss true, makes_contact false, Shield 2`

#### Hundred Hand Slap (`HundredHandSlap`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 15`
- **Target/Shape:** `aoe_considers_character_size false, target_mode tile, restrictions must_have_character, range_mode standard, aoe_mode standard, min_range 1, max_range 1, min_aoe 0, max_aoe 0, multihit 10, randomize_knockback_direction_except_for_finisher true`
- **Damage/Effects:** `damage "1+bonus_melee_ability_damage/5", type melee, knockback 10`

#### Kamehameha (`Kamehameha`)
- **Template:** `spell`
- **Cost:** `cantrip true, mana 0, once_per_fight 3-X`
- **Target/Shape:** `max_aoe 0, max_range 5, X_is custom, restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 14`

#### Ki Burst (`KiBurst`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `target_mode none, aoe_mode standard, min_aoe 1, max_aoe 1, aoe_considers_character_size true, aoe_excludes_self true`
- **Damage/Effects:** `damage 1, knockback 1`

#### Kinetic Charge (`KineticCharge`)
- **Template:** `self_buff`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, status KineticSpikes, stacks 1, turns 1, expires_on_begin_turn true`

#### Meditate (`Meditate`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 8, Sleep 8, Shield 8, AllStatsUp 2`

#### Nirvana (`Nirvana`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana "4-clamp(floor(X/7), 0, 1)"`
- **Target/Shape:** `X_is current_shield`
- **Damage/Effects:** `Shield 1, IntelligenceUp 1`

#### One Punch (`OnePunch`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 0, once_per_fight true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1, Instakill 25`

#### One With the Wind (`OneWithTheWind`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TempMovement 20`

#### Perfect Form (`PerfectForm`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `X_is custom`
- **Damage/Effects:** `Shield X, MonkStanceSwitch 1`

#### Pogo (`Pogo`)
- **Template:** `jump_attack`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `max_range 3, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, aoe_excludes_self false, restrictions none, always_bounce true`
- **Damage/Effects:** `damage 3+bonus_melee_ability_damage, IgnoreSelf 1`

#### Porcupine (`Porcupine`)
- **Template:** `self_buff`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, status Thorns, stacks 2, turns 1, expires_on_begin_turn true`

#### Position (`Position`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_range 2, min_range 2`
- **Damage/Effects:** `None`

#### Propel (`Propell`)
- **Template:** `dash_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `damage 3+bonus_melee_ability_damage`

#### Pummel (`Pummel`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `X_is this_ability_storm_count`
- **Damage/Effects:** `damage 1+X*3`

#### Quick Attack (`QuickAttack`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_range 1+X*2, min_range 1, X_is custom`
- **Damage/Effects:** `None`

#### Really Fast Run (`ReallyFastRun`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `range_mode cross, max_range 4, restrictions [must_be_moveable must_move], straight_shot true, allow_diagonals true`
- **Damage/Effects:** `None`

#### Release Energy (`ReleaseEnergy`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 12`
- **Target/Shape:** `Default`
- **Damage/Effects:** `RandomMagicMissile 10`

#### Reverberate (`Reverberate`)
- **Template:** `melee_attack`
- **Cost:** `mana 22-X*3, cantrip true`
- **Target/Shape:** `target_mode none, aoe_mode cross, X_is storm_count`
- **Damage/Effects:** `damage 0, type spell, knockback 2, incidentally_collects_pickups false`

#### Sidestep (`SideStep`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

#### Slapback (`Slapback`)
- **Template:** `melee_attack`
- **Cost:** `requires_reload true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 2+bonus_melee_ability_damage, crit_chance 50%, type melee`

#### Charge Spirit Bomb (`SpiritBomb`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TransformAbility ThrowSpiritBomb`

#### Stone Fists (`StoneFists`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `X_is current_shield`
- **Damage/Effects:** `TempStrengthUp X, TempDexterityUp X`

#### Way of the Mantis (`TrainArms`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 12`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ExtraBasicAttacks_Status 1`

#### Way of the Turtle (`TrainBody`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 9`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Brace 1`

#### Way of the Hare (`TrainLegs`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 9`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ExtraBasicMoves_Status 1`

#### Way of the Owl (`TrainMind`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 13`
- **Target/Shape:** `Default`
- **Damage/Effects:** `DoubleCastSpellsEachTurn_Status 1`

#### Transcend (`Transcend`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Cleanse 0, Shield 1`

#### Unbridled Hits (`UnbridledHits`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `X_is custom, multihit X+1`
- **Damage/Effects:** `damage 2+bonus_melee_ability_damage`

#### Unimpeded Lunge (`UnimpededLunge`)
- **Template:** `dash_attack`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_range X+1, X_is custom`
- **Damage/Effects:** `damage X+1, knockback X+1`

#### Warm Up Stretch (`WarmupStretch`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 8-X*2`
- **Target/Shape:** `X_is custom`
- **Damage/Effects:** `DexterityUp 1, SpeedUp 1`

### Passives

| Passive Name | Internal ID | Description |
| :--- | :--- | :--- |
| **Brick Skin** | `BrickSkin` | Any [img:shield] you gain is increased by 2. |
| **Cobra Style** | `CobraStyle` | When an enemy moves into an adjacent tile, perform a weak melee attack on it. |
| **Counter Barrage** | `CounterBarrage` | When you take damage from an enemy attack, gain +1 Bonus Attack. |
| **Dancing Lights** | `DancingLights` | When you switch stances, for each empty armor slot, emit a Sparkle. If all slots are empty gain +1 to a random stat. |
| **Energy Fists** | `EnergyFists` | Emit a Sparkle when you use your basic attack. |
| **Flow State** | `FlowState` | When you deal damage to another unit, gain +1 [img:str] and +2 [img:dex] until the end of the turn. |
| **Harden** | `Harden` | When you gain [img:shield], also gain temporary Brace 1. |
| **Iron Skin Technique** | `IronSkin` | Gain +2 [img:shield] when you land a critical hit. +10% critical chance. |
| **Jagged Edges** | `JaggedEdges` | When you lose [img:shield], gain +1 Thorns. |
| **Jet Fists** | `JetFists` | Your melee attacks and abilities blow wind through the tiles they hit. |
| **Long Arms** | `LongArms` | +1 Range and +1 Reach. |
| **Mind Breaker** | `MindBreaker` | Your basic attack inflicts Magic Weakness 1. |
| **Mixup** | `Mixup` | When you switch stances, your next basic attack this turn is critical. |
| **Monkey Style** | `MonkeyStyle` | 15% chance to block damage and counter-attack. |
| **Perfect Technique** | `PerfectTechnique` | While in ranged stance, You have +1 Range and +2 Magic Damage. While in melee stance, you have +1 Brace. |
| **Rapid Flow** | `RapidFlow` | When you switch stances, do a spin attack that hits all adjacent units. |
| **Running Jab** | `RunningJab` | When you end your movement, automatically use your basic attack if an enemy is in range. |
| **Safe Switching** | `SafeSwitching` | When you switch stances, gain +2 [img:shield]. |
| **Spread the Pain** | `SpreadThePain` | Deal 2 extra damage the first time you damage each unit each turn. |
| **Tenderize** | `Tenderize` | Your basic melee attacks inflict Bruise 1. |
| **Turnabout** | `Turnabout` | Your basic melee attacks inflict Confusion 1 and make units face away from you. |
| **Unburdened Motion** | `UnburdenedMotion` | +1 [img:spd] and +10% dodge chance for each empty armor slot. If all of your armor slots are empty, you can use your movement action an extra time. |
| **Unburdened Strikes** | `UnburdenedStrikes` | +10% critical hit chance and +25% critical hit damage for each empty armor slot. If all of your armor slots are empty, counter-attack whenever you get hit. |
| **Unburdened Thoughts** | `UnburdenedThoughts` | +1 [img:int] and +1 [img:cha] for each empty armor slot. If all of your armor slots are empty, your spells cost 1 less mana. |
| **Unstoppable!** | `Unstoppable` | You're immune to knockback, Stun, Slow, and other mobility debuffs. |

---

## Class: Necromancer (`Necromancer`)

### Actives & Attacks

#### Absorb Soul (`AbsorbSoul`)
- **Template:** `spell`
- **Cost:** `cantrip true, mana 0`
- **Target/Shape:** `min_range 1, max_range 5, max_aoe 0, restrictions [must_have_ally must_not_have_boss must_have_living_character]`
- **Damage/Effects:** `damage 0, ManaSteal -1, SafeDie 1`

#### Eternal Servitude (`AnimateDead`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 12`
- **Target/Shape:** `min_range 1, max_range 4, max_aoe 0, aoe_restrictions [must_have_corpse enemies_only], restrictions aoe_must_exist`
- **Damage/Effects:** `heal 0, type spell, can_revive true, HealPercentMaxHP 100, FactionConversion 1, CaptureFamiliar 1`

#### Leech Shot (`BasicNecroRanged`)
- **Template:** `lobbed_attack`
- **Cost:** `Free`
- **Target/Shape:** `min_range 1, max_range 3+bonus_range`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, Leeches 1`

#### Blood Geyser (`BloodGeyser`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `max_aoe 0, min_range 1, max_range 4, X_is max_health`
- **Damage/Effects:** `damage "ceil(X/2)", Fear 2`

#### Blood Rain (`BloodRain`)
- **Template:** `spell`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero, aoe_restrictions allies_only, aoe_excludes_self true`
- **Damage/Effects:** `heal 1`

#### Bloodletting (`Bloodletting`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `max_aoe 0, min_range 1, max_range 3`
- **Damage/Effects:** `damage 0, Cleanse 0, Purge 0, Bleed 5`

#### Carrion Shot (`CarrionShot`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 3+bonus_range`
- **Damage/Effects:** `damage 1, Leeches 1`

#### Clew of Leeches (`ClewOfLeeches`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `min_range 1, max_range 5+bonus_range, restrictions [must_have_animate_character]`
- **Damage/Effects:** `damage 0, Imprison CharmedLeech`

#### Coffin Flop (`CoffinFlop`)
- **Template:** `jump_attack`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `max_range 2, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, aoe_excludes_self false`
- **Damage/Effects:** `type none, damage 0`

#### Curse (`Curse`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 3`
- **Damage/Effects:** `LuckUp -4`

#### Dark Step (`DarkStep`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_range 4`
- **Damage/Effects:** `None`

#### Death Bloom (`DeathBloom`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 0`
- **Target/Shape:** `max_range 20, splash_damage_aoe_begin 1, restrictions must_have_destructible_corpse`
- **Damage/Effects:** `damage 0, cant_miss true, ExplodeCharacter_DeathBloom 5`

#### Debone (`Debone`)
- **Template:** `melee_attack`
- **Cost:** `mana 7, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 2+bonus_melee_ability_damage, Weakness 1, EquipPermanentItem BoneClub`

#### Demonic Pact (`DemonicPact`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 10, main_turn_only true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `RandomInjury 1, TakeExtraTurn 1`

#### Dig Up the Dead (`DigUpTheDead`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 16`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `None`

#### Donate Blood (`DonateBlood`)
- **Template:** `spell`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 3, max_aoe 0`
- **Damage/Effects:** `heal 5`

#### Evil Incarnate (`EvilIncarnate`)
- **Template:** `spell`
- **Cost:** `mana 12, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero, aoe_restrictions enemies_only`
- **Damage/Effects:** `damage 0, Fear 1`

#### Feed (`Feed`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `aoe_restrictions must_have_destructible_corpse, restrictions aoe_must_exist`
- **Damage/Effects:** `damage 0, incidentally_collects_pickups false, VaporizeCorpse 1, AddLeechesStatus 1`

#### Flatline (`Flatline`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 3, must_not_be_a_summon true`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Flesh Golem (`FleshGolem`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 0, once_per_fight true`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Forbidden Famine (`ForbiddenFamine`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 0, once_per_fight true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero, aoe_restrictions enemies_only`
- **Damage/Effects:** `damage 0, Weakness 5, Poison 2, Madness 2`

#### Full Moon (`FullMoon`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_aoe 1, max_range 5`
- **Damage/Effects:** `damage 0, Lifesteal 1`

#### Giga Drain (`GigaDrain`)
- **Template:** `melee_attack`
- **Cost:** `mana X, infcantrip true, X_cant_be_zero true, disallow_cost_modification true`
- **Target/Shape:** `X_is current_mana`
- **Damage/Effects:** `damage X, type spell, piercing true, Leech 1`

#### Go Limp (`GoLimp`)
- **Template:** `self_buff`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TempInjuryImmunity 1`

#### Gravecrawl (`Gravecrawl`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `None`

#### Hush (`Hush`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `Sleep 1`

#### Leech Swarm (`LeechSwarm`)
- **Template:** `lobbed_attack`
- **Cost:** `mana 12, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, aoe_excludes_self true, knockback_mode zero`
- **Damage/Effects:** `damage 0, type status_spell, Leeches 3`

#### Leeches (`Leeches`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `min_range 1, max_range 3+bonus_range`
- **Damage/Effects:** `damage 0, Leeches 1`

#### Lifedrain (`LifeDrain`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0`
- **Damage/Effects:** `damage 2, Leech 1`

#### Decompose (`MaggotArmy`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 1, max_range 4, max_aoe 0, restrictions must_have_destructible_corpse`
- **Damage/Effects:** `damage 0, VaporizeCorpse 1, ObjectOnHitCharacter CharmedLeech, ObjectOnHitCharacter CharmedLeech, ObjectOnHitCharacter CharmedLeech`

#### Mass Psychosis (`MassPsychosis`)
- **Template:** `spell`
- **Cost:** `mana 15, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero, aoe_restrictions enemies_only`
- **Damage/Effects:** `damage 0, Madness 1`

#### Pestilence (`Pestilence`)
- **Template:** `spell`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero`
- **Damage/Effects:** `damage 1`

#### Reanimate (`Reanimate`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 1, max_range 4, max_aoe 0, aoe_restrictions must_have_corpse, restrictions aoe_must_exist`
- **Damage/Effects:** `Reanimate 50%`

#### Reap (`Reap`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `min_range 1, max_range 20, restrictions aoe_must_exist, aoe_restrictions must_have_low_health_character, low_health_character_threshold 5`
- **Damage/Effects:** `damage 0, IgnoreSelf 1, VaporizeTarget 1, VisualFXTile sytheCut`

#### Reaper Step (`ReaperStep`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `max_range 1+X, X_is custom`
- **Damage/Effects:** `None`

#### Rebirth (`Rebirth`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_range 20, aoe_restrictions must_have_destructible_corpse, restrictions aoe_must_exist`
- **Damage/Effects:** `damage 0, makes_contact true, VaporizeCorpse 1`

#### Replace (`Replace`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `min_range 1, max_range 20, restrictions aoe_must_exist, aoe_restrictions familiars_only`
- **Damage/Effects:** `damage 0, IgnoreSelf 1, VaporizeTarget 1`

#### Scare (`Scare`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `aoe_mode normal, min_range 1, max_range 20, max_aoe 1, restrictions [must_be_moveable must_be_directly_in_front_of_enemy], knockback_mode character_to_tile`
- **Damage/Effects:** `damage 0, knockback 4, type spell, IgnoreSelf 1`

#### Seance (`Seance`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Shriek (`Shriek`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 9`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe 3, aoe_considers_character_size true, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, Fear 1, Confusion 2, Madness 2`

#### Soul Link (`SoulLink`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `max_aoe 1, min_range 0, max_range 4`
- **Damage/Effects:** `SoulLink 1`

#### Dark Ritual (`SoulSuck`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `aoe_restrictions must_have_destructible_corpse, restrictions aoe_must_exist`
- **Damage/Effects:** `damage 0, type melee, incidentally_collects_pickups false, VaporizeCorpse 1, FreeSpell 1`

#### Soul Transfer (`SoulTransfer`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 1`
- **Target/Shape:** `max_aoe 0, min_range 1, max_range 4, X_is max_health`
- **Damage/Effects:** `heal 4, piercing true, cant_miss true, ConstitutionUp 1`

#### Spider Egg (`SpiderEgg`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `min_range 1, max_range 3+bonus_range`
- **Damage/Effects:** `damage 0, SpiderInfested 1`

#### Summon Bones (`SummonBones`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 4, max_aoe 0, restrictions must_have_destructible_corpse`
- **Damage/Effects:** `damage 0, VaporizeCorpse 1, ObjectOnHitCharacter SkeletonCatFamiliar`

#### Summon Shade (`SummonShade`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 13, must_not_be_a_summon true`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Trade Life (`TradeLife`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 1, max_range 3, max_aoe 0, restrictions [must_have_ally must_not_have_boss]`
- **Damage/Effects:** `damage 0, TradeLife 1`

#### Unearth (`Unearth`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_range 1`
- **Damage/Effects:** `None`

#### We Are One (`WeAreOne`)
- **Template:** `spell`
- **Cost:** `mana 15, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero, aoe_restrictions enemies_only`
- **Damage/Effects:** `damage 0, SoulLink 1`

#### Weakness (`Weakness`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_aoe 0, min_range 1, max_range 4`
- **Damage/Effects:** `damage 0, Weakness 5`

#### Whisper (`Whisper`)
- **Template:** `melee_spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type status_spell, incidentally_collects_pickups false, Fear 1, Madness level`

### Passives

| Passive Name | Internal ID | Description |
| :--- | :--- | :--- |
| **Bed Bugs** | `BedBugs` | You start battles with 2 beefy leech familiars. |
| **Cambion Conception** | `CambionConception` | When you're downed, spawn a demon kitten familiar. |
| **Chains of Guilt** | `ChainsOfGuilt` | When an enemy downs you and it wasn't a boss, it joins your party permanently. |
| **Corpse Connoisseur** | `CorpseConnoisseur` | Start each battle with 2-3 corpses near you. When you destroy a corpse, heal 2 HP and spawn a food pickup. |
| **Dark Priest** | `DarkPriest` | At the start of each battle, if you don't have a weapon, gain a temporary Soul Dagger weapon. |
| **Servus Mortem** | `DeathIncarnate` | Destroy a random non-boss enemy at the start of each battle. |
| **Eternal Health** | `EternalHealth` | Suffer only Jinxed when downed. When your party wins a battle, if you were downed, heal to full. |
| **Immortal Leeches** | `ImmortalLeeches` | When a unit you inflicted Leeches on dies or loses its leeches, your next basic attack inflicts that many additional leeches. |
| **Infected** | `Infected` | When you down a unit, reanimate it with 50% HP. |
| **Infinite Rebirth** | `InfiniteRebirth` | At the end of each round, if there is a body on the map and you're downed, you respawn on that tile with 1 HP and +10 temporary Speed. If that body was a party member, you spawn with full HP instead. |
| **Last Grasp** | `LastGasp` | When you're downed, deal 6 damage to each enemy and heal 6 HP to all allies. Bonus ability: Seppuku |
| **Leech Mother** | `Leechmother` | Your basic attack spawns a leech familiar. |
| **Numbing Leeches** | `NumbingLeeches` | Your basic attack deals 0 damage but its status and hit effects are tripled. |
| **Offload Pain** | `OffloadPain` | When you heal, deal 1 damage to each enemy. |
| **One With Nothing** | `OneWithNothing` | If you end your turn with 0 mana, your Mana Regeneration is doubled. |
| **Parasitic** | `Parasitic` | When you gain health, spawn a leech familiar. |
| **Relentless Dead** | `RelentlessDead` | At the end of each round, spawn a zombie kitten familiar onto a random tile. |
| **Sacrificial Lamb** | `SacrificialLamb` | When you're downed, allies gain All Stats Up and take an extra turn. |
| **Soul Bond** | `SoulBound` | Your basic attack inflicts Soul Link. |
| **Spread Sorrow** | `SpreadSorrow` | When you inflict a debuff to an enemy, inflict that same debuff on another random enemy. |
| **Superstition** | `Superstition` | Your basic attack inflicts -1[img:lck].  When a unit damages you, inflict -1[img:lck] on it. |
| **Torpor** | `Torpor` | While you're downed, your basic attack is Haunt. Your body gains +6 corpse HP. |
| **Undeath** | `Undeath` | When you're downed, reanimate each ally to 33% HP. (Once per battle.) |
| **Vampirism** | `Vampirism` | Your basic attack has lifesteal. |
| **Worm Lord** | `WormLord` | When you take damage, spawn a leech familiar. |

---

## Class: Psychic (`Psychic`)

### Actives & Attacks

#### Alter DNA (`AlterDNA`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana X, X_cant_be_zero true, disallow_cost_modification true`
- **Target/Shape:** `min_range 1, max_range 20, max_aoe 0, X_is current_mana, restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 0, type status_spell, RandomStatUp "ceil(X/3)"`

#### Ancestral Recall (`AncestralRecall`)
- **Template:** `self_buff`
- **Cost:** `mana 8, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `UpgradeRandomAbility 1, AllStatsUp 1`

#### Asteroid (`Asteroid`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 9`
- **Target/Shape:** `min_range 1, max_range 20, max_aoe 0, restrictions must_have_line_of_sight, knockback_mode zero`
- **Damage/Effects:** `damage 5, Burn 1, BounceRock SmallLavaRock`

#### Psychic Pull (`BasicPsychicPull`)
- **Template:** `spell`
- **Cost:** `move_points 0, act_points 1`
- **Target/Shape:** `max_aoe 0, max_range 20, knockback_mode target_to_character`
- **Damage/Effects:** `damage 2+bonus_basic_spell_damage, knockback 1, elements [, Gravity, ]`

#### Become Entropy (`BecomeEntropy`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 14`
- **Target/Shape:** `min_range 1, max_range 20, max_aoe 0, restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 0, PreventDeathTransforms 1, Vaporize 1`

#### Blinding Flash (`BlindingFlash`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_aoe 3, target_mode none, aoe_excludes_self true, aoe_restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 0, Blind 2`

#### Chaos Swap (`ChaosSwap`)
- **Template:** `swap`
- **Cost:** `mana 2, infcantrip true`
- **Target/Shape:** `target_mode random_tile, max_range 20`
- **Damage/Effects:** `None`

#### Cumulative Blast (`CumulativeBlast`)
- **Template:** `spell`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `max_aoe 0, max_range 20, restrictions must_have_line_of_sight, X_is custom`
- **Damage/Effects:** `damage 1+X`

#### Echo (`Echo`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 1`
- **Target/Shape:** `target_mode random_tile, min_range 1, max_range 20, range_mode last_targeted_tile`
- **Damage/Effects:** `None`

#### Extra Turn? (`ExtraTurnQuestion`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4, main_turn_only true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Stun 1, TempNoManaRegen 1`

#### Fast Forward (`FastForward`)
- **Template:** `spell`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero, aoe_excludes_self false, aoe_restrictions [allies_only character_has_turns_left]`
- **Damage/Effects:** `type status_spell, TempInitiativeChange 9999`

#### Flash Forward (`FlashForward`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `min_range 1, max_range 20, range_mode normal`
- **Damage/Effects:** `None`

#### Flicker (`Flicker`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `min_range 2, max_range 2, range_mode normal, restrictions [aoe_must_be_displaceable]`
- **Damage/Effects:** `damage 0, makes_contact true, IgnoreSelf 1, Displace 1`

#### Flip (`Flip`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `min_range 0, max_range 20, max_aoe 0, restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 0, type status_spell, Confusion 1, TurnAround 1`

#### Gravity Blast (`ForceBlast`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `target_mode none, max_aoe 1, aoe_excludes_self true, X_is is_at_max_mana`
- **Damage/Effects:** `damage 0, knockback 10, formula X*10, OverrideKnockbackDamage X*10`

#### Gravity Wave (`ForceCone`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe 3, aoe_considers_character_size true, aoe_excludes_self true`
- **Damage/Effects:** `damage 2, knockback 4, OverrideChainKnockback 1`

#### Future Sight (`FutureSight`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 1, max_range 20, max_aoe 0, restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 0, type status_spell, BackflipWhenTargeted 1`

#### Glare (`Glare`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `min_range 0, max_range 20, max_aoe 0, restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 0, type status_spell, Madness 1`

#### Hallucinate (`Hallucinate`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, restrictions must_have_line_of_sight, aoe_restrictions [exclude_blocking]`
- **Damage/Effects:** `None`

#### Increase Gravity (`IncreaseGravity`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `min_range 1, max_range 20, max_aoe 0, aoe_excludes_self true, restrictions must_have_line_of_sight, X_is is_at_max_mana`
- **Damage/Effects:** `raw_damage X*6, formula X, Immobile 1`

#### Inversion (`Inversion`)
- **Template:** `swap`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `max_range 20, restrictions [must_be_swappable must_have_line_of_sight]`
- **Damage/Effects:** `None`

#### Gravity Pull (`MagnetPull`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `min_aoe 1, max_aoe 1, max_range 5, knockback_mode tile_to_target`
- **Damage/Effects:** `damage 0, knockback 1, elements [, Gravity, ]`

#### Manifest (`Manifest`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `range_mode cross, max_range 20, restrictions [aoe_must_be_displaceable must_have_animate_character must_have_line_of_sight]`
- **Damage/Effects:** `damage 5, type spell, makes_contact true, IgnoreSelf 1`

#### Mass Hysteria (`MassHysteria`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 10`
- **Target/Shape:** `aoe_mode all, target_mode none, aoe_excludes_self true, aoe_restrictions [must_have_line_of_sight exclude_allies]`
- **Damage/Effects:** `damage 0, type status_spell, Charmed 1, TakeExtraTurn 1`

#### Mass Mana Leech (`MassManaLeech`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_aoe 3, target_mode none, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, type status_spell, ManaLeeches 2, Weakness 2`

#### Mega Grav (`MegaGrav`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `target_mode none, max_aoe 3, aoe_excludes_self true`
- **Damage/Effects:** `damage 2, min_dist 3, max_dist 20, damage inherit`

#### Mimic (`Mimic`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `min_range 1, max_range 20, max_aoe 0, restrictions [must_have_line_of_sight must_have_player_cat]`
- **Damage/Effects:** `MimicMetronome 1`

#### Mindblast (`MindBlast`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `target_mode none, min_aoe 1, max_aoe 3`
- **Damage/Effects:** `damage 0, knockback 3, Stun [1 .1], Madness 1`

#### Mind Control (`MindControl`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 15`
- **Target/Shape:** `min_range 1, max_range 20, max_aoe 0, aoe_excludes_self true, restrictions [aoe_must_exist must_have_line_of_sight], aoe_restrictions [enemies_only]`
- **Damage/Effects:** `damage 0, type status_spell, Charmed 1`

#### Mindcrack (`MindCrack`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `aoe_mode all, target_mode none, aoe_excludes_self true, aoe_restrictions must_have_line_of_sight`
- **Damage/Effects:** `type status_spell, MagicWeakness 2`

#### Mind Meld (`MindMeld`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 10, main_turn_only true`
- **Target/Shape:** `min_range 1, max_range 3, max_aoe 0, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, type status_spell, TakeExtraTurn 1`

#### Order (`Order`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `min_range 1, max_range 20, max_aoe 0, aoe_excludes_self true, restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 0, type status_spell, ForceMoveAndAttack 1`

#### Pass (`Pass`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 3, must_be_first_action true, main_turn_only true`
- **Target/Shape:** `min_range 1, max_range 20, max_aoe 0, restrictions must_have_line_of_sight`
- **Damage/Effects:** `TakeExtraTurn 1`

#### Ping (`Ping`)
- **Template:** `spell`
- **Cost:** `requires_reload true, mana 0`
- **Target/Shape:** `max_aoe 0, max_range 20, restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 1`

#### Psyflutter (`PsyFlutter`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 3, max_range 3, range_mode normal`
- **Damage/Effects:** `None`

#### Psychic Choke (`PsychicChoke`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_aoe 0, max_range 20, knockback_mode zero, restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 2, Bruise 1`

#### Puppet (`Puppet`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `min_range 1, max_range 20, max_aoe 0, aoe_excludes_self true, restrictions [aoe_must_exist must_have_line_of_sight], aoe_restrictions [enemies_only]`
- **Damage/Effects:** `damage 0, type status_spell, CharmedFacingForceAttack 1`

#### Reality Scramble (`RealityScramble`)
- **Template:** `spell`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero`
- **Damage/Effects:** `damage 0, type status_spell, cant_miss true`

#### Reset (`Reset`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 16, once_per_fight true`
- **Target/Shape:** `aoe_mode all, target_mode none, aoe_excludes_self false, aoe_restrictions none`
- **Damage/Effects:** `type status_spell, PurgeAll 1, Revive 100%, PurgeAll 1, FullHeal 1`

#### Shatter the Sky (`SkyShatter`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_aoe 1, max_range 20, max_aoe 0, restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 0, ChangeTile FloatingGlassTile`

#### Slipstream (`Slipstream`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `range_mode 8cross, max_range 3, restrictions [must_be_moveable must_move], straight_shot true, allow_diagonals true`
- **Damage/Effects:** `None`

#### Snatch (`Snatch`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 1`
- **Target/Shape:** `max_aoe 0, max_range 20, restrictions [must_have_tag must_have_line_of_sight], target_requires_tag pickup`
- **Damage/Effects:** `damage 0, CollectsPickups 1`

#### Stasis (`Stasis`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `min_range 1, max_range 20, max_aoe 0, restrictions must_have_line_of_sight`
- **Damage/Effects:** `Freeze 1`

#### Suggestion (`Suggestion`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 0, max_range 20, max_aoe 0, aoe_excludes_self true, restrictions [aoe_must_exist must_have_line_of_sight], aoe_restrictions [enemies_only must_have_living_character]`
- **Damage/Effects:** `damage 0, type status_spell, CharmedForceAttack 1`

#### Supernova (`Supernova`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 10`
- **Target/Shape:** `aoe_mode all, target_mode none, aoe_excludes_self true, aoe_restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 12, Blind 3`

#### Telekinesis (`Telekinesis`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_aoe 0, max_range 20, knockback_mode character_to_target, restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 0, knockback 10`

#### Temporal Shards (`TemporalShards`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `min_range 0, max_range 20, max_aoe 0, restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 0, type status_spell, status BleedThorns, stacks 3, turns 1`

#### Think Deep (`ThinkDeep`)
- **Template:** `self_buff`
- **Cost:** `mana 5, cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `FillMana 1, Sleep 1`

#### Vacuum (`Vaccuum`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `target_mode tile, max_range 20, max_aoe 4, shuffle_tile_order true`
- **Damage/Effects:** `damage 0, DisplaceToAbilityTarget 1`

#### Withdraw (`Withdraw`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 0, max_range 20, max_aoe 0, restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 0, DisplaceTowardsSource 1`

#### Look Away (`YouSeeNothing`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `aoe_mode all, target_mode none, aoe_excludes_self true, aoe_restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 0, type status_spell, FaceAway 1`

### Passives

| Passive Name | Internal ID | Description |
| :--- | :--- | :--- |
| **Beckon** | `Beckon` | Your basic attack has +4 Knockback. |
| **Blink** | `Blink` | 33% chance to teleport to a random tile when targeted by an enemy. |
| **Drag** | `Drag` | Units that you knockback take 1 damage for each tile they pass through. |
| **Eldritch Visage** | `EldritchVisage` | At the start of your turn, inflict Magic Weakness 1 on all enemies in your line of sight. |
| **Enlightened** | `Enlightened` | While at full mana, the first spell you cast each turn is free. |
| **Flourish** | `Flourish` | Gravity element abilities do not harm allies. Gravity element abilities give a random positive status effect when used on allies. When you inflict a positive status effect, inflict +1 of that status effect. |
| **Antigravity** | `Flying` | You have Flying Movement. When you use a Gravity element ability gain +1 [img:spd]. Gravity element spells cost -1 mana. |
| **Full Power** | `FullPower` | While at full mana, your basic attack deals triple damage and has +3 Knockback. |
| **Glow** | `Glow` | Your basic attack inflicts Blind. |
| **Gravity Well** | `GravityWell` | When a unit is knocked through a tile adjacent to you, stop it and inflict Stun. |
| **Mad Visage** | `MadVisage` | All injuries you get are Disfigured. While at full mana, your basic action inflicts Madness. While you have 0 or less [img:cha] you can attack an additional time each turn. |
| **Mental Storm** | `MentalStorm` | Gain +1 Charge when you cast a spell. |
| **Mind Tempest** | `MindTempest` | After every sixth spell you cast, gain All Stats Up and +1 Magic Damage. |
| **Omniscience** | `Omniscience` | You can see EVERYTHING. Line of sight restrictions are ignored. |
| **Overflow** | `Overflow` | While at full mana, gain +2 Brace and Flying Movement. Your mana is uncapped. |
| **Power Up** | `PowerUp` | When you gain excess mana, gain +1 Magic Damage and +1 [img:int]. |
| **Psionic Repel** | `PsionicRepel` | Units that attack or contact you get knocked back 10 tiles. |
| **Psy Smack** | `PsySmack` | Knockback damage you and your allies deal is doubled. |
| **Braingeyser** | `Radiation` | When you gain excess mana, emit that many Sparkles. |
| **Reality Shatter** | `RealityShatter` | Gravity element abilities spawn Floating Glass. |
| **Repressed Memories** | `RepressedMemories` | When you spend mana, cast a random Psychic spell that costs less than the mana spent. |
| **Soul Shatter** | `SoulShatter` | When you kill a unit, deal 1 damage to all enemies. |
| **True Sight** | `TrueSight` | You and your allies can't miss enemies within your line of sight. |
| **Twiddle** | `Twiddle` | Your basic attack deals 0 damage, but you can use it 2 additional times each turn. |
| **Wither** | `Wither` | Gravity element abilities inflict a random negative status effect when used on enemies. |

---

## Class: Tank (`Tank`)

### Actives & Attacks

#### Aftershock (`Aftershock`)
- **Template:** `spell`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_restrictions [tile_must_have_element], aoe_tile_requires_element Earth`
- **Damage/Effects:** `damage 5, damage inherit, max_dist 2`

#### Anchor (`Anchor`)
- **Template:** `self_buff`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `status Brace, stacks 4, turns 1, expires_on_move true`

#### Ass Blast (`AssBlast`)
- **Template:** `melee_attack`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `aoe_mode standard, max_aoe 2, aoe_excludes_self true, knockback_mode character_to_tile`
- **Damage/Effects:** `type spell, damage 0, knockback 4, incidentally_collects_pickups false, elements [, Explosion, ]`

#### Backbreaker (`BackBreaker`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 3+bonus_melee_ability_damage, type melee, Immobile 1`

#### Barbed Wire (`BarbedWire`)
- **Template:** `lobbed_attack`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `min_range 0, max_range 5, max_aoe 0`
- **Damage/Effects:** `damage 0, status Thorns, stacks 5, turns 1, expires_on_appliers_turn true`

#### Push Attack (`BasicTankMelee`)
- **Template:** `dash_attack`
- **Cost:** `Free`
- **Target/Shape:** `max_range 1+bonus_range, max_aoe 1+bonus_melee_range, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1`

#### Batter Up (`BatterUp`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type melee, knockback 10, OverrideKnockbackDamage 3+bonus_melee_ability_damage, SoundEventOnHit Batterup_Connect`

#### Grab (`BearHug`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_aoe 2, knockback_mode tile_to_character, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 0, knockback 10`

#### Belly Flop (`BellyFlop`)
- **Template:** `jump_attack`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `max_range 3, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, aoe_excludes_self false, restrictions none`
- **Damage/Effects:** `damage 1+bonus_melee_ability_damage, IgnoreSelf 1, Immobile 1`

#### Big Rock (`BigRock`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_be_displaceable, aoe_restrictions none`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, type melee, force_no_contact true`

#### Body Guard (`BodyGuard`)
- **Template:** `self_buff`
- **Cost:** `mana 2, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `stacks 1, ability BodyGuardSwap`

#### Bowl Over (`BowlOver`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `range_mode diagcross, max_range 1, restrictions [must_be_moveable must_move], straight_shot true, allow_diagonals true`
- **Damage/Effects:** `None`

#### Chew (`Chew`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, type melee, Leech 1`

#### Chew Cud (`ChewCud`)
- **Template:** `self_buff`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 3`

#### Clap (`Clap`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `aoe_mode custom, custom_aoe [ [1, 1], [1, -1] ], range_display_include_direction true, knockback_mode perp_towards_facing`
- **Damage/Effects:** `damage 0, knockback 1`

#### Demolish (`Demolish`)
- **Template:** `melee_attack`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `knockback_mode zero`
- **Damage/Effects:** `damage 0, ChangeTile DirtTile, VaporizeInanimate 1, tag rock`

#### Goad (`DrawAttention`)
- **Template:** `spell`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 6, max_aoe 0, restrictions must_have_enemy`
- **Damage/Effects:** `damage 0, ForceMoveTowards 1`

#### Earthquake (`Earthquake`)
- **Template:** `spell`
- **Cost:** `mana 7, infcantrip true`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe 4`
- **Damage/Effects:** `damage 2, SpawnRock [1, .20], Petrify [1, .1]`

#### Eat Rock (`EatRock`)
- **Template:** `tile_targeted_melee_attack`
- **Cost:** `mana 1, infcantrip true`
- **Target/Shape:** `restrictions [must_have_tag], target_requires_tag rock`
- **Damage/Effects:** `damage 0, IgnoreSelf 1, tag rock, Vaporize 1`

#### Fault Line (`FaultLine`)
- **Template:** `spell`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `target_mode direction, aoe_mode line, min_aoe 1, max_aoe 10`
- **Damage/Effects:** `damage 2, damage inherit, max_dist 2`

#### Fissure (`Fissure`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `target_mode direction, aoe_mode custom, custom_aoe [, [1, 1], [2, 1], [3, 1], [4, 1], [5, 1], [6, 1], [7, 1], [8, 1], [9, 1], [10, 1], [1, 0], [2, 0], [3, 0], [4, 0], [5, 0], [6, 0], [7, 0], [8, 0], [9, 0], [10, 0], [1,-1], [2,-1], [3,-1], [4,-1], [5,-1], [6,-1], [7,-1], [8,-1], [9,-1], [10,-1], ], knockback_mode perp_towards_facing_middle_pull`
- **Damage/Effects:** `damage 0, knockback 1, custom_additional_ai_weight magnetize_favorlineup, Petrify [1 .1]`

#### Flip Flop (`FlipFlop`)
- **Template:** `jump_attack`
- **Cost:** `mana spd, move_points 0, act_points 0, charge "1-clamp(spd,0,1)", initial_charge 1`
- **Target/Shape:** `max_range 3, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, aoe_excludes_self false, restrictions none`
- **Damage/Effects:** `damage 3+bonus_melee_ability_damage, IgnoreSelf 1`

#### Full Force (`FullForce`)
- **Template:** `jump_attack`
- **Cost:** `mana 8, infcantrip true`
- **Target/Shape:** `max_range 1, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, aoe_excludes_self false, restrictions none`
- **Damage/Effects:** `damage con, Stun 1, OverrideDamage 0`

#### Gang Up (`GangUp`)
- **Template:** `throw_attack`
- **Cost:** `mana 9, infcantrip true`
- **Target/Shape:** `max_range 3`
- **Damage/Effects:** `damage 0, MassAttackThis 1`

#### Gore (`Gore`)
- **Template:** `dash_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_range 3`
- **Damage/Effects:** `damage 2+bonus_melee_ability_damage, makes_contact true, DisplaceToOriginalPosition 1, Bruise 1`

#### Headbutt (`HeadButt`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1, Stun 1`

#### Intimidate (`Intimidate`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type status_spell, makes_contact false, incidentally_collects_pickups false, Fear 1`

#### Iron Head (`IronHead`)
- **Template:** `dash_attack`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `max_range 3, min_range 1, target_mode tile, range_mode cross, aoe_mode standard, min_aoe 1, max_aoe 1, knockback_mode character_to_tile, aoe_considers_character_size true, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, knockback 1`

#### Lunge (`Lunge`)
- **Template:** `dash_attack`
- **Cost:** `mana 0, act_points 0, move_points 1, charge 0`
- **Target/Shape:** `max_range 1+bonus_range, max_aoe 1, aoe_restrictions must_have_line_of_sight_unpurgable`
- **Damage/Effects:** `damage 5+bonus_melee_damage, knockback 1`

#### Gorgon Glare (`Medusa`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 10`
- **Target/Shape:** `aoe_mode all, target_mode none, aoe_excludes_self true, aoe_restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 0, Petrify 1`

#### Nudge (`Nudge`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type melee, knockback 1`

#### Plant Your Feet (`PlantFeet`)
- **Template:** `self_buff`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `formula spd, SpeedUp -1, Shield 5`

#### Push Through (`PushThrough`)
- **Template:** `move`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `range_mode cross, max_range 2, restrictions [must_move must_not_be_knockback_immune_animate_character], straight_shot true`
- **Damage/Effects:** `damage 3, override_trample_damage true, VaporizeInanimate 1`

#### Rock Blast (`RockBlast`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `aoe_restrictions must_be_empty, restrictions aoe_must_exist`
- **Damage/Effects:** `damage 0, type melee, incidentally_collects_pickups false, SendRock 1`

#### Rock Crusher (`RockCrusher`)
- **Template:** `jump_attack`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `max_range 20, min_range 1, min_aoe 0, max_aoe 0, aoe_excludes_self false, restrictions [must_have_tag], target_requires_tag rock`
- **Damage/Effects:** `damage 0, override_trample_damage true, IgnoreSelf 1, tag rock, ExplodeCharacter_RockCrusher 5`

#### Rock Tomb (`RockTomb`)
- **Template:** `spell`
- **Cost:** `mana 8, infcantrip true`
- **Target/Shape:** `min_range 0, max_range 3, max_aoe 0`
- **Damage/Effects:** `damage 3, Petrify 1`

#### Rock Toss (`RockToss`)
- **Template:** `lobbed_attack`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 3+bonus_range`
- **Damage/Effects:** `damage 2+bonus_ranged_damage, Stun [1, .10], BounceObject SmallRock`

#### Sandstorm (`Sandstorm`)
- **Template:** `self_buff`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `StackingSandstorm 1`

#### Pincushion (`Spur`)
- **Template:** `self_buff`
- **Cost:** `mana 0, act_points 0, move_points 1, charge 0`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Thorns 3`

#### Steelskin (`SteelSkin`)
- **Template:** `self_buff`
- **Cost:** `mana 0, requires_reload true, start_reloaded true`
- **Target/Shape:** `min_range 1, max_range 4, max_aoe 0`
- **Damage/Effects:** `damage 0, status Brace, stacks 99, turns 1, expires_on_begin_turn true`

#### Stone Breath (`StoneGaze`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `target_mode direction, aoe_mode line, max_aoe 10, aoe_considers_character_size true, aoe_excludes_self true, knockback_mode character_to_tile, aoe_restrictions must_have_line_of_sight`
- **Damage/Effects:** `damage 0, Petrify 1`

#### Suplex (`Suplex`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `knockback_mode zero, aoe_considers_character_size false, target_mode tile, restrictions [aoe_must_be_displaceable must_have_character], range_mode standard, aoe_mode standard, min_range 1, max_range 1, min_aoe 0, max_aoe 0`
- **Damage/Effects:** `damage 3+bonus_melee_ability_damage, type melee, blocked_multiplier 2, makes_contact false`

#### Supper (`Supper`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 0, once_per_fight true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `heal 15, SpeedUp -2`

#### Rock Song (`TankRockSong`)
- **Template:** `spell`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode all`
- **Damage/Effects:** `type none, damage 0, tag rock, FloatingRockTrap 1`

#### Swap (`TankSwap`)
- **Template:** `swap`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `max_range 20, restrictions [must_be_swappable aoe_must_exist], aoe_restrictions [allies_only]`
- **Damage/Effects:** `None`

#### Tantrum (`TankTantrum`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `target_mode none, aoe_mode cross, knockback_mode character_to_tile`
- **Damage/Effects:** `damage 1+bonus_melee_ability_damage, elements [, Earth, ]`

#### Trample Dash (`TankTrample`)
- **Template:** `trample_dash`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 3`

#### Thicken (`Thicken`)
- **Template:** `self_buff`
- **Cost:** `mana 2, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TempBonusKnockback 1, TempBonusKnockbackDamage 1`

#### Throw Scrap (`ThrowShield`)
- **Template:** `lobbed_attack`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `min_range 1, max_range 2+level`
- **Damage/Effects:** `damage 0, Shield 3, ObjectOnHitFullyEmpty RandomArmorPickup`

#### To the Rescue! (`ToTheRescue`)
- **Template:** `jump_attack`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `max_range 20, min_aoe 0, max_aoe 0, aoe_excludes_self false, restrictions [must_be_adjacent_to_ally]`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, IgnoreSelf 1`

#### Toss (`Toss`)
- **Template:** `throw_attack`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `max_range 3+2*level`
- **Damage/Effects:** `damage 1, blocked_damage 5+bonus_melee_ability_damage`

### Passives

| Passive Name | Internal ID | Description |
| :--- | :--- | :--- |
| **Bouncer** | `Bouncer` | When an ally takes damage, move 3 tiles toward the source of the damage and attack it if you can. |
| **Cat-A-Pult** | `CatAPult` | You can throw adjacent allies up to 4 tiles on their turns without using their movement action. |
| **Chain Knockback** | `ChainKnockback` | Your basic attack gains +1 Knockback. Units you knockback will Knockback other units. |
| **Follow Up** | `FollowUp` | After you use your basic attack, dash forward as far as you can. |
| **Hard Head** | `HardHead` | You block attacks from the front. |
| **Hardy** | `Hardy` | Heal to full HP at the start of each battle. |
| **Heavy Handed** | `HeavyHanded` | +2 Knockback Damage. |
| **Home Run** | `HomeRun` | Knockback you deal is increased by 10. |
| **Mountain Form** | `MountainForm` | Knockback immunity. Tiles you walk over become dirt and may spawn rocks. |
| **My Leg!** | `MyLeg` | All injuries you get are Broken Legs. If you have four broken legs, gain +4 Thorns, Trample, and adjacent allies have Toss as a bonus ability. |
| **Pet Rocks** | `PetRocks` | Rocks you spawn are alive!! ...and have +3 HP. Spawn a rock at the start of the battle. |
| **Plow** | `Plow` | When you knock back a unit, leave a rock where that unit was. |
| **Priority Target** | `PriorityTarget` | Enemies will attack you instead of your allies if they can. |
| **Protective** | `ProtectiveAura` | Your allies have Brace 1. |
| **Rock Aspect** | `RockAspect` | Units that attack or contact you have a 10% chance to get Petrified. |
| **Scabs** | `Scabs` | Gain +2 Shield when you take damage from an ability. |
| **Shoving Match** | `ShovingMatch` | When you knock a unit into an ally, or knock an ally into an enemy, that ally uses their basic attack on the other unit. Your basic attack has +1 Knockback. |
| **Slack Off** | `SlackOff` | If you end your turn with unused movement actions, gain 8 HP. |
| **Slow and Steady** | `SlowAndSteady` | Gain -2 [img:spd] and +1 Range at the end of each turn. If your [img:spd] is 0, you can attack an extra time each turn. |
| **Stoic** | `Stoic` | If you end your turn with unused movement actions, gain +2 Bonus Moves. |
| **Thorns** | `Thorns` | Thorns 2. |
| **Thunder Thighs** | `ThunderThighs` | Trample. |
| **Toad Style** | `ToadStyle` | Your movement action is a jump. Landing on a unit deals damage and displaces it. |
| **Wide Load** | `WideLoad` | When an adjacent ally is targeted by an enemy, swap places with the ally. |
| **Wrestlemaniac** | `Wrestlemaniac` | Your basic attack becomes Suplex when adjacent to enemies. You gain the ability Toss. |

---

## Class: Thief (`Thief`)

### Actives & Attacks

#### Assassinate (`Assassinate`)
- **Template:** `melee_spell`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `restrictions [aoe_must_exist], aoe_restrictions [must_backstab]`
- **Damage/Effects:** `type melee, damage 10+bonus_melee_ability_damage, crit_chance 50%, piercing true, incidentally_collects_pickups true`

#### Rearm (`AttackAgain`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `Default`
- **Damage/Effects:** `RefreshActPoints 1`

#### Backflip (`Backflip`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `stacks 1, ability BackflipDodge`

#### BasicStraightShot_Thief (`BasicStraightShot_Thief`)
- **Template:** `*(None)*`
- **Cost:** `Free`
- **Target/Shape:** `Default`
- **Damage/Effects:** `None`

#### Blur (`Blur`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4, cant_cast X-65`
- **Target/Shape:** `X_is custom`
- **Damage/Effects:** `DodgeChance_Status 10`

#### Boost Backstab (`BoostBackstab`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TempBackstab 75, TempBackstabPiercing 1`

#### Caltrops (`Caltrops`)
- **Template:** `move`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_range 4`
- **Damage/Effects:** `None`

#### Chakram (`Chakram`)
- **Template:** `straightshot_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_aoe 3+bonus_range, upgrade_straight_shot_to_piercing true, upgrade_straight_shot_to_boomerang true`
- **Damage/Effects:** `damage 1+bonus_ranged_damage, CollectsPickups 1`

#### Cheat (`Cheat`)
- **Template:** `self_buff`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, status LuckUp, stacks 5, turns 1, expires_on_begin_turn true`

#### Coin Toss (`CoinToss`)
- **Template:** `straightshot_attack`
- **Cost:** `requires_reload true, mana X, coins 1`
- **Target/Shape:** `max_aoe 5, X_is this_ability_storm_count`
- **Damage/Effects:** `damage 10+bonus_ranged_damage, CoinTossBounce X`

#### Cut Purse (`CutPurse`)
- **Template:** `straightshot_attack`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_aoe 3+bonus_range`
- **Damage/Effects:** `damage 1+bonus_ranged_damage, piercing true, KnockOutCoin 1`

#### Declaw (`Declaw`)
- **Template:** `melee_attack`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1+bonus_melee_ability_damage, Bleed 1, DamageUp -1`

#### Distract (`Distract`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `max_aoe 0, max_range 4, min_range 1, knockback_mode character_to_tile_4snap`
- **Damage/Effects:** `damage 0, FaceAway 1`

#### Eagle Eye (`EagleEye`)
- **Template:** `spawn`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `target_mode none, aoe_mode square, max_aoe 20, min_targets 2, max_targets 3, aoe_restrictions [must_be_empty]`
- **Damage/Effects:** `None`

#### Fade (`Fade`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 10`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Stealth 1`

#### Greedstep (`GreedStep`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_range 20, restrictions [must_be_moveable must_have_tag], target_requires_tag money`
- **Damage/Effects:** `None`

#### Jitter (`Jitter`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `target_mode none, aoe_mode standard, min_aoe 1, max_aoe 1, aoe_considers_character_size true, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, Confusion 1`

#### Loot Corpse (`LootCorpse`)
- **Template:** `melee_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `aoe_restrictions must_have_corpse, restrictions aoe_must_exist`
- **Damage/Effects:** `damage 0, type melee, incidentally_collects_pickups false, VaporizeCorpseFlipAdvantage [1 .33], min 1, max 3`

#### Lucky Penny (`LuckyPenny`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 1`
- **Target/Shape:** `max_range 1, restrictions must_have_tag, target_requires_tag pickup`
- **Damage/Effects:** `damage 0, type status_spell, LuckUp 2`

#### Move Again (`MoveAgain`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `RefreshMovePoints 1`

#### Nail Flurry (`NailFlurry`)
- **Template:** `straightshot_attack`
- **Cost:** `infcantrip true, mana 10`
- **Target/Shape:** `max_aoe 10`
- **Damage/Effects:** `damage 1, piercing true`

#### Nightshade (`Nightshade`)
- **Template:** `melee_spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, type melee, Poison 4`

#### Outskirts (`Outskirts`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `range_mode map_edges`
- **Damage/Effects:** `None`

#### Pickpocket (`PickPocket`)
- **Template:** `melee_attack`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 0, BurgleCoin 1, BurgleCoin [1 .5], BurgleCoin [1 .5], DamageUp -1`

#### Pierce (`Pierce`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TempPenetrate 1, TempRangeUp 2`

#### Pierce Shot (`PierceShot`)
- **Template:** `straightshot_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_aoe 3+bonus_range, upgrade_straight_shot_to_piercing true`
- **Damage/Effects:** `damage 3+bonus_ranged_damage, piercing true`

#### Pocket Sand (`PocketSand`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `target_mode direction, aoe_mode cone, min_aoe 1, max_aoe 2, aoe_considers_character_size true, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, type status_spell, elements [, Wind, ], Blind 1`

#### Poison Dip (`PoisonDip`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana X, cant_cast 5-X, X_cant_be_zero true, disallow_cost_modification true, once_per_fight true`
- **Target/Shape:** `X_is current_mana`
- **Damage/Effects:** `damage 0, PoisonLace "X/5"`

#### Poison Gas (`PoisonGas`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `target_mode none, aoe_mode standard, min_aoe 1, max_aoe 1, aoe_considers_character_size true, aoe_excludes_self true`
- **Damage/Effects:** `damage 0, Poison 2`

#### Poison Nail (`PoisonNail`)
- **Template:** `straightshot_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_aoe 3+bonus_range`
- **Damage/Effects:** `damage 1+bonus_ranged_damage, piercing true, Poison 1`

#### Quick Roll (`QuickRoll`)
- **Template:** `move`
- **Cost:** `requires_reload true, mana 0`
- **Target/Shape:** `range_mode cross, max_range 3, restrictions [must_be_moveable must_move], straight_shot true`
- **Damage/Effects:** `None`

#### Rebound (`Rebound`)
- **Template:** `melee_attack`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `restrictions [aoe_must_exist], aoe_restrictions [must_have_character], knockback_mode orientation`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage`

#### Sever Artery (`SeverArtery`)
- **Template:** `melee_attack`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1+bonus_melee_ability_damage, Bleed 5`

#### Shadow (`Shadow`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_range 4, restrictions [must_be_moveable must_be_directly_behind_character]`
- **Damage/Effects:** `None`

#### Shadow Shift (`Shadowshift`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_range 2, min_range 2`
- **Damage/Effects:** `None`

#### Sharp Nail (`SharpNail`)
- **Template:** `straightshot_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_aoe 3+bonus_range`
- **Damage/Effects:** `damage 1+bonus_ranged_damage, piercing true, Bleed 1`

#### Sharpen Nail (`SharpenNail`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `DexterityUp 1, RangeUp 1`

#### Skin Disguise (`SkinDisguise`)
- **Template:** `targeted_status`
- **Cost:** `cantrip true, mana 3`
- **Target/Shape:** `aoe_restrictions [must_have_destructible_corpse enemies_only], restrictions aoe_must_exist, max_range 1, min_range 1`
- **Damage/Effects:** `damage 0, type melee, incidentally_collects_pickups false, FactionDisguiseSource 1, VaporizeCorpse 1`

#### Slice (`Slice`)
- **Template:** `melee_attack`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 5+bonus_melee_ability_damage, piercing true`

#### Slingshade (`SlingShade`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 3, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Sneak Up (`SneakUp`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `target_mode random_tile, max_range 20, restrictions [must_be_moveable must_be_directly_behind_enemy]`
- **Damage/Effects:** `None`

#### Stalk (`Stalk`)
- **Template:** `teleport`
- **Cost:** `cantrip true, mana 3`
- **Target/Shape:** `max_range 20, track_target true, delayed_trigger true, adjust_target stalk, restrictions [must_have_enemy]`
- **Damage/Effects:** `None`

#### Steal Kidney (`StealKidney`)
- **Template:** `melee_attack`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1+bonus_melee_ability_damage, crit_chance 20%, EquipPermanentItem Kidney`

#### Steal Luck (`StealLuck`)
- **Template:** `melee_attack`
- **Cost:** `mana 3, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1+bonus_melee_ability_damage, LuckUp -1, LuckUp 1`

#### Steal Time (`StealTime`)
- **Template:** `melee_attack`
- **Cost:** `mana 4, infcantrip true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `damage 1+bonus_melee_ability_damage, RefreshActPoints 1, RefreshMovePoints 1`

#### Over Here, Over There (`ThiefSwap`)
- **Template:** `swap`
- **Cost:** `mana 0, cantrip true`
- **Target/Shape:** `max_range 20, restrictions [must_be_swappable aoe_must_exist], aoe_restrictions [allies_only]`
- **Damage/Effects:** `SourceSwapsBackEndOfTurn ThiefSwapBack`

#### Time Walk (`TimeWalk`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 10, main_turn_only true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TakeExtraTurnEndOfRound 1`

#### Triple Nails (`TripleNails`)
- **Template:** `straightshot_attack`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_range 10, aoe_mode custom, custom_aoe [[1, 1] [1, 0] [1,-1]]`
- **Damage/Effects:** `damage 1+bonus_ranged_damage, piercing true`

#### Venom Barrage (`VenomBarrage`)
- **Template:** `ranged_attack`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `target_mode none, max_aoe 20, aoe_restrictions [must_have_line_of_sight enemies_only]`
- **Damage/Effects:** `damage 1+bonus_ranged_damage, piercing true, Poison 1`

#### Weakening Nail (`WeakeningNail`)
- **Template:** `straightshot_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_aoe 3+bonus_range`
- **Damage/Effects:** `damage 1+bonus_ranged_damage, piercing true, Weakness 1`

#### Wind Up (`WindUp`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 1`
- **Target/Shape:** `Default`
- **Damage/Effects:** `TempRangeUp 1`

### Passives

| Passive Name | Internal ID | Description |
| :--- | :--- | :--- |
| **After Image** | `AfterImage` | When you move, spawn a shadow where you moved from. The shadow mimics your basic action but fades away at the end of your turn. |
| **Agile** | `Agile` | +2 Movement Range. If you move fewer tiles than your full movement range, you can move a 2nd time for the rest of your movement range. |
| **First Strike** | `AlphaStrike` | Gain an extra turn at the start of the battle. |
| **Backstabber** | `Backstabber` | Your backstabs are always critical. |
| **Bounty Hunter** | `BountyHunter` | During your turn, one random enemy has a Bounty. |
| **Burgle** | `Burgle` | Your basic attack gains you 1 coin when it deals damage. |
| **Cripple** | `Cripple` | Your critical hits inflict Immobilize and Weakness 2. |
| **Critical** | `Critical` | Your critical hits deal +100% more damage. Gain +1 [img:lck] whenever you make a critical hit. |
| **Double Throw** | `DoubleThrow` | Your basic attack hits twice for half damage. |
| **Flip a Coin** | `FlipACoin` | When you gain a coin, you have a 50% chance to spawn a coin on a random tile and a 50% chance to gain +2 [img:spd] and +2 [img:lck]. |
| **Golden Claws** | `GoldenClaws` | Gain +1 Damage for each coin you collect. |
| **Loot Hoarder** | `LootHoarder` | Automatically collect all pickups at the end of the battle if you're not downed. |
| **Swift Looter** | `Looter` | When you collect a coin pickup, refresh your movement action. 1-2 extra coins spawn in each battle. |
| **Penetrate** | `Penetrate` | Your basic attack passes through units and ignores shield. +1 Range. |
| **Pinpoint** | `Pinpoint` | Your critical hits inflict Marked. |
| **Poison Tips** | `PoisonTips` | Your basic attack inflicts Poison 1. |
| **Razor Claws** | `RazorClaws` | Your basic attack inflicts Bleed 1. |
| **Stealthed** | `Shadow` | Start each battle with Stealth. |
| **Shake Down** | `ShakeDown` | Your critical hits spawn a coin and a random pickup. |
| **Shank** | `Shank` | When behind and adjacent to an enemy, your basic attack is a melee attack that hits twice. |
| **Shiv** | `Shiv` | Your basic attack has +2 damage, +25% critical chance, and inflicts Bleed 1 when attacking a unit in melee range. |
| **Sweetspot** | `SweetSpot` | +1 Range. Your basic attack deals more damage the farther away you are from the target. |
| **More!** | `SwiftKiller` | When you kill a unit, refresh your movement action. |
| **Weak Spot** | `WeakSpot` | Your basic attack ignores shield and inflicts Weakness 1. |
| **ZIP!** | `Zip` | Your movement action is Shadowstep. |

---

## Class: Tinkerer (`Tinkerer`)

### Actives & Attacks

#### Armor Up (`ArmorUp`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `pool tinkerer_default, slot random_empty_armor`

#### Autopilot (`AutoPilot`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 10`
- **Target/Shape:** `Default`
- **Damage/Effects:** `include_spells true`

#### Split the Atom (`BatteryNuke`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 50, can_pay_over_multiple_turns true, disallow_cost_modification true`
- **Target/Shape:** `target_mode none, aoe_mode all, aoe_considers_character_size false, knockback_mode zero, aoe_restrictions exclude_allies`
- **Damage/Effects:** `damage 50, Burn 10`

#### Bombchu (`Bombchu`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Build Nuke (`BuildNuke`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Build Turret (`BuildTurret`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Catbot (`Catbot`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Craft (`Craft`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `restrictions aoe_must_exist, aoe_restrictions must_have_cat_with_empty_weapon_slot`
- **Damage/Effects:** `damage 0, pool tinkerer_default, slot weapon`

#### Discharge (`Discharge`)
- **Template:** `spell`
- **Cost:** `mana X, infcantrip true, X_cant_be_zero true, disallow_cost_modification true`
- **Target/Shape:** `max_aoe 0, max_range 1, min_range 1, X_is current_mana`
- **Damage/Effects:** `damage X, elements [, Electric, ]`

#### Drill Down (`DrillDown`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `range_mode cross, max_range 10`
- **Damage/Effects:** `None`

#### Eject Button (`EjectButton`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ExplosionIfHitSomething 5, stacks 20, min_dist 4`

#### Electric Nail (`ElectricNail`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `min_range 1, max_range 4, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Electrolyze (`Electrolyze`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `CurrentWeaponDamageUp 3, CurrentWeaponAddElectricElement 1`

#### Eureka! (`Eureka`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5, once_per_fight true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Tech 3, stacks 1, tickdown_this_turn true`

#### Experimental Teleporter (`ExperimentalTeleporter`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_range 20`
- **Damage/Effects:** `None`

#### Fabricate (`Fabricate`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_range 3, min_range 1, restrictions aoe_must_exist, aoe_restrictions must_have_cat_with_empty_weapon_slot`
- **Damage/Effects:** `damage 0, type status_spell, CloneWeaponTemp 1`

#### Fast Hands (`FastHands`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `Default`
- **Damage/Effects:** `RefreshNonManaItemAbilities 1`

#### Firecracker (`Firecrackers`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `max_aoe 2, min_range 1, max_range 5+bonus_range, max_targets 3, restrictions none, can_multihit true`
- **Damage/Effects:** `damage 0, type ranged, SmallHitExplosion 1`

#### Fresh off the Forge (`FreshOffTheForge`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Shield 7, Burn 3`

#### Improve (`Improve`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 2`
- **Target/Shape:** `Default`
- **Damage/Effects:** `RandomStatUp 1`

#### Instant Barrier (`InstantBarrier`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 1, enabled_formula 1-X`
- **Target/Shape:** `X_is current_shield`
- **Damage/Effects:** `Shield 6`

#### Math! (`Math`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `max_aoe 0, max_range 5`
- **Damage/Effects:** `raw_damage 0, show_damage_on_0 true, stacks 1, Stun 1`

#### Mech Suit (`MechSuit`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 15, once_per_fight true`
- **Target/Shape:** `range_mode custom, custom_range [[-2 0] [-2 -1] [-1 -2] [0 -2] [-1 1] [0 1] [1 0] [1 -1]], aoe_mode custom, dont_orient_aoe true, custom_aoe [[0 0] [1 0] [0 1] [1 1]], range_excludes_blocking false, restrictions must_fit_2x2_character, aoe_restrictions none, range_display_include_aoe true, mouse_offset [.5 .5]`
- **Damage/Effects:** `None`

#### Nurse Bot (`NurseBot`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 9`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Punchbot (`PunchBot`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `min_range 1, max_range 2, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Recycle (`Recycle`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5, requires_destructible_weapon true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `DestroyWeapon 1, Tech 1, RefreshActPoints 1`

#### Refine Materials (`RefineMaterials`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 1`
- **Target/Shape:** `max_range 3, restrictions must_have_tag, target_requires_tag pickup`
- **Damage/Effects:** `damage 0, type status_spell, Tech 1`

#### Remote Detonator (`RemoteDetonator`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `max_range 20, restrictions must_have_familiar`
- **Damage/Effects:** `damage 0, cant_miss true, ExplodeCharacter 5`

#### Repair (`Repair`)
- **Template:** `spell`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `max_aoe 0, max_range 1, min_range 0`
- **Damage/Effects:** `damage 0, type status_spell, cant_miss true, RepairAll 1, RepairAllCondition 1`

#### Repair Armor (`RepairArmor`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ResetArmorShield 1, RepairArmorCondition 1`

#### Reprogram (`Reprogram`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `Default`
- **Damage/Effects:** `ConjureBonusAbility Class`

#### Research (`Research`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 5`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Tech 1`

#### Robo-Vac (`RoboVac`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Rocket Ride (`RocketRide`)
- **Template:** `jump_attack`
- **Cost:** `infcantrip true, mana 6`
- **Target/Shape:** `aoe_mode standard, min_aoe 0, max_aoe 1, max_range 20, knockback_mode character_to_tile, aoe_excludes_self false`
- **Damage/Effects:** `damage 8, knockback 1, type spell, incidentally_collects_pickups false, VisualFXTile Explosion`

#### Rocket Skates (`RocketSkates`)
- **Template:** `dash_attack`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `aoe_mode standard, min_aoe 0, max_aoe 1, knockback_mode character_to_tile, aoe_excludes_self false`
- **Damage/Effects:** `damage 5, knockback 1, type spell, incidentally_collects_pickups false, VisualFXTile Explosion`

#### Shed Scrap (`ShedScrap`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 1, enabled_formula X`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, X_is current_shield, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Shock Therapy (`ShockTherapy`)
- **Template:** `spell`
- **Cost:** `mana 5, infcantrip true`
- **Target/Shape:** `max_aoe 0, max_range 1, min_range 0`
- **Damage/Effects:** `damage 1, Cleanse 0, RandomStatUp 1, Stun [1 .25]`

#### Shockwave (`Shockwave`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `aoe_mode all, target_mode none, aoe_excludes_self true`
- **Damage/Effects:** `damage 10, DamageDistanceAOEFalloff 1`

#### Shoddy Jetpack (`ShoddyJetpack`)
- **Template:** `jump_attack`
- **Cost:** `mana 6, infcantrip true`
- **Target/Shape:** `max_range 20, aoe_mode occupied_tiles, aoe_excludes_self false, restrictions none, randomize_target_within_range 3`
- **Damage/Effects:** `damage 0, type none, cant_miss true, IgnoreSelf true, ExplosionIfHitSomething 5`

#### Short Circuit (`ShortCircuit`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 3`
- **Target/Shape:** `target_mode none, aoe_mode standard, min_aoe 1, max_aoe 1, aoe_considers_character_size true, aoe_excludes_self true`
- **Damage/Effects:** `damage 1, knockback 0, min 1, max 3`

#### Smash (`Smash`)
- **Template:** `melee_attack`
- **Cost:** `requires_destructible_weapon true, infcantrip true, mana 5`
- **Target/Shape:** `min_range 1, max_range 4+bonus_range`
- **Damage/Effects:** `damage 0`

#### Spare Parts (`SpareParts`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 1, requires_destructible_weapon true`
- **Target/Shape:** `Default`
- **Damage/Effects:** `DestroyWeapon 1, Shield 2, Charge 4, Thorns 1, GainCoins 1`

#### Sparks (`Sparks`)
- **Template:** `lobbed_attack`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `target_mode none, aoe_excludes_self true, max_aoe 20, max_targets 3, aoe_restrictions [must_have_enemy_or_robot must_have_living_character]`
- **Damage/Effects:** `damage 3, type spell, VisualFXTile WaterConduct`

#### Spawn Decoy (`SpawnDecoy`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 8`
- **Target/Shape:** `min_range 1, max_range 3`
- **Damage/Effects:** `None`

#### Spring Shoes (`SpringShoes`)
- **Template:** `jump_attack`
- **Cost:** `mana 2, infcantrip true`
- **Target/Shape:** `target_mode tile, min_range 1, max_range 2, aoe_mode occupied_tiles, min_aoe 0, max_aoe 0, range_display_include_character_size true, restrictions must_be_moveable`
- **Damage/Effects:** `type none, damage 0`

#### Tesla Coil (`TeslaCoil`)
- **Template:** `spawn`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `min_range 1, max_range 1, max_aoe 0, range_excludes_blocking false, restrictions aoe_must_exist`
- **Damage/Effects:** `None`

#### Craft Weapon (`TinkererCraft`)
- **Template:** `self_buff`
- **Cost:** `Free`
- **Target/Shape:** `restrictions aoe_must_exist, aoe_restrictions must_have_cat_with_empty_weapon_slot`
- **Damage/Effects:** `damage 0, pool tinkerer_default, slot weapon`

#### Unreliable Missile Launcher (`UnreliableMissile`)
- **Template:** `spell`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `target_mode random_tile, min_range 1, max_range 20, restrictions must_have_enemy`
- **Damage/Effects:** `damage 5, knockback 1, elements [, Explosion, Fire, ]`

#### Unreliable Shield Generator (`UnreliableShield`)
- **Template:** `self_buff`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `Default`
- **Damage/Effects:** `Shield 6, status Brace, stacks 1, turns 1, expires_on_begin_turn true`

#### Upgrade (`Upgrade`)
- **Template:** `targeted_status`
- **Cost:** `infcantrip true, mana 4`
- **Target/Shape:** `min_range 0, max_range 3, max_aoe 0, restrictions aoe_must_exist, aoe_restrictions familiars_only`
- **Damage/Effects:** `damage 0, AllStatsUp 1, FullHeal 1`

#### Volt Tackle (`VoltTackle`)
- **Template:** `teleport`
- **Cost:** `infcantrip true, mana 7`
- **Target/Shape:** `max_range 20, restrictions [aoe_must_be_displaceable must_move must_be_conductive]`
- **Damage/Effects:** `damage 5, type spell, IgnoreSelf 1, VisualFXTile WaterConduct`

### Passives

| Passive Name | Internal ID | Description |
| :--- | :--- | :--- |
| **Armor Specialist** | `ArmorSpecialist` | Your equipment passive effects are doubled. |
| **Armored Plating** | `ArmoredPlating` | Robots you spawn gain the stats and [img:shield] of your equipped armor. |
| **Blacksmith** | `Blacksmith` | If you have a weapon, your basic attack becomes Hone. |
| **Booby Trap** | `BoobyTrap` | When an item you have equipped breaks, it explodes! |
| **Conductor** | `Conductor` | Electric damage you deal is increased by 2 for each piece of metal armor you have equipped. If you are wearing metal, your weapon deals electric damage. |
| **Demo Man** | `DemoMan` | Always craft a bomb at Tech 1 or less. +2 Blast Resistance. |
| **Duct Tape** | `DuctTape` | Items you craft stay with you between battles, but become cursed. |
| **EMP** | `EMP` | Your explosions are Electric element and deal +2 damage. Instead of knockback, explosions have a chance to inflict Stun. +2 Blast Resistance. |
| **Energizer** | `Energizer` | When you cast a spell, your weapon gets +1 Damage. |
| **Escape Sequence** | `EscapeSequence` | When you take damage, explode and get launched to a random tile. This explosion doesn't damage you. |
| **Fuzzy Feet** | `FuzzyFeet` | When you end your movement, deal 1 Electric Damage to all adjacent units for each tile you moved. |
| **Ingenuity** | `Ingenuity` | Pickups give you +1 Tech in addition to their other effects. |
| **Item Proxy** | `ItemProxy` | You need one fewer piece of equipment to get set bonuses. |
| **IT'S ALIVE!** | `ItsAlive` | Hitting a body with electric damage revives it with 1 HP. The revived corpse is charmed and takes an extra turn, then dies. |
| **Lightning Rod** | `LightningRod` | You have Electric immunity and are conductive. Electric damage you deal is increased by 1. Gain 1 Tech when you are hit with electric damage. |
| **Living Battery** | `LivingBattery` | When an adjacent ally spends mana, gain that much mana. |
| **Mr. Mega** | `MrMega` | Your explosions are larger and deal +3 damage. +3 Blast Resistance. |
| **Nanobots** | `Nanobots` | Gain +2 Diminishing Health Regeneration every time you take damage from an attack or spell. |
| **Napalm** | `Napalm` | Your explosions inflict Burn 3 and light tiles on fire. +2 Blast Resistance. |
| **Reactive Armor** | `ReactiveArmor` | When you take damage, craft a Tinkerer weapon or armor piece and equip it in an empty slot. |
| **Robot Arms** | `RobotArms` | You can use your weapon an additional time each turn. |
| **Scrapper** | `Scrapper` | Find an extra consumable item at the end of each battle. When you use up a consumable or trinket, equip a new consumable from your inventory if you have any. |
| **Shrapnel** | `Shrapnel_Tinkerer` | When you break an item, gain +1 Thorns. |
| **v2.0** | `VersionTwo` | Start with 1 Tech. Your Tech can't drop below 1. |
| **Weapon Proficiency** | `WeaponProficiency` | Your weapon damage scales with your stats and counts as a basic attack. |

---

