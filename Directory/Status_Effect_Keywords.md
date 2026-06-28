# Status Effect Keywords Directory

## File: `keyword_tooltips.gon`

### `Adrenaline`
**Name:** Adrenaline  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ADRENALINE_DESC`: "Keeps Exhaustion at 0. <br/> +25% Crit Chance. <br/> +25% Block Chance."

```
Adrenaline {
    name "KEYWORD_ADRENALINE_NAME"
    tooltip "KEYWORD_ADRENALINE_DESC"
}
```

---

### `AllStatsUp`
**Name:** All Stats Up  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ALLSTATSDOWN_NAME`: "All Stats Down"
- `KEYWORD_ALLSTATSUP_DESC`: "All Stats increased by {stacks}"
- `KEYWORD_ALLSTATSDOWN_DESC`: "All Stats decreased by {absstacks}"

```
AllStatsUp {
    name "KEYWORD_ALLSTATSUP_NAME"
    name_stacks_neg "KEYWORD_ALLSTATSDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_ALLSTATSUP_DESC"
    tooltip_stacks_neg "KEYWORD_ALLSTATSDOWN_DESC"

    tooltip_stackless none
    //tooltip_stackless_pos "Increases all primary stats. \n([img:str] [img:dex] [img:con] [img:int] [img:cha] [img:spd] [img:lck])."
    //tooltip_stackless_neg "Decreases all primary stats. \n([img:str] [img:dex] [img:con] [img:int] [img:cha] [img:spd] [img:lck])."
}
```

---

### `AlphaAllStatsUp`
**Source:** `keyword_tooltips.gon`  

```
AlphaAllStatsUp {
    alias AllStatsUp
}
```

---

### `AlphaDodgeChance`
**Source:** `keyword_tooltips.gon`  

```
AlphaDodgeChance {
    alias DodgeChance_Status
}
```

---

### `AlphaCat`
**Name:** The Alpha  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ALPHA_DESC`: "This is the Alpha. Certain abilities care about this."
- `KEYWORD_ALPHA_DESC_STACKLESS`: "No effects on its own. Only one unit can be The Alpha. Certain spells and abilities provide bonuses for The Alpha."

```
AlphaCat {
    name "KEYWORD_ALPHA_NAME"
    tooltip "KEYWORD_ALPHA_DESC"
    tooltip_stackless "KEYWORD_ALPHA_DESC_STACKLESS"
}
```

---

### `AllyDodgeChanceAura`
**Source:** `keyword_tooltips.gon`  

```
AllyDodgeChanceAura {
    alias DodgeChance_Status
}
```

---

### `LowHealthAllyDodgeChanceAura`
**Source:** `keyword_tooltips.gon`  

```
LowHealthAllyDodgeChanceAura {
    alias DodgeChance_Status
}
```

---

### `AllyInfested`
**Source:** `keyword_tooltips.gon`  

```
AllyInfested {
    alias Infested
}
```

---

### `Ammo`
**Name:** Ammo  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_AMMO_DESC`: "{stacks} shots left."
- `KEYWORD_AMMO_DESC_STACKLESS`: "Certain abilities require ammo to use."

```
Ammo { //used for Zodiac miniboss (+a few others) to show how many rounds are left in his gun
    name "KEYWORD_AMMO_NAME"
    tooltip_stacks "KEYWORD_AMMO_DESC"
    tooltip_stackless none //tooltip_stackless "KEYWORD_AMMO_DESC_STACKLESS"
}
```

---

### `Attraction`
**Name:** Attraction  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ATTRACTION_REF`: "Attraction"
- `KEYWORD_ATTRACTION_DESC`: "The thing attracting you is gone. Does nothing."
- `KEYWORD_ATTRACTION_DESC_REF`: "Moves towards {applier} at the start of its turn."
- `KEYWORD_ATTRACTION_DESC_STACKLESS`: "Moves towards you at the start of its turn."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BACKFLIP_DESC`: "Backflips out of the way the next time it's targeted."

```
BackflipWhenTargeted {
    name "KEYWORD_BACKFLIP_NAME"
    tooltip "KEYWORD_BACKFLIP_DESC"
}
```

---

### `BlastResistance`
**Name:** Blast Resistance  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BLASTRESISTANCE_DESC`: "Takes {stacks} less damage from explosions."
- `KEYWORD_BLASTRESISTANCE_DESC_STACKLESS`: "Reduces damage taken from explosions."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BLEED_DESC`: "Takes {stacks} damage at the end of the round, then increase Bleed by 1."
- `KEYWORD_BLEED_DESC_STACKLESS`: "Takes damage at the end of the round, then increase Bleed by 1."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BLEEDTHORNS_DESC`: "Deals {stacks} damage and inflicts Bleed {stacks} to units that contact you."
- `KEYWORD_BLEEDTHORNS_DESC_STACKLESS`: "Deals damage and inflicts Bleed to units that contact you."

```
BleedThorns { //todo: does this need to trigger a tooltip for Bleed?
    name "KEYWORD_BLEEDTHORNS_NAME"
    tooltip_stacks "KEYWORD_BLEEDTHORNS_DESC"

    tooltip_stackless "KEYWORD_BLEEDTHORNS_DESC_STACKLESS"
}
```

---

### `BlessingOfPeace`
**Name:** Blessing of Peace  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BLESSINGOFPEACE_DESC`: "Gain +{stacks} [img:divineshield] at the end of your turn. Lose this when you deal damage."
- `KEYWORD_BLESSINGOFPEACE_DESC_STACKLESS`: "Gain [img:divineshield] at the end of your turn. Lose this when you deal damage."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BLIND_DESC`: "30% miss chance for the next {stacks} turns."
- `KEYWORD_BLIND_DESC_STACKLESS`: "30% miss chance for the next turn."
- `KEYWORD_PERMABLIND_DESC`: "30% miss chance."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BLOODZERK_DESC`: "When you deal health damage to a bleeding unit, heal that much health."

```
Bloodzerked {
    name "KEYWORD_BLOODZERK_NAME"
    tooltip_stacks "KEYWORD_BLOODZERK_DESC"
}
```

---

### `Blur`
**Source:** `keyword_tooltips.gon`  

```
Blur {
    alias DodgeChance_Status
}
```

---

### `BodyGuard`
**Name:** Body Guard  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BODYGUARD_DESC`: "The next time an ally is targeted, swap places with them first."

```
BodyGuard {
    name "KEYWORD_BODYGUARD_NAME"
    tooltip "KEYWORD_BODYGUARD_DESC"
}
```

---

### `BoostDamageAura`
**Source:** `keyword_tooltips.gon`  

```
BoostDamageAura {
    alias DamageUp
}
```

---

### `BoostDamageGlobalAura`
**Source:** `keyword_tooltips.gon`  

```
BoostDamageGlobalAura {
    alias DamageUp
}
```

---

### `Bounty`
**Name:** Bounty  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BOUNTY_DESC`: "Takes 25% extra damage. If killed, gain {stacks} coins."
- `KEYWORD_BOUNTY_DESC_STACKLESS`: "Takes 25% extra damage. If killed, gain coins."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BRACE_DESC`: "Takes {stacks} less damage from all sources."
- `KEYWORD_BRACE_DESC_STACKLESS`: "Reduces all incoming damage."

```
Brace {
    name "KEYWORD_BRACE_NAME"
    tooltip_stacks "KEYWORD_BRACE_DESC"
    tooltip_stackless "KEYWORD_BRACE_DESC_STACKLESS"
}
```

---

### `BraceForEachNeighboringEnemy`
**Source:** `keyword_tooltips.gon`  

```
BraceForEachNeighboringEnemy {
    alias Brace
}
```

---

### `Bruise`
**Name:** Bruise  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BRUISE_DESC`: "Takes {stacks} more damage from physical sources."
- `KEYWORD_BRUISE_DESC_STACKLESS`: "Increases all incoming physical damage."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BURN_DESC`: "Takes {stacks} damage at start of its turn, then decrease Burn by 1."
- `KEYWORD_BURN_DESC_STACKLESS`: "Takes damage at start of its turn, then decrease Burn by 1."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_PROMOTE_DESC`: "The next familiar you spawn is upgraded into a [img:champion] Champion."

```
ChampionUpgradeNextMinion {
    name "KEYWORD_PROMOTE_NAME"
    tooltip "KEYWORD_PROMOTE_DESC"
}
```

---

### `EliteUpgradeNextMinion`
**Name:** Promote+  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_PROMOTE2_DESC`: "The next familiar you spawn is upgraded into an [img:elite] Elite."

```
EliteUpgradeNextMinion {
    name "KEYWORD_PROMOTE2_NAME"
    tooltip "KEYWORD_PROMOTE2_DESC"
}
```

---

### `Charge`
**Name:** Charge  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_CHARGE_DESC`: "Gains {stacks} mana at the start of its next turn."
- `KEYWORD_CHARGE_DESC_STACKLESS`: "Gains mana at the start of its next turn."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_CHARGEFISTS_DESC`: "Your basic attack emits {stacks} Sparkles until the end of the turn."
- `KEYWORD_CHARGEFISTS_DESC_SINGULAR`: "Your basic attack emits a Sparkle until the end of the turn."
- `KEYWORD_CHARGEFISTS_DESC_STACKLESS`: "Your basic attack emits Sparkles until the end of the turn."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_CHADOWN_NAME`: "Charisma Down"
- `KEYWORD_CHAUP_DESC`: "Charisma increased by {stacks}. <br/> Charisma affects max mana and initial mana."
- `KEYWORD_CHADOWN_DESC`: "Charisma decreased by {absstacks}. <br/> Charisma affects max mana and initial mana."

```
CharismaUp {
    name "KEYWORD_CHAUP_NAME"
    name_stacks_neg "KEYWORD_CHADOWN_NAME"
    tooltip_stacks_pos "KEYWORD_CHAUP_DESC"
    tooltip_stacks_neg "KEYWORD_CHADOWN_DESC"

    tooltip_stackless none //tooltip_stackless "Charisma affects max mana and initial mana."
}
```

---

### `CharmAllFlies`
**Source:** `keyword_tooltips.gon`  

```
CharmAllFlies {
    alias Charmed
}
```

---

