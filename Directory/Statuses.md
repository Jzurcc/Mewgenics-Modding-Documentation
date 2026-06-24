# Statuses Directory

### `Adrenaline`
**Name:** Adrenaline  
**Tooltip:** Keeps Exhaustion at 0.  
+25% Crit Chance.  
+25% Block Chance.  
**Source:** `keyword_tooltips.gon`  

```
Adrenaline {
    name "KEYWORD_ADRENALINE_NAME"
    tooltip "KEYWORD_ADRENALINE_DESC"
}
```

---

### `AllStatsUp`
**Name:** All Stats Up  
**Name Stacks Neg:** All Stats Down  
**Tooltip Stacks Pos:** All Stats increased by {stacks}  
**Tooltip Stacks Neg:** All Stats decreased by {absstacks}  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
AllStatsUp {
    name "KEYWORD_ALLSTATSUP_NAME"
    name_stacks_neg "KEYWORD_ALLSTATSDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_ALLSTATSUP_DESC"
    tooltip_stacks_neg "KEYWORD_ALLSTATSDOWN_DESC"

    tooltip_stackless none
    
    
}
```

---

### `AlphaAllStatsUp`
**Alias:** `AllStatsUp`  
**Source:** `keyword_tooltips.gon`  

```
AlphaAllStatsUp {
    alias AllStatsUp
}
```

---

### `AlphaDodgeChance`
**Alias:** `DodgeChance_Status`  
**Source:** `keyword_tooltips.gon`  

```
AlphaDodgeChance {
    alias DodgeChance_Status
}
```

---

### `AlphaCat`
**Name:** The Alpha  
**Tooltip:** This is the Alpha. Certain abilities care about this.  
**Tooltip Stackless:** No effects on its own. Only one unit can be The Alpha. Certain spells and abilities provide bonuses for The Alpha.  
**Source:** `keyword_tooltips.gon`  

```
AlphaCat {
    name "KEYWORD_ALPHA_NAME"
    tooltip "KEYWORD_ALPHA_DESC"
    tooltip_stackless "KEYWORD_ALPHA_DESC_STACKLESS"
}
```

---

### `AllyDodgeChanceAura`
**Alias:** `DodgeChance_Status`  
**Source:** `keyword_tooltips.gon`  

```
AllyDodgeChanceAura {
    alias DodgeChance_Status
}
```

---

### `LowHealthAllyDodgeChanceAura`
**Alias:** `DodgeChance_Status`  
**Source:** `keyword_tooltips.gon`  

```
LowHealthAllyDodgeChanceAura {
    alias DodgeChance_Status
}
```

---

### `AllyInfested`
**Alias:** `Infested`  
**Source:** `keyword_tooltips.gon`  

```
AllyInfested {
    alias Infested
}
```

---

### `Ammo`
**Name:** Ammo  
**Tooltip Stacks:** {stacks} shots left.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
Ammo { 
    name "KEYWORD_AMMO_NAME"
    tooltip_stacks "KEYWORD_AMMO_DESC"
    tooltip_stackless none 
}
```

---

### `Attraction`
**Name:** Attraction  
**Name Reference Applier:** Attraction  
**Tooltip Stacks:** The thing attracting you is gone. Does nothing.  
**Tooltip Reference Applier:** Moves towards {applier} at the start of its turn.  
**Tooltip Stackless:** Moves towards you at the start of its turn.  
**Source:** `keyword_tooltips.gon`  

```
Attraction {
    name "KEYWORD_ATTRACTION_NAME"
    name_reference_applier "KEYWORD_ATTRACTION_REF"
    tooltip_stacks "KEYWORD_ATTRACTION_DESC"
    tooltip_reference_applier "KEYWORD_ATTRACTION_DESC_REF"

    tooltip_stackless "KEYWORD_ATTRACTION_DESC_STACKLESS"
}
```

---

### `BackflipWhenTargeted`
**Name:** Backflip  
**Tooltip:** Backflips out of the way the next time it's targeted.  
**Source:** `keyword_tooltips.gon`  

```
BackflipWhenTargeted {
    name "KEYWORD_BACKFLIP_NAME"
    tooltip "KEYWORD_BACKFLIP_DESC"
}
```

---

### `BlastResistance`
**Name:** Blast Resistance  
**Tooltip Stacks:** Takes {stacks} less damage from explosions.  
**Tooltip Stackless:** Reduces damage taken from explosions.  
**Source:** `keyword_tooltips.gon`  

```
BlastResistance {
    name "KEYWORD_BLASTRESISTANCE_NAME"
    tooltip_stacks "KEYWORD_BLASTRESISTANCE_DESC"
    tooltip_stackless "KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"
}
```

---

### `Bleed`
**Name:** Bleed  
**Tooltip Stacks:** Takes {stacks} damage at the end of the round, then increase Bleed by 1.  
**Tooltip Stackless:** Takes damage at the end of the round, then increase Bleed by 1.  
**Source:** `keyword_tooltips.gon`  

```
Bleed {
    name "KEYWORD_BLEED_NAME"
    tooltip_stacks "KEYWORD_BLEED_DESC"
    tooltip_stackless "KEYWORD_BLEED_DESC_STACKLESS"
}
```

---

### `BleedThorns`
**Name:** Bleed Thorns  
**Tooltip Stacks:** Deals {stacks} damage and inflicts Bleed {stacks} to units that contact you.  
**Tooltip Stackless:** Deals damage and inflicts Bleed to units that contact you.  
**Source:** `keyword_tooltips.gon`  

```
BleedThorns { 
    name "KEYWORD_BLEEDTHORNS_NAME"
    tooltip_stacks "KEYWORD_BLEEDTHORNS_DESC"

    tooltip_stackless "KEYWORD_BLEEDTHORNS_DESC_STACKLESS"
}
```

---

### `BlessingOfPeace`
**Name:** Blessing of Peace  
**Tooltip:** Gain +{stacks} [img:divineshield] at the end of your turn. Lose this when you deal damage.  
**Tooltip Stackless:** Gain [img:divineshield] at the end of your turn. Lose this when you deal damage.  
**Source:** `keyword_tooltips.gon`  

```
BlessingOfPeace {
    name "KEYWORD_BLESSINGOFPEACE_NAME"
    tooltip "KEYWORD_BLESSINGOFPEACE_DESC"

    tooltip_stackless "KEYWORD_BLESSINGOFPEACE_DESC_STACKLESS"
}
```

---

### `Blind`
**Name:** Blind  
**Tooltip Stacks:** 30% miss chance for the next {stacks} turns.  
**Tooltip Stacks Singular:** 30% miss chance for the next turn.  
**Tooltip Stacks Neg:** 30% miss chance.  
**Source:** `keyword_tooltips.gon`  

```
Blind {
    name "KEYWORD_BLIND_NAME"
    tooltip_stacks "KEYWORD_BLIND_DESC"
    tooltip_stacks_singular "KEYWORD_BLIND_DESC_STACKLESS"
    tooltip_stacks_neg "KEYWORD_PERMABLIND_DESC"
}
```

---

### `Bloodzerked`
**Name:** Bloodzerked  
**Tooltip Stacks:** When you deal health damage to a bleeding unit, heal that much health.  
**Source:** `keyword_tooltips.gon`  

```
Bloodzerked {
    name "KEYWORD_BLOODZERK_NAME"
    tooltip_stacks "KEYWORD_BLOODZERK_DESC"
}
```

---

### `Blur`
**Alias:** `DodgeChance_Status`  
**Source:** `keyword_tooltips.gon`  

```
Blur {
    alias DodgeChance_Status
}
```

---

### `BodyGuard`
**Name:** Body Guard  
**Tooltip:** The next time an ally is targeted, swap places with them first.  
**Source:** `keyword_tooltips.gon`  

```
BodyGuard {
    name "KEYWORD_BODYGUARD_NAME"
    tooltip "KEYWORD_BODYGUARD_DESC"
}
```

---

### `BoostDamageAura`
**Alias:** `DamageUp`  
**Source:** `keyword_tooltips.gon`  

```
BoostDamageAura {
    alias DamageUp
}
```

---

### `BoostDamageGlobalAura`
**Alias:** `DamageUp`  
**Source:** `keyword_tooltips.gon`  

```
BoostDamageGlobalAura {
    alias DamageUp
}
```

---

### `Bounty`
**Name:** Bounty  
**Tooltip Stacks:** Takes 25% extra damage. If killed, gain {stacks} coins.  
**Tooltip Stackless:** Takes 25% extra damage. If killed, gain coins.  
**Source:** `keyword_tooltips.gon`  

```
Bounty {
    name "KEYWORD_BOUNTY_NAME"
    tooltip_stacks "KEYWORD_BOUNTY_DESC"
    tooltip_stackless "KEYWORD_BOUNTY_DESC_STACKLESS"
}
```

---

### `Brace`
**Name:** Brace  
**Tooltip Stacks:** Takes {stacks} less damage from all sources.  
**Tooltip Stackless:** Reduces all incoming damage.  
**Source:** `keyword_tooltips.gon`  

```
Brace {
    name "KEYWORD_BRACE_NAME"
    tooltip_stacks "KEYWORD_BRACE_DESC"
    tooltip_stackless "KEYWORD_BRACE_DESC_STACKLESS"
}
```

---

### `BraceForEachNeighboringEnemy`
**Alias:** `Brace`  
**Source:** `keyword_tooltips.gon`  

```
BraceForEachNeighboringEnemy {
    alias Brace
}
```

---

### `Bruise`
**Name:** Bruise  
**Tooltip Stacks:** Takes {stacks} more damage from physical sources.  
**Tooltip Stackless:** Increases all incoming physical damage.  
**Source:** `keyword_tooltips.gon`  

```
Bruise {
    name "KEYWORD_BRUISE_NAME"
    tooltip_stacks "KEYWORD_BRUISE_DESC"
    tooltip_stackless "KEYWORD_BRUISE_DESC_STACKLESS"
}
```

---

### `Burn`
**Name:** Burn  
**Tooltip Stacks:** Takes {stacks} damage at start of its turn, then decrease Burn by 1.  
**Tooltip Stackless:** Takes damage at start of its turn, then decrease Burn by 1.  
**Source:** `keyword_tooltips.gon`  

```
Burn {
    name "KEYWORD_BURN_NAME"
    tooltip_stacks "KEYWORD_BURN_DESC"
    tooltip_stackless "KEYWORD_BURN_DESC_STACKLESS"
}
```

---

### `ChampionUpgradeNextMinion`
**Name:** Promote  
**Tooltip:** The next familiar you spawn is upgraded into a [img:champion] Champion.  
**Source:** `keyword_tooltips.gon`  

```
ChampionUpgradeNextMinion {
    name "KEYWORD_PROMOTE_NAME"
    tooltip "KEYWORD_PROMOTE_DESC"
}
```

---

### `EliteUpgradeNextMinion`
**Name:** Promote+  
**Tooltip:** The next familiar you spawn is upgraded into an [img:elite] Elite.  
**Source:** `keyword_tooltips.gon`  

```
EliteUpgradeNextMinion {
    name "KEYWORD_PROMOTE2_NAME"
    tooltip "KEYWORD_PROMOTE2_DESC"
}
```

---

### `Charge`
**Name:** Charge  
**Tooltip Stacks:** Gains {stacks} mana at the start of its next turn.  
**Tooltip Stackless:** Gains mana at the start of its next turn.  
**Source:** `keyword_tooltips.gon`  

```
Charge {
    name "KEYWORD_CHARGE_NAME"
    tooltip_stacks "KEYWORD_CHARGE_DESC"
    tooltip_stackless "KEYWORD_CHARGE_DESC_STACKLESS"
}
```

---

### `ChargeFists`
**Name:** Charge Fists  
**Tooltip Stacks:** Your basic attack emits {stacks} Sparkles until the end of the turn.  
**Tooltip Stacks Singular:** Your basic attack emits a Sparkle until the end of the turn.  
**Tooltip Stackless:** Your basic attack emits Sparkles until the end of the turn.  
**Source:** `keyword_tooltips.gon`  

```
ChargeFists {
    name "KEYWORD_CHARGEFISTS_NAME"
    tooltip_stacks "KEYWORD_CHARGEFISTS_DESC"
    tooltip_stacks_singular "KEYWORD_CHARGEFISTS_DESC_SINGULAR"
    tooltip_stackless "KEYWORD_CHARGEFISTS_DESC_STACKLESS"
}
```

---

