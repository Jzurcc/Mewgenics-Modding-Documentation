# Enemy AI Directory

## File: `decision_presets.gon`

### `default`
**Source:** `decision_presets.gon`  

```
default {
    damage_ally -1
    damage_enemy 1
    heal_ally 1
    heal_enemy -1
    
    kill_enemy 0
    kill_ally  0
    
    debuff_ally -1
    buff_ally 1
    debuff_enemy 1
    buff_enemy -1
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 1
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `default_no_revive`
**Source:** `decision_presets.gon`  

```
default_no_revive {
    damage_ally -1
    damage_enemy 1
    heal_ally 1
    heal_enemy -1
    
    kill_enemy 0
    kill_ally  0
    
    debuff_ally -1
    buff_ally 1
    debuff_enemy 1
    buff_enemy -1
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 0
    revive_enemy_corpse 0
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `careless`
**Source:** `decision_presets.gon`  

```
careless {
    damage_ally 0
    damage_enemy 1
    heal_ally 1
    heal_enemy 0
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally 0
    buff_ally 1
    debuff_enemy 1
    buff_enemy 0
    
    damage_self -1
    heal_self 0
    buff_self 0
    debuff_self -1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 1
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally 0
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `extra_careless`
**Source:** `decision_presets.gon`  

```
extra_careless {
    damage_ally 0
    damage_enemy 1
    heal_ally 1
    heal_enemy 0
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally 0
    buff_ally 1
    debuff_enemy 1
    buff_enemy 0
    
    damage_self 0
    heal_self 0
    buff_self 0
    debuff_self 0
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 1
    revive_enemy_corpse 0
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally 0
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `angry`
**Source:** `decision_presets.gon`  

```
angry {
    damage_ally 0
    damage_enemy 1
    heal_ally 0
    heal_enemy 0
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally 0
    buff_ally 0
    debuff_enemy 1
    buff_enemy 0
    
    damage_self -1
    heal_self 0
    buff_self 0
    debuff_self -1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 0
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally 0
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `spawn_randomly`
**Source:** `decision_presets.gon`  

```
spawn_randomly {
    damage_ally -1
    damage_enemy 1
    heal_ally 1
    heal_enemy -1
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally -1
    buff_ally 1
    debuff_enemy 1
    buff_enemy -1
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 1
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy 0
    spawn_object_distance_to_ally 0
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `heal_others`
**Source:** `decision_presets.gon`  

```
heal_others {
    damage_ally -1
    damage_enemy 1
    heal_ally 100
    heal_enemy -1
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally -1
    buff_ally 1
    debuff_enemy 1
    buff_enemy -1
    
    damage_self -0.1
    heal_self -100
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 100
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `always_cast`
**Source:** `decision_presets.gon`  

```
always_cast {
    damage_ally -1
    damage_enemy 1
    heal_ally 1
    heal_enemy -1
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally -1
    buff_ally 1
    debuff_enemy 1
    buff_enemy -1
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 1
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99

    flat_cast_bonus 99999
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `always_cast_careless`
**Source:** `decision_presets.gon`  

```
always_cast_careless {
    damage_ally 0
    damage_enemy 1
    heal_ally 1
    heal_enemy 0
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally 0
    buff_ally 1
    debuff_enemy 1
    buff_enemy 0
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 1
    revive_enemy_corpse 0
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99

    flat_cast_bonus 99999
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `simple`
**Source:** `decision_presets.gon`  

```
simple {
    damage_ally 0
    damage_enemy 1
    heal_ally 1
    heal_enemy 0
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally 0
    buff_ally 1
    debuff_enemy 1
    buff_enemy 0
    
    damage_self 0
    heal_self 0
    buff_self 0
    debuff_self 0
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 1
    revive_enemy_corpse 0
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally 0
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage false
    consider_secondary_damage false
    accurate_knockback false
    consider_overkill true
    simple true
    consider_aoe false
}
```

---

### `semi_simple`
**Source:** `decision_presets.gon`  

```
semi_simple {
    damage_ally 0
    damage_enemy 1
    heal_ally 1
    heal_enemy 0
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally 0
    buff_ally 1
    debuff_enemy 1
    buff_enemy 0
    
    damage_self 0
    heal_self 0
    buff_self 0
    debuff_self 0
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 1
    revive_enemy_corpse 0
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally 0
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage false
    accurate_knockback false
    consider_overkill true
    simple true
    consider_aoe true
}
```

---

### `rabies_any`
**Source:** `decision_presets.gon`  

```
rabies_any {
    damage_ally 1
    damage_enemy 1
    heal_ally 1
    heal_enemy 1
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally 1
    buff_ally 1
    debuff_enemy 1
    buff_enemy 1
    
    damage_self -1.1
    heal_self 0
    buff_self 0
    debuff_self -1.1
    
    damage_ally_corpse 1
    damage_enemy_corpse 1
    revive_ally_corpse 1
    revive_enemy_corpse 1
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally -.01
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `rabies_enemy`
**Source:** `decision_presets.gon`  

```
rabies_enemy {
    damage_ally 0
    damage_enemy 1
    heal_ally 1
    heal_enemy 0
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally 0
    buff_ally 1
    debuff_enemy 1
    buff_enemy 0
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 1
    revive_ally_corpse 1
    revive_enemy_corpse 0
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally 0
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `prioritize_healing`
**Source:** `decision_presets.gon`  

```
prioritize_healing {
    damage_ally -1
    damage_enemy 1
    heal_ally 10
    heal_enemy -1
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally -1
    buff_ally 10
    debuff_enemy 1
    buff_enemy -1
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 10
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `blind`
**Source:** `decision_presets.gon`  

```
blind {
    damage_ally 0
    damage_enemy 0
    heal_ally 0
    heal_enemy 0
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally 0
    buff_ally 0
    debuff_enemy 0
    buff_enemy 0
    
    damage_self 0
    heal_self 0
    buff_self 0
    debuff_self 0
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 0
    revive_enemy_corpse 0
    
    spawn_object 0
    spawn_object_distance_to_enemy 0
    spawn_object_distance_to_ally 0
    
    negative_weight_scale .99
    spend_mana_scale .99

    flat_cast_bonus 99999
    
    consider_total_damage false
    consider_secondary_damage false
    accurate_knockback false
    consider_overkill false
}
```

---

### `default_ignore_selfdamage`
**Source:** `decision_presets.gon`  

```
default_ignore_selfdamage {
    damage_ally -1
    damage_enemy 1
    heal_ally 1
    heal_enemy -1
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally -1
    buff_ally 1
    debuff_enemy 1
    buff_enemy -1
    
    damage_self 0
    heal_self 0
    buff_self 0
    debuff_self 0
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 1
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `nubs_fakeblind`
**Source:** `decision_presets.gon`  

```
nubs_fakeblind {
    damage_ally 0
    damage_enemy 1
    heal_ally 0
    heal_enemy 0
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally 0
    buff_ally 0
    debuff_enemy 0
    buff_enemy 0
    
    damage_self 0
    heal_self 0
    buff_self 0
    debuff_self 0
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 0
    revive_enemy_corpse 0
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally 0
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage false
    consider_secondary_damage false
    accurate_knockback false
    consider_overkill true
}
```

---

### `zombie`
**Source:** `decision_presets.gon`  

```
zombie {
    damage_ally -1
    damage_enemy 1
    heal_ally 1
    heal_enemy -1
    
    kill_enemy 0
    kill_ally  0
    
    debuff_ally -1
    buff_ally 1
    debuff_enemy 1
    buff_enemy -1
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 100
    damage_enemy_corpse 100
    revive_ally_corpse 0
    revive_enemy_corpse 0
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `reaper`
**Source:** `decision_presets.gon`  

```
reaper {
    damage_ally -1
    damage_enemy 1
    heal_ally 1
    heal_enemy -1
    
    kill_enemy .2
    kill_ally 0
    
    debuff_ally -1
    buff_ally 1
    debuff_enemy 1
    buff_enemy -1
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse .1
    revive_ally_corpse 1
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99

    flat_cast_bonus 99999
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `default_spawn_at_preferred_distance`
**Source:** `decision_presets.gon`  

```
default_spawn_at_preferred_distance {
    damage_ally -1
    damage_enemy 1
    heal_ally 1
    heal_enemy -1
    
    kill_enemy 0
    kill_ally  0
    
    debuff_ally -1
    buff_ally 1
    debuff_enemy 1
    buff_enemy -1
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 1
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    spawn_object_preferred_distance 4
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `peashy`
**Source:** `decision_presets.gon`  

```
peashy {
    damage_ally .5
    damage_enemy 1
    heal_ally 1
    heal_enemy -1
    
    kill_enemy 50
    kill_ally  40
    
    debuff_ally .5
    buff_ally 1
    debuff_enemy 1
    buff_enemy -1
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 1
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `peashy_rage`
**Source:** `decision_presets.gon`  

```
peashy_rage {
    damage_ally 0
    damage_enemy 1
    heal_ally 1
    heal_enemy -1
    
    kill_enemy 50
    kill_ally  40
    
    debuff_ally 0
    buff_ally 1
    debuff_enemy 1
    buff_enemy -1
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 1
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `dustdevil`
**Source:** `decision_presets.gon`  

```
dustdevil { //numbers multiplied by 100 so DustDash "favor tile far away" is more of a tiebreaker than a decider
    damage_ally -100
    damage_enemy 100
    heal_ally 100
    heal_enemy -100
    
    kill_enemy 0
    kill_ally  0
    
    debuff_ally -100
    buff_ally 100
    debuff_enemy 100
    buff_enemy -100
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 100
    revive_enemy_corpse -100
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `util_target_enemies`
**Source:** `decision_presets.gon`  

```
util_target_enemies {
    damage_ally 0
    damage_enemy 1
    heal_ally 0
    heal_enemy 0
    
    kill_enemy 0
    kill_ally  0
    
    debuff_ally 0
    buff_ally 0
    debuff_enemy 1
    buff_enemy 0
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 0
    revive_enemy_corpse 0
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `util_target_allies`
**Source:** `decision_presets.gon`  

```
util_target_allies {
    damage_ally 0
    damage_enemy 0
    heal_ally 1
    heal_enemy 0
    
    kill_enemy 0
    kill_ally  0
    
    debuff_ally 0
    buff_ally 1
    debuff_enemy 0
    buff_enemy 0
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 0
    revive_enemy_corpse 0
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `cop`
**Source:** `decision_presets.gon`  

```
cop {
    damage_ally -1
    damage_enemy 1
    heal_ally 1
    heal_enemy -1
    
    kill_enemy 0
    kill_ally  0
    
    debuff_ally -1
    buff_ally 1
    debuff_enemy 1
    buff_enemy -1
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 999
    revive_ally_corpse 1
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `teslacoil`
**Source:** `decision_presets.gon`  

```
teslacoil {
    damage_ally 1
    damage_enemy 1
    heal_ally 0
    heal_enemy 0
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally 0
    buff_ally 0
    debuff_enemy 0
    buff_enemy 0
    
    damage_self 0
    heal_self 0
    buff_self 0
    debuff_self 0
    
    damage_ally_corpse 1
    damage_enemy_corpse 1
    revive_ally_corpse 0
    revive_enemy_corpse 0
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally 0
    
    negative_weight_scale .99
    spend_mana_scale .99

    flat_cast_bonus 99999
    
    consider_total_damage false
    consider_secondary_damage false
    accurate_knockback false
    consider_overkill true
    simple true
    consider_aoe false
}
```

---

### `no_act`
**Source:** `decision_presets.gon`  

```
no_act {
    damage_ally 0
    damage_enemy 0
    heal_ally 0
    heal_enemy 0
    
    kill_enemy 0
    kill_ally  0
    
    debuff_ally 0
    buff_ally 0
    debuff_enemy 0
    buff_enemy 0
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 0
    revive_enemy_corpse 0
    
    spawn_object 0
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `spawn_far`
**Source:** `decision_presets.gon`  

```
spawn_far {
    damage_ally -1
    damage_enemy 1
    heal_ally 1
    heal_enemy -1
    
    kill_enemy 0
    kill_ally  0
    
    debuff_ally -1
    buff_ally 1
    debuff_enemy 1
    buff_enemy -1
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 1
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy 1
    spawn_object_distance_to_ally -.0001
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `terminator`
**Source:** `decision_presets.gon`  

```
terminator {
    damage_ally -1
    damage_enemy 1
    heal_ally 1
    heal_enemy -1
    
    kill_enemy 100
    kill_ally  0
    
    debuff_ally -1
    buff_ally 1
    debuff_enemy 1
    buff_enemy -1
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0.1
    revive_ally_corpse 1
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy 0
    spawn_object_distance_to_ally 0
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `dybbuk_suicidal`
**Source:** `decision_presets.gon`  

```
dybbuk_suicidal { //extra careless but weights for damage self and spawn object turned off
    damage_ally 0
    damage_enemy 1
    heal_ally 1
    heal_enemy 0
    
    kill_enemy 0
    kill_ally 0
    
    debuff_ally 0
    buff_ally 1
    debuff_enemy 1
    buff_enemy 0
    
    damage_self 2
    heal_self -1
    buff_self -1
    debuff_self 2
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 1
    revive_enemy_corpse 0
    
    spawn_object 0
    spawn_object_distance_to_enemy 0
    spawn_object_distance_to_ally 0
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

### `default_t3hitler`
**Source:** `decision_presets.gon`  

```
default_t3hitler {
    damage_ally -1
    damage_enemy 1
    heal_ally 1
    heal_enemy -1
    
    kill_enemy 0
    kill_ally  0
    
    debuff_ally -1
    buff_ally 1
    debuff_enemy 1
    buff_enemy -1
    
    damage_self -0.1
    heal_self 0
    buff_self 0
    debuff_self -0.1
    
    damage_ally_corpse 0
    damage_enemy_corpse 0
    revive_ally_corpse 1
    revive_enemy_corpse -1
    
    spawn_object 1
    spawn_object_distance_to_enemy -.01
    spawn_object_distance_to_ally .0001
    spawn_object_preferred_distance 5
    
    negative_weight_scale .99
    spend_mana_scale .99
    
    consider_total_damage true
    consider_secondary_damage true
    accurate_knockback false
    consider_overkill true
}
```

---

## File: `move_presets.gon`

### `keep_distance`
**Source:** `move_presets.gon`  

```
keep_distance {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance mov
    total_distance_moved -0.01
    face_closest_enemy 1
}
```

---

### `stay_close`
**Source:** `move_presets.gon`  

```
stay_close {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved -0.01
    face_closest_enemy 1
}
```

---

### `keep_distance_always_move`
**Source:** `move_presets.gon`  

```
keep_distance_always_move {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance mov
    total_distance_moved 0.01
    face_closest_enemy 1
}
```

---

### `minimum_move`
**Source:** `move_presets.gon`  

```
minimum_move {
    distance_to_enemy 0
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved -1
    face_closest_enemy 1
}
```

---

### `stay_close_always_move`
**Source:** `move_presets.gon`  

```
stay_close_always_move {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 0.01
    face_closest_enemy 1
}
```

---

### `stay_far`
**Source:** `move_presets.gon`  

```
stay_far {
    distance_to_enemy 1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved -0.01
    face_closest_enemy 1
}
```

---

### `stay_far_always_move`
**Source:** `move_presets.gon`  

```
stay_far_always_move {
    distance_to_enemy 1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 0.01
    face_closest_enemy 1
}
```

---

### `stay_far_move_far`
**Source:** `move_presets.gon`  

```
stay_far_move_far {
    distance_to_enemy 1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 10
    face_closest_enemy 1
}
```

---

### `stay_close_move_far`
**Source:** `move_presets.gon`  

```
stay_close_move_far {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 10
    face_closest_enemy 1
}
```

---

### `random`
**Source:** `move_presets.gon`  

```
random {
    distance_to_enemy 0
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 0
    face_closest_enemy 0
}
```

---

### `chaotic_runaway`
**Source:** `move_presets.gon`  

```
chaotic_runaway {
    distance_to_enemy 0
    distance_to_ally 0
    distance_to_character 1
    preferred_distance 0
    total_distance_moved .5
    face_closest_enemy 1
}
```

---

### `chaotic`
**Source:** `move_presets.gon`  

```
chaotic {
    distance_to_enemy 0
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 1
    face_closest_enemy 1
}
```

---

### `blind_move_far`
**Source:** `move_presets.gon`  

```
blind_move_far {
    distance_to_enemy 0
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 1
    face_closest_enemy 0
}
```

---

### `keep_far_distance`
**Source:** `move_presets.gon`  

```
keep_far_distance {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance mov+5
    total_distance_moved 0.01
    face_closest_enemy 1
}
```

---

### `keep_ranged_distance`
**Source:** `move_presets.gon`  

```
keep_ranged_distance {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance reach
    total_distance_moved 0.01
    face_closest_enemy 1
}
```

---

### `keep_max_ranged_distance`
**Source:** `move_presets.gon`  

```
keep_max_ranged_distance {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance mov+reach
    total_distance_moved 0.01
    face_closest_enemy 1
}
```

---

### `rabies_any`
**Source:** `move_presets.gon`  

```
rabies_any {
    distance_to_enemy 0
    distance_to_ally 0
    distance_to_character -1
    preferred_distance 0
    total_distance_moved 0
    face_closest_enemy 0
}
```

---

### `rabies_enemy`
**Source:** `move_presets.gon`  

```
rabies_enemy {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 0
    face_closest_enemy 0
}
```

---

### `prefer_tall_grass_always_move`
**Source:** `move_presets.gon`  

```
prefer_tall_grass_always_move {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance mov
    total_distance_moved 0.01
    face_closest_enemy 1
    tall_grass 5
}
```

---

### `stay_near_allies`
**Source:** `move_presets.gon`  

```
stay_near_allies {
    distance_to_enemy .01
    distance_to_ally -1
    distance_to_character 0
    preferred_distance 0
    total_distance_moved -0.001
    face_closest_enemy 1
}
```

---

### `stay_near_allies_always_move`
**Source:** `move_presets.gon`  

```
stay_near_allies_always_move {
    distance_to_enemy .01
    distance_to_ally -1
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 0.001
    face_closest_enemy 1
}
```

---

### `keep_distance_popeye`
**Source:** `move_presets.gon`  

```
keep_distance_popeye {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 3
    total_distance_moved -0.01
    face_closest_enemy 1
}
```

---

### `chubs_and_nubs_blind`
**Source:** `move_presets.gon`  

```
chubs_and_nubs_blind {
    distance_to_enemy 0
    distance_to_ally 0
    //distance_to_ally 1
    //cap_distance_to_ally 1
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 1
    face_closest_enemy 0
}
```

---

### `chubs_and_nubs_rage`
**Source:** `move_presets.gon`  

```
chubs_and_nubs_rage {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 10
    face_closest_enemy 0
    randomness 4
}
```

---

### `gunslinger_reposition`
**Source:** `move_presets.gon`  

```
gunslinger_reposition {
    distance_to_enemy 0
    distance_to_ally 0
    cap_distance_to_character 2
    distance_to_character 1
    preferred_distance 0
    total_distance_moved 1
    face_closest_enemy 0
}
```

---

### `stay_near_allies_siren`
**Source:** `move_presets.gon`  

```
stay_near_allies_siren {
    distance_to_enemy .01
    distance_to_ally -1
    distance_to_character 0
    preferred_distance 0
    total_distance_moved -0.001
    face_closest_enemy 1
    exclude_characters_tagged siren
}
```

---

### `stay_near_map_center`
**Source:** `move_presets.gon`  

```
stay_near_map_center {
    distance_to_enemy 0
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved -0.01
    face_closest_enemy 0
    distance_to_center -1
}
```

---

### `bat_chaos_runaway`
**Source:** `move_presets.gon`  

```
bat_chaos_runaway {
    distance_to_enemy 1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 1
    face_closest_enemy 1
    randomness 6
}
```

---

### `keep_distance_always_move_towards_water`
**Source:** `move_presets.gon`  

```
keep_distance_always_move_towards_water {
    distance_to_water -1
    distance_to_enemy -.01
    distance_to_ally 0
    distance_to_character 0
    preferred_distance mov
    total_distance_moved 0.0001
    face_closest_enemy 1
}
```

---

### `keep_distance_always_move_prefer_water`
**Source:** `move_presets.gon`  

```
keep_distance_always_move_prefer_water {
    distance_to_water -.0001
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance mov
    total_distance_moved 0.01
    face_closest_enemy 1
}
```

---

### `zombie`
**Source:** `move_presets.gon`  

```
zombie {
    distance_to_enemy -1
    distance_to_corpse -100
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved -0.01
    face_closest_enemy 1
}
```

---

### `stay_close_avoid_allies`
**Source:** `move_presets.gon`  

```
stay_close_avoid_allies {
    distance_to_enemy -1
    distance_to_character 0
    preferred_distance 0
    total_distance_moved -0.01
    face_closest_enemy 1

    distance_to_ally 1
    cap_distance_to_ally 2
}
```

---

### `keep_distance_always_move_spider`
**Source:** `move_presets.gon`  

```
keep_distance_always_move_spider {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance mov+1
    total_distance_moved 0.01
    face_closest_enemy 1
}
```

---

### `keep_close_distance_always_move`
**Source:** `move_presets.gon`  

```
keep_close_distance_always_move {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance mov-2
    total_distance_moved 0.01
    face_closest_enemy 1
}
```

---

### `rattle_distance`
**Source:** `move_presets.gon`  

```
rattle_distance {
    distance_to_enemy -1
    cap_distance_to_enemy 2
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 2
    total_distance_moved -0.01
    face_closest_enemy 1
}
```

---

### `dustdevil`
**Source:** `move_presets.gon`  

```
dustdevil {
    distance_to_enemy 0
    distance_to_ally 1
    cap_distance_to_ally 4
    distance_to_character 0
    preferred_distance 0
    total_distance_moved -0.01
    face_closest_enemy 1
}
```

---

### `bird`
**Source:** `move_presets.gon`  

```
bird {
    distance_to_enemy 1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 1
    cap_total_distance_moved 1
    face_closest_enemy 1
}
```

---

### `stay_close_lenny`
**Source:** `move_presets.gon`  

```
stay_close_lenny {
    distance_to_enemy -1
    distance_to_ally -.1
    distance_to_corpse -.1
    distance_to_character 0
    preferred_distance 0
    total_distance_moved -0.01
    face_closest_enemy 1
}
```

---

### `security_bot`
**Source:** `move_presets.gon`  

```
security_bot {
    distance_to_enemy -.5
    distance_to_ally -1
    cap_distance_to_ally 2
    distance_to_character 0
    preferred_distance 3
    total_distance_moved -0.01
    face_closest_enemy 1
}
```

---

### `wash_johnny`
**Source:** `move_presets.gon`  

```
wash_johnny {
    distance_to_enemy 0
    distance_to_ally -1
    distance_to_character 0
    preferred_distance 0
    total_distance_moved -0.001
    face_closest_enemy 0
    face_aggro_target 1
}
```

---

### `prefer_lava_always_move`
**Source:** `move_presets.gon`  

```
prefer_lava_always_move {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance mov
    total_distance_moved 0.01
    face_closest_enemy 1
    lava 5
}
```

---

### `semi_blind`
**Source:** `move_presets.gon`  

```
semi_blind {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 0.01
    face_closest_enemy 0
    randomness 50
}
```

---

### `towards_aggro`
**Source:** `move_presets.gon`  

```
towards_aggro {
    distance_to_enemy 0
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved -0.01
    face_closest_enemy 0
    distance_to_aggro_target -1
}
```

---

### `util_minmove`
**Source:** `move_presets.gon`  

```
util_minmove {
    distance_to_enemy 0
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved -1
    face_closest_enemy 0
}
```

---

### `stay_close_move_if_possible`
**Source:** `move_presets.gon`  

```
stay_close_move_if_possible {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved -0.01
    face_closest_enemy 1
    count_nomove_in_eval false
}
```

---

### `towards_aggro_stay_close`
**Source:** `move_presets.gon`  

```
towards_aggro_stay_close {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved -0.01
    face_closest_enemy 1
    face_aggro_target 10
    distance_to_aggro_target -10
    consider_aggro_target_enemy true
}
```

---

### `keep_distance_face_camera`
**Source:** `move_presets.gon`  

```
keep_distance_face_camera {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance mov
    total_distance_moved -0.01
    face_closest_enemy 1
    face_camera 1000
}
```

---

### `trampy_chaos`
**Source:** `move_presets.gon`  

```
trampy_chaos {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance mov
    total_distance_moved -0.01
    face_closest_enemy 1
    randomness 6
}
```

---

### `stay_close_ish`
**Source:** `move_presets.gon`  

```
stay_close_ish {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 0.1
    face_closest_enemy 1
    randomness 6
}
```

---

### `terminator_stay_close`
**Source:** `move_presets.gon`  

```
terminator_stay_close {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved -0.01
    face_closest_enemy 1
    danger_avoidance .1
}
```

---

### `terminator_keep_distance_always_move`
**Source:** `move_presets.gon`  

```
terminator_keep_distance_always_move {
    distance_to_enemy -1
    distance_to_ally 0
    distance_to_character 0
    preferred_distance mov
    total_distance_moved 0.01
    face_closest_enemy 1
    danger_avoidance 20
}
```

---

### `run_far`
**Source:** `move_presets.gon`  

```
run_far {
    distance_to_enemy 0
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 1
    face_closest_enemy 1
}
```

---

### `stay_close_g3`
**Source:** `move_presets.gon`  

```
stay_close_g3 {
    distance_to_aggro_target -1
    distance_to_enemy 0
    distance_to_ally 0
    distance_to_corpse 0
    distance_to_character 0
    preferred_distance 1
    total_distance_moved -0.01
    face_closest_enemy 1
}
```

---

### `drmangler`
**Source:** `move_presets.gon`  

```
drmangler {
    distance_to_enemy 1
    distance_to_ally 2
    cap_distance_to_ally 7
    cap_distance_to_enemy 5
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 0.01
    face_closest_enemy 1
    danger_avoidance 1000
}
```

---

### `chaos_always_move`
**Source:** `move_presets.gon`  

```
chaos_always_move {
    distance_to_enemy 0
    distance_to_ally 0
    distance_to_character 0
    preferred_distance 0
    total_distance_moved 100
    face_closest_enemy 1
}
```

---