### `Charmed`
**Name:** Charmed  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_CHARMED_DESC`: "It's brainwashed!"
- `KEYWORD_CHARMED_DESC_STACKLESS`: "Behaves as if it's on your team."

```
Charmed { //tooltip is weird because allies can be charmed by enemies, so what it really does depends on who charmed it
    name "KEYWORD_CHARMED_NAME"
    tooltip "KEYWORD_CHARMED_DESC"

    tooltip_stackless "KEYWORD_CHARMED_DESC_STACKLESS"
}
```

---

### `Cleave`
**Name:** Cleave  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_CLEAVE_DESC`: "Cuts a chunk of meat off what it hits."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_PROBED_DESC`: "It's being controlled! Attack it to break the probe!"
- `KEYWORD_PROBED_DESC_STACKLESS`: "Behaves as if it's on your team. Attacks from allies will break the probe."

```
ProbeCharmed { //tooltip is weird because allies can be charmed by enemies, so what it really does depends on who charmed it
    name "KEYWORD_PROBED_NAME"
    tooltip "KEYWORD_PROBED_DESC" //NOTE: only allies will break the probe if attacking it

    tooltip_stackless "KEYWORD_PROBED_DESC_STACKLESS"
}
```

---

### `Confusion`
**Name:** Confusion  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_CONFUSION_DESC`: "When performing an action, 33% chance to instead hit itself equal to its strength. Lasts {stacks} turns."
- `KEYWORD_CONFUSION_DESC_STACKLESS`: "When performing an action, 33% chance to instead hit itself equal to its strength."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_CONFUSION_DESC_STACKLESS`: "When performing an action, 33% chance to instead hit itself equal to its strength."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_CONDOWN_NAME`: "Constitution Down"
- `KEYWORD_CONUP_DESC`: "Constitution increased by {stacks}. <br/> Constitution affects max health and post-battle health regen."
- `KEYWORD_CONDOWN_DESC`: "Constitution decreased by {absstacks}. <br/> Constitution affects max health and post-battle health regen."

```
ConstitutionUp {
    name "KEYWORD_CONUP_NAME"
    name_stacks_neg "KEYWORD_CONDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_CONUP_DESC"
    tooltip_stacks_neg "KEYWORD_CONDOWN_DESC"

    tooltip_stackless none //tooltip_stackless "Constitution affects max health and post-combat health regen."
}
```

---

### `CounterNextAttacks`
**Name:** Counter Attack  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_COUNTER_DESC`: "Attack the next thing that damages you automatically."
- `KEYWORD_COUNTER_DESC_STACKS`: "Attack the next {stacks} things that damage you automatically."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_CRITCHANCE_DESC`: "Crit Chance increased by {stacks}%"

```
CritChanceUp {
    name "KEYWORD_CRITCHANCE_NAME"
    tooltip_stacks "KEYWORD_CRITCHANCE_DESC"

    tooltip_stackless none //tooltip_stackless "Adds Critical Hit chance to physical attacks and spells. Critical hits deal +100% damage."
}
```

---

### `DamageReductionAura`
**Source:** `keyword_tooltips.gon`  

```
DamageReductionAura {
    alias Brace
}
```

---

### `DamageUp`
**Name:** Damage Up  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_DAMAGEDOWN_NAME`: "Damage Down"
- `KEYWORD_DAMAGEUP_DESC`: "Basic attack damage increased by {stacks}."
- `KEYWORD_DAMAGEDOWN_DESC`: "Basic attack damage decreased by {absstacks}."
- `KEYWORD_DAMAGEUP_DESC_STACKLESS`: "Increases the damage (or heal) of its basic attack."
- `KEYWORD_DAMAGEDOWN_DESC_STACKLESS`: "Decreases the damage (or heal) of its basic attack."

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

### `DelayedPain`
**Name:** Delayed Pain  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_DELAYEDPAIN_DESC`: "Takes {stacks} damage at the end of its turn."
- `KEYWORD_DELAYEDPAIN_DESC_STACKLESS`: "Delayed damage is taken all at once at the end of your turn."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_DEXDOWN_NAME`: "Dexterity Down"
- `KEYWORD_DEXUP_DESC`: "Dexterity increased by {stacks}. <br/> Dexterity affects ranged attack and ranged ability damage."
- `KEYWORD_DEXDOWN_DESC`: "Dexterity decreased by {absstacks}. <br/> Dexterity affects ranged attack and ranged ability damage."

```
DexterityUp {
    name "KEYWORD_DEXUP_NAME"
    name_stacks_neg "KEYWORD_DEXDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_DEXUP_DESC"
    tooltip_stacks_neg "KEYWORD_DEXDOWN_DESC"

    tooltip_stackless none //tooltip_stackless "Dexterity affects ranged attack and ranged ability damage."
}
```

---

### `DiminishingHealthRegen`
**Name:** Health Regen (Diminishing)  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_DIMINISHREGEN_DESC`: "Regen {stacks} health at the end of its turn, then decreases Health Regen by 1."
- `KEYWORD_DIMINISHREGEN_DESC_STACKLESS`: "Regen health at the end of its turn, then decreases Health Regen by 1."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_DIVINESHIELD_DESC`: "Blocks an entire instance of incoming damage."

```
DivineShield {
    name "KEYWORD_DIVINESHIELD_NAME"
    tooltip "KEYWORD_DIVINESHIELD_DESC"

    icon_frame 141
}
```

---

### `divine_shield`
**Source:** `keyword_tooltips.gon`  

```
divine_shield {
    alias DivineShield
}
```

---

### `NonStackingDivineShield`
**Source:** `keyword_tooltips.gon`  

```
NonStackingDivineShield {
    alias DivineShield
}
```

---

### `Dodge`
**Name:** Dodge  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_DODGE_DESC`: "Dodges the next {stacks} attacks."
- `KEYWORD_DODGE_DESC_STACKLESS`: "Dodges the next attack."

```
Dodge { //when I say 'attacks' I mean 'attacks or abilities'
    name "KEYWORD_DODGE_NAME"
    tooltip_stacks "KEYWORD_DODGE_DESC"

    tooltip_stackless "KEYWORD_DODGE_DESC_STACKLESS"
}
```

---

### `DodgeChance_Status`
**Name:** Dodge Chance  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_DODGECHANCE_DESC`: "Dodge Chance increased by {stacks}%."

```
DodgeChance_Status {
    name "KEYWORD_DODGECHANCE_NAME"
    tooltip_stacks "KEYWORD_DODGECHANCE_DESC"

    tooltip_stackless none //tooltip_stackless "Increases Dodge Chance."
}
```

---

### `Doomed`
**Name:** Doomed  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_DOOMED_DESC`: "Ticks down at the end of your turn. When it hits 0, Die."

```
Doomed {
    name "KEYWORD_DOOMED_NAME"
    tooltip "KEYWORD_DOOMED_DESC" //would need an alt for if stacks is 1 (turns plural) so just write like this in cases like that I guess
}
```

---

### `DoubleCast`
**Name:** Double Action  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_DOUBLECAST_DESC`: "The next ability you use is used an additional time for free."

```
DoubleCast { //TODO: this one actually double casts attacks and items too, "DoubleCastSpellThisTurn" is used when only spells. this ability is actually cut tho
    name "KEYWORD_DOUBLECAST_NAME"
    tooltip "KEYWORD_DOUBLECAST_DESC"
}
```

---

### `DoubleCastSpell`
**Name:** Double Cast  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_DOUBLECASTSPELL_DESC`: "The next spell you cast is cast an additional time for free."

```
DoubleCastSpell {
    name "KEYWORD_DOUBLECASTSPELL_NAME"
    tooltip "KEYWORD_DOUBLECASTSPELL_DESC"
}
```

---

### `DoubleCastSpellThisTurn`
**Name:** Double Cast (This Turn)  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_DOUBLECASTTHISTURN_DESC`: "The next spell you cast this turn is cast an additional time for free."

```
DoubleCastSpellThisTurn {
    name "KEYWORD_DOUBLECASTTHISTURN_NAME"
    tooltip "KEYWORD_DOUBLECASTTHISTURN_DESC"
}
```

---

### `Drowsy`
**Name:** Drowsy  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_DROWSY_DESC`: "Falls asleep at the end of its turn."

```
Drowsy {
    name "KEYWORD_DROWSY_NAME"
    tooltip "KEYWORD_DROWSY_DESC"
}
```

---

### `DybbukPossessed`
**Name:** Possessed by Dybbuk  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_DYBBUKED_DESC`: "This cat is possessed by Dybbuk. Down this cat to exorcise him."

```
DybbukPossessed {
    name "KEYWORD_DYBBUKED_NAME"
    tooltip "KEYWORD_DYBBUKED_DESC"
}
```

---

### `EmptyMind`
**Name:** Empty Mind  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_EMPTYMIND_DESC`: "Spells are disabled. Whenever it gets a kill, it takes an extra turn."

```
EmptyMind {
    name "KEYWORD_EMPTYMIND_NAME"
    tooltip "KEYWORD_EMPTYMIND_DESC"
}
```

---

### `Enrage`
**Name:** Enrage  
**Source:** `keyword_tooltips.gon`  

```
Enrage { //currently cut
    name "Enrage"
    tooltip None
}
```

---

### `EventBounty`
**Name:** Bounty  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_EVENTBOUNTY_DESC`: "Hunted by the bounty hunter."

```
EventBounty {
    name "KEYWORD_EVENTBOUNTY_NAME"
    tooltip_stacks "KEYWORD_EVENTBOUNTY_DESC"
}
```

---

### `Exhaustion`
**Name:** Exhaustion  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_EXHAUSTION_DESC`: "Takes {stacks} unblockable damage at the start of its turn, then increase Exhaustion by 1. Whenever it would gain mana or health, gain {stacks} less mana or health. Combat regen disabled. Cannot be removed. It's time to finish the fight."
- `KEYWORD_EXHAUSTION_DESC_STACKLESS`: "Takes unblockable damage at the start of its turn, then increase Exhaustion by 1. Decreases mana and health gain. Combat regen disabled."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_EXTRAATTACK_DESC`: "Can attack {stacks} extra times each turn."

```
ExtraBasicAttacks_Status {
    name "KEYWORD_EXTRAATTACK_NAME"
    tooltip_stacks "KEYWORD_EXTRAATTACK_DESC"
    tooltip_stackless none //tooltip_stacks_singular "Can attack an extra time each turn"
}
```

---

### `ExtraBasicMoves_Status`
**Name:** Extra Moves  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_EXTRAMOVE_DESC`: "Can move {stacks} extra times each turn."

```
ExtraBasicMoves_Status {
    name "KEYWORD_EXTRAMOVE_NAME"
    tooltip_stacks "KEYWORD_EXTRAMOVE_DESC"
    tooltip_stackless none //tooltip_stacks_singular "Can move an extra time each turn"
}
```

---

### `Fear`
**Name:** Fear  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_FEAR_DESC`: "Moves as far away from enemies as it can at the start of its turn."

```
Fear {
    name "KEYWORD_FEAR_NAME"
    tooltip "KEYWORD_FEAR_DESC"
}
```

---

### `FireArmor`
**Name:** FireArmor  
**Source:** `keyword_tooltips.gon`  

```
FireArmor { //cut
    name "FireArmor"
    tooltip None
}
```

---

### `FireArmor2`
**Name:** FireArmor2  
**Source:** `keyword_tooltips.gon`  

```
FireArmor2 { //cut
    name "FireArmor2"
    tooltip None
}
```

---

### `FlyDamageIncrease`
**Source:** `keyword_tooltips.gon`  

```
FlyDamageIncrease {
    alias DamageUp
}
```

---

### `FreeSpell`
**Name:** Free Spell  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_FREESPELL_DESC`: "The next spell you cast costs 0 mana."