### `CharismaUp`
**Name:** Charisma Up  
**Name Stacks Neg:** Charisma Down  
**Tooltip Stacks Pos:** Charisma increased by {stacks}.  
Charisma affects max mana and initial mana.  
**Tooltip Stacks Neg:** Charisma decreased by {absstacks}.  
Charisma affects max mana and initial mana.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
CharismaUp {
    name "KEYWORD_CHAUP_NAME"
    name_stacks_neg "KEYWORD_CHADOWN_NAME"
    tooltip_stacks_pos "KEYWORD_CHAUP_DESC"
    tooltip_stacks_neg "KEYWORD_CHADOWN_DESC"

    tooltip_stackless none 
}
```

---

### `CharmAllFlies`
**Alias:** `Charmed`  
**Source:** `keyword_tooltips.gon`  

```
CharmAllFlies {
    alias Charmed
}
```

---

### `Charmed`
**Name:** Charmed  
**Tooltip:** It's brainwashed!  
**Tooltip Stackless:** Behaves as if it's on your team.  
**Source:** `keyword_tooltips.gon`  

```
Charmed { 
    name "KEYWORD_CHARMED_NAME"
    tooltip "KEYWORD_CHARMED_DESC"

    tooltip_stackless "KEYWORD_CHARMED_DESC_STACKLESS"
}
```

---

### `Cleave`
**Name:** Cleave  
**Tooltip:** Cuts a chunk of meat off what it hits.  
**Icon Frame:** `152`  
**Source:** `keyword_tooltips.gon`  

```
Cleave {
    name "KEYWORD_CLEAVE_NAME"
    tooltip "KEYWORD_CLEAVE_DESC"

    icon_frame 152
}
```

---

### `ProbeCharmed`
**Name:** Probed  
**Tooltip:** It's being controlled! Attack it to break the probe!  
**Tooltip Stackless:** Behaves as if it's on your team. Attacks from allies will break the probe.  
**Source:** `keyword_tooltips.gon`  

```
ProbeCharmed { 
    name "KEYWORD_PROBED_NAME"
    tooltip "KEYWORD_PROBED_DESC" 

    tooltip_stackless "KEYWORD_PROBED_DESC_STACKLESS"
}
```

---

### `Confusion`
**Name:** Confusion  
**Tooltip Stacks:** When performing an action, 33% chance to instead hit itself equal to its strength. Lasts {stacks} turns.  
**Tooltip Stackless:** When performing an action, 33% chance to instead hit itself equal to its strength.  
**Source:** `keyword_tooltips.gon`  

```
Confusion {
    name "KEYWORD_CONFUSION_NAME"
    tooltip_stacks "KEYWORD_CONFUSION_DESC"

    tooltip_stackless "KEYWORD_CONFUSION_DESC_STACKLESS"
}
```

---

### `PermanentConfusion`
**Name:** Confusion  
**Tooltip Stacks:** When performing an action, 33% chance to instead hit itself equal to its strength.  
**Tooltip Stackless:** When performing an action, 33% chance to instead hit itself equal to its strength.  
**Source:** `keyword_tooltips.gon`  

```
PermanentConfusion {
    name "KEYWORD_CONFUSION_NAME"
    tooltip_stacks "KEYWORD_CONFUSION_DESC_STACKLESS"

    tooltip_stackless "KEYWORD_CONFUSION_DESC_STACKLESS"
}
```

---

### `ConstitutionUp`
**Name:** Constitution Up  
**Name Stacks Neg:** Constitution Down  
**Tooltip Stacks Pos:** Constitution increased by {stacks}.  
Constitution affects max health and post-battle health regen.  
**Tooltip Stacks Neg:** Constitution decreased by {absstacks}.  
Constitution affects max health and post-battle health regen.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
ConstitutionUp {
    name "KEYWORD_CONUP_NAME"
    name_stacks_neg "KEYWORD_CONDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_CONUP_DESC"
    tooltip_stacks_neg "KEYWORD_CONDOWN_DESC"

    tooltip_stackless none 
}
```

---

### `CounterNextAttacks`
**Name:** Counter Attack  
**Tooltip Stacks Singular:** Attack the next thing that damages you automatically.  
**Tooltip Stacks:** Attack the next {stacks} things that damage you automatically.  
**Source:** `keyword_tooltips.gon`  

```
CounterNextAttacks {
    name "KEYWORD_COUNTER_NAME"
    tooltip_stacks_singular "KEYWORD_COUNTER_DESC"
    tooltip_stacks "KEYWORD_COUNTER_DESC_STACKS"
}
```

---

### `CritChanceUp`
**Name:** Crit Chance Up  
**Tooltip Stacks:** Crit Chance increased by {stacks}%  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
CritChanceUp {
    name "KEYWORD_CRITCHANCE_NAME"
    tooltip_stacks "KEYWORD_CRITCHANCE_DESC"

    tooltip_stackless none 
}
```

---

### `DamageReductionAura`
**Alias:** `Brace`  
**Source:** `keyword_tooltips.gon`  

```
DamageReductionAura {
    alias Brace
}
```

---

### `DamageUp`
**Name:** Damage Up  
**Name Stacks Neg:** Damage Down  
**Tooltip Stacks Pos:** Basic attack damage increased by {stacks}.  
**Tooltip Stacks Neg:** Basic attack damage decreased by {absstacks}.  
**Tooltip Stackless Pos:** Increases the damage (or heal) of its basic attack.  
**Tooltip Stackless Neg:** Decreases the damage (or heal) of its basic attack.  
**Source:** `keyword_tooltips.gon`  

```
DamageUp {
    name "KEYWORD_DAMAGEUP_NAME"
    name_stacks_neg "KEYWORD_DAMAGEDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_DAMAGEUP_DESC"
    tooltip_stacks_neg "KEYWORD_DAMAGEDOWN_DESC"

    tooltip_stackless_pos "KEYWORD_DAMAGEUP_DESC_STACKLESS"
    tooltip_stackless_neg "KEYWORD_DAMAGEDOWN_DESC_STACKLESS"
}
```

---

### `DelayedStatusApplication`
**Name:** `KEYWORD_DELAYEDSTATUS_NAME`  
**Tooltip:** `KEYWORD_DELAYEDSTATUS_DESC`  
**Source:** `keyword_tooltips.gon`  

```
DelayedStatusApplication {
    name "KEYWORD_DELAYEDSTATUS_NAME"
    tooltip "KEYWORD_DELAYEDSTATUS_DESC"
}
```

---

### `DelayedPain`
**Name:** Delayed Pain  
**Tooltip Stacks:** Takes {stacks} damage at the end of its turn.  
**Tooltip Stackless:** Delayed damage is taken all at once at the end of your turn.  
**Source:** `keyword_tooltips.gon`  

```
DelayedPain {
    name "KEYWORD_DELAYEDPAIN_NAME"
    tooltip_stacks "KEYWORD_DELAYEDPAIN_DESC"

    tooltip_stackless "KEYWORD_DELAYEDPAIN_DESC_STACKLESS"
}
```

---

### `DexterityUp`
**Name:** Dexterity Up  
**Name Stacks Neg:** Dexterity Down  
**Tooltip Stacks Pos:** Dexterity increased by {stacks}.  
Dexterity affects ranged attack and ranged ability damage.  
**Tooltip Stacks Neg:** Dexterity decreased by {absstacks}.  
Dexterity affects ranged attack and ranged ability damage.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
DexterityUp {
    name "KEYWORD_DEXUP_NAME"
    name_stacks_neg "KEYWORD_DEXDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_DEXUP_DESC"
    tooltip_stacks_neg "KEYWORD_DEXDOWN_DESC"

    tooltip_stackless none 
}
```

---

### `DiminishingHealthRegen`
**Name:** Health Regen (Diminishing)  
**Tooltip Stacks:** Regen {stacks} health at the end of its turn, then decreases Health Regen by 1.  
**Tooltip Stackless:** Regen health at the end of its turn, then decreases Health Regen by 1.  
**Source:** `keyword_tooltips.gon`  

```
DiminishingHealthRegen {
    name "KEYWORD_DIMINISHREGEN_NAME"
    tooltip_stacks "KEYWORD_DIMINISHREGEN_DESC"

    tooltip_stackless "KEYWORD_DIMINISHREGEN_DESC_STACKLESS"
}
```

---

### `DivineShield`
**Name:** Holy Shield  
**Tooltip:** Blocks an entire instance of incoming damage.  
**Icon Frame:** `141`  
**Source:** `keyword_tooltips.gon`  

```
DivineShield {
    name "KEYWORD_DIVINESHIELD_NAME"
    tooltip "KEYWORD_DIVINESHIELD_DESC"

    icon_frame 141
}
```

---

### `divine_shield`
**Alias:** `DivineShield`  
**Source:** `keyword_tooltips.gon`  

```
divine_shield {
    alias DivineShield
}
```

---

### `NonStackingDivineShield`
**Alias:** `DivineShield`  
**Source:** `keyword_tooltips.gon`  

```
NonStackingDivineShield {
    alias DivineShield
}
```

---

### `Dodge`
**Name:** Dodge  
**Tooltip Stacks:** Dodges the next {stacks} attacks.  
**Tooltip Stackless:** Dodges the next attack.  
**Source:** `keyword_tooltips.gon`  

```
Dodge { 
    name "KEYWORD_DODGE_NAME"
    tooltip_stacks "KEYWORD_DODGE_DESC"

    tooltip_stackless "KEYWORD_DODGE_DESC_STACKLESS"
}
```

---

### `DodgeChance_Status`
**Name:** Dodge Chance  
**Tooltip Stacks:** Dodge Chance increased by {stacks}%.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
DodgeChance_Status {
    name "KEYWORD_DODGECHANCE_NAME"
    tooltip_stacks "KEYWORD_DODGECHANCE_DESC"

    tooltip_stackless none 
}
```

---

### `Doomed`
**Name:** Doomed  
**Tooltip:** Ticks down at the end of your turn. When it hits 0, Die.  
**Source:** `keyword_tooltips.gon`  

```
Doomed {
    name "KEYWORD_DOOMED_NAME"
    tooltip "KEYWORD_DOOMED_DESC" 
}
```

---

### `DoubleCast`
**Name:** Double Action  
**Tooltip:** The next ability you use is used an additional time for free.  
**Source:** `keyword_tooltips.gon`  

```
DoubleCast { 
    name "KEYWORD_DOUBLECAST_NAME"
    tooltip "KEYWORD_DOUBLECAST_DESC"
}
```

---

### `DoubleCastSpell`
**Name:** Double Cast  
**Tooltip:** The next spell you cast is cast an additional time for free.  
**Source:** `keyword_tooltips.gon`  

```
DoubleCastSpell {
    name "KEYWORD_DOUBLECASTSPELL_NAME"
    tooltip "KEYWORD_DOUBLECASTSPELL_DESC"
}
```

---

### `DoubleCastSpellThisTurn`
**Name:** Double Cast (This Turn)  
**Tooltip:** The next spell you cast this turn is cast an additional time for free.  
**Source:** `keyword_tooltips.gon`  

```
DoubleCastSpellThisTurn {
    name "KEYWORD_DOUBLECASTTHISTURN_NAME"
    tooltip "KEYWORD_DOUBLECASTTHISTURN_DESC"
}
```

---

### `DoubleLoot`
**Name:** `Double Loot`  
**Tooltip:** `The next pickup you collect does double its effects`  
**Source:** `keyword_tooltips.gon`  

```
DoubleLoot { 
    name "Double Loot"
    tooltip "The next pickup you collect does double its effects"
}
```

---

### `Drowsy`
**Name:** Drowsy  
**Tooltip:** Falls asleep at the end of its turn.  
**Source:** `keyword_tooltips.gon`  

```
Drowsy {
    name "KEYWORD_DROWSY_NAME"
    tooltip "KEYWORD_DROWSY_DESC"
}
```

---

### `DybbukPossessed`
**Name:** Possessed by Dybbuk  
**Tooltip:** This cat is possessed by Dybbuk. Down this cat to exorcise him.  
**Source:** `keyword_tooltips.gon`  

```
DybbukPossessed {
    name "KEYWORD_DYBBUKED_NAME"
    tooltip "KEYWORD_DYBBUKED_DESC"
}
```

---

### `EmptyMind`
**Name:** Empty Mind  
**Tooltip:** Spells are disabled. Whenever it gets a kill, it takes an extra turn.  
**Source:** `keyword_tooltips.gon`  

```
EmptyMind {
    name "KEYWORD_EMPTYMIND_NAME"
    tooltip "KEYWORD_EMPTYMIND_DESC"
}
```

---

### `Enrage`
**Name:** `Enrage`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
Enrage { 
    name "Enrage"
    tooltip None
}
```

---

### `EventBounty`
**Name:** Bounty  
**Tooltip Stacks:** Hunted by the bounty hunter.  
**Source:** `keyword_tooltips.gon`  

```
EventBounty {
    name "KEYWORD_EVENTBOUNTY_NAME"
    tooltip_stacks "KEYWORD_EVENTBOUNTY_DESC"
}
```

---

### `Exhaustion`
**Name:** Exhaustion  
**Tooltip Stacks:** Takes {stacks} unblockable damage at the start of its turn, then increase Exhaustion by 1. Whenever it would gain mana or health, gain {stacks} less mana or health. Combat regen disabled. Cannot be removed. It's time to finish the fight.  
**Tooltip Stackless:** Takes unblockable damage at the start of its turn, then increase Exhaustion by 1. Decreases mana and health gain. Combat regen disabled.  
**Source:** `keyword_tooltips.gon`  

```
Exhaustion {
    name "KEYWORD_EXHAUSTION_NAME"
    tooltip_stacks "KEYWORD_EXHAUSTION_DESC"
    tooltip_stackless "KEYWORD_EXHAUSTION_DESC_STACKLESS"
}
```

---

### `ExtraBasicAttacks_Status`
**Name:** Extra Attacks  
**Tooltip Stacks:** Can attack {stacks} extra times each turn.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
ExtraBasicAttacks_Status {
    name "KEYWORD_EXTRAATTACK_NAME"
    tooltip_stacks "KEYWORD_EXTRAATTACK_DESC"
    tooltip_stackless none 
}
```

---

### `ExtraBasicMoves_Status`
**Name:** Extra Moves  
**Tooltip Stacks:** Can move {stacks} extra times each turn.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
ExtraBasicMoves_Status {
    name "KEYWORD_EXTRAMOVE_NAME"
    tooltip_stacks "KEYWORD_EXTRAMOVE_DESC"
    tooltip_stackless none 
}
```

