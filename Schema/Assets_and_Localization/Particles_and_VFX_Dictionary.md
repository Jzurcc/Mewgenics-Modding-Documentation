---
title: "Particles & VFX Schema"
description: "Identifiers for spawning visual effects."
---

# Particles & VFX Schema


<details open>
<summary><strong>Quick Navigation</strong></summary>

<table>
  <tr>
    <td width="22%"><strong>Core Entities & Combat</strong></td>
    <td><a href="../Core_Entities_and_Combat/Abilities_and_Spells.md">Abilities & Spells</a> • <a href="../Core_Entities_and_Combat/Characters_and_Bosses.md">Characters & Bosses</a> • <a href="../Core_Entities_and_Combat/Items_and_Equipment.md">Items & Equipment</a> • <a href="../Core_Entities_and_Combat/Passives_and_Statuses.md">Passives & Statuses</a> • <a href="../Core_Entities_and_Combat/Elite_Buffs.md">Elite Buffs</a> • <a href="../Core_Entities_and_Combat/Enemy_AI.md">Enemy AI</a> • <a href="../Core_Entities_and_Combat/Status_Effect_Keywords.md">Status Keywords</a></td>
  </tr>
  <tr>
    <td><strong>Engine Scripts & Logic</strong></td>
    <td><a href="../Engine_Scripts_and_Logic/Engine_LogicKeys.md">Logic Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_EventKeys.md">Event Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_DamagingKeys.md">Damaging Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md">Status & Passive Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md">Global Modifiers</a> • <a href="../Engine_Scripts_and_Logic/Math_Equations.md">Math Equations</a></td>
  </tr>
  <tr>
    <td><strong>Player Progression & Cats</strong></td>
    <td><a href="../Player_Progression_and_Cats/Cat_Classes.md">Cat Classes</a> • <a href="../Player_Progression_and_Cats/Cat_Mutations.md">Cat Mutations</a> • <a href="../Player_Progression_and_Cats/Custom_Cats.md">Custom Cats</a> • <a href="../Player_Progression_and_Cats/Injuries.md">Injuries</a> • <a href="../Player_Progression_and_Cats/Progression_Unlocks.md">Progression Unlocks</a> • <a href="../Player_Progression_and_Cats/Combat_Rewards.md">Combat Rewards</a></td>
  </tr>
  <tr>
    <td><strong>World, Maps & Events</strong></td>
    <td><a href="../World_Maps_and_Events/Events_and_Encounters.md">Events & Encounters</a> • <a href="../World_Maps_and_Events/House_and_Environment.md">House & Environment</a> • <a href="../World_Maps_and_Events/Map_Generation_and_Routing.md">Map Gen & Routing</a> • <a href="../World_Maps_and_Events/Furniture_and_Metaprogression.md">Furniture & Meta</a> • <a href="../World_Maps_and_Events/Shops.md">Shops</a> • <a href="../World_Maps_and_Events/Spawns_and_Enemy_Pools.md">Spawns & Enemy Pools</a> • <a href="../World_Maps_and_Events/Boss_Cutscene_Info.md">Boss Cutscenes</a> • <a href="../World_Maps_and_Events/NPC_Scripts.md">NPC Scripts</a></td>
  </tr>
  <tr>
    <td><strong>Assets & Localization</strong></td>
    <td><a href="../Assets_and_Localization/Audio_SFX_Dictionary.md">Audio SFX</a> • <a href="../Assets_and_Localization/Particles_and_VFX_Dictionary.md">Particles & VFX</a> • <a href="../Assets_and_Localization/Damage_Text_Styles.md">Damage Text</a> • <a href="../Assets_and_Localization/Localization_Guide.md">Localization Guide</a> • <a href="../Assets_and_Localization/Text_Formatting_and_Effects.md">Text Formatting</a> • <a href="../Assets_and_Localization/Strings.md">Strings</a></td>
  </tr>
  <tr>
    <td><strong>Reference & Meta</strong></td>
    <td><a href="../Reference_and_Meta/Enums.md">Enums</a> • <a href="../Reference_and_Meta/Arrays.md">Arrays</a> • <a href="../Reference_and_Meta/Item_Pools.md">Item Pools</a> • <a href="../Reference_and_Meta/Difficulties.md">Difficulties</a> • <a href="../Reference_and_Meta/Engine_Hidden_Passives_and_Statuses.md">Hidden Passives</a> • <a href="../Reference_and_Meta/Passive_Identifiers_Audit.md">Passive Audit</a> • <a href="../Reference_and_Meta/Engine_Uncategorized_Resources.md">Uncategorized Keys</a> • <a href="../Reference_and_Meta/Miscellaneous.md">Miscellaneous</a></td>
  </tr>
</table>

</details>

