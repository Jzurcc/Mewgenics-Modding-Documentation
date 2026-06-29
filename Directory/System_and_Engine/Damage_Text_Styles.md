# System and Engine/Damage Text Styles Directory

<details open>
<summary><strong>Quick Navigation</strong></summary>

<table>
  <tr>
    <td width="22%"><strong>Abilities</strong></td>
    <td><a href="../Abilities/Ability_Pools.md">Ability Pools</a> • <a href="../Abilities/Cat_Abilities.md">Cat Abilities</a> • <a href="../Abilities/Enemy_and_Boss_Abilities.md">Enemy & Boss Abilities</a> • <a href="../Abilities/System_and_Item_Abilities.md">System & Item Abilities</a></td>
  </tr>
  <tr>
    <td><strong>Cats and Classes</strong></td>
    <td><a href="../Cats_and_Classes/Cat_Quotes.md">Cat Quotes</a> • <a href="../Cats_and_Classes/Classes.md">Classes</a> • <a href="../Cats_and_Classes/Custom_Cats.md">Custom Cats</a> • <a href="../Cats_and_Classes/Mutations.md">Mutations</a> • <a href="../Cats_and_Classes/Special_Strays.md">Special Strays</a> • <a href="../Cats_and_Classes/Tutorial_Cats.md">Tutorial Cats</a></td>
  </tr>
  <tr>
    <td><strong>Enemies and Combat</strong></td>
    <td><a href="../Enemies_and_Combat/Boss_Cutscene_Info.md">Boss Cutscene Info</a> • <a href="../Enemies_and_Combat/Combat_Rewards.md">Combat Rewards</a> • <a href="../Enemies_and_Combat/Elite_Buffs.md">Elite Buffs</a> • <a href="../Enemies_and_Combat/Enemies_and_Characters.md">Enemies & Characters</a> • <a href="../Enemies_and_Combat/Enemy_AI.md">Enemy AI</a> • <a href="../Enemies_and_Combat/Spawns_and_Enemy_Pools.md">Spawns & Enemy Pools</a> • <a href="../Enemies_and_Combat/Team_Names.md">Team Names</a></td>
  </tr>
  <tr>
    <td><strong>Items and Passives</strong></td>
    <td><a href="../Items_and_Passives/Item_Pools.md">Item Pools</a> • <a href="../Items_and_Passives/Item_Set_Bonuses.md">Item Set Bonuses</a> • <a href="../Items_and_Passives/Items_and_Equipment.md">Items & Equipment</a> • <a href="../Items_and_Passives/Passive_Pools.md">Passive Pools</a> • <a href="../Items_and_Passives/Passives.md">Passives</a></td>
  </tr>
  <tr>
    <td><strong>Statuses and Injuries</strong></td>
    <td><a href="../Statuses_and_Injuries/Injuries.md">Injuries</a> • <a href="../Statuses_and_Injuries/Status_Effect_Keywords.md">Status Effect Keywords</a></td>
  </tr>
  <tr>
    <td><strong>System and Engine</strong></td>
    <td><a href="../System_and_Engine/Damage_Text_Styles.md">Damage Text Styles</a> • <a href="../System_and_Engine/Difficulties.md">Difficulties</a> • <a href="../System_and_Engine/Particles_and_VFX_Dictionary.md">Particles & VFX Dictionary</a> • <a href="../System_and_Engine/Progression_Unlocks.md">Progression Unlocks</a></td>
  </tr>
  <tr>
    <td><strong>World and Events</strong></td>
    <td><a href="../World_and_Events/Events_and_Encounters.md">Events & Encounters</a> • <a href="../World_and_Events/Furniture_and_Metaprogression.md">Furniture & Metaprogression</a> • <a href="../World_and_Events/House_and_Environment.md">House & Environment</a> • <a href="../World_and_Events/Map_Generation_and_Routing.md">Map Generation & Routing</a> • <a href="../World_and_Events/NPC_Scripts.md">NPC Scripts</a> • <a href="../World_and_Events/Shops.md">Shops</a></td>
  </tr>
</table>

</details>

## File: `damage_text_styles.gon`

### `health_damage`
**Source:** `damage_text_styles.gon`  

```
health_damage {
	color [.74 .39 .39]
}
```

---

### `shield_damage`
**Source:** `damage_text_styles.gon`  

