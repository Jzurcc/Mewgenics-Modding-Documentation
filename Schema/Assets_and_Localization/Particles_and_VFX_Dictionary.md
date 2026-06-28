---
title: "Particles & VFX Schema"
description: "Identifiers for spawning visual effects."
---

# Particles & VFX Schema

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