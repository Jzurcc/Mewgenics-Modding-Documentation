# System and Engine/Particles and VFX Dictionary Directory

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
    <td><a href="../Statuses_and_Injuries/Disorders.md">Disorders</a> • <a href="../Statuses_and_Injuries/Injuries.md">Injuries</a> • <a href="../Statuses_and_Injuries/Status_Effect_Keywords.md">Status Effect Keywords</a> • <a href="../Statuses_and_Injuries/Statuses.md">Statuses</a></td>
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

## File: `particles.gon`

### `test`
**Source:** `particles.gon`  

```
test {
    movieclip ParticleTestNoRandom
    
    render_mode default
    //render_mode separate
    
    //update_mode locked
    
    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 240
    emit_amount 1
    emit_direction [0, 1, 0]
    friction [.1 .1 .1]
    emit_spread 180//30
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [.1 2]
    speed_start 4
    //speed_end 5
    //force_start [0 -70 0]
    //force_end [0 90 0]
    //rotation_start [0, 360]
    //rotation_speed_start [-900, 900]
    //rotation_speed_end 0
    size_start [.1 1]
    size_end .2
    alpha_start 2
    alpha_end 0
    speed_scale .1
    inherit_speed 1//.21
    face_moving_direction true
}
```

---

### `test2`
**Source:** `particles.gon`  

```
test2 {
    movieclip ParticleTestNoRandom
    
    render_mode default
   // render_mode separate
    
    //update_mode locked
    
    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    //flat_movement true

    
    emit_rate 24000
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 30
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  1
    speed_start 11
    //speed_end 5
    force_start [0 -70 0]
    force_end [0 90 0]
    //rotation_start [0, 360]
    //rotation_speed_start [-900, 900]
    //rotation_speed_end 0
    size_start .1
    size_end .2
    alpha_start 2
    alpha_end 0
    speed_scale .2
    face_moving_direction true
}
```

---

### `FinalEvaporate`
**Source:** `particles.gon`  

```
FinalEvaporate {
    combo [FevaporateLight FevaporateDark]
}
```

---

### `FevaporateLight`
**Source:** `particles.gon`  

```
FevaporateLight {
    movieclip DissolveParticle
    
    render_mode default
   // render_mode separate
    
    //update_mode locked
    
    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    //flat_movement true

    
    emit_rate 400
    emit_amount 1
    emit_direction [0, -1, 0]
    emit_spread 10
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  1
    speed_start 14
    //speed_end 5
    force_start [0 100 0]
    force_end [0 70 0]
    //rotation_start [0, 360]
    //rotation_speed_start [-900, 900]
    //rotation_speed_end 0
    size_start [.2 1.2]
    size_end .1
    alpha_start 1
    alpha_end 1
    speed_scale [0 1.6]
    face_moving_direction true
}
```

---

### `FevaporateDark`
**Source:** `particles.gon`  

```
FevaporateDark {
    movieclip DissolveDark
    
    render_mode default
   // render_mode separate
    
    //update_mode locked
    
    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    //flat_movement true

    
    emit_rate 400
    emit_amount 1
    emit_direction [0, -1, 0]
    emit_spread 7
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime .5
    speed_start 14
    //speed_end 5
    force_start [150 70 150]
    force_end [0 70 0]
    //rotation_start [0, 360]
    //rotation_speed_start [-900, 900]
    //rotation_speed_end 0
    size_start [3 5]
    size_end .1
    alpha_start 2
    alpha_end 0
    speed_scale 1
    face_moving_direction true
}
```

---

### `test3`
**Source:** `particles.gon`  

```
test3 {
    movieclip ParticleTestNoRandom
    
    render_mode default
    //render_mode separate
    
    //update_mode locked
    
    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 2400
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 30
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  1
    speed_start 15
    //speed_end 5
    force_start [0 -70 0]
    //rotation_start [0, 360]
    //rotation_speed_start [-900, 900]
    //rotation_speed_end 0
    size_start .1
    size_end .2
    alpha_start 2
    alpha_end 0
    speed_scale .2
    face_moving_direction true
    
    scripts {
        ParticleBouncePlane {
            dampening .25
        }
    }
}
```

---

### `test4`
**Source:** `particles.gon`  

```
test4 {
    movieclip ParticleTestNoRandom
    
    render_mode default
    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 240
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_radius 5
    friction [.2 .2 .2]
    emit_spread 180
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  .5
    speed_start 0
    //speed_end 5

    rotation_start [0, 360]
    rotation_speed_start [-900, 900]
    //rotation_speed_end 0
    size_start [1 3]
    size_end 0
    alpha_start 0
    alpha_end 2
    //speed_scale .5
    face_moving_direction false
    
    scripts {
        ParticleAttractor 100
    }
}
```

---

### `test5`
**Source:** `particles.gon`  

```
test5 {
    movieclip ParticleTestNoRandom
    
    render_mode default
   // render_mode separate //37 fps
    
    //update_mode locked
    
    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 2400
    emit_amount 1
    emit_direction [0, 1, 0]
    //friction [.1 .1 .1]
    emit_spread 180
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  3
    speed_start 10
    //speed_end 5

    //rotation_start [0, 360]
    //rotation_speed_start [-900, 900]
    //rotation_speed_end 0
    size_start .1
    size_end .2
    alpha_start 1
    alpha_end 0
    speed_scale .5
    face_moving_direction true
    
    scripts {
        ParticleAttractor {
            towards [5 0 5]
            force 100
        }
    }
}
```

---

### `test6`
**Source:** `particles.gon`  

```
test6 {
    movieclip ParticleTestNoRandom
    
    render_mode default

    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 2400
    emit_amount 1
    emit_direction [1, 0, -1]
    emit_spread 0
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  2
    speed_start 10
    //speed_end 5

    //rotation_start [0, 360]
    //rotation_speed_start [-900, 900]
    //rotation_speed_end 0
    size_start .1
    size_end .2
    alpha_start 1
    alpha_end 0
    speed_scale .5
    face_moving_direction true
    
    scripts {
        ParticleRandomForce [0, [-20, 20], 0]
        /*ParticleRandomForce { //if you want it to vary
            begin [0, [-20, 20], 0]
            end [-20, 0, 20]
        }*/
    }
}
```

---

### `test7`
**Source:** `particles.gon`  

```
test7 {
    movieclip ParticleTestNoRandom
    
    //render_mode default
    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 10
    emit_amount 1
    emit_direction [0, 1, 0]

    emit_spread 180//30
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime 1
    speed_start 2

    alpha_in .5
    alpha_out .5
    size_end 2

    face_moving_direction true
}
```

---

### `test8`
**Source:** `particles.gon`  

```
test8 {
    movieclip ParticleTestNoRandom

    render_mode separate
    simulation_space global
    max_particles 10000

    projection_matrix default
    
    emit_rate 200
    emit_amount [0 3]
    emit_direction [0, -1, 0]

    emit_spread 180
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime .025
    speed_start 40
    speed_scale .2
    size .2

    face_moving_direction true
    chain test8
    chain_chance .9
}
```

---

### `test9`
**Source:** `particles.gon`  

```
test9 {
    movieclip ParticleTestNoRandom
    
    render_mode default
    //render_mode separate
    
    //update_mode locked
    
    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate .5
    emit_amount 1000
    emit_timespread .25
    emit_timespread_curve ease_out
    emit_direction [0, 1, 0]
    friction [.1 .1 .1]
    emit_spread 30
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [.1 .5]
    speed_start 10
    //speed_end 5
    //force_start [0 -70 0]
    //force_end [0 90 0]
    //rotation_start [0, 360]
    //rotation_speed_start [-900, 900]
    //rotation_speed_end 0
    size_start [.1 1]
    size_end .2
    alpha_in .5
    alpha_out .5
    speed_scale .1
    face_moving_direction true
}
```

---

### `firework`
**Source:** `particles.gon`  

```
firework {
    movieclip ParticleTestNoRandom
    
    //render_mode default
    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    projection_matrix default
    
    emit_rate [.5, 1]
    emit_amount 1
    emit_direction [0, 1, 0]
    friction [.01 .01 .01]
    emit_spread 30
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [1 2]
    speed_start 4
    size_start 1
    speed_scale .1
    face_moving_direction true
    chain firework_burst
}
```

---

### `firework_burst`
**Source:** `particles.gon`  

```
firework_burst {
    combo [firework_bursta, firework_burstb]
}
```

---

### `firework_bursta`
**Source:** `particles.gon`  

```
firework_bursta {
    movieclip ParticleTestNoRandom
    
    //render_mode default
    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount [10, 100]
    emit_direction [0, 1, 0]
    friction [.01 .01 .01]
    emit_spread 180
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [1 2]
    speed_start [0 4]
    size_start .5
    size_end 0
    speed_scale .1
    face_moving_direction true
}
```

---

### `firework_burstb`
**Source:** `particles.gon`  

```
firework_burstb {
    movieclip ParticleTestNoRandom
    
    //render_mode default
    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount [50,100]
    emit_direction [0, 1, 0]
    friction [.1 .1 .1]
    emit_spread 180
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [1 2]
    speed_start [8 10]
    size_start .5
    size_end 0
    speed_scale .1
    face_moving_direction true
}
```

---

### `firework_burst_recursive`
**Source:** `particles.gon`  

```
firework_burst_recursive {
    movieclip ParticleTestNoRandom
    
    render_mode default
    max_particles 10000

    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount 5//[10, 100]
    emit_direction [0, 1, 0]
    friction [.01 .01 .01]
    emit_spread 180
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [1 2]
    speed_start [0 4]
    size_start .5
    //size_end .1
    speed_scale .4
    face_moving_direction true
    
    chain firework_burst_recursive
}
```

---

### `Rain`
**Source:** `particles.gon`  

```
Rain {
    movieclip RainParticle
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 200
    emit_amount 1
    emit_direction [0, -1, 0]
    //friction [.01 .01 .01]
    emit_spread 0
    live_bounds [-999 999  0 999 -999 999]
    emit_box [0 10 10 10 0 10]
    
    
    particle_lifetime  5
    speed_start 10
    size_start .5
    speed_scale .1
    alpha .5
    face_moving_direction true
    chain splash
    force [0 -10 0]

    scripts {
        ParticleGlobalForce {
            id Wind
            amount 1
        }
    }
}
```

---

### `splash`
**Source:** `particles.gon`  

```
splash {
    movieclip RainSplashParticle
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount [1 10]
    emit_direction [0, 1, 0]
    friction [.1 0 .1]
    emit_spread 180
    live_bounds [-999 999  0 999 -999 999]
    
    particle_lifetime  .5
    speed_start 4
    size_start .2
    size_end 0
    speed_scale .1
    alpha .5
    face_moving_direction true
    force [0 -20 0]
}
```

---

### `Kingblood1`
**Source:** `particles.gon`  

```
Kingblood1 {
    movieclip KingBlood1
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate [1,5]
    emit_amount [0,2]
    emit_direction [0, -1, 0]
    //friction [.01 .01 .01]
    emit_spread 0
    live_bounds [-999 999  0 999 -999 999]
    emit_box [0 .4 0 0 0 .4]
    
    
    particle_lifetime  5
    speed_start [1.7,2.4]
    size_start [.8,1.3]
    //speed_scale .1
    //alpha .5
    face_moving_direction true
    chain Kingblood2
    force [0 -1 0]

    scripts {
        ParticleGlobalForce {
            id Wind
            amount 1
        }
    }
}
```

---

### `Kingblood2`
**Source:** `particles.gon`  

```
Kingblood2 {
    movieclip KingBlood2
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount 1
    //emit_spread 180
    live_bounds [-999 999  0 999 -999 999]
    
    particle_lifetime  8
    speed_start 4
    size_start [1,1.3]
    //size_end 0
    speed_scale .1
    //alpha .5
    //face_moving_direction true
    //force [0 -20 0]
}
```

---

### `AcidRain`
**Source:** `particles.gon`  

```
AcidRain {
    movieclip AcidRainParticle
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 100
    emit_amount 1
    emit_direction [0, -1, 0]
    //friction [.01 .01 .01]
    emit_spread 0
    live_bounds [-999 999  0 999 -999 999]
    emit_box [0 10 10 10 0 10]
    
    
    particle_lifetime  5
    speed_start 10
    size_start .5
    speed_scale .1
    alpha .5
    face_moving_direction true
    chain AcidSplash
    force [0 -10 0]

    scripts {
        ParticleGlobalForce {
            id Wind
            amount 1
        }
    }
}
```

---

### `AcidSplash`
**Source:** `particles.gon`  

```
AcidSplash {
    movieclip AcidRainSplashParticle
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount [1 10]
    emit_direction [0, 1, 0]
    friction [.1 0 .1]
    emit_spread 180
    live_bounds [-999 999  0 999 -999 999]
    
    particle_lifetime  .5
    speed_start 4
    size_start .2
    size_end 0
    speed_scale .1
    alpha .5
    face_moving_direction true
    force [0 -20 0]
}
```

---

### `CaveDrip`
**Source:** `particles.gon`  

```
CaveDrip {
    movieclip RainParticle
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate [.5 5]
    emit_amount 1
    emit_direction [0, -1, 0]
    //friction [.01 .01 .01]
    emit_spread 0
    live_bounds [-999 999  0 999 -999 999]
    emit_box [0 10 10 10 0 10]
    
    
    particle_lifetime  5
    speed_start 10
    size_start .5
    speed_scale .1
    alpha .5
    face_moving_direction true
    chain CaveSplash
    force [0 -10 0]

    scripts {
        ParticleGlobalForce {
            id Wind
            amount 1
        }
    }
}
```

---

### `CaveSplash`
**Source:** `particles.gon`  

```
CaveSplash {
    movieclip RainSplashParticle
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount [15 20]
    emit_direction [0, 1, 0]
    friction [.1 0 .1]
    emit_spread 180
    live_bounds [-999 999  0 999 -999 999]
    
    particle_lifetime  .5
    speed_start 4
    size_start .2
    size_end 0
    speed_scale .1
    alpha .5
    face_moving_direction true
    force [0 -20 0]
}
```

---

### `MegaBlast`
**Source:** `particles.gon`  

```
MegaBlast {
    combo [MegaBlastA MegaBlastB]
}
```

---

### `MegaBlastA`
**Source:** `particles.gon`  

```
MegaBlastA {
    movieclip MegaBlastParticle

    render_mode separate
    
    simulation_space global
    projection_matrix default
    
    emit_rate 1000
    emit_amount 1
    emit_direction [0, 0, -1]
    friction [.2 .3 .2]
    emit_spread 50
   //live_bounds [-999 999  0 1 -999 999]
    
    particle_lifetime  [.2 .3]
    speed_start 60
    alpha_start 4
    alpha_end 0
    size_start 0
    size_end 2
    //speed_scale -.1
    face_moving_direction true
}
```