```
FreeSpell { //stacks = number of free spells (probably not necessary to say)
    name "KEYWORD_FREESPELL_NAME"
    tooltip "KEYWORD_FREESPELL_DESC"
}
```

---

### `Freeze`
**Name:** Freeze  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_FREEZE_DESC`: "Cannot take damage. Unfreezes at the start of its turn."

```
Freeze {
    name "KEYWORD_FREEZE_NAME"
    tooltip "KEYWORD_FREEZE_DESC"
}
```

---

### `GlobalFamiliarDamageBoost`
**Source:** `keyword_tooltips.gon`  

```
GlobalFamiliarDamageBoost {
    alias DamageUp
}
```

---

### `GlobalFamiliarMoveBoost`
**Source:** `keyword_tooltips.gon`  

```
GlobalFamiliarMoveBoost {
    alias MovementUp
}
```

---

### `Grappled`
**Name:** Grappled  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_GRAPPLED_DESC`: "Immobile as long as it's next to the thing that grappled it."

```
Grappled {
    name "KEYWORD_GRAPPLED_NAME"
    tooltip "KEYWORD_GRAPPLED_DESC"
}
```

---

### `HealthRegenUp`
**Name:** Health Regen  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_HEALTHREGEN_DESC`: "Regenerate {stacks} health at the end of its turn."
- `KEYWORD_HEALTHREGEN_DESC_STACKLESS`: "Regenerates health at the end of its turn."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_DEHYDRATED_DESC`: "Heals are reduced by 1. Does not heal after battle. Can be mitigated with water."

```
HeatWave {
    name "KEYWORD_DEHYDRATED_NAME"
    tooltip "KEYWORD_DEHYDRATED_DESC"
}
```

---

### `HeavierHits`
**Name:** Heavier Hits  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_HEAVIERHITS_DESC_STACKS`: "Physical damage inflicts Bruise {stacks} this turn."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_HEAVYHITS_DESC_STACKS`: "Basic attack inflicts Bruise {stacks} this turn."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_HEX_DESC`: "Spells cost {stacks} more mana to cast."
- `KEYWORD_HEX_DESC_STACKLESS`: "Spells cost more mana to cast."

```
Hex {
    name "KEYWORD_HEX_NAME"
    tooltip_stacks "KEYWORD_HEX_DESC"

    tooltip_stackless "KEYWORD_HEX_DESC_STACKLESS"
}
```

---

### `IceArmor`
**Name:** IceArmor  
**Source:** `keyword_tooltips.gon`  

```
IceArmor { //CUT
    name "IceArmor"
    tooltip None
}
```

---

### `ImbueBleed`
**Name:** ImbueBleed  
**Source:** `keyword_tooltips.gon`  

```
ImbueBleed { //cut maybe?
    name "ImbueBleed"
    tooltip_stacks "Next physical attack inflicts Bleed {stacks}"
    tooltip_stackless "Next physical attack inflicts Bleed"
}
```

---

### `ImbueKnockOutCoin`
**Name:** ImbueKnockOutCoin  
**Source:** `keyword_tooltips.gon`  

```
ImbueKnockOutCoin { //cut
    name "ImbueKnockOutCoin"
    tooltip None
}
```

---

### `ImbueManaLeech`
**Name:** ImbueManaLeech  
**Source:** `keyword_tooltips.gon`  

```
ImbueManaLeech { //cut
    name "ImbueManaLeech"
    tooltip None
}
```

---

### `ImbuePoison`
**Name:** ImbuePoison  
**Source:** `keyword_tooltips.gon`  

```
ImbuePoison { //cut
    name "ImbuePoison"
    tooltip None
}
```

---

### `ImbueRandomStatDown`
**Name:** ImbueRandomStatDown  
**Source:** `keyword_tooltips.gon`  

```
ImbueRandomStatDown { //cut
    name "ImbueRandomStatDown"
    tooltip None
}
```

---

### `ImbueWeakness`
**Name:** ImbueWeakness  
**Source:** `keyword_tooltips.gon`  

```
ImbueWeakness { //cut
    name "ImbueWeakness"
    tooltip None
}
```

---

### `Immobile`
**Name:** Immobile  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_IMMOBILE_DESC`: "Cannot move."

```
Immobile {
    name "KEYWORD_IMMOBILE_NAME"
    tooltip "KEYWORD_IMMOBILE_DESC"
}
```

---

### `Infested`
**Name:** Infested  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_INFESTED_DESC`: "The things infesting this pop out when it dies, destroying its corpse."

```
Infested {
    name "KEYWORD_INFESTED_NAME"
    tooltip "KEYWORD_INFESTED_DESC"
}
```

---

### `IntelligenceUp`
**Name:** Intelligence Up  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_INTDOWN_NAME`: "Intelligence Down"
- `KEYWORD_INTUP_DESC`: "Intelligence increased by {stacks}. <br/> Intelligence affects mana regen."
- `KEYWORD_INTDOWN_DESC`: "Intelligence decreased by {absstacks}. <br/> Intelligence affects mana regen."

```
IntelligenceUp {
    name "KEYWORD_INTUP_NAME"
    name_stacks_neg "KEYWORD_INTDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_INTUP_DESC"
    tooltip_stacks_neg "KEYWORD_INTDOWN_DESC"

    tooltip_stackless none //tooltip_stackless "Intelligence affects mana regen."
}
```

---

### `Invulnerable`
**Name:** Invulnerable  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_INVULNERABLE_DESC`: "Does not take damage."

```
Invulnerable {
    name "KEYWORD_INVULNERABLE_NAME"
    tooltip "KEYWORD_INVULNERABLE_DESC"
}
```

---

### `KineticSpikes`
**Name:** Kinetic Spikes  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_KINETICSPPIKES_DESC`: "When this takes damage, emit {stacks} Sparkles."
- `KEYWORD_KINETICSPPIKES_DESC_SINGULAR`: "When this takes damage, emit a Sparkle."
- `KEYWORD_KINETICSPPIKES_DESC_STACKLESS`: "When this takes damage, emit Sparkles."

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
**Name:** Knockback  
**Source:** `keyword_tooltips.gon`  

```
Knockback { //not really a status, just here so ability tooltips could show a knockback icon
    name "Knockback"
    tooltip None
}
```

---

### `LateBloomer`
**Name:** Late Bloomer  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_LATEBLOOMER_DESC`: "Gain All Stats Up 3 in {stacks} turns."
- `KEYWORD_LATEBLOOMER_SINGULAR_DESC`: "Gain All Stats Up 3 next turn."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_LEECHES_NAME_APPLIER`: "{applier's} Leeches."
- `KEYWORD_LEECHES_DESC`: "Drains {stacks} health at the end of the round."
- `KEYWORD_LEECHES_DESC_APPLIER`: "Drains {stacks} health at the end of {applier's} turn and gives it to {applier}."
- `KEYWORD_LEECHES_DESC_STACKLESS`: "Drains health from the leeched unit at the end of your turn."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_LIFESTEAL_DESC`: "The next {stacks} basic attacks you do heal you for the amount of health damage they inflict."
- `KEYWORD_LIFESTEAL_DESC_STACKLESS`: "Your next basic attack heals you for the amount of health damage it inflicts."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_LIFESTEAL2_DESC`: "Heals you equal to the amount of health damage dealt."

```
Leech {
    name "KEYWORD_LIFESTEAL_NAME"
    tooltip "KEYWORD_LIFESTEAL2_DESC"

    icon_frame 17
}
```

---

### `LoseShieldNextTurn`
**Name:** LoseShieldNextTurn  
**Source:** `keyword_tooltips.gon`  

```
LoseShieldNextTurn { //cut
    name "LoseShieldNextTurn"
    tooltip None
}
```

---

### `LuckUp`
**Name:** Luck Up  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_LCKDOWN_NAME`: "Luck Down"
- `KEYWORD_LCKUP_DESC`: "Luck increased by {stacks}. <br/> Luck affects base crit chance and all randomness."
- `KEYWORD_LCKDOWN_DESC`: "Luck decreased by {absstacks}. <br/> Luck affects base crit chance and all randomness."

```
LuckUp {
    name "KEYWORD_LCKUP_NAME"
    name_stacks_neg "KEYWORD_LCKDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_LCKUP_DESC"
    tooltip_stacks_neg "KEYWORD_LCKDOWN_DESC"

    tooltip_stackless none //tooltip_stackless "Luck affects base crit chance and all randomness."
}
```

---

### `Madness`
**Name:** Madness  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_MADNESS_DESC`: "Thinks everything is an enemy. Uncontrollable."

```
Madness {
    name "KEYWORD_MADNESS_NAME"
    tooltip "KEYWORD_MADNESS_DESC"
}
```

---

### `MagicWeakness`
**Name:** Magic Weakness  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_MAGICWEAKNESS_DESC`: "Incoming magic damage has 100% Crit Chance and can't miss."

```
MagicWeakness {
    name "KEYWORD_MAGICWEAKNESS_NAME"
    tooltip "KEYWORD_MAGICWEAKNESS_DESC"
}
```

---

### `ManaLeeches`
**Name:** Mana Leeches  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_MANALEECHES_NAME_APPLIER`: "{applier's} Mana Leeches"
- `KEYWORD_MANALEECHES_DESC`: "Drains {stacks} mana at the end of the round."
- `KEYWORD_MANALEECHES_DESC_APPLIER`: "Drains {stacks} mana at the end of {applier's} turn and gives it to {applier}."
- `KEYWORD_MANALEECHES_DESC_STACKLESS`: "Drains mana from the leeched unit at the end of your turn."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_MARKED_DESC`: "Incoming physical damage has 100% Crit Chance, ignores shield, and can't miss."

```
Marked {
    name "KEYWORD_MARKED_NAME"
    tooltip "KEYWORD_MARKED_DESC"
}
```

---

### `Meaty`
**Name:** Meaty  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_MEATY_DESC`: "Turns into meat when it dies."

```
Meaty {
    name "KEYWORD_MEATY_NAME"
    tooltip "KEYWORD_MEATY_DESC"
}
```

---