---

### `Fear`
**Name:** Fear  
**Tooltip:** Moves as far away from enemies as it can at the start of its turn.  
**Source:** `keyword_tooltips.gon`  

```
Fear {
    name "KEYWORD_FEAR_NAME"
    tooltip "KEYWORD_FEAR_DESC"
}
```

---

### `FireArmor`
**Name:** `FireArmor`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
FireArmor { 
    name "FireArmor"
    tooltip None
}
```

---

### `FireArmor2`
**Name:** `FireArmor2`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
FireArmor2 { 
    name "FireArmor2"
    tooltip None
}
```

---

### `FlyDamageIncrease`
**Alias:** `DamageUp`  
**Source:** `keyword_tooltips.gon`  

```
FlyDamageIncrease {
    alias DamageUp
}
```

---

### `FreeSpell`
**Name:** Free Spell  
**Tooltip:** The next spell you cast costs 0 mana.  
**Source:** `keyword_tooltips.gon`  

```
FreeSpell { 
    name "KEYWORD_FREESPELL_NAME"
    tooltip "KEYWORD_FREESPELL_DESC"
}
```

---

### `Freeze`
**Name:** Freeze  
**Tooltip:** Cannot take damage. Unfreezes at the start of its turn.  
**Source:** `keyword_tooltips.gon`  

```
Freeze {
    name "KEYWORD_FREEZE_NAME"
    tooltip "KEYWORD_FREEZE_DESC"
}
```

---

### `GlobalFamiliarDamageBoost`
**Alias:** `DamageUp`  
**Source:** `keyword_tooltips.gon`  

```
GlobalFamiliarDamageBoost {
    alias DamageUp
}
```

---

### `GlobalFamiliarMoveBoost`
**Alias:** `MovementUp`  
**Source:** `keyword_tooltips.gon`  

```
GlobalFamiliarMoveBoost {
    alias MovementUp
}
```

---

### `Grappled`
**Name:** Grappled  
**Tooltip:** Immobile as long as it's next to the thing that grappled it.  
**Source:** `keyword_tooltips.gon`  

```
Grappled {
    name "KEYWORD_GRAPPLED_NAME"
    tooltip "KEYWORD_GRAPPLED_DESC"
}
```

---

### `HealthRegenUp`
**Name:** Health Regen  
**Tooltip Stacks:** Regenerate {stacks} health at the end of its turn.  
**Tooltip Stackless:** Regenerates health at the end of its turn.  
**Source:** `keyword_tooltips.gon`  

```
HealthRegenUp {
    name "KEYWORD_HEALTHREGEN_NAME"
    tooltip_stacks "KEYWORD_HEALTHREGEN_DESC"
    tooltip_stackless "KEYWORD_HEALTHREGEN_DESC_STACKLESS"
}
```

---

### `HeatWave`
**Name:** Heat Wave  
**Tooltip:** Heals are reduced by 1. Does not heal after battle. Can be mitigated with water.  
**Source:** `keyword_tooltips.gon`  

```
HeatWave {
    name "KEYWORD_DEHYDRATED_NAME"
    tooltip "KEYWORD_DEHYDRATED_DESC"
}
```

---

### `HeavierHits`
**Name:** Heavier Hits  
**Tooltip Stacks:** Physical damage inflicts Bruise {stacks} this turn.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
HeavierHits {
    name "KEYWORD_HEAVIERHITS_NAME"
    tooltip_stacks "KEYWORD_HEAVIERHITS_DESC_STACKS"
    tooltip_stackless none
}
```

---

### `HeavyHits`
**Name:** Heavy Hits  
**Tooltip Stacks:** Basic attack inflicts Bruise {stacks} this turn.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
HeavyHits {
    name "KEYWORD_HEAVYHITS_NAME"
    tooltip_stacks "KEYWORD_HEAVYHITS_DESC_STACKS"
    tooltip_stackless none
}
```

---

### `Hex`
**Name:** Hex  
**Tooltip Stacks:** Spells cost {stacks} more mana to cast.  
**Tooltip Stackless:** Spells cost more mana to cast.  
**Source:** `keyword_tooltips.gon`  

```
Hex {
    name "KEYWORD_HEX_NAME"
    tooltip_stacks "KEYWORD_HEX_DESC"

    tooltip_stackless "KEYWORD_HEX_DESC_STACKLESS"
}
```

---

### `IceArmor`
**Name:** `IceArmor`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
IceArmor { 
    name "IceArmor"
    tooltip None
}
```

---

### `ImbueBleed`
**Name:** `ImbueBleed`  
**Tooltip Stacks:** `Next physical attack inflicts Bleed {stacks}`  
**Tooltip Stackless:** `Next physical attack inflicts Bleed`  
**Source:** `keyword_tooltips.gon`  

```
ImbueBleed { 
    name "ImbueBleed"
    tooltip_stacks "Next physical attack inflicts Bleed {stacks}"
    tooltip_stackless "Next physical attack inflicts Bleed"
}
```

---

### `ImbueKnockOutCoin`
**Name:** `ImbueKnockOutCoin`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
ImbueKnockOutCoin { 
    name "ImbueKnockOutCoin"
    tooltip None
}
```

---

### `ImbueManaLeech`
**Name:** `ImbueManaLeech`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
ImbueManaLeech { 
    name "ImbueManaLeech"
    tooltip None
}
```

---

### `ImbuePoison`
**Name:** `ImbuePoison`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
ImbuePoison { 
    name "ImbuePoison"
    tooltip None
}
```

---

### `ImbueRandomStatDown`
**Name:** `ImbueRandomStatDown`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
ImbueRandomStatDown { 
    name "ImbueRandomStatDown"
    tooltip None
}
```

---

### `ImbueWeakness`
**Name:** `ImbueWeakness`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
ImbueWeakness { 
    name "ImbueWeakness"
    tooltip None
}
```

---

### `Immobile`
**Name:** Immobile  
**Tooltip:** Cannot move.  
**Source:** `keyword_tooltips.gon`  

```
Immobile {
    name "KEYWORD_IMMOBILE_NAME"
    tooltip "KEYWORD_IMMOBILE_DESC"
}
```

---

### `Infested`
**Name:** Infested  
**Tooltip:** The things infesting this pop out when it dies, destroying its corpse.  
**Source:** `keyword_tooltips.gon`  

```
Infested {
    name "KEYWORD_INFESTED_NAME"
    tooltip "KEYWORD_INFESTED_DESC"
}
```

---

### `IntelligenceUp`
**Name:** Intelligence Up  
**Name Stacks Neg:** Intelligence Down  
**Tooltip Stacks Pos:** Intelligence increased by {stacks}.  
Intelligence affects mana regen.  
**Tooltip Stacks Neg:** Intelligence decreased by {absstacks}.  
Intelligence affects mana regen.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
IntelligenceUp {
    name "KEYWORD_INTUP_NAME"
    name_stacks_neg "KEYWORD_INTDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_INTUP_DESC"
    tooltip_stacks_neg "KEYWORD_INTDOWN_DESC"

    tooltip_stackless none 
}
```

---

### `Invulnerable`
**Name:** Invulnerable  
**Tooltip:** Does not take damage.  
**Source:** `keyword_tooltips.gon`  

```
Invulnerable {
    name "KEYWORD_INVULNERABLE_NAME"
    tooltip "KEYWORD_INVULNERABLE_DESC"
}
```

---

### `KineticSpikes`
**Name:** Kinetic Spikes  
**Tooltip Stacks:** When this takes damage, emit {stacks} Sparkles.  
**Tooltip Stacks Singular:** When this takes damage, emit a Sparkle.  
**Tooltip Stackless:** When this takes damage, emit Sparkles.  
**Source:** `keyword_tooltips.gon`  

```
KineticSpikes {
    name "KEYWORD_KINETICSPPIKES_NAME"
    tooltip_stacks "KEYWORD_KINETICSPPIKES_DESC"
    tooltip_stacks_singular "KEYWORD_KINETICSPPIKES_DESC_SINGULAR"
    tooltip_stackless "KEYWORD_KINETICSPPIKES_DESC_STACKLESS"
}
```

---

### `Knockback`
**Name:** `Knockback`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
Knockback { 
    name "Knockback"
    tooltip None
}
```

---

### `LateBloomer`
**Name:** Late Bloomer  
**Tooltip Stacks:** Gain All Stats Up 3 in {stacks} turns.  
**Tooltip Stacks Singular:** Gain All Stats Up 3 next turn.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
LateBloomer {
    name "KEYWORD_LATEBLOOMER_NAME"
    tooltip_stacks "KEYWORD_LATEBLOOMER_DESC"
    tooltip_stacks_singular "KEYWORD_LATEBLOOMER_SINGULAR_DESC"

    tooltip_stackless none
}
```

---

### `Leeches`
**Name:** Leeches  
**Name Reference Applier:** {applier's} Leeches.  
**Tooltip Stacks:** Drains {stacks} health at the end of the round.  
**Tooltip Reference Applier:** Drains {stacks} health at the end of {applier's} turn and gives it to {applier}.  
**Tooltip Stackless:** Drains health from the leeched unit at the end of your turn.  
**Source:** `keyword_tooltips.gon`  

```
Leeches {
    name "KEYWORD_LEECHES_NAME"
    name_reference_applier "KEYWORD_LEECHES_NAME_APPLIER"
    tooltip_stacks "KEYWORD_LEECHES_DESC"
    tooltip_reference_applier "KEYWORD_LEECHES_DESC_APPLIER"

    tooltip_stackless "KEYWORD_LEECHES_DESC_STACKLESS"
}
```

---

### `Lifesteal`
**Name:** Lifesteal  
**Tooltip Stacks:** The next {stacks} basic attacks you do heal you for the amount of health damage they inflict.  
**Tooltip Stackless:** Your next basic attack heals you for the amount of health damage it inflicts.  
**Source:** `keyword_tooltips.gon`  

```
Lifesteal {
    name "KEYWORD_LIFESTEAL_NAME"
    tooltip_stacks "KEYWORD_LIFESTEAL_DESC"

    tooltip_stackless "KEYWORD_LIFESTEAL_DESC_STACKLESS"
}
```

---

### `Leech`
**Name:** Lifesteal  
**Tooltip:** Heals you equal to the amount of health damage dealt.  
**Icon Frame:** `17`  
**Source:** `keyword_tooltips.gon`  

```
Leech {
    name "KEYWORD_LIFESTEAL_NAME"
    tooltip "KEYWORD_LIFESTEAL2_DESC"

    icon_frame 17
}
```

---

### `LoseShieldNextTurn`
**Name:** `LoseShieldNextTurn`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
LoseShieldNextTurn { 
    name "LoseShieldNextTurn"
    tooltip None
}
```

---

### `LuckUp`
**Name:** Luck Up  
**Name Stacks Neg:** Luck Down  
**Tooltip Stacks Pos:** Luck increased by {stacks}.  
Luck affects base crit chance and all randomness.  
**Tooltip Stacks Neg:** Luck decreased by {absstacks}.  
Luck affects base crit chance and all randomness.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
LuckUp {
    name "KEYWORD_LCKUP_NAME"
    name_stacks_neg "KEYWORD_LCKDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_LCKUP_DESC"
    tooltip_stacks_neg "KEYWORD_LCKDOWN_DESC"

    tooltip_stackless none 
}
```

---

### `Madness`
**Name:** Madness  
**Tooltip:** Thinks everything is an enemy. Uncontrollable.  
**Source:** `keyword_tooltips.gon`  

```
Madness {
    name "KEYWORD_MADNESS_NAME"
    tooltip "KEYWORD_MADNESS_DESC"
}
```

---

### `MagicWeakness`
**Name:** Magic Weakness  
**Tooltip:** Incoming magic damage has 100% Crit Chance and can't miss.  
**Source:** `keyword_tooltips.gon`  

```
MagicWeakness {
    name "KEYWORD_MAGICWEAKNESS_NAME"
    tooltip "KEYWORD_MAGICWEAKNESS_DESC"
}
```

---

### `ManaLeeches`
**Name:** Mana Leeches  
**Name Reference Applier:** {applier's} Mana Leeches  
**Tooltip Stacks:** Drains {stacks} mana at the end of the round.  
**Tooltip Reference Applier:** Drains {stacks} mana at the end of {applier's} turn and gives it to {applier}.  
**Tooltip Stackless:** Drains mana from the leeched unit at the end of your turn.  
**Source:** `keyword_tooltips.gon`  

```
ManaLeeches {
    name "KEYWORD_MANALEECHES_NAME"
    name_reference_applier "KEYWORD_MANALEECHES_NAME_APPLIER"
    tooltip_stacks "KEYWORD_MANALEECHES_DESC"
    tooltip_reference_applier "KEYWORD_MANALEECHES_DESC_APPLIER"

    tooltip_stackless "KEYWORD_MANALEECHES_DESC_STACKLESS"
}
```

---

### `Marked`
**Name:** Marked  
**Tooltip:** Incoming physical damage has 100% Crit Chance, ignores shield, and can't miss.  
**Source:** `keyword_tooltips.gon`  

```
Marked {
    name "KEYWORD_MARKED_NAME"
    tooltip "KEYWORD_MARKED_DESC"
}
```

---

### `Meaty`
**Name:** Meaty  
**Tooltip:** Turns into meat when it dies.  
**Source:** `keyword_tooltips.gon`  

```
Meaty {
    name "KEYWORD_MEATY_NAME"
    tooltip "KEYWORD_MEATY_DESC"
}
```

---

### `MissChance`
**Name:** Miss Chance  
**Tooltip Stacks:** Miss chance increased by {stacks}%.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
MissChance {
    name "KEYWORD_MISSCHANCE_NAME"
    tooltip_stacks "KEYWORD_MISSCHANCE_DESC"
    tooltip_stackless none 
}
```