---

### `MegaBlastB`
**Source:** `particles.gon`  

```
MegaBlastB {
    movieclip MegaBlastParticle
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate 200
    emit_amount 1
    emit_direction [0, 0, -1]
    friction [0 .05 0]
    emit_spread 45
   //live_bounds [-999 999  0 1 -999 999]
    
    particle_lifetime  .35
    speed_start 15
    alpha_start 0
    alpha_end 2
    size_start 1
    size_end 0
    //speed_scale .1
    face_moving_direction true
}
```

---

### `GroundPoof`
**Source:** `particles.gon`  

```
GroundPoof {
    movieclip ParticlePuff
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount 15
    emit_direction [0, 1, 0]
    friction [.2 1 .2]
    emit_spread 180
   
    rotation [0 360]
    rotation_speed_start [-1000 1000]
    rotation_speed_end 0
    particle_lifetime  [.35 .65]
    speed_start 10
    alpha_start 1
    alpha_end 0
    size_start 0
    size_end [.5 1]
    //speed_scale .1
    //face_moving_direction true
}
```

---

### `PointPoof`
**Source:** `particles.gon`  

```
PointPoof {
    movieclip PuffNoOutline
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount [6 8]
    emit_direction [0, 1, 0]
    friction [.03 .35 .03]
    emit_spread 180
   
    rotation [0 360]
    rotation_speed_start [-1000 1000]
    rotation_speed_end 0
    particle_lifetime  [.45 .75]
    speed_start 2
    alpha_start .8
    alpha_end 0
    size_start [.2 .3]
    size_end [.7 1.3]

    force_start [0 40 0]
    force_end [0 -60 0]

}
```

---

### `SmallDirt`
**Source:** `particles.gon`  

```
SmallDirt {
    movieclip ParticleDirt
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount [2 7]
    emit_direction [0, 1, 0]
    friction [.02 .35 .02]
    emit_spread 180
    live_bounds [-999 999  0 999 -999 999]
    
    particle_lifetime  .5
    speed_start 2.5
    size_start [.4 .7]
    size_end 0
    speed_scale .1
    alpha_start [1 3]
    alpha_end 0
    face_moving_direction true

    force_start [0 150 0]
    force_end [0 -250 0]

}
```

---

### `Blood`
**Source:** `particles.gon`  

```
Blood {
    combo [BloodPoof BloodBounce]
}
```

---

### `BloodCrit`
**Source:** `particles.gon`  

```
BloodCrit {
    combo [BloodPoofCrit BloodBounceCrit BloodPopCrit]
}
```

---

### `Blood_Absorb`
**Source:** `particles.gon`  

```
Blood_Absorb {
    combo [BloodPoof_Absorb BloodBounce_Absorb]
}
```

---

### `BloodCrit_Absorb`
**Source:** `particles.gon`  

```
BloodCrit_Absorb {
    combo [BloodPoofCrit_Absorb BloodBounceCrit_Absorb BloodPopCrit_Absorb]
}
```

---

### `BloodPoof`
**Source:** `particles.gon`  

```
BloodPoof {
    movieclip ParticleBlood

    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 1
    emit_amount 20
    emit_direction [0, 1, 0]
    friction_start [.2 .2 .2]
    friction_end [1 1 1]
    emit_spread 180//30
    force_start [0 -20 0]
    force_end [0 -5 0]
    
    
    particle_lifetime  [.5 1]
    speed_start [0 10]

    size_start [.3 1]
    size_end 0
    alpha_start 2
    alpha_end 0
    speed_scale .5
    inherit_speed [5 30]//.21
    face_moving_direction true
}
```

---

### `BloodPoof_Absorb`
**Source:** `particles.gon`  

```
BloodPoof_Absorb {
    variant_of BloodPoof
    ownership local

    scripts {
        ParticleAttractor {
            force_start 0
            force_end 200
            towards [0 .5 0]
        }
    }
}
```

---

### `BloodPoofCrit`
**Source:** `particles.gon`  

```
BloodPoofCrit {
    variant_of BloodPoof

    speed_start [0 15]
}
```

---

### `BloodPoofCrit_Absorb`
**Source:** `particles.gon`  

```
BloodPoofCrit_Absorb {
    variant_of BloodPoofCrit
    ownership local

    scripts {
        ParticleAttractor {
            force_start 0
            force_end 200
            towards [0 .5 0]
        }
    }
}
```

---

### `BloodBounce`
**Source:** `particles.gon`  

```
BloodBounce {
    movieclip ParticleBlood

    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 1
    emit_amount 20
    emit_direction [0, 1, 0]
    friction [.05 .1 .05]
    emit_spread 45//30
    force_start [0 -20 0]
    
    
    particle_lifetime  [.5 1.5]
    speed_start [0 10]

    size_start [.1 .5]
    size_end 0
    alpha_start 2
    alpha_end 0
    speed_scale 1
    inherit_speed [7 12]//.21
    face_moving_direction true
    
    scripts {
        ParticleBouncePlane {
            dampening .1
        }
    }
}
```

---

### `BloodBounce_Absorb`
**Source:** `particles.gon`  

```
BloodBounce_Absorb {
    variant_of BloodBounce
    ownership local

    scripts {
        ParticleAttractor {
            force_start 0
            force_end 200
            towards [0 .5 0]
        }
    }
}
```

---

### `BloodBounceCrit`
**Source:** `particles.gon`  

```
BloodBounceCrit {
    variant_of BloodBounce

    emit_spread 90
    speed_start [0 15]
}
```

---

### `BloodBounceCrit_Absorb`
**Source:** `particles.gon`  

```
BloodBounceCrit_Absorb {
    variant_of BloodBounceCrit
    ownership local

    scripts {
        ParticleAttractor {
            force_start 0
            force_end 200
            towards [0 .5 0]
        }
    }
}
```

---

### `BloodPopCrit`
**Source:** `particles.gon`  

```
BloodPopCrit {
    movieclip ParticleBlood

    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 1
    emit_amount 20
    emit_direction [0, 1, 0]
    friction_start [0 0 0]
    friction_end [1 1 1]
    emit_spread 180//30
    
    particle_lifetime  [.1 2]
    speed_start [10 30]

    size_start [.2 .5]
    size_end 0
    alpha_start 2
    alpha_end 0
    speed_scale .5
    inherit_speed 1
    face_moving_direction true
}
```

---

### `BloodPopCrit_Absorb`
**Source:** `particles.gon`  

```
BloodPopCrit_Absorb {
    variant_of BloodPopCrit
    ownership local

    friction_end [.5 .5 .5]

    scripts {
        ParticleAttractor {
            force_start 0
            force_end 500
            towards [0 .5 0]
        }
    }
}
```

---

### `HairballTrail`
**Source:** `particles.gon`  

```
HairballTrail {
    movieclip ParticleTestNoRandom
    
    //render_mode default
    render_mode separate
    depth_bias .25
    
    //update_mode locked
    
    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 60
    emit_amount 1
    emit_direction [0, 1, 0]
    //friction [.1 .1 .1]
    emit_spread 180//30
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [.1 .4]
    speed_start 1
    //speed_end 5
    force [0 -10 0]
    //force_end [0 90 0]
    //rotation_start [0, 360]
    //rotation_speed_start [-900, 900]
    //rotation_speed_end 0
    size_start .2
    size_end .1
    alpha_start 2
    alpha_end 0
    speed_scale .5
    inherit_speed .1//.21
    face_moving_direction true
}
```

---

### `FirePlumes`
**Source:** `particles.gon`  

```
FirePlumes {
    movieclip ParticleFire1
    
    render_mode separate
    flat_movement true
    depth_bias 0.2

    simulation_space global
    projection_matrix default
    
    emit_rate 15
    emit_amount 1
    emit_direction [0, 1, 0]
    speed [0 10]
    friction [.6 .35 .6]
    emit_spread 180
   
    rotation [-10 10]
    rotation_speed_start [-20 20]
    particle_lifetime .
    size [.3 .8]

    //force[0 70 0]
    scripts {
        ParticleRandomForce [0, [40, 80], 0]
    }

    emit_box [0 0 .3 .3 0 0]

}
```

---

### `FireWaves`
**Source:** `particles.gon`  

```
FireWaves {
    movieclip ParticleFire2
    
    render_mode separate
    flat_movement true
    depth_bias 0.1

    simulation_space global
    projection_matrix default
    
    emit_rate 6
    emit_amount 1
    emit_direction [0, 1, 0]
    speed [0 .5]
    friction [.03 .35 .03]
    emit_spread 180
   
    rotation [-10 10]
    rotation_speed_start [-20 20]
    particle_lifetime 1
    size [.6 .8]

    //force[0 70 0]
    scripts {
        ParticleRandomForce [0, [10, 60], 0]
    }
    emit_box [0 0 .3 .3 0 0]
}
```

---

### `FireBase`
**Source:** `particles.gon`  

```
FireBase {
    movieclip ParticleFire3
    
    render_mode separate
    flat_movement true
    depth_bias 0

    simulation_space global
    projection_matrix default
    
    emit_rate 10
    emit_amount 1
    emit_direction [0, 1, 0]
    speed [0 10]
    friction [.55 .6 .55]
    emit_spread 180
   
    rotation [-10 10]
    rotation_speed_start [-20 20]
    particle_lifetime 1
    size [.6 .85]

    //force_start [0 -140 0]
    //force_end [0 490 0]

    scripts {
        ParticleRandomForce { //if you want it to vary
            begin [0, -20, 0]
            end [0, [40, 120], 0]
        }
    }
    emit_box [0 0 .1 .1 0 0]
}
```

---

### `FireWhites`
**Source:** `particles.gon`  

```
FireWhites {
    movieclip ParticleFire4
    
    render_mode separate
    flat_movement true
    depth_bias -0.1

    simulation_space global
    projection_matrix default
    
    emit_rate 20
    emit_amount 1
    emit_direction [0, 1, 0]
    speed [0 1]
    friction [.12 .6 .12]
    emit_spread 180
   
    rotation [-10 10]
    rotation_speed_start [-20 20]
    particle_lifetime .5
    size [.3 .6]

    alpha_start 1.3
    alpha_end 0

    //force_start [0 -140 0]
    //force_end [0 490 0]

    scripts {
        ParticleRandomForce { //if you want it to vary
            begin [0, -10, 0]
            end [0, [200, 900], 0]
        }
    }
    emit_box [-.03 .03 .1 0 -.03 .03]
}
```

---

### `FireSmoke`
**Source:** `particles.gon`  

```
FireSmoke {
    movieclip ParticleSmoke1
    
    render_mode separate
    flat_movement true
    depth_bias 0.3

    simulation_space global
    projection_matrix default
    
    emit_rate 20
    emit_amount 1
    emit_direction [0, 1, 0]
    speed [0 4]
    friction [.2 .35 .2]
    emit_spread 180
   
    rotation [-10 10]
    rotation_speed_start [-20 20]
    particle_lifetime .7
    size [.2 1]

    scripts {
        ParticleRandomForce[0, [75, 85], 0]
    }

    emit_box [0 0 .3 .9 0 0]

}
```

---

### `FireFull`
**Source:** `particles.gon`  

```
FireFull {
    combo [FireSmoke, FirePlumes, FireWaves, FireBase, FireWhites]
}
```

---

### `FirePlumesSmall`
**Source:** `particles.gon`  

```
FirePlumesSmall {
    movieclip ParticleFire1
    
    render_mode separate
    flat_movement true
    depth_bias 0.2

    simulation_space global
    projection_matrix default
    
    emit_rate 6
    emit_amount 1
    emit_direction [0, 1, 0]
    speed [0 10]
    friction [.6 .6 .6]
    emit_spread 180
   
    rotation [-2 2]
    rotation_speed_start [-20 20]
    particle_lifetime 1
    size [.3 .4]

    //force[0 70 0]
    scripts {
        ParticleRandomForce [0, [40, 80], 0]
    }

    emit_box [0 0 .1 .1 0 0]

}
```

---

### `FireWavesSmall`
**Source:** `particles.gon`  

```
FireWavesSmall {
    movieclip ParticleFire2
    
    render_mode separate
    flat_movement true
    depth_bias 0.1

    simulation_space global
    projection_matrix default
    
    emit_rate 6
    emit_amount 1
    emit_direction [0, 1, 0]
    speed [0 .5]
    friction [.6 .6 .6]
    emit_spread 180
   
    rotation [-10 10]
    rotation_speed_start [-20 20]
    particle_lifetime 1
    size [.2 .4]

    //force[0 70 0]
    scripts {
        ParticleRandomForce [0, [10, 60], 0]
    }
    emit_box [0 0 .1 .1 0 0]
}
```

---

### `FireBaseSmall`
**Source:** `particles.gon`  

```
FireBaseSmall {
    movieclip ParticleFire3
    
    render_mode separate
    flat_movement true
    depth_bias 0

    simulation_space global
    projection_matrix default
    
    emit_rate 10
    emit_amount 1
    emit_direction [0, 1, 0]
    speed [0 10]
    friction [1 .6 1]
    emit_spread 180
   
    rotation [-10 10]
    rotation_speed_start [-20 20]
    particle_lifetime 1
    size [.3 .5]

    //force_start [0 -140 0]
    //force_end [0 490 0]

    scripts {
        ParticleRandomForce { //if you want it to vary
            begin [0, -20, 0]
            end [0, [40, 120], 0]
        }
    }
    emit_box [0 0 .1 .1 0 0]
}
```

---

### `FireWhitesSmall`
**Source:** `particles.gon`  

```
FireWhitesSmall {
    movieclip ParticleFire4
    
    render_mode separate
    flat_movement true
    depth_bias -0.1

    simulation_space global
    projection_matrix default
    
    emit_rate 20
    emit_amount 1
    emit_direction [0, 1, 0]
    speed [0 1]
    friction [.6 .8 .6]
    emit_spread 180
   
    rotation [-10 10]
    rotation_speed_start [-20 20]
    particle_lifetime .5
    size [.15 .3]

    alpha_start 1.3
    alpha_end 0

    //force_start [0 -140 0]
    //force_end [0 490 0]

    scripts {
        ParticleRandomForce { //if you want it to vary
            begin [0, -10, 0]
            end [0, [200, 900], 0]
        }
    }
    emit_box [-.02 .02 .1 0 -.02 .02]
}
```

---

### `FireSmokeSmall`
**Source:** `particles.gon`  