### `MissChance`
**Name:** Miss Chance  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_MISSCHANCE_DESC`: "Miss chance increased by {stacks}%."

```
MissChance {
    name "KEYWORD_MISSCHANCE_NAME"
    tooltip_stacks "KEYWORD_MISSCHANCE_DESC"
    tooltip_stackless none //tooltip_stackless "Increases miss chance"
}
```

---

### `MovementUp`
**Name:** Movement Up  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_MOVEMENTDOWN_NAME`: "Movement Down"
- `KEYWORD_MOVEMENTUP_DESC`: "Basic movement range increased by {stacks}."
- `KEYWORD_MOVEMENTDOWN_DESC`: "Basic movement range decreased by {stacks}."
- `KEYWORD_MOVEMENTUP_DESC_STACKLESS`: "Increases your basic movement's range."
- `KEYWORD_MOVEMENTDOWN_DESC_STACKLESS`: "Decreases your basic movement's range."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BONUSMOVE_DESC`: "An extra basic move that is saved across turns if unused."
- `KEYWORD_BONUSMOVE_DESC_STACKS`: "{stacks} extra basic moves that are saved across turns if unused."

```
MoveQuivered {
    name "KEYWORD_BONUSMOVE_NAME"
    tooltip_stacks_singular "KEYWORD_BONUSMOVE_DESC"
    tooltip_stacks "KEYWORD_BONUSMOVE_DESC_STACKS"
}
```

---

### `MutateAfterXTurns`
**Source:** `keyword_tooltips.gon`  

```
MutateAfterXTurns {
    alias TransformInXTurns
}
```

---

### `Muted`
**Name:** Muted  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_MUTED_DESC_SINGULAR`: "One of your spells is disabled until {applier} dies."
- `KEYWORD_MUTED_DESC`: "{stacks} of your spells are disabled until {applier} dies."
- `KEYWORD_MUTED_DESC_STACKLESS`: "Disables a random spell until the applier is killed."

```
Muted { //TODO: list which abilities are disabled in the tooltip
    name "KEYWORD_MUTED_NAME"
    tooltip_stacks_singular "KEYWORD_MUTED_DESC_SINGULAR"
    tooltip_stacks "KEYWORD_MUTED_DESC"

    tooltip_stackless "KEYWORD_MUTED_DESC_STACKLESS"
}
```

---

### `NextAbilityHeals`
**Name:** NextAbilityHeals  
**Source:** `keyword_tooltips.gon`  

```
NextAbilityHeals { //cut
    name "NextAbilityHeals"
    tooltip None
}
```

---

### `NextAbilityIncreaseRange`
**Name:** NextAbilityIncreaseRange  
**Source:** `keyword_tooltips.gon`  

```
NextAbilityIncreaseRange { //cut
    name "NextAbilityIncreaseRange"
    tooltip None
}
```

---

### `NextActionLuckUp`
**Source:** `keyword_tooltips.gon`  

```
NextActionLuckUp {
    alias LuckUp
}
```

---

### `NextAttackBonusRange`
**Name:** Bonus Range  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BONUSRANGE_DESC`: "Your next basic attack has +{stacks} range."
- `KEYWORD_BONUSRANGE_DESC_STACKLESS`: "Increases the range of your next basic attack."

```
NextAttackBonusRange {
    name "KEYWORD_BONUSRANGE_NAME"
    tooltip_stacks "KEYWORD_BONUSRANGE_DESC"
    tooltip_stackless "KEYWORD_BONUSRANGE_DESC_STACKLESS"
}
```

---

### `NextDamageReduceAndHealAllies`
**Name:** NextDamageReduceAndHealAllies  
**Source:** `keyword_tooltips.gon`  

```
NextDamageReduceAndHealAllies { //cut
    name "NextDamageReduceAndHealAllies"
    tooltip None
}
```

---

### `NextDamageReduceAndPushback`
**Name:** NextDamageReduceAndPushback  
**Source:** `keyword_tooltips.gon`  

```
NextDamageReduceAndPushback { //cut
    name "NextDamageReduceAndPushback"
    tooltip None
}
```

---

### `NextDamageReduceThisTurn`
**Name:** NextDamageReduceThisTurn  
**Source:** `keyword_tooltips.gon`  

```
NextDamageReduceThisTurn { //cut
    name "NextDamageReduceThisTurn"
    tooltip None
}
```

---

### `NextMoveRangeIncrease`
**Name:** NextMoveRangeIncrease  
**Source:** `keyword_tooltips.gon`  

```
NextMoveRangeIncrease { //cut
    name "NextMoveRangeIncrease"
    tooltip None
}
```

---

### `NextSpellHealEqualToMana`
**Name:** NextSpellHealEqualToMana  
**Source:** `keyword_tooltips.gon`  

```
NextSpellHealEqualToMana { //cut
    name "NextSpellHealEqualToMana"
    tooltip None
}
```

---

### `NextTurnDoubleRangedDamage`
**Name:** Double Ranged Damage  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_DOUBLERANGEDDMG_DESC`: "All ranged physical attacks and abilities deal double damage."

```
NextTurnDoubleRangedDamage { //used for Stake Out hunter ability
    name "KEYWORD_DOUBLERANGEDDMG_NAME"
    tooltip "KEYWORD_DOUBLERANGEDDMG_DESC"
}
```

---

### `NoHealthRegen`
**Name:** No Health Regen  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_NOHEALTHREGEN_DESC`: "Health won't regen automatically and does not regen at the end of battle."

```
NoHealthRegen {
    name "KEYWORD_NOHEALTHREGEN_NAME"
    tooltip "KEYWORD_NOHEALTHREGEN_DESC"
}
```

---

### `NoManaRegen`
**Name:** No Mana Regen  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_NOMANAREGEN_DESC`: "Mana won't regen automatically."

```
NoManaRegen {
    name "KEYWORD_NOMANAREGEN_NAME"
    tooltip "KEYWORD_NOMANAREGEN_DESC"
}
```

---

### `OldStealth`
**Name:** OldStealth  
**Source:** `keyword_tooltips.gon`  

```
OldStealth { //cut
    name "OldStealth"
    tooltip None
}
```

---

### `OneUseSpellDamageUp`
**Source:** `keyword_tooltips.gon`  

```
OneUseSpellDamageUp {
    alias SpellDamageUp
}
```

---

### `Ostracized`
**Name:** Ostracized  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_OSTRACIZED_DESC`: "Every unit sees this as an enemy and will attack it with priority."

```
Ostracized {
    name "KEYWORD_OSTRACIZED_NAME"
    tooltip "KEYWORD_OSTRACIZED_DESC"
}
```

---

### `PassiveBrace`
**Source:** `keyword_tooltips.gon`  

```
PassiveBrace {
    alias Brace
}
```

---

### `PermanentCharm`
**Source:** `keyword_tooltips.gon`  

```
PermanentCharm {
    alias Charmed
}
```

---

### `CapturedFamiliarIcon`
**Name:** Captured Familiar  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_CAPTUREDFAMILIAR_DESC`: "Was once an enemy, is now on your team. Will follow you to future battles if it doesn't die."

```
CapturedFamiliarIcon {
    name "KEYWORD_CAPTUREDFAMILIAR_NAME"
    tooltip "KEYWORD_CAPTUREDFAMILIAR_DESC"
}
```

---

### `PermanentImmobile`
**Source:** `keyword_tooltips.gon`  

```
PermanentImmobile {
    alias Immobile
}
```

---

### `PermanentMadness`
**Source:** `keyword_tooltips.gon`  

```
PermanentMadness {
    alias Madness
}
```

---

### `Petrify`
**Name:** Petrify  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_PETRIFY_DESC`: "It's a rock for {stacks} turns."
- `KEYWORD_PETRIFY_DESC_SINGULAR`: "It's a rock for 1 turn."
- `KEYWORD_PETRIFY_DESC_STACKLESS`: "Becomes a rock temporarily."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_POISON_DESC`: "Takes {stacks} damage at the start of each of its turns. Incoming healing is less effective but cures 1 Poison."
- `KEYWORD_POISON_DESC_STACKLESS`: "Takes damage at the start of every turn. Incoming healing is less effective but cures 1 Poison."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_POISONLACE_DESC`: "Basic attack inflicts +{stacks} Poison."
- `KEYWORD_POISONLACE_DESC_STACKLESS`: "Basic attack inflicts Poison."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_WPOISONLACE_DESC`: "Your weapon inflicts +{stacks} Poison."
- `KEYWORD_WPOISONLACE_DESC_STACKLESS`: "Your weapon inflicts Poison."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_POISONOUS_DESC`: "Inflicts Poison {stacks} to units that contact you."
- `KEYWORD_POISONOUS_DESC_STACKLESS`: "Inflicts Poison to units that contact you."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_POSSESSED_DESC`: "Takes {stacks} extra turns and is uncontrollable and charmed on those turns."
- `KEYWORD_POSSESSED_DESC_SIGNULAR`: "Takes an extra turn and is uncontrollable and charmed on that turn."
- `KEYWORD_POSSESSED_DESC_STACKLESS`: "Takes an extra Charmed turn."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_PREEMTIVECOUNTER_DESC`: "Attack the next {stacks} things that target you before they attack you, automatically."
- `KEYWORD_PREEMTIVECOUNTER_DESC_STACKLESS`: "Attack the next thing that targets you before it attacks you, automatically."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_QUIVERED_DESC_STACKLESS`: "An extra basic attack that is saved across turns if unused."
- `KEYWORD_QUIVERED_DESC`: "{stacks} extra basic attacks that are saved across turns if unused."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_RANDOMINJURY_DESC`: "Gain a random injury that lowers one of your stats by 1, permanently."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_HEALRANDOMINJURY_DESC`: "Cure a random injury that was permanently lowering one of your stats, if you have any."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_SPARKLE_DESC`: "A projectile that deals 1 magic damage to a random enemy."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_RANGEUP_DESC`: "Range increased by {stacks}."
- `KEYWORD_RANGEUP_DESC_STACKLESS`: "Increases the range of your basic attack and projectile abilities."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BONUSKNOCKBACK_DESC`: "Knockback you inflict is increased by {stacks}."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BONUSKNOCKBACKDAMAGE_DESC`: "Knockback damage you deal is increased by {stacks}."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TEMPITEM_DESC`: "Is lost at the end of the battle."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TEMPRANGE_DESC`: "Range increased by {stacks} until the end of the turn."
- `KEYWORD_TEMPRANGE_DESC_STACKLESS`: "Increases the range of your basic attack and projectile abilities until the end of the turn."

```
TempRangeUp {
    name "KEYWORD_TEMPRANGE_NAME"
    tooltip_stacks "KEYWORD_TEMPRANGE_DESC"
    tooltip_stackless "KEYWORD_TEMPRANGE_DESC_STACKLESS"
}
```

---

### `Reduce`
**Name:** Reduce  
**Source:** `keyword_tooltips.gon`  

```
Reduce { //cut
    name "Reduce"
    tooltip None
}
```

---