---

### `MovementUp`
**Name:** Movement Up  
**Name Stacks Neg:** Movement Down  
**Tooltip Stacks Pos:** Basic movement range increased by {stacks}.  
**Tooltip Stacks Neg:** Basic movement range decreased by {stacks}.  
**Tooltip Stackless Pos:** Increases your basic movement's range.  
**Tooltip Stackless Neg:** Decreases your basic movement's range.  
**Source:** `keyword_tooltips.gon`  

```
MovementUp {
    name "KEYWORD_MOVEMENTUP_NAME"
    name_stacks_neg "KEYWORD_MOVEMENTDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_MOVEMENTUP_DESC"
    tooltip_stacks_neg "KEYWORD_MOVEMENTDOWN_DESC"

    tooltip_stackless_pos "KEYWORD_MOVEMENTUP_DESC_STACKLESS"
    tooltip_stackless_neg "KEYWORD_MOVEMENTDOWN_DESC_STACKLESS"
}
```

---

### `MoveQuivered`
**Name:** Bonus Move  
**Tooltip Stacks Singular:** An extra basic move that is saved across turns if unused.  
**Tooltip Stacks:** {stacks} extra basic moves that are saved across turns if unused.  
**Source:** `keyword_tooltips.gon`  

```
MoveQuivered {
    name "KEYWORD_BONUSMOVE_NAME"
    tooltip_stacks_singular "KEYWORD_BONUSMOVE_DESC"
    tooltip_stacks "KEYWORD_BONUSMOVE_DESC_STACKS"
}
```

---

### `MutateAfterXTurns`
**Alias:** `TransformInXTurns`  
**Source:** `keyword_tooltips.gon`  

```
MutateAfterXTurns {
    alias TransformInXTurns
}
```

---

### `Muted`
**Name:** Muted  
**Tooltip Stacks Singular:** One of your spells is disabled until {applier} dies.  
**Tooltip Stacks:** {stacks} of your spells are disabled until {applier} dies.  
**Tooltip Stackless:** Disables a random spell until the applier is killed.  
**Source:** `keyword_tooltips.gon`  

```
Muted { 
    name "KEYWORD_MUTED_NAME"
    tooltip_stacks_singular "KEYWORD_MUTED_DESC_SINGULAR"
    tooltip_stacks "KEYWORD_MUTED_DESC"

    tooltip_stackless "KEYWORD_MUTED_DESC_STACKLESS"
}
```

---

### `NextAbilityHeals`
**Name:** `NextAbilityHeals`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
NextAbilityHeals { 
    name "NextAbilityHeals"
    tooltip None
}
```

---

### `NextAbilityIncreaseRange`
**Name:** `NextAbilityIncreaseRange`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
NextAbilityIncreaseRange { 
    name "NextAbilityIncreaseRange"
    tooltip None
}
```

---

### `NextActionLuckUp`
**Alias:** `LuckUp`  
**Source:** `keyword_tooltips.gon`  

```
NextActionLuckUp {
    alias LuckUp
}
```

---

### `NextAttackBonusRange`
**Name:** Bonus Range  
**Tooltip Stacks:** Your next basic attack has +{stacks} range.  
**Tooltip Stackless:** Increases the range of your next basic attack.  
**Source:** `keyword_tooltips.gon`  

```
NextAttackBonusRange {
    name "KEYWORD_BONUSRANGE_NAME"
    tooltip_stacks "KEYWORD_BONUSRANGE_DESC"
    tooltip_stackless "KEYWORD_BONUSRANGE_DESC_STACKLESS"
}
```

---

### `NextDamageReduceAndHealAllies`
**Name:** `NextDamageReduceAndHealAllies`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
NextDamageReduceAndHealAllies { 
    name "NextDamageReduceAndHealAllies"
    tooltip None
}
```

---

### `NextDamageReduceAndPushback`
**Name:** `NextDamageReduceAndPushback`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
NextDamageReduceAndPushback { 
    name "NextDamageReduceAndPushback"
    tooltip None
}
```

---

### `NextDamageReduceThisTurn`
**Name:** `NextDamageReduceThisTurn`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
NextDamageReduceThisTurn { 
    name "NextDamageReduceThisTurn"
    tooltip None
}
```

---

### `NextMoveRangeIncrease`
**Name:** `NextMoveRangeIncrease`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
NextMoveRangeIncrease { 
    name "NextMoveRangeIncrease"
    tooltip None
}
```

---

### `NextSpellHealEqualToMana`
**Name:** `NextSpellHealEqualToMana`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
NextSpellHealEqualToMana { 
    name "NextSpellHealEqualToMana"
    tooltip None
}
```

---

### `NextTurnDoubleRangedDamage`
**Name:** Double Ranged Damage  
**Tooltip:** All ranged physical attacks and abilities deal double damage.  
**Source:** `keyword_tooltips.gon`  

```
NextTurnDoubleRangedDamage { 
    name "KEYWORD_DOUBLERANGEDDMG_NAME"
    tooltip "KEYWORD_DOUBLERANGEDDMG_DESC"
}
```

---

### `NoHealthRegen`
**Name:** No Health Regen  
**Tooltip:** Health won't regen automatically and does not regen at the end of battle.  
**Source:** `keyword_tooltips.gon`  

```
NoHealthRegen {
    name "KEYWORD_NOHEALTHREGEN_NAME"
    tooltip "KEYWORD_NOHEALTHREGEN_DESC"
}
```

---

### `NoManaRegen`
**Name:** No Mana Regen  
**Tooltip:** Mana won't regen automatically.  
**Source:** `keyword_tooltips.gon`  

```
NoManaRegen {
    name "KEYWORD_NOMANAREGEN_NAME"
    tooltip "KEYWORD_NOMANAREGEN_DESC"
}
```

---

### `OldStealth`
**Name:** `OldStealth`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
OldStealth { 
    name "OldStealth"
    tooltip None
}
```

---

### `OneUseSpellDamageUp`
**Alias:** `SpellDamageUp`  
**Source:** `keyword_tooltips.gon`  

```
OneUseSpellDamageUp {
    alias SpellDamageUp
}
```

---

### `Ostracized`
**Name:** Ostracized  
**Tooltip:** Every unit sees this as an enemy and will attack it with priority.  
**Source:** `keyword_tooltips.gon`  

```
Ostracized {
    name "KEYWORD_OSTRACIZED_NAME"
    tooltip "KEYWORD_OSTRACIZED_DESC"
}
```

---

### `PassiveBrace`
**Alias:** `Brace`  
**Source:** `keyword_tooltips.gon`  

```
PassiveBrace {
    alias Brace
}
```

---

### `PermanentCharm`
**Alias:** `Charmed`  
**Source:** `keyword_tooltips.gon`  

```
PermanentCharm {
    alias Charmed
}
```

---

### `CapturedFamiliarIcon`
**Name:** Captured Familiar  
**Tooltip:** Was once an enemy, is now on your team. Will follow you to future battles if it doesn't die.  
**Source:** `keyword_tooltips.gon`  

```
CapturedFamiliarIcon {
    name "KEYWORD_CAPTUREDFAMILIAR_NAME"
    tooltip "KEYWORD_CAPTUREDFAMILIAR_DESC"
}
```

---

### `PermanentImmobile`
**Alias:** `Immobile`  
**Source:** `keyword_tooltips.gon`  

```
PermanentImmobile {
    alias Immobile
}
```

---

### `PermanentMadness`
**Alias:** `Madness`  
**Source:** `keyword_tooltips.gon`  

```
PermanentMadness {
    alias Madness
}
```

---

### `Petrify`
**Name:** Petrify  
**Tooltip Stacks:** It's a rock for {stacks} turns.  
**Tooltip Stacks Singular:** It's a rock for 1 turn.  
**Tooltip Stackless:** Becomes a rock temporarily.  
**Source:** `keyword_tooltips.gon`  

```
Petrify {
    name "KEYWORD_PETRIFY_NAME"
    tooltip_stacks "KEYWORD_PETRIFY_DESC"
    tooltip_stacks_singular KEYWORD_PETRIFY_DESC_SINGULAR
    tooltip_stackless "KEYWORD_PETRIFY_DESC_STACKLESS"
}
```

---

### `Poison`
**Name:** Poison  
**Tooltip Stacks:** Takes {stacks} damage at the start of each of its turns. Incoming healing is less effective but cures 1 Poison.  
**Tooltip Stackless:** Takes damage at the start of every turn. Incoming healing is less effective but cures 1 Poison.  
**Source:** `keyword_tooltips.gon`  

```
Poison {
    name "KEYWORD_POISON_NAME"
    tooltip_stacks "KEYWORD_POISON_DESC"
    tooltip_stackless "KEYWORD_POISON_DESC_STACKLESS"
}
```

---

### `PoisonLace`
**Name:** Poison Lace  
**Tooltip Stacks:** Basic attack inflicts +{stacks} Poison.  
**Tooltip Stackless:** Basic attack inflicts Poison.  
**Source:** `keyword_tooltips.gon`  

```
PoisonLace {
    name "KEYWORD_POISONLACE_NAME"
    tooltip_stacks "KEYWORD_POISONLACE_DESC"
    tooltip_stackless "KEYWORD_POISONLACE_DESC_STACKLESS"
}
```

---

### `CurrentWeaponAddPoison`
**Name:** Poison Lace (Weapon)  
**Tooltip Stacks:** Your weapon inflicts +{stacks} Poison.  
**Tooltip Stackless:** Your weapon inflicts Poison.  
**Source:** `keyword_tooltips.gon`  

```
CurrentWeaponAddPoison {
    name "KEYWORD_WPOISONLACE_NAME"
    tooltip_stacks "KEYWORD_WPOISONLACE_DESC"
    tooltip_stackless "KEYWORD_WPOISONLACE_DESC_STACKLESS"
}
```

---

### `PoisonThorns`
**Name:** Poisonous  
**Tooltip Stacks:** Inflicts Poison {stacks} to units that contact you.  
**Tooltip Stackless:** Inflicts Poison to units that contact you.  
**Source:** `keyword_tooltips.gon`  

```
PoisonThorns {
    name "KEYWORD_POISONOUS_NAME"
    tooltip_stacks "KEYWORD_POISONOUS_DESC"
    tooltip_stackless "KEYWORD_POISONOUS_DESC_STACKLESS"
}
```

---

### `Possessed`
**Name:** Possessed  
**Tooltip Stacks:** Takes {stacks} extra turns and is uncontrollable and charmed on those turns.  
**Tooltip Stacks Singular:** Takes an extra turn and is uncontrollable and charmed on that turn.  
**Tooltip Stackless:** Takes an extra Charmed turn.  
**Source:** `keyword_tooltips.gon`  

```
Possessed {
    name "KEYWORD_POSSESED_NAME"
    tooltip_stacks "KEYWORD_POSSESSED_DESC"
    tooltip_stacks_singular KEYWORD_POSSESSED_DESC_SIGNULAR
    tooltip_stackless "KEYWORD_POSSESSED_DESC_STACKLESS"
}
```

---

### `PreEmptiveCounterNextAttacks`
**Name:** Preemptive Counter  
**Tooltip Stacks:** Attack the next {stacks} things that target you before they attack you, automatically.  
**Tooltip Stacks Singular:** Attack the next thing that targets you before it attacks you, automatically.  
**Tooltip Stackless:** Attack the next thing that targets you before it attacks you, automatically.  
**Source:** `keyword_tooltips.gon`  

```
PreEmptiveCounterNextAttacks {
    name "KEYWORD_PREEMTIVECOUNTER_NAME"
    tooltip_stacks "KEYWORD_PREEMTIVECOUNTER_DESC"
    tooltip_stacks_singular "KEYWORD_PREEMTIVECOUNTER_DESC_STACKLESS"
    tooltip_stackless "KEYWORD_PREEMTIVECOUNTER_DESC_STACKLESS"
}
```

---

### `Quivered`
**Name:** Bonus Attack  
**Tooltip Stacks Singular:** An extra basic attack that is saved across turns if unused.  
**Tooltip Stacks:** {stacks} extra basic attacks that are saved across turns if unused.  
**Source:** `keyword_tooltips.gon`  

```
Quivered {
    name "KEYWORD_QUIVERED_NAME"
    tooltip_stacks_singular "KEYWORD_QUIVERED_DESC_STACKLESS"
    tooltip_stacks "KEYWORD_QUIVERED_DESC"
}
```

---

### `RandomInjury`
**Name:** Random Injury  
**Tooltip:** Gain a random injury that lowers one of your stats by 1, permanently.  
**Icon Frame:** `58`  
**Source:** `keyword_tooltips.gon`  