```
FireSmokeSmall {
    movieclip ParticleSmoke1
    
    render_mode separate
    flat_movement true
    depth_bias 0.3

    simulation_space global
    projection_matrix default
    
    emit_rate 6
    emit_amount 1
    emit_direction [0, 1, 0]
    speed [0 4]
    friction [.33 .5 .33]
    emit_spread 180
   
    rotation [-10 10]
    rotation_speed_start [-20 20]
    particle_lifetime .7
    size [.1 .2]

    scripts {
        ParticleRandomForce[0, [75, 85], 0]
    }

    emit_box [0 0 0 .1 0 0]

}
```

---

### `FireFullSmall`
**Source:** `particles.gon`  

```
FireFullSmall {
    combo [FireSmokeSmall, FirePlumesSmall, FireWavesSmall, FireBaseSmall, FireWhitesSmall]
}
```

---

### `FirePlumesLarge`
**Source:** `particles.gon`  

```
FirePlumesLarge {
    movieclip ParticleFire1
    
    render_mode separate
    flat_movement true
    depth_bias 0.2

    simulation_space global
    projection_matrix default
    
    emit_rate 20
    emit_amount 1
    emit_direction [0, 1, 0]
    speed [0 10]
    friction [.6 .35 .6]
    emit_spread 180
   
    rotation [-10 10]
    rotation_speed_start [-20 20]
    particle_lifetime 1
    size [.3 .8]

    //force[0 70 0]
    scripts {
        ParticleRandomForce [0, [40, 80], 0]
    }

    emit_box [-.22 .22 .3 .3 -.22 .22]

}
```

---

### `FireWavesLarge`
**Source:** `particles.gon`  

```
FireWavesLarge {
    movieclip ParticleFire2
    
    render_mode separate
    flat_movement true
    depth_bias 0.1

    simulation_space global
    projection_matrix default
    
    emit_rate 6
    emit_amount 1
    emit_direction [0, 1, 0]
    speed [0 .5]
    friction [.03 .35 .03]
    emit_spread 180
   
    rotation [-10 10]
    rotation_speed_start [-20 20]
    particle_lifetime 1
    size [.8 1.2]

    //force[0 70 0]
    scripts {
        ParticleRandomForce [0, [10, 60], 0]
    }
    emit_box [-.1 .1 .3 .3 -.1 .1]
}
```

---

### `FireBaseLarge`
**Source:** `particles.gon`  

```
FireBaseLarge {
    movieclip ParticleFire3
    
    render_mode separate
    flat_movement true
    depth_bias 0

    simulation_space global
    projection_matrix default
    
    emit_rate 20
    emit_amount 1
    emit_direction [0, 1, 0]
    speed [0 10]
    friction [.55 .6 .55]
    emit_spread 180
   
    rotation [-10 10]
    rotation_speed_start [-20 20]
    particle_lifetime 1
    size [.9 1.3]

    //force_start [0 -140 0]
    //force_end [0 490 0]

    scripts {
        ParticleRandomForce { //if you want it to vary
            begin [0, -20, 0]
            end [0, [40, 120], 0]
        }
    }
    emit_box [-.13 .13 .1 .1 -.13 .13]
}
```

---

### `FireWhitesLarge`
**Source:** `particles.gon`  

```
FireWhitesLarge {
    movieclip ParticleFire4
    
    render_mode separate
    flat_movement true
    depth_bias -0.1

    simulation_space global
    projection_matrix default
    
    emit_rate 100
    emit_amount 1
    emit_direction [0, 1, 0]
    speed [0 1]
    friction [.12 .6 .12]
    emit_spread 180
   
    rotation [-10 10]
    rotation_speed_start [-20 20]
    particle_lifetime .5
    size [.3 .6]

    alpha_start 1
    alpha_end 0

    //force_start [0 -140 0]
    //force_end [0 490 0]

    scripts {
        ParticleRandomForce { //if you want it to vary
            begin [0, -10, 0]
            end [0, [200, 900], 0]
        }
    }
    emit_box [-.1 .1 0 0 -.1 .1]
}
```

---

### `FireSmokeLarge`
**Source:** `particles.gon`  

```
FireSmokeLarge {
    movieclip ParticleSmoke1
    
    render_mode separate
    flat_movement true
    depth_bias 0.3

    simulation_space global
    projection_matrix default
    
    emit_rate 40
    emit_amount 1
    emit_direction [0, 1, 0]
    speed [0 4]
    friction [.2 .35 .2]
    emit_spread 180
   
    rotation [-10 10]
    rotation_speed_start [-20 20]
    particle_lifetime .7
    size [.2 1]

    scripts {
        ParticleRandomForce[0, [75, 85], 0]
    }

    emit_box [-.3 .3 .3 .9 -.3 .3]

}
```

---

### `FireFullLarge`
**Source:** `particles.gon`  

```
FireFullLarge {
    combo [FireSmokeLarge, FirePlumesLarge, FireWavesLarge, FireBaseLarge, FireWhitesLarge]
}
```

---

### `PointSmoke`
**Source:** `particles.gon`  

```
PointSmoke {
    movieclip ParticleSmoke1
    
    render_mode separate
    flat_movement true

    simulation_space global
    projection_matrix default
    
    emit_rate 25
    emit_amount 1
    emit_direction [0, 1, 0]
    speed [0 10]
    friction [.4 .35 .4]
    emit_spread 180
   
    rotation [-10 10]
    rotation_speed_start [-20 20]
    particle_lifetime .7
    size [.15 1]

    force[0 70 0]

}
```

---

### `SplatterSmall`
**Source:** `particles.gon`  

```
SplatterSmall {
    movieclip ParticleDrop
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate .5
    emit_amount [2 5]
    emit_direction [0, 1, 0]
    friction [.04 .35 .04]
    emit_spread 90
    live_bounds [-999 999  0 999 -999 999]
    
    particle_lifetime  [.1 .3]
    speed_start 2.5
    size_start [.4 .7]
    size_end .1
    speed_scale .1
    face_moving_direction true

    force_start [0 100 0]
    force_end [0 -200 0]
    
    chain MiniSplatter
}
```

---

### `SplatterMed`
**Source:** `particles.gon`  

```
SplatterMed {
    movieclip ParticleDrop
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate .5
    emit_amount [5 15]
    emit_direction [0, 1, 0]
    friction [.02 .35 .02]
    emit_spread 90
    live_bounds [-999 999  0 999 -999 999]
    
    particle_lifetime  [.1 .7]
    speed_start 2.5
    size_start [.4 .7]
    size_end .1
    speed_scale .1
    face_moving_direction true

    force_start [0 150 0]
    force_end [0 -250 0]
    
    chain MiniSplatter
}
```

---

### `SplatterLarge`
**Source:** `particles.gon`  

```
SplatterLarge {
    movieclip ParticleDrop
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate .5
    emit_amount [50 70]
    emit_direction [0, 1, 0]
    friction [.008 .4 .008]
    emit_spread 90
    live_bounds [-999 999  0 999 -999 999]
    
    particle_lifetime  [.05 .8]
    speed_start 2.5
    size_start [.3 .9]
    size_end .3
    speed_scale .1
    face_moving_direction true

    //emit_box [0 0 .1 .1 0 0]

    force_start [0 150 0]
    force_end [0 -250 0]
    chain MiniSplatter2
}
```

---

### `SplatterXL`
**Source:** `particles.gon`  

```
SplatterXL {
    movieclip ParticleDrop
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate .5
    emit_amount 1500
    emit_direction [0, 1, 0]
    friction [.008 .4 .008]
    emit_spread 90
    live_bounds [-.2 10 0 10 -.2 10]
    
    particle_lifetime  [.7 .8]
    speed_start [1 17]
    size_start [.3 1]
    size_end .3
    speed_scale .1
    face_moving_direction true

    //emit_box [0 0 .1 .1 0 0]

    //force_start [0 150 0]
    //force_end [0 -250 0]
    scripts {
        ParticleRandomForce { //if you want it to vary
            begin [0, [-400, 200], 0]
            end [0, -450, 0]
        }
    }
    chain MiniSplatter3
}
```

---

### `MiniSplatter`
**Source:** `particles.gon`  

```
MiniSplatter {
    movieclip ParticleSpatter

    render_mode separate
    render_layer splatters

    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false

    emit_rate 1
    emit_amount 1
    particle_lifetime 2
    size [1 1.8]
}
```

---

### `MiniSplatter2`
**Source:** `particles.gon`  

```
MiniSplatter2 {
    movieclip ParticleSpatter

    render_mode separate
    render_layer splatters

    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false

    emit_rate 1
    emit_amount 1
    particle_lifetime 2
    size [1.8 2.3]
}
```

---

### `MiniSplatter3`
**Source:** `particles.gon`  

```
MiniSplatter3 {
    movieclip ParticleSpatter

    render_mode separate
    render_layer splatters

    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false

    emit_rate 1
    emit_amount [1,2]
    particle_lifetime [5,7]
    size [1.8 3]
}
```

---

### `Snow`
**Source:** `particles.gon`  

```
Snow {
    movieclip ParticleTestNoRandom
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 200
    emit_amount 1
    emit_direction [0, -1, 0]
    emit_spread 10
    emit_box [0 10 10 10 0 10]
    live_bounds [-0.5 999  -999 999 -0.5 999]
    
    
    particle_lifetime  7
    speed_start [2, 4]
    size_start [.3 .8]
    size_end 0
    rotation [0 360]
    rotation_speed [-100, 100]
    rotation_speed_end 0
    alpha .5
    
    scripts {
        ParticleBouncePlane {
            dampening 1
            friction 1
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane back
            position 10.5
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane right
            position 10.5
        }

        ParticleGlobalForce {
            id Wind
            amount .1
        }
    }
}
```

---

### `FireTileSmall`
**Source:** `particles.gon`  

```
FireTileSmall {
    movieclip ParticleFire3
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 5
    emit_amount 1
    emit_direction [0, -1, 0]
    //friction [.01 .01 .01]
    emit_spread 0
    live_bounds [-999 999  0 999 -999 999]
    emit_box [.05 .95 0 0 .05 .95]
    
    
    particle_lifetime  30
    speed_start 10
    size_start .5
    speed_scale .1
    alpha 0
    face_moving_direction true
    chain FireFullSmall
    force [0 -10 0]
}
```

---

### `CreepBubbles`
**Source:** `particles.gon`  

```
CreepBubbles {
    movieclip CreepBubbleParticle
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate [.7, 2]
    emit_amount 1
    emit_direction [0, 0, 0]
    //friction [.01 .01 .01]
    emit_spread 0
    live_bounds [-999 999  0 999 -999 999]
    emit_box [-.4 .4 0 0 -.4 .4]
    
    
    particle_lifetime 1.5
    speed_start 0
    size_start [.5 1]
    face_moving_direction false
}
```

---

### `ToxicBubbles`
**Source:** `particles.gon`  

```
ToxicBubbles {
    movieclip ToxicBubbleParticle
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate [.7, 2]
    emit_amount 1
    emit_direction [0, 0, 0]
    //friction [.01 .01 .01]
    emit_spread 0
    live_bounds [-999 999  0 999 -999 999]
    emit_box [-.4 .4 0 0 -.4 .4]
    
    
    particle_lifetime 1.5
    speed_start 0
    size_start [.5 1]
    face_moving_direction false
}
```

---

### `Lava_Distortion`
**Source:** `particles.gon`  

```
Lava_Distortion {
    movieclip Particle_HeatWaveDistortion
    
    render_mode separate
    material distorter
    render_layer sorted_distortions
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 10
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 4
    live_bounds [-999 999  0 999 -999 999]
    emit_box [-.4 .4 0 0 -.4 .4]
    
    
    particle_lifetime [.5, 1]
    speed_start [1, 2]
    size_start 1
    size_end 3
    rotation [0 0]
    //rotation_speed [-100, 100]
    rotation_speed_end 0
    alpha .01
    alpha_end 0
    //alpha .01
    
    scripts {
        ParticleGlobalForce {
            id Wind
            amount 3
        }
    }
}
```

---

### `SandStorm`
**Source:** `particles.gon`  

```
SandStorm {
    movieclip SandStormParticle
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 200
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 360
    emit_box [0 10 0 5 0 10]
    live_bounds [-999 999  -999 999 -999 999]
    
    
    particle_lifetime [.1 3]
    speed_start 5
    size_start [.4 .6]
    size_end 0
    alpha_start -1
    alpha_end 2
    speed_scale .25
    face_moving_direction true
    
    scripts {
        ParticleBouncePlane {
            dampening 0
            friction 1
        }

        ParticleTornadoForce {
            point [5 0 5]
            axis [0 1 0]
            force 20
        }
    }
}
```

---

### `Meteornado`
**Source:** `particles.gon`  

```
Meteornado {
    movieclip FX_MoonRock
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 200
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 360
    emit_box [0 10 0 5 0 10]
    live_bounds [-999 999  -999 999 -999 999]
    
    
    particle_lifetime [.1 3]
    speed_start 5
    size_start [.5 1.5]
    
    alpha_in .2
    alpha_out .2

    rotation [0 360]
    rotation_speed [-1000 1000]
    
    scripts {
        ParticleBouncePlane {
            dampening 0
            friction 1
        }

        ParticleTornadoForce {
            point [5 0 5]
            axis [0 1 0]
            force 20
        }
    }
}
```

---

### `Fog`
**Source:** `particles.gon`  

```
Fog {
    movieclip FogParticle
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 100
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 360
    emit_box [-5 10 0 2 -5 10]
    live_bounds [-999 999  -999 999 -999 999]
    
    
    particle_lifetime [3 5]
    speed_start .1
    size_start [.2 1]
    alpha_start 2
    alpha_end 0

    friction [0 1 0]

    scripts {
        ParticleGlobalForce {
            id Wind
            amount 1
        }
    }
}
```

---

### `Mist`
**Source:** `particles.gon`  

```
Mist {
    movieclip FogParticle
    
    render_mode separate
    material mist
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 100
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 360
    emit_box [-5 10 0 2 -5 10]
    live_bounds [-999 999  -999 999 -999 999]
    
    
    particle_lifetime [3 5]
    speed_start .1
    size_start [.2 1]
    alpha_start 1
    alpha_end 0

    friction [0 1 0]

    scripts {
        ParticleGlobalForce {
            id Wind
            amount 1
        }
    }
}
```

---

### `DarkFog`
**Source:** `particles.gon`  

```
DarkFog {
    movieclip DarkFogParticle
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 100
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 360
    emit_box [-5 10 0 2 -5 10]
    live_bounds [-999 999  -999 999 -999 999]
    
    
    particle_lifetime [3 5]
    speed_start .1
    size_start [.2 1]
    alpha_start 2
    alpha_end 0

    friction [0 1 0]

    scripts {
        ParticleGlobalForce {
            id Wind
            amount 1
        }
    }
}
```

---

### `test_tornado`
**Source:** `particles.gon`  