### `ReduceManaCost`
**Name:** Insight  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_REDUCEMANACOST_DESC`: "Spells cost {stacks} less mana to cast."
- `KEYWORD_REDUCEMANACOST_DESC_STACKLESS`: "Spells cost less mana to cast."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_INSIGHT_DESC`: "Spells cost {stacks} less mana to cast, excluding Brainstorm."
- `KEYWORD_INSIGHT_DESC_STACKLESS`: "Spells cost less mana to cast, excluding Brainstorm. (cannot reduce cost to 0)."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_REFLECT_DESC`: "Reflects the next {stacks} projectiles you are hit with back at the attacker."
- `KEYWORD_REFLECT_DESC_STACKLESS`: "Reflect the next projectile you're hit with back at the attacker."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_AUTOREVIVE_DESC_SINGULAR`: "Revives at the end of the round."
- `KEYWORD_AUTOREVIVE_DESC`: "Revives at the end of the next round."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ENERGIZED_DESC`: "Takes an extra turn. Cannot be Energized again until after that turn ends."

```
Robot { //tooltip only shows when the robot is energized, so this is an "energized" tooltip
    name "KEYWORD_ENERGIZED_NAME"
    tooltip "KEYWORD_ENERGIZED_DESC"
    tooltip_stackless none
}
```

---

### `Rot`
**Name:** Rot  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ROT_DESC`: "Hatches a Fly at the end of its turn. Damage from worms and bugs always crits against this."

```
Rot { //the rot fly is "enemies to the thing that spawned it", dont know the best way to word this. 90% of the time it means it spawns an "ally fly" (ally Rots an enemy, the enemy spawns an ally)
    name "KEYWORD_ROT_NAME"
    tooltip "KEYWORD_ROT_DESC"
}
```

---

### `SafeDoomed`
**Name:** Doomed  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_SAFEDOOMED_DESC`: "Ticks down at the end of your turn. When it hits 0, Die (without being injured)."

```
SafeDoomed {
    name "KEYWORD_SAFEDOOMED_NAME"
    tooltip "KEYWORD_SAFEDOOMED_DESC"
}
```

---

### `Scrambled`
**Name:** Scrambled  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_SCRAMBLED_DESC`: "Abilities are scrambled, temporarily."

```
Scrambled { //todo: alternate tooltip for cat vs non-cat
    name "KEYWORD_SCRAMBLED_NAME"
    tooltip "KEYWORD_SCRAMBLED_DESC"
}
```

---

### `SerratedClaws`
**Name:** Serrated Claws  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_SERRATED_DESC`: "Basic attack inflicts +{stacks} Bleed."
- `KEYWORD_SERRATED_DESC_STACKLESS`: "Basic attack inflicts Bleed."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_SHIELD_DESC_STACKLESS`: "Blocks incoming damage."

```
Shield { //not a status, used so an icon can show up on abilities
    name "KEYWORD_SHIELD_NAME"
    tooltip None

    tooltip_stackless "KEYWORD_SHIELD_DESC_STACKLESS"
}
```

---

### `shield`
**Source:** `keyword_tooltips.gon`  

```
shield {
    alias Shield
}
```

---

### `ShortCircuit`
**Name:** Short Circuit  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_SHORTCIRCUIT_DESC`: "All actions are disabled. Cast Break Circuit to break."

```
ShortCircuit {
    name "KEYWORD_SHORTCIRCUIT_NAME"
    tooltip "KEYWORD_SHORTCIRCUIT_DESC"
}
```

---

### `SkipNextTurn`
**Name:** SkipNextTurn  
**Source:** `keyword_tooltips.gon`  

```
SkipNextTurn { //cut
    name "SkipNextTurn"
    tooltip None
}
```

---

### `Sleep`
**Name:** Sleep  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_SLEEP_DESC`: "Skip the next {stacks} turns. Being attacked has a chance to wake you up."
- `KEYWORD_SLEEP_DESC_STACKLESS`: "Skip the next turn. Being attacked has a chance to wake you up."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_SLEEPPAR_DESC`: "You are asleep until your sleep paralysis demon is killed."

```
SleepParalysis {
    name "KEYWORD_SLEEPPAR_NAME"
    tooltip_stacks "KEYWORD_SLEEPPAR_DESC"
}
```

---

### `Slow`
**Name:** Slow  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_SLOW_DESC`: "Movement range is reduced to 2 for the next {stacks} turns. Takes its turn later."
- `KEYWORD_SLOW_DESC_STACKLESS`: "Movement range is reduced to 2. Takes its turn later."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_SOULLINK_DESC`: "Whenever a soul linked character loses health, all soul linked characters lose that health as well."

```
SoulLink {
    name "KEYWORD_SOULLINK_NAME"
    tooltip "KEYWORD_SOULLINK_DESC"
}
```

---

### `SpeedUp`
**Name:** Speed Up  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_SPDDOWN_NAME`: "Speed Down"
- `KEYWORD_SPDUP_DESC`: "Speed increased by {stacks}. <br/> Speed affects movement range and turn order."
- `KEYWORD_SPWDDOWN_DESC`: "Speed decreased by {absstacks}. <br/> Speed affects movement range and turn order."

```
SpeedUp {
    name "KEYWORD_SPDUP_NAME"
    name_stacks_neg "KEYWORD_SPDDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_SPDUP_DESC"
    tooltip_stacks_neg "KEYWORD_SPWDDOWN_DESC"

    tooltip_stackless none //tooltip_stackless "Speed affects movement range and turn order."
}
```

---

### `SpeedUp_WithoutInitiative`
**Source:** `keyword_tooltips.gon`  

```
SpeedUp_WithoutInitiative {
    alias SpeedUp
}
```

---

### `SpellDamageUp`
**Name:** Magic Damage Up  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_MAGICDMGUP_DESC`: "Magic damage you inflict does {stacks} extra damage."
- `KEYWORD_MAGICDMGUP_DESC_STACKLESS`: "Increases any magical damage you deal."

```
SpellDamageUp { //its never negative currently
    name "KEYWORD_MAGICDMGUP_NAME"
    tooltip_stacks "KEYWORD_MAGICDMGUP_DESC"

    tooltip_stackless "KEYWORD_MAGICDMGUP_DESC_STACKLESS"
}
```

---

### `SpellShield`
**Name:** SpellShield  
**Source:** `keyword_tooltips.gon`  

```
SpellShield { //currently unused
    name "SpellShield"
    tooltip None
}
```

---

### `SpiderInfested`
**Name:** Infested  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_SPIDERINFESTED_DESC`: "The spiders infesting this pop out when it dies, destroying its corpse."

```
SpiderInfested {
    name "KEYWORD_SPIDERINFESTED_NAME"
    tooltip "KEYWORD_SPIDERINFESTED_DESC"
}
```

---

### `SproutsGrantMovement`
**Source:** `keyword_tooltips.gon`  

```
SproutsGrantMovement {
    alias MovementUp
}
```

---

### `StatBounty`
**Name:** Stat Bounty  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_STATBOUNTY_DESC`: "Whoever kills this gets All Stats Up {stacks}."
- `KEYWORD_STATBOUNTY_DESC_STACKLESS`: "Whoever kills this gets All Stats Up."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_STEALTH_DESC`: "50% Dodge Chance. Lose Stealth when you get hit."

```
Stealth {
    name "KEYWORD_STEALTH_NAME"
    tooltip "KEYWORD_STEALTH_DESC"
}
```

---

### `StealthUntilBasicAttack`
**Name:** Stealth  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_STEALTHUNTIL_DESC`: "50% Dodge Chance. Lose Stealth when you get hit or use your basic attack."

```
StealthUntilBasicAttack {
    name "KEYWORD_STEALTHUNTIL_NAME"
    tooltip "KEYWORD_STEALTHUNTIL_DESC"
}
```

---

### `StrDownAura`
**Source:** `keyword_tooltips.gon`  

```
StrDownAura {
    alias StrengthUp
}
```

---

### `DexDownAura`
**Source:** `keyword_tooltips.gon`  

```
DexDownAura {
    alias DexterityUp
}
```

---

### `SpdDownAura`
**Source:** `keyword_tooltips.gon`  

```
SpdDownAura {
    alias SpeedUp
}
```

---

### `StrengthForEachNeighboringEnemy`
**Source:** `keyword_tooltips.gon`  

```
StrengthForEachNeighboringEnemy {
    alias StrengthUp
}
```

---

### `StrengthUp`
**Name:** Strength Up  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_STRDOWN_NAME`: "Strength Down"
- `KEYWORD_STRUP_DESC`: "Strength increased by {stacks}. <br/> Strength affects melee attack and melee ability damage."
- `KEYWORD_STRDOWN_DESC`: "Strength decreased by {absstacks}. <br/> Strength affects melee attack and melee ability damage."

```
StrengthUp {
    name "KEYWORD_STRUP_NAME"
    name_stacks_neg "KEYWORD_STRDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_STRUP_DESC"
    tooltip_stacks_neg "KEYWORD_STRDOWN_DESC"

    tooltip_stackless none //tooltip_stackless "Strength affects melee attack and melee ability damage."
}
```

---

### `Stun`
**Name:** Stun  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_STUN_DESC`: "Skip the next {stacks} turns."
- `KEYWORD_STUN_DESC_STACKLESS`: "Skip the next turn."

```
Stun {
    name "KEYWORD_STUN_NAME"
    tooltip_stacks "KEYWORD_STUN_DESC"

    tooltip_stackless "KEYWORD_STUN_DESC_STACKLESS"
}
```

---

### `Switcheroo`
**Name:** Switcheroo  
**Source:** `keyword_tooltips.gon`  

```
Switcheroo { //cut
    name "Switcheroo"
    tooltip None
}
```

---

### `Tarred`
**Name:** Tarred  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TARRED_DESC`: "Speed decreased by {stacks}. Flammable. <br/> Speed affects movement range and turn order."
- `KEYWORD_TARRED_DESC_STACKLESS`: "Decreases speed. Flammable."

```
Tarred {
    name "KEYWORD_TARRED_NAME"
    tooltip_stacks "KEYWORD_TARRED_DESC"

    tooltip_stackless "KEYWORD_TARRED_DESC_STACKLESS"
}
```

---

### `Taunted`
**Name:** Taunted  
**Source:** `keyword_tooltips.gon`  

```
Taunted { //cut
    name "Taunted"
    tooltip None
}
```

---

### `Taunting`
**Name:** Taunting  
**Source:** `keyword_tooltips.gon`  

```
Taunting { //cut
    name "Taunting"
    tooltip None
}
```

---