```
RandomInjury {
    name "KEYWORD_RANDOMINJURY_NAME"
    tooltip "KEYWORD_RANDOMINJURY_DESC"

    icon_frame 58
}
```

---

### `HealRandomInjury`
**Name:** Cure Random Injury  
**Tooltip:** Cure a random injury that was permanently lowering one of your stats, if you have any.  
**Icon Frame:** `158`  
**Source:** `keyword_tooltips.gon`  

```
HealRandomInjury {
    name "KEYWORD_HEALRANDOMINJURY_NAME"
    tooltip "KEYWORD_HEALRANDOMINJURY_DESC"

    icon_frame 158
}
```

---

### `RandomMagicMissile`
**Name:** Sparkle  
**Tooltip:** A projectile that deals 1 magic damage to a random enemy.  
**Icon Frame:** `154`  
**Source:** `keyword_tooltips.gon`  

```
RandomMagicMissile {
    name "KEYWORD_SPARKLE_NAME"
    tooltip "KEYWORD_SPARKLE_DESC"

    icon_frame 154
}
```

---

### `RangeUp`
**Name:** Range Up  
**Tooltip Stacks:** Range increased by {stacks}.  
**Tooltip Stackless:** Increases the range of your basic attack and projectile abilities.  
**Source:** `keyword_tooltips.gon`  

```
RangeUp {
    name "KEYWORD_RANGEUP_NAME"
    tooltip_stacks "KEYWORD_RANGEUP_DESC"
    tooltip_stackless "KEYWORD_RANGEUP_DESC_STACKLESS"
}
```

---

### `TempBonusKnockback`
**Name:** Bonus Knockback  
**Tooltip Stacks:** Knockback you inflict is increased by {stacks}.  
**Tooltip Stackless:** `None`  
**Source:** `keyword_tooltips.gon`  

```
TempBonusKnockback {
    name "KEYWORD_BONUSKNOCKBACK_NAME"
    tooltip_stacks "KEYWORD_BONUSKNOCKBACK_DESC"
    tooltip_stackless None
}
```

---

### `TempBonusKnockbackDamage`
**Name:** Bonus Knockback Damage  
**Tooltip Stacks:** Knockback damage you deal is increased by {stacks}.  
**Tooltip Stackless:** `None`  
**Source:** `keyword_tooltips.gon`  

```
TempBonusKnockbackDamage {
    name "KEYWORD_BONUSKNOCKBACKDAMAGE_NAME"
    tooltip_stacks "KEYWORD_BONUSKNOCKBACKDAMAGE_DESC"
    tooltip_stackless None
}
```

---

### `TemporaryItem`
**Name:** Temporary Item  
**Tooltip:** Is lost at the end of the battle.  
**Icon Frame:** `164`  
**Source:** `keyword_tooltips.gon`  

```
TemporaryItem {
    name "KEYWORD_TEMPITEM_NAME"
    tooltip "KEYWORD_TEMPITEM_DESC"

    icon_frame 164
}
```

---

### `TempRangeUp`
**Name:** Range Up (Temporary)  
**Tooltip Stacks:** Range increased by {stacks} until the end of the turn.  
**Tooltip Stackless:** Increases the range of your basic attack and projectile abilities until the end of the turn.  
**Source:** `keyword_tooltips.gon`  

```
TempRangeUp {
    name "KEYWORD_TEMPRANGE_NAME"
    tooltip_stacks "KEYWORD_TEMPRANGE_DESC"
    tooltip_stackless "KEYWORD_TEMPRANGE_DESC_STACKLESS"
}
```

---

### `Reduce`
**Name:** `Reduce`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
Reduce { 
    name "Reduce"
    tooltip None
}
```

---

### `ReduceManaCost`
**Name:** Insight  
**Tooltip Stacks:** Spells cost {stacks} less mana to cast.  
**Tooltip Stackless:** Spells cost less mana to cast.  
**Source:** `keyword_tooltips.gon`  

```
ReduceManaCost {
    name "KEYWORD_REDUCEMANACOST_NAME"
    tooltip_stacks "KEYWORD_REDUCEMANACOST_DESC"
    tooltip_stackless "KEYWORD_REDUCEMANACOST_DESC_STACKLESS"
}
```

---

### `ReduceManaCostExcludeBrainstorm`
**Name:** Insight  
**Tooltip Stacks:** Spells cost {stacks} less mana to cast, excluding Brainstorm.  
**Tooltip Stackless:** Spells cost less mana to cast, excluding Brainstorm. (cannot reduce cost to 0).  
**Source:** `keyword_tooltips.gon`  

```
ReduceManaCostExcludeBrainstorm {
    name "KEYWORD_INSIGHT_NAME"
    tooltip_stacks "KEYWORD_INSIGHT_DESC"
    tooltip_stackless "KEYWORD_INSIGHT_DESC_STACKLESS"
}
```

---

### `Reflect`
**Name:** Reflect  
**Tooltip Stacks:** Reflects the next {stacks} projectiles you are hit with back at the attacker.  
**Tooltip Stacks Singular:** Reflect the next projectile you're hit with back at the attacker.  
**Source:** `keyword_tooltips.gon`  

```
Reflect {
    name "KEYWORD_REFLECT_NAME"
    tooltip_stacks "KEYWORD_REFLECT_DESC"
    tooltip_stacks_singular "KEYWORD_REFLECT_DESC_STACKLESS"
}
```

---

### `ReviveNextRound`
**Name:** Auto Revive  
**Tooltip Stacks Singular:** Revives at the end of the round.  
**Tooltip Stacks:** Revives at the end of the next round.  
**Tooltip Stackless:** Revives at the end of the next round.  
**Source:** `keyword_tooltips.gon`  

```
ReviveNextRound {
    name "KEYWORD_AUTOREVIVE_NAME"
    tooltip_stacks_singular "KEYWORD_AUTOREVIVE_DESC_SINGULAR"
    tooltip_stacks "KEYWORD_AUTOREVIVE_DESC"
    tooltip_stackless KEYWORD_AUTOREVIVE_DESC
}
```

---

### `Robot`
**Name:** Energized  
**Tooltip:** Takes an extra turn. Cannot be Energized again until after that turn ends.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
Robot { 
    name "KEYWORD_ENERGIZED_NAME"
    tooltip "KEYWORD_ENERGIZED_DESC"
    tooltip_stackless none
}
```

---

### `Rot`
**Name:** Rot  
**Tooltip:** Hatches a Fly at the end of its turn. Damage from worms and bugs always crits against this.  
**Source:** `keyword_tooltips.gon`  

```
Rot { 
    name "KEYWORD_ROT_NAME"
    tooltip "KEYWORD_ROT_DESC"
}
```

---

### `SafeDoomed`
**Name:** Doomed  
**Tooltip:** Ticks down at the end of your turn. When it hits 0, Die (without being injured).  
**Source:** `keyword_tooltips.gon`  

```
SafeDoomed {
    name "KEYWORD_SAFEDOOMED_NAME"
    tooltip "KEYWORD_SAFEDOOMED_DESC"
}
```

---

### `Scrambled`
**Name:** Scrambled  
**Tooltip:** Abilities are scrambled, temporarily.  
**Source:** `keyword_tooltips.gon`  

```
Scrambled { 
    name "KEYWORD_SCRAMBLED_NAME"
    tooltip "KEYWORD_SCRAMBLED_DESC"
}
```

---

### `SerratedClaws`
**Name:** Serrated Claws  
**Tooltip Stacks:** Basic attack inflicts +{stacks} Bleed.  
**Tooltip Stackless:** Basic attack inflicts Bleed.  
**Source:** `keyword_tooltips.gon`  

```
SerratedClaws {
    name "KEYWORD_SERRATED_NAME"
    tooltip_stacks "KEYWORD_SERRATED_DESC"
    tooltip_stackless "KEYWORD_SERRATED_DESC_STACKLESS"
}
```

---

### `Shield`
**Name:** Shield  
**Tooltip:** `None`  
**Tooltip Stackless:** Blocks incoming damage.  
**Source:** `keyword_tooltips.gon`  

```
Shield { 
    name "KEYWORD_SHIELD_NAME"
    tooltip None

    tooltip_stackless "KEYWORD_SHIELD_DESC_STACKLESS"
}
```

---

### `shield`
**Alias:** `Shield`  
**Source:** `keyword_tooltips.gon`  

```
shield {
    alias Shield
}
```

---

### `ShortCircuit`
**Name:** Short Circuit  
**Tooltip:** All actions are disabled. Cast Break Circuit to break.  
**Source:** `keyword_tooltips.gon`  

```
ShortCircuit {
    name "KEYWORD_SHORTCIRCUIT_NAME"
    tooltip "KEYWORD_SHORTCIRCUIT_DESC"
}
```

---

### `SkipNextTurn`
**Name:** `SkipNextTurn`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
SkipNextTurn { 
    name "SkipNextTurn"
    tooltip None
}
```

---

### `Sleep`
**Name:** Sleep  
**Tooltip Stacks:** Skip the next {stacks} turns. Being attacked has a chance to wake you up.  
**Tooltip Stackless:** Skip the next turn. Being attacked has a chance to wake you up.  
**Source:** `keyword_tooltips.gon`  

```
Sleep {
    name "KEYWORD_SLEEP_NAME"
    tooltip_stacks "KEYWORD_SLEEP_DESC"

    tooltip_stackless "KEYWORD_SLEEP_DESC_STACKLESS"
}
```

---

### `SleepParalysis`
**Name:** Sleep (Paralysis)  
**Tooltip Stacks:** You are asleep until your sleep paralysis demon is killed.  
**Source:** `keyword_tooltips.gon`  

```
SleepParalysis {
    name "KEYWORD_SLEEPPAR_NAME"
    tooltip_stacks "KEYWORD_SLEEPPAR_DESC"
}
```

---

### `Slow`
**Name:** Slow  
**Tooltip Stacks:** Movement range is reduced to 2 for the next {stacks} turns. Takes its turn later.  
**Tooltip Stackless:** Movement range is reduced to 2. Takes its turn later.  
**Tooltip Stacks Neg:** Movement range is reduced to 2. Takes its turn later.  
**Source:** `keyword_tooltips.gon`  

```
Slow {
    name "KEYWORD_SLOW_NAME"
    tooltip_stacks "KEYWORD_SLOW_DESC"
    tooltip_stackless "KEYWORD_SLOW_DESC_STACKLESS"
    tooltip_stacks_neg "KEYWORD_SLOW_DESC_STACKLESS"
}
```

---

### `SoulLink`
**Name:** Soul Link  
**Tooltip:** Whenever a soul linked character loses health, all soul linked characters lose that health as well.  
**Source:** `keyword_tooltips.gon`  

```
SoulLink {
    name "KEYWORD_SOULLINK_NAME"
    tooltip "KEYWORD_SOULLINK_DESC"
}
```

---

### `SpeedUp`
**Name:** Speed Up  
**Name Stacks Neg:** Speed Down  
**Tooltip Stacks Pos:** Speed increased by {stacks}.  
Speed affects movement range and turn order.  
**Tooltip Stacks Neg:** Speed decreased by {absstacks}.  
Speed affects movement range and turn order.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
SpeedUp {
    name "KEYWORD_SPDUP_NAME"
    name_stacks_neg "KEYWORD_SPDDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_SPDUP_DESC"
    tooltip_stacks_neg "KEYWORD_SPWDDOWN_DESC"

    tooltip_stackless none 
}
```

---

### `SpeedUp_WithoutInitiative`
**Alias:** `SpeedUp`  
**Source:** `keyword_tooltips.gon`  

```
SpeedUp_WithoutInitiative {
    alias SpeedUp
}
```

---

### `SpellDamageUp`
**Name:** Magic Damage Up  
**Tooltip Stacks:** Magic damage you inflict does {stacks} extra damage.  
**Tooltip Stackless:** Increases any magical damage you deal.  
**Source:** `keyword_tooltips.gon`  

```
SpellDamageUp { 
    name "KEYWORD_MAGICDMGUP_NAME"
    tooltip_stacks "KEYWORD_MAGICDMGUP_DESC"

    tooltip_stackless "KEYWORD_MAGICDMGUP_DESC_STACKLESS"
}
```

---

