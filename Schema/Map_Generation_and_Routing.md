# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Map Generation & Routing

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `empty, battle, npc` | Classification type. |
| `easy` | [`Array`](./Arrays.md#array-easy) | `[ easy bigsharklevels ], [ easy ]` |  |
| `folder` | [`Enum/String`](./Enums.md#enum-folder) | `alley, bunker, boneyard` |  |
| `hard` | [`Array`](./Arrays.md#array-hard) | `[ easy bigsharklevels ], [ easy ], [ hard ]` |  |
| `miniboss` | [`Array`](./Arrays.md#array-miniboss) | `[ miniboss ]` |  |
| `normal` | [`Array`](./Arrays.md#array-normal) | `[ common boneyard_events.gon ], [ common bunker_events.gon ], [ common alley_events.gon ]` |  |
| `rare` | [`Array`](./Arrays.md#array-rare) | `[ rare ]` |  |
| `chapter_item_pool` | [`Enum/String`](./Enums.md#enum-chapter_item_pool) | `boneyarditems, alleyitems, bunkeritems` |  |
| `large` | [`Array`](./Arrays.md#array-large) | `[ KillDozer ], [ Shambler ], [ ]` |  |
| `medium` | [`Array`](./Arrays.md#array-medium) | `[ ZombieCat SkeletonCat TallSkeletonCat WolfCat Tatters S..., [ Rat Leaper Pooter Kitten TomTom Mangy CatCaller ], [ AtomicKitten RoboTom CatCultist Cultist CultistZealot C...` |  |
| `small` | [`Array`](./Arrays.md#array-small) | `[ ], [ Maggot Fly Flea Pinky ], [ Flea Wisp Fly Maggot ]` |  |
| `special` | [`Array`](./Arrays.md#array-special) | `[ special ]` |  |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `Treasure_LargeMeteor, Treasure_SmallMeteor, TreasureHard` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNode_SmallMeteor, Rare_Treasure, MapNode_LargeMetor` |  |
| `jestercat` | [`Enum/String`](./Enums.md#enum-jestercat) | `auto` |  |
| `abandonedones` | [`Enum/String`](./Enums.md#enum-abandonedones) | `auto` |  |
| `advance` | Number | `1` |  |
| `alley` | Block | `{ ... }` |  |
| `boneyard` | Block | `{ ... }` |  |
| `bumblefoot` | [`Enum/String`](./Enums.md#enum-bumblefoot) | `auto` |  |
| `bunker` | Block | `{ ... }` |  |
| `butchercat` | [`Enum/String`](./Enums.md#enum-butchercat) | `auto` |  |
| `cancreeper` | [`Enum/String`](./Enums.md#enum-cancreeper) | `auto` |  |
| `cavecatfamily` | [`Enum/String`](./Enums.md#enum-cavecatfamily) | `auto` |  |
| `caves` | Block | `{ ... }` |  |
| `cerberubs` | [`Enum/String`](./Enums.md#enum-cerberubs) | `auto` |  |
| `choose_one` | [`Array`](./Arrays.md#array-choose_one) | `[ GenFlag_Boss_Stacy, GenFlag_Boss_Spewer ]` |  |
| `clericcat` | [`Enum/String`](./Enums.md#enum-clericcat) | `auto` |  |
| `core` | Block | `{ ... }` |  |
| `crater` | Block | `{ ... }` |  |
| `desert` | Block | `{ ... }` |  |
| `dinocouple` | [`Enum/String`](./Enums.md#enum-dinocouple) | `auto` |  |
| `drmangler` | [`Enum/String`](./Enums.md#enum-drmangler) | `auto` |  |
| `druidcat` | [`Enum/String`](./Enums.md#enum-druidcat) | `auto` |  |
| `fightercat` | [`Enum/String`](./Enums.md#enum-fightercat) | `auto` |  |
| `flushmaster` | [`Enum/String`](./Enums.md#enum-flushmaster) | `auto` |  |
| `gambit` | [`Enum/String`](./Enums.md#enum-gambit) | `auto` |  |
| `head_start` | Number | `99` |  |
| `huntercat` | [`Enum/String`](./Enums.md#enum-huntercat) | `auto` |  |
| `iceelemental` | [`Enum/String`](./Enums.md#enum-iceelemental) | `auto` |  |
| `infestedduo` | [`Enum/String`](./Enums.md#enum-infestedduo) | `auto` |  |
| `junkyard` | Block | `{ ... }` |  |
| `lab` | Block | `{ ... }` |  |
| `lenny` | [`Enum/String`](./Enums.md#enum-lenny) | `auto` |  |
| `lightningelemental` | [`Enum/String`](./Enums.md#enum-lightningelemental) | `auto` |  |
| `locked` | Boolean | `true` |  |
| `magecat` | [`Enum/String`](./Enums.md#enum-magecat) | `auto` |  |
| `mamamaggot` | [`Enum/String`](./Enums.md#enum-mamamaggot) | `auto` |  |
| `meatworld` | Block | `{ ... }` |  |
| `monkcat` | [`Enum/String`](./Enums.md#enum-monkcat) | `auto` |  |
| `moon` | Block | `{ ... }` |  |
| `musiclayer` | [`Enum/String`](./Enums.md#enum-musiclayer) | `boss` |  |
| `necrocat` | [`Enum/String`](./Enums.md#enum-necrocat) | `auto` |  |
| `nemesis` | [`Array`](./Arrays.md#array-nemesis) | `[ nemesis ]` |  |
| `psychiccat` | [`Enum/String`](./Enums.md#enum-psychiccat) | `auto` |  |
| `queenhippo` | [`Enum/String`](./Enums.md#enum-queenhippo) | `auto` |  |
| `radicalrat` | [`Enum/String`](./Enums.md#enum-radicalrat) | `auto` |  |
| `ratking` | [`Enum/String`](./Enums.md#enum-ratking) | `auto` |  |
| `repeat` | [`Enum/String`](./Enums.md#enum-repeat) | `never` |  |
| `rockybobo` | [`Enum/String`](./Enums.md#enum-rockybobo) | `auto` |  |
| `sewers` | Block | `{ ... }` |  |
| `slime` | [`Enum/String`](./Enums.md#enum-slime) | `auto` |  |
| `spawn_node` | [`Enum/String`](./Enums.md#enum-spawn_node) | `start` |  |
| `spewer` | [`Enum/String`](./Enums.md#enum-spewer) | `auto` |  |
| `stacy` | [`Enum/String`](./Enums.md#enum-stacy) | `auto` |  |
| `tankcat` | [`Enum/String`](./Enums.md#enum-tankcat) | `auto` |  |
| `thebloat` | [`Enum/String`](./Enums.md#enum-thebloat) | `auto` |  |
| `thiefcat` | [`Enum/String`](./Enums.md#enum-thiefcat) | `auto` |  |
| `tinkerercat` | [`Enum/String`](./Enums.md#enum-tinkerercat) | `auto` |  |
| `trampy` | [`Enum/String`](./Enums.md#enum-trampy) | `auto` |  |
| `zodiac` | [`Enum/String`](./Enums.md#enum-zodiac) | `auto` |  |

</details>

---

### Context: `exit0`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean | `false, true` |  |
| `next_map` | [`Enum/String`](./Enums.md#enum-next_map) | `meatworld.gon, core.gon, sewers.gon` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNodeExit_Core, MapNodeExit_MeatWorld, MapNodeExit_Sewers` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `exit` | Classification type. |
| `hidden` | Boolean | `false, true` |  |

</details>

---

### Context: `quest_event`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNode_Veins, MapNode_VeinsDrained, MapNode_Empty` |  |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `Quest_WallOfFlesh, Quest_ThrobbingArtery2, Quest_ThrobbingArtery` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `empty, special_event` | Classification type. |

</details>

---

### Context: `boss`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `boss` | Classification type. |
| `boss_cutscene` | [`Enum/String`](./Enums.md#enum-boss_cutscene) | `spiderkitten, johnny, dybbuk` |  |
| `is_final_boss` | Boolean | `true` |  |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `spewer, stacy` |  |
| `override_music` | [`Enum/String`](./Enums.md#enum-override_music) | `chaos_boss, finalboss` |  |
| `tileset` | [`Enum/String`](./Enums.md#enum-tileset) | `finalboss` |  |
| `unlockcheck_on_complete` | [`Enum/String`](./Enums.md#enum-unlockcheck_on_complete) | `map_unlock_junkyard` |  |

</details>

---

### Context: `exit1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean | `false, true` |  |
| `next_map` | [`Enum/String`](./Enums.md#enum-next_map) | `crater.gon, future.gon, junkyard.gon` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNodeExit_Future, MapNodeExit_Junkyard, MapNodeExit_Crater` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `exit` | Classification type. |

</details>

---

### Context: `time_machine`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `Quest_TimeMachineFuture, Quest_TimeMachineJurassic, Quest_TimeMachineIceAge` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNode_TimeMachine` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `special_event` | Classification type. |

</details>

---

### Context: `hard_initial`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `locked` | Boolean | `false, true` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `hard` | Classification type. |

</details>

---

### Context: `exit_desert`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `true` |  |
| `locked` | Boolean | `true` |  |
| `next_map` | [`Enum/String`](./Enums.md#enum-next_map) | `desert.gon` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNodeExit_Desert` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `exit` | Classification type. |

</details>

---

### Context: `exit_lab`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `true` |  |
| `locked` | Boolean | `true` |  |
| `next_map` | [`Enum/String`](./Enums.md#enum-next_map) | `lab.gon` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNodeExit_Lab` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `exit` | Classification type. |

</details>

---

### Context: `mw_boss`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `boss_cutscene` | [`Enum/String`](./Enums.md#enum-boss_cutscene) | `throbbingking` |  |
| `override_music` | [`Enum/String`](./Enums.md#enum-override_music) | `throbbingking` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `boss` | Classification type. |

</details>

---

### Context: `mw_quest_event`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `Quest_DeadKing` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNode_DeadKing` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `special_event` | Classification type. |

</details>

---

### Context: `mw_hard1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `musiclayer` | [`Enum/String`](./Enums.md#enum-musiclayer) | `boss` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `hard` | Classification type. |

</details>

---

### Context: `miniboss_event`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `empty, special_event` | Classification type. |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `StacyMutant1` |  |

</details>

---

### Context: `mw_altar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `Quest_MeatWorldAltar` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `MapNode_MeatAltar` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `special_event` | Classification type. |

</details>

---

### Context: `mw_battle1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `battle` | Classification type. |

</details>

---

### Context: `mw_event1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `event` | Classification type. |

</details>

---

### Context: `mw_home`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `home` | Classification type. |

</details>

---

### Context: `mw_treasure`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `false, true` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `treasure` | Classification type. |

</details>

---

### Context: `shop_cheapwater`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `WaterShopCheap` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `cheapwatershop` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `shop` | Classification type. |

</details>

---

### Context: `shop_water`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `WaterShop` |  |
| `override_art` | [`Enum/String`](./Enums.md#enum-override_art) | `cheapwatershop` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `shop` | Classification type. |

</details>

---

### Context: `event`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `Butch_Tutorial` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `event` | Classification type. |

</details>

---

### Context: `mw_earlyhome`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `hidden` | Boolean | `true` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `home` | Classification type. |

</details>

---

### Context: `treasure`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `TreasureTutorial` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `treasure` | Classification type. |

</details>

---

### Context: `weather_event`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `level` | [`Enum/String`](./Enums.md#enum-level) | `CraterWeatherEvent` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `special_event` | Classification type. |

</details>

---

### Context: `battle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `battle` | Classification type. |

</details>

---

### Context: `dimensionx`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

</details>

---

### Context: `endoftime`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

</details>

---

### Context: `future`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

</details>

---

### Context: `home`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `home` | Classification type. |

</details>

---

### Context: `iceage`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

</details>

---

### Context: `jurassic`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

</details>

---

### Context: `start`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `enter` | Classification type. |

</details>

---

### Context: `theend`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | `true` |  |

</details>

---

### Context: `BoneyardUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `BothObelisksUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `BunkerUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `CavesUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ChaosAntennaAttached`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `CoreObeliskUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `CoreUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `CraterUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `DimensionXUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `EndOfTimeUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `FutureUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `GenFlag_Boss_Spewer`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `GenFlag_Boss_Stacy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `HardPathUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `IceAgeUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `JunkyardUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `JurassicUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `MeatWorldUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `MeatWorldUnlockedFull`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `MoonObeliskUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `MoonUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `SewersUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `TheEndUnlocked`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `ThrobbingArteryDone`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `VolcanoAntennaAttached`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

### Context: `WallOfFleshDone`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