```
test_tornado {
    movieclip ParticleTestNoRandom
    
    //render_mode default
    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 240
    emit_amount 1
    emit_direction [0, 1, 0]
    friction [.2 .03 .2]
    emit_spread 90//30
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [.1 1]
    speed_start 10
    //speed_end 5
    force_start [0 10 0]
    force_end [0 0 0]
    //rotation_start [0, 360]
    //rotation_speed_start [-900, 900]
    //rotation_speed_end 0
    size_start [.1 1]
    size_end .2
    alpha_start 2
    alpha_end 0
    speed_scale .1
    inherit_speed 1//.21
    face_moving_direction true

    scripts {
        ParticleTornadoForce {
            point [0 0 0]
            axis [0 1 0]
            force 5
        }
    }
}
```

---

### `ManaDrain`
**Source:** `particles.gon`  

```
ManaDrain {
    movieclip ManaParticle
    
    render_mode separate
    simulation_space global
    ownership local
    projection_matrix default
    
    emit_rate 1
    emit_amount 10
    emit_direction [0, 1, 0]
    emit_radius .2
    friction_start [.06 .06 .06]
    friction_end [.2 .2 .2]
    emit_spread 180
    live_bounds [-999 999 -999 999 -999 999]

    emit_box [0 0 .5 .5 0 0]
    
    
    particle_lifetime  [.8 1.2]
    speed_start 10
    //speed_end 5

    rotation_start [0, 360]
    rotation_speed_start [-2000, 2000]
    //rotation_speed_end 0
    size_start 2
    size_end 1
    alpha_start 3
    alpha_end 0
    //speed_scale .5
    face_moving_direction false
    
    scripts {
        ParticleAttractor {
            force_start 0
            force_end 500
            towards [0 .5 0]
        }
    }
}
```

---

### `fartoom`
**Source:** `particles.gon`  

```
fartoom {
    combo [fartoom_trail, fartoom_burst]
}
```

---

### `fartoom_trail`
**Source:** `particles.gon`  

```
fartoom_trail {
    movieclip ParticleStinkCloudSlow
    
    //render_mode default
    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 80
    emit_amount 1
    emit_direction [0, -1, 0]
    friction [.1 .015 .1]
    //emit_spread 30
    emit_radius .2
    //emit_box [0 0 2.5 2.5 0 0]
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [.5 2]
    speed_start 7
    size_start [.2 1]
    size_end [1 2]
    alpha_start 2
    alpha_end 0
    speed_scale .1
    //inherit_speed 1//.21
    face_moving_direction true

    scripts {
        ParticleTornadoForce {
            point [0 0 0]
            axis [0 -1 0]
            force 2
        }
        ParticleBouncePlane {
            dampening 1
            friction 5
        }
    }
}
```

---

### `fartoom_burst`
**Source:** `particles.gon`  

```
fartoom_burst {
    movieclip ParticleStinkCloudSlow
    
    //render_mode default
    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount [90, 150]
    emit_direction [0, 1, 0]
    friction [.15 .1 .15]
    emit_spread 300
    emit_box [0 0 -.95 -.95 0 0]
    live_bounds [-999 999 -999 999 -999 999]
    
    particle_lifetime  [.5 2]
    speed_start [2 9]
    size_start [.5 1]
    size_end [.1 6]
    alpha_end 0
    speed_scale .3
    face_moving_direction true

    //chain fartoom_trail

    scripts {
        ParticleBouncePlane {
            dampening 1
            friction 5
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane back
            position 10.5
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane right
            position 10.5
        }
        ParticleTornadoForce {
            point [0 0 0]
            axis [0 1 0]
            force 0
        }
    }
}
```

---

### `dustCloud`
**Source:** `particles.gon`  

```
dustCloud {
    movieclip ParticleDustCloudSlow
    
    //render_mode default
    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount 100
    emit_direction [0, 1, 0]
    friction [.15 .1 .15]
    emit_spread 300
    emit_box [0 0 -.95 -.95 0 0]
    live_bounds [-999 999 -999 999 -999 999]
    
    particle_lifetime  [.5 2]
    speed_start [2 9]
    size_start [.5 1]
    size_end [.1 6]
    alpha_end 0
    speed_scale .3
    face_moving_direction true

    //chain fartoom_trail

    scripts {
        ParticleBouncePlane {
            dampening 1
            friction 5
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane back
            position 10.5
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane right
            position 10.5
        }
        ParticleTornadoForce {
            point [0 0 0]
            axis [0 1 0]
            force 0
        }
    }
}
```

---

### `druidFlowers`
**Source:** `particles.gon`  

```
druidFlowers {
    movieclip ParticlePetals
    
    render_mode separate
    
    simulation_space global
    ownership local
    projection_matrix default
    
    emit_rate 1
    emit_amount 150
    emit_direction [0, 1, 0]
    friction [.2 .2 .2]
    emit_spread 50
    emit_radius .5
    live_bounds [-999 999 -999 999 -999 999]
    emit_box [0 0 0 0 0 0]
    
    particle_lifetime  [.1 1]
    speed_start [0.01 0.5]
    speed_end 0

    rotation_start [0, 360]
    rotation_speed_start [-60, 60]
    //rotation_speed_end 1

    size_start 0.1
    size_end [1 1.8]
    alpha_start 1.5
    alpha_end 0
    speed_scale .1
    inherit_speed .1

    scripts {
        ParticleTornadoForce {
            point [0 0 0]
            axis [0 1 0]
            force 2
            //force_start 80
            //force_end 2
        }
        ParticleBouncePlane {
            dampening 1
            friction 1
        }
    }
}
```

---

### `musicalSwirl`
**Source:** `particles.gon`  

```
musicalSwirl {
    movieclip ParticleMusicNotes
    
    //render_mode default
    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 18
    emit_amount 1
    emit_direction [0, 1, 0]
    friction [.2 .1 .2]
    //emit_spread 1000
    live_bounds [-999 999 -999 999 -999 999]
    //emit_radius .05
    emit_box [.2 .2 .1 .1 .2 .2] //wtf
    
    
    particle_lifetime 2.5//[1 3]
    speed_start 1
    //speed_end -1
    force_start [0 10 0]
    force_end [0 0 0]
    rotation_start [-10, 10]
    rotation_speed_start [-30 30]
    //rotation_speed_end 0
    size_start .5
    size_end 1
    alpha_start 1.1
    alpha_end 0
    speed_scale .1
    //inherit_speed 1//.21
    //face_moving_direction true

    scripts {
        ParticleTornadoForce {
            point [0 0 0]
            axis [0 1 0]
            force 5
            //force_end 40000
        }
    }
}
```

---

### `coolLaserBeam`
**Source:** `particles.gon`  

```
coolLaserBeam {
    combo[coolLaserBeamInner, coolLaserBeamOuter]
}
```

---

### `coolLaserBeamOuter`
**Source:** `particles.gon`  

```
coolLaserBeamOuter {
    movieclip ParticleColor

    render_mode separate

    simulation_space global
    ownership local
    projection_matrix default

    emit_rate 150
    emit_amount 3
    emit_direction [1, 0, 0]
    friction [0 .1 .1]
    emit_spread 1
    live_bounds [-999 999 -999 999 -999 999]
    emit_radius .2

    particle_lifetime [.6 .85]//[1 3]
    speed_start 20

    size_start [.1 .1]
    size_end [.1 .8]
    alpha_start 5
    alpha_end .5
    speed_scale .2

    face_moving_direction true

    scripts {
        ParticleTornadoForce {
            point [0 0 0]
            axis [-1 0 0]
            force 8
            //force_end 40000
        }
        ParticleBouncePlane {
            dampening .95
            friction 2
            plane back
            position 10.5
        }
        ParticleBouncePlane {
            dampening 1
            friction 2
            plane right
            position 10.5
        }
        /*ParticleBouncePlane {
            dampening 0
            friction .1
        }*/
    }
}
```

---

### `coolLaserBeamInner`
**Source:** `particles.gon`  

```
coolLaserBeamInner {
    movieclip ParticleTestNoRandom

    render_mode separate

    simulation_space global
    ownership local
    projection_matrix default

    emit_rate 40
    emit_amount 3
    emit_direction [1, 0, 0]
    friction [0 .0 .0]
    emit_spread 2
    live_bounds [-999 999 -999 999 -999 999]
    emit_radius .25

    particle_lifetime [.6 1]//[1 3]
    speed_start 25

    size_start .7
    size_end 1
    alpha_start 2
    alpha_end 0
    speed_scale .1

    face_moving_direction true

    scripts {
        ParticleBouncePlane {
            dampening .95
            friction 1.4
            plane back
            position 10.5
        }
        ParticleBouncePlane {
            dampening .95
            friction 1.4
            plane right
            position 10.5
        }
        /*ParticleBouncePlane {
            dampening 0
            friction .1
        }*/
    }
}
```

---

### `Feathers`
**Source:** `particles.gon`  

```
Feathers {
    movieclip ParticleFeather
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate .5
    emit_amount 4
    emit_direction [0, 1, 0]
    emit_radius .3
    friction [.12 .5 .12]
    emit_spread 10
    live_bounds [-999 999 -999 999 -999 999]
    emit_box [0 0 .7 .7 0 0]
    
    
    particle_lifetime  [2 2.5]
    speed_start [10 25]
    size_start 1
    size_end 1
    alpha_start 3
    alpha_end 0
    face_moving_direction false
    force_start [0 -40 0]

    scripts {
        ParticleBouncePlane {
            dampening 1
            friction 1
        }
    }
}
```

---

### `GuillotinaGuts`
**Source:** `particles.gon`  

```
GuillotinaGuts {
    movieclip ParticleGuilchunk
    
    render_mode default
    //render_mode separate
    
    //update_mode locked
    
    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 150
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 10
    emit_box [-.3 .3 0 0 -.3 .3]
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  1.4
    speed_start [10 20]
    //speed_end 5
    force_start [0 -40 0]
    //rotation_start [0, 360]
    //rotation_speed_start [-900, 900]
    //rotation_speed_end 0
    size_start 1.2
    size_end 1
    alpha_start 9
    alpha_end 0
    //speed_scale 1
    face_moving_direction true
    
    scripts {
        ParticleBouncePlane {
            dampening .5
        }
    }
}
```

---

### `TrackingTest`
**Source:** `particles.gon`  

```
TrackingTest {
    movieclip ParticleTestNoRandom

    render_mode separate
    simulation_space global
    projection_matrix default
    
    emit_rate 240
    emit_amount 1
    emit_direction [0, 1, 0]
    friction [.1 .1 .1]
    emit_spread 180//30
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [.1 2]
    speed_start 0

    size_start .5
    size_end .1
    alpha_start 2
    alpha_end 0
    speed_scale .1
    inherit_speed 0
    face_moving_direction true
}
```

---

### `MagicMissileTrail`
**Source:** `particles.gon`  

```
MagicMissileTrail {
    movieclip SparkleParticle

    render_mode separate
    simulation_space global
    projection_matrix default
    
    emit_rate 240
    emit_amount 1
    emit_radius .1
    live_bounds [-999 999 -999 999 -999 999]

    particle_lifetime  [.2 .8]
    speed_start 0

    size_start [.5 1]
    //rotation [0 360]
    size_end .1

    inherit_speed 0
}
```

---

### `MagicMissileTrailSmall`
**Source:** `particles.gon`  

```
MagicMissileTrailSmall {
    movieclip SparkleParticle

    render_mode separate
    simulation_space global
    projection_matrix default
    
    emit_rate 180
    emit_amount 1
    emit_radius .05
    live_bounds [-999 999 -999 999 -999 999]

    particle_lifetime  [.2 .5]
    speed_start 0

    size_start [.25 .5]
    //rotation [0 360]
    size_end .1

    inherit_speed 0
}
```

---

### `SparkleBuff`
**Source:** `particles.gon`  

```
SparkleBuff {
    movieclip SparkleParticle
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    ownership local
    projection_matrix default
    
    emit_rate 50
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 180
    emit_box [0 0 0 1 0 0]
    live_bounds [-999 999  -999 999 -999 999]
    
    
    particle_lifetime [.1 1]
    speed_start .8
    size_start [.4 .6]
    size_end 0
    alpha_start -1
    alpha_end 2
    speed_scale 1
    face_moving_direction true
    
    scripts {
        ParticleBouncePlane {
            dampening 0
            friction 1
        }

        ParticleTornadoForce {
            point [0 0 0]
            axis [0 1 0]
            force 5
        }
    }
}
```

---

### `HeatWave_Particles`
**Source:** `particles.gon`  

```
HeatWave_Particles {
    movieclip ParticleFire2
    movieclip_timescale .5
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 100
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 10
    emit_box [0 10 0 1 0 10]
    live_bounds [-0.5 999  -999 999 -0.5 999]
    
    
    particle_lifetime [1, 4]
    speed_start [.5, 1]
    size_start .5
    size_end 2
    rotation [0 0]
    rotation_speed [-100, 100]
    rotation_speed_end 0
    alpha .3
    alpha_end 0
    
    scripts {
        ParticleGlobalForce {
            id Wind
            amount 1
        }
    }
}
```

---

### `HeatWave_Distortion`
**Source:** `particles.gon`  

```
HeatWave_Distortion {
    movieclip Particle_HeatWaveDistortion
    
    render_mode separate
    material distorter
    render_layer sorted_distortions
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 20
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 10
    emit_box [-5 10 0 5 -5 10]
    live_bounds [-999 999  -999 999 -999 999]
    
    
    particle_lifetime [1, 3]
    speed_start [.5, 1]
    size_start 1
    size_end 5
    rotation [0 0]
    //rotation_speed [-100, 100]
    rotation_speed_end 0
    alpha .01
    alpha_end 0
    //alpha .01
    
    scripts {
        ParticleGlobalForce {
            id Wind
            amount 1
        }
    }
}
```

---

### `CoreHeatWave_Distortion`
**Source:** `particles.gon`  

```
CoreHeatWave_Distortion {
    movieclip Particle_HeatWaveDistortion
    
    render_mode separate
    material distorter
    render_layer sorted_distortions
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 10
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 10
    emit_box [-5 10 0 5 -5 10]
    live_bounds [-999 999  -999 999 -999 999]
    
    
    particle_lifetime [1, 3]
    speed_start [.5, 1]
    size_start 1
    size_end 5
    rotation [0 0]
    //rotation_speed [-100, 100]
    rotation_speed_end 0
    alpha .005
    alpha_end 0
    //alpha .01
    
    scripts {
        ParticleGlobalForce {
            id Wind
            amount 1
        }
    }
}
```

---

### `HeatWave`
**Source:** `particles.gon`  