### `Tech`
**Name:** Tech  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TECH_DESC`: "Increases the quality of the next item you craft or the next familiar you spawn. <br/> Up to 3 Tech can be used at a time."

```
Tech {
    name "KEYWORD_TECH_NAME"
    tooltip "KEYWORD_TECH_DESC"
}
```

---

### `TempBackstab`
**Name:** Backstab Bonus  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TEMPBACKSTAB_DESC`: "+{stacks}% Backstab Damage this turn. (Plus the default 25% backstab bonus.)"
- `KEYWORD_TEMPBACKSTAB_DESC_STACKLESS`: "Increases the damage your Backstabs deal."

```
TempBackstab {
    name "KEYWORD_TEMPBACKSTAB_NAME"
    tooltip_stacks "KEYWORD_TEMPBACKSTAB_DESC"

    tooltip_stackless "KEYWORD_TEMPBACKSTAB_DESC_STACKLESS"
}
```

---

### `TempCharmed`
**Source:** `keyword_tooltips.gon`  

```
TempCharmed {
    alias Charmed
}
```

---

### `TempCounterAttack`
**Name:** Counter Attack  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TEMPCOUNTER_DESC`: "Attack things that damage you automatically."

```
TempCounterAttack { //stacks = how many turns it lasts for (ticks down start of your turn, since it lasts through enemy turns)
    name "KEYWORD_TEMPCOUNTER_NAME"
    tooltip "KEYWORD_TEMPCOUNTER_DESC"
}
```

---

### `TempCritChanceUp`
**Source:** `keyword_tooltips.gon`  

```
TempCritChanceUp {
    alias CritChanceUp
}
```

---

### `TempDamageUp`
**Source:** `keyword_tooltips.gon`  

```
TempDamageUp {
    alias DamageUp
}
```

---

### `TempDexterityUp`
**Source:** `keyword_tooltips.gon`  

```
TempDexterityUp {
    alias DexterityUp
}
```

---

### `TempInitiativeChange`
**Name:** Initiative Up  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TEMPINIT_DESC`: "You take your turn earlier in the round."
- `KEYWORD_TEMPINITDOWN_NAME`: "Initiative Down"
- `KEYWORD_TEMPINITDOWN_DESC`: "You take your turn later in the round."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TEMPIMMUNE_DESC`: "Cannot receive Injuries for any reason. Lasts {stacks} turns."
- `KEYWORD_TEMPIMMUNE_DESC_SINGULAR`: "Cannot receive Injuries for any reason. Lasts 1 turn."

```
TempInjuryImmunity {
     name "KEYWORD_TEMPIMMUNE_NAME"
     tooltip_stacks "KEYWORD_TEMPIMMUNE_DESC"
     tooltip_stacks_singular "KEYWORD_TEMPIMMUNE_DESC_SINGULAR"
     tooltip_stackless none //tooltip_stackless "Cannot receive Injuries for any reason."
}
```

---

### `TempManaCostReduction`
**Name:** Insight  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TEMPMANAREDUCTION_DESC`: "Spells cost {stacks} less mana to cast until the end of the turn."
- `KEYWORD_TEMPMANAREDUCTION_DESC_STACKLESS`: "Spells cost less mana to cast until the end of the turn."

```
TempManaCostReduction {
    name "KEYWORD_TEMPMANAREDUCTION_NAME"
    tooltip_stacks "KEYWORD_TEMPMANAREDUCTION_DESC"
    tooltip_stackless "KEYWORD_TEMPMANAREDUCTION_DESC_STACKLESS"
}
```

---

### `TempMovement`
**Source:** `keyword_tooltips.gon`  

```
TempMovement {
    alias MovementUp
}
```

---

### `TempPreEmptiveCounterAttack`
**Name:** Preemptive Counter  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_PRECOUNTER_DESC`: "Attack things that target you before they attack you, automatically."

```
TempPreEmptiveCounterAttack { //stacks = how many turns it lasts for (ticks down start of your turn, since it lasts through enemy turns)
    name "KEYWORD_PRECOUNTER_NAME"
    tooltip "KEYWORD_PRECOUNTER_DESC"
}
```

---

### `TempSpeedUp`
**Source:** `keyword_tooltips.gon`  

```
TempSpeedUp {
    alias SpeedUp
}
```

---

### `TempSpellDamageUp`
**Source:** `keyword_tooltips.gon`  

```
TempSpellDamageUp { //its never negative currently
    alias SpellDamageUp
}
```

---

### `TempStrengthUp`
**Source:** `keyword_tooltips.gon`  

```
TempStrengthUp {
    alias StrengthUp
}
```

---

### `Thorns`
**Name:** Thorns  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_THORNS_DESC`: "Deals {stacks} damage to units that contact you."
- `KEYWORD_THORNS_DESC_STACKLESS`: "Deals damage to units that contact you."

```
Thorns {
    name "KEYWORD_THORNS_NAME"
    tooltip_stacks "KEYWORD_THORNS_DESC"

    tooltip_stackless "KEYWORD_THORNS_DESC_STACKLESS"
}
```

---

### `TilesMovedToCritChance`
**Name:** TilesMovedToCritChance  
**Source:** `keyword_tooltips.gon`  

```
TilesMovedToCritChance { //cut
    name "TilesMovedToCritChance"
    tooltip None
}
```

---

### `TilesMovedToHealth`
**Name:** TilesMovedToHealth  
**Source:** `keyword_tooltips.gon`  

```
TilesMovedToHealth { //cut
    name "TilesMovedToHealth"
    tooltip None
}
```

---

### `TilesMovedToMana`
**Name:** TilesMovedToMana  
**Source:** `keyword_tooltips.gon`  

```
TilesMovedToMana { //cut
    name "TilesMovedToMana"
    tooltip None
}
```

---

### `TilesMovedToNeighborHeal`
**Name:** TilesMovedToNeighborHeal  
**Source:** `keyword_tooltips.gon`  

```
TilesMovedToNeighborHeal { //cut
    name "TilesMovedToNeighborHeal"
    tooltip None
}
```

---

### `TilesMovedToStrength`
**Name:** TilesMovedToStrength  
**Source:** `keyword_tooltips.gon`  

```
TilesMovedToStrength { //cut
    name "TilesMovedToStrength"
    tooltip None
}
```

---

### `TowerDefenseStatus`
**Name:** Sentry Mode  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_SENTRY_DESC`: "The next time an enemy ends its movement in your basic attack range, attack it."

```
TowerDefenseStatus {
    name "KEYWORD_SENTRY_NAME"
    tooltip "KEYWORD_SENTRY_DESC"
}
```

---

### `TowerDefenseStatus2`
**Name:** Sentry Mode+  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_SENTRYPLUS_DESC`: "When an enemy ends its movement in your basic attack range, attack it. Lasts {stacks} turns."
- `KEYWORD_SENTRYPLUS_DESC_STACKLESS`: "When an enemy ends its movement in your basic attack range, attack it."

```
TowerDefenseStatus2 {
    name "KEYWORD_SENTRYPLUS_NAME"
    tooltip_stacks "KEYWORD_SENTRYPLUS_DESC"

    tooltip_stackless "KEYWORD_SENTRYPLUS_DESC_STACKLESS"
}
```

---

### `TrailBlazer`
**Name:** Trail Blazer  
**Source:** `keyword_tooltips.gon`  

```
TrailBlazer { //cut
    name "Trail Blazer"
    tooltip None
}
```

---

### `Trample`
**Name:** Trample  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TRAMPLE_DESC_STACKLESS`: "You can move through other units, damaging and displacing them."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TRANSFORM_DESC`: "Transforms when the timer hits 0."

```
TransformInXTurns { //used for Jekyll enemies
    name "KEYWORD_TRANSFORM_NAME"
    tooltip "KEYWORD_TRANSFORM_DESC"
}
```

---

### `VeinyBonus`
**Source:** `keyword_tooltips.gon`  

```
VeinyBonus {
    alias StrengthUp
}
```

---

### `Weakness`
**Name:** Weakness  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_WEAKNESS_DESC`: "-2 [img:dex], -2 [img:str], -2 [img:spd]. Lasts {stacks} turns."
- `KEYWORD_WEAKNESS_DESC_SINGULAR`: "-2 [img:dex], -2 [img:str], -2 [img:spd]. Lasts 1 turn."
- `KEYWORD_WEAKNESS_DESC_STACKLESS`: "-2 [img:dex], -2 [img:str], -2 [img:spd], temporarily."

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
**Source:** `keyword_tooltips.gon`  

```
DepressionAura { //different effect from Weakness, used for Depression
    alias AllStatsUp
}
```

---

### `Webbed`
**Name:** Webbed  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_WEBBED_DESC`: "Immobile. Use basic attack to break free."

```
Webbed {
    name "KEYWORD_WEBBED_NAME"
    tooltip "KEYWORD_WEBBED_DESC"
}
```

---

### `Tangled`
**Name:** Entangled  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TANGLED_DESC`: "Immobile. Use basic attack to break free."

```
Tangled {
    name "KEYWORD_TANGLED_NAME"
    tooltip "KEYWORD_TANGLED_DESC"
}
```

---

### `Wet`
**Name:** Wet  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_WET_DESC`: "Wet."

```
Wet {
    name "KEYWORD_WET_NAME"
    tooltip "KEYWORD_WET_DESC"
}
```

---

### `Zombie`
**Name:** Zombie  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ZOMBIE_DESC`: "-2 [img:str]. -2 [img:int]. Takes damage from Holy Element heals. Does not get injured when downed."

```
Zombie {
    name "KEYWORD_ZOMBIE_NAME"
    tooltip "KEYWORD_ZOMBIE_DESC"
}
```

---

### `Metal`
**Name:** Metal  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_METAL_DESC`: "This item is electrically conductive."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_FRAGILE_DESC`: "This item breaks when you're downed."

```
Fragile {
    name "KEYWORD_FRAGILE_NAME"
    tooltip "KEYWORD_FRAGILE_DESC"

    icon_frame 149
}
```

---

### `FragileDuringElement`
**Source:** `keyword_tooltips.gon`  

```
FragileDuringElement {
    alias Fragile
}
```

---

### `Brittle`
**Name:** Brittle  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_BRITTLE_DESC`: "This item has a 25% chance to break when you take damage."

```
Brittle {
    name "KEYWORD_BRITTLE_NAME"
    tooltip "KEYWORD_BRITTLE_DESC"

    icon_frame 150
}
```

---

### `BrittleDuringElement`
**Source:** `keyword_tooltips.gon`  

```
BrittleDuringElement {
    alias Brittle
}
```

---

### `Flammable`
**Name:** Flammable  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_FLAMMABLE_DESC`: "This item burns up when hit with fire."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_CURSED_DESC`: "This item cannot be unequipped once equipped."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_RELOAD_DESC`: "This action starts disabled and does not refresh on its own after use. Meet the condition to refresh it."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_RELOADB_DESC`: "This action does not refresh on its own after use. Meet the condition to refresh it."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_FLYING_DESC`: "Ignores tiles and can pass over units and objects."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_COMFORT_DESC`: "Affects how often cats will breed or fight."