### `SpellShield`
**Name:** `SpellShield`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
SpellShield { 
    name "SpellShield"
    tooltip None
}
```

---

### `SpiderInfested`
**Name:** Infested  
**Tooltip:** The spiders infesting this pop out when it dies, destroying its corpse.  
**Source:** `keyword_tooltips.gon`  

```
SpiderInfested {
    name "KEYWORD_SPIDERINFESTED_NAME"
    tooltip "KEYWORD_SPIDERINFESTED_DESC"
}
```

---

### `SproutsGrantMovement`
**Alias:** `MovementUp`  
**Source:** `keyword_tooltips.gon`  

```
SproutsGrantMovement {
    alias MovementUp
}
```

---

### `StatBounty`
**Name:** Stat Bounty  
**Tooltip Stacks:** Whoever kills this gets All Stats Up {stacks}.  
**Tooltip Stackless:** Whoever kills this gets All Stats Up.  
**Source:** `keyword_tooltips.gon`  

```
StatBounty {
    name "KEYWORD_STATBOUNTY_NAME"
    tooltip_stacks "KEYWORD_STATBOUNTY_DESC"
    tooltip_stackless "KEYWORD_STATBOUNTY_DESC_STACKLESS"
}
```

---

### `Stealth`
**Name:** Stealth  
**Tooltip:** 50% Dodge Chance. Lose Stealth when you get hit.  
**Source:** `keyword_tooltips.gon`  

```
Stealth {
    name "KEYWORD_STEALTH_NAME"
    tooltip "KEYWORD_STEALTH_DESC"
}
```

---

### `StealthUntilBasicAttack`
**Name:** Stealth  
**Tooltip:** 50% Dodge Chance. Lose Stealth when you get hit or use your basic attack.  
**Source:** `keyword_tooltips.gon`  

```
StealthUntilBasicAttack {
    name "KEYWORD_STEALTHUNTIL_NAME"
    tooltip "KEYWORD_STEALTHUNTIL_DESC"
}
```

---

### `StrDownAura`
**Alias:** `StrengthUp`  
**Source:** `keyword_tooltips.gon`  

```
StrDownAura {
    alias StrengthUp
}
```

---

### `DexDownAura`
**Alias:** `DexterityUp`  
**Source:** `keyword_tooltips.gon`  

```
DexDownAura {
    alias DexterityUp
}
```

---

### `SpdDownAura`
**Alias:** `SpeedUp`  
**Source:** `keyword_tooltips.gon`  

```
SpdDownAura {
    alias SpeedUp
}
```

---

### `StrengthForEachNeighboringEnemy`
**Alias:** `StrengthUp`  
**Source:** `keyword_tooltips.gon`  

```
StrengthForEachNeighboringEnemy {
    alias StrengthUp
}
```

---

### `StrengthUp`
**Name:** Strength Up  
**Name Stacks Neg:** Strength Down  
**Tooltip Stacks Pos:** Strength increased by {stacks}.  
Strength affects melee attack and melee ability damage.  
**Tooltip Stacks Neg:** Strength decreased by {absstacks}.  
Strength affects melee attack and melee ability damage.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
StrengthUp {
    name "KEYWORD_STRUP_NAME"
    name_stacks_neg "KEYWORD_STRDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_STRUP_DESC"
    tooltip_stacks_neg "KEYWORD_STRDOWN_DESC"

    tooltip_stackless none 
}
```

---

### `Stun`
**Name:** Stun  
**Tooltip Stacks:** Skip the next {stacks} turns.  
**Tooltip Stackless:** Skip the next turn.  
**Source:** `keyword_tooltips.gon`  

```
Stun {
    name "KEYWORD_STUN_NAME"
    tooltip_stacks "KEYWORD_STUN_DESC"

    tooltip_stackless "KEYWORD_STUN_DESC_STACKLESS"
}
```

---

### `Switcheroo`
**Name:** `Switcheroo`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
Switcheroo { 
    name "Switcheroo"
    tooltip None
}
```

---

### `Tarred`
**Name:** Tarred  
**Tooltip Stacks:** Speed decreased by {stacks}. Flammable.  
Speed affects movement range and turn order.  
**Tooltip Stackless:** Decreases speed. Flammable.  
**Source:** `keyword_tooltips.gon`  

```
Tarred {
    name "KEYWORD_TARRED_NAME"
    tooltip_stacks "KEYWORD_TARRED_DESC"

    tooltip_stackless "KEYWORD_TARRED_DESC_STACKLESS"
}
```

---

### `Taunted`
**Name:** `Taunted`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
Taunted { 
    name "Taunted"
    tooltip None
}
```

---

### `Taunting`
**Name:** `Taunting`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
Taunting { 
    name "Taunting"
    tooltip None
}
```

---

### `Tech`
**Name:** Tech  
**Tooltip:** Increases the quality of the next item you craft or the next familiar you spawn.  
Up to 3 Tech can be used at a time.  
**Source:** `keyword_tooltips.gon`  

```
Tech {
    name "KEYWORD_TECH_NAME"
    tooltip "KEYWORD_TECH_DESC"
}
```

---

### `TempBackstab`
**Name:** Backstab Bonus  
**Tooltip Stacks:** +{stacks}% Backstab Damage this turn. (Plus the default 25% backstab bonus.)  
**Tooltip Stackless:** Increases the damage your Backstabs deal.  
**Source:** `keyword_tooltips.gon`  

```
TempBackstab {
    name "KEYWORD_TEMPBACKSTAB_NAME"
    tooltip_stacks "KEYWORD_TEMPBACKSTAB_DESC"

    tooltip_stackless "KEYWORD_TEMPBACKSTAB_DESC_STACKLESS"
}
```

---

### `TempCharmed`
**Alias:** `Charmed`  
**Source:** `keyword_tooltips.gon`  

```
TempCharmed {
    alias Charmed
}
```

---

### `TempCounterAttack`
**Name:** Counter Attack  
**Tooltip:** Attack things that damage you automatically.  
**Source:** `keyword_tooltips.gon`  

```
TempCounterAttack { 
    name "KEYWORD_TEMPCOUNTER_NAME"
    tooltip "KEYWORD_TEMPCOUNTER_DESC"
}
```

---

### `TempCritChanceUp`
**Alias:** `CritChanceUp`  
**Source:** `keyword_tooltips.gon`  

```
TempCritChanceUp {
    alias CritChanceUp
}
```

---

### `TempDamageUp`
**Alias:** `DamageUp`  
**Source:** `keyword_tooltips.gon`  

```
TempDamageUp {
    alias DamageUp
}
```

---

### `TempDexterityUp`
**Alias:** `DexterityUp`  
**Source:** `keyword_tooltips.gon`  

```
TempDexterityUp {
    alias DexterityUp
}
```

---

### `TempInitiativeChange`
**Name:** Initiative Up  
**Tooltip:** You take your turn earlier in the round.  
**Name Stacks Neg:** Initiative Down  
**Tooltip Stacks Neg:** You take your turn later in the round.  
**Tooltip Stackless Neg:** You take your turn later in the round.  
**Source:** `keyword_tooltips.gon`  

```
TempInitiativeChange {
    name "KEYWORD_TEMPINIT_NAME"
    tooltip "KEYWORD_TEMPINIT_DESC"
    name_stacks_neg "KEYWORD_TEMPINITDOWN_NAME"
    tooltip_stacks_neg "KEYWORD_TEMPINITDOWN_DESC"
    tooltip_stackless_neg "KEYWORD_TEMPINITDOWN_DESC"
}
```

---

### `TempInjuryImmunity`
**Name:** Injury Immunity  
**Tooltip Stacks:** Cannot receive Injuries for any reason. Lasts {stacks} turns.  
**Tooltip Stacks Singular:** Cannot receive Injuries for any reason. Lasts 1 turn.  
**Tooltip Stackless:** none  
**Source:** `keyword_tooltips.gon`  

```
TempInjuryImmunity {
     name "KEYWORD_TEMPIMMUNE_NAME"
     tooltip_stacks "KEYWORD_TEMPIMMUNE_DESC"
     tooltip_stacks_singular "KEYWORD_TEMPIMMUNE_DESC_SINGULAR"
     tooltip_stackless none 
}
```

---

### `TempManaCostReduction`
**Name:** Insight  
**Tooltip Stacks:** Spells cost {stacks} less mana to cast until the end of the turn.  
**Tooltip Stackless:** Spells cost less mana to cast until the end of the turn.  
**Source:** `keyword_tooltips.gon`  

```
TempManaCostReduction {
    name "KEYWORD_TEMPMANAREDUCTION_NAME"
    tooltip_stacks "KEYWORD_TEMPMANAREDUCTION_DESC"
    tooltip_stackless "KEYWORD_TEMPMANAREDUCTION_DESC_STACKLESS"
}
```

---

### `TempMovement`
**Alias:** `MovementUp`  
**Source:** `keyword_tooltips.gon`  

```
TempMovement {
    alias MovementUp
}
```

---

### `TempPreEmptiveCounterAttack`
**Name:** Preemptive Counter  
**Tooltip:** Attack things that target you before they attack you, automatically.  
**Source:** `keyword_tooltips.gon`  

```
TempPreEmptiveCounterAttack { 
    name "KEYWORD_PRECOUNTER_NAME"
    tooltip "KEYWORD_PRECOUNTER_DESC"
}
```

---

### `TempSpeedUp`
**Alias:** `SpeedUp`  
**Source:** `keyword_tooltips.gon`  

```
TempSpeedUp {
    alias SpeedUp
}
```

---

### `TempSpellDamageUp`
**Alias:** `SpellDamageUp`  
**Source:** `keyword_tooltips.gon`  

```
TempSpellDamageUp { 
    alias SpellDamageUp
}
```

---

### `TempStrengthUp`
**Alias:** `StrengthUp`  
**Source:** `keyword_tooltips.gon`  

```
TempStrengthUp {
    alias StrengthUp
}
```

---

### `Thorns`
**Name:** Thorns  
**Tooltip Stacks:** Deals {stacks} damage to units that contact you.  
**Tooltip Stackless:** Deals damage to units that contact you.  
**Source:** `keyword_tooltips.gon`  

```
Thorns {
    name "KEYWORD_THORNS_NAME"
    tooltip_stacks "KEYWORD_THORNS_DESC"

    tooltip_stackless "KEYWORD_THORNS_DESC_STACKLESS"
}
```

---

### `TilesMovedToCritChance`
**Name:** `TilesMovedToCritChance`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
TilesMovedToCritChance { 
    name "TilesMovedToCritChance"
    tooltip None
}
```

---

### `TilesMovedToHealth`
**Name:** `TilesMovedToHealth`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
TilesMovedToHealth { 
    name "TilesMovedToHealth"
    tooltip None
}
```

---

### `TilesMovedToMana`
**Name:** `TilesMovedToMana`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
TilesMovedToMana { 
    name "TilesMovedToMana"
    tooltip None
}
```

---

### `TilesMovedToNeighborHeal`
**Name:** `TilesMovedToNeighborHeal`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
TilesMovedToNeighborHeal { 
    name "TilesMovedToNeighborHeal"
    tooltip None
}
```

---

### `TilesMovedToStrength`
**Name:** `TilesMovedToStrength`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
TilesMovedToStrength { 
    name "TilesMovedToStrength"
    tooltip None
}
```

---

### `TowerDefenseStatus`
**Name:** Sentry Mode  
**Tooltip:** The next time an enemy ends its movement in your basic attack range, attack it.  
**Source:** `keyword_tooltips.gon`  

```
TowerDefenseStatus {
    name "KEYWORD_SENTRY_NAME"
    tooltip "KEYWORD_SENTRY_DESC"
}
```

---

### `TowerDefenseStatus2`
**Name:** Sentry Mode+  
**Tooltip Stacks:** When an enemy ends its movement in your basic attack range, attack it. Lasts {stacks} turns.  
**Tooltip Stackless:** When an enemy ends its movement in your basic attack range, attack it.  
**Source:** `keyword_tooltips.gon`  

```
TowerDefenseStatus2 {
    name "KEYWORD_SENTRYPLUS_NAME"
    tooltip_stacks "KEYWORD_SENTRYPLUS_DESC"

    tooltip_stackless "KEYWORD_SENTRYPLUS_DESC_STACKLESS"
}
```

---

### `TrailBlazer`
**Name:** `Trail Blazer`  
**Tooltip:** `None`  
**Source:** `keyword_tooltips.gon`  

```
TrailBlazer { 
    name "Trail Blazer"
    tooltip None
}
```

---

### `Trample`
**Name:** Trample  
**Tooltip:** `None`  
**Tooltip Stackless:** You can move through other units, damaging and displacing them.  
**Icon Frame:** `153`  
**Source:** `keyword_tooltips.gon`  

```
Trample { 
    name "KEYWORD_TRAMPLE_NAME"
    tooltip None

    tooltip_stackless "KEYWORD_TRAMPLE_DESC_STACKLESS"

    icon_frame 153
}
```

---

### `TransformInXTurns`
**Name:** Transformation  
**Tooltip:** Transforms when the timer hits 0.  
**Source:** `keyword_tooltips.gon`  

```
TransformInXTurns { 
    name "KEYWORD_TRANSFORM_NAME"
    tooltip "KEYWORD_TRANSFORM_DESC"
}
```

---

### `VeinyBonus`
**Alias:** `StrengthUp`  
**Source:** `keyword_tooltips.gon`  

```
VeinyBonus {
    alias StrengthUp
}
```

---

### `Weakness`
**Name:** Weakness  
**Tooltip Stacks:** -2 [img:dex], -2 [img:str], -2 [img:spd]. Lasts {stacks} turns.  
**Tooltip Stacks Singular:** -2 [img:dex], -2 [img:str], -2 [img:spd]. Lasts 1 turn.  
**Tooltip Stackless:** -2 [img:dex], -2 [img:str], -2 [img:spd], temporarily.  
**Source:** `keyword_tooltips.gon`  

```
Weakness {
    name "KEYWORD_WEAKNESS_NAME"
    tooltip_stacks "KEYWORD_WEAKNESS_DESC"
    tooltip_stacks_singular "KEYWORD_WEAKNESS_DESC_SINGULAR"
    tooltip_stackless "KEYWORD_WEAKNESS_DESC_STACKLESS"
}
```

---

### `DepressionAura`
**Alias:** `AllStatsUp`  
**Source:** `keyword_tooltips.gon`  

```
DepressionAura { 
    alias AllStatsUp
}
```

---

