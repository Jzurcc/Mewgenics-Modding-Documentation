# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Events & Encounters

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_OPEN_ANSW", "EVENT_LEAVE_ANSW", "EVENT_PICK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex, none, lck` |  |
| `requirements` | [`Block`](./Events_and_Encounters.md#context-requirements) | `{ ... }` | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_twentyfive, choice_dex_alt, choice_leave` |  |
| `prompt` | String | `"EVENT_TRASHBIN_REW3", "EVENT_ABEGGAR_REW2", "EVENT_BEGGAR_NOTENOUGHMONEY"` |  |
| `set_frame` | Number | `2, 5, 4` |  |
| `copy_results` | [`Enum/String`](./Enums.md#enum-copy_results) | `smash, examine` |  |
| `good` | [`Block`](./Events_and_Encounters.md#context-good) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Good' action. |
| `get_item_from_pool` | [`Enum/String`](./Enums.md#enum-get_item_from_pool) | `food, chapter_rare` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `bad` | [`Block`](./Events_and_Encounters.md#context-bad) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `reward` | [`Block`](./Events_and_Encounters.md#context-reward) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Reward' action. |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `stat_max` | Number | `10, 25, 15` |  |
| `stat_min` | Number | `10, 25, 15` |  |
| `weight` | [`Enum/String`](./Enums.md#enum-weight) | `.5, .25, 15` | Probability weight for this outcome. |
| `cha` | Number | `1` |  |
| `con` | Number | `1` |  |
| `int` | Number | `1` |  |
| `lck` | Number | `1` |  |
| `spd` | Number | `1` |  |
| `str` | Number | `1` |  |
| `add_weather` | [`Enum/String`](./Enums.md#enum-add_weather) | `SolarFlare` |  |
| `dex` | Number | `1` |  |
| `gain_familiar` | [`Enum/String`](./Enums.md#enum-gain_familiar) | `Toad` | Event Action: Adds a specific familiar to the party. |
| `next_event_bonus` | Number | `2` |  |
| `requires_flag` | [`Enum/String`](./Enums.md#enum-requires_flag) | `SolarFlareUnlocked` | Prerequisite: Must meet this condition. |
| `self_status_next_fight` | [`Block`](./Events_and_Encounters.md#context-self_status_next_fight) | `{ ... }` | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |

</details>

---

### Context: `rare`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`attack`](./Events_and_Encounters.md#context-attack), [`good`](./Events_and_Encounters.md#context-good), [`loot`](./Events_and_Encounters.md#context-loot), [`main`](./Events_and_Encounters.md#context-main), [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prompt` | String | `"EVENT_CLOSEDWINDOW_REW2", "EVENT_CLOSEDWINDOW_REW6", "EVENT_CLOSEDWINDOW_REW4"` |  |
| `set_frame` | Number | `4, 6, 3` |  |
| `get_item_from_pool` | [`Block`](./Events_and_Encounters.md#context-get_item_from_pool) | `{ ... }, treasure_easy, bone_equipment` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `gain_disorder` | [`Enum/String`](./Enums.md#enum-gain_disorder) | `Dyslexia, BorrowedTime, Brave` |  |
| `gain_disorder_from_pool` | [`Enum/String`](./Enums.md#enum-gain_disorder_from_pool) | `diseases, all_disorders, physical_disorders` |  |
| `injury` | [`Enum/String`](./Enums.md#enum-injury) | `radiated, str, cursed` |  |
| `get_item` | [`Enum/String`](./Enums.md#enum-get_item) | `MomsKnife, BigToe, MomsToeNail` |  |
| `random_mutation` | [`Block`](./Events_and_Encounters.md#context-random_mutation) | `{ ... }, 2, 1` | Event Reward: Applies a completely random mutation to a character. |
| `event_now_same_cat` | [`Enum/String`](./Enums.md#enum-event_now_same_cat) | `BigToe, CatHole, SpookieApparation` |  |
| `get_parasite` | [`Enum/String`](./Enums.md#enum-get_parasite) | `FaceShards, BigToeCursed, MetalRod` |  |
| `gain_familiar` | [`Enum/String`](./Enums.md#enum-gain_familiar) | `CharmedLeaper, CharmedFetus2, CharmedHeadTumor` | Event Action: Adds a specific familiar to the party. |
| `random_pool` | [`Array`](./Arrays.md#array-random_pool) | `[ { event_now_same_cat Crate } { event_now_same_cat Safe ..., [ { permanent_stats { str -1 } } { permanent_stats { dex ..., [ { party_heal 100% gain_food [ 10 25 ]` |  |
| `get_parasite_from_pool` | [`Enum/String`](./Enums.md#enum-get_parasite_from_pool) | `sludge_armor, parasites, good_parasites` |  |
| `set_adventure_token` | [`Enum/String`](./Enums.md#enum-set_adventure_token) | `AdventureToken_TrippedOnBigToe, MysteriousStranger_HasLostFinger, HasPlayedMysteriousStranger` |  |
| `damage` | Number | `6, 10, 99%` | Event Node: Story branch or dialog option representing the 'Damage' action. |
| `gain_coins` | [`Array`](./Arrays.md#array-gain_coins) | `[ 20 100 ], [ 10 15 ], [ 10 30 ]` |  |
| `next_event_bonus` | Number | `-2, 1, -1` |  |
| `self_damage` | Number | `50%, 1, 99%` | Recoil or self-inflicted damage/effects applied to the caster. |
| `play_animation` | [`Array`](./Arrays.md#array-play_animation) | `resultHole, [ resultLeave 0 ]` |  |
| `learn_passive` | [`Enum/String`](./Enums.md#enum-learn_passive) | `DeathProof, PoisonTips, CobraStyle` |  |
| `party_damage` | [`Array`](./Arrays.md#array-party_damage) | `[ 5 10 ], 2, 5` |  |
| `party_heal` | Number | `6, 100%, 5` |  |
| `battle` | [`Equation`](./Enums.md#enum-mathequation) | `"events/chupacabra.lvl", "events/bigtoe.lvl", "events/crackinthewall.lvl"` |  |
| `increment_legacy_counter` | [`Enum/String`](./Enums.md#enum-increment_legacy_counter) | `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_ToiletFlushes, WorldEventLegacyCounter_CrackInTheWall` |  |
| `override_end_option_prompt` | String | `"EVENT_MYSTERIOUSSTRANGER_END_AGAIN2", "EVENT_LOCKEDDOOR_PROMPT2", "EVENT_MYSTERIOUSTENT_PROMPT"` |  |
| `party_random_mutation` | Number | `1` |  |
| `ambush_next_basic_fights` | Number | `1` |  |
| `lose_item` | [`Enum/String`](./Enums.md#enum-lose_item) | `inventory, equipped` |  |
| `set_legacy_token` | [`Enum/String`](./Enums.md#enum-set_legacy_token) | `WorldEventLegacyToken_HeadInTireCompleted, WorldEventLegacyToken_MomsKnife, WorldEventLegacyToken_MonkeyPaw1` |  |
| `gain_food` | [`Array`](./Arrays.md#array-gain_food) | `[ 2 5 ], [ 1 5 ], [ 8 10 ]` |  |
| `hide_appearance_changes` | Number | `1` |  |
| `shop_now` | [`Enum/String`](./Enums.md#enum-shop_now) | `Event_SmallShop, Event_RareShop, TreasureHard` |  |
| `ally_ambush_next_fights` | Number | `2, 1` |  |
| `decrement_legacy_counter` | [`Enum/String`](./Enums.md#enum-decrement_legacy_counter) | `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall` |  |
| `add_weather` | [`Enum/String`](./Enums.md#enum-add_weather) | `HauntedNight, RestlessDead` |  |
| `full_heal` | Number | `1` |  |
| `learn_ability` | [`Enum/String`](./Enums.md#enum-learn_ability) | `FutureSight, BarfBall` |  |
| `gain_cat_familiar` | Number | `1` |  |
| `kill` | [`Enum/String`](./Enums.md#enum-kill) | `cat` |  |
| `level_up` | [`Enum/String`](./Enums.md#enum-level_up) | `self` |  |
| `lose_item_from_inventory` | [`Enum/String`](./Enums.md#enum-lose_item_from_inventory) | `cat` |  |
| `make_old` | [`Enum/String`](./Enums.md#enum-make_old) | `self` |  |
| `next_event_from_set` | [`Block`](./Events_and_Encounters.md#context-next_event_from_set) | `{ ... }, WatchingHead2` | Event Action: Chains immediately into a randomly selected subsequent story event. |
| `spawn_reflection_next_fight` | Block | `{ ... }, 1` | Event Penalty: Spawns dark clones/reflections of the party in the next combat encounter. |
| `event_now` | [`Enum/String`](./Enums.md#enum-event_now) | `MysteriousMachine_Good, MysteriousMachine_Bad` |  |
| `lose_specific_item` | [`Enum/String`](./Enums.md#enum-lose_specific_item) | `SlagTight` |  |
| `party_heal_disorder` | Number | `2` |  |
| `party_heal_injury` | Number | `99` |  |
| `set_age` | Number | `1` |  |
| `upgrade_ability` | [`Enum/String`](./Enums.md#enum-upgrade_ability) | `random` |  |
| `upgrade_passive` | [`Enum/String`](./Enums.md#enum-upgrade_passive) | `random` |  |
| `ambush` | [`Equation`](./Enums.md#enum-mathequation) | `"events/chupacabra.lvl"` |  |
| `clear_result_animation` | Number | `1` |  |
| `gain_immortal_familiar` | [`Enum/String`](./Enums.md#enum-gain_immortal_familiar) | `CharmedFleaSpecial` |  |
| `get_and_equip_item` | [`Enum/String`](./Enums.md#enum-get_and_equip_item) | `FlyLarva` |  |
| `heal_disorder` | Number | `2` |  |
| `learn_ability_from_pool` | [`Enum/String`](./Enums.md#enum-learn_ability_from_pool) | `Necromancer` |  |
| `learn_passive_from_pool` | [`Enum/String`](./Enums.md#enum-learn_passive_from_pool) | `AnyUnlocked` |  |
| `lose_all_equipped_items` | [`Enum/String`](./Enums.md#enum-lose_all_equipped_items) | `cat` |  |
| `party_injury` | [`Enum/String`](./Enums.md#enum-party_injury) | `random` |  |
| `play_result_animation` | [`Enum/String`](./Enums.md#enum-play_result_animation) | `resultVeryGood` |  |
| `scramble_abilities` | [`Enum/String`](./Enums.md#enum-scramble_abilities) | `all` |  |
| `scramble_basic_attack` | [`Enum/String`](./Enums.md#enum-scramble_basic_attack) | `all` |  |
| `trigger_adventure_unlock` | [`Enum/String`](./Enums.md#enum-trigger_adventure_unlock) | `legacy_event_unlock_momsknife` |  |

</details>

---

### Context: `common`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prompt` | String | `"EVENT_CLOSEDWINDOW_REW5", "EVENT_CLOSEDWINDOW_REW1", "EVENT_CLOSEDWINDOW_REW3"` |  |
| `set_frame` | Number | `2, 5, 3` |  |
| `get_item_from_pool` | [`Enum/String`](./Enums.md#enum-get_item_from_pool) | `consumables, { ... }, [ CarvingKnife RazorBlade ButterflyKnife ]` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `random_pool` | [`Array`](./Arrays.md#array-random_pool) | `[ { prompt "EVENT_KNIFEINTHEWALL_REW1" } { prompt "EVENT_..., [ { permanent_stats { str -1 } } { permanent_stats { dex ..., [ { party_heal 5 gain_food [ 2 4 ]` |  |
| `damage` | [`Array`](./Arrays.md#array-damage) | `[ 5 10 ], 5, [ 3 6 ]` | Event Node: Story branch or dialog option representing the 'Damage' action. |
| `gain_coins` | [`Array`](./Arrays.md#array-gain_coins) | `[ 5 15 ], 5, [ 4 8 ]` |  |
| `injury` | [`Enum/String`](./Enums.md#enum-injury) | `spd, radiated, str` |  |
| `self_damage` | Number | `50%, 1, 99%` | Recoil or self-inflicted damage/effects applied to the caster. |
| `random_mutation` | [`Block`](./Events_and_Encounters.md#context-random_mutation) | `{ ... }, 2, 1` | Event Reward: Applies a completely random mutation to a character. |
| `clear_adventure_token` | [`Enum/String`](./Enums.md#enum-clear_adventure_token) | `AdventureToken_RedNeedle, AdventureToken_HasTakenNeedle, AdventureToken_BlueNeedle` |  |
| `gain_disorder_from_pool` | [`Enum/String`](./Enums.md#enum-gain_disorder_from_pool) | `mental_disorders, all_disorders, physical_disorders` |  |
| `play_animation` | [`Enum/String`](./Enums.md#enum-play_animation) | `resultLeave, resultConfused, [ resultLeave 0 ]` |  |
| `event_now_same_cat` | [`Enum/String`](./Enums.md#enum-event_now_same_cat) | `UnmarkedGrave, ElephantsFootCloser, random` |  |
| `gain_food` | Number | `-5, [ 1 4 ], [ 5 10 ]` |  |
| `gain_familiar` | [`Enum/String`](./Enums.md#enum-gain_familiar) | `CharmedFetus, CharmedPinky, Snake` | Event Action: Adds a specific familiar to the party. |
| `party_damage` | [`Array`](./Arrays.md#array-party_damage) | `[ 1 6 ], 5, 3` |  |
| `party_heal` | Number | `1, 100%, 3` |  |
| `get_item` | [`Enum/String`](./Enums.md#enum-get_item) | `EnchantingPoop, SeedBombs, CatnipBig` |  |
| `heal` | Number | `10, 1, 3` |  |
| `gain_disorder` | [`Enum/String`](./Enums.md#enum-gain_disorder) | `IntestinalProlapse, Scatological, Stinky` |  |
| `get_parasite_from_pool` | [`Enum/String`](./Enums.md#enum-get_parasite_from_pool) | `parasites, [ AmoebaHat AmoebaNeck AmoebaFace ], [ CrimsonMask_Cursed RedCap_Cursed PoundOfFlesh_Cursed ]` |  |
| `override_end_option_prompt` | String | `"EVENT_MYSTERIOUSTENT_PROMPT", "EVENT_MYSTERIOUSSTRANGER_END_AGAIN", "EVENT_LOCKEDDOOR_PROMPT1"` |  |
| `ally_ambush_next_fights` | Number | `2, 1` |  |
| `full_heal` | Number | `1` |  |
| `ambush_next_basic_fights` | Number | `1` |  |
| `set_adventure_token` | [`Enum/String`](./Enums.md#enum-set_adventure_token) | `MysteriousStranger_HasLostFinger, AdventureToken_UnmarkedGraveForced, HasPlayedMysteriousStranger` |  |
| `get_parasite` | [`Enum/String`](./Enums.md#enum-get_parasite) | `CursedHairball, PawShards, EnchantingPoop_Cursed` |  |
| `next_event_bonus` | Number | `2, 1, -1` |  |
| `increment_legacy_counter` | [`Enum/String`](./Enums.md#enum-increment_legacy_counter) | `WorldEventLegacyToken_StartDigging, WorldEventLegacyCounter_CrackInTheWall, WorldEventLegacyCounter_VolcanoSacrifices` |  |
| `kill` | [`Enum/String`](./Enums.md#enum-kill) | `cat` |  |
| `lose_item` | [`Enum/String`](./Enums.md#enum-lose_item) | `inventory, weapon, equipped` |  |
| `shop_now` | [`Enum/String`](./Enums.md#enum-shop_now) | `Event_SmallShop, TreasureEasy` |  |
| `add_weather` | [`Enum/String`](./Enums.md#enum-add_weather) | `RestlessDead, Sandstorm` |  |
| `event_now` | [`Enum/String`](./Enums.md#enum-event_now) | `random` |  |
| `lose_specific_item` | [`Enum/String`](./Enums.md#enum-lose_specific_item) | `SlagTight` |  |
| `party_heal_disorder` | Number | `2` |  |
| `spin` | [`Enum/String`](./Enums.md#enum-spin) | `again` |  |
| `clear_result_animation` | Number | `1` |  |
| `decrement_legacy_counter` | [`Enum/String`](./Enums.md#enum-decrement_legacy_counter) | `WorldEventLegacyCounter_CrackInTheWall` |  |
| `get_and_equip_item` | [`Enum/String`](./Enums.md#enum-get_and_equip_item) | `Catnip` |  |
| `heal_disorder` | Number | `1` |  |
| `heal_injury` | Number | `1` |  |
| `learn_ability_from_pool` | [`Enum/String`](./Enums.md#enum-learn_ability_from_pool) | `AnyUnlocked` |  |
| `self_heal` | Number | `10` |  |
| `set_legacy_token` | [`Enum/String`](./Enums.md#enum-set_legacy_token) | `WorldEventLegacyToken_HasRunFromDeath` |  |
| `upgrade_ability` | [`Enum/String`](./Enums.md#enum-upgrade_ability) | `random` |  |

</details>

---

### Context: `good`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `reward` | [`Block`](./Events_and_Encounters.md#context-reward) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Reward' action. |
| `set_frame` | Number | `4, 2, 3` |  |
| `prompt` | String | `"EVENT_CLOSEDWINDOW_REW8", "EVENT_TRASHBIN_REW1", "EVENT_SEALEDCRYPT_LEAVE"` |  |
| `play_animation` | [`Enum/String`](./Enums.md#enum-play_animation) | `resultHole, resultVeryGood, [ resultLeave 0 ]` |  |
| `increment_legacy_counter` | [`Enum/String`](./Enums.md#enum-increment_legacy_counter) | `WorldEventLegacyCounter_TestLegacyFoo, WorldEventLegacyCounter_SealedCrypt, WorldEventLegacyCounter_Jack` |  |
| `conditional_reward` | [`Block`](./Events_and_Encounters.md#context-conditional_reward) | `{ ... }` | Event Action: Provides a reward only if a specific condition is met. |
| `set_legacy_token` | [`Enum/String`](./Enums.md#enum-set_legacy_token) | `WorldEventLegacyToken_StacyMutant, mapflag_ThrobbingArteryDone, MeatWorldQuest_Leech` |  |
| `cutscene` | [`Block`](./Events_and_Encounters.md#context-cutscene) | `{ ... }, "chapterintros/bunker"` | Event Node: Triggers a narrative cutscene. |
| `begin_chapter` | [`Enum/String`](./Enums.md#enum-begin_chapter) | `iceage.gon, future.gon, dimensionx.gon` |  |
| `complete_item_quest` | [`Enum/String`](./Enums.md#enum-complete_item_quest) | `PutridLeech, GuillotinasHead, ThrobbingGristle` |  |
| `random_mutation` | Number | `10, 1, 5` | Event Reward: Applies a completely random mutation to a character. |
| `set_adventure_token` | [`Enum/String`](./Enums.md#enum-set_adventure_token) | `StacyMutant_Thorns, StacyMutant_Holy, StacyMutant_Brace` |  |
| `event_now` | [`Enum/String`](./Enums.md#enum-event_now) | `StacyMutant3, StacyMutant4, StacyMutant2` |  |
| `event_now_same_cat` | [`Enum/String`](./Enums.md#enum-event_now_same_cat) | `MysteriousTomb1, BodyOfGlorg_Gift, random` |  |
| `gain_disorder` | [`Enum/String`](./Enums.md#enum-gain_disorder) | `Gargantuan, Anxiety, Depression` |  |
| `lose_specific_item` | [`Enum/String`](./Enums.md#enum-lose_specific_item) | `PutridLeech, PyrophinasCollar, ThrobbingGristle` |  |
| `trigger_adventure_unlock` | [`Enum/String`](./Enums.md#enum-trigger_adventure_unlock) | `legacy_event_unlock_momsknife, time_machine_quest_finalstep, meat_world_open` |  |
| `add_weather` | [`Enum/String`](./Enums.md#enum-add_weather) | `MeteorShower, SolarFlare, GeomagneticStorm` |  |
| `random_pool` | [`Array`](./Arrays.md#array-random_pool) | `[ { prompt "EVENT_TRAVERSETHENECROPOLIS_REW1" play_animat..., [ { weight 90 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran..., [ { weight 95 prompt "EVENT_ABEGGAR_REW1" set_frame 3 ran...` |  |
| `get_item` | [`Enum/String`](./Enums.md#enum-get_item) | `MomsKnife, HumanBrain, CryogenicTimeChamber_Full` |  |
| `get_item_from_pool` | [`Enum/String`](./Enums.md#enum-get_item_from_pool) | `godly_items, glitched_items, bloody_items` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `heal_disorder` | [`Enum/String`](./Enums.md#enum-heal_disorder) | `mental_disorders, 1, Anxiety` |  |
| `injury` | [`Enum/String`](./Enums.md#enum-injury) | `random` |  |
| `level_up` | [`Enum/String`](./Enums.md#enum-level_up) | `self, all` |  |
| `mutation` | [`Block`](./Events_and_Encounters.md#context-mutation) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Mutation' action. |
| `random_pool_consider_luck` | [`Array`](./Arrays.md#array-random_pool_consider_luck) | `[ { prompt "EVENT_VENDINGMACHINE_REW4" set_frame 5 gain_d..., [ { prompt "EVENT_TRACY_REW11" weight 1 get_item_from_poo..., [ { prompt "EVENT_TRACY_REW1" weight 1 get_parasite_from_...` |  |
| `rare` | [`Block`](./Events_and_Encounters.md#context-rare) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rare' action. |
| `get_parasite` | [`Enum/String`](./Enums.md#enum-get_parasite) | `Beepis, Cunch, Feebis` |  |
| `heal_injury` | Number | `1, 5` |  |
| `kill` | [`Enum/String`](./Enums.md#enum-kill) | `cat` |  |
| `transform_item` | [`Array`](./Arrays.md#array-transform_item) | `[ JarOfRadiation JarOfRadiatedBlood ], [ JarOfRadiatedBlood JarOfChaos ], [ CryogenicTimeChamber_Empty CryogenicTimeChamber_Full ]` |  |
| `unlock_item_quest` | [`Enum/String`](./Enums.md#enum-unlock_item_quest) | `JarOfRadiatedBlood, JarOfChaos, CryogenicTimeChamber_Full` |  |
| `clear_surviving_kaiju` | [`Enum/String`](./Enums.md#enum-clear_surviving_kaiju) | `zaratana, pyrophina` |  |
| `cutscene_on_exit` | [`Enum/String`](./Enums.md#enum-cutscene_on_exit) | `king_intro` |  |
| `full_heal` | Number | `1` |  |
| `gain_disorder_from_pool` | [`Enum/String`](./Enums.md#enum-gain_disorder_from_pool) | `all_disorders` |  |
| `learn_ability_from_pool` | [`Enum/String`](./Enums.md#enum-learn_ability_from_pool) | `Necromancer, [ Smack Meow Hiss ]` |  |
| `learn_passive_from_pool` | [`Enum/String`](./Enums.md#enum-learn_passive_from_pool) | `Necromancer, [ MiniMe SkillShare ]` |  |
| `override_end_option_prompt` | String | `"EVENT_MYSTERIOUSTOMB_END", "EVENT_MYSTERIOUSTOMB1_END"` |  |
| `party_gain_disorder_from_pool` | [`Array`](./Arrays.md#array-party_gain_disorder_from_pool) | `[ Gigantism ], [ Dwarfism ]` |  |
| `ally_ambush_next_fights` | Number | `1` |  |
| `clone_self_to_party` | Number | `1` |  |
| `copy_items_to_party` | Number | `1` |  |
| `copy_party_items` | Number | `1` |  |
| `gain_food` | [`Array`](./Arrays.md#array-gain_food) | `[ 10 20 ]` |  |
| `get_full_item_set_from_pool` | [`Enum/String`](./Enums.md#enum-get_full_item_set_from_pool) | `common` |  |
| `global_effect_next_fight` | [`Block`](./Events_and_Encounters.md#context-global_effect_next_fight) | `{ ... }` | Event Penalty/Reward: Applies a global Map Modifier (e.g., LowerAmbientLight, Rain) during the next combat encounter. |
| `heal` | Number | `50%` |  |
| `lose_item` | [`Enum/String`](./Enums.md#enum-lose_item) | `parasite` |  |
| `next_event_bonus` | Number | `1` |  |
| `next_event_from_set` | [`Block`](./Events_and_Encounters.md#context-next_event_from_set) | `{ ... }` | Event Action: Chains immediately into a randomly selected subsequent story event. |
| `scramble_abilities` | [`Enum/String`](./Enums.md#enum-scramble_abilities) | `all` |  |
| `scramble_passives` | [`Enum/String`](./Enums.md#enum-scramble_passives) | `all` |  |
| `shop_now` | [`Enum/String`](./Enums.md#enum-shop_now) | `Event_SmallShop` |  |
| `trigger_butterfly_effect` | Number | `1` |  |
| `upgrade_ability` | [`Enum/String`](./Enums.md#enum-upgrade_ability) | `random` |  |
| `upgrade_passive` | [`Enum/String`](./Enums.md#enum-upgrade_passive) | `random` |  |

</details>

---

### Context: `intro`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cat_choice` | [`Enum/String`](./Enums.md#enum-cat_choice) | `random` |  |
| `event_clip` | [`Enum/String`](./Enums.md#enum-event_clip) | `NonWheelEvent` |  |
| `subject_clip` | [`Enum/String`](./Enums.md#enum-subject_clip) | `EventSubject` |  |
| `subject_frame` | [`Enum/String`](./Enums.md#enum-subject_frame) | `trashcan, brokenwindow, mouse_nest` |  |
| `title` | String | `"EVENT_MOUSENEST_NAME", "EVENT_TRASHBIN_NAME", "EVENT_CLOSEDWINDOW_NAME"` |  |
| `choose_cat_with_item` | [`Enum/String`](./Enums.md#enum-choose_cat_with_item) | `PutridLeech, GuillotinasHead, ThrobbingGristle` |  |
| `different_from_last_x_cats` | Number | `2, 1, 3` |  |
| `subject_frame_inner` | Number | `2, 4` |  |
| `choose_cat_with_highest_stat` | [`Enum/String`](./Enums.md#enum-choose_cat_with_highest_stat) | `int` |  |
| `choose_cat_with_item_slot_equipped` | [`Enum/String`](./Enums.md#enum-choose_cat_with_item_slot_equipped) | `weapon` |  |
| `choose_cat_with_min_health` | Number | `75%` |  |
| `choose_cat_with_most_injuries` | Boolean | `true` |  |
| `choose_cat_with_parasite` | Boolean | `true` |  |
| `set_frame` | Number | `1` |  |

</details>

---

### Context: `bad`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`main`](./Events_and_Encounters.md#context-main), [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `reward` | [`Block`](./Events_and_Encounters.md#context-reward) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Reward' action. |
| `set_frame` | Number | `2, 3, 4` |  |
| `prompt` | String | `"QEVENT_STACYMUTANT1_REW4_B", "EVENT_CLOSEDWINDOW_REW7", "QEVENT_STACYMUTANT1_REW4"` |  |
| `play_animation` | [`Enum/String`](./Enums.md#enum-play_animation) | `resultHole, resultVeryBad, [ resultLeave 0 ]` |  |
| `injury` | [`Enum/String`](./Enums.md#enum-injury) | `dex, str, con` |  |
| `battle` | [`Equation`](./Enums.md#enum-mathequation) | `"events/Death.lvl"` |  |
| `gain_disorder_from_pool` | [`Enum/String`](./Enums.md#enum-gain_disorder_from_pool) | `diseases, all_disorders` |  |
| `kill` | [`Enum/String`](./Enums.md#enum-kill) | `cat` |  |
| `cutscene` | [`Block`](./Events_and_Encounters.md#context-cutscene) | `{ ... }` | Event Node: Triggers a narrative cutscene. |
| `event_now` | [`Enum/String`](./Enums.md#enum-event_now) | `StacyMutant3, StacyMutant4, StacyMutant2` |  |
| `event_now_same_cat` | [`Enum/String`](./Enums.md#enum-event_now_same_cat) | `StevenFetus, random` |  |
| `get_parasite_from_pool` | [`Enum/String`](./Enums.md#enum-get_parasite_from_pool) | `parasites` |  |
| `next_event_bonus` | Number | `-1` |  |
| `gain_immortal_familiar` | [`Enum/String`](./Enums.md#enum-gain_immortal_familiar) | `CharmedFlea` |  |
| `get_parasite` | [`Enum/String`](./Enums.md#enum-get_parasite) | `CursedRock` |  |
| `lose_item` | [`Enum/String`](./Enums.md#enum-lose_item) | `parasite` |  |
| `select_item_from_pool_for_cutscene_only` | [`Enum/String`](./Enums.md#enum-select_item_from_pool_for_cutscene_only) | `glitched_items` |  |
| `set_legacy_token` | [`Enum/String`](./Enums.md#enum-set_legacy_token) | `WorldEventLegacyToken_StacyMutant` |  |

</details>

---

### Context: `requirements`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `has_token` | [`Enum/String`](./Enums.md#enum-has_token) | `WorldEventLegacyToken_StacyMutant, AdventureToken_TrippedOnBigToe, HasPlayedMysteriousStranger` |  |
| `counter_range` | [`Array`](./Arrays.md#array-counter_range) | `[ WorldEventLegacyCounter_SealedCrypt 1 1 ], [ WorldEventLegacyCounter_SealedCrypt 2 2 ], [ WorldEventLegacyCounter_SealedCrypt 0 0 ]` |  |
| `not_has_token` | [`Enum/String`](./Enums.md#enum-not_has_token) | `AdventureToken_UnmarkedGraveForced, WorldEventLegacyToken_MomsKnife, WorldEventLegacyToken_CryptOpened` |  |
| `counter_minimum` | [`Array`](./Arrays.md#array-counter_minimum) | `[ WorldEventLegacyCounter_CrackInTheWall 4 ], [ WorldEventLegacyCounter_TestLegacyFoo 3 ], [ WorldEventLegacyToken_StartDigging 4 ]` |  |
| `cat_has_item_equipped` | [`Enum/String`](./Enums.md#enum-cat_has_item_equipped) | `PutridLeech, GuillotinasHead, ThrobbingGristle` |  |
| `counter_maximum` | [`Array`](./Arrays.md#array-counter_maximum) | `[ WorldEventLegacyCounter_SealedCrypt 4 ], [ WorldEventLegacyCounter_CrackInTheWall 0 ], [ WorldEventLegacyCounter_CrackInTheWall 3 ]` |  |
| `is_not_chapter` | [`Array`](./Arrays.md#array-is_not_chapter) | `[ future theend ], [ jurassic iceage ], [ iceage jurassic ]` |  |
| `is_chapter` | [`Array`](./Arrays.md#array-is_chapter) | `[ future theend ], [ future ], [ theend ]` |  |
| `minimum_party_size` | Number | `2` |  |
| `not_cat_has_item_equipped` | [`Enum/String`](./Enums.md#enum-not_cat_has_item_equipped) | `GuillotinasHead, CryogenicTimeChamber_Full` |  |
| `not_on_quest` | Number | `1` |  |
| `cat_has_injury_count_min` | Number | `2` |  |
| `cat_has_item_slot_equipped` | [`Enum/String`](./Enums.md#enum-cat_has_item_slot_equipped) | `weapon` |  |
| `cat_has_parasite` | Boolean | `true` |  |

</details>

---

### Context: `main`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prompt` | String | `"EVENT_MOUSENEST_QUES", "EVENT_CLOSEDWINDOW_QUES", "EVENT_TRASHBIN_QUES"` |  |
| `bad` | [`Block`](./Events_and_Encounters.md#context-bad) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `goto` | [`Enum/String`](./Enums.md#enum-goto) | `end` |  |
| `max_options` | Number | `2, 3` |  |
| `set_frame` | Number | `16, 3, 15` |  |
| `shuffle_options` | Boolean | `true` |  |
| `weight` | [`Enum/String`](./Enums.md#enum-weight) | `.5, .25` | Probability weight for this outcome. |
| `add_weather` | [`Enum/String`](./Enums.md#enum-add_weather) | `MeteorShower` |  |
| `gain_familiar` | [`Enum/String`](./Enums.md#enum-gain_familiar) | `Snake` | Event Action: Adds a specific familiar to the party. |
| `leave` | [`Block`](./Events_and_Encounters.md#context-leave) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Leave' action. |
| `next_event_from_set` | [`Enum/String`](./Enums.md#enum-next_event_from_set) | `Tragedy` | Event Action: Chains immediately into a randomly selected subsequent story event. |
| `party_heal` | Number | `3` |  |
| `party_permanent_stats` | [`Block`](./Events_and_Encounters.md#context-party_permanent_stats) | `{ ... }` | Event Reward: Permanently increases (or decreases) the core stats of all party members. |
| `play_animation` | [`Array`](./Arrays.md#array-play_animation) | `resultVeryGood` |  |
| `rare` | [`Block`](./Events_and_Encounters.md#context-rare) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rare' action. |
| `requires_flag` | [`Enum/String`](./Enums.md#enum-requires_flag) | `MeteorShowerUnlocked` | Prerequisite: Must meet this condition. |
| `self_damage` | [`Array`](./Arrays.md#array-self_damage) | `[ 4 8 ]` | Recoil or self-inflicted damage/effects applied to the caster. |
| `self_status_next_fight` | [`Block`](./Events_and_Encounters.md#context-self_status_next_fight) | `{ ... }` | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. |
| `shop_now` | [`Enum/String`](./Enums.md#enum-shop_now) | `Event_RareShop` |  |

</details>

---

### Context: `reward`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`bad`](./Events_and_Encounters.md#context-bad), [`good`](./Events_and_Encounters.md#context-good)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prompt` | String | `"EVENT_SEALEDCRYPT_QUES2", "EVENT_SEALEDCRYPT_QUES1", "EVENT_TRASHBIN_REW2"` |  |
| `set_frame` | Number | `2, 1, 3` |  |
| `clear_adventure_token` | [`Enum/String`](./Enums.md#enum-clear_adventure_token) | `AdventureToken_RedNeedle, AdventureToken_HasTakenNeedle, AdventureToken_BlueNeedle` |  |
| `get_item_from_pool` | [`Block`](./Events_and_Encounters.md#context-get_item_from_pool) | `{ ... }, consumables, food` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `set_adventure_token` | [`Enum/String`](./Enums.md#enum-set_adventure_token) | `AdventureToken_StevenTryAgain3, AdventureToken_Mirage2, HasPlayedMysteriousStranger` |  |
| `set_subject` | [`Enum/String`](./Enums.md#enum-set_subject) | `throbbing_artery_noflesh, wall_of_flesh_noartery, dimensionx_head2` |  |
| `random_pool` | [`Array`](./Arrays.md#array-random_pool) | `[ { weight 10 gain_disorder_from_pool diseases } { weight..., [ { get_item_from_pool rare get_item_from_pool rare } { g..., [ { get_item_from_pool uncommon get_item_from_pool uncomm...` |  |
| `next_event_bonus` | Number | `-2, 1, -1` |  |
| `trigger_adventure_unlock` | [`Enum/String`](./Enums.md#enum-trigger_adventure_unlock) | `meat_world_unlock, end_of_time_unlock` |  |
| `play_animation` | [`Array`](./Arrays.md#array-play_animation) | `resultVeryGood, resultBad` |  |
| `cutscene_on_exit` | [`Enum/String`](./Enums.md#enum-cutscene_on_exit) | `infinite_intro` |  |
| `gain_disorder_from_pool` | [`Enum/String`](./Enums.md#enum-gain_disorder_from_pool) | `diseases, Steven_disorders` |  |
| `injury` | [`Enum/String`](./Enums.md#enum-injury) | `con, random` |  |
| `spawn_unit_next_fight` | [`Block`](./Events_and_Encounters.md#context-spawn_unit_next_fight) | `{ ... }` | Event Penalty/Reward: Injects a specific entity (friendly or hostile) into the next combat encounter. |
| `event_now` | [`Enum/String`](./Enums.md#enum-event_now) | `MeatGolem` |  |
| `gain_coins` | [`Array`](./Arrays.md#array-gain_coins) | `[ 4 15 ]` |  |
| `get_item` | [`Enum/String`](./Enums.md#enum-get_item) | `BrokenWindow` |  |
| `get_parasite_from_pool` | [`Enum/String`](./Enums.md#enum-get_parasite_from_pool) | `parasites` |  |
| `party_damage` | [`Array`](./Arrays.md#array-party_damage) | `[ 5 10 ]` |  |
| `set_legacy_token` | [`Enum/String`](./Enums.md#enum-set_legacy_token) | `WorldEventLegacyToken_CryptOpened` |  |
| `weight` | Number | `3` | Probability weight for this outcome. |

</details>

---

### Context: `ignore`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_IGNORE_ANSW, "EVENT_LEAVE_ANSW", "EVENT_IGNORE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con, none` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_leave` |  |
| `hint_chapter_exit` | [`Enum/String`](./Enums.md#enum-hint_chapter_exit) | `home` |  |

</details>

---

### Context: `self_status_next_fight`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`main`](./Events_and_Encounters.md#context-main)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Fear` | Number | `2, 1, 5` | Applies or references the 'Fear' effect/state. |
| `Poison` | Number | `10, 2, 3` | Applies or references the 'Poison' effect/state. |
| `Bleed` | Number | `2, 1, 3` | Applies or references the 'Bleed' effect/state. |
| `AbilityOnBattleStart_Immediate` | [`Enum/String`](./Enums.md#enum-abilityonbattlestart_immediate) | `SummonBrambles2, FlowerEventSleep, BrambleRandomTileEvent` | Applies or references the 'AbilityOnBattleStart_Immediate' effect/state. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |
| `SpeedUp` | Number | `2, -4, -2` | Applies or references the 'SpeedUp' effect/state. |
| `StrengthUp` | Number | `-2, 2, -1` | Applies or references the 'StrengthUp' effect/state. |
| `ConstitutionUp` | Number | `1, -1` | Applies or references the 'ConstitutionUp' effect/state. |
| `AddStartingMana` | Number | `5` | Applies or references the 'AddStartingMana' effect/state. |
| `Burn` | Number | `6, 5, 4` | Applies or references the 'Burn' effect/state. |
| `CharismaUp` | Number | `2, -2, -1` | Applies or references the 'CharismaUp' effect/state. |
| `Confusion` | Number | `2, 4` | Applies or references the 'Confusion' effect/state. |
| `HealthRegenUp` | Number | `2, 1` | Applies or references the 'HealthRegenUp' effect/state. |
| `Webbed` | Number | `2, 1` | Applies or references the 'Webbed' effect/state. |
| `Blind` | Number | `6, 4` | Applies or references the 'Blind' effect/state. |
| `Bruise` | Number | `1` | Applies or references the 'Bruise' effect/state. |
| `DexterityUp` | Number | `2, -1` | Applies or references the 'DexterityUp' effect/state. |
| `IntelligenceUp` | Number | `3, -3` | Applies or references the 'IntelligenceUp' effect/state. |
| `NoHealthRegen` | Number | `1` | Applies or references the 'NoHealthRegen' effect/state. |
| `Sleep` | Number | `2, 1` | Applies or references the 'Sleep' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `AbilityOnBattleStart` | [`Enum/String`](./Enums.md#enum-abilityonbattlestart) | `Flush` | Applies or references the 'AbilityOnBattleStart' effect/state. |
| `AddInitiative` | Number | `-99` | Applies or references the 'AddInitiative' effect/state. |
| `AlphaTurns` | Number | `1` | Applies or references the 'AlphaTurns' effect/state. |
| `ChangeTileUnderCharacterAtStart` | [`Enum/String`](./Enums.md#enum-changetileundercharacteratstart) | `GlassTile` | Applies or references the 'ChangeTileUnderCharacterAtStart' effect/state. |
| `DivineShield` | Number | `2` | Applies or references the 'DivineShield' effect/state. |
| `Fights` | Number | `99` | Applies or references the 'Fights' effect/state. |
| `LuckUp` | Number | `1` | Applies or references the 'LuckUp' effect/state. |
| `Madness` | Number | `1` | Applies the Madness debuff/status effect. |
| `MissChance` | Number | `10` | Applies or references the 'MissChance' effect/state. |
| `NoManaRegen` | Number | `1` | Applies or references the 'NoManaRegen' effect/state. |
| `PermanentConfusion` | Number | `1` | Applies or references the 'PermanentConfusion' effect/state. |
| `ProbeCharmed` | Number | `1` | Applies or references the 'ProbeCharmed' effect/state. |
| `RandomStatUp` | Number | `1` | Applies or references the 'RandomStatUp' effect/state. |
| `Rot` | Number | `2` | Applies or references the 'Rot' effect/state. |
| `Slow` | Number | `3` | Applies or references the 'Slow' effect/state. |
| `SpiderInfested` | Number | `1` | Applies or references the 'SpiderInfested' effect/state. |
| `Tarred` | Number | `1` | Applies or references the 'Tarred' effect/state. |
| `TempStrengthUp` | Number | `1` | Applies or references the 'TempStrengthUp' effect/state. |

</details>

---

### Context: `permanent_stats`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `2, 1, -1` |  |
| `random` | Number | `2, 1, -1` |  |
| `int` | Number | `-4, 1, -1` |  |
| `lck` | Number | `-2, 1, -1` |  |
| `spd` | Number | `-2, 1, -1` |  |
| `str` | Number | `2, 1, -1` |  |
| `cha` | [`Enum/String`](./Enums.md#enum-cha) | `+1, 1, -1` |  |
| `dex` | Number | `2, 1, -1` |  |

</details>

---

### Context: `spawn_unit_next_fight`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`reward`](./Events_and_Encounters.md#context-reward)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `RandomNonCoinPickup, DeadPinky, [ Junk Junk TrashBag ]` |  |
| `count` | Number | `8, 3, [ 3 6 ]` | Quantity. |
| `spawn_side` | [`Enum/String`](./Enums.md#enum-spawn_side) | `anywhere, cats, enemies` |  |
| `side` | [`Enum/String`](./Enums.md#enum-side) | `enemies` |  |

</details>

---

### Context: `examine`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_EXAMINE_ANSW", EVENT_EXAMINE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int, lck` |  |
| `copy_results` | [`Enum/String`](./Enums.md#enum-copy_results) | `smash, open` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `gain_coins` | [`Array`](./Arrays.md#array-gain_coins) | `[ 5 15 ]` |  |

</details>

---

### Context: `leave`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LEAVE_ANSW", "EVENT_WALKAWAY_ANSW", "EVENT_IGNORE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd, lck, none` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_leave` |  |

</details>

---

### Context: `mutation`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `eyes` | Number | `900, -2, 702` |  |
| `mouth` | Number | `900, -2, 705` |  |
| `ears` | Number | `310, -2, 328` |  |
| `eyebrows` | Number | `900, 440, -2` |  |
| `head` | Number | `900, 305` | Event Node: Story branch or dialog option representing the 'Head' action. |
| `legs` | Number | `900, 322` |  |
| `arms` | Number | `900` |  |
| `body` | Number | `900` | Event Node: Story branch or dialog option representing the 'Body' action. |
| `tail` | Number | `900` | Event Node: Story branch or dialog option representing the 'Tail' action. |
| `eye1` | Number | `-2, -1` |  |
| `arm1` | Number | `-2` |  |
| `ear1` | Number | `-2` |  |
| `eyebrow1` | Number | `-2` |  |
| `leg1` | Number | `-2` |  |
| `eye2` | Number | `-1` |  |

</details>

---

### Context: `loot`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_dex_alt, choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_LOOT_ANSW, QEVENT_DEADKING_LOOTCORPSE_ANSW, "EVENT_LOOT_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex, lck` |  |
| `rare` | [`Block`](./Events_and_Encounters.md#context-rare) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rare' action. |

</details>

---

### Context: `get_item_from_pool`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `pool` | [`Enum/String`](./Enums.md#enum-pool) | `chapter_common, chapter, chapter_rare` |  |
| `restrict` | [`Array`](./Arrays.md#array-restrict) | `consumables, [ weapon, trinket, armor ], trinket` |  |
| `prompt` | String | `"EVENT_FRANK2_REW4"` |  |

</details>

---

### Context: `random_mutation_from_set`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `mouth` | Number | `1500, 1026, -1` |  |
| `count` | Number | `1, 3` | Quantity. |
| `tail` | Number | `1500, 760, -1` | Event Node: Story branch or dialog option representing the 'Tail' action. |
| `ears` | Number | `1500, -2, -1` |  |
| `eyes` | Number | `-1, -2, 1029` |  |
| `legs` | Number | `306, -1` |  |
| `body` | Number | `758, -1` | Event Node: Story branch or dialog option representing the 'Body' action. |
| `eyebrows` | Number | `-2, -1` |  |
| `head` | Number | `759, -1` | Event Node: Story branch or dialog option representing the 'Head' action. |
| `arm1` | Number | `-2, -1` |  |
| `arm2` | Number | `-2, -1` |  |
| `leg1` | Number | `-1` |  |
| `leg2` | Number | `-1` |  |
| `texture` | Number | `-1` |  |

</details>

---

### Context: `else`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prompt` | String | `"EVENT_MIRAGE_REW4", "QEVENT_STACYMUTANT1_QUES1", "EVENT_MIRAGE_REW3"` |  |
| `event_now_same_cat` | [`Enum/String`](./Enums.md#enum-event_now_same_cat) | `Needles` |  |
| `set_adventure_token` | [`Enum/String`](./Enums.md#enum-set_adventure_token) | `AdventureToken_Mirage1` |  |
| `party_damage` | [`Array`](./Arrays.md#array-party_damage) | `[ 10 15 ], 1, 5` |  |
| `set_frame` | Number | `4, 3` |  |
| `event_now` | [`Enum/String`](./Enums.md#enum-event_now) | `Mirage` |  |
| `random_pool` | [`Array`](./Arrays.md#array-random_pool) | `[ { get_item FrozenHat get_item FrozenMask get_item Froze..., [ { get_item Catnip } { gain_food [ 2 5 ]` |  |
| `gain_disorder` | [`Enum/String`](./Enums.md#enum-gain_disorder) | `Soulless, AcidReflux` |  |
| `get_item_from_pool` | [`Array`](./Arrays.md#array-get_item_from_pool) | `[ LeafyMask LeafyHat LeafyNecklace DinoHat DinoMask DinoN...` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `damage` | Number | `50%` | Event Node: Story branch or dialog option representing the 'Damage' action. |
| `next_event_bonus` | Number | `1` |  |
| `set_legacy_token` | [`Enum/String`](./Enums.md#enum-set_legacy_token) | `WorldEventLegacyToken_HasRunFromDeath` |  |

</details>

---

### Context: `eat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_EAT_ANSW", "EVENT_DRINK_ANSW", EVENT_EAT_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `cutscene`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`good`](./Events_and_Encounters.md#context-good)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cutscene` | String | `"time_machine", "desert_intro", "chaos_ending_good"` | Event Node: Triggers a narrative cutscene. |
| `skip_result_screen` | Boolean | `true` |  |

</details>

---

### Context: `random_mutation`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Number | `2, 1, 15` | Quantity. |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `melted, animal, birth_defect` | Specific entity tag required. |
| `asymmetric` | Boolean | `false, true` |  |

</details>

---

### Context: `smash`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_SMASH_ANSW", "EVENT_MYSTERIOUSTOMB_ANSW", "EVENT_GOLEMSMASH_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex, str, none` |  |
| `copy_results` | [`Enum/String`](./Enums.md#enum-copy_results) | `open` |  |

</details>

---

### Context: `destroy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DESTROY_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `party_permanent_stats_exclude_self`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `cha` | Number | `2, 1` |  |
| `con` | Number | `2, 1` |  |
| `dex` | Number | `2, 1` |  |
| `int` | Number | `2, 1` |  |
| `lck` | Number | `2, 1` |  |
| `spd` | Number | `2, 1` |  |
| `str` | Number | `2, 1` |  |

</details>

---

### Context: `bash`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BASH_ANSW", "EVENT_BASHOPEN_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `party_status_next_fight`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `Poison` | Number | `2, 1, 3` | Applies or references the 'Poison' effect/state. |
| `AbilityOnBattleStart_Immediate` | [`Enum/String`](./Enums.md#enum-abilityonbattlestart_immediate) | `RocksFallEvent, SummonBrambles2, GrassEvent` | Applies or references the 'AbilityOnBattleStart_Immediate' effect/state. |
| `NoHealthRegen` | Number | `1` | Applies or references the 'NoHealthRegen' effect/state. |
| `Bleed` | Number | `3` | Applies or references the 'Bleed' effect/state. |
| `DivineShield` | Number | `1` | Applies or references the 'DivineShield' effect/state. |
| `HealthRegenUp` | Number | `2` | Applies or references the 'HealthRegenUp' effect/state. |
| `Immobile` | Number | `1` | Applies or references the 'Immobile' effect/state. |
| `Tangled` | Number | `2` | Applies a tangled/ensnared status effect, often modifying visual sprites. |
| `Tarred` | Number | `1` | Applies or references the 'Tarred' effect/state. |
| `Webbed` | Number | `1` | Applies or references the 'Webbed' effect/state. |

</details>

---

### Context: `sneak`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_SNEAKBY_ANSW, EVENT_RUN_ANSW, "EVENT_SNEAKBY_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd, dex` |  |

</details>

---

### Context: `touch`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_OBELISK_MOON_TOUCH_ANSW, QEVENT_OBELISK_CORE_TOUCH_ANSW, "EVENT_MYSTERIOUSOBELISK_TOUCH_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha, none, lck` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |

</details>

---

### Context: `a`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"1", "class ability pool", "1 injury"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |

</details>

---

### Context: `b`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"5", "set ability pool", "many injuries"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |

</details>

---

### Context: `c`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"all (symmetric)", "class passive pool", "specific disorder"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |

</details>

---

### Context: `activate_p`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_OBELISK_MOON_ACTIVATE_ANSW, QEVENT_OBELISK_CORE_ACTIVATE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest, none` |  |

</details>

---

### Context: `activate_z`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_OBELISK_MOON_ACTIVATE_ANSW, QEVENT_OBELISK_CORE_ACTIVATE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest, none` |  |

</details>

---

### Context: `options`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `bad` | [`Block`](./Events_and_Encounters.md#context-bad) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Bad' action. |
| `damage` | [`Block`](./Events_and_Encounters.md#context-damage) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Damage' action. |
| `rare` | [`Block`](./Events_and_Encounters.md#context-rare) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rare' action. |
| `get_item_from_pool` | [`Enum/String`](./Enums.md#enum-get_item_from_pool) | `any_chapter, flesh_items` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `prompt` | String | `"EVENT_TRAVERSETHENECROPOLIS_REW6", "EVENT_TRACY_REW5"` |  |
| `gain_familiar` | [`Enum/String`](./Enums.md#enum-gain_familiar) | `Squirrel` | Event Action: Adds a specific familiar to the party. |
| `play_animation` | [`Enum/String`](./Enums.md#enum-play_animation) | `resultGood` |  |
| `weight` | [`Enum/String`](./Enums.md#enum-weight) | `.5` | Probability weight for this outcome. |

</details>

---

### Context: `d`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"all (asymmetric)", "pool disorder", "set passive pool"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |

</details>

---

### Context: `open`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_OPEN_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |
| `copy_results` | [`Enum/String`](./Enums.md#enum-copy_results) | `smash` |  |

</details>

---

### Context: `take`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_TAKE_ANSW", "EVENT_GOAROUND_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd, con, lck` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_dex_alt` |  |

</details>

---

### Context: `home`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `hint_chapter_exit` | [`Enum/String`](./Enums.md#enum-hint_chapter_exit) | `home` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_TIMEMACHINE_HOME_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `past`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `hint_chapter_exit` | [`Enum/String`](./Enums.md#enum-hint_chapter_exit) | `jurassic, iceage, endoftime` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_TIMEMACHINE_ICEAGE_PAST_ANSW, QEVENT_TIMEMACHINE_JURASSIC_INFINITE_ANSW, QEVENT_TIMEMACHINE_PAST_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `attack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BREAK_ANSW", "EVENT_BASH_ANSW", "EVENT_ATTACK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |
| `rare` | [`Block`](./Events_and_Encounters.md#context-rare) | `{ ... }` | Event Node: Story branch or dialog option representing the 'Rare' action. |

</details>

---

### Context: `charm`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_CHARM_ANSW, "EVENT_CHARM_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `fight`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_FIGHT_ANSW, "EVENT_FIGHT_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `next_event_from_set`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `event` | [`Enum/String`](./Enums.md#enum-event) | `Tragedy, Death` |  |
| `same_cat` | Boolean | `true` |  |
| `count` | Number | `4, 1, 3` | Quantity. |

</details>

---

### Context: `enter`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_HOLEINTHEEARTH_ENTER_ANSW", QEVENT_DIMENSIONXPORTAL_ENTER_ANSW, "EVENT_ENTER_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none, con, lck` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `hint_chapter_exit` | [`Enum/String`](./Enums.md#enum-hint_chapter_exit) | `dimensionx` |  |

</details>

---

### Context: `leave_party_temporarily`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `fights_skipped` | Number | `0, 1` |  |
| `return_as` | [`Enum/String`](./Enums.md#enum-return_as) | `enemy` |  |
| `return_during` | [`Enum/String`](./Enums.md#enum-return_during) | `boss` |  |

</details>

---

### Context: `lick`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LICK_ANSW", QEVENT_GLOWINGORB_LICK_ANSW, "EVENT_GOLEMLICK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha, con, none` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |

</details>

---

### Context: `bite`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_con` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_WALLOFFLESH_BITE2_ANSW, QEVENT_THROBBINGARTERY_BITE_ANSW, QEVENT_WALLOFFLESH_BITE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str, con` |  |

</details>

---

### Context: `inspect`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_INSPECT_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `skip`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT2_ANSW4", "QEVENT_STACYMUTANT1_ANSW4", "QEVENT_STACYMUTANT3_ANSW4"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `run`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_RUN_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_leave` |  |

</details>

---

### Context: `10coins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_ten` |  |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `get_item_from_pool` | [`Enum/String`](./Enums.md#enum-get_item_from_pool) | `chapter_rare` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `label` | String | `"EVENT_BEGGAR_5_ANSW"` |  |
| `prompt` | String | `"EVENT_ABEGGAR_REW2"` |  |
| `set_frame` | Number | `2` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `coins` |  |
| `stat_max` | Number | `10` |  |
| `stat_min` | Number | `10` |  |
| `weight` | Number | `10` | Probability weight for this outcome. |

</details>

---

### Context: `5coins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_one` |  |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `get_item_from_pool` | [`Enum/String`](./Enums.md#enum-get_item_from_pool) | `chapter_rare` | Event Action: Rewards the player with an item drawn from a specific loot pool. |
| `label` | String | `"EVENT_BEGGAR_5_ANSW"` |  |
| `prompt` | String | `"EVENT_ABEGGAR_REW2"` |  |
| `set_frame` | Number | `2` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `coins` |  |
| `stat_max` | Number | `5` |  |
| `stat_min` | Number | `5` |  |
| `weight` | Number | `5` | Probability weight for this outcome. |

</details>

---

### Context: `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `tag` | [`Enum/String`](./Enums.md#enum-tag) | `robot, rat` | Specific entity tag required. |
| `Fear` | Number | `1` | Applies or references the 'Fear' effect/state. |
| `Stun` | Number | `1` | Applies or references the 'Stun' effect/state. |
| `AllStatsUp` | Number | `1` | Applies or references the 'AllStatsUp' effect/state. |

</details>

---

### Context: `damage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BAHPHOMET_HEALTH_ANSW", "EVENT_DAMAGE_ANSW", "QEVENT_STACYMUTANT3_ANSW2"` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `drink`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_DRINK_ANSW, "EVENT_DRINK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con, lck` |  |

</details>

---

### Context: `kiss`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_KISS_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `party_random_mutation_from_set`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Number | `1` | Quantity. |
| `ears` | Number | `-2` |  |
| `eyebrows` | Number | `-2` |  |
| `eyes` | Number | `-2` |  |
| `mouth` | Number | `-2` |  |

</details>

---

### Context: `go_around`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GOAROUND_ANSW", "EVENT_TAKELONGWAY_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd, none, lck` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_leave` |  |

</details>

---

### Context: `outcome`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `play_animation` | [`Array`](./Arrays.md#array-play_animation) | `[ resultTragedy .5 ], [ resultBlessing .5 ], [ resultWeather .5 ]` |  |
| `random_pool` | [`Array`](./Arrays.md#array-random_pool) | `[ { set_frame 12 prompt "EVENT_ACAT_REW1" gain_cat_famili..., [ { set_frame 1 prompt "EVENT_BLESSING_REW1" heal 5 } { s..., [ { set_frame 1 prompt "EVENT_TRAGEDY_REW1" } { set_frame...` |  |
| `add_weather` | [`Enum/String`](./Enums.md#enum-add_weather) | `Birdemic` |  |
| `weather_roll` | [`Array`](./Arrays.md#array-weather_roll) | `[ { weight 1 set_frame 2 prompt "EVENT_HAPPENING_FOG_REW"...` |  |

</details>

---

### Context: `buy1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_one` |  |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `label` | String | `"EVENT_BUY_ANSW"` |  |
| `prompt` | String | `"EVENT_TRACY_REW4"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `coins` |  |
| `stat_max` | Number | `1` |  |
| `stat_min` | Number | `1` |  |
| `weight` | Number | `1` | Probability weight for this outcome. |

</details>

---

### Context: `StatusRandomEnemiesOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `count` | Number | `99, 2, 1` | Quantity. |
| `Fear` | Number | `2, 3` | Applies or references the 'Fear' effect/state. |
| `Bleed` | Number | `2` | Applies or references the 'Bleed' effect/state. |

</details>

---

### Context: `attach_antenna`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_GLOWINGORB_ANTENNA_ANSW, QEVENT_VOLCANO_ANTENNA_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `boogers`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_BEEPIS_ANSW", "EVENT_BOOGERS_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `donate_10`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_ten` |  |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `label` | String | `"EVENT_DONATE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `coins` |  |
| `stat_max` | Number | `10` |  |
| `stat_min` | Number | `10` |  |

</details>

---

### Context: `donate_15`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_ten` |  |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `label` | String | `"EVENT_DONATE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `coins` |  |
| `stat_max` | Number | `15` |  |
| `stat_min` | Number | `15` |  |

</details>

---

### Context: `donate_20`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_twentyfive` |  |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `label` | String | `"EVENT_DONATE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `coins` |  |
| `stat_max` | Number | `20` |  |
| `stat_min` | Number | `20` |  |

</details>

---

### Context: `donate_5`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_one` |  |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `label` | String | `"EVENT_DONATE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `coins` |  |
| `stat_max` | Number | `5` |  |
| `stat_min` | Number | `5` |  |

</details>

---

### Context: `global_effect_next_fight`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Fights` | Number | `1, 3` | Applies or references the 'Fights' effect/state. |

</details>

---

### Context: `investigate`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_INVESTIGATE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `poop`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_FEEBIS_ANSW", "EVENT_POOP_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `protection`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_CUTS_ANSW", "EVENT_PROTECTION_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `put_in_coins`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_coins_ten` |  |
| `animation_fail` | [`Enum/String`](./Enums.md#enum-animation_fail) | `choice_no_coins` |  |
| `label` | String | `"EVENT_VENDINGMACHINE_COINS_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `coins` |  |
| `stat_max` | Number | `10` |  |
| `stat_min` | Number | `10` |  |

</details>

---

### Context: `repell`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSCAVE1_RAPPEL_ANSW", "EVENT_MYSTERIOUSCAVE1_TALKTO_ANSW", "EVENT_MYSTERIOUSCAVE3_CLIMB_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex, str, cha` |  |

</details>

---

### Context: `blue`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `copy_results` | [`Enum/String`](./Enums.md#enum-copy_results) | `red` |  |
| `fixed_chance` | Number | `50%` |  |
| `label` | String | `"EVENT_BLUE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `button`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `copy_results` | [`Enum/String`](./Enums.md#enum-copy_results) | `lever` |  |
| `fixed_chance` | Number | `50%` |  |
| `label` | String | `"EVENT_PUSHBUTTON_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `find_another_way`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_JAGEDPATHWAY_ANSW_AROUND", "EVENT_FINDANOTHERWAY_ANSW"` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_leave` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `future`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `hint_chapter_exit` | [`Enum/String`](./Enums.md#enum-hint_chapter_exit) | `future` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_TIMEMACHINE_FUTURE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `infinite`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `hint_chapter_exit` | [`Enum/String`](./Enums.md#enum-hint_chapter_exit) | `endoftime` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_TIMEMACHINE_THEEND_INFINITE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `lever`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `fixed_chance` | Number | `50%` |  |
| `label` | String | `"EVENT_PULLLEVER_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `move_closer`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_ELEPHANTSFOOTCLOSER_ANSW", "EVENT_ELEPHANTSFOOT_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `play`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSSTRANGER_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd` |  |

</details>

---

### Context: `red`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `fixed_chance` | Number | `50%` |  |
| `label` | String | `"EVENT_RED_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `repair`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_REPAIR_ANSW", EVENT_REPAIR_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none, lck` |  |

</details>

---

### Context: `sacrifice`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BAHPHOMET_SACRIFICE_ANSW", "QEVENT_VOLCANO_SACRIFICE_ANSW"` |  |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `traverse`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_TRAVERSETHENECROPOLIS_ANSW"` |  |
| `play_animation` | [`Enum/String`](./Enums.md#enum-play_animation) | `resultGood` |  |
| `prompt` | String | `"EVENT_TRAVERSETHENECROPOLIS_REW5"` |  |
| `shop_now` | [`Enum/String`](./Enums.md#enum-shop_now) | `TreasureHard` |  |

</details>

---

### Context: `turnon`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSMACHINE_TURNITON_ANSW", "EVENT_TURNONTV_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int, lck` |  |

</details>

---

### Context: `KillEnemyOfTypeAtBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `enemy_type` | [`Enum/String`](./Enums.md#enum-enemy_type) | `any, cat` |  |
| `fallback_spawn` | [`Array`](./Arrays.md#array-fallback_spawn) | `[ TomTom Kitten CatCaller Mangy ]` |  |

</details>

---

### Context: `attach_amplifier`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_THEHEAD_AMPLIFIER_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `attach_leech`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_THROBBINGARTERY_ATTACH_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `book`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_SOMEOLDBOOK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `brace`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT1_ANSW2"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `counter`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT4_ANSW2"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `donate`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"Donate"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `double`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT4_ANSW1"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `fill_jar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_THEHEAD_FILLJAR_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `fire`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT2_ANSW1"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `holy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT1_ANSW3"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `hp`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT3_ANSW1"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `ice`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT2_ANSW2"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `intimidation`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_INTIMIDATION_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `itchies`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_ITCHIES_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `knife`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"Get a knife"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `leave_it_in`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_leave` |  |
| `label` | String | `"EVENT_JAGGEDPATHWAY_STALACTITE_ANSW2"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `lightning`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT2_ANSW3"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `loot_heart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_DEADKING_TAKEHEART_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `makeup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_MAKEUP_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `nothanks`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_leave` |  |
| `label` | String | `"EVENT_NOTHANKS_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `pirouette`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_PIROUETTE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `place_gristle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_WALLOFFLESH_PLACE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `receive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"Receive"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `reflect`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT4_ANSW3"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `run_again`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_leave` |  |
| `label` | String | `"EVENT_RUN_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd` |  |

</details>

---

### Context: `sacrifice_full_favor`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_VOLCANO_SACRIFICE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `sacrifice_normal`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_MEATALTAR_SACRIFICE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `sacrifice_partial_favor`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_VOLCANO_SACRIFICE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `sacrifice_quest`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_MEATALTAR_SACRIFICE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `setup`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `set_frame` | Number | `4` |  |

</details>

---

### Context: `speed`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT3_ANSW3"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `surprise`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_SURPRISE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `take_blood`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `QEVENT_DEADKING_DRAINBLOOD_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `tappytoes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_TAPPYTOES_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `thorns`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"QEVENT_STACYMUTANT1_ANSW1"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `w1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW1"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `w2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW2"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `w3`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW3"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `w4`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW4"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `w5`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW5"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `w6`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_CRATERWEATHER_ANSW6"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `wheezies`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `animation` | [`Enum/String`](./Enums.md#enum-animation) | `choice_misc` |  |
| `label` | String | `"EVENT_WHEEZIES_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `altar_sacrifice`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"king intro"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `arm`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_ARMINSIDE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `bash_past_alt`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BASH_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `bite_it_off`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BIGTOE_BITE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `blue_needle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_NEEDLES_BLUE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `body`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_GENIE_CHOICE_CURSEBODY` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `break_lock`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LOCKEDCRATE_BREAK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `bribe`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_BRIBE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `catch`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_CATCH_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd` |  |

</details>

---

### Context: `challenge_to_game`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DEATH_CHALLENGE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `chaos_ending`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"chaos ending"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `chapter_cutscene`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"chap"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `charm_past_alt`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_CHARM_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `climb`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_CLIMB_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `comfort`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_COMFORT_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `communicate`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_COMMUNICATE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `concheck`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GETINTHEHOLE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `conditional_reward`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `prompt` | String | `"EVENT_CATSINHEAT_REW6", "EVENT_CATSINHEAT_REW8"` |  |

</details>

---

### Context: `copy`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSMACHINE_COPY_ANSW"` |  |

</details>

---

### Context: `crack_open`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_CRACKOPEN_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `cut_wires`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_CUTWIRES_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `damage_1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DEMONICIDOL_1DAMAGE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `damage_full`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DEMONICIDOL_FULLDAMAGE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `damage_half`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DEMONICIDOL_HALFDAMAGE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `desert_cutscene`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"desert"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `dexcheck`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GETINTHEHOLE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `dig`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DIG_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `disarm`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DISARM_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `dive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DIVE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `eat_meat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LEAKINGMEAT_EAT_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `enter_crater`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSCRATER_ENTER_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `fiddle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_EXAMINE_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `find`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GOLEMFIND_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `follow`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_FOLLOW_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd` |  |

</details>

---

### Context: `free`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_FREE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `gain_familiar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `initial_health` | Number | `10` |  |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `CharmedCaveBaby` |  |

</details>

---

### Context: `hack`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_HACK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `intcheck`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GETINTHEHOLE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `join`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_JOININ_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `jump`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_JUMPOVER_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd` |  |

</details>

---

### Context: `jump_over`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_JUMPOVER_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `kiss_meat`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LEAKINGMEAT_KISS_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `leg`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LEGINSIDE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `lick_alt`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LICK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `listen`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LISTEN_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `looks`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_GENIE_CHOICE_LOOKS` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `mind`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_GENIE_CHOICE_CURSEMIND` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `outsmart`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BUTCHTUTORIAL_OUTSMART_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `party_permanent_stats`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `1` |  |

</details>

---

### Context: `patch_up`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_PATCHUP_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `pick_lock`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_LOCKEDCRATE_PICK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `pilfer`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_PILFER_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `power`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_GENIE_CHOICE_POWER` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `print`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSMACHINE_PRINT_ANSW"` |  |

</details>

---

### Context: `pull`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_PULLKNIFE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `pull_it_out`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_JAGGEDPATHWAY_STALACTITE_ANSW1"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `purify`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSCHAMBER_PURIFY_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `push_through`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_JAGEDPATHWAY_ANSW_PUSH"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `put_out_of_misery`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_PUTOUTOFMISERY_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `random_chance`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `chance` | Number | `50%` | Probability weight for this outcome. |
| `get_item_from_pool` | [`Enum/String`](./Enums.md#enum-get_item_from_pool) | `chapter` | Event Action: Rewards the player with an item drawn from a specific loot pool. |

</details>

---

### Context: `reach_inside`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_SMALLBLACKHOLE_REACHINSIDE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd` |  |

</details>

---

### Context: `read`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_READ_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `int` |  |

</details>

---

### Context: `red_needle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_NEEDLES_RED_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `remove`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_REMOVE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `remove_the_nail`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BIGTOE_NAIL_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `repair_quest`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_REPAIR_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `quest` |  |

</details>

---

### Context: `rest`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_REST_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `revive`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_REVIVE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `rub`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_RUB_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `run_away`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_RUNAWAY_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `spd` |  |

</details>

---

### Context: `scale`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSMACHINE_SCALE_ANSW"` |  |

</details>

---

### Context: `scream`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GOLEMSCREAM_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `shake`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_VENDINGMACHINE_SHAKE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `slip_through`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_SLIPTHROUGH_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `sneak_by`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_SNEAKBY_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `sneak_past_alt`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_SNEAKBY_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `dex` |  |

</details>

---

### Context: `soul`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_GENIE_CHOICE_CURSESOUL` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `sweet_talk`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_DEATH_SWEETTALK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `swim`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_SWIM_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `tail`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_TAILINSIDE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `talk`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_TALKTO_ANSW` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `talk_to`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_TALKTO_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `cha` |  |

</details>

---

### Context: `teleport`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSCHAMBER_TELEPORT_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `throw`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_HOLEINTHEEARTH_THROW_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `timemachine`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"Go to The Past"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `upgrade_yourself`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MYSTERIOUSCHAMBER_UPGRADE_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `use_item`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_USE_ITEM_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `use_toilet_con`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_USETOILET_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `use_toilet_str`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_USETOILET_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `wealth`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | [`Enum/String`](./Enums.md#enum-label) | `EVENT_GENIE_CHOICE_WEALTH` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `wish_genes`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MONKEYPAW_WISH2"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `wish_items`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MONKEYPAW_WISH3"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `wish_levelups`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MONKEYPAW_WISH4"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `wish_strength`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_MONKEYPAW_WISH1"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `none` |  |

</details>

---

### Context: `withstand`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_ELEPHANTSFOOTEVENCLOSER_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `con` |  |

</details>

---

### Context: `yank_it_out`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BIGTOE_YANK_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `str` |  |

</details>

---

### Context: `yellow_needle`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_NEEDLES_YELLOW_ANSW"` |  |
| `stat` | [`Enum/String`](./Enums.md#enum-stat) | `lck` |  |

</details>

---

### Context: `break_ice`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_FROZENHUMANOID_BREAKICE_ANSW"` |  |

</details>

---

### Context: `cross`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_CROSS_ANSW"` |  |

</details>

---

### Context: `face`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GIFTOFGLORG_FACE_ANSW"` |  |

</details>

---

### Context: `flush_yourself`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_FLUSHYOURSELF_ANSW"` |  |

</details>

---

### Context: `gain_clone_familiar`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `PlayerCat_MachineClone` |  |

</details>

---

### Context: `give_parasite`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_BODYOFGLORG_PARASITE_ANSW"` |  |

</details>

---

### Context: `head`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GIFTOFGLORG_HEAD_ANSW"` |  |

</details>

---

### Context: `keep_going`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_KEEPGOING_ANSW"` |  |

</details>

---

### Context: `neck`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_GIFTOFGLORG_NECK_ANSW"` |  |

</details>

---

### Context: `pull_lever`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_ODDDEVICE_PULLLEVER_ANSW"` |  |

</details>

---

### Context: `push_buttons`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_ODDDEVICE_PUSHBUTTONS_ANSW"` |  |

</details>

---

### Context: `use_weapon`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `label` | String | `"EVENT_USE_WEAPON_ANSW"` |  |

</details>

---

### Context: `spawn_reflection_next_fight`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |

</details>

---