```
HeatWave {
    combo[HeatWave_Particles, HeatWave_Distortion]
}
```

---

### `healing_gas`
**Source:** `particles.gon`  

```
healing_gas {
    movieclip ParticleStinkCloudSlow
    
    //render_mode default
    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 15
    emit_amount 50
    emit_direction [0, -1, 0]
    friction [.1 .015 .1]
    //emit_spread 30
    emit_radius .2
    //emit_box [0 0 2.5 2.5 0 0]
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [.5 1]
    speed_start [5 7]
    size_start [.2 1]
    size_end [1 2]
    alpha_start 1.5
    alpha_end 0
    speed_scale [.05 .1]
    //inherit_speed 1//.21
    face_moving_direction true

    scripts {
        ParticleTornadoForce {
            point [0 0 0]
            axis [0 -0.5 0]
            force 1.5
        }
        ParticleBouncePlane {
            dampening 1
            friction 5
        }
        ParticleBouncePlane {
            dampening 1
            friction 1
            plane back
            position 10.5
        }
        ParticleBouncePlane {
            dampening 1
            friction 1
            plane right
            position 10.5
        }

    }
}
```

---

### `alienLaserCharge`
**Source:** `particles.gon`  

```
alienLaserCharge {
    movieclip ParticleTestNoRandom
    
    render_mode default
    render_mode separate
    
    simulation_space global
    ownership local
    projection_matrix default
    
    emit_rate 30
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_radius 1.5
    friction_start [.9 .9 .9]
    friction_end [.15 .15 .15]
    emit_spread 180
    live_bounds [-999 999 -999 999 -999 999]
    
    particle_lifetime  .5
    speed_start 0

    rotation_start [0, 360]
    rotation_speed_start [-900, 900]
    //rotation_speed_end 0
    size_start [.1 1]
    size_end 0
    alpha_start 0
    alpha_end 2
    speed_scale .1
    face_moving_direction true
    
    scripts {
        ParticleAttractor 100
    }
}
```

---

### `TormentorGuts`
**Source:** `particles.gon`  

```
TormentorGuts {
    movieclip ParticleTormentorGib
    
    render_mode separate
    
    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate .5
    emit_amount 400
    emit_direction [0, 1, 0]
    emit_spread 500
    //live_bounds [-1 10 -10 10 -1 10]
    
    
    particle_lifetime  2
    speed_start [3, 25]
    //speed_end 5
    //force_start [0 -20 0]
    rotation_start [0, 360]
    rotation_speed_start [-900, 900]
    //rotation_speed_end 0
    size_start .6
    //size_end .6
    alpha_start 4
    alpha_end 0
    //speed_scale .01
    //face_moving_direction true
    

    scripts {
        ParticleRandomForce [0, [-80, -10], 0]
        /*ParticleRandomForce { //if you want it to vary
            begin [0, [-20, 20], 0]
            end [-20, 0, 20]
        }*/
            ParticleBouncePlane {
                dampening .25
            }
            ParticleBouncePlane {
                dampening .75
                friction 0
                plane back
                position 10.5
            }
            ParticleBouncePlane {
            dampening .75
            friction 0
            plane right
            position 10.5
            }
        }
}
```

---

### `TormentorFull`
**Source:** `particles.gon`  

```
TormentorFull {
    combo[TormentorGuts, SplatterXL]
}
```

---

### `PassivePoison`
**Source:** `particles.gon`  

```
PassivePoison {
    movieclip Particle_PoisonDrip
    
    /*render_mode default
    simulation_space local
    ownership local*/
    render_mode separate
    simulation_space global

    projection_matrix default
    
    emit_rate 7
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_radius .4
    emit_spread 45
    friction [.05, .01, .05]
    emit_box [0 0 .3 .3 0 0]
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [.25 1]
    speed_start 1
    size_start 0
    size_end [.5 1]
    alpha_end 0
    alpha_start 2
    rotation [-30 30]
}
```

---

### `PassiveBleed`
**Source:** `particles.gon`  

```
PassiveBleed {
    movieclip Particle_BloodDrip
    
    /*render_mode default
    simulation_space local
    ownership local*/
    render_mode separate
    simulation_space global

    projection_matrix default
    
    emit_rate 4
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_radius .4
    emit_box [0 0 .7 .7 0 0]
    live_bounds [-999 999 -999 999 -999 999]
    force_start [0 0 0]
    force_end [0 -5 0]
    
    particle_lifetime  [.5 .75]
    speed_start 0
    size [.5 1]
    size_in .3
    alpha_out .5
    rotation -90
}
```

---

### `PassiveFire`
**Source:** `particles.gon`  

```
PassiveFire {
    movieclip Particle_BurnFlame
    unlit true
    
    /*render_mode default
    simulation_space local
    ownership local*/
    render_mode separate
    simulation_space global

    projection_matrix default
    
    emit_rate 10
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_radius .4
    emit_spread 45
    friction [.05, .01, .05]
    emit_box [0 0 .3 .3 0 0]
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [.25 1]
    speed_start 1
    size_start 0
    size_end [.5 1]
    alpha_in .1
    alpha_out .5
    rotation [-30 30]
}
```

---

### `PassiveWet`
**Source:** `particles.gon`  

```
PassiveWet {
    movieclip Particle_WaterDrip
    
    /*render_mode default
    simulation_space local
    ownership local*/
    render_mode separate
    simulation_space global

    projection_matrix default
    
    emit_rate 4
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_radius .4
    emit_box [0 0 .7 .7 0 0]
    live_bounds [-999 999 -999 999 -999 999]
    force_start [0 0 0]
    force_end [0 -10 0]
    
    particle_lifetime  [.35 .55]
    speed_start 0
    size .5
    size_in .3
    alpha_out .5
    rotation -90
}
```

---

### `PassiveTar`
**Source:** `particles.gon`  

```
PassiveTar {
    movieclip Particle_TarDrip
    
    /*render_mode default
    simulation_space local
    ownership local*/
    render_mode separate
    simulation_space global

    spurt PassiveTarSplat

    projection_matrix default
    
    emit_rate 4
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_radius .4
    emit_box [0 0 .7 .7 0 0]
    live_bounds [-999 999 -999 999 -999 999]
    force_start [0 0 0]
    force_end [0 -1 0]
    
    particle_lifetime  [1 1.5]
    speed_start 0
    size .5
    size_in .1
    alpha_in .2
    alpha_out .5
    rotation -90
}
```

---

### `FireExtinguish_Steam`
**Source:** `particles.gon`  

```
FireExtinguish_Steam {
    movieclip ParticleDustCloud

    render_mode separate
    simulation_space global

    projection_matrix default
    
    emit_rate 1
    emit_amount 200
    emit_timespread .75
    emit_timespread_curve ease_out
    emit_direction [0, 1, 0]
    emit_radius .4
    speed [1 3]
    emit_box [-.1 .1 .2 .2 -.1 .1]
    live_bounds [-999 999 -999 999 -999 999]
    
    particle_lifetime 1
    size [.5 2]
    alpha .1

    scripts {
        ParticleGlobalForce {
            id Wind
            amount 2
        }
    }
}
```

---

### `FireExtinguish`
**Source:** `particles.gon`  

```
FireExtinguish {
    combo [FireExtinguish_Steam]
}
```

---

### `WindLeaves`
**Source:** `particles.gon`  

```
WindLeaves {
    movieclip Particle_WindLeaf
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 50
    emit_amount 1
    emit_direction [1, 0, 0]
    emit_spread 30
    emit_box [-10 10 0 10 -10 10]
    live_bounds [-999 999  -999 999 -999 999]
    //friction [.01 .01 .01]
    //force_end [0 -1 0]
    
    particle_lifetime [2 10]
    speed_start [0, 2]
    size [.3 .8]
    alpha 1
    alpha_in .2
    alpha_out .2
    
    scripts {
        ParticleBouncePlane {
            dampening .75
            friction 0
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane back
            position 10.5
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane right
            position 10.5
        }
        ParticleGlobalForce {
            id Wind
            amount .5
        }
    }
}
```

---

### `WindDebris`
**Source:** `particles.gon`  

```
WindDebris {
    movieclip Particle_WindDebris
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 100
    emit_amount 1
    emit_direction [1, 0, 0]
    emit_spread 10
    emit_box [-10 10 0 10 -10 10]
    live_bounds [-999 999  -999 999 -999 999]
    //friction [.1 .1 .1]
    //force_end [0 -1 0]
    
    particle_lifetime [2 4]
    speed_start [2, 4]
    size [.1 1]
    //speed_scale 3
    //face_moving_direction true
    size_in .5
    size_out .5
    
    scripts {
        ParticleGlobalForce {
            id Wind
            amount 1
        }
    }
}
```

---

### `WindDust`
**Source:** `particles.gon`  

```
WindDust {
    movieclip Particle_WindDust
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    //material mist
    
    emit_rate 100
    emit_amount 1
    emit_direction [1, 0, 0]
    emit_spread 10
    emit_box [-10 10 0 10 -10 10]
    live_bounds [-999 999  -999 999 -999 999]
    //friction [.1 .1 .1]
    //force_end [0 -1 0]
    
    particle_lifetime [2 4]
    speed_start [2, 4]
    size [.1 1]
    alpha .03
    alpha_in .3
    alpha_out .3
    //speed_scale 3
    //face_moving_direction true
    size [1 3]
    
    scripts {
        ParticleGlobalForce {
            id Wind
            amount 1
        }
    }
}
```

---

### `WindWisps`
**Source:** `particles.gon`  

```
WindWisps {
    movieclip Particle_WindWisps
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    //material mist
    
    emit_rate 20
    emit_amount 1
    emit_direction [1, 0, 0]
    emit_spread 10
    emit_box [-1 10 0 10 -1 10]
    live_bounds [-999 999  -999 999 -999 999]
    //friction [.1 .1 .1]
    //force_end [0 -1 0]
    
    particle_lifetime 2
    speed_start .001
    alpha .5
    //speed_scale 3
    face_moving_direction true
    size [1 3]
}
```

---

### `WindFull`
**Source:** `particles.gon`  

```
WindFull {
    combo [WindDebris WindLeaves WindDust WindWisps]
}
```

---

### `FloatingRocks`
**Source:** `particles.gon`  

```
FloatingRocks {
    movieclip FX_MoonRock
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    //material mist
    
    emit_rate 3
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 0
    emit_box [0 10 0 0 0 10]
    live_bounds [-999 999  -999 999 -999 999]
    //friction [.1 .1 .1]
    force_end [0 1 0]

    
    particle_lifetime [10 20]
    speed_start [.1 .2]
    rotation [0 360]
    rotation_speed [-50 50]
    size [.5 .9]
    //size_in .05
    size_out .5
    alpha_in .05
    alpha 1
    //speed_scale 3
}
```

---

### `Embers`
**Source:** `particles.gon`  

```
Embers {
    movieclip FX_Ember
    
    render_mode separate
    unlit true
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 20
    emit_amount 1
    emit_direction [-.5, -1, 0]
    emit_spread 10
    emit_box [0 10 0 10 0 10]
    live_bounds [-999 999  -999 999 -999 999]
    //friction [.1 .1 .1]
    //force_end [0 -1 0]
    
    particle_lifetime [2 4]
    speed_start [0, 1]
    size [.2 .4]
    rotation [0 360]
    rotation_speed [-100 100]
    //speed_scale 3
    //face_moving_direction true
    alpha_in .2
    alpha_out .2
    
    scripts {
        ParticleGlobalForce {
            id Wind
            amount .5
        }

        ParticleBouncePlane {
            dampening .5
            friction .5
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane back
            position 10.5
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane right
            position 10.5
        }
    }
}
```

---

### `EQRocks`
**Source:** `particles.gon`  

```
EQRocks {
    movieclip ParticleRocks
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount [0 4]
    emit_direction [0, 1, 0]
    friction [.02 0 .02]
    emit_spread 20
    emit_radius .3
   
    rotation [0 360]
    rotation_speed [-500 500]
    rotation_speed_end 0
    particle_lifetime  [1 1.5]
    speed_start [7 13]
    size [.8 1.5]
    alpha_out .2

    force [0 -30 0]

    scripts {
        ParticleBouncePlane {
            dampening .5
            friction .2
        }
    }
}
```

---

### `PassiveStealth`
**Source:** `particles.gon`  

```
PassiveStealth {
    movieclip ParticleDarkPuff
    
    render_mode separate
    simulation_space global

    projection_matrix default
    
    emit_rate 100
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_radius .4
    emit_spread 360
    friction [.01, .01, .01]
    emit_box [0 0 .3 .5 0 0]
    live_bounds [-999 999 -999 999 -999 999]
    force [0 -.5 0]
    
    particle_lifetime  [1 1]
    speed_start [0 .5]
    size [.5 1]

    alpha .10
    alpha_in .5
    alpha_out .5
    rotation [-180 180]
    rotation_speed [-100, 100]

    scripts {
        ParticleBouncePlane {
            dampening 1
            friction 0
        }
    }
}
```

---

### `Firestorm_Distortion`
**Source:** `particles.gon`  

```
Firestorm_Distortion {
    movieclip Particle_HeatWaveDistortion
    
    render_mode separate
    material distorter
    render_layer sorted_distortions
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 40
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 10
    emit_box [-5 10 0 5 -5 10]
    live_bounds [-999 999  -999 999 -999 999]
    
    
    particle_lifetime [1, 3]
    speed_start [1, 2]
    size_start 1
    size_end 5
    rotation [0 0]
    //rotation_speed [-100, 100]
    rotation_speed_end 0
    alpha .01
    alpha_end 0
    //alpha .01
    
    scripts {
        ParticleGlobalForce {
            id Wind
            amount 1
        }
    }
}
```

---

### `Firestorm_Embers`
**Source:** `particles.gon`  

```
Firestorm_Embers {
    movieclip FX_Ember
    
    render_mode separate
    unlit true
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 200
    emit_amount 1
    emit_direction [-.5, -1, 0]
    emit_spread 10
    emit_box [0 10 0 10 0 10]
    live_bounds [-999 999  -999 999 -999 999]
    //friction [.1 .1 .1]
    //force_end [0 -1 0]
    
    particle_lifetime [2 4]
    speed_start [1, 2]
    size [.2 .4]
    rotation [0 360]
    rotation_speed [-100 100]
    //speed_scale 3
    //face_moving_direction true
    alpha_in .2
    alpha_out .2
    
    scripts {
        ParticleGlobalForce {
            id Wind
            amount .5
        }

        ParticleBouncePlane {
            dampening .5
            friction .5
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane back
            position 10.5
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane right
            position 10.5
        }
    }
}
```

---

### `Firenado_Embers`
**Source:** `particles.gon`  