```
shield_damage {
	color gray
	right_icon shield
}
```

---

### `divineshield_damage`
**Source:** `damage_text_styles.gon`  

```
divineshield_damage {
	color [.39 .74 .71]
	right_icon divineshield
}
```

---

### `shield_loss`
**Source:** `damage_text_styles.gon`  

```
shield_loss {
	color gray
	right_icon shield
}
```

---

### `divineshield_loss`
**Source:** `damage_text_styles.gon`  

```
divineshield_loss {
	color [.39 .74 .71]
	right_icon divineshield
}
```

---

### `damagescale_thresholds`
**Source:** `damage_text_styles.gon`  

```
damagescale_thresholds [
	[0  damagescale_zero]
	[1  damagescale_small]
	[5  damagescale_medium]
	[10 damagescale_large]
	[25 damagescale_extreme]
]
```

---

### `damagescale_zero`
**Source:** `damage_text_styles.gon`  

```
damagescale_zero {
	color gray
}
```

---

### `damagescale_small`
**Source:** `damage_text_styles.gon`  

```
damagescale_small {
	scale .75
}
```

---

### `damagescale_medium`
**Source:** `damage_text_styles.gon`  

```
damagescale_medium {
	scale 1
}
```

---

### `damagescale_large`
**Source:** `damage_text_styles.gon`  

```
damagescale_large {
	scale 1.33
}
```

---

### `damagescale_extreme`
**Source:** `damage_text_styles.gon`  

```
damagescale_extreme {
	scale 1.66
}
```

---

### `crit`
**Source:** `damage_text_styles.gon`  

```
crit {
	suffix "!!!"
}
```

---

### `miss`
**Source:** `damage_text_styles.gon`  

```
miss {
	color gray
}
```

---

### `blocked`
**Source:** `damage_text_styles.gon`  

```
blocked {
	color gray
}
```

---

### `health_gain`
**Source:** `damage_text_styles.gon`  

```
health_gain {
	color white
    right_icon heal
}
```

---

### `shield_gain`
**Source:** `damage_text_styles.gon`  

```
shield_gain {
	color [.75 .75 .75]
	right_icon shield
}
```

---

### `divineshield_gain`
**Source:** `damage_text_styles.gon`  

```
divineshield_gain {
	color [.39 .74 .71]
	right_icon divineshield
}
```

---

### `mana_gain`
**Source:** `damage_text_styles.gon`  

```
mana_gain {
	color [.63 .73 .94]
	right_icon mana
}
```

---

### `mana_loss`
**Source:** `damage_text_styles.gon`  

```
mana_loss {
	color [.60 .45 .74]
	right_icon mana
}
```

---

### `coin_gain`
**Source:** `damage_text_styles.gon`  

```
coin_gain {
	color [.74 .58 .37]
	right_icon coin
}
```

---

### `injury`
**Source:** `damage_text_styles.gon`  

```
injury {
	color [.32 .10 .10]
}
```

---

### `injury_heal`
**Source:** `damage_text_styles.gon`  

```
injury_heal {
	color [.80 .50 .50]
}
```

---

### `equipment_broke`
**Source:** `damage_text_styles.gon`  

```
equipment_broke {
	color gray
}
```

---

### `run_away`
**Source:** `damage_text_styles.gon`  

```
run_away {
	color [.91 .83 .83]
}
```

---

### `gained_disorder`
**Source:** `damage_text_styles.gon`  

```
gained_disorder {
	color black
	outline_color white
}
```

---

### `caught_disease`
**Source:** `damage_text_styles.gon`  

```
caught_disease {
	color black
	outline_color white
}
```

---

### `cured_disease`
**Source:** `damage_text_styles.gon`  

```
cured_disease {
	color [.80 .99 .74]
}
```

---

### `caught_fire`
**Source:** `damage_text_styles.gon`  

```
caught_fire {
	color [.76 .43 .21]
}
```

---

### `damagesource_poison`
**Source:** `damage_text_styles.gon`  

```
damagesource_poison {
	back_icon poison
	color [.27 .47 .18]
}
```

---

### `damagesource_burn`
**Source:** `damage_text_styles.gon`  

```
damagesource_burn {
	back_icon burn
	color [.76 .43 .21]
}
```

---

### `damagesource_bleed`
**Source:** `damage_text_styles.gon`  