## Overview
> [!NOTE]
> This schema describes how to hook engine events up to the particle emitter systems for cool visual bursts.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
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

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Particles_and_VFX_Dictionary.md`](../../Directory/System_and_Engine/Particles_and_VFX_Dictionary.md)

---



> **Associated Files:** `data/particles.gon`, `data/particles2d.gon`

This document lists all valid Particle and VFX triggers parsed from the unpacked particle `.gon` files. These keys can be used in `graphics {}` blocks to spawn effects.

## particles.gon (183 particles)

- `AbsorbBuff`
- `AcidRain`
- `AcidSplash`
- `AngelClouds`
- `Blood`
- `BloodBounce`
- `BloodBounceCrit`
- `BloodBounceCrit_Absorb`
- `BloodBounce_Absorb`
- `BloodCrit`
- `BloodCrit_Absorb`
- `BloodPoof`
- `BloodPoofCrit`
- `BloodPoofCrit_Absorb`
- `BloodPoof_Absorb`
- `BloodPopCrit`
- `BloodPopCrit_Absorb`
- `BloodRain`
- `Blood_Absorb`
- `CaveDrip`
- `CaveSplash`
- `ChaosTPIn`
- `ChaosTPOut`
- `ChaosTPTracer`
- `Confetti`
- `CoreHeatWave_Distortion`
- `CraterLeaves`
- `CreepBubbles`
- `DarkFog`
- `DruidFlowersVictory`
- `EQRocks`
- `Embers`
- `Feathers`
- `FevaporateDark`
- `FevaporateLight`
- `FightBallCloud`
- `FinalEvaporate`
- `FireBallTrail`
- `FireBase`
- `FireBaseLarge`
- `FireBaseSmall`
- `FireExtinguish`
- `FireExtinguish_Steam`
- `FireFull`
- `FireFullLarge`
- `FireFullSmall`
- `FirePlumes`
- `FirePlumesLarge`
- `FirePlumesSmall`
- `FireSmoke`
- `FireSmokeLarge`
- `FireSmokeSmall`
- `FireStorm`
- `FireTileSmall`
- `FireWaves`
- `FireWavesLarge`
- `FireWavesSmall`
- `FireWhites`
- `FireWhitesLarge`
- `FireWhitesSmall`
- `Firenado`
- `Firenado_Embers`
- `Firenado_Fire`
- `Firestorm_Distortion`
- `Firestorm_Embers`
- `Firestorm_Fire`
- `FloatingRocks`
- `FlyBuff`
- `Fog`
- `GibsBloodSpurt`
- `GibsBloodSpurtHuge`
- `Gibs_Medium`
- `Gibs_animal`
- `Gibs_bag`
- `Gibs_blob`
- `Gibs_box`
- `Gibs_bug`
- `Gibs_cactus`
- `Gibs_cat`
- `Gibs_default`
- `Gibs_demon`
- `Gibs_fetus`
- `Gibs_huge`
- `Gibs_humanoid`
- `Gibs_plant`
- `Gibs_poop`
- `Gibs_rat`
- `Gibs_robot`
- `Gibs_rock`
- `Gibs_skeleton`
- `Gibs_terminatorskin`
- `GlitchShards`
- `GlitchTile`
- `GravityBurst`
- `GravityBurstB`
- `GravityBurstS`
- `GravityHoverRings`
- `GroundPoof`
- `GuillotinaGuts`
- `HadoukenBall`
- `HairballTrail`
- `HeatWave`
- `HeatWave_Distortion`
- `HeatWave_Particles`
- `Kingblood1`
- `Kingblood2`
- `Lava_Distortion`
- `MagicMissileTrail`
- `MagicMissileTrailSmall`
- `ManaDrain`
- `MeatCaveDrip`
- `MeatCaveSplash`
- `MegaBlast`
- `MegaBlastA`
- `MegaBlastB`
- `Meteornado`
- `MiniSplatter`
- `MiniSplatter2`
- `MiniSplatter3`
- `Mist`
- `PassiveBleed`
- `PassiveEnergized`
- `PassiveFire`
- `PassivePoison`
- `PassiveScrambled`
- `PassiveStealth`
- `PassiveTar`
- `PassiveWet`
- `PointPoof`
- `PointSmoke`
- `Rain`
- `RocketTrail`
- `SandStorm`
- `SandStormBuff`
- `ShineBuff`
- `SmallDirt`
- `SmokeBuff`
- `Snow`
- `SparkleBuff`
- `SpikeBuff`
- `SplatterLarge`
- `SplatterMed`
- `SplatterSmall`
- `SplatterXL`
- `TinkererVictoryFirework`
- `TormentorFull`
- `TormentorGuts`
- `ToxicBubbles`
- `TrackingTest`
- `VolcanoSpurt`
- `VolcanoSpurt_Trail`
- `WindDebris`
- `WindDust`
- `WindFull`
- `WindLeaves`
- `WindWisps`
- `alienLaserCharge`
- `coolLaserBeam`
- `coolLaserBeamInner`
- `coolLaserBeamOuter`
- `druidFlowers`
- `dustCloud`
- `fartoom`
- `fartoom_burst`
- `fartoom_trail`
- `firework`
- `firework_burst`
- `firework_burst_recursive`
- `firework_bursta`
- `firework_burstb`
- `healing_gas`
- `musicalSwirl`
- `splash`
- `test`
- `test2`
- `test3`
- `test4`
- `test5`
- `test6`
- `test7`
- `test8`
- `test9`
- `test_tornado`

## particles2d.gon (23 particles)

- `Rain`
- `RainB`
- `RainF`
- `RainM`
- `Snow`
- `SnowB`
- `SnowF`
- `SnowM`
- `TRainB`
- `TRainF`
- `TRainM`
- `Thunderstorm`
- `TsplashM`
- `WindDebris`
- `WindDust`
- `WindFull`
- `WindLeavesB`
- `WindLeavesF`
- `WindWisps`
- `splashB`
- `splashF`
- `splashM`
- `splashM2`