```
Comfort {
    name "KEYWORD_COMFORT_NAME"
    tooltip "KEYWORD_COMFORT_DESC"
}
```

---

### `Stimulation`
**Name:** [img:stimulation] Stimulation  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_STIMULATION_DESC`: "Affects the quality of newborn kittens."

```
Stimulation {
    name "KEYWORD_STIMULATION_NAME"
    tooltip "KEYWORD_STIMULATION_DESC"
}
```

---

### `Appeal`
**Name:** [img:appeal] Appeal  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_APPEAL_DESC`: "Affects the quality of the stray cats that show up each day"

```
Appeal {
    name "KEYWORD_APPEAL_NAME"
    tooltip "KEYWORD_APPEAL_DESC"
}
```

---

### `Evolution`
**Name:** [img:evolution] Mutation  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_EVOLUTION_DESC`: "Adds a chance for cats to receive random mutations each night."

```
Evolution {
    name "KEYWORD_EVOLUTION_NAME"
    tooltip "KEYWORD_EVOLUTION_DESC"
}
```

---

### `Health`
**Name:** [img:health] Health  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_HEALTH_DESC`: "Affects lifespan and chance to develop or cure disorders each night"

```
Health {
    name "KEYWORD_HEALTH_NAME"
    tooltip "KEYWORD_HEALTH_DESC"
}
```

---

### `DemonicGlyph_Bite`
**Name:** Lucifer Rune  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TOR_BITE_DESC`: "Imbues its owner with an extra turn and the power to Bite"

```
DemonicGlyph_Bite {
    name "KEYWORD_TOR_BITE_NAME"
    tooltip "KEYWORD_TOR_BITE_DESC"
}
```

---

### `DemonicGlyph_Fire`
**Name:** Brimstone Rune  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TOR_FIRE_DESC`: "Imbues its owner's basic attack with +2 Damage and +2 Burn."

```
DemonicGlyph_Fire {
    name "KEYWORD_TOR_FIRE_NAME"
    tooltip "KEYWORD_TOR_FIRE_DESC"
}
```

---

### `DemonicGlyph_Summon`
**Name:** Pentagram Rune  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TOR_SUMMON_DESC`: "Imbues its owner with an extra turn and the power to Summon"

```
DemonicGlyph_Summon {
    name "KEYWORD_TOR_SUMMON_NAME"
    tooltip "KEYWORD_TOR_SUMMON_DESC"
}
```

---

### `DemonicGlyph_Movement`
**Name:** Hexagram Rune  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TOR_MOVE_DESC`: "Imbues its owner with +1 Movement Range and +3 Trample Damage"

```
DemonicGlyph_Movement {
    name "KEYWORD_TOR_MOVE_NAME"
    tooltip "KEYWORD_TOR_MOVE_DESC"
}
```

---

### `DemonicGlyph_Bounce`
**Name:** Chaos Rune  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_TOR_BOUNCE_DESC`: "Imbues its owner with the ability to repel attackers."

```
DemonicGlyph_Bounce {
    name "KEYWORD_TOR_BOUNCE_NAME"
    tooltip "KEYWORD_TOR_BOUNCE_DESC"
}
```

---

### `FinalBossHitCountdownHoly`
**Name:** The Child's Flame  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_CHILDHOLY_DESC`: "Counts down every time it gets hit. At 0, unleash the holy beams."

```
FinalBossHitCountdownHoly {
    name "KEYWORD_CHILDHOLY_NAME"
    tooltip "KEYWORD_CHILDHOLY_DESC"
}
```

---

### `FinalBossHitCountdownBoris`
**Name:** The Child's Flame  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_CHILDPULSE_DESC`: "Counts down every time it gets hit. At 0, releases a pulse."

```
FinalBossHitCountdownBoris {
    name "KEYWORD_CHILDPULSE_NAME"
    tooltip "KEYWORD_CHILDPULSE_DESC"
}
```

---

### `FinalBossHitCountdownExplosive`
**Name:** The Child's Flame  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_CHILDWRATH_DESC`: "Counts down every time it gets hit. At 0, unleash a wrath of holy light."

```
FinalBossHitCountdownExplosive {
    name "KEYWORD_CHILDWRATH_NAME"
    tooltip "KEYWORD_CHILDWRATH_DESC"
}
```

---

### `TVBotObey`
**Name:** OBEY  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `ENEMY_TVBOT_OBEY_DESC`: "Basic attacks of its enemies are disabled."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `ENEMY_TVBOT_STOP_DESC`: "Basic movement of its enemies is disabled."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `ENEMY_TVBOT_DUMB_DESC`: "Spells of its enemies are disabled."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `ENEMY_TVBOT_DIE_DESC`: "It is too late. Win now or die."

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
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_SPIKY_DESC`: "+2 Thorns"

```
EliteBuff_Spiky {
    name "KEYWORD_ELITE_SPIKY_NAME"
    tooltip "KEYWORD_ELITE_SPIKY_DESC"
}
```

---

### `EliteBuff_BossSpiky`
**Name:** Elite Buff: Spiky  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_BOSSSPIKY_DESC`: "+1 Thorns"

```
EliteBuff_BossSpiky {
    name "KEYWORD_ELITE_BOSSSPIKY_NAME"
    tooltip "KEYWORD_ELITE_BOSSSPIKY_DESC"
}
```

---

### `EliteBuff_Reactive`
**Name:** Elite Buff: Reactive  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_REACTIVE_DESC`: "+1 Kinetic Spikes"

```
EliteBuff_Reactive {
    name "KEYWORD_ELITE_REACTIVE_NAME"
    tooltip "KEYWORD_ELITE_REACTIVE_DESC"
}
```

---

### `EliteBuff_BossReactive`
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossReactive {
    alias EliteBuff_Reactive
}
```

---

### `EliteBuff_Damaging`
**Name:** Elite Buff: Damaging  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_DAMAGING_DESC`: "+2 Damage"

```
EliteBuff_Damaging {
    name "KEYWORD_ELITE_DAMAGING_NAME"
    tooltip "KEYWORD_ELITE_DAMAGING_DESC"
}
```

---

### `EliteBuff_BossDamaging`
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossDamaging {
    alias EliteBuff_Damaging
}
```

---

### `EliteBuff_Tough`
**Name:** Elite Buff: Tough  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_TOUGH_DESC`: "+2 Brace"

```
EliteBuff_Tough {
    name "KEYWORD_ELITE_TOUGH_NAME"
    tooltip "KEYWORD_ELITE_TOUGH_DESC"
}
```

---

### `EliteBuff_BossTough`
**Name:** Elite Buff: Tough  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_BOSSTOUGH_DESC`: "+1 Brace"

```
EliteBuff_BossTough {
    name "KEYWORD_ELITE_BOSSTOUGH_NAME"
    tooltip "KEYWORD_ELITE_BOSSTOUGH_DESC"
}
```

---

### `EliteBuff_Shielded1`
**Name:** Elite Buff: Shielded  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_SHIELDED1_DESC`: "At the start of each round, if it has less than 3 [img:shield], set [img:shield] to 3. -20% max health."

```
EliteBuff_Shielded1 {
    name "KEYWORD_ELITE_SHIELDED1_NAME"
    tooltip "KEYWORD_ELITE_SHIELDED1_DESC"
}
```

---

### `EliteBuff_BossShielded1`
**Name:** Elite Buff: Shielded  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_BOSSSHIELDED1_DESC`: "At the start of each round, if it has less than 4 [img:shield], set [img:shield] to 4. -20% max health."

```
EliteBuff_BossShielded1 {
    name "KEYWORD_ELITE_BOSSSHIELDED1_NAME"
    tooltip "KEYWORD_ELITE_BOSSSHIELDED1_DESC"
}
```

---

### `EliteBuff_Shielded2`
**Name:** Elite Buff: Shielded  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_SHIELDED2_DESC`: "At the start of each round, if it has less than 5 [img:shield], set [img:shield] to 5. -20% max health."

```
EliteBuff_Shielded2 {
    name "KEYWORD_ELITE_SHIELDED2_NAME"
    tooltip "KEYWORD_ELITE_SHIELDED2_DESC"
}
```

---

### `EliteBuff_BossShielded2`
**Name:** Elite Buff: Shielded  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_BOSSSHIELDED2_DESC`: "At the start of each round, if it has less than 8 [img:shield], set [img:shield] to 8. -20% max health."

```
EliteBuff_BossShielded2 {
    name "KEYWORD_ELITE_BOSSSHIELDED2_NAME"
    tooltip "KEYWORD_ELITE_BOSSSHIELDED2_DESC"
}
```

---

### `EliteBuff_Shielded3`
**Name:** Elite Buff: Shielded  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_SHIELDED3_DESC`: "At the start of each round, if it has less than 7 [img:shield], set [img:shield] to 7. -20% max health."

```
EliteBuff_Shielded3 {
    name "KEYWORD_ELITE_SHIELDED3_NAME"
    tooltip "KEYWORD_ELITE_SHIELDED3_DESC"
}
```

---

### `EliteBuff_BossShielded3`
**Name:** Elite Buff: Shielded  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_BOSSSHIELDED3_DESC`: "At the start of each round, if it has less than 12 [img:shield], set [img:shield] to 12. -20% max health."

```
EliteBuff_BossShielded3 {
    name "KEYWORD_ELITE_BOSSSHIELDED3_NAME"
    tooltip "KEYWORD_ELITE_BOSSSHIELDED3_DESC"
}
```

---

### `EliteBuff_Shielded4`
**Name:** Elite Buff: Shielded  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_SHIELDED4_DESC`: "At the start of each round, if it has less than 9 [img:shield], set [img:shield] to 9. -20% max health."

```
EliteBuff_Shielded4 {
    name "KEYWORD_ELITE_SHIELDED4_NAME"
    tooltip "KEYWORD_ELITE_SHIELDED4_DESC"
}
```

---

### `EliteBuff_BossShielded4`
**Name:** Elite Buff: Shielded  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_BOSSSHIELDED4_DESC`: "At the start of each round, if it has less than 16 [img:shield], set [img:shield] to 16. -20% max health."

```
EliteBuff_BossShielded4 {
    name "KEYWORD_ELITE_BOSSSHIELDED4_NAME"
    tooltip "KEYWORD_ELITE_BOSSSHIELDED4_DESC"
}
```

---

### `EliteBuff_Protected`
**Name:** Elite Buff: Protected  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_PROTECTED_DESC`: "At the end of each turn, set [img:divineshield] to 1 if it had no [img:divineshield]. -20% max health."

```
EliteBuff_Protected {
    name "KEYWORD_ELITE_PROTECTED_NAME"
    tooltip "KEYWORD_ELITE_PROTECTED_DESC"
}
```

---

### `EliteBuff_BossProtected`
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossProtected {
    alias EliteBuff_Protected
}
```