```
Firenado_Embers {
    movieclip FX_Ember
    
    render_mode separate
    unlit true
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 200
    emit_amount 1
    emit_direction [-.5, -1, 0]
    emit_spread 10
    emit_box [0 10 0 10 0 10]
    live_bounds [-999 999  -999 999 -999 999]
    //friction [.1 .1 .1]
    //force_end [0 -1 0]
    
    particle_lifetime [2 4]
    speed_start [1, 2]
    size [.2 .4]
    rotation [0 360]
    rotation_speed [-100 100]
    //speed_scale 3
    //face_moving_direction true
    alpha_in .2
    alpha_out .2
    
    scripts {
        ParticleGlobalForce {
            id Wind
            amount .5
        }

        ParticleBouncePlane {
            dampening .5
            friction .5
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane back
            position 10.5
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane right
            position 10.5
        }
        ParticleTornadoForce {
            point [5 0 5]
            axis [0 1 0]
            force 10
        }
    }
}
```

---

### `Firestorm_Fire`
**Source:** `particles.gon`  

```
Firestorm_Fire {
    movieclip Particle_BurnFlame
    unlit true
    
    /*render_mode default
    simulation_space local
    ownership local*/
    render_mode separate
    simulation_space global

    projection_matrix default
    
    emit_rate 200
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_radius .4
    emit_spread 45
    friction [.05, .01, .05]
    emit_box [0 10 0 3 0 10]
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [.25 1]
    speed_start 1
    size_start 0
    size_end [.5 1]
    alpha_in .1
    alpha_out .5
    rotation [-30 30]
}
```

---

### `Firenado_Fire`
**Source:** `particles.gon`  

```
Firenado_Fire {
    movieclip Particle_BurnFlame
    unlit true
    
    /*render_mode default
    simulation_space local
    ownership local*/
    render_mode separate
    simulation_space global

    projection_matrix default
    
    emit_rate 200
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_radius .4
    emit_spread 45
    friction [.05, .01, .05]
    emit_box [0 10 0 3 0 10]
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [.25 1]
    speed_start 1
    size_start 0
    size_end [.5 1]
    alpha_in .1
    alpha_out .5
    rotation [-30 30]

    scripts {
        ParticleTornadoForce {
            point [5 0 5]
            axis [0 1 0]
            force 5
        }
    }
}
```

---

### `CraterLeaves`
**Source:** `particles.gon`  

```
CraterLeaves {
    movieclip Particle_WindLeafCrater
    movieclip_timescale .5
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 15
    emit_amount 1
    emit_direction [-.4, -.4, 0]
    emit_spread 30
    emit_box [-10 10 0 10 -10 10]
    live_bounds [-999 999  -999 999 -999 999]
    //friction [.01 .01 .01]
    //force_end [0 -1 0]
    
    particle_lifetime [4 10]
    speed_start [0, 1]
    size [.5 1]
    alpha 1
    alpha_in .2
    alpha_out .2
    
    scripts {
        ParticleBouncePlane {
            dampening .75
            friction 0
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane back
            position 10.5
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane right
            position 10.5
        }
        ParticleGlobalForce {
            id Wind
            amount .5
        }
    }
}
```

---

### `FireStorm`
**Source:** `particles.gon`  

```
FireStorm {
    combo [Firestorm_Fire Firestorm_Embers Firestorm_Distortion]
}
```

---

### `Firenado`
**Source:** `particles.gon`  

```
Firenado {
    combo [Firenado_Fire Firenado_Embers Firestorm_Distortion]
}
```

---

### `HadoukenBall`
**Source:** `particles.gon`  

```
HadoukenBall {
    //movieclip ParticleColor
    movieclip Particle_BurnFlame

    render_mode separate

    simulation_space global
    ownership local
    projection_matrix default

    emit_rate 50
    emit_amount 3
    emit_direction [0 0 0]
    live_bounds [-999 999 -999 999 -999 999]
    emit_radius .1

    particle_lifetime [.6 1]//[1 3]

    size_start [.5 0]
    size_end [.1 .1]
    alpha_start 1
    alpha_end .2
    speed_scale .4

    face_moving_direction true

    scripts {
        ParticleTornadoForce {
            point [0 .8 0]
            axis [1 0 0]
            force 15
        }
    }
}
```

---

### `GibsBloodSpurt`
**Source:** `particles.gon`  

```
GibsBloodSpurt {
    movieclip ParticleBlood

    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 1
    emit_amount 10
    emit_direction [0, 1, 0]
    emit_spread 45
    force_start [0 -20 0]
    
    
    particle_lifetime  [1 2]
    speed_start [0 2]

    size_start [.1 .5]
    size_end 0
    alpha_start 2
    alpha_end 0
    speed_scale 1
    inherit_speed [.1 .9]//.21
    face_moving_direction true
    
    scripts {
        ParticleBouncePlane {
            dampening .5
            friction .1
        }
    }
}
```

---

### `Gibs_default`
**Source:** `particles.gon`  

```
Gibs_default {
    movieclip Gibs_Default

    render_mode separate
    
    simulation_space global
    projection_matrix default
    //continual_emission false
    
    emit_rate .5
    emit_amount 3
    emit_direction [0, 1, 0]
    emit_spread 60
    emit_shell .5
    emit_box [0, 0, 0, 0, 0, 0]
    live_bounds [-999 999 -999 999 -999 999]
    spurt GibsBloodSpurt
    
    particle_lifetime  [1.5 2]
    speed_start [3 7]
    //speed_end 5
    force_start [0 -20 0]
    //rotation_start [0, 360]
    rotation_speed_start [-900, 900]
    rotation_speed_end 0
    size_start 1.2
    size_end 1
    alpha_start 9
    alpha_end 0
    //speed_scale 1
    //face_moving_direction true
    
    scripts {
        ParticleBouncePlane {
            dampening .5
            friction .1
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane back
            position 10.5
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane right
            position 10.5
        }
    }
}
```

---

### `Gibs_cat`
**Source:** `particles.gon`  

```
Gibs_cat {
    variant_of Gibs_default
}
```

---

### `Gibs_humanoid`
**Source:** `particles.gon`  

```
Gibs_humanoid {
    variant_of Gibs_default
	
	movieclip Gibs_Human
}
```

---

### `Gibs_demon`
**Source:** `particles.gon`  

```
Gibs_demon {
    variant_of Gibs_default
	
	movieclip Gibs_Demon
}
```

---

### `Gibs_animal`
**Source:** `particles.gon`  

```
Gibs_animal {
    variant_of Gibs_default
}
```

---

### `Gibs_rat`
**Source:** `particles.gon`  

```
Gibs_rat {
    variant_of Gibs_default
	
	movieclip Gibs_Rat
}
```

---

### `Gibs_blob`
**Source:** `particles.gon`  

```
Gibs_blob {
    variant_of Gibs_default

    movieclip Gibs_Blob
}
```

---

### `Gibs_skeleton`
**Source:** `particles.gon`  

```
Gibs_skeleton {
    variant_of Gibs_default

    movieclip Gibs_Undead
}
```

---

### `Gibs_rock`
**Source:** `particles.gon`  

```
Gibs_rock {
    variant_of Gibs_default

    movieclip Gibs_Rock
}
```

---

### `Gibs_plant`
**Source:** `particles.gon`  

```
Gibs_plant {
    variant_of Gibs_default

    movieclip Gibs_Plant
}
```

---

### `Gibs_robot`
**Source:** `particles.gon`  

```
Gibs_robot {
    variant_of Gibs_default

    movieclip Gibs_Robot
}
```

---

### `Gibs_bug`
**Source:** `particles.gon`  

```
Gibs_bug {
    variant_of Gibs_default

    movieclip Gibs_Bugs
}
```

---

### `Gibs_poop`
**Source:** `particles.gon`  

```
Gibs_poop {
    variant_of Gibs_default

    movieclip Gibs_Poop
}
```

---

### `Gibs_fetus`
**Source:** `particles.gon`  

```
Gibs_fetus {
    variant_of Gibs_default

    movieclip Gibs_Fetus
}
```

---

### `Gibs_box`
**Source:** `particles.gon`  

```
Gibs_box {
    variant_of Gibs_default

    movieclip Gibs_Box
}
```

---

### `Gibs_bag`
**Source:** `particles.gon`  

```
Gibs_bag {
    variant_of Gibs_default

    movieclip Gibs_Bag
}
```

---

### `Gibs_cactus`
**Source:** `particles.gon`  

```
Gibs_cactus {
    variant_of Gibs_default

    movieclip Gibs_Cactus
}
```

---

### `Gibs_terminatorskin`
**Source:** `particles.gon`  

```
Gibs_terminatorskin {
    variant_of Gibs_default

    emit_amount 3
}
```

---

### `VolcanoSpurt`
**Source:** `particles.gon`  

```
VolcanoSpurt {
    movieclip ParticleRocks
    render_mode separate

    simulation_space global
    projection_matrix default

    spurt VolcanoSpurt_Trail
    
    emit_rate 1
    emit_amount 5
    emit_direction [0, 1, 0]
    friction [.02 0 .02]
    emit_spread 20
    emit_radius .3
   
    rotation [0 360]
    rotation_speed [-500 500]
    rotation_speed_end 0
    particle_lifetime  [1 1.5]
    speed_start [7 13]
    size [.8 1.5]
    alpha_out .2

    force [0 -30 0]

    scripts {
        ParticleBouncePlane {
            dampening .5
            friction .2
        }
    }
}
```

---

### `VolcanoSpurt_Trail`
**Source:** `particles.gon`  

```
VolcanoSpurt_Trail {
    movieclip Particle_BurnFlame
    unlit true
    
    /*render_mode default
    simulation_space local
    ownership local*/
    render_mode separate
    simulation_space global

    projection_matrix default
    
    emit_rate 1
    emit_amount 10
    emit_direction [0, 1, 0]
    emit_radius 0
    emit_spread 30
    friction [.01, .01, .01]
    live_bounds [-999 999 -999 999 -999 999]

    //inherit_speed [.1 .9]//.21
    
    
    particle_lifetime  [.25 1]
    speed_start [0 3]
    size_start 0
    size_end [.5 1]
    alpha_in .1
    alpha_out .5
    rotation [-30 30]
}
```

---

### `RocketTrail`
**Source:** `particles.gon`  

```
RocketTrail {
    movieclip PuffNoOutline
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate 30
    emit_amount 1
    emit_direction [0, 1, 0]
    friction [.03 .35 .03]
    emit_spread 180
   
    rotation [0 360]
    rotation_speed_start [-1000 1000]
    rotation_speed_end 0
    particle_lifetime  1
    speed_start 0
    alpha_start .8
    alpha_end 0
    size_start 1
    size_end 0

}
```

---

### `GravityHoverRings`
**Source:** `particles.gon`  

```
GravityHoverRings {
    movieclip Particle_GravityHoverRing
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate 3
    emit_amount 1
    emit_direction [.1, -1, .1]
    emit_box [0 0 .1 .1 0 0]

    emit_spread 0
   
    //rotation [0 360]
    //rotation_speed_start [-1000 1000]
    rotation_speed_end 0
    particle_lifetime  1
    speed_start .5
    alpha_in .3
    alpha_out .2
    size_start 1
    size_end .3

    scripts {
        ParticleBouncePlane {
            dampening 1
            friction 1
        }
    }
}
```

---

### `GravityBurstB`
**Source:** `particles.gon`  

```
GravityBurstB {
    movieclip Particle_GravityHoverRing
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount 4
    emit_timespread .1
    //emit_timespread_curve ease_out
    emit_direction [1, 0, 0]
    emit_box [0 0 .1 .1 0 0]
    friction [.01 .01 .01]

    emit_spread 0
   
    rotation 90
    //rotation_speed_start [-1000 1000]
    rotation_speed_end 0
    particle_lifetime  [.4 .6]
    speed_start [0 2]
    alpha_in .01
    alpha_out .5
    size_start 1
    size_end .5
}
```

---

### `GravityBurstS`
**Source:** `particles.gon`  

```
GravityBurstS {
    movieclip Particle_GravityHoverRing
    
    render_mode separate

    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount 15
    emit_timespread .1
    //emit_timespread_curve ease_out
    emit_direction [1, 0, 0]
    emit_box [0 0 .1 .1 0 0]
    friction [.05 .05 .05]

    emit_spread 0
   
    rotation 90
    //rotation_speed_start [-1000 1000]
    rotation_speed_end 0
    particle_lifetime  [.4 .6]
    speed_start [1 10]
    alpha_in .01
    alpha_out .2
    size_start [.2 .5]
    size_end .1
}
```

---

### `GravityBurst`
**Source:** `particles.gon`  

```
GravityBurst {
    combo [GravityBurstB GravityBurstS]
}
```

---

### `MeatCaveDrip`
**Source:** `particles.gon`  

```
MeatCaveDrip {
    variant_of CaveDrip
	emit_rate [10 25]
	alpha 1
	force [0 -10 0]
	speed_start 2
	speed_scale .2
    movieclip RedWaterParticle
    chain MeatCaveSplash
}
```

---

### `MeatCaveSplash`
**Source:** `particles.gon`  

```
MeatCaveSplash {
    variant_of CaveSplash
    movieclip RedWaterSplashParticle
}
```

---

### `DruidFlowersVictory`
**Source:** `particles.gon`  

```
DruidFlowersVictory {
    movieclip ParticlePetals
    
    render_mode separate
    
    simulation_space global
    projection_matrix default
    
    emit_rate 240
    emit_amount [100, 300]
    emit_direction [0, 1, 0]
    emit_spread 30
    live_bounds [-999 999 -999 999 -999 999]
    
    particle_lifetime  [2, 3]
    speed_start [1.5, 2.5]
    speed_end [0.7, 1]
    force_start [0 -5 0]
    rotation_start [0, 360]
    size_start .5
    size_end .6
    alpha_start 2
    alpha_end 0
    speed_scale .2
    face_moving_direction true

    scripts {
        ParticleBouncePlane {
            dampening 1
            friction 1
        }
    }
}
```

---

### `TinkererVictoryFirework`
**Source:** `particles.gon`  

```
TinkererVictoryFirework {
    movieclip ParticleTestNoRandom
    
    render_mode separate
    
    simulation_space global
    projection_matrix default
    
    emit_rate [.5, 1]
    emit_amount [3, 5]
    emit_direction [0, 1, 0]
    friction [.01 .01 .01]
    emit_spread 30
    live_bounds [-999 999 -999 999 -999 999]
    
    particle_lifetime  [.2 .45]
    speed_start 10
    speed_end 5
    force_start [0 -20 0]
    size_start .65
    speed_scale .1
    face_moving_direction true
    chain firework_burst
}
```

---

### `FireBallTrail`
**Source:** `particles.gon`  

```
FireBallTrail {
    movieclip Particle_BurnFlame
    unlit true

    render_mode separate
    simulation_space global
    projection_matrix default
    
    emit_rate 100
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_radius .1
    emit_spread 45
    friction [.05, .01, .05]
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [.25 1]
    speed_start 2
    size_start 1
    size_end [.5 .25]
    alpha_in .1
    alpha_out .5
    rotation [-30 30]

    inherit_speed 0
}
```

---

### `Confetti`
**Source:** `particles.gon`  

```
Confetti {
    movieclip ConfettiParticle
    
    render_mode separate
    
    simulation_space global
    projection_matrix default
    
    emit_rate [.5]
    emit_amount [100]
    emit_direction [0, 1, 0]
    friction [.05 .05 .05]
    emit_spread 45
    emit_shell .5
    live_bounds [-999 999 -999 999 -999 999]
    
    particle_lifetime  [2 4]
    speed_start [2 15]
    force_start [0 -10 0]
    force_end [0 -2 0]
    size_start [.5 .75]
    speed_scale .1

    rotation [0 360]
    rotation_speed [-1000 1000]
    rotation_speed_end 0

    alpha_out .2

    scripts {
        ParticleBouncePlane {
            dampening 1
            friction 1
            rotation_dampening 1
        }
        ParticleBouncePlane {
            dampening .5
            friction 0
            plane back
            position 10.5
        }
        ParticleBouncePlane {
            dampening .5
            friction 0
            plane right
            position 10.5
        }
    }
}
```

---

### `GlitchShards`
**Source:** `particles.gon`  

```
GlitchShards {
    movieclip Particle_InvertShards
    
    render_mode default
    render_layer top
    
    simulation_space global
    is_3D false

    emit_rate 100
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_box [0 0 7.955 7.955 0 0]
    //friction [.01 .01 .01]
    emit_spread 180//30
    emit_shell 15
    emitshape_scale [1 0.5625]
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  4
    rotation_start [0 360]
    speed_start -2
    //speed_end 5
    //force_start [0 -70 0]
    //force_end [0 90 0]
    //rotation_start [0, 360]
    //rotation_speed_start [-900, 900]
    //rotation_speed_end 0
    //size_start [1 3]
    //size_end 0
    size [2 5]
    size_in .1
    size_out .9
}
```

---

### `GlitchTile`
**Source:** `particles.gon`  

```
GlitchTile {
    movieclip Particle_InvertShards
    
    render_mode separate

    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 50
    emit_amount 1
    emit_direction [0, 1, 0]
    friction [.05 .05 .05]
    emit_spread 45
    live_bounds [-999 999  0 999 -999 999]
    emit_box [-.4 .4 0 0 -.4 .4]
    
    
    particle_lifetime [.5, 1]
    speed_start [0, 2]

    rotation [0 360]

    size [0 1]
    size_in .1
    size_out .9

    scripts {
        ParticleGlobalForce {
            id Wind
            amount 3
        }
    }
}
```

---

### `PassiveScrambled`
**Source:** `particles.gon`  

```
PassiveScrambled {
    movieclip Particle_InvertShards
    
    /*render_mode default
    simulation_space local
    ownership local*/
    render_mode separate
    simulation_space global

    projection_matrix default
    
    emit_rate 20
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_radius .4
    emit_spread 180
    friction [.05, .05, .05]
    emit_box [0 0 .5 .5 0 0]
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime  [.25 1]
    speed_start 1
    rotation [0 360]

    size [0 1]
    size_in .1
    size_out .9
}
```

---

### `FightBallCloud`
**Source:** `particles.gon`  

```
FightBallCloud {
    movieclip ParticleDustCloudSlow
    
    //render_mode default
    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount 100
    emit_direction [0, 1, 0]
    friction [.15 .1 .15]
    emit_spread 300
    emit_box [0 0 -.95 -.95 0 0]
    live_bounds [-999 999 -999 999 -999 999]
    
    particle_lifetime  [.5 2]
    speed_start [2 9]
    size_start [.5 1]
    size_end [.1 6]
    alpha_end 0
    speed_scale .3
    face_moving_direction true

    scripts {
        ParticleTornadoForce {
            point [0 0 0]
            axis [0 1 0]
            force 0
        }
    }
}
```

---

### `ChaosTPOut`
**Source:** `particles.gon`  

```
ChaosTPOut {
    movieclip Particle_InvertShards
    
    render_mode separate

    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount 500
    emit_direction [0, 1, 0]
    friction [.05 .05 .05]
    emit_spread 360
    live_bounds [-999 999  0 999 -999 999]
    emit_radius 1
    emit_box [0 0 0 4 0 0]
    
    
    particle_lifetime [.5, 1]
    speed_start [2, 8]

    rotation [0 360]

    size [0 1]
    size_in .1
    size_out .9

    scripts {
        ParticleGlobalForce {
            id Wind
            amount 3
        }
    }
}
```

---

### `ChaosTPIn`
**Source:** `particles.gon`  

```
ChaosTPIn {
    movieclip Particle_InvertShards
    
    render_mode separate

    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount 500
    emit_timespread 1
    emit_timespread_curve ease_out
    emit_direction [0, 1, 0]
    friction [.05 .05 .05]
    emit_spread 360
    live_bounds [-999 999  0 999 -999 999]
    emit_radius 2
    emit_box [0 0 0 4 0 0]
    
    
    particle_lifetime [.5, 1]
    speed_start [1, 8]

    rotation [0 360]

    size [0 1]
    size_in .1
    size_out .9

    scripts {
        ParticleGlobalForce {
            id Wind
            amount 3
        }
    }
}
```

---

### `ChaosTPTracer`
**Source:** `particles.gon`  

```
ChaosTPTracer {
    movieclip Particle_InvertShards
    
    render_mode separate

    //update_mode locked
    simulation_space global
    projection_matrix default
    continual_emission true
    
    emit_rate 10000
    emit_amount 1
    emit_direction [0, 1, 0]
    friction [.2 .2 .2]
    emit_spread 360
    live_bounds [-999 999  0 999 -999 999]
    emit_radius 2
    emit_box [0 0 0 4 0 0]
    
    
    particle_lifetime [.5, 1]
    speed_start [0, 1]

    rotation [0 360]

    size [0 1]
    size_in .1
    size_out .9
    inherit_speed .15

    scripts {
        ParticleGlobalForce {
            id Wind
            amount 3
        }
    }
}
```

---

### `SandStormBuff`
**Source:** `particles.gon`  

```
SandStormBuff {
    movieclip SandStormParticle
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    ownership local
    projection_matrix default
    
    emit_rate 100
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 180
    emit_box [0 0 0 1 0 0]
    live_bounds [-999 999  -999 999 -999 999]
    
    
    particle_lifetime [.1 1]
    speed_start 1
    size_start [.4 .6]
    size_end 0
    alpha_start -1
    alpha_end 2
    speed_scale .25
    face_moving_direction true
    
    scripts {
        ParticleBouncePlane {
            dampening 0
            friction 1
        }

        ParticleTornadoForce {
            point [0 0 0]
            axis [0 1 0]
            force 10
        }
    }
}
```

---

### `AbsorbBuff`
**Source:** `particles.gon`  

```
AbsorbBuff {
    movieclip ManaParticle
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    ownership local
    projection_matrix default
    
    emit_rate 4
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 180
    emit_box [0 0 0 1 0 0]
    live_bounds [-999 999  -999 999 -999 999]
    
    
    particle_lifetime [.5 1.5]
    speed_start 1
    size_start [2, 3]
    size_end .5
    alpha_start -1
    alpha_end 2
    speed_scale 0
    face_moving_direction true
    
    scripts {
        ParticleBouncePlane {
            dampening 0
            friction 1
        }

        ParticleTornadoForce {
            point [0 0 0]
            axis [0 1 0]
            force 1
        }
    }
}
```

---

### `FlyBuff`
**Source:** `particles.gon`  

```
FlyBuff {
    movieclip Critter_Fly
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    ownership local
    projection_matrix default
    
    emit_rate 50
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 180
    emit_box [0 0 0 1 0 0]
    live_bounds [-999 999  -999 999 -999 999]
    
    
    particle_lifetime [.5 1.5]
    speed_start 1
    size_start [3 4]
    size_end 0
    alpha_start -1
    alpha_end 2
    speed_scale .25
    face_moving_direction true
    
    scripts {
        ParticleBouncePlane {
            dampening 0
            friction 1
        }

        ParticleTornadoForce {
            point [0 -8 0]
            axis [0 1.5 0]
            force 2
        }
    }
}
```

---

### `SpikeBuff`
**Source:** `particles.gon`  

```
SpikeBuff {
    movieclip Particle_Thorns
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    ownership local
    projection_matrix default
    
    emit_rate 4
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 180
    emit_box [0 0 0 1 0 0]
    live_bounds [-999 999  -999 999 -999 999]
    
    
    particle_lifetime .5
    speed_start .5
    size_start .3
    size_end .5
    alpha_start 1
    alpha_end 2
    speed_scale .25
    face_moving_direction true
    
    scripts {
        ParticleBouncePlane {
            dampening 0
            friction 1
        }
    }
}
```

---

### `ShineBuff`
**Source:** `particles.gon`  

```
ShineBuff {
    movieclip SparkleParticle
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    ownership local
    projection_matrix default
    
    emit_rate 15
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 180
    emit_box [0 0 0 1 0 0]
    live_bounds [-999 999  -999 999 -999 999]
    
    
    particle_lifetime .5
    speed_start 1
    size_start .5
    size_end .7
    alpha_start .5
    alpha_end 2
    speed_scale .50
    face_moving_direction true
    
    scripts {
        ParticleBouncePlane {
            dampening 0
            friction 1
        }
    }
}
```

---

### `SmokeBuff`
**Source:** `particles.gon`  

```
SmokeBuff {
    movieclip ParticleSmoke1
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    ownership local
    projection_matrix default
    
    emit_rate 25
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_spread 100
    emit_box [0 0 0 1 0 0]
    live_bounds [-999 999  -999 999 -999 999]
    
    
    particle_lifetime [.5 1]
    speed_start .001
    size_start [1 1.4]
    size_end 0
    alpha_start -1
    alpha_end 2
    speed_scale .25
    face_moving_direction true
    
    scripts {
        ParticleBouncePlane {
            dampening 0
            friction 1
        }

        ParticleTornadoForce {
            point [1 1 1]
            axis [0 .5 0]
            force 1
        }
    }
}
```

---

### `AngelClouds`
**Source:** `particles.gon`  

```
AngelClouds {
    movieclip PuffNoOutline
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 1000
    emit_amount 1
    emit_direction [0, -1, 0]
    emit_spread 360
    emit_box [0 10 0 .1 0 10]
    live_bounds [-999 999  -999 999 -999 999]
    friction [.02 .2 .02]
    
    
    particle_lifetime  7
    speed_start [.1, .5]
    size_start [1 1.4]
    rotation [0 360]
    rotation_speed [-10, 10]
    rotation_speed_end 0
    alpha_in .2
    alpha_out .2
    alpha .05
    
    scripts {
        ParticleBouncePlane {
            dampening 0
            friction 1
        }

        ParticleGlobalForce {
            id Wind
            amount .1
        }

        ParticleCharacterCollision {
            character_sphere_offset 0
            pushforce 2
            inherit_velocity .5
        }
    }
}
```

---

### `Gibs_huge`
**Source:** `particles.gon`  

```
Gibs_huge {
    movieclip Gibs_Default

    render_mode separate
    
    simulation_space global
    projection_matrix default
    //continual_emission false
    
    emit_rate .5
    emit_amount 50
    emit_direction [0, .05, 0]
    emit_spread 360
    emit_shell .5
    emit_box [0, 0, 0, 0, 0, 0]
    live_bounds [-999 999 -999 999 -999 999]
    spurt GibsBloodSpurtHuge
    
    particle_lifetime  [1.5 3]
    speed_start [7 13]
    //speed_end 5
    force_start [0 -20 0]
    //rotation_start [0, 360]
    rotation_speed_start [-900, 900]
    rotation_speed_end 0
    size_start 1.2
    size_end 1
    alpha_start 9
    alpha_end 0
    //speed_scale 1
    //face_moving_direction true
    
    scripts {
        ParticleBouncePlane {
            dampening .5
            friction .1
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane back
            position 10.5
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane right
            position 10.5
        }
    }
}
```

---

### `GibsBloodSpurtHuge`
**Source:** `particles.gon`  

```
GibsBloodSpurtHuge {
    movieclip ParticleBlood

    render_mode separate
    
    //update_mode locked
    
    simulation_space global
    //ownership local
    projection_matrix default
    //continual_emission false
    
    emit_rate 1
    emit_amount 30
    emit_direction [0, 1, 0]
    emit_spread 60
    force_start [0 -30 0]
    
    
    particle_lifetime  [1 3]
    speed_start [1 5]

    size_start [.3 .8]
    size_end 0
    alpha_start [.1 2]
    alpha_end 0
    speed_scale 1.2
    inherit_speed [.4 1.5]//.21
    face_moving_direction true
    
    scripts {
        ParticleBouncePlane {
            dampening .5
            friction .1
        }
    }
}
```

---

### `PassiveEnergized`
**Source:** `particles.gon`  

```
PassiveEnergized {
    movieclip Particle_Electric
    unlit true
    
    /*render_mode default
    simulation_space local
    ownership local*/
    render_mode separate
    simulation_space global

    projection_matrix default
    
    emit_rate 15
    emit_amount 1
    emit_direction [0, 1, 0]
    emit_radius .4
    emit_spread 45
    friction [-.05 -.1 -.05]
    emit_box [0 0 .3 .3 0 0]
    live_bounds [-999 999 -999 999 -999 999]
    
    
    particle_lifetime .5
    speed_start [0 2]
    size_in .1
    size [.5 1]
    rotation [-90 90]
}
```

---

### `BloodRain`
**Source:** `particles.gon`  

```
BloodRain {
    movieclip Particle_BloodDrip
    
    render_mode separate
    
    //update_mode locked
    simulation_space global
    projection_matrix default
    
    emit_rate 200
    emit_amount 1
    emit_direction [0, 1, 0]
    //friction [.01 .01 .01]
    emit_spread 0
    live_bounds [-999 999  0 999 -999 999]
    emit_box [0 10 0 0 0 10]
    
    
    particle_lifetime  5
    speed_start 0
    size_start [.25 1]
    speed_scale .2
    alpha .5
    face_moving_direction true
    //chain bloodsplash
    force [0 10 0]

    scripts {
        ParticleGlobalForce {
            id Wind
            amount 1
        }
    }
}
```

---

### `Gibs_Medium`
**Source:** `particles.gon`  