### `Webbed`
**Name:** Webbed  
**Tooltip:** Immobile. Use basic attack to break free.  
**Source:** `keyword_tooltips.gon`  

```
Webbed {
    name "KEYWORD_WEBBED_NAME"
    tooltip "KEYWORD_WEBBED_DESC"
}
```

---

### `Tangled`
**Name:** Entangled  
**Tooltip:** Immobile. Use basic attack to break free.  
**Source:** `keyword_tooltips.gon`  

```
Tangled {
    name "KEYWORD_TANGLED_NAME"
    tooltip "KEYWORD_TANGLED_DESC"
}
```

---

### `Wet`
**Name:** Wet  
**Tooltip:** Wet.  
**Source:** `keyword_tooltips.gon`  

```
Wet {
    name "KEYWORD_WET_NAME"
    tooltip "KEYWORD_WET_DESC"
}
```

---

### `Zombie`
**Name:** Zombie  
**Tooltip:** -2 [img:str]. -2 [img:int]. Takes damage from Holy Element heals. Does not get injured when downed.  
**Source:** `keyword_tooltips.gon`  

```
Zombie {
    name "KEYWORD_ZOMBIE_NAME"
    tooltip "KEYWORD_ZOMBIE_DESC"
}
```

---

### `Metal`
**Name:** Metal  
**Tooltip:** This item is electrically conductive.  
**Icon Frame:** `151`  
**Source:** `keyword_tooltips.gon`  

```
Metal {
    name "KEYWORD_METAL_NAME"
    tooltip "KEYWORD_METAL_DESC"

    icon_frame 151
}
```

---

### `Fragile`
**Name:** Fragile  
**Tooltip:** This item breaks when you're downed.  
**Icon Frame:** `149`  
**Source:** `keyword_tooltips.gon`  

```
Fragile {
    name "KEYWORD_FRAGILE_NAME"
    tooltip "KEYWORD_FRAGILE_DESC"

    icon_frame 149
}
```

---

### `FragileDuringElement`
**Alias:** `Fragile`  
**Source:** `keyword_tooltips.gon`  

```
FragileDuringElement {
    alias Fragile
}
```

---

### `Brittle`
**Name:** Brittle  
**Tooltip:** This item has a 25% chance to break when you take damage.  
**Icon Frame:** `150`  
**Source:** `keyword_tooltips.gon`  

```
Brittle {
    name "KEYWORD_BRITTLE_NAME"
    tooltip "KEYWORD_BRITTLE_DESC"

    icon_frame 150
}
```

---

### `BrittleDuringElement`
**Alias:** `Brittle`  
**Source:** `keyword_tooltips.gon`  

```
BrittleDuringElement {
    alias Brittle
}
```

---

### `Flammable`
**Name:** Flammable  
**Tooltip:** This item burns up when hit with fire.  
**Icon Frame:** `148`  
**Source:** `keyword_tooltips.gon`  

```
Flammable {
    name "KEYWORD_FLAMMABLE_NAME"
    tooltip "KEYWORD_FLAMMABLE_DESC"

    icon_frame 148
}
```

---

### `Cursed`
**Name:** Cursed  
**Tooltip:** This item cannot be unequipped once equipped.  
**Icon Frame:** `156`  
**Source:** `keyword_tooltips.gon`  

```
Cursed {
    name "KEYWORD_CURSED_NAME"
    tooltip "KEYWORD_CURSED_DESC"

    icon_frame 156
}
```

---

### `Reload`
**Name:** Reload  
**Tooltip:** This action starts disabled and does not refresh on its own after use. Meet the condition to refresh it.  
**Icon Frame:** `159`  
**Source:** `keyword_tooltips.gon`  

```
Reload {
    name "KEYWORD_RELOAD_NAME"
    tooltip "KEYWORD_RELOAD_DESC"

    icon_frame 159
}
```

---

### `ReloadB`
**Name:** Reload  
**Tooltip:** This action does not refresh on its own after use. Meet the condition to refresh it.  
**Icon Frame:** `159`  
**Source:** `keyword_tooltips.gon`  

```
ReloadB {
    name "KEYWORD_RELOAD_NAME"
    tooltip "KEYWORD_RELOADB_DESC"

    icon_frame 159
}
```

---

### `Flying`
**Name:** Flying  
**Tooltip:** Ignores tiles and can pass over units and objects.  
**Icon Frame:** `157`  
**Source:** `keyword_tooltips.gon`  

```
Flying {
    name "KEYWORD_FLYING_NAME"
    tooltip "KEYWORD_FLYING_DESC"

    icon_frame 157
}
```

---

### `Comfort`
**Name:** [img:comfort] Comfort  
**Tooltip:** Affects how often cats will breed or fight.  
**Source:** `keyword_tooltips.gon`  

```
Comfort {
    name "KEYWORD_COMFORT_NAME"
    tooltip "KEYWORD_COMFORT_DESC"
}
```

---

### `Stimulation`
**Name:** [img:stimulation] Stimulation  
**Tooltip:** Affects the quality of newborn kittens.  
**Source:** `keyword_tooltips.gon`  

```
Stimulation {
    name "KEYWORD_STIMULATION_NAME"
    tooltip "KEYWORD_STIMULATION_DESC"
}
```

---

### `Appeal`
**Name:** [img:appeal] Appeal  
**Tooltip:** Affects the quality of the stray cats that show up each day  
**Source:** `keyword_tooltips.gon`  

```
Appeal {
    name "KEYWORD_APPEAL_NAME"
    tooltip "KEYWORD_APPEAL_DESC"
}
```

---

### `Evolution`
**Name:** [img:evolution] Mutation  
**Tooltip:** Adds a chance for cats to receive random mutations each night.  
**Source:** `keyword_tooltips.gon`  

```
Evolution {
    name "KEYWORD_EVOLUTION_NAME"
    tooltip "KEYWORD_EVOLUTION_DESC"
}
```

---

### `Health`
**Name:** [img:health] Health  
**Tooltip:** Affects lifespan and chance to develop or cure disorders each night  
**Source:** `keyword_tooltips.gon`  

```
Health {
    name "KEYWORD_HEALTH_NAME"
    tooltip "KEYWORD_HEALTH_DESC"
}
```

---

### `DemonicGlyph_Bite`
**Name:** Lucifer Rune  
**Tooltip:** Imbues its owner with an extra turn and the power to Bite  
**Source:** `keyword_tooltips.gon`  

```
DemonicGlyph_Bite {
    name "KEYWORD_TOR_BITE_NAME"
    tooltip "KEYWORD_TOR_BITE_DESC"
}
```

---

### `DemonicGlyph_Fire`
**Name:** Brimstone Rune  
**Tooltip:** Imbues its owner's basic attack with +2 Damage and +2 Burn.  
**Source:** `keyword_tooltips.gon`  

```
DemonicGlyph_Fire {
    name "KEYWORD_TOR_FIRE_NAME"
    tooltip "KEYWORD_TOR_FIRE_DESC"
}
```

---

### `DemonicGlyph_Summon`
**Name:** Pentagram Rune  
**Tooltip:** Imbues its owner with an extra turn and the power to Summon  
**Source:** `keyword_tooltips.gon`  

```
DemonicGlyph_Summon {
    name "KEYWORD_TOR_SUMMON_NAME"
    tooltip "KEYWORD_TOR_SUMMON_DESC"
}
```

---

### `DemonicGlyph_Movement`
**Name:** Hexagram Rune  
**Tooltip:** Imbues its owner with +1 Movement Range and +3 Trample Damage  
**Source:** `keyword_tooltips.gon`  

```
DemonicGlyph_Movement {
    name "KEYWORD_TOR_MOVE_NAME"
    tooltip "KEYWORD_TOR_MOVE_DESC"
}
```

---

### `DemonicGlyph_Bounce`
**Name:** Chaos Rune  
**Tooltip:** Imbues its owner with the ability to repel attackers.  
**Source:** `keyword_tooltips.gon`  

```
DemonicGlyph_Bounce {
    name "KEYWORD_TOR_BOUNCE_NAME"
    tooltip "KEYWORD_TOR_BOUNCE_DESC"
}
```

---

### `FinalBossHitCountdownHoly`
**Name:** The Child's Flame  
**Tooltip:** Counts down every time it gets hit. At 0, unleash the holy beams.  
**Source:** `keyword_tooltips.gon`  

```
FinalBossHitCountdownHoly {
    name "KEYWORD_CHILDHOLY_NAME"
    tooltip "KEYWORD_CHILDHOLY_DESC"
}
```

---

### `FinalBossHitCountdownBoris`
**Name:** The Child's Flame  
**Tooltip:** Counts down every time it gets hit. At 0, releases a pulse.  
**Source:** `keyword_tooltips.gon`  

```
FinalBossHitCountdownBoris {
    name "KEYWORD_CHILDPULSE_NAME"
    tooltip "KEYWORD_CHILDPULSE_DESC"
}
```

---

### `FinalBossHitCountdownExplosive`
**Name:** The Child's Flame  
**Tooltip:** Counts down every time it gets hit. At 0, unleash a wrath of holy light.  
**Source:** `keyword_tooltips.gon`  

```
FinalBossHitCountdownExplosive {
    name "KEYWORD_CHILDWRATH_NAME"
    tooltip "KEYWORD_CHILDWRATH_DESC"
}
```

---

### `TVBotObey`
**Name:** OBEY  
**Tooltip:** Basic attacks of its enemies are disabled.  
**Icon Frame:** `155`  
**Source:** `keyword_tooltips.gon`  

```
TVBotObey {
    name "ENEMY_TVBOT_OBEY_NAME"
    tooltip "ENEMY_TVBOT_OBEY_DESC"

    icon_frame 155
}
```

---

### `TVBotStop`
**Name:** STOP  
**Tooltip:** Basic movement of its enemies is disabled.  
**Icon Frame:** `155`  
**Source:** `keyword_tooltips.gon`  

```
TVBotStop {
    name "ENEMY_TVBOT_STOP_NAME"
    tooltip "ENEMY_TVBOT_STOP_DESC"

    icon_frame 155
}
```

---

### `TVBotDumb`
**Name:** DUMB  
**Tooltip:** Spells of its enemies are disabled.  
**Icon Frame:** `155`  
**Source:** `keyword_tooltips.gon`  

```
TVBotDumb {
    name "ENEMY_TVBOT_DUMB_NAME"
    tooltip "ENEMY_TVBOT_DUMB_DESC"

    icon_frame 155
}
```

---

### `TVBotDie`
**Name:** DIE  
**Tooltip:** It is too late. Win now or die.  
**Icon Frame:** `155`  
**Source:** `keyword_tooltips.gon`  

```
TVBotDie {
    name "ENEMY_TVBOT_DIE_NAME"
    tooltip "ENEMY_TVBOT_DIE_DESC"

    icon_frame 155
}
```

---

### `EliteBuff_Spiky`
**Name:** Elite Buff: Spiky  
**Tooltip:** +2 Thorns  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Spiky {
    name "KEYWORD_ELITE_SPIKY_NAME"
    tooltip "KEYWORD_ELITE_SPIKY_DESC"
}
```

---

### `EliteBuff_BossSpiky`
**Name:** Elite Buff: Spiky  
**Tooltip:** +1 Thorns  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossSpiky {
    name "KEYWORD_ELITE_BOSSSPIKY_NAME"
    tooltip "KEYWORD_ELITE_BOSSSPIKY_DESC"
}
```

---

### `EliteBuff_Reactive`
**Name:** Elite Buff: Reactive  
**Tooltip:** +1 Kinetic Spikes  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Reactive {
    name "KEYWORD_ELITE_REACTIVE_NAME"
    tooltip "KEYWORD_ELITE_REACTIVE_DESC"
}
```

---

### `EliteBuff_BossReactive`
**Alias:** `EliteBuff_Reactive`  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossReactive {
    alias EliteBuff_Reactive
}
```

---

### `EliteBuff_Damaging`
**Name:** Elite Buff: Damaging  
**Tooltip:** +2 Damage  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Damaging {
    name "KEYWORD_ELITE_DAMAGING_NAME"
    tooltip "KEYWORD_ELITE_DAMAGING_DESC"
}
```

---

### `EliteBuff_BossDamaging`
**Alias:** `EliteBuff_Damaging`  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossDamaging {
    alias EliteBuff_Damaging
}
```

---

### `EliteBuff_Tough`
**Name:** Elite Buff: Tough  
**Tooltip:** +2 Brace  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Tough {
    name "KEYWORD_ELITE_TOUGH_NAME"
    tooltip "KEYWORD_ELITE_TOUGH_DESC"
}
```

---

### `EliteBuff_BossTough`
**Name:** Elite Buff: Tough  
**Tooltip:** +1 Brace  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossTough {
    name "KEYWORD_ELITE_BOSSTOUGH_NAME"
    tooltip "KEYWORD_ELITE_BOSSTOUGH_DESC"
}
```

---

### `EliteBuff_Shielded1`
**Name:** Elite Buff: Shielded  
**Tooltip:** At the start of each round, if it has less than 3 [img:shield], set [img:shield] to 3. -20% max health.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Shielded1 {
    name "KEYWORD_ELITE_SHIELDED1_NAME"
    tooltip "KEYWORD_ELITE_SHIELDED1_DESC"
}
```

---

### `EliteBuff_BossShielded1`
**Name:** Elite Buff: Shielded  
**Tooltip:** At the start of each round, if it has less than 4 [img:shield], set [img:shield] to 4. -20% max health.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossShielded1 {
    name "KEYWORD_ELITE_BOSSSHIELDED1_NAME"
    tooltip "KEYWORD_ELITE_BOSSSHIELDED1_DESC"
}
```