---

### `EliteBuff_Speedy`
**Name:** Elite Buff: Speedy  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_SPEEDY_DESC`: "+4 [img:spd]"

```
EliteBuff_Speedy {
    name "KEYWORD_ELITE_SPEEDY_NAME"
    tooltip "KEYWORD_ELITE_SPEEDY_DESC"
}
```

---

### `EliteBuff_BossSpeedy`
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossSpeedy {
    alias EliteBuff_Speedy
}
```

---

### `EliteBuff_Flaming`
**Name:** Elite Buff: Flaming  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_FLAMING_DESC`: "Fire Immune. Leaves a trail of fire."

```
EliteBuff_Flaming {
    name "KEYWORD_ELITE_FLAMING_NAME"
    tooltip "KEYWORD_ELITE_FLAMING_DESC"
}
```

---

### `EliteBuff_BossFlaming`
**Name:** Elite Buff: Flaming  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_BOSSFLAMING_DESC`: "Fire Immune. Leaves a trail of fire. Applies Burn 1 to attackers."

```
EliteBuff_BossFlaming {
    name "KEYWORD_ELITE_BOSSFLAMING_NAME"
    tooltip "KEYWORD_ELITE_BOSSFLAMING_DESC"
}
```

---

### `EliteBuff_Creepy`
**Name:** Elite Buff: Creepy  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_CREEPY_DESC`: "Basic attack inflicts Poison. Leaves a trail of creep."

```
EliteBuff_Creepy {
    name "KEYWORD_ELITE_CREEPY_NAME"
    tooltip "KEYWORD_ELITE_CREEPY_DESC"
}
```

---

### `EliteBuff_Lucky`
**Name:** Elite Buff: Lucky  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_LUCKY_DESC`: "+3 [img:lck]. +10% Crit Chance. +10% Dodge Chance."

```
EliteBuff_Lucky {
    name "KEYWORD_ELITE_LUCKY_NAME"
    tooltip "KEYWORD_ELITE_LUCKY_DESC"
}
```

---

### `EliteBuff_BossLucky`
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossLucky {
    alias EliteBuff_Lucky
}
```

---

### `EliteBuff_Static`
**Name:** Elite Buff: Static  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_STATIC_DESC`: "Arcs 1 electric damage to neighbors whenever it moves."

```
EliteBuff_Static {
    name "KEYWORD_ELITE_STATIC_NAME"
    tooltip "KEYWORD_ELITE_STATIC_DESC"
}
```

---

### `EliteBuff_BossStatic`
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossStatic {
    alias EliteBuff_Static
}
```

---

### `EliteBuff_Bouncy`
**Name:** Elite Buff: Bouncy  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_BOUNCY_DESC`: "When hit, bounces itself and its attacker apart."

```
EliteBuff_Bouncy {
    name "KEYWORD_ELITE_BOUNCY_NAME"
    tooltip "KEYWORD_ELITE_BOUNCY_DESC"
}
```

---

### `EliteBuff_BossBouncy`
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossBouncy {
    alias EliteBuff_Bouncy
}
```

---

### `EliteBuff_Mirror`
**Name:** Elite Buff: Mirror  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_MIRROR_DESC`: "Reflects all projectiles. Takes 2 damage when it reflects a projectile."

```
EliteBuff_Mirror {
    name "KEYWORD_ELITE_MIRROR_NAME"
    tooltip "KEYWORD_ELITE_MIRROR_DESC"
}
```

---

### `EliteBuff_Resonant`
**Name:** Elite Buff: Resonant  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_RESONANT_DESC`: "Whenever an enemy casts a spell, gain All Stats Up 1 and heal 1."

```
EliteBuff_Resonant {
    name "KEYWORD_ELITE_RESONANT_NAME"
    tooltip "KEYWORD_ELITE_RESONANT_DESC"
}
```

---

### `EliteBuff_Undying`
**Name:** Elite Buff: Undying  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_UNDYING_DESC`: "Revives to 50% health at the end of the round. +2 Corpse Health."

```
EliteBuff_Undying {
    name "KEYWORD_ELITE_UNDYING_NAME"
    tooltip "KEYWORD_ELITE_UNDYING_DESC"
}
```

---

### `EliteBuff_SubUndying`
**Name:** Elite Buff: Undying  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_SUBUNDYING_DESC`: "Revives to 50% health at the end of the round."

```
EliteBuff_SubUndying {
    name "KEYWORD_ELITE_SUBUNDYING_NAME"
    tooltip "KEYWORD_ELITE_SUBUNDYING_DESC"
}
```

---

### `EliteBuff_Healthy`
**Name:** Elite Buff: Healthy  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_HEALTHY_DESC`: "+3 Health Regen. +20 unfilled max health."

```
EliteBuff_Healthy {
    name "KEYWORD_ELITE_HEALTHY_NAME"
    tooltip "KEYWORD_ELITE_HEALTHY_DESC"
}
```

---

### `EliteBuff_Sandy`
**Name:** Elite Buff: Sandy  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_SANDY_DESC`: "+10% Dodge Chance. Starts a sandstorm when it dies."

```
EliteBuff_Sandy {
    name "KEYWORD_ELITE_SANDY_NAME"
    tooltip "KEYWORD_ELITE_SANDY_DESC"
}
```

---

### `EliteBuff_Infested`
**Name:** Elite Buff: Infested  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_INFESTED_DESC`: "Spawns a fly swarm when it dies."

```
EliteBuff_Infested {
    name "KEYWORD_ELITE_INFESTED_NAME"
    tooltip "KEYWORD_ELITE_INFESTED_DESC"
}
```

---

### `EliteBuff_Absorbant`
**Name:** Elite Buff: Absorbent  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_ABSORBANT_DESC`: "Drains all unused mana from units when they end their turn, and deals damage to them equal to the amount of mana drained."

```
EliteBuff_Absorbant {
    name "KEYWORD_ELITE_ABSORBANT_NAME"
    tooltip "KEYWORD_ELITE_ABSORBANT_DESC"
}
```

---

### `EliteBuff_BossAbsorbant`
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossAbsorbant {
    alias EliteBuff_Absorbant
}
```

---

### `EliteBuff_Depressing`
**Name:** Elite Buff: Depressing  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_DEPRESSING_DESC`: "While alive, its enemies have -1 to all stats."

```
EliteBuff_Depressing {
    name "KEYWORD_ELITE_DEPRESSING_NAME"
    tooltip "KEYWORD_ELITE_DEPRESSING_DESC"
}
```

---

### `EliteBuff_BossDepressing`
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossDepressing {
    alias EliteBuff_Depressing
}
```

---

### `EliteBuff_SlightlyDepressing`
**Name:** Elite Buff: Slightly Depressing  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_SLIGHTLYDEPRESSING_DESC`: "While alive, adjacent enemies have -1 to all stats."

```
EliteBuff_SlightlyDepressing {
    name "KEYWORD_ELITE_SLIGHTLYDEPRESSING_NAME"
    tooltip "KEYWORD_ELITE_SLIGHTLYDEPRESSING_DESC"
}
```

---

### `EliteBuff_BossSlightlyDepressing`
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossSlightlyDepressing {
    alias EliteBuff_SlightlyDepressing
}
```

---

### `EliteBuff_Evolving`
**Name:** Elite Buff: Evolving  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_EVOLVING_DESC`: "At the end of each round, gain a random Elite Buff."

```
EliteBuff_Evolving {
    name "KEYWORD_ELITE_EVOLVING_NAME"
    tooltip "KEYWORD_ELITE_EVOLVING_DESC"
}
```

---

### `EliteBuff_Plow`
**Name:** Elite Buff: Plow  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_PLOW_DESC`: "Trample. Moves one space towards attackers when damaged."

```
EliteBuff_Plow {
    name "KEYWORD_ELITE_PLOW_NAME"
    tooltip "KEYWORD_ELITE_PLOW_DESC"
}
```

---

### `EliteBuff_Mega`
**Name:** Elite Buff: Mega  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_MEGA_DESC`: "Takes one less turn per round. +50% health and damage"

```
EliteBuff_Mega {
    name "KEYWORD_ELITE_MEGA_NAME"
    tooltip "KEYWORD_ELITE_MEGA_DESC"
}
```

---

### `EliteBuff_Mad`
**Name:** Elite Buff: Mad  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_MAD_DESC`: "Madness. Takes an extra turn per round. Gains +1 all stats and heals 4 when it gets a kill."

```
EliteBuff_Mad {
    name "KEYWORD_ELITE_MAD_NAME"
    tooltip "KEYWORD_ELITE_MAD_DESC"
}
```

---

### `EliteBuff_BossMad`
**Name:** Elite Buff: Mad  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_BOSSMAD_DESC`: "Madness. Gains +1 all stats and heals 4 when it gets a kill."

```
EliteBuff_BossMad {
    name "KEYWORD_ELITE_BOSSMAD_NAME"
    tooltip "KEYWORD_ELITE_BOSSMAD_DESC"
}
```

---

### `EliteBuff_Twin`
**Name:** Elite Buff: Twin  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_TWIN_DESC`: "Half health. Comes with a twin."

```
EliteBuff_Twin {
    name "KEYWORD_ELITE_TWIN_NAME"
    tooltip "KEYWORD_ELITE_TWIN_DESC"
}
```

---

### `EliteBuff_BossTwin`
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossTwin {
    alias EliteBuff_Twin
}
```

---

### `EliteBuff_SubTwin`
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_SubTwin {
    alias EliteBuff_Twin
}
```

---

### `EliteBuff_BossSubTwin`
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossSubTwin {
    alias EliteBuff_Twin
}
```

---

### `EliteBuff_Hardy`
**Name:** Elite Buff: Hardy  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_HARDY_DESC`: "Immune to stuns."

```
EliteBuff_Hardy {
    name "KEYWORD_ELITE_HARDY_NAME"
    tooltip "KEYWORD_ELITE_HARDY_DESC"
}
```

---

### `EliteBuff_BossHardy`
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossHardy {
    alias EliteBuff_Hardy
}
```

---

### `EliteBuff_Sticky`
**Name:** Elite Buff: Sticky  
**Source:** `keyword_tooltips.gon`  

**Localization Strings:**
- `KEYWORD_ELITE_STICKY_DESC`: "Anything that contacts or attacks this gets Tarred 1."

```
EliteBuff_Sticky {
    name "KEYWORD_ELITE_STICKY_NAME"
    tooltip "KEYWORD_ELITE_STICKY_DESC"
}
```

---

### `EliteBuff_BossSticky`
**Source:** `keyword_tooltips.gon`  

```
EliteBuff_BossSticky {
    alias EliteBuff_Sticky
}
```

---