```
Gibs_Medium {
    movieclip Gibs_Default

    render_mode separate
    
    simulation_space global
    projection_matrix default
    //continual_emission false
    
    emit_rate .5
    emit_amount 10
    emit_direction [0, 1, 0]
    emit_spread 60
    emit_shell .5
    emit_box [0, 0, 0, 0, 0, 0]
    live_bounds [-999 999 -999 999 -999 999]
    spurt GibsBloodSpurt
    
    particle_lifetime  [1.5 2]
    speed_start [3 7]
    //speed_end 5
    force_start [0 -20 0]
    //rotation_start [0, 360]
    rotation_speed_start [-900, 900]
    rotation_speed_end 0
    size_start 1.2
    size_end 1
    alpha_start 9
    alpha_end 0
    //speed_scale 1
    //face_moving_direction true
    
    scripts {
        ParticleBouncePlane {
            dampening .5
            friction .1
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane back
            position 10.5
        }
        ParticleBouncePlane {
            dampening .75
            friction 0
            plane right
            position 10.5
        }
    }
}
```

---

## File: `particles2d.gon`

### `RainB`
**Source:** `particles2d.gon`  

```
RainB {
    movieclip RainParticle
    
    render_mode default
    simulation_space global
    projection_matrix default
    render_layer background
    
    emit_rate 1000
    emit_amount 1
    emit_direction [.1, -1]
    //friction [.01 .01]
    emit_spread 0
    live_bounds [-999 999  0 999]
    emit_box [-20 50 40 40]
    
    
    particle_lifetime  5
    speed_start [25 50]
    size_start .3
    speed_scale .05
    alpha .1
    face_moving_direction true
    chain splashB
    force [0 -10]

    scripts {

    }
}
```

---

### `RainM`
**Source:** `particles2d.gon`  

```
RainM {
    movieclip RainParticle
    
    render_mode default
    simulation_space global
    projection_matrix default
    
    emit_rate 400
    emit_amount 1
    emit_direction [.1, -1]
    //friction [.01 .01]
    emit_spread 0
    live_bounds [-999 999  0 999]
    emit_box [-20 50 40 40]
    
    
    particle_lifetime  5
    speed_start 50
    size_start .5
    speed_scale .05
    alpha .5
    face_moving_direction true
    chain splashM
    force [0 -10]

    scripts {
        ParticleLineCollisions {
            end_on_collision true
        }
    }
}
```

---

### `RainF`
**Source:** `particles2d.gon`  

```
RainF {
    movieclip RainParticle
    
    render_mode default
    simulation_space global
    projection_matrix default
    
    emit_rate 100
    emit_amount 1
    emit_direction [.1, -1]
    //friction [.01 .01]
    emit_spread 0
    live_bounds [-999 999  0 999]
    emit_box [-20 50 40 40]
    
    
    particle_lifetime  5
    speed_start [50 75]
    size_start .7
    speed_scale .05
    alpha .3
    face_moving_direction true
    chain splashF
    force [0 -10]

    scripts {

    }
}
```

---

### `Rain`
**Source:** `particles2d.gon`  

```
Rain {
    combo [RainB RainM RainF]
}
```

---

### `splashM`
**Source:** `particles2d.gon`  

```
splashM {
    movieclip RainSplashParticle
    chain splashM2
    
    render_mode default
    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount [1 5]
    emit_direction [0, 1]
    emit_box [0 0 .01 .01]
    friction_start [0 0]
    friction_end [1 0]
    emit_spread 180
    live_bounds [-999 999  0 999]
    
    particle_lifetime 10
    speed_start 10
    size_start .2
    size_end 0
    speed_scale .2
    alpha .5
    face_moving_direction true
    force [0 -40]

    scripts {
        ParticleLineCollisions {
            dampening .5
            friction 0
        }
    }
}
```

---

### `splashM2`
**Source:** `particles2d.gon`  

```
splashM2 {
    movieclip RainSplashParticle
    
    render_mode default
    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount [1 10]
    emit_direction [0, 1]
    emit_box [0 0 .01 .01]
    friction_start [0 0]
    friction_end [1 0]
    emit_spread 180
    live_bounds [-999 999  0 999]
    
    particle_lifetime .5
    speed_start 10
    size_start .2
    size_end 0
    speed_scale .2
    alpha .5
    face_moving_direction true
    force [0 -40]

    scripts {
        ParticleLineCollisions {
            dampening .5
            friction 0
        }
    }
}
```

---

### `splashB`
**Source:** `particles2d.gon`  

```
splashB {
    movieclip RainSplashParticle

    render_mode default
    simulation_space global
    projection_matrix default
    render_layer background
    
    emit_rate 1
    emit_amount [1 5]
    emit_direction [0, 1]
    emit_box [0 0 .01 .01]
    friction_start [0 0]
    friction_end [1 0]
    emit_spread 180
    live_bounds [-999 999  0 999]
    
    particle_lifetime 10
    speed_start 10
    size_start .1
    size_end 0
    speed_scale .2
    alpha .2
    face_moving_direction true
    force [0 -40]

    scripts {
        ParticleLineCollisions {
            dampening .5
            friction 0
        }
    }
}
```

---

### `splashF`
**Source:** `particles2d.gon`  

```
splashF {
    movieclip RainSplashParticle

    render_mode default
    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount [1 5]
    emit_direction [0, 1]
    emit_box [0 0 .01 .01]
    friction_start [0 0]
    friction_end [1 0]
    emit_spread 180
    live_bounds [-999 999  0 999]
    
    particle_lifetime 10
    speed_start 10
    size_start .2
    size_end 0
    speed_scale .2
    alpha .3
    face_moving_direction true
    force [0 -40]

    scripts {
        ParticleLineCollisions {
            dampening .5
            friction 0
        }
    }
}
```

---

### `SnowM`
**Source:** `particles2d.gon`  

```
SnowM {
    movieclip ParticleTestNoRandom
    
    render_mode default
    simulation_space global
    projection_matrix default
    
    
    emit_rate 250
    emit_amount 1
    emit_direction [0, -1]
    emit_spread 10
    emit_box [-20 50 40 40]
    live_bounds [-999 999  -999 999]
    
    
    particle_lifetime 20
    speed_start [2, 4]
    size [.3 .8]
    size_out .25
    rotation [0 360]
    rotation_speed [-100, 100]
    rotation_speed_end 0
    alpha .5
    
    scripts {
        ParticleBouncePlane {
            dampening 1
            friction 1
        }
        ParticleLineCollisions {
            dampening 1
            friction 1
        }
    }
}
```

---

### `SnowB`
**Source:** `particles2d.gon`  

```
SnowB {
    movieclip ParticleTestNoRandom
    
    render_mode default
    simulation_space global
    projection_matrix default
    render_layer background
    
    emit_rate 100
    emit_amount 1
    emit_direction [0, -1]
    emit_spread 10
    emit_box [-20 50 40 40]
    live_bounds [-999 999  -999 999]
    
    
    particle_lifetime  20
    speed_start [2, 4]
    size [.2 .6]
    size_out .25
    rotation [0 360]
    rotation_speed [-100, 100]
    rotation_speed_end 0
    alpha .3
    
    scripts {
        ParticleBouncePlane {
            dampening 1
            friction 1
        }
    }
}
```

---

### `SnowF`
**Source:** `particles2d.gon`  

```
SnowF {
    movieclip ParticleTestNoRandom
    
    render_mode default
    simulation_space global
    projection_matrix default

    emit_rate 30
    emit_amount 1
    emit_direction [0, -1]
    emit_spread 10
    emit_box [-20 50 40 40]
    live_bounds [-999 999  -999 999]
    
    
    particle_lifetime  20
    speed_start [3, 5]
    size [.4 .9]
    size_out .25
    rotation [0 360]
    rotation_speed [-100, 100]
    rotation_speed_end 0
    alpha .3
    
    scripts {
        ParticleBouncePlane {
            dampening 1
            friction 1
        }
    }
}
```

---

### `Snow`
**Source:** `particles2d.gon`  

```
Snow {
    combo [SnowB SnowM SnowF]
}
```

---

### `WindLeavesF`
**Source:** `particles2d.gon`  

```
WindLeavesF {
    movieclip Particle_WindLeaf
    
    render_mode default
    simulation_space global
    projection_matrix default
    
    emit_rate 25
    emit_amount 1
    emit_direction [1, 0]
    emit_spread 30
    emit_box [-20 50 0 40]
    live_bounds [-999 999  -999 999]
    //friction [.01 .01 .01]
    //force_end [0 -1 0]
    
    particle_lifetime [2 10]
    speed_start [0, 2]
    size [.3 .8]
    alpha 1
    alpha_in .2
    alpha_out .2

    //force [3 0]
    
    scripts {
        ParticleBouncePlane {
            dampening .75
            friction 0
        }

        ParticleRandomForce [3, [-1, 1]]
    }
}
```

---

### `WindLeavesB`
**Source:** `particles2d.gon`  

```
WindLeavesB {
    movieclip Particle_WindLeaf
    
    render_mode default
    simulation_space global
    projection_matrix default
    render_layer background
    
    emit_rate 50
    emit_amount 1
    emit_direction [1, 0]
    emit_spread 30
    emit_box [-20 50 0 40]
    live_bounds [-999 999  -999 999]
    //friction [.01 .01 .01]
    //force_end [0 -1 0]
    
    particle_lifetime [2 10]
    speed_start [0, 2]
    size [.3 .8]
    alpha 1
    alpha_in .2
    alpha_out .2

    //force [3 0]
    
    scripts {
        ParticleBouncePlane {
            dampening .75
            friction 0
        }

        ParticleRandomForce [3, [-1, 1]]
    }
}
```

---

### `WindDebris`
**Source:** `particles2d.gon`  

```
WindDebris {
    movieclip Particle_WindDebris
    
    render_mode default
    simulation_space global
    projection_matrix default
    
    emit_rate 100
    emit_amount 1
    emit_direction [1, 0]
    emit_spread 10
    emit_box [-20 50 0 40]
    live_bounds [-999 999  -999 999]
    //friction [.1 .1 .1]
    //force_end [0 -1 0]
    
    particle_lifetime [2 4]
    speed_start [2, 4]
    size [.1 1]
    //speed_scale 3
    //face_moving_direction true
    size_in .5
    size_out .5

    force [6 0]
    
    scripts {
    }
}
```

---

### `WindDust`
**Source:** `particles2d.gon`  

```
WindDust {
    movieclip Particle_WindDust
    
    render_mode default
    simulation_space global
    projection_matrix default
    //material mist
    
    emit_rate 100
    emit_amount 1
    emit_direction [1, 0]
    emit_spread 10
    emit_box [-20 50 0 40]
    live_bounds [-999 999  -999 999]
    //friction [.1 .1 .1]
    //force_end [0 -1 0]
    
    particle_lifetime [2 4]
    speed_start [2, 4]
    size [.1 1]
    alpha .03
    alpha_in .3
    alpha_out .3
    //speed_scale 3
    //face_moving_direction true
    size [1 3]

    force [6 0]
    
    scripts {
    }
}
```

---

### `WindWisps`
**Source:** `particles2d.gon`  

```
WindWisps {
    movieclip Particle_WindWisps
    
    render_mode default
    simulation_space global
    projection_matrix default
    //material mist
    
    emit_rate 20
    emit_amount 1
    emit_direction [1, 0]
    emit_spread 10
    emit_box [-20 50 0 40]
    live_bounds [-999 999  -999 999]
    //friction [.1 .1 .1]
    //force_end [0 -1 0]
    
    particle_lifetime 2
    speed_start .001
    alpha .5
    //speed_scale 3
    face_moving_direction true
    size [1 3]
}
```

---

### `WindFull`
**Source:** `particles2d.gon`  

```
WindFull {
    combo [WindDebris WindLeavesF WindLeavesB WindDust WindWisps]
}
```

---

### `TRainB`
**Source:** `particles2d.gon`  

```
TRainB {
    movieclip RainParticle
    
    render_mode default
    simulation_space global
    projection_matrix default
    render_layer background
    
    emit_rate 1000
    emit_amount 1
    emit_direction [.3, -1]
    //friction [.01 .01]
    emit_spread 0
    live_bounds [-999 999  0 999]
    emit_box [-30 50 40 40]
    
    
    particle_lifetime  5
    speed_start [25 50]
    size_start .3
    speed_scale .05
    alpha .1
    face_moving_direction true
    chain splashB
    force [0 -10]

    scripts {

    }
}
```

---

### `TRainM`
**Source:** `particles2d.gon`  

```
TRainM {
    movieclip RainParticle
    
    render_mode default
    simulation_space global
    projection_matrix default
    
    emit_rate 800
    emit_amount 1
    emit_direction [.3, -1]
    //friction [.01 .01]
    emit_spread 0
    live_bounds [-999 999  0 999]
    emit_box [-30 50 40 40]
    
    
    particle_lifetime  5
    speed_start 50
    size_start .5
    speed_scale .05
    alpha .5
    face_moving_direction true
    chain TsplashM
    force [0 -10]

    scripts {
        ParticleLineCollisions {
            end_on_collision true
        }
    }
}
```

---

### `TRainF`
**Source:** `particles2d.gon`  

```
TRainF {
    movieclip RainParticle
    
    render_mode default
    simulation_space global
    projection_matrix default
    
    emit_rate 200
    emit_amount 1
    emit_direction [.3, -1]
    //friction [.01 .01]
    emit_spread 0
    live_bounds [-999 999  0 999]
    emit_box [-30 50 40 40]
    
    
    particle_lifetime  5
    speed_start [50 75]
    size_start .7
    speed_scale .05
    alpha .3
    face_moving_direction true
    chain splashF
    force [0 -10]

    scripts {

    }
}
```

---

### `TsplashM`
**Source:** `particles2d.gon`  

```
TsplashM {
    movieclip RainSplashParticle
    chain splashM2
    
    render_mode default
    simulation_space global
    projection_matrix default
    
    emit_rate 1
    emit_amount [1 2]
    emit_direction [0, 1]
    emit_box [0 0 .01 .01]
    friction_start [0 0]
    friction_end [1 0]
    emit_spread 180
    live_bounds [-999 999  0 999]
    
    particle_lifetime 10
    speed_start 10
    size_start .2
    size_end 0
    speed_scale .2
    alpha .5
    face_moving_direction true
    force [20 -40]

    scripts {
        ParticleLineCollisions {
            dampening .5
            friction 0
        }
    }
}
```

---

### `Thunderstorm`
**Source:** `particles2d.gon`  

```
Thunderstorm {
    combo [TRainB TRainM TRainF /*WindDebris WindLeavesF WindLeavesB*/ WindDust /*WindWisps*/]
}
```

---