```
damagesource_bleed {
	back_icon bleed
	color [.54 .12 .12]
}
```

---

### `damagesource_thorns`
**Source:** `damage_text_styles.gon`  

```
damagesource_thorns {
	back_icon thorns
}
```

---

### `damagesource_leech`
**Source:** `damage_text_styles.gon`  

```
damagesource_leech {
	back_icon leech
}
```

---

### `damagesource_manaleech`
**Source:** `damage_text_styles.gon`  

```
damagesource_manaleech {
	back_icon mana_leech
}
```

---

### `damagesource_knockback`
**Source:** `damage_text_styles.gon`  

```
damagesource_knockback {
	back_icon knockback
}
```

---

### `damagesource_confusion`
**Source:** `damage_text_styles.gon`  

```
damagesource_confusion {
	back_icon confusion
}
```

---

### `status_default`
**Source:** `damage_text_styles.gon`  

```
status_default {
	color white
}
```

---

### `status_stunned`
**Source:** `damage_text_styles.gon`  

```
status_stunned {
}
```

---

### `status_immobile`
**Source:** `damage_text_styles.gon`  

```
status_immobile {
}
```

---

### `status_frozen`
**Source:** `damage_text_styles.gon`  

```
status_frozen {
}
```

---

### `status_petrified`
**Source:** `damage_text_styles.gon`  

```
status_petrified {
}
```

---

### `status_mad`
**Source:** `damage_text_styles.gon`  

```
status_mad {
}
```

---

### `status_sleeping`
**Source:** `damage_text_styles.gon`  

```
status_sleeping {
}
```

---

### `status_exerted`
**Source:** `damage_text_styles.gon`  

```
status_exerted {
}
```

---

### `status_fear`
**Source:** `damage_text_styles.gon`  

```
status_fear {
}
```

---

### `status_confused`
**Source:** `damage_text_styles.gon`  

```
status_confused {
}
```

---

### `status_hurt_confusion`
**Source:** `damage_text_styles.gon`  

```
status_hurt_confusion {
}
```

---

### `status_breakfree`
**Source:** `damage_text_styles.gon`  

```
status_breakfree {
}
```

---

### `status_charged`
**Source:** `damage_text_styles.gon`  

```
status_charged {
}
```

---

### `status_exhausted`
**Source:** `damage_text_styles.gon`  

```
status_exhausted {
}
```

---

### `status_rot`
**Source:** `damage_text_styles.gon`  

```
status_rot {
}
```

---

### `status_study`
**Source:** `damage_text_styles.gon`  

```
status_study {
}
```

---

### `status_takeaim`
**Source:** `damage_text_styles.gon`  

```
status_takeaim {
}
```

---

### `status_losetakeaim`
**Source:** `damage_text_styles.gon`  

```
status_losetakeaim {
}
```

---

### `status_holster`
**Source:** `damage_text_styles.gon`  

```
status_holster {
}
```

---

### `status_catch_projectile`
**Source:** `damage_text_styles.gon`  

```
status_catch_projectile {
}
```

---

### `status_reload`
**Source:** `damage_text_styles.gon`  

```
status_reload {
}
```

---

### `status_reload_move`
**Source:** `damage_text_styles.gon`  

```
status_reload_move {
}
```

---

### `status_rebirth`
**Source:** `damage_text_styles.gon`  

```
status_rebirth {
}
```

---

### `status_countered`
**Source:** `damage_text_styles.gon`  

```
status_countered {
}
```

---

### `status_energized`
**Source:** `damage_text_styles.gon`  

```
status_energized {
}
```

---

### `status_bugbite`
**Source:** `damage_text_styles.gon`  

```
status_bugbite {
}
```

---

### `status_burn`
**Source:** `damage_text_styles.gon`  

```
status_burn {
}
```

---

### `status_poison`
**Source:** `damage_text_styles.gon`  

```
status_poison {
}
```

---

### `status_bleed`
**Source:** `damage_text_styles.gon`  

```
status_bleed {
}
```

---

### `status_hex`
**Source:** `damage_text_styles.gon`  

```
status_hex {
}
```

---

### `status_leech`
**Source:** `damage_text_styles.gon`  

```
status_leech {
}
```

---

### `status_manaleech`
**Source:** `damage_text_styles.gon`  

```
status_manaleech {
}
```

---