---

### `EliteBuff_Shielded2`
**Name:** Elite Buff: Shielded  
**Tooltip:** At the start of each round, if it has less than 5 [img:shield], set [img:shield] to 5. -20% max health.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Shielded2 {
    name "KEYWORD_ELITE_SHIELDED2_NAME"
    tooltip "KEYWORD_ELITE_SHIELDED2_DESC"
}
```

---

### `EliteBuff_BossShielded2`
**Name:** Elite Buff: Shielded  
**Tooltip:** At the start of each round, if it has less than 8 [img:shield], set [img:shield] to 8. -20% max health.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossShielded2 {
    name "KEYWORD_ELITE_BOSSSHIELDED2_NAME"
    tooltip "KEYWORD_ELITE_BOSSSHIELDED2_DESC"
}
```

---

### `EliteBuff_Shielded3`
**Name:** Elite Buff: Shielded  
**Tooltip:** At the start of each round, if it has less than 7 [img:shield], set [img:shield] to 7. -20% max health.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Shielded3 {
    name "KEYWORD_ELITE_SHIELDED3_NAME"
    tooltip "KEYWORD_ELITE_SHIELDED3_DESC"
}
```

---

### `EliteBuff_BossShielded3`
**Name:** Elite Buff: Shielded  
**Tooltip:** At the start of each round, if it has less than 12 [img:shield], set [img:shield] to 12. -20% max health.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossShielded3 {
    name "KEYWORD_ELITE_BOSSSHIELDED3_NAME"
    tooltip "KEYWORD_ELITE_BOSSSHIELDED3_DESC"
}
```

---

### `EliteBuff_Shielded4`
**Name:** Elite Buff: Shielded  
**Tooltip:** At the start of each round, if it has less than 9 [img:shield], set [img:shield] to 9. -20% max health.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Shielded4 {
    name "KEYWORD_ELITE_SHIELDED4_NAME"
    tooltip "KEYWORD_ELITE_SHIELDED4_DESC"
}
```

---

### `EliteBuff_BossShielded4`
**Name:** Elite Buff: Shielded  
**Tooltip:** At the start of each round, if it has less than 16 [img:shield], set [img:shield] to 16. -20% max health.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossShielded4 {
    name "KEYWORD_ELITE_BOSSSHIELDED4_NAME"
    tooltip "KEYWORD_ELITE_BOSSSHIELDED4_DESC"
}
```

---

### `EliteBuff_Protected`
**Name:** Elite Buff: Protected  
**Tooltip:** At the end of each turn, set [img:divineshield] to 1 if it had no [img:divineshield]. -20% max health.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Protected {
    name "KEYWORD_ELITE_PROTECTED_NAME"
    tooltip "KEYWORD_ELITE_PROTECTED_DESC"
}
```

---

### `EliteBuff_BossProtected`
**Alias:** `EliteBuff_Protected`  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossProtected {
    alias EliteBuff_Protected
}
```

---

### `EliteBuff_Speedy`
**Name:** Elite Buff: Speedy  
**Tooltip:** +4 [img:spd]  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Speedy {
    name "KEYWORD_ELITE_SPEEDY_NAME"
    tooltip "KEYWORD_ELITE_SPEEDY_DESC"
}
```

---

### `EliteBuff_BossSpeedy`
**Alias:** `EliteBuff_Speedy`  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossSpeedy {
    alias EliteBuff_Speedy
}
```

---

### `EliteBuff_Flaming`
**Name:** Elite Buff: Flaming  
**Tooltip:** Fire Immune. Leaves a trail of fire.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Flaming {
    name "KEYWORD_ELITE_FLAMING_NAME"
    tooltip "KEYWORD_ELITE_FLAMING_DESC"
}
```

---

### `EliteBuff_BossFlaming`
**Name:** Elite Buff: Flaming  
**Tooltip:** Fire Immune. Leaves a trail of fire. Applies Burn 1 to attackers.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossFlaming {
    name "KEYWORD_ELITE_BOSSFLAMING_NAME"
    tooltip "KEYWORD_ELITE_BOSSFLAMING_DESC"
}
```

---

### `EliteBuff_Creepy`
**Name:** Elite Buff: Creepy  
**Tooltip:** Basic attack inflicts Poison. Leaves a trail of creep.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Creepy {
    name "KEYWORD_ELITE_CREEPY_NAME"
    tooltip "KEYWORD_ELITE_CREEPY_DESC"
}
```

---

### `EliteBuff_Lucky`
**Name:** Elite Buff: Lucky  
**Tooltip:** +3 [img:lck]. +10% Crit Chance. +10% Dodge Chance.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Lucky {
    name "KEYWORD_ELITE_LUCKY_NAME"
    tooltip "KEYWORD_ELITE_LUCKY_DESC"
}
```

---

### `EliteBuff_BossLucky`
**Alias:** `EliteBuff_Lucky`  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossLucky {
    alias EliteBuff_Lucky
}
```

---

### `EliteBuff_Static`
**Name:** Elite Buff: Static  
**Tooltip:** Arcs 1 electric damage to neighbors whenever it moves.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Static {
    name "KEYWORD_ELITE_STATIC_NAME"
    tooltip "KEYWORD_ELITE_STATIC_DESC"
}
```

---

### `EliteBuff_BossStatic`
**Alias:** `EliteBuff_Static`  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossStatic {
    alias EliteBuff_Static
}
```

---

### `EliteBuff_Bouncy`
**Name:** Elite Buff: Bouncy  
**Tooltip:** When hit, bounces itself and its attacker apart.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Bouncy {
    name "KEYWORD_ELITE_BOUNCY_NAME"
    tooltip "KEYWORD_ELITE_BOUNCY_DESC"
}
```

---

### `EliteBuff_BossBouncy`
**Alias:** `EliteBuff_Bouncy`  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossBouncy {
    alias EliteBuff_Bouncy
}
```

---

### `EliteBuff_Mirror`
**Name:** Elite Buff: Mirror  
**Tooltip:** Reflects all projectiles. Takes 2 damage when it reflects a projectile.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Mirror {
    name "KEYWORD_ELITE_MIRROR_NAME"
    tooltip "KEYWORD_ELITE_MIRROR_DESC"
}
```

---

### `EliteBuff_Resonant`
**Name:** Elite Buff: Resonant  
**Tooltip:** Whenever an enemy casts a spell, gain All Stats Up 1 and heal 1.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Resonant {
    name "KEYWORD_ELITE_RESONANT_NAME"
    tooltip "KEYWORD_ELITE_RESONANT_DESC"
}
```

---

### `EliteBuff_Undying`
**Name:** Elite Buff: Undying  
**Tooltip:** Revives to 50% health at the end of the round. +2 Corpse Health.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Undying {
    name "KEYWORD_ELITE_UNDYING_NAME"
    tooltip "KEYWORD_ELITE_UNDYING_DESC"
}
```

---

### `EliteBuff_SubUndying`
**Name:** Elite Buff: Undying  
**Tooltip:** Revives to 50% health at the end of the round.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_SubUndying {
    name "KEYWORD_ELITE_SUBUNDYING_NAME"
    tooltip "KEYWORD_ELITE_SUBUNDYING_DESC"
}
```

---

### `EliteBuff_Healthy`
**Name:** Elite Buff: Healthy  
**Tooltip:** +3 Health Regen. +20 unfilled max health.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Healthy {
    name "KEYWORD_ELITE_HEALTHY_NAME"
    tooltip "KEYWORD_ELITE_HEALTHY_DESC"
}
```

---

### `EliteBuff_Sandy`
**Name:** Elite Buff: Sandy  
**Tooltip:** +10% Dodge Chance. Starts a sandstorm when it dies.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Sandy {
    name "KEYWORD_ELITE_SANDY_NAME"
    tooltip "KEYWORD_ELITE_SANDY_DESC"
}
```

---

### `EliteBuff_Infested`
**Name:** Elite Buff: Infested  
**Tooltip:** Spawns a fly swarm when it dies.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Infested {
    name "KEYWORD_ELITE_INFESTED_NAME"
    tooltip "KEYWORD_ELITE_INFESTED_DESC"
}
```

---

### `EliteBuff_Absorbant`
**Name:** Elite Buff: Absorbent  
**Tooltip:** Drains all unused mana from units when they end their turn, and deals damage to them equal to the amount of mana drained.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Absorbant {
    name "KEYWORD_ELITE_ABSORBANT_NAME"
    tooltip "KEYWORD_ELITE_ABSORBANT_DESC"
}
```

---

### `EliteBuff_BossAbsorbant`
**Alias:** `EliteBuff_Absorbant`  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossAbsorbant {
    alias EliteBuff_Absorbant
}
```

---

### `EliteBuff_Depressing`
**Name:** Elite Buff: Depressing  
**Tooltip:** While alive, its enemies have -1 to all stats.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Depressing {
    name "KEYWORD_ELITE_DEPRESSING_NAME"
    tooltip "KEYWORD_ELITE_DEPRESSING_DESC"
}
```

---

### `EliteBuff_BossDepressing`
**Alias:** `EliteBuff_Depressing`  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossDepressing {
    alias EliteBuff_Depressing
}
```

---

### `EliteBuff_SlightlyDepressing`
**Name:** Elite Buff: Slightly Depressing  
**Tooltip:** While alive, adjacent enemies have -1 to all stats.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_SlightlyDepressing {
    name "KEYWORD_ELITE_SLIGHTLYDEPRESSING_NAME"
    tooltip "KEYWORD_ELITE_SLIGHTLYDEPRESSING_DESC"
}
```

---

### `EliteBuff_BossSlightlyDepressing`
**Alias:** `EliteBuff_SlightlyDepressing`  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossSlightlyDepressing {
    alias EliteBuff_SlightlyDepressing
}
```

---

### `EliteBuff_Evolving`
**Name:** Elite Buff: Evolving  
**Tooltip:** At the end of each round, gain a random Elite Buff.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Evolving {
    name "KEYWORD_ELITE_EVOLVING_NAME"
    tooltip "KEYWORD_ELITE_EVOLVING_DESC"
}
```

---

### `EliteBuff_Plow`
**Name:** Elite Buff: Plow  
**Tooltip:** Trample. Moves one space towards attackers when damaged.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Plow {
    name "KEYWORD_ELITE_PLOW_NAME"
    tooltip "KEYWORD_ELITE_PLOW_DESC"
}
```

---

### `EliteBuff_Mega`
**Name:** Elite Buff: Mega  
**Tooltip:** Takes one less turn per round. +50% health and damage  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Mega {
    name "KEYWORD_ELITE_MEGA_NAME"
    tooltip "KEYWORD_ELITE_MEGA_DESC"
}
```

---

### `EliteBuff_Mad`
**Name:** Elite Buff: Mad  
**Tooltip:** Madness. Takes an extra turn per round. Gains +1 all stats and heals 4 when it gets a kill.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Mad {
    name "KEYWORD_ELITE_MAD_NAME"
    tooltip "KEYWORD_ELITE_MAD_DESC"
}
```

---

### `EliteBuff_BossMad`
**Name:** Elite Buff: Mad  
**Tooltip:** Madness. Gains +1 all stats and heals 4 when it gets a kill.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossMad {
    name "KEYWORD_ELITE_BOSSMAD_NAME"
    tooltip "KEYWORD_ELITE_BOSSMAD_DESC"
}
```

---

### `EliteBuff_Twin`
**Name:** Elite Buff: Twin  
**Tooltip:** Half health. Comes with a twin.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Twin {
    name "KEYWORD_ELITE_TWIN_NAME"
    tooltip "KEYWORD_ELITE_TWIN_DESC"
}
```

---

### `EliteBuff_BossTwin`
**Alias:** `EliteBuff_Twin`  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossTwin {
    alias EliteBuff_Twin
}
```

---

### `EliteBuff_SubTwin`
**Alias:** `EliteBuff_Twin`  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_SubTwin {
    alias EliteBuff_Twin
}
```

---

### `EliteBuff_BossSubTwin`
**Alias:** `EliteBuff_Twin`  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossSubTwin {
    alias EliteBuff_Twin
}
```

---

### `EliteBuff_Hardy`
**Name:** Elite Buff: Hardy  
**Tooltip:** Immune to stuns.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Hardy {
    name "KEYWORD_ELITE_HARDY_NAME"
    tooltip "KEYWORD_ELITE_HARDY_DESC"
}
```

---

### `EliteBuff_BossHardy`
**Alias:** `EliteBuff_Hardy`  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossHardy {
    alias EliteBuff_Hardy
}
```

---

### `EliteBuff_Sticky`
**Name:** Elite Buff: Sticky  
**Tooltip:** Anything that contacts or attacks this gets Tarred 1.  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_Sticky {
    name "KEYWORD_ELITE_STICKY_NAME"
    tooltip "KEYWORD_ELITE_STICKY_DESC"
}
```

---

### `EliteBuff_BossSticky`
**Alias:** `EliteBuff_Sticky`  
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossSticky {
    alias EliteBuff_Sticky
}
```

---

