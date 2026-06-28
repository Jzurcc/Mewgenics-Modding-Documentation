---
title: "Status & Passive Keys Schema"
description: "Hooks for triggering logic when statuses are applied."
---

# Status & Passive Keys Schema

## Overview
> [!NOTE]
> This schema details internal triggers that fire when a unit receives, loses, or stacks a buff or debuff.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
OnStunned {
    on_status_applied {
        if_status "Stun"
        trigger_anim "dizzy"
    }
}
```

---



## Engine: Status and Passive Keys

This document lists every confirmed Status and Passive ID found across all game data files. These IDs are used as **dynamic keys** in any Status or Passive Container block (e.g. `statuses`, `passives`, `AddStatusToBasicAttack`, `bonus_passives`). The value paired with each key depends on the context: typically a stack count or duration for statuses, or a boolean/nested object for passives.

> **Note:** With over 1,200 unique IDs, this is the largest system in the game. Granting a character an ID (like `AddStatusToBasicAttack`) gives the character that reactive behaviour permanently.

> **Referenced by:** [`damage_instance` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-damage_instance), [`effects` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-effects), [`bonus_passives` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-bonus_passives), [`temporary_effects` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-temporary_effects), [`Else` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-else), [`ApplyToSource` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytosource), [`Conditional_HasTag` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_hastag), [`Conditional_Enemy` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_Ally` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_ally), [`keyword_tooltips` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-keyword_tooltips), [`additional_passives` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-additional_passives), [`RandomStatusFromPool` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-randomstatusfrompool), [`Conditional_Boss` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_boss), [`ApplyToSourceOnKill` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytosourceonkill), [`CanApplyToInanimate` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-canapplytoinanimate), [`Conditional_NotBoss` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_notboss), [`Conditional_HasStatus` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_hasstatus), [`Conditional_GoodRoll` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_goodroll), [`Conditional_Speculative` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_speculative), [`ApplyPassives` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applypassives), [`Conditional_FormulaIsPositive` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_formulaispositive), [`ApplyStatusIfCrit` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applystatusifcrit), [`Conditional_Corpse` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_corpse), [`Conditional_InForm` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_inform), [`Conditional_HealthThreshold` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_healththreshold), [`Conditional_Object` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_object), [`Conditional_PlayerCat` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_playercat), [`CollectsPickupsWithAltEffects` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-collectspickupswithalteffects), [`Conditional_Familiar` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_familiar), [`LateStatusApplication` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-latestatusapplication), [`TakeBonusTurnWithStatus` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-takebonusturnwithstatus), [`TempPassiveWhileHasStatus` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-temppassivewhilehasstatus), [`TimeDelayStatusApplication` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-timedelaystatusapplication), [`post_spawn_statuses` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-post_spawn_statuses), [`ApplyMultipleTimes` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applymultipletimes), [`Conditional_AffectedByElement` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_affectedbyelement), [`Conditional_FirstApplicationThisTurn` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_firstapplicationthisturn), [`Conditional_LastHit` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_lasthit), [`StatusOnBattleEnd` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-statusonbattleend), [`extra_statuses` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-extra_statuses), [`AddStatusToBasicAttack` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-addstatustobasicattack), [`ApplyToRandomPartyMemberIfPossible` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytorandompartymemberifpossible), [`Conditional_BadRoll` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_badroll), [`Conditional_BossOrBig` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_bossorbig), [`Conditional_Buddy` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_buddy), [`Conditional_Displaceable` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_displaceable), [`Conditional_NotAlly` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_notally), [`Conditional_NotBossOrBig` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_notbossorbig), [`Conditional_NotShielded` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_notshielded), [`Conditional_OncePerBattle` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_onceperbattle), [`Conditional_Shielded` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_shielded), [`Math` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-math), [`MeleeRevengeDamage` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-meleerevengedamage), [`OverHealToStatuses` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-overhealtostatuses), [`XIsTargetHealth` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-xistargethealth), [`AlphaStatusOnTurnBegin` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-alphastatusonturnbegin), [`ApplyPassivesToSpawnerWhileAlive` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applypassivestospawnerwhilealive), [`ApplyStatusesNextTurnBegin` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applystatusesnextturnbegin), [`ApplyToOthersWithSharedTagAndFaction` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-applytootherswithsharedtagandfaction), [`Conditional_ActiveWeather_Any` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_activeweather_any), [`Conditional_Backstab` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_backstab), [`Conditional_CanBeHealed` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_canbehealed), [`Conditional_DebuffRoll` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_debuffroll), [`Conditional_HasCleansableDebuffs` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_hascleansabledebuffs), [`Conditional_LivingPlayerCat` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_livingplayercat), [`Conditional_RandomChance` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_randomchance), [`Conditional_SourceAbilityHasTag` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_sourceabilityhastag), [`Conditional_SourceHasStatus` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-conditional_sourcehasstatus), [`PassiveWhileNotTakingTurn` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-passivewhilenottakingturn), [`ReviveNextRound` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-revivenextround), [`StatusGroup` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-statusgroup), [`StatusKillers` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-statuskillers), [`VisualCountDownThenApplyStatus` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-visualcountdownthenapplystatus), [`innate_passives` (Cat_Classes)](../Player_Progression_and_Cats/Cat_Classes.md#object-innate_passives), [`passives` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-passives), [`AddStatusToBasicAttack` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-addstatustobasicattack), [`effects` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-effects), [`MeleeRevengeDamage` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-meleerevengedamage), [`AddStatusToBasicMeleeAttack` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-addstatustobasicmeleeattack), [`StatusOnTookDamage` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statusontookdamage), [`StatusEachTurnBegin` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statuseachturnbegin), [`RandomStatusFromPool` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-randomstatusfrompool), [`StatusEachTurnEnd` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statuseachturnend), [`Conditional_RandomChance` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-conditional_randomchance), [`StatusEveryXSpellCasts` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statuseveryxspellcasts), [`StatusKilledCharacters` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statuskilledcharacters), [`StatusOnBattleEnd` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statusonbattleend), [`StatusOnEndMove` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statusonendmove), [`StatusOnTookDamageFromAbility` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statusontookdamagefromability), [`Conditional_FirstApplicationThisTurn` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-conditional_firstapplicationthisturn), [`Conditional_GoodRoll` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-conditional_goodroll), [`PassiveWhenAtFullMana` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-passivewhenatfullmana), [`StatusEachRoundEnd` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statuseachroundend), [`StatusEveryXSpellCastsEachTurn` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statuseveryxspellcastseachturn), [`StatusIfDidntMove` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statusifdidntmove), [`StatusIfUnusedMovePoints` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statusifunusedmovepoints), [`StatusOnAllyCatDeath` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statusonallycatdeath), [`StatusOnCastSpell` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statusoncastspell), [`StatusOnDie` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statusondie), [`StatusOnEatFood` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statusoneatfood), [`StatusOnKill` (Cat_Mutations)](../Player_Progression_and_Cats/Cat_Mutations.md#object-statusonkill), [`passives` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passives), [`AddStatusToBasicAttack` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-addstatustobasicattack), [`MeleeRevengeDamage` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-meleerevengedamage), [`ally_rewards` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-ally_rewards), [`effects` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-effects), [`PassiveGroup` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passivegroup), [`StatusCollector` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statuscollector), [`statuses` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statuses), [`StatusEachTurnEnd` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statuseachturnend), [`StatusOnKill` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statusonkill), [`StatusOnTookDamageFromAbility` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statusontookdamagefromability), [`keyword_tooltips` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-keyword_tooltips), [`RandomPassivePool` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-randompassivepool), [`Conditional_GoodRoll` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-conditional_goodroll), [`Holy` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-holy), [`StatusGroup` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statusgroup), [`StatusOnSpawnIn` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statusonspawnin), [`StatusOnTookDamage` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statusontookdamage), [`TempPassiveUntilSettled` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-temppassiveuntilsettled), [`alternate_energized_effect` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-alternate_energized_effect), [`passive` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passive), [`statuses_on_enter_form` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statuses_on_enter_form), [`AddStatusToReceivedDamage` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-addstatustoreceiveddamage), [`AddStatusToSpells` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-addstatustospells), [`AddStatusToTrampleDamage` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-addstatustotrampledamage), [`AddStatusToWeapons` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-addstatustoweapons), [`AdventureTokenPassivePool` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-adventuretokenpassivepool), [`Conditional_BadRoll` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-conditional_badroll), [`Conditional_HasKnockback` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-conditional_hasknockback), [`Conditional_IsPhysicalAttack` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-conditional_isphysicalattack), [`Else` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-else), [`FinalBossHitCountdownBoris` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-finalbosshitcountdownboris), [`FinalBossHitCountdownExplosive` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-finalbosshitcountdownexplosive), [`Fire` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-fire), [`ModularPickup` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-modularpickup), [`PassiveWhenDead` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-passivewhendead), [`RandomStatusFromPool` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-randomstatusfrompool), [`StacyMutant_Brace` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_brace), [`StacyMutant_Counter` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_counter), [`StacyMutant_Damage` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_damage), [`StacyMutant_DoubleHead` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_doublehead), [`StacyMutant_Fire` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_fire), [`StacyMutant_Health` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_health), [`StacyMutant_Holy` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_holy), [`StacyMutant_Ice` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_ice), [`StacyMutant_Lightning` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_lightning), [`StacyMutant_Mirror` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_mirror), [`StacyMutant_Speed` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_speed), [`StacyMutant_Thorns` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-stacymutant_thorns), [`StatusAfterXTurns` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statusafterxturns), [`StatusEachTurnBeginIfHasStatus` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statuseachturnbeginifhasstatus), [`StatusEachTurnEndForEachTurn` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statuseachturnendforeachturn), [`StatusEachTurnEndIfEnabledAtStartOfTurn` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statuseachturnendifenabledatstartofturn), [`StatusOnDie` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statusondie), [`StatusOnEndMove` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statusonendmove), [`StatusOnEnemyConfused` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statusonenemyconfused), [`StatusOnGainCoins` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statusongaincoins), [`StatusOverlappingCharactersAndDie` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statusoverlappingcharactersanddie), [`StatusWhenStatusCompletelyRemoved` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-statuswhenstatuscompletelyremoved), [`additional_statuses` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-additional_statuses), [`damage_instance` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-damage_instance), [`passives` (Elite_Buffs)](../Core_Entities_and_Combat/Elite_Buffs.md#object-passives), [`StatusEachRoundBegin` (Elite_Buffs)](../Core_Entities_and_Combat/Elite_Buffs.md#object-statuseachroundbegin), [`effects` (Elite_Buffs)](../Core_Entities_and_Combat/Elite_Buffs.md#object-effects), [`MeleeRevengeDamage` (Elite_Buffs)](../Core_Entities_and_Combat/Elite_Buffs.md#object-meleerevengedamage), [`StatusEachTurnEnd` (Elite_Buffs)](../Core_Entities_and_Combat/Elite_Buffs.md#object-statuseachturnend), [`statuses` (Elite_Buffs)](../Core_Entities_and_Combat/Elite_Buffs.md#object-statuses), [`AddStatusToBasicAttack` (Elite_Buffs)](../Core_Entities_and_Combat/Elite_Buffs.md#object-addstatustobasicattack), [`StatusEachRoundEnd` (Elite_Buffs)](../Core_Entities_and_Combat/Elite_Buffs.md#object-statuseachroundend), [`StatusOnDie` (Elite_Buffs)](../Core_Entities_and_Combat/Elite_Buffs.md#object-statusondie), [`StatusOnEnemyCastSpell` (Elite_Buffs)](../Core_Entities_and_Combat/Elite_Buffs.md#object-statusonenemycastspell), [`StatusOnKill` (Elite_Buffs)](../Core_Entities_and_Combat/Elite_Buffs.md#object-statusonkill), [`self_status_next_fight` (Events_and_Encounters)](../World_Maps_and_Events/Events_and_Encounters.md#object-self_status_next_fight), [`party_status_next_fight` (Events_and_Encounters)](../World_Maps_and_Events/Events_and_Encounters.md#object-party_status_next_fight), [`global_effect_next_fight` (Events_and_Encounters)](../World_Maps_and_Events/Events_and_Encounters.md#object-global_effect_next_fight), [`CharacterTypeGainsStatusAtBattleStart` (Events_and_Encounters)](../World_Maps_and_Events/Events_and_Encounters.md#object-charactertypegainsstatusatbattlestart), [`StatusRandomEnemiesOnBattleStart` (Events_and_Encounters)](../World_Maps_and_Events/Events_and_Encounters.md#object-statusrandomenemiesonbattlestart), [`effects` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-effects), [`Else` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-else), [`StatusCharactersOnRoundEnd` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-statuscharactersonroundend), [`ApplyPassives` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-applypassives), [`CharacterTypeGainsStatusAtBattleStart` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-charactertypegainsstatusatbattlestart), [`Conditional_GoodRoll` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-conditional_goodroll), [`RandomStatusFromPool` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-randomstatusfrompool), [`StatusAllCharactersOnSpawn` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-statusallcharactersonspawn), [`StatusCharactersOnRoundStart` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-statuscharactersonroundstart), [`Conditional_Corpse` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-conditional_corpse), [`Conditional_HasTag` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-conditional_hastag), [`Conditional_PartyMember` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-conditional_partymember), [`StatusOnBattleEnd` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-statusonbattleend), [`extra_statuses` (House_and_Environment)](../World_Maps_and_Events/House_and_Environment.md#object-extra_statuses), [`passives` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passives), [`AddStatusToBasicAttack` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addstatustobasicattack), [`effects` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-effects), [`MeleeRevengeDamage` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-meleerevengedamage), [`StatusOnBattleEnd` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonbattleend), [`StatusEachTurnEnd` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statuseachturnend), [`StatusOnBreak` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonbreak), [`Conditional_GoodRoll` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_goodroll), [`StatusOnKill` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonkill), [`StatusOnTookDamage` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusontookdamage), [`StatusOnBattleStart` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonbattlestart), [`StatusEachTurnBegin` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statuseachturnbegin), [`AddSelfStatusToBasicAttack` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addselfstatustobasicattack), [`AddStatusToAllDamage` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addstatustoalldamage), [`StatusAlliesOnBattleStart` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusalliesonbattlestart), [`StatusOnKillEnemy` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonkillenemy), [`AddPassivesToMinions` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addpassivestominions), [`ApplyToSource` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-applytosource), [`StatusOnDie` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusondie), [`StatusOnEndMove` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonendmove), [`Conditional_HasStatus` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_hasstatus), [`Else` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-else), [`StatusOnTakeHealthOrShieldDamage` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusontakehealthorshielddamage), [`StatusOnTurnEndIfDidntCastAbilityTypes` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonturnendifdidntcastabilitytypes), [`StatusRandomEnemiesOnBattleStart` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusrandomenemiesonbattlestart), [`CatchProjectiles` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-catchprojectiles), [`Conditional_PartyMember` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_partymember), [`PassiveWhenDead` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passivewhendead), [`StatusAllCharactersOnSpawn` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusallcharactersonspawn), [`StatusEveryXSpellCasts` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statuseveryxspellcasts), [`StatusIfUnusedMovePoints` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusifunusedmovepoints), [`StatusOnPopCorpse` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonpopcorpse), [`AddStatusToElementDamage` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addstatustoelementdamage), [`AddStatusToKnockbackDamage` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addstatustoknockbackdamage), [`AddStatusToSpells` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addstatustospells), [`ApplyStatusesToRandomEnemiesEachTurn` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-applystatusestorandomenemieseachturn), [`Conditional_Adjacent` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_adjacent), [`Conditional_BadRoll` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_badroll), [`Conditional_Boss` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_boss), [`Conditional_HasTag` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_hastag), [`Conditional_OncePerBattle` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_onceperbattle), [`PassiveIfWeaponIsUsable` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passiveifweaponisusable), [`StatusAfterCastSpell` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusaftercastspell), [`StatusAfterXStacks` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusafterxstacks), [`StatusIfUnusedActPoints` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusifunusedactpoints), [`StatusOnAllyCatDeath` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonallycatdeath), [`StatusOnBackstab` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonbackstab), [`StatusOnBreakItem` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonbreakitem), [`StatusOnCastSpell` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusoncastspell), [`StatusOnGainCoins` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusongaincoins), `StatusOnSetPieceBreak` (Items_and_Equipment), [`bonus_passives` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-bonus_passives), [`keyword_tooltips` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-keyword_tooltips), [`passive` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passive), [`AddPassivesToCharmed` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addpassivestocharmed), [`AddSelfStatusToWeapons` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addselfstatustoweapons), [`AddStatusToBackstabs` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addstatustobackstabs), `AddStatusToFirstSpellEachTurn` (Items_and_Equipment), [`AddStatusToWeapons` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-addstatustoweapons), [`ApplyPassives` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-applypassives), [`ApplyToRandomPartyMemberIfPossible` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-applytorandompartymemberifpossible), [`Conditional_Ally` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_ally), [`Conditional_Corpse` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_corpse), [`Conditional_Enemy` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_enemy), `Conditional_HasCleansableDebuffs` (Items_and_Equipment), [`Conditional_HealthThreshold` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_healththreshold), [`Conditional_ManaThreshold` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_manathreshold), [`Conditional_PlayerCat` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_playercat), [`Conditional_RandomChance` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_randomchance), [`Conditional_Shielded` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_shielded), [`ConvertDamageToScaledStatus` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-convertdamagetoscaledstatus), [`CritsApplyStatus` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-critsapplystatus), [`Eternal` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-eternal), `GlobalFlowerTrapperAura` (Items_and_Equipment), [`PassiveWhileHasDurability` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passivewhilehasdurability), [`PassiveWhileInMonkMeleeStance` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passivewhileinmonkmeleestance), [`PassiveWhileShielded` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-passivewhileshielded), [`RandomStatusFromPool` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-randomstatusfrompool), [`ReviveNextRound` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-revivenextround), [`ScaledStatusOnHolyShieldBlock` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-scaledstatusonholyshieldblock), [`ScaledStatusOnSpendMana` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-scaledstatusonspendmana), [`StatDependentPassive` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statdependentpassive), [`StatusAfterXTurns` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusafterxturns), [`StatusAlliesEachTurn` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusallieseachturn), [`StatusAlliesOnDeath` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusalliesondeath), [`StatusEachRoundEnd` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statuseachroundend), [`StatusEachTurnEndForEachTurn` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statuseachturnendforeachturn), [`StatusOnCollectPickup` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusoncollectpickup), [`StatusOnDodge` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusondodge), [`StatusOnEatFood` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusoneatfood), `StatusOnEatPill` (Items_and_Equipment), [`StatusOnEnemyDeath` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonenemydeath), [`StatusOnFallAsleep` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonfallasleep), [`StatusOnHealed` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonhealed), [`StatusOnPickupCoins` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonpickupcoins), `StatusOnTurnEndIfCastNSpells` (Items_and_Equipment), [`StatusOnUseBasicAttack` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statusonusebasicattack), [`StatusWhenAllySpendsMana` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-statuswhenallyspendsmana), [`TempPassiveUntilSettled` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-temppassiveuntilsettled), [`damage_instance` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-damage_instance), [`CharacterTypeGainsStatusAtBattleStart` (Miscellaneous)](../Reference_and_Meta/Miscellaneous.md#object-charactertypegainsstatusatbattlestart), [`passives` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives), [`AddStatusToBasicAttack` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicattack), [`effects` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects), [`AddPassivesToMinions` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addpassivestominions), [`StatusOnTookDamage` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusontookdamage), [`StatusEachTurnEnd` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnend), [`StatusOnBattleEnd` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonbattleend), [`StatusOnKill` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonkill), [`StatusOnStanceSwitch` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonstanceswitch), [`StatusEachTurnBegin` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnbegin), [`Conditional_Ally` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_ally), [`CritsApplyStatus` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-critsapplystatus), [`MeleeRevengeDamage` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-meleerevengedamage), [`PassiveIfAllArmorEmpty` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveifallarmorempty), [`RandomStatusFromPool` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-randomstatusfrompool), [`StatusOnCrit` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusoncrit), [`Conditional_Enemy` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_enemy), [`PassiveIfEmptyFace` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveifemptyface), [`PassiveIfEmptyHead` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveifemptyhead), [`PassiveIfEmptyNeck` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveifemptyneck), [`StatusAlliesOnDeath` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusalliesondeath), [`StatusOnUseAbilityWithTag` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonuseabilitywithtag), [`AddStatusToElementAbilities` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoelementabilities), [`AddStatusToWeapons` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoweapons), [`Else` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-else), [`keyword_tooltips` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-keyword_tooltips), [`AddStatusToAllDamage` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoalldamage), [`AddStatusToBasicMeleeAttack` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicmeleeattack), [`StatusOnCastSpell` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusoncastspell), [`StatusOnOverHealed` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonoverhealed), [`AddPassivesToCharmed` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addpassivestocharmed), [`AddStatusToElementDamage` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoelementdamage), [`AddStatusToExplosions` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoexplosions), [`Conditional_FirstApplicationThisTurn` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_firstapplicationthisturn), [`PassiveWhenAtFullMana` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhenatfullmana), [`StatusAlliesOnKill` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusalliesonkill), [`StatusIfUnusedMovePoints` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusifunusedmovepoints), [`StatusOnTurnEndIfCastNSpells` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonturnendifcastnspells), [`StatusOnTurnEndIfManaExact` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonturnendifmanaexact), [`StatusOnTurnEndIfManaOrHealthExact` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonturnendifmanaorhealthexact), [`AddSelfStatusToBasicAttack` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addselfstatustobasicattack), [`Conditional_BadRoll` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_badroll), [`Conditional_HasStatus` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_hasstatus), [`StatusEveryXSpellCasts` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseveryxspellcasts), [`StatusGroup` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusgroup), [`StatusKilledCharacters` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuskilledcharacters), [`StatusOnAllyCatDeath` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonallycatdeath), [`StatusOnBattleStart` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonbattlestart), [`StatusOnEatFood` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusoneatfood), [`StatusOnGainCoins` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusongaincoins), [`StatusOnHealed` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonhealed), [`StatusOnKillEnemy` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonkillenemy), [`StatusOnTookDamageFromAbility` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusontookdamagefromability), [`statuses` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuses), [`AddPassivesToSummonAbilityMinions` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addpassivestosummonabilityminions), [`AddSelfStatusToWeapons` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addselfstatustoweapons), [`AddStatusToAllDamageAbilities` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoalldamageabilities), [`AddStatusToFirstBasicAttack` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustofirstbasicattack), [`AddStatusToTrampleDamage` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustotrampledamage), [`ApplyStatusIfCrit` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-applystatusifcrit), [`ApplyStatusesToRandomEnemiesEachTurn` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-applystatusestorandomenemieseachturn), [`ApplyToSource` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-applytosource), [`CatchProjectiles` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catchprojectiles), [`Conditional_Adjacent` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_adjacent), [`Conditional_Boss` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_boss), [`Conditional_Corpse` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_corpse), [`Conditional_HasTag` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_hastag), [`Conditional_NotBoss` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_notboss), [`Conditional_PartyMember` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_partymember), [`Conditional_Shielded` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_shielded), [`Electric` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-electric), [`Eternal` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-eternal), [`Fire` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-fire), [`Grass` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-grass), [`Gravity` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-gravity), [`Holy` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-holy), [`HolyDamageBlessing` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-holydamageblessing), [`Ice` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-ice), [`LateBloomer` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-latebloomer), [`LightningRod` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-lightningrod), [`NextBattleStatus` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-nextbattlestatus), [`PassiveAtFullHealth` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveatfullhealth), [`PassiveGroup` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivegroup), [`PassiveUntilCastSpell` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveuntilcastspell), [`PassiveWhileInMonkMeleeStance` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhileinmonkmeleestance), [`PassiveWhileInMonkRangedStance` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhileinmonkrangedstance), [`PassiveWhilePreviewingMonkRangedStance` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhilepreviewingmonkrangedstance), [`ScaledStatusOnOverMana` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-scaledstatusonovermana), [`ScaledStatusOnSpendMana` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-scaledstatusonspendmana), [`SpecialFriends` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-specialfriends), [`StatusAfterCastSpell` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusaftercastspell), [`StatusAlliesOnBattleStart` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusalliesonbattlestart), [`StatusAlliesOnGainCoins` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusalliesongaincoins), [`StatusAllyWhenAllySpendsMana` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusallywhenallyspendsmana), [`StatusAnyCatAllyWhoKills` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusanycatallywhokills), [`StatusDamagers` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusdamagers), [`StatusEachTurnEndForEachTurn` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnendforeachturn), [`StatusEachTurnEndPerEnemyKill` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnendperenemykill), [`StatusEnemiesOnDeath` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusenemiesondeath), [`StatusEveryXTurnBegins` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseveryxturnbegins), [`StatusKillers` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuskillers), [`StatusOnAnyDeath` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonanydeath), [`StatusOnBreakItem` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonbreakitem), [`StatusOnCollectPickup` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusoncollectpickup), [`StatusOnDealtDamage` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusondealtdamage), [`StatusOnDealtDamageThreshold` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusondealtdamagethreshold), [`StatusOnEndMove` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonendmove), [`StatusOnGainShield` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusongainshield), [`StatusOnHeal` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonheal), [`StatusOnOverMana` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonovermana), [`StatusOnPickupCoins` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonpickupcoins), [`StatusOnPopCorpse` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonpopcorpse), [`StatusOnTookDamageFromEnemyAbility` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusontookdamagefromenemyability), [`StatusOnTriggerTrap` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusontriggertrap), [`StatusOnUseBasicAttack` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonusebasicattack), [`StatusOnUseElementAbility` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonuseelementability), [`StatusPerInjury` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusperinjury), [`StatusWhenAllySpendsMana` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuswhenallyspendsmana), [`TaggedPickupEffectReplacement` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-taggedpickupeffectreplacement), [`AddStatusToKnockbackDamage` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoknockbackdamage), [`AddStatusToSpells` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustospells), [`AddStatusesIfPersistentWeatherElement` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatusesifpersistentweatherelement), [`AddStatusesToReceivedElementalDamage` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatusestoreceivedelementaldamage), [`Conditional_DoesDamage` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_doesdamage), [`Conditional_GoodRoll` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_goodroll), [`Diabetes` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-diabetes), [`PassiveLevelScaledStatus` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivelevelscaledstatus), [`RandomPassivePool` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-randompassivepool), [`ScaledStatusOnBleedDamage` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-scaledstatusonbleeddamage), [`ScaledStatusOnLoseShield` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-scaledstatusonloseshield), [`StatusAlliesEachTurn` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusallieseachturn), [`StatusAlliesOnSpendMana` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusalliesonspendmana), [`StatusAlliesScaledByCursedOnDeath` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusalliesscaledbycursedondeath), [`StatusIfBattleAlreadyBegan` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusifbattlealreadybegan), [`StatusOnEatPill` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusoneatpill), [`StatusOnLoseShield` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonloseshield), [`StatusOnTakeHealthDamage` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusontakehealthdamage), [`StatusOnTurnEndIfDidntCastAbilityTypes` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonturnendifdidntcastabilitytypes), [`TakeBonusTurnWithStatus` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-takebonusturnwithstatus), [`TheHunger` (Passives_and_Statuses)](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-thehunger)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2807 | `{ . . . }` |
| [`class`](../Reference_and_Meta/Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1484 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 990 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 583 | `{ . . . }` |
| [`int`](../Reference_and_Meta/Enums.md#enum-int) | Enum / Integer  | The Intelligence stat value or modifier. | 355 | `-1`<br>`-10`<br>`-2` |
| [`neck`](../Reference_and_Meta/Enums.md#enum-neck) | Enum | The neck equipment item assigned to the unit. | 209 | `AngelicAura`<br>`AngelicAura_Terminator`<br>`DruidNeck` |
| [`lck`](../Reference_and_Meta/Enums.md#enum-lck) | Enum / Integer  | The Luck stat value or modifier. | 283 | `-1`<br>`-2`<br>`-3` |
| [`bonus_passives`](../Reference_and_Meta/Miscellaneous.md#object-bonus_passives) | Object  | Grants temporary passive abilities to the caster for the duration of the ability. | 138 | `{ . . . }` |
| [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 248 | `{ . . . }` |
| [`Colorless`](./Engine_LogicKeys.md#object-colorless) | Object  | Specifies the 'Colorless' form within FormChanger, used for boss dialogue. | 247 | `{ . . . }` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 124 | `1`<br>`2`<br>`true` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 618 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`FormChanger`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-formchanger) | Object  | Defines the unit's form-changing data, including multiple form definitions and their sub-properties. | 106 | `{ . . . }` |
| [`SpawnOnDeath`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnondeath) | Enum / Object  | Specifies an object and its faction to spawn when the unit dies. | 81 | `{ . . . }`<br>`Antidote`<br>`BiggestFood`<br>`FrankPinky` |
| `IgnoreSelf` | Boolean / Integer | If set to 1 or true, the damage instance ignores the source unit (does not affect itself). | 75 | `1`<br>`true` |
| [`Tinkerer`](./Engine_LogicKeys.md#object-tinkerer) | Object  | Form identifier for the Tinkerer boss type. | 132 | `{ . . . }` |
| [`Hunter`](./Engine_LogicKeys.md#object-hunter) | Object  | Defines a list of quotes for the Hunter class (vs boss, embark, return early). | 136 | `{ . . . }` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 108 | `1`<br>`10`<br>`2` |
| [`Medic`](./Engine_LogicKeys.md#object-medic) | Object  | Defines a list of quotes for the Medic class. | 119 | `{ . . . }` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 836 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`RandomArmorPickup`](./Engine_LogicKeys.md#object-randomarmorpickup) | Float / Object  | The amount of random armor pickups spawned. | 61 | `{ . . . }`<br>`4.5`<br>`40` |
| [`BasicMelee`](./Engine_StatusAndPassiveKeys.md#object-basicmelee) | Object  | An object defining properties for a basic melee attack passive. | 126 | `{ . . . }` |
| [`StatusImmunity`](../Reference_and_Meta/Arrays.md#array-statusimmunity) | Array / Enum  | A list of status effect names the unit is immune to. | 38 | `Burn`<br>`Poison`<br>`Tarred` |
| [`Wood`](./Engine_StatusAndPassiveKeys.md#object-wood) | Variable | A variable representing the Wood element or material type. | 25 ||
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 50 | `1`<br>`10`<br>`100` |
| `HealthGain` | Integer | The amount of health restored to the source. | 63 | `1`<br>`10`<br>`2` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 130 | `1`<br>`2`<br>`3` |
| [`FormChangeWhileHasStatus`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-formchangewhilehasstatus) | Object  | Defines a form change condition that activates while the unit has a specific status effect. | 35 | `{ . . . }` |
| [`StatusOnTookDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusontookdamage) | Object  | Specifies status effects or actions triggered when the unit takes damage. | 46 | `{ . . . }` |
| [`AddElementsToBasicAttack`](../Reference_and_Meta/Enums.md#enum-addelementstobasicattack) | Enum | Specifies an elemental damage type that is added to the unit's basic attacks. | 23 | `Electric`<br>`Fire`<br>`Gravity` |
| `Jester` | Array | An array of dialogue quotes for the Jester class. | 52 | `[` |
| [`MulticlassLevelUp`](../Reference_and_Meta/Enums.md#enum-multiclasslevelup) | Enum | Specifies the class that this unit gains a level in when multiclassing. | 28 | `Butcher`<br>`Druid`<br>`Fighter` |
| [`AddPassivesToMinions`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addpassivestominions) | Object  | An object containing passives that are granted to all minions spawned by the unit. | 36 | `{ . . . }` |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |
| `DodgeChance` | Integer | The percentage chance the unit has to dodge incoming attacks. | 35 | `10%`<br>`15%`<br>`2%` |
| [`EliteTint`](../Reference_and_Meta/Arrays.md#array-elitetint) | Array | An RGBA tint color (r g b a) applied to elite variants of a unit. | 30 | `[.3 .25 .3 .75]`<br>`[.4 .4 .4]`<br>`[.5 .5 .8 1]` |
| [`RevengeDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-revengedamage) | Object  | An object defining the damage and effects that trigger when the unit is attacked. | 31 | `{ . . . }` |
| `AddCritMultiplier` | Integer | The percentage added to the critical hit damage multiplier. | 24 | `100%`<br>`125%`<br>`150%` |
| [`TransformAbility`](../Reference_and_Meta/Enums.md#enum-transformability) | Enum | Specifies the ability that replaces the current ability. | 28 | `BerserkDash`<br>`BerserkDash2`<br>`BirthSquirrel` |
| [`knockback`](../Reference_and_Meta/Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 314 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| `AddBonusRange` | Integer | The number of additional tiles of range added to the unit's abilities. | 32 | `1`<br>`10`<br>`2` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |
| [`ImmediateAbilityReaction`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-immediateabilityreaction) | Array / Enum / Object  | Specifies an ability or list of abilities used immediately in reaction to a triggering event. | 26 | `{ . . . }`<br>`BirthwortReactionShot`<br>`BumbleButt`<br>`CatGoop` |
| `Knockback` | Equation | The number of tiles the target is pushed away from the source on hit. | 33 | `1`<br>`10`<br>`2` |
| [`Paper`](./Engine_StatusAndPassiveKeys.md#object-paper) | Variable | A variable representing the Paper element or material type. | 26 ||
| `even_if_dead` | Boolean | If true, the effect triggers even if the unit is dead. | 25 | `true` |
| `Undead` | Integer | If set, flags the unit as undead (e.g., 1) with associated mechanics. | 26 | `1` |
| `Brittle` | Integer | The number of stacks of the Brittle status, or an object defining its properties. | 26 | `1` |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 24 | `10`<br>`15`<br>`20` |
| [`party_status_next_fight`](../Reference_and_Meta/Miscellaneous.md#object-party_status_next_fight) | Object  | An object defining status effects to apply to the party at the start of the next fight. | 26 | `{ . . . }` |
| [`PassiveWhenAffectedByElement`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhenaffectedbyelement) | Object  | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 18 | `{ . . . }` |
| [`SpawnOnBattleStart`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnonbattlestart) | Enum / Object  | Specifies the object that spawns adjacent to the unit at the start of battle. | 54 | `{ . . . }`<br>`BeefyCharmedLeech`<br>`BuffCharmedKitten`<br>`CharmedCultist` |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 160 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 50 | `1`<br>`2`<br>`4` |
| [`mode`](../Reference_and_Meta/Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 29 | `equal`<br>`greater`<br>`greater_or_equal` |
| [`StatusOnBreak`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonbreak) | Object  | An object defining statuses or effects applied when an item or object breaks. | 22 | `{ . . . }` |
| [`threshold`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 49 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| [`additional_passives`](../Reference_and_Meta/Miscellaneous.md#object-additional_passives) | Object  | Additional passive abilities applied to the spawned unit. | 20 | `{ . . . }` |
| [`BossRewards`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bossrewards) | Object  | Defines the common and rare item rewards dropped by a boss on defeat. | 20 | `{ . . . }` |
| [`Brace`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 169 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`ForceUseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 33 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`MeleeRevengeDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-meleerevengedamage) | Object  | Defines the damage and effects applied back to a melee attacker upon being hit. | 73 | `{ . . . }` |
| [`EliteParticle`](../Reference_and_Meta/Enums.md#enum-eliteparticle) | Enum | Specifies the particle effect name attached to an elite unit. | 19 | `AbsorbBuff`<br>`FireExtinguish_Steam`<br>`FlyBuff` |
| [`FindItemFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 43 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`BirdRewards`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-birdrewards) | Object  | Defines the rewards and statuses applied when a bird allies with the unit. | 18 | `{ . . . }` |
| [`Buddy`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-buddy) | Enum / Object  | Specifies a buddy unit that accompanies or is spawned alongside the unit, with optional reclaim and targeting properties. | 24 | `{ . . . }`<br>`BoyDino`<br>`CaveCatDad`<br>`Chubs` |
| [`Coin`](./Engine_LogicKeys.md#object-coin) | Integer / Object  | The number of coin pickups spawned. | 34 | `{ . . . }`<br>`1`<br>`70` |
| [`Consumed`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-consumed) | Object  | An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`. | 23 | `{ . . . }` |
| [`SpawnThingOnDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnthingondamage) | Object  | Specifies an object that spawns on the tile when the unit takes damage. | 38 | `{ . . . }` |
| [`StatusOnKill`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonkill) | Object  | Specifies status effects or actions triggered when the unit kills an enemy. | 40 | `{ . . . }` |
| [`AbilityOnBattleStart_Immediate`](../Reference_and_Meta/Enums.md#enum-abilityonbattlestart_immediate) | Enum | Specifies the ability triggered instantly at the start of battle. | 17 | `BrambleRandomTileEvent`<br>`FlowerEventSleep`<br>`Flush` |
| `CollectsPickups` | Integer | If set to 1 or greater, the unit collects pickups (e.g., items) on contact. | 17 | `1`<br>`2` |
| [`Conditional_GoodRoll`](./Engine_StatusAndPassiveKeys.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 37 | `{ . . . }` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 51 | `-1`<br>`-2`<br>`-4` |
| `OverrideKnockbackDamage` | Enum / Equation | A formula or flat value that sets the damage dealt when knockback occurs, overriding default calculations. | 17 | `"max(5+bonus_melee_ability_damage, 1)"`<br>`0`<br>`2` |
| [`RandomMagicMissile`](./Engine_StatusAndPassiveKeys.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. | 41 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `rat` | Variable | A variable representing the Rat element or material type. | 15 ||
| [`AddStatusToBasicMeleeAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicmeleeattack) | Object  | An object listing status effects applied by the unit's basic melee attack. | 11 | `{ . . . }` |
| [`CharacterLightSource`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-characterlightsource) | Object  | Defines a dynamic light source attached to the unit, including color, glow, and size. | 16 | `{ . . . }` |
| [`ElementImmune`](../Reference_and_Meta/Enums.md#enum-elementimmune) | Enum | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 51 | `Creep`<br>`Electric`<br>`Fire` |
| [`HealthPickup`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-healthpickup) | Object  | Defines properties for a health pickup object, such as healing amount and visual frame range. | 16 | `{ . . . }` |
| `less_or_equal` | Variable | A variable representing a comparison mode for threshold checks (less than or equal). | 16 ||
| `PassiveLevelUpAtCombatEnd` | Integer | The number of times a passive levels up automatically when combat ends. | 10 | `1` |
| [`pyrophina`](./Engine_StatusAndPassiveKeys.md#object-pyrophina) | Variable | A variable representing the Pyrophina element or material type. | 14 ||
| [`StatusEachTurnBegin`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnbegin) | Object  | Specifies status effects applied to the unit at the start of each of its turns. | 27 | `{ . . . }` |
| [`StatusEachTurnEnd`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnend) | Object  | Specifies status effects applied to the unit at the end of each of its turns. | 57 | `{ . . . }` |
| [`zaratana`](./Engine_StatusAndPassiveKeys.md#object-zaratana) | Variable | A variable representing the Zaratana element or material type. | 19 ||
| [`ApplyToSourceOnKill`](../Reference_and_Meta/Miscellaneous.md#object-applytosourceonkill) | Object  | Contains effects that are applied to the source when it kills the target. | 15 | `{ . . . }` |
| [`CanApplyToInanimate`](./Engine_StatusAndPassiveKeys.md#object-canapplytoinanimate) | Object  | An object containing effects that can be applied to inanimate objects. | 15 | `{ . . . }` |
| `HealthMultiplier` | Float | A multiplier applied to the unit's base health. | 15 | `.5`<br>`.8`<br>`1.5` |
| [`Maggot`](./Engine_StatusAndPassiveKeys.md#object-maggot) | Object  | An object defining properties for the Maggot passive or status. | 46 | `{ . . . }` |
| [`ReplaceSpawnedObjects`](../Reference_and_Meta/Arrays.md#array-replacespawnedobjects) | Array | An array of [original_object replacement_object] pairs for swapping spawned objects. | 15 | `[Boulder AnimatedBoulder]`<br>`[Boulder AnimatedLavaBoulder]`<br>`[Crow Crow2]` |
| [`ChangeCatClass`](../Reference_and_Meta/Enums.md#enum-changecatclass) | Enum | Specifies the new class to assign to the unit. | 14 | `Butcher`<br>`Colorless`<br>`Druid` |
| `EndTurn` | Integer | If set to 1, ends the current unit's turn immediately after this effect. | 14 | `1` |
| `meat` | Variable | A variable representing the Meat element or material type. | 7 ||
| [`PassiveGroup`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivegroup) | Object  | A group of passive abilities that can be randomly assigned. | 14 | `{ . . . }` |
| [`SpawnOnDowned`](../Reference_and_Meta/Enums.md#enum-spawnondowned) | Enum | Specifies the character or object spawned when the unit is downed. | 8 | `CharmedFly`<br>`CharmedKitten`<br>`CharmedSpookie` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 234 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`statuses`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuses) | Object  | Defines the status effects applied when the parent trigger event occurs. | 14 | `{ . . . }` |
| `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 127 | `1`<br>`3`<br>`4` |
| [`TransformBasicAttack`](../Reference_and_Meta/Enums.md#enum-transformbasicattack) | Enum | Specifies the ability that replaces the unit's basic attack. | 14 | `AntlerSwipe`<br>`AntlerSwipe2`<br>`Chitter` |
| [`ApplyPassives`](../Reference_and_Meta/Miscellaneous.md#object-applypassives) | Object  | Specifies the passives or status effects to apply to the unit. | 13 | `{ . . . }` |
| [`DeathRattleRevive`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-deathrattlerevive) | Enum / Object  | Specifies an ability or effect that revives the unit upon death, with options for stunning behavior. | 13 | `{ . . . }`<br>`DoNothing`<br>`HCHumanDie`<br>`ToxPuff` |
| `Flammable` | Integer | The number of stacks of Flammable, or an object defining its properties. | 14 | `1`<br>`2` |
| [`SafeDoomed`](../Reference_and_Meta/Enums.md#enum-safedoomed) | Enum / Integer  | The number of SafeDoomed stacks applied, or 'level' to scale with character level. | 16 | `1`<br>`2`<br>`level` |
| [`TransformOnDeath`](../Reference_and_Meta/Arrays.md#array-transformondeath) | Array / Enum  | Specifies the unit or list of units to transform into upon death. | 13 | `BishopHat`<br>`CanCreeperOut`<br>`Carcus` |
| `AddBonusMeleeRange` | Integer | The number of additional tiles of range added to the unit's melee attacks. | 11 | `1`<br>`10`<br>`2` |
| `AddCorpseHealth` | Integer | The amount of bonus health the unit's corpse has before it can be resurrected. | 20 | `-999`<br>`-999999`<br>`100` |
| `AddMaxHealth` | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 14 | `-25`<br>`10`<br>`2` |
| [`Bionic`](./Engine_StatusAndPassiveKeys.md#object-bionic) | Variable | A variable representing the Bionic element or material type. | 18 ||
| [`BonusAbility`](../Reference_and_Meta/Enums.md#enum-bonusability) | Enum | Specifies the name of a bonus ability granted. | 18 | `Bloodzerk`<br>`BonusToss`<br>`BonusToss2` |
| [`CritsApplyStatus`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-critsapplystatus) | Object  | An object containing statuses applied to the target when the unit lands a critical hit. | 12 | `{ . . . }` |
| [`DeadAltAbility`](../Reference_and_Meta/Enums.md#enum-deadaltability) | Enum | Specifies an alternative ability used when the unit is dead. | 12 | `CarrionShot_Afterlife`<br>`CarrionShot_Afterlife2`<br>`CoffinFlop_Afterlife` |
| `Displace` | Integer | If set to 1, the unit is displaced to another location (e.g., teleport). | 12 | `1` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 414 | `[`<br>`[Heat Fire]` |
| [`EquipTemporaryItem`](../Reference_and_Meta/Enums.md#enum-equiptemporaryitem) | Enum | Specifies which temporary item is equipped. | 12 | `Bottles`<br>`ButcherHook_Temporary`<br>`FoodBig` |
| `IgnoreTiles` | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 15 | `1` |
| `NoHealthOnlyShield` | Integer | If set (e.g., 1), the unit has no health and only a shield for damage absorption. | 12 | `1` |
| [`ObjectOnHitCharacter`](./Engine_StatusAndPassiveKeys.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 31 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`SpawnEachTurn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawneachturn) | Object  | Specifies an object that spawns on a random adjacent tile each turn, with optional chance. | 22 | `{ . . . }` |
| [`ChanceToBreakFree`](./Engine_StatusAndPassiveKeys.md#object-chancetobreakfree) | Object  | Defines the chance and ability used for a grappled or restrained unit to break free. | 11 | `{ . . . }` |
| [`DoScreenShake`](./Engine_StatusAndPassiveKeys.md#object-doscreenshake) | Integer / Object  | If an integer, the number of screen shakes; if an object, defines the duration and intensity of the screen shake. | 12 | `{ . . . }`<br>`1` |
| [`EliteFlatTint`](../Reference_and_Meta/Arrays.md#array-eliteflattint) | Array | An RGB or RGBA tint multiplier applied uniformly to an elite unit's sprite. | 11 | `[.05 .05 .05 .75]`<br>`[.6 1 1]`<br>`[1.1 1.1 1.1]` |
| [`Food`](../World_Maps_and_Events/Shops.md#object-food) | Integer / Object  | The number of food pickups spawned. | 35 | `{ . . . }`<br>`20` |
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. | 16 | `1` |
| [`BoostWeaponDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-boostweapondamage) | Object  | The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields. | 9 | `{ . . . }` |
| [`BrambleRandomTileEvent`](./Engine_StatusAndPassiveKeys.md#object-bramblerandomtileevent) | Object  | An object defining the BrambleRandomTileEvent ability or effect. | 12 | `{ . . . }` |
| `CoinPickup` | Integer | The amount of coins awarded when this pickup is collected. | 10 | `1`<br>`10`<br>`2` |
| `ExtraMovePoints` | Integer | The number of additional movement points granted to this unit. | 10 | `1` |
| `FadeInsteadOfDie` | Integer | If non-zero, the unit fades out instead of dying. | 10 | `1` |
| [`GainCoins`](../Reference_and_Meta/Arrays.md#array-gaincoins) | Array / Integer | The amount of coins gained, or a [min, max] range. | 10 | `-5`<br>`1`<br>`2` |
| `KnockbackDamageImmuneUntilSettled` | Integer | If non-zero, makes the target immune to damage from knockback until they stop moving. | 10 | `1` |
| `PartialPurge` | Integer | The amount of beneficial status effects removed from the target. | 10 | `1` |
| [`PassiveAtStatThreshold`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveatstatthreshold) | Object  | An object defining passives granted when a unit's stat meets a specified threshold. | 13 | `{ . . . }` |
| [`Quivered`](../Reference_and_Meta/Arrays.md#array-quivered) | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 36 | `1`<br>`2`<br>`5` |
| `RandomPermanentStat` | Integer | The amount of a random permanent stat change (positive or negative). | 11 | `-1`<br>`-2`<br>`-3` |
| [`ReplaceBasicMove`](../Reference_and_Meta/Enums.md#enum-replacebasicmove) | Enum | Specifies an alternative movement ability that replaces the unit's default move. | 17 | `BasicDashAttackMove`<br>`BasicJump`<br>`BellyFlop_BasicMove` |
| [`SpawnOnBattleStartRandomEmptyTile`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnonbattlestartrandomemptytile) | Object  | Specifies an object that spawns on a random empty tile at the start of battle. | 11 | `{ . . . }` |
| [`StatusOnCrit`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusoncrit) | Object  | An object containing statuses applied to the unit when it lands a critical hit. | 8 | `{ . . . }` |
| `StripStatuses` | Integer | If 1, removes all status effects from the unit at the beginning of its turn. | 10 | `1` |
| `WaterWalk` | Integer | If greater than 0, allows the unit to traverse water tiles as if they were ground. | 21 | `1` |
| `Ammo` | Integer | The amount of ammo to add or remove (negative values subtract). | 15 | `-1`<br>`-99999`<br>`1` |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| `Creep` | Variable | A variable representing the Creep element or material type. | 17 ||
| `DeferVaporize` | Integer | If set to 1, the unit's vaporize (instant death) is delayed until the end of the current action. | 9 | `1` |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. | 12 | `1`<br>`2`<br>`3` |
| [`FormChangeOnElementInfluence`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-formchangeonelementinfluence) | Object  | Defines the element that triggers a form change, optional visual effects, and the target form. | 9 | `{ . . . }` |
| `Plant` | Integer | If set to 1, marks the unit as a Plant type, granting associated immunities and interactions. | 9 | `1` |
| `RandomMutation` | Integer | The number of random mutations to apply. | 13 | `1`<br>`3` |
| [`Rot`](../Reference_and_Meta/Arrays.md#array-rot) | Array / Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 20 | `-999999`<br>`1`<br>`2` |
| [`SmallRockBehavior`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-smallrockbehavior) | Integer / Object  | Defines the damage, knockback, and chain properties of small rocks spawned from this unit when destroyed. | 9 | `{ . . . }`<br>`0`<br>`5` |
| `SpawnCreep` | Integer | If set to 1, spawns a creep tile under the target. | 9 | `1` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 24 | `1`<br>`3` |
| [`StatusCollector`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuscollector) | Object  | Specifies the status effects and their stack counts that the unit collects to trigger transformations. | 9 | `{ . . . }` |
| [`TransformInXTurns`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-transforminxturns) | Object  | Defines a delayed transformation after a set number of turns, with optional target object and initiative handling. | 11 | `{ . . . }` |
| [`TransformOnElementInfluence`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-transformonelementinfluence) | Object  | Defines the element that triggers a transformation and the object to transform into. | 9 | `{ . . . }` |
| `AddKnockbackDamage` | Integer | The amount of additional knockback damage applied. | 8 | `1`<br>`2`<br>`3` |
| `AddLevelUpRerolls` | Integer | The number of additional rerolls the unit gets when leveling up. | 14 | `1`<br>`2`<br>`3` |
| [`AddStatusToWeapons`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoweapons) | Object  | Specifies status effects to add to the unit's weapon attacks, with their stack counts. | 8 | `{ . . . }` |
| `AlphaTurns` | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 13 | `-1`<br>`1` |
| [`AmplifyStatus`](../Reference_and_Meta/Enums.md#enum-amplifystatus) | Enum | Specifies the status effect to amplify, or an object with the status and number of stacks to add. | 12 | `Bleed`<br>`Burn`<br>`Poison` |
| [`BasicMagicMissile`](./Engine_StatusAndPassiveKeys.md#object-basicmagicmissile) | Object  | Directs a basic magic missile projectile at the target. | 6 | `{ . . . }` |
| [`BlacklistPickupType`](../Reference_and_Meta/Enums.md#enum-blacklistpickuptype) | Enum | Specifies a pickup type (e.g., food, catnip) that the unit will refuse to pick up. | 5 | `catnip`<br>`food` |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 23 | `1`<br>`2`<br>`3` |
| [`CharmedFly`](./Engine_StatusAndPassiveKeys.md#object-charmedfly) | Object  | Transforms the unit into a charmed fly that fights for the allies faction. | 17 | `{ . . . }` |
| [`DisableAbilitiesWithTag`](../Reference_and_Meta/Enums.md#enum-disableabilitieswithtag) | Enum | Specifies a tag that disables any ability with that tag on the unit. | 5 | `consumable`<br>`meat`<br>`musical` |
| `ExtraWeaponAttacks` | Integer | The number of additional weapon attacks the unit can perform. | 10 | `1`<br>`2` |
| `ForceSpecificInjury` | Enum | Forces the unit to receive an injury to the specified stat. | 8 | `cha`<br>`int`<br>`lck` |
| [`FormChangeOffMap`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-formchangeoffmap) | Object  | Specifies the unit's form when off the map and when on the map. | 8 | `{ . . . }` |
| [`Grappled`](../Reference_and_Meta/Arrays.md#array-grappled) | Array / Integer | The number of stacks and probability of applying the Grappled status, in format [stacks, probability] or just stacks. | 9 | `1`<br>`[1, .50]`<br>`[1, .75]` |
| [`InnateElement`](../Reference_and_Meta/Enums.md#enum-innateelement) | Enum | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 18 | `Earth`<br>`Electric`<br>`Fire` |
| `Lucky` | Enum | Indicates the unit's luck modifier or classification. | 18 ||
| [`ManaCostReductionTagged`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-manacostreductiontagged) | Object  | Reduces the mana cost of abilities with the specified tag by the given reduction amount. | 6 | `{ . . . }` |
| `NonStackingDivineShield` | Integer | The number of Divine Shield stacks that do not stack with duplicates. | 10 | `1` |
| `NonStackingShield` | Integer | The amount of non-stacking shield granted. | 16 | `12`<br>`16`<br>`3` |
| [`PassiveIfAllArmorEmpty`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveifallarmorempty) | Object  | Grants the contained passive effects when no armor is equipped in any slot. | 8 | `{ . . . }` |
| [`PassiveIfEmptyFace`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveifemptyface) | Object  | Grants the contained passive effects when the face armor slot is empty. | 7 | `{ . . . }` |
| [`PassiveIfEmptyHead`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveifemptyhead) | Object  | Grants the contained passive effects when the head armor slot is empty. | 7 | `{ . . . }` |
| [`PassiveIfEmptyNeck`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveifemptyneck) | Object  | Grants the contained passive effects when the neck armor slot is empty. | 7 | `{ . . . }` |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 203 | `1`<br>`10`<br>`2` |
| [`RandomizeAIWeightsEachTurn`](../Reference_and_Meta/Arrays.md#array-randomizeaiweightseachturn) | Array | The range of random weights applied to AI actions each turn. | 8 | `[` |
| [`RandomStatusFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 35 | `{ . . . }` |
| [`ReplaceBasicAttack`](../Reference_and_Meta/Enums.md#enum-replacebasicattack) | Enum | Specifies the ability ID that replaces the unit's basic attack. | 25 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`StatusAlliesOnDeath`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusalliesondeath) | Object  | Applies the contained status effects to all allies when the unit dies. | 8 | `{ . . . }` |
| [`StatusEachRoundBegin`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachroundbegin) | Object  | Applies the contained status effects at the beginning of each round. | 8 | `{ . . . }` |
| [`StatusEveryXSpellCasts`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseveryxspellcasts) | Object  | An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts. | 8 | `{ . . . }` |
| [`StatusOnCastSpell`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusoncastspell) | Object  | An object listing status effects applied to the unit whenever it casts a spell. | 8 | `{ . . . }` |
| [`StatusOnUseAbilityWithTag`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonuseabilitywithtag) | Object  | Applies the contained status effects when the unit uses an ability with the specified tag. | 7 | `{ . . . }` |
| `AbilityEnabledOncePerFightAtHealthThreshold` | Integer | The health threshold (absolute or percentage) at which this ability becomes enabled once per fight. | 7 | `16`<br>`25%`<br>`50%` |
| [`AbilityWhenBuddyDies`](../Reference_and_Meta/Enums.md#enum-abilitywhenbuddydies) | Enum | Specifies the ability to cast when a nearby allied unit dies. | 7 | `BoyDinoCry`<br>`ChubsRage`<br>`GirlDinoCry` |
| `BramblesOnHit` | Integer | If set to 1, spawns bramble tiles on the target's location on hit. | 7 | `1` |
| [`BrittleDuringElement`](../Reference_and_Meta/Enums.md#enum-brittleduringelement) | Enum | Makes the unit brittle while in contact with the specified element. | 8 | `water` |
| [`ChanceToSpitOnDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-chancetospitondamage) | Object  | Configures the chance to use a spit ability when taking damage, including base chance and per-damage bonus. | 7 | `{ . . . }` |
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. | 16 | `-1`<br>`-2`<br>`1` |
| `ContextualHeal` | Integer | The amount of healing applied contextually (e.g., to allies). | 7 | `1` |
| [`DamageNeighborsOnEndMove`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-damageneighborsonendmove) | Object  | Deals damage and knockback to units on neighboring tiles when the unit finishes moving. | 7 | `{ . . . }` |
| [`DurabilityTransform`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-durabilitytransform) | Object  | Transforms the item into another when durability reaches specified thresholds. | 7 | `{ . . . }` |
| [`GainCoinsRange`](./Engine_StatusAndPassiveKeys.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 11 | `{ . . . }` |
| [`Ice`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-ice) | Object  | Applies the Slow status effect to targets hit by ice-element abilities. | 61 | `{ . . . }` |
| `ManaSteal` | Integer | The amount of mana stolen (negative values may drain instead). | 7 | `-1`<br>`5` |
| `MinimumKnockbackFromAllDamage` | Integer | The minimum knockback distance the unit will suffer from any damage source. | 7 | `1` |
| [`OverrideBasicAttack`](../Reference_and_Meta/Enums.md#enum-overridebasicattack) | Enum | Replaces the unit's basic attack with the specified ability. | 7 | `BasicExplosiveShot`<br>`BasicMelee`<br>`BasicMetronome` |
| `OverrideMaxHealth` | Integer | Replaces the unit's maximum health with this value. | 7 | `1`<br>`25` |
| [`PassiveIfStrAuxEquals`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveifstrauxequals) | Object  | Grants the contained passive effects when the unit's specified auxiliary stat equals the given value. | 7 | `{ . . . }` |
| [`PassiveWhenOnTile`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhenontile) | Object  | Grants the contained passive effects while the unit is standing on one of the specified tile types. | 7 | `{ . . . }` |
| [`SetFragileImmune`](../Assets_and_Localization/Strings.md#string-setfragileimmune) | String | Sets the unit's material to the specified type, granting immunity to the Fragile status. | 7 | `""`<br>`Bionic`<br>`Cardboard` |
| [`TriggerWerewolfTransform`](../Reference_and_Meta/Arrays.md#array-triggerwerewolftransform) | Array / Float | The number of stacks and probability of triggering the werewolf transformation. | 7 | `.5`<br>`[1 .15]`<br>`[1 .20]` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 19 | `1`<br>`2`<br>`[1 .1]` |
| `XIsFreeArmorSlots` | Integer | The number of armor slots that are free (no cost) for the unit. | 7 | `1` |
| `AbilityEnabledPercentEachTurn` | Integer | The percentage chance each turn that this ability is enabled. | 6 | `25%`<br>`33%`<br>`35%` |
| [`AbilityOnBattleStart`](../Reference_and_Meta/Enums.md#enum-abilityonbattlestart) | Enum | Casts the specified ability when the battle begins. | 15 | `Flush`<br>`Heathens`<br>`Heathens2` |
| `AddDamage` | Integer | The amount of damage added to all attacks. Negative values reduce damage. | 8 | `-1`<br>`1`<br>`2` |
| [`AddDamageToElementDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-adddamagetoelementdamage) | Object  | Defines additional damage of a specific element added to the unit's attacks. | 9 | `{ . . . }` |
| `AddMovement` | Integer | The amount of bonus movement points added to the unit's base movement. | 25 | `-1`<br>`-2`<br>`1` |
| [`AddStatusToElementAbilities`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoelementabilities) | Object  | Adds the contained status effects to all abilities with the specified element. | 6 | `{ . . . }` |
| [`AddTemporaryEffectsToBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addtemporaryeffectstobasicattack) | Object  | A container object that lists temporary status effects applied to the unit's basic attack. | 7 | `{ . . . }` |
| [`animation_suffix`](../Reference_and_Meta/Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 89 | `""`<br>`"0"`<br>`"1"` |
| `BackstabImmunity` | Integer | If greater than 0, prevents the unit from taking extra damage from backstabs. | 12 | `1` |
| `BasicAttackAOEBonus` | Integer | The additional area of effect radius for the basic attack. | 5 | `1`<br>`2` |
| `BasicAttackDamageMultiplier` | Float | A multiplier applied to the damage of the basic attack. | 6 | `0`<br>`33.333334%`<br>`50%` |
| [`Bird`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bird) | Enum / Object  | The object dropped by this bird unit upon death. | 11 | `{ . . . }`<br>`CookedChickenLeg` |
| `BlastResistance` | Integer | The amount of damage reduction against blast-type damage. | 8 | `2`<br>`3`<br>`4` |
| [`BounceRock`](../Reference_and_Meta/Arrays.md#array-bouncerock) | Array / Enum  | Specifies the rock object to bounce. | 6 | `LavaBoulder`<br>`SmallLavaRock`<br>`SmallRock` |
| [`CaveFamilyEnrage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-cavefamilyenrage) | Object  | Specifies the ability used when the number of family members with a given tag falls below a threshold. | 6 | `{ . . . }` |
| `ClearStarving` | Integer | The number of stacks of Starving cleared. | 6 | `1` |
| [`Conditional_BadRoll`](./Engine_StatusAndPassiveKeys.md#object-conditional_badroll) | Object  | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 8 | `{ . . . }` |
| [`CureDisease`](./Engine_StatusAndPassiveKeys.md#object-curedisease) | Object  | Attempts to cure the specified disease with the given chance. | 6 | `{ . . . }` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 113 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`DefaultMove`](./Engine_StatusAndPassiveKeys.md#object-defaultmove) | Object  | Defines the default movement ability for the unit. | 326 | `{ . . . }` |
| [`DelayedAutoRevive`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-delayedautorevive) | Object  | Configures an automatic revival after a delay, with specified rounds and health percentage. | 6 | `{ . . . }` |
| [`Divide4OnDeath`](../Reference_and_Meta/Enums.md#enum-divide4ondeath) | Enum | The object that spawns in four instances upon this unit's death. | 6 | `BiggestFood`<br>`Clot`<br>`MedSlime` |
| [`DoDistortionRing`](./Engine_StatusAndPassiveKeys.md#object-dodistortionring) | Object  | Configuration for a distortion ring visual effect, with speed, intensity, and radius. | 6 | `{ . . . }` |
| [`Electric`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-electric) | Object  | Applies a Stun status effect with specified stacks and probability based on variable X. | 78 | `{ . . . }` |
| `ExtraBasicAttacks` | Integer | The number of additional basic attacks the unit can perform per turn. | 15 | `1`<br>`2` |
| [`Fire`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-fire) | Integer / Object  | Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack. | 168 | `{ . . . }`<br>`1` |
| [`FormChangeWhilePrimingAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-formchangewhileprimingability) | Object  | Defines the form changes when a specific ability is being primed and when it is not. | 6 | `{ . . . }` |
| `Fragile` | Integer | The number of stacks of the Fragile status, causing increased damage taken. | 24 | `1` |
| `FreeFirstCast` | Integer | The number of free casts of this ability per battle. | 6 | `1`<br>`4` |
| [`FreePathfindElement`](../Reference_and_Meta/Enums.md#enum-freepathfindelement) | Enum | Specifies a terrain element (e.g., Water, Grass) that the unit can pathfind through without penalty. | 8 | `Grass`<br>`Water` |
| [`Hyde`](./Engine_StatusAndPassiveKeys.md#object-hyde) | Object  | Defines the properties of the Hyde transformation effect. | 10 | `{ . . . }` |
| [`ItemAuxTransform`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-itemauxtransform) | Object  | Transforms the item into another when its auxiliary value reaches specified thresholds. | 6 | `{ . . . }` |
| `KaijuKnockbackImmune` | Integer | If 1, the unit is immune to knockback from kaiju sources. | 6 | `1` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 41 | `1`<br>`2`<br>`3` |
| `KnockbackImmunity` | Integer | If set to 1, the unit cannot be knocked back. | 11 | `1` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 22 | `1`<br>`2`<br>`[1, 0.1]` |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 32 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`PassiveWhenAtFullMana`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhenatfullmana) | Object  | An object listing passive effects that are active only while the unit's mana is full. | 5 | `{ . . . }` |
| `PermanentConstitution` | Integer | The amount of permanent Constitution stat added or removed. | 11 | `-1`<br>`-2`<br>`1` |
| `PoisonThorns` | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 15 | `1`<br>`2`<br>`3` |
| [`ReplaceBasicAttackWhenCastable`](../Reference_and_Meta/Enums.md#enum-replacebasicattackwhencastable) | Enum | Replaces the basic attack with the specified ability when that ability can be cast. | 6 | `BasicSuplex`<br>`Hone`<br>`Hone2` |
| [`ReplaceBasicMove_Mutation`](../Reference_and_Meta/Enums.md#enum-replacebasicmove_mutation) | Enum | Replaces the unit's basic movement with the specified mutation-based move. | 3 | `BasicDig`<br>`BasicJump` |
| [`ScatterCoins`](./Engine_StatusAndPassiveKeys.md#object-scattercoins) | Object  | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 8 | `{ . . . }` |
| [`ScatterHeldCoin`](../Reference_and_Meta/Arrays.md#array-scatterheldcoin) | Array / Integer | The number of coins scattered, with an optional probability as a second element. | 6 | `1`<br>`[1 .3]`<br>`[1 .5]` |
| [`SetBrittleImmune`](../Assets_and_Localization/Strings.md#string-setbrittleimmune) | String | Sets the unit's material to the specified type, granting immunity to the Brittle status. | 6 | `""`<br>`AdvancedAlloy`<br>`Alloy` |
| `SetDistanceDisplace` | Integer | The fixed distance to displace the target. | 6 | `5` |
| `ShowHiddenThings` | Integer | If nonzero, reveals hidden objects or tiles on the map. | 4 | `1` |
| [`StatusIfUnusedMovePoints`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusifunusedmovepoints) | Object  | Specifies status effects applied if the unit ends its turn with unused movement points. | 8 | `{ . . . }` |
| [`StatusKilledCharacters`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuskilledcharacters) | Object  | An object listing status effects applied to the unit when it kills a character. | 5 | `{ . . . }` |
| [`StatusOnBattleEnd`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonbattleend) | Object  | An object containing status effects or passives applied to the unit when the battle ends. | 53 | `{ . . . }` |
| [`StatusOnEndMove`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonendmove) | Object  | Specifies status effects or actions triggered when the unit finishes moving. | 10 | `{ . . . }` |
| [`StatusOnStanceSwitch`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonstanceswitch) | Object  | Applies the contained status effects when the unit changes stances. | 14 | `{ . . . }` |
| [`StatusOnTookDamageFromAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusontookdamagefromability) | Object  | Specifies status effects triggered when the unit takes damage specifically from an ability (not environmental). | 9 | `{ . . . }` |
| [`StunImmunity`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stunimmunity) | Integer / Object  | If 1, the unit is immune to stun. The optional object configures whether to cleanse stun on apply. | 6 | `{ . . . }`<br>`1` |
| [`TagGreed`](../Reference_and_Meta/Enums.md#enum-taggreed) | Enum | The tag of items that this unit will move towards to collect. | 6 | `bishop_hat`<br>`food`<br>`pickup` |
| [`TeamCastAbility`](./Engine_StatusAndPassiveKeys.md#object-teamcastability) | Enum / Object  | Specifies the ability name for the team to cast, with optional tag restriction and same orientation. | 6 | `{ . . . }`<br>`Huddle_Impl`<br>`Spin`<br>`TeamFlex_Impl` |
| [`TwisterDisplaceWithDamage`](./Engine_StatusAndPassiveKeys.md#object-twisterdisplacewithdamage) | Object  | Configuration for a twister displacement that deals damage, with min/max distance and damage value. | 6 | `{ . . . }` |
| `YOffset` | Float | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 11 | `-.18`<br>`.25`<br>`.35` |
| `ally_chance` | Integer | The percentage chance for an ally to catch incoming projectiles. | 5 | `100%`<br>`15%` |
| `Angel` | Integer | If 1, the unit is an angel type, which may affect behavior like reviving. | 7 | `1` |
| [`ChangeTilesUnder`](../Reference_and_Meta/Enums.md#enum-changetilesunder) | Enum | The tile type to change the ground tiles under the target to. | 9 | `DirtTile`<br>`GlassTile`<br>`LavaTile` |
| [`CollectsPickupsWithAltEffects`](./Engine_StatusAndPassiveKeys.md#object-collectspickupswithalteffects) | Object  | Contains alternative effects that are applied when collecting pickups. | 5 | `{ . . . }` |
| `DamageOrHealConditionally` | Integer | The amount of conditional damage or healing applied, based on certain conditions (e.g., ally or enemy). | 8 | `1` |
| `fetus` | Variable | A variable used in status effect calculations; specific usage depends on context. | 14 ||
| [`FlySwarm`](./Engine_StatusAndPassiveKeys.md#object-flyswarm) | Object  | Summons a fly swarm with the given chance or intensity percentage. | 11 | `{ . . . }` |
| [`FlySwarm`](./Engine_StatusAndPassiveKeys.md#object-flyswarm) | Object  | Summons a fly swarm with the given chance or intensity percentage. | 11 | `{ . . . }` |
| `HeadArmorPassiveMultiplierBonus` | Integer | A multiplier bonus applied to passive effects granted by head armor. | 5 | `1`<br>`2` |
| `HitExplosion` | Integer | The radius of the explosion triggered on hit. | 7 | `10`<br>`5`<br>`X` |
| [`KnockbackDirectionIsFacingDirection`](../Reference_and_Meta/Enums.md#enum-knockbackdirectionisfacingdirection) | Enum / Integer  | Specifies how to alter knockback direction relative to the unit's facing: 1 (same), flip (opposite), rotate_right. | 5 | `1`<br>`flip`<br>`rotate_right` |
| `MonkStanceSwitch` | Integer | The number of times to switch monk stance. | 5 | `1` |
| [`MoveTowardsKillers`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-movetowardskillers) | Enum / Object  | Determines the movement behavior when moving towards units that have killed an ally. | 5 | `{ . . . }`<br>`ReaperRevenge` |
| `NoHealthRegen` | Number | Prevents the unit from regenerating health normally. | 7 | `1` |
| [`ObjectOnHit`](./Engine_StatusAndPassiveKeys.md#object-objectonhit) | Enum / Object  | Specifies the object to spawn on the hit tile. | 7 | `{ . . . }`<br>`Bait`<br>`BiggestFood`<br>`Carcus` |
| [`ObjectOnHitEmpty`](../Reference_and_Meta/Enums.md#enum-objectonhitempty) | Enum | Specifies the object to spawn on hitting an empty cell. | 5 | `AnimalEgg`<br>`AnimalEgg2`<br>`HeadTumor` |
| `RefreshMovePointsIfHit` | Integer | The amount of movement points restored on hit. | 5 | `1` |
| `RepairTrinket` | Integer | The number of stacks of the Repair Trinket status effect to apply. | 6 | `1`<br>`99` |
| `SharkySmellsBlood` | Integer | If 1, the unit is attracted to damaged units and may prioritize them. | 5 | `1` |
| [`SpawnCoinAnywhere`](../Reference_and_Meta/Arrays.md#array-spawncoinanywhere) | Array / Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 7 | `1`<br>`[1 .5]` |
| [`SpawnRock`](../Reference_and_Meta/Arrays.md#array-spawnrock) | Array / Integer | The number of rocks to spawn, or an array with stacks and probability. | 5 | `1`<br>`[1, .20]` |
| `StartOffMap` | Integer | If 1, the unit begins the encounter off the map. | 5 | `1` |
| [`StatusGroup`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusgroup) | Object  | A container grouping multiple status effects to be applied simultaneously. | 6 | `{ . . . }` |
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonturnendifdidntcastabilitytypes) | Object  | Applies the contained status effects at turn end if the unit did not cast an ability of the specified type(s). | 5 | `{ . . . }` |
| [`Tangled`](./Engine_StatusAndPassiveKeys.md#object-tangled) | Array / Integer / Object  | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 10 | `{ . . . }`<br>`1`<br>`2`<br>`[1, .05]` |
| [`TransformItemOnElementInfluence`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-transformitemonelementinfluence) | Object  | Transforms the item into the specified one when influenced by the given element, optionally fully repairing it. | 5 | `{ . . . }` |
| [`TransformOnDeathImmediately`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-transformondeathimmediately) | Enum / Object  | The object to transform into immediately upon death, with optional turn handling. | 5 | `{ . . . }`<br>`NoHead` |
| `UpgradeRandomAbility` | Integer | The number of random abilities upgraded upon effect. | 5 | `1` |
| `water` | Variable | A variable representing water element intensity or presence. | 41 ||
| [`Water`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-water) | Object  | Form state for water element, applying a puddle or movement bonus. | 71 | `{ . . . }` |
| [`XIsLivingAlliesWithTag`](../Reference_and_Meta/Enums.md#enum-xislivingallieswithtag) | Enum | Specifies the tag that living allies must have for this passive to affect them. | 5 | `dc_crow`<br>`hitler_clone_fetus`<br>`terminator_mini` |
| [`AbilityAfterEnemyCastSpell_Stackable`](../Reference_and_Meta/Enums.md#enum-abilityafterenemycastspell_stackable) | Enum | The ability to cast after an enemy spell, which can stack in effect. | 4 | `ThornUp`<br>`ThornUpX` |
| [`AbilityReaction`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-abilityreaction) | Enum / Object  | Specifies the ability used as a reaction when the unit is targeted by an ability. | 25 | `{ . . . }`<br>`AnkyloSpin`<br>`GSOpen`<br>`Gassy_AssBlast` |
| [`AbilityWhenTaggedCharacterMovesNear`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-abilitywhentaggedcharactermovesnear) | Object  | An object containing `ability`, `tag`, and `range` that triggers the specified ability when a character with the given tag moves within range. | 5 | `{ . . . }` |
| `AddDamageToBasicAttack` | String | Additional damage added to the basic attack, either as a flat value or formula. | 5 | `1`<br>`2`<br>`4` |
| `AddManaRegen` | Integer | The flat amount of mana regenerated per turn. | 16 | `1`<br>`2`<br>`3` |
| `AddMeleeKnockback` | Integer | The amount of additional knockback dealt by melee attacks. | 4 | `1`<br>`10`<br>`2` |
| [`AddPassivesToCharmed`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addpassivestocharmed) | Object  | Grants the contained passive effects to units under the charm status. | 5 | `{ . . . }` |
| [`AddSelfStatusToBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addselfstatustobasicattack) | Object  | Applies the contained status effects to the unit when it uses its basic attack. | 11 | `{ . . . }` |
| `AddSpeed` | Integer | The amount of speed added (or subtracted) to the unit. | 6 | `-3`<br>`4`<br>`6` |
| [`AddStatusToAllDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoalldamage) | Object  | Adds the contained status effects to all damage dealt by the unit. | 13 | `{ . . . }` |
| [`AddStatusToAllDamageAbilities`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoalldamageabilities) | Object  | Adds the contained status effects to all damaging abilities (spells and attacks). | 2 | `{ . . . }` |
| [`AddStatusToElementDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoelementdamage) | Object  | An object that applies a specific status effect when dealing damage of a specified element. Contains sub-keys for the element and the status to apply. | 6 | `{ . . . }` |
| `AllyDamageReduction` | Integer | The amount by which damage dealt to allies is reduced. | 4 | `0` |
| [`AllyManaRegenAura`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-allymanaregenaura) | Object  | An object granting a mana regeneration aura to allies, with sub-keys for stacks and range. | 4 | `{ . . . }` |
| `AmplifyKnockback` | Integer | The additional distance (in tiles) a unit is knocked back. | 5 | `10`<br>`2` |
| `any` | Variable | A wildcard key that matches any property name, often used for generic or dynamic lookups. | 19 ||
| `AOEPuddle` | Enum | Specifies the pattern or shape of an area-of-effect puddle left on the ground. | 2 | `X-1` |
| [`ApplyToConsumed`](./Engine_StatusAndPassiveKeys.md#object-applytoconsumed) | Object  | Container for effects that are applied to the consumed object. | 4 | `{ . . . }` |
| [`ArcLightning`](./Engine_StatusAndPassiveKeys.md#object-arclightning) | Object  | Configuration for arc lightning chain, with stacks, chance, max distance, and enemy-only flag. | 4 | `{ . . . }` |
| [`AutocastEachRound`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-autocasteachround) | Enum / Object  | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 10 | `{ . . . }`<br>`SpiderReturn` |
| `BackstabAllDirections` | Integer | If 1, the unit deals backstab damage from all directions. | 4 | `1` |
| [`BaitAura`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-baitaura) | Object  | The range of the bait aura that draws enemies towards the unit. | 4 | `{ . . . }` |
| [`BasicStraightShot`](./Engine_StatusAndPassiveKeys.md#object-basicstraightshot) | Object  | An object defining a basic attack that fires a projectile in a straight line. | 6 | `{ . . . }` |
| [`BasicTankMelee`](./Engine_StatusAndPassiveKeys.md#object-basictankmelee) | Object  | An object defining a basic melee attack for a tank-type unit. | 10 | `{ . . . }` |
| [`BeefyCharmedLeech`](./Engine_StatusAndPassiveKeys.md#object-beefycharmedleech) | Object  | An object defining a variant of the Maggot familiar, specifically a charmed, larger leech. | 12 | `{ . . . }` |
| `BreakAtAux` | Integer | The number of auxiliary item uses before this item breaks. | 4 | `0` |
| [`BuffImmunity`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-buffimmunity) | Integer / Object  | If 1, the unit is immune to buffs. An optional object can list buffs to exclude from immunity. | 4 | `{ . . . }`<br>`1` |
| `bug` | Variable | A variable key likely indicating a known issue or placeholder value. | 18 ||
| `CatchBoomerang` | Integer | If set, allows the ability to catch a boomerang, with the integer representing the number of catches. | 4 | `1` |
| [`ChanceToBackflip`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-chancetobackflip) | Object  | An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit. | 6 | `{ . . . }` |
| [`ChangeTileOnPop`](../Reference_and_Meta/Enums.md#enum-changetileonpop) | Enum | The type of tile that appears when this unit is destroyed. | 4 | `CreepTile`<br>`GlitchTile`<br>`OilTile` |
| [`CharmedTinySpider`](./Engine_StatusAndPassiveKeys.md#object-charmedtinyspider) | Object  | An object defining a charmed variant of the TinySpider familiar. | 16 | `{ . . . }` |
| [`ClassManaCostReduction`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-classmanacostreduction) | Object  | Defines a reduction in mana cost for abilities of a specific class. | 7 | `{ . . . }` |
| [`CobraReflex`](../Reference_and_Meta/Enums.md#enum-cobrareflex) | Enum | Specifies which basic attack or ability grants increased dodge or counterattack chance. | 3 | `BasicMonkMelee` |
| [`Conditional_PartyMember`](./Engine_StatusAndPassiveKeys.md#object-conditional_partymember) | Object  | A conditional block that executes its child actions only if the target is a party member. | 6 | `{ . . . }` |
| `ConsumablesInfiniteRange` | Integer | If non-zero, consumable items can be used at any range without distance restrictions. | 3 | `1` |
| `CopyBasicAttackEffects` | Integer | If set, the ability copies the effects from the unit's basic attack. | 4 | `1` |
| `CountAsCorpse` | Integer | If 1, the unit counts as a corpse for interactions like raising or necromancy. | 4 | `1` |
| [`CounterAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-counterattack) | Array / Enum / Object  | Specifies the ability used when the unit counterattacks after being hit. | 39 | `{ . . . }`<br>`BungaSwipe`<br>`CloakerHex`<br>`CollectiveCounter` |
| `CreepTile` | Variable | A variable key referencing a tile type that applies a creep or detrimental effect. | 8 ||
| `crow` | Variable | A variable key likely representing a unit or effect related to the crow faction. | 6 ||
| [`DisableAbilities`](../Reference_and_Meta/Enums.md#enum-disableabilities) | Enum | Specifies which category of abilities to disable, such as 'all_items' or 'basic_attack'. | 4 | `all_items`<br>`all_spells`<br>`basic_attack` |
| [`DisplayDangerAOE`](../Reference_and_Meta/Enums.md#enum-displaydangeraoe) | Enum | The ability whose area of effect is displayed to warn players. | 4 | `GrenadeExplode`<br>`MoonHead_Blow`<br>`TheChild_Wrath` |
| [`DistanceBonusDamage`](./Engine_StatusAndPassiveKeys.md#object-distancebonusdamage) | Object  | An object that adds bonus damage based on the distance from the target, with sub-keys for stacks and minimum range. | 4 | `{ . . . }` |
| `DownRankAIIfWeaponUsable` | Float | A multiplier that reduces the AI's priority to use this ability if the unit has a usable weapon. | 4 | `.001` |
| [`ElementalManaCostReduction`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-elementalmanacostreduction) | Object  | An object that reduces the mana cost of spells of specified elements, with sub-keys for element and reduction amount. | 5 | `{ . . . }` |
| [`EnableWeather`](../Reference_and_Meta/Enums.md#enum-enableweather) | Enum | Specifies the weather effect to enable. | 4 | `KaijuFirestorm`<br>`KaijuMeteornado`<br>`KaijuMeteornadoSolo` |
| `equal` | Variable | A variable key used in conditional comparisons to check equality. | 4 ||
| [`EquipRandomTemporaryItemFromPool`](../Reference_and_Meta/Enums.md#enum-equiprandomtemporaryitemfrompool) | Enum | Specifies the item pool (e.g., 'pills' or 'weapons') from which a random temporary item is equipped. | 2 | `pills`<br>`weapons` |
| `ExplosionIfHitSomething` | Integer | The radius of explosion triggered if the attack hits an entity. | 4 | `5` |
| [`extra_statuses`](../Reference_and_Meta/Miscellaneous.md#object-extra_statuses) | Object  | An object containing additional status effects (with stack counts) applied to the consumed unit. | 4 | `{ . . . }` |
| `ExtraDispersedTurns` | Integer | The number of additional or fewer turns in the dispersed turn order. | 5 | `-1`<br>`1` |
| `FaceArmorPassiveMultiplierBonus` | Integer | A multiplier bonus applied to the effects of face armor passives. | 4 | `1`<br>`2` |
| [`FactionUprising`](../Reference_and_Meta/Enums.md#enum-factionuprising) | Enum | Specifies which faction triggers a global uprising event, adding allied units of that faction. | 4 | `alien`<br>`ghost`<br>`robot` |
| `Fights` | Number | The number of fights this status or effect persists for. | 10 | `1`<br>`3`<br>`99` |
| [`FragileDuringElement`](../Reference_and_Meta/Enums.md#enum-fragileduringelement) | Enum | Specifies an element during which the unit becomes fragile, taking increased damage. | 5 | `water` |
| `FreezePiercing` | Integer | The number of stacks of freeze resistance that are ignored when applying freeze. | 6 | `1` |
| `GrassTile` | Number | The numerical identifier for a grass-type tile. | 5 | `15`<br>`80` |
| [`GroundFlopper`](../Reference_and_Meta/Enums.md#enum-groundflopper) | Enum | The movement ability used when this unit is on the ground. | 4 | `DefaultMove`<br>`MoveOne` |
| `HouseFoodRequirementMultiplier` | Integer | A multiplier for the amount of food the house requires; 0 removes the food requirement. | 3 | `0` |
| `IncreaseExplosionDamage` | Integer | The flat amount by which explosion damage is increased. | 10 | `1`<br>`2`<br>`3` |
| [`LateStatusApplication`](./Engine_StatusAndPassiveKeys.md#object-latestatusapplication) | Object  | Container for status effects that are applied late after the main effect. | 4 | `{ . . . }` |
| [`LevelUpClassOverride`](../Reference_and_Meta/Enums.md#enum-levelupclassoverride) | Enum | Specifies which class the unit gains upon leveling up, overriding the default class. | 6 | `Colorless`<br>`Jester` |
| [`LoopingSoundWhileAlive`](../Reference_and_Meta/Enums.md#enum-loopingsoundwhilealive) | Enum | The looping sound effect played while the unit is alive. | 4 | `BigUFO_ambient_looping`<br>`Bomb_FuseLoop`<br>`Twister_loop` |
| [`LowerAmbientLight`](../Reference_and_Meta/Miscellaneous.md#object-lowerambientlight) | Object  | If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly. | 7 | `{ . . . }` |
| [`LowerAmbientLight`](../Reference_and_Meta/Miscellaneous.md#object-lowerambientlight) | Object  | If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly. | 7 | `{ . . . }` |
| `ManaCostReduction` | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 13 | `-2`<br>`1`<br>`2` |
| [`Metronome`](./Engine_StatusAndPassiveKeys.md#object-metronome) | Integer / Object  | The number of times Metronome triggers, or an object with stacks and banned abilities. | 16 | `{ . . . }`<br>`1`<br>`2` |
| [`Metronome`](./Engine_StatusAndPassiveKeys.md#object-metronome) | Boolean (Flag) / Float / Object  | The number of times Metronome triggers, or an object with stacks and banned abilities. | 16 | `{ . . . }`<br>`1`<br>`2` |
| `musical` | Variable | A variable key likely related to musical abilities or sound effects. | 52 ||
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. | 9 | `1`<br>`9999` |
| [`PassiveAtHealthThreshold`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveathealththreshold) | Object  | An object that grants additional passives when the unit's health meets a specified threshold, with sub-keys for threshold, mode, and passives. | 9 | `{ . . . }` |
| [`PassiveWhenDead`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhendead) | Object  | Passive effects that remain active while the unit is dead. | 4 | `{ . . . }` |
| `PermanentIntelligence` | Integer | The permanent amount of intelligence added or removed. | 6 | `-1`<br>`1`<br>`2` |
| [`PoopWhenHit`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-poopwhenhit) | Object  | Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`. | 4 | `{ . . . }` |
| `PrioritizeFarAwayTargets` | Integer | The weight for AI to prioritize targets based on distance; higher values favor farther targets. | 4 | `1`<br>`10` |
| [`RandomPassivePool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-randompassivepool) | Object  | A pool of random passives from which one is chosen for this unit. | 4 | `{ . . . }` |
| [`RandomSeededStatModifier`](../Reference_and_Meta/Arrays.md#array-randomseededstatmodifier) | Array | An array defining a random, seeded modifier to stats, typically in the format [modifier, offset]. | 4 | `[2 -1]` |
| [`ReflectProjectiles`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-reflectprojectiles) | Integer / Object  | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 15 | `{ . . . }`<br>`1`<br>`10%`<br>`100%` |
| `RemoveActPoints` | Integer | The number of action points removed from the target. | 4 | `1` |
| [`RepairWeapon`](../Reference_and_Meta/Arrays.md#array-repairweapon) | Array / Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 7 | `1`<br>`6`<br>`99` |
| [`ReplaceSpell`](./Engine_StatusAndPassiveKeys.md#object-replacespell) | Object  | Defines which spell slot to replace and with which ability. | 4 | `{ . . . }` |
| `SendRock` | Integer | The number of rocks to send as projectiles. | 4 | `1` |
| `SizeScale` | Float | The multiplier applied to the unit's visual and hitbox size. | 20 | `.4`<br>`.6`<br>`.7` |
| [`SmartMetronome`](./Engine_StatusAndPassiveKeys.md#object-smartmetronome) | Integer / Object  | The number of stacks of a buff that increases damage by a percentage, with an optional upgrade flag. | 8 | `{ . . . }`<br>`20` |
| [`SmartMetronome`](./Engine_StatusAndPassiveKeys.md#object-smartmetronome) | Integer / Object  | The number of stacks of a buff that increases damage by a percentage, with an optional upgrade flag. | 8 | `{ . . . }`<br>`20` |
| [`SpawnCatCopyOnBattleStart`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawncatcopyonbattlestart) | Object  | An object that spawns a copy of the unit's cat at the start of battle, with sub-keys for the copy object and chain-prevention tag. | 4 | `{ . . . }` |
| [`SpawnThingOnDeath`](../Reference_and_Meta/Enums.md#enum-spawnthingondeath) | Enum | Specifies the name of an object to spawn upon death. | 16 | `Boulder`<br>`CharmedDemonKitten`<br>`CharmedFlySwarm` |
| [`StatusOnAllyCatDeath`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonallycatdeath) | Object  | An object listing status effects applied to the unit when an allied cat dies. | 6 | `{ . . . }` |
| [`StatusOnEatFood`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusoneatfood) | Object  | An object listing status effects applied to the unit when it eats food. | 5 | `{ . . . }` |
| [`StatusOnGainCoins`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusongaincoins) | Object  | Specifies status effects applied when this unit gains coins. | 6 | `{ . . . }` |
| [`StatusOnHealed`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonhealed) | Object  | An object that applies a status effect to the unit whenever it is healed. | 4 | `{ . . . }` |
| [`StatusOnOverHealed`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonoverhealed) | Object  | An object that applies a status effect to the unit whenever it receives overhealing (healing beyond max health). | 5 | `{ . . . }` |
| [`StatusOnTakeHealthOrShieldDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusontakehealthorshielddamage) | Object  | An object that applies a status effect when the unit takes damage to either health or shields. | 4 | `{ . . . }` |
| [`StatusOnTurnEndIfCastNSpells`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonturnendifcastnspells) | Object  | An object that applies a status effect at the end of the turn if the unit has cast a specified number of spells. | 5 | `{ . . . }` |
| [`StatusOnTurnEndIfManaExact`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonturnendifmanaexact) | Object  | An object that applies a status effect at the end of the turn if the unit's mana is exactly a specified value. | 4 | `{ . . . }` |
| [`StatusOnTurnEndIfManaOrHealthExact`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonturnendifmanaorhealthexact) | Object  | An object that applies a status effect at the end of the turn if the unit's mana or health is exactly a specified value. | 4 | `{ . . . }` |
| [`StatusRandomEnemiesOnBattleStart`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusrandomenemiesonbattlestart) | Object  | An object that applies a status effect to a random number of enemies at the start of battle, with sub-keys for count and the status. | 7 | `{ . . . }` |
| [`SwitchMusic`](./Engine_StatusAndPassiveKeys.md#object-switchmusic) | Object  | Defines a new song or layer for the background music. | 7 | `{ . . . }` |
| `TauntAlways` | Integer | If non-zero, the unit is always taunted, forcing it to target the first enemy in range. | 4 | `1` |
| [`TempPassiveWhileHasStatus`](../Reference_and_Meta/Miscellaneous.md#object-temppassivewhilehasstatus) | Object  | An object defining passives temporarily granted to the unit while it has a specific status effect. | 4 | `{ . . . }` |
| [`TileTrail`](../Reference_and_Meta/Enums.md#enum-tiletrail) | Enum | Specifies the type of tile left behind as the unit moves. | 14 | `BrambleTile`<br>`CreepTile`<br>`FireTile` |
| [`TimeDelayStatusApplication`](./Engine_StatusAndPassiveKeys.md#object-timedelaystatusapplication) | Object  | Container for status effects applied after a specified delay. | 4 | `{ . . . }` |
| [`ToadJump_BasicMove`](./Engine_StatusAndPassiveKeys.md#object-toadjump_basicmove) | Object  | An object defining a basic movement ability for a toad-like unit. | 4 | `{ . . . }` |
| [`Trapper`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-trapper) | Object  | Specifies a trap-placing ability and its targeting parameters. | 5 | `{ . . . }` |
| `UncappedMana` | Integer | If non-zero, the unit has no maximum mana limit. | 3 | `1` |
| `Vegan` | Integer | If nonzero, sets the unit as Vegan; can also be an object with localization fields and the `Disorder` class. | 8 | `1` |
| [`WeremanTransformationReceiver`](../Reference_and_Meta/Enums.md#enum-weremantransformationreceiver) | Enum | Determines which transformation animation or effect is applied when this unit is turned by a were-creature. | 4 | `CaveManTransform`<br>`CaveWomanDropTransform` |
| `AbilityEnabledOncePerRound` | Integer | If set, the ability can only be used once per round. | 3 | `1` |
| [`AbilityEnableIfConsumedCharacterHasTag`](../Reference_and_Meta/Enums.md#enum-abilityenableifconsumedcharacterhastag) | Enum | Specifies the tag that a consumed character must have for the ability to be enabled. | 3 | `sp_pill_fire`<br>`sp_pill_normal`<br>`sp_pill_tar` |
| `AbilityInheritsWeaponEffects` | Integer | If set, the ability inherits properties from the unit's weapon, with higher values indicating different inheritance modes. | 3 | `1`<br>`2` |
| `AddEndOfCombatRegen` | Integer | The amount of health regenerated after combat ends. | 3 | `12`<br>`999999` |
| `AggroTargetIsCurrentTurn` | Integer | If set to 1, the unit's aggro target is the unit currently taking its turn. | 3 | `1` |
| `AllStatsUpPerDisorder` | Integer | The amount by which all stats increase for each disorder (negative status) the unit has. | 3 | `1` |
| [`ApplyMultipleTimes`](./Engine_StatusAndPassiveKeys.md#object-applymultipletimes) | Object  | An object containing a `stacks` value that specifies how many times the nested effects are applied. | 3 | `{ . . . }` |
| `BaseStatMultiply` | Float | A multiplier applied to the unit's base stats. | 3 | `.25`<br>`.5`<br>`.666` |
| `BasicAttackCritChance` | Float | A multiplier for the critical hit chance of basic attacks, either as a float or percentage. | 3 | `.1`<br>`100%` |
| `bishop_hat` | Variable | A variable key referencing a specific item or graphical element (the bishop hat). | 5 ||
| `BoneArmorPassive` | Integer | The number of stacks of bone armor granted, which absorbs damage. | 3 | `1` |
| [`BonusTurnPattern`](../Reference_and_Meta/Arrays.md#array-bonusturnpattern) | Array | An array defining the pattern of bonus turns granted to this unit. | 3 | `[` |
| `Bounty` | Integer | The number of bounty stacks applied to enemies, increasing rewards on defeat. | 5 | `1`<br>`3` |
| [`BreakOnElement`](../Reference_and_Meta/Enums.md#enum-breakonelement) | Enum | Specifies an element that, when dealt to the unit, causes its armor or item to break. | 3 | `water` |
| [`CanMutateTo`](../Reference_and_Meta/Arrays.md#array-canmutateto) | Array / Enum  | Specifies the mutation forms this unit can transform into, either a single form or an array of possible forms. | 3 | `Hyde`<br>`[Lumpy, Leaper]`<br>`[TumorousMaggot, ChargeyMaggot, SwappyMaggot]` |
| `CantCatchDiseases` | Integer | The number of stacks that prevent the unit from contracting diseases. | 3 | `1` |
| `CantSpreadDiseases` | Integer | The number of stacks that prevent the unit from spreading diseases. | 3 | `1` |
| [`CatPartsSizeScaleStatus`](./Engine_StatusAndPassiveKeys.md#object-catpartssizescalestatus) | Object  | Configures scale multipliers for individual cat body parts (body, arms, mouth). | 3 | `{ . . . }` |
| `ChanceToBlock` | Integer | The percentage chance to block incoming damage. | 3 | `10%` |
| [`CharmedTinyTumor`](./Engine_StatusAndPassiveKeys.md#object-charmedtinytumor) | Object  | An object defining a specific variant of the TinyTumor status, typically with its own graphics scale. | 7 | `{ . . . }` |
| `CollideWithConsumed` | Equation | Damage formula for collision with consumed objects, e.g., '4+bonus_melee_damage'. | 3 | `1+bonus_melee_damage`<br>`4+bonus_melee_damage`<br>`5+bonus_melee_damage` |
| [`Conditional_Adjacent`](./Engine_StatusAndPassiveKeys.md#object-conditional_adjacent) | Object  | An object whose nested keys define statuses or effects applied to or by units that are adjacent to the unit. | 4 | `{ . . . }` |
| [`Conditional_RandomChance`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_randomchance) | Object  | An object containing effects that execute only if a random roll succeeds, with an odds value defined inside. | 4 | `{ . . . }` |
| [`Conditional_Shielded`](./Engine_StatusAndPassiveKeys.md#object-conditional_shielded) | Object  | An object containing effects that are only applied if the target has a shield active. | 5 | `{ . . . }` |
| [`CookedChickenLeg`](./Engine_StatusAndPassiveKeys.md#object-cookedchickenleg) | Object  | An undefined object; no examples or paths found in the provided context. | 5 | `{ . . . }` |
| `CopyPassiveSlot` | Integer | An index (0-based) specifying which equipment slot's passive to copy onto this unit. | 3 | `0`<br>`1` |
| `CorpseVaporizer` | Integer | The number of corpses vaporized on hit. | 3 | `1` |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 99 | `0`<br>`1`<br>`10` |
| [`CreateGlobalModifiers`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-createglobalmodifiers) | Object  | Defines global gameplay modifiers to activate. | 5 | `{ . . . }` |
| `DestroyWeapon` | Integer | The number of weapons destroyed. | 3 | `1` |
| `DestroyWeaponThrow` | Integer | The number of weapons destroyed after being thrown. | 3 | `1` |
| [`DigestDeadBodies`](../Reference_and_Meta/Enums.md#enum-digestdeadbodies) | Enum | Specifies the ability or animation used when digesting a dead body. | 3 | `Digest`<br>`LennyCatDies`<br>`MoonHead_Digest` |
| [`DoubleStatus`](../Reference_and_Meta/Enums.md#enum-doublestatus) | Enum | The name of a status effect whose stacks are doubled when applied. | 3 | `Bleed`<br>`Burn`<br>`Poison` |
| [`DropAsFamiliarOnArmorBreak`](../Reference_and_Meta/Enums.md#enum-dropasfamiliaronarmorbreak) | Enum | Specifies the familiar type to drop onto the tile when this status holder's armor breaks. | 3 | `FaceGrubFamiliar`<br>`HeadGrubFamiliar`<br>`NeckGrubFamiliar` |
| [`DustOnHit`](./Engine_StatusAndPassiveKeys.md#object-dustonhit) | Object  | Configuration for a dust object spawned on hit. | 3 | `{ . . . }` |
| [`EquipPermanentItem`](../Reference_and_Meta/Enums.md#enum-equippermanentitem) | Enum | The name of the item to permanently equip to the source. | 5 | `BoneClub`<br>`Kidney` |
| `ExtraBasicMoves_Status` | Integer | The number of extra basic moves per turn granted. | 6 | `1` |
| `ForceDisplace` | Integer | The distance the target is forced to displace. | 3 | `1` |
| [`ForceMoveTowardsEnemies`](../Reference_and_Meta/Enums.md#enum-forcemovetowardsenemies) | Enum / Integer  | Specifies the ability or distance to force the target to move towards enemies. | 3 | `1`<br>`DumbMove_Impl`<br>`MoveOne` |
| [`FormChangeHealthThreshold`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-formchangehealththreshold) | Object  | Specifies health thresholds that trigger form changes, with form_below for health at or below and form_above for health above. | 3 | `{ . . . }` |
| [`Holy`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-holy) | Enum / Object  | Specifies the 'Holy' form within FormChanger, with its own animation suffix and passives. | 86 | `{ . . . }`<br>`MegaGuppy_TransformHoly` |
| `IllusionTint` | Integer | If non-zero, applies an illusionary tint to the unit's sprite. | 3 | `1` |
| [`IncAuxCounterClamped`](./Engine_StatusAndPassiveKeys.md#object-incauxcounterclamped) | Object  | An object with `change` and `max` properties modifying the auxiliary counter by `change`, clamped to `max`. | 3 | `{ . . . }` |
| `include_spells` | Boolean | If true, the AI-controlled bonus turn includes spells as available actions. | 4 | `true` |
| `InstantMaxHealthUp` | Integer | The amount of permanent maximum health increase. | 3 | `20`<br>`4` |
| [`KnockOutCoin`](./Engine_StatusAndPassiveKeys.md#object-knockoutcoin) | Integer / Object  | The number of coins knocked out, with an optional probability or an object with stacks and chance. | 5 | `{ . . . }`<br>`1`<br>`[1 .5]` |
| [`Lava_Distortion`](./Engine_StatusAndPassiveKeys.md#object-lava_distortion) | Variable | A configuration object for a visual distortion effect, typically defining a movieclip and render settings. | 4 ||
| `Lifesteal` | Integer | The amount of lifesteal stacks applied. | 6 | `1`<br>`3` |
| [`ManaPickup`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-manapickup) | Object  | The amount of mana stacks and the frame range for the pickup animation. | 6 | `{ . . . }` |
| `Meteornado` | Integer | The number of Meteornado status stacks applied, or an object defining its visual effects. | 6 | `1` |
| `MimicSpawnerAttacks` | Integer | If positive, the number of attacks mimicked; if -1, mimics all attacks from spawner. | 3 | `-1`<br>`1` |
| `MinimumKnockbackFromPhysicalAttacks` | Integer | The minimum knockback distance applied when hit by a physical attack. | 3 | `1` |
| `MoonHeadFinisherEnabler` | Integer | Determines the finisher state for MoonHead abilities; negative values may disable. | 3 | `-1`<br>`0`<br>`1` |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](../Reference_and_Meta/Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | Enum | Specifies the name of the ability the unit will move and attempt to use at the start of each of its turns. | 3 | `Cannibalize`<br>`EatShit`<br>`face_EatNeverstone` |
| `must_do_damage` | Boolean | If true, the status or effect will only be applied if the attack or ability actually deals damage. | 3 | `true` |
| [`MutateViaAbility`](../Reference_and_Meta/Enums.md#enum-mutateviaability) | Enum | Specifies the ability that triggers a mutation form change. | 3 | `BBTransformMutant` |
| `NeckArmorPassiveMultiplierBonus` | Integer | A multiplier bonus applied to the passives of the unit's neck armor slot. | 3 | `1`<br>`2` |
| `NextAttackBonusRange` | Integer | The added range for the unit's next basic attack. | 4 | `1`<br>`3`<br>`5` |
| `PermanentDexterity` | Integer | The permanent amount of dexterity added or removed. | 5 | `1`<br>`2` |
| `PermanentSpeed` | Integer | The permanent amount of speed added or removed. | 5 | `-1`<br>`1`<br>`2` |
| `Piercing` | Integer | The amount of armor or damage reduction ignored by the attack or ability. | 4 | `1` |
| `PlayBackground` | Integer | Specifies the background index to play. | 5 | `0`<br>`1` |
| `PrioritizeHitDifferentTargets` | Integer | If set to 1, the unit's AI prioritizes hitting different targets rather than focusing one. | 3 | `1` |
| `RangeUp` | Integer | The number of stacks of bonus attack range applied. | 6 | `1` |
| `RepairOnKill` | Integer | The number of charges restored to the ability upon killing a target. | 3 | `1`<br>`2` |
| `RockyArmorPassive` | Integer | The number of stacks of the Rocky Armor status effect granted. | 3 | `1` |
| `RunInXTurns` | Integer | The number of turns after which this unit will flee the battle. | 3 | `1`<br>`2`<br>`3` |
| [`SetCrazyEyeBackgroundWeights`](./Engine_StatusAndPassiveKeys.md#object-setcrazyeyebackgroundweights) | Object  | An object containing a `weights` array that sets the weighting for which Crazy Eye background variant is displayed. | 3 | `{ . . . }` |
| [`SetDefaultFacePassive`](../Reference_and_Meta/Enums.md#enum-setdefaultfacepassive) | Enum | Specifies the name of the default face passive to be assigned to this unit. | 3 | `euphoric`<br>`insane` |
| `SharePickupsWithSpawner` | Integer | If set to 1, pickups collected by this unit are also given to its spawner. | 3 | `0`<br>`1` |
| `SpawnCreepOnHit` | Integer | If set to 1, spawns creep on the tile when this unit takes damage. | 3 | `1` |
| [`SpawnCustomTrap`](../Reference_and_Meta/Enums.md#enum-spawncustomtrap) | Enum | Specifies the name of a custom trap blueprint to spawn at the target location. | 3 | `CharmTrap`<br>`EggSackTrap`<br>`SpikeTrap` |
| `SpawnNeutralWebTrapOnMiss` | Integer | The number of neutral web traps spawned on the tile if the attack misses. | 3 | `1` |
| [`SpawnVolcanoOnBattleStart`](./Engine_StatusAndPassiveKeys.md#object-spawnvolcanoonbattlestart) | Object  | An object containing parameters (object type, tile, radius) for spawning a volcano effect at the start of battle. | 3 | `{ . . . }` |
| [`StackingFlowerTrail`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stackingflowertrail) | Object  | An object defining how a flower trail status stacks (stacks count, stack key) when the unit moves. | 3 | `{ . . . }` |
| [`StatusAllCharactersOnSpawn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusallcharactersonspawn) | Object  | Defines status effects applied to all characters when they spawn into the battlefield. | 5 | `{ . . . }` |
| [`StatusCharactersOnRoundEnd`](./Engine_StatusAndPassiveKeys.md#object-statuscharactersonroundend) | Object  | An object whose nested keys define statuses or effects applied to characters at the end of each round. | 3 | `{ . . . }` |
| [`SupportFormChangeInsteadOfRun`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-supportformchangeinsteadofrun) | Enum / Object  | Specifies a form change to trigger instead of fleeing, either as a passive object with ability details or a direct form name. | 3 | `{ . . . }`<br>`Attacker` |
| [`tag_filter`](../Reference_and_Meta/Enums.md#enum-tag_filter) | Enum | Specifies a tag (e.g., 'crow', 'rock', 'grub_familiar') used to filter which units a status or effect applies to. | 4 | `crow`<br>`grub_familiar`<br>`rock` |
| [`TakeBonusTurnWithAIControl`](../Reference_and_Meta/Miscellaneous.md#object-takebonusturnwithaicontrol) | Object  | An object configuring whether the bonus turn happens at the end of the round and whether spells are included. | 3 | `{ . . . }` |
| `TempInitiativeChange` | Integer | The flat change to the unit's initiative value. | 5 | `-100`<br>`-999`<br>`100` |
| [`ThornUpX`](./Engine_StatusAndPassiveKeys.md#object-thornupx) | Object  | An object defining a self-buff status effect, typically with its own animation (e.g., 'spikes'). | 5 | `{ . . . }` |
| [`TileTrail_Ahead`](../Reference_and_Meta/Enums.md#enum-tiletrail_ahead) | Enum | Specifies the type of tile to place one tile ahead of the unit's movement. | 4 | `FireTile`<br>`FlowerTile`<br>`OilTile` |
| `TriggerGameEnding` | Integer | If set to 1, triggers the game's ending sequence; 0 disables it. | 3 | `0`<br>`1` |
| `TrueShot` | Integer | The number of stacks of a buff that makes the unit's attacks unmissable. | 3 | `1` |
| [`TVOff`](./Engine_StatusAndPassiveKeys.md#object-tvoff) | Object  | An object defining a self-buff status effect that plays a 'turnOff' animation. | 5 | `{ . . . }` |
| [`UseAbility_NonStack`](../Reference_and_Meta/Enums.md#enum-useability_nonstack) | Enum | Specifies an ability to use on kill that does not stack with itself. | 3 | `BBTransformZealot`<br>`GenericRage` |
| `VaporizeTarget` | Integer | If non-zero, instantly destroys the target, leaving no corpse. | 3 | `1` |
| [`XIsMultipliedPercentHealth`](../Reference_and_Meta/Arrays.md#array-xismultipliedpercenthealth) | Array | The [stacks, probability] for multiplying health by a percentage. | 3 | `[1 12]`<br>`[14 1]`<br>`[6 2]` |
| [`AbilityChargeRefundChance`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-abilitychargerefundchance) | Object  | An object containing a percentage chance to refund an ability charge, with an advantage softcap. | 1 | `{ . . . }` |
| [`AbilityEnabledIfHasStatus`](../Reference_and_Meta/Enums.md#enum-abilityenabledifhasstatus) | Enum | Specifies the status effect that must be present on the unit for the ability to be enabled. | 2 | `DemonicGlyph_Bite`<br>`DemonicGlyph_Summon` |
| [`AbilityHealthThreshold`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-abilityhealththreshold) | Object  | Defines an ability and conditions for its activation when the unit's health reaches a threshold. | 13 | `{ . . . }` |
| [`AbilityOnRoundEnd`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-abilityonroundend) | Object  | Specifies an ability that is automatically executed at the end of each round. | 2 | `{ . . . }` |
| [`AbsorbBuff`](./Engine_StatusAndPassiveKeys.md#object-absorbbuff) | Variable | A visual effect object (e.g., ManaParticle) that plays when mana or a buff is absorbed. | 3 ||
| `AbsorbManaAura` | Integer | The amount of mana absorbed from nearby enemies each turn. | 2 | `1` |
| `AddAllyNeighborsToAbilityRange` | Integer | The number of additional tiles an ability's range is extended to include adjacent allies. | 1 | `1` |
| `AddChaScalingSpellDamage` | Integer | The amount of spell damage added that scales with the unit's Charisma stat. | 1 | `3` |
| [`AddHiddenTag`](../Reference_and_Meta/Enums.md#enum-addhiddentag) | Enum | A hidden tag applied to the unit for internal logic and triggers. | 6 | `bowling_ball`<br>`grown_hitler_clone`<br>`hitler_clone_fetus` |
| `AddInitiative` | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 10 | `-10`<br>`-100`<br>`-20` |
| `AddKnockbackToEverything` | Integer | The number of tiles of knockback added to all damage instances. | 2 | `1` |
| `AddLootMultiplier` | Integer | The multiplier added to loot drops from this unit. | 1 | `1` |
| [`AddPassivesToSummonAbilityMinions`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addpassivestosummonabilityminions) | Object  | An object whose nested keys define passives applied to minions summoned by abilities. | 2 | `{ . . . }` |
| [`AddPassiveToSpawnedRocks`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addpassivetospawnedrocks) | Object  | An object whose nested keys define passives applied to rocks spawned by the unit. | 2 | `{ . . . }` |
| `AddRangedCritChance` | Integer | The percentage chance added to critically hit with ranged attacks. | 1 | `25%` |
| [`AddSelfStatusToWeapons`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addselfstatustoweapons) | Object  | An object whose nested keys define status effects applied to the unit's own weapons. | 3 | `{ . . . }` |
| `AddSpellDamage` | Integer | The flat amount of spell damage added to all spell attacks. | 6 | `1`<br>`2` |
| `AddSpiritBombCharges` | Integer | The number of charges added to the Spirit Bomb ability. | 2 | `1`<br>`2` |
| `AddStartingMana` | Number | The amount of bonus mana the unit starts each battle with. | 7 | `20`<br>`5` |
| [`AddStatusToBasicAttackWithCooldown`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicattackwithcooldown) | Object  | An object whose nested keys define statuses applied to basic attacks, subject to a cooldown. | 2 | `{ . . . }` |
| [`AddStatusToExplosions`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoexplosions) | Object  | An object whose nested keys define statuses applied to explosion damage. | 4 | `{ . . . }` |
| [`AddStatusToFirstBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustofirstbasicattack) | Object  | An object whose nested keys define statuses applied only to the unit's first basic attack. | 2 | `{ . . . }` |
| [`AddStatusToKnockbackDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoknockbackdamage) | Object  | An object whose nested keys define statuses applied to damage caused by knockback. | 3 | `{ . . . }` |
| [`AddStatusToMeleeDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustomeleedamage) | Object  | An object whose nested keys define statuses applied to melee damage. | 2 | `{ . . . }` |
| [`AddStatusToSpells`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustospells) | Object  | Specifies status effects added to all spell attacks used by this unit. | 4 | `{ . . . }` |
| [`AddStatusToTrampleDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustotrampledamage) | Object  | An object whose nested keys define statuses applied to trample damage. | 3 | `{ . . . }` |
| [`AddTag`](../Reference_and_Meta/Enums.md#enum-addtag) | Enum | Specifies a gameplay tag (e.g., 'rock', 'plant') to add to the unit, used for interaction checks. | 12 | `bug`<br>`cat`<br>`fetus` |
| [`AddTemporaryEffectsToEquipment`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addtemporaryeffectstoequipment) | Object  | An object whose nested keys define temporary status effects added to equipment. | 1 | `{ . . . }` |
| `AddUnfilledMaxHealth` | Integer | The amount of maximum health added, but not healed (the health bar remains at its current level). | 4 | `10`<br>`20`<br>`50` |
| `AddWeaponScaling` | Integer | The amount of scaling added to damage based on the weapon's stats. | 2 | `1` |
| [`AfterImage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-afterimage) | Object  | Specifies the object or skill used to create an afterimage of the unit. | 7 | `{ . . . }` |
| `AggroTargetIsBuddy` | Integer | If set to 1, the unit's aggro target is its buddy (linked partner). | 2 | `1` |
| `all_items` | Variable | A variable field for specifying all items; no standard examples provided. | 2 ||
| `AllDamageCrits` | Integer | If set to 1, all damage dealt by the unit becomes critical hits. | 2 | `1` |
| `AllDamageImmune_IncludingSpeculative` | Integer | If set to 1, this unit is immune to all damage, including speculative damage. | 2 | `1` |
| `AlliesAvoidTraps` | Integer | If set to 1, allied units will not trigger traps. | 1 | `1` |
| `AllowPassTurn` | Integer | If set to 1, the unit can skip its turn. If 0, it cannot. | 2 | `0`<br>`1` |
| [`AllyBonusAbilityAura`](../Reference_and_Meta/Enums.md#enum-allybonusabilityaura) | Enum | Specifies an ability name granted to adjacent allies in an aura, optionally with a square radius. | 4 | `NubbyToss` |
| `AllyChainKnockback` | Integer | The number of additional tiles of knockback applied to enemies hit by chain knockback effects. | 1 | `1` |
| [`AllyDamageReaction`](../Reference_and_Meta/Enums.md#enum-allydamagereaction) | Enum | Specifies the ability to use when an ally takes damage, such as 'attack'. | 2 | `attack` |
| [`AllyHealthRegenAura`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-allyhealthregenaura) | Object  | An object defining an aura that grants health regeneration to allies, typically with 'stacks' and 'range' fields. | 2 | `{ . . . }` |
| [`AllyMoveAbilityAura`](../Reference_and_Meta/Enums.md#enum-allymoveabilityaura) | Enum | Determines the movement ability granted to allies within an aura. | 2 | `CatapultJump`<br>`CatapultJump2` |
| `AllyMultiplyKnockbackDamage` | Integer | A multiplier for knockback damage dealt to allies. | 2 | `2` |
| `AllyMultiplyKnockbackDistance` | Integer | A multiplier for knockback distance applied to allies. | 1 | `2` |
| `AllyUncappedHPAura` | Integer | The number of stacks granting uncapped maximum health to allies via an aura. | 1 | `1` |
| [`AlternateCraftingPools`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-alternatecraftingpools) | Object  | An object mapping crafting pool categories to alternate pools for the unit. | 2 | `{ . . . }` |
| `AlwaysHitDifferentTargets` | Integer | If set to 1, attacks always target different units, never the same target twice. | 2 | `1` |
| `AmplifyNegativeStatus` | Integer | The number of stacks that amplify the intensity of negative statuses on enemies. | 1 | `1` |
| `AmplifyPositiveStatus` | Integer | The number of stacks that amplify the intensity of positive statuses on allies. | 2 | `1`<br>`2` |
| `Antidote` | Float | The multiplier for the number of antidote pickups spawned. | 25 | `.5`<br>`1` |
| [`ApplyStatusesToRandomEnemiesEachTurn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-applystatusestorandomenemieseachturn) | Object  | An object specifying statuses to apply to random enemies each turn, with an optional 'count' field. | 4 | `{ . . . }` |
| [`ApplyStatusIfCrit`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-applystatusifcrit) | Object  | Defines effects that are applied only when the attack scores a critical hit. | 9 | `{ . . . }` |
| [`ApplyToTile`](./Engine_StatusAndPassiveKeys.md#object-applytotile) | Object  | Defines effects to apply to the target tile. | 2 | `{ . . . }` |
| [`ArmorBreakOnHit`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-armorbreakonhit) | Object  | An object defining durability loss and chance for armor to break when hit. | 2 | `{ . . . }` |
| `ArmorDodgeChance` | Integer | The percentage chance to dodge incoming attacks when wearing this armor. | 20 | `10%`<br>`15%`<br>`20%` |
| [`AutocastEachTurn`](../Reference_and_Meta/Enums.md#enum-autocasteachturn) | Enum | Specifies the ability automatically cast at the end of each turn. | 2 | `DarkOneStrike`<br>`ViolentOutburst` |
| [`AutocastEachTurnBegin`](../Reference_and_Meta/Enums.md#enum-autocasteachturnbegin) | Enum | Specifies the ability automatically cast at the start of each turn, optionally with chance and polarity. | 3 | `MindCrack_EldritchVisage`<br>`MindCrack_EldritchVisage2` |
| `AutoCritLowDamage` | Integer | The amount of damage below which attacks automatically critically strike. | 2 | `2`<br>`3` |
| `AutoEquipConsumables` | Integer | The number of consumables automatically equipped per turn. | 4 | `1` |
| `BackstabCritChance` | Float | A multiplier for critical hit chance on backstab attacks. | 6 | `.25`<br>`1` |
| `BackstabFront` | Integer | If set to 1, allows backstab bonuses to apply when attacking from the front. | 1 | `1` |
| `BasicAttackCantMiss` | Integer | If nonzero, the unit's basic attack cannot miss. | 2 | `1` |
| `BasicAttackStatusCarefulness` | Integer | The number of stacks of Carefulness applied by basic attacks. | 2 | `1` |
| [`BasicMonkMelee`](./Engine_StatusAndPassiveKeys.md#object-basicmonkmelee) | Object  | An object defining the basic melee attack for a monk class. | 7 | `{ . . . }` |
| [`BasicRanged`](./Engine_StatusAndPassiveKeys.md#object-basicranged) | Object  | An object defining the basic ranged attack for a unit. | 7 | `{ . . . }` |
| [`BasicSuplex`](./Engine_StatusAndPassiveKeys.md#object-basicsuplex) | Object  | An object defining the basic suplex ability for a unit. | 3 | `{ . . . }` |
| [`BodyGuard`](./Engine_StatusAndPassiveKeys.md#object-bodyguard) | Object  | An object that applies a bodyguard status, optionally linking to a swap ability. | 8 | `{ . . . }` |
| [`BodyGuard`](./Engine_StatusAndPassiveKeys.md#object-bodyguard) | Object  | An object that applies a bodyguard status, optionally linking to a swap ability. | 8 | `{ . . . }` |
| `BonusFoodEachBattle` | Integer | The amount of bonus food earned at the end of each battle. | 2 | `2`<br>`20` |
| `BonusHealthRegenBasedOnDex` | Integer | The amount of bonus health regeneration per point of dexterity. | 1 | `5` |
| `BonusRangeBasedOnDex` | Integer | The amount of bonus range per point of dexterity. | 1 | `5` |
| [`BonusToss`](./Engine_StatusAndPassiveKeys.md#object-bonustoss) | Object  | An object defining a bonus toss ability for the unit. | 3 | `{ . . . }` |
| [`BonusToss2`](./Engine_StatusAndPassiveKeys.md#object-bonustoss2) | Object  | An object defining a second bonus toss ability for the unit. | 2 | `{ . . . }` |
| [`BoobyTrapItems`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-boobytrapitems) | Object  | An object defining effects to apply when items are thrown or broken. | 2 | `{ . . . }` |
| [`BoomerCatExplode`](./Engine_StatusAndPassiveKeys.md#object-boomercatexplode) | Object  | An object defining the explosion ability for a boomerang cat, including its spell template and graphics. | 5 | `{ . . . }` |
| `BoostAllyStatsOnDeath` | Integer | The number of stacks that boost ally stats when this unit dies. | 2 | `1`<br>`2` |
| `BoostDamageGlobalAura` | Integer | The amount of damage boost applied by a global aura to all allies. | 2 | `1` |
| `BoostHeals` | Integer | The number of stacks that increase healing received or dealt. | 9 | `-2`<br>`1`<br>`2` |
| `BoostRangeGlobalAura` | Integer | The amount of range boost applied by a global aura to all allies. | 1 | `1` |
| [`BouncyProjectiles`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bouncyprojectiles) | Object  | An object with 'max_bounces' and 'max_range' defining projectile bounciness behavior. | 3 | `{ . . . }` |
| `Bound` | Integer | The number of stacks of the Bound status effect applied to the target. | 2 | `3` |
| `BraceForEachNeighboringEnemy` | Integer | The number of Brace stacks gained for each adjacent enemy. | 3 | `1`<br>`2` |
| `BreakWhenNoShield` | Integer | If 1, the armor breaks when the unit has no shield remaining. | 2 | `1` |
| [`BungaEntrance`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bungaentrance) | Object  | Specifies the entrance animation, ability, and conditions for this unit's dramatic battle entrance. | 5 | `{ . . . }` |
| [`BungaSwipe`](./Engine_StatusAndPassiveKeys.md#object-bungaswipe) | Object  | An object defining a melee swipe ability with AI and graphics. | 4 | `{ . . . }` |
| `CancelPrimedAbilities` | Integer | If non-zero, cancels any primed abilities on the target. | 2 | `1` |
| `CanLevelUpWhenDead` | Integer | If 1, allows the unit to gain experience and level up while dead. | 2 | `1` |
| `CanRemoveCursedItems` | Integer | If nonzero, allows the unit to remove cursed items from equipment slots. | 3 | `1` |
| `CanShield` | Integer | If set to 1, this unit can generate shields. | 2 | `1` |
| `CapDamageFromAllies` | Integer | The maximum amount of damage the unit can take from allies per hit. | 2 | `1` |
| `CapMovementAbilityRange` | Integer | The maximum range allowed for movement abilities. | 2 | `1` |
| `CapTechSpent` | Integer | The maximum amount of tech that can be spent on this ability per turn. | 2 | `0`<br>`1` |
| [`CatAPultAnimation`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catapultanimation) | Object  | An object specifying the ability and animation used for the CatAPult passive. | 2 | `{ . . . }` |
| [`CatapultJump`](./Engine_StatusAndPassiveKeys.md#object-catapultjump) | Object  | An object defining the Catapult Jump ability, a variant of BasicJump. | 4 | `{ . . . }` |
| [`CatapultJump2`](./Engine_StatusAndPassiveKeys.md#object-catapultjump2) | Object  | An object defining an upgraded Catapult Jump ability with a different description. | 3 | `{ . . . }` |
| [`CatchProjectiles`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catchprojectiles) | Object  | An object defining chance to catch projectiles and optionally apply statuses. | 8 | `{ . . . }` |
| `CCImmunity` | Integer | If set to 1, this unit is immune to crowd control effects. | 3 | `1` |
| `ChainKnockback` | Integer | If 1, enables knockback to chain to additional targets. | 6 | `1` |
| [`ChanceToBlockAndCounter`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-chancetoblockandcounter) | Integer / Object  | The percentage chance or an object defining chance and conditions to block and counter an attack. | 4 | `{ . . . }`<br>`15%`<br>`25%`<br>`33%` |
| `ChanceToDisableActionsIfNotCharmed` | Integer | The percentage chance to disable actions of enemies that are not charmed. | 2 | `75%` |
| [`ChanceToRevive`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-chancetorevive) | Integer / Object  | The percentage chance or an object defining chance, health, and statuses on revival. | 9 | `{ . . . }`<br>`100`<br>`25` |
| [`ChangeFaction`](../Reference_and_Meta/Enums.md#enum-changefaction) | Enum | Specifies the name of the faction to switch the target to. | 2 | `sabertooths` |
| `ChangeTauntPriority` | Integer | The amount to adjust the unit's taunt priority, affecting enemy targeting. | 2 | `-1` |
| [`ChangeTileOnDeath`](../Reference_and_Meta/Enums.md#enum-changetileondeath) | Enum | Specifies the tile type that replaces the current tile when this unit dies. | 2 | `WaterTile` |
| [`ChargeFists`](./Engine_StatusAndPassiveKeys.md#object-chargefists) | Integer / Object  | The number of charge stacks applied to unarmed attacks. | 6 | `{ . . . }`<br>`1` |
| [`ChargeFists`](./Engine_StatusAndPassiveKeys.md#object-chargefists) | Integer / Object  | The number of charge stacks applied to unarmed attacks. | 6 | `{ . . . }`<br>`1` |
| [`ChargeSpiritBombAura`](../Reference_and_Meta/Enums.md#enum-chargespiritbombaura) | Enum | Specifies the ability to charge for spirit bomb aura. | 2 | `DonateEnergy`<br>`DonateEnergy2` |
| `CharmAllFlies` | Integer | If 1, charms all fly-type enemies, causing them to become allies. | 3 | `1` |
| [`CharmedDemonKitten`](./Engine_StatusAndPassiveKeys.md#object-charmeddemonkitten) | Object  | An object defining the Charmed Demon Kitten familiar, a variant of Hyde. | 4 | `{ . . . }` |
| [`CharmedFlySwarm`](./Engine_StatusAndPassiveKeys.md#object-charmedflyswarm) | Object  | Specifies the definition for a charmed fly swarm that inherits properties from FlySwarm, with faction set to allies and inheriting faction. | 3 | `{ . . . }` |
| `CharmedForceAttack` | Integer | If non-zero, forces the charmed target to use its basic attack on a random nearby unit. | 4 | `1` |
| [`CherubimReaction`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-cherubimreaction) | Object  | Specifies the abilities used when this unit leaves or returns to the battlefield. | 2 | `{ . . . }` |
| `ClearNegativeEffects` | Integer | The number of negative effects cleared from the target. | 2 | `1` |
| `CoinsAddDamage` | Integer | The amount of damage added based on the number of coins the unit has. | 2 | `1`<br>`2` |
| `CollectPickupsOnBattleEnd` | Integer | The number of pickups automatically collected from corpses on the battlefield when the battle ends. | 2 | `1` |
| `CollideWithThrowTarget` | Integer | Determines whether the thrown object collides with the primary target (0 disables collision). | 2 | `0` |
| [`Conductor`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conductor) | Object  | The number of times the Conduct effect is applied. | 7 | `{ . . . }` |
| `ConductorManaRegen` | Integer | The amount of mana regenerated per turn by the Conductor effect. | 1 | `2` |
| [`ConjureBonusAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conjurebonusability) | Enum / Object  | Specifies the name of the bonus ability to conjure. | 8 | `{ . . . }`<br>`Class`<br>`Colorless`<br>`Mage` |
| [`ConjureBonusAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conjurebonusability) | Enum / Object  | Specifies the name of the bonus ability to conjure. | 8 | `{ . . . }`<br>`Class`<br>`Colorless`<br>`Mage` |
| `ConjureCastSpellsForAllies` | Integer | The number of additional spells conjured for allies when casting. | 2 | `1`<br>`2` |
| `ConsumableEffectsMultiplierBonus` | Integer | A multiplier bonus applied to the effects of consumable items. | 3 | `1` |
| `CopyCatPassive_Initializer` | Integer | The number of copies of this passive to initialize. | 2 | `1`<br>`2` |
| [`CopySpells`](./Engine_StatusAndPassiveKeys.md#object-copyspells) | Integer / Object  | The number of spells copied from the target, or an object specifying `stacks` and whether the copy is `upgraded`. | 2 | `{ . . . }`<br>`1` |
| [`Counterspell`](./Engine_StatusAndPassiveKeys.md#object-counterspell) | Integer / Object  | If non-zero, negates the next incoming enemy spell and triggers the configured counterspell effects. | 6 | `{ . . . }`<br>`1` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1684 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `DamageBasedOnMissingHealth` | Integer | The percentage of the target's missing health dealt as additional damage. | 2 | `25`<br>`50` |
| `DamageDistanceAOEFalloff` | Integer | The falloff multiplier applied to AoE damage based on distance from the center of the effect. | 2 | `1`<br>`2` |
| `DamageEnemiesOnHeal` | Integer | The amount of damage dealt to enemies whenever the unit is healed. | 2 | `1`<br>`2` |
| `DamageEnemiesOnKill` | Integer | The amount of damage dealt to enemies whenever the unit kills an enemy. | 2 | `1`<br>`2` |
| [`DamageNeighborsAfterMove`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-damageneighborsaftermove) | Object  | Defines the spell damage and effects applied to neighboring tiles after the unit moves. | 4 | `{ . . . }` |
| [`DamageNeighborTilesWhenCastSpell`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-damageneighbortileswhencastspell) | Object  | Defines the spell damage and effects applied to neighbor tiles when a spell is cast. | 2 | `{ . . . }` |
| [`DamageReductionAura`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-damagereductionaura) | Object  | Defines an aura that reduces incoming damage, with range, ally-only, and stack settings. | 3 | `{ . . . }` |
| `DamageTrinket` | Integer | The amount of durability damage dealt to the target's equipped trinket. | 2 | `1` |
| `DeathChill` | Integer | The number of Chill stacks applied to the killer upon death. | 3 | `1` |
| [`DeathRattle`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-deathrattle) | Enum / Object  | Specifies an ability or effect triggered when the unit dies, optionally with a pop_corpse flag. | 36 | `{ . . . }`<br>`BBExplode`<br>`BloatyExplodey`<br>`BombFlyExplode` |
| `DebuffImmunity` | Integer | If 1, the unit is immune to debuffs. | 8 | `1` |
| `DejaVu` | Integer | The percentage chance or definition for the DejaVu disorder, causing repeated events. | 3 | `10%` |
| [`DelayCastAbility`](./Engine_StatusAndPassiveKeys.md#object-delaycastability) | Enum / Object  | Specifies the name of an ability to cast after a delay. | 2 | `{ . . . }`<br>`HitlerNuke` |
| `DelayedFury` | Integer | The percentage of Fury damage that is stored and applied after a delay. | 2 | `0`<br>`75` |
| `DemonicGlyph_Bite` | Integer | The weight for the demonic glyph of bite, or its configuration. | 4 | `1` |
| `DemonicGlyph_Summon` | Integer | The weight for the demonic glyph of summon, or its configuration. | 4 | `1` |
| `DemonicGlyphFrames` | Integer | The number of animation frames for the demonic glyph effect. | 2 | `1` |
| `DepressionAura` | Integer | The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings. | 11 | `1`<br>`2` |
| [`DiesToElement`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-diestoelement) | Enum / Object  | Specifies the element that instantly kills this unit, optionally with an instant flag. | 2 | `{ . . . }`<br>`Wind` |
| `DieViaAbilityInternally` | Integer | If non-zero, causes the target to die via an internal ability trigger. | 2 | `1` |
| `DirtyClaws` | Integer | The number of additional damage instances from Dirty Claws on attack. | 6 | `1` |
| `DisablePassiveSlot` | Integer | If non-zero, disables the specified passive slot index (0 or 1). | 2 | `0`<br>`1` |
| `DisplaceToOriginalPosition` | Integer | If non-zero, returns the unit to its original position after the effect resolves. | 2 | `1` |
| `DissuadeInstakills` | Integer | If set to 1, this unit cannot be instantly killed. | 2 | `1` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 26 | `1`<br>`10`<br>`100` |
| `DoubleCastSpell` | Integer | The number of times the next spell cast is doubled, or a template with name and tooltip. | 6 | `1`<br>`2` |
| `DoubleCastWeapons` | Integer | The number of additional weapon casts per attack. | 3 | `1`<br>`2` |
| [`DoubleLoot`](./Engine_StatusAndPassiveKeys.md#object-doubleloot) | Integer / Object  | The multiplier for loot drops, where 1 or 2 doubles the loot. | 5 | `{ . . . }`<br>`1`<br>`2` |
| [`DoubleLoot`](./Engine_StatusAndPassiveKeys.md#object-doubleloot) | Integer / Object  | The multiplier for loot drops, where 1 or 2 doubles the loot. | 5 | `{ . . . }`<br>`1`<br>`2` |
| `DrinkWater` | Integer | The number of water-drink actions performed. | 3 | `1` |
| [`DrMangler`](./Engine_StatusAndPassiveKeys.md#object-drmangler) | Object  | Defines the Dr Mangler passive, typically increasing damage based on missing health. | 5 | `{ . . . }` |
| `DukeOfFlies` | Integer | The number of flies spawned when the unit dies. | 4 | `1` |
| [`Dyslexia`](../Reference_and_Meta/Arrays.md#array-dyslexia) | Array | An array [minRange maxRange] defining the random range of spell range swap caused by Dyslexia. | 8 | `[3 5]`<br>`[6 9]` |
| `EachSpellFreeAtFullMana` | Integer | The number of spells that cost no mana when the unit has full mana. | 1 | `1` |
| [`Earth`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-earth) | Object  | Defines the Earth element effects, including damage value. | 30 | `{ . . . }` |
| [`ElementalAttunement`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-elementalattunement) | Object  | Defines the elemental effects (Fire, Ice, etc.) applied by the attunement. | 5 | `{ . . . }` |
| [`EMP`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-emp) | Object  | Defines the EMP effect, including spell graphics override for pulsed area damage. | 6 | `{ . . . }` |
| `Empath` | Integer | The percentage of damage shared with nearby allies from the Empath disorder. | 5 | `100%`<br>`50%` |
| `EmptyMana` | Integer | If non-zero, sets the unit's mana to empty when applied. | 2 | `1` |
| [`EmptyMind`](./Engine_StatusAndPassiveKeys.md#object-emptymind) | Integer / Object  | The number of Empty Mind stacks, likely disabling special abilities. | 6 | `{ . . . }`<br>`1` |
| [`EmptyMind`](./Engine_StatusAndPassiveKeys.md#object-emptymind) | Integer / Object  | The number of Empty Mind stacks, likely disabling special abilities. | 6 | `{ . . . }`<br>`1` |
| `EnemiesGetPickupsKnockedOut` | Integer | The number of pickups knocked out of enemies when they are defeated. | 2 | `1`<br>`2` |
| `EnergyStorm` | Integer | The period or definition for the Energy Storm, dealing periodic damage in an area. | 6 | `3` |
| [`Enlarge`](./Engine_StatusAndPassiveKeys.md#object-enlarge) | Integer / Object  | The number of turns the unit is enlarged, increasing its size and stats. | 3 | `{ . . . }`<br>`3` |
| [`Enlarge`](./Engine_StatusAndPassiveKeys.md#object-enlarge) | Integer / Object  | The number of turns the unit is enlarged, increasing its size and stats. | 3 | `{ . . . }`<br>`3` |
| `EquipmentPassiveMultiplierBonus` | Integer | A multiplier bonus applied to passive effects from equipment. | 2 | `1` |
| `EquipmentSetBonusBonus` | Integer | The number of additional set bonuses granted from equipment. | 2 | `1`<br>`2` |
| [`EscapeSequence`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-escapesequence) | Object  | Defines an escape sequence with safe explosion displacement and random distance displacement. | 4 | `{ . . . }` |
| [`Eternal`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-eternal) | Object  | Defines the Eternal revival effect, setting stacks and the health percentage restored. | 5 | `{ . . . }` |
| `ExpireOnSpawnerTurnEnd` | Integer | If set to 1, this unit is removed from battle at the end of its spawner's turn. | 2 | `1` |
| `ExplodeOverkilledEnemies` | Integer | The number of explosions caused by overkilled enemies. | 2 | `1`<br>`2` |
| `ExplosionImmunity` | Integer | If non-zero, grants immunity to explosion damage. | 2 | `1` |
| [`ExtraStatusWhenDealingDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-extrastatuswhendealingdamage) | Object  | Defines additional statuses applied to the target or source when dealing damage, with conditionals. | 5 | `{ . . . }` |
| `ExtraTrinketUses` | Integer | The number of additional uses granted to trinkets. | 2 | `1`<br>`10` |
| [`FaceLastDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-facelastdamage) | Integer / Object  | If set to 1, the unit turns to face the direction of the last damage received; an object can specify animation settings. | 2 | `{ . . . }`<br>`1` |
| `FaceShield` | Integer | If 1, the unit has a face shield that protects it from certain attacks or effects. | 6 | `0`<br>`1` |
| [`FamiliarBonusAbility`](../Reference_and_Meta/Enums.md#enum-familiarbonusability) | Enum | Specifies the name of the bonus ability added to familiars. | 2 | `FamiliarSelfDestruct`<br>`FamiliarSelfDestruct2` |
| `FamiliarSecondaryDamageImmunity` | Integer | If non-zero, grants immunity to secondary damage sources for familiars. | 2 | `1` |
| [`FinalBossShield`](../Reference_and_Meta/Enums.md#enum-finalbossshield) | Enum | Specifies the shield ability used by a final boss, or None for no shield. | 2 | `DestroyerShieldBash`<br>`None` |
| [`FindExtraItemFromPoolOnBattleEnd`](../Reference_and_Meta/Enums.md#enum-findextraitemfrompoolonbattleend) | Enum | Specifies the item pool from which an extra item is granted at the end of combat. | 3 | `combat_reward_easy`<br>`pills` |
| [`FindItem`](../Reference_and_Meta/Enums.md#enum-finditem) | Enum | The name of the specific item to find and add to the source's inventory. | 3 | `BoneClub`<br>`Molars`<br>`Pearl` |
| `FireStorm` | Integer | The percentage chance or combo definition for the Fire Storm effect. | 3 | `0%`<br>`33%` |
| `FlatHealWhenDealDamage` | Integer | The flat amount of health healed each time damage is dealt. | 1 | `1` |
| `FlatLeechIfDamaged` | Integer | The flat amount of health leeched when the unit takes damage. | 2 | `3`<br>`5` |
| `FlippedFacingForceAttack` | Integer | If non-zero, forces the unit to attack after flipping its facing direction. | 2 | `1` |
| `FlowerPowerAuraBrace` | Integer | The amount of brace (defense) granted by the Flower Power aura. | 2 | `1` |
| `FlowerPowerAuraStrength` | Integer | The amount of strength (attack) granted by the Flower Power aura. | 2 | `1` |
| `FlowersOnEndTurn` | Integer | The number of flowers spawned on the unit's tile at the end of each turn. | 4 | `1`<br>`3`<br>`4` |
| `FlowersOnHit` | Integer | The number of flowers spawned on the tile upon hitting the target. | 2 | `1` |
| [`FlyDamageIncrease`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-flydamageincrease) | Object  | The number of stacks or alias for damage increase against flying units. | 4 | `{ . . . }` |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 18 | `1` |
| [`FollowUp`](../Reference_and_Meta/Enums.md#enum-followup) | Enum | Specifies the name of the follow-up ability triggered after an attack. | 4 | `FollowUpDash`<br>`FollowUpDash2` |
| `ForceMoveNonAlliesInRangeTowardsTile` | Integer | The tile range within which non-allied units are forcibly moved towards a specified tile. | 2 | `3`<br>`4` |
| [`ForceMoveTowardsTaggedObject`](./Engine_StatusAndPassiveKeys.md#object-forcemovetowardstaggedobject) | Object  | An object specifying the `ability` and optional `tag` used to forcibly move the unit towards a tagged object. | 2 | `{ . . . }` |
| [`FormChangeDuringWeatherElement`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-formchangeduringweatherelement) | Object  | Specifies a form change that triggers when the weather matches a given element. | 2 | `{ . . . }` |
| `FrontstabCritChance` | Integer | The percentage chance to critically hit when attacking from the front. | 1 | `100%` |
| `FullHealthAllStatsUp` | Integer | The number of AllStatsUp stacks granted when at full health. | 1 | `1` |
| `FullHealthCritChance` | Integer | The additional critical hit chance percentage when at full health. | 2 | `100` |
| `FullHealthManaRegen` | Integer | The amount of mana regenerated per turn while at full health. | 1 | `5` |
| `FullPower` | Integer | The number of stacks applied per turn while at full health or full mana. | 4 | `3` |
| `GainExtraShield` | Integer | The amount of shield gained on turn start. | 3 | `2`<br>`4` |
| `GainManaWhenAnythingDies` | Integer | The amount of mana gained whenever any unit dies. | 1 | `1` |
| `GlobalManaBurnAura` | Integer | The amount of mana burned from all enemies per turn. | 2 | `-1` |
| [`GlobalSpawnOnRoundEnd`](./Engine_StatusAndPassiveKeys.md#object-globalspawnonroundend) | Object  | Specifies the object to spawn globally at the end of each round. | 2 | `{ . . . }` |
| `GoopWalk` | Integer | If set to 1, this unit can move through goop tiles without being slowed or damaged. | 2 | `1` |
| [`Grass`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-grass) | Object  | Specifies the status effects applied to allies standing on grass tiles. | 25 | `{ . . . }` |
| `GrassTileHealing` | Integer | The amount of healing received per turn while on a grass tile. | 2 | `1` |
| [`GravityWell`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-gravitywell) | Object  | Specifies the damage and effect applied to units pulled into a gravity well. | 6 | `{ . . . }` |
| `greater` | Variable | Specifies a conditional check for a value being greater than another value. | 2 ||
| [`GrenadeExplode`](./Engine_StatusAndPassiveKeys.md#object-grenadeexplode) | Object  | Specifies the explosion effect and graphics used when a grenade detonates. | 5 | `{ . . . }` |
| [`Haunt`](./Engine_StatusAndPassiveKeys.md#object-haunt) | Object  | Specifies the status effect applied when haunting a target. | 4 | `{ . . . }` |
| `HealAndOverhealToShield` | Integer | The amount of healing that also converts overhealing into shield. | 2 | `12`<br>`20` |
| `HealAtStart` | Integer | The percentage or amount of health restored at the start of the turn. | 1 | `100%` |
| `HealDamagesEnemies` | Integer | If true, healing actions also damage enemies by this amount. | 2 | `1` |
| `HealingAura` | Integer | The amount of healing per turn granted to nearby allies. | 3 | `1` |
| `HealsAlsoRegenMana` | Integer | The percentage or amount of mana regenerated whenever healing is applied. | 2 | `2`<br>`50%` |
| `HealsCanRevive` | Integer | The number of times per battle healing can revive a fallen ally. | 2 | `1`<br>`3` |
| `HolyDamageMultiplierBonus` | Integer | The multiplier bonus applied to holy damage. | 1 | `1` |
| `HolyShieldTransferToSpawner` | Integer | If true, holy shield is transferred to the unit that spawned this one on death. | 2 | `1` |
| [`HolyShieldTransferToTaggedMinions`](../Reference_and_Meta/Enums.md#enum-holyshieldtransfertotaggedminions) | Enum | Specifies the tag of minions that receive holy shield on the owner's death. | 2 | `any`<br>`crow` |
| `HPGainBlock` | Integer | If true, the unit cannot gain health from any source. | 2 | `1` |
| [`IceArmor`](./Engine_StatusAndPassiveKeys.md#object-icearmor) | Integer / Object  | The number of Ice Armor stacks granting defensive properties. | 7 | `{ . . . }`<br>`1` |
| [`IceArmor`](./Engine_StatusAndPassiveKeys.md#object-icearmor) | Integer / Object  | The number of Ice Armor stacks granting defensive properties. | 7 | `{ . . . }`<br>`1` |
| [`ImmediateUseDirectionalAbility`](../Reference_and_Meta/Enums.md#enum-immediateusedirectionalability) | Enum | Specifies the name of a directional ability to be used immediately by the unit. | 2 | `BowlDash`<br>`BowlDash2` |
| `ImmobilePassive` | Integer | If set to 1, this unit cannot move from its starting position. | 2 | `1` |
| `ImmortalLeeches` | Integer | The number of leech stacks that persist beyond death. | 4 | `1` |
| `IncreaseExplosionSize` | Integer | The number of extra tiles added to the radius of explosions. | 7 | `1`<br>`2`<br>`7` |
| `IncreaseHealingSpellRange` | Integer | The number of extra tiles added to the range of healing spells. | 2 | `2` |
| `IncreaseItemUsesOnEquip` | Integer | The number of extra uses granted to items when equipped. | 1 | `1` |
| `IncreaseSpellRange` | Integer | The number of extra tiles added to the range of spells. | 4 | `10`<br>`2`<br>`20` |
| [`InfiniteRebirth`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-infiniterebirth) | Object  | Specifies the health and effects for unlimited rebirth upon death. | 5 | `{ . . . }` |
| `InjuryImmunity` | Integer | The number of turns the unit is immune to injuries. | 13 | `1` |
| `JohnnyCriesForWashers` | Integer | The number of washers (currency) requested by the Johnny NPC. | 2 | `1`<br>`2` |
| [`KaijuWinCon`](../Reference_and_Meta/Enums.md#enum-kaijuwincon) | Enum | Determines which kaiju victory condition is active for this unit. | 2 | `pyrophina`<br>`zaratana` |
| `KillsHeal` | Integer | The amount or percentage of health restored on kill. | 4 | `5`<br>`50%` |
| [`KillsToMeat`](../Reference_and_Meta/Enums.md#enum-killstomeat) | Enum | Specifies the type of meat item spawned when killing certain enemies. | 4 | `Food` |
| [`LateBloomer`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-latebloomer) | Object  | Specifies the stats gained after a set number of turns or stacks. | 6 | `{ . . . }` |
| [`LeaveBehindOnceEachMove`](../Reference_and_Meta/Enums.md#enum-leavebehindonceeachmove) | Enum | Specifies the object left behind on the tile once per move. | 2 | `Poop`<br>`Scrap` |
| `LeechPercent` | Integer | The percentage of damage dealt restored as health. | 2 | `50` |
| `LightningAspectCharge` | Integer | The number of charges gained that enhance the next lightning attack. | 2 | `0`<br>`1` |
| [`LightningRod`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-lightningrod) | Object  | Specifies the unit tags and conditions that cause lightning strikes. | 4 | `{ . . . }` |
| `LimitDamage` | Integer | The maximum amount of damage the unit can take from a single hit. | 11 | `1` |
| `LimitHeal` | Integer | If 1, prevents the unit from being healed. | 11 | `0`<br>`1` |
| `LineOfSightTrueSightAura` | Float | The multiplier or chance for line of sight true sight aura to reveal hidden units. | 2 | `.5`<br>`0` |
| `LobbedHook` | Integer | The number of hooks that arc over obstacles to pull targets. | 2 | `1`<br>`2` |
| [`LowHealthAllyDodgeChanceAura`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-lowhealthallydodgechanceaura) | Object  | Specifies the health threshold and dodge chance granted to nearby low-health allies. | 3 | `{ . . . }` |
| `MagicDamageImmune` | Integer | If set to 1, this unit is immune to magic damage. | 2 | `1` |
| `MakeBasicAttackPassThroughThings` | Integer | If true, basic attacks pass through obstacles and other units. | 2 | `1` |
| `MakeBasicAttackPull` | Integer | If nonzero, the unit's basic attack pulls the target closer. | 2 | `1` |
| `MakeSpellsRequireCharge` | Integer | If true, spells require a charge-up turn before casting. | 5 | `1` |
| `MamaCatAnimations` | Integer | If set to 1, enables special mama cat animations. | 2 | `1` |
| `ManaRegenMultiplierIfManaEmpty` | Integer | The multiplier applied to mana regen when mana is empty. | 2 | `2` |
| [`Math`](./Engine_StatusAndPassiveKeys.md#object-math) | Object  | An object containing a `stacks` value that determines how many times the nested effects are applied. | 6 | `{ . . . }` |
| `MaxHPUp` | Integer | The amount of maximum health permanently increased. | 2 | `100` |
| `MegaMinions` | Integer | The number of extra minions spawned or maximum minion count. | 4 | `3` |
| `Metal` | Integer | The number of armor stacks or metal keyword effects. | 100 | `1` |
| `MetalDetector` | Integer | The number of extra metal drops or scrap found per turn. | 4 | `10`<br>`5` |
| `MinimumTech` | Integer | The minimum tech level guaranteed when crafting or upgrading. | 2 | `1` |
| [`MiniVolcanoReaction`](../Reference_and_Meta/Enums.md#enum-minivolcanoreaction) | Enum | Specifies the ability triggered when a mini volcano erupts near this unit. | 2 | `MiniVolcano_Spurt`<br>`ThrobShot_Reaction` |
| [`MockingbirdForm`](./Engine_StatusAndPassiveKeys.md#object-mockingbirdform) | Object  | Specifies the shape-shift ability that transforms the unit into a mockingbird. | 5 | `{ . . . }` |
| [`ModifyAbility`](./Engine_StatusAndPassiveKeys.md#object-modifyability) | Object  | Specifies the modifications to an ability's properties, such as cost or type. | 2 | `{ . . . }` |
| [`MotherTumorSpawnInCapture`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-mothertumorspawnincapture) | Object  | Specifies the form changes and statuses applied when the mother tumor spawns after capturing a cat or non-cat. | 2 | `{ . . . }` |
| [`MoveAwayFromDamageSource`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-moveawayfromdamagesource) | Object  | Specifies the move ability used to flee from the source of damage, or an object with `move_ability`. | 3 | `{ . . . }` |
| [`MovementReaction`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-movementreaction) | Object  | Specifies an ability to cast when a unit moves within range, with options for targeting and conditions. | 11 | `{ . . . }` |
| [`MoveOne`](./Engine_StatusAndPassiveKeys.md#object-moveone) | Object  | Specifies a forced movement of exactly one tile in a direction. | 20 | `{ . . . }` |
| `MoveRandomly` | Integer | If true, the unit moves randomly to an adjacent tile each turn. | 1 | `1` |
| `MoveSpeedMultiplier` | Float | A multiplier for the unit's movement speed. | 2 | `.5` |
| [`MoveTowardsDamageSource`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-movetowardsdamagesource) | Enum / Object  | Determines the movement behavior when moving towards the unit that dealt damage to it. | 11 | `{ . . . }`<br>`MoveOne` |
| [`MoveWhenDamaged`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-movewhendamaged) | Enum / Object  | Defines movement behavior when the unit takes damage, such as weights and move ability. | 12 | `{ . . . }`<br>`TKNG_Hop`<br>`move` |
| [`neck_NukeBonus`](./Engine_StatusAndPassiveKeys.md#object-neck_nukebonus) | Object  | A self-buff ability that grants the Nuke Explosion sub-ability, augmenting the unit's next weapon-based attack with a nuclear detonation. | 3 | `{ . . . }` |
| [`neck_NukeExplode`](./Engine_StatusAndPassiveKeys.md#object-neck_nukeexplode) | Object  | A spell template ability representing the nuclear explosion triggered by Nuke Bonus, playing the NukeBlastLarge center particle and no animation. | 4 | `{ . . . }` |
| [`Necro_SoulDagger_Uncharged`](./Engine_StatusAndPassiveKeys.md#object-necro_souldagger_uncharged) | Object  | The uncharged state of the Necromancer's Soul Dagger ability, dealing reduced damage or having a weaker effect compared to the charged version. | 5 | `{ . . . }` |
| [`NextAttackSpecialCrit`](./Engine_StatusAndPassiveKeys.md#object-nextattackspecialcrit) | Integer / Object  | The number of charges for a special crit on the next attack, or an object defining its bonus properties. | 2 | `{ . . . }`<br>`1` |
| [`NextBattleStatus`](./Engine_StatusAndPassiveKeys.md#object-nextbattlestatus) | Object  | A set of status effects (e.g., stat buffs, full heal) automatically applied to the unit at the start of the next battle. | 2 | `{ . . . }` |
| `NoManaRegen` | Integer | The unit does not naturally regenerate mana per turn. Value indicates the stage or flag enabling this restriction. | 3 | `1` |
| `NoReflection` | Integer | The unit's reflected damage effects are disabled. Value acts as a binary flag. | 2 | `1` |
| [`NubbyToss`](./Engine_StatusAndPassiveKeys.md#object-nubbytoss) | Object  | An ability or action where the unit throws a stumpy or truncated projectile, typically dealing damage or applying a debuff. | 3 | `{ . . . }` |
| `NubbyTossPriority` | Integer | Determines the priority order for the Nubby Toss action relative to other available actions. | 3 | `1` |
| [`NukeQuestFinalBossModifications`](./Engine_StatusAndPassiveKeys.md#object-nukequestfinalbossmodifications) | Object  | Contains modifications for the nuke quest final boss, such as damage_instance effects. | 2 | `{ . . . }` |
| `NumbingLeeches` | Integer | The number of leeches that apply a numbing effect, reducing the target's output or disabling certain actions. Also the name of a Necromancer passive. | 4 | `3` |
| `OneUseSpellDamageUp` | Integer | Increases spell damage by the specified amount, but the effect is consumed after a single use. Alias for SpellDamageUp. | 3 | `2` |
| `OverhealGainsBothShield` | Integer | Any healing beyond maximum health also grants shield points equal to the overheal amount. Value controls the conversion rate. | 2 | `1`<br>`2` |
| [`OverHealToStatuses`](./Engine_StatusAndPassiveKeys.md#object-overhealtostatuses) | Object  | Specifies a set of statuses applied to the target based on the amount of over-healing dealt. | 2 | `{ . . . }` |
| `ParasitesArentCursed` | Integer | Parasites attached to the unit are not considered cursed items, preventing negative curse effects. Value is a binary flag. | 2 | `1` |
| `passive0` | Enum | Specifies the first passive ability assigned to the unit from a predefined list (e.g., SelfAssured, HotBlooded). | 2 | `HotBlooded`<br>`SelfAssured` |
| [`PassiveAfterXKills`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveafterxkills) | Object  | Activates a set of passive effects (e.g., extra attacks, stat boosts) after the unit achieves a certain number of kills defined by the 'stacks' sub-key. | 4 | `{ . . . }` |
| [`PassiveAtFullHealth`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveatfullhealth) | Object  | Applies a set of passive effects (e.g., mana cost reduction, extra damage taken) only while the unit is at maximum health. | 2 | `{ . . . }` |
| [`PassiveAtInjuryThreshold`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveatinjurythreshold) | Object  | Applies a set of passive effects when the unit's injury level ('injury' sub-key) meets or exceeds the specified 'threshold' using the comparison 'mode'. | 2 | `{ . . . }` |
| [`PassiveEnergized`](./Engine_StatusAndPassiveKeys.md#object-passiveenergized) | Variable | Enables an electrified visual effect (using Particle_Electric particle) on the unit, indicating a charged or energized state. | 3 ||
| [`PassiveIfWeaponIsUsable`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveifweaponisusable) | Object  | Activates a set of passive effects (e.g., Brace) only if the unit's current weapon is in a usable condition (not broken or disabled). | 2 | `{ . . . }` |
| [`PassiveTar`](./Engine_StatusAndPassiveKeys.md#object-passivetar) | Variable | Enables a dripping tar particle effect (using Particle_TarDrip) on the unit, indicating a tar-related passive. | 3 ||
| [`PassiveUntilCastSpell`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveuntilcastspell) | Object  | Applies a set of passive effects (e.g., healing allies each turn) that remain active until the unit casts a spell. | 2 | `{ . . . }` |
| [`PassiveUntilGetKill`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passiveuntilgetkill) | Object  | Applies a set of passive effects (e.g., Holy Damage Blessing with burn) that remain active until the unit scores a kill. | 2 | `{ . . . }` |
| [`PassiveWhenTheAlpha`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhenthealpha) | Object  | Activates a set of passive effects (e.g., TogglableRoundEndExtraTurn) only while the unit holds the Alpha status on the team. | 2 | `{ . . . }` |
| [`PassiveWhileHasStatus`](../Reference_and_Meta/Miscellaneous.md#object-passivewhilehasstatus) | Object  | An object containing `status` and `passives` that grants the listed passives while the unit has the specified status. | 6 | `{ . . . }` |
| [`PassiveWhileInMonkMeleeStance`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhileinmonkmeleestance) | Object  | Applies specific passive effects (e.g., Brace, HealthRegenUp) while the unit is in the Monk's melee combat stance. | 3 | `{ . . . }` |
| [`PassiveWhileInMonkRangedStance`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhileinmonkrangedstance) | Object  | Applies specific passive effects (e.g., AddBonusRange, AddSpellDamage) while the unit is in the Monk's ranged combat stance. | 2 | `{ . . . }` |
| [`PassiveWhileNotHasStatus`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhilenothasstatus) | Object  | Specifies a set of passives that are active only when this unit does not have the given status. | 2 | `{ . . . }` |
| [`PassiveWhilePreviewingMonkRangedStance`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhilepreviewingmonkrangedstance) | Object  | Applies specific passive effects (e.g., AddBonusRange) while the unit is previewing the Monk's ranged stance before committing to it. | 2 | `{ . . . }` |
| [`PassiveWhileWearingMetal`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhilewearingmetal) | Object  | Applies a set of passive effects (e.g., AddElementsToWeapon with Electric) while the unit is equipped with metal armor or accessories. | 2 | `{ . . . }` |
| `PermanentItems` | Integer | The number of equipment slots that are immune to being unequipped or removed, permanently binding items to those slots. | 2 | `1`<br>`2` |
| `PermanentUpgradeRandomActive` | Integer | The number of random active abilities permanently upgraded. | 2 | `1`<br>`4` |
| `Phasing` | Integer | If set to 1, allows the character to phase through solid objects or obstacles. | 2 | `1` |
| [`PlayerCat_ThiefShade2`](./Engine_StatusAndPassiveKeys.md#object-playercat_thiefshade2) | Object  | A customization or modifier for the Thief Shade ability variant 2, altering its behavior or appearance for the player cat. | 3 | `{ . . . }` |
| `PoisonMultiplier` | Integer | A multiplier on all poison damage or poison stack application, increasing the potency of poison effects. | 1 | `2` |
| `Poop` | Object | A deployable object that acts as a hazard or obstacle, spawning a Poop movieclip with its own name and sound effects. | 22 | `{ . . . }` |
| `PrioritizeAggroTarget` | Integer | A priority weight for targeting the current aggro target. | 2 | `1` |
| `PrioritizePlayerCats` | Integer | A priority weight for targeting player-controlled cats. | 2 | `1` |
| `PrioritizeWeakestEnemy` | Integer | A priority weight for targeting the weakest enemy unit. | 2 | `1` |
| [`ProtectTargetedAllies`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-protecttargetedallies) | Object  | Specifies the ability used to protect targeted allies, including an optional target filter. | 4 | `{ . . . }` |
| [`QuakeAreaChance`](./Engine_StatusAndPassiveKeys.md#object-quakeareachance) | Object  | An object containing a radius and a chance to trigger a quake area effect. | 2 | `{ . . . }` |
| `Quiver` | Integer | Grants additional ammunition capacity or reload charges for ranged weapon abilities, increasing how many times they can be fired. | 6 | `1`<br>`2` |
| [`RandomDistanceDisplace`](./Engine_StatusAndPassiveKeys.md#object-randomdistancedisplace) | Integer / Object  | The number of stacks of a random distance displacement effect, or an object with stacks, min_dist, and chance. | 4 | `{ . . . }`<br>`20` |
| [`RandomKnockback`](./Engine_StatusAndPassiveKeys.md#object-randomknockback) | Object  | An object defining the minimum and maximum distance in tiles for a random knockback. | 2 | `{ . . . }` |
| `RandomLightning` | Integer | Chance per turn or action for a random lightning strike to occur, expressed as a percentage (e.g., 50%). | 2 | `50%` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 52 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`RandomTaggedMutation`](../Reference_and_Meta/Enums.md#enum-randomtaggedmutation) | Enum | Specifies the tag to filter random mutations by. | 2 | `bird`<br>`melted` |
| `RangedTrueShot` | Integer | Ranged attacks cannot miss or be dodged, guaranteeing a hit. Value acts as a binary flag. | 4 | `1` |
| [`RatKing`](./Engine_StatusAndPassiveKeys.md#object-ratking) | Object  | An ability or entity that spawns or controls a group of rats, applying swarm mechanics or empowered rat effects. | 5 | `{ . . . }` |
| [`ReaperRevenge`](./Engine_StatusAndPassiveKeys.md#object-reaperrevenge) | Object  | A teleport-based ability that damages the user while applying buffs (e.g., AllStatsUp) upon arrival at the target location. | 5 | `{ . . . }` |
| `RebukeDamage` | Integer | The amount of damage dealt by a rebuke backlash effect. | 2 | `1`<br>`2` |
| [`red`](../Reference_and_Meta/Miscellaneous.md#object-red) | Object  | Configuration for one of the dialog options (label 'EVENT_RED_ANSW'), with a fixed chance and associated animation, in a choice event. | 16 | `{ . . . }` |
| [`Reflect`](./Engine_StatusAndPassiveKeys.md#object-reflect) | Integer / Object  | The amount of reflect stacks applied. | 11 | `{ . . . }`<br>`1`<br>`5` |
| [`RefreshEquipmentAbilityOnElement`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-refreshequipmentabilityonelement) | Object  | Refreshes the cooldown of the unit's equipment ability when the unit's attack matches the specified element (e.g., Electric), displaying a recharge popup. | 2 | `{ . . . }` |
| `RefreshMoveOnWeaponConnect` | Integer | Grants an extra move action when the unit successfully lands a weapon hit. Value indicates the number of extra moves. | 1 | `1` |
| [`Regurge`](./Engine_StatusAndPassiveKeys.md#object-regurge) | Integer / Object  | The number of regurgitation triggers. | 5 | `{ . . . }`<br>`1` |
| [`Regurge`](./Engine_StatusAndPassiveKeys.md#object-regurge) | Integer / Object  | The number of regurgitation triggers. | 5 | `{ . . . }`<br>`1` |
| `ReloadOnKill` | Integer | If set, this ability's reload charge is restored on kill (any kill). | 2 | `1` |
| `ReloadOnKillEnemy` | Integer | If set, this ability's reload charge is restored only when killing an enemy. | 2 | `1` |
| `ReloadOnTotalDamageReceived` | Integer | The threshold of total damage received to restore a reload charge. | 2 | `15`<br>`25` |
| `RemoteLeech` | Integer | The amount of remote leech applied to the target on basic attack. | 2 | `1` |
| `RemoveLineOfSightRestrictions` | Integer | Line of sight requirements for targeting are ignored, allowing the unit to target any visible cell regardless of obstacles. | 3 | `1` |
| `RemoveOncePerFightRestriction` | Integer | Abilities or effects with a 'once per fight' limitation can be used multiple times per fight. Value acts as a binary flag. | 2 | `1` |
| `RepairArmorCondition` | Integer | The amount of armor condition restored. | 2 | `1` |
| [`ReplaceBasicAttack_Mutation`](../Reference_and_Meta/Enums.md#enum-replacebasicattack_mutation) | Enum | Specifies the mutation-based ability (e.g., FetusSpit) that replaces the unit's standard basic attack. | 1 | `FetusSpit` |
| [`ReplaceBasicAttackWhenDead`](../Reference_and_Meta/Enums.md#enum-replacebasicattackwhendead) | Enum | Specifies the ability (e.g., Haunt) that replaces the unit's basic attack when it is in a dead state. | 2 | `Haunt` |
| [`ReplaceBrain`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-replacebrain) | Object  | Defines a replacement AI brain and behavior pattern for the mutant. | 4 | `{ . . . }` |
| [`ReplaceSpellsWhenDead`](../Reference_and_Meta/Enums.md#enum-replacespellswhendead) | Enum | Specifies the spell set (e.g., Spook) that replaces the unit's normal spell list when it is in a dead state. | 1 | `Spook` |
| `ResetArmorShield` | Integer | The amount of armor shield restored. | 2 | `1` |
| `ReturnBoundItemOnBattleEnd` | Integer | If set to 1, items bound to this character are returned to their owner at the end of battle. | 2 | `1` |
| `ReviveOnWin` | Integer | Chance (as a percentage) for the unit to automatically revive after the battle ends, if it was dead at the time of victory. | 2 | `100%` |
| [`Robot`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-robot) | Integer / Object  | If an integer 1, the unit is robotic and affected by electric/energized effects. If an object, contains further robot-specific properties. | 49 | `{ . . . }`<br>`1` |
| `robot` | Variable | Indicates the unit is considered a robotic entity, potentially sharing interactions or restrictions with mechanical/robot-related systems. | 53 ||
| `RobotsInheritArmor` | Integer | Robots summoned or controlled by the unit inherit a percentage of the unit's armor value. Value controls the inheritance amount. | 2 | `1`<br>`2` |
| `RockDetector` | Integer | Grants the ability to detect or sense rock-type objects or terrain within the specified range (e.g., 10 tiles). | 2 | `10` |
| `SafeExplosions` | Integer | Explosions caused by the unit do not damage friendly units. Value acts as a binary flag. | 2 | `1` |
| [`Sandstorm`](./Engine_StatusAndPassiveKeys.md#object-sandstorm) | Object  | A self-buff ability that creates a sandstorm, applying a status effect (may be 'Sandstorm 1' or an object definition with a specific template). | 10 | `{ . . . }` |
| [`Sandstorm`](./Engine_StatusAndPassiveKeys.md#object-sandstorm) | Object  | A self-buff ability that creates a sandstorm, applying a status effect (may be 'Sandstorm 1' or an object definition with a specific template). | 10 | `{ . . . }` |
| [`ScaledStatusOnLoseShield`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-scaledstatusonloseshield) | Object  | Applies a scaled status effect (e.g., Thorns proportional to shield lost) when the unit loses shield points. Value includes a 'shield' sub-key for threshold. | 1 | `{ . . . }` |
| [`ScaledStatusOnOverHealed`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-scaledstatusonoverhealed) | Object  | An object containing status effect definitions to apply when the unit receives healing that exceeds its maximum health, with the number of stacks scaled by the amount of over-healing. | 1 | `{ . . . }` |
| [`ScaledStatusOnOverMana`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-scaledstatusonovermana) | Object  | An object containing status effect definitions to apply when the unit gains mana that exceeds its maximum mana, with the number of stacks scaled by the amount of over-mana. | 2 | `{ . . . }` |
| [`ScaledStatusOnSpendMana`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-scaledstatusonspendmana) | Object  | An object containing status effect definitions to apply when the unit spends mana, with the number of stacks scaled by the amount of mana spent. | 3 | `{ . . . }` |
| `ScrambleEverything` | Integer | The percentage chance to scramble all abilities and passives on the target. | 2 | `0`<br>`10%` |
| [`SecurityBotProtect`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-securitybotprotect) | Object  | Specifies the ability and movement used by a security bot to protect allies. | 8 | `{ . . . }` |
| `SelfStatusCarefulness` | Integer | The carefulness level when applying statuses to self, used to control stacking. | 2 | `1` |
| [`SelfStun`](../Reference_and_Meta/Arrays.md#array-selfstun) | Array / Integer | The number of stacks of self-stun applied, with an optional probability as a second element. | 2 | `1`<br>`[1 .5]` |
| [`SetDefaultFace`](../Reference_and_Meta/Enums.md#enum-setdefaultface) | Enum | Specifies the default facial expression, such as 'happy', 'sad', or 'insane'. | 3 | `happy`<br>`insane`<br>`sad` |
| [`SetItemAux`](./Engine_StatusAndPassiveKeys.md#object-setitemaux) | Object  | Configures an item's auxiliary value by specifying a target slot and a formula for the new value. | 3 | `{ . . . }` |
| `SetSpellCosts` | Integer | Overrides the cost of all spells to this value. | 8 | `0`<br>`1`<br>`3` |
| [`Shadowstep`](./Engine_StatusAndPassiveKeys.md#object-shadowstep) | Object  | An object defining the Shadowstep ability, which allows the unit to teleport behind a target before an attack. | 4 | `{ . . . }` |
| `ShareHealthRegen` | Integer | The amount of health regeneration shared with nearby allies. | 2 | `1` |
| [`SharePickups`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-sharepickups) | Object  | If 1 or an object with include_coins, makes the unit share pickups with nearby allies. | 3 | `{ . . . }` |
| [`Shatter`](./Engine_StatusAndPassiveKeys.md#object-shatter) | Integer / Object  | The amount of damage dealt when a frozen or petrified status is shattered, or a template definition for a Shatter ability. | 5 | `{ . . . }`<br>`15` |
| [`ShortCircuit`](./Engine_StatusAndPassiveKeys.md#object-shortcircuit) | Integer / Object  | The number of stacks of the ShortCircuit status effect. | 7 | `{ . . . }`<br>`1` |
| [`ShortCircuit`](./Engine_StatusAndPassiveKeys.md#object-shortcircuit) | Integer / Object  | The number of stacks of the ShortCircuit status effect. | 7 | `{ . . . }`<br>`1` |
| `ShoulderCheck` | Integer | The chance (as a percentage) to perform a Shoulder Check, pushing a target back after a melee attack. | 5 | `100%`<br>`33%` |
| [`ShovingMatch`](../Reference_and_Meta/Enums.md#enum-shovingmatch) | Enum | Determines which stat (e.g., 'attack') is used for the Shoving Match shoving contest. | 5 | `attack` |
| `SignalFinalBossShieldBroke` | Integer | If set to a non-zero number, signals that the final boss's shield has been broken. | 2 | `1` |
| [`SleepDart2`](./Engine_StatusAndPassiveKeys.md#object-sleepdart2) | Object  | An object defining the Sleep Dart 2 status, which puts a target to sleep on hit. | 3 | `{ . . . }` |
| [`SlotMachineRollPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-slotmachinerollpool) | Object  | Defines the weighted pool of possible slot machine roll results. | 2 | `{ . . . }` |
| `SmallEnemiesIgnoreYou` | Integer | If non-zero, enemies considered 'small' will ignore this unit and not target it. | 2 | `1` |
| [`SmellBlood`](./Engine_StatusAndPassiveKeys.md#object-smellblood) | Integer / Object  | If non-zero, activates the Smell Blood ability which reveals nearby injured units. | 5 | `{ . . . }`<br>`1` |
| [`SmellBlood`](./Engine_StatusAndPassiveKeys.md#object-smellblood) | Integer / Object  | If non-zero, activates the Smell Blood ability which reveals nearby injured units. | 5 | `{ . . . }`<br>`1` |
| [`SmiteEnemiesWhoKill`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-smiteenemieswhokill) | Object  | An object defining a smite effect applied to enemies who kill another unit, typically dealing damage and applying a stun. | 2 | `{ . . . }` |
| [`SparkleBuff`](./Engine_StatusAndPassiveKeys.md#object-sparklebuff) | Variable | A variable defining a sparkle particle effect buffer for visual feedback. | 3 ||
| `SpawnBearTrapOnMiss` | Integer | The number of bear traps to spawn on the tile adjacent to the target when the unit misses an attack. | 2 | `1` |
| [`SpawnCatCopyWhenDowned`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawncatcopywhendowned) | Object  | An object defining a cat copy to spawn when the unit is downed, typically a shade or specter. | 2 | `{ . . . }` |
| [`SpawnExtraThingsOnBattleStart`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnextrathingsonbattlestart) | Object  | An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start. | 32 | `{ . . . }` |
| [`SpawnItemLinkedFamiliar`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnitemlinkedfamiliar) | Object  | An object defining a familiar to spawn that is linked to a specific item, which breaks when the familiar is defeated. | 2 | `{ . . . }` |
| [`SpawnMeatOnMove`](../Reference_and_Meta/Enums.md#enum-spawnmeatonmove) | Enum | Specifies the type of meat object (e.g., 'Food') to spawn on the tile the unit moves from. | 1 | `Food` |
| `SpawnNearEnemies` | Integer | The number of units to spawn near each enemy at the start of battle. | 2 | `1` |
| [`SpawnObjectOnPopCorpse`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnobjectonpopcorpse) | Enum / Object  | Specifies an object (as a string or an object with 'object', 'count', 'except_tiny' keys) to spawn on a corpse when it is popped. | 6 | `{ . . . }`<br>`Catnip`<br>`Coin`<br>`Food` |
| [`SpecialFriends`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-specialfriends) | Object  | An object containing a set of status effects applied to allied units that are considered 'special friends' (e.g., granted by a passive). | 4 | `{ . . . }` |
| [`SpecialGodRays`](./Engine_StatusAndPassiveKeys.md#object-specialgodrays) | Object  | An object defining visual god rays that follow a specific character tag, used for cinematic or boss effects. | 2 | `{ . . . }` |
| [`SpikeBuff`](./Engine_StatusAndPassiveKeys.md#object-spikebuff) | Variable | A variable defining a spike/bramble particle effect buffer for visual feedback. | 3 ||
| `SplittableMove` | Integer | The number of times a move action can be split into smaller segments. | 2 | `1`<br>`3` |
| [`Spook`](./Engine_StatusAndPassiveKeys.md#object-spook) | Object  | An object defining the Spook status, which causes the affected unit to flee or become frightened. | 3 | `{ . . . }` |
| `SpreadExtraDebuffs` | Integer | The number of additional debuffs to spread to nearby enemies when applying a debuff. | 2 | `1`<br>`2` |
| `SpreadPainBonus` | Integer | The amount of bonus damage dealt to enemies who are also affected by the Spread Pain effect. | 2 | `2` |
| `SpreadPainBonusCrit` | Integer | The additional critical hit chance against enemies affected by Spread Pain. | 1 | `1` |
| [`StackingDodgeChanceOnTookDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stackingdodgechanceontookdamage) | Object  | An object with 'amount' (percent) and 'cap' (percent) defining a stacking dodge chance buff that increases each time the unit takes damage, up to a maximum. | 1 | `{ . . . }` |
| `StatMinimum` | Integer | The minimum value that a particular stat cannot fall below. | 2 | `5`<br>`7` |
| [`StatsAtLowHealth`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statsatlowhealth) | Object  | An object containing a 'threshold' (health value) and stat bonuses (e.g., 'strength', 'speed') that are applied when the unit's health is below the threshold. | 2 | `{ . . . }` |
| [`StatusAfterCastSpell`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusaftercastspell) | Object  | An object containing status effects to apply to the unit immediately after it casts any spell. | 4 | `{ . . . }` |
| [`StatusAfterXTurns`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusafterxturns) | Object  | Applies a status effect or forces an ability usage after a set number of turns. | 2 | `{ . . . }` |
| [`StatusAlliesOnBattleStart`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusalliesonbattlestart) | Object  | An object containing status effects to apply to all allies at the start of battle. | 10 | `{ . . . }` |
| [`StatusAlliesOnGainCoins`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusalliesongaincoins) | Object  | An object containing status effects to apply to allies when the unit gains coins, with an optional 'scaled' boolean to scale stacks. | 2 | `{ . . . }` |
| [`StatusAlliesOnKill`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusalliesonkill) | Object  | An object containing status effects to apply to all allies when any ally kills an enemy. | 4 | `{ . . . }` |
| [`StatusAlliesOnSpendMana`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusalliesonspendmana) | Object  | An object containing status effects to apply to allies when the unit spends mana. | 1 | `{ . . . }` |
| [`StatusAlliesScaledByCursedOnDeath`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusalliesscaledbycursedondeath) | Object  | An object containing status effects to apply to allies when the unit dies, with stacks scaled by the number of Cursed stacks the unit had. | 1 | `{ . . . }` |
| [`StatusAllyWhenAllySpendsMana`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusallywhenallyspendsmana) | Object  | An object with a 'threshold' (mana amount) and status effects to apply to an ally whenever any ally spends at least that much mana. | 2 | `{ . . . }` |
| [`StatusAnyCatAllyWhoKills`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusanycatallywhokills) | Object  | An object containing status effects to apply to any cat ally who kills an enemy. | 2 | `{ . . . }` |
| `StatusCarefulness` | Integer | The carefulness level when applying statuses, used to control stacking behavior. | 3 | `1` |
| [`StatusCharactersOnRoundStart`](./Engine_StatusAndPassiveKeys.md#object-statuscharactersonroundstart) | Object  | An object containing status effects to apply to all characters on the battlefield at the start of each round. | 2 | `{ . . . }` |
| [`StatusDamagers`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusdamagers) | Object  | An object defining status effects that damage the unit, with parameters for each status. | 2 | `{ . . . }` |
| [`StatusEachRoundEnd`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachroundend) | Object  | An object listing status effects applied to the unit at the end of each round. | 3 | `{ . . . }` |
| [`StatusEachTurnEndForEachTurn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnendforeachturn) | Object  | Statuses applied at the end of each turn, with the number of turns as nested values. | 4 | `{ . . . }` |
| [`StatusEachTurnEndPerEnemyKill`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnendperenemykill) | Object  | An object containing status effects to apply at the end of each turn for each enemy killed during that turn. | 2 | `{ . . . }` |
| [`StatusEnemiesOnDeath`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusenemiesondeath) | Object  | An object containing status effects to apply to all enemies when the unit dies. | 2 | `{ . . . }` |
| [`StatusEveryXSpellCastsEachTurn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseveryxspellcastseachturn) | Object  | An object with a 'stacks' value defining status effects applied every X spell casts within a single turn. | 1 | `{ . . . }` |
| [`StatusEveryXTurnBegins`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseveryxturnbegins) | Object  | An object with a 'turns' value defining status effects applied every X turns at the start of the turn. | 2 | `{ . . . }` |
| [`StatusIfDidntMove`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusifdidntmove) | Object  | An object containing status effects to apply to the unit if it did not move during its turn. | 1 | `{ . . . }` |
| [`StatusIfUnusedActPoints`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusifunusedactpoints) | Object  | An object containing status effects to apply to the unit if it has unused action points at the end of its turn. | 2 | `{ . . . }` |
| [`StatusKillers`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuskillers) | Object  | An object containing nested conditionals that apply status effects when the unit kills an enemy. | 3 | `{ . . . }` |
| [`StatusOnAnyDeath`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonanydeath) | Object  | An object containing status effects to apply whenever any unit (ally or enemy) dies. | 2 | `{ . . . }` |
| [`StatusOnBackstab`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonbackstab) | Object  | An object containing status effects to apply when the unit performs a backstab attack. | 2 | `{ . . . }` |
| [`StatusOnBattleEndIfKillThresholdMet`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonbattleendifkillthresholdmet) | Object  | An object containing a 'kills' threshold and status effects to apply at the end of battle if the unit's kill count meets or exceeds the threshold. | 2 | `{ . . . }` |
| [`StatusOnBattleStart`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonbattlestart) | Object  | An object containing status effects to apply to the unit at the start of every battle. | 16 | `{ . . . }` |
| [`StatusOnBreakItem`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonbreakitem) | Object  | An object containing status effects to apply when the unit breaks a weapon or armor item. | 4 | `{ . . . }` |
| [`StatusOnCollectPickup`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusoncollectpickup) | Object  | An object containing status effects to apply when the unit collects a pickup item. | 3 | `{ . . . }` |
| [`StatusOnDealtDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusondealtdamage) | Object  | An object containing status effects to apply to the unit whenever it deals damage to an enemy. | 2 | `{ . . . }` |
| [`StatusOnDealtDamageThreshold`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusondealtdamagethreshold) | Object  | Specifies the effects applied when the unit deals damage equal to or exceeding the defined threshold. | 2 | `{ . . . }` |
| [`StatusOnDie`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusondie) | Object  | Specifies status effects or actions triggered when the unit dies. | 9 | `{ . . . }` |
| [`StatusOnEatPill`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusoneatpill) | Object  | Specifies the effects applied when the unit consumes a pill item. | 2 | `{ . . . }` |
| [`StatusOnGainShield`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusongainshield) | Object  | Specifies the effects applied when the unit gains a shield. | 2 | `{ . . . }` |
| [`StatusOnHeal`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonheal) | Object  | Specifies the effects applied when the unit receives healing. | 2 | `{ . . . }` |
| [`StatusOnKillEnemy`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonkillenemy) | Object  | Specifies the effects applied when the unit kills an enemy. | 11 | `{ . . . }` |
| [`StatusOnOverMana`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonovermana) | Object  | Specifies the effects applied when the unit's mana exceeds its maximum. | 2 | `{ . . . }` |
| [`StatusOnPickupCoins`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonpickupcoins) | Object  | Specifies the effects applied when the unit picks up coins. | 3 | `{ . . . }` |
| [`StatusOnPopCorpse`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonpopcorpse) | Object  | Specifies the effects applied when the unit pops a corpse. | 5 | `{ . . . }` |
| [`StatusOnSetPieceBreak`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonsetpiecebreak) | Object  | Specifies the effects applied when the unit breaks a set piece. | 2 | `{ . . . }` |
| [`StatusOnSpawnIn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonspawnin) | Object  | Applies statuses or actions upon the unit spawning into the battlefield. | 2 | `{ . . . }` |
| [`StatusOnTookDamageFromEnemyAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusontookdamagefromenemyability) | Object  | Specifies the effects applied when the unit takes damage from an enemy ability. | 2 | `{ . . . }` |
| [`StatusOnTriggerTrap`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusontriggertrap) | Object  | Specifies the effects applied when the unit triggers a trap. | 2 | `{ . . . }` |
| [`StatusOnUseBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonusebasicattack) | Object  | Specifies the effects applied when the unit performs a basic attack. | 3 | `{ . . . }` |
| [`StatusOnUseElementAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonuseelementability) | Object  | Specifies the effects applied when the unit uses an ability matching the specified element. | 2 | `{ . . . }` |
| [`StatusPerInjury`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusperinjury) | Object  | Specifies the effects granted per injury the unit has, up to an optional cap. | 2 | `{ . . . }` |
| [`StatusReplacement`](../Reference_and_Meta/Arrays.md#array-statusreplacement) | Array | Specifies status replacements, where the first status is replaced by the second when applied. | 2 | `[Petrify PetrifyCharmed]` |
| [`StatusThingsKnockedBack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusthingsknockedback) | Object  | Specifies the effects applied when the unit knocks back another unit. | 2 | `{ . . . }` |
| [`StatusWhenAllySpendsMana`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuswhenallyspendsmana) | Object  | Specifies the effects applied when an ally spends mana. | 3 | `{ . . . }` |
| `StrengthForEachNeighboringEnemy` | Integer | The amount of strength gained for each adjacent enemy. | 3 | `2`<br>`3` |
| `StrengthInNumbersAura` | Integer | The amount of strength gained per nearby ally within the aura. | 2 | `1` |
| `Study` | Integer | The number of stacks of the Study status applied. | 4 | `1` |
| `SurviveAt1HP` | Integer | If 1, the unit survives a fatal hit with 1 HP instead of dying. | 2 | `1` |
| `SwallowSmallCharacter` | Integer | The percentage chance to swallow a smaller character on hit. | 2 | `100%`<br>`50%` |
| `SwapHighestAndLowestStat` | Integer | If non-zero, swaps the unit's highest base stat value with its lowest. | 2 | `1` |
| [`Switcheroo`](./Engine_StatusAndPassiveKeys.md#object-switcheroo) | Integer / Object  | The number of stacks of the Switcheroo status effect. | 5 | `{ . . . }`<br>`1` |
| [`Switcheroo`](./Engine_StatusAndPassiveKeys.md#object-switcheroo) | Integer / Object  | The number of stacks of the Switcheroo status effect. | 5 | `{ . . . }`<br>`1` |
| [`TaggedPickupEffectReplacement`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-taggedpickupeffectreplacement) | Object  | Specifies a replacement effect for picking up items with a given tag. | 2 | `{ . . . }` |
| `TempCounterAttack` | Integer | The number of turns TempCounterAttack lasts, ticking down at the start of the unit's turn. | 4 | `1` |
| `TempCritChanceUp` | Integer | The amount of temporary critical hit chance (in percentage points) added. | 3 | `100`<br>`30` |
| `TempNoManaRegen` | Integer | The number of turns the unit cannot regenerate mana. | 2 | `1` |
| `ThornsDamageImmuneUntilSettled` | Integer | The number of turns the target is immune to thorns damage until it settles. | 2 | `1` |
| `TileDamageImmuneUntilSettled` | Integer | The number of turns the target is immune to tile damage until it settles. | 2 | `1` |
| `TileDamageMultiplier` | Integer | Multiplier for damage dealt to environmental tiles. | 2 | `2` |
| [`TinkererBasicAttackSwitching`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-tinkererbasicattackswitching) | Object  | Defines the abilities used for the Tinkerer's basic attack switching mechanic. | 3 | `{ . . . }` |
| [`TowerDefense`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-towerdefense) | Object  | Specifies the range and damage of the Tower Defense counterattack. | 6 | `{ . . . }` |
| [`TowerDefenseReflex`](../Reference_and_Meta/Enums.md#enum-towerdefensereflex) | Enum | Specifies the ability or attack used when the unit counterattacks in tower defense reflex mode. | 3 | `BasicRanged_1DMG`<br>`attack` |
| [`TradeLife`](./Engine_StatusAndPassiveKeys.md#object-tradelife) | Integer / Object  | The amount of health life traded, or a template for a TradeLife ability. | 6 | `{ . . . }`<br>`1` |
| [`TradeLife`](./Engine_StatusAndPassiveKeys.md#object-tradelife) | Integer / Object  | The amount of health life traded, or a template for a TradeLife ability. | 6 | `{ . . . }`<br>`1` |
| [`TrailBlazer`](./Engine_StatusAndPassiveKeys.md#object-trailblazer) | Enum / Integer / Object  | The number of trail blazer stacks applied, or a string alias like 'mov'. | 5 | `{ . . . }`<br>`1`<br>`mov` |
| [`TrailBlazer`](./Engine_StatusAndPassiveKeys.md#object-trailblazer) | Enum / Integer / Object  | The number of trail blazer stacks applied, or a string alias like 'mov'. | 5 | `{ . . . }`<br>`1`<br>`mov` |
| [`TransformOnElementInfluencex`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-transformonelementinfluencex) | Object  | Transforms into a specified object when influenced by a given element. | 2 | `{ . . . }` |
| [`TransformWhenBuddyDies`](../Reference_and_Meta/Enums.md#enum-transformwhenbuddydies) | Enum | Specifies the form the unit transforms into when its buddy dies. | 2 | `UltraOrnstein`<br>`UltraSmough` |
| `TrapEffectsMultiplier` | Integer | Multiplier for the potency of trap effects triggered by the unit. | 2 | `2` |
| `TriggerDOTStatuses` | Integer | If set to 1, triggers damage over time statuses on the target immediately. | 2 | `0`<br>`1` |
| `triggers_limit` | Integer | The maximum number of times this passive effect can trigger per battle. | 2 | `1` |
| `TrinketActiveEffectsMultiplierBonus` | Integer | Bonus multiplier to the active effects of equipped trinkets. | 6 | `1`<br>`2` |
| `TrinketPassiveMultiplierBonus` | Integer | Bonus multiplier to the passive effects of equipped trinkets. | 10 | `1`<br>`2` |
| `UncappedHP` | Integer | If 1, the unit's maximum HP is not capped by standard limits. | 4 | `1` |
| `UncappedHPBonusStr` | Integer | The amount of strength gained per point of HP exceeding the maximum cap. | 1 | `5` |
| `Uncontrollable` | Integer | If non-zero, the unit becomes uncontrollable by the player. | 6 | `1` |
| `UnlockOrientation` | Integer | If 1, allows the unit to freely rotate or face any direction regardless of movement. | 2 | `1` |
| [`UpgradeLevelUpClassActives`](../Reference_and_Meta/Enums.md#enum-upgradelevelupclassactives) | Enum | Specifies the upgrade path for class active abilities on level up. | 2 | `Colorless` |
| [`UpgradeLevelUpClassPassives`](../Reference_and_Meta/Enums.md#enum-upgradelevelupclasspassives) | Enum | Specifies the upgrade path for class passive abilities on level up. | 2 | `Colorless` |
| `UpgradeSpawnedPickups` | Integer | The number of times spawned pickups are upgraded in quality. | 3 | `1`<br>`2` |
| [`UpgradeTaggedSpawnsToChampions`](../Reference_and_Meta/Enums.md#enum-upgradetaggedspawnstochampions) | Enum | Specifies which tag of spawns are upgraded to champion versions. | 2 | `bug`<br>`worm` |
| `Vengeful` | Integer | The number of Vengeful stacks, causing retaliation damage when hit. | 4 | `1` |
| `VisualFlySwarm` | Integer | If non-zero, enables the visual fly swarm effect on the unit. | 3 | `1` |
| `WeaponActiveEffectsMultiplierBonus` | Integer | Bonus multiplier to the active effects of the equipped weapon. | 2 | `2` |
| `WeaponCountsAsBasicAttack` | Integer | If non-zero, the weapon's ability counts as a basic attack. | 2 | `1` |
| `WeaponDamageMultiplierBonus` | Integer | Bonus multiplier to weapon damage. | 3 | `1`<br>`2` |
| `WeaponPassiveMultiplierBonus` | Integer | Bonus multiplier to the passive effects of the equipped weapon. | 2 | `2` |
| `WeaponsDontLoseDurability` | Integer | If set to 1, weapons equipped by this unit do not lose durability. | 4 | `0`<br>`1` |
| [`XIsLivingCharactersWithTag`](../Reference_and_Meta/Enums.md#enum-xislivingcharacterswithtag) | Enum | Specifies the tag that living characters must have for this passive to affect them. | 2 | `husk`<br>`rock` |
| `XIsOtherHealsThisTurn` | Integer | If set, tracks other heals this turn for some effect. | 2 | `1` |
| [`XIsSpellStormRampAndReset`](./Engine_StatusAndPassiveKeys.md#object-xisspellstormrampandreset) | Integer / Object  | If integer 0, resets stacks; if object, contains 'stacks' and 'reset_percent' for spell storm ramp. | 2 | `{ . . . }`<br>`0` |
| [`XIsTargetHealth`](./Engine_StatusAndPassiveKeys.md#object-xistargethealth) | Object  | Evaluates a bonus damage formula where X is the target's current health. | 2 | `{ . . . }` |
| `XIsTimesDamageTaken` | Integer | If set, multiplier for damage taken to apply some effect. | 2 | `1` |
| `Zombie` | Number | The number of stacks or value for the Zombie status. | 10 | `1` |
| `AbilityDamageMultiplier` | Float | Multiplier for all ability damage dealt by the unit. | 1 | `1.5` |
| `AbilityDisableIfLivingCrow` | Integer | If set, disables the ability if there is a living crow on the field. | 1 | `1` |
| `AbilityEnabledAtHealthThreshold` | Integer | The health percentage threshold at which the ability becomes enabled. | 1 | `50%` |
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Integer | If set, ability is enabled only if the unit used a basic attack this turn. | 1 | `1` |
| `AbilityEnabledIfMovementTrapped` | Integer | If set, ability is enabled only when the unit's movement is trapped. | 1 | `1` |
| `AbilityEnabledIfNoAggroTarget` | Integer | If set, ability is enabled only when the unit has no aggro target. | 1 | `1` |
| [`AbilityEnabledIfNotHasStatus`](../Reference_and_Meta/Enums.md#enum-abilityenabledifnothasstatus) | Enum | Specifies the status that must be absent for ability to be enabled. | 1 | `BackflipWhenTargeted` |
| [`AbilityEnabledIfSpecificItemEquipped`](../Reference_and_Meta/Enums.md#enum-abilityenabledifspecificitemequipped) | Enum | Specifies the item that must be equipped for ability to be enabled. | 1 | `Neverstone` |
| [`AbilityOnBattleStart_UseAI`](../Reference_and_Meta/Enums.md#enum-abilityonbattlestart_useai) | Enum | Specifies the ability the unit will use at the start of battle via AI resolution. | 1 | `TheCreator_SpawnCloneTeam` |
| [`AbilityOnRoundEndOnce`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-abilityonroundendonce) | Object  | Specifies an ability to be used once at the end of the round. | 1 | `{ . . . }` |
| `AbsorbManaFromOtherSpells` | Integer | If set, this ability absorbs mana from other spells when cast. | 1 | `1` |
| `AcidRain` | Integer | If non-zero, enables the Acid Rain weather effect dealing damage each turn. | 4 | `2` |
| [`AddAdvantageToEvent`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addadvantagetoevent) | Object  | Specifies additional advantage options to add to a specific event type. | 1 | `{ . . . }` |
| `AddAllyNeighborsToAttackRange` | Integer | The number of ally-occupied tiles added to the unit's attack range. | 1 | `1` |
| `AddConstitution` | Integer | The amount of constitution added to the unit. | 1 | `2` |
| [`AddElementsToSpells`](../Reference_and_Meta/Enums.md#enum-addelementstospells) | Enum | Specifies which element to add to spells. | 1 | `Earth` |
| `AddExtraTurnsBeforeRun` | Integer | The number of additional turns added before the run ends. | 1 | `2` |
| `AddLevelUpStatMultiplier` | Integer | Multiplier applied to stat gains on level up. | 1 | `1` |
| [`AddPostProcessEffect`](./Engine_StatusAndPassiveKeys.md#object-addpostprocesseffect) | Object  | Specifies a post-process shader effect to apply to the scene. | 1 | `{ . . . }` |
| `AddRandomEliteBuff` | Integer | The number of random elite buffs to apply to the unit. | 1 | `1` |
| [`AddStatusesIfPersistentWeatherElement`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatusesifpersistentweatherelement) | Object  | Specifies statuses applied if the persistent weather matches the given elements. | 1 | `{ . . . }` |
| [`AddStatusesToReceivedElementalDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatusestoreceivedelementaldamage) | Object  | An object defining statuses applied to the unit when it takes elemental damage of the specified types. | 1 | `{ . . . }` |
| [`AddStatusToBackstabs`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobackstabs) | Object  | An object defining statuses applied to the target when the unit performs a backstab attack. | 1 | `{ . . . }` |
| [`AddStatusToFirstSpellEachTurn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustofirstspelleachturn) | Object  | An object defining statuses applied to the target after the first spell cast by the unit each turn. | 1 | `{ . . . }` |
| [`AddStatusToReceivedDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoreceiveddamage) | Object  | Applies a status effect to the attacker when the unit takes damage. | 1 | `{ . . . }` |
| [`AddStatusToReceivedDamage_ExcludeStatuses`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoreceiveddamage_excludestatuses) | Object  | An object defining statuses applied to the attacking unit when the owner receives damage, excluding damage from sources carrying the specified statuses. | 1 | `{ . . . }` |
| [`AddTilesetObjects`](./Engine_StatusAndPassiveKeys.md#object-addtilesetobjects) | Object  | An object configuring the spawning of decorative debris or objects on the tileset for an effect. | 1 | `{ . . . }` |
| `Adrenaline` | Integer | The flat amount of Adrenaline (a resource or stat) granted to the unit. | 2 | `10` |
| [`AdvancedTint`](../Reference_and_Meta/Arrays.md#array-advancedtint) | Array | An RGBA color array for advanced sprite tinting. | 1 | `[` |
| [`AdventureTokenPassivePool`](../Reference_and_Meta/Miscellaneous.md#object-adventuretokenpassivepool) | Object  | A pool of passive definitions granted to the unit when picked up as an adventure token. | 1 | `{ . . . }` |
| [`AggroTargetIsGovernedByHitEffect`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-aggrotargetisgovernedbyhiteffect) | Object  | If set, the aggro target is determined by the unit's hit effect, with a sub-key for enemies_only. | 1 | `{ . . . }` |
| `AggroTargetIsLastEnemyThatDealtDamage` | Integer | If 1, the unit's aggro target is the last enemy that damaged it. | 1 | `1` |
| `AggroTargetIsLowestHealthEnemyTillItDies` | Integer | If 1, the unit focuses the lowest health enemy until that enemy dies. | 1 | `1` |
| `AggroTargetIsLowestMaxHealthCat` | Integer | If 1, the unit targets the cat ally with the lowest maximum health. | 1 | `1` |
| [`AIControlNextTurn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-aicontrolnextturn) | Object  | An object that causes the unit to be controlled by the AI on its next turn, with configurable stacks and spell usage. | 1 | `{ . . . }` |
| `AIFavorLowHealth` | Integer | The AI's favorability weight for targeting low-health units. | 1 | `100` |
| [`AlienBeastDangerZones`](../Reference_and_Meta/Arrays.md#array-alienbeastdangerzones) | Array | An array of ability names that mark dangerous zones for the Alien Beast fight. | 1 ||
| `AlienBeastEyeStalks` | Integer | The number of eye stalk segments on the Alien Beast. | 1 | `3` |
| `all_spells` | Variable | A variable representing a collection of every spell definition available in the game. | 1 ||
| `AlliesScrambleSpellAfterCast` | Integer | The number of times an ally's next spell cast will be scrambled (randomly redirected or modified) after the owner casts a spell. | 1 | `1` |
| `AlliesTakeExtraTurn` | Integer | The number of extra turns granted to allies. | 1 | `1` |
| `AllSpellsCostActPoints` | Integer | If 1, all spells require action points instead of mana or other resources. | 1 | `1` |
| `AllSpellsCostCharge` | Integer | The number of charges required to cast any spell, adding a universal charge cost. | 1 | `1` |
| [`AllStatsAura`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-allstatsaura) | Object  | An aura that grants bonus stacks of all stats to allies within range. | 1 | `{ . . . }` |
| `AllUnitsExplodeOnDeath` | Integer | The radius of the explosion that triggers when any unit dies. | 1 | `5` |
| [`AlluringDoodieEater`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-alluringdoodieeater) | Object  | An object defining the chance and damage instance for a unit that consumes an alluring doodie. | 1 | `{ . . . }` |
| [`AllyDodgeChanceAura`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-allydodgechanceaura) | Object  | An object granting allies within a specified range a percentage chance to dodge incoming attacks. | 2 | `{ . . . }` |
| `AlphaAllStatsUp` | Integer | The amount by which all of the unit's stats are increased if it is the alpha (highest stat total or designated leader). | 2 | `1` |
| `AlphaDodgeChance` | Integer | The dodge chance granted to the alpha (leader) unit. | 2 | `50%` |
| [`AlphaStatusOnTurnBegin`](./Engine_StatusAndPassiveKeys.md#object-alphastatusonturnbegin) | Object  | Specifies status effects applied to the alpha at the start of each turn. | 1 | `{ . . . }` |
| [`AlternateIdleAnimation`](../Reference_and_Meta/Enums.md#enum-alternateidleanimation) | Enum | Specifies the name of an alternative idle animation to play. | 1 | `berserkIdle` |
| `AlwaysChosenForLevelUp` | Integer | If set to 1, this unit is always presented as a level-up option when gaining a level. | 1 | `1` |
| `AOEBonus` | Integer | The bonus number of additional targets or tiles affected by an area-of-effect ability. | 1 | `1` |
| [`ApplyPassivesToSpawnerWhileAlive`](./Engine_StatusAndPassiveKeys.md#object-applypassivestospawnerwhilealive) | Object  | An object defining passives that are applied to the spawner while this unit is alive. | 1 | `{ . . . }` |
| `ApplyShieldToApplierBasedOnMaxHealth` | Integer | The amount of shield applied to the applier based on a fraction of their max health. | 1 | `1` |
| [`ApplyStatusesNextTurnBegin`](./Engine_StatusAndPassiveKeys.md#object-applystatusesnextturnbegin) | Object  | Specifies a set of statuses to apply to the target at the beginning of their next turn. | 1 | `{ . . . }` |
| [`ApplyToOthersWithSharedTagAndFaction`](./Engine_StatusAndPassiveKeys.md#object-applytootherswithsharedtagandfaction) | Object  | Specifies statuses to apply to other units that share a tag and faction with the target. | 1 | `{ . . . }` |
| [`ApplyToRandomClosestAlly`](./Engine_StatusAndPassiveKeys.md#object-applytorandomclosestally) | Object  | Specifies statuses to apply to a random ally closest to the target. | 1 | `{ . . . }` |
| [`Autism`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-autism) | Object  | An object defining the Autism disorder, including its name, description, class, and stat modifications for innate and learned levels. | 4 | `{ . . . }` |
| `AvoidDamagingCharmedEnemies` | Integer | If 1, the unit avoids dealing damage to charmed enemies. | 1 | `1` |
| `AwardCoinsOnDeath` | Integer | The amount of coins awarded to the killer when this unit dies. | 1 | `10` |
| `BackstabWeakness` | Float | A multiplier for damage taken from backstab attacks. | 1 | `0.75` |
| `BalanceStats` | Integer | If set to 1, the unit's stats are balanced (redistributed) towards an average value. | 1 | `1` |
| `BasicAIDangerZone` | Integer | The radius of the danger zone used by the basic AI for area denial. | 1 | `2` |
| [`BasicAttackStatusSwap`](../Reference_and_Meta/Arrays.md#array-basicattackstatusswap) | Array | An array of two status IDs; when the unit performs a basic attack, the first status is removed and the second is applied in its place. | 1 | `[TempDamageUp DamageUp]` |
| [`BasicButcherMelee`](./Engine_StatusAndPassiveKeys.md#object-basicbutchermelee) | Object  | An object defining a basic melee attack for the Butcher class. | 5 | `{ . . . }` |
| [`BasicDruidAbility`](./Engine_StatusAndPassiveKeys.md#object-basicdruidability) | Object  | An object defining a basic ability for the Druid class. | 3 | `{ . . . }` |
| [`BasicMagicShortRanged`](./Engine_StatusAndPassiveKeys.md#object-basicmagicshortranged) | Object  | An object defining a basic short-ranged magical attack. | 5 | `{ . . . }` |
| [`BasicMedicMelee`](./Engine_StatusAndPassiveKeys.md#object-basicmedicmelee) | Object  | An object defining a basic melee attack for the Medic class. | 5 | `{ . . . }` |
| [`BasicMelee_4Hits`](./Engine_StatusAndPassiveKeys.md#object-basicmelee_4hits) | Object  | An object defining a variant of the basic melee attack that hits the target 4 times. | 2 | `{ . . . }` |
| [`BasicNecroRanged`](./Engine_StatusAndPassiveKeys.md#object-basicnecroranged) | Object  | An object defining a basic ranged attack for the Necromancer class. | 5 | `{ . . . }` |
| [`BasicPsychicPull`](./Engine_StatusAndPassiveKeys.md#object-basicpsychicpull) | Object  | An object defining a basic psychic ability that pulls a target towards the caster. | 5 | `{ . . . }` |
| [`BattlefieldUniqueRandomPassive`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-battlefielduniquerandompassive) | Object  | A pool of unique random passives that can be applied to each battlefield instance. | 1 | `{ . . . }` |
| [`BBTransformMutant`](./Engine_StatusAndPassiveKeys.md#object-bbtransformmutant) | Object  | An object defining a transformation spell that turns the unit into a mutant. | 5 | `{ . . . }` |
| [`BBTransformZealot`](./Engine_StatusAndPassiveKeys.md#object-bbtransformzealot) | Object  | An object defining a transformation spell that turns the unit into a zealot. | 5 | `{ . . . }` |
| [`BiggestFood`](./Engine_LogicKeys.md#object-biggestfood) | Integer / Object  | The number of biggest food pickups spawned. | 9 | `{ . . . }`<br>`1`<br>`15`<br>`4` |
| `BigSplashDamage` | Integer | The additional tile radius of the splash damage effect applied by an attack. | 1 | `2` |
| `BlackHolePassive` | Integer | If 1, the unit has black hole passive mechanics. | 1 | `1` |
| `BlackHoleSuck` | Integer | The strength of the black hole's pull effect. | 1 | `1` |
| `BlessingOfPeace` | Integer | The number of stacks of the Blessing of Peace status applied to the unit each turn. | 2 | `1` |
| [`BloatEyeMovement2`](./Engine_StatusAndPassiveKeys.md#object-bloateyemovement2) | Object  | An object defining a movement ability for the Bloat Eye enemy. | 3 | `{ . . . }` |
| [`BloatEyePassive2`](../Reference_and_Meta/Enums.md#enum-bloateyepassive2) | Enum | Specifies the movement ability for the Bloat Eye enemy. | 1 | `BloatEyeMovement2` |
| [`BloatyExplodey`](./Engine_StatusAndPassiveKeys.md#object-bloatyexplodey) | Object  | An object defining a spell that causes the target to become bloated and explode. | 3 | `{ . . . }` |
| `BlockAllDamage` | Integer | If 1, the unit blocks all incoming damage. | 1 | `1` |
| `BlockDamageUnderThreshold` | Integer | The maximum amount of damage from a single hit that will be completely blocked. | 1 | `1` |
| `BlockNegativeStatus` | Integer | The percentage chance to completely block the application of a negative status effect. | 1 | `30%` |
| `Bloodzerked` | Integer | The number of Bloodzerk stacks applied. | 2 | `1` |
| `BombBehavior` | Integer | If 1, the unit explodes after a set duration or on death. | 1 | `1` |
| [`BombRatTurtle`](./Engine_StatusAndPassiveKeys.md#object-bombratturtle) | Integer / Object  | The number of bomb rat turtle spawns triggered. | 4 | `{ . . . }`<br>`1` |
| [`BoneWormShotMed`](./Engine_StatusAndPassiveKeys.md#object-bonewormshotmed) | Object  | An object defining a medium-range lobbed attack that fires a bone worm projectile. | 2 | `{ . . . }` |
| [`BonusAbility_DelayedApplication`](../Reference_and_Meta/Enums.md#enum-bonusability_delayedapplication) | Enum | Specifies the name of a bonus ability to apply with a delay. | 1 | `Slap` |
| `BonusDamageBasedOnMana` | Integer | The amount of bonus damage dealt, scaled by the target's current mana. | 1 | `1` |
| `BonusHealthRegenPerDisorder` | Integer | The amount of additional health regenerated per turn for each disorder the unit has. | 1 | `1` |
| `BoostDamageAura` | Integer | The amount of bonus damage granted to allies within the aura's range. | 2 | `1` |
| `BoostRangeAura` | Integer | The amount of bonus range (in tiles) granted to allies within the aura's range. | 1 | `1` |
| `BoostReceivedHealing` | Integer | The amount of bonus healing received from all sources. | 1 | `2` |
| [`BoyDino`](./Engine_StatusAndPassiveKeys.md#object-boydino) | Object  | An object defining the Boy Dino passive or character definition. | 4 | `{ . . . }` |
| [`BoyDinoCry`](./Engine_StatusAndPassiveKeys.md#object-boydinocry) | Object  | An object defining an ability or effect that causes the unit to cry, typically applying a debuff to nearby enemies. | 3 | `{ . . . }` |
| `BrittleCharismaUp` | Integer | The number of stacks of temporary Charisma gained on kill. | 1 | `2` |
| `BrittleConstitutionUp` | Integer | The number of stacks of temporary Constitution gained on kill. | 1 | `2` |
| `BrittleDexterityUp` | Integer | The number of stacks of temporary Dexterity gained on kill. | 1 | `2` |
| `BrittleIntelligenceUp` | Integer | The number of stacks of temporary Intelligence gained on kill. | 1 | `2` |
| `BrittleLuckUp` | Integer | The number of stacks of temporary Luck gained on kill. | 1 | `2` |
| `BrittleSpeedUp` | Integer | The number of stacks of temporary Speed gained on kill. | 1 | `2` |
| `BrittleStrengthUp` | Integer | The number of stacks of temporary Strength gained on kill. | 1 | `2` |
| [`BungaCheers`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bungacheers) | Object  | Defines cheer particle effects and sounds triggered by ally or enemy actions. | 1 | `{ . . . }` |
| `ButterflySwarm` | Integer | The number of butterflies spawned for the Butterfly Swarm effect. | 4 | `2` |
| `BypassRockKnockback` | Integer | If set to a non-zero number, bypasses normal rock knockback behavior. | 1 | `1` |
| `CanceledQueuedInput` | Integer | If set to a non-zero number, cancels any queued input from the target. | 1 | `1` |
| `CantDodge` | Integer | If set to 1, the unit cannot dodge any incoming attacks. | 1 | `1` |
| `CapBasicAttackDamage` | Integer | The maximum amount of damage that can be dealt by a basic attack. | 1 | `1` |
| `CapReceivedDamage` | Integer | If 1, the unit caps incoming damage to a maximum per hit. | 1 | `1` |
| [`CatGoop`](./Engine_StatusAndPassiveKeys.md#object-catgoop) | Object  | Defines a specific attack or ability template, including its graphics and targeting parameters. | 3 | `{ . . . }` |
| [`CatPartsSizeScale`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catpartssizescale) | Object  | A multiplier for the size of specific cat parts (e.g., head, body). | 1 | `{ . . . }` |
| [`CaveCatDad`](./Engine_StatusAndPassiveKeys.md#object-cavecatdad) | Object  | Configures a specific enemy cat type, including its graphics, name, and custom data. | 3 | `{ . . . }` |
| `CaveWomanBirthControl` | Integer | If true, restricts or controls the spawning of additional units via birth mechanics. | 1 | `1` |
| [`CerberubsAggroTargetBehavior`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-cerberubsaggrotargetbehavior) | Object  | Defines the default and alert forms used by Cerberubs when changing aggro behavior. | 1 | `{ . . . }` |
| [`CerberubsStraightReaction`](./Engine_StatusAndPassiveKeys.md#object-cerberubsstraightreaction) | Object  | Defines a specific attack ability with a straight-line projectile and configurable area of effect. | 3 | `{ . . . }` |
| `ChampionUpgradeNextMinion` | Integer | The number of champion upgrades applied to the next spawned minion. | 2 | `1` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 101 | `.02`<br>`.1`<br>`.15` |
| `ChanceToAmbush` | Integer | The percentage chance for the unit to ambush an enemy. | 1 | `25%` |
| [`ChanceToForceEvent`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-chancetoforceevent) | Object  | Defines the chance and the specific event to force to occur. | 1 | `{ . . . }` |
| [`ChanceToFormChangeOnAbilityDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-chancetoformchangeonabilitydamage) | Object  | A chance to transform into a different form when damaged by an ability. | 1 | `{ . . . }` |
| [`ChangeTileUnderCharacterAtStart`](../Reference_and_Meta/Enums.md#enum-changetileundercharacteratstart) | Enum | Specifies the tile type to change the tile under the character to at the start of battle. | 1 | `GlassTile` |
| `ChaosBossFlipMidTeleport` | Integer | If set to a non-zero number, causes the chaos boss to flip direction mid-teleport. | 1 | `1` |
| `ChaosBossFormChange` | Integer | If set to a non-zero number, triggers a chaos boss form change. | 1 | `1` |
| [`ChaosBossFormChangeGuide`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-chaosbossformchangeguide) | Object  | Defines active and passive piece sets and a health threshold for the Chaos boss's form change pattern. | 1 | `{ . . . }` |
| [`ChaosBossPieces`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-chaosbosspieces) | Object  | Defines the list of active and passive piece tags for the Chaos boss fight. | 1 | `{ . . . }` |
| [`ChaosHeadDropIn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-chaosheaddropin) | Object  | Defines the tag, spawn ability, and music for the Chaos head's drop-in sequence. | 1 | `{ . . . }` |
| [`CharacterTypeGainsStatusAtBattleStart`](../Reference_and_Meta/Miscellaneous.md#object-charactertypegainsstatusatbattlestart) | Object  | Defines status effects applied to characters with a specific tag at the start of a battle. | 8 | `{ . . . }` |
| `CharismaIsMaxStat` | Integer | Treats the Charisma stat as the character's maximum stat for calculations. | 1 | `1` |
| `CharmedFacingForceAttack` | Integer | If set to a non-zero number, the charmed target is forced to attack the direction they are facing. | 1 | `1` |
| [`CharmedLeech`](./Engine_StatusAndPassiveKeys.md#object-charmedleech) | Object  | Defines a charmed version of the Leech familiar, including its variant and graphics. | 18 | `{ . . . }` |
| [`CharmedPooter`](./Engine_StatusAndPassiveKeys.md#object-charmedpooter) | Object  | Defines a charmed version of the Pooter familiar, including its variant, faction, and properties. | 8 | `{ . . . }` |
| [`CharmedReaper`](./Engine_StatusAndPassiveKeys.md#object-charmedreaper) | Object  | Defines a charmed version of the Reaper familiar, including its variant, faction, and properties. | 2 | `{ . . . }` |
| `CharmImmunity` | Integer | If true, the unit is immune to the Charmed status effect. | 1 | `1` |
| `choose_favorite_cat` | Variable | A variable referencing the selection of the player's favorite cat. | 1 ||
| [`Chubs`](./Engine_StatusAndPassiveKeys.md#object-chubs) | Object  | Defines the Chubs enemy or summon type, including its properties and abilities. | 6 | `{ . . . }` |
| [`ChubsGoop`](./Engine_StatusAndPassiveKeys.md#object-chubsgoop) | Object  | Defines the specific attack ability for Chubs, using a straight-shot template with no mana cost. | 3 | `{ . . . }` |
| [`ChubsRage`](./Engine_StatusAndPassiveKeys.md#object-chubsrage) | Object  | Defines the self-buff ability for Chubs, typically applying a rage animation and stat increases. | 3 | `{ . . . }` |
| `ClearDefaultDebris` | Integer | If true, removes all default debris from the battlefield. | 1 | `1` |
| `ClearFinalBossBattlefield` | Integer | If set to a non-zero number, clears the battlefield during the final boss fight. | 1 | `1` |
| `CloneWeaponTemp` | Integer | The number of turns the cloned weapon persists before being removed. | 1 | `1` |
| `CockroachSwarm` | Integer | If true, the unit spawns as a Cockroach Swarm, with its specific mechanics and effects. | 3 | `1` |
| `CoinTossBounce` | Enum | Specifies the ability triggered when the coin lands on its edge after a bounce. | 1 | `X` |
| `Conditional_Flying` | Object | Defines a conditional block that applies effects or actions only to flying units. | 1 | `{ . . . }` |
| [`Conditional_ManaThreshold`](./Engine_StatusAndPassiveKeys.md#object-conditional_manathreshold) | Object  | Defines a conditional block that applies effects only if a unit's mana meets a specified threshold. | 1 | `{ . . . }` |
| [`Conditional_SourceHasTag`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_sourcehastag) | Object  | Defines a conditional block that applies effects only if the source of the effect has a specified tag. | 1 | `{ . . . }` |
| `Conditional_Tiny` | Object | Defines a conditional block that applies effects only to tiny-sized units. | 1 | `{ . . . }` |
| [`ConfusionEffectOnTaggedAbilities`](../Reference_and_Meta/Enums.md#enum-confusioneffectontaggedabilities) | Enum | Specifies the type of ability tag (e.g., consumable) that triggers a confusion effect when used. | 1 | `consumable` |
| [`ConjureSingleUseBonusAbility`](../Reference_and_Meta/Enums.md#enum-conjuresingleusebonusability) | Enum | Specifies the bonus ability to conjure for single use (e.g., 'random' for a random one). | 1 | `random` |
| `ConsumablesMeleeRange` | Integer | Causes consumable items to have a melee range instead of their default range. | 1 | `1` |
| [`ConvertDamageToScaledStatus`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-convertdamagetoscaledstatus) | Object  | Converts a portion of incoming damage into a specified status effect with a given number of stacks. | 1 | `{ . . . }` |
| [`CounterAttackAfterEnemyCastSpell`](../Reference_and_Meta/Enums.md#enum-counterattackafterenemycastspell) | Enum | Specifies the ability the unit uses to counterattack after an enemy casts a spell. | 1 | `Telekinesis` |
| `CounterNextAttacks` | Integer | The number of incoming attacks the unit will counterattack. | 2 | `2` |
| [`CraterCreeperOut`](./Engine_StatusAndPassiveKeys.md#object-cratercreeperout) | Object  | Defines the specific enemy type Crater Creeper Out, including its graphics and spawn offset. | 2 | `{ . . . }` |
| `CrowAttackLink` | Integer | If 1, allows this unit's attacks to chain or link to nearby enemies like a crow. | 1 | `1` |
| `CurrentWeaponAddElectricElement` | Integer | The number of turns the current weapon gains the electric element. | 1 | `1` |
| [`CyborgTurns`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-cyborgturns) | Object  | Defines the number of extra turns controlled by AI and their timing for a Cyborg unit. | 1 | `{ . . . }` |
| `DamageFromBehindOnly` | Integer | If 1, the unit can only be damaged when attacked from behind. | 1 | `1` |
| [`DamageIfDidntUseSpecificAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-damageifdidntusespecificability) | Object  | Deals a specified amount of damage if the unit did not use a designated ability on its previous turn. | 1 | `{ . . . }` |
| `DamageWeapon` | Integer | The amount of durability damage dealt to the equipped weapon. | 1 | `1` |
| [`DarkOneStrike`](./Engine_StatusAndPassiveKeys.md#object-darkonestrike) | Object  | Defines a specific powerful attack ability for the Dark One enemy. | 2 | `{ . . . }` |
| [`DeathwormUnderground`](../Reference_and_Meta/Enums.md#enum-deathwormunderground) | Enum | Specifies the ability triggered when the Deathworm emerges from underground. | 1 | `DeathWormEat` |
| [`DecoyExplode`](./Engine_StatusAndPassiveKeys.md#object-decoyexplode) | Object  | Defines the explosion effect for a decoy unit. | 4 | `{ . . . }` |
| `DecoySwapper` | Integer | If true, the decoy swaps places with the source when spawned. | 1 | `1` |
| `DelayedPain` | Integer | The number of stacks of DelayedPain applied, dealing damage after a delay. | 3 | `1` |
| [`DelayedWindCone`](./Engine_StatusAndPassiveKeys.md#object-delayedwindcone) | Object  | An object containing parameters for a delayed wind cone, such as damage and distance. | 2 | `{ . . . }` |
| `DeleteInanimateObjectsChance` | Integer | The percentage chance per tick to delete all inanimate objects on the battlefield. | 1 | `25%` |
| `DeleteTraps` | Integer | If true, removes all traps from the map. | 1 | `1` |
| `DemonicGlyph_Bounce` | Integer | The weight for the demonic glyph of bounce, or its configuration. | 3 | `1` |
| `DemonicGlyph_Fire` | Integer | The weight for the demonic glyph of fire, or its configuration. | 3 | `1` |
| `DemonicGlyph_Movement` | Integer | The weight for the demonic glyph of movement, or its configuration. | 4 | `1` |
| `DemonicGlyphStealer` | Integer | If 1, the unit can steal demonic glyphs from other units. | 1 | `1` |
| [`DestroyerShieldBash`](./Engine_StatusAndPassiveKeys.md#object-destroyershieldbash) | Object  | Defines the shield bash ability for the Destroyer enemy type. | 2 | `{ . . . }` |
| `DestroyNeckArmor` | Integer | If true, destroys the target's neck armor slot. | 1 | `1` |
| [`Diabetes`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-diabetes) | Object  | Defines the Diabetes disorder, including its name, description, and associated passive effects. | 5 | `{ . . . }` |
| [`DiceBehavior`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-dicebehavior) | Object  | Defines the dice size and knockback damage for the Dice enemy. | 1 | `{ . . . }` |
| [`DicerArt`](../Reference_and_Meta/Arrays.md#array-dicerart) | Array | An array of art offset values for the Dicer enemy. | 1 | `[59 52 65 50 54 63 64]` |
| [`DiesToPiercingAndSpikes`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-diestopiercingandspikes) | Object  | Makes the unit take lethal damage from piercing attacks and spike terrain. | 1 | `{ . . . }` |
| `DieWhenOnlyGolemsLeft` | Integer | If 1, the unit dies when only golem-type allies remain on the field. | 1 | `1` |
| `DieWhenSpawnerDies` | Integer | If 1, the unit dies when its spawner unit dies. | 1 | `1` |
| [`Digest`](./Engine_StatusAndPassiveKeys.md#object-digest) | Object  | Defines the digestion mechanic, typically applied to units that swallow others. | 3 | `{ . . . }` |
| [`DinoLegAnimation`](../Reference_and_Meta/Enums.md#enum-dinoleganimation) | Enum | Specifies the animation trigger for the dinosaur leg (e.g., 'poop' for the poop animation). | 1 | `poop` |
| `DisableSpells` | Integer | If 1, the unit cannot cast spells. | 1 | `1` |
| `Disguised` | Integer | If true, the unit is disguised, appearing as a different faction or model. | 2 | `1` |
| [`DisguisedTrapper`](../Reference_and_Meta/Enums.md#enum-disguisedtrapper) | Enum | Specifies the passive used when disguised as a trapper, e.g. FearMelee. | 1 | `FearMelee` |
| `DisplayBuddyCatOnSpawn` | Integer | The number of buddy cat objects to display when the unit spawns. | 1 | `3` |
| `DissolveRandomArmorPiece` | Integer | If true, destroys a random armor piece (head, body, neck) on the target. | 1 | `1` |
| `DivineShieldPickup` | Integer | The number of divine shield charges granted on pickup. | 1 | `1` |
| `DodgeChanceWithBlindSpot` | Integer | The percentage chance to dodge attacks while a blind spot condition is active. | 1 | `25%` |
| [`DodgeWhenTargeted`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-dodgewhentargeted) | Object  | An object defining the ability and effects triggered when the unit is targeted for an attack. | 1 | `{ . . . }` |
| `DoubleCast` | Integer | The number of double-cast stacks, allowing a spell to be cast twice. | 3 | `1` |
| `DoubleCastSpellIfManaCostUnderThreshold` | Integer | If a spell's mana cost is under this threshold, it will be cast twice. | 1 | `3` |
| `DoubleCastSpellsEachTurn_Status` | Integer | The number of turns the unit gains Double Cast for spells each turn. | 2 | `1` |
| `DoubleCastSpellThisTurn` | Integer | If non-zero, grants the unit a double cast effect for spells this turn. | 3 | `1` |
| [`DoubleCastTaggedSpells`](../Reference_and_Meta/Enums.md#enum-doublecasttaggedspells) | Enum | Specifies the spell tag (e.g., musical) that causes spells to be cast twice. | 1 | `musical` |
| `DoubleReceivedNegativeStatus` | Integer | If true, the unit receives double the stacks of negative status effects applied to it. | 1 | `1` |
| `DoubleReceivedPositiveStatus` | Integer | If true, the unit receives double the stacks of positive status effects applied to it. | 1 | `1` |
| `DrainAllyCatsForFleshGolem` | Integer | The amount of health drained from ally cats to heal the Flesh Golem. | 1 | `7` |
| [`DropAsFamiliarOnTookDamage`](../Reference_and_Meta/Enums.md#enum-dropasfamiliarontookdamage) | Enum | Specifies the familiar type to be dropped when the unit takes damage. | 1 | `PhantomMaskRock` |
| [`DropSoulJarOnDeath`](../Reference_and_Meta/Enums.md#enum-dropsouljarondeath) | Enum | Specifies the type of soul jar to be dropped when the unit dies. | 1 | `SoulJar_Full` |
| `DuplicateRandomEquippedItem` | Integer | If true, creates a copy of a random equipped item. | 1 | `1` |
| `DustCloudBehavior` | Integer | An integer flag that controls the behavior mode of a dust cloud entity. | 1 | `1` |
| `Dybbuk1HPTracker` | Integer | A flag indicating the unit tracks that it has 1 HP remaining for Dybbuk possession mechanics. | 1 | `1` |
| `DybbukManualExitTag` | Variable | A variable referencing the tag that allows a Dybbuk unit to manually exit its host. | 1 ||
| [`DybbukPossessionFallback`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-dybbukpossessionfallback) | Object  | An object specifying the fallback form and exit ability used when possession fails. | 1 | `{ . . . }` |
| [`EatShit`](./Engine_StatusAndPassiveKeys.md#object-eatshit) | Object  | Defines a specific ability or effect related to consuming or eating feces. | 2 | `{ . . . }` |
| `ElectricArcs` | Integer | The number of electric arcs emitted by this unit. | 1 | `1` |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 80 | `Electric`<br>`Fire`<br>`Gravity` |
| [`ElementWeakness`](../Reference_and_Meta/Enums.md#enum-elementweakness) | Enum | Determines which element the unit is weak to, e.g. Fire. | 1 | `Fire` |
| `EliteUpgradeNextMinion` | Integer | The number of elite upgrades applied to the next spawned minion. | 2 | `1` |
| `end_of_round` | Boolean | If true, the effect triggers at the end of the round instead of at the start of the turn. | 3 | `true` |
| `enemies` | Variable | A variable representing the group of enemy units. | 351 ||
| `EnrageOnDamage` | Integer | If set to 1, the unit gains enrage stacks when taking damage. | 1 | `1` |
| [`EnterMount`](../Reference_and_Meta/Enums.md#enum-entermount) | Enum | Specifies the name of the mount status to apply to the unit. | 2 | `enter` |
| `EraseSpawnCoins` | Integer | If set to 1, the unit erases spawn coins from the map on spawn. | 1 | `1` |
| [`euphoric`](../Reference_and_Meta/Miscellaneous.md#object-euphoric) | Object  | Defines the facial expression configuration for the euphoric emotional state of a unit. | 3 | `{ . . . }` |
| `EventBounterHunterPassive` | Integer | A flag enabling the event bounty hunter passive behavior. | 1 | `1` |
| `exclude_self` | Boolean | If true, the effect does not apply to the source unit itself. | 3 | `false` |
| [`ExcludeFromEvents`](../Reference_and_Meta/Enums.md#enum-excludefromevents) | Enum | Specifies the event type (e.g., Tragedy) that this unit is excluded from participating in. | 1 | `Tragedy` |
| `ExhaustionRoundChange` | Integer | The number of rounds added to the exhaustion counter. | 1 | `3` |
| `ExistUntilIdleUpkeep` | Integer | If true, the entity persists until the source unit enters idle upkeep. | 2 | `1` |
| `ExplodeCharacter_DeathBloom` | Integer | The amount of damage dealt by the DeathBloom explosion. | 1 | `5` |
| `ExplodeCharacter_DeathBloom2` | Integer | The amount of damage dealt by the DeathBloom2 explosion. | 1 | `5` |
| `ExtraInjuryOnDeath` | Integer | The number of additional injuries inflicted upon death. | 1 | `1` |
| [`ExtraTurnsPerTaggedUnit`](../Reference_and_Meta/Enums.md#enum-extraturnspertaggedunit) | Enum | Specifies the tag of units that grant extra turns when present. | 1 | `sprout` |
| [`face_EatNeverstone`](./Engine_StatusAndPassiveKeys.md#object-face_eatneverstone) | Object  | Defines the ability used when the unit eats a Neverstone, typically a self-buff. | 2 | `{ . . . }` |
| [`face_LeechBrood`](./Engine_StatusAndPassiveKeys.md#object-face_leechbrood) | Object  | Defines the ability used when the unit activates Leech Brood, typically a self-buff or attack. | 2 | `{ . . . }` |
| [`FaceAwayLastDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-faceawaylastdamage) | Object  | An object defining animation overrides for the last damage event when the unit faces away. | 1 | `{ . . . }` |
| `FactionDisguiseSource` | Integer | If true, the unit adopts the faction of the source unit for disguise. | 1 | `1` |
| `FastKnockback` | Integer | The number of tiles the target is knocked back with fast animation. | 1 | `4` |
| [`FinalBossBeamQueue`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finalbossbeamqueue) | Object  | An object defining the queue of beam ability actions for the final boss form. | 1 | `{ . . . }` |
| [`FinalBossBecomeTheChild`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finalbossbecomethechild) | Object  | An object defining the transformation and environment changes when the boss becomes TheChild. | 1 | `{ . . . }` |
| [`FinalBossHitCountdownBoris`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finalbosshitcountdownboris) | Object  | An object defining the countdown status effect properties for the Boris phase, including stacks, icons, and forced abilities. | 3 | `{ . . . }` |
| [`FinalBossHitCountdownExplosive`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finalbosshitcountdownexplosive) | Object  | An object defining the countdown status effect properties for the Explosive phase, including stacks, icons, and forced abilities. | 2 | `{ . . . }` |
| [`FinalBossHitCountdownHoly`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finalbosshitcountdownholy) | Object  | An object defining the countdown status effect properties for the Holy phase, including stacks and icons. | 2 | `{ . . . }` |
| [`FinalBossPupils`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finalbosspupils) | Object  | An object configuring the visual tracking of the final boss's pupils, including radius, head position, and teleport tracking. | 1 | `{ . . . }` |
| `FinalBossQueueBeam` | Integer | If true, queues the final boss beam attack. | 1 | `1` |
| [`FinalBossShieldHealth`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finalbossshieldhealth) | Object  | An object defining the shield health thresholds per visual state for the final boss. | 1 | `{ . . . }` |
| [`FinalBossSyncAnimations`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finalbosssyncanimations) | Object  | An object defining animation synchronization with another character, including form change abilities. | 1 | `{ . . . }` |
| [`FireArmor`](./Engine_StatusAndPassiveKeys.md#object-firearmor) | Integer / Object  | The number of Fire Armor stacks providing damage reflection. | 6 | `{ . . . }`<br>`1` |
| [`FireArmor2`](./Engine_StatusAndPassiveKeys.md#object-firearmor2) | Integer / Object  | The number of Fire Armor2 stacks (likely a variant). | 4 | `{ . . . }`<br>`1` |
| [`FireExtinguish_Steam`](./Engine_StatusAndPassiveKeys.md#object-fireextinguish_steam) | Variable | Defines the particle effect for steam created when fire is extinguished. | 3 ||
| `FireflySwarm` | Integer | The number of fireflies in the swarm effect. | 4 | `2` |
| `FistOfFateUniqueEnemyTracker` | Integer | Increases the damage tracking counter for unique enemies hit by Fist of Fate. | 1 | `1` |
| `FlingObjectsOnTop` | Integer | The number of objects to fling on top of this unit. | 1 | `8` |
| [`FlushmasterCelebration`](../Reference_and_Meta/Enums.md#enum-flushmastercelebration) | Enum | Specifies the celebration animation or effect name used by the Flushmaster. | 1 | `celebrate` |
| [`FlyBuff`](./Engine_StatusAndPassiveKeys.md#object-flybuff) | Variable | Defines the visual effect or buff for the Fly familiar. | 2 ||
| `Fog` | Integer | When an integer, the intensity of fog; when an object, defines the fog particle effect. | 5 | `1` |
| `ForceCollectsPickups` | Integer | If true, the unit automatically collects nearby pickups. | 1 | `1` |
| `ForceDodgeEverything` | Integer | If set to 1, the unit will always dodge all incoming attacks. | 1 | `1` |
| [`ForceImmediateMoveAndAttack`](./Engine_StatusAndPassiveKeys.md#object-forceimmediatemoveandattack) | Object  | An object that forces the unit to instantly move toward the target and perform a specified ability attack. | 1 | `{ . . . }` |
| `ForceMoveAndAttack` | Integer | If true, forces the target to move and attack its nearest enemy. | 1 | `1` |
| `ForceTransferWeapon` | Integer | If true, forces the weapon to be transferred to the target. | 1 | `1` |
| [`ForceUseAbilityOnTarget`](./Engine_StatusAndPassiveKeys.md#object-forceuseabilityontarget) | Object  | Defines a chance to force the unit to use a specified ability on the target. | 1 | `{ . . . }` |
| [`FormChangeWhenBuddyDies`](../Reference_and_Meta/Enums.md#enum-formchangewhenbuddydies) | Enum | Specifies the form name the unit changes into when its buddy dies. | 1 | `Rage` |
| [`FrankBolts`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-frankbolts) | Integer / Object  | The number of Frank Bolts applied or available. | 4 | `{ . . . }`<br>`1` |
| `FreeFirstCastAndAfterSpendMana` | Integer | If set to 1, the first cast of the ability and each cast after spending mana costs no resources. | 1 | `1` |
| `FreeFirstCastEachMatch` | Integer | If set to 1, the first cast of the ability each match costs no resources. | 1 | `1` |
| `FreeSpellsAtFullMana` | Integer | The number of spells that cost no mana when mana is full. | 1 | `1` |
| `FrontstabBasicAttackCritChance` | Integer | The percentage chance for basic attacks to critically hit when attacking from the front. | 1 | `100%` |
| `FullBlockEverything` | Integer | If set to 1, the unit fully blocks all incoming damage. | 1 | `1` |
| `FullBlockEverythingTo0Damage` | Integer | If set to 1, the unit reduces all incoming damage to 0. | 1 | `1` |
| [`FurnitureStats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-furniturestats) | Object  | Defines the Comfort, Stimulation, and Appeal stats of furniture. | 1 | `{ . . . }` |
| `GasCanBehavior` | Integer | An integer flag that controls the behavior mode of a gas can entity. | 1 | `1` |
| `GasCloudBehavior2` | Integer | An integer flag that controls a secondary behavior mode of a gas cloud entity. | 1 | `2` |
| `GeminiTwin` | Integer | If set to 1, this unit is the twin in a Gemini pair. | 1 | `1` |
| [`GirlDino`](./Engine_StatusAndPassiveKeys.md#object-girldino) | Object  | Defines the Girl Dino creature or its ability. | 5 | `{ . . . }` |
| [`GirlDinoCry`](./Engine_StatusAndPassiveKeys.md#object-girldinocry) | Object  | Defines the cry ability of Girl Dino, typically a self-buff with a cry animation. | 3 | `{ . . . }` |
| `GiveBoundItemToTarget` | Integer | If true, gives the source's bound item to the target. | 1 | `1` |
| `GlobalFamiliarDamageBoost` | Integer | The amount of damage boost applied to all familiars globally. | 2 | `1` |
| `GlobalFamiliarMoveBoost` | Integer | The amount of movement boost applied to all familiars globally. | 2 | `1` |
| [`GlobalFlowerTrapperAura`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-globalflowertrapperaura) | Object  | Defines an aura that applies Tangled to enemies with specified stacks and probability. | 1 | `{ . . . }` |
| `GlobalHealthRegenAura` | Integer | The amount of health regenerated per turn to all units in range. | 1 | `3` |
| `GlobalManaDrainAura` | Integer | The amount of mana drained per turn from all units in range. | 1 | `-1` |
| [`GlobalMeleeRevengeDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-globalmeleerevengedamage) | Object  | Defines revenge damage properties (e.g., knockback) when hit by a melee attack. | 1 | `{ . . . }` |
| [`GlobalSpawnCharacter`](../Reference_and_Meta/Enums.md#enum-globalspawncharacter) | Enum | Specifies the name of a character to spawn globally. | 3 | `MegaGuppy` |
| `GoopImmunity` | Integer | If set to 1, the unit is immune to goop status effects. | 1 | `1` |
| `grub_familiar` | Variable | Defines the Grub familiar's properties. | 2 ||
| [`Guillotina2Body`](./Engine_StatusAndPassiveKeys.md#object-guillotina2body) | Object  | Defines the Guillotina's second body ability or body part. | 4 | `{ . . . }` |
| [`Guillotina2Head`](./Engine_StatusAndPassiveKeys.md#object-guillotina2head) | Object  | Defines the Guillotina's second head ability or head part. | 4 | `{ . . . }` |
| [`Guillotina3Body`](./Engine_StatusAndPassiveKeys.md#object-guillotina3body) | Object  | Defines the Guillotina's third body ability or body part. | 4 | `{ . . . }` |
| [`Guillotina3Head`](./Engine_StatusAndPassiveKeys.md#object-guillotina3head) | Object  | Defines the Guillotina's third head ability or head part. | 4 | `{ . . . }` |
| `GuillotinaDeathHead` | Integer | If set to 1, the unit spawns a head object upon death via guillotine. | 1 | `1` |
| [`HarpoonTrapPassive`](../Reference_and_Meta/Enums.md#enum-harpoontrappassive) | Enum | Specifies the ability name used when the harpoon trap is triggered. | 1 | `HarpoonTrapPull` |
| [`HCHumanDie`](./Engine_StatusAndPassiveKeys.md#object-hchumandie) | Object  | Defines the human die animation and buff when a human dies. | 3 | `{ . . . }` |
| [`HealNeighborsEachTurn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-healneighborseachturn) | Object  | An object defining the amount and target filtering for healing adjacent units each turn. | 1 | `{ . . . }` |
| `HealPercentMaxHP` | Integer | The percentage of max HP healed (e.g., 100 for full heal). | 1 | `100` |
| `HealTo` | Integer | The target HP percentage to heal the unit to (e.g., '50%' for half max HP). | 1 | `50%` |
| `HeatWave` | Integer | When an integer, the intensity of the heat wave; when an object, defines the visual effects or status properties. | 7 | `1` |
| `HeavyHits` | Integer | The number of Heavy Hits stacks increasing attack impact. | 2 | `1` |
| [`HemBounce`](./Engine_StatusAndPassiveKeys.md#object-hembounce) | Object  | Defines the Hem's bounce melee attack ability. | 3 | `{ . . . }` |
| `HiddenDoomed` | Integer | The number of stacks of a hidden doomed status effect applied to the unit. | 1 | `2` |
| [`HideEquipment`](../Reference_and_Meta/Enums.md#enum-hideequipment) | Enum | Specifies which equipment slot is visually hidden. | 2 | `neck` |
| `HideSomeHudStuff` | Integer | If set to 1, hides certain HUD elements. | 1 | `1` |
| [`HitlerExecute`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-hitlerexecute) | Object  | An object defining the tag, ability, and health threshold for executing a clone. | 1 | `{ . . . }` |
| [`HPAltStates`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-hpaltstates) | Object  | An object defining alternate visual frames based on current HP thresholds. | 1 | `{ . . . }` |
| `Hypomania` | Integer | When an integer, the stacks of Hypomania; when an object, defines the Hypomania disorder status. | 5 | `3` |
| `IceBlockBehavior` | Integer | An integer flag that controls the behavior mode of an ice block entity. | 1 | `1` |
| [`IDSprout`](./Engine_StatusAndPassiveKeys.md#object-idsprout) | Object  | Defines the ID Sprout spawn ability. | 3 | `{ . . . }` |
| `IgnoreDebuffs` | Integer | If true, the effect ignores debuffs on the target. | 1 | `1` |
| [`IncAuxCounterCycle`](./Engine_StatusAndPassiveKeys.md#object-incauxcountercycle) | Object  | An object containing parameters for incrementing an auxiliary counter with a change and maximum value. | 1 | `{ . . . }` |
| `IncreaseCumulativeBlastDamage` | Integer | If true, increases the cumulative blast damage counter. | 1 | `1` |
| `IncreaseItemAuxOnKill` | Integer | If true, increases the item's aux counter on kill. | 1 | `1` |
| `InheritSpawnerStats` | Integer | If set to 1, the unit inherits the stats of its spawner. | 1 | `1` |
| [`insane`](../Reference_and_Meta/Miscellaneous.md#object-insane) | Object  | Defines the 'insane' facial expression with eyebrow and mouth positions. | 4 | `{ . . . }` |
| `InsertIntoBackgroundPlaceholder` | Integer | If set to 1, the unit is inserted into a background placeholder slot. | 1 | `1` |
| `InterchangeDisabler` | Integer | If set to 1, prevents the unit from being interchanged with another unit. | 1 | `1` |
| `InterchangeMoveActPoints` | Integer | If true, swaps the unit's remaining move points and action points. | 1 | `1` |
| `InvertBrainFaction` | Integer | If set to 1, inverts the unit's faction (e.g., allies become enemies). | 1 | `1` |
| `Invulnerable` | Integer | The number of Invulnerable stacks, making the unit immune to damage. | 2 | `1` |
| `JesterLevelUpRerolls` | Integer | The number of additional rerolls granted when leveling up. | 1 | `1` |
| [`JohnnyNeedsWashing`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-johnnyneedswashing) | Object  | An object specifying the form names for washed and unwashed states. | 1 | `{ . . . }` |
| [`JohnnyWasher`](../Reference_and_Meta/Enums.md#enum-johnnywasher) | Enum | Specifies the ability name used by the washer form to clean Johnny. | 1 | `BBTransformZealot` |
| `JudgementDay` | Integer | When an integer, the turn count or damage for Judgement Day; when an object, defines the weather status. | 3 | `25` |
| [`KnockbackIfCrit`](./Engine_StatusAndPassiveKeys.md#object-knockbackifcrit) | Object  | Defines knockback properties applied when a critical hit occurs. | 1 | `{ . . . }` |
| [`LegacySpawnSavedCatIfExists`](../Reference_and_Meta/Enums.md#enum-legacyspawnsavedcatifexists) | Enum | Specifies the legacy saved cat ID to spawn if it exists in the save data. | 1 | `Legacy_Marshmallow_StolenCatID` |
| [`LennyCatDies`](./Engine_StatusAndPassiveKeys.md#object-lennycatdies) | Object  | Defines the ability triggered when Lenny the cat dies. | 3 | `{ . . . }` |
| [`LimitedTileTrail`](../Reference_and_Meta/Enums.md#enum-limitedtiletrail) | Enum | Specifies the type of tile left behind as a trail when the unit moves. | 1 | `FlowerTile` |
| `LimitSelfKnockbackDamage` | Integer | The maximum amount of damage taken from self-inflicted knockback. | 1 | `1` |
| [`LockOrientationFaceTile`](../Reference_and_Meta/Arrays.md#array-lockorientationfacetile) | Array | A tile coordinate [x y] that the unit's orientation is locked to face. | 1 | `[0 0]` |
| `LowGravityKnockbackBoost` | Integer | The multiplier or bonus to knockback force under low gravity. | 1 | `1` |
| `LowGravityRangeBoost` | Integer | The increase in attack range under low gravity. | 1 | `2` |
| `MadnessChanceOnTurnBegin` | Integer | The chance (as a multiplier) to inflict Madness status at the start of each turn in the next battle. | 2 | `2` |
| `MakeWeaponUnbreakable` | Integer | If true, makes the equipped weapon unbreakable. | 1 | `1` |
| [`ManaGainRange`](./Engine_StatusAndPassiveKeys.md#object-managainrange) | Object  | Defines the minimum and maximum mana gained per turn. | 1 | `{ . . . }` |
| `ManaStealToHealth` | Integer | The amount of mana stolen and converted to health (negative values may drain health). | 1 | `-1` |
| `ManglerAttack` | Integer | If true, the attack triggers the Mangler's attack pattern. | 1 | `1` |
| [`ManglerEnrage`](./Engine_StatusAndPassiveKeys.md#object-manglerenrage) | Object  | Defines the enrage ability of the Mangler monster. | 3 | `{ . . . }` |
| [`ManglerMonsterDashAttack`](./Engine_StatusAndPassiveKeys.md#object-manglermonsterdashattack) | Object  | Defines the dash attack ability of the Mangler monster. | 3 | `{ . . . }` |
| [`ManglerMonsterPassive`](../Reference_and_Meta/Enums.md#enum-manglermonsterpassive) | Enum | Specifies the ability name used for the Mangler monster's dash attack. | 1 | `ManglerMonsterDashAttack` |
| `ManglerShuffle` | Boolean | If true, the order of effects in this damage instance is randomized before application. | 1 | `false` |
| [`ManglersMonster`](./Engine_StatusAndPassiveKeys.md#object-manglersmonster) | Object  | Defines the Mangler monster's properties. | 4 | `{ . . . }` |
| `MassAttackThis` | Integer | The number of additional targets this attack hits via the Mass Attack mechanic. | 1 | `1` |
| `MaxAccuracy` | Integer | The maximum allowed accuracy percentage for the unit. | 2 | `1` |
| `MaxStartingMana` | Integer | The maximum amount of mana the unit starts with. | 2 | `1` |
| `Meaty` | Integer | The number of Meaty stacks increasing health or size. | 3 | `1` |
| [`MechExplode`](./Engine_StatusAndPassiveKeys.md#object-mechexplode) | Object  | Defines the explosion ability of a mech unit. | 2 | `{ . . . }` |
| [`MegaDinoDropController`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-megadinodropcontroller) | Object  | An object defining the abilities and stable leg count for the Mega Dino's leg drop sequence. | 1 | `{ . . . }` |
| [`MegaFart`](./Engine_StatusAndPassiveKeys.md#object-megafart) | Object  | Defines the Mega Fart ability. | 2 | `{ . . . }` |
| [`MegaGuppy_SummonTheChild`](./Engine_StatusAndPassiveKeys.md#object-megaguppy_summonthechild) | Object  | Defines the ability to summon the child from Mega Guppy. | 3 | `{ . . . }` |
| [`MergeDamageInstance`](./Engine_StatusAndPassiveKeys.md#object-mergedamageinstance) | Object  | Specifies parameters to merge multiple damage instances into one, controlling hit animation and instant pop behavior. | 1 | `{ . . . }` |
| `MeteorShower` | Integer | The chance (as a percentage) for a meteor shower to occur on a given turn. | 4 | `25%` |
| `MimicMetronome` | Integer | The number of random abilities the Metronome effect selects from this unit's ability pool. | 1 | `1` |
| `ModelingClayPassive` | Integer | If set to 1, enables the passive that duplicates the equipped item on the unit. | 1 | `1` |
| [`ModularPickup`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-modularpickup) | Object  | An object defining the effects and sounds triggered when the unit is picked up. | 1 | `{ . . . }` |
| [`MonkCatReactionAbilities`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-monkcatreactionabilities) | Object  | A set of mappings from action types (move, attack, spell, trinket) to the corresponding ability IDs the MonkCat will use for reactions. | 1 | `{ . . . }` |
| [`MoonHead_KillHands`](./Engine_StatusAndPassiveKeys.md#object-moonhead_killhands) | Object  | An object defining a targeted status effect applied when MoonHead kills an enemy with its hands. | 2 | `{ . . . }` |
| [`MoonHeadCrackedVisual`](../Reference_and_Meta/Enums.md#enum-moonheadcrackedvisual) | Enum | Specifies the visual state for the character's cracked head appearance. | 1 | `Cracked` |
| [`MotherGrowController`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-mothergrowcontroller) | Object  | Controls the growth of tumors on The Mother, including the tumor object, damage type, damage amount, and whether it pierces defense when eating damage. | 1 | `{ . . . }` |
| `MotherTumorDebugForcePass` | Integer | If non-zero, forces the Mother Tumor boss to pass its turn, skipping its normal action. | 1 | `1` |
| [`MotherTumorPassive`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-mothertumorpassive) | Object  | Defines the passive behavior for a MotherTumor, including the forms considered for pass/receive, the pass and receive animations, and the grow ability. | 1 | `{ . . . }` |
| [`Mount`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-mount) | Object  | Defines the entering and ejecting abilities for a mountable unit, along with its death rattle ability. | 1 | `{ . . . }` |
| [`MoveAfterAnyAttemptedAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-moveafteranyattemptedattack) | Object  | Defines the movement behavior (weights and abilities) used after any attempted attack. | 1 | `{ . . . }` |
| [`MoveAwayWhenEnemyAdjacent`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-moveawaywhenenemyadjacent) | Object  | Defines the movement behavior (move_ability, weights, and whether it triggers once per turn) when an enemy is adjacent. | 1 | `{ . . . }` |
| `MulticatHeads` | Integer | The number of additional heads the Multicat has. | 1 | `0` |
| `MultiplyCoinsOnBattleStart` | Integer | The multiplier applied to the unit's coin count at the start of battle. | 1 | `2` |
| `MultiplyReceivedHealing` | Integer | The multiplier applied to all healing the unit receives. | 1 | `2` |
| [`MultiSpawnOnDeath`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-multispawnondeath) | Object  | Specifies the object to spawn and the range of number of objects to spawn on death. | 1 | `{ . . . }` |
| `MutateAfterXTurns` | Integer | The number of turns after which the character automatically mutates (or transforms). | 2 | `3` |
| `Muted` | Integer | The number of Muted stacks, disabling certain abilities. | 2 | `1` |
| `MuteDemonicGlyphDisplay` | Integer | If set to 1, suppresses the display of demonic glyphs on the character. | 1 | `1` |
| `NextAbilityHeals` | Integer | The number of stacks causing the next ability to heal instead of damage. | 3 | `1` |
| `NextActionLuckUp` | Integer | The number of stacks increasing luck for the next action. | 2 | `99` |
| [`NextBasicAttackCritsThisTurn`](./Engine_StatusAndPassiveKeys.md#object-nextbasicattackcritsthisturn) | Object  | An object or number configuring the next basic attack to be a critical hit this turn. An object may contain stack, cant_miss, or piercing sub-keys. | 3 | `{ . . . }` |
| [`NextBattleStatusStacks`](./Engine_StatusAndPassiveKeys.md#object-nextbattlestatusstacks) | Object  | An object specifying status effects and their stacks to be applied at the start of the next battle. Contains a "fights" counter and nested status keys. | 1 | `{ . . . }` |
| `NextDamageReduceAndHealAllies` | Integer | The number of stacks reducing next damage and healing nearby allies. | 3 | `1` |
| `NextTurnDoubleRangedDamage` | Integer | The number of stacks doubling ranged damage on the next turn. | 2 | `1` |
| [`NoHead`](./Engine_StatusAndPassiveKeys.md#object-nohead) | Object  | An object that replaces the unit's head graphics with a headless cat model and sets the enemy name. | 7 | `{ . . . }` |
| [`NonChampionFlySwarm`](./Engine_StatusAndPassiveKeys.md#object-nonchampionflyswarm) | Object  | An object defining a fly swarm that only spawns on non-champion units. | 2 | `{ . . . }` |
| `NonLethal` | Integer | If set to 1, damage dealt by the unit cannot kill enemies; it leaves them at 1 HP. | 1 | `1` |
| [`Nubs`](./Engine_StatusAndPassiveKeys.md#object-nubs) | Object  | An object defining a visual or mechanical replacement of the unit's limbs with stubs. | 8 | `{ . . . }` |
| [`NubsGoop`](./Engine_StatusAndPassiveKeys.md#object-nubsgoop) | Object  | An object defining a lobbed attack that costs 0 mana and fires goop. | 3 | `{ . . . }` |
| [`ObjectDetector`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-objectdetector) | Object  | An object that grants a chance to detect a specific item (e.g., CharmedDip) when loot is evaluated. | 1 | `{ . . . }` |
| [`ObjectOnHitFullyEmpty`](../Reference_and_Meta/Enums.md#enum-objectonhitfullyempty) | Enum | Specifies the object (e.g., RandomArmorPickup) to spawn on the target when the attacker's inventory is completely empty. | 1 | `RandomArmorPickup` |
| [`Ornstein`](./Engine_StatusAndPassiveKeys.md#object-ornstein) | Object  | An object defining a passive or status effect mimicking Ornstein's behavior (e.g., charge attack). | 3 | `{ . . . }` |
| `OrthogonalAIDangerZone` | Integer | The range (in tiles) for the AI's orthogonal danger zone detection. | 1 | `10` |
| `OverHealToShield` | Integer | The amount of excess healing converted into temporary shield points. | 1 | `1` |
| `OverManaReducesManaCosts` | Integer | If set to 1, any mana the unit has above their maximum reduces the cost of abilities. | 1 | `1` |
| `OverrideMaxMana` | Integer | Sets the unit's maximum mana to this integer value, overriding the default. | 1 | `1` |
| `OverridePalette` | Integer | Forces the unit to use a specific color palette index. | 1 | `87` |
| `PackHunting` | Integer | If set to 1, enables pack hunting behavior for the character. | 1 | `1` |
| [`Paranoia`](../Reference_and_Meta/Enums.md#enum-paranoia) | Enum | Specifies the type of paranoid melee attack the unit will use instead of their normal attack. | 8 | `ParanoiaBasicMelee` |
| [`PassiveLevelScaledStatus`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivelevelscaledstatus) | Object  | An object containing status effects whose values scale with the unit's level, using X as the level variable. | 1 | `{ . . . }` |
| [`PassiveWhileHasDurability`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhilehasdurability) | Object  | An object containing passives that are active only while the item has remaining durability. | 1 | `{ . . . }` |
| [`PassiveWhileNotTakingTurn`](./Engine_StatusAndPassiveKeys.md#object-passivewhilenottakingturn) | Object  | A nested passive object that is active only while the unit is not currently taking its turn. | 1 | `{ . . . }` |
| [`PassiveWhileShielded`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhileshielded) | Object  | An object containing passives that are active only while the unit has a shield. | 1 | `{ . . . }` |
| `PercentHeal` | Integer | The percentage of max HP healed when this effect triggers. | 1 | `50` |
| `PermanentConfusion` | Number | If set to 1, the unit is permanently confused and cannot be cured. | 3 | `1` |
| `PermanentImmobile` | Integer | The permanent amount of immobility stacks applied. | 3 | `1` |
| `PermanentKitten` | Integer | If set to 1, the unit retains its kitten form permanently instead of aging. | 1 | `1` |
| `PermanentUpgradeRandomActiveOrPassive` | Integer | The number of random active or passive abilities permanently upgraded. | 1 | `1` |
| [`PersistentElement`](../Reference_and_Meta/Enums.md#enum-persistentelement) | Enum | Specifies the element type that this status effect permanently imbues (e.g., Holy). | 1 | `Holy` |
| `PhysicalAttacksMiss` | Integer | If set to 1, all physical attacks against the unit automatically miss. | 1 | `1` |
| `pickup` | Variable | A variable that marks an object as a pickup item that can be collected on the battlefield. | 21 ||
| `plant` | Variable | A variable that marks an object as a plantable item on the battlefield. | 10 ||
| [`PoolMetronome`](./Engine_StatusAndPassiveKeys.md#object-poolmetronome) | Object  | An object containing a "pool" array of ability names that the Metronome effect can randomly select from. | 1 | `{ . . . }` |
| `PreEmptiveCounterNextAttacks` | Integer | The number of next incoming attacks that the unit will counter preemptively before they land. | 2 | `1` |
| `PreventSpecificInjury` | Enum | Specifies a body part tag (e.g., 'int' for head) that cannot receive injuries. | 1 | `int` |
| [`QueueUseAbility`](../Reference_and_Meta/Enums.md#enum-queueuseability) | Enum | Specifies the ability ID to be used immediately after the current action resolves. | 1 | `Spider_GoInsane` |
| `RandomKnockbackDirection` | Integer | The number of random directions the target can be knocked back (e.g., 4 selects from 4 cardinal directions). | 1 | `4` |
| [`RandomPermanentStatsDistinct`](./Engine_StatusAndPassiveKeys.md#object-randompermanentstatsdistinct) | Object  | An object defining a set of stat changes (positive and negative) that are randomly applied as permanent modifications. | 1 | `{ . . . }` |
| [`RandomWeatherEachFight`](../Reference_and_Meta/Arrays.md#array-randomweathereachfight) | Array | An array of weather types from which one is randomly selected at the start of each battle. | 1 ||
| `RealTimePressure_OneUnit` | Integer | The amount of real-time pressure (countdown) applied to the unit each turn. | 1 | `5` |
| [`ReceivedStatusReplacement`](../Reference_and_Meta/Arrays.md#array-receivedstatusreplacement) | Array | An array specifying a status that replaces another status when it would be applied (e.g., Sleep becomes SleepParalysis). | 1 | `[Sleep SleepParalysis]` |
| `ReclaimItemOnBreak` | Integer | If set to 1, the item returns to the inventory when it breaks instead of being lost. | 1 | `1` |
| `ReduceManaCostExcludeBrainstorm` | Integer | The number of stacks reducing mana cost, excluding Brainstorm. | 2 | `1` |
| `ReduceSpellCostsPerDisorder` | Integer | The amount of mana cost reduction per disorder the unit has. | 1 | `1` |
| `ReduceSpellCostsPerParasite` | Integer | The amount of mana cost reduction per parasite the unit is hosting. | 1 | `1` |
| `ReformMoonHead` | Integer | If non-zero, triggers the Moon Head's reformation mechanic (e.g., after it eats a cat). | 1 | `1` |
| `RefreshItemAbilities` | Integer | The number of times all item abilities are recharged (cooldowns reset). | 1 | `1` |
| `RefreshNonManaItemAbilities` | Integer | The number of times non-mana item abilities are recharged. | 1 | `1` |
| `RefreshOncePerFightAbilities` | Integer | The number of times abilities limited to once per fight are refreshed. | 1 | `1` |
| `ReloadOnAllyCatDies` | Integer | If set to 1, restores a charge when an allied cat dies. | 1 | `1` |
| `ReloadOnAllyDies` | Integer | If set to 1, restores a charge when any ally dies. | 1 | `1` |
| `ReloadOnAnyDamage` | Integer | If set to 1, restores a charge when any damage is taken. | 1 | `1` |
| `ReloadOnBackstab` | Integer | If set to 1, restores a charge when performing a backstab. | 1 | `1` |
| [`ReloadOnElementalDamageReceived`](../Reference_and_Meta/Enums.md#enum-reloadonelementaldamagereceived) | Enum | Specifies the elemental type of damage that, when received, restores a charge. | 1 | `Holy` |
| `ReloadOnGainCoins` | Integer | If set to 1, restores a charge when coins are gained. | 1 | `1` |
| `ReloadOnGainDivineShield` | Integer | If set to 1, restores a charge when a Divine Shield is gained. | 1 | `1` |
| [`ReloadOnKillTagged`](../Reference_and_Meta/Enums.md#enum-reloadonkilltagged) | Enum | Specifies the tag of enemies that, when killed, restore a charge. | 1 | `rock` |
| `ReloadOnSpendMana` | Integer | If set to 1, restores a charge when mana is spent. | 1 | `1` |
| `ReloadOnUseAbilityWithManaCost` | Integer | Specifies the amount of mana cost that, when used, restores a charge. | 1 | `6` |
| `RemoteFlatLeech` | Integer | The flat amount of remote leech applied to the target on basic attack. | 1 | `1` |
| `RemoveAmbientLightEffects` | Float | The fade-out duration in seconds for ambient light effects. | 2 | `.5`<br>`4` |
| `RemoveExtraDispersedTurn` | Integer | If set to 1, the unit's turn order is not delayed by the 'Dispersed' status effect. | 1 | `1` |
| [`RemoveGlobalModifiers`](../Reference_and_Meta/Arrays.md#array-removeglobalmodifiers) | Array | List of global modifier names to remove upon death. | 1 | `[BloodRain]` |
| `RepairAllCondition` | Integer | If non-zero, fully repairs the condition of all equipped items. | 1 | `1` |
| [`ReplaceBlankTilesOnBattleStart`](../Reference_and_Meta/Enums.md#enum-replaceblanktilesonbattlestart) | Enum | Specifies a tile type (e.g., GlassTile) that replaces all blank tiles on the battle grid at the start of combat. | 1 | `GlassTile` |
| `RerollEnemy` | Integer | The number of times the target enemy is re-rolled (transformed into a new random enemy). | 1 | `1` |
| `RerollItemsOnBattleEnd` | Integer | If set to 1, all items in the unit's inventory are rerolled to new random items at the end of battle. | 1 | `1` |
| `ReturnDinoLegs` | Integer | If non-zero, returns the Dino Legs ability to the unit after it is consumed. | 1 | `1` |
| `RNGCannonRandomDamage` | Integer | The maximum random damage value for the RNG Cannon attack. | 1 | `100` |
| `RockyArmorSalvage` | Float | A multiplier for the percentage of armor value salvaged when the unit takes damage. | 1 | `.75` |
| `RunWhenKittensDead` | Integer | If set to 1, causes the character to attempt to flee when all associated kittens are dead. | 1 | `1` |
| [`RunWhenLastPlayerCatIsCharmed`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-runwhenlastplayercatischarmed) | Object  | Defines the behavior (including mid-turn decision allowance and legacy save key) for fleeing when the last player cat is charmed. | 1 | `{ . . . }` |
| [`SandStormBuff`](./Engine_StatusAndPassiveKeys.md#object-sandstormbuff) | Variable | A variable containing graphical settings (movieclip, render mode) for a sandstorm visual effect on the unit. | 2 ||
| [`ScaldingOrbMoonBossOneShot`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-scaldingorbmoonbossoneshot) | Object  | An object that completes the ScaldingOrb quest and removes the item from the unit's inventory. | 1 | `{ . . . }` |
| [`ScaledStatusAlliesOnSpendMana`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-scaledstatusalliesonspendmana) | Object  | An object that applies a scaled status (e.g., ManaGain) to adjacent allies whenever the unit spends mana. | 1 | `{ . . . }` |
| [`ScaledStatusOnBleedDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-scaledstatusonbleeddamage) | Object  | An object that applies a scaled status (e.g., Charge) on the unit when they take bleed damage. | 1 | `{ . . . }` |
| [`ScaledStatusOnHolyShieldBlock`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-scaledstatusonholyshieldblock) | Object  | An object that applies a scaled status (e.g., RandomMagicMissile) when the unit blocks an attack with a holy shield. | 1 | `{ . . . }` |
| [`ScalingAttackAnimation`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-scalingattackanimation) | Object  | Maps attack animations to damage thresholds; when the unit's attack stat reaches a threshold, the corresponding animation overrides the default. | 1 | `{ . . . }` |
| `SchizoIllusionAIModifier` | Integer | If non-zero, modifies the AI behavior for schizo illusions. | 1 | `1` |
| `SchrodingerDisorder` | Integer | A percentage chance for the unit to be simultaneously alive and dead (Schrödinger's cat) at the start of battle. | 4 | `50%` |
| `Scleroderma` | Integer | If set to 1, the unit's skin becomes hard, reducing damage but also movement. | 5 | `1` |
| [`ScrambleLastUsedSpell`](./Engine_StatusAndPassiveKeys.md#object-scramblelastusedspell) | Object  | An object containing a "permanent" boolean. If true, permanently scrambles (randomizes) the last used spell. | 1 | `{ . . . }` |
| [`self_status_next_fight`](../Reference_and_Meta/Miscellaneous.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 199 | `{ . . . }` |
| [`SelfDamageWhenDealDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-selfdamagewhendealdamage) | Object  | An object defining the damage the unit takes to itself whenever it deals damage to an enemy. | 1 | `{ . . . }` |
| [`set_WitchJump`](./Engine_StatusAndPassiveKeys.md#object-set_witchjump) | Object  | An object that configures the unit's witch jump ability (teleport-like movement). | 2 | `{ . . . }` |
| [`SetAnimationAlts`](./Engine_StatusAndPassiveKeys.md#object-setanimationalts) | Object  | Specifies alternative animation names for the target's dying and dead states. | 1 | `{ . . . }` |
| [`SetFaction`](../Reference_and_Meta/Enums.md#enum-setfaction) | Enum | Specifies the faction the unit belongs to (e.g., 'enemies'). | 1 | `enemies` |
| `ShadowCrit` | Integer | If non-zero, enables the Shadow Crit mechanic, granting bonus critical hit chance or damage from stealth. | 1 | `1` |
| [`ShineBuff`](./Engine_StatusAndPassiveKeys.md#object-shinebuff) | Variable | A variable containing graphical settings (movieclip, render mode) for a sparkling visual effect on the unit. | 2 ||
| `ShootHereCommand` | Integer | If non-zero, commands an allied unit to shoot at this unit's target. | 1 | `1` |
| `ShootHereReceiver` | Integer | If non-zero, marks this unit as the receiver of a Shoot Here command. | 1 | `1` |
| [`Shove`](./Engine_StatusAndPassiveKeys.md#object-shove) | Object  | Configures a knockback ability that pushes the target a set distance. | 5 | `{ . . . }` |
| [`SkipFirstRounds`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-skipfirstrounds) | Object  | Determines the number of initial rounds to skip and the chance per round of 'popping' (becoming active). | 1 | `{ . . . }` |
| [`SleepDart`](./Engine_StatusAndPassiveKeys.md#object-sleepdart) | Object  | Defines a projectile or targeted ability that applies the Sleep status effect on hit. | 3 | `{ . . . }` |
| `SleepParalysis` | Variable | The amount of stacks of Sleep Paralysis applied, which prevents the unit from acting while asleep. | 8 ||
| `SmallHitExplosion` | Integer | The number of small explosion VFX to spawn on hit. | 1 | `1` |
| [`SmokeBuff`](./Engine_StatusAndPassiveKeys.md#object-smokebuff) | Variable | Defines a visual particle effect (SmokeBuff) for rendering smoke or fog around the unit. | 2 ||
| [`Smough`](./Engine_StatusAndPassiveKeys.md#object-smough) | Object  | An object defining the Smough ability or template, likely a melee attack or passive with special properties. | 3 | `{ . . . }` |
| `Snow` | Integer | The number of snow particle instances or the integer value controlling snow intensity for weather effects. | 17 | `1` |
| [`Snow`](./Engine_StatusAndPassiveKeys.md#object-snow) | Float / Object  | The number of snow particle instances or the integer value controlling snow intensity for weather effects. | 17 | `{ . . . }`<br>`1` |
| [`SolarFlare`](./Engine_StatusAndPassiveKeys.md#object-solarflare) | Object  | Defines the Solar Flare weather effect, which applies damage and status effects (burn, blind) to units each turn. | 4 | `{ . . . }` |
| [`SoundEventOnHit`](../Reference_and_Meta/Enums.md#enum-soundeventonhit) | Enum | Specifies the sound event ID to play on hit (e.g., "Batterup_Connect"). | 1 | `Batterup_Connect` |
| [`SourceSwapsBackEndOfTurn`](../Reference_and_Meta/Enums.md#enum-sourceswapsbackendofturn) | Enum | Specifies the ability ID to use to swap the source unit back at the end of the turn. | 1 | `ThiefSwapBack` |
| `SpawnCatCloneOnCorpsePopped` | Integer | The number of cat clones spawned when a corpse is popped (destroyed) by the unit. | 1 | `1` |
| `SpawnCreepOnHitKnockback` | Integer | If set to 1, spawns creep on the tile where a hit knocks back an enemy. | 1 | `1` |
| `spawner` | Variable | A variable identifying the unit or object responsible for spawning other entities or effects. | 1 ||
| `SpawnerCatDataReference` | Integer | A reference ID pointing to the spawner cat's data, used by minions to link back to their spawner. | 1 | `1` |
| [`SpawnRandomPickupsOnTaggedUnitKilled`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnrandompickupsontaggedunitkilled) | Object  | Defines a pool of random pickups (items) spawned when a unit with a specific tag is killed, with a count range. | 1 | `{ . . . }` |
| [`SpawnTilePuddleOnBattleStart`](./Engine_StatusAndPassiveKeys.md#object-spawntilepuddleonbattlestart) | Object  | Defines a puddle of a specific tile type (e.g., OilTile) that is spawned on the battlefield at the start, with a radius range. | 1 | `{ . . . }` |
| `SpawnWebTrap` | Integer | The number of web traps to spawn on the target tile. | 1 | `1` |
| [`SpecialBossMultipartInstakill`](../Reference_and_Meta/Enums.md#enum-specialbossmultipartinstakill) | Enum | Specifies the boss ID (e.g., "moonboss") whose multipart instakill mechanic is triggered. | 1 | `moonboss` |
| `SpeedUp_WithoutInitiative` | Integer | The number of stacks of Speed Up that do not affect the unit's initiative (turn order) stat. | 3 | `1` |
| `SpellShield` | Integer | The number of stacks of SpellShield, which blocks incoming spells. | 3 | `1` |
| [`SpewerAltGraphics`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-speweraltgraphics) | Object  | Maps different Spewer liquid types (Normal, Fire, Tar) to their corresponding alternate graphic indices. | 1 | `{ . . . }` |
| [`SpiderReturn`](./Engine_StatusAndPassiveKeys.md#object-spiderreturn) | Object  | Defines the Spider Return ability, which teleports the unit back to a previously marked location after attacking. | 8 | `{ . . . }` |
| `SpitConsumed` | Integer | If non-zero, marks the object consumed by the Spit ability as having been used. | 1 | `1` |
| `SpreadWater` | Integer | If set to 1, causes the character to spread water onto adjacent tiles. | 1 | `1` |
| `sprout` | Variable | A variable associated with plant-based growth or spawning mechanics, likely a seed or sprout identifier. | 2 ||
| `SproutsGrantMovement` | Integer | If set to 1, sprouts on the character grant additional movement (aliases to MovementUp). | 2 | `1` |
| [`StacyMutant_Brace`](./Engine_StatusAndPassiveKeys.md#object-stacymutant_brace) | Object  | A passive group granting the Brace ability and cosmetic changes. | 2 | `{ . . . }` |
| [`StacyMutant_Counter`](./Engine_StatusAndPassiveKeys.md#object-stacymutant_counter) | Object  | A passive group granting a counter attack and a bleed effect on basic attacks. | 2 | `{ . . . }` |
| [`StacyMutant_Damage`](./Engine_StatusAndPassiveKeys.md#object-stacymutant_damage) | Object  | A passive group increasing damage and decreasing max health with cosmetic changes. | 2 | `{ . . . }` |
| [`StacyMutant_DoubleHead`](./Engine_StatusAndPassiveKeys.md#object-stacymutant_doublehead) | Object  | A passive group granting an extra dispersed turn and cosmetic changes. | 2 | `{ . . . }` |
| [`StacyMutant_Fire`](./Engine_StatusAndPassiveKeys.md#object-stacymutant_fire) | Object  | A passive group granting fire immunity and a lava shot basic attack. | 2 | `{ . . . }` |
| [`StacyMutant_Health`](./Engine_StatusAndPassiveKeys.md#object-stacymutant_health) | Object  | A passive group increasing max health, reducing speed, and scaling size. | 2 | `{ . . . }` |
| [`StacyMutant_Holy`](./Engine_StatusAndPassiveKeys.md#object-stacymutant_holy) | Object  | A passive group granting a divine shield and cosmetic changes. | 2 | `{ . . . }` |
| [`StacyMutant_Ice`](./Engine_StatusAndPassiveKeys.md#object-stacymutant_ice) | Object  | A passive group granting ice immunity and an ice breath basic attack. | 2 | `{ . . . }` |
| [`StacyMutant_Lightning`](./Engine_StatusAndPassiveKeys.md#object-stacymutant_lightning) | Object  | A passive group granting electric immunity and a lightning dash basic attack. | 2 | `{ . . . }` |
| [`StacyMutant_Mirror`](./Engine_StatusAndPassiveKeys.md#object-stacymutant_mirror) | Object  | A passive group granting projectile reflection and random magic missile each turn. | 2 | `{ . . . }` |
| [`StacyMutant_Speed`](./Engine_StatusAndPassiveKeys.md#object-stacymutant_speed) | Object  | A passive group increasing speed, reducing damage, and scaling size. | 2 | `{ . . . }` |
| [`StacyMutant_Thorns`](./Engine_StatusAndPassiveKeys.md#object-stacymutant_thorns) | Object  | A passive group granting thorns damage and cosmetic changes. | 2 | `{ . . . }` |
| `StartDead` | Integer | The percentage chance that the character starts the battle already dead. | 1 | `100%` |
| `StatBounty` | Integer | The number of stacks of the StatBounty status effect. | 2 | `1` |
| [`StatDependentPassive`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statdependentpassive) | Object  | An object containing formulas that dynamically modify passive effects based on the unit's stats (e.g., str, dex, int). | 1 | `{ . . . }` |
| [`StatusAdjacentOnTheirTurnBegin`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusadjacentontheirturnbegin) | Object  | Defines a status effect applied to adjacent units when their turn begins, such as forcing them to move away. | 1 | `{ . . . }` |
| [`StatusAdjacentOnTheirTurnEnd`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusadjacentontheirturnend) | Object  | Defines a status effect applied to adjacent units when their turn ends, such as forcing them to move away. | 1 | `{ . . . }` |
| [`StatusAfterXStacks`](./Engine_StatusAndPassiveKeys.md#object-statusafterxstacks) | Object  | Defines a condition that triggers a status effect when a specified stack key reaches a threshold, optionally expiring at turn end. | 2 | `{ . . . }` |
| [`StatusAlliesEachTurn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusallieseachturn) | Object  | Defines a status effect applied to all allies each turn, with an optional exclusion of the owner and conditional checks. | 2 | `{ . . . }` |
| [`StatusEachTurnBeginIfHasStatus`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnbeginifhasstatus) | Object  | Defines a status effect to apply (and optionally consume) at the start of each turn if the character already has a specific status, with a specified animation. | 1 | `{ . . . }` |
| [`StatusEachTurnEndIfEnabledAtStartOfTurn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnendifenabledatstartofturn) | Object  | Defines an ability to force-use at the end of each turn if the character was in the specified form at the start of the turn. | 1 | `{ . . . }` |
| [`StatusIfBattleAlreadyBegan`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusifbattlealreadybegan) | Object  | Defines a status effect that is applied only if the battle has already started (not on the first turn). | 1 | `{ . . . }` |
| [`StatusOnDodge`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusondodge) | Object  | Defines a status effect applied to the unit each time it successfully dodges an attack. | 1 | `{ . . . }` |
| [`StatusOnEnemyCastSpell`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonenemycastspell) | Object  | Defines a status effect applied to the unit each time an enemy casts a spell. | 1 | `{ . . . }` |
| [`StatusOnEnemyConfused`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonenemyconfused) | Object  | Defines an ability to immediately use when an enemy becomes confused. | 1 | `{ . . . }` |
| [`StatusOnEnemyDeath`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonenemydeath) | Object  | Defines a status effect applied to the unit each time an enemy dies. | 1 | `{ . . . }` |
| [`StatusOnFallAsleep`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonfallasleep) | Object  | Defines one or more beneficial status effects applied to the unit when it falls asleep. | 1 | `{ . . . }` |
| [`StatusOnFullMana`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonfullmana) | Object  | Defines a status effect applied to the unit when its mana is full, with an optional once-per-battle conditional. | 1 | `{ . . . }` |
| [`StatusOnLoseShield`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonloseshield) | Object  | Defines a status effect applied to the unit each time it loses a shield point. | 1 | `{ . . . }` |
| [`StatusOnTakeHealthDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusontakehealthdamage) | Object  | Defines a status effect applied to the unit each time it takes health damage, such as a permanent stat reduction. | 1 | `{ . . . }` |
| [`StatusOverlappingCharactersAndDie`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusoverlappingcharactersanddie) | Object  | Defines a status effect applied to overlapping characters, after which the character dies. | 1 | `{ . . . }` |
| [`StatusWhenStatusCompletelyRemoved`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuswhenstatuscompletelyremoved) | Object  | Defines a status to apply and an ability to use when a specific status is completely removed from the character. | 1 | `{ . . . }` |
| `StealDemonicGlyph` | Integer | The number of Demonic Glyphs stolen from the target. | 1 | `1` |
| [`StealEquipment`](../Reference_and_Meta/Enums.md#enum-stealequipment) | Enum | Specifies the type of equipment to steal (e.g., "any") from the target. | 1 | `any` |
| `StealthCritChance` | Integer | The percentage chance to critically hit while stealthed. | 1 | `100` |
| `StealthUntilBasicAttack` | Integer | The number of stacks of Stealth that are removed when the unit performs a basic attack. | 2 | `1` |
| `StealTurn` | Integer | The number of turns stolen from the target to grant to the attacker. | 1 | `1` |
| `StevenBolts` | Integer | The number of Steven Bolts (a special resource or charge) the unit has for a unique ability. | 1 | `1` |
| `StrictLimitDamage` | Integer | The amount of damage strict limit applies, capping incoming damage to a fixed value per hit. | 1 | `1` |
| `StripKnockback` | Integer | If non-zero, removes all knockback effects from the unit's attacks or abilities. | 1 | `1` |
| [`SupportDieInsteadOfRun`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-supportdieinsteadofrun) | Object  | Configures alternative dying and dead animations for support units that die instead of fleeing. | 1 | `{ . . . }` |
| [`SwapWeapon`](./Engine_StatusAndPassiveKeys.md#object-swapweapon) | Object  | An object containing a "pool" array of weapon names to randomly swap to. | 1 | `{ . . . }` |
| [`SwimmingFormChange`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-swimmingformchange) | Object  | Defines the form names to switch to when in water and when exiting water. | 1 | `{ . . . }` |
| [`SyncFormsWithBuddy`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-syncformswithbuddy) | Object  | Specifies the form to revert to if the character has no buddy, ensuring form synchronization. | 1 | `{ . . . }` |
| `T2CopyCatInternal` | Variable | An internal variable used by the T2 Copy Cat passive to track clone spawning state. | 2 ||
| [`T3HitlerSpawningPhase`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-t3hitlerspawningphase) | Object  | Defines weighted groups of spawn abilities used during the T3Hitler boss's spawning phase. | 1 | `{ . . . }` |
| `T3HitlerTriggerInitialSpawns` | Integer | If non-zero, triggers the initial spawn sequence for the T3 Hitler boss. | 1 | `1` |
| [`TagMetronome`](../Reference_and_Meta/Enums.md#enum-tagmetronome) | Enum | Specifies a tag (e.g., "musical") used to filter which abilities the Metronome effect can pick. | 1 | `musical` |
| [`TakeBonusTurnWithStatus`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-takebonusturnwithstatus) | Object  | Container for status effects applied when taking a bonus turn. | 5 | `{ . . . }` |
| `TakeExtraTurnEndOfRound` | Integer | The number of extra turns taken at the end of the round. | 1 | `1` |
| `TakeWeaponFromSpawner` | Integer | If set to 1, the minion inherits the weapon from its spawner. | 1 | `1` |
| `Tall` | Integer | If set to 1, the character occupies a taller hitbox or sprite space. | 16 | `1` |
| [`TallTumorManaBurn`](../Reference_and_Meta/Enums.md#enum-talltumormanaburn) | Enum | Specifies the mana burn ability used by the TallTumor. | 1 | `TT_ManaBurn` |
| `TargetedMetronome` | Integer | The number of random targets hit by the Targeted Metronome effect. | 1 | `20` |
| [`TattersFear`](./Engine_StatusAndPassiveKeys.md#object-tattersfear) | Object  | Defines a targeted fear ability that causes the target to flee in a random direction. | 3 | `{ . . . }` |
| `TauntAtFullHealth` | Integer | The number of stacks of Taunt applied to the unit when it is at full health. | 1 | `1` |
| `Taunting` | Integer | The number of stacks of Taunting, which forces enemies to target the unit. | 3 | `1` |
| [`TC_DashReaction`](./Engine_StatusAndPassiveKeys.md#object-tc_dashreaction) | Object  | Defines a trample dash reaction ability that triggers when a unit dashes, dealing damage to enemies in the path. | 3 | `{ . . . }` |
| [`TeamBonusAbility`](../Reference_and_Meta/Enums.md#enum-teambonusability) | Enum | Specifies the ability ID granted to allies as a team bonus. | 1 | `ShootHere` |
| [`TeleportBackAtTurnEnd`](../Reference_and_Meta/Enums.md#enum-teleportbackatturnend) | Enum | Specifies the ability ID used to teleport the unit back to its starting position at turn end. | 1 | `FlashBack` |
| `TempBackstab` | Integer | The amount of temporary backstab bonus, typically as a percentage. | 2 | `75` |
| `TempBackstabBleed` | Integer | The number of temporary Bleed status stacks applied on a backstab attack. | 1 | `1` |
| `TempBackstabPiercing` | Integer | The amount of temporary piercing added to backstab attacks. | 1 | `1` |
| `TempBackstabPoison` | Integer | The amount of temporary poison stacks applied with backstab attacks. | 1 | `1` |
| `TempBasicAttackBonusAOE` | Integer | The amount of temporary area-of-effect bonus on basic attacks. | 1 | `1` |
| `TempBonusKnockback` | Integer | The number of stacks of temporary bonus knockback distance. | 2 | `1` |
| `TempBonusKnockbackDamage` | Integer | The number of stacks of temporary bonus knockback damage. | 2 | `1` |
| `TempInjuryImmunity` | Integer | The number of stacks of temporary immunity to Injuries. | 2 | `1` |
| `TempManaCostReduction` | Integer | The number of stacks of temporary mana cost reduction. | 2 | `1` |
| `TempMeleeRangeUp` | Integer | The number of tiles added to the unit's melee attack range as a temporary buff. | 1 | `1` |
| `TempPenetrate` | Integer | The amount of temporary penetration applied to attacks. | 1 | `1` |
| `TempPreEmptiveCounterAttack` | Integer | The number of turns of temporary pre-emptive counterattack status. | 2 | `1` |
| [`Terminator2Chase`](../Reference_and_Meta/Enums.md#enum-terminator2chase) | Enum | Specifies the movement ability used by Terminator2 when chasing the target. | 1 | `move` |
| [`Terminator2Run`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-terminator2run) | Object  | Defines the movement ability and movement weights used by Terminator2 when running away. | 1 | `{ . . . }` |
| [`TerminatorChase`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-terminatorchase) | Object  | Defines the movement ability and reaction ability used by Terminator1 when chasing a target, plus whether it prioritizes player cats. | 1 | `{ . . . }` |
| [`TerminatorSkin`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-terminatorskin) | Object  | Defines the status effect and groups of stacks applied by the Terminator's skin passive. | 1 | `{ . . . }` |
| [`TheCreator_SpawnCloneTeam`](./Engine_StatusAndPassiveKeys.md#object-thecreator_spawncloneteam) | Object  | Defines an ability that spawns a team of clones of the original cat, controlled by The Creator. | 3 | `{ . . . }` |
| [`TheHunger`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-thehunger) | Object  | Defines the Hunger passive, which applies Madness or other effects each turn, representing a disorder. | 5 | `{ . . . }` |
| [`ThornUp`](./Engine_StatusAndPassiveKeys.md#object-thornup) | Object  | Defines a self-buff ability that increases the unit's Thorns damage, reflecting damage back to attackers. | 3 | `{ . . . }` |
| [`ThrobbingKing2`](./Engine_StatusAndPassiveKeys.md#object-throbbingking2) | Object  | An object defining the Throbbing King 2 ability, likely a boss attack or passive with pulsing damage or effects. | 3 | `{ . . . }` |
| [`TickDownStatus`](../Reference_and_Meta/Enums.md#enum-tickdownstatus) | Enum | Specifies the name of the status effect whose duration is reduced by one tick. | 1 | `ShortCircuit` |
| [`TileElementDamageImmunity`](../Reference_and_Meta/Enums.md#enum-tileelementdamageimmunity) | Enum | Determines which tile element type the character is immune to damage from. | 1 | `Ice` |
| `TilesMovedToCritChance` | Integer | The number of stacks of a status that grants critical hit chance based on tiles moved. | 3 | `1` |
| `TilesMovedToMana` | Integer | The number of stacks of a status that grants mana based on tiles moved. | 3 | `1` |
| [`TilesMovedToNeighborHeal`](../Reference_and_Meta/Enums.md#enum-tilesmovedtoneighborheal) | Enum | Specifies the scaling type for healing neighbors based on tiles moved (e.g., 'level'). | 3 | `level` |
| `TilesMovedToStrength` | Integer | The number of stacks of a status that grants strength based on tiles moved. | 3 | `1` |
| [`TintItem`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-tintitem) | Object  | Defines additive and multiplicative color tint adjustments applied to an item's appearance, with an optional ignore condition. | 1 | `{ . . . }` |
| `TireBehavior` | Integer | If set to 1, activates special tire-related behavior for the character. | 1 | `1` |
| `TormentorHeal` | Integer | If set to 1, the Tormentor can heal itself. | 1 | `1` |
| [`TormentorRuneAbsorb`](./Engine_StatusAndPassiveKeys.md#object-tormentorruneabsorb) | Object  | Defines a spell ability that absorbs runes or energy from a target, typically used by the Tormentor enemy. | 3 | `{ . . . }` |
| `TossTargetIsAggroTarget` | Integer | If set to 1, the toss target is the unit's current aggro target. | 1 | `1` |
| `TossTargetIsBuddy` | Integer | If set to 1, the toss target is the unit's buddy. | 1 | `1` |
| `TossTargetIsNotInWater` | Integer | If set to 1, the toss target must not be in water terrain. | 1 | `1` |
| [`TourettesMeows`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-tourettesmeows) | Object  | Defines a passive that triggers random vocalizations (hiss, hit, normal) at random cooldown intervals. | 1 | `{ . . . }` |
| `TowerDefenseStatus` | Integer | The number of stacks of the sentry/tower defense status, granting stationary attack capabilities. | 2 | `1` |
| `TowerDefenseStatus2` | Integer | The number of stacks of the enhanced sentry/tower defense status. | 2 | `1` |
| [`ToxicBubbles`](./Engine_StatusAndPassiveKeys.md#object-toxicbubbles) | Variable | A variable defining the visual particle effect for toxic bubbles, used for environmental hazards or attacks. | 2 ||
| [`ToxPuff`](./Engine_StatusAndPassiveKeys.md#object-toxpuff) | Object  | Defines a self-buff ability that creates a toxic puff visual effect around the unit. | 2 | `{ . . . }` |
| [`TrackAmountKilledByPlayer`](../Reference_and_Meta/Enums.md#enum-trackamountkilledbyplayer) | Enum | Specifies the name of the counter used to track how many of this type the player has killed. | 1 | `BonusBirdsKilled` |
| [`TransformBasicMove`](../Reference_and_Meta/Enums.md#enum-transformbasicmove) | Enum | Specifies the name of the basic move to transform into. | 1 | `BasicDashAttackMove_NoKnockback` |
| [`TransformEquipment`](./Engine_StatusAndPassiveKeys.md#object-transformequipment) | Object  | Defines an equipment transformation from one item to another, with 'from' and 'to' sub-keys. | 2 | `{ . . . }` |
| [`TransformNow`](../Reference_and_Meta/Enums.md#enum-transformnow) | Enum | Specifies the name of the form to immediately transform into. | 1 | `Hitler` |
| [`TransformOnStatusThreshold`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-transformonstatusthreshold) | Object  | Defines the status effect, the stack threshold at which to transform, and the object to transform into. | 1 | `{ . . . }` |
| `Trapper_Status` | Integer | The number of trap-related status stacks applied. | 1 | `1` |
| [`TrexSwitchTarget`](./Engine_StatusAndPassiveKeys.md#object-trexswitchtarget) | Object  | Defines a targeted status ability that forces an enemy to switch its target to the caster. | 3 | `{ . . . }` |
| `TriggerBleedOnBleed` | Integer | If non-zero, causes the unit to trigger additional bleed effects whenever it applies bleed to an enemy. | 1 | `1` |
| `TriggerMotherConsume` | Integer | The number of times the Mother consume effect is triggered. | 1 | `1` |
| `TriggerMotherGrow` | Integer | The number of times the Mother grow effect is triggered. | 1 | `4` |
| `Triskaidekaphobia` | Integer | The threshold number (typically 13) at which a negative effect triggers due to the disorder Triskaidekaphobia. | 6 | `13` |
| [`TT_Thrash`](./Engine_StatusAndPassiveKeys.md#object-tt_thrash) | Object  | Defines a melee attack ability that uses the thrash animation and deals damage to the target. | 3 | `{ . . . }` |
| `tumor` | Variable | A variable identifying a tumor growth passive or effect, likely related to status application or visual changes. | 21 ||
| [`TunnelVision`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-tunnelvision) | Object  | If present, grants the TunnelVision status, which modifies crit_chance as defined in its sub-properties. | 1 | `{ . . . }` |
| `TurnAround` | Integer | The number of times the unit turns around. | 1 | `1` |
| `TurnControlDelay` | Float | Specifies the delay in seconds before the unit regains turn control. | 1 | `.25` |
| `TurnRight` | Integer | The number of times the unit turns to the right. | 1 | `1` |
| `TutorialBossRiggedFight` | Integer | The turn count at which the tutorial boss fight becomes rigged. | 1 | `16` |
| `TVBotDisableAttack` | Integer | If set to 1, disables the TVBot's ability to attack. | 1 | `1` |
| `TVBotDisableMove` | Integer | If set to 1, disables the TVBot's ability to move. | 1 | `1` |
| `TVBotDisableSpells` | Integer | If set to 1, disables the TVBot's ability to use spells. | 1 | `1` |
| [`TVBotScreen`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-tvbotscreen) | Object  | Maps TVBot screen channel names to their corresponding form indices. | 1 | `{ . . . }` |
| `Twister_loop` | Enum | Specifies which loop animation to use for the Twister effect. | 1 ||
| [`TwisterFling`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-twisterfling) | Object  | Defines the minimum distance, maximum distance, and damage for the TwisterFling ability. | 1 | `{ . . . }` |
| [`UFO_BigExplode`](./Engine_StatusAndPassiveKeys.md#object-ufo_bigexplode) | Object  | Defines the visual and template properties for the UFO's large explosion effect. | 2 | `{ . . . }` |
| [`UltraSmough`](./Engine_StatusAndPassiveKeys.md#object-ultrasmough) | Object  | Defines the properties for the UltraSmough entity or status. | 3 | `{ . . . }` |
| `UndoDamage` | Integer | The amount of damage reversed. | 1 | `1` |
| [`UnlimitedDeathRattleRevive`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-unlimiteddeathrattlerevive) | Object  | Configures an unlimited revive effect, including the ability to use and whether it works even when stunned. | 1 | `{ . . . }` |
| `UpTireBehavior` | Integer | The behavior type integer for the Tire's upward form. | 1 | `5` |
| [`UseAbility_Madness`](../Reference_and_Meta/Enums.md#enum-useability_madness) | Enum | Determines which ability type (e.g., weapon) is forcibly used when Madness triggers. | 1 | `weapon` |
| [`UseAbilityWhenOutOfStatus`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-useabilitywhenoutofstatus) | Object  | Defines an ability to execute when the unit no longer has a specified status. | 1 | `{ . . . }` |
| [`UseAbilityWhenShieldDepleted`](../Reference_and_Meta/Enums.md#enum-useabilitywhenshielddepleted) | Enum | The ability to use when the unit's shield is fully depleted. | 1 | `T3Pebbles_PrimeBoulderDrop` |
| [`UseMoveAbilityWithAI`](./Engine_StatusAndPassiveKeys.md#object-usemoveabilitywithai) | Object  | Defines a move ability to execute with AI-controlled movement weights. | 1 | `{ . . . }` |
| `UseRandomSpell_Madness` | Integer | The number of random spells cast when Madness triggers. | 1 | `1` |
| `VaporizeDice` | Integer | The number of dice vaporized. | 1 | `1` |
| [`VisualCountDownThenApplyStatus`](./Engine_StatusAndPassiveKeys.md#object-visualcountdownthenapplystatus) | Object  | Contains a visual countdown sequence that culminates in applying a status effect, optionally forcing an ability use. | 1 | `{ . . . }` |
| [`WaggleClone`](./Engine_StatusAndPassiveKeys.md#object-waggleclone) | Object  | Defines a waggle clone ability with health thresholds and object sizes. | 4 | `{ . . . }` |
| `Wall` | Integer | If 1, the unit is treated as an impassable wall. | 5 | `1` |
| `Wet` | Integer | The number of stacks of the Wet status effect applied. | 2 | `1` |
| [`WhitelistPickupType`](../Reference_and_Meta/Enums.md#enum-whitelistpickuptype) | Enum | Specifies the type of pickup that this unit is allowed to collect. | 1 | `food` |
| `WideBackstab` | Integer | The additional width for backstab attacks, in tiles. | 1 | `1` |
| [`Wind`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-wind) | Object  | Defines the properties for the Wind element, such as knockback amount. | 75 | `{ . . . }` |
| `Windy` | Integer | The number representing the Windy weather intensity or whether it is active. | 12 | `1`<br>`10` |
| [`Windy`](./Engine_StatusAndPassiveKeys.md#object-windy) | Float / Object  | The number representing the Windy weather intensity or whether it is active. | 12 | `{ . . . }`<br>`1`<br>`10` |
| `WispDodge` | Integer | If 1, the unit gains the Wisp's dodge ability. | 1 | `1` |
| `WobblyCat` | Integer | The chance (as a percentage) or stack count for the WobblyCat disorder. | 5 | `25%` |
| `XIsConsumedCharacterMaxHP` | Integer | Specifies the multiplier used to set X to the maximum HP of the consumed character. | 1 | `3` |
| `XIsCountDeaths` | Integer | If set to 1, X is equal to the number of deaths in the match. | 1 | `1` |
| [`XIsCountStatusStacks`](../Reference_and_Meta/Enums.md#enum-xiscountstatusstacks) | Enum | Specifies the status field whose stacks are counted to set X. | 1 | `DodgeChance_Status` |
| `XIsFormulaLockedUntilComplete` | Enum | Specifies a stat (e.g., dex) whose value is locked in and used for X until the ability completes. | 1 | `dex` |
| `XIsIncreaseEachTurn` | Integer | Specifies the amount by which X increases each turn. | 1 | `1` |
| `XIsRampAndReset` | Integer | If set to 1, X ramps up over time and resets after use; 0 disables this behavior. | 1 | `0` |
| `XIsRecycleCostReduction` | Integer | Specifies the amount of recycle cost reduction applied to X. | 1 | `5` |
| `ZeroKnockbackDamage` | Integer | If 1, the unit takes no damage from knockback effects. | 1 | `1` |
| [`AcidRain`](./Engine_StatusAndPassiveKeys.md#object-acidrain) | Float / Object  | If non-zero, enables the Acid Rain weather effect dealing damage each turn. | 4 | `{ . . . }`<br>`2` |
| `Adrenaline` | Integer | The flat amount of Adrenaline (a resource or stat) granted to the unit. | 2 | `10` |
| `Ammo` | Integer | The amount of ammo to add or remove (negative values subtract). | 15 | `-1`<br>`-99999`<br>`1` |
| `Bloodzerked` | Integer | The number of Bloodzerk stacks applied. | 2 | `1` |
| [`BombRatTurtle`](./Engine_StatusAndPassiveKeys.md#object-bombratturtle) | Integer / Object  | The number of bomb rat turtle spawns triggered. | 4 | `{ . . . }`<br>`1` |
| [`BounceRock`](../Reference_and_Meta/Arrays.md#array-bouncerock) | Array / Enum  | Specifies the rock object to bounce. | 6 | `LavaBoulder`<br>`SmallLavaRock`<br>`SmallRock` |
| [`ButterflySwarm`](./Engine_StatusAndPassiveKeys.md#object-butterflyswarm) | Float / Object  | The number of butterflies spawned for the Butterfly Swarm effect. | 4 | `{ . . . }`<br>`2` |
| `ChampionUpgradeNextMinion` | Integer | The number of champion upgrades applied to the next spawned minion. | 2 | `1` |
| [`CockroachSwarm`](./Engine_StatusAndPassiveKeys.md#object-cockroachswarm) | Float / Object  | If true, the unit spawns as a Cockroach Swarm, with its specific mechanics and effects. | 3 | `{ . . . }`<br>`1` |
| `CollideWithConsumed` | String | Damage formula for collision with consumed objects, e.g., '4+bonus_melee_damage'. | 3 | `1+bonus_melee_damage`<br>`4+bonus_melee_damage`<br>`5+bonus_melee_damage` |
| [`CopySpells`](./Engine_StatusAndPassiveKeys.md#object-copyspells) | Integer / Object  | The number of spells copied from the target, or an object specifying `stacks` and whether the copy is `upgraded`. | 2 | `{ . . . }`<br>`1` |
| [`Counterspell`](./Engine_StatusAndPassiveKeys.md#object-counterspell) | Integer / Object  | If non-zero, negates the next incoming enemy spell and triggers the configured counterspell effects. | 6 | `{ . . . }`<br>`1` |
| [`DelayCastAbility`](./Engine_StatusAndPassiveKeys.md#object-delaycastability) | Enum / Object  | Specifies the name of an ability to cast after a delay. | 2 | `{ . . . }`<br>`HitlerNuke` |
| [`DelayCastAbility`](./Engine_StatusAndPassiveKeys.md#object-delaycastability) | Enum / Object  | Specifies the name of an ability to cast after a delay. | 2 | `{ . . . }`<br>`HitlerNuke` |
| `DoubleCast` | Integer | The number of double-cast stacks, allowing a spell to be cast twice. | 3 | `1` |
| `DoubleCastSpell` | Integer | The number of times the next spell cast is doubled, or a template with name and tooltip. | 6 | `1`<br>`2` |
| `EliteUpgradeNextMinion` | Integer | The number of elite upgrades applied to the next spawned minion. | 2 | `1` |
| [`FactionUprising`](./Engine_StatusAndPassiveKeys.md#object-factionuprising) | Enum / Object  | Specifies which faction triggers a global uprising event, adding allied units of that faction. | 4 | `{ . . . }`<br>`alien`<br>`ghost`<br>`robot` |
| [`FireArmor`](./Engine_StatusAndPassiveKeys.md#object-firearmor) | Integer / Object  | The number of Fire Armor stacks providing damage reflection. | 6 | `{ . . . }`<br>`1` |
| [`FireArmor2`](./Engine_StatusAndPassiveKeys.md#object-firearmor2) | Integer / Object  | The number of Fire Armor2 stacks (likely a variant). | 4 | `{ . . . }`<br>`1` |
| [`FireflySwarm`](./Engine_StatusAndPassiveKeys.md#object-fireflyswarm) | Float / Object  | The number of fireflies in the swarm effect. | 4 | `{ . . . }`<br>`2` |
| [`FireStorm`](./Engine_StatusAndPassiveKeys.md#object-firestorm) | Float / Object  | The percentage chance or combo definition for the Fire Storm effect. | 3 | `{ . . . }`<br>`0%`<br>`33%` |
| [`Fog`](./Engine_StatusAndPassiveKeys.md#object-fog) | Float / Object  | When an integer, the intensity of fog; when an object, defines the fog particle effect. | 5 | `{ . . . }`<br>`1` |
| [`ForceMoveTowardsEnemies`](../Reference_and_Meta/Enums.md#enum-forcemovetowardsenemies) | Enum / Integer  | Specifies the ability or distance to force the target to move towards enemies. | 3 | `1`<br>`DumbMove_Impl`<br>`MoveOne` |
| [`Grappled`](../Reference_and_Meta/Arrays.md#array-grappled) | Array / Integer  | The number of stacks and probability of applying the Grappled status, in format [stacks, probability] or just stacks. | 9 | `1`<br>`[1, .50]`<br>`[1, .75]` |
| [`HeatWave`](./Engine_StatusAndPassiveKeys.md#object-heatwave) | Array / Float / Object  | When an integer, the intensity of the heat wave; when an object, defines the visual effects or status properties. | 7 | `{ . . . }`<br>`1` |
| `HeavyHits` | Integer | The number of Heavy Hits stacks increasing attack impact. | 2 | `1` |
| `IgnoreSelf` | Boolean / Integer | If set to 1 or true, the damage instance ignores the source unit (does not affect itself). | 75 | `1`<br>`true` |
| `Invulnerable` | Integer | The number of Invulnerable stacks, making the unit immune to damage. | 2 | `1` |
| [`JudgementDay`](./Engine_StatusAndPassiveKeys.md#object-judgementday) | Float / Object  | When an integer, the turn count or damage for Judgement Day; when an object, defines the weather status. | 3 | `{ . . . }`<br>`25` |
| [`KnockbackDirectionIsFacingDirection`](../Reference_and_Meta/Enums.md#enum-knockbackdirectionisfacingdirection) | Enum / Integer  | Specifies how to alter knockback direction relative to the unit's facing: 1 (same), flip (opposite), rotate_right. | 5 | `1`<br>`flip`<br>`rotate_right` |
| `Meaty` | Integer | The number of Meaty stacks increasing health or size. | 3 | `1` |
| [`Meteornado`](./Engine_StatusAndPassiveKeys.md#object-meteornado) | Float / Object  | The number of Meteornado status stacks applied, or an object defining its visual effects. | 6 | `{ . . . }`<br>`1` |
| [`MeteorShower`](./Engine_StatusAndPassiveKeys.md#object-meteorshower) | Float / Object  | The chance (as a percentage) for a meteor shower to occur on a given turn. | 4 | `{ . . . }`<br>`25%` |
| `Muted` | Integer | The number of Muted stacks, disabling certain abilities. | 2 | `1` |
| `NextAbilityHeals` | Integer | The number of stacks causing the next ability to heal instead of damage. | 3 | `1` |
| `NextActionLuckUp` | Integer | The number of stacks increasing luck for the next action. | 2 | `99` |
| `NextAttackBonusRange` | Integer | The added range for the unit's next basic attack. | 4 | `1`<br>`3`<br>`5` |
| [`NextAttackSpecialCrit`](./Engine_StatusAndPassiveKeys.md#object-nextattackspecialcrit) | Integer / Object  | The number of charges for a special crit on the next attack, or an object defining its bonus properties. | 2 | `{ . . . }`<br>`1` |
| [`NextBasicAttackCritsThisTurn`](./Engine_StatusAndPassiveKeys.md#object-nextbasicattackcritsthisturn) | Object  | An object or number configuring the next basic attack to be a critical hit this turn. An object may contain stack, cant_miss, or piercing sub-keys. | 3 | `{ . . . }` |
| `NextDamageReduceAndHealAllies` | Integer | The number of stacks reducing next damage and healing nearby allies. | 3 | `1` |
| `NextTurnDoubleRangedDamage` | Integer | The number of stacks doubling ranged damage on the next turn. | 2 | `1` |
| `OverrideKnockbackDamage` | Enum / Equation | A formula or flat value that sets the damage dealt when knockback occurs, overriding default calculations. | 17 | `"max(5+bonus_melee_ability_damage, 1)"`<br>`0`<br>`2` |
| `OverrideKnockbackDamage` | Enum / Equation | A formula or flat value that sets the damage dealt when knockback occurs, overriding default calculations. | 17 | `"max(5+bonus_melee_ability_damage, 1)"`<br>`0`<br>`2` |
| `PermanentImmobile` | Integer | The permanent amount of immobility stacks applied. | 3 | `1` |
| [`RandomDistanceDisplace`](./Engine_StatusAndPassiveKeys.md#object-randomdistancedisplace) | Integer / Object  | The number of stacks of a random distance displacement effect, or an object with stacks, min_dist, and chance. | 4 | `{ . . . }`<br>`20` |
| `ReduceManaCostExcludeBrainstorm` | Integer | The number of stacks reducing mana cost, excluding Brainstorm. | 2 | `1` |
| [`ScatterHeldCoin`](../Reference_and_Meta/Arrays.md#array-scatterheldcoin) | Array / Integer  | The number of coins scattered, with an optional probability as a second element. | 6 | `1`<br>`[1 .3]`<br>`[1 .5]` |
| [`SelfStun`](../Reference_and_Meta/Arrays.md#array-selfstun) | Array / Integer  | The number of stacks of self-stun applied, with an optional probability as a second element. | 2 | `1`<br>`[1 .5]` |
| [`Shatter`](./Engine_StatusAndPassiveKeys.md#object-shatter) | Integer / Object  | The amount of damage dealt when a frozen or petrified status is shattered, or a template definition for a Shatter ability. | 5 | `{ . . . }`<br>`15` |
| [`SpawnRock`](../Reference_and_Meta/Arrays.md#array-spawnrock) | Array / Integer  | The number of rocks to spawn, or an array with stacks and probability. | 5 | `1`<br>`[1, .20]` |
| `SpellShield` | Integer | The number of stacks of SpellShield, which blocks incoming spells. | 3 | `1` |
| `StatBounty` | Integer | The number of stacks of the StatBounty status effect. | 2 | `1` |
| `Taunting` | Integer | The number of stacks of Taunting, which forces enemies to target the unit. | 3 | `1` |
| [`TeamCastAbility`](./Engine_StatusAndPassiveKeys.md#object-teamcastability) | Enum / Object  | Specifies the ability name for the team to cast, with optional tag restriction and same orientation. | 6 | `{ . . . }`<br>`Huddle_Impl`<br>`Spin`<br>`TeamFlex_Impl` |
| `TempBackstab` | Integer | The amount of temporary backstab bonus, typically as a percentage. | 2 | `75` |
| `TempBonusKnockback` | Integer | The number of stacks of temporary bonus knockback distance. | 2 | `1` |
| `TempBonusKnockbackDamage` | Integer | The number of stacks of temporary bonus knockback damage. | 2 | `1` |
| `TempCritChanceUp` | Integer | The amount of temporary critical hit chance (in percentage points) added. | 3 | `100`<br>`30` |
| `TempInitiativeChange` | Integer | The flat change to the unit's initiative value. | 5 | `-100`<br>`-999`<br>`100` |
| `TempInitiativeChange` | Integer | The flat change to the unit's initiative value. | 5 | `-100`<br>`-999`<br>`100` |
| `TempInjuryImmunity` | Integer | The number of stacks of temporary immunity to Injuries. | 2 | `1` |
| `TempManaCostReduction` | Integer | The number of stacks of temporary mana cost reduction. | 2 | `1` |
| `TempPreEmptiveCounterAttack` | Integer | The number of turns of temporary pre-emptive counterattack status. | 2 | `1` |
| `TilesMovedToCritChance` | Integer | The number of stacks of a status that grants critical hit chance based on tiles moved. | 3 | `1` |
| `TilesMovedToMana` | Integer | The number of stacks of a status that grants mana based on tiles moved. | 3 | `1` |
| [`TilesMovedToNeighborHeal`](../Reference_and_Meta/Enums.md#enum-tilesmovedtoneighborheal) | Enum  | Specifies the scaling type for healing neighbors based on tiles moved (e.g., 'level'). | 3 | `level` |
| `TilesMovedToStrength` | Integer | The number of stacks of a status that grants strength based on tiles moved. | 3 | `1` |
| `TowerDefenseStatus` | Integer | The number of stacks of the sentry/tower defense status, granting stationary attack capabilities. | 2 | `1` |
| `TowerDefenseStatus2` | Integer | The number of stacks of the enhanced sentry/tower defense status. | 2 | `1` |
| [`TriggerWerewolfTransform`](../Reference_and_Meta/Arrays.md#array-triggerwerewolftransform) | Array / Float  | The number of stacks and probability of triggering the werewolf transformation. | 7 | `.5`<br>`[1 .15]`<br>`[1 .20]` |
| `TurnControlDelay` | Float | Specifies the delay in seconds before the unit regains turn control. | 1 | `.25` |
| [`VisualFlySwarm`](./Engine_StatusAndPassiveKeys.md#object-visualflyswarm) | Float / Object  | If non-zero, enables the visual fly swarm effect on the unit. | 3 | `{ . . . }`<br>`1` |

| [`AddDamageToElementDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-adddamagetoelementdamage) | Object  | Defines additional damage of a specific element added to the unit's attacks. | 9 | `{ . . . }` | `AddLeechesStatus` | Integer | The number of stacks of Leech status applied to the source, healing when dealing damage. | 0 | `1` | [`AddStatusesIfPersistentWeatherElement`](Miscellaneous.md#object-addstatusesifpersistentweatherelement) | Object | Specifies statuses applied if the persistent weather matches the given elements. | 0 | `{ . . . }` | [`AddStatusesToReceivedElementalDamage`](Miscellaneous.md#object-addstatusestoreceivedelementaldamage) | Object | An object defining statuses applied to the unit when it takes elemental damage of the specified types. | 0 | `{ . . . }` | [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Contains status effects to add to the basic attack. | 178 | `{ . . . }` | [`AddStatusToElementDamage`](Items_and_Equipment.md#object-addstatustoelementdamage) | Object | An object that applies a specific status effect when dealing damage of a specified element. Contains sub-keys for the element and the status to apply. | 4 | `{ . . . }` | [`AddStatusToTrampleDamage`](Characters_and_Bosses.md#object-addstatustotrampledamage) | Object | An object whose nested keys define statuses applied to trample damage. | 2 | `{ . . . }` | `AddWeaponAux` | Integer / String | The amount or expression to add to the source's weapon auxiliary stat. | 0 | `"-max(min(X+1, item_aux), 0)"`<br>`-item_aux`<br>`1` | `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 0 | `-1`<br>`-2`<br>`1` | `AlphaCat` | Integer | The number of AlphaCat stacks applied to the source on kill. | 2 | `1` | [`ApplyPassives`](Abilities_and_Spells.md#object-applypassives) | Object | Specifies the passives or status effects to apply to the unit. | 0 | `{ . . . }` | `BigSplashDamage` | Integer | The additional tile radius of the splash damage effect applied by an attack. | 0 | `2` | `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` | `Blind` | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | `-1`<br>`1`<br>`2` | [`BloodRain`](Engine_GlobalModifierKeys.md#object-bloodrain) | Integer / Object | If non-zero, enables the blood rain visual effect. | 2 | `{ . . . }`<br>`1` | `BonusCritChance` | Integer | The flat percentage increase to critical hit chance. | 0 | `100`<br>`25`<br>`50` | `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 0 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` | `BonusDamageBasedOnDistance` | Integer | The flat bonus damage added per tile of distance between the source and target. | 0 | `1` | `BonusKnockbackDamage` | Integer | The extra damage dealt per tile of knockback. | 0 | `2`<br>`3`<br>`5` | `BrittleCharismaUp` | Integer | The number of stacks of temporary Charisma gained on kill. | 0 | `2` | `BrittleConstitutionUp` | Integer | The number of stacks of temporary Constitution gained on kill. | 0 | `2` | `BrittleDexterityUp` | Integer | The number of stacks of temporary Dexterity gained on kill. | 0 | `2` | `BrittleIntelligenceUp` | Integer | The number of stacks of temporary Intelligence gained on kill. | 0 | `2` | `BrittleLuckUp` | Integer | The number of stacks of temporary Luck gained on kill. | 0 | `2` | `BrittleSpeedUp` | Integer | The number of stacks of temporary Speed gained on kill. | 0 | `2` | `BrittleStrengthUp` | Integer | The number of stacks of temporary Strength gained on kill. | 0 | `2` | [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` | `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` | `CapDamage` | Integer | The maximum amount of damage dealt, capping the total after all modifiers are applied. | 0 | `1` | `CaptureFamiliar` | Integer | The number of times to attempt to capture the target as a familiar. | 0 | `1` | `ChanceToBreak` | Integer | Specifies the percentage chance that the item breaks on use. | 0 | `100`<br>`15`<br>`20` | [`CharacterTypeGainsStatusAtBattleStart`](Engine_LogicKeys.md#object-charactertypegainsstatusatbattlestart) | Object | Defines status effects applied to characters with a specific tag at the start of a battle. | 1 | `{ . . . }` | `Charge` | Integer | The number of charge stacks applied. | 0 | `1`<br>`2`<br>`3` | `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 0 | `1`<br>`2`<br>`3` | [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 2 | `{ . . . }`<br>`0`<br>`1` | `CompleteItemQuest` | Enum | Specifies the item quest ID to mark as complete on kill. | 0 | `BlackShard`<br>`Nuke`<br>`ScaldingOrb` | [`Conditional_HasStatus`](./Engine_LogicKeys.md#conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 0 | `{ . . . }` | [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `{ . . . }`<br>`1`<br>`10`<br>`2` | `ConjureRandomAbilityFromCat` | Integer | The number of random abilities created or given to the cat unit from a pool of cat-themed abilities. | 0 | `1` | `CrackMoonHead` | Integer | If set, cracks the MoonHead's head, triggering its death sequence. | 0 | `1` | `CurrentWeaponDamageUp` | Integer | The amount of temporary damage increase to the current weapon. | 0 | `1`<br>`3`<br>`5` | `DeleteObject` | Integer | If set, deletes the target object from the map. | 0 | `1` | `DestroyTrinket` | Integer | The number of trinkets destroyed. | 0 | `1` | [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | If set, kills the target immediately. | 0 | `{ . . . }`<br>`1`<br>`6` | `DieViolently` | Integer | If true, causes the target to die with a violent, explosive visual effect. | 0 | `1` | `DisableWeapon` | Integer | If set, disables the source's weapon, preventing its use. | 0 | `1` | `disallow_modifications` | Boolean | If true, the damage instance cannot be modified by external effects (e.g., passives, statuses). | 0 | `true` | `DisplaceToAbilityTarget` | Integer | If set, displaces the source to the ability's target location. | 0 | `1` | `DisplaceTowardsSource` | Integer | If set, displaces the target towards the source of the effect. | 0 | `1` | [`DistanceBonusDamage`](./Engine_StatusAndPassiveKeys.md#object-distancebonusdamage) | Object | An object that adds bonus damage based on the distance from the target, with sub-keys for stacks and minimum range. | 0 | `{ . . . }` | `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 0 | `1`<br>`2`<br>`4` | `DontHealEnemies` | Integer | If true, the healing effect does not affect enemy units. | 0 | `1` | `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 0 | `1`<br>`2`<br>`3` | `EmptyMana` | Integer | If non-zero, sets the unit's mana to empty when applied. | 0 | `1` | `EventBounty` | Integer | The number of stacks of Event Bounty applied, increasing event rewards. | 0 | `5` | `ExplodeCharacter` | Integer | The radius (in tiles) of an explosion centered on the character. | 0 | `5` | `ExplodeCharacter_NoDie` | Integer | The damage dealt when a character explodes without dying. | 0 | `1`<br>`5` | `ExplodeCharacter_Party` | Integer | The radius (in tiles) of an explosion centered on the character that also damages party members. | 0 | `5` | `ExplodeCharacter_PartyBoss` | Integer | The damage dealt to the party boss when it explodes. | 0 | `5` | `ExplodeCharacter_RockCrusher` | Integer | The number of RockCrusher explosion triggers applied to non-boss characters. | 0 | `5`<br>`9` | `ExplodeCharacter_RockCrusher_PetrifyBreak` | Integer | The damage dealt when a petrified RockCrusher explodes. | 0 | `5`<br>`9` | `FaceAway` | Integer | If set, forces the target to face away from the source. | 0 | `1` | `FaceCamera` | Integer | If non-zero, forces the character to rotate and face the camera. | 0 | `1` | `FactionConversion` | Integer | Converts the target to the caster's faction. | 0 | `1` | `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 0 | `1`<br>`10`<br>`2` | `Fights` | Number | The number of fights this status or effect persists for. | 4 | `1`<br>`3`<br>`99` | `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. | 0 | `1`<br>`[1 .10]`<br>`[1 .25]` | `FlatAIBonus` | Integer | A flat adjustment to the AI's evaluation score for this action; positive values encourage the AI to use it, negative values discourage it. | 0 | `-999999`<br>`100`<br>`999999` | `FlatLeech` | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. | 0 | `1`<br>`10`<br>`2` | `FloatingRockTrap` | Integer | The number of stacks of Floating Rock Trap applied to the target, dealing damage when stepped on. | 0 | `1` | `ForceImmediateMove` | Integer | If non-zero, forces the character to move instantly without waiting for normal action order. | 0 | `1` | `ForceMoveAway` | Integer | The distance to force the target away from the source. | 0 | `1` | `ForceMoveTowards` | Integer | The number of tiles to force the target to move toward the caster. | 0 | `1` | `ForceUseAbility_NonStack` | Enum | Forces the unit to use a specific non-stackable ability when the conditional roll is successful. | 0 | `Endeavor_Auto`<br>`Indigestion_Fart`<br>`Indigestion_Fart2` | [`ForceUseAbilityOnTarget`](./Engine_StatusAndPassiveKeys.md#object-forceuseabilityontarget) | Object | Defines a chance to force the unit to use a specified ability on the target. | 0 | `{ . . . }` | `FullHeal` | Integer | If non-zero, fully restores the target's health. | 0 | `0`<br>`1` | `GainDisorder` | Enum | Specifies the name of the disorder gained. | 0 | `Chungus`<br>`Psychosis` | `GainDisorderFromPool_PostCast` | Enum | Specifies the pool of disorders the unit can gain after the spell is cast. | 0 | `forbidden_spell_consequences`<br>`forbidden_spell_consequences_crippling` | `GenericDebuff` | Integer | The number of stacks of a generic, untooltipped debuff applied to the target. | 0 | `1`<br>`10`<br>`100` | `HealRandomInjury` | Integer | The number of random injuries healed on the target. | 0 | `1` | `HealthGain` | Integer | The amount of health restored to the source. | 0 | `1`<br>`10`<br>`2` | `IgnoreDamage` | Integer | If set, the target ignores all damage for the duration. | 0 | `1` | [`ImmediateUseAbility`](./Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object | Specifies the name of an ability to be triggered instantly from this effect. | 0 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` | `ImmediateUseAbility_Instant` | Enum | Specifies the name of an ability to use instantly as a passive effect. | 0 | `head_CrownOfHorns` | `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `0`<br>`1`<br>`10%` | `Imprison` | Enum | Specifies the type of unit or object to summon as a prison. | 0 | `BeefyCharmedLeech`<br>`CharmedLeech`<br>`Fly` | `InnateElement` | Enum | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 8 | `Earth`<br>`Electric`<br>`Fire` | `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 0 | `25`<br>`50`<br>`999` | [`KnockbackIfCrit`](./Engine_StatusAndPassiveKeys.md#object-knockbackifcrit) | Object | Defines knockback properties applied when a critical hit occurs. | 0 | `{ . . . }` | `KnockOutClone` | Enum | Specifies the ability ID used to knock out or remove the player's clone unit from battle. | 0 | `PlayerCat_MiniMiniMe` | `LaunchOffScreen` | Equation | A formula string that determines the knockback force to launch the unit off-screen. | 0 | `10+bonus_melee_ability_damage` | `LaunchOffScreenInstakill` | Integer | If non-zero, the unit is instantly killed and launched off-screen. | 0 | `1` | `LeaveBehindRockOnKnockback` | Integer | If non-zero, leaves behind a rock on each tile the target is knocked through. | 0 | `1` | `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 6 | `1`<br>`2` | `LeechPercent` | Integer | The percentage of damage dealt restored as health. | 0 | `50` | [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 0 | `{ . . . }`<br>`1`<br>`2`<br>`3` | `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. | 0 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` | [`Marked`](./Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 0 | `{ . . . }`<br>`1`<br>`3`<br>`5` | `NonLethal` | Integer | If set to 1, damage dealt by the unit cannot kill enemies; it leaves them at 1 HP. | 0 | `1` | `OverrideDamage` | Integer | Overrides the damage of the current action to this flat value (can be negative to heal). | 0 | `-10`<br>`0`<br>`1` | [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 5118 | `{ . . . }` | `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 0 | `1` | `PermanentDexterity` | Integer | The permanent amount of dexterity added or removed. | 0 | `1`<br>`2` | `PreEmptiveCounterNextAttacks` | Integer | The number of next incoming attacks that the unit will counter preemptively before they land. | 0 | `1` | `PurgeAll` | Integer | If non-zero, removes all temporary status effects (buffs, debuffs) from the target. | 0 | `1` | `RandomBonusDamage` | Integer | The maximum random bonus damage added to the base damage; the actual bonus is a random value between 0 and this number. | 0 | `25` | `RandomStatDown` | Array / Integer / String | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 0 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`1` | `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` | [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 0 | `{ . . . }` | `RefreshActPoints` | Integer | The amount of action points restored to the source. | 0 | `1` | `RefreshMovePoints` | Integer | The amount of movement points restored to the source. | 0 | `1` | `RefreshWeaponAbility` | Integer | The number of times the weapon's ability is refreshed. | 0 | `1` | `RemoteFlatLeech` | Integer | The flat amount of remote leech applied to the target on basic attack. | 0 | `1` | `RemoteLeech` | Integer | The amount of remote leech applied to the target on basic attack. | 0 | `1` | `RemoveAmbientLightEffects` | Float | The fade-out duration in seconds for ambient light effects. | 0 | `.5`<br>`4` | `RemoveGlobalModifiers` | Array | List of global modifier names to remove upon death. | 0 | `[BloodRain]` | `RemoveItem` | Enum | Specifies the item ID to remove from the source on kill. | 0 | `BlackShard`<br>`BlackShard_Glowing`<br>`ScaldingOrb` | `RemoveKnockback` | Integer | The number of knockback stacks removed from the received damage. | 0 | `1` | `RemoveMovePoints` | Integer | The number of move points to remove from the target, preventing them from moving. | 0 | `1` | `RemoveStatus` | Enum | The name of the status effect to remove from the source. | 0 | `AlphaCat`<br>`Brace`<br>`DodgeChance_Status` | [`RemoveStatusStacks`](./Engine_StatusAndPassiveKeys.md#object-removestatusstacks) | Object | An object specifying a status name and the number of stacks to remove from the target. | 0 | `{ . . . }` | `RemoveTurnsThisRound` | Integer | The number of turns to remove from the target's turn order this round. | 0 | `1` | `RepairWeapon` | Array / Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 0 | `1`<br>`6`<br>`99` | [`Revive`](./Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | `{ . . . }`<br>`1`<br>`100%`<br>`50%` | `Rot` | Array / Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 0 | `-999999`<br>`1`<br>`2` | `ScatterRandomPickups` | Integer | The number of random pickups scattered around the target's location. | 0 | `2`<br>`5` | `SetHealth` | Integer | Sets the target's health to a specific flat value or percentage. | 0 | `1`<br>`100%`<br>`50%` | [`SetItemAux`](./Engine_StatusAndPassiveKeys.md#object-setitemaux) | Object | Configures an item's auxiliary value by specifying a target slot and a formula for the new value. | 0 | `{ . . . }` | `SetKnockback` | Integer | The knockback distance to set for the damage instance, overriding default. | 0 | `0` | `SetShield` | Integer | Sets the target's shield value to a specific flat amount. | 0 | `0`<br>`88` | `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` | [`ShowFakeDamage`](Abilities_and_Spells.md#object-showfakedamage) | Object | Displays a fake damage number (with optional style) for visual effect without actually changing health. | 0 | `{ . . . }` | `ShowText` | String | Specifies the localization key for a popup text displayed on the target. | 0 | `"COMBAT_POPUP_BRAINSTORM"`<br>`"COMBAT_POPUP_RELOAD"`<br>`"COMBAT_POPUP_REPAIRED"` | [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `{ . . . }`<br>`-1`<br>`1`<br>`2` | `SpawnBearTrap` | Integer | If non-zero, spawns a bear trap on the tile. | 0 | `1` | `SpawnBearTrapIfHitKills` | Integer | If non-zero, spawns a bear trap at the target's location upon a killing blow. | 0 | `1` | `SpawnBearTrapOnMiss` | Integer | The number of bear traps to spawn on the tile adjacent to the target when the unit misses an attack. | 0 | `1` | `SpawnFlames` | `Array` | An array containing the number of flame tiles to spawn and the chance per tile. | 0 | `[1, .20+.1*level]`<br>`[1, .20]` | `SpawnThingIfHitKills` | Enum | The name of the thing (e.g., a food type) to spawn at the target's location upon a killing blow. | 0 | `Bait`<br>`BigFood`<br>`BiggestFood` | `SpecificInjury` | Enum | The stat (str, spd, int) to which a specific injury is applied, reducing that stat. | 0 | `int`<br>`spd`<br>`str` | `SpeculativeMoveSelfCorpseOffMap` | Integer | If true, attempts to remove the character's corpse from the map, used for speculative AI targeting. | 0 | `1` | `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 0 | `-1`<br>`-2`<br>`-4` | `SpeedUp_WithoutInitiative` | Integer | The number of stacks of Speed Up that do not affect the unit's initiative (turn order) stat. | 0 | `1` | `StackingSandstorm` | Integer | If non-zero, enables the stacking sandstorm mechanic which increases damage per stack. | 0 | `1` | `StanceSwitchToMelee` | Integer | If set, switches the source to melee stance. | 0 | `1` | `StanceSwitchToRanged` | Integer | If set, switches the source to ranged stance. | 0 | `1` | `status` | Enum | Specifies the status effect to apply in a Temporary object. | 0 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` | [`StatusEachRoundEnd`](Cat_Mutations.md#object-statuseachroundend) | Object | An object listing status effects applied to the unit at the end of each round. | 2 | `{ . . . }` | `StatusImmunity` | Array / Enum | A list of status effect names the unit is immune to. | 0 | `Burn`<br>`Poison`<br>`Tarred` | [`StatusRandomEnemiesOnBattleStart`](Events_and_Encounters.md#object-statusrandomenemiesonbattlestart) | Object | An object that applies a status effect to a random number of enemies at the start of battle, with sub-keys for count and the status. | 0 | `{ . . . }` | `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 0 | `"max(int, 0)"`<br>`-1`<br>`-2` | `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 0 | `1`<br>`2`<br>`3` | `T2CopyCat` | Integer | The number of T2 Clone copies created or applied to the target cat. | 0 | `1` | `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 0 | `1` | `TempDexterityUp` | Enum | The number of temporary dexterity stacks applied, or a string alias like 'X'. | 0 | `2`<br>`X` | `TempLuckUp` | Integer | The amount of temporary luck increase. | 0 | `2`<br>`99` | [`Temporary`](./Engine_StatusAndPassiveKeys.md#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 0 | `{ . . . }` | [`TempPassiveUntilSettled`](./Engine_StatusAndPassiveKeys.md#object-temppassiveuntilsettled) | Object | An object containing a temporary passive that is applied until the character's position is settled. | 0 | `{ . . . }` | [`TempPassiveWhileHasStatus`](Abilities_and_Spells.md#object-temppassivewhilehasstatus) | Object | An object defining passives temporarily granted to the unit while it has a specific status effect. | 0 | `{ . . . }` | `TempStrengthUp` | Equation | The number of stacks of temporary Strength Up applied to the unit. | 0 | `1`<br>`2`<br>`X` | `TempTrampleUntilSettled` | Integer | The number of stacks of temporary Trample applied to the source, allowing movement through enemies until the source ends its turn. | 0 | `3` | `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 14 | `1`<br>`3`<br>`4` | `UseAbility_Madness` | Enum | Determines which ability type (e.g., weapon) is forcibly used when Madness triggers. | 0 | `weapon` | `UseAbility_NonStack` | Enum | Specifies an ability to use on kill that does not stack with itself. | 0 | `BBTransformZealot`<br>`GenericRage` | `Vaporize` | Integer | Removes the target from play, preventing its corpse from being interacted with. | 0 | `1`<br>`20` | `VaporizeCorpse` | Integer | If set, vaporizes the target's corpse, preventing revival. | 0 | `1` | `VaporizeCorpseFlipAdvantage` | `Array` | The number of stacks and probability of vaporizing a corpse to gain loot flip advantage. | 0 | `[1 .33]` | `VaporizeInanimate` | Integer | If non-zero, instantly destroys inanimate objects (corpses, rocks) as if they were vaporized. | 0 | `1` | `VisualFX` | Enum | Specifies the name of the visual effect to play. | 0 | `BigMagicMissileBlast`<br>`Bolt`<br>`Cleanse` | [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `{ . . . }`<br>`1`<br>`2`<br>`3` | `WeaponAuxMultiplier` | Number | A multiplier string (e.g., '.5') for the weapon's auxiliary counter on kill. | 0 | `.5`

</details>

### Valid Nested Objects

The following objects all behave as `{Status and Passive Keys}` containers. Each has its own unique parameters listed below its entry.


---


#### `AddPassivesToCharmed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 113 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |

</details>


---


#### `AddPassivesToMinions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 36

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 109 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |
| [`Quivered`](../Reference_and_Meta/Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 36 | `1`<br>`2`<br>`5` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 113 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `PoisonThorns` | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 15 | `1`<br>`2`<br>`3` |
| [`tag_filter`](../Reference_and_Meta/Enums.md#enum-tag_filter) | Enum | Specifies a tag (e.g., 'crow', 'rock', 'grub_familiar') used to filter which units a status or effect applies to. | 4 | `crow`<br>`grub_familiar`<br>`rock` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |
| [`Buddy`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-buddy) | Enum / Object  | Specifies a buddy unit that accompanies or is spawned alongside the unit, with optional reclaim and targeting properties. | 24 | `{ . . . }`<br>`BoyDino`<br>`CaveCatDad`<br>`Chubs` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 50 | `1`<br>`2`<br>`4` |
| [`ForceAttack`](./Engine_StatusAndPassiveKeys.md#object-forceattack) | Integer / Object  | If set to 1, forces the target to perform an attack against a random or specified target. | 11 | `{ . . . }`<br>`1` |
| `HealthGain` | Integer | The amount of health restored to the source. | 63 | `1`<br>`10`<br>`2` |

</details>


---


#### `AddSelfStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 109 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Quivered`](../Reference_and_Meta/Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 36 | `1`<br>`2`<br>`5` |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| [`ForceUseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 33 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`RandomMagicMissile`](./Engine_StatusAndPassiveKeys.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. | 41 | `{ . . . }`<br>`1`<br>`10`<br>`2` |

</details>


---


#### `AddSelfStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RepairWeapon`](../Reference_and_Meta/Arrays.md#array-repairweapon) | Array / Integer  | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 7 | `1`<br>`6`<br>`99` |
| `ChanceToBreak` | Integer | Specifies the percentage chance that the item breaks on use. | 11 | `100`<br>`15`<br>`20` |
| [`RepairWeapon`](../Reference_and_Meta/Arrays.md#array-repairweapon) | Array / Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 7 | `1`<br>`6`<br>`99` |

</details>


---


#### `AddStatusToAllDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Blind`](../Reference_and_Meta/Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 43 | `-1`<br>`1`<br>`2` |
| [`Blind`](../Reference_and_Meta/Arrays.md#array-blind) | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 43 | `-1`<br>`1`<br>`2` |
| [`Conditional_HasStatus`](./Engine_StatusAndPassiveKeys.md#object-conditional_hasstatus) | Object  | Contains an inner effect block that only executes if the target has the specified status effect. | 20 | `{ . . . }` |
| [`Conditional_HasTag`](./Engine_StatusAndPassiveKeys.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 47 | `{ . . . }` |
| `must_do_damage` | Boolean | If true, the status or effect will only be applied if the attack or ability actually deals damage. | 3 | `true` |
| [`Rot`](../Reference_and_Meta/Arrays.md#array-rot) | Array / Integer  | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 20 | `-999999`<br>`1`<br>`2` |
| [`KnockbackIfCrit`](./Engine_StatusAndPassiveKeys.md#object-knockbackifcrit) | Object  | Defines knockback properties applied when a critical hit occurs. | 1 | `{ . . . }` |
| `LeaveBehindRockOnKnockback` | Integer | If non-zero, leaves behind a rock on each tile the target is knocked through. | 4 | `1` |
| `NonLethal` | Integer | If set to 1, damage dealt by the unit cannot kill enemies; it leaves them at 1 HP. | 1 | `1` |
| [`Rot`](../Reference_and_Meta/Arrays.md#array-rot) | Array / Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 20 | `-999999`<br>`1`<br>`2` |
| `BonusKnockbackDamage` | Integer | The extra damage dealt per tile of knockback. | 4 | `2`<br>`3`<br>`5` |

</details>


---


#### `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 248

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| [`Bruise`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 133 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 203 | `1`<br>`10`<br>`2` |
| [`Blind`](../Reference_and_Meta/Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 43 | `-1`<br>`1`<br>`2` |
| [`Confusion`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 86 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 113 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 39 | `1`<br>`2` |
| [`Conditional_Ally`](./Engine_StatusAndPassiveKeys.md#object-conditional_ally) | Object  | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 37 | `{ . . . }` |
| [`Immobile`](../Reference_and_Meta/Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 47 | `0`<br>`1`<br>`10%` |
| [`Slow`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 75 | `{ . . . }`<br>`-1`<br>`1`<br>`2` |
| [`Weakness`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-weakness) | Array / Integer / Object  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 59 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Conditional_Enemy`](./Engine_StatusAndPassiveKeys.md#object-conditional_enemy) | Object  | An object containing status effects or actions applied only if the target is an enemy. | 44 | `{ . . . }` |
| [`Conditional_GoodRoll`](./Engine_StatusAndPassiveKeys.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 37 | `{ . . . }` |
| [`Conditional_Adjacent`](./Engine_StatusAndPassiveKeys.md#object-conditional_adjacent) | Object  | An object whose nested keys define statuses or effects applied to or by units that are adjacent to the unit. | 4 | `{ . . . }` |
| [`Conditional_Shielded`](./Engine_StatusAndPassiveKeys.md#object-conditional_shielded) | Object  | An object containing effects that are only applied if the target has a shield active. | 5 | `{ . . . }` |
| [`Leeches`](./Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object  | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 25 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`MagicWeakness`](../Reference_and_Meta/Arrays.md#array-magicweakness) | Array / Integer  | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 21 | `1`<br>`2`<br>`3` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 52 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`SoulLink`](./Engine_StatusAndPassiveKeys.md#object-soullink) | Integer / Object  | The number of soul link stacks applied. | 15 | `{ . . . }`<br>`1` |
| [`Conditional_HasTag`](./Engine_StatusAndPassiveKeys.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 47 | `{ . . . }` |
| [`Conditional_SourceHasTag`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-conditional_sourcehastag) | Object  | Defines a conditional block that applies effects only if the source of the effect has a specified tag. | 1 | `{ . . . }` |
| [`Burn`](../Reference_and_Meta/Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 154 | `1`<br>`10`<br>`2` |
| [`Else`](./Engine_StatusAndPassiveKeys.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 86 | `{ . . . }` |
| [`ApplyToSource`](./Engine_StatusAndPassiveKeys.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 59 | `{ . . . }` |
| [`BounceObject`](./Engine_StatusAndPassiveKeys.md#object-bounceobject) | Enum / Object  | Specifies the object or projectile to spawn and bounce from the target. | 39 | `{ . . . }`<br>`AllyRotFly`<br>`Amoeba`<br>`BeefyCharmedLeech` |
| [`BurgleCoin`](../Reference_and_Meta/Arrays.md#array-burglecoin) | Array / Integer  | The number of coins stolen from the target, or an array of `[number, probability]`. | 6 | `1`<br>`3`<br>`[1 .5]` |
| [`ChangeTile`](./Engine_StatusAndPassiveKeys.md#object-changetile) | Enum / Object  | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 74 | `{ . . . }`<br>`BlankTile`<br>`BrambleTile`<br>`CreepTile` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 47 | `1`<br>`2`<br>`3` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 108 | `1`<br>`10`<br>`2` |
| `FlatLeech` | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. | 9 | `1`<br>`10`<br>`2` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 51 | `1`<br>`2`<br>`[1 .01]` |
| [`GainDisorderFromPool`](./Engine_StatusAndPassiveKeys.md#object-gaindisorderfrompool) | Enum / Object  | Specifies a pool of disorders from which one is randomly gained on basic attack, with an optional chance. | 3 | `{ . . . }`<br>`all_disorders` |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 12 | `25`<br>`50`<br>`999` |
| `Knockback` | Equation | The number of tiles the target is pushed away from the source on hit. | 33 | `1`<br>`10`<br>`2` |
| [`KnockOutCoin`](./Engine_StatusAndPassiveKeys.md#object-knockoutcoin) | Integer / Object  | The number of coins knocked out, with an optional probability or an object with stacks and chance. | 5 | `{ . . . }`<br>`1`<br>`[1 .5]` |
| [`KnockUpAndAway`](./Engine_StatusAndPassiveKeys.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 25 | `{ . . . }` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 51 | `-1`<br>`-2`<br>`-4` |
| [`Madness`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 45 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `ManaLeeches` | Integer | The number of mana leech stacks applied. | 5 | `1`<br>`2` |
| [`Marked`](./Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 27 | `{ . . . }`<br>`1`<br>`3`<br>`5` |
| `OverrideChainKnockback` | Integer | The custom number of tiles for chain knockback, overriding the default. | 11 | `0`<br>`1`<br>`10` |
| `OverrideChainKnockbackDamage` | String | A formula string that overrides the damage dealt by chain knockback (e.g., "3+bonus_melee_ability_damage"). | 2 | `0`<br>`3+bonus_melee_ability_damage` |
| [`Petrify`](../Reference_and_Meta/Arrays.md#array-petrify) | Array / Integer  | The amount of petrify stacks applied, or an [stacks, probability] array. | 35 | `1`<br>`[1 .15]`<br>`[1 .1]` |
| `Possessed` | Integer | The number of possession stacks applied, or a template with name and tooltips. | 4 | `1` |
| `PullSourceToTarget` | Integer | The amount of tiles the source is pulled towards the target after the attack. | 4 | `1` |
| [`Rot`](../Reference_and_Meta/Arrays.md#array-rot) | Array / Integer  | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 20 | `-999999`<br>`1`<br>`2` |
| `SpiderInfested` | Integer | The number of spider infestation stacks applied. | 10 | `1`<br>`2`<br>`4` |
| `SplashDamage` | Integer | The radius (in tiles) for splash damage applied to adjacent targets. | 2 | `1`<br>`2` |
| [`SpreadDisease`](./Engine_StatusAndPassiveKeys.md#object-spreaddisease) | Object  | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 13 | `{ . . . }` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 138 | `1`<br>`2`<br>`3` |
| [`Tangled`](./Engine_StatusAndPassiveKeys.md#object-tangled) | Array / Integer / Object  | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 10 | `{ . . . }`<br>`1`<br>`2`<br>`[1, .05]` |
| [`VisualFXTile`](../Reference_and_Meta/Enums.md#enum-visualfxtile) | Enum  | Specifies the name of the visual effect to play on the target tile. | 39 | `Bolt`<br>`BurnTrigger`<br>`Explosion` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 19 | `1`<br>`2`<br>`[1 .1]` |

</details>


---


#### `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| [`Bruise`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 133 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Confusion`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 86 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Immobile`](../Reference_and_Meta/Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 47 | `0`<br>`1`<br>`10%` |
| `Knockback` | Equation | The number of tiles the target is pushed away from the source on hit. | 33 | `1`<br>`10`<br>`2` |
| [`KnockUpAndAway`](./Engine_StatusAndPassiveKeys.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 25 | `{ . . . }` |
| [`SpreadDisease`](./Engine_StatusAndPassiveKeys.md#object-spreaddisease) | Object  | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 13 | `{ . . . }` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 138 | `1`<br>`2`<br>`3` |

</details>


---


#### `AddStatusToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddDamageToElementDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-adddamagetoelementdamage) | Object  | Defines additional damage of a specific element added to the unit's attacks. | 9 | `{ . . . }` |
| [`Conditional_Corpse`](./Engine_StatusAndPassiveKeys.md#object-conditional_corpse) | Object  | Contains an inner effect block that only executes if the target is a corpse. | 11 | `{ . . . }` |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 80 | `Electric`<br>`Fire`<br>`Gravity` |
| [`Burn`](../Reference_and_Meta/Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 154 | `1`<br>`10`<br>`2` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 138 | `1`<br>`2`<br>`3` |

</details>


---


#### `AddStatusToKnockbackDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bruise`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 133 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Bruise`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 133 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 138 | `1`<br>`2`<br>`3` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 138 | `1`<br>`2`<br>`3` |

</details>


---


#### `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 39 | `1`<br>`2` |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 39 | `1`<br>`2` |
| [`Conditional_Enemy`](./Engine_StatusAndPassiveKeys.md#object-conditional_enemy) | Object  | An object containing status effects or actions applied only if the target is an enemy. | 44 | `{ . . . }` |
| `LeechPercent` | Integer | The percentage of damage dealt restored as health. | 2 | `50` |

</details>


---


#### `AddStatusToTrampleDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bruise`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 133 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Bruise`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 133 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Cleave`](./Engine_StatusAndPassiveKeys.md#object-cleave) | Integer / Object  | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 19 | `{ . . . }`<br>`1` |
| [`Cleave`](./Engine_StatusAndPassiveKeys.md#object-cleave) | Integer / Object  | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 19 | `{ . . . }`<br>`1` |

</details>


---


#### `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 39 | `1`<br>`2` |
| [`Cleave`](./Engine_StatusAndPassiveKeys.md#object-cleave) | Integer / Object  | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 19 | `{ . . . }`<br>`1` |
| `PullSourceToKnockbackImmuneTarget` | Integer | The amount of pull force applied to the source toward a knockback-immune target. | 4 | `1` |

</details>


---


#### `AdventureTokenPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


#### `ApplyPassives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `YOffset` | Float | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 11 | `-.18`<br>`.25`<br>`.35` |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 18 | `1` |

</details>


---


#### `ApplyStatusIfCrit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| [`Purge`](./Engine_StatusAndPassiveKeys.md#object-purge) | Integer / Object  | The number of status effects to purge from the target. | 10 | `{ . . . }`<br>`0`<br>`3` |
| [`ApplyToSource`](./Engine_StatusAndPassiveKeys.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 59 | `{ . . . }` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 51 | `-1`<br>`-2`<br>`-4` |

</details>


---


#### `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 99 | `0`<br>`1`<br>`10` |
| `Bounty` | Integer | The number of bounty stacks applied to enemies, increasing rewards on defeat. | 5 | `1`<br>`3` |
| [`Marked`](./Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 27 | `{ . . . }`<br>`1`<br>`3`<br>`5` |

</details>


---


#### `CatchProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 4710 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 5455 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`Quivered`](../Reference_and_Meta/Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 36 | `1`<br>`2`<br>`5` |
| `ally_chance` | Integer | The percentage chance for an ally to catch incoming projectiles. | 5 | `100%`<br>`15%` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 101 | `.02`<br>`.1`<br>`.15` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |

</details>


---


#### `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 990 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`Stealth`](../Reference_and_Meta/Arrays.md#array-stealth) | Array / Integer  | The number of stealth stacks applied. | 11 | `1`<br>`2`<br>`[1 .1]` |
| `Conditional_Flying` | Object | Defines a conditional block that applies effects or actions only to flying units. | 1 | `{ . . . }` |
| [`Else`](./Engine_StatusAndPassiveKeys.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 86 | `{ . . . }` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 108 | `1`<br>`10`<br>`2` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 138 | `1`<br>`2`<br>`3` |

</details>


---


#### `CritsApplyStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| [`Bruise`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 133 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Confusion`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 86 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Immobile`](../Reference_and_Meta/Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 47 | `0`<br>`1`<br>`10%` |
| [`Weakness`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-weakness) | Array / Integer / Object  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 59 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Conditional_HasStatus`](./Engine_StatusAndPassiveKeys.md#object-conditional_hasstatus) | Object  | Contains an inner effect block that only executes if the target has the specified status effect. | 20 | `{ . . . }` |
| [`Else`](./Engine_StatusAndPassiveKeys.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 86 | `{ . . . }` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 108 | `1`<br>`10`<br>`2` |
| [`ObjectOnHitCharacter`](./Engine_StatusAndPassiveKeys.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 31 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 138 | `1`<br>`2`<br>`3` |

</details>


---


#### `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_PartyMember`](./Engine_StatusAndPassiveKeys.md#object-conditional_partymember) | Object  | A conditional block that executes its child actions only if the target is a party member. | 6 | `{ . . . }` |
| [`Conditional_Ally`](./Engine_StatusAndPassiveKeys.md#object-conditional_ally) | Object  | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 37 | `{ . . . }` |

</details>


---


#### `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 73

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2166 | `{ . . . }` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 836 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`knockback`](../Reference_and_Meta/Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 314 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 203 | `1`<br>`10`<br>`2` |
| [`InnateElement`](../Reference_and_Meta/Enums.md#enum-innateelement) | Enum | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 18 | `Earth`<br>`Electric`<br>`Fire` |
| [`AddDamageToElementDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-adddamagetoelementdamage) | Object  | Defines additional damage of a specific element added to the unit's attacks. | 9 | `{ . . . }` |
| [`Immobile`](../Reference_and_Meta/Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 47 | `0`<br>`1`<br>`10%` |
| [`Weakness`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-weakness) | Array / Integer / Object  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 59 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`AddStatusToElementDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustoelementdamage) | Object  | An object that applies a specific status effect when dealing damage of a specified element. Contains sub-keys for the element and the status to apply. | 6 | `{ . . . }` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 1684 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `cant_miss` | Boolean | If true, the damage instance always hits its target regardless of accuracy or evasion. | 131 | `true` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 51 | `1`<br>`2`<br>`[1 .01]` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 414 | `[`<br>`[Heat Fire]` |
| [`SpreadDisease`](./Engine_StatusAndPassiveKeys.md#object-spreaddisease) | Object  | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 13 | `{ . . . }` |
| [`StatusImmunity`](../Reference_and_Meta/Arrays.md#array-statusimmunity) | Array / Enum  | A list of status effect names the unit is immune to. | 38 | `Burn`<br>`Poison`<br>`Tarred` |

</details>


---


#### `PassiveAfterXKills`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2807 | `{ . . . }` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 234 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


#### `PassiveAtHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2807 | `{ . . . }` |
| [`mode`](../Reference_and_Meta/Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 29 | `equal`<br>`greater`<br>`greater_or_equal` |
| [`threshold`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 49 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |

</details>


---


#### `PassiveAtStatThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2807 | `{ . . . }` |
| [`mode`](../Reference_and_Meta/Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 29 | `equal`<br>`greater`<br>`greater_or_equal` |
| [`threshold`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 49 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |

</details>


---


#### `PassiveGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |
| [`CatPartsTransform`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 55 | `{ . . . }` |
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. | 16 | `-1`<br>`-2`<br>`1` |
| [`FormChange`](./Engine_StatusAndPassiveKeys.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 140 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 45 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 91 | `-1`<br>`-2`<br>`-4` |

</details>


---


#### `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2807 | `{ . . . }` |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 80 | `Electric`<br>`Fire`<br>`Gravity` |

</details>


---


#### `PassiveWhenAtFullMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 169 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 113 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 18 | `1` |

</details>


---


#### `PassiveWhenDead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`StatusEachTurnBegin`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnbegin) | Object  | Specifies status effects applied to the unit at the start of each of its turns. | 27 | `{ . . . }` |
| [`AutocastEachRound`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-autocasteachround) | Enum / Object  | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 10 | `{ . . . }`<br>`SpiderReturn` |
| [`AutocastEachRound`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-autocasteachround) | Enum / Object  | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 10 | `{ . . . }`<br>`SpiderReturn` |
| [`StatusEachRoundEnd`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachroundend) | Object  | An object listing status effects applied to the unit at the end of each round. | 3 | `{ . . . }` |
| [`AddStatusToTrampleDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustotrampledamage) | Object  | An object whose nested keys define statuses applied to trample damage. | 3 | `{ . . . }` |

</details>


---


#### `PassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2807 | `{ . . . }` |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 160 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |

</details>


---


#### `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |
| [`Brace`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 169 | `{ . . . }`<br>`1`<br>`10`<br>`2` |

</details>


---


#### `RandomPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TransformInXTurns`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-transforminxturns) | Object  | Defines a delayed transformation after a set number of turns, with optional target object and initiative handling. | 11 | `{ . . . }` |

</details>


---


#### `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 109 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 50 | `1`<br>`10`<br>`100` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 130 | `1`<br>`2`<br>`3` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |
| [`Brace`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 169 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Quivered`](../Reference_and_Meta/Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 36 | `1`<br>`2`<br>`5` |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 23 | `1`<br>`2`<br>`3` |
| [`Bruise`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 133 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 203 | `1`<br>`10`<br>`2` |
| [`Blind`](../Reference_and_Meta/Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 43 | `-1`<br>`1`<br>`2` |
| [`Confusion`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 86 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 113 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 41 | `1`<br>`2`<br>`3` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 22 | `1`<br>`2`<br>`[1, 0.1]` |
| [`Immobile`](../Reference_and_Meta/Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 47 | `0`<br>`1`<br>`10%` |
| [`Slow`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 75 | `{ . . . }`<br>`-1`<br>`1`<br>`2` |
| [`Weakness`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-weakness) | Array / Integer / Object  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 59 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`BackflipWhenTargeted`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-backflipwhentargeted) | Enum / Integer / Object  | The number of backflip charges, or an object defining its ability. | 15 | `{ . . . }`<br>`1`<br>`2`<br>`X` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 26 | `1`<br>`10`<br>`100` |
| [`MagicWeakness`](../Reference_and_Meta/Arrays.md#array-magicweakness) | Array / Integer  | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 21 | `1`<br>`2`<br>`3` |
| [`PoisonLace`](./Engine_StatusAndPassiveKeys.md#object-poisonlace) | Integer / Object / String  | Integer or fractional string (e.g., 'X/3') specifying the duration or intensity of the PoisonLace effect. | 10 | `{ . . . }`<br>`"X/3"`<br>`"X/5"`<br>`1` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 52 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Reflect`](./Engine_StatusAndPassiveKeys.md#object-reflect) | Integer / Object  | The amount of reflect stacks applied. | 11 | `{ . . . }`<br>`1`<br>`5` |
| [`Burn`](../Reference_and_Meta/Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 154 | `1`<br>`10`<br>`2` |
| [`Infested`](./Engine_StatusAndPassiveKeys.md#object-infested) | Integer / Object  | The number of stacks of Infested applied. | 15 | `{ . . . }`<br>`1` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 29 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. | 16 | `-1`<br>`-2`<br>`1` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 47 | `1`<br>`2`<br>`3` |
| [`ConstitutionUp`](../Reference_and_Meta/Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 46 | `-1`<br>`-2`<br>`1` |
| `DelayedPain` | Integer | The number of stacks of DelayedPain applied, dealing damage after a delay. | 3 | `1` |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 25 | `-1`<br>`1`<br>`2` |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. | 12 | `1`<br>`2`<br>`3` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 50 | `1`<br>`2`<br>`4` |
| `Drowsy` | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. | 12 | `1`<br>`8` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 108 | `1`<br>`10`<br>`2` |
| [`FormChange`](./Engine_StatusAndPassiveKeys.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 140 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 51 | `1`<br>`2`<br>`[1 .01]` |
| [`GainCoins`](../Reference_and_Meta/Arrays.md#array-gaincoins) | Array / Integer  | The amount of coins gained, or a [min, max] range. | 10 | `-5`<br>`1`<br>`2` |
| `Hex` | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. | 6 | `1` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 45 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `Lifesteal` | Integer | The amount of lifesteal stacks applied. | 6 | `1`<br>`3` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 51 | `-1`<br>`-2`<br>`-4` |
| [`Madness`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 45 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 40 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Marked`](./Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 27 | `{ . . . }`<br>`1`<br>`3`<br>`5` |
| [`ObjectOnHitCharacter`](./Engine_StatusAndPassiveKeys.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 31 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `Ostracized` | Integer | The number of stacks of Ostracized applied. | 4 | `1`<br>`2`<br>`4` |
| `PermanentCharisma` | Integer | The amount of permanent Charisma added to the unit's base stats. | 3 | `1`<br>`2` |
| `PermanentLuck` | Integer | The amount of permanent Luck added to the unit's base stats. | 3 | `1`<br>`2` |
| `PermanentStrength` | Integer | The amount of permanent bonus strength (physical damage modifier) granted. | 5 | `1`<br>`2` |
| [`Petrify`](../Reference_and_Meta/Arrays.md#array-petrify) | Array / Integer  | The amount of petrify stacks applied, or an [stacks, probability] array. | 35 | `1`<br>`[1 .15]`<br>`[1 .1]` |
| [`RandomStatDown`](../Reference_and_Meta/Arrays.md#array-randomstatdown) | Array / Integer / String  | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 12 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`1` |
| [`Rot`](../Reference_and_Meta/Arrays.md#array-rot) | Array / Integer  | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 20 | `-999999`<br>`1`<br>`2` |
| `Scrambled` | Integer | The number of stacks of Scrambled applied. | 3 | `1`<br>`2` |
| [`Sleep`](../Reference_and_Meta/Arrays.md#array-sleep) | Array / Integer  | The amount of sleep stacks applied, or an [stacks, probability] array. | 35 | `1`<br>`2`<br>`3` |
| [`SpawnCoinAnywhere`](../Reference_and_Meta/Arrays.md#array-spawncoinanywhere) | Array / Integer  | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 7 | `1`<br>`[1 .5]` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 91 | `-1`<br>`-2`<br>`-4` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 24 | `1`<br>`3` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 71 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 138 | `1`<br>`2`<br>`3` |
| [`Tarred`](../Reference_and_Meta/Arrays.md#array-tarred) | Array / Integer  | The amount of tarred stacks applied, or an [stacks, probability] array. | 17 | `1`<br>`2`<br>`[1 .1]` |
| `TempCounterAttack` | Integer | The number of turns TempCounterAttack lasts, ticking down at the start of the unit's turn. | 4 | `1` |

</details>


---


#### `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 31

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2166 | `{ . . . }` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 836 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`knockback`](../Reference_and_Meta/Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 314 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 1684 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 414 | `[`<br>`[Heat Fire]` |

</details>


---


#### `StatusAfterCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. | 12 | `-1`<br>`1`<br>`2` |
| `TempRangeUp` | Integer | The amount of temporary range increase applied. | 9 | `1`<br>`2`<br>`20` |
| `TempSpellDamageUp` | Integer | The amount of temporary spell damage increase applied. | 5 | `1` |
| [`UseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. | 14 | `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |

</details>


---


#### `StatusAfterXTurns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 234 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`ForceUseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 33 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |

</details>


---


#### `StatusAllCharactersOnSpawn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 203 | `1`<br>`10`<br>`2` |
| [`Conditional_Boss`](./Engine_StatusAndPassiveKeys.md#object-conditional_boss) | Object  | Contains effects that apply only if the target is a boss enemy. | 21 | `{ . . . }` |
| [`Conditional_PartyMember`](./Engine_StatusAndPassiveKeys.md#object-conditional_partymember) | Object  | A conditional block that executes its child actions only if the target is a party member. | 6 | `{ . . . }` |
| `Conditional_Tiny` | Object | Defines a conditional block that applies effects only to tiny-sized units. | 1 | `{ . . . }` |
| [`Else`](./Engine_StatusAndPassiveKeys.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 86 | `{ . . . }` |

</details>


---


#### `StatusAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 52 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 52 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Conditional_Adjacent`](./Engine_StatusAndPassiveKeys.md#object-conditional_adjacent) | Object  | An object whose nested keys define statuses or effects applied to or by units that are adjacent to the unit. | 4 | `{ . . . }` |
| `exclude_self` | Boolean | If true, the effect does not apply to the source unit itself. | 3 | `false` |

</details>


---


#### `StatusAlliesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 109 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Brace`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 169 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 113 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`ConstitutionUp`](../Reference_and_Meta/Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 46 | `-1`<br>`-2`<br>`1` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 45 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 51 | `-1`<br>`-2`<br>`-4` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 91 | `-1`<br>`-2`<br>`-4` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 71 | `"max(int, 0)"`<br>`-1`<br>`-2` |

</details>


---


#### `StatusAlliesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Reanimate`](./Engine_StatusAndPassiveKeys.md#object-reanimate) | Integer / Object  | The percentage chance to reanimate the target. | 12 | `{ . . . }`<br>`100%`<br>`33%`<br>`50%` |
| `triggers_limit` | Integer | The maximum number of times this passive effect can trigger per battle. | 2 | `1` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 50 | `1`<br>`2`<br>`4` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 51 | `1`<br>`2`<br>`[1 .01]` |

</details>


---


#### `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DoDamage`](./Engine_StatusAndPassiveKeys.md#object-dodamage) | Object  | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 7 | `{ . . . }` |
| [`UseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. | 14 | `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |

</details>


---


#### `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 27

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 24 | `10`<br>`15`<br>`20` |
| [`Quivered`](../Reference_and_Meta/Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 36 | `1`<br>`2`<br>`5` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 22 | `1`<br>`2`<br>`[1, 0.1]` |
| [`Conditional_BadRoll`](./Engine_StatusAndPassiveKeys.md#object-conditional_badroll) | Object  | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 8 | `{ . . . }` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 52 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Revive`](./Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object  | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 21 | `{ . . . }`<br>`1`<br>`100%`<br>`50%` |
| [`Conditional_GoodRoll`](./Engine_StatusAndPassiveKeys.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 37 | `{ . . . }` |
| [`Burn`](../Reference_and_Meta/Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 154 | `1`<br>`10`<br>`2` |
| `BlessingOfPeace` | Integer | The number of stacks of the Blessing of Peace status applied to the unit each turn. | 2 | `1` |
| `DoubleCastSpellThisTurn` | Integer | If non-zero, grants the unit a double cast effect for spells this turn. | 3 | `1` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 108 | `1`<br>`10`<br>`2` |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. | 11 | `1`<br>`[1 .10]`<br>`[1 .25]` |
| [`ForceUseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 33 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 45 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 91 | `-1`<br>`-2`<br>`-4` |
| [`UseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. | 14 | `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| `Wet` | Integer | The number of stacks of the Wet status effect applied. | 2 | `1` |

</details>


---


#### `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 57

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 109 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 41 | `1`<br>`2`<br>`3` |
| [`Conditional_GoodRoll`](./Engine_StatusAndPassiveKeys.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 37 | `{ . . . }` |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 71 | `{ . . . }`<br>`0`<br>`1` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 52 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Stealth`](../Reference_and_Meta/Arrays.md#array-stealth) | Array / Integer  | The number of stealth stacks applied. | 11 | `1`<br>`2`<br>`[1 .1]` |
| [`Conditional_BadRoll`](./Engine_StatusAndPassiveKeys.md#object-conditional_badroll) | Object  | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 8 | `{ . . . }` |
| [`Conditional_HasCleansableDebuffs`](./Engine_StatusAndPassiveKeys.md#object-conditional_hascleansabledebuffs) | Object  | An object containing effects that execute only if the unit has cleansable debuffs. | 2 | `{ . . . }` |
| [`Conditional_ManaThreshold`](./Engine_StatusAndPassiveKeys.md#object-conditional_manathreshold) | Object  | Defines a conditional block that applies effects only if a unit's mana meets a specified threshold. | 1 | `{ . . . }` |
| [`Burn`](../Reference_and_Meta/Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 154 | `1`<br>`10`<br>`2` |
| `AddWeaponAux` | Equation | The amount or expression to add to the source's weapon auxiliary stat. | 5 | `"-max(min(X+1, item_aux), 0)"`<br>`-item_aux`<br>`1` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |
| [`ConstitutionUp`](../Reference_and_Meta/Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 46 | `-1`<br>`-2`<br>`1` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 50 | `1`<br>`2`<br>`4` |
| [`ForceUseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 33 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `HealthGain` | Integer | The amount of health restored to the source. | 63 | `1`<br>`10`<br>`2` |
| [`ImmediateUseAbility`](./Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 11 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 45 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `NonStackingDivineShield` | Integer | The number of Divine Shield stacks that do not stack with duplicates. | 10 | `1` |
| [`ObjectOnHitCharacter`](./Engine_StatusAndPassiveKeys.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 31 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. | 16 | `1` |
| `PreEmptiveCounterNextAttacks` | Integer | The number of next incoming attacks that the unit will counter preemptively before they land. | 2 | `1` |
| [`RandomStatDown`](../Reference_and_Meta/Arrays.md#array-randomstatdown) | Array / Integer / String  | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 12 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`1` |
| `RangeUp` | Integer | The number of stacks of bonus attack range applied. | 6 | `1` |
| [`SpawnCoinAnywhere`](../Reference_and_Meta/Arrays.md#array-spawncoinanywhere) | Array / Integer  | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 7 | `1`<br>`[1 .5]` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 91 | `-1`<br>`-2`<br>`-4` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 71 | `"max(int, 0)"`<br>`-1`<br>`-2` |

</details>


---


#### `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 33 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`RandomMagicMissile`](./Engine_StatusAndPassiveKeys.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. | 41 | `{ . . . }`<br>`1`<br>`10`<br>`2` |

</details>


---


#### `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 234 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 45 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`ObjectOnHitCharacter`](./Engine_StatusAndPassiveKeys.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 31 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`RandomMagicMissile`](./Engine_StatusAndPassiveKeys.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. | 41 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `ReduceManaCost` | Integer | The number of stacks reducing mana cost of abilities. | 5 | `1`<br>`2` |
| [`RepairWeapon`](../Reference_and_Meta/Arrays.md#array-repairweapon) | Array / Integer  | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 7 | `1`<br>`6`<br>`99` |
| `RepairWeaponCondition` | Integer | The amount of weapon condition restored. | 3 | `1` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 24 | `1`<br>`3` |

</details>


---


#### `StatusGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 25 | `-1`<br>`1`<br>`2` |
| [`FindItemFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 43 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 51 | `1`<br>`2`<br>`[1 .01]` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 51 | `-1`<br>`-2`<br>`-4` |
| [`SpawnCoinAnywhere`](../Reference_and_Meta/Arrays.md#array-spawncoinanywhere) | Array / Integer  | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 7 | `1`<br>`[1 .5]` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 91 | `-1`<br>`-2`<br>`-4` |

</details>


---


#### `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 109 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Brace`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 169 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 22 | `1`<br>`2`<br>`[1, 0.1]` |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |
| [`ConstitutionUp`](../Reference_and_Meta/Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 46 | `-1`<br>`-2`<br>`1` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 50 | `1`<br>`2`<br>`4` |
| `HealthGain` | Integer | The amount of health restored to the source. | 63 | `1`<br>`10`<br>`2` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 40 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |

</details>


---


#### `StatusKilledCharacters`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_RandomChance`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_randomchance) | Object  | An object containing effects that execute only if a random roll succeeds, with an odds value defined inside. | 4 | `{ . . . }` |
| [`Conditional_Ally`](./Engine_StatusAndPassiveKeys.md#object-conditional_ally) | Object  | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 37 | `{ . . . }` |
| `AutoReanimate` | Number | The percentage chance for the unit to automatically reanimate upon death. | 4 | `100%`<br>`50%` |
| `AutoReanimate` | Number | The percentage chance for the unit to automatically reanimate upon death. | 4 | `100%`<br>`50%` |

</details>


---


#### `StatusKillers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 86 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Confusion`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 86 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Conditional_Boss`](./Engine_StatusAndPassiveKeys.md#object-conditional_boss) | Object  | Contains effects that apply only if the target is a boss enemy. | 21 | `{ . . . }` |
| [`Conditional_NotBoss`](./Engine_StatusAndPassiveKeys.md#object-conditional_notboss) | Object  | Contains effects that apply only if the target is not a boss enemy. | 16 | `{ . . . }` |

</details>


---


#### `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 113 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 50 | `1`<br>`2`<br>`4` |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. | 11 | `1`<br>`[1 .10]`<br>`[1 .25]` |
| `HealthGain` | Integer | The amount of health restored to the source. | 63 | `1`<br>`10`<br>`2` |

</details>


---


#### `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 53

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | If true, the effect triggers even if the unit is dead. | 25 | `true` |
| [`Conditional_GoodRoll`](./Engine_StatusAndPassiveKeys.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 37 | `{ . . . }` |
| [`Conditional_Corpse`](./Engine_StatusAndPassiveKeys.md#object-conditional_corpse) | Object  | Contains an inner effect block that only executes if the target is a corpse. | 11 | `{ . . . }` |
| [`Conditional_Shielded`](./Engine_StatusAndPassiveKeys.md#object-conditional_shielded) | Object  | An object containing effects that are only applied if the target has a shield active. | 5 | `{ . . . }` |
| [`FindItemFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 43 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`GainCoins`](../Reference_and_Meta/Arrays.md#array-gaincoins) | Array / Integer  | The amount of coins gained, or a [min, max] range. | 10 | `-5`<br>`1`<br>`2` |
| `PermanentStrength` | Integer | The amount of permanent bonus strength (physical damage modifier) granted. | 5 | `1`<br>`2` |
| `RepairAll` | Integer | The amount of durability restored to all equipped items. | 5 | `1`<br>`10` |
| [`RepairWeapon`](../Reference_and_Meta/Arrays.md#array-repairweapon) | Array / Integer  | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 7 | `1`<br>`6`<br>`99` |
| [`TransformWeapon`](./Engine_StatusAndPassiveKeys.md#object-transformweapon) | Object  | An object with `from` and `to` fields specifying the weapon transformation. | 2 | `{ . . . }` |

</details>


---


#### `StatusOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 169 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Craft`](./Engine_StatusAndPassiveKeys.md#object-craft) | Object  | Specifies the loot pool and slot to craft an item for the source. | 20 | `{ . . . }` |
| [`DestroyEquipmentAndAttachParasite`](./Engine_StatusAndPassiveKeys.md#object-destroyequipmentandattachparasite) | Object  | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 6 | `{ . . . }` |
| [`FindItemFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 43 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`ForceUseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 33 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`ObjectOnHitCharacter`](./Engine_StatusAndPassiveKeys.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 31 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`RandomMagicMissile`](./Engine_StatusAndPassiveKeys.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. | 41 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`ReviveNextRound`](./Engine_StatusAndPassiveKeys.md#object-revivenextround) | Integer / Object  | The number of revives granted, or an object defining revive properties. | 6 | `{ . . . }`<br>`2` |
| `SafeDie` | Integer | The number of times the unit can survive a fatal hit. | 7 | `1` |
| [`Sleep`](../Reference_and_Meta/Arrays.md#array-sleep) | Array / Integer  | The amount of sleep stacks applied, or an [stacks, probability] array. | 35 | `1`<br>`2`<br>`3` |
| `StealthUntilBasicAttack` | Integer | The number of stacks of Stealth that are removed when the unit performs a basic attack. | 2 | `1` |

</details>


---


#### `StatusOnBreak`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |
| [`Bruise`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 133 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`ApplyToRandomPartyMemberIfPossible`](./Engine_StatusAndPassiveKeys.md#object-applytorandompartymemberifpossible) | Object  | Contains an inner effect block that is applied to a random living party member if one exists. | 3 | `{ . . . }` |
| [`ConstitutionUp`](../Reference_and_Meta/Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 46 | `-1`<br>`-2`<br>`1` |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 25 | `-1`<br>`1`<br>`2` |
| [`FindItemFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 43 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| `HealthGain` | Integer | The amount of health restored to the source. | 63 | `1`<br>`10`<br>`2` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 45 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`ObjectOnHitCharacter`](./Engine_StatusAndPassiveKeys.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 31 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 71 | `"max(int, 0)"`<br>`-1`<br>`-2` |

</details>


---


#### `StatusOnBreakItem`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 109 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 130 | `1`<br>`2`<br>`3` |
| [`DoDamage`](./Engine_StatusAndPassiveKeys.md#object-dodamage) | Object  | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 7 | `{ . . . }` |

</details>


---


#### `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 109 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |
| `HealthGain` | Integer | The amount of health restored to the source. | 63 | `1`<br>`10`<br>`2` |

</details>


---


#### `StatusOnCollectPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 17 | `1`<br>`3` |

</details>


---


#### `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_RandomChance`](../Core_Entities_and_Combat/Items_and_Equipment.md#object-conditional_randomchance) | Object  | An object containing effects that execute only if a random roll succeeds, with an odds value defined inside. | 4 | `{ . . . }` |
| [`FindItemFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 43 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`RandomMagicMissile`](./Engine_StatusAndPassiveKeys.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. | 41 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `RemoveAmbientLightEffects` | Float | The fade-out duration in seconds for ambient light effects. | 2 | `.5`<br>`4` |
| [`ScatterCoins`](./Engine_StatusAndPassiveKeys.md#object-scattercoins) | Object  | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 8 | `{ . . . }` |

</details>


---


#### `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 71 | `{ . . . }`<br>`0`<br>`1` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 52 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 45 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 71 | `"max(int, 0)"`<br>`-1`<br>`-2` |

</details>


---


#### `StatusOnEatPill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |
| [`RandomPermanentStatsDistinct`](./Engine_StatusAndPassiveKeys.md#object-randompermanentstatsdistinct) | Object  | An object defining a set of stat changes (positive and negative) that are randomly applied as permanent modifications. | 1 | `{ . . . }` |

</details>


---


#### `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_FirstApplicationThisTurn`](./Engine_StatusAndPassiveKeys.md#object-conditional_firstapplicationthisturn) | Object  | Container for effects applied only on the first application of this ability during the turn. | 8 | `{ . . . }` |
| [`Conditional_GoodRoll`](./Engine_StatusAndPassiveKeys.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 37 | `{ . . . }` |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 50 | `1`<br>`2`<br>`4` |
| [`ForceAttack`](./Engine_StatusAndPassiveKeys.md#object-forceattack) | Integer / Object  | If set to 1, forces the target to perform an attack against a random or specified target. | 11 | `{ . . . }`<br>`1` |
| [`ImmediateUseAbility`](./Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 11 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 91 | `-1`<br>`-2`<br>`-4` |
| `SpeedUp_WithoutInitiative` | Integer | The number of stacks of Speed Up that do not affect the unit's initiative (turn order) stat. | 3 | `1` |
| [`RemoveStatusStacks`](./Engine_StatusAndPassiveKeys.md#object-removestatusstacks) | Object  | An object specifying a status name and the number of stacks to remove from the target. | 4 | `{ . . . }` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 50 | `1`<br>`2`<br>`4` |
| [`ImmediateUseAbility`](./Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 11 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |
| `SpeedUp_WithoutInitiative` | Integer | The number of stacks of Speed Up that do not affect the unit's initiative (turn order) stat. | 3 | `1` |
| [`ForceAttack`](./Engine_StatusAndPassiveKeys.md#object-forceattack) | Integer / Object  | If set to 1, forces the target to perform an attack against a random or specified target. | 11 | `{ . . . }`<br>`1` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 91 | `-1`<br>`-2`<br>`-4` |

</details>


---


#### `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 109 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`BackflipWhenTargeted`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-backflipwhentargeted) | Enum / Integer / Object  | The number of backflip charges, or an object defining its ability. | 15 | `{ . . . }`<br>`1`<br>`2`<br>`X` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 50 | `1`<br>`2`<br>`4` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 51 | `-1`<br>`-2`<br>`-4` |

</details>


---


#### `StatusOnHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 109 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 130 | `1`<br>`2`<br>`3` |
| [`ObjectOnHitCharacter`](./Engine_StatusAndPassiveKeys.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 31 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |

</details>


---


#### `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 40

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 109 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 113 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Conditional_GoodRoll`](./Engine_StatusAndPassiveKeys.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 37 | `{ . . . }` |
| [`Conditional_FirstApplicationThisTurn`](./Engine_StatusAndPassiveKeys.md#object-conditional_firstapplicationthisturn) | Object  | Container for effects applied only on the first application of this ability during the turn. | 8 | `{ . . . }` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 52 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Stealth`](../Reference_and_Meta/Arrays.md#array-stealth) | Array / Integer  | The number of stealth stacks applied. | 11 | `1`<br>`2`<br>`[1 .1]` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. | 16 | `-1`<br>`-2`<br>`1` |
| [`ConstitutionUp`](../Reference_and_Meta/Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 46 | `-1`<br>`-2`<br>`1` |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 25 | `-1`<br>`1`<br>`2` |
| `HealthGain` | Integer | The amount of health restored to the source. | 63 | `1`<br>`10`<br>`2` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 45 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 51 | `-1`<br>`-2`<br>`-4` |
| `RangeUp` | Integer | The number of stacks of bonus attack range applied. | 6 | `1` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 91 | `-1`<br>`-2`<br>`-4` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 71 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `BrittleCharismaUp` | Integer | The number of stacks of temporary Charisma gained on kill. | 1 | `2` |
| `BrittleConstitutionUp` | Integer | The number of stacks of temporary Constitution gained on kill. | 1 | `2` |
| `BrittleDexterityUp` | Integer | The number of stacks of temporary Dexterity gained on kill. | 1 | `2` |
| `BrittleIntelligenceUp` | Integer | The number of stacks of temporary Intelligence gained on kill. | 1 | `2` |
| `BrittleLuckUp` | Integer | The number of stacks of temporary Luck gained on kill. | 1 | `2` |
| `BrittleSpeedUp` | Integer | The number of stacks of temporary Speed gained on kill. | 1 | `2` |
| `BrittleStrengthUp` | Integer | The number of stacks of temporary Strength gained on kill. | 1 | `2` |
| [`UseAbility_NonStack`](../Reference_and_Meta/Enums.md#enum-useability_nonstack) | Enum | Specifies an ability to use on kill that does not stack with itself. | 3 | `BBTransformZealot`<br>`GenericRage` |

</details>


---


#### `StatusOnKillEnemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 169 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 113 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 50 | `1`<br>`2`<br>`4` |
| [`ForceUseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 33 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `HealthGain` | Integer | The amount of health restored to the source. | 63 | `1`<br>`10`<br>`2` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 51 | `-1`<br>`-2`<br>`-4` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 40 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |

</details>


---


#### `StatusOnPickupCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 25 | `-1`<br>`1`<br>`2` |
| [`GainCoins`](../Reference_and_Meta/Arrays.md#array-gaincoins) | Array / Integer  | The amount of coins gained, or a [min, max] range. | 10 | `-5`<br>`1`<br>`2` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 91 | `-1`<br>`-2`<br>`-4` |

</details>


---


#### `StatusOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer | The amount of health restored to the source. | 63 | `1`<br>`10`<br>`2` |
| [`RepairWeapon`](../Reference_and_Meta/Arrays.md#array-repairweapon) | Array / Integer  | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 7 | `1`<br>`6`<br>`99` |

</details>


---


#### `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 46

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 109 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 130 | `1`<br>`2`<br>`3` |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 113 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Conditional_HasStatus`](./Engine_StatusAndPassiveKeys.md#object-conditional_hasstatus) | Object  | Contains an inner effect block that only executes if the target has the specified status effect. | 20 | `{ . . . }` |
| [`Craft`](./Engine_StatusAndPassiveKeys.md#object-craft) | Object  | Specifies the loot pool and slot to craft an item for the source. | 20 | `{ . . . }` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 26 | `1`<br>`10`<br>`100` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 52 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Conditional_HealthThreshold`](./Engine_StatusAndPassiveKeys.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 7 | `{ . . . }` |
| [`Else`](./Engine_StatusAndPassiveKeys.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 86 | `{ . . . }` |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |
| [`ConstitutionUp`](../Reference_and_Meta/Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 46 | `-1`<br>`-2`<br>`1` |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. | 12 | `1`<br>`2`<br>`3` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 50 | `1`<br>`2`<br>`4` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 45 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 51 | `-1`<br>`-2`<br>`-4` |
| `MovementUp` | Integer | The amount of movement increase or decrease applied. | 12 | `-2`<br>`1`<br>`2` |
| `RandomInjury` | Integer | The number of random injuries applied. | 8 | `1` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 91 | `-1`<br>`-2`<br>`-4` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 71 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. | 12 | `-1`<br>`1`<br>`2` |
| `TempMovement` | Enum / Integer | The amount of temporary movement range added, or a string alias like 'mov'. | 4 | `1`<br>`20`<br>`mov` |

</details>


---


#### `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 109 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. | 12 | `1`<br>`2`<br>`3` |
| `ExtraBasicAttacks_Status` | Integer | The number of additional basic attacks the unit can perform each turn. | 7 | `1` |

</details>


---


#### `StatusOnUseBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 113 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `HealthGain` | Integer | The amount of health restored to the source. | 63 | `1`<br>`10`<br>`2` |

</details>


---


#### `StatusRandomEnemiesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| [`Confusion`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 86 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 99 | `0`<br>`1`<br>`10` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 47 | `1`<br>`2`<br>`3` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 108 | `1`<br>`10`<br>`2` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 51 | `1`<br>`2`<br>`[1 .01]` |

</details>


---


#### `StatusWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 40 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`OneUseSpellDamageUp`](./Engine_StatusAndPassiveKeys.md#object-oneusespelldamageup) | Array / Float / Object  | Increases spell damage by the specified amount, but the effect is consumed after a single use. Alias for SpellDamageUp. | 3 | `{ . . . }`<br>`2` |

</details>


---


#### `TakeBonusTurnWithAIControl`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | If true, the AI-controlled bonus turn includes spells as available actions. | 4 | `true` |
| `end_of_round` | Boolean | If true, the effect triggers at the end of the round instead of at the start of the turn. | 3 | `true` |

</details>


---


#### `TakeBonusTurnWithStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 86 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Madness`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 45 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 138 | `1`<br>`2`<br>`3` |

</details>


---


#### `TempPassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 160 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |

</details>


---


#### `additional_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 113 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. | 11 | `1`<br>`[1 .10]`<br>`[1 .25]` |
| `HealthGain` | Integer | The amount of health restored to the source. | 63 | `1`<br>`10`<br>`2` |
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. | 16 | `1` |
| [`ReviveNextRound`](./Engine_StatusAndPassiveKeys.md#object-revivenextround) | Integer / Object  | The number of revives granted, or an object defining revive properties. | 6 | `{ . . . }`<br>`2` |
| [`SafeDoomed`](../Reference_and_Meta/Enums.md#enum-safedoomed) | Enum / Integer  | The number of SafeDoomed stacks applied, or 'level' to scale with character level. | 16 | `1`<br>`2`<br>`level` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 91 | `-1`<br>`-2`<br>`-4` |

</details>


---


#### `bonus_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 138

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 50 | `1`<br>`10`<br>`100` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |
| `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 127 | `1`<br>`3`<br>`4` |
| [`AutocastEachRound`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-autocasteachround) | Enum / Object  | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 10 | `{ . . . }`<br>`SpiderReturn` |
| `AlphaDodgeChance` | Integer | The dodge chance granted to the alpha (leader) unit. | 2 | `50%` |
| `DownRankAIIfWeaponUsable` | Float | A multiplier that reduces the AI's priority to use this ability if the unit has a usable weapon. | 4 | `.001` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 45 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`XIsSpellStormRampAndReset`](./Engine_StatusAndPassiveKeys.md#object-xisspellstormrampandreset) | Integer / Object  | If integer 0, resets stacks; if object, contains 'stacks' and 'reset_percent' for spell storm ramp. | 2 | `{ . . . }`<br>`0` |

</details>


---


#### `extra_statuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 203 | `1`<br>`10`<br>`2` |
| [`Conditional_HasTag`](./Engine_StatusAndPassiveKeys.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 47 | `{ . . . }` |
| [`Burn`](../Reference_and_Meta/Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 154 | `1`<br>`10`<br>`2` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |
| `HealthGain` | Integer | The amount of health restored to the source. | 63 | `1`<br>`10`<br>`2` |
| [`Tarred`](../Reference_and_Meta/Arrays.md#array-tarred) | Array / Integer  | The amount of tarred stacks applied, or an [stacks, probability] array. | 17 | `1`<br>`2`<br>`[1 .1]` |

</details>


---


#### `party_status_next_fight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 203 | `1`<br>`10`<br>`2` |
| [`Immobile`](../Reference_and_Meta/Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 47 | `0`<br>`1`<br>`10%` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 50 | `1`<br>`2`<br>`4` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 108 | `1`<br>`10`<br>`2` |
| [`NoHealthRegen`](./Engine_StatusAndPassiveKeys.md#object-nohealthregen) | Array / Float / Object  | Prevents the unit from regenerating health normally. | 7 | `{ . . . }`<br>`1` |
| [`Tangled`](./Engine_StatusAndPassiveKeys.md#object-tangled) | Array / Integer / Object  | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 10 | `{ . . . }`<br>`1`<br>`2`<br>`[1, .05]` |
| [`Tarred`](../Reference_and_Meta/Arrays.md#array-tarred) | Array / Integer  | The amount of tarred stacks applied, or an [stacks, probability] array. | 17 | `1`<br>`2`<br>`[1 .1]` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 19 | `1`<br>`2`<br>`[1 .1]` |

</details>


---


#### `passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2805

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


#### `self_status_next_fight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 143

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 24 | `10`<br>`15`<br>`20` |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| [`Bruise`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 133 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 203 | `1`<br>`10`<br>`2` |
| [`Blind`](../Reference_and_Meta/Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 43 | `-1`<br>`1`<br>`2` |
| [`Confusion`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 86 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Slow`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 75 | `{ . . . }`<br>`-1`<br>`1`<br>`2` |
| [`Burn`](../Reference_and_Meta/Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 154 | `1`<br>`10`<br>`2` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. | 16 | `-1`<br>`-2`<br>`1` |
| [`ConstitutionUp`](../Reference_and_Meta/Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 46 | `-1`<br>`-2`<br>`1` |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 25 | `-1`<br>`1`<br>`2` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 50 | `1`<br>`2`<br>`4` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 108 | `1`<br>`10`<br>`2` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 45 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 51 | `-1`<br>`-2`<br>`-4` |
| [`Madness`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 45 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`NoHealthRegen`](./Engine_StatusAndPassiveKeys.md#object-nohealthregen) | Array / Float / Object  | Prevents the unit from regenerating health normally. | 7 | `{ . . . }`<br>`1` |
| [`NoManaRegen`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-nomanaregen) | Array / Float / Object  | The unit does not naturally regenerate mana per turn. Value indicates the stage or flag enabling this restriction. | 3 | `{ . . . }`<br>`1` |
| [`PermanentConfusion`](./Engine_StatusAndPassiveKeys.md#object-permanentconfusion) | Array / Float / Object  | If set to 1, the unit is permanently confused and cannot be cured. | 3 | `{ . . . }`<br>`1` |
| `ProbeCharmed` | Integer | The number of charm stacks applied by a probe. | 3 | `1` |
| [`Rot`](../Reference_and_Meta/Arrays.md#array-rot) | Array / Integer  | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 20 | `-999999`<br>`1`<br>`2` |
| [`Sleep`](../Reference_and_Meta/Arrays.md#array-sleep) | Array / Integer  | The amount of sleep stacks applied, or an [stacks, probability] array. | 35 | `1`<br>`2`<br>`3` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 91 | `-1`<br>`-2`<br>`-4` |
| `SpiderInfested` | Integer | The number of spider infestation stacks applied. | 10 | `1`<br>`2`<br>`4` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 71 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 138 | `1`<br>`2`<br>`3` |
| [`Tarred`](../Reference_and_Meta/Arrays.md#array-tarred) | Array / Integer  | The amount of tarred stacks applied, or an [stacks, probability] array. | 17 | `1`<br>`2`<br>`[1 .1]` |
| `TempStrengthUp` | Enum | The number of stacks of temporary Strength Up applied to the unit. | 7 | `1`<br>`2`<br>`X` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 19 | `1`<br>`2`<br>`[1 .1]` |

</details>


---


#### `statuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>
## Discovered Objects

> These tables were auto-generated by the schema audit tool. They document objects found in the `.gon` files that were not previously documented.


### Object: `DefaultMove`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 326

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BasicMelee`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 126

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `Maggot`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 46

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `Paper`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 26

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Assets_and_Localization/Strings.md#string-name) | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Assets_and_Localization/Strings.md#string-desc) | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |

</details>


### Object: `Wood`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 25

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Assets_and_Localization/Strings.md#string-name) | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Assets_and_Localization/Strings.md#string-desc) | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |

</details>


### Object: `MoveOne`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `zaratana`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 19

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Assets_and_Localization/Strings.md#string-name) | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `frame_label` | String | Specifies the frame or cutscene animation label for the boss encounter. | 1 | `AlienBeast`<br>`ColorlessCat_Tutorial`<br>`DrMangler` |
| `level` | String | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| `quotes` | Array | An array of dialogue quotes for the boss cutscene. | 1 | `[` |
| `act` | Number | The act number (game progression stage) in which this encounter or script takes place. | 1 | `1`<br>`2`<br>`3` |
| `music` | String | Specifies the name of the music track to play during the encounter. | 1 | `alley`<br>`guillotina`<br>`hitler3` |
| `arrival_unlock` | String | The name of the cutscene or event that is unlocked upon arrival. | 1 | `npc_houseboss_intro_guillotina_1`<br>`npc_houseboss_intro_guillotina_2`<br>`npc_houseboss_intro_guillotina_3` |
| `index` | Number | The index used to order or identify this encounter within its list. | 1 | `1`<br>`2`<br>`3` |
| [`initial_cooldown`](../Reference_and_Meta/Arrays.md#array-initial_cooldown) | Array   | A list of possible initial cooldown values (in turns) before the encounter can trigger. | 1 | `[0]`<br>`[3 7]` |
| `lead_time` | Number | The number of turns before the event activates. | 1 | `7` |
| [`rematch_cooldown`](../Reference_and_Meta/Arrays.md#array-rematch_cooldown) | Array   | The minimum and maximum number of days before a rematch becomes available. | 1 | `[3 7]` |
| [`savefile_string`](../Assets_and_Localization/Strings.md#string-savefile_string) | String | A unique string identifier used to track the save file associated with this encounter. | 1 | `"SAVE_FILE_FIGHT_HOUSEBOSS_GUILLOTINA_1"`<br>`"SAVE_FILE_FIGHT_HOUSEBOSS_GUILLOTINA_2"`<br>`"SAVE_FILE_FIGHT_HOUSEBOSS_GUILLOTINA_3"` |
| `initial_cutscene_day` | String | The name of the cutscene that plays on the first day the encounter appears. | 1 | `kaiju_fight`<br>`moonboss_intro`<br>`pyro_intro` |
| `rematch_cutscene_day` | String | Specifies the cutscene to play on the day of the rematch. | 1 | `house_boss_returns_kaijufight`<br>`house_boss_returns_pyro`<br>`house_boss_returns_zara` |
| `BOSS_ZARATANA_QUOTE_1` | String | A string for the first quote spoken by the boss Zara Tana. | 1 ||
| `BOSS_ZARATANA_QUOTE_2` | String | A string for the second quote spoken by the boss Zara Tana. | 1 ||

</details>
### Object: `CharmedLeech`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 18

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `Bionic`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 18

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Assets_and_Localization/Strings.md#string-name) | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Assets_and_Localization/Strings.md#string-desc) | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |

</details>


### Object: `CharmedFly`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 17

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `CharmedTinySpider`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 2 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 2 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |

</details>


### Object: `pyrophina`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Assets_and_Localization/Strings.md#string-name) | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `frame_label` | String | Specifies the frame or cutscene animation label for the boss encounter. | 1 | `AlienBeast`<br>`ColorlessCat_Tutorial`<br>`DrMangler` |
| `level` | String | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| `quotes` | Array | An array of dialogue quotes for the boss cutscene. | 1 | `[` |
| `act` | Number | The act number (game progression stage) in which this encounter or script takes place. | 1 | `1`<br>`2`<br>`3` |
| `music` | String | Specifies the name of the music track to play during the encounter. | 1 | `alley`<br>`guillotina`<br>`hitler3` |
| `arrival_unlock` | String | The name of the cutscene or event that is unlocked upon arrival. | 1 | `npc_houseboss_intro_guillotina_1`<br>`npc_houseboss_intro_guillotina_2`<br>`npc_houseboss_intro_guillotina_3` |
| `index` | Number | The index used to order or identify this encounter within its list. | 1 | `1`<br>`2`<br>`3` |
| [`initial_cooldown`](../Reference_and_Meta/Arrays.md#array-initial_cooldown) | Array   | A list of possible initial cooldown values (in turns) before the encounter can trigger. | 1 | `[0]`<br>`[3 7]` |
| `lead_time` | Number | The number of turns before the event activates. | 1 | `7` |
| [`rematch_cooldown`](../Reference_and_Meta/Arrays.md#array-rematch_cooldown) | Array   | The minimum and maximum number of days before a rematch becomes available. | 1 | `[3 7]` |
| [`savefile_string`](../Assets_and_Localization/Strings.md#string-savefile_string) | String | A unique string identifier used to track the save file associated with this encounter. | 1 | `"SAVE_FILE_FIGHT_HOUSEBOSS_GUILLOTINA_1"`<br>`"SAVE_FILE_FIGHT_HOUSEBOSS_GUILLOTINA_2"`<br>`"SAVE_FILE_FIGHT_HOUSEBOSS_GUILLOTINA_3"` |
| `initial_cutscene_day` | String | The name of the cutscene that plays on the first day the encounter appears. | 1 | `kaiju_fight`<br>`moonboss_intro`<br>`pyro_intro` |
| `rematch_cutscene_day` | String | Specifies the cutscene to play on the day of the rematch. | 1 | `house_boss_returns_kaijufight`<br>`house_boss_returns_pyro`<br>`house_boss_returns_zara` |
| `BOSS_PYROPHINA_QUOTE_1` | String | Localization key for the first boss quote for Pyrophina. | 1 ||
| `BOSS_PYROPHINA_QUOTE_2` | String | Localization key for the second boss quote for Pyrophina. | 1 ||

</details>


### Object: `BrambleRandomTileEvent`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `BeefyCharmedLeech`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `Hyde`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| `head` | Float | The catalog ID for the cat's head part. | 1 | `-1`<br>`1`<br>`1.3` |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 1 | `-1`<br>`-2`<br>`1` |
| `palette` | Number | Specifies the color palette index for the ability's visuals. | 1 | `-1`<br>`0`<br>`1` |
| `texture` | Number | The catalog ID for the cat's texture. | 1 | `-1`<br>`1`<br>`1000` |
| `tail` | Number | The catalog ID for the cat's tail part. | 1 | `-1`<br>`1000`<br>`1001` |
| `default_frame` | Number | The default sprite frame used for the character's portrait or body. | 1 | `1`<br>`1000`<br>`1001` |
| `arm2` | Number | The catalog ID for the cat's second arm part. | 1 | `-1`<br>`-2`<br>`1` |
| `body` | Float | The catalog ID for the cat's body part. | 1 | `-1`<br>`1`<br>`1.1` |
| `arm1` | Number | The catalog ID for the cat's first arm part. | 1 | `-1`<br>`-2`<br>`1` |
| `righteye` | Number | The sprite frame index for the character's right eye. | 1 | `1`<br>`100`<br>`1001` |
| `voice` | String | Determines which voice set or type is used for the character. | 1 | `ankylosaurus`<br>`female1`<br>`female10` |
| `lefteye` | Number | The sprite frame index for the character's left eye. | 1 | `1`<br>`100`<br>`1001` |
| `claws` | Number | The sprite frame index for the character's claws. | 1 | `1`<br>`1032`<br>`2` |
| `leg1` | Number | The catalog ID for the cat's first leg part. | 1 | `-1`<br>`-2`<br>`1` |
| `leg2` | Number | The catalog ID for the cat's second leg part. | 1 | `-1`<br>`1`<br>`10` |
| `rightear` | Number | The sprite frame index for the character's right ear. | 1 | `1000`<br>`1001`<br>`1004` |
| `leftear` | Number | The sprite frame index for the character's left ear. | 1 | `1`<br>`1000`<br>`1001` |
| `righteyebrow` | Number | The sprite frame index for the character's right eyebrow. | 1 | `1`<br>`1000`<br>`1001` |
| `lefteyebrow` | Number | The sprite frame index for the character's left eyebrow. | 1 | `1`<br>`1000`<br>`1001` |
| `pitch` | Float | The sound pitch multiplier for the character's voice or sounds. | 1 | `.3`<br>`.5`<br>`.6` |
| `default_face` | String | Specifies the default facial expression for the unit's portrait. | 1 | `angry`<br>`happy`<br>`mad` |

</details>


### Object: `BasicTankMelee`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `SpiderReturn`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `Nubs`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 0 | `{ . . . }` |

</details>


### Object: `CharmedPooter`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `NoHead`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| `head` | Float | The catalog ID for the cat's head part. | 1 | `-1`<br>`1`<br>`1.3` |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 1 | `-1`<br>`-2`<br>`1` |
| `palette` | Number | Specifies the color palette index for the ability's visuals. | 1 | `-1`<br>`0`<br>`1` |
| `texture` | Number | The catalog ID for the cat's texture. | 1 | `-1`<br>`1`<br>`1000` |
| `default_frame` | Number | The default sprite frame used for the character's portrait or body. | 1 | `1`<br>`1000`<br>`1001` |
| `righteye` | Number | The sprite frame index for the character's right eye. | 1 | `1`<br>`100`<br>`1001` |
| `voice` | String | Determines which voice set or type is used for the character. | 1 | `ankylosaurus`<br>`female1`<br>`female10` |
| `lefteye` | Number | The sprite frame index for the character's left eye. | 1 | `1`<br>`100`<br>`1001` |
| `claws` | Number | The sprite frame index for the character's claws. | 1 | `1`<br>`1032`<br>`2` |
| `rightear` | Number | The sprite frame index for the character's right ear. | 1 | `1000`<br>`1001`<br>`1004` |
| `leftear` | Number | The sprite frame index for the character's left ear. | 1 | `1`<br>`1000`<br>`1001` |
| `righteyebrow` | Number | The sprite frame index for the character's right eyebrow. | 1 | `1`<br>`1000`<br>`1001` |
| `lefteyebrow` | Number | The sprite frame index for the character's left eyebrow. | 1 | `1`<br>`1000`<br>`1001` |
| `pitch` | Float | The sound pitch multiplier for the character's voice or sounds. | 1 | `.3`<br>`.5`<br>`.6` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 0 | `{ . . . }` |

</details>


### Object: `CharmedTinyTumor`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `BasicRanged`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `BasicMonkMelee`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `Chubs`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 0 | `{ . . . }` |

</details>


### Object: `BasicStraightShot`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `BasicMagicMissile`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `TVOff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `ThornUpX`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Shove`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |

</details>


### Object: `ReaperRevenge`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }` |

</details>


### Object: `RatKing`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `Necro_SoulDagger_Uncharged`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Assets_and_Localization/Strings.md#string-name) | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Assets_and_Localization/Strings.md#string-desc) | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |

</details>


### Object: `MockingbirdForm`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`tags`](../Reference_and_Meta/Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |

</details>


### Object: `GrenadeExplode`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }` |

</details>


### Object: `GirlDino`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `DrMangler`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `CookedChickenLeg`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `BoomerCatExplode`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `BBTransformZealot`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BBTransformMutant`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BasicPsychicPull`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `BasicNecroRanged`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `BasicMedicMelee`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `BasicMagicShortRanged`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `BasicButcherMelee`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `ToadJump_BasicMove`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `Shadowstep`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `neck_NukeExplode`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }` |
| [`bonus_passives`](../Reference_and_Meta/Miscellaneous.md#object-bonus_passives) | Object  | Grants temporary passive abilities to the caster for the duration of the ability. | 1 | `{ . . . }` |
| [`splash_damage`](../Reference_and_Meta/Miscellaneous.md#object-splash_damage) | Object  | Defines additional damage or effects applied to nearby targets around the primary target. | 1 | `{ . . . }` |

</details>


### Object: `ManglersMonster`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `Lava_Distortion`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| [`particle_lifetime`](../Reference_and_Meta/Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| [`speed_start`](../Reference_and_Meta/Arrays.md#array-speed_start) | Array   | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`scripts`](../Reference_and_Meta/Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| `size_start` | Float | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| `size_end` | Float | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| `alpha_end` | Float | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| [`rotation`](../Reference_and_Meta/Arrays.md#array-rotation) | Array  | The rotation of the effect, specified as a single value or a random range [min, max] in degrees. | 1 | `-90`<br>`90`<br>`[-10 10]` |
| `alpha` | Float | The alpha transparency value for the particle system (e.g., '0.03'). | 1 | `.005`<br>`.01`<br>`.03` |
| `rotation_speed_end` | Number | The rotation speed (in degrees per second) of the effect at the end of its animation. | 1 | `0` |
| `render_layer` | String | The render layer on which the effect is drawn (e.g., background, top). | 1 | `background`<br>`sorted_distortions`<br>`splatters` |
| `material` | String | The material shader name used for rendering the visual effect. | 1 | `distorter`<br>`mist` |

</details>


### Object: `Haunt`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `Guillotina3Head`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `Guillotina3Body`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `Guillotina2Head`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `Guillotina2Body`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `DecoyExplode`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `CharmedDemonKitten`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `CatapultJump`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `BungaSwipe`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `ai_ability` | String | Specifies the ability to use as the AI's behavior for this ability. | 1 | `AZ_Jump_AI`<br>`BasicBigMelee`<br>`BasicMelee` |

</details>


### Object: `BoyDino`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `UltraSmough`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `TT_Thrash`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `TrexSwitchTarget`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `TormentorRuneAbsorb`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `ThrobbingKing2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `ThornUp`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `TheCreator_SpawnCloneTeam`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spawn`](../Reference_and_Meta/Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. | 2 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`tags`](../Reference_and_Meta/Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |

</details>


### Object: `TC_DashReaction`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`temporary_effects`](../Reference_and_Meta/Miscellaneous.md#object-temporary_effects) | Object  | Applies temporary status effects on the caster upon using the ability. | 1 | `{ . . . }` |
| `ai_ability` | String | Specifies the ability to use as the AI's behavior for this ability. | 1 | `AZ_Jump_AI`<br>`BasicBigMelee`<br>`BasicMelee` |

</details>


### Object: `TattersFear`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `Spook`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `SpikeBuff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `particle_lifetime` | Float | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `speed_start` | Float | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`scripts`](../Reference_and_Meta/Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| `size_start` | Float | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| `size_end` | Float | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| `speed_scale` | Float | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| `alpha_end` | Float | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| `alpha_start` | Float | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1`<br>`.5`<br>`.8` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local`<br>`local*/` |

</details>


### Object: `SparkleBuff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| [`particle_lifetime`](../Reference_and_Meta/Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `speed_start` | Float | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`scripts`](../Reference_and_Meta/Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| [`size_start`](../Reference_and_Meta/Arrays.md#array-size_start) | Array   | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| `size_end` | Float | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| `speed_scale` | Float | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| `alpha_end` | Float | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| `alpha_start` | Float | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1`<br>`.5`<br>`.8` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local`<br>`local*/` |

</details>


### Object: `Smough`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `SleepDart2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Assets_and_Localization/Strings.md#string-name) | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Assets_and_Localization/Strings.md#string-desc) | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `durability` | Number | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |

</details>


### Object: `SleepDart`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Assets_and_Localization/Strings.md#string-name) | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Assets_and_Localization/Strings.md#string-desc) | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `durability` | Number | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |

</details>


### Object: `PlayerCat_ThiefShade2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `PassiveTar`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| [`particle_lifetime`](../Reference_and_Meta/Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `size` | Float | The scale factor (size multiplier) of the spawned unit. | 1 | `.2`<br>`.5`<br>`1` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `speed_start` | Float | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| `rotation` | Number | The rotation of the effect, specified as a single value or a random range [min, max] in degrees. | 1 | `-90`<br>`90`<br>`[-10 10]` |
| [`force_start`](../Reference_and_Meta/Arrays.md#array-force_start) | Array   | The initial force applied to particles, as a scalar or 3D vector. | 1 | `0`<br>`[0 -10 0]`<br>`[0 -20 0]` |
| `emit_radius` | Float | The radius from which particles or effects are emitted. | 1 | `.05`<br>`.1`<br>`.2` |
| `alpha_out` | Float | The alpha (opacity) value at the end of the effect's outro animation. | 1 | `.2`<br>`.3`<br>`.5` |
| `alpha_in` | Float | The alpha (opacity) value at the start of the effect's intro animation. | 1 | `.01`<br>`.05`<br>`.1` |
| [`force_end`](../Reference_and_Meta/Arrays.md#array-force_end) | Array   | The final force applied to particles over time, as a scalar or 3D vector. | 1 | `200`<br>`500`<br>`[0 -1 0]` |
| `size_in` | Float | The size of the effect at the beginning of its intro animation. | 1 | `.1`<br>`.3`<br>`.5` |
| `spurt` | String | The name of the spurt particle effect to play. | 1 | `GibsBloodSpurt`<br>`GibsBloodSpurtHuge`<br>`PassiveTarSplat` |

</details>


### Object: `PassiveEnergized`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `particle_lifetime` | Float | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`size`](../Reference_and_Meta/Arrays.md#array-size) | Array  | The scale factor (size multiplier) of the spawned unit. | 1 | `.2`<br>`.5`<br>`1` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| [`friction`](../Reference_and_Meta/Arrays.md#array-friction) | Array  | A scalar or 3D vector multiplier for velocity reduction applied over time. | 1 | `.1`<br>`.2`<br>`.5` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| [`speed_start`](../Reference_and_Meta/Arrays.md#array-speed_start) | Array   | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`rotation`](../Reference_and_Meta/Arrays.md#array-rotation) | Array  | The rotation of the effect, specified as a single value or a random range [min, max] in degrees. | 1 | `-90`<br>`90`<br>`[-10 10]` |
| `emit_radius` | Float | The radius from which particles or effects are emitted. | 1 | `.05`<br>`.1`<br>`.2` |
| `size_in` | Float | The size of the effect at the beginning of its intro animation. | 1 | `.1`<br>`.3`<br>`.5` |
| `unlit` | Boolean | If true, the effect is not affected by scene lighting. | 1 | `true` |

</details>


### Object: `Ornstein`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `NubsGoop`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `NubbyToss`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `neck_NukeBonus`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`bonus_passives`](../Reference_and_Meta/Miscellaneous.md#object-bonus_passives) | Object  | Grants temporary passive abilities to the caster for the duration of the ability. | 1 | `{ . . . }` |
| `sub_ability` | String | Specifies a sub-ability that is part of this ability, often used for multi-part abilities. | 1 | `CollectiveCounterImpl`<br>`CollectiveSpinImpl`<br>`HomingBlasts2_sub` |

</details>


### Object: `MegaGuppy_SummonTheChild`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spawn`](../Reference_and_Meta/Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. | 2 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `ManglerMonsterDashAttack`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `ManglerEnrage`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `LennyCatDies`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }` |

</details>


### Object: `IDSprout`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spawn`](../Reference_and_Meta/Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. | 2 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `HemBounce`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `HCHumanDie`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `GirlDinoCry`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `FireExtinguish_Steam`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`speed`](../Reference_and_Meta/Arrays.md#array-speed) | Array  | The speed of the projectile or move, can be a value or a range. | 1 | `-30`<br>`-4`<br>`.5` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `particle_lifetime` | Float | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`size`](../Reference_and_Meta/Arrays.md#array-size) | Array  | The scale factor (size multiplier) of the spawned unit. | 1 | `.2`<br>`.5`<br>`1` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`scripts`](../Reference_and_Meta/Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| `alpha` | Float | The alpha transparency value for the particle system (e.g., '0.03'). | 1 | `.005`<br>`.01`<br>`.03` |
| `emit_radius` | Float | The radius from which particles or effects are emitted. | 1 | `.05`<br>`.1`<br>`.2` |
| `emit_timespread` | Float | The time spread over which emissions occur, controlling the duration of the emission burst. | 1 | `.1`<br>`.25`<br>`.75` |
| `emit_timespread_curve` | String | The curve type (e.g., ease_out) that defines how emission rate changes over time. | 1 | `ease_out` |

</details>


### Object: `Digest`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }` |

</details>


### Object: `cWaggle2x2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `cWaggle`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `ChubsRage`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `ChubsGoop`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `CharmedFlySwarm`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `CerberubsStraightReaction`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `CaveCatDad`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`equipment`](../Reference_and_Meta/Miscellaneous.md#object-equipment) | Object  | A container object defining the character's equipped items (head, face, neck, weapon, etc.). | 1 | `{ . . . }` |

</details>


### Object: `CatGoop`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `CatapultJump2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `BoyDinoCry`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BonusToss`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `BloatyExplodey`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `BloatEyeMovement2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `BasicSuplex`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`tags`](../Reference_and_Meta/Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |

</details>


### Object: `BasicDruidAbility`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`tags`](../Reference_and_Meta/Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |

</details>


### Object: `AbsorbBuff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| [`particle_lifetime`](../Reference_and_Meta/Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `speed_start` | Float | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`scripts`](../Reference_and_Meta/Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| [`size_start`](../Reference_and_Meta/Arrays.md#array-size_start) | Array   | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| `size_end` | Float | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| `speed_scale` | Float | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| `alpha_end` | Float | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| `alpha_start` | Float | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1`<br>`.5`<br>`.8` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local`<br>`local*/` |

</details>


### Object: `XIsSpellStormRampAndReset`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `reset_percent` | Integer | The percentage of the ramp-up value to reset to upon casting. | 1 | `50%` |

#### `ApplyToSourceOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AlphaCat` | Integer | The number of AlphaCat stacks applied to the source on kill. | 18 | `1` |
| [`Revive`](./Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object  | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 21 | `{ . . . }`<br>`1`<br>`100%`<br>`50%` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |
| [`EvolveAbilityFromPool`](../Reference_and_Meta/Miscellaneous.md#object-evolveabilityfrompool) | Enum / Object  | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. | 26 | `{ . . . }`<br>`Butcher`<br>`Druid`<br>`Fighter` |
| `HealthGain` | Integer | The amount of health restored to the source. | 63 | `1`<br>`10`<br>`2` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 40 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 71 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `WeaponAuxMultiplier` | Float | A multiplier string (e.g., '.5') for the weapon's auxiliary counter on kill. | 1 | `.5` |

</details>


---


#### `Consumed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`struggle_ability`](../Reference_and_Meta/Enums.md#enum-struggle_ability) | Enum | Specifies the name of the ability the consumed unit uses to attempt escape. | 17 | `CHuskStruggle`<br>`CaveWomanEscape`<br>`LennyStruggle` |
| `force_contact` | Boolean | If true, the consumed unit is forced into contact with the consumer. | 15 | `true` |
| `instant` | Boolean | If true, the consumption happens immediately without a timer. | 13 | `true` |
| [`mount_mode`](../Reference_and_Meta/Enums.md#enum-mount_mode) | Boolean / Enum | Specifies the mounting mode; values include 'auto' or 'true'. | 12 | `auto`<br>`true` |
| `do_not_pop_corpse` | Boolean | If true, the consumed unit's corpse is not popped upon consumption. | 11 | `true` |
| [`drop_on_death`](../Reference_and_Meta/Enums.md#enum-drop_on_death) | Boolean / Enum | Determines if and how the consumed unit is dropped on death; values include 'true', 'false', or 'deferred'. | 11 | `deferred`<br>`false`<br>`true` |
| `wet` | Boolean | If true, the consumed unit is considered wet (e.g., for elemental interactions). | 8 | `false`<br>`true` |
| `drop_on_self_death` | Boolean | If true, the consumed unit is dropped when the consumer dies. | 3 | `true` |
| [`extra_statuses`](../Reference_and_Meta/Miscellaneous.md#object-extra_statuses) | Object  | An object containing additional status effects (with stack counts) applied to the consumed unit. | 4 | `{ . . . }` |
| `use_placeholder` | Boolean | If true, renders the ability using a temporary placeholder animation instead of the final art. | 17 | `true` |
| [`drop_body_ability`](../Reference_and_Meta/Enums.md#enum-drop_body_ability) | Enum | Specifies the ability used to drop the consumed body. | 1 | `MoonHandDrop` |
| `kill_on_consume` | Boolean | If true, the consumed unit is killed immediately upon consumption. | 1 | `true` |

</details>


---


### Object: `UFO_BigExplode`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `ToxPuff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `ToxicBubbles`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| [`emit_rate`](../Reference_and_Meta/Arrays.md#array-emit_rate) | Array   | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `particle_lifetime` | Float | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `speed_start` | Float | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`size_start`](../Reference_and_Meta/Arrays.md#array-size_start) | Array   | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |

</details>


### Object: `SmokeBuff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| [`particle_lifetime`](../Reference_and_Meta/Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `speed_start` | Float | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`scripts`](../Reference_and_Meta/Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| [`size_start`](../Reference_and_Meta/Arrays.md#array-size_start) | Array   | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| `size_end` | Float | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| `speed_scale` | Float | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| `alpha_end` | Float | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| `alpha_start` | Float | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1`<br>`.5`<br>`.8` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local`<br>`local*/` |

</details>


### Object: `ShineBuff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `particle_lifetime` | Float | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `speed_start` | Float | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`scripts`](../Reference_and_Meta/Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| `size_start` | Float | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| `size_end` | Float | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| `speed_scale` | Float | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| `alpha_end` | Float | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| `alpha_start` | Float | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1`<br>`.5`<br>`.8` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local`<br>`local*/` |

</details>


### Object: `set_WitchJump`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `SandStormBuff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| [`particle_lifetime`](../Reference_and_Meta/Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `speed_start` | Float | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`scripts`](../Reference_and_Meta/Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| [`size_start`](../Reference_and_Meta/Arrays.md#array-size_start) | Array   | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| `size_end` | Float | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| `speed_scale` | Float | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| `alpha_end` | Float | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| `alpha_start` | Float | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1`<br>`.5`<br>`.8` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local`<br>`local*/` |

</details>


### Object: `NonChampionFlySwarm`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `MoonHead_KillHands`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `MegaFart`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `MechExplode`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }` |

</details>


### Object: `FlyBuff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| [`particle_lifetime`](../Reference_and_Meta/Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `speed_start` | Float | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`scripts`](../Reference_and_Meta/Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| [`size_start`](../Reference_and_Meta/Arrays.md#array-size_start) | Array   | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| `size_end` | Float | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| `speed_scale` | Float | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| `alpha_end` | Float | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| `alpha_start` | Float | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1`<br>`.5`<br>`.8` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local`<br>`local*/` |

</details>


### Object: `face_LeechBrood`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `face_EatNeverstone`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`bonus_passives`](../Reference_and_Meta/Miscellaneous.md#object-bonus_passives) | Object  | Grants temporary passive abilities to the caster for the duration of the ability. | 1 | `{ . . . }` |

</details>


### Object: `EatShit`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `DestroyerShieldBash`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `DarkOneStrike`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `cWaggle3x3`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `CraterCreeperOut`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |

</details>


### Object: `CharmedReaper`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |

</details>


### Object: `BonusToss2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `BoneWormShotMed`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |

</details>


### Object: `BasicMelee_4Hits`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `XIsTargetHealth`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 2 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


---


## Auto-Discovered Objects


### Object: `Windy`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 2 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`adventure_weather`](../Reference_and_Meta/Enums.md#enum-adventure_weather) | Enum   | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain`<br>`Snow`<br>`Thunderstorm` |
| `prewarm` | Number | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20`<br>`5` |
| [`skybox_frame`](../Reference_and_Meta/Enums.md#enum-skybox_frame) | Enum   | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain`<br>`day_snow`<br>`day_thunderstorm` |
| [`particles`](../Reference_and_Meta/Arrays.md#array-particles) | Array  | A list of particle system identifiers used to render the weather effects. | 1 | `[Rain]`<br>`[Snow]`<br>`[Thunderstorm]` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`hint_persistent_elements`](../Reference_and_Meta/Arrays.md#array-hint_persistent_elements) | Array   | A list of element types that remain persistent on the ground during this weather. | 1 | `[Fire]`<br>`[Heat]`<br>`[Holy]` |


### Object: `Wet`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Webbed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `WaggleClone`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`cWaggle`](./Engine_StatusAndPassiveKeys.md#object-cwaggle) | Boolean (Flag) / Object  | Defines a clone variant of the Waggle unit with its own graphics and properties. | 1 | `{ . . . }` |
| [`cWaggle2x2`](./Engine_StatusAndPassiveKeys.md#object-cwaggle2x2) | Boolean (Flag) / Object  | Defines a larger 2x2 tile clone variant of the Waggle unit. | 1 | `{ . . . }` |
| [`cWaggle3x3`](./Engine_StatusAndPassiveKeys.md#object-cwaggle3x3) | Boolean (Flag) / Object  | Defines an even larger 3x3 tile clone variant of the Waggle unit. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |


### Object: `VisualFlySwarm`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |


### Object: `VisualCountDownThenApplyStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |


### Object: `UseMoveAbilityWithAI`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |


### Object: `TwisterDisplaceWithDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 6 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `max_dist` | Integer | The maximum distance in tiles the target can be displaced by the knockback effect. | 6 | `2`<br>`20`<br>`3` |
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 2 | `2`<br>`3`<br>`4` |
| [`exclude_prefix`](../Reference_and_Meta/Enums.md#enum-exclude_prefix) | Enum   | Specifies a prefix string; units with a matching prefix in their ID are excluded from the displacement effect. | 1 | `Twister` |


### Object: `TransformWeapon`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`to`](../Reference_and_Meta/Enums.md#enum-to) | Enum | Specifies the target equipment item after transformation. | 2 | `JarOfNothing`<br>`Necro_SoulDagger_Charged`<br>`Necro_SoulDagger_Uncharged` |
| [`from`](../Reference_and_Meta/Enums.md#enum-from) | Enum | Specifies the source equipment item to be transformed. | 2 | `JarOfChaos`<br>`Necro_SoulDagger_Charged`<br>`Necro_SoulDagger_Uncharged` |


### Object: `TransformEquipment`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`to`](../Reference_and_Meta/Enums.md#enum-to) | Enum | Specifies the target equipment item after transformation. | 2 | `JarOfNothing`<br>`Necro_SoulDagger_Charged`<br>`Necro_SoulDagger_Uncharged` |
| [`from`](../Reference_and_Meta/Enums.md#enum-from) | Enum | Specifies the source equipment item to be transformed. | 2 | `JarOfChaos`<br>`Necro_SoulDagger_Charged`<br>`Necro_SoulDagger_Uncharged` |


### Object: `TrailBlazer`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TradeLife`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`bonus_passives`](../Reference_and_Meta/Miscellaneous.md#object-bonus_passives) | Object | Grants temporary passive abilities to the caster for the duration of the ability. | 1 | `{ . . . }` |


### Object: `TowerDefenseStatus2`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `TowerDefenseStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TimeDelayStatusApplication`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `delay` | Float | The delay in seconds before the ability's effect triggers. | 4 | `.05`<br>`.1`<br>`.25` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>tag |
| [`SwitchMusic`](./Engine_StatusAndPassiveKeys.md#object-switchmusic) | Object | Defines a new song or layer for the background music. | 2 | `{ . . . }` |
| [`FormChange`](./Engine_StatusAndPassiveKeys.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 1 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 1 | `{ . . . }`<br>`0`<br>`1` |
| `Vaporize` | Integer | Removes the target from play, preventing its corpse from being interacted with. | 1 | `1`<br>`20` |
| `FullHeal` | Integer | If non-zero, fully restores the target's health. | 1 | `0`<br>`1` |
| [`DoScreenShake`](./Engine_StatusAndPassiveKeys.md#object-doscreenshake) | Integer / Object | If an integer, the number of screen shakes; if an object, defines the duration and intensity of the screen shake. | 1 | `{ . . . }`<br>`1` |
| [`CreateGlobalModifiers`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-createglobalmodifiers) | Object  | Defines global gameplay modifiers to activate. | 1 | `{ . . . }` |
| `PlayBackground` | Integer | Specifies the background index to play. | 1 | `0`<br>`1` |
| [`GlobalSpawnCharacter`](../Reference_and_Meta/Enums.md#enum-globalspawncharacter) | Enum | Specifies the name of a character to spawn globally. | 1 | `MegaGuppy` |
| `RemoveAmbientLightEffects` | Float | The fade-out duration in seconds for ambient light effects. | 1 | `.5`<br>`4` |


### Object: `TilesMovedToStrength`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TilesMovedToNeighborHeal`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TilesMovedToMana`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TilesMovedToCritChance`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TempStrengthUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](../Reference_and_Meta/Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. | 1 | `AllStatsUp`<br>`Brace`<br>`Brittle` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `TempSpellDamageUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](../Reference_and_Meta/Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. | 1 | `AllStatsUp`<br>`Brace`<br>`Brittle` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `TempRangeUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `TempPreEmptiveCounterAttack`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TempPassiveUntilSettled`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>tag |
| [`MeleeRevengeDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-meleerevengedamage) | Object  | Defines the damage and effects applied back to a melee attacker upon being hit. | 2 | `{ . . . }` |
| `LimitHeal` | Integer | If 1, prevents the unit from being healed. | 1 | `0`<br>`1` |


### Object: `TemporaryItem`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `icon_frame` | Number | The sprite frame index for the buff icon. | 1 | `141`<br>`148`<br>`149` |


### Object: `Temporary`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 57 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 57 | `{ . . . }` |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 56 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 52 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `expires_on_begin_turn` | Boolean | If true, the temporary effect expires at the start of the target's turn. | 25 | `true` |
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 21 | `true` |
| `data` | Integer | An integer value used for custom data associated with the temporary effect. | 2 | `2` |
| `expires_on_appliers_turn` | Boolean | If true, the temporary effect expires at the start of the applier's next turn. | 2 | `true` |
| `expires_on_move` | Boolean | If true, the temporary effect expires when the target moves. | 1 | `true` |


### Object: `TempMovement`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](../Reference_and_Meta/Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. | 1 | `AllStatsUp`<br>`Brace`<br>`Brittle` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `TempManaCostReduction`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `TempInjuryImmunity`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Reference_and_Meta/Enums.md#enum-tooltip_stackless) | Enum   | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| [`tooltip_stacks_singular`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_singular) | String | The localization key for the singular form of the stack count in the tooltip. | 1 | `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |


### Object: `TempDamageUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](../Reference_and_Meta/Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. | 1 | `AllStatsUp`<br>`Brace`<br>`Brittle` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `TempCritChanceUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](../Reference_and_Meta/Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. | 1 | `AllStatsUp`<br>`Brace`<br>`Brittle` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `TempCounterAttack`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TempBonusKnockbackDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Reference_and_Meta/Enums.md#enum-tooltip_stackless) | Enum   | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `TempBonusKnockback`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Reference_and_Meta/Enums.md#enum-tooltip_stackless) | Enum   | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `TempBackstab`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `TeamCastAbility`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`tag_restriction`](../Reference_and_Meta/Enums.md#enum-tag_restriction) | Enum   | Specifies a tag that the target unit must have for the team cast to trigger. | 2 | `collective`<br>`dc_cat`<br>`dinofamily` |
| `same_orientation` | Boolean | If true, the team cast ability only triggers if the caster and target face the same direction. | 1 | `true` |


### Object: `Taunting`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Tarred`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `Tangled`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`alt_art`](../Reference_and_Meta/Enums.md#enum-alt_art) | Enum | Specifies an alternative art asset name to use for the status. | 1 | `TangledMeat` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `SwitchMusic`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`new_layer`](../Reference_and_Meta/Enums.md#enum-new_layer) | Enum | Specifies the music layer to switch to (e.g., 'event', 'battle', 'map'). | 7 | `battle`<br>`event`<br>`map` |
| [`new_song`](../Reference_and_Meta/Enums.md#enum-new_song) | Enum | Specifies the song to switch to; 'same' keeps the current song playing on the new layer. | 6 | `same` |
| `crossfade_speed` | Integer | The duration in seconds for the crossfade transition between music tracks. | 1 | `1` |


### Object: `Switcheroo`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `SwapWeapon`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 1 | `2`<br>`3`<br>`4` |


### Object: `Stun`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `StealthUntilBasicAttack`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `StatusCharactersOnRoundStart`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Else`](./Engine_StatusAndPassiveKeys.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| [`Madness`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Conditional_GoodRoll`](./Engine_StatusAndPassiveKeys.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |


### Object: `StatusCharactersOnRoundEnd`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>tag |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |
| [`Conditional_GoodRoll`](./Engine_StatusAndPassiveKeys.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ . . . }` |
| `FloatingRockTrap` | Integer | The number of stacks of Floating Rock Trap applied to the target, dealing damage when stepped on. | 1 | `1` |
| [`tag_filter`](../Reference_and_Meta/Enums.md#enum-tag_filter) | Enum | Specifies a tag (e.g., 'crow', 'rock', 'grub_familiar') used to filter which units a status or effect applies to. | 1 | `crow`<br>`grub_familiar`<br>`rock` |


### Object: `StatusAfterXStacks`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`threshold`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| [`stack_key`](../Reference_and_Meta/Enums.md#enum-stack_key) | Enum | Specifies the key of the status stack to check for the condition. | 2 | `CATHIDE`<br>`EMPTY_GENERATOR`<br>`FANNY_PACK` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 2 | `{ . . . }` |
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 1 | `true` |
| `RefreshActPoints` | Integer | The amount of action points restored to the source. | 1 | `1` |
| `ExtraBasicMoves_Status` | Integer | The number of extra basic moves per turn granted. | 1 | `1` |


### Object: `StatBounty`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `StacyMutant_Thorns`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |
| [`CatPartsTransform`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |


### Object: `StacyMutant_Speed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| `SizeScale` | Float | The multiplier applied to the unit's visual and hitbox size. | 1 | `.4`<br>`.6`<br>`.7` |
| `AddDamage` | Integer | The amount of damage added to all attacks. Negative values reduce damage. | 1 | `-1`<br>`1`<br>`2` |
| `AddSpeed` | Integer | The amount of speed added (or subtracted) to the unit. | 1 | `-3`<br>`4`<br>`6` |


### Object: `StacyMutant_Mirror`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| [`ReflectProjectiles`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-reflectprojectiles) | Integer / Object  | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 1 | `{ . . . }`<br>`1`<br>`10%`<br>`100%` |
| [`StatusEachTurnEndForEachTurn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnendforeachturn) | Object  | Statuses applied at the end of each turn, with the number of turns as nested values. | 1 | `{ . . . }` |


### Object: `StacyMutant_Lightning`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| [`ElementImmune`](../Reference_and_Meta/Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 1 | `Creep`<br>`Electric`<br>`Fire` |
| [`ReplaceBasicAttack`](../Reference_and_Meta/Enums.md#enum-replacebasicattack) | Enum  | Specifies the ability ID that replaces the unit's basic attack. | 1 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`ReplaceBrain`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-replacebrain) | Object  | Defines a replacement AI brain and behavior pattern for the mutant. | 1 | `{ . . . }` |


### Object: `StacyMutant_Ice`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| [`ElementImmune`](../Reference_and_Meta/Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 1 | `Creep`<br>`Electric`<br>`Fire` |
| `AddMovement` | Integer | The amount of bonus movement points added to the unit's base movement. | 1 | `-1`<br>`-2`<br>`1` |
| [`ReplaceBasicAttack`](../Reference_and_Meta/Enums.md#enum-replacebasicattack) | Enum  | Specifies the ability ID that replaces the unit's basic attack. | 1 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`ReplaceBrain`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-replacebrain) | Object  | Defines a replacement AI brain and behavior pattern for the mutant. | 1 | `{ . . . }` |


### Object: `StacyMutant_Holy`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |


### Object: `StacyMutant_Health`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| `SizeScale` | Float | The multiplier applied to the unit's visual and hitbox size. | 1 | `.4`<br>`.6`<br>`.7` |
| `AddMaxHealth` | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 1 | `-25`<br>`10`<br>`2` |
| `AddSpeed` | Integer | The amount of speed added (or subtracted) to the unit. | 1 | `-3`<br>`4`<br>`6` |


### Object: `StacyMutant_Fire`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| [`ElementImmune`](../Reference_and_Meta/Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 1 | `Creep`<br>`Electric`<br>`Fire` |
| [`ReplaceBasicAttack`](../Reference_and_Meta/Enums.md#enum-replacebasicattack) | Enum  | Specifies the ability ID that replaces the unit's basic attack. | 1 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`ReplaceBrain`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-replacebrain) | Object  | Defines a replacement AI brain and behavior pattern for the mutant. | 1 | `{ . . . }` |


### Object: `StacyMutant_DoubleHead`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| `ExtraDispersedTurns` | Integer | The number of additional or fewer turns in the dispersed turn order. | 1 | `-1`<br>`1` |


### Object: `StacyMutant_Damage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| `AddMaxHealth` | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 1 | `-25`<br>`10`<br>`2` |
| `AddDamage` | Integer | The amount of damage added to all attacks. Negative values reduce damage. | 1 | `-1`<br>`1`<br>`2` |


### Object: `StacyMutant_Counter`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 1 | `{ . . . }` |
| [`CatPartsTransform`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| [`CounterAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-counterattack) | Array / Enum / Object  | Specifies the ability used when the unit counterattacks after being hit. | 1 | `{ . . . }`<br>`BungaSwipe`<br>`CloakerHex`<br>`CollectiveCounter` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |


### Object: `StacyMutant_Brace`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`CatPartsTransform`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |


### Object: `SpreadDisease`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`disease`](../Reference_and_Meta/Enums.md#enum-disease) | Enum  | Determines which disease is applied when spreading disease. | 13 | `BirdFlu`<br>`Cancer`<br>`CommonCold` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 12 | `.02`<br>`.1`<br>`.15` |
| `can_apply_to_anything` | Boolean | If true, this disease can be spread to any unit, regardless of type. | 6 | `true` |


### Object: `SpiderInfested`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `SpellShield`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `SpeedUp_WithoutInitiative`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](../Reference_and_Meta/Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. | 1 | `AllStatsUp`<br>`Brace`<br>`Brittle` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `SpecialGodRays`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Big`](../Reference_and_Meta/Miscellaneous.md#object-big) | Object | Defines the 'Big' form, including its animation, attack, passives, and positional data. | 2 | `{ . . . }` |


### Object: `SpawnVolcanoOnBattleStart`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 3 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `max_radius` | Float | The maximum radius of the spawned puddle or volcano in tiles. | 2 | `2.2`<br>`3.5` |
| `min_radius` | Float / String | The minimum radius of the spawned puddle or volcano in tiles. | 2 | `.2`<br>`1`<br>`1.5` |
| [`puddle_tile`](../Reference_and_Meta/Arrays.md#array-puddle_tile) | Array / Enum | An array specifying the tile types to use for the puddle or volcano. | 2 | `LavaTile`<br>`[BrambleTile TallBrambleTile]` |
| [`number`](../Reference_and_Meta/Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 1 | `1`<br>`10`<br>`2` |


### Object: `SpawnTilePuddleOnBattleStart`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tile`](../Reference_and_Meta/Arrays.md#array-tile) | Array / Enum  | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 1 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |
| `max_radius` | Float | The maximum radius of the spawned puddle or volcano in tiles. | 1 | `2.2`<br>`3.5` |
| `min_radius` | Float | The minimum radius of the spawned puddle or volcano in tiles. | 1 | `.2`<br>`1`<br>`1.5` |


### Object: `SoulLink`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `SolarFlare`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2 | `{ . . . }` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 1 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array  | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 | `[`<br>`[Heat Fire]` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |


### Object: `Snow`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 2 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`adventure_weather`](../Reference_and_Meta/Enums.md#enum-adventure_weather) | Enum   | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain`<br>`Snow`<br>`Thunderstorm` |
| `prewarm` | Number | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20`<br>`5` |
| [`skybox_frame`](../Reference_and_Meta/Enums.md#enum-skybox_frame) | Enum   | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain`<br>`day_snow`<br>`day_thunderstorm` |
| [`particles`](../Reference_and_Meta/Arrays.md#array-particles) | Array  | A list of particle system identifiers used to render the weather effects. | 1 | `[Rain]`<br>`[Snow]`<br>`[Thunderstorm]` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`render_mode`](../Reference_and_Meta/Enums.md#enum-render_mode) | Enum   | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `particle_lifetime` | Float | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| [`simulation_space`](../Reference_and_Meta/Enums.md#enum-simulation_space) | Enum   | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| [`projection_matrix`](../Reference_and_Meta/Enums.md#enum-projection_matrix) | Enum   | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| [`speed_start`](../Reference_and_Meta/Arrays.md#array-speed_start) | Array   | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`scripts`](../Reference_and_Meta/Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| [`size_start`](../Reference_and_Meta/Arrays.md#array-size_start) | Array   | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| `size_end` | Float | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| [`rotation`](../Reference_and_Meta/Arrays.md#array-rotation) | Array | The rotation of the effect, specified as a single value or a random range [min, max] in degrees. | 1 | `-90`<br>`90`<br>`[-10 10]` |
| `alpha` | String | The alpha transparency value for the particle system (e.g., '0.03'). | 1 | `.005`<br>`.01`<br>`.03` |
| [`combo`](../Reference_and_Meta/Arrays.md#array-combo) | Array  | A list of particle effect names that are spawned together in sequence. | 1 | `[BloodPoof BloodBounce]`<br>`[BloodPoofCrit BloodBounceCrit BloodPopCrit]`<br>`[BloodPoof_Absorb BloodBounce_Absorb]` |
| `rotation_speed_end` | Number | The rotation speed (in degrees per second) of the effect at the end of its animation. | 1 | `0` |
| [`rotation_speed`](../Reference_and_Meta/Arrays.md#array-rotation_speed) | Array | The minimum and maximum rotation speed for a particle or visual effect. | 1 | `[-10, 10]`<br>`[-100 100]`<br>`[-100, 100]` |
| [`hint_persistent_elements`](../Reference_and_Meta/Arrays.md#array-hint_persistent_elements) | Array   | A list of element types that remain persistent on the ground during this weather. | 1 | `[Fire]`<br>`[Heat]`<br>`[Holy]` |


### Object: `SmellBlood`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |


### Object: `SmartMetronome`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 1 | `true` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`tags`](../Reference_and_Meta/Arrays.md#array-tags) | Array / Enum  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |


### Object: `Sleep`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `ShortCircuit`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Shield`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |


### Object: `Shatter`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |


### Object: `SetItemAux`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `value` | Enum | The numeric value or formula associated with the buff. | 3 | `.5`<br>`0`<br>`1` |
| [`slot`](../Reference_and_Meta/Enums.md#enum-slot) | Enum / Integer  | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 3 | `0`<br>`1`<br>`2` |


### Object: `SetCrazyEyeBackgroundWeights`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](../Reference_and_Meta/Arrays.md#array-weights) | Array / Enum  | Specifies the weight array or named preset for the crazy eye background AI. | 3 | `[0 0 1]`<br>`[0 1 0]`<br>`[1 0 0]` |


### Object: `SetAnimationAlts`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dying`](../Reference_and_Meta/Enums.md#enum-dying) | Enum  | Determines the animation set used when the unit is in a dying state. | 1 | `shot` |
| [`dead`](../Reference_and_Meta/Enums.md#enum-dead) | Enum  | Determines the animation set used when the unit is dead. | 1 | `deadShot` |


### Object: `SerratedClaws`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `ScrambleLastUsedSpell`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `permanent` | Boolean | If true, the scrambled spell selection persists permanently rather than resetting after use. | 1 | `true` |


### Object: `Scrambled`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `ScatterCoins`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `stackable` | Boolean | If true, the scatter coins effect can stack with multiple applications. | 2 | `true` |


### Object: `Sandstorm`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |


### Object: `Rot`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `ReviveNextRound`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `revive_health` | Integer | The amount of health (as a flat integer or percentage) the unit revives with. | 4 | `1`<br>`100%`<br>`50%` |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 3 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 2 | `{ . . . }` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| [`tooltip_stacks_singular`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_singular) | String | The localization key for the singular form of the stack count in the tooltip. | 1 | `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |


### Object: `Revive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |


### Object: `RepressedMemoriesMetronome`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 2 | `2`<br>`3`<br>`4` |


### Object: `ReplaceSpell`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`slot`](../Reference_and_Meta/Enums.md#enum-slot) | Enum / Integer  | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 4 | `0`<br>`1`<br>`2` |


### Object: `RemoveStatusStacks`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 4 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | passives<br>class<br>tag |


### Object: `Regurge`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spawn`](../Reference_and_Meta/Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. | 2 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |


### Object: `Reflect`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| [`tooltip_stacks_singular`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_singular) | String | The localization key for the singular form of the stack count in the tooltip. | 1 | `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |


### Object: `ReduceManaCostExcludeBrainstorm`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `Reanimate`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |


### Object: `RangeUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `RandomPermanentStatsDistinct`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |


### Object: `RandomMagicMissile`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `full_size` | Boolean | If true, the magic missile uses its full size instead of a reduced size. | 2 | `true` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `icon_frame` | Number | The sprite frame index for the buff icon. | 1 | `141`<br>`148`<br>`149` |


### Object: `RandomKnockback`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 2 | `10`<br>`2`<br>`25` |
| `min` | Integer | The minimum amount of coins that will be gained. | 2 | `0`<br>`1`<br>`10` |


### Object: `RandomInjury`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `icon_frame` | Number | The sprite frame index for the buff icon. | 1 | `141`<br>`148`<br>`149` |


### Object: `RandomDistanceDisplace`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 1 | `2`<br>`3`<br>`4` |


### Object: `QuakeAreaChance`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |
| [`radius`](../Reference_and_Meta/Arrays.md#array-radius) | Array / Integer | The range in tiles of the distortion ring effect; an array [min, max] specifies a random radius within that range. | 2 | `0`<br>`1`<br>`13` |


### Object: `Purge`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |


### Object: `ProbeCharmed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |


### Object: `PreEmptiveCounterNextAttacks`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| [`tooltip_stacks_singular`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_singular) | String | The localization key for the singular form of the stack count in the tooltip. | 1 | `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |


### Object: `Possessed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| [`tooltip_stacks_singular`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_singular) | String | The localization key for the singular form of the stack count in the tooltip. | 1 | `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |


### Object: `PoolMetronome`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 1 | `2`<br>`3`<br>`4` |


### Object: `PoisonLace`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `Petrify`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| [`tooltip_stacks_singular`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_singular) | String | The localization key for the singular form of the stack count in the tooltip. | 1 | `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |


### Object: `PermanentConfusion`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `PassiveWhileNotTakingTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |


### Object: `OverHealToStatuses`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 1 | `1` |
| `stack_scale` | Integer | The scaling factor for how many stacks of the over-heal status are applied. | 1 | `0` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |


### Object: `Ostracized`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `OneUseSpellDamageUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](../Reference_and_Meta/Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. | 1 | `AllStatsUp`<br>`Brace`<br>`Brittle` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `ObjectOnHitCharacter`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 7 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | passives<br>class<br>tag |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 5 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |


### Object: `ObjectOnHit`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |


### Object: `NukeQuestFinalBossModifications`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 2 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`splash_damage`](../Reference_and_Meta/Miscellaneous.md#object-splash_damage) | Object  | Defines additional damage or effects applied to nearby targets around the primary target. | 1 | `{ . . . }` |


### Object: `NoHealthRegen`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `NextTurnDoubleRangedDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `NextDamageReduceAndHealAllies`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `NextBattleStatusStacks`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MadnessChanceOnTurnBegin` | Integer | The chance (as a multiplier) to inflict Madness status at the start of each turn in the next battle. | 1 | `2` |
| `fights` | Integer | The number of future battles the status effect will be applied at the start of. | 1 | `1`<br>`9999` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |


### Object: `NextBattleStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| `FullHeal` | Integer | If non-zero, fully restores the target's health. | 2 | `0`<br>`1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `NextBasicAttackCritsThisTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `cant_miss` | Boolean | If true, the damage instance always hits its target regardless of accuracy or evasion. | 1 | `true` |
| `piercing` | Boolean | If true, the damage instance ignores armor or damage reduction effects on the target. | 1 | `true` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |


### Object: `NextAttackSpecialCrit`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Integer | The additional critical hit damage multiplier. | 1 | `2` |
| `extra_coins_per_stack` | Integer | The number of extra coins gained per stack of the associated status. | 1 | `2` |
| `luck_increase` | Integer | The flat increase to the unit's luck stat. | 1 | `1` |


### Object: `NextAttackBonusRange`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `NextActionLuckUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](../Reference_and_Meta/Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. | 1 | `AllStatsUp`<br>`Brace`<br>`Brittle` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `NextAbilityHeals`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Muted`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| [`tooltip_stacks_singular`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_singular) | String | The localization key for the singular form of the stack count in the tooltip. | 1 | `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |


### Object: `MovementUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stacks_neg`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_neg) | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. | 1 | `"KEYWORD_ALLSTATSDOWN_DESC"`<br>`"KEYWORD_CHADOWN_DESC"`<br>`"KEYWORD_CONDOWN_DESC"` |
| [`name_stacks_neg`](../Assets_and_Localization/Strings.md#string-name_stacks_neg) | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. | 1 | `"KEYWORD_ALLSTATSDOWN_NAME"`<br>`"KEYWORD_CHADOWN_NAME"`<br>`"KEYWORD_CONDOWN_NAME"` |
| [`tooltip_stacks_pos`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_pos) | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. | 1 | `"KEYWORD_ALLSTATSUP_DESC"`<br>`"KEYWORD_CHAUP_DESC"`<br>`"KEYWORD_CONUP_DESC"` |
| [`tooltip_stackless_neg`](../Assets_and_Localization/Strings.md#string-tooltip_stackless_neg) | String | Localization key for the tooltip of the negative variant when not showing stack count. | 1 | `"KEYWORD_DAMAGEDOWN_DESC_STACKLESS"`<br>`"KEYWORD_MOVEMENTDOWN_DESC_STACKLESS"`<br>`"KEYWORD_TEMPINITDOWN_DESC"` |
| [`tooltip_stackless_pos`](../Assets_and_Localization/Strings.md#string-tooltip_stackless_pos) | String | Localization key for the tooltip of the positive variant when not showing stack count. | 1 | `"KEYWORD_DAMAGEUP_DESC_STACKLESS"`<br>`"KEYWORD_MOVEMENTUP_DESC_STACKLESS"` |


### Object: `ModifyAbility`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 2 | `{ . . . }` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 2 | `{ . . . }` |


### Object: `Metronome`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`banned_abilities`](../Reference_and_Meta/Arrays.md#array-banned_abilities) | Array   | A list of ability IDs that are excluded from random selection or usage in the Metronome effect. | 1 | `[BatteryNuke WeAreOne Metronome SmartMetronome BecomeEntropy ForbiddenFamine]` (Array) |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| `frame` | Integer | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| [`kind`](../Reference_and_Meta/Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| [`set`](../Reference_and_Meta/Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| [`rarity`](../Reference_and_Meta/Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. | 1 | `common`<br>`consumable_common`<br>`consumable_rare` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`tags`](../Reference_and_Meta/Arrays.md#array-tags) | Array / Enum  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |


### Object: `MeteorShower`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |


### Object: `Meteornado`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`render_mode`](../Reference_and_Meta/Enums.md#enum-render_mode) | Enum   | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| [`particle_lifetime`](../Reference_and_Meta/Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| [`simulation_space`](../Reference_and_Meta/Enums.md#enum-simulation_space) | Enum   | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| [`projection_matrix`](../Reference_and_Meta/Enums.md#enum-projection_matrix) | Enum   | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `speed_start` | Float | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`scripts`](../Reference_and_Meta/Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| [`size_start`](../Reference_and_Meta/Arrays.md#array-size_start) | Array   | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`rotation`](../Reference_and_Meta/Arrays.md#array-rotation) | Array | The rotation of the effect, specified as a single value or a random range [min, max] in degrees. | 1 | `-90`<br>`90`<br>`[-10 10]` |
| `alpha_out` | String | The alpha (opacity) value at the end of the effect's outro animation. | 1 | `.2`<br>`.3`<br>`.5` |
| `alpha_in` | String | The alpha (opacity) value at the start of the effect's intro animation. | 1 | `.01`<br>`.05`<br>`.1` |
| [`rotation_speed`](../Reference_and_Meta/Arrays.md#array-rotation_speed) | Array | The minimum and maximum rotation speed for a particle or visual effect. | 1 | `[-10, 10]`<br>`[-100 100]`<br>`[-100, 100]` |


### Object: `MergeDamageInstance`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `can_instapop` | Boolean | If false, the ability cannot instantly kill or remove the target, often used for non-lethal effects. | 1 | `false` |
| `force_no_hit_animation` | Boolean | If true, suppresses the hit animation when merging damage instances. | 1 | `true` |


### Object: `Meaty`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Math`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 2 | `{ . . . }` |
| [`ApplyToSource`](./Engine_StatusAndPassiveKeys.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 1 | `{ . . . }` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |


### Object: `Marked`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `ManaLeeches`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| [`name_reference_applier`](../Assets_and_Localization/Strings.md#string-name_reference_applier) | String | A localization key for the name displayed to the applier of this status effect. | 1 | `"KEYWORD_ATTRACTION_REF"`<br>`"KEYWORD_LEECHES_NAME_APPLIER"`<br>`"KEYWORD_MANALEECHES_NAME_APPLIER"` |
| [`tooltip_reference_applier`](../Assets_and_Localization/Strings.md#string-tooltip_reference_applier) | String | A localization key for the tooltip description displayed to the applier of this status effect. | 1 | `"KEYWORD_ATTRACTION_DESC_REF"`<br>`"KEYWORD_LEECHES_DESC_APPLIER"`<br>`"KEYWORD_MANALEECHES_DESC_APPLIER"` |


### Object: `ManaGainRange`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 1 | `10`<br>`2`<br>`25` |
| `min` | Integer | The minimum amount of coins that will be gained. | 1 | `0`<br>`1`<br>`10` |


### Object: `MagicWeakness`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Leeches`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| [`name_reference_applier`](../Assets_and_Localization/Strings.md#string-name_reference_applier) | String | A localization key for the name displayed to the applier of this status effect. | 1 | `"KEYWORD_ATTRACTION_REF"`<br>`"KEYWORD_LEECHES_NAME_APPLIER"`<br>`"KEYWORD_MANALEECHES_NAME_APPLIER"` |
| [`tooltip_reference_applier`](../Assets_and_Localization/Strings.md#string-tooltip_reference_applier) | String | A localization key for the tooltip description displayed to the applier of this status effect. | 1 | `"KEYWORD_ATTRACTION_DESC_REF"`<br>`"KEYWORD_LEECHES_DESC_APPLIER"`<br>`"KEYWORD_MANALEECHES_DESC_APPLIER"` |


### Object: `Leech`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |
| `icon_frame` | Number | The sprite frame index for the buff icon. | 1 | `141`<br>`148`<br>`149` |


### Object: `LeaveBehind`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 4 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |


### Object: `LateStatusApplication`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CurrentWeaponDamageUp` | Integer | The amount of temporary damage increase to the current weapon. | 3 | `1`<br>`3`<br>`5` |
| `AddWeaponAux` | Equation | The amount or expression to add to the source's weapon auxiliary stat. | 1 | `"-max(min(X+1, item_aux), 0)"`<br>`-item_aux`<br>`1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `KnockUpAndAway`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 24 | `-3`<br>`10`<br>`2` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 22 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 2 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| `height` | Integer | The height in tiles the target is launched into the air. | 2 | `0`<br>`1`<br>`2` |
| `displace` | Boolean | If true, the knockback also displaces the target to a different tile. | 2 | `true` |
| `circular_variance` | Integer | The random variance in the knockback direction, in tiles. | 1 | `2` |


### Object: `KnockOutCoin`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |


### Object: `KnockbackIfCrit`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`knockback`](../Reference_and_Meta/Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 1 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| `override_chain_knockback` | Integer | The distance in tiles the unit is knocked back if a critical hit triggers chain knockback. | 1 | `10` |


### Object: `Knockback`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `KillEnemyOfTypeAtBattleStart`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`enemy_type`](../Reference_and_Meta/Enums.md#enum-enemy_type) | Enum | Specifies the type of enemy to kill at the start of battle. | 2 | `any`<br>`cat` |
| [`fallback_spawn`](../Reference_and_Meta/Arrays.md#array-fallback_spawn) | Array | An array of enemy names to spawn as a fallback if no matching enemy type is present. | 1 | `[TomTom Kitten CatCaller Mangy]` |


### Object: `JudgementDay`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |


### Object: `Invulnerable`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `IntelligenceUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Reference_and_Meta/Enums.md#enum-tooltip_stackless) | Enum   | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks_neg`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_neg) | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. | 1 | `"KEYWORD_ALLSTATSDOWN_DESC"`<br>`"KEYWORD_CHADOWN_DESC"`<br>`"KEYWORD_CONDOWN_DESC"` |
| [`name_stacks_neg`](../Assets_and_Localization/Strings.md#string-name_stacks_neg) | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. | 1 | `"KEYWORD_ALLSTATSDOWN_NAME"`<br>`"KEYWORD_CHADOWN_NAME"`<br>`"KEYWORD_CONDOWN_NAME"` |
| [`tooltip_stacks_pos`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_pos) | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. | 1 | `"KEYWORD_ALLSTATSUP_DESC"`<br>`"KEYWORD_CHAUP_DESC"`<br>`"KEYWORD_CONUP_DESC"` |


### Object: `Infested`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`class`](../Reference_and_Meta/Enums.md#enum-class) | Enum  | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| `value` | Enum | The numeric value or formula associated with the buff. | 1 | `.5`<br>`0`<br>`1` |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 1 | `-1`<br>`-2`<br>`1` |
| [`palette`](../Reference_and_Meta/Enums.md#enum-palette) | Enum / Integer  | Specifies the color palette index for the ability's visuals. | 1 | `-1`<br>`0`<br>`1` |
| `texture` | Integer | The catalog ID for the cat's texture. | 1 | `-1`<br>`1`<br>`1000` |
| `default_frame` | Number | The default sprite frame used for the character's portrait or body. | 1 | `1`<br>`1000`<br>`1001` |
| `righteye` | Number | The sprite frame index for the character's right eye. | 1 | `1`<br>`100`<br>`1001` |
| [`voice`](../Reference_and_Meta/Enums.md#enum-voice) | Enum  | Determines which voice set or type is used for the character. | 1 | `ankylosaurus`<br>`female1`<br>`female10` |
| `lefteye` | Number | The sprite frame index for the character's left eye. | 1 | `1`<br>`100`<br>`1001` |
| `righteyebrow` | Number | The sprite frame index for the character's right eyebrow. | 1 | `1`<br>`1000`<br>`1001` |
| `lefteyebrow` | Number | The sprite frame index for the character's left eyebrow. | 1 | `1`<br>`1000`<br>`1001` |
| `pitch` | String | The sound pitch multiplier for the character's voice or sounds. | 1 | `.3`<br>`.5`<br>`.6` |
| `icon_frame` | Number | The sprite frame index for the buff icon. | 1 | `141`<br>`148`<br>`149` |


### Object: `IncAuxCounterCycle`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 1 | `10`<br>`2`<br>`25` |
| `change` | Integer | The amount to adjust the auxiliary counter by. | 1 | `-1`<br>`-2`<br>`-3` |


### Object: `IncAuxCounterClamped`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 3 | `10`<br>`2`<br>`25` |
| `change` | Integer | The amount to adjust the auxiliary counter by. | 3 | `-1`<br>`-2`<br>`-3` |


### Object: `ImmediateUseAbility`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 1 | `true` |


### Object: `IceArmor`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`class`](../Reference_and_Meta/Enums.md#enum-class) | Enum  | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `HolyDamageBlessing`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Burn`](../Reference_and_Meta/Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 2 | `1`<br>`10`<br>`2` |
| `damage_multiplier` | Number | A multiplier for holy damage dealt. | 2 | `2`<br>`3` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `Hex`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `HeavyHits`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Reference_and_Meta/Enums.md#enum-tooltip_stackless) | Enum   | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `HeatWave`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`combo`](../Reference_and_Meta/Arrays.md#array-combo) | Array  | A list of particle effect names that are spawned together in sequence. | 1 | `[BloodPoof BloodBounce]`<br>`[BloodPoofCrit BloodBounceCrit BloodPopCrit]`<br>`[BloodPoof_Absorb BloodBounce_Absorb]` |
| [`hint_persistent_elements`](../Reference_and_Meta/Arrays.md#array-hint_persistent_elements) | Array   | A list of element types that remain persistent on the ground during this weather. | 1 | `[Fire]`<br>`[Heat]`<br>`[Holy]` |


### Object: `HealAlliesEachTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mana` | Equation | The amount of mana required to cast, as a formula or stat. | 2 | `"4-clamp(floor(X/7), 0, 1)"`<br>`"max(4-X, 0)"`<br>`"max(7-2*X,0)"` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `exclude_self` | Boolean | If true, the effect does not apply to the source unit itself. | 2 | `false` |


### Object: `Grappling`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](../Reference_and_Meta/Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 1 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`exit_animations`](../Reference_and_Meta/Miscellaneous.md#object-exit_animations) | Object | An object mapping exit conditions to their corresponding animation names. | 1 | `{ . . . }` |


### Object: `Grappled`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `GlobalSpawnOnRoundEnd`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](../Reference_and_Meta/Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 1 | `1`<br>`10`<br>`2` |


### Object: `GainDisorderFromPool`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 1 | `2`<br>`3`<br>`4` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |


### Object: `GainCoinsRange`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 11 | `10`<br>`2`<br>`25` |
| `min` | Integer | The minimum amount of coins that will be gained. | 11 | `0`<br>`1`<br>`10` |


### Object: `Freeze`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `FormChange`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form`](../Reference_and_Meta/Enums.md#enum-form) | Enum / Integer  | Specifies the name of the form the unit changes into. | 75 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |


### Object: `ForceUseAbilityOnTarget`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |


### Object: `ForceMoveTowardsTaggedObject`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |


### Object: `ForceImmediateMoveAndAttack`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_cant_reach` | Boolean | If true, forces the unit to attempt to move and attack even if the target is not reachable. | 1 | `true` |


### Object: `ForceAttack`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 2 | `false`<br>`true` |


### Object: `Fog`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`render_mode`](../Reference_and_Meta/Enums.md#enum-render_mode) | Enum   | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| [`particle_lifetime`](../Reference_and_Meta/Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| [`simulation_space`](../Reference_and_Meta/Enums.md#enum-simulation_space) | Enum   | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| [`projection_matrix`](../Reference_and_Meta/Enums.md#enum-projection_matrix) | Enum   | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| [`friction`](../Reference_and_Meta/Arrays.md#array-friction) | Array  | A scalar or 3D vector multiplier for velocity reduction applied over time. | 1 | `.1`<br>`.2`<br>`.5` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `speed_start` | String | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`scripts`](../Reference_and_Meta/Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| [`size_start`](../Reference_and_Meta/Arrays.md#array-size_start) | Array   | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| `alpha_end` | Float | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| `alpha_start` | Float | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1`<br>`.5`<br>`.8` |


### Object: `FlySwarm`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`properties`](../Reference_and_Meta/Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| [`abilities`](../Reference_and_Meta/Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`ai`](../Reference_and_Meta/Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |


### Object: `FireStorm`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`combo`](../Reference_and_Meta/Arrays.md#array-combo) | Array  | A list of particle effect names that are spawned together in sequence. | 1 | `[BloodPoof BloodBounce]`<br>`[BloodPoofCrit BloodBounceCrit BloodPopCrit]`<br>`[BloodPoof_Absorb BloodBounce_Absorb]` |


### Object: `FireflySwarm`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |


### Object: `FireArmor2`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `FireArmor`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 2 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`class`](../Reference_and_Meta/Enums.md#enum-class) | Enum  | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Fear`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `FactionUprising`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`extra_statuses`](../Reference_and_Meta/Miscellaneous.md#object-extra_statuses) | Object | An object containing additional status effects (with stack counts) applied to the consumed unit. | 1 | `{ . . . }` |


### Object: `Enlarge`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |


### Object: `EmptyMind`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Else`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 17 | `{ . . . }` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 6 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`FormChange`](./Engine_StatusAndPassiveKeys.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 2 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| [`Confusion`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 2 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 2 | `{ . . . }`<br>`0`<br>`1` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Marked`](./Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 2 | `{ . . . }`<br>`1`<br>`3`<br>`5` |
| [`Revive`](./Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object  | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | `{ . . . }`<br>`1`<br>`100%`<br>`50%` |
| [`RandomStatDown`](../Reference_and_Meta/Arrays.md#array-randomstatdown) | Array / Integer / String  | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`1` |
| [`GainCoinsRange`](./Engine_StatusAndPassiveKeys.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 2 | `{ . . . }` |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 2 | `1` |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`Bruise`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| [`Slow`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 1 | `{ . . . }`<br>`-1`<br>`1`<br>`2` |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 1 | `1`<br>`10`<br>`100` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |
| [`Immobile`](../Reference_and_Meta/Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | `0`<br>`1`<br>`10%` |
| [`ConstitutionUp`](../Reference_and_Meta/Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| [`ObjectOnHitCharacter`](./Engine_StatusAndPassiveKeys.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 1 | `1`<br>`10`<br>`100` |
| [`Leeches`](./Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object  | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Cleave`](./Engine_StatusAndPassiveKeys.md#object-cleave) | Integer / Object  | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 1 | `{ . . . }`<br>`1` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .1]` |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 1 | `25`<br>`50`<br>`999` |
| [`ImmediateUseAbility`](./Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 1 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. | 1 | `1`<br>`9999` |
| `TempSpeedUp` | Enum / Integer | The number of stacks of temporary Speed Up applied to the unit. | 1 | `10`<br>`4`<br>`X` |
| [`ScatterCoins`](./Engine_StatusAndPassiveKeys.md#object-scattercoins) | Object  | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 1 | `{ . . . }` |
| [`DybbukPossessed`](../Reference_and_Meta/Miscellaneous.md#object-dybbukpossessed) | Object  | Contains parameters for the Dybbuk possession status, specifying exit ability and self-punch ability. | 1 | `{ . . . }` |
| [`AllyInfested`](../Reference_and_Meta/Miscellaneous.md#object-allyinfested) | Array / Float / Object  | Defines the AllyInfested object, which spawns an infested ally under the player's control. | 1 | `{ . . . }` |


### Object: `EliteUpgradeNextMinion`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `DustOnHit`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 3 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |


### Object: `Drowsy`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Drag`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`class`](../Reference_and_Meta/Enums.md#enum-class) | Enum  | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |


### Object: `DoubleLoot`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |


### Object: `DoubleCastSpellThisTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `DoubleCastSpell`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `DoubleCast`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `DoScreenShake`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `intensity` | Integer | The strength of the screen shake effect; positive values shake more, negative values may invert direction. | 10 | `-1`<br>`-2`<br>`1` |
| `time` | Float | The duration in seconds of the screen shake effect. | 10 | `.5`<br>`.75`<br>`1` |


### Object: `DoDistortionRing`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`speed`](../Reference_and_Meta/Arrays.md#array-speed) | Array / Float  | The speed of the projectile or move, can be a value or a range. | 6 | `-30`<br>`-4`<br>`.5` |
| `intensity` | Integer | The strength of the screen shake effect; positive values shake more, negative values may invert direction. | 6 | `-1`<br>`-2`<br>`1` |
| [`radius`](../Reference_and_Meta/Arrays.md#array-radius) | Array / Integer | The range in tiles of the distortion ring effect; an array [min, max] specifies a random radius within that range. | 6 | `0`<br>`1`<br>`13` |


### Object: `DoDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 7 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum  | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 7 | `[attack move spell]`<br>`attack`<br>`battle` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | passives<br>class<br>tag |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 4 | `{ . . . }` |
| [`damage_tiles`](../Reference_and_Meta/Enums.md#enum-damage_tiles) | Enum   | Specifies whether the damage effect applies to tiles; 'all' damages every tile in the area. | 4 | `all` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array  | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 2 | `[`<br>`[Heat Fire]` |


### Object: `DistanceBonusDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `min_range` | Integer | The minimum range of the ability. | 4 | `0`<br>`1`<br>`2` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `DiminishingHealthRegen`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `DexterityUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Reference_and_Meta/Enums.md#enum-tooltip_stackless) | Enum   | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks_neg`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_neg) | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. | 1 | `"KEYWORD_ALLSTATSDOWN_DESC"`<br>`"KEYWORD_CHADOWN_DESC"`<br>`"KEYWORD_CONDOWN_DESC"` |
| [`name_stacks_neg`](../Assets_and_Localization/Strings.md#string-name_stacks_neg) | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. | 1 | `"KEYWORD_ALLSTATSDOWN_NAME"`<br>`"KEYWORD_CHADOWN_NAME"`<br>`"KEYWORD_CONDOWN_NAME"` |
| [`tooltip_stacks_pos`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_pos) | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. | 1 | `"KEYWORD_ALLSTATSUP_DESC"`<br>`"KEYWORD_CHAUP_DESC"`<br>`"KEYWORD_CONUP_DESC"` |


### Object: `DestroyEquipmentAndAttachParasite`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 6 | `2`<br>`3`<br>`4` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 4 | `.02`<br>`.1`<br>`.15` |


### Object: `DelayedWindCone`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 2 | `-3`<br>`10`<br>`2` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 1 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |


### Object: `DelayedWind`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 1 | `-3`<br>`10`<br>`2` |


### Object: `DelayedPain`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `DelayCastAbility`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `lingering` | Boolean | If true, the ability effect lingers after the initial cast. | 1 | `true` |
| `relative` | Boolean | If true, the delay is calculated relative to the current turn count rather than as an absolute time. | 1 | `false` |


### Object: `CurrentWeaponAddPoison`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `CureDisease`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 6 | `.02`<br>`.1`<br>`.15` |
| [`disease`](../Reference_and_Meta/Enums.md#enum-disease) | Enum  | Determines which disease is applied when spreading disease. | 6 | `BirdFlu`<br>`Cancer`<br>`CommonCold` |
| `can_apply_to_anything` | Boolean | If true, this disease can be spread to any unit, regardless of type. | 1 | `true` |


### Object: `Craft`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 15 | `2`<br>`3`<br>`4` |
| [`slot`](../Reference_and_Meta/Enums.md#enum-slot) | Enum / Integer  | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 14 | `0`<br>`1`<br>`2` |
| `temporary` | Boolean | If true, the crafted item is temporary and will be removed after the battle or a set duration. | 4 | `false` |
| `works_with_tech` | Boolean | If true, the craft effect is compatible with tech-based interactions or abilities. | 4 | `true` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |


### Object: `Counterspell`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |


### Object: `CopySpells`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 1 | `true` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |


### Object: `ConstitutionUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Reference_and_Meta/Enums.md#enum-tooltip_stackless) | Enum   | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks_neg`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_neg) | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. | 1 | `"KEYWORD_ALLSTATSDOWN_DESC"`<br>`"KEYWORD_CHADOWN_DESC"`<br>`"KEYWORD_CONDOWN_DESC"` |
| [`name_stacks_neg`](../Assets_and_Localization/Strings.md#string-name_stacks_neg) | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. | 1 | `"KEYWORD_ALLSTATSDOWN_NAME"`<br>`"KEYWORD_CHADOWN_NAME"`<br>`"KEYWORD_CONDOWN_NAME"` |
| [`tooltip_stacks_pos`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_pos) | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. | 1 | `"KEYWORD_ALLSTATSUP_DESC"`<br>`"KEYWORD_CHAUP_DESC"`<br>`"KEYWORD_CONUP_DESC"` |


### Object: `Conditional_Shielded`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cleave`](./Engine_StatusAndPassiveKeys.md#object-cleave) | Integer / Object  | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 2 | `{ . . . }`<br>`1` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`2`<br>`3` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 1 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`SetItemAux`](./Engine_StatusAndPassiveKeys.md#object-setitemaux) | Object  | Configures an item's auxiliary value by specifying a target slot and a formula for the new value. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |


### Object: `Conditional_PartyMember`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 3 | Default<br>FormChange<br>Druid |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `1`<br>`2`<br>`3` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |


### Object: `Conditional_NotBoss`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 3 | Default<br>FormChange<br>Druid |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 2 | `1`<br>`2`<br>`3` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>tag |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 1 | `1` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |


### Object: `Conditional_ManaThreshold`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RepairTrinket` | Integer | The number of stacks of the Repair Trinket status effect to apply. | 1 | `1`<br>`99` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |


### Object: `Conditional_HealthThreshold`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 7 | Default<br>FormChange<br>Druid |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>tag |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 1 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 1 | `25`<br>`50`<br>`999` |
| [`Die`](../Reference_and_Meta/Miscellaneous.md#object-die) | Integer / Object  | If set, kills the target immediately. | 1 | `{ . . . }`<br>`1`<br>`6` |
| `FlatLeech` | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. | 1 | `1`<br>`10`<br>`2` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |


### Object: `Conditional_HasTag`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 46 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 41 | Default<br>FormChange<br>Druid |
| [`ImmediateUseAbility`](./Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 3 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Die`](../Reference_and_Meta/Miscellaneous.md#object-die) | Integer / Object  | If set, kills the target immediately. | 2 | `{ . . . }`<br>`1`<br>`6` |
| [`ChangeTilesUnder`](../Reference_and_Meta/Enums.md#enum-changetilesunder) | Enum  | The tile type to change the ground tiles under the target to. | 2 | `DirtTile`<br>`GlassTile`<br>`LavaTile` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 1 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`UseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. | 1 | `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 1 | `25`<br>`50`<br>`999` |
| [`PopAndSpawn`](../Reference_and_Meta/Miscellaneous.md#object-popandspawn) | Enum / Object  | The object (enemy or entity) to spawn on the target's tile, optionally with visual effects. | 1 | `{ . . . }`<br>`Sprout`<br>`StemCat_HalfHealth`<br>`TheDestroyer` |
| `EventBounty` | Integer | The number of stacks of Event Bounty applied, increasing event rewards. | 1 | `5` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |


### Object: `Conditional_HasStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 20 | passives<br>class<br>tag |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 6 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 5 | Default<br>FormChange<br>Druid |
| [`Burn`](../Reference_and_Meta/Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 2 | `1`<br>`10`<br>`2` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| [`Confusion`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 2 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Slow`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 2 | `{ . . . }`<br>`-1`<br>`1`<br>`2` |
| [`FormChange`](./Engine_StatusAndPassiveKeys.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 1 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`Quivered`](../Reference_and_Meta/Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`5` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |


### Object: `Conditional_HasCleansableDebuffs`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| [`RandomStatusFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 1 | `{ . . . }` |
| [`VisualFX`](../Reference_and_Meta/Enums.md#enum-visualfx) | Enum  | Specifies the name of the visual effect to play. | 1 | `BigMagicMissileBlast`<br>`Bolt`<br>`Cleanse` |
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. | 1 | `1`<br>`9999` |
| `GenericBuff` | Integer | A generic buff value applied to the unit. | 1 | `100`<br>`5` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |


### Object: `Conditional_GoodRoll`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 37 | `.1`<br>`.16666666`<br>`.3` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 37 | Default<br>FormChange<br>Druid |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 14 | passives<br>class<br>tag |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 6 | `1`<br>`2`<br>`[1 .01]` |
| [`FindItemFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 5 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`ForceUseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 3 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `RandomMutation` | Integer | The number of random mutations to apply. | 3 | `1`<br>`3` |
| [`ImmediateUseAbility`](./Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 1 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| [`ChangeTilesUnder`](../Reference_and_Meta/Enums.md#enum-changetilesunder) | Enum  | The tile type to change the ground tiles under the target to. | 1 | `DirtTile`<br>`GlassTile`<br>`LavaTile` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |


### Object: `Conditional_FirstApplicationThisTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 3 | Default<br>FormChange<br>Druid |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `Charge` | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 1 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. | 1 | `1`<br>`[1 .10]`<br>`[1 .25]` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |


### Object: `Conditional_Enemy`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 9 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | passives<br>class<br>tag |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 7 | Default<br>FormChange<br>Druid |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| [`Weakness`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-weakness) | Array / Integer / Object  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Madness`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `Attraction` | Integer | The number of stacks of Attraction applied, drawing enemy units toward the target. | 2 | `1` |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`Burn`](../Reference_and_Meta/Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 1 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`Marked`](./Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 1 | `{ . . . }`<br>`1`<br>`3`<br>`5` |
| [`Leeches`](./Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object  | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. | 1 | `-1`<br>`1`<br>`2` |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 1 | `1`<br>`2`<br>`3` |
| `Hex` | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. | 1 | `1` |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 1 | `1` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |


### Object: `Conditional_Corpse`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Revive`](./Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object  | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 7 | `{ . . . }`<br>`1`<br>`100%`<br>`50%` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>tag |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `1`<br>`2`<br>`3` |
| [`SafeDoomed`](../Reference_and_Meta/Enums.md#enum-safedoomed) | Enum / Integer  | The number of SafeDoomed stacks applied, or 'level' to scale with character level. | 2 | `1`<br>`2`<br>`level` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| [`Madness`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `RandomMutation` | Integer | The number of random mutations to apply. | 1 | `1`<br>`3` |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 1 | `1` |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. | 1 | `1` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |


### Object: `Conditional_Boss`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 6 | Default<br>FormChange<br>Druid |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`2`<br>`3` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>tag |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `1`<br>`2`<br>`3` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 2 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| `Drowsy` | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`8` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |


### Object: `Conditional_BadRoll`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 8 | `.1`<br>`.16666666`<br>`.3` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 8 | Default<br>FormChange<br>Druid |
| [`Madness`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 1 | `25`<br>`50`<br>`999` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |


### Object: `Conditional_Ally`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 17 | passives<br>class<br>tag |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 5 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 4 | Default<br>FormChange<br>Druid |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | `-1`<br>`-2`<br>`1` |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 3 | `{ . . . }`<br>`0`<br>`1` |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `HealthGain` | Integer | The amount of health restored to the source. | 2 | `1`<br>`10`<br>`2` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `TempSpeedUp` | Enum / Integer | The number of stacks of temporary Speed Up applied to the unit. | 2 | `10`<br>`4`<br>`X` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 1 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. | 1 | `-1`<br>`1`<br>`2` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |


### Object: `Conditional_Adjacent`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | passives<br>class<br>tag |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`10`<br>`2` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 2 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 2 | Default<br>FormChange<br>Druid |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 0 | `{ . . . }` |


### Object: `CollectsPickupsWithAltEffects`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 3 | `{ . . . }` |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | `1`<br>`3` |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | `-1`<br>`-2`<br>`-4` |
| [`Quivered`](../Reference_and_Meta/Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`5` |
| `CurrentWeaponAddPoison` | Integer | The number of poison stacks added to the target's current weapon; an integer value applies that many stacks. | 1 | `1` |


### Object: `CockroachSwarm`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |


### Object: `Cleave`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `icon_frame` | Number | The sprite frame index for the buff icon. | 1 | `141`<br>`148`<br>`149` |


### Object: `Cleanse`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |


### Object: `Charmed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |


### Object: `CharismaUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Reference_and_Meta/Enums.md#enum-tooltip_stackless) | Enum   | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks_neg`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_neg) | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. | 1 | `"KEYWORD_ALLSTATSDOWN_DESC"`<br>`"KEYWORD_CHADOWN_DESC"`<br>`"KEYWORD_CONDOWN_DESC"` |
| [`name_stacks_neg`](../Assets_and_Localization/Strings.md#string-name_stacks_neg) | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. | 1 | `"KEYWORD_ALLSTATSDOWN_NAME"`<br>`"KEYWORD_CHADOWN_NAME"`<br>`"KEYWORD_CONDOWN_NAME"` |
| [`tooltip_stacks_pos`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_pos) | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. | 1 | `"KEYWORD_ALLSTATSUP_DESC"`<br>`"KEYWORD_CHAUP_DESC"`<br>`"KEYWORD_CONUP_DESC"` |


### Object: `ChargeFists`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| [`keyword_tooltips`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 1 | `{ . . . }` |
| [`tooltip_stacks_singular`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_singular) | String | The localization key for the singular form of the stack count in the tooltip. | 1 | `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |


### Object: `ChangeTile`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tile`](../Reference_and_Meta/Arrays.md#array-tile) | Array / Enum  | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 12 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |
| `aoe` | Integer | The radius (in tiles) of the area affected by the tile change. | 2 | `1` |


### Object: `ChanceToBreakFree`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 11 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`fail_ability`](../Reference_and_Meta/Enums.md#enum-fail_ability) | Enum | Specifies the ability to be used when the parent condition (e.g., breaking free) fails. | 3 | `CHuskDropFail`<br>`LennyStruggleFail`<br>`XXX` |


### Object: `ChampionUpgradeNextMinion`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `CatPartsSizeScaleStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 1 | `-1`<br>`-2`<br>`1` |
| `arm2` | Number | The catalog ID for the cat's second arm part. | 1 | `-1`<br>`-2`<br>`1` |
| `body` | Float | The catalog ID for the cat's body part. | 1 | `-1`<br>`1`<br>`1.1` |
| `arm1` | Number | The catalog ID for the cat's first arm part. | 1 | `-1`<br>`-2`<br>`1` |


### Object: `CastAgainWithStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `OverrideDamage` | Integer | Overrides the damage of the current action to this flat value (can be negative to heal). | 1 | `-10`<br>`0`<br>`1` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |


### Object: `CanApplyToInanimate`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](./Engine_StatusAndPassiveKeys.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 10 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 5 | `{ . . . }` |
| [`BreakIntoRocks`](../Reference_and_Meta/Enums.md#enum-breakintorocks) | Enum | Specifies the type of rock (e.g., 'Coin', 'SmallRock') to spawn when breaking an inanimate object. | 4 | `Coin`<br>`SmallRock` |
| [`ApplyToSource`](./Engine_StatusAndPassiveKeys.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 3 | `{ . . . }` |
| `Vaporize` | Integer | Removes the target from play, preventing its corpse from being interacted with. | 3 | `1`<br>`20` |
| `GetAggroTarget` | Integer | The number of aggro targets to acquire. | 2 | `1` |
| [`Temporary`](./Engine_StatusAndPassiveKeys.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 1 | `{ . . . }` |
| `PreventDeathTransforms` | Integer | Number of death transforms prevented for non-boss characters. | 1 | `1` |


### Object: `ButterflySwarm`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |


### Object: `Bounty`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `BounceObject`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`obj`](../Reference_and_Meta/Arrays.md#array-obj) | Array / Enum  | Specifies one or more object names to bounce towards the target. | 3 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |
| `slide` | Integer | The number of tiles the bounced object slides toward the target. | 1 | `10` |


### Object: `BombRatTurtle`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `BodyGuard`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Bloodzerked`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 1 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `BlessingOfPeace`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 1 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |


### Object: `ArcLightning`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 4 | `false`<br>`true` |
| `max_distance` | Integer | The maximum range in tiles for the arc lightning to chain to subsequent targets. | 4 | `1`<br>`2`<br>`3` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| `ignore_self` | Boolean | If true, the arc lightning effect does not chain to or affect the source unit itself. | 1 | `true` |


### Object: `ApplyToTile`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ObjectOnHit`](./Engine_StatusAndPassiveKeys.md#object-objectonhit) | Enum / Object | Specifies the object to spawn on the hit tile. | 2 | `{ . . . }`<br>`Bait`<br>`BiggestFood`<br>`Carcus` |
| `SpawnBearTrap` | Integer | If non-zero, spawns a bear trap on the tile. | 2 | `1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 2 | `{ . . . }` |


### Object: `ApplyToSource`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 20 | `{ . . . }` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 6 | `-1`<br>`-2`<br>`1` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 6 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `HealthGain` | Integer | The amount of health restored to the source. | 6 | `1`<br>`10`<br>`2` |
| `Shield` | Enum / Equation | The amount of shield granted to the source, absorbing incoming damage. | 5 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`FormChange`](./Engine_StatusAndPassiveKeys.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 4 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`EvolveAbilityFromPool`](../Reference_and_Meta/Miscellaneous.md#object-evolveabilityfrompool) | Enum / Object  | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. | 4 | `{ . . . }`<br>`Butcher`<br>`Druid`<br>`Fighter` |
| [`ConstitutionUp`](../Reference_and_Meta/Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 3 | `-1`<br>`-2`<br>`1` |
| `AddWeaponAux` | Equation | The amount or expression to add to the source's weapon auxiliary stat. | 3 | `"-max(min(X+1, item_aux), 0)"`<br>`-item_aux`<br>`1` |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 2 | `{ . . . }`<br>`0`<br>`1` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |
| `Charge` | Equation | The number of charge stacks applied. | 2 | `1`<br>`2`<br>`3` |
| [`FindItemFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 2 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| `FreeSpell` | Integer | The number of stacks of Free Spell applied to the source, allowing the next spells to be cast without mana cost. | 2 | `1`<br>`2` |
| [`EquipPermanentItem`](../Reference_and_Meta/Enums.md#enum-equippermanentitem) | Enum  | The name of the item to permanently equip to the source. | 2 | `BoneClub`<br>`Kidney` |
| [`Brace`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Bruise`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| [`DivineShield`](../Reference_and_Meta/Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | `1`<br>`2`<br>`3` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 1 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`ForceUseAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`[1, 0.1]` |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 1 | `1`<br>`3` |
| [`GainCoinsRange`](./Engine_StatusAndPassiveKeys.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 1 | `{ . . . }` |
| [`FindItem`](../Reference_and_Meta/Enums.md#enum-finditem) | Enum  | The name of the specific item to find and add to the source's inventory. | 1 | `BoneClub`<br>`Molars`<br>`Pearl` |


### Object: `ApplyToRandomPartyMemberIfPossible`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`GainDisorderFromPool`](./Engine_StatusAndPassiveKeys.md#object-gaindisorderfrompool) | Enum / Object  | Specifies a pool of disorders from which one is randomly gained on basic attack, with an optional chance. | 2 | `{ . . . }`<br>`all_disorders` |


### Object: `ApplyToRandomClosestAlly`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveTowards` | Integer | The number of tiles to force the target to move toward the caster. | 1 | `1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `ApplyToOthersWithSharedTagAndFaction`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Marked`](./Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 1 | `{ . . . }`<br>`1`<br>`3`<br>`5` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `ApplyToConsumed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DeleteObject` | Integer | If set, deletes the target object from the map. | 3 | `1` |
| [`Die`](../Reference_and_Meta/Miscellaneous.md#object-die) | Integer / Object  | If set, kills the target immediately. | 1 | `{ . . . }`<br>`1`<br>`6` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `ApplyStatusesNextTurnBegin`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Quivered`](../Reference_and_Meta/Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`5` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |


### Object: `ApplyPassivesToSpawnerWhileAlive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`HideEquipment`](../Reference_and_Meta/Enums.md#enum-hideequipment) | Enum  | Specifies which equipment slot is visually hidden. | 1 | `neck` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |


### Object: `ApplyMultipleTimes`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>tag |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`RandomStatusFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 3 | `{ . . . }` |


### Object: `AlphaStatusOnTurnBegin`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DoubleCastSpellThisTurn` | Integer | If non-zero, grants the unit a double cast effect for spells this turn. | 1 | `1` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |


### Object: `AlphaDodgeChance`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](../Reference_and_Meta/Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. | 1 | `AllStatsUp`<br>`Brace`<br>`Brittle` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `Adrenaline`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](../Reference_and_Meta/Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. | 1 | `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `AddTilesetObjects`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FloatingDebris`](../Reference_and_Meta/Miscellaneous.md#object-floatingdebris) | Object | An object defining parameters for spawning floating debris tileset objects. | 1 | `{ . . . }` |


### Object: `AddPostProcessEffect`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `requires_framebuffer` | Boolean | If true, the post-process effect requires a framebuffer to be active. | 1 | `false` |
| [`shader`](../Reference_and_Meta/Enums.md#enum-shader) | Enum | Specifies which shader to use for the post-process effect. | 1 | `shimmervignette` |


### Object: `AcidRain`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`render_mode`](../Reference_and_Meta/Enums.md#enum-render_mode) | Enum   | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `particle_lifetime` | Float | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| [`simulation_space`](../Reference_and_Meta/Enums.md#enum-simulation_space) | Enum   | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| [`projection_matrix`](../Reference_and_Meta/Enums.md#enum-projection_matrix) | Enum   | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `speed_start` | Float | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`scripts`](../Reference_and_Meta/Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| `size_start` | String | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| `speed_scale` | String | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| [`force`](../Reference_and_Meta/Arrays.md#array-force) | Array  | The force vector applied to particles. | 1 | `0`<br>`1`<br>`1.5` |
| `alpha` | String | The alpha transparency value for the particle system (e.g., '0.03'). | 1 | `.005`<br>`.01`<br>`.03` |
| `chain` | Boolean | Specifies the ability to chain into and execute. | 1 | `AcidSplash`<br>`CaveSplash`<br>`FireFullSmall` |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |

