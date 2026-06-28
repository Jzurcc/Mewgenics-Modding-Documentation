---
title: "Map Gen & Routing Schema"
description: "Biome layout rules and node generation logic."
---

# Map Gen & Routing Schema


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
> This schema feeds the procedural generator. It defines node types (combat, event, shop) and how they link together to form a playable map.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
levels {
    folder alley
    easy [easy]
    hard [easy] //switch this to "hard" in the brackets if we get specific hard levels in!
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Map_Generation_and_Routing.md`](../../Directory/World_and_Events/Map_Generation_and_Routing.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Map Generation & Routing

> **Associated Files:** `data/maps/`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 168

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 62 | `common`<br>`rare`<br>`cha` |
| [`boss`](./Map_Generation_and_Routing.md#object-boss) | Object  | An object defining the properties of a boss encounter, such as rewards or level. | 60 | `{ . . . }` |
| [`easy`](../Reference_and_Meta/Arrays.md#array-easy) | Array | Configuration for easy difficulty, including elite/champ budgets and rewards. | 59 | `[easy bigsharklevels]`<br>`[easy]` |
| [`miniboss`](../Reference_and_Meta/Arrays.md#array-miniboss) | Array | An array or object defining the reward table for miniboss encounters, including coin ranges, food ranges, and loot chances. | 42 | `[miniboss]` |
| `rare` | `Array`  | Defines the rare reward block for a boss encounter. | 40 | `1`<br>`10`<br>`15` |
| [`special`](../Reference_and_Meta/Arrays.md#array-special) | Array | An array or boolean indicating that an item or entry is a special container or category. | 38 | `[special]`<br>`true` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 34 | `{ . . . }` |
| [`hard`](../Reference_and_Meta/Arrays.md#array-hard) | Array | Configuration for hard difficulty, including elite/champ budgets and rewards. | 24 | `[easy bigsharklevels]`<br>`[easy]`<br>`[hard]` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 22 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`normal`](../Reference_and_Meta/Arrays.md#array-normal) | Array | An array or object defining the reward table for normal encounters, including coin ranges, food ranges, and loot chances. | 20 | `[` |
| [`folder`](../Reference_and_Meta/Enums.md#enum-folder) | Enum | The subdirectory or group name used to organize related levels or content. | 20 | `alley`<br>`boneyard`<br>`bunker` |
| [`small`](../Reference_and_Meta/Arrays.md#array-small) | Array | An array of enemy unit identifiers used as the small enemy pool for an area or boss encounter. | 19 | `[Amoeba]`<br>`[Flea Wisp Fly Maggot]`<br>`[Maggot Fly Flea Pinky]` |
| [`medium`](../Reference_and_Meta/Arrays.md#array-medium) | Array | An array of enemy unit identifiers used as the medium enemy pool for an area or boss encounter. | 19 | `[Rat Leaper Pooter Kitten TomTom Mangy CatCaller]` |
| [`large`](../Reference_and_Meta/Arrays.md#array-large) | Array | An array of enemy unit identifiers used as the large enemy pool for an area or boss encounter. | 19 | `[Carnibulb]`<br>`[KillDozer]`<br>`[MegaFetus]` |
| [`chapter_item_pool`](../Reference_and_Meta/Enums.md#enum-chapter_item_pool) | Enum | Specifies the item pool identifier used by a chapter or boss to determine which items can be found. | 19 | `alleyitems`<br>`boneyarditems`<br>`bunkeritems` |
| `include` | String | Specifies the path to another file to include and merge into the current schema definition. | 19 ||
| [`exit0`](./Map_Generation_and_Routing.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 15 | `{ . . . }` |
| [`treasure`](./Map_Generation_and_Routing.md#object-treasure) | Object | Defines a treasure node containing items or item pools. | 14 | `{ . . . }` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 12 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 12 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`quest_event`](./Map_Generation_and_Routing.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 9 | `{ . . . }` |
| [`alley`](./Map_Generation_and_Routing.md#object-alley) | Object | Specifies the name, map flag, or connection for the Alley area. | 7 | `{ . . . }` |
| [`jurassic`](./Map_Generation_and_Routing.md#object-jurassic) | Object | Specifies the name, map flag, or connection for the Jurassic area. | 7 | `{ . . . }` |
| [`caves`](./Map_Generation_and_Routing.md#object-caves) | Object | Specifies the name, map flag, or connection for the Caves area. | 7 | `{ . . . }` |
| [`bunker`](./Map_Generation_and_Routing.md#object-bunker) | Object | Specifies the name, map flag, or connection for the Bunker area. | 7 | `{ . . . }` |
| [`crater`](./Map_Generation_and_Routing.md#object-crater) | Object | Specifies the name, map flag, or connection for the Crater area. | 7 | `{ . . . }` |
| [`junkyard`](./Map_Generation_and_Routing.md#object-junkyard) | Object | Specifies the name, map flag, or connection for the Junkyard area. | 7 | `{ . . . }` |
| [`theend`](./Map_Generation_and_Routing.md#object-theend) | Object | Specifies the name, map flag, or connection for The End area. | 6 | `{ . . . }` |
| [`meatworld`](./Map_Generation_and_Routing.md#object-meatworld) | Object | An enum specifying the Meatworld chapter area, or an object with its specific properties. | 6 | `{ . . . }` |
| [`boneyard`](./Map_Generation_and_Routing.md#object-boneyard) | Object | Specifies the name, map flag, or connection for the Boneyard area. | 6 | `{ . . . }` |
| [`core`](./Map_Generation_and_Routing.md#object-core) | Object | Specifies the name, map flag, or connection for the Core area. | 6 | `{ . . . }` |
| [`moon`](./Map_Generation_and_Routing.md#object-moon) | Object | Specifies the name, map flag, or connection for the Moon area. | 6 | `{ . . . }` |
| [`iceage`](./Map_Generation_and_Routing.md#object-iceage) | Object | Specifies the name, map flag, or connection for the Ice Age area. | 6 | `{ . . . }` |
| [`future`](./Map_Generation_and_Routing.md#object-future) | Object | Specifies the name, map flag, or connection for the Future area. | 6 | `{ . . . }` |
| [`desert`](./Map_Generation_and_Routing.md#object-desert) | Object | Specifies the name, map flag, or connection for the Desert area. | 6 | `{ . . . }` |
| [`sewers`](./Map_Generation_and_Routing.md#object-sewers) | Object | Specifies the name, map flag, or connection for the Sewers area. | 6 | `{ . . . }` |
| [`lab`](./Map_Generation_and_Routing.md#object-lab) | Object | Specifies the name, map flag, or connection for the Lab area. | 5 | `{ . . . }` |
| [`time_machine`](./Map_Generation_and_Routing.md#object-time_machine) | Object | Defines a special event node that leads to a time machine quest level. | 4 | `{ . . . }` |
| [`dimensionx`](./Map_Generation_and_Routing.md#object-dimensionx) | Object | An enum specifying the Dimension X chapter area, or an object with its specific properties. | 4 | `{ . . . }` |
| [`jestercat`](../Reference_and_Meta/Enums.md#enum-jestercat) | Enum | Specifies the boss or miniboss configuration for JesterCat, often set to "auto" for procedural generation. | 3 | `auto` |
| [`exit1`](./Map_Generation_and_Routing.md#object-exit1) | Object  | An object defining the properties of the second exit from this node. | 3 | `{ . . . }` |
| [`start`](../Reference_and_Meta/Enums.md#enum-start) | Enum | Specifies the initial animation state played at the beginning of an ability. | 3 | `attack`<br>`lickAttack`<br>`monkAttack` |
| [`nemesis`](../Reference_and_Meta/Arrays.md#array-nemesis) | Array | A list of nemesis definitions to use for this level. | 3 | `[nemesis]` |
| [`endoftime`](./Map_Generation_and_Routing.md#object-endoftime) | Object | Configures various attributes of the End of Time area, depending on context. | 3 | `{ . . . }` |
| [`battle`](./Map_Generation_and_Routing.md#object-battle) | Object | Defines a battle encounter by preset, level file path, or reverb settings. | 2 | `{ . . . }` |
| [`home`](./Map_Generation_and_Routing.md#object-home) | Object | Specifies the option to go home (exit to the main hub). | 2 | `{ . . . }` |
| [`event`](../Reference_and_Meta/Enums.md#enum-event) | Enum | Specifies the event to force, either by name or by a nested object defining its type and level. | 2 | `Blessing`<br>`Death`<br>`Tragedy` |
| [`BothObelisksUnlocked`](./Map_Generation_and_Routing.md#object-bothobelisksunlocked) | Object  | Configures the map event and art when both obelisks have been unlocked. | 2 | `{ . . . }` |
| [`hard_initial`](./Map_Generation_and_Routing.md#object-hard_initial) | Object  | An object defining the properties of the initial hard path node. | 2 | `{ . . . }` |
| [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#object-meatworldunlocked) | Object  | Configures the map event and routes when MeatWorld is initially unlocked. | 2 | `{ . . . }` |
| [`DimensionXUnlocked`](./Map_Generation_and_Routing.md#object-dimensionxunlocked) | Object  | Configures the map event and art when Dimension X is unlocked. | 2 | `{ . . . }` |
| [`EndOfTimeUnlocked`](./Map_Generation_and_Routing.md#object-endoftimeunlocked) | Object  | Configures the map event and route visibility when End of Time is unlocked. | 2 | `{ . . . }` |
| [`HardPathUnlocked`](./Map_Generation_and_Routing.md#object-hardpathunlocked) | Object  | Unlocks the hard difficulty path on the map, usually by setting a node's locked state to false. | 2 | `{ . . . }` |
| [`VolcanoAntennaAttached`](./Map_Generation_and_Routing.md#object-volcanoantennaattached) | Object  | Configures the map event and art when the Volcano Antenna has been attached. | 2 | `{ . . . }` |
| [`GenFlag_Boss_Spewer`](./Map_Generation_and_Routing.md#object-genflag_boss_spewer) | Object  | Configures the boss encounter event for the Spewer boss on the map. | 2 | `{ . . . }` |
| [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#object-genflag_boss_stacy) | Object  | Configures the miniboss and boss encounter events for the Stacy Mutant boss on the map. | 2 | `{ . . . }` |
| [`repeat`](../Reference_and_Meta/Enums.md#enum-repeat) | Enum | Determines how many times an event, song, or unlock can be triggered. Accepts a positive integer or the string "infinite". | 1 | `1`<br>`2`<br>`20` |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 1 | `false`<br>`true` |
| [`bumblefoot`](../Reference_and_Meta/Enums.md#enum-bumblefoot) | Enum | Specifies the Bumblefoot miniboss encounter. | 1 | `auto` |
| [`queenhippo`](../Reference_and_Meta/Enums.md#enum-queenhippo) | Enum | Specifies the boss configuration for QueenHippo. Setting to "auto" generates it procedurally, or an inline object can define custom subfolder and cutscene. | 1 | `auto` |
| [`gambit`](../Reference_and_Meta/Enums.md#enum-gambit) | Enum | Determines which Gambit boss encounter occurs. | 1 | `auto` |
| [`radicalrat`](../Reference_and_Meta/Enums.md#enum-radicalrat) | Enum | Specifies the Radical Rat boss encounter. | 1 | `auto` |
| [`spewer`](../Reference_and_Meta/Enums.md#enum-spewer) | Enum | Specifies the Spewer boss encounter. | 1 | `auto` |
| [`drmangler`](../Reference_and_Meta/Enums.md#enum-drmangler) | Enum | Specifies the Dr. Mangler miniboss encounter. | 1 | `auto` |
| [`infestedduo`](../Reference_and_Meta/Enums.md#enum-infestedduo) | Enum | Specifies the Infested Duo miniboss encounter. | 1 | `auto` |
| [`ratking`](../Reference_and_Meta/Enums.md#enum-ratking) | Enum | Specifies the Rat King miniboss encounter. | 1 | `auto` |
| [`CoreObeliskUnlocked`](./Map_Generation_and_Routing.md#object-coreobeliskunlocked) | Object  | Configures the map event and art when the Core Obelisk is raised and unlocked. | 1 | `{ . . . }` |
| [`MoonObeliskUnlocked`](./Map_Generation_and_Routing.md#object-moonobeliskunlocked) | Object  | Configures the map event and art when the Moon Obelisk is raised and unlocked. | 1 | `{ . . . }` |
| [`butchercat`](../Reference_and_Meta/Enums.md#enum-butchercat) | Enum | Specifies the miniboss configuration for ButcherCat, typically set to "auto". | 1 | `auto` |
| [`fightercat`](../Reference_and_Meta/Enums.md#enum-fightercat) | Enum | Specifies the miniboss configuration for FighterCat, typically set to "auto". | 1 | `auto` |
| [`magecat`](../Reference_and_Meta/Enums.md#enum-magecat) | Enum | Specifies the miniboss configuration for MageCat, typically set to "auto". | 1 | `auto` |
| [`monkcat`](../Reference_and_Meta/Enums.md#enum-monkcat) | Enum | Specifies the miniboss configuration for MonkCat, typically set to "auto". | 1 | `auto` |
| [`necrocat`](../Reference_and_Meta/Enums.md#enum-necrocat) | Enum | Specifies the miniboss configuration for NecroCat, typically set to "auto". | 1 | `auto` |
| [`thiefcat`](../Reference_and_Meta/Enums.md#enum-thiefcat) | Enum | Specifies the miniboss configuration for ThiefCat, typically set to "auto". | 1 | `auto` |
| [`tinkerercat`](../Reference_and_Meta/Enums.md#enum-tinkerercat) | Enum | Specifies the miniboss configuration for TinkerCat, typically set to "auto". | 1 | `auto` |
| [`flushmaster`](../Reference_and_Meta/Enums.md#enum-flushmaster) | Enum | Specifies the Flushmaster miniboss encounter. | 1 | `auto` |
| [`zodiac`](../Reference_and_Meta/Enums.md#enum-zodiac) | Enum | Specifies the Zodiac boss encounter. | 1 | `auto` |
| [`abandonedones`](../Reference_and_Meta/Enums.md#enum-abandonedones) | Enum | Specifies the Abandoned Ones miniboss encounter. | 1 | `auto` |
| [`cancreeper`](../Reference_and_Meta/Enums.md#enum-cancreeper) | Enum | Specifies the Cancreeper miniboss encounter. | 1 | `auto` |
| [`cerberubs`](../Reference_and_Meta/Enums.md#enum-cerberubs) | Enum | Specifies the Cerberubs miniboss encounter. | 1 | `auto` |
| [`clericcat`](../Reference_and_Meta/Enums.md#enum-clericcat) | Enum | Specifies the Cleric Cat miniboss encounter. | 1 | `auto` |
| [`druidcat`](../Reference_and_Meta/Enums.md#enum-druidcat) | Enum | Specifies the Druid Cat miniboss encounter. | 1 | `auto` |
| [`huntercat`](../Reference_and_Meta/Enums.md#enum-huntercat) | Enum | Specifies the Hunter Cat miniboss encounter. | 1 | `auto` |
| [`lenny`](../Reference_and_Meta/Enums.md#enum-lenny) | Enum | Specifies the Lenny miniboss encounter. | 1 | `auto` |
| [`mamamaggot`](../Reference_and_Meta/Enums.md#enum-mamamaggot) | Enum | Specifies the Mama Maggot miniboss encounter. | 1 | `auto` |
| [`rockybobo`](../Reference_and_Meta/Enums.md#enum-rockybobo) | Enum | Specifies the Rocky Bobo miniboss encounter. | 1 | `auto` |
| [`slime`](../Reference_and_Meta/Enums.md#enum-slime) | Enum | Specifies the Slime miniboss encounter. | 1 | `auto` |
| [`stacy`](../Reference_and_Meta/Enums.md#enum-stacy) | Enum | Specifies the Stacy boss encounter. | 1 | `auto` |
| [`tankcat`](../Reference_and_Meta/Enums.md#enum-tankcat) | Enum | Specifies the Tank Cat miniboss encounter. | 1 | `auto` |
| [`trampy`](../Reference_and_Meta/Enums.md#enum-trampy) | Enum | Specifies the Trampy miniboss encounter. | 1 | `auto` |
| [`psychiccat`](../Reference_and_Meta/Enums.md#enum-psychiccat) | Enum | Specifies the miniboss configuration for PsychicCat, typically set to "auto". | 1 | `auto` |
| [`BoneyardUnlocked`](./Map_Generation_and_Routing.md#object-boneyardunlocked) | Object  | Unlocks an exit route to the Boneyard on the map. | 1 | `{ . . . }` |
| [`BunkerUnlocked`](./Map_Generation_and_Routing.md#object-bunkerunlocked) | Object  | Unlocks an exit route to the Bunker on the map. | 1 | `{ . . . }` |
| [`cavecatfamily`](../Reference_and_Meta/Enums.md#enum-cavecatfamily) | Enum | Specifies the Cave Cat Family miniboss encounter. | 1 | `auto` |
| [`CavesUnlocked`](./Map_Generation_and_Routing.md#object-cavesunlocked) | Object  | Unlocks an exit route to the Caves on the map. | 1 | `{ . . . }` |
| [`CoreUnlocked`](./Map_Generation_and_Routing.md#object-coreunlocked) | Object  | Unlocks an exit route to the Core on the map. | 1 | `{ . . . }` |
| [`CraterUnlocked`](./Map_Generation_and_Routing.md#object-craterunlocked) | Object  | Unlocks an exit route to the Crater on the map. | 1 | `{ . . . }` |
| [`dinocouple`](../Reference_and_Meta/Enums.md#enum-dinocouple) | Enum | Specifies the Dino Couple miniboss encounter. | 1 | `auto` |
| [`FutureUnlocked`](./Map_Generation_and_Routing.md#object-futureunlocked) | Object  | Configures the map event and art when the Future is unlocked. | 1 | `{ . . . }` |
| [`IceAgeUnlocked`](./Map_Generation_and_Routing.md#object-iceageunlocked) | Object  | Configures the map event and art when Ice Age is unlocked. | 1 | `{ . . . }` |
| [`iceelemental`](../Reference_and_Meta/Enums.md#enum-iceelemental) | Enum | Specifies the Ice Elemental miniboss encounter. | 1 | `auto` |
| [`JunkyardUnlocked`](./Map_Generation_and_Routing.md#object-junkyardunlocked) | Object  | Unlocks an exit route to the Junkyard on the map. | 1 | `{ . . . }` |
| [`JurassicUnlocked`](./Map_Generation_and_Routing.md#object-jurassicunlocked) | Object  | Unlocks an exit route to the Jurassic area on the map. | 1 | `{ . . . }` |
| [`lightningelemental`](../Reference_and_Meta/Enums.md#enum-lightningelemental) | Enum | Specifies the Lightning Elemental miniboss encounter. | 1 | `auto` |
| [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull) | Object  | Unlocks hidden battle and hard nodes within the MeatWorld area on the map. | 1 | `{ . . . }` |
| [`miniboss_event`](./Map_Generation_and_Routing.md#object-miniboss_event) | Object  | An object defining the properties of a mini-boss event at this node. | 1 | `{ . . . }` |
| [`MoonUnlocked`](./Map_Generation_and_Routing.md#object-moonunlocked) | Object  | Unlocks an exit route to the Moon on the map. | 1 | `{ . . . }` |
| [`musiclayer`](../Reference_and_Meta/Enums.md#enum-musiclayer) | Enum | Specifies the music layer to play for this node (e.g., 'boss'). | 1 | `boss` |
| [`mw_battle1`](./Map_Generation_and_Routing.md#object-mw_battle1) | Object  | An object defining the properties of the first MeatWorld battle node. | 1 | `{ . . . }` |
| [`mw_boss`](./Map_Generation_and_Routing.md#object-mw_boss) | Object  | An object defining the properties of the MeatWorld boss node. | 1 | `{ . . . }` |
| [`mw_earlyhome`](./Map_Generation_and_Routing.md#object-mw_earlyhome) | Object  | An object defining the properties of the MeatWorld early home node. | 1 | `{ . . . }` |
| [`mw_event1`](./Map_Generation_and_Routing.md#object-mw_event1) | Object  | An object defining the properties of the first MeatWorld event node. | 1 | `{ . . . }` |
| [`mw_hard1`](./Map_Generation_and_Routing.md#object-mw_hard1) | Object  | An object defining the properties of the first MeatWorld hard path node. | 1 | `{ . . . }` |
| [`mw_home`](./Map_Generation_and_Routing.md#object-mw_home) | Object  | An object defining the properties of the MeatWorld home node. | 1 | `{ . . . }` |
| [`mw_quest_event`](./Map_Generation_and_Routing.md#object-mw_quest_event) | Object  | An object defining the properties of the MeatWorld quest event node. | 1 | `{ . . . }` |
| [`mw_treasure`](./Map_Generation_and_Routing.md#object-mw_treasure) | Object  | An object defining the properties of the MeatWorld treasure node. | 1 | `{ . . . }` |
| [`SewersUnlocked`](./Map_Generation_and_Routing.md#object-sewersunlocked) | Object  | Unlocks an exit route to the Sewers on the map. | 1 | `{ . . . }` |
| [`thebloat`](../Reference_and_Meta/Enums.md#enum-thebloat) | Enum | Specifies The Bloat miniboss encounter. | 1 | `auto` |
| [`TheEndUnlocked`](./Map_Generation_and_Routing.md#object-theendunlocked) | Object  | An object that stores flags related to unlocking the 'The End' chapter. | 1 | `{ . . . }` |
| `advance` | Number | The number of levels the nemesis advances when triggered. | 1 | `1` |
| [`ChaosAntennaAttached`](./Map_Generation_and_Routing.md#object-chaosantennaattached) | Object  | Configures the map event and art when the Chaos Antenna has been attached. | 1 | `{ . . . }` |
| [`exit_desert`](./Map_Generation_and_Routing.md#object-exit_desert) | Object | Defines the exit node properties for the desert map, including type, next map, lock state, and art. | 1 | `{ . . . }` |
| [`exit_lab`](./Map_Generation_and_Routing.md#object-exit_lab) | Object | Defines the exit node properties for the lab map, including type, next map, lock state, and art. | 1 | `{ . . . }` |
| `head_start` | Number | The initial number of turns the nemesis has before the player can act. | 1 | `99` |
| [`mw_altar`](./Map_Generation_and_Routing.md#object-mw_altar) | Object | A map node that represents a Meat World special event altar with custom art. | 1 | `{ . . . }` |
| [`shop_cheapwater`](./Map_Generation_and_Routing.md#object-shop_cheapwater) | Object | Node definition for a cheap water shop, specifying its type, level, and override art. | 1 | `{ . . . }` |
| [`shop_water`](./Map_Generation_and_Routing.md#object-shop_water) | Object | Node definition for a water shop, specifying its type, level, and override art. | 1 | `{ . . . }` |
| [`spawn_node`](../Reference_and_Meta/Enums.md#enum-spawn_node) | Enum | The name of the node where the nemesis first spawns on the map. | 1 | `start` |
| [`ThrobbingArteryDone`](./Map_Generation_and_Routing.md#object-throbbingarterydone) | Object  | An object that stores flags related to completing the Throbbing Artery quest. | 1 | `{ . . . }` |
| [`WallOfFleshDone`](./Map_Generation_and_Routing.md#object-walloffleshdone) | Object  | An object that stores flags related to completing the Wall of Flesh quest. | 1 | `{ . . . }` |
| [`weather_event`](./Map_Generation_and_Routing.md#object-weather_event) | Object | Defines a special event that triggers a crater weather level. | 1 | `{ . . . }` |
| [`choose_one`](../Reference_and_Meta/Arrays.md#array-choose_one) | Array | A list of generation flags from which exactly one is randomly selected. | 1 | `[GenFlag_Boss_Stacy, GenFlag_Boss_Spewer]` |
| :--- | :--- | :--- | 0 | :--- |

</details>


---


### Object: `boss`


**Definition:** An object defining the properties of a boss encounter, such as rewards or level.  
**Total Count:** 213

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`GenFlag_Boss_Spewer`](./Map_Generation_and_Routing.md#object-genflag_boss_spewer), [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#object-genflag_boss_stacy), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 19 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`boss_cutscene`](../Reference_and_Meta/Enums.md#enum-boss_cutscene) | Enum | Specifies which boss cutscene to play before this encounter. | 16 | `alienqueen`<br>`coven`<br>`dybbuk` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 2 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_music`](../Reference_and_Meta/Enums.md#enum-override_music) | Enum | Specifies an alternative music track to play during this boss encounter. | 2 | `chaos_boss`<br>`finalboss`<br>`throbbingking` |
| `is_final_boss` | Boolean | If true, this encounter is the final boss of the chapter. | 2 | `true` |
| [`tileset`](../Reference_and_Meta/Enums.md#enum-tileset) | Enum | Specifies the tileset to use for this boss arena. | 1 | `finalboss` |
| [`unlockcheck_on_complete`](../Reference_and_Meta/Enums.md#enum-unlockcheck_on_complete) | Enum | The unlock check that is performed upon completing this boss encounter. | 1 | `map_unlock_junkyard` |

</details>


---


### Object: `jurassic`


**Definition:** Specifies the name, map flag, or connection for the Jurassic area.  
**Total Count:** 56

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | If true, cats on this node will rotate to face their movement direction. | 1 | `true` |

</details>


---


### Object: `theend`


**Definition:** Specifies the name, map flag, or connection for The End area.  
**Total Count:** 51

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | If true, cats on this node will rotate to face their movement direction. | 1 | `true` |

</details>


---


### Object: `treasure`


**Definition:** Defines a treasure node containing items or item pools.  
**Total Count:** 45

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |

</details>


---


### Object: `moon`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 45

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `meatworld`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 45

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `endoftime`


**Definition:** Configures various attributes of the End of Time area, depending on context.  
**Total Count:** 45

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | If true, cats on this node will rotate to face their movement direction. | 1 | `true` |

</details>


---


### Object: `dimensionx`


**Definition:** An enum specifying the Dimension X chapter area, or an object with its specific properties.  
**Total Count:** 45

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | If true, cats on this node will rotate to face their movement direction. | 1 | `true` |

</details>


---


### Object: `core`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 45

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `boneyard`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 45

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `caves`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 42

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `battle`


**Definition:** Defines a battle encounter by preset, level file path, or reverb settings.  
**Total Count:** 36

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `iceage`


**Definition:** Specifies the name, map flag, or connection for the Ice Age area.  
**Total Count:** 32

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | If true, cats on this node will rotate to face their movement direction. | 1 | `true` |

</details>


---


### Object: `future`


**Definition:** Specifies the name, map flag, or connection for the Future area.  
**Total Count:** 30

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `spin_cats` | Boolean | If true, cats on this node will rotate to face their movement direction. | 1 | `true` |

</details>


---


### Object: `exit0`


**Definition:** An object defining the properties of the first exit from this node.  
**Total Count:** 27

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoneyardUnlocked`](./Map_Generation_and_Routing.md#object-boneyardunlocked), [`BunkerUnlocked`](./Map_Generation_and_Routing.md#object-bunkerunlocked), [`CavesUnlocked`](./Map_Generation_and_Routing.md#object-cavesunlocked), [`CoreUnlocked`](./Map_Generation_and_Routing.md#object-coreunlocked), [`EndOfTimeUnlocked`](./Map_Generation_and_Routing.md#object-endoftimeunlocked), [`JurassicUnlocked`](./Map_Generation_and_Routing.md#object-jurassicunlocked), [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#object-meatworldunlocked), [`MoonUnlocked`](./Map_Generation_and_Routing.md#object-moonunlocked), [`ROOT`](./Map_Generation_and_Routing.md#object-root), [`SewersUnlocked`](./Map_Generation_and_Routing.md#object-sewersunlocked), [`TheEndUnlocked`](./Map_Generation_and_Routing.md#object-theendunlocked)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 17 | `false`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 15 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 15 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`next_map`](../Reference_and_Meta/Enums.md#enum-next_map) | Enum | Specifies which map file to load when this exit is used. | 15 | `bunker.gon`<br>`core.gon`<br>`crater.gon` |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 10 | `false`<br>`true` |

</details>


---


### Object: `alley`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 25

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `quest_event`


**Definition:** An object defining the properties of a quest-related event at this node, such as its level and art.  
**Total Count:** 24

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BothObelisksUnlocked`](./Map_Generation_and_Routing.md#object-bothobelisksunlocked), [`ChaosAntennaAttached`](./Map_Generation_and_Routing.md#object-chaosantennaattached), [`CoreObeliskUnlocked`](./Map_Generation_and_Routing.md#object-coreobeliskunlocked), [`DimensionXUnlocked`](./Map_Generation_and_Routing.md#object-dimensionxunlocked), [`FutureUnlocked`](./Map_Generation_and_Routing.md#object-futureunlocked), [`IceAgeUnlocked`](./Map_Generation_and_Routing.md#object-iceageunlocked), [`MeatWorldUnlocked`](./Map_Generation_and_Routing.md#object-meatworldunlocked), [`MoonObeliskUnlocked`](./Map_Generation_and_Routing.md#object-moonobeliskunlocked), [`ROOT`](./Map_Generation_and_Routing.md#object-root), [`ThrobbingArteryDone`](./Map_Generation_and_Routing.md#object-throbbingarterydone), [`VolcanoAntennaAttached`](./Map_Generation_and_Routing.md#object-volcanoantennaattached), [`WallOfFleshDone`](./Map_Generation_and_Routing.md#object-walloffleshdone)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 24 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 19 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 11 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `desert`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 23

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `bunker`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 21

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `sewers`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>
### Object: `lab`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `home`


**Definition:** Specifies the option to go home (exit to the main hub).  
**Total Count:** 20

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `crater`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `junkyard`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 18

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


### Object: `event`


**Definition:** Specifies the event to force, either by name or by a nested object defining its type and level.  
**Total Count:** 15

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |

</details>


---


### Object: `start`


**Definition:** Specifies the initial animation state played at the beginning of an ability.  
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `time_machine`


**Definition:** Defines a special event node that leads to a time machine quest level.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 4 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 4 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 4 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |

</details>


---


### Object: `exit1`


**Definition:** An object defining the properties of the second exit from this node.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CraterUnlocked`](./Map_Generation_and_Routing.md#object-craterunlocked), [`JunkyardUnlocked`](./Map_Generation_and_Routing.md#object-junkyardunlocked), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 5 | `false`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 3 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 3 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| [`next_map`](../Reference_and_Meta/Enums.md#enum-next_map) | Enum | Specifies which map file to load when this exit is used. | 3 | `bunker.gon`<br>`core.gon`<br>`crater.gon` |

</details>


---


### Object: `hard_initial`


**Definition:** An object defining the properties of the initial hard path node.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`HardPathUnlocked`](./Map_Generation_and_Routing.md#object-hardpathunlocked), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 4 | `false`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `BothObelisksUnlocked`


**Definition:** Configures the map event and art when both obelisks have been unlocked.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


---


### Object: `MoonObeliskUnlocked`


**Definition:** Configures the map event and art when the Moon Obelisk is raised and unlocked.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `MeatWorldUnlocked`


**Definition:** Configures the map event and routes when MeatWorld is initially unlocked.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 2 | `{ . . . }` |
| [`quest_event`](./Map_Generation_and_Routing.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


---


### Object: `HardPathUnlocked`


**Definition:** Unlocks the hard difficulty path on the map, usually by setting a node's locked state to false.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`hard_initial`](./Map_Generation_and_Routing.md#object-hard_initial) | Object  | An object defining the properties of the initial hard path node. | 2 | `{ . . . }` |

</details>


---


### Object: `EndOfTimeUnlocked`


**Definition:** Configures the map event and route visibility when End of Time is unlocked.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 2 | `{ . . . }` |

</details>


---


### Object: `DimensionXUnlocked`


**Definition:** Configures the map event and art when Dimension X is unlocked.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


---


### Object: `CoreObeliskUnlocked`


**Definition:** Configures the map event and art when the Core Obelisk is raised and unlocked.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `VolcanoAntennaAttached`


**Definition:** Configures the map event and art when the Volcano Antenna has been attached.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 2 | `{ . . . }` |

</details>


---


### Object: `TheEndUnlocked`


**Definition:** An object that stores flags related to unlocking the 'The End' chapter.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `SewersUnlocked`


**Definition:** Unlocks an exit route to the Sewers on the map.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `mw_treasure`


**Definition:** An object defining the properties of the MeatWorld treasure node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_quest_event`


**Definition:** An object defining the properties of the MeatWorld quest event node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |

</details>


---


### Object: `mw_home`


**Definition:** An object defining the properties of the MeatWorld home node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_hard1`


**Definition:** An object defining the properties of the first MeatWorld hard path node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`musiclayer`](../Reference_and_Meta/Enums.md#enum-musiclayer) | Enum | Specifies the music layer to play for this node (e.g., 'boss'). | 1 | `boss` |

</details>


---


### Object: `mw_event1`


**Definition:** An object defining the properties of the first MeatWorld event node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `mw_earlyhome`


**Definition:** An object defining the properties of the MeatWorld early home node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 1 | `false`<br>`true` |

</details>


---


### Object: `mw_boss`


**Definition:** An object defining the properties of the MeatWorld boss node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`boss_cutscene`](../Reference_and_Meta/Enums.md#enum-boss_cutscene) | Enum | Specifies which boss cutscene to play before this encounter. | 1 | `alienqueen`<br>`coven`<br>`dybbuk` |
| [`override_music`](../Reference_and_Meta/Enums.md#enum-override_music) | Enum | Specifies an alternative music track to play during this boss encounter. | 1 | `chaos_boss`<br>`finalboss`<br>`throbbingking` |

</details>


---


### Object: `mw_battle1`


**Definition:** An object defining the properties of the first MeatWorld battle node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeatWorldUnlockedFull`](./Map_Generation_and_Routing.md#object-meatworldunlockedfull), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 2 | `false`<br>`true` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `MoonUnlocked`


**Definition:** Unlocks an exit route to the Moon on the map.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `miniboss_event`


**Definition:** An object defining the properties of a mini-boss event at this node.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`GenFlag_Boss_Stacy`](./Map_Generation_and_Routing.md#object-genflag_boss_stacy), [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |

</details>


---


### Object: `MeatWorldUnlockedFull`


**Definition:** Unlocks hidden battle and hard nodes within the MeatWorld area on the map.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mw_battle1`](./Map_Generation_and_Routing.md#object-mw_battle1) | Object  | An object defining the properties of the first MeatWorld battle node. | 1 | `{ . . . }` |
| [`mw_boss`](./Map_Generation_and_Routing.md#object-mw_boss) | Object  | An object defining the properties of the MeatWorld boss node. | 1 | `{ . . . }` |
| [`mw_earlyhome`](./Map_Generation_and_Routing.md#object-mw_earlyhome) | Object  | An object defining the properties of the MeatWorld early home node. | 1 | `{ . . . }` |
| [`mw_event1`](./Map_Generation_and_Routing.md#object-mw_event1) | Object  | An object defining the properties of the first MeatWorld event node. | 1 | `{ . . . }` |
| [`mw_hard1`](./Map_Generation_and_Routing.md#object-mw_hard1) | Object  | An object defining the properties of the first MeatWorld hard path node. | 1 | `{ . . . }` |
| [`mw_home`](./Map_Generation_and_Routing.md#object-mw_home) | Object  | An object defining the properties of the MeatWorld home node. | 1 | `{ . . . }` |
| [`mw_quest_event`](./Map_Generation_and_Routing.md#object-mw_quest_event) | Object  | An object defining the properties of the MeatWorld quest event node. | 1 | `{ . . . }` |
| [`mw_treasure`](./Map_Generation_and_Routing.md#object-mw_treasure) | Object  | An object defining the properties of the MeatWorld treasure node. | 1 | `{ . . . }` |

</details>


---


### Object: `JurassicUnlocked`


**Definition:** Unlocks an exit route to the Jurassic area on the map.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `JunkyardUnlocked`


**Definition:** Unlocks an exit route to the Junkyard on the map.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit1`](./Map_Generation_and_Routing.md#object-exit1) | Object  | An object defining the properties of the second exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `IceAgeUnlocked`


**Definition:** Configures the map event and art when Ice Age is unlocked.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `GenFlag_Boss_Stacy`


**Definition:** Configures the miniboss and boss encounter events for the Stacy Mutant boss on the map.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`boss`](./Map_Generation_and_Routing.md#object-boss) | Object  | An object defining the properties of a boss encounter, such as rewards or level. | 1 | `{ . . . }` |
| [`miniboss_event`](./Map_Generation_and_Routing.md#object-miniboss_event) | Object  | An object defining the properties of a mini-boss event at this node. | 1 | `{ . . . }` |

</details>


---


### Object: `GenFlag_Boss_Spewer`


**Definition:** Configures the boss encounter event for the Spewer boss on the map.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`boss`](./Map_Generation_and_Routing.md#object-boss) | Object  | An object defining the properties of a boss encounter, such as rewards or level. | 1 | `{ . . . }` |

</details>


---


### Object: `FutureUnlocked`


**Definition:** Configures the map event and art when the Future is unlocked.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `CraterUnlocked`


**Definition:** Unlocks an exit route to the Crater on the map.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit1`](./Map_Generation_and_Routing.md#object-exit1) | Object  | An object defining the properties of the second exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `CoreUnlocked`


**Definition:** Unlocks an exit route to the Core on the map.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `CavesUnlocked`


**Definition:** Unlocks an exit route to the Caves on the map.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `BunkerUnlocked`


**Definition:** Unlocks an exit route to the Bunker on the map.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `BoneyardUnlocked`


**Definition:** Unlocks an exit route to the Boneyard on the map.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit0`](./Map_Generation_and_Routing.md#object-exit0) | Object  | An object defining the properties of the first exit from this node. | 1 | `{ . . . }` |

</details>


---


### Object: `weather_event`


**Definition:** Defines a special event that triggers a crater weather level.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |

</details>


---


---


## Auto-Discovered Objects


### Object: `WallOfFleshDone`


**Definition:** An object that stores flags related to completing the Wall of Flesh quest.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `ThrobbingArteryDone`


**Definition:** An object that stores flags related to completing the Throbbing Artery quest.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---


### Object: `shop_water`


**Definition:** Node definition for a water shop, specifying its type, level, and override art.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |

</details>


---


### Object: `shop_cheapwater`


**Definition:** Node definition for a cheap water shop, specifying its type, level, and override art.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |

</details>


---


### Object: `mw_altar`


**Definition:** A map node that represents a Meat World special event altar with custom art.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`level`](../Reference_and_Meta/Enums.md#enum-level) | Enum | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |

</details>


---


### Object: `exit_lab`


**Definition:** Defines the exit node properties for the lab map, including type, next map, lock state, and art.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 1 | `false`<br>`true` |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 1 | `false`<br>`true` |
| [`next_map`](../Reference_and_Meta/Enums.md#enum-next_map) | Enum | Specifies which map file to load when this exit is used. | 1 | `bunker.gon`<br>`core.gon`<br>`crater.gon` |

</details>


---


### Object: `exit_desert`


**Definition:** Defines the exit node properties for the desert map, including type, next map, lock state, and art.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`override_art`](../Reference_and_Meta/Enums.md#enum-override_art) | Enum | Specifies the visual art key used to override the default node appearance on the map. | 1 | `MapNodeExit_Bunker`<br>`MapNodeExit_Core`<br>`MapNodeExit_Crater` |
| `hidden` | Boolean | If true, this exit is not shown on the map until it is discovered. | 1 | `false`<br>`true` |
| `locked` | Boolean | If true, this exit is locked and cannot be used until unlocked by a condition. | 1 | `false`<br>`true` |
| [`next_map`](../Reference_and_Meta/Enums.md#enum-next_map) | Enum | Specifies which map file to load when this exit is used. | 1 | `bunker.gon`<br>`core.gon`<br>`crater.gon` |

</details>


---


### Object: `ChaosAntennaAttached`


**Definition:** Configures the map event and art when the Chaos Antenna has been attached.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Map_Generation_and_Routing.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`quest_event`](./Map_Generation_and_Routing.md#object-quest_event) | Object  | An object defining the properties of a quest-related event at this node, such as its level and art. | 1 | `{ . . . }` |

</details>


---